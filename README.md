# PyTimelineJS

PyTimelineJS est une bibliothèque python permettant de générer des frises chronologiques.

Cette bibliothèque a été programmée afin d'être simple d'utilisation pour des élèves.

La frise chronologique produit un fichier html et utilise la bibliothèque [TimelineJs](https://github.com/NUKnightLab/TimelineJS3/).

![image](https://user-images.githubusercontent.com/53106394/224863188-78f483b8-2a4b-421b-9d87-b931bc038e28.png)

## Exemple :
Le fichier `pytimelinejs.py` doit être placé dans le même dossier que le script python de l'élève.
```python
from pytimelinejs import *

titre("Le Web")

date("1965", "Invention et programmation du concept d’hypertexte par Ted Nelson")
date("1989", "Naissance au CERN par Tim Berners Lee")
date("1993", "Mise dans le domaine public, disponibilité du premier navigateur Mosaic")
date("1995", "Mise à disposition de technologies pour le développement de site Web interactif (langage JavaScript) et dynamique (langage PHP)")
date("2001", "Standardisation des pages grâce au DOM (Document Object Model)")
date("2010", "Mise à disposition de technologies pour le développement d’applications sur mobiles")

generer()
```

## Commandes disponibles

### titre
Définie le titre de la frise chronologique (ne devrait être appelée qu'une seule fois)
```python
titre("Le Web")
titre("Le Web", "Cette frise contient les dates présente dans le programme de SNT") # Il est possible d'ajouter une description
```

### date
Ajoute une date à la frise chronologique
```python
date("2002", "Première version de Firefox")
date("2002", "Première version de Firefox", "Firefox s'appelait à l'époque Phoenix.") # Ajout d'une description
date("09/2002", "Première version de Firefox") # Ajout du mois
date("23/09/2002", "Première version de Firefox") # Ajout du mois et du jour
```

### periode
Ajoute une période à la frise chronologique
```python
periode("1995", "2022", "Internet explorer")
periode("1995", "2022", "Internet explorer", "Internet Explorer est un ancien navigateur développé par Microsoft") # Ajout d'une description
periode("08/1995", "12/2022", "Internet explorer") # Ajout du mois
periode("16/08/1995", "13/12/2022", "Internet explorer") # Ajout du mois et du jour
```

### generer
Génère le fichier html contenant la frise et ouvre le fichier dans le navigateur par défaut.
```python
generer()
```
