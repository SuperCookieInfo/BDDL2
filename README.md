
# BDDL2
bdd1

SELECT raison, activité FROM `entreprise` WHERE 1 

SELECT `inscrit` FROM inscrire WHERE sess = 'CRUNGA' 

SELECT nom FROM inscrire JOIN participant USING (inscrit) WHERE sess = 'CRUNGA' 

SELECT nom FROM inscrire A , participant B WHERE sess = 'CRUNGA' AND A.inscrit= B.inscrit 

SELECT `nom` FROM participant JOIN inscrire USING (inscrit) WHERE entr IS NULL AND sess = 'CRUNGA' 

SELECT DISTINCT (raison) FROM entreprise A, participant B WHERE A.entr = B.entr 

SELECT DISTINCT (raison) FROM entreprise A JOIN participant B USING (entr)

SELECT sess, intitulé, date_format(début, "%a %d") AS 'jour' FROM session WHERE début BETWEEN '1984-08-01' AND '1984-08-31' 

SELECT nom , date AS "date d'inscription" , sess AS 'session' , début FROM inscrire JOIN session USING (sess) JOIN participant USING (inscrit) WHERE date = (début - 1)

