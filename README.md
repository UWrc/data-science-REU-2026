# UW REU Python Data Science Workshop 2026

Training materials for the 2026 University of Washington Research Experience for Undergraduates (REU).

This workshop introduces Python and Jupyter, builds basic programming skills, and applies them to data loading, visualization, regression, and neural networks. The materials are designed for a hands-on workshop and can also be used later for self-paced practice.

## Getting started

The workshop runs in JupyterLab on the Hyak Klone cluster through UW-IT Research Computing's [Open OnDemand](https://ondemand.hyak.uw.edu/) portal.

If you do not yet have a Hyak account, follow the [Hyak account creation instructions](https://hyak.uw.edu/docs/account-creation).

Complete the introductory materials in order:

1. [Prerequisites](introduction/00-prereqs.md) — confirm your account, 2FA, and SSH client are ready.
2. [Logging in to Hyak](introduction/01-logging-in.md) — connect to UW VPN, initialize your Klone home directory, clone this repository into scratch storage space, and make it accessible from Open OnDemand.
3. [Starting JupyterLab](introduction/02-start-jupyter.md) — launch a JupyterLab session through Open OnDemand and open a Python notebook.
4. [Introduction to Jupyter](introduction/03-introduction.ipynb) — learn how to work with notebook cells, Markdown, and the Python kernel.

## Workshop materials

### 1. Python basics

The [`python_basics`](python_basics/) section covers variables, data types, built-in functions, lists and strings, libraries, loops, and conditionals.

- `01`–`07`: learner notebooks with exercises
- `S01`–`S07`: corresponding notebooks with exercise solutions

Jupyter notebooks were adapted from Software Carpentry's [Plotting and Programming in Python](https://swcarpentry.github.io/python-novice-gapminder/) and [Programming with Python](https://swcarpentry.github.io/python-novice-inflammation/).

### 2. Working with scientific data

The [`python_plotting`](python_plotting/) section introduces the Python data science ecosystem and progress from NumPy arrays to pandas DataFrames and data visualization.

- `01`–`03`: learner notebooks with exercises
- `S01`–`S03`: corresponding notebooks with exercise solutions
- [`data`](python_plotting/data/): data used by the notebooks

Learning materials were adapted from Software Carpentry's [Plotting and Programming in Python](https://swcarpentry.github.io/python-novice-gapminder/) and Jake VanderPlas's [Python Data Science Handbook](https://jakevdp.github.io/PythonDataScienceHandbook/).

### 3. Data analysis

The [`analysis`](analysis/) section applies the workshop concepts to regression with scikit-learn and neural networks with PyTorch.

- [`reu_basics-todo.ipynb`](analysis/reu_basics-todo.ipynb): participant notebook with in-session tasks to complete
- [`reu_basics.ipynb`](analysis/reu_basics.ipynb): completed reference notebook

## Using the notebooks

The notebooks are meant to be a resource for your reference after the workshop has concluded. The workshop will be a hands-on coding demonstration. The notebooks include additional practice exercises.

## Feedback

We appreciate your feedback. [Please respond to this short survey.](https://forms.cloud.microsoft/r/MSg3FtiCws)

## License and attribution

Some data and exercises are adapted from Software Carpentry materials made available under the [Creative Commons Attribution 4.0 license](https://creativecommons.org/licenses/by/4.0/). See [`python_basics/LICENSE.md`](python_basics/LICENSE.md) for attribution and details about the original materials.
