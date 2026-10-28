<div align="center">

# 🏁 F1 Race Analytics

### Exploring Formula 1 through data

**Season trends · Driver performance · Race reliability · Tyre strategies**

### Explore the Project

🌐 **[Visit F1 Race Analytics](https://amanpawar182006-glitch.github.io/F1-Race-analysis/)**  
📖 **[Explore the Methodology](https://amanpawar182006-glitch.github.io/F1-Race-analysis/#methodology)**

A Data Analytics with Tableau course project supported by a responsive project website.

</div>

---

## About the project

F1 Race Analytics brings together questions about team points, driver rankings, race conditions and finishing positions. The analysis uses the course-supplied Formula 1 dataset to organise these comparisons into clear visual topics.

The website introduces the analysis, explains the measures used and provides project documentation. Its design uses an ivory background, navy text, blue accents and a circuit illustration.

## Dataset overview

The supplied project documentation describes the following dataset:

| Detail | Description |
|---|---|
| Source workbook | `F1 Racing Project Dataset.xlsx` |
| Main analysis sheet | `race_results` |
| Result records | 6,464 |
| Season values | 2010–2026 |
| Analysis topics | 9 |

The workbook also contains `circuits`, `championship_standings`, `lap_intelligence` and `qualifying_results`.

These figures reflect the supplied documentation. The Excel dataset and Tableau workbook are not included in this repository.

## Analysis topics

| # | Topic | What it examines |
|---:|---|---|
| 01 | Team Points by Season | Changes in recorded team points across seasons |
| 02 | Driver Points Leaderboard | Driver rankings based on summed points |
| 03 | Non-finishes by Reason | Recorded reasons for race non-finishes |
| 04 | DNF Rate by Weather | Proportion of DNF records within weather categories |
| 05 | Team Points Leaderboard | Comparison of constructor point totals |
| 06 | Average Positions Gained | Mean movement between starting and finishing positions |
| 07 | Starting Compound Mix | Frequency of recorded starting tyre compounds |
| 08 | Points by Circuit Type | Point totals across circuit categories |
| 09 | Average Finish Position | Mean valid finishing positions by team |

## Analytical approach

The project groups race-result records by season, driver, team and race conditions.

- **Points:** summed within each selected group.
- **Non-finishes:** counted using the DNF flag.
- **DNF rate:** calculated as the average of a validated 0/1 DNF flag.
- **Position measures:** compared using averages.
- **Starting compounds:** compared using record counts.

Season should be treated as a grouping dimension rather than a value to sum. Missing finish values also need to be considered when interpreting average finishing positions.

## Website features

- Responsive layouts for desktop and smaller screens.
- Nine cards explaining the analysis topics.
- Methodology and dataset-scope sections.
- Accessible navigation and reduced-motion support.
- HTML, CSS and an inline circuit illustration.
- No installation or build step required.

This website presents project information. Live charts and external visualization links are not configured in this edition.

## Tools used

| Tool | Purpose |
|---|---|
| Microsoft Excel | Source workbook |
| Tableau Public | Worksheet, dashboard and Story development |
| HTML5 | Website structure |
| CSS3 | Styling and responsive layouts |
| GitHub Actions | Deployment workflow |
| GitHub Pages | Static website hosting |

## Run locally

Download the repository and open `index.html` in a browser.

The website uses system fonts and does not require external libraries.

## Project structure

```text
.
├── .github/
│   └── workflows/
│       └── pages.yml
├── docs/
│   └── project-report.md
├── .gitignore
├── .nojekyll
├── index.html
├── styles.css
└── README.md
```

## Documentation

The detailed report in `docs/project-report.md` covers the problem statement, dataset scope, preparation approach, analytical views and limitations.

## Deployment

The included workflow publishes the website through GitHub Pages when changes are pushed to `main`.

In the repository settings, select **Pages → Source → GitHub Actions**. The final website address appears in Pages settings after a successful deployment.

## Reading the results

The analysis describes the supplied records. A result-record count is not a count of separate Grand Prix events, and point totals should not be treated as independently verified career statistics.

Weather and tyre comparisons show patterns within the data. They do not establish the causes of race outcomes or identify an optimal strategy.

---

<div align="center">

**F1 Race Analytics**  
Data Analytics with Tableau · Course Project

</div>
