---
title: Appendix
date: Last Modified 
permalink: /appendix/
eleventyNavigation:
  key: Appendix 
  order: 50
  title: Appendix
---

### Lease Maintenance Compensation

Global Caps & Floors: caps/floors on the netted aggregate measure across all maintenance components

#### Non-rate definitions

* MR Payout Policy: relates to:
* EPR modules: per module cash balance or grouped (all modules front to back)
* LLPs: 5 variations on the calculation of the total LLP reimbursement
* Gears: separate cash balances per gear or one grouped balance for the set

#### MR Settings

* Drop-down: Post-payout balance (the closing MR balance post reimbursement)
  * Roll Forward: balance persists
  * Sweep to Lessee: balance paid to lessee and resets to zero
  * Sweep to Lessor: balance reset to zero with no cashflow
* LC in lieu: toggle 'virtual MR' (letter-of-credit)
* MR Cap: per component cap

#### EOL Settings

* Compensation Level: remaining life % to compensate to, e.g. 100% is full-life, 50% is half-life, etc.
* Mirrored: toggle mirrored compensation level (requires a tech spec at delivery date)
* EOL Cap: per component cap
* EOL Floor: per component floor, e.g. $0 floor is an upsy lease

### Defining Rates

#### Specified rate settings

* Rate as of: the rate will escalate on each anniversary
* Escalation rate %: annual escalation rate
* Metric: charge metric – note EOL compensation to less than 100% will not calculate if the chosen metric is not a limiter; same for cost-sharing lessor contribution definitions

#### Rate Modularity: relates to

* EPR, there are 3 possible rate definitions:
  * Group: single all-module rate (no modular logic)
  * Group Weighted: Group rate is first defined as above, then second, a % distribution of that group rate is defined per module
  * Modular: full nominal rate definitions per module

* Gears, there are 3 possible rate definitions:
  * Group: single rate for the set of gears
  * Per Gear %: Group rate is first defined as above, then second, a % distribution of that group rate is defined per gear
  * Per Gear: nominal rate per gear

#### Extra EPR-specific rate definitions

* Rate Table: define a $/FH rate table per sector length and derate
* Factor Table: multiply the single nominal rate by the table of factors
* Mature Run Adjustment Factor: factor by which to multiply the first run rate post first SV, e.g. 100% means no first/mature run rate split
* EOL EPR reference derate: lookup derate to use for resolving the applicable rate in the EOL calculation. Also, for compensation level of less than 100%, the reference derate is used to lookup the flight-hour-interval to use as the basis for % life.

#### Per component caps/floors behave as follows

* Engine caps/floors are per engine but not per module
* Landing gear caps/floors are for aggregate MR on all gears – not per gear
* EOL Floors are always applied after any inner component aggregation. Consequently, no floor is applied to the EOL calculated amount:
  * Per EPR module
  * Per LLP
  * Per gear
