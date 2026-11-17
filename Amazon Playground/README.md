# AWS Bedrock – Wine AI Teszt

A teszt célja, hogy összehasonlítam az AWS Bedrock platformon elérhető különböző MI modellek teljesítményét borászati témakörben.

Azt szeretném megvizsgálni, hogy melyik modell képes a legjobb minőségű, szakmailag helyes és gyakorlatban is használható válaszokat adni egy borászati szituációban.

Nemcsak a modellek általános tudását figyelem, hanem azt is, hogyan kezelik a több lépésből álló beszélgetéseket és a nyelvváltást.
A tesztelés az Amazon Web Services (AWS) Bedrock platformon történik.

Az AWS Bedrockon keresztül elérhető különböző AI-modelleket ugyanazzal a három kérdésből álló tesztsorral vizsgálom.

Minden modellt azonos feltételek mellett tesztelünk, hogy a kapott válaszok összehasonlíthatók legyenek.


Hat fő képességet értékelünk:

Vizsgált képesség	Mit szeretnénk megtudni?

Magyar nyelv	Természetes és szakmailag helyes magyar fogalmazás

Borászati szaktudás	Szőlőfajták, borstílusok és borászati összefüggések ismerete

Kontextuskezelés	Képes-e az új információk alapján módosítani korábbi válaszát?

Angol nyelv	Természetes és helyes angol kommunikáció

Fogyasztói tanácsadás	Tud-e konkrét, megfelelő borajánlást adni?

Szakmai pontosság	Elkerüli-e a téves vagy kitalált információkat?

Hogyan épül fel a teszt?
A teszt három egymásra épülő kérdésből áll:

Magyar prompt:
 Egy bornak magas a savtartalma, alacsony az alkoholtartalma és intenzív gyümölcsös aromái vannak.

Milyen szőlőfajták vagy bortípusok készülhetnek ilyen jellemzőkkel? Mondj 3 lehetőséget, rövid szakmai indoklással!

Angol kérdés: A modell új információt kap a termőhely meleg klímájáról. Megvizsgáljuk, hogy képes-e újragondolni korábbi következtetéseit, miközben angolra vált.
The wine comes from a warm climate region. Does this change your previous assessment? Explain briefly in English, considering how climate influences acidity, alcohol levels and fruit aromas.

Angol kérdés: Fogyasztói szituációban kell konkrét bort ajánlania, megkülönböztetve a gyümölcsös aromákat és az édességet.

A customer says: "I don't like sweet wines, but I enjoy fruity wines."

Based on the previous discussion, recommend one specific grape variety or wine style. Explain why it is suitable and clarify the difference between fruity and sweet. Keep your answer practical and concise.

# Nova 2 Lite

A Nova 2 Lite egy fejlett, multimodális AI-modell, amely a teljesítményt és a hatékonyságot ötvözi. A feladat összetettségéhez igazítja a gondolkodási mélységet, ezért alkalmas összetett feladatok, automatizált munkafolyamatok, szoftverfejlesztés és üzleti alkalmazások támogatására.

User: Egy bornak magas a savtartalma, alacsony az alkoholtartalma és intenzív gyümölcsös aromái vannak.

Milyen szőlőfajták vagy bortípusok készülhetnek ilyen jellemzőkkel? Mondj 3 lehetőséget, rövid szakmai indoklással!
Model: ### 3 bortípus/grape variety, amelyek megfelelnek a leírt jellemzőknek:

---

#### 1. **Német Riesling (pl. Mosel, Rheingau, Pfalz)**
- **Indoklás:**  
  A Riesling klasszikusan **magas savtartalmat** mutat (tartós, friss savak – citrus, zelenina, mineral notes), miközben **alacsony alkoholtartalma** (8,5–12% vol.) jellemző, főleg hűvös éghajlati régiókban (pl. Mosel). Az **intenzív gyümölcsös aromák** (citrus, citrom, grapefruít, fehér személyes gyümölcsök, valamint virágos, petrol notes) erősen kiemelkednek, különösen fiatal koraiban vagy könnyű, száraz stílusban készítve. A borok könnyen élvezhetők fiatal korukban, és remek példája a sav–édesen–gyümölcsös egyensúlynak.

---

#### 2. **Vinho Verde (Észak-Portugália)**
- **Indoklás:**  
  A Vinho Verde (**zöld bor**) típus tipikusan **alacsony alkoholtartalmú** (9–11,5% vol.), mert fiatal szölőből, hűvös éghajlatból készül. A **magas savtartalom** (friss, csipős savak) és a **határozott gyümölcsös aromák** (zöld alma, citrom, görögdinnye, valamint valók, szárnyvirágok) jellemzik. A borok könnyű, könnyen inni valóak, és gyakran szénsavanyú (pezsgő) változatban is ismertek, ami tovább erősíti a friss, dinamikus jellegüket.

---

#### 3. **Grüner Veltliner (Ausztria)**
- **Indoklás:**  
  Ez az ausztriai szőlőfajta **kivételesen magas savtartalmat** termel (éles, dinamikus savak), miközben az alkoholtartalma tipikusan **közepesen alacsony** (11–13% vol.), főleg hűvös hegyvidéki szőlőkben. Az **intenzív gyümölcsös aromák** (zöld alma, káposzta virág, citrom, görögdinnye, valamint finom fűszeres jelek – fűszerbokor, fekete szerecsnyefű) egyedülálló kombinációt alkot. A borok komplexek, de ugyanakkor könnyen ivhatók fiatal korukban, és ideális kiegészítő a könnyű ételekhez.

