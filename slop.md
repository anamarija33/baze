


- Definicija
  - Transakcija (engl. transaction) - skup od jedne ili više SQL naredbi koje čine logičku jedinicu rada nad bazom podataka
  - Princip "Sve ili ništa"
- Osnovno načelo transakcija
  - Mora biti provedena u cijelosti ili
  - Ne smije biti provedena uopće
- Pogreške u bazi
  - Neutralizacija ako transakcija nije obavljena do kraja
  - Svi promijenjeni podaci moraju se vratiti na polazne vrijednosti
- Primjer
  - Uplate između bankovnih računa (novac se ne smije izgubiti ili biti viška)

- Upute za transakcije
  - Počinje naredbom START TRANSACTION ili BEGIN WORK
  - Završava s COMMIT \[WORK] ili ROLLBACK \[WORK]



- COMMIT
  - Uspješan završetak i trajno pohranjivanje promjena
- ROLLBACK
  - Neuspješan završetak i poništavanje promjena


- Rad s bazom podataka
  - Svaka operacija čitanja ili pisanja iz baze odvija se unutar transakcije



- Implicitne i eksplicitne transakcije
  - Automatsko pokretanje i završavanje transakcija

- Način isključivanja automatskog potvrđivanja
  - Naredba: SET AUTOCOMMIT = 0;

- Ovisno o DBMS-u
  - Automatsko isključivanje AUTOCOMMIT prilikom poziva BEGIN WORK


- Oporavljivost (engl. Recoverable)
- Serijabilnost, sekvencijalnost (engl. Serialisable)


- Atomarnost
- Konzistentnost
- Izolacija
- Izdržljivost

- Osigurava zapisivanjem rezultata transakcije samo u međuspremnik

Konzistentnost

- Baza prelazi iz jednog konzistentnog stanja u drugo

 Izolacija

- Učinak transakcija jednak kao da su se odvijale jedna nakon druge
Izdržljivost

- Efekti transakcije ne smiju biti izgubljeni nakon završetka

 Ograničenja

- DDL naredbe poput CREATE, DROP, ALTER izazivaju implicitni COMMIT

 Pohranjivanje

- Mogućnost opovrgavanja dijela transakcije pomoću točaka pohranjivanja




## Sigurnost

- Korisnici; Objekti; Sheme; Dozvole; Uloge

**Opći uvjet**

- Baza podataka mora biti sigurna od fizičke korupcije bez obzira na:
  - Hardverski/softverski kvar
  - Neautorizirani pristup
  - Neželjeni program
  - Preopterećenje
  - Programska pogreška
- DBMS rješenja:
  - Kontrola pristupa
  - Auditing
  - Authentication
  - Enkripcija
  - Kontrola integriteta
  - Sigurnosne kopije
  - Vatrozid i sustav za otkrivanje napada

**Očekivanja od DBMS-a**

- Zajamčena sigurnost podataka
- Potrebno je osigurati zaštitu od:
  - Tehničkih kvarova
  - Pogrešnih transakcija
  - Zlonamjernih pristupa
- Mehanizmi za čuvanje sigurnosti baze uključeni u fizičku shemu projekta
- Mehanizmi oporavka u slučaju oštećenja

## Oporavak Baze

- Oštećenja mogu nastati od:
  - Pogrešne ili nepotpune transakcije
  - Pogrešno sastavljene transakcije
  - Softverske pogreške u DBMS-u ili operacijskom sustavu
  - Hardverske pogreške
- Moderni DBMS omogućuje povratak u što ažurnije i konzistentno stanje

**Za oporavak potrebno:**

- DBMS-ov mehanizam za upravljanje transakcijama
- Redovito stvaranje rezervnih kopija baze
- Održavanje dnevnika promjena

**Vrste oporavka**

- Neutralizacija ako je transakcija pogrešna
- Koristeći dnevnik za povratak u ranije stanje
- Rezervna kopija za uspostavljanje baze u slučaju znatnijeg oštećenja

## Ovlaštenja

- Zaštita putem SQL -naredbi GRANT i REVOKE
- Mogućnosti ovlaštenja:
  - Globalno za sve baze
  - Za jednu bazu
  - Za jednu relaciju jedne baze
  - Za pojedine atribute u jednoj relaciji

## Pogled kao mehanizam zaštite

