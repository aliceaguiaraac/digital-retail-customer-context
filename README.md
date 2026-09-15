# Digital Retail Journey | Customer Context Retention

This project started as an independent Digital Analytics exercise.

I took the initiative to explore a publicly available automotive digital retail journey and look for a real customer behaviour that could be turned into an analytics question.

During the exploration, I identified a case where a vehicle preference selected earlier in the journey was not preserved when the user moved to available stock, requiring the preference to be manually selected again.

From that observation, I mapped the customer journey, designed a measurement plan and used AI to generate a **synthetic behavioural dataset** for Power BI to demonstrate how I would measure, analyse and investigate the behaviour.


[Open the interactive Power BI report](https://app.powerbi.com/view?r=eyJrIjoiNTJlNWI5ZmEtNjQ5MC00ZmYzLWJmZGItN2U3M2U2YjhlZTE1IiwidCI6IjM1ODAxOWMyLWZmMWQtNGRlOC04MDBlLTk2YTRkMzgwNzMwYyIsImMiOjl9)

## Analytics Question

The analysis focuses on three main questions:

- Is the selected vehicle context preserved during the **Vehicle Selection → Stock** hand-off?
- When context is lost, how often do users manually reapply their vehicle preference?
- Is context preservation associated with differences in downstream progression towards commercial intent?

## Journey Analysed

The main journey analysed in the report is:

**Vehicle Line Selected → Available Vehicles Click → Stock Results → Vehicle Detail → Proposal Start → Proposal Submit**

The analysis also compares downstream behaviour between sessions where customer context was preserved and sessions where it was not.

## Key Insights

- Progression through the main stock-to-proposal journey
- Context retention at Stock entry
- Manual vehicle-line reapplication after context loss
- Progression from Stock Results to Vehicle Detail
- Proposal start and submission rates
- Downstream comparison between preserved and non-preserved context sessions

## Key Finding

In the synthetic scenario, a meaningful share of stock-entry sessions did not preserve the previously selected vehicle context, and many of those sessions manually reapplied the vehicle line.

However, proposal submission remained broadly similar between sessions where context was preserved and those where it was not.

There is also a meaningful drop between **Stock Results and Vehicle Detail** that should be investigated further, but the synthetic data does not suggest that context loss is the main driver.

### Main takeaway

**Identify the friction, measure it, but do not force a conversion story when the data does not support one.**

## Recommendation

Track **context retention** and **manual reapplication** as journey-quality indicators, and investigate the **Stock Results → Vehicle Detail** drop using real behavioural and qualitative customer data.

## Next Step

Validate the journey using real behavioural and qualitative data.

If context loss appears to affect customer effort or downstream progression, test a context-preserving hand-off through an A/B experiment.

## Measurement Approach

As part of the exercise, I designed a proposed event-tracking framework to support the analysis.

Example events include:

- `vehicle_line_select`
- `available_stock_click`
- `stock_results_view`
- `stock_line_filter_apply`
- `vehicle_detail_view`
- `proposal_start`
- `proposal_submit`


The measurement plan also includes contextual parameters such as:

- Vehicle model
- Vehicle line
- Device type
- Journey step
- Source page
- CTA
- Context preservation status
- Session identifier

## Data

The report uses **synthetic behavioural data generated to simulate realistic digital retail journeys for demonstration purposes**.

Synthetic data was deliberately used because no internal customer or production analytics data was available.

The dataset allows the analytical approach, data model, KPIs, funnel logic and segmentation strategy to be demonstrated without making claims about actual business performance.

## Tools & Techniques

- Power BI
- DAX
- Power Query
- Data Modeling
- Digital Analytics
- Customer Journey Analysis
- Funnel Analysis
- Segmentation
- Measurement Planning
- KPI Design
- A/B Testing Framework
- AI-assisted Synthetic Data Generation

## Report Preview

![Digital Retail Journey](digitalretailjourney.png)
