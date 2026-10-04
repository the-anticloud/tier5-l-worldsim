# Deploy Guide — L_WORLDSIM
**Tier:** TIER_5_WORLD_NEURO_EMBODIED | **Stack:** Python 3.11, PyTorch 2.10+, K_HELIX, K_DREAMER4, PAX 27B, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, K_HELIX (CUDA required), K_DREAMER4 checkpoint, PAX 27B weights, A100 for large-scale sim.

## Environment
A100 80GB for large-scale parallel simulation. T4 for sequential episodes. 64GB RAM.

## AIOSS Integration
```bash
aioss init --module L_WORLDSIM --output ./l_worldsim.aioss
aioss append --chain ./l_worldsim.aioss --payload ./output.bin --module L_WORLDSIM
aioss verify --chain ./l_worldsim.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="L_WORLDSIM",
    aioss_chain="./L_WORLDSIM.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./L_WORLDSIM.aioss --verbose
python -m L_WORLDSIM.tests.smoke
```
