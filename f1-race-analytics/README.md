# F1 Race Analytics

A Formula 1 data analytics project covering season points, driver performance, race reliability, tyres and circuit types.

This edition includes a static project website and a development report. The frontend uses an ivory and navy palette with blue accents, a circuit illustration, and nine cards introducing the analysis topics.

## Project overview

The analytical questions focus on how team points vary across seasons, how driver totals compare, and how non-finishes are distributed across race conditions. The website introduces these questions and the measures used to explore them.

[Read the project report](docs/project-report.md) · [GitHub repository](https://github.com/amanpawar182006-glitch/F1-Race-analysis)

## Dataset

The supplied project documentation describes `F1 Racing Project Dataset.xlsx`, with five sheets:

- `race_results`
- `circuits`
- `championship_standings`
- `lap_intelligence`
- `qualifying_results`

The documented analysis uses `race_results`, described as containing 6,464 result records with Season values from 2010 to 2026. These figures come from the supplied documentation; the source Excel file is not included in this repository.

## Analysis topics

| Topic | Measure and grouping |
|---|---|
| Team points by season | Sum of points by season and team |
| Driver points leaderboard | Sum of points by driver |
| Non-finishes by reason | Sum of the 0/1 DNF flag by reason |
| DNF rate by weather | Average DNF flag by weather category |
| Team points leaderboard | Sum of points by team |
| Positions gained by team | Average positions gained |
| Starting compound mix | Count of result records by starting compound |
| Points by circuit type | Sum of points by circuit category |
| Finish position by team | Average valid finish position |

These are descriptions of the analytical views. The website itself displays project information rather than live charts. External visualization links and embedded views are not configured in this edition.

## Run locally

Open `index.html` in a browser. The website uses HTML, CSS and an inline SVG illustration, with no dependencies or build step. Fonts use the system's installed font stack.

## GitHub Pages

The repository includes `.github/workflows/pages.yml`. After uploading the files to a repository's `main` branch, choose **GitHub Actions** in **Settings → Pages → Build and deployment → Source**.

A push to `main` starts the deployment workflow. The published address is provided by the repository's Pages settings after deployment succeeds. Expected website after deployment: https://amanpawar182006-glitch.github.io/F1-Race-analysis/. Deployment has not yet been verified for this copy.

## Files

```text
.
├── .github/workflows/pages.yml
├── docs/project-report.md
├── .gitignore
├── .nojekyll
├── index.html
├── styles.css
└── README.md
```

## Interpretation

Result records are not counts of separate Grand Prix events. Points totals describe the supplied records and are not independently verified career statistics. Weather and tyre comparisons are descriptive; they do not establish causes or identify an optimal strategy. Average finish positions depend on the records with valid finishing values.

The source workbook and Tableau workbook are not included. Data validation, workbook filters, Story scene counts and rendering performance should be documented from the actual workbook before claiming those items have been verified.
