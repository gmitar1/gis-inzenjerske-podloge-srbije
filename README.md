### Digitalizovane inženjerske podloge Republike Srbije 

Ovaj repo sadrži katalog raznih inženjerskih podloga, prvobitno namenjenih za sveobuhvatnu analizu životne sredine u Republici Srbiji, u lične svrhe.
Projekat čeka neka lepša vremena, katalog podloga, međutim, ih ne mora čekati i ovim putem ga obelodanjujem svima zainteresovanim na raspolaganje. Bilo kakav tim upotrebe, lični ili komercijalni je dozvoljen.
U slučaju komercijalne upotrebe - ne garantujem tačnost podataka i odluke donositi na sopstveni rizik.

Podržavam sve inicijative otvorenog koda i otvorenih podataka i smatram da ovakvi podaci moraju biti javno dostupni u upotrebljivom formatu svim zainteresovanim građanima. 
Tlo ispod nas, vazduh koji dišemo i vodu koju pijemo na prvom mestu u vlasništvu je prirode pa zatim naroda, a ne "države", zavoda ili kojekakve korporacije.
Nadahnut prethodnim ovim putem bih pozvao sve stručnjake, entuzijaste i studente nauka koji se bave životnom sredinom ili inženjerstvom uopšte da se udruže, otvore i podele sve svoje projekte i doprinesu društvu u potrazi za otvorenim podacima.
Savršen epilog bi bio formiranje digitalne komunalne biblioteke otvorenih podataka (podloga, skupova, analiza, itd.) za teritoriju Republike Srbije. [Portal otvorenih podataka](https://data.gov.rs/sr/) postoji, 
međutim to je sve samo ne komunalna razmena podataka jer ga održava kancelarija za IT i eUpravu ili ko god već.

Sam projekat je organizovan kao QGIS projekat i sastoji se od 3 datoteke:

 - **project.qgz** (glavna projektna datoteka koja se učitava u QGIS)
 - **data.sqlite** (SQLite baza podataka u kojoj je smeštena geometrija kao i svi drugi podaci)
 - **data.qmd** (metapodaci, možda i nije potrebna datoteka, ispitaću pa ću skloniti ako nije)

Katalog trenutno sadrži sledeće podloge:

 - **Površinske vode**
   - Mreža rečnih tokova i slivna područja za velike i srednje reke prema [klasifikaciji RHMZ-a](https://www.hidmet.gov.rs/ciril/hidrologija/povrsinske/index.php)
   - Mreža drenažnih kanala i kanala za navodnjavanje kao i poligone većih vodenih tela. Izvor je OpenStreetMap preuzeto od [Geofrabrik](https://download.geofabrik.de/europe/serbia.html)
   - Male reke i potoci su mapirani kombinacijom OpenStreetMap podataka i modela slivnog područja preko DEM-a (digital elevation model)
 - **Podzemne vode**
   - Slivna područja za podzemne vode prema [klasifickaciji RHMZ-a](https://www.hidmet.gov.rs/ciril/hidrologija/podzemne/naslovna.php)
 - **Hidrogeologija**
   - Karta sa podacima o nivou i tipu vodopropusnosti podzemnog sloja preuzeta i digitalizovana od [geološkog informacionog sistema Srbije](https://geoliss.mre.gov.rs/prez/geolAtlas/karte/12_hidrogeo.htm)
 - **Tip zemljišta**
   - Karta tipa zemljišta na osnovu [pedološke karte Jugoslavije](https://esdac.jrc.ec.europa.eu/content/soil-map-serbia-pedoloska-karta-jugoslavije) (A. Škorić, M. Bogunović)
   - Tip zemljišta sadrži mapiranje domaće klasifikacije sa standardizovanom WRB klasifikacijom

  Osim toga, veći deo podataka zapravo čine podaci različitih osmatračkih sistema:

   - **Klimatološka merenja**
     - Podaci za 2023. godinu iz [meteorološkog godišnjaka RHMZ-a](https://www.hidmet.gov.rs/latin/meteorologija/klimatologija_godisnjaci.php)
     - Podaci za period 2023-2024 iz [operativnih biltena RHMZ-a](https://www.hidmet.gov.rs/latin/meteorologija/op_bilteni.php)
   - **Hidrološka merenja - površinske vode**
     - Podaci (protok, nivo, temperatura) za 2023. godinu iz [hidrološkog godišnjaka RHMZ-a](https://www.hidmet.gov.rs/latin/hidrologija/povrsinske_godisnjaci.php)
   - **Hidrološka merenja - podzemne vode**
     - Podaci (nivo, temperatura) za 2023. godinu iz [hidrološkog godišnjaka RHMZ-a](https://www.hidmet.gov.rs/latin/hidrologija/povrsinske_godisnjaci.php)
   - **Kvalitet vode**
     - Merenja kvaliteta vode od [agencije za zaštitu životne sredine](https://sepa.gov.rs/vode/)

Podloge koje su predviđene za dodavanje u sledećem izdanju:

 - Lokacije divljih deponija
 - Merenja kvaliteta vazduha
 - Proširenje hidroloških i klimatoloških merenja na period 2024, kao i na pre 2022 (izuzetno mukotrpan proces)

Prvobitna zamisao bila mi je da se prikupe sve potrebne podloge za modeliranje celokupnog hidrološkog ciklusa (mreža reka, slivovi, infiltracija - tip zemljišta, perkolacija - hidrogeološka karta).
Jedino što suštinski nedostaje su karte pokrivenosti vegetacijom i urbane zone za proračun evapotranspiraije (nadam se da ću to uspeti da dobavim u nekom od sledećih izdanja).

Sam cilj projekta mi nije bio najkristalniji ali je išao u pravcu sveobuhvatne analize stanja životne sredine, ponajviše spajanjem zagađenja vazduha i kako se to prenosi na zagađenje podzemnih i površinskih reka.
Podaci su očišćeni i standardizovani kako bi se mogli učitati u SQLite bazu podataka a GIS geometrija bi trebalo da bude negde u nivou srednje rezolucije (sasvim ok za opšte ne-lokalizovane projekte).
Samim tim što je visok kvalitet podataka bio jedan od glavnih motiva ove podloge su veoma pogodne za razne vrste hidroloških, geoloških, bioloških i drugih analiza, primenu mašinskog učenja (SQLite baza je odvojena od GIS sloja) pa na kraju krajeva i za pravljenje vizuelizacija.

Svako ko je zainteresovan za bilo kakvu diskusiju vezanu za projekat ili postoje neke nejasnoće ili pak greške nek se slobodni javi!
