# Loi de probabilité discrète

## Loi de Poisson

Modélise le **nombre d’événements rares** sur un intervalle donné (temps, espace, surface…).

### Hypothèses

* événements **indépendants**
* taux moyen **constant**
* probabilité d’un événement sur un intervalle très petit **faible**
* pas d’événements simultanés

### Paramètre

* **λ (lambda)** : intensité du phénomène
  → moyenne du nombre d’événements

### Propriétés

* **Espérance** : `E(X) = λ`
* **Variance** : `Var(X) = λ`

### Loi

$$
P(X = k) = \frac{e^{-λ} λ^k}{k!}, \quad k \in \mathbb{N}
$$

### Exemples

* nombre d’appels par minute
* défauts rares sur une chaîne de production
* arrivées de clients

---

## Loi de Bernoulli

Modélise une **expérience aléatoire à deux issues**.

### Issues

* `1` : succès
* `0` : échec

### Paramètre

* **p** : probabilité de succès (`P(X = 1)`)

### Propriétés

* **Espérance** : `E(X) = p`
* **Variance** : `Var(X) = p(1 − p)`

### Exemples

* oui / non
* succès / échec
* pile / face

---

## Loi Binomiale

Modélise le **nombre de succès** dans **n expériences de Bernoulli indépendantes**.

### Paramètres

* **n** : nombre d’essais
* **p** : probabilité de succès

### Loi

$$
P(X = k) = \binom{n}{k} p^k (1 - p)^{n - k}
$$

### Propriétés

* **Espérance** : `E(X) = np`
* **Variance** : `Var(X) = np(1 − p)`

### Exemples

* nombre de succès sur `n` essais
* nombre de pièces défectueuses sur un lot

---

## 🔗 Liens entre les lois

* **Bernoulli** → 1 seul essai
* **Binomiale** → somme de Bernoulli
* **Poisson** ≈ Binomiale si :

  * `n` grand
  * `p` petit
  * `λ = np`

---

## Mémo rapide

* **Bernoulli** : oui / non
* **Binomiale** : plusieurs Bernoulli
* **Poisson** : événements rares
* **Poisson** : `E(X) = Var(X) = λ`


