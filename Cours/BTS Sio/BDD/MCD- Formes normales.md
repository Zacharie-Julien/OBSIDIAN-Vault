


>En MCD, une **forme normale** est un niveau de structuration des données qui vise à éliminer les redondances et les anomalies dans la base de données. Chaque forme normale impose des règles spécifiques pour organiser les entités et leurs dépendances fonctionnelles de manière plus optimale et cohérente.


### Première forme normale (1NF) :
---
> Pour qu'une relation soit en première forme normale elle doit respecter les conditions suivantes : 
> 
> --> **Avoir une clef primaire**
> --> **Etre constitué de valeur atomiques**
> --> **Ne pas contenir d'attributs ou d'ensembles d'attributs qui soint des collection de la valeurs**
> 
### Deuxième forme normale (2NF) :
---
> Pour qu'une relation soit en deuxième forme normale elle doit respecter les conditions suivantes : 
> 
> --> **Qu'elle soit en première forme normale**
> --> **Que tous les attributs ne faisant pas partie de ses clés dépendent des clés candidates complètes et non seulement d'une partie d'entre elles**
> 
### Troisième forme normale (3NF) :
---
> Pour qu'une relation soit en troisième forme normale elle doit respecter les conditions suivantes : 
> 
> --> **Qu'elle soit en deuxième forme normale**
> --> **Que tous les attributs ne faisant pas partie des clés dépendent directement des clés candidates**
> 
### Forme normale de Boyce Codd (BCNF) :
---
> Pour qu'une relation soit en forme normale de Boyce Codd elle doit respecter les conditions suivantes : 
> 
> --> **Qu'elle soit en troisième forme normale**
> --> **Que tous les attributs ne faisant pas partie des clés dépendent exclussivement des clés candidates**
> 