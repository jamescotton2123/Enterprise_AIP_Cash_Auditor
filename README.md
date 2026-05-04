# Enterprise_AIP_Cash_Auditor
Automated WealthTech reconciliation pipeline bypassing legacy RPA limits
# Enterprise AIP Cash Auditor & Reconciliation Pipeline

## The Architecture Problem
In a high-throughput Wealth Management environment ($3B+ AUM), legacy API loops and low-code RPA tools (Power Automate / SharePoint) suffer from severe memory bottlenecks and API timeouts when handling datasets exceeding 5,000 rows. Relying on these legacy systems for fractional share payouts and residual cash auditing resulted in multi-hour processing times and unacceptable risks of data truncation.

## The 0-to-1 Solution
This repository contains the architecture for a fully decoupled, Python-based reconciliation engine. By shifting the data transformation layer into a Pandas environment, this pipeline utilizes vectorized mathematics and relational Left Joins to bypass API pagination limits entirely. 

What previously took 3 hours of manual validation and low-code processing is now executed deterministically in milliseconds, ensuring 100% auditable accuracy for institutional wire processing across custodial accounts (Orion/Schwab).

## Core Capabilities
* **Relational Discrepancy Auditing:** Executes high-speed `Left Joins` between Sales CRM data and Custodial Exports to instantly identify unfunded exceptions and ghost leads.
* **Vectorized Financial Logic:** Eliminates standard iteration loops by calculating management fees and residual balances across institutional arrays simultaneously.
* **Deterministic Output:** Generates strictly formatted, audit-ready Excel outputs for the Operations and Accounting teams, fully sanitized of `NaN` or `Null` exceptions.

## Tech Stack
* **Language:** Python 3.x
* **Core Libraries:** Pandas, Logging
* **Domain:** WealthTech, Custodial Reconciliation, Data Engineering
