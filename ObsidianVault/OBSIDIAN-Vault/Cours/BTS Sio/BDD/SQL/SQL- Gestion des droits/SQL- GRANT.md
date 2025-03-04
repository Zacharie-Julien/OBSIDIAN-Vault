

> [!important] Pourquoi GRANT et REVOKE ?
> Dans MySQL, les commandes **GRANT** et **REVOKE** permettent d’attribuer et de retirer des droits d’accès et des privilèges à des utilisateurs sur les bases de données, tables, ou d’autres objets.
> 
> • **GRANT :** Utilisée pour donner des permissions spécifiques à un utilisateur.


### **Syntaxe de GRANT** :
---

```
GRANT <privilèges> ON <objet> TO <utilisateur>, [WITH GRANT OPTION];
```

---
> **privilèges** **:** Les droits à accorder, comme SELECT, INSERT, UPDATE, ou ALL PRIVILEGES. 
--- 
> **objet** : L’étendue des permissions (par exemple, une table ou une base).
	•   \*.* : Toutes les bases et tables.
	• ma_base.* : Toutes les tables dans une base spécifique.
	• ma_base.ma_table : Une table spécifique.
---
> **utilisateur** **:** Le nom de l’utilisateur MySQL.
---
   **hôte** **:** L’adresse IP ou le domaine depuis lequel l’utilisateur se connecte (souvent localhost).
---
   **WITH GRANT OPTION** : permet d'accordé le droit de grant à un utilisateur 


### **Exemple de GRANT** :
---

>**Donner l’accès en lecture (SELECT) à une base de données :**

```
GRANT SELECT ON ma_base.* TO user1;
```

>**Donner tous les privilèges sur une table spécifique :**

```
GRANT ALL PRIVILEGES ON ma_base.ma_table TO user2;
```

>**Créer un nouvel utilisateur avec un mot de passe et des droits spécifiques :**

```
GRANT INSERT, UPDATE ON ma_base.* TO user3 IDENTIFIED BY 'password123';
```

>**Donner tous les privilèges sur toutes les bases :**

```
GRANT ALL PRIVILEGES ON *.* TO admin WITH GRANT OPTION;
```


> [!important] WITH GRANT OPTION
>  Permet à l’utilisateur de déléguer ses propres privilèges à d’autres utilisateurs.
