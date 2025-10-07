# Consensus Model Scoring Matrix (Quantitative Assessment)

## Abstract
The matrix presents normalized scores for candidate consensus models across critical dimensions. Scores are derived from weighted criteria: Safety (30%), Liveness (20%), Performance (20%), Operational Complexity (15%), Regulatory Alignment (15%).

| Model | Safety (0-10) | Liveness (0-10) | Performance (0-10) | Operational Complexity (0-10, lower better) | Regulatory Alignment (0-10) | Weighted Score |
|-------|---------------|-----------------|--------------------|---------------------------------------------|-----------------------------|----------------|
| HotStuff | 9 | 8 | 8 | 6 | 8 | 8.05 |
| HoneyBadgerBFT | 10 | 9 | 5 | 7 | 6 | 7.75 |
| Algorand | 8 | 8 | 8 | 6 | 8 | 7.90 |
| Ouroboros Praos | 8 | 7 | 7 | 5 | 8 | 7.65 |
| Avalanche | 7 | 8 | 9 | 7 | 6 | 7.45 |
| BABE + GRANDPA | 8 | 8 | 8 | 6 | 8 | 7.85 |
| Hybrid HotStuff + HoneyBadger | 9 | 9 | 8 | 8 | 7 | 7.95 |

## Interpretation
- **HotStuff** scores highest due to balanced safety, performance, and manageable complexity.
- **HoneyBadgerBFT** excels in safety/liveness but penalized for performance overhead.
- **Hybrid approach** offers strong guarantees but introduces operational complexity necessitating advanced automation.

## Methodology Notes
- Operational complexity score inverted before weighting (10 - score) to reward lower complexity.
- Weighted score computed as Σ(weight_i × normalized_score_i).
- Data sources include simulation benchmarks, peer-reviewed literature, and internal engineering assessments.
