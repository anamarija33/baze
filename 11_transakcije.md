# Transakcije

- baze podataka može istovremeno koristiti nekoliko programa
        - može dovesti do nekonzistentnosti stanja baze podataka

- Transakcija u bazi podataka je skup operacija koje se izvršavaju kao jedna logička cjelina, izmjene podataka u bazi se vrše kao jedna jedinstvena operacija
- Transakcija je osnovna jedinica za upravljanje i osiguravanje konzistentnosti podataka u bazi podataka

**BEGIN WORK** - početak transakcije
**COMMIT WORK** - potvrđivanje transakcije
**ROLLBACK WORK** - poništavanje transakcije- poništavanje svih izmjena koje je transakcija obavila


### Stanja transakcije
Aktivna - tijekom izvođenja
Djelomično završena - nakon što je obavljena njezina posljednja operacija
Neispravna - nije moguće nastaviti njezino normalno izvođenje
Neuspješno završena - poništena, njezini efekti i baza podataka se vraćaju u stanje u kakvom su bili prije nego što je transakcija započela
Potvrđena - uspješno završena

### ACID - svojstva transakcije
**Atomarnost** - transakcija je atomarna ako su svi koraci izvršeni u potpunosti ili ako se ne izvrše
**Konzistentnost** - transakcija je konzistentna ako jse po završetku transakcije baza podataka nalazi u ispravnom stanju
**Izoliranost** - transakcija se smatra izoliranom ako se njezinne izmjene ne iterferiraju sa drugim transakcijama koje se odvijaju u isto vrijeme
**Trajnost** - transakcija se smatra trajnom ako se njezine promjene održavaju u bazi i nakon što je transakcija dovršena (promjene su trajno zapisane)


SQLite podržava ACID transakcije temeljem:
- eksplicitne transakcije - definiraju se pomoću naredbi BEGIN, COMMIT i ROLLBACK
    -> begin, insert into ili neka naredba , commit
- implicitne transakcije - koriste se ako nije definirana eksplicitna transakcija. 
    - svaka sql operacija izvršava se u okviru svoje transakcije. Ako je uspješna - završava, ako ne uspije - poništava se
    -> obična insert into npr


- 
