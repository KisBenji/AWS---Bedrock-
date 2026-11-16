# Amazon Playground

Interaktív fejlesztői felület, ahol különböző AI-modellek tesztelhetők, promptok próbálhatók ki, valamint a modellek válaszai és beállításai összehasonlíthatók kódolás nélkül.

# Nova 2.5 Sonic 

Leírás: Valós idejű, hangalapú AI-modell, amely természetes, kétirányú beszélgetéseket tesz lehetővé. Támogatja a többnyelvű kommunikációt, a hangalapú utasítások értelmezését, a megszakítások kezelését és a külső eszközök használatát. Ideális hangvezérelt chatbotokhoz, AI-asszisztensekhez és telefonos ügyfélszolgálati rendszerekhez.

Prompt magyarul: 
```text
Egy AI-alapú alkalmazást szeretnék fejleszteni borászatok számára, amely drasztikusan csökkenti a napi adminisztratív feladatokra fordított időt.

Az alkalmazás egyetlen rendszerben kezelje a borászat mindennapi folyamatait: pincei munkanapló, borkezelési műveletek, laboreredmények, készletnyilvántartás, szőlőbeszállítás, dokumentáció és határidők.

Gondolkodj egyszerre borászati szakértőként, üzleti tanácsadóként és szoftverarchitektként!

Tervezz egy modern, AI-központú alkalmazást, amely:
- Automatizálja az ismétlődő adminisztratív feladatokat.
- Természetes nyelvű utasításokkal és hangvezérléssel is használható.
- AI segítségével feldolgozza a dokumentumokat és borászati adatokat.
- Figyelmeztet a fontos teendőkre, határidőkre és lehetséges problémákra.
- Mobiltelefonon és számítógépen egyaránt egyszerűen használható.

Mutasd be a legfontosabb funkciókat, egy konkrét napi használati példát, valamint a javasolt technológiai architektúrát AWS és Amazon Bedrock használatával.

A végén térj ki három kérdésre:
1. Mi lenne az alkalmazás három legértékesebb funkciója?
2. Mely adminisztratív feladatok automatizálhatók a legnagyobb mértékben?
3. Milyen MVP-verzióval indulnál, amelyet már valódi borászatok is használhatnak?

Legyél gyakorlatias, innovatív és üzletileg reális. Ne általános AI-ötleteket sorolj, hanem egy valóban megvalósítható borászati alkalmazást tervezz.
```

Válasz: A felépített prompt esetén a modell tört magyarral válaszolt. Nehéz volt a megértése és a válasz is inkább tűnt találgatásnak, mint pontos pontokba szedett ajánlásnak.

Angol nyelvre váltás hatása:

A modell azonnal tökéletes nyelvtani pontossággal adott választ és teljesen érthető lett. Amikor arra kértem viselkedjen úgy, mint egy borász és egy ügyvezető és a legfontosabb pontokat sorolja fel az applikációhoz. Határozott választ adott és ötletet, amik felhasználhatóak lennének és valóban megkönnyítenék a mindennap adminisztrációt. 


User: Egy AI-alapú alkalmazást szeretnék fejleszteni borászatok számára, amely drasztikusan csökkenti a napi adminisztratív feladatokra fordított időt.

Az alkalmazás egyetlen rendszerben kezelje a borászat mindennapi folyamatait: pincei munkanapló, borkezelési műveletek, laboreredmények, készletnyilvántartás, szőlőbeszállítás, dokumentáció és határidők.

Gondolkodj egyszerre borászati szakértőként, üzleti tanácsadóként és szoftverarchitektként!

Tervezz egy modern, AI-központú alkalmazást, amely:
- Automatizálja az ismétlődő adminisztratív feladatokat.
- Természetes nyelvű utasításokkal és hangvezérléssel is használható.
- AI segítségével feldolgozza a dokumentumokat és borászati adatokat.
- Figyelmeztet a fontos teendőkre, határidőkre és lehetséges problémákra.
- Mobiltelefonon és számítógépen egyaránt egyszerűen használható.

Mutasd be a legfontosabb funkciókat, egy konkrét napi használati példát, valamint a javasolt technológiai architektúrát AWS és Amazon Bedrock használatával.

