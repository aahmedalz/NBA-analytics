# NBA Scoring, Three-Point Volume, and MVP Voting (2003–2022)

This project analyzes how the NBA evolved from 2003–2022 with pace-and-space and the three-point revolution. I quantify:
1) Scoring across eras, 2) whether high-volume 3PA shooters maintain efficiency, and 3) how MVP vote share tracks a simple box composite (PTS/AST/TRB).

## Dataset
Kaggle: NBA player data from 2003–2022. *(Add exact Kaggle link or citation.)*

## Research Questions
- RQ1: Did average PPG increase post-2015 vs 2003–2015?
- RQ2: Do players with ≥6 3PA/G maintain equal or better eFG%?
- RQ3: How strongly does MVP vote share correlate with a simple PTS/AST/TRB composite?

## Methods (short)
- Filtered seasons; minutes floor (MP ≥ 12) for stability.
- eFG% compared across 3PA volume groups (<6 vs ≥6 3PA/G).
- Standardized PTS/AST/TRB (z-scores) and summed for a simple box composite.
- Correlated composite with MVP vote share on seasons above a minimal share threshold.

## Results (key numbers)
- **RQ1 – Scoring rose:** Avg PPG increased from **8.55** (2003–2015) to **9.17** (2015–2022), ~**+0.70 PPG** per player.
- **RQ2 – High-volume 3PA stayed efficient (or better):** mean eFG% **0.528** (≥6 3PA/G) vs **0.499** (<6); median **0.527** vs **0.497**.
- **RQ3 – MVP vs box composite:** correlation **r ≈ 0.41** (moderate positive).

## Conclusion
From 2003–2022: **scoring increased**, **high-volume 3-point shooters stayed efficient (or better)**, and **a basic box composite moderately predicts MVP voting**.

## Reproducibility
- 
otebooks/01_analysis.ipynb runs end-to-end.
- Put the dataset under data/ (path used in the notebook).
- Python deps: see equirements.txt.

## Figures
- igures/ppg_by_year.png
- igures/efg_by_3pa_group.png
- igures/mvp_vs_box_scatter.png

## Next Ideas
- Add BLK/STL; try alternative weights (e.g., assists > points).
- Regularized regression for MVP share prediction.
- Era adjustments (pace, league-avg eFG% normalization).

## License
MIT
