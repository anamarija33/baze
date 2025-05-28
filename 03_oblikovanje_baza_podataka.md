# Oblikovanje baza podataka

### Životni ciklus baze podataka
- utvrđivanje korisničkih zahtjeva
- ER modeliranje, Pogledi, Transformacija u SQL tablice, Normalizacija
- indeksi, denormalizacija
- implementacija, nadgledanje, održavanje i promjene


### Informacijski zahtjevi
- utvrđivanje poslovnih potreba, odn izvore podataka i podatke koje je potrebno modelirati

Faze: 
- identificiranje poslovnog konteksta
- provođenje intervjua sa ključnim dionicima
- sinteza očekivanje i zahtjeva
- razvoj mapiranja "izvor-cilj"

### Logički dizajn
- konceptualni dijagram modela podataka i njihovih odnosa
- ER ili UML
- konstrukti modela podataka se transformiraju u normalizirane tablice ili relacije
Obuhvaća : 
- konceptualno modeliranje podataka
- poglede
- transformaciju konceptualnog modela podataka u normalizirane tablice
- normalizacija tablica 

### Fizički dizajn
- optimiziranje ispunjenje zahtjeva/učinaka??
 - odabir indeksa
 - particioniranje
 - klasteriranje podataka
 - pogledi 
 - denormalizaciju

### Osnovni ER konstrukti 

#### Entiteti
- osnovni objekti o kojima se trebaju prikupljati podaci
- objekti mogu biti stvarni ili apstraktni
- pojava entiteta - instanca entiteta
- pravokutnik, imenica


#### Atributi 
- svojstva (karakteristike) entiteta koje omogućuju opisne detalje o njima
- pojava atributa unutar entiteta - vrijednost atributa
- oval sa imenom atributa
- 2 tipa: identifikatori i deskriptori

#### Relacije
- realna pridruživanja između jednog ili više entiteta
- opisane kroz stupanj, povezanost i postojanost
- povezanost : 1-1, 1-M, M-N
- romb, glagol

    ##### Stupanj
    - broj entiteta pridruženih u relaciju
    Rekurzivna binarna - povezan samo sa drugom instancom svog tipa ( npr zaposlenik, može upravljat ostalim podređenim zaposlenicima)
    Binarna - entitet povezan sa drugim entitetom
    Trinarna - entitet povezan sa druga dva entiteta

    ##### Povezanost
    - opisuje ograničenja povezivanja entiteta u relaciji
    - jedan, mnogo
    <b>Kardinalnost</b> - definira koliko instanci jednog entiteta je povezano sa instancama drugog entiteta
    1:1 - instanca jednog entiteta je povezana samo s jednom instancom iz drugog entiteta
        Razlozi: sigurnost, nemogućnost kombiniranja podataka u jedan entitet
    1:N - instanca jednog entiteta je povezana sa više instanci drugog entiteta
    M:N - više instanci jednog entiteta je povezano sa više instanci drugog entiteta
         -> asocijativni entitet - entitet koji povezuje 2 entiteta
            -> sadrži atribute relacije 
        ##### Postojanost
        - pojavnost entiteta - obavezni ili izborni
        - sporedni entitet mora postojati kako bi se realizirala relacija
        - izborni - entitet ne mora postojati - 0
        
        
        