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
