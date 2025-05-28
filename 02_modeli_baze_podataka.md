# Model baze podataka

- definira način organizacije, povezivanja i upravljanja podacima
- omogućava pogled s konceptualne razine radi boljeg razumijevanja problema

### Plošni model
- temeljna jedinica pohrane je datoteka
- podaci se pohranjuju u tekstualnim (csv,txt) ili binarnim datotekama
- podaci su organizirani u strukturiranom obliku, bez indexa i veza
- podaci su organizirani u redove i stupce
- red predstavlja jedan zapis u tablici
- fiksna širina stupca i graničnici(s čim se odvajaju podaci - , , tab, | , ;)
- područje primjene : skupovi podataka, log, konfiguracijske datoteke


### Hijerarhijski model
- podaci su organizirani u obliku stabla
- svaka jedinica podatka (čvor ili entitet) ima točno jednog roditelja
- podaci su povezani kroz relacije
- parent-child veza, jedno dijete može imati jednog roditelja
- hijerarhija je striktno organizirana
- putanja polazi od korijena (root)
- upotreba: xml, window registry

### Mrežni model
- naprednija verzija hijerarhijskog modela
- sadrži višestruke veze između entiteta (M:N)
- dijete može imati više roditelja
- povezanost uz pomoć adresnih pokazivača
- imenovane veze

### Relacijski model
- Relacija je temeljni konstrukt koji predstavlja skup n-torki
- ntorka je uređeni skup elemenata - svaki element predstavlja vrijednost jednog atributa u tablici
- relacija je tablica podataka, ntorke- zapisi u tablici, a atributi su svojstva svakog zapisa
- tablica - način pohrane podataka, red - jedinstveni zapis s određenim atributima

#### Relacijska instanca
- konačan skup ntorki koje predstavljaju podatke u bazi podataka
- svaki zapis u tablici mora biti jedinstven
- može se mijenjati dodavanjem, ažuriranjem ili brisanjem ntorki
- sama struktura relacije (opis i atributi) ostaje nepromijenjena

#### Shema relacije
- shema relacije je opis strukture podataka u relacijskom modelu
    - naziv relacijske sheme ( naziv tablice )
    - skup atributa- atributi su svojstva ili stupci u tablici

- shema definira koje vrste podataka i koje informacije će biti pohranjene u tablici
    - sadrži strukturu podataka

- upiti (DQL - data query language - SELECT)
- pohrana i upravljanje podacima (DDL - data definition language - used for defining, altering and deleting db structures - CREATE, DROP, ALTER, TRUNCATE, COMMENT, RENAME), (DML - data manipulation language - koristi se za manipuliranje podacima - INSERT, UPDATE, DELETE, LOCK, CALL, EXPLAIN PLAN)


### Objektni model
- dizajniran za pohranu i upravljanje složenih podatkovnih struktura i veza
- podaci su organizirani temeljem objekata sa definiranim karakteristikama i ponašanjem
- objekt reprezentira entitete
    - svaki objekt ima jedinstveni odentifikator
    - objekt ima atribute(stanja) i ponašanja (operacije, metode)
- objekti su kategorizirani temeljem vrsta ili klase
- objekt je instanca vrste ili klase
- klasa - grupirani objekti koji su sličnih karakteristika (npr Parent class i child classes?)
- metode reprezentiraju realne aktivnosti
- nasljeđivanje - nova klasa može naslijediti atribute i metode stare klase

### NoSQL modeli
- manje ograničenja u dosljednosti u odnosu na tradicionalne relacijske baze podataka

#### Ključ - vrijednost
- jednostavan model podataka, ključ ima jedinstvenu vrijednost
- sličan riječniku po strukturi
- nema upitni jezik
- omogućuje pronalaženje, dodavanje i uklanjanje parova
- tri operacije ->  GET(key), PUT(key,value), DELETE(key)

#### Graf
- koristi se kod aplikacija kojima su bitni odnosi među podacima
- sastoji se od čvorova i lukova
- čvorovi su podaci, lukovi  su odnosi među njima
- svojstva sadrže key/value parove i sadrže podatke koji su smješteni u čvorove

#### Stupčani
- podaci se spremaju u stupce
- stupcima se može pristupati pojedinačno
- stupci se grupiraju u obiteljske stupce


### Dokument
- osnovni model je dokument (uređeni skup ključeva s pridruženim vrijednostima)
- svaki dokument mora sadržavati primarni ključ
- dokumenti se pohranjuju u BSON formatu
- dokumenti se smještaju u kolekcije
- kolekcija nema definiranu shemu, svaki dokument unutar kolekcije može imati svoju strukturu
- dokument može sadržavati drugi dokument
