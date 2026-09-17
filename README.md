<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/hero-dark.3987cabf.svg">
    <source media="(prefers-color-scheme: light)" srcset="assets/hero-light.9232c579.svg">
    <img alt="João Filipe: optimization, integer programming and AI automation" src="assets/hero-light.9232c579.svg" width="100%">
  </picture>
</p>

<p align="center">
  <img alt="Optimization" src="https://img.shields.io/badge/Optimization-001A70?style=for-the-badge">
  <img alt="Integer programming" src="https://img.shields.io/badge/Integer%20programming-0B5FA8?style=for-the-badge">
  <img alt="Simulation" src="https://img.shields.io/badge/Quant%20logistics%20%26%20finance-0079BE?style=for-the-badge">
</p>

I build decision systems. I take an operational problem, write it down as a model, solve it with the
right tool, and then ship the result into something a person actually uses. That means an exact
formulation when the problem admits one, and a heuristic when it does not. MSc in Industrial Engineering and Management at
**Instituto Superior Técnico**, currently on exchange in Complex Systems Engineering and Management at
**TU Delft**.

Most of my work sits in one of four places: **integer programming and network design**, **supply-chain and
logistics optimization**, **quantitative finance and market simulation**, and, increasingly, **automating
the document-heavy operational work** that surrounds all three.

---

## Selected work

<img alt="Optimization and integer programming" src="https://img.shields.io/badge/Optimization%20%26%20integer%20programming-001A70?style=flat-square">

