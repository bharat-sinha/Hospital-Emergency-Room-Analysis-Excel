# Hospital Emergency Room Performance Dashboard (Excel)

![Hospital ER dashboard](Hospital%20ER%20Dashboard.png)

An interactive Excel dashboard that tracks emergency room demand, wait times, admission outcomes, department referrals and patient satisfaction across 9,216 patient visits. Hospital administrators can filter by month, year and patient demographics to find where the ER is under pressure.

**Tools:** Excel (Power Query, PivotTables, PivotCharts, slicers)
**Domain:** Healthcare analytics, operations and patient experience

---

## Business problem

Emergency rooms run under constant pressure. Long waits hurt patient experience, and a crowded ER hurts care quality. Hospital management needs one view that shows when demand peaks, who is using the ER, how long they wait, and where patients are referred, so staffing and triage decisions rest on data.

## Questions the dashboard answers

1. How many patients visit each month and year?
2. What is the average wait time, and how many patients are served on time vs delayed?
3. How satisfied are patients, and does satisfaction move with wait time?
4. What share of patients is admitted?
5. Which age groups and genders use the ER most?
6. Which departments receive the most referrals?

## Dataset

- **Source:** Hospital Emergency Room raw data (a public practice dataset, included as `Hospital Emergency Room Raw Data.csv`)
- **Size:** 9,216 patient visits
- **Main fields:** visit date, patient age and gender, wait time, department referral, admission status, satisfaction score
- **Note:** this is a sample dataset, not data from a real hospital.

## Approach

1. **Clean** the raw CSV in Power Query: fix data types, handle blanks, standardize category labels, create age-group bands.
2. **Analyze** with PivotTables for volume, wait time, admission, demographics and referrals.
3. **Visualize** with PivotCharts and KPI cards on a single dashboard sheet.
4. **Make it interactive** with slicers for month, year and demographics, so a user can drill down without rebuilding anything.

## Key findings

| Metric | Result |
|---|---|
| Total patient visits | 9,216 |
| Average wait time | 35.26 minutes |
| Average patient satisfaction | 4.99 (out of 10) |
| Admission outcome | Close to a 50/50 split between admitted and not admitted |
| Highest-use age group | 60 to 69 |
| Largest referral departments | General Practice and Orthopedics |

Read these as patterns in the sample data, not as proven causes.

## Recommendations

These are hypotheses for hospital management to test, based on what the dashboard shows.

1. **Review triage for referral flow.** General Practice and Orthopedics take the largest share of referrals. Check whether a fast-track or urgent-care path could handle some of these cases outside the main ER.
2. **Plan staffing around peak periods.** Use the monthly and yearly views to find the busiest periods and schedule staff to match.
3. **Target the 60 to 69 age group.** They use the ER most. Look at whether follow-up care or community programs could reduce avoidable visits.
4. **Look into the admission split.** About half of patients are admitted. Combine this with triage severity (not in this dataset) to learn whether the non-admitted half could have been treated elsewhere.
5. **Track wait time as a distribution, not just an average.** An average of 35 minutes can hide a long tail of very long waits.

## Limitations

- The dataset has no triage severity or diagnosis, so I can't say which visits were truly urgent.
- "Not admitted" does not mean "non-critical." That group may include patients treated and sent home.
- The satisfaction score is a single number per visit, with no comments, so the reasons behind it are unknown.
- The data is a sample, so results should not be generalized to any real hospital.

## Next steps

- Report median and 90th-percentile wait time next to the average.
- Define the on-time threshold clearly (for example, within a set number of minutes) and show it on the dashboard.
- Add peak hour and day-of-week analysis if the data supports it.
- Rebuild the dashboard in Power BI and compare it with this Excel version.

## Repository contents

```
├── Hospital Emergency Room Raw Data.csv            # raw dataset
├── pivot + dashboard hospital emergency room.xlsx  # PivotTables and dashboard
├── Hospital ER Dashboard.png                       # dashboard screenshot
├── Hospital Emergency Room Analysis.pdf            # exported report
└── README.md
```

**To explore:** download the `.xlsx` file, open it in Excel, and use the slicers on the dashboard sheet to filter by month, year and patient group.

## Skills demonstrated

Data cleaning (Power Query) · PivotTables and PivotCharts · KPI design · Dashboard design with slicers · Healthcare operations analysis · Turning findings into recommendations

## Author

**Bharat Sinha**, aspiring data analyst
[LinkedIn](https://www.linkedin.com/in/bharat-sinha-122791130/) | [GitHub](https://github.com/bharat-sinha) | sinha.bharat8@gmail.com
