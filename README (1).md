# Pricer d'Options — Black-Scholes & Monte Carlo

Ce projet calcule le prix d'options financières de deux façons différentes,
et compare les résultats avec des graphiques.

C'est un projet de finance quantitative réalisé en Python.

---

## C'est quoi une option ?

Une option financière, c'est un contrat qui donne le **droit** (mais pas l'obligation)
d'acheter ou de vendre une action à un prix fixé à l'avance.

- Un **CALL** → droit d'**acheter** l'action à un prix fixé (utile si on pense que ça va monter)
- Un **PUT**  → droit de **vendre** l'action à un prix fixé (utile si on pense que ça va baisser)

La grande question : **combien vaut ce droit ?** C'est ce que ce projet calcule.

---

## Les deux méthodes utilisées

### 1. Black-Scholes (formule directe)
Une formule mathématique développée en 1973 qui donne le prix exact de l'option
en quelques millisecondes. Elle repose sur des hypothèses simplificatrices
(marchés parfaits, volatilité constante...).

### 2. Monte Carlo (simulation)
On simule des milliers de scénarios possibles pour le futur prix de l'action,
on calcule combien vaudrait l'option dans chaque scénario, et on fait la moyenne.
Plus lent, mais beaucoup plus flexible que Black-Scholes.

---

## Contenu du projet

| Section | Ce qu'on fait |
|---|---|
| **1. Paramètres** | On définit le prix actuel de l'action, le strike, la durée, le taux et la volatilité |
| **2. Black-Scholes** | On calcule le prix exact + les "Greeks" (sensibilités du prix) |
| **3. Monte Carlo** | On simule 200 000 scénarios et on estime le prix |
| **4. Comparaison** | On compare les deux méthodes dans un tableau et des graphiques |
| **5. Convergence** | On montre que Monte Carlo devient plus précis quand on simule plus |
| **6. Vol. Implicite** | On retrouve la volatilité cachée derrière un prix de marché observé |

---

## Paramètres utilisés par défaut

```
Prix de l'action  S₀ = 100 €
Strike            K  = 105 €
Durée             T  =   1 an
Taux sans risque  r  =   5 %
Volatilité        σ  =  20 %
```

---

## Installation

Avoir Python installé, puis lancer :

```bash
pip install numpy pandas matplotlib scipy jupyter
```

## Lancement

```bash
jupyter notebook options_pricer.ipynb
```

---

## Ce qu'on observe

- Black-Scholes et Monte Carlo donnent des résultats très proches (écart < 0.01€)
- Monte Carlo devient plus précis quand on augmente le nombre de simulations
- La volatilité implicite montre que le marché réel est plus complexe que le modèle

---

## Structure du projet

```
options-pricer/
├── options_pricer.ipynb   # Le notebook principal (code + explications)
└── README.md              # Ce fichier
```