A végén térj ki három kérdésre:
1. Mi lenne az alkalmazás három legértékesebb funkciója?
2. Mely adminisztratív feladatok automatizálhatók a legnagyobb mértékben?
3. Milyen MVP-verzióval indulnál, amelyet már valódi borászatok is használhatnak?

Legyél gyakorlatias, innovatív és üzletileg reális. Ne általános AI-ötleteket sorolj, hanem egy valóban megvalósítható borászati alkalmazást tervezz.
Model: Nagyszerű ötlet! A borászatok napi munkája rendkívül sok információ kezelését igényli: a szőléskerttől a pincéig, a laboreredményektől a jogi dokumentumig. A manuális adminisztráció időigényes, hibalehetőségekkel teli – és mégis elengedhetetlen az üzemeléshez. Egy **AI-alapú, borászatra szabott integrált platform** valóban drasztikusan csökkentheti a terhet és növelheti a hatékonyságot.

Tervezzük meg együtt a **VINAIOS (VIno + AI + Operational System)** – egy borászati műveleti szisztéma szakértő, üzleti és technológiai szemmel.

---

## 🔹 Cél
**Egy AI-központú, multiplatformos alkalmazás, amely egyetlen helyen egységesíti a borászatok egész napi munkafolyamatait, automatikusan feldolgozza az adatokat, támogat természetes nyelvű interakciót és proaktívan segít döntéshozatalban – akár napi felügyelet nélkül is működő rendszerként.**

---

## 🛠️ **Fő funkciók (AI és folyamatvezérelt)**

### 1. **AI-menedzserek – Digitális borászasszisztensek**
- Név: **"PinceMester", "AdminAssist", "LaborAI"**
- Minden egyes szerepkörnek saját AI "mentora".
- Például: *„PinceMester, ma reggel mik voltak a malolaktikus erjedés adatok a Cabernet Sauvignonnál?”* → automatikus válasz, diagrammal, trenddel.
- Hangvezérléssel és chaten is elérhető.

### 2. **Automatikus dokumentumfeldolgozás (AWS Textract + Bedrock)**
- Számlák, szőlőbeszállítói jegyzőkönyvek, laboreredmények PDF vagy kép formátumban feltöltve → AI kinyeri az adatokat (szőlőfajta, cukortartalom, savtartalom, szállító, mennyiség).
- Automatikusan frissül a készlet, napi munkanapló, labornapló.

### 3. **Intelligens munkanapló és pincei napló**
- AI generálja a pincei munkanapló bejegyzéseket a naplózott tevékenységekből (pl. „Tölcsérvezetés 4. hordó, Pinot Noir, 200 l”).
- Manuális vagy hangalapú rögzítés esetén: *„Hétfőn 10-kor tölcsérvezetést végeztünk a 3A hordón, 80 liter Pinot Noirból 3B-be”* → a rendszer automatikusan rögzíti a készletváltozást és időpontot.

### 4. **Készlet- és hordókövetés valós időben**
- Minden hordó állapota nyomon követhető: milyen bor van benne, kor, erjesztési fázisa, helye a pincében, utolsó laboradat.
- Automatikus készletösszesítés: értékesítési, beszállítói és maradék készlet.

### 5. **Laboreredmények AI-elemzése**
- AI figyeli a laboradatok (sűrűség, pH, szabad SO₂, alkoholtartalom) trendjeit.
- Figyelmeztet pl.: *„A Chardonnay pH-ja 3,7-ről 3,9-re emelkedett, növekszik a bakteriális kockázat — javaslok SO₂-dózist 20 mg/l-re”*.

### 6. **Határidő- és szabálykövetési riasztó (AI Compliance Engine)**
- Felügyeli az OIV, EU, magyar szabályozások dátumait:
  - Kéntelenítési határidők
  - Átvezetések dokumentálása
  - Áfás számlázás határideje
- Automatikusan generálja a szükséges űrlapokat (pl. vám-794, borkezelési nyilvántartás).

### 7. **Szőlőbeszállítás feldolgozása AI-láncban**
- Beszállítók küldenek képet a jegyzőkönyvnek → AI kinyeri a fajtát, cukortartalmat, mennyiséget → automatikusan frissül a beszállítói adatbázis és a pincei munkanapló.
- Beépített kalorimeter- és mustsűrűség-átváltó.

### 8. **Szóbeli naplózás + offline módban is**
- A munkás hangosan beleszól a telefont: *„Most kezdtük az erjesztést, 5 hordó Cabernet, természetes élesztő”* → AI feldolgozza, beírja a naplóba.
- Offline rögzítés, majd felhőszinkron.

---

## 📅 **Napi használati példa: Borász András, egy kis közepes méretű családi borászat tulajdonosa**

**Reggel 7:30**
- András belép a **VINAIOS appba** telefonján. AI-mentora üdvözli:  
  *„Jó reggelt! Ma három határidő: 1. SO₂-mérés a Régi Pince 2. hordójánál, 2. a Balassa-csapat szőlőt szállít délután 14 órára, 3. a vám-794 jelentés határideje pénteken.”*
- Megnyitja a hordóállapot-áttekintőt: AI jelez egy pH-emelkedést a Sangiovisén, javasol SO₂-befújást.

**8:15**
- A laborból érkezik PDF laborjegyzőkönyv. Automatikusan bekerül az AI rendszerbe, adatok kinyerése AWS Textracttel → frissül a borprofil és riasztás ha szükséges.

**9:00**
- A szőlőmunkások szállítanak mustot. Rendszergazda fényképet küld a beszállítói jegyzőkönyvről.
- AI automatikusan beolvassa: „Furmint, 21 hl, 16,2°Bx, Szabó Ferenc, 2025-09-04”
- A rendszer azonnal frissíti a pincei naplót, készletet és kifizetési javaslatot készít (fizetendő összeg).

**12:00**
- András mondja: *„VINAIOS, naplózd: ma 11-kor tölcsérvezetés volt a Sangiovisé 3A-ból 3B-be, 190 liter”* → AI rögzíti, készletváltozás frissült, hordó állapota naprakész.

**15:00**
- AI figyelmeztet: *„A 4B hordóban lévő Pinot Noir 14 napja fermet, a cukorszint nullához közelít – javaslom erjedéslezárás és malolaktikusra való átállítás.”*
- András jóváhagyja, a rendszer automatikusan létrehozza a munkabeosztást és naplóz.

**17:00**
- Jelentés készül: „Havi Összegzés – Munkaóra, készletváltozás, határidők” kiküldve a csapatnak.
- Automatikus adatszinkron a könyvelő programmal (pl. Xero vagy NAV).

---

## ☁️ **Technológiai architektúra az AWS-en (Amazon Bedrock és AI-ekoszisztéma)**

```
+---------------------------------------------------------+
|                    Felhasználói felületek               |
|   Web (React.js / Next.js) + Mobil (React Native)       |
|   Hangfelismerés: AWS Transcribe                        |
+---------------------------------------------------------+
                       ↓ (API Gateway)
+---------------------------------------------------------+
|                    Backend - Express.js / Lambda        |
|   Felhasználókezelés (Cognito), Auth, RBAC               |
+---------------------------------------------------------+
                       ↓
+---------------------------------------------------------+
|                     AI Services (Bedrock)               |
| - Természetes nyelvi értelmezés (Claude 3 Sonnet)       |
| - Dokumentumelemzés, szabálygenerálás                   |
| - Proaktív javaslatok, döntéstámogatás                  |
+---------------------------------------------------------+
                       ↓
+---------------------------------------------------------+
|                    AWS folyamat- és adatréteg           |
| - S3: dokumentumok, laborjegyzőkönyvek, képek           |
| - Textract: automata adatextrakció PDF-ből              |
| - DynamoDB: gyors tranzakciók, készlet, naplók           |
| - RDS (PostgreSQL): strukturált adatok (borok, szállítók)|
| - EventBridge: határidőfigyelés, riasztások              |
| - Step Functions: automatikus munkafolyamatok            |
+---------------------------------------------------------+
                       ↓
+---------------------------------------------------------+
|                     Integrációk                         |
| - Könyvelő rendszer (Xero, SAP, vagy API)                |
| - NAV adatszolgáltatás (vám-794 automatikus kitöltése)  |
| - IoT szenzorok (hőmérséklet, páratartalom – jövő)       |
+---------------------------------------------------------+
```

> 🔍 **Miért Amazon Bedrock?**
- Egységes API több LLM-hez (Anthropic, Mistral, Amazon Titan)
- Szigorú adatvédelem: nem tárol adatokat kint, ideális érzékeny borászati és gazdálkodási adatokhoz
- Finomhangolható prompt-engineering segítségével specifikus szakértelmet beépíteni (pl. malolaktikus erjedés kockázatának becslése)

