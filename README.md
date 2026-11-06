# Applied Data Science Capstone — SpaceX Falcon 9 First-Stage Landing Prediction

IBM Applied Data Science Capstone (Course 5). This project predicts whether the SpaceX Falcon 9 first stage will land successfully, so the cost of a launch can be estimated.

## Final report

- **Project report (PDF, 17 slides):** [Data_Science_Capstone_Report_17slides.pdf](Data_Science_Capstone_Report_17slides.pdf)
- **Interactive slide deck (GitHub Pages):** https://sadmanjarif.github.io/applied-data-science-capstone/capstone_slides.html
- **Slide deck source:** [capstone_slides.html](capstone_slides.html)

## What was done

- **Data collection:** SpaceX REST API (`api.spacexdata.com/v4/launches/past`) and web scraping of Wikipedia's "List of Falcon 9 and Falcon Heavy launches" — 90 Falcon 9 launches, 2010–2020.
- **Data wrangling:** cleaned the data, handled missing `LandingPad` values (26 of 90), created the binary target `Class` (1 = successful landing), one-hot encoded Orbit, LaunchSite, LandingPad and Serial (80 feature columns).
- **Exploratory data analysis:** data visualization (scatter, bar and line charts) and SQL (SQLite, `spacex.csv`, 101 rows).
- **Interactive visual analytics:** Folium launch-site map and a Plotly Dash dashboard (site dropdown, success pie chart, payload range slider, payload vs. outcome scatter).
- **Predictive analysis:** Logistic Regression, SVM, Decision Tree and KNN on an 80/20 train–test split (18 test records).

## Key results

- Overall first-stage landing success rate: **66.7%** (60 of 90).
- Success rose from 0% in 2010–2013 to **90.0% in 2019** and 84.2% in 2020.
- Best launch site: KSC LC 39A (**77.3%**); best orbits: VLEO 85.7%, SSO 100%; hardest major orbit: GTO 51.9%.
- Best model: **Decision Tree, 94.44% test accuracy** (17 of 18 correct; confusion matrix [[5, 1], [0, 12]]). Logistic Regression 83.33%, SVM (sigmoid) 83.33%, KNN 66.67%.

## Course grade

IBM Applied Data Science Specialization, Course 5 (Applied Data Science Capstone) — **100% overall**. All six quizzes/assignments scored 100% and the final AI-graded submission scored 15/15.
