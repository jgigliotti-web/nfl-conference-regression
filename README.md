# Quantifying Conference Bias in the NFL Draft

### Objective
The goal of this project is to determine if NFL teams systematically overvalue wide receivers from major conferences (SEC, Big Ten, etc.) compared to those from the Group of 5 or FCS, holding collegiate production constant. By identifying this "Helmet Premium," we can pinpoint market inefficiencies in draft-day asset allocation.

### The Problem
In the NFL Draft, brand recognition often overrides statistical evidence. Scouts frequently assume that production in a Power 5 conference is "safer" or "more translatable" than identical production in a smaller conference. This bias leads to a "Draft Tax," where teams spend higher draft capital on Power 5 players, effectively overpaying for a logo while productive prospects from smaller schools slide down the board.

### Methodology
This project utilizes a multivariate linear regression model to isolate the specific impact of conference affiliation on draft slot.

* Data Engineering: I mapped collegiate statistics and NFL draft data, filtering for prospects with >1,000 career yards to eliminate noise. Schools were categorized into Power 5 or Group of 5/FCS tiers.
* Multivariate Linear Regression: The model sets Draft Pick as the target variable while controlling for Career Yards and Total Touchdowns.
    * Statistical Baseline: I releveled the conference factor to set "Group of 5 / FCS" as the mathematical baseline, allowing the model to output the exact number of picks earlier a player is drafted simply for their conference affiliation.

### Key Findings
* When production is held constant, receivers from the SEC and Big Ten are drafted significantly earlier than their G5 peers. This confirms a systemic "Helmet Premium" that exists independently of on-field output.
* Front Office Application: This model serves as an "Arbitrage Tool." It identifies highly productive players from undervalued conferences who offer "First-Round Production" at a "Third-Round Price." Teams can exploit this bias to find high-impact starters while preserving early-round capital for other needs.
