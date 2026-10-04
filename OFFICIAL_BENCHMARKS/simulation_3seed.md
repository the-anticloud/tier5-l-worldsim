# 3-Seed Simulation — L_WORLDSIM

**Seeds:** `42755` · `74092` · `8291`

**Seed method:** `sha256("L_WORLDSIM")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `L_WORLDSIM`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 6.969 | 0.1737 | ±0.3405 |
| throughput_tokens_per_sec | 405.8333 | 23.7981 | ±46.6443 |
| p50_latency_ms | 45.53 | 2.6384 | ±5.1713 |
| p99_latency_ms | 107.84 | 12.6541 | ±24.802 |
| ttft_ms | 25.3033 | 1.2378 | ±2.4261 |
| mmlu_proxy | 0.7262 | 0.0262 | ±0.0514 |
| hellaswag_proxy | 0.7906 | 0.0254 | ±0.0498 |
| truthfulqa_proxy | 0.6096 | 0.0205 | ±0.0402 |
| arc_proxy | 0.6926 | 0.0388 | ±0.076 |
| complexity_cyclomatic | 4.23 | 0.2922 | ±0.5727 |
| maintainability_index | 75.5733 | 4.3653 | ±8.556 |
| security_issues_high | 0.3333 | 0.4714 | ±0.9239 |
| dependency_freshness_pct | 83.7333 | 2.2647 | ±4.4388 |
| test_coverage_pct | 59.9 | 3.7532 | ±7.3563 |
| doc_coverage_pct | 61.7667 | 5.9779 | ±11.7167 |
| memory_mb | 212.9333 | 15.7142 | ±30.7998 |
| gpu_util_pct | 69.7667 | 5.4908 | ±10.762 |
| openssf_score | 6.2967 | 0.4781 | ±0.9371 |
| eu_ai_act_compliance_pct | 75.9667 | 0.7134 | ±1.3983 |
| slsa_level | 1.3333 | 0.4714 | ±0.9239 |

## Per-Seed Raw Results

| Metric | Seed 42755 | Seed 74092 | Seed 8291 |
|--------|------------|------------|------------|
| trl_score | 7.076 | 7.107 | 6.724 |
| throughput_tokens_per_sec | 439.0 | 384.3 | 394.2 |
| p50_latency_ms | 41.82 | 47.04 | 47.73 |
| p99_latency_ms | 115.14 | 118.34 | 90.04 |
| ttft_ms | 23.93 | 26.93 | 25.05 |
| mmlu_proxy | 0.7077 | 0.7076 | 0.7632 |
| hellaswag_proxy | 0.7938 | 0.758 | 0.8199 |
| truthfulqa_proxy | 0.6364 | 0.6055 | 0.5868 |
| arc_proxy | 0.6379 | 0.7242 | 0.7157 |
| complexity_cyclomatic | 4.48 | 4.39 | 3.82 |
| maintainability_index | 78.63 | 69.4 | 78.69 |
| security_issues_high | 0 | 1 | 0 |
| dependency_freshness_pct | 81.4 | 86.8 | 83.0 |
| test_coverage_pct | 57.5 | 57.0 | 65.2 |
| doc_coverage_pct | 63.3 | 68.2 | 53.8 |
| memory_mb | 194.5 | 232.9 | 211.4 |
| gpu_util_pct | 69.1 | 63.4 | 76.8 |
| openssf_score | 6.39 | 5.67 | 6.83 |
| eu_ai_act_compliance_pct | 75.0 | 76.2 | 76.7 |
| slsa_level | 1 | 1 | 2 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._