---
title: Pricing an Aircraft
date: Last Modified 
permalink: /pricing-aircraft/
eleventyNavigation:
  key: Pricing an Aircraft 
  order: 10
  title: Pricing an aircraft
---

## Step 1: Searching and Aircraft

The Analytics Suite facilitates the trading and pricing analysis of aircraft across the global fleet of commercial aircraft. This is made possible through the application of Aergo Capital underwriting assumptions for engine, airframe and part costing and scheduling to aircraft types and engine sub-types that are defined in the global fleet.

To search an aircraft within the global fleet for pricing:

* Log-in to the ‘Analytics Suite’ and the aircraft search page will appear
* Enter the desired aircraft MSN or Registration into the search bar
* The aircraft will be available for pricing if a maintenance forecast is provided (Figure 1)
* User can return to the search page by selecting the aircraft tooltip in the left-hand ribbon

![Hello, world](/content/images/picture-1.png)->_Figure 1_<-

## Step 2: Entering a Tech Spec

Once an aircraft is selected for pricing, a Tech Spec must be created. In this step, the Tech Spec editor will be used to define the consumed and remaining life for the aircraft's engines, engine LLPs, airframe, landing gear and APU.

To create a Tech Spec:

* Using the top ribbon: Technical → Snapshots → Create New Assembly Snapshot
* The user will need to enter the “As of date” for the Tech Spec
* The system will navigate the user to the Tech Spec editor, as seen in Figure 2
* Tech Spec fields can be populated for each component through selecting the component, selecting edit and defining the necessary metric.
* For each engine and part component, key metrics include total hours and cycles consumed/remaining, hours and cycles SLSV and shop visit dates.
* If no shop visit has occurred, these fields can be left blank. When all metrics are entered, select “Save.”
* Once all fields are completed, select “Return to Assembly Snapshots”

::: callout-blue
**Note:** Users can edit, change the “As of” date, or delete an assembly snapshot using the Actions tooltips in the Snapshot page (Figure 3)
:::

![Hello, world](/content/images/picture-2.png)->_Figure 2_<-
![Hello, world](/content/images/picture-2.1.png)->_Figure 3_<-

## Step 3: Entering a Contracted Lease

To create a Contracted Lease, follow the below steps for each section:

* Using the top ribbon: Commercial → Contracted Lease → Create New Contracted Lease.
* To activate a component of the contracted lease, use the toggle button.

### Fundamentals

* Enter an appropriate lease name that is identifiable and informational.
* ExternalID may be left blank for pricing external aircraft
* Define the lease duration using the Start/End Date fields and select the operator.

### Rent

* There is always a 'Base rent' definition: this is the rental definition across the entire lease timeline in the absence of any alterations to the rent schedule.
* The available rent definitions are – click the blue rent definition icon to change it:
  * Flat
  * PBH
  * Seasonal – click the '>' to set the rent per calendar month
* Payment Period is the frequency of payment; e.g. quarterly rent is a payment period of 3 months.
* To vary the rental schedule, click “+ New Rent Period”. Select the period in which the new arrangement takes effect, then define as before.
* Multiple rent period may be created. The arrangement in the latest period runs to the end of the lease.

![Hello, world](/content/images/picture-3.png)->_Figure 4: Example of varying rental schedule, see how in 2025-01 it reverts to the original base rent_<-

### Maintenance Deposit

* Monthly Deposit is the monthly cash contribution
* Final Deposit is the total final deposit balance  (cash contributions cease once this balance is reached)

::: callout-blue

#### Maintenance Compensation (Using Industry Rates)

* The Industry Rates feature enables users to set up maintenance compensation arrangements in seconds via the underwriting data that is stored in the Knowledge Base.
* Industry rates feature refers to the maintenance cost divided by interval, i.e. set the rate to unit cost (the model will then escalate such rates by maintenance cost escalation analysis parameter)
* Use the buffer to add an % margin to the industry rate.

:::

* For more detailed maintenance compensation definitions, please see [Appendix 1](/appendix/).

### Lessor Contribution

* Payout Policy: define when the lessor contribution is settled
* Type:
  * Max defines a maximum nominal top-up
  * Cost-Share defines the maximum top-up as a % of event cost
  * Auto defines either of the above measures based on the delivery cert

### Redelivery Conditions

* Redelivery Conditions can be defined on utilisation by Min Remaining or Max Consumed. Note these definitions may be applied to % life of the component

## Step 4: Entering a Lease Snapshot

To create a Lease Snapshot , follow the below steps for each section:

Using the top ribbon: Commercial → Contracted Lease → Lease Snapshots →  Create New Contracted Lease

* Enter the “As of date” for the Lease Snapshot
* To activate a component of the contracted lease, use the toggle button
* Current cash balance, payables and receivable status of all lease components can be input on this screen

## Step 5: Perform Trading Analysis

Once the Tech Spec, the Contracted Lease and the Lease Snapshot have been created, trading analysis can now be performed.  

Key steps to starting a pricing analysis are as follows:

* Using the top ribbon: Commercial → Trading → Analyse (in top right)
* Select “Add aircraft pricing settings” – here pricing fundamentals are entered.
* If the deal is subject to SPA adjustments, these settings can be defined by toggling “Set SPA” on.
* When these inputs are defined, the Purchase Price, and Fee Breakouts (SPA also if set) will be calculated, as well as a yield and cashflow analysis.
* Pricing parameters can also be added for Financing and Fee Structure, along with any other non-pricing related parameters such as utilisation, etc.
* Before performing further scenario analyses, the initial pricing analysis can be saved as “Base.”  
