# LeBron-Acquisition-Bayesian-Analysis
This project features a Bayesian decision model to evaluate whether a particular NBA team (Toronto Raptors) should offer LeBron James a contract in an effort to acquire him in Free Agency

## Overview
This project applies probabilistic modeling, Bayesian inference, and decision analysis to evaluate a high-stakes strategic question for an NBA team: Should the team sign LeBron James? The goal is to integrate financial, performance, risk, and reputational factors into a comprehensive, data-driven framework to guide decision-making under uncertainty.

Using a Bayesian Network implemented in PyMC, the model simulates various real-world scenarios to estimate the expected utility of signing (or not signing) LeBron under different informational and operational strategies—such as conducting market research, requesting gambling background checks, or making decisions blindly.

⚙️ Tools and Technologies
PyMC – Probabilistic programming in Python for Bayesian modeling

ArviZ – Exploratory analysis of Bayesian models and MCMC diagnostics

NumPy – Scientific computing and numerical operations

Matplotlib – Visualization of probabilistic outputs and diagnostic plots

Jupyter Notebooks (optional) – For interactive development and interpretation

📊 Core Components & Model Structure
The decision model evaluates the expected utility of six plausible decision strategies, each involving a combination of the following actions:

Acquire LeBron James or not

Conduct market research to assess public interest/popularity

Request a gambling investigation to assess off-court risk

For each scenario, the following stochastic variables and dependencies are modeled:

🧠 Decision and Observation Nodes
Popularity: Modeled with a Beta distribution. Observable via market research.

Gambling and Caught: Indicates off-court risk; observable through optional investigation.

LeBron_Games_Missed: Modeled as a Gamma distribution to simulate injury risk.

LeBron_Games_Played: A deterministic function dependent on acquisition and injuries.

Games_Won: Normal distribution dependent on team strength and LeBron’s impact (WAR).

LeBron_Jersey_Sales: Informed by LeBron's popularity and availability.

Ticket_Sales: A nonlinear function of wins, popularity, and LeBron’s attendance.

💸 Revenue and Cost Drivers
Team fixed costs: Salaries and operations of the rest of the team

LeBron’s salary: If signed, a fixed contract of $52M

Market research and gambling investigation costs: Each cost $1M

Revenue streams:

Ticket sales (impacted by wins, popularity, and LeBron’s presence)

Merchandise (team and LeBron)

Other fixed profits

🏆 Outcome Measures
Win_Championship: Derived from playoff seed based on number of wins

Profit: Total revenue minus costs

Utility:

Profit utility: Sigmoid function mapping diminishing returns on profit

Championship utility: Binary (1 if championship is won)

Total utility: Weighted combination of profit and championship outcomes
