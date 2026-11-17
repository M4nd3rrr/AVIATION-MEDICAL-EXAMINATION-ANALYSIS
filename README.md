# AVIATION-MEDICAL-EXAMINATION-ANALYSIS
Analysed aviation medical dataset to gain some useful insght to support business decisions
Aviation Medical Examination Analysis
An interactive Power BI dashboard exploring aviation medical examination activity, applicant patterns, examination outcomes, referring organisations, scheduling delays, and certificates approaching expiry.
Project note: This is a portfolio analysis project built with a demonstration dataset. The figures should not be interpreted as the actual performance of a hospital, clinic, aviation medical centre, or referring organisation.

Dashboard preview
Add your dashboard screenshot to the repository at Screenshots/aviation-medical-dashboard.png, then it will appear here:

Project objective
The purpose of this project is to demonstrate how data analysis and visualisation can turn examination records into information that supports operational monitoring and business discussions.

The dashboard is designed to help answer questions such as:
- How many applicant records are represented in the selected period?
- What is the balance between initial and renewal examinations?
- Which referring organisations contribute the most applicants?
- How are examination outcomes distributed?
- How does applicant volume change over time?
- What are the observed appointment-to-examination scheduling delays?
- Which certificates are approaching expiry?
Tools
- Microsoft Power BI Desktop — data modelling, measures, report design, filters, and visualisations.
- Dataset — demonstration aviation medical examination records.
Dashboard features
1. Applicant count
A KPI card displays the applicant count for the current filter selection. The dashboard screenshot displays approximately 15K.

The exact interpretation depends on the measure used: a count of records is not necessarily the same as a distinct count of applicants if an applicant can have multiple examination records.
2. Scheduling delay
Three KPI cards summarise scheduling delay:
KPI	Displayed value
Average scheduling delay	4
Maximum scheduling delay	14
Minimum scheduling delay	0


These values represent the dashboard's scheduling-delay measure. The intended definition should be confirmed against the underlying Power BI measure and source date fields before the figures are used for operational decisions. If the measure is based on appointment and examination dates, state the unit (for example, days) in the report.
3. Initial vs Renewal
A pie chart compares initial examinations with renewal examinations. The visual shows a broadly balanced split between the two categories.

This comparison can help the service understand the mix of new examination demand and returning applicants who require renewal examinations.
4. Applicants by referring organisation
A column chart compares applicant volume across referring organisations. The categories visible in the dashboard include:
- Skylink Airways
- Arik Air
- National Flight Services
- Regional Aviation Group
- Independent Applicant
- Other Organisations
This view can help identify major sources of applicant referrals and provide a starting point for discussions about referral relationships. Applicant volume alone does not establish revenue, profitability, or the value of a relationship.
5. Examination outcomes
A doughnut chart presents the distribution of examination outcomes. The dashboard displays approximately:
Outcome	Share displayed
Fit / Issued	77%
Deferred	15%
Unfit / Denied	8%


The outcome categories should be interpreted according to the definitions used in the dataset. In particular, a deferred case should not automatically be treated as a final unsuccessful outcome; it may require further review or follow-up.
6. Monthly applicant volume
A line chart shows applicant volume by month. It helps reveal changes in demand over time and highlights months that may warrant further investigation.

A peak or decline is a signal to investigate, not proof of its cause. It can be explored further by comparing the period with examination type, certificate class, and referring organisation.
7. Certificates approaching expiry
The Expiring Soon table lists applicant records with certificate information, including applicant ID, certificate class, and date components.

This view can support renewal planning and timely follow-up. The exact expiry window and the logic used to identify records as “expiring soon” should be documented in the report or measure.
Report filters and interaction
The dashboard includes two sets of slicers:
- Certificate Class: Class 1, Class 2, and Class 3.
- Appointment Year: 2024, 2025, and 2026.
Users can select a certificate class and/or appointment year to focus the report on a particular segment of examination activity. Selecting a chart category may also cross-filter other visuals, depending on the visual interaction settings in Power BI.

To return to the overall view, clear the selections or restore the slicers to their default state.
Potential business questions
The dashboard can support further investigation into questions such as:
1. Which referring organisations are contributing the most applicants, and how is their referral volume changing?
2. Are deferred cases eventually issued certificates, remain deferred, or become unfit/denied?
3. Are scheduling delays higher for a particular month, certificate class, or examination type?
4. Can upcoming certificate expirations help the team anticipate future renewal demand?
5. Are monthly demand peaks consistent from year to year?
These are questions for further analysis; the dashboard alone does not establish their answers.
Important limitations
- The displayed figures are from a demonstration dataset and are not evidence of actual organisational performance.
- Applicant count should be checked to establish whether it counts rows, examinations, or unique people.
- The definitions of initial, renewal, fit/issued, deferred, and unfit/denied should match the source data.
- Scheduling-delay units and calculation logic should be verified against the underlying measure.
- The date window and calculation behind “Expiring Soon” should be documented.
- The dashboard does not currently show revenue, payments, costs, or profit. Financial conclusions would require appropriate financial records and a reliable way to link them to examination activity.
- No identifiable or confidential patient information should be published in this repository.
Possible next steps
- Add a breakdown of deferred cases by reason and follow-up status.
- Track the eventual outcome of deferred cases where follow-up records are available.
- Add a clearly defined certificate-expiry window (for example, the next 30, 60, or 90 days).
- Verify and document the scheduling-delay calculation and its unit.
- If suitable data becomes available, analyse examination fees, invoices, payments received, and costs separately from applicant volume.
