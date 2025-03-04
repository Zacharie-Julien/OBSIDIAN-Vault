

> [!important] Pourquoi GRANT et REVOKE ?
> Dans MySQL, les commandes **GRANT** et **REVOKE** permettent d’attribuer et de retirer des droits d’accès et des privilèges à des utilisateurs sur les bases de données, tables, ou d’autres objets.
> 
>• **REVOKE :** Utilisée pour retirer des permissions accordées.


### **Syntaxe de REVOKE** :
---

```
REVOKE [Grant option for] <privilèges> ON <objet> FROM <utilisateur>;
```

---
> **privilèges** **:**  Les permissions à retirer.
--- 
> **objet** :  La portée des droits (comme dans [[SQL- GRANT]]).
---
> **utilisateur** **:** Le nom de l’utilisateur MySQL.
---
   **hôte** **:** L’adresse IP ou le domaine depuis lequel l’utilisateur se connecte (souvent localhost).
---
> **Grant option for** **:** permet de retirer la possibilité de GRANT à l'utilisateur
### **Exemple de REVOKE** :
---

>**Retirer l’accès en lecture (SELECT) d’une base de données :**

```
REVOKE SELECT ON ma_base.* FROM 'user1'@'localhost';
```

>**Retirer tous les privilèges sur une table spécifique :**

```
REVOKE ALL PRIVILEGES ON ma_base.ma_table FROM 'user2'@'localhost';
```

> **Retirer des privilèges spécifiques :**

```
REVOKE INSERT, UPDATE ON ma_base.* FROM 'user3'@'localhost';
```

>**Retirer la capacité de déléguer ses droits :**

```
REVOKE GRANT OPTION ON *.* FROM 'admin'@'%';
```
