# BIT2118 Scientific Computing

## Project Overview

This repository contains our group coursework for **BIT2118 - Scientific Computing**. It demonstrates how Python can be used to translate mathematical models into numerical algorithms, test the algorithms, visualise their behaviour, and interpret the results in practical situations.

The work is organised into three sections:

| Section | Purpose |
| --- | --- |
| [Tasks 1-8](./TASK%201-8/) | Foundational scientific-computing exercises and introductory task work. |
| [Tasks 9-12](./numerical-methods-task-9-12/) | Structured numerical-method implementations with automated tests, plots, and written results. |
| [Tasks 13-20](./TASK%2013-20/) | Applied examples covering interpolation, calculus, differential equations, optimisation, and simulation. |

The repository is intended to show both the **mathematical method** and the **computational evidence** produced by that method.

## What the Project Demonstrates

Across the twenty tasks, the project demonstrates how to:

- represent mathematical problems as Python functions and data;
- use numerical methods when an exact solution is difficult or unavailable;
- compare methods and investigate convergence and accuracy;
- use NumPy, SciPy, and Matplotlib for scientific computation;
- test numerical results against expected mathematical conditions;
- explain assumptions, parameter changes, limitations, and real-world meaning.

## Repository Guide

### Tasks 1-8: Foundations

The [Tasks 1-8](./TASK%201-8/) directory contains the introductory coursework exercises. The section notes explain the mathematical ideas and the expected work for each task. The individual task files are stored directly in that directory.

### Tasks 9-12: Numerical Methods with Tests

This is the most structured and testable part of the repository. Source code is in `numerical-methods-task-9-12/tasks/`, tests are in `numerical-methods-task-9-12/tests/`, and generated figures and interpretations are in `numerical-methods-task-9-12/outputs/`.

| Task | Method | Example application | Main file |
| --- | --- | --- | --- |
| 9 | Eigenvalues, eigenvectors, and eigenvector centrality | Analysing the importance of locations in a campus network | `task_09_eigenvalues.py` |
| 10 | Bisection and fixed-point iteration | Finding greenhouse temperature equilibrium | `task_10_bisection_fixed_point.py` |
| 11 | Newton-Raphson and secant methods | Estimating the internal rate of return for a solar-pumping investment | `task_11_newton_secant.py` |
| 12 | Solving a nonlinear system | Finding intersections for a reservoir and embankment design | `task_12_nonlinear_equations.py` |

The section's [`outputs/execution_results.md`](./numerical-methods-task-9-12/outputs/execution_results.md) file records the numerical results and interpretations. The PNG files in the same directory show convergence, heat balance, network centrality, and geometric intersections.

### Tasks 13-20: Applied Numerical Computing

The [Tasks 13-20](./TASK%2013-20/) directory applies additional numerical techniques to practical examples:

| Task | Technique | Example application | Main file |
| --- | --- | --- | --- |
| 13 | Linear interpolation | Estimating a temperature between measured values | `task 13 Interpolation.py` |
| 14 | Curve fitting | Predicting server response time from user load | `TASK14 Curve_fitting.py` |
| 15 | Numerical differentiation | Estimating vehicle speed from GPS position data | `Task-15-Numerical-Differentiation.py` |
| 16 | Numerical integration | Estimating energy consumption from smart-meter readings | `Task-16-Numerical-Integration.py` |
| 17 | Euler's method for ODEs | Modelling Newton's law of cooling | `task 17 Euler's Method.py` |
| 18 | SciPy `solve_ivp()` for ODEs | Simulating an RC charging circuit | `task 18 solve_ivp().py` |
| 19 | Numerical optimisation | Minimising the operating cost of a server configuration | `task 19 minimize().py` |
| 20 | Monte Carlo simulation | Estimating the probability that demand exceeds stock | `TASK -20 -monte_carlo.py` |

The section-level [readme](./TASK%2013-20/readme.md) gives the mathematical background, real-world interpretation, and suggested parameter experiments for these tasks.

## How to Run the Project

### Requirements

Install Python 3.10 or later. Tasks 9-12 require the packages listed in `numerical-methods-task-9-12/requirements.txt`:

```text
numpy
scipy
matplotlib
pytest
```

### Run Tasks 9-12

From the repository root:

```powershell
cd numerical-methods-task-9-12
python -m pip install -r requirements.txt
```

Run an individual task:

```powershell
python -m tasks.task_09_eigenvalues
python -m tasks.task_10_bisection_fixed_point
python -m tasks.task_11_newton_secant
python -m tasks.task_12_nonlinear_equations
```

These programs print numerical results and generate plots in the `outputs/` directory.

### Run the Automated Tests

From inside `numerical-methods-task-9-12`:

```powershell
pytest -v
```

The tests verify the core calculations, including centrality, root finding, Newton/secant results, and nonlinear-equation solutions. They also check invalid input such as a non-square matrix where appropriate.

### Run Tasks 13-20

The files in `TASK 13-20` are standalone Python scripts. From the repository root, run a script using quotes because some filenames contain spaces or punctuation:

```powershell
python ".\TASK 13-20\task 13 Interpolation.py"
python ".\TASK 13-20\TASK14 Curve_fitting.py"
python ".\TASK 13-20\Task-15-Numerical-Differentiation.py"
python ".\TASK 13-20\Task-16-Numerical-Integration.py"
python ".\TASK 13-20\task 17 Euler's Method.py"
python ".\TASK 13-20\task 18 solve_ivp().py"
python ".\TASK 13-20\task 19 minimize().py"
python ".\TASK 13-20\TASK -20 -monte_carlo.py"
```

These scripts may display plots or print calculated values. Run them one at a time so that each result can be observed and discussed.

## How to Read and Assess the Results

For each task, follow this sequence:

1. Read the mathematical concept and identify the input data and assumptions.
2. Open the corresponding Python file and identify the implemented formula or algorithm.
3. Run the file and record the numerical result and any generated plot.
4. Change the suggested parameter, such as the step size, number of intervals, heat gain, cash flow, or number of Monte Carlo trials.
5. Compare the original and modified results.
6. Explain whether the result is accurate, convergent, stable, and meaningful for the stated application.

The important evidence is not only the final number. It is the connection between the mathematical model, the algorithm, the computed output, and the interpretation.

## Assumptions and Limitations

The examples use simplified models and illustrative data. Their results depend on the selected inputs, initial guesses, step sizes, stopping criteria, and convergence assumptions. A numerical answer is therefore an approximation within the stated model; it is not automatically a measurement of a real-world system.

Some scripts are designed for demonstration and exploration, while the Tasks 9-12 package has the clearest automated validation. Plots and generated output should be interpreted together with the source code and the written explanations.

## Collaboration

This is a group project maintained with Git and GitHub. Work can be organised by task section or individual task. A typical workflow is:

```text
git pull
git checkout -b feature/task-description
# edit and test the assigned task
git add .
git commit -m "Implement BIT2118 task"
git push -u origin feature/task-description
```

Changes should be reviewed before they are merged into `main`.

## Academic Information

| Item | Details |
| --- | --- |
| Course code | BIT2118 |
| Course | Scientific Computing |
| Project | Numerical Methods and Scientific Computing |
| Language | Python |
| Destination repository | [SCIENTIFIC-COMPUTING-GROUP-WORK](https://github.com/AlvinCharles001/SCIENTIFIC-COMPUTING-GROUP-WORK) |

## Contributors

This repository is a collaborative coursework submission. Contributions are organised around the task sections and the responsibilities of the group members.
