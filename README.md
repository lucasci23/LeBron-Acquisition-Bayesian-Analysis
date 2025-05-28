# LeBron-Acquisition-Bayesian-Analysis
This project features a Bayesian decision model to evaluate whether a particular NBA team (Toronto Raptors) should offer LeBron James a contract in an effort to acquire him in Free Agency

## Overview
This project applies probabilistic modeling, Bayesian inference, and decision analysis to evaluate a high-stakes strategic question for an NBA team: Should the team sign LeBron James? The goal is to integrate financial, performance, risk, and reputational factors into a comprehensive, data-driven framework to guide decision-making under uncertainty.

Using a Bayesian Network implemented in PyMC, the model simulates various real-world scenarios to estimate the expected utility of signing (or not signing) LeBron under different informational and operational strategies—such as conducting market research, requesting gambling background checks, or making decisions blindly.

## Tools and Technologies
• PyMC – Probabilistic programming in Python for Bayesian modeling/n
• ArviZ – Exploratory analysis of Bayesian models and MCMC diagnostics

• NumPy – Scientific computing and numerical operations

• Matplotlib – Visualization of probabilistic outputs and diagnostic plots

• Jupyter Notebooks – For interactive development and interpretation

## Core Components & Model Structure
The decision model evaluates the expected utility of six plausible decision strategies, each involving a combination of the following actions:

• Acquire LeBron James or not
• Conduct market research to assess public interest/popularity
• Request a gambling investigation to assess off-court risk

### Decision and Observation Nodes
For each scenario, the following stochastic variables and dependencies are modeled:

• Popularity: Modeled with a Beta distribution. Observable via market research.
• Gambling and Caught: Indicates off-court risk; observable through optional investigation.
• LeBron_Games_Missed: Modeled as a Gamma distribution to simulate injury risk.
• LeBron_Games_Played: A deterministic function dependent on acquisition and injuries.
• Games_Won: Normal distribution dependent on team strength and LeBron’s impact (WAR).
• LeBron_Jersey_Sales: Informed by LeBron's popularity and availability.
• Ticket_Sales: A nonlinear function of wins, popularity, and LeBron’s attendance.

### Revenue and Cost Drivers

• Team fixed costs: Salaries and operations of the rest of the team
• LeBron’s salary: If signed, a fixed contract of $52M
• Market research and gambling investigation costs: Each cost $1M

### Revenue streams:

• Ticket sales (impacted by wins, popularity, and LeBron’s presence)
• Merchandise (team and LeBron)
• Other fixed profits (Eg. broadcast deals, corporate parterships...)

### Outcome Measures

• Win_Championship: Derived from playoff seed based on number of wins
• Profit: Total revenue minus costs
• Profit utility: Sigmoid function mapping diminishing returns on profit
• Championship utility: Binary (1 if championship is won)
• Total utility: Weighted combination of profit and championship outcomes

## Key Insights Enabled

• Estimation of the financial and cultural value of signing a superstar
• Quantification of risks like injury and reputation damage
• Ability to assess the value of information (VOI) from market research or background checks
• Support for multi-objective decision-making under uncertainty using utility theory

## Future Enhancements

• Incorporation of additional player options for comparative analysis
• Dynamic pricing for tickets and merchandise
• Modeling playoff performance more granularly (series outcomes, team matchups)
• Integration of fan base growth and media revenue impact


