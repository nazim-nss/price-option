# 📈 Options Pricer — Black-Scholes & Monte Carlo

> Valorisation d'options européennes par deux méthodes : formule analytique (Black-Scholes) et simulation stochastique (Monte Carlo).

## Contenu du notebook

| Section | Description |
|---|---|
| **1. Paramètres** | Définition des paramètres de marché (S, K, T, r, σ) |
| **2. Black-Scholes** | Formule analytique + calcul des Greeks (Δ, Γ, ν, θ, ρ) |
| **3. Monte Carlo** | Simulation avec variables antithétiques + IC 95% |
| **4. Comparaison** | Tableau d'écarts + surface de prix 3D |
| **5. Convergence** | Graphique de convergence MC en O(1/√N) |
| **6. Vol. Implicite** | Inversion numérique (Brent) + smile + term structure |

## Prérequis

```bash
pip install numpy pandas matplotlib scipy jupyter
```

## Lancement

```bash
jupyter notebook options_pricer.ipynb
```

## Résultats clés

- Black-Scholes donne une solution fermée exacte sous ses hypothèses
- Monte Carlo converge vers BS avec une erreur en `O(1/√N)`
- Les variables antithétiques réduisent la variance de ~40%
- La volatilité implicite révèle le smile absent du modèle BS flat

## Paramètres par défaut

```
S₀ = 100  |  K = 105  |  T = 1 an  |  r = 5%  |  σ = 20%
```

## Structure

```
options-pricer/
├── options_pricer.ipynb   # Notebook principal
└── README.md
```
