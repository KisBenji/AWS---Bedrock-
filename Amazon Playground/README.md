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


Model: ### 3 bortípus/gazdag szőlőfajta ilyen jellemzőkkel  

1. **Riesling (főleg hőmérsékleten alacsonyabb régiókban, pl. Mosel, Rheingau, Alsácia)**  
   - **Indoklás:** A Riesling természetesen magas savtartalommal (5–8 g/l) bír, és ha hűvös éghajlaton vagy korai szüretkor gyüjtik be, az alkoholtartalom alacsony marad (8–10% ABV). A borok intenzív gyümölcsös (citrus, tropikus gyümölcs), virágos és mineralis aromákat mutatnak, ami pontosan a leírásodhoz illeszkedik.  

2. **Pinot Gris (főleg Burgundia, Alsácia vagy Deutsch-Osten)**  
   - **Indoklás:** A Pinot Gris kisebb cukortartommal rendelkezik, ezért alacsonyabb alkoholtartalomú (8,5–10,5% ABV) borokat ad, miközben kivételesen magas savanyagságra (4–6 g/l) jogosít. Hűvös klímában intenzív alma, körte, citrom és fehér szőlő aromákat fejleszt, ami erősen illeszkedik a „gyümölcsös aromák” követelményhez.  

3. **Sauvignon Blanc (főleg hűvös éghajlatú régiókban, pl. Loire-völgy, Burgundia vagy Dél-Ausztrália)**  
   - **Indoklás:** A Sauvignon Blanc természetesen savanykás (5–7 g/l), és ha hűvös időjárás vagy korai szüret biztosítja, az alkoholtartalom is alacsony marad (8–9,5% ABV). A borok élénk citrusos (limon, citrom), zöldfűszeres és intenzív gyümölcsös (ananasz, mangó) aromákkal rendelkeznek, miközben a sav Anyagozott szöveg.  

**Rövid összefoglaló:** Ezek a bortípusok hűvös klímában, korai szüretben vagy alacsony cukorszintű szőlőkben termelve tökéletesen egyeznek a magas sav-, alacsony alkohol- és intenzív gyümölcsös aróma követelményekkel.
User: The wine comes from a warm climate region. Does this change your previous assessment? Explain briefly in English, considering how climate influences acidity, alcohol levels and fruit aromas.
Model: ### **Revised Assessment for Warm Climate Wines**  
Warm climates fundamentally alter the balance of acidity, alcohol, and aroma development in grapes, making the original recommendations (Riesling, Pinot Gris, Sauvignon Blanc) **less ideal**, as these varieties typically thrive in cooler regions to retain high acidity and lower alcohol. Here’s why, and three revised suggestions:

---

#### **Why Warm Climates Change the Profile**  
1. **Acidity ↓**:  
   In warm regions, grapes ripen fully under abundant sun, dissolving natural acids (malic, tartaric). This reduces total acidity (TA), often below 5 g/l unless mitigated by viticultural tricks (e.g., early harvest, cool microclimates).  

2. **Alcohol ↑**:  
   Warm sun spurs sugar accumulation. Grapes often reach high Brix levels, leading to alcohol content **>12% ABV** if fermented dry — conflicting with the “low alcohol” requirement.  

3. **Fruit Aromas ↔️**:  
   Warm climates amplify **ripeness-driven** fruit notes (stone fruits, tropical flavors) but can dull the crisp, citrusy/virginity notes prized in cooler-climate whites. Intense aromatics survive but shift toward jammy or honeyed tones.  

---

#### **3 Revised Options for Warm-Climate Wines with High Acidity, Low Alcohol & Intense Fruit Aromas**  

1. **Chenin Blanc (e.g., Loire Valley “dry” styles or South Africa’s coastal regions)**  
   - **Why it fits**:  
     Chenin Blanc can retain **moderate acidity (4–6 g/l)** even in warmth if harvested early or from cooler sites (e.g., morning slopes). Its natural acidity is higher than many warm-climate varieties.  
     - **Alcohol control**: Lower yields and early picking keep alcohol around **9–11% ABV**.  
     - **Aromas**: Offers intense stone-fruit (apricot, peach), honey, and floral notes without excessive jamminess.  

