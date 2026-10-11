# Windows 12 klon
 
**Datum:** 11. oktobar 2026. | **Vrijeme:** 18:42
 
Veb simulacija operativnog sistema u stilu Windows 12, napravljena kao jedna samostalna HTML stranica. Radi u svakom modernom pregledaču, bez instalacije, servera i spoljnih biblioteka.
 
## Kako je nastao
 
Ideja i zahtev: **Saša Jovanović**
Izrada: **Claude** (Anthropic), model Claude Opus 5.5
 
Ceo projekat je nastao iz jednog jedinog prompta:
 
> ok sad kreiraj windows 12 klon i da ne pada i nema greske
 
Claude je na osnovu toga sam osmislio izgled, napisao kompletan kod (oko 1.600 redova HTML, CSS i JavaScript-a), testirao ga i objavio. Nije bilo dodatnih uputstava, skica ni ručnih ispravki.
 
## Pokretanje
 
Otvorite `windows12.html` u pregledaču (Chrome, Edge, Firefox ili Safari). To je sve.
 
## Šta sadrži
 
**Radno okruženje**
- Plutajuća traka zadataka u sredini (ili levo, po izboru), sa oznakama pokrenutih aplikacija
- Gornja traka sa vremenskom prognozom i pretragom
- Ikone na radnoj površini i meni na desni klik
- Ekran za pokretanje, zaključavanje, spavanje, gašenje i restart
**Upravljanje prozorima**
- Prevlačenje, promena veličine sa svih strana, minimizacija, maksimizacija
- Pripajanje uz ivice: povucite prozor do gornje ivice za ceo ekran, do leve ili desne za pola
- Dvoklik na naslovnu traku uvećava prozor
- Na malim ekranima prozori se automatski otvaraju preko celog ekrana
**Start meni**
- Prikačene aplikacije i preporučene (skorašnje) datoteke
- Pretraga aplikacija i fajlova, otporna na kvačice (č, ć, š, ž, đ)
**Aplikacije**
- **Istraživač:** navigacija, istorija (nazad/napred), novi folder i datoteka, preimenovanje (F2), brisanje u korpu (Del), vraćanje iz korpe, pražnjenje korpe
- **Beležnica:** otvaranje, čuvanje (Ctrl+S), „Sačuvaj kao“, prelamanje redova, veličina slova, ubacivanje datuma (F5), upozorenje na nesačuvane izmene
- **Kalkulator:** osnovne operacije, procenat, kvadrat, koren, 1/x, rad sa tastature, bezbedno deljenje nulom
- **Paint:** olovka, gumica, linija, pravougaonik, elipsa, kanta za popunjavanje, 16 boja, debljina, poništavanje, čuvanje slike u folder Slike
- **Terminal:** `help`, `dir`, `cd`, `type`, `echo`, `mkdir`, `touch`, `del`, `open`, `start`, `cls`, `date`, `time`, `ver`, `whoami`, `neofetch`, `exit`, uz istoriju komandi strelicama
- **Podešavanja:** tamna/svetla tema, 8 boja isticanja, 5 pozadina, poravnanje trake, osvetljenost, zvuk, noćno svetlo, Wi-Fi, Bluetooth, avionski režim
**Brza podešavanja i kalendar**
- Prekidači za Wi-Fi, Bluetooth, avionski režim, noćno svetlo, tamni režim i uštedu baterije
- Klizači za osvetljenost i jačinu zvuka
- Obaveštenja i kalendar po mesecima
## Tehničke napomene
 
- Jedna datoteka, oko 104 KB, bez spoljnih zavisnosti
- Sve ikone su ručno pisani SVG, pozadine su CSS gradijenti
- Fajl sistem postoji samo u memoriji, a podešavanja se pamte u pregledaču (localStorage)
- Sve aplikacije se pokreću zaštićeno: ako jedna naiđe na problem, ostatak sistema nastavlja da radi
- Dijalozi su sopstveni, ne koriste `alert` i `prompt` pregledača
## Testiranje
 
Pre objavljivanja kod je proveren na sintaksne greške, a zatim pokrenut u simuliranom pregledaču (jsdom). Test je otvorio svih šest aplikacija, izvršio komande u terminalu, proverio računanje u kalkulatoru (uključujući deljenje nulom i procenat), menjao temu, pozadinu i poravnanje, koristio brza podešavanja, kalendar, meni na desni klik, Istraživač i meni za napajanje. Rezultat: **0 grešaka**.
 
Simulirani pregledač ne zamenjuje test u pravom pregledaču, pa su moguće sitne razlike u prikazu.
 
## Ograničenja
 
- Fajlovi koje napravite nestaju kada zatvorite ili osvežite stranicu
- Nema pravog interneta ni web pregledača unutar sistema
- Vremenska prognoza u gornjoj traci je demonstraciona, nije stvarna
## Pravna napomena
 
Ovo je nezavisan, nekomercijalan projekat inspirisan izgledom Windows-a. Nije proizvod kompanije Microsoft niti je sa njom povezan. „Windows“ je zaštićeni znak kompanije Microsoft Corporation.
 
