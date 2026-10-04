# Developer Cookbook — L_WORLDSIM
**Stack:** Python 3.11, PyTorch 2.10+, K_HELIX, K_DREAMER4, PAX 27B, AIOSS_FORMAT
**Domain:** WorldSim: sovereign world simulation for training and testing Anticloud embodied AI

## Language-configured simulation
```python
from l_worldsim import WorldSim

sim = WorldSim(
    physics_backend="k_helix",
    world_model="k_dreamer4",
    pax_model="./pax-27b-q4.gguf",
    aioss_chain="./worldsim.aioss"
)

# Natural language scenario configuration
scenario = sim.configure_from_language(
    "Simulate a warehouse robot sorting 50 packages of varying sizes and weights "
    "on conveyor belts with 10% random sensor noise",
    pax_model="./pax-27b-q4.gguf"
)

results = sim.run(scenario, n_episodes=1000, parallel=8)
print(f"Success rate: {results.success_rate:.2%}")
print(f"Mean time per episode: {results.mean_duration_s:.1f}s")
print(f"Chain: {results.chain_hash}")
```

## Mixed physics + dream episodes
```python
results = sim.run_hybrid(
    scenario, real_physics_fraction=0.3, dream_fraction=0.7
)
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
