### Conventions

| Écriture                  | Signification                                 | Exemple                 | Lecture                                                   |
| ------------------------- | --------------------------------------------- | ----------------------- | --------------------------------------------------------- |
| $P(A)$                    | Probabilité de l’événement $A$                | $P(\text{pile}) = 0.5$  | La probabilité de pile est 0,5                       |
| $P(A \cap B)$             | Probabilité conjointe de $A$ et $B$           | $P(A \cap B)$           | La probabilité que A et B se produisent simultanément|
| $P(A \cup B)$             | Probabilité de $A$ ou $B$                     | $P(A \cup B)$           | La probabilité que A ou B se produise                |
| $P(A \mid B)$             | Probabilité conditionnelle de $A$ sachant $B$ | $P(A \mid B)$           | La probabilité de A sachant que B est réalisé        |
| $P(\bar{A})$ ou $P(A^c)$  | Probabilité de non-$A$                        | $P(\bar{A}) = 1 - P(A)$ | La probabilité que A ne se produise pas              |
| $P(B \setminus A)$        | Probabilité de $B$ sans $A$                   | $P(B \setminus A)$      | La probabilité de B mais pas A                       |
| $P(A_1, A_2, \dots, A_n)$ | Probabilité jointe de plusieurs événements    | $P(X=2, Y=3)$           | La probabilité que X=2 et Y=3                        |
| $P(X = x)$                | Loi de probabilité d’une variable aléatoire   | $P(X = 5)$              | Probabilité que la variable $X$ prenne la valeur 5   |





**A∩B** 
- se lit "A **intersection** B" ou  " A inter B"
- sous-ensemble de  Ω qui contient les éléments qui sont à la fois dans A et dans B

**A∪B**
- se lit "<font color="orange">A union B</font>"
- le sous-ensemble de  Ω qui contient les éléments qui sont soit dans A , soit dans B

A = {1,3,5}
B = {3,6}
A∪A = Ω
A∩A = ∅
A∩B={3}
A∪B={1,3,5,6}


##### Probabilité conditionnelle
$$P(A∣B)= \frac{P(A∩B)}{P(B)} \quad\text{si P(B)>0}$$
​ 



| Terme | Définition |
| ----- | ---------- |
|<font color="orange">Univers</font> ==Ω== (Omega )<br>ou<br><font color="orange">ensemble fondamental</font> | <br>**ensemble fini ou infini** des issues possibles |
|<font color="orange">expérience aléatoire</font> | on connait l'==Ω== mais pas  le résultat :<br>Toutes les issues sont connues,<br>mais laquelle sera  réalisée ?<br>le résultat est imprévisible |
| <font color="orange">cardinal</font> d'un ensemble fini A<br>noté <font color="orange">\|A\|</font>| nombre d'éléments que contient l'ensemble|

Si
- le nombre d'issue de l'expérience est fini
- les issues sont équiprobable
Alors :
- probabilité d'un évènement =  cardinal de l'évènement / cardinal de son univers
  $P(A)=∣A∣ / ∣Ω∣​$


lancer de dé
==Ω = {1, 2, 3, 4, 5, 6}==

<font color="orange">événements </font>(sous ensemble) par exemple :
A = {1}
B = {2, 3, 5}
C = {5, 6}
...

### tribu d'évènement

L'ensemble des sous-ensemble  ==p(Ω)==   ==p de oméga==
est une <font color="orange">tribu d'évènements</font> associé à l'expérience aléatoire

### espace probabilisable
<font color="orange">couple univers / tribu d'événement</font>
espace probabilisable associé à l'expérience aléatoire   :

par exemple ==(Ω, p(Ω))==



<font color="orange">Univers</font>  Ω  est l'ensemble des résultats possibles
	<font color="orange">tribu d'événements</font> T ou ==p(Ω)== 

| Ensemble des parties de l'ensemble `E = {a,b,c}`                |                     |
| --------------------------------------------------------------- | ------------------- |
|                                                                 |                     |
| le sous ensemble vide                                           | `∅`                 |
| les sous-ensembles qui contiennent un seul élément (singletons) | `{a},{b},{c}`       |
| les sous-ensembles contenant une paire d'éléments               | `{a,b},{a,c},{b,c}` |
| le sous ensemble contenant tous les éléments                    | `{a,b,c}`           |

**donc 𝒫(E)={ ∅, {a}, {b}, {c}, {a,b}, {a,c}, {b,c}, {a,b,c} }**

### événement contraire

Pour un événement A donné, sous-ensemble de Ω
l'événement contraire de A , noté $\overline{A}$ ,  est un autre sous-ensemble
qui contient tous les éléments de  Ω qui ne sont pas dans A .
C'est ce que l'on appelle l'ensemble complémentaire de A dans Ω

$\overline{A}$={2,4,6}





application probabilité P : outil pour calculer les chances de chaque issue  possible


## issues équiprobables et finie

### application  ℙ 
  ℙ  = cardinal de l'évènement / cardinal de l'univers
  
$$ \mathbb{P}(A) = \frac{\text{Cardinal}(A)}{\text{Cardinal}(\Omega)} $$

avec la notation cardinal(A) = |A|
$$ \mathbb{P}(A) = \frac{|A|}{|\Omega|} $$


#### Lancé de dé
Considérons  l'événement A : obtenir un 6

Cet événement est un ensemble contenant 1 élément :
A = {6}       ----->       |A|  = 1
 
L'univers  Ω  = {1,2,3,4,5,6}.        ----->         |Ω |  = 6

Probabilité   
$$ \mathbb{P}(A) = \frac{|A|}{|\Omega|} = \frac{1}{6} $$




#### Définitions

**Ω** est l'ensemble des résultats possibles
**𝒯** une tribu d'événements

Lorsque **Ω** est fini
l'ensemble des parties de **Ω**, **𝒫(Ω)** peut toujours être considéré comme une tribu d'événements.

**probabilité** :
toute application **ℙ** de  **𝒯** dans l'intervalle [0;1]

**espace probabilisable**
le couple  **(Ω,𝒯)** 

application  **ℙ** 

**espace probabilisé** :
Triplet (Ω,𝒯,ℙ)

Evénement certain  ℙ = 1

Evénement impossible  ℙ = 0

Evénements A et B incompatibles :     ℙ(A∪B) = ℙ(A) + ℙ(B)

Evénement $\overline A$ , contraire de A :      ℙ($\overline A$) = 1 − ℙ(A)


### Probabilité conditionnelle
#### application _probabilité sachant A_


définie pour tout événement B associé à l'expérience aléatoire par :$$ \mathbb{P}(B|A) = \frac{\mathbb{P}(A \cap B)}{\mathbb{P}(A)} $$Lire  : probabilité de  B sachant A égale = etc.


Lancé de dé, quelle est la probabilité d'obtenir 4, sachant que le dé affiche un nombre pair ?
A = "obtenir un nombre pair"
B = "obtenir 4"
Dans ce cas, l'intersection de A et de B est tout simplement B
$$
P(B \mid A) = \frac{P(A \cap B)}{P(A)} = \frac{P(B)} {P(A)} = \frac{\frac{1}{6}}{\frac{1}{2}} = \frac{4}{3}
$$
