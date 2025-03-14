

> [!important] C'est quoi une **procédure stockée** en SQL ?
> Une **procédure stockée** en SQL est un ensemble de commandes SQL précompilées et stockées sur le serveur de base de données. Elle peut être exécutée en appelant son nom, souvent avec des paramètres d’entrée ou de sortie. Les procédures stockées sont utilisées pour automatiser des tâches répétitives, appliquer des règles métiers, ou effectuer des opérations complexes sur les données.

### **Caractéristiques principales :**

---
> **Stockée sur le serveur** :
> 	• Les procédures sont enregistrées directement dans la base de données et restent   disponibles pour les utilisateurs autorisés.
> 
> **Exécution optimisée** :
> 	• Elles sont précompilées, ce qui signifie qu’une fois créées, elles peuvent être exécutées plus rapidement qu’un script SQL classique.
> 
> **Réutilisables** :
> 	• Une procédure peut être appelée plusieurs fois, ce qui réduit la duplication de code.
> 	
> **Paramètres d’entrée et de sortie** :
> 	• Elles peuvent accepter des **paramètres d’entrée** pour personnaliser leur comportement et renvoyer des **valeurs de sortie**.


### **Syntaxe d’une procédure stockée dans SQL Server :**

---
```
CREATE PROCEDURE NomProcedure
    @ParamEntree INT,
    @ParamSortie INT OUTPUT
AS
BEGIN
    -- Instructions SQL
    SELECT @ParamSortie = @ParamEntree * 2;
END;
```


### **Appeler une procédure :**

---
```
DECLARE @Resultat INT;
EXEC NomProcedure @ParamEntree = 5, @ParamSortie = @Resultat OUTPUT;
PRINT @Resultat; -- Affiche le résultat
```


### **Exemple simple (MySQL) :**

---
```
DELIMITER //

CREATE PROCEDURE AjouterUtilisateur(IN Nom VARCHAR(50), IN Email VARCHAR(50))
BEGIN
    INSERT INTO Utilisateurs (nom, email) VALUES (Nom, Email);
END //

DELIMITER ;
```

```
CALL AjouterUtilisateur('Jean Dupont', 'jean.dupont@example.com');
```



	Trois type de parametre :
		IN // parametre entran mais pas sortant
		OUT // parametre entran vide mais sortant
		INOUT // les deux 


Pour supprimer uen procedure : 
	DROP le_nom_de_la_procedure 

Déclaré une variable :
	DECLARE nom_de_la_variable type [DEFAULT valeur]
	SET nom_de_la_variable = valeur;

Bloc conditionnel : 
	IF condition THEN 
		ELSE 
	END IF ; 
SWITH CASE :
	CASE valeur
		WHEN val1 THEN instruction
		WHEN val2 THEN instruction
		ELSE instruction
	END CASE;


Bloc boucle :
	BEGIN 
		WHILE condition DO
			
		END WHILE;


Curseur :
	DECLARE mon_cur CURSOR
		FOR la requetes ;
			DECLARE les_valeur renvoyé par la requetes
			OPEN mon_cur;
				DECLARE OVER int DEFAULT 0;
				DECLARE CONTINUE HANDLER FOR NOT FOUND SET over = 1;
				WHILE over != 1 DO
					FETCH mar_cur INTO v1, v2, v3;
					code_courant
				END WHILE;
				CLOSE mon_cur;

Gestion des erreurs : 

	
		DECLARE CONTINUE | EXIT HANDLER 
			FOR 45000
		SIGNAL SQLSTATE '45000'
			SET message_text = "Mon erreur "
