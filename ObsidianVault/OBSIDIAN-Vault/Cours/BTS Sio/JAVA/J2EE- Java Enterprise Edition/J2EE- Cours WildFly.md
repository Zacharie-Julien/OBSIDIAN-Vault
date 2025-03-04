
> [!important] Qu'est ce que J2EE
>  **J2EE** (Java 2 Platform, Enterprise Edition), maintenant appelé **Java EE** (et plus récemment **Jakarta EE**), est une plateforme basée sur Java qui fournit un ensemble d’outils et de bibliothèques pour le développement d’applications d’entreprise robustes, évolutives et sécurisées. Elle est une extension de Java SE (Standard Edition) et est spécifiquement orientée vers les applications **client-serveur** et **distribuées**, utilisées dans les environnements professionnels.

### EJB (Enterprise JavaBean): 
---
>Un **EJB** (Enterprise JavaBean) est un composant côté serveur dans l’architecture Java EE, conçu pour encapsuler la logique métier d’une application d’entreprise. Il facilite le développement d’applications robustes et sécurisées en gérant automatiquement des aspects comme les transactions, la sécurité, la concurrence et l’évolutivité. Il existe différent type d'EJB : **[[#StateLess EJB]]** / **[[#StateFull EJB]]** / **[[#SingleTon EJB]]**
>

### JPA (Java Persistant API) :
---
> JPA est une API standardisée pour la persistance des données en Java, permettant aux développeurs de gérer les opérations de base de données via des objets Java. Elle simplifie le développement en éliminant la nécessité d’écrire du code SQL directement, rendant ainsi l’application plus maintenable et indépendante du SGBD utilisé. C'est un ORM (**[[#ORM (Object Relation Mapping)]]**).
> 

### JAX- RS ((Java API for RESTful Web Services) :
---
>**JAX-RS** (Java API for RESTful Web Services) est une API de Java EE (maintenant Jakarta EE) qui permet de créer des services web RESTful en Java de manière standardisée et simplifiée
>

### JSP/ JSF (Java Server Pages / Java Server Faces ) :
---
>Vue / Controleur (à modifier en demandant plus de précision au prof)
>

### ORM (Object Relation Mapping) : 
---
> L’ORM est une technique qui permet de convertir des données entre des systèmes de types incompatibles en utilisant des objets de programmation. Concrètement, dans le contexte des bases de données relationnelles, un ORM permet de **mapper les objets d’une application** aux tables de la base de données, facilitant ainsi la manipulation des données sous forme d’objets plutôt que de lignes et colonnes.
> 

### StateLess EJB :
---
>Un **EJB Stateless** (ou **Stateless Session Bean**) est un type de composant EJB (Enterprise JavaBean) en Java EE qui n’a pas d’état associé à un client particulier. Cela signifie que chaque instance de ce bean est interchangeable et ne conserve pas d’informations entre les appels de méthodes. Les Stateless EJB sont utilisés pour implémenter des opérations réutilisables, indépendantes du contexte utilisateur, comme des calculs ou des accès à la base de données, sans avoir à mémoriser d’informations spécifiques au client.
>

### StateFull EJB :
---
>Un **EJB Stateful** (ou **Stateful Session Bean**) est un type de composant EJB (Enterprise JavaBean) qui **conserve l’état** d’un client spécifique pendant la durée de la session. Contrairement aux Stateless EJB, les Stateful EJB sont liés à un client particulier et peuvent mémoriser des informations entre plusieurs appels de méthodes, ce qui est utile pour des processus qui nécessitent un suivi d’état (par exemple, un panier d’achat en ligne).
>

### SingleTon EJB : 
---
>Un **EJB Singleton** est un type de composant EJB (Enterprise JavaBean) qui garantit qu’une seule instance du bean est créée pour l’ensemble de l’application, partageant cette instance entre tous les clients. Cela signifie que, quelle que soit la manière dont plusieurs clients interagissent avec le Singleton, ils accèdent tous à la même instance.
>