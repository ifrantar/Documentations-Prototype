---
title: Technical Analysis
date: Last Modified
permalink: /technical-analysis/
eleventyNavigation:
  key: Technical Analysis 
  order: 50
  title: Technical Analysis
---

### Analysis Setup

The Analytics Suite allows for technical analysis across both Aergo Capital’s existing fleet and the global fleet of commercial aircraft. This is made possible through the application of Aergo Capital underwriting assumptions for engine, airframe and part costing and scheduling to aircraft types and engine sub-types that are defined in the global fleet.

Technical analysis requires a technical snapshot i.e., the Tech Spec. The technical snapshot defines the condition of the aircraft based on an “As Of” date, from which the maintenance model will run the forecast. Tech Specs for the Aergo fleet are automatically generated from the monthly data upload process. However, Tech Specs for the global fleet can be manually created using the guidance in Appendix 1. Thus, to select/set-up an aircraft for technical analysis:

* Log-in to the ‘Analytics Suite’ and the aircraft search page will appear
* Enter the desired aircraft MSN or Registration into the search bar
* Technical → Snapshots → Create New Assembly Snapshot (only relevant if from global fleet).

Once completed, a base context will be created. The base context will populate with default Knowledge Base parameters (detailed training guide on knowledge base parameter settings will be provided in the future).

### Performing Technical Analysis

Figure 1, below, provides an example of the Cost to Full Life section of the Analytics Suite. The Cost to Full Life section offers an in-depth visual of maintenance event burndown, timing and breakdown, as well as the analysis context editor.

![Hello, world](/content/images/picture-6.png)->_Figure 1: Cost to full life graph_<-

#### Cost to Full Life interaction

The Cost to Full Life graph aids the analyst in examining the maintenance schedule over the forecast period.

1. A background burndown visual plots the reduction in remaining life of components.
2. The occurrence of a maintenance event is flagged on the Cost to Full Life plot, indicated by the “M” tooltip.
3. Selecting the “M” tooltip opens a drill-down of the maintenance event below the graph. See Figure 2 for an example.

![Hello, world](/content/images/picture-7.png)->_Figure 2: Maintenance Event Drill Down_<-

#### Creating an analyis

To begin analysing, press ‘Analyse’ in the top right-hand corner of the page, as seen in Figure 1. Now, all analysis parameters on the right-hand-side (the 'analysis editor') may be edited (unsaved). The Cost to Full Life graph will instantly update as parameters are adjusted in the analysis editor. Note that analyses can also be created in other sections of the platform, including the Maintenance Adjustment, Cashflow and EOL Accrual sections. Technical analysis parameters are discussed in more detail in the following pages.

The analysis editor comprises an array of parameters covering many aspects of the forecast. Those parameters relevant to technical analysis are laid out below.

#### Lessee Operator

::: callout-blue
**Note:** The leased operation of the aircraft is defined here
:::

![Hello, world](/content/images/picture-8.png)->_Figure 3: Lesee Operator - Analysis Parameters_<-

Firstly, the user must define the sequence of leases assumed in the forecast. 'Lease Method' set to 'Auto' causes the model to attempt to run the contracted lease as the first in the sequence. Changing 'Lease Method' to 'Specified' enables the user to select a different lease sequence.

'Add New Lease' enables the user to add to the sequence of future leases.

Within each lease, the below parameters may be set:

* Transition Costs – covered in lease analysis doc to be sent shortly
* Utilization:
  * Auto: establish the utilization from the knowledge base – see utilization settings doc to be sent shortly
  * Specified: override the knowledge base assumptions. Changes in utilization over the course of the lease can be defined by selecting “Add period.”

#### Non-leased Operator

::: callout-blue
**Note:** Operation of the aircraft without a lease is defined here
:::

Auto and specified settings behave in broadly the same manner as in the 'Lessee Operator' section.

'Auto' setting yields the additional 'Ground if Leased' parameter. When selected, as soon as a lease is introduced in the 'Lessee Operator' section, the aircraft will be grounded during any off-lease period thereby nullifying any utilization inputs in this section.

_A common use-case for de-selecting this parameter would be the modelling of a sale-and-leaseback transaction. It is selected by default._

#### Operation Severity

![Hello, world](/content/images/picture-9.png)->_Figure 4: Operating Severity - Analysis Parameters_<-

* Operating severity dictates the engine takeoff derate and the aircraft operating conditions.
* The takeoff derate will determine the EPR flight-hour-interval as defined in the knowledge base severity table, if any.
* Operating Conditions is the % reduction in the EPR flight-hour-interval owing to harsher environmental conditions.

#### Engine interdependencies

![Hello, world](/content/images/picture-10.png)->_Figure 5: Engine Interdependencies - Analysis Parameters_<-

These settings determine engine shop-visit workscope

* LLP Build Life (Cycles): on entering shop, all LLPs with FC remaining below this number will be replaced.
* LLP Replacement Stub Life (%): same as the above parameter except that the minimum FC are determined as a % of the forecast limit of each LLP.
* PR Stub Life (%): on entering shop, any modules with a life remaining below this % will be restored.

_Engine shop-visit workscopes may be visualised in the burn-downs as each EPR module and LLP stack is represented as a lateral strip whereby the strip from top-bottom represents the engine from front-back._

#### Maintenance Inflation

* Maintenance cost inflation per component. Note any industry maintenance rates will escalate at these rates.

#### Maintenance Policies

* This section allows LLP limits to be defined on a “Regulatory" (Chapter 5) or “Planning” basis.

### Saving Analysis

Once analysis is complete, it can be discarded, saved as “Base” or as a new analysis.

New Analyses: New, non-base, analyses can be created by selecting Analyse → Save As → enter analysis name e.g., “Scenario 1.” If the name of an existing analysis is entered the user will receive an overwrite warning.

### Analysis Forecast

To navigate to the Analysis Forecast using the top ribbon: Fundamentals → Analysis Forecast

The Analysis Forecast section of the platform allows the user to view all maintenance, lease and pricing outputs in the form of a table that is exportable to Excel as a CSV. ​Given that we are concerned with technical analysis, the most applicable filters are those under the 'Maintenance' category.

The filters applied allow the user to view some of the following on a month-by-month basis:

The exact timing of maintenance events

* The full and remaining life value of maintenance
* The cost to full life
* Remaining hours/cycles/life for all aircraft parts and engine components (at an LLP level) which is useful for analysing engine interdependencies. Can also view the LLP limiter i.e., the LLP with the lowest remaining life.
* Life used SLSV
* Cost rates per month

![Hello, world](/content/images/picture-11.png)->_Figure 5: Analysis Forecast filters for maintenance_<-

### Creating a Tech Spec

To create a Tech Spec:

* Using the top ribbon: Technical → Snapshots → Create New Assembly Snapshot.
* The user will need to enter the “As of date” for the Tech Spec.
* The system will navigate the user to the Tech Spec editor, as seen in Figure 8.
* Tech Spec fields can be populated for each component through selecting the component, selecting edit and defining the necessary metric.
* For each engine and part component, key metrics include total hours and cycles consumed/remaining, hours and cycles SLSV and shop visit dates.
* If no shop visit has occurred, these fields can be left blank. When all metrics are entered, select “Save.”
* Once all fields are completed, select “Return to Assembly Snapshots.”

::: callout-blue
Note: Users can edit, change the “As of” date, or delete an assembly snapshot using the Actions tooltips in the Snapshot page (Figure 9)..
:::

![Hello, world](/content/images/picture-12.png)->_Figure 8: Tech Spec Editor_<-

![Hello, world](/content/images/picture-13.png)->_Figure 9: Technical Snapshot_<-
