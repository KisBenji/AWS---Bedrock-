# AWS Bedrock – Wine AI Teszt

A teszt célja, hogy összehasonlítam az AWS Bedrock platformon elérhető különböző MI modellek teljesítményét borászati témakörben.

Azt szeretném megvizsgálni, hogy melyik modell képes a legjobb minőségű, szakmailag helyes és gyakorlatban is használható válaszokat adni egy borászati szituációban.

Nemcsak a modellek általános tudását figyelem, hanem azt is, hogyan kezelik a több lépésből álló beszélgetéseket és a nyelvváltást.
A tesztelés az Amazon Web Services (AWS) Bedrock platformon történik.

Az AWS Bedrockon keresztül elérhető különböző AI-modelleket ugyanazzal a három kérdésből álló tesztsorral vizsgálom.

Minden modellt azonos feltételek mellett tesztelünk, hogy a kapott válaszok összehasonlíthatók legyenek.


## A modellek értékelési szempontjai

A teszt során hat fő képességet vizsgálunk, amelyek meghatározzák, hogy egy AI-modell mennyire alkalmas egy borászati asszisztens működtetésére.

| Vizsgált képesség | Mit szeretnénk megtudni? |
|:---|:---|
| 🇭🇺 **Magyar nyelv** | Természetes és szakmailag helyes magyar fogalmazás. |
| 🍇 **Borászati szaktudás** | Ismeri-e a szőlőfajtákat, borstílusokat és a borászati összefüggéseket? |
| 🧠 **Kontextuskezelés** | Képes-e az új információk alapján módosítani és pontosítani a korábbi válaszát? |
| 🌍 **Angol nyelv** | Természetes és nyelvtanilag helyes angol kommunikáció. |
| 🍷 **Fogyasztói tanácsadás** | Tud-e konkrét, a fogyasztói igényekhez illeszkedő borajánlást adni? |
| 🎯 **Szakmai pontosság** | Elkerüli-e a téves, félrevezető vagy kitalált információkat? |

Hogyan épül fel a teszt?

A teszt három egymásra épülő kérdésből áll:

**Magyar prompt:**
```text
Egy bornak magas a savtartalma, alacsony az alkoholtartalma és intenzív gyümölcsös aromái vannak.

Milyen szőlőfajták vagy bortípusok készülhetnek ilyen jellemzőkkel? Mondj 3 lehetőséget, rövid szakmai indoklással!
```

**Angol kérdés:** 
A modell új információt kap a termőhely meleg klímájáról. Megvizsgáljuk, hogy képes-e újragondolni korábbi következtetéseit, miközben angolra vált.

```text
The wine comes from a warm climate region. Does this change your previous assessment? Explain briefly in English, considering how climate influences acidity, alcohol levels and fruit aromas.
```

**Angol kérdés:** 
Fogyasztói szituációban kell konkrét bort ajánlania, megkülönböztetve a gyümölcsös aromákat és az édességet.

```text
A customer says: "I don't like sweet wines, but I enjoy fruity wines."
Based on the previous discussion, recommend one specific grape variety or wine style. Explain why it is suitable and clarify the difference between fruity and sweet. Keep your answer practical and concise.
```

# Kiértékelés

A **Nova 2 Lite** kiegyensúlyozott teljesítményt nyújtott. A magyar nyelvű válasza érthető és szakmailag releváns volt, bár néhány pontatlanság és megfogalmazási hiba előfordult. [Beszélgetés megtekintése](<../Nova 2 Lite/README.md>)

A meleg klímára vonatkozó kiegészítő információt megfelelően beépítette a korábbi értékelésébe. Helyesen felismerte, hogy a melegebb termőhely általában alacsonyabb savtartalommal, magasabb potenciális alkoholtartalommal és érettebb gyümölcsaromákkal járhat.

A fogyasztói ajánlás során a száraz Chenin Blanc mellett döntött. A gyümölcsösség és az édesség közötti különbséget világosan és gyakorlatiasan magyarázta el.

A **Qwen3-235B-A22B-2507** magyar nyelvű válasza jól érthető volt, és három releváns szőlőfajtát ajánlott: Riesling, Grüner Veltliner és Sauvignon Blanc. [Beszélgetés megtekintése](<../Qwen3 235B A22B 2507/README.md>)

A meleg klímára vonatkozó kérdésnél helyesen módosította a korábbi értékelését. Megfelelően magyarázta el a klíma hatását a savtartalomra, az alkoholszintre és a gyümölcsaromákra.

A harmadik kérdésben száraz Sauvignon Blanc-t ajánlott. A gyümölcsösség és az édesség különbségét helyesen és közérthetően magyarázta el.

A **Nova Micro** jól kezelte a beszélgetés egymásra épülő kérdéseit, és az angol nyelvű válaszai egyértelműek, jól strukturáltak voltak.

A magyar nyelvű első válaszban azonban több nyelvi és terminológiai hiba jelentkezett. A gyümölcsaromák felsorolásában hibás vagy értelmetlen kifejezések szerepeltek, például a „banyán” és az „aprica”.

A meleg klímára vonatkozó magyarázat alapvetően helyes volt, de az alkoholszint növekedését pontatlanul az erjedés hosszával és teljességével magyarázta. Helyesebb indoklás lett volna a szőlő magasabb cukortartalma és az ebből származó magasabb potenciális alkoholtartalom.

A harmadik kérdésre adott válasza viszont jó minőségű volt. A száraz Sauvignon Blanc ajánlása praktikus, a gyümölcsösség és édesség közötti különbség magyarázata pedig szakmailag megfelelő.

[Beszélgetés megtekintése](IDE_MÁSOLOD_BE_A_PATH-OT)
