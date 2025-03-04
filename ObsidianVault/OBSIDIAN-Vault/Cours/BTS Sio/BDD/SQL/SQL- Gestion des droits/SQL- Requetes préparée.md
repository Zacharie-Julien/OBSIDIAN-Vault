
PREPARE nom_requete FROM requete;

	exemple : 
		PREAPRE recherche FROM SELECT * FROM Article
			WHERE art_nom LIKE ?

	EXECUTE recherche_art USING "%ch%"


? permet de remplacer par la variable passer en parametre