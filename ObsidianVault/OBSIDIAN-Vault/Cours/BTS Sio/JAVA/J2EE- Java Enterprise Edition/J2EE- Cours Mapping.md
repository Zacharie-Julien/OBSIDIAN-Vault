

> [!important] Qu'est ce que le MAPPING en J2EE
>  Le mapping en JEE est la **correspondance** entre les attributs d’une classe Java et les colonnes d’une table d’une base de données, réalisée principalement à l’aide de l’API JPA (Java Persistence API). Cela inclut également la gestion des relations entre différentes entités.


### ORM (Object Relational Mapping): 
---
>L’ORM (Object-Relational Mapping), ou **mapping objet-relationnel**, est une technique permettant de convertir automatiquement des données entre un système de gestion de bases de données relationnelles (RDBMS) et un système de programmation orienté objet.
>En pratique, l’ORM associe les classes et les objets d’une application à des tables et des lignes d’une base de données, rendant ainsi transparentes les opérations de persistance (création, lecture, mise à jour et suppression de données).
>

### Les annotations de base en JEE :
---

### ***1- Annotation pour les entités*** :
#### @Entity :
>Indique que la classe Java est une entité JPA (représente une table dans la base de données).

```
@Entity #Annotation
public class MyEntity { ... }
```

#### @Table :
>Spécifie les détails de la table à laquelle une entité est mappée (nom, schéma, etc.)

```
@Entity
@Table(name = "my_table") #Annotation
public class MyEntity {...}
```


### ***2- Annotations pour les colonnes*** :

#### @Column :
>Utilisée pour mapper un champ de la classe à une colonne de la table.

```
#A declarer une fois l'entite declare/annote

@Column(name = "column_name")
```

#### @Id :
>Indique que le champ est la clé primaire de l’entité.

```
#A declarer une fois l'entite declare/annote

@Id
@Column(name = "column_name")
private String dateAchat;
```

#### @GeneratedValue :
> Spécifie la stratégie de génération automatique des clés primaires.
> Stratégies :
> 	 ***AUTO, IDENTITY, SEQUENCE, TABLE.

```
#A declarer une fois l'entite declare/annote

@Id
@GeneratedValue(strategy = GenerationType.AUTO)
@Column(name = "column_name")
private Long id;
```

#### @Transient :
> Exclut un champ de la persistance (il ne sera pas stocké dans la base de données).

```
#A declarer une fois l'entite declare/annote

@Transient
private String tempValue;
```


### ***3-  Annotations pour les relations :

#### @OneToOne:
> Définit une relation un-à-un entre deux entités.

```
#A declarer une fois l'entite declare/annote

@OneToOne
@JoinColumn(name = "foreign_key", referencedColumnName = "foreign_key")
private OtherEntity otherEntity;
```

#### @ManyToOne:
> Définit une relation plusieurs-à-un (par exemple, plusieurs commandes associées à un client).

```
#A declarer une fois l'entite declare/annote

@ManyToOne
@JoinColumn(name = "foreign_key", referencedColumnName = "foreign_key")
private OtherEntity otherEntity;
```

#### @OneToMany:
> Définit une relation un-à-plusieurs (par exemple, une commande avec plusieurs articles).

```
#A declarer une fois l'entite declare/annote

@OneToMany
@JoinColumn(name = "foreign_key", referencedColumnName = "foreign_key")
private OtherEntity otherEntity;
```

#### @ManyToMany:
> Définit une relation plusieurs-à-plusieurs (souvent avec une table de jointure).

```
#A declarer une fois l'entite declare/annote

@ManyToMany
@JoinTable(
	name = "user_roles",
	joinColumns = @JoinColumn(name = "user_id"),
	inverseJoinColumns = @JoinColumn(name = "role_id")
)
private Set<Role> roles;
```


### ***4-  Annotations avancées :

#### @Embedded et @Embeddable :
> Pour des objets intégrables (par exemple, une adresse en tant qu’objet dans une entité principale).

```
#A declarer une fois l'entite declare/annote

@Embeddable
public class Address {
    private String street;
    private String city;
}
```

#### @JoinColumn :
> Définit la clé étrangère pour les relations (ex. : @ManyToOne, @OneToOne).

```
#A declarer une fois l'entite declare/annote

@JoinColumn(name = "foreign_key", referencedColumnName = "foreign_key")
```

#### @JoinTable :
> Utilisée pour définir une table de jointure dans les relations @ManyToMany.

```
#A declarer une fois l'entite declare/annote

@JoinTable(
    name = "relation_table",
    joinColumns = @JoinColumn(name = "entity1_id"),
    inverseJoinColumns = @JoinColumn(name = "entity2_id")\
)
```

#### @Access :
> Spécifie le type d’accès aux champs ou getters (FIELD ou PROPERTY).

```
#A declarer une fois l'entite declare/annote

@Access(AccessType.FIELD)
```


### ***5-  Annotations pour les relations :

#### @Fetch  (optionnel) :
> Définit la stratégie de chargement (EAGER ou LAZY).

```
#A declarer une fois l'entite declare/annote

@OneToMany(fetch = FetchType.LAZY)
private List<Item> items;
```
