# Normalizacija

- postupak učinkovitog organiziranja podataka u bazi podataka

Cilj:
- smanjenje redundancije
- organizacija podataka u tablice na način da slijede logiku međusobne ovisnosti
- izbjegavanje anomalija unosa, izmjena i brisanja

Normalne forme (NF):
- prva 1NF
- druga 2NF
- treća 3NF
- boyce coddova BCNF
- četvrta 4NF
- peta 5NF
- šesta 6NF

### Anomalije
- nenormaliziranje tablice predstavljaju određene probleme povezane uz ažuriranje podataka u njima
- Anomalija unosa podataka - nije moguć unos zapisa (n-torke) jer postoji zavisnost od druge relacije
- Anomalija brisanja podataka - brisanje jednog podatka dovelo bi do brisanja podataka drugog entiteta
- Anomalija nadopune podataka - ažuriranje jednog podataka uzrokuje ažuriranje više zapisa (n-torka)

#### 1NF
- svi atributi su osnovni / elementarni (ATOMARNI) , nema ponavljajućih
- svaki atribut mora biti jedinstven
- jedna vrijednost po atributu - atomične vrijednosti podatka - nedjeljive vrijednosti
- svaki redak mora imati jedinstveni identifikator (PK)



The "ADD CONSTRAINT" command in SQL is used to add rules to an existing table, such as primary keys, foreign keys, or unique constraints, 
ensuring data integrity. This command is typically used with the "ALTER TABLE" statement to modify the table's structure.

ALTER TABLE studenti_i_predmeti ADD CONSTRAINT
pk_studenti_i_predmeti PRIMARY KEY (ID_studenta, ID_predmeta);

#### 2NF
- tablica mora biti u 1NF
- svi atributi moraju ovisiti o cijelom primarnom ključu, a ne samo o nekom njegovom dijelu
- zapisi u tablici moraju ovisiti samo o primarnom ključu

#### 3NF

- tablica mora biti u 2NF
- svaki neprimarni atribut relacije R je izravno ovisan o svim dijelovima primarnog ključa na relaciji R
- neprimarni atribut relacije R je onaj atribut koji ne pripada ni u jednom kandidatu za ključ










