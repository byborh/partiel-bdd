Voici lé preuve que j'ai effectué cette requête:

---
1) 
SELECT
    a.nom,
    a.prenom,
    e.nom AS epreuve,
    ROUND(SUM(n.valeur * c.poids) / SUM(c.poids), 2) AS note_finale
FROM athlete a
JOIN participation p ON p.id_athlete = a.id_athlete
JOIN epreuve e ON e.id_epreuve = p.id_epreuve
JOIN run r ON r.id_athlete = a.id_athlete AND r.id_epreuve = e.id_epreuve
JOIN note n ON n.id_run = r.id_run
JOIN critere c ON c.id_critere = n.id_critere
GROUP BY a.id_athlete, a.nom, a.prenom, e.id_epreuve, e.nom
ORDER BY a.nom, a.prenom, e.nom;

![alt text](image.png)
---

SELECT CONCAT(a.prenom, ' ', UPPER(a.nom)) AS 'Prénom NOM'
FROM athlete a
JOIN participation p ON p.id_athlete = a.id_athlete
GROUP BY a.id_athlete, a.prenom, a.nom
HAVING COUNT(DISTINCT p.id_epreuve) >= 2
ORDER BY a.prenom, a.nom;

![alt text](image-1.png)


---
voici la requête pour la question 3

SELECT DISTINCT a.nom, p.nom AS pays
FROM athlete a
JOIN pays p ON p.id_pays = a.id_pays
JOIN participation pa ON pa.id_athlete = a.id_athlete
LEFT JOIN run r ON r.id_athlete = pa.id_athlete AND r.id_epreuve = pa.id_epreuve
WHERE r.id_run IS NULL
ORDER BY a.nom, p.nom;

![alt text](image-2.png)
---

voici la requête souhaitée pour la question 4:

DELIMITER $$
DROP PROCEDURE IF EXISTS classement_epreuve $$

CREATE PROCEDURE classement_epreuve(IN p_id_epreuve INT)
BEGIN
    SELECT
        @rang := @rang + 1 AS rang,
        resultat.nom,
        resultat.prenom,
        resultat.epreuve,
        resultat.note_finale
    FROM (
        SELECT
            a.nom,
            a.prenom,
            e.nom AS epreuve,
            ROUND(SUM(n.valeur * c.poids) / SUM(c.poids), 2) AS note_finale
        FROM athlete a
        JOIN participation pa ON pa.id_athlete = a.id_athlete
        JOIN epreuve e ON e.id_epreuve = pa.id_epreuve
        JOIN run r ON r.id_athlete = a.id_athlete AND r.id_epreuve = e.id_epreuve
        JOIN note n ON n.id_run = r.id_run
        JOIN critere c ON c.id_critere = n.id_critere
        WHERE e.id_epreuve = p_id_epreuve
        GROUP BY a.id_athlete, a.nom, a.prenom, e.id_epreuve, e.nom
        ORDER BY note_finale DESC
    ) AS resultat
    CROSS JOIN (SELECT @rang := 0) AS init;
END $$

DELIMITER ;

Voici la preuve de ma requête :

``
CALL classement_epreuve(1);
``

![alt text](image-3.png)