2. **Falanghina (Southern Italy, especially Campania)**  
   - **Why it fits**:  
     Falanghina ripens early, allowing growers to harvest **before extreme sugar spikes**, preserving **acidity (4–5 g/l)**. Its thick skins resist over-ripeness.  
     - **Alcohol**: Typically **9–10.5% ABV** when harvested at lower sugar levels.  
     - **Aromas**: Bright citrus (lemon zest), pear, and mineral notes with a distinctively fruity intensity.  

3. **Viognier (Plantation-grown in high-altitude warm zones, e.g., northern Spain or California mountains)**  
   - **Why it fits**:  
     Viognier *can* maintain **decent acidity (3.5–5 g/l)** if grown at altitude or with strict yield control, counteracting warm valley heat.  
     - **Alcohol**: Careful harvesting limits ABV to **10–11%**.  
     - **Aromas**: Explosive stone-fruit (peach, apricot), floral, and spicy notes — very aromatic, though prone to higher alcohol if mismanaged.  

---

#### **Key Adjustments for Warm Climates**  
To achieve **high acidity + low alcohol** in warm regions, winemakers often:  
- **Harvest early** (before peak sugar).  
- **Select acid-retaining clones** (e.g., Chenin Blanc sub-varieties).  
- **Use viticultural tricks**: shade netting, cool-favored rootstocks, or Morning-facing vineyards.  
- **Add acidity post-fermentation** (tartaric acid) if regulations permit.  

The original Riesling/Pinot Gris/Sauvignon Blanc trio remains perfect for *cool* climates, but warm regions demand varieties with **earlier ripening** and **built-in acid resilience** — like the three above.
User: A customer says: "I don't like sweet wines, but I enjoy fruity wines."

Based on the previous discussion, recommend one specific grape variety or wine style. Explain why it is suitable and clarify the difference between fruity and sweet. Keep your answer practical and concise.
Model: ### **Recommendation: Dry Chenin Blanc**  

**Why it fits:**  
- **Fruity but dry**: Dry Chenin Blanc (especially from warm regions like South Africa’s coastal zones or the Loire Valley) delivers **intense stone-fruit flavors** (peach, apricot, pineapple) and floral/honey notes *without residual sugar*. The fruitiness comes from concentrated flavor compounds, not sweetness.  
- **Acidity balance**: It retains crisp acidity (4–6 g/l), keeping the palate refreshed and preventing the wine from tasting cloying—even in warm climates.  
- **Low to moderate alcohol**: When harvested at moderate ripeness, it stays around **9–11% ABV**, avoiding the high alcohol typical of warm-climate wines.  

**Fruity vs. Sweet – The Key Difference:**  
- **Fruity** = *Flavor profile*: The wine tastes of ripe fruits (e.g., peach, citrus) due to aromatic compounds in the grapes. This can exist in **dry, off-dry, or sweet** wines.  
- **Sweet** = *Residual sugar*: Measured in grams/liter (e.g., 50+ g/l for dessert wines). Sweetness adds sweetness to the palate, coating the tongue.  

Dry Chenin Blanc is **fruity** (lots of fruit flavor) but **not sweet** (low sugar, high acidity), making it ideal for your customer.

A Nova 2 Lite jól teljesített a borászati teszt során. Különösen erős a strukturált válaszadásban, a kontextus kezelésében és az angol nyelvű fogyasztói tanácsadásban.

A modell képes volt a magyar nyelvű kérdés után angolul folytatni a beszélgetést, figyelembe venni az újonnan megadott klimatikus körülményt, és ennek megfelelően módosítani az ajánlásait.

A legnagyobb fejlesztendő terület a borászati szakmai pontosság: egyes szőlőfajták tulajdonságait és a termőhelyi összefüggéseket túl általánosan kezelte, illetve néhány konkrét állítása pontatlan volt.

A Nova 2 Lite ígéretes választás lehet egy borászati AI-asszisztens alapjául. Jól kommunikál magyarul és angolul, képes a korábbi beszélgetésre építeni, és használható fogyasztói ajánlásokat készít.

Ugyanakkor borászati szakértőként még nem tekinthető teljesen megbízhatónak, ezért további szakmai tesztelés szükséges.
