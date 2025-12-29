<div style="
    background-color: #439cc8; 
    color: #fff; 
    font-size: 16px; 
    font-style: italic; 
    padding: 10px 15px; 
    margin-bottom: 15px; 
    border-radius: 8px;">
<h2>Statistiques descriptives</h2>
</div>

- Mesure de tendance centrale
	- moyenne arythmétique
	- moyenne géométrique
	- moyenne harmonique
	- moyenne quadratique
	- médiane
	- mode
- Mesure de dispersion
- Distribution

## Mesure de tendance centrale
### moyenne arythmétique `np.mean`
Somme des valeurs divisée par leur nombre<br>
Donne le centre des données mais tres sensible au valeurs extrêmes
#### moyenne géométrique `scipy.stats.gmean(variable)`
moyenne multiplicative<br>
robuste aux valeurs extrêmes<br>
non définie pour les valrurs négztives ou nulles
conseillées pour les données qui varient de manère multiplicative
#### moyenne harmonique `scipy.stats.hmean(variable)`
moyenne des inverses<br>
très sensible aux faibles valeurs<br>
conseillées pour les taux et ratios<br>
tres influencé par les valeurs proches de zéro
#### moyenne quadratique `np.sqrt(np.mean(np.square(variable)))`
moyenne des carrés<br>
utile pour l'analyse de variance
conseillées pour les données qui concernent l'énergie, la puissance
sensible aux valeur extremes

### Médiane
`np.median(variable)`<br>
`df['column'].median()`<br>
Le point milieu d'un jeu de données<br>
si le nombre de données est apir, ilfaut faire la moyenne des 2 valeurs centrales<br>
50 % des unités ont une valeur inférieure ou égale à la médiane
50 % des unités ont une valeur supérieure ou égale**
robuste aux valeurs extrêmes

### Mode `modes = df['column'].mode().tolist()`
valeur la plus présente<br>
s'applique aux variables numériques et catégorielles


## Mesure de dispersion



###  Étendue  $= X_{\max} - X_{\min}$ `np.ptp(data)`

numpy fonction peaktopeak `np.ptp()`
– Mesure la distance entre la plus grande et la plus petite valeur<br>
– C’est simple et rapide pour avoir une idée du "span" des données<br>
– Très sensible aux valeurs extrêmes (outliers)<br>
– Ne dit rien sur la distribution des autres valeurs

---

### Quartile, écart interquartile, bornes
Le Quartile divise les données en 4 parties égales :
- Q1 valeur en dessous de laquelle se trouve 25 % des données
- Q2 est la médiane qui divise les données en 2
- Q3 valeur au dessus de laquelle se trouve 25 % des données
- Q3 - Q1 = écart interquartile contient 50 % des valeurs d'un jeu de données
- bornes inf et supérieur : au dela, les valeurs sont considérées come des outliers
- bornes inférieure = Q1 - 1,5 écart interquartile
- bornes supérieure = Q1 - 1,5 écart interquartile

|     Quartile / IQR   |     Numpy             |    Pandas   |
| -------------------- | --------------------- | ----------- |
| Q1   | `q1 = np.percentile(data, 25)`    | `series.quantiles(0,25)` |
| Q3   | `q2 = np.percentile(data, 75)`   |  `series.quantiles(0,75)` |
| IQR | `iqr = q3 - q1`  |  |
| Borne inférieure   | `q1 - 1.5*iqr`   |   |
| Borne supérieure   | `q3 + 1.5*iqr`   |   |

---



###  Variance :


$${Var}(X) = \frac{1}{n} \sum_{i=1}^{n} (X_i - \bar{X})^2$$

– Mesure la dispersion moyenne des valeurs autour de la moyenne.  
– Chaque écart est mis au carré pour éviter que les écarts positifs et négatifs ne s'annulent.

Si on travaille sur un **échantillon**, on divise par $n - 1$ au lieu de $n$ :

$${Var}(X) = \frac{1}{n - 1} \sum_{i=1}^{n} (X_i - \bar{X})^2$$
---
### Écart-type :

$$\sigma_X = \sqrt{{Var}(X)}$$

La racine carrée de la variance : il s’exprime dans la même unité que les données (contrairement à la variance).

|                            |                                                     |       |
| -------------------------- | --------------------------------------------------- | ----- |
| **Ecart-type    $\sigma$** | $\sqrt{\text{variance}}$                            | sigma |
| **variance**               | moyenne des ( écarts par rapport à la moyenne )$^2$ |       |


|Mesure|Cas d’usage|Sensibilité aux valeurs extrêmes|
|---|---|---|
|Étendue|Repérer rapidement l’amplitude des données|Très sensible|
|Variance / écart-type|Étudier la dispersion globale (utile en statistique, modélisation)|Sensible, mais moins qu’une simple étendue|


---

| Terme            | Définition courte                                                                                                                       |
| ---------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| **Centrer**      | Soustraire la **moyenne** → valeurs réparties autour de 0                                                                               |
| **Réduire**      | Diviser par l’**écart-type** → met toutes les variables sur une échelle comparable                                                      |
| **Standardiser** | **Centrer + Réduire** → moyenne = 0, écart-type = 1                                                                                     |
| **Normaliser**   | **Ramener dans un intervalle fixe** (souvent $0,1$) → met toutes les valeurs à la même échelle sans changer la forme de la distribution |


<div style="
    background-color: #439cc8; 
    color: #fff; 
    font-size: 16px; 
    font-style: italic; 
    padding: 10px 15px; 
    margin-bottom: 15px; 
    border-radius: 8px;">
<h2>Statistiques inferentielles</h2>
</div>