- Pogled kao logička nezavisnost podataka
- Kreiranje pogleda pomoću CREATE VIEW
- Definiranje pogleda uključuje administratora i projektanta
- Pogledi pomažu u ograničavanju pristupa i stvaranju virtualnih relacija

## SQL Security

- Može poprimiti vrijednost DEFINER ili INVOKER
- Kontekst sigurnosti vezan uz CREATE VIEW i EXECUTE privilegije

## Sigurnost na Internetu

- Osiguravanje ovlaštenosti korisnika i integriteta akcija
- Definiranje pravila pristupa

**Zaštita baze na Internetu**

- Ograničavanje mrežnih mogućnosti DBMS-a
- Korištenje enkripcije za komunikaciju
- Osiguravanje sigurnog pohranjivanja i obrade podataka
- Anonimiziranje osjetljivih podataka
- Sigurno uklanjanje nepotrebnih podataka

**Ranjivosti**

- Nedostatak računalnih kapaciteta
- Loša kontrola pristupa
- Ograničen budžet
- Napadi na servise, curenje podataka
- Loše odabrane šifre
- Nekonzistentni sigurnosni standardi

**Enkripcija**

- Proces šifriranja kako bi se informacije učinile nečitljivim bez ključa
- Metode: DES, TripleDES, RSA, AES, Twofish

**Kriptografija**

- Kriptiranje i dekriptiranje poruka i podataka
- Uključuje simetrične i asimetrične kriptosustave

**Metode enkripcije u bazama podataka**

- API metoda
- Plug-In metoda
- TDE metoda

**Razina enkripcije**

- Polje u tablici
- Stupac
- Tablica
- Datoteka

## Rizici

- Upravljanje ključevima
- Gubitak ključeva i pristupa enkriptiranim podacima


## NoSQL Principi

- Ključ vrijednost baza
- Dokument baze
- Mapiranje

## Nerelacijske baze podataka

- Ponavljanje: Relacijske baze
  - Edgar F. Cood: "A Relational Model of Data for Large Shared Data Banks" (1970)
  - Razvoj strukturalnog jezika SEQUEL (SQL)
  - IBM's System R
  - Oracle Version2

**Prednosti relacijskih baza podataka**

- Kvalitetna i stabilna softverska rješenja
- Standardizirani i poznati SQL jezik
- Jednostavnije financijsko planiranje
- Jednostavna terminologija (tablice, stupci)

**Nedostaci relacijskih baza podataka**

- Ograničena podrška za moderne podatke
- Nije optimalan za složene strukture podataka
- SQL nije optimalan za nestandardne oblike podataka
- Potreba za razumijevanjem strukture baze
- Interni mehanizmi zaključavanja nisu pogodni za složene podatke

## NoSQL Pojam

- Prvo korištenje 1998. (Carlo Strozzi)
- Ponovno korištenje 2009.
  - "Open-source distributed, non-relational databases"

**Karakteristike NoSQL baza**

- Nerelacijska baza podataka
- Bez sheme
- Vodoravno skalabilne
- Nema pridržavanja ACID pravila
- Nestandardizirani jezik upita
- Otvorenog koda

## JSON (JavaScript Object Notation)

- Pravila:
  - Podatci se zapisuju kao parovi naziv-vrijednost
  - Podatci su odvojeni zarezom
  - Vitičasta zagrada označava objekt, uglata zagrada niz
- JSON vrijednost može biti: String, Broj, Objekt, Niz, Boolean, Null

## Razlike između relacijskih i nerelacijskih datoteka

- Nerelacijska baza: fleksibilnija, nepohranjuje podatke u tabličnom obliku
- Podatci su strukturirani u kolekcije, zapisi pohranjeni kao JSON dokumenti

## Primjene nerelacijskih baza

- Organizacija velikih količina složenih podataka
- Optimalne za podatke koji se često mijenjaju
- Podržavaju brzo razvijajuće programe

## Najpoznatije NoSQL baze

- Ključ-vrijednost baze podataka
  - DynamoDB, Riak, Berkeley DB, Redis, Voldemart, Tokyo Tyrant, Oracle NoSQL
- Dokument baze podataka
  - Smještaju dokumente u kolekcije
  - JSON, XML, BSON formati
- Stupčane baze podataka
  - Apacheov Hbase, Cassandra, Kudu
- Graf baze podataka
  - Neo4J, Apache Giraph, Infinite Graph, OrientDB, FlockDB


