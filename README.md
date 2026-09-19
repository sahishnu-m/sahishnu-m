# Sahishnu's Project Profile

[![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)](https://github.com/sahishnu-m?tab=repositories&language=python)
[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit&logoColor=white)](https://streamlit.io)
[![Machine Learning](https://img.shields.io/badge/machine%20learning-1baf7a)](https://github.com/sahishnu-m/tennis-match-predictor)

I build data and machine learning projects that turn public data into answers
to specific questions, usually around sports and the Reno area. Each one ships
as a working app with the method and the numbers laid out, not just a result.

Each entry links to a live app and the code, except one hardware project that was never finished and has neither. Open **Preview** for a screenshot where one exists.

---

- [Tennis Match Predictor](https://github.com/sahishnu-m/tennis-match-predictor)
  - **[Try it live](https://tennis-match-predictor-model.streamlit.app/)** · [View the code](https://github.com/sahishnu-m/tennis-match-predictor)
  - Predicts the probability that one ATP player beats another.
  - Combines Elo ratings, serve and return stats, recent form, fatigue and head-to-head records from 26 years of match data, with every feature computed only from matches played before it. Tested on 10,382 matches from 2023 onward, never seen during training, where it picked the winner 66.5% of the time overall and 72.7% at Grand Slams.
  - Elo alone already reaches 65.5%; the added features are a real but modest gain, and the next step would be modelling surface transitions within a season rather than treating each match independently.
  - `Python` `XGBoost` `scikit-learn` `Streamlit`
  <details>
  <summary>Preview</summary>

  <img src="https://raw.githubusercontent.com/sahishnu-m/tennis-match-predictor/main/docs/app_screenshot.png" alt="Tennis Match Predictor app" width="600">

  </details>

---

- [School Start Times](https://github.com/sahishnu-m/school-start-times)
  - **[Try it live](https://school-start-time-impact.streamlit.app/)** · [View the code](https://github.com/sahishnu-m/school-start-times)
  - Tests whether high schools that start later show better academic results.
  - The main sample is 425 New York City high schools, chosen because the city publishes a start time for every school and all of them sit inside one school system, holding busing budgets, union contracts and state funding constant instead of letting them get tangled up with start time. Estimates are reported with poverty, size, English learners, disability, borough and admissions selectivity added one block at a time, with standard errors clustered on the school building. A second sample of 38 Nevada high schools is kept to show why the question is hard to study at all: 29 of them start at exactly 7:00 AM.
  - The finding is mostly null: graduation rate and attendance show nothing, while Advanced Regents diplomas move against later starts and college readiness moves with them, a pattern more consistent with residual confounding than a real effect.
  - `Python` `pandas` `numpy` `Streamlit` `matplotlib` `NYC Open Data`
  <details>
  <summary>Preview</summary>

  <img src="https://raw.githubusercontent.com/sahishnu-m/school-start-times/main/docs/app_screenshot.png" alt="School Start Times app" width="600">

  </details>

---

- [Menu Inflation Index](https://github.com/sahishnu-m/menu-inflation-index)
  - **[Try it live](https://menu-inflation-index.streamlit.app)** · [View the code](https://github.com/sahishnu-m/menu-inflation-index)
  - Measures what eating out costs in Reno and Sparks, month over month.
  - Menu prices from 20 restaurants across three price tiers are collected monthly and turned into a chained Laspeyres price index built on a fixed basket of dishes, so the number moves only when prices move, then compared against the BLS CPI series for food away from home. Matches items through renames and portion-size changes, so a drink shrinking from 16oz to 12oz at the same price reads as the increase it is. Scraping treats robots.txt as binding and records every site that declines; 16 of 20 currently permit it.
  - Real collection has not run long enough yet to replace the simulated demo data the dashboard shows by default; the next step is simply letting the monthly scrape accumulate months.
  - `Python` `SQLite` `BeautifulSoup` `Altair` `Streamlit` `BLS API`
  <details>
  <summary>Preview</summary>

  <img src="https://raw.githubusercontent.com/sahishnu-m/menu-inflation-index/main/docs/app_screenshot.png" alt="Menu Inflation Index app" width="600">

  </details>

---

- [Court Conditions](https://github.com/sahishnu-m/court-conditions)
  - **[Try it live](https://court-conditions.streamlit.app)** · [View the code](https://github.com/sahishnu-m/court-conditions)
  - Predicts whether outdoor tennis courts around Reno and Sparks are playable and free, at a given hour, across 9 public courts.
  - A rule-based score out of 100 shows its working for every deduction: recent rain on a drying curve, temperature bands, wind weighted toward gusts, daylight and lights, and an ice check that fires on cold combined with recent wet. A separate crowding model estimates how many courts will be open, kept apart from playability because the two often point in opposite directions.
  - The weights behind that score are my own judgment, not yet validated against observed conditions; the next step is logging real playability for a month and comparing it against what the model predicted.
  - `Python` `Streamlit` `pandas` `Altair` `Open-Meteo`
  <details>
  <summary>Preview</summary>

  <img src="https://raw.githubusercontent.com/sahishnu-m/court-conditions/main/docs/app_screenshot.png" alt="Court Conditions app" width="600">

  </details>

---

- [Titration Liquid Separation Automation](https://github.com/sahishnu-m/titration-automation)
  - [View the code](https://github.com/sahishnu-m/titration-automation)
  - Automates a manual step of titration: shaking two containers, swapping their positions, then controlling flow through a polarity-reversing ball valve, using three stepper motors, two solenoids, and a flow meter wired in only as a circuit check.
  - Built as a mechanical engineering research assistant at UNR under Prof. Menezes. Abandoned before the rig was fully assembled, so this repo is a post-mortem: the design, the original Arduino sketches, and the wiring and supply-voltage bug that looked like a software problem before it turned out not to be.
  - There is no live app, no photograph of the finished rig, and no performance data, since the project never reached a working state; the next step, if it were picked back up, would be verifying supply voltage against each actuator's spec before writing any more control code.
  - `Arduino` `C++` `Mechanical Engineering`

---

New projects are added here as I build them.
