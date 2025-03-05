 



Création d'un trigger :



DELIMITER $$

	CREATE TRIGGER monTrigger (AFTER | BEFORE) (SELECT | UPDATE | DELETE)
	ON nom_table
	FOR EACH ROW
	
	BEGIN

	END
	
DELIMITER ;

exemple :

	CREATE TRIGGER monTrig AFTER INSERT
	ON Ligne_commande
	FOR EACH ROW (FOLLOWS | PRECEDES) monTrig0
		DECLARE pu DECIMAL(10,2);
		SELECT art_pu INTO pu 
		FROM Article 
		WHERE art_num = NEW.art_num
		NEW total_ligne = NEW.lcde_qte * pu; 
	END;

Pour la gestion des priorité :

	FOLLOWS
	PRECEDES