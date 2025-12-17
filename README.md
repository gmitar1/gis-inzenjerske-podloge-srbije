## Digitalizovane inženjerske podloge Republike Srbije 

Ovaj repo sadrži katalog raznih inženjerskih podloga (hidrološke i geološke) kao i bazu podataka mernih vrednosti osmatračkog sistema (meteorološki, hidrološki, kvalitet vode) prvobitno namenjene za hobi projekat sveobuhvatne analize životne sredine u Republici Srbiji. Taj projekat trenutno čeka neka lepša vremena.
Međutim, nema razloga da katalog podloga stoji neiskorišćen kad je već ogroman broj sati uložen u njega a ovim putem ga obelodanjujem svim zainteresovanima. Bilo kakva vrsta upotrebe, lična ili komercijalna je dozvoljena (licenca CC0), doduše u slučaju upotrebe u komercijalne svrhe ove podatke koristiti na sopstveni rizik.

Do sada je verovatno jasno da podržavam sve inicijative otvorenih podataka i koda a po mom mišljenju podaci ovakve prirode bi trebalo da budu dostupni svim građanima, u formatu upotrebljivom za obradu. Pozvao bih sve studente, stručnjake, organizacije i hobiste koji se bave zaštitom životne sredine, inženjerstvom ili naukom uopšte da se udruže, otvore i javno podele sve svoje projekte i doprinesu društvu u potrazi za otvorenim i besplatnim znanjem. "Open-source" i "community-driven" načini razmišljanja široko su prisutni u IT zajednici i smatram da je vreme da se to proširi i na druge grane.

## Sadržaj kataloga

Katalog je organizovan kao QGIS projekat i sastoji se od 3 datoteke:

 - **project.qgz** (glavna projektna datoteka koja se učitava u QGIS)
 - **data.sqlite** (SQLite baza podataka u kojoj je smeštena geometrija kao i svi drugi podaci)
 - **data.qmd** (metapodaci, možda i nije potrebna datoteka, ispitaću pa ću skloniti ako nije)

*U slučaju da niste upoznati sa [QGIS-om](https://qgis.org/) to je "open-source" zamena za ArcGIS, postoji izdanje za Windows, Linux i Mac a toplo je preporučujem. Ove datoteke verovatno neće moći neposredno da se otvore u ArcGIS-u pa ako bude nekih problema mogu napraviti i izdanje zasnovano na .shp (shapefile) datotekama (ili jednostavno možete pružiti šansu QGIS-u :-D).*

U katalogu trenutno se nalaze sledeće podloge:

<img width="700" height="240" alt="Image" src="https://github.com/user-attachments/assets/b4fe5d4d-02bc-493e-8f5a-dc4a17f0741b" />

*(Slika 1: Slivovi i reke, hidrogeološka i karta tipa zemljišta, sa leva na desno)*

 - **Površinske vode**
   - Mreža rečnih tokova i slivna područja za velike i srednje reke prema [klasifikaciji RHMZ-a](https://www.hidmet.gov.rs/ciril/hidrologija/povrsinske/index.php)
   - Mreža drenažnih kanala i kanala za navodnjavanje kao i poligoni većih vodenih tela. Izvor je OpenStreetMap preuzeto od [Geofrabrik](https://download.geofabrik.de/europe/serbia.html)
   - Male reke i potoci su mapirani kombinacijom OpenStreetMap podataka i modela slivnog područja preko DEM-a (digital elevation model)
 - **Podzemne vode**
   - Slivna područja za podzemne vode prema [klasifikaciji RHMZ-a](https://www.hidmet.gov.rs/ciril/hidrologija/podzemne/naslovna.php)
 - **Hidrogeologija**
   - Karta sa podacima o nivou i tipu vodopropusnosti podzemnog sloja preuzeta i digitalizovana je sa [geološkog informacionog sistema Srbije](https://geoliss.mre.gov.rs/prez/geolAtlas/karte/12_hidrogeo.htm)
 - **Tip zemljišta**
   - Karta tipa zemljišta digitalizovana je na osnovu [pedološke karte Jugoslavije](https://esdac.jrc.ec.europa.eu/content/soil-map-serbia-pedoloska-karta-jugoslavije) (A. Škorić, M. Bogunović)
   - Tip zemljišta sadrži mapiranje domaće klasifikacije sa standardizovanom WRB klasifikacijom

Osim toga, veći deo podataka zapravo čine podaci različitih osmatračkih sistema:

<img width="900" height="310" alt="Image" src="https://github.com/user-attachments/assets/9df7e253-652a-48f6-a5a5-886007fd56be" />

*(Slika 2: DB Browser for SQLite snimak ekrana baze podataka)*

   - **Klimatološka merenja**
     - Podaci za 2023. godinu iz [meteorološkog godišnjaka RHMZ-a](https://www.hidmet.gov.rs/latin/meteorologija/klimatologija_godisnjaci.php)
     - Podaci za period 2023-2024 iz [operativnih biltena RHMZ-a](https://www.hidmet.gov.rs/latin/meteorologija/op_bilteni.php)
   - **Hidrološka merenja - površinske vode**
     - Podaci (protok, nivo, temperatura) za 2023. godinu iz [hidrološkog godišnjaka RHMZ-a](https://www.hidmet.gov.rs/latin/hidrologija/povrsinske_godisnjaci.php)
   - **Hidrološka merenja - podzemne vode**
     - Podaci (nivo, temperatura) za 2023. godinu iz [hidrološkog godišnjaka RHMZ-a](https://www.hidmet.gov.rs/latin/hidrologija/povrsinske_godisnjaci.php)
   - **Kvalitet vode**
     - Merenja kvaliteta vode od [agencije za zaštitu životne sredine](https://sepa.gov.rs/vode/)

## Planirani radovi

Proširenja koje su predviđena za dodavanje u sledećem izdanju:

 - Lokacije divljih deponija ([SEPA](https://data.gov.rs/sr/reuses/divlje-deponije/))
 - Merenja kvaliteta vazduha ([SEPA](https://data.gov.rs/sr/datasets/kvalitet-vazdukha/))
 - Proširenje hidroloških i klimatoloških merenja na period 2024, kao i na pre 2022 (izuzetno mukotrpan proces)
 - Karta pokrivenosti vegetacijom i urbane zone

## Komentari

 - AI (veštačka inteligencija) nije pri izradi ovih podloga, sve je "ručni rad"
 - Većina podloga nema podatke na teritoriji Kosova i Metohije. Ako uspem da nađem prošireni osmatrački sistem za KiM dodaću.

## Kontakt

Svako ko je zainteresovan da predloži, ukaže na grešku ili nejasnoću neka se slobodni javi na [LinkedIn](https://www.linkedin.com/in/aleksandar-mitrovic/) ili na <img width="177" height="20" alt="Image" src="https://github.com/user-attachments/assets/64304c13-cbab-4e48-be6d-2ca85e0aac4c" />
   
