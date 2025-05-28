# Data Query Language - DQL


SELECT - dohvat podataka iz baze podataka

Dohvaćanje samo različitih vrijednosti :
SELECT DISTINCT column_name, column_name2 FROM table_name;

Prebrojavanje različitih vrijednosti
SELECT COUNT (DISTINCT column_name) FROM table_name;

WHERE - koristi se za filtriranje podataka, dohvaćaju se podaci koji ispunjavaju neki uvjet

Sintaksa
SELECT column1, column2, ...
FROM table_name
WHERE condition;


posebni operatori:
<> Nije jednako (kod pojedinih verzija SQL; !=)
BETWEEN U rangu između
LIKE Traži po obilježju
IN Za određivanje moguće višestruke vrijednosti u stupcu

ORDER BY - koristi se za sortiranje rezultata u rastućem ili padajućem nizu
    - zadano sortiranje je rastuće - ASC

Sintaksa
SELECT column1, column2, ...
FROM table_name
ORDER BY column1, column2, ASC | DESC;


GROUP BY - koristi se za raspoređivanje podataka u grupe i njihovo sumiranje

Sintaksa
SELECT column1, column2, ...
FROM table_name
WHERE conditions
GROUP BY column1, column2, …
ORDER BY column1, column2, …


