# How to Operate — L_WORLDSIM
**Platform:** Anticloud | **IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg

## Module Overview
L_WORLDSIM — WorldSim: sovereign world simulation for training and testing Anticloud embodied AI
Stack: Python 3.11, PyTorch 2.10+, K_HELIX, K_DREAMER4, PAX 27B, AIOSS_FORMAT

## Daily Operations
1. `aioss verify --chain ./l_worldsim.aioss`
2. Check service health via api-oss-monitor
3. Review api-oss-logging for error-level events
4. Confirm PAX 27B is loaded and responding

## Incident Response
- Chain tamper: halt, notify compliance, restore from backup
- GPU OOM: reduce batch size, check memory leak
- High latency >2s P99: check queue depth, scale workers
- Compliance gap: run api-oss-compliance report

## Backup (nightly)
```bash
python -m api_oss_backup backup --sources ./l_worldsim.aioss --output ./backups/
```