| Project | What it demonstrates | Stack |
|---|---|---|
| [Hop-constrained spanning trees](https://github.com/joaofilipe5/hop-constrained-spanning-tree) | Network design under a bound on root-to-node hops: an exact MILP alongside a constructive tree-repair heuristic, compared on generated instances | Python · PuLP/CBC · NetworkX |
| [Green hydrogen supply chain](https://github.com/joaofilipe5/GCAProject) | National-scale MIP: facility location, renewable allocation, storage, transport and investment timing, with a sensitivity study over the cost drivers | Python · PuLP/CBC · Sensitivity analysis |
| [Travelling purchaser visualizer](https://github.com/joaofilipe5/top-visualizer) | Joint purchasing and routing decisions made visible: construction heuristics and local search you can step through in the browser | React · TypeScript · Heuristics |
| [Justice operations: ML + allocation](https://github.com/joaofilipe5/PIC) | Forecasting completed court cases, then feeding those forecasts into an integer staff-allocation model | Python · Gurobi · Regression &amp; ensembles |

<img alt="Quantitative finance" src="https://img.shields.io/badge/Quantitative%20finance-0B5FA8?style=flat-square">

| Project | What it demonstrates | Stack |
|---|---|---|
| [Limit order book simulation](https://github.com/joaofilipe5/limit-order-book-simulation) | A discrete-event matching engine plus analysis of the order flow it generates: arrivals, executions, cancellations, depth and spread | Simul8 · Python · pandas |
| [Twin-win barrier payoff](https://github.com/joaofilipe5/TwinWinOption) | Monte Carlo simulation of a twin-win structure on WTI, with seeded, reproducible runs and explicit assumptions | Python · Monte Carlo · NumPy |

<img alt="Simulation and modelling" src="https://img.shields.io/badge/Simulation%20%26%20modelling-203850?style=flat-square">

| Project | What it demonstrates | Stack |
|---|---|---|
| [Antimicrobial resistance dynamics](https://github.com/joaofilipe5/antimicrobial-resistance-system-dynamics) | Stock-and-flow modelling with nonlinear calibration and scenario analysis | System dynamics · Excel · Solver |
| [Numerical methods for epidemics](https://github.com/joaofilipe5/Numerical_Methods_Epidemic) | SEIQV worm-propagation dynamics: equilibria by Newton iteration, trajectories by Heun integration | MATLAB · ODEs · Root finding |

<details>
<summary><b>More repositories</b>: smaller or older work, kept for the record</summary>

<br>

| Project | Note |
|---|---|
| [Traffic flow simulation](https://github.com/joaofilipe5/traffic-flow-simulation) | Exploratory animation of stochastic arrivals, signal phases and queue spacing |
| [US elections sentiment](https://github.com/joaofilipe5/US_Elections_Sentiment) | Lexicon sentiment and keyword grouping over Reddit discussion titles |
| [PortfolioCalc](https://github.com/joaofilipe5/PortfolioCalc) | Early portfolio-metrics prototype; its README documents the methodology limits rather than hiding them |

</details>

Each repository states what it needs to run, where its outputs are, and where its conclusions stop.
Group coursework credits its full team.

---

## How a problem becomes a decision

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/pipeline-dark.7eab4eff.svg">
    <source media="(prefers-color-scheme: light)" srcset="assets/pipeline-light.833490f5.svg">
    <img alt="Operational data to formulation, to an exact MILP or heuristics, to bounds and sensitivity, to a decision and the automation it ships into, with the outcome fed back" src="assets/pipeline-light.833490f5.svg" width="100%">
  </picture>
</p>

Most of what I build reduces to the same shape. Choose what to open, and assign demand to it, at least cost:

$$
\begin{aligned}
\min_{x,y} \quad & \sum_{i \in F} f_i y_i + \sum_{i \in F} \sum_{j \in C} c_{ij} x_{ij} \\
\text{subject to} \quad & \sum_{i \in F} x_{ij} = 1 \quad \forall j \in C \\
& x_{ij} \le y_i \quad \forall i \in F, \quad j \in C \\
& \sum_{j \in C} d_j x_{ij} \le K_i y_i \quad \forall i \in F \\
& x_{ij} \ge 0, \quad y_i \in \lbrace 0, 1 \rbrace
\end{aligned}
$$

Facilities, hydrogen plants, court staff, hops in a tree, purchases on a route. The objects change, the
discipline does not. State the decision variables, defend every constraint, report the bound alongside
the answer, and say where the model stops being trustworthy.

---

## Private work

<img alt="Private repositories" src="https://img.shields.io/badge/PRIVATE-CODE%20NOT%20PUBLIC-203850?style=for-the-badge&labelColor=0079BE">

I build and maintain two systems for a **Portuguese freight forwarder**. Both repositories are
private and the client is not named, so these summaries stand in for code I cannot link.

### Operations platform &nbsp; <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white"> <img alt="PostgreSQL" src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"> <img alt="Status: preparing for rollout" src="https://img.shields.io/badge/status-preparing%20for%20rollout-0079BE?style=flat-square&labelColor=203850">

This is the system the company uses to run a shipment from start to finish. The work used to live
in spreadsheets and email.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/platform-dark.ed45b6aa.svg">
    <source media="(prefers-color-scheme: light)" srcset="assets/platform-light.4117dcc3.svg">
    <img alt="Email and files feed the five stages of a shipment: quote, award, operation, documents, delivery. One record holds price, cost, margin and access for all of them." src="assets/platform-light.4117dcc3.svg" width="100%">
  </picture>
</p>

Everything about a shipment sits in one record. The quote, the costs, the documents and the
delivery are all in the same place, and each person sees only the part their role allows.

It also handles the money. What the client pays, what the shipment costs, the margin, and freight
in more than one currency.

It reads the company mailbox and turns those messages into records, so nobody copies data by hand.

It is written in TypeScript. The data lives in PostgreSQL, with the rules that matter written into
the database itself.

The documentation has one rule: **the code wins**. If a document disagrees with the code, the
document is wrong and gets fixed. Every claim about the business is marked with where it came
from: how the industry works, how this company works, or what the code does. When two sources
disagree, the rule is to stop and ask.

**Where it stands.** It is being prepared for rollout. Everything is built and tested end to end.
There is no hosting or scheduler yet, and it has not run on a real shipment.

### Customs filing automation &nbsp; <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black"> <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white"> <img alt="OCR" src="https://img.shields.io/badge/OCR-Tesseract-0B5FA8?style=flat-square&labelColor=203850">

A Chrome extension that fills in a government customs portal, so the team stops retyping the same
numbers. It works in both directions of the warehouse, goods in and goods out.

It reads the customs declaration and the shipping documents, including scanned ones, using OCR. It
matches each line of cargo to the right document by comparing figures that appear in both.

**It never submits the form.** It fills the fields it can. It checks the fields it cannot change
against the source documents and marks each one pass or fail. It shows anything the portal would
reject. Then it stops, and a person presses the button.

It also builds as a userscript, for computers where extensions are blocked.

---

## Toolkit

<p align="center">
  <img alt="Python" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" height="36">
  &nbsp;&nbsp;
  <img alt="C++" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/cplusplus/cplusplus-original.svg" height="36">
  &nbsp;&nbsp;
  <img alt="C" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" height="36">
  &nbsp;&nbsp;
  <img alt="TypeScript" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-original.svg" height="36">
  &nbsp;&nbsp;
  <img alt="React" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg" height="36">
  &nbsp;&nbsp;
  <img alt="R" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/r/r-original.svg" height="36">
  &nbsp;&nbsp;
  <img alt="MATLAB" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/matlab/matlab-original.svg" height="36">
  &nbsp;&nbsp;
  <img alt="PostgreSQL" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/postgresql/postgresql-original.svg" height="36">
  &nbsp;&nbsp;
  <img alt="NumPy" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/numpy/numpy-original.svg" height="36">
  &nbsp;&nbsp;
  <img alt="scikit-learn" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/scikitlearn/scikitlearn-original.svg" height="36">
  &nbsp;&nbsp;
  <img alt="PyTorch" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/pytorch/pytorch-original.svg" height="36">
  &nbsp;&nbsp;
  <img alt="Jupyter" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/jupyter/jupyter-original.svg" height="36">
</p>

<p align="center">
  <img alt="pandas" src="https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white">
  <img alt="LaTeX" src="https://img.shields.io/badge/LaTeX-008080?style=flat-square&logo=latex&logoColor=white">
  <img alt="Gurobi" src="https://img.shields.io/badge/Gurobi-EE3524?style=flat-square">
  <img alt="CBC" src="https://img.shields.io/badge/CBC-203850?style=flat-square">
  <img alt="PuLP" src="https://img.shields.io/badge/PuLP-203850?style=flat-square">
  <img alt="Simul8" src="https://img.shields.io/badge/Simul8-203850?style=flat-square">
  <img alt="Stata" src="https://img.shields.io/badge/Stata-1A476F?style=flat-square">
  <img alt="Power BI" src="https://img.shields.io/badge/Power%20BI-F2C811?style=flat-square">
  <img alt="Excel" src="https://img.shields.io/badge/Excel-217346?style=flat-square">
</p>

Core interests: integer and mixed-integer programming, network design, heuristics and local
search, **parallel computing**, discrete-event and system-dynamics **simulation**, supply-chain
and logistics optimization, market microstructure, and reproducible modelling.

---

## Background

- <img alt="Instituto Superior Técnico" src="assets/logo-ist.204a6456.png" height="28"> &nbsp; **MSc, Industrial Engineering and Management**, Instituto Superior Técnico, 2025–2027 · current GPA **18.2/20**. **BSc** in the same programme, 2022–2025.
- <img alt="TU Delft" src="assets/logo-delft.ac2c2a12.png" height="28"> &nbsp; **Exchange semester** at TU Delft, Complex Systems Engineering and Management, September–December 2026.
- <img alt="Efficio" src="assets/logo-efficio.3d7a528a.png" height="28"> &nbsp; **Consulting intern at Efficio.** Spend analysis, supplier assessment and sourcing decisions.
- <img alt="Técnico Investment Club" src="assets/logo-tic.f0bbdb4d.png" height="28"> &nbsp; **Vice President / Head of Asset Management, Técnico Investment Club.** Portfolio risk visualization, optimization and simulation.

**Languages:** Portuguese (native) · English (fluent, Cambridge Advanced).

---

<p align="center">
  <a href="https://www.linkedin.com/in/jo%C3%A3o-filipe-495848249/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-001A70?style=for-the-badge&logo=linkedin&logoColor=white"></a>
  &nbsp;
  <a href="mailto:joaofilipe.contact@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-0079BE?style=for-the-badge&logo=maildotru&logoColor=white"></a>
  &nbsp;
  <a href="https://github.com/joaofilipe5?tab=repositories"><img alt="All repositories" src="https://img.shields.io/badge/All%20repositories-203850?style=for-the-badge&logo=github&logoColor=white"></a>
</p>
