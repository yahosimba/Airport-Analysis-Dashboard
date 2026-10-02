# Airport passenger and operations management review

## Main findings

DXB reported 95.2 million passengers and 454,800 flight movements in 2025. Passenger growth calculated from its rounded published annual totals is 3.1%. The network reached 291 destinations in 110 countries.

DXB handled 86.75 million bags. Reported mishandled baggage fell from 5.5 to 2.47 bags per 1,000 guests between 2024 and 2025. Departure passport control processed 99.35% within ten minutes; security processed 98.9% within five minutes. These service rates refer to different thresholds and populations.

Heathrow handled 55,720,797 passengers in January–August 2026, down 0.4% against the same eight months of 2025. Air transport movements fell 1.7% to 312,559. Cargo excluding mail increased 1.5% to 1,036,943.687 tonnes. This is a matched-period comparison; 2026 is not annualised.

Review passenger demand and movement capacity together. Heathrow's aggregate throughput was 178.3 passengers per movement during the matched 2026 period. This ratio is not aircraft load factor. The report's market contribution charts support investigation of regional changes; public aggregates do not establish the causes of those changes.

## Report guide

| Page | Management use |
|---|---|
| 01 DXB executive | Annual passengers, movements and baggage trajectory |
| 02 DXB market network | Published country and city concentrations, network expansion |
| 03 DXB service operations | Baggage reliability, service thresholds and load factor |
| 04 DXB Heathrow comparison | Annual traffic context with movement scope caveats |
| 05 Heathrow latest review | Matched monthly passenger, movement and cargo review; month selector |
| 06 Heathrow passenger markets | Market mix, growth and contributions to change |
| 07 Heathrow seasonality | Monthly patterns across historical comparison years |
| 08 Heathrow operating intensity | Movements, passengers per movement, daily throughput and scatter analysis |
| 09 Heathrow cargo | Cargo trends, regional mix and contributions |
| 10 Sources and data quality | Source links, reconciliations, exceptions and metric definitions |

Visuals include lines, areas, columns, bars, donuts, a treemap, gauges, waterfalls, a scatter chart, a matrix and detailed tables. Click chart categories to explore associated values. Use the month dropdown on page 05; clear its selection to restore all eight months.

## Files and refresh

- Open `Airport_Operations.pbix` in Power BI Desktop. Its imported data is embedded, so viewing the saved report does not require an internet connection or a login.
- `Airport_Operations_Data.xlsx` contains the clean source tables, calculated summary, provenance and audit notes.
- `Airport_Operations.pbip` and its report/model folders provide editable project sources.
- The `data` folder contains typed input CSV tables. Power Query currently refers to their absolute paths on this computer. If the folder moves, update those paths before refreshing. Refresh reloads these local snapshots; it does not automatically fetch new airport publications.
- The `sources` folder preserves the original Heathrow workbook and Dubai publication snapshots.

## Sources and coverage

Official [Dubai Airports releases](https://media.dubaiairports.ae/dxb-sets-global-benchmark-as-record-traffic-become-the-norm/) supply annual DXB figures for 2021–2025 and published 2025 market/service figures. The workbook's Sources tab lists all five annual release URLs.

Official [Heathrow traffic statistics](https://www.heathrow.com/company/investor-centre/reports/traffic-statistics) supply 260 monthly observations from January 2005 through August 2026 and 2,080 associated regional records. Sources were retrieved on 2 October 2026.

## Data limitations and cleaning decisions

- These are real published airport aggregates. Monthly DXB operations, individual passengers, flight delays and cancellations are unavailable in these inputs.
- DXB 2024–2025 passenger totals are rounded to 0.1 million. Preserve that precision when interpreting growth.
- Missing published values remain blank, including DXB 2025 cargo and 2021 baggage. No values were invented to fill gaps.
- The DXB country chart includes a calculated remainder labelled “Unlisted markets”; it is not an independently published country category. The city treemap contains only the five published leading cities.
- DXB all-flight movements and Heathrow air transport movements have different scopes. Cross-airport throughput ratios require that caveat.
- DXB's published 2025 baggage growth rate differs from the growth implied by published volume levels. The report retains the levels and excludes the disputed rate. Its published 214 passengers per flight also differs from total passengers divided by all movements, which is 209.3; the report labels the calculated denominator explicitly.
- Heathrow February and March 2008 contain fractional published passenger/movement counts. They remain preserved and flagged; the operating scatter starts in 2016.
- Monthly dates are unique. Regional passenger totals reconcile with headline totals; regional cargo totals reconcile within a 0.001-tonne tolerance. Comparisons match January–August in both years.

## Verification

All ten pages were opened in Power BI Desktop and visually reviewed. The month selector was checked against January 2026: 6,460,877 passengers, 38,439 movements and a passenger increase of 141,801 (+2.2%) versus January 2025. It was then reset to all months. Excel summary formulas were recalculated and inspected for formula errors.

The saved PBIX was closed and reopened successfully. Both the DXB executive and Heathrow monthly review remained populated without refreshing. Verification screenshots are in the screenshots folder.
