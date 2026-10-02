# Airport passenger and operations review

A Power BI management report built from public Dubai International Airport (DXB) annual operating releases and Heathrow Airport monthly traffic statistics. The included PBIX is ready to open with an embedded data snapshot. The editable Power BI Project (PBIP) is in `powerbi/`.

## Included files

- `Airport_Operations.pbix`: saved report snapshot.
- `powerbi/`: editable report and semantic model.
- `data/`: normalized CSV inputs, table-build JSON and validation summary used for the report.
- `sources/`: original Heathrow workbook and Dubai release text and URL snapshots.
- `scripts/`: retrieval, data preparation, Power BI generation, presentation polish and clone-path setup.
- `Management_Brief.md`, `DATA_NOTICES.md` and `LICENSE`.

## Open or refresh

Open `Airport_Operations.pbix` in Power BI Desktop for the populated saved report. To refresh the editable project after cloning, install Python 3.10+, run `python scripts/configure_powerbi_paths.py` from this folder, and then open `powerbi/Airport_Operations.pbip`. Refresh in Power BI Desktop to reload the included CSV snapshot.

## Rebuild from the archived source data

Install dependencies using `python -m pip install -r requirements.txt`, then run from the repository root:

```powershell
python scripts/prepare_data.py
python scripts/build_powerbi.py
python scripts/polish_powerbi.py
python scripts/configure_powerbi_paths.py
```

This regenerates the CSV tables and PBIP project. It does not regenerate the PBIX file.

To check current source publications, run `python scripts/fetch_sources.py` and then `python scripts/prepare_data.py`. Heathrow may link to a newer workbook, so updated results can differ from the included frozen snapshot. Review the new source workbook and `data/Data_Validation.json` before publishing a refreshed report.

## Pages

1. DXB executive traffic and baggage trend
2. DXB country and city network
3. DXB service rates and baggage reliability
4. DXB and Heathrow annual context
5. Heathrow matched-month traffic review
6. Heathrow regional passenger markets
7. Heathrow seasonality
8. Heathrow operating intensity
9. Heathrow cargo
10. Sources and data quality

The report includes KPI cards, lines, areas, clustered columns and bars, donuts, a treemap, gauges, waterfalls, a scatter chart, a matrix and detail tables. Page 5 has a month selector, defaulting to the eight matched months.

## Coverage and interpretation

DXB annual data covers 2021–2025. Heathrow includes 260 monthly records from January 2005 through August 2026 and eight regional categories. Selected DXB market and service data is reported for 2025. Monthly Heathrow 2026 comparisons use January–August against the same months in 2025 and are not annualized. Heathrow cargo excludes mail. Missing source figures stay blank. Some DXB totals are rounded as published. “Unlisted markets” is a calculated remainder. DXB all-flight movements and Heathrow air transport movements have different scopes. Passengers per movement is a throughput ratio, not aircraft load factor.

## Sources

- [Dubai Airports 2025 traffic release](https://media.dubaiairports.ae/dxb-sets-global-benchmark-as-record-traffic-become-the-norm/) and 2021–2024 URLs in `sources/DXB_Source_URLs.json`.
- [Heathrow traffic statistics](https://www.heathrow.com/company/investor-centre/reports/traffic-statistics).

The included source snapshots were retrieved on 2 October 2026. See the workbook’s Sources, Definitions and Audit tabs and the report’s page 10 for full provenance and checks.

The repository also includes the full Airport_Operations_Process_Handbook.docx process record.