---

## ❓ **Három kulkérdésre válasz:**

### 1. **Mi lenne az alkalmazás három legértékesebb funkciója?**

1. **Automatikus dokumentumfeldolgozás + adatbázis-frissítés**  
   → Számla, jegyzőkönyv, laborjegyzőkönyv feltöltése = 5 másodperc, helyettesít 15-20 perc gépelést naponta.

2. **AI-vezérelt határidő- és szabálykövetési motor**  
   → Automatikusan figyelmeztet a vám-794, kénezés, borkezelési nyilvántartás határidejeire – csökkenti a bírságok kockázatát.

3. **Hangalapú naplózás + offline modul**  
   → A borász a pincében kézben tartva a telefont rögzítheti tevékenységeket anélkül, hogy gép elé kellene ülnie.

> ✅ *Ezek napi legalább 1-2 óra időmegtakarítást jelentenek egy átlagos borásznak.*

---

### 2. **Mely adminisztratív feladatok automatizálhatók a legnagyobb mértékben?**

- ✔️ **Szőlőbeszállítás rögzítése** → papírjegyzőkönyvről automatikus adatfeldolgozás  
- ✔️ **Pincei munkanapló írása** → AI generálja a bejegyzéseket hangból vagy tevékenységből  
- ✔️ **Laboreredmények értelmezése és dokumentálása** → AI figyeli trendeket, javasol intézkedéseket  
- ✔️ **Készletfrissítés hordóról hordóra** → átvezetések, kikeverések, értékesítés – automatikus követés  
- ✔️ **Adatszolgáltatások (pl. vám-794)** → AI összegyűjti az adatokat, kitölt sablont, javasol leadásra  

> **Automatizációs arány:** 70-80% a naplózásban, 90% a dokumentálásban.

---

### 3. **Milyen MVP-verzióval indulnál, amelyet már valódi borászatok is használhatnak?**

### 💡 **VINAIOS MVP (v1.0) – 3 hónap alatt kifejleszthető alapváltozat**

**Funkciók:**
- ✔️ Hangvezérelt pencei napló (hangbemenet → szöveg → adatbázis)
- ✔️ Kép alapú dokumentumfeldolgozás (szőlőbeszállító jegyzőkönyv PDF/foto → adat kinyerés → készlet frissül)
- ✔️ Alapszintű borkezelési napló (átvezetés, töltés, erjedés) – kézi vagy AI-generált bejegyzések
- ✔️ Egyszerű határidőfigyelő (manuálisan hozzáadott vagy fix dátumok pl. „vám-794 15-én”)
- ✔️ Webes és mobil felület (React + React Native, AWS Amplify)

**Korlátok:**
- Nem tartalmaz még automatikus labor-adatfigyelést vagy komplex SO₂-előrejelzést.
- Nincs integráció könyvelőrendszerrel – export CSV/EXCEL.

**Cél:**
- **5-10 kis–közepes borászattal tesztelni 3 hónapon át, feedback alapján iterálni**.
- MVP után jöhetnek a bővítések: Bedrock AI javaslatok, automatikus vám-794 export, laborAPI integrációk.

---

## 🚀 Üzleti potenciál és új irányok

- **B2B modell**: havi előfizetés (pl. 7.990 Ft/borászat/hó, + bővíthető modulok)
- **Szállítókkal integrálható**: beszállítók is rögzíthetik adatokat (reputáció rendszer)
- **Adatérték**: aggregált, anonim adatok alapján klímamodell, terméskárt előrejelzés, stb. – jövőbeni szolgáltatás

---

## ✅ Összegzés: VINAIOS

> **Egy valóban megvalósítható, AI-alapú borászati operációs rendszer, amely nem csak „digitális papír”, hanem aktív munkatárs a pincében.**

Integrál minden napi folyamatot, kiveszi az adminisztráció terhét, miközben megbízható, szabálykövető és borászatra specializált. Az AWS és a **Bedrock segítségével biztonságosan, magasan skálázhatóan és üzletileg fenntarthatóan** építhető fel.

**A borászatok nem csak digitálisak lesznek – intelligensek.**  
És te vezeted a forradalmat.

---

