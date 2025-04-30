# Gymnastics Lineup Simulator 🇺🇸

This project predicts and optimizes the best possible lineup for Team USA in the 2024 Women's Artistic Gymnastics Olympics. Using competition data from Tokyo 2021, World Championships, and other major events (2022–2023), we simulate thousands of potential team combinations to find the lineup that maximizes expected medal counts.

---

## Project Overview

- **Goal**: Select the optimal USA women's gymnastics team lineup to maximize medal counts (gold → silver → bronze).
- **Data Sources**:
  - Tokyo 2021 Olympic results
  - 2022–2023 international competition results (Worlds, Euros, etc.)
- **Methods**:
  - Data cleaning and standardization
  - Score prediction using Linear Regression (based on historical performance)
  - Monte Carlo simulation (2000 runs per lineup)
  - Rule-based selection (5-4-3 qualification, 5-3-3 team final, AA & event finals)

---

## Modeling

- **Models evaluated**:
  - Linear Regression (selected for final use)
  - Random Forest Regressor
  - Baseline (mean prediction)
- **Key features**: apparatus, event round, location, days before event, gymnast's average historical score

---

## Simulation Process

1. Fix rosters of competing countries
2. Predict gymnast scores by event & round (with added noise)
3. Simulate qualification, team final, all-around, and event finals
4. Track medal outcomes across 2000+ simulations
5. Rank team combinations by average medals

---

## Results

- The optimal lineup closely matches the real 2024 Team USA selections.
- On average:
  - 🥇 Gold: ~3 medals
  - 🥈 Silver: ~2 medals
  - 🥉 Bronze: ~1.5 medals
- Vault and Team Final are USA's strongest events.

---

## Future Outlook

- Integrate more granular scoring (D-score, E-score, penalties)
- Include rising talents not present in 2023 data
- Extend to other countries and 2028 Olympics

---

## Author

**Jiapeng Wang** 

---

## Folder Structure

- `data/`      # Raw and cleaned competition datasets
- `code/`    # Modeling and simulation scripts
- `docs/`       # Technical report and presentation slides



