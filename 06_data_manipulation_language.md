# Data manipulation language (DML)

### Vanjski ključ (FK- Foreign key)
- koristi se za uspostavu referencijalnog integriteta u bazi (relacija između tablica)
- Uspostavom referencijalnog integriteta stvaramo „roditeljsku tablicu”, a tablica sa vanjskim ključem je podređena tj. „tablica djece”. - ne znan što znači
- vanjski ključ u tablici djece referencira primarni ključ u nadređenoj tablici
- FK se definira pri kreiranju tablice

Sintaksa
CREATE TABLE table_name
(
column1 datatype [ NULL | NOT NULL ],
column2 datatype [ NULL | NOT NULL ],
...
CONSTRAINT fk_column
FOREIGN KEY (column1, column2, ... column_n)
REFERENCES parent_table (column1, column2, ...
column_n)
);

PRIMJER : 
CREATE TABLE odjel
(id INTEGER PRIMARY KEY AUTOINCREMENT,
ime VARCHAR
);

CREATE TABLE zaposlenik
(zaposlenik_id INTEGER PRIMARY KEY AUTOINCREMENT,
ime VARCHAR NOT NULL,
prezime VARCHAR,
odjel_id INTEGER,
CONSTRAINT fk_odjel
FOREIGN KEY (odjel_id)
REFERENCES odjel(id)
);




### Update

UPDATE table
SET column1 =
expression1,
column2 = expression2,
...
[WHERE conditions];



UPDATE table
SET column1 = expression1,
column2 = expression2,
...
[WHERE conditions]
[ORDER BY expression [ ASC | DESC ]]
[LIMIT number_rows OFFSET offset_value];


### Delete

Brisanje s jednim uvjetom
DELETE FROM table
[WHERE conditions];

Brisanje s više uvjeta
DELETE FROM employees
WHERE last_name = ‘Smith’
AND employee_id < 50;

- prvo se brišu zapisi koji su povezani uz tablicu djece, pa onda zapis iz tablice djece


### EXPORT
a.) Export kreirajte temeljem Opcije – Database – Export the database
b.) Odaberite sve objekte za export
c.) Format exporta je SQL, export radite u datoteku pod nazivom
racun_export.db
d.) Otvorite datoteku kroz tekstualni editor, snimite u format txt pod vašim
imenom i prezimenom, txt datoteku stavite na Merlin u okviru Vježbe 06 –
Export baze podataka

