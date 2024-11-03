
> [!important]
>#### Vocabulaire BDD :
> - ##### [[#Clé primaire]]
> - ##### [[#Clé étrangère]]
> - ##### [[#Attribut]]
> #### Vocabulaire MCD :
> - ##### [[#Entités]]
> - ##### [[#Association]]
> - ##### [[#Cardinalité]]
> - ##### [[#Identifiant]]
> #### Vocabulaire HERITAGES :
> - ##### [[#Exclusion]]
> - ##### [[#Totalité]]
> - ##### [[#Partition]]




>Une BDD est un ensemble d’informations stocké sur un système informatique. Cet ensemble est implanté physiquement (généralement sur disque dur) sous la forme d’un ou plusieurs fichiers. Cette organisation est assurée par un logiciel spécialisé : le SGBD (Système de Gestion de Base de Données).


> [!NOTE]
> Une **table** est un tableau dans lequel les **lignes** sont appelées les **enregistrements** (ou tuples) (!)

### Attribut : 
---
> Un attribut est une information désignant le plus petit élément d’information manipulable. Il est caractérisé par un nom et d’un type.
> 
### Clé primaire : 
---
> La clé primaire est un attribut qui permet de distinguer chaque occurrence d’une relation par rapport à tous les autres. Toutes les valeurs de cet attribut doivent être uniques.
> 
### Clé étrangère : 
---
> Une clé étrangère correspond à la clé primaire d’une autre table.Elle permet de matérialiser les liens entre les différentes tables.
> 



>Un **MCD** (Modèle Conceptuel de Données) est une représentation graphique qui décrit les données importantes d’un système ainsi que leurs relations. Utilisé dans la conception de bases de données, il représente les **[[#Entités]]** (objets ou concepts), leurs **[[#Attribut]]** (caractéristiques), et les liens (**[[#Association]]**) entre elles. Le MCD est essentiel pour structurer les données de manière logique et claire avant de passer à la création physique de la base de données.

### Entités : 
---
> Une entité modélise un élément concret, ou abstrait, impliqué dans le système, et pourvu d'une existence propre indépendante du système.
> 
### Association : 
---
> Une association modélise un lien informationnel mettant en jeu une ou plusieurs entités. Chaque association ne doit modéliser qu'une seule information et ne peut donc avoir qu'un seul sens dans le système.
> 
### Cardinalité : 
---
> Dans une association, les cardinalités correspondent à 2 nombres, qui expriment le nombre minimum et maximum d'occurrences de l'association pour une occurrence de l'entité concernée. La cardinalité minimale doit être inférieure ou égale à la maximale.
> 
### Identifiant : 
---
> C'est une propriété obligatoire dans chaque entité, qui permet d'identifier sans ambiguïté, de façon unique, et biunivoque chaque occurrence de l'entité.
> 



>En MCD, **l’héritage** représente une relation entre une **entité mère** et une ou plusieurs **entités filles**, qui héritent des **[[#Attribut]]** et des **[[#Association]]** de l’entité mère. Cela permet de modéliser une hiérarchie de concepts où les entités filles partagent des caractéristiques communes tout en ajoutant leurs propres spécificités. 

### Exclusion (X) : 
---
>Une contrainte d’exclusion, placée entre deux associations, signifie qu’on ne puisse pas participer aux deux relations à la fois (l’un, l’autre ou aucune).
> 
### Totalité (T) :
---
>Une contrainte de totalité, signifie qu’on doit absolument participer à l’une ou l’autre des deux associations (l’une, l’autre ou les deux).
>
### Partition (XT) :
---
>Une contrainte de partition, placée entre deux associations, signifie qu’on ne puisse ni participer aux deux relations à la fois ni à participer à aucune (l’une, l’autre).
> 

