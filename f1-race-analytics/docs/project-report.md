# F1 Race Analytics

## Project scope

F1 Race Analytics presents an overview of a Formula 1 analytics project. It introduces comparisons of season points, driver and team performance, reliability, starting tyres and circuit categories.

The repository contains the website and this report. The source Excel file and Tableau workbook are outside the package. This edition has no external visualization links or embedded views.

## Problem statement

A race-results sheet contains many records that are difficult to compare directly. The project organises the analysis around specific questions:

- How do recorded team points change across seasons?
- Which drivers and teams have higher points totals within the data?
- What reasons are recorded for non-finishes?
- How does the share of DNF records vary between weather categories?
- How do starting compounds, circuit types and position measures compare?

The intended audience is a student, course reviewer or reader interested in descriptive sports analysis. The aim is to make the chosen measures and their interpretation clear.

## Requirements and relevance

The analytical workflow covers data inspection, field preparation, appropriate aggregation, visual comparison and explanation of limitations. Tableau can be used to develop the worksheet views, combine them into a dashboard and arrange a sequence of Story scenes.

For classroom use, these comparisons provide examples of sorting, grouping, rates, averages and trend charts. Real team decisions would require independently validated data and more context than these summaries provide.

## Data source

The supplied project documentation names `F1 Racing Project Dataset.xlsx` and describes five sheets:

| Sheet | Documented scope |
|---|---|
| `race_results` | Main analytical source |
| `circuits` | Additional circuit information |
| `championship_standings` | Championship information |
| `lap_intelligence` | Lap information |
| `qualifying_results` | Qualifying information |

The main sheet is described as containing 6,464 result records with season values from 2010 to 2026. This report carries that source description forward; it does not record a new inspection of the raw workbook.

A result record is not a distinct Grand Prix. The season range also does not establish that every official race or driver from those years is present.

## Data preparation

The following decisions define how to prepare the fields for the listed comparisons:

1. Review the field types, record count, missing values and duplicate identifiers in `race_results`.
2. Use Season as a grouping dimension rather than summing the numeric year values.
3. Confirm that DNF is coded as 0 or 1 before calculating a count or rate.
4. Keep non-finish records for reliability analysis and examine how their finish values are represented.
5. Use sums for points, record counts for starting-compound usage and averages for position measures.
6. Apply the intended season selection consistently when comparing views.

These steps describe the preparation approach. A validation log should reflect checks actually performed on the workbook used for submission.

## Analytical views

| # | View | Main setup and interpretation |
|---:|---|---|
| 1 | Team Points by Season | Season on Columns, sum of Points on Rows, Team on Color; compare trends with a line chart |
| 2 | Driver Points Leaderboard | Driver grouped by summed points, sorted in descending order |
| 3 | Non-finishes by Reason | DNF Reason grouped by summed DNF flag |
| 4 | DNF Rate by Weather | Weather grouped by average DNF flag |
| 5 | Team Points Leaderboard | Team grouped by summed points, sorted in descending order |
| 6 | Average Positions Gained | Team grouped by the mean positions-gained value |
| 7 | Starting Compound Mix | Compound grouped by the count of result records |
| 8 | Points by Circuit Type | Circuit category grouped by summed points |
| 9 | Average Finish Position | Team grouped by the average valid finish position |

For a 0/1 DNF flag, an average of 0.06 represents 6% of the records in that group. This is a mathematical example, not a measured result from this package.

A comparison of total points by circuit type should also consider the number of records in each category. Likewise, driver and team totals depend on the records and filters included.

## Website design

The website has four sections: an overview, the nine analysis topics, the preparation workflow and a short data-scope note. Navigation links move to those sections or open this report.

The visual style uses an ivory background, navy text, blue accents and a decorative circuit illustration. Cards and layout columns adapt to narrower screens. The circuit drawing is illustrative and is not a mapped official track.

The page does not load external fonts, scripts or visualization embeds. Its contents are informational; the analysis cards do not display calculated chart results.

## Interpretation and limitations

- Recorded points are used as supplied, without adjusting seasons to a common scoring system.
- Driver and team totals are not verified career totals.
- A weather comparison can show different DNF rates without establishing the cause of a non-finish.
- Starting-compound frequency does not identify the best tyre strategy.
- Average finishing positions depend on the availability and meaning of valid finish values.
- The raw data, calculated fields, filters and workbook layout have not been newly verified as part of this frontend copy.

## Performance and verification

This static website has no data-processing runtime or live workbook connection. Website navigation and source-file checks can be assessed separately from Tableau performance.

No Tableau loading times, filter response times, device-layout results or confirmed workbook scene counts are claimed for this copy. Those measurements depend on the workbook actually submitted.

## Hosting

The supplied workflow publishes the static repository files to GitHub Pages when changes are pushed to `main`. The repository owner needs to select GitHub Actions as the Pages source. Deployment status and the final website address are available in GitHub after the workflow runs.

The site can also be opened locally through `index.html` without installing dependencies.

## References

The original analytical approach draws on Tableau's documentation for worksheets and Stories, and Formula 1's introductory explanations of championship points and race weekends. The course-supplied dataset remains the source for the record-level fields described here.
