# Applied Stochastic Processes (MATH F424)

[![Python](https://img.shields.io/badge/Python-3.12+-3776AB?style=flat&logo=python&logoColor=white)](https://www.python.org/)
[![Package Manager](https://img.shields.io/badge/uv-Package%20Manager-DE5FE9?style=flat)](https://github.com/astral-sh/uv)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?style=flat&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License](https://img.shields.io/badge/license-Academic-blue.svg)](LICENSE)

A comprehensive repository for **Applied Stochastic Processes (MATH F424)**, featuring analytical derivations, mathematical modeling, and Monte Carlo simulations implemented in Python and Jupyter Notebooks.

---

## 📌 Repository Contents

```text
ASP/
├── ASP Assignment.ipynb                       # Course assignment notebook
├── ASP_Assignment_Complete.ipynb              # Complete assignment solution & analysis
├── ASP 2026_Lab Resources/                    # Laboratory modules and resources
│   ├── ASP_Stationarity.ipynb                 # Stationarity tests and long-run behavior
│   ├── New_DTMC.ipynb                         # Discrete-Time Markov Chains
│   ├── CTMC.ipynb                             # Continuous-Time Markov Chains
│   ├── BM.ipynb                               # Brownian Motion & Wiener processes
│   ├── Branching_Process/                     # Galton-Watson branching process
│   │   ├── branching_process.ipynb            # Analytical & Monte Carlo simulations
│   │   ├── offspring_distribution.csv         # Offspring probability distribution
│   │   ├── analytical_expectation.csv         # Theoretical expectation values
│   │   ├── sample_paths.csv                   # Simulated sample paths
│   │   └── simulation_summary.csv             # Summary metrics
│   └── Renewal_Process/                       # Renewal theory & reward processes
│       ├── renewal_process_light_bulb_explainer.ipynb
│       ├── renewal_analytical_long_run.csv    # Long-run theoretical limits
│       ├── renewal_interarrival_distribution.csv
│       ├── renewal_sample_paths.csv           # Path simulations
│       └── renewal_simulation_summary.csv     # Convergence and metrics
├── pyproject.toml                             # Project dependencies and configuration
├── uv.lock                                    # Deterministic uv dependency lockfile
├── .gitignore                                 # Git ignore rules (checkpoints, env, caches)
└── README.md                                  # Repository documentation
```

---

## 🔬 Core Topics Covered

### 1. Cyber-Incident Escalation (Course Assignment)
* **Model:** Absorbing Discrete-Time Markov Chain (DTMC).
* **State Space:** 
  * Transient States: $\mathcal{T} = \{\text{Green } (G), \text{Yellow } (Y), \text{Orange } (O), \text{Red } (R)\}$
  * Absorbing States: $\mathcal{A} = \{\text{Contained } (C), \text{Breached } (B)\}$
* **Key Analyses:**
  * Fundamental Matrix calculation: $N = (I - Q)^{-1}$
  * Absorption probabilities: $B = N R$
  * Expected time to absorption: $\mathbf{t} = N \mathbf{1}$
  * Probability of breach within $k$ hours: $\Pr(T_B \le 24)$ via matrix exponentiation $P^k$
  * Cost modeling: Running costs ($c$) vs. Terminal containment / breach penalties ($g$)

### 2. Discrete-Time Markov Chains (DTMC) & Stationarity
* Transition probability matrices, irreducibility, and aperiodicity.
* Stationary distributions $\pi = \pi P$ and convergence criteria.
* Hitting times, absorption probabilities, and recurrence.

### 3. Continuous-Time Markov Chains (CTMC)
* Transition rate matrices ($Q$-matrix / infinitesimal generator).
* Kolmogorv forward and backward differential equations.
* Holding times (exponential distributions) and embedded jump chains.

### 4. Branching Processes (Galton-Watson)
* Probability Generating Functions (PGFs): $G_X(s) = \mathbb{E}[s^X]$.
* Extinction probability: $\eta = \min \{ s \in [0, 1] : G(s) = s \}$.
* Mean and variance propagation across generations: $\mathbb{E}[Z_n] = \mu^n$.
* Monte Carlo simulations vs. analytical predictions.

### 5. Renewal Theory & Renewal Reward Processes
* Interarrival distribution modeling and renewal function $M(t) = \mathbb{E}[N(t)]$.
* Elementary Renewal Theorem and Blackwell's Theorem.
* Application: **Light Bulb Replacement Problem** (Renewal Reward Theorem for long-run cost optimization).

### 6. Brownian Motion (Wiener Process)
* Independent and Gaussian increments: $W(t) - W(s) \sim \mathcal{N}(0, t - s)$.
* Standard Brownian motion, drift, and geometric Brownian motion.
* First passage times and sample path properties.

---

## 🚀 Getting Started

### Prerequisites
* **Python 3.12+**
* [**uv**](https://github.com/astral-sh/uv) (recommended) or standard `pip`

### Installation

#### Option 1: Using `uv` (Fastest & Recommended)
```bash
# Clone the repository
git clone https://github.com/uday-lathar/ASP.git
cd ASP

# Create virtual environment and install dependencies from uv.lock
uv sync

# Launch Jupyter Lab or Notebook
uv run jupyter lab
```

#### Option 2: Using standard `pip`
```bash
# Clone the repository
git clone https://github.com/uday-lathar/ASP.git
cd ASP

# Create and activate virtual environment
python3 -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install required dependencies
pip install ipykernel pandas numpy scipy matplotlib networkx

# Start Jupyter
jupyter notebook
```

---

## 🛠️ Tech Stack & Libraries

* **Language:** Python 3.12+
* **Environment:** Jupyter Notebooks (`ipykernel`)
* **Scientific Computing:** `numpy`, `scipy`
* **Data Manipulation:** `pandas`
* **Visualization:** `matplotlib`
* **Graph & Network Theory:** `networkx`
* **Package Management:** `uv`

---

## 📄 License & Academic Note

This repository contains academic coursework, laboratory exercises, and assignment solutions for Applied Stochastic Processes. If referencing this work for coursework or projects, please adhere to relevant academic integrity guidelines.