---

### Összegzés:
- **Riesling:** A legklasszikusabb példa magas savra és intenzív aromára alacsony alkohol mellett.  
- **Vinho Verde:** Regionális specialitás, tipikusan nagyon alacsony alkohol és friss gyümölcsös jelleg.  
- **Grüner Veltliner:** Ausztria jellegzetes borfajta, amely egyedi aromakombinációval kombinálja a savanykás frissességet és a gyümölcsösséget.
User: The wine comes from a warm climate region. Does this change your previous assessment? Explain briefly in English, considering how climate influences acidity, alcohol levels and fruit aromas.
Model: ### **Revised Assessment for Warm Climate Regions**  

Warm climates **increase alcohol levels** (due to full ripening and sugar accumulation) and often **reduce natural acidity** (as malic acid diminishes during long, hot growing seasons). However, certain grapes or winemaking techniques can still produce wines with **high acidity, low alcohol, and intense fruit aromas** even in warmth. Here’s the revised list, with explanations of how these wines adapt to warm conditions:

---

#### **1. Assyrtiko (Santorini, Greece)**  
- **Why it fits warm climates:**  
  Santorini’s **volcanic soils, intense sunlight, and strong winds** create a unique microclimate. Despite the warm region, Assyrtiko retains **exceptionally high acidity** (citric and malic) due to poor soil nutrition and salt-rich conditions that slow ripening. Alcohol levels stay **moderate (12–13% ABV)** if harvested early, and the wine exhibits **intense, vibrant fruit aromas** (citrus, pineapple, grapefruit, and mineral notes). The warmth enhances flavor concentration without excessive alcohol.  

---

#### **2. Etna Bianco (Mount Etna, Sicily, Italy)**  
- **Why it fits warm climates:**  
  Mount Etna’s **high altitude, volcanic soils, and cool night temperatures** counteract Sicily’s heat. Etna Bianco (often a blend of **Carricante, Neretta, and Malvasia**) maintains **bright, crisp acidity** due to diurnal temperature swings. Alcohol remains **modest (12–13% ABV)** when picked early, while the warmth amplifies **intense, aromatic fruit flavors** (lemon zest, lime, orange blossom, and floral hints). The high elevation preserves freshness even in a hot region.  

---

#### **3. Early-Harvest Riesling (Warm-Climate Regions, e.g., South Australia or California)**  
- **Why it fits warm climates:**  
  In warm areas (e.g., **Clare Valley, Australia**, or **Central Coast, California**), Riesling can still achieve **high acidity** if harvested **very early** (before full ripeness). While alcohol may rise slightly (**11–13% ABV**), careful harvesting preserves **zesty acidity** and allows **intense, pure fruit aromas** (citrus, green apple, and stone-fruit notes). Winemakers often use **cool-fermentation techniques** and avoid oak to retain freshness. The warmth intensifies flavor depth without turning jammy or raisiny.  

---

### **Key Climate Influences Explained**  
1. **Acidity:**  
   - In warm climates, acidity naturally drops as grapes ripen.  
   - **Solutions:** Early harvesting, poor-soil grapes (like Assyrtiko), or high-altitude vineyards (like Etna) preserve acidity.  

2. **Alcohol:**  
   - Warmth boosts sugar levels → higher alcohol.  
   - **Solutions:** Early picking and selecting grapes with lower inherent sugar (e.g., Riesling) keep alcohol **low-to-moderate**.  

3. **Fruit Aromas:**  
   - Warmth concentrates flavors but can mute freshness if overripe.  
   - **Solutions:** Grapes with natural intensity (Assyrtiko’s citrus, Riesling’s aromatics) and cool nights (Etna) maintain vibrant, zesty notes.  

---

### **Conclusion**  
Warm climates *do* change the assessment: classic cool-climate varieties (like Mosel Riesling or Vinho Verde) may not fit unless grown in microclimates. However, **Assyrtiko, Etna Bianco, and early-harvest Riesling** are proven to deliver **high acidity, low-moderate alcohol, and intense fruit** even in warmth, thanks to **altitude, soil, or precise viticultural practices**.
User: A customer says: "I don't like sweet wines, but I enjoy fruity wines."

Based on the previous discussion, recommend one specific grape variety or wine style. Explain why it is suitable and clarify the difference between fruity and sweet. Keep your answer practical and concise.
Model: ### **Recommendation: Dry Assyrtiko (Santorini, Greece)**  

#### **Why it’s perfect for you:**  
- **Fruity but not sweet:** Assyrtiko delivers **intense, vibrant fruit flavors** (citrus, pineapple, grapefruit, and mineral notes) while being **bone-dry** (no residual sugar). Its high acidity keeps it refreshing and far from sweet.  
- **Warm-climate advantage:** Despite Santorini’s heat, volcanic soils and strong winds preserve acidity and prevent excessive sugar buildup, ensuring the wine stays crisp and fruit-forward without any sweetness.  

#### **Fruity vs. Sweet – Key Difference:**  
- **Fruity** = *Flavor profile*: The wine tastes of citrus, stone fruit, or tropical notes (like a juicy fruit salad), but it’s **dry** (no sugar).  
- **Sweet** = *Sugar content*: Wines with residual sugar (like dessert wines) taste syrupy or sticky, which you dislike.  

Assyrtiko gives you the **fruitiness you love** without any of the **sweetness you avoid**. Serve it chilled as an aperitif or with seafood!
