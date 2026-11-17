# Tableau Movie Analysis

A learning portfolio project by Sam exploring recorded movie revenue, release years, original language and runtime in the supplied dataset.

## Open the project

Download `Movies_Analysis.twbx` and open it in Tableau Desktop or Tableau Public 2026.3 or later. Data is embedded in the package. For the XML workbook, keep `Movies_Analysis.twb` beside the `Data` folder.

## Dashboard views

- Recorded revenue by release year.
- Recorded revenue by original language.
- Average runtime by title.
- Dataset summary with average runtime, average rating and average popularity rather than misleading sums.

## Data and definitions

The source has 4,535 populated rows and 4,527 unique movie IDs. IDs are the preferred film key: titles can repeat. Revenue and budget retain the source's units because currency documentation was not provided. Release years describe films in this sample, not complete annual industry performance.

Zero revenue: 0 rows. Zero budget: 1,115 rows. Zero runtime: 18 rows. Original values are preserved. Zero may reflect missing reporting and should not automatically be interpreted as no earnings or no budget. Average runtime includes source zeros; filter Runtime > 0 for a known-runtime-only view. Vote average is an unweighted mean across source rows, not a vote-weighted audience rating. Repeated movie IDs contribute more than once; deduplicate against an authoritative source before treating the row average as a distinct-film average. Recorded revenue is not profit, and ROI is not calculated.

## Improvements

Descriptive worksheet and dashboard names replace generic labels. Runtime, ratings and popularity use averages instead of sums. The workbook now uses a relative packaged source, cached thumbnails and machine fingerprint metadata are removed, and the unrelated sales spreadsheet from the original package is excluded.

## Provenance and validation

Source: user-supplied `Movies_data_2000.xlsx`, sheet `movie-database`. The filename does not establish a release-year filter or row limit. Upstream provenance and redistribution licence were not provided; confirm before public redistribution.

XML parsing, ZIP integrity and packaged connection paths checked. Data controls were independently calculated from the supplied sources. Tableau could not expose an application window in this session, so native rendering, refresh, dashboard actions and the revised Excel connection remain unverified. Open in Tableau 2026.3 or later and refresh before publishing screenshots.

See `data_checks.json` for independently computed source checks. This is a learning portfolio project.
