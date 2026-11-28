# MSFT Submission Status and Handoff

The active submission target is **MSFT only**. The project configuration and stock-analysis notebooks now point to MSFT; cached outputs from earlier analyses have been cleared so they cannot be mistaken for MSFT results.

## Changes made

- Set `TARGET_TICKER = "MSFT"` in `tslab/config.py`.
- Renamed the two ticker-specific introductory notebooks to `1_market_data_and_candlesticks_MSFT.ipynb` and `2_stationarity_and_returns_MSFT.ipynb` and updated their content to MSFT.
- Updated the stock-specific references in the four in-scope MSFT notebooks (1–4) and cleared cached execution outputs in those notebooks.
- Changed the lab submission form to MSFT and added the four supplied member names/IDs with proposed task allocations. These are clearly marked as drafts requiring each member's confirmation; personal learning statements are not invented.

## Forecast file and analysis status

The user-provided `forecast_clean.csv` has been added as `data/forecast_basic.csv`. It has the required columns (`date`, `forecast`, `lower`, `upper`) and 63 rows from **2026-11-26 through 2027-02-22**. Its first forecast value ($490.24) is close to the user-provided MSFT close-history file's last close ($489.93 on 2026-11-25), so the forecast dates and starting level appear aligned. The close-history upload itself is not the checked-in OHLCV dataset and contains only a Close field; the repo's `target_MSFT.csv` currently ends on **2026-11-09**. Confirm the forecast source/model and include the corresponding history snapshot if the team intends to use that later cutoff.

The notebook outputs were cleared rather than relabeled from another ticker. MSFT stationarity, walk-forward metrics, DM tests, and any other numerical claims still need to come from rerunning the four in-scope notebooks. The forecast CSV alone does not establish those results.

## Remaining team actions

1. Work only through the four in-scope MSFT notebooks: 1, 2, 3, and 4. Run each from a fresh kernel with the MSFT configuration.
2. Record the data download date, data-quality findings, stationarity tests, walk-forward metrics, and DM tests from that MSFT run.
3. Confirm that the forecast CSV came from the team's MSFT model run and maintain a consistent data snapshot across the analysis and forecast.
4. Confirm whether Power BI is required in addition to the four notebooks; validate the existing MSFT report only if in scope.
5. Each team member must verify/edit their contribution draft and learning reflection. The team name is now recorded as **B6**.
6. Run `python -m pytest tests` after installing `requirements/dev.txt` in the course-supported Python environment.

Do not present old cached notebook figures as validated MSFT results until the four in-scope notebooks have been rerun.
