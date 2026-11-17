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
```text
Egy bornak magas a savtartalma, alacsony az alkoholtartalma és intenzív gyümölcsös aromái vannak.

Milyen szőlőfajták vagy bortípusok készülhetnek ilyen jellemzőkkel? Mondj 3 lehetőséget, rövid szakmai indoklással!
```

Angol kérdés: A modell új információt kap a termőhely meleg klímájáról. Megvizsgáljuk, hogy képes-e újragondolni korábbi következtetéseit, miközben angolra vált.

```text
The wine comes from a warm climate region. Does this change your previous assessment? Explain briefly in English, considering how climate influences acidity, alcohol levels and fruit aromas.
```

Angol kérdés: Fogyasztói szituációban kell konkrét bort ajánlania, megkülönböztetve a gyümölcsös aromákat és az édességet.

```text
A customer says: "I don't like sweet wines, but I enjoy fruity wines."
Based on the previous discussion, recommend one specific grape variety or wine style. Explain why it is suitable and clarify the difference between fruity and sweet. Keep your answer practical and concise.
```


A Nova 2 Lite ígéretes választás lehet egy borászati AI-asszisztens alapjául. Jól kommunikál magyarul és angolul, képes a korábbi beszélgetésre építeni, és használható fogyasztói ajánlásokat készít.

Ugyanakkor borászati szakértőként még nem tekinthető teljesen megbízhatónak, ezért további szakmai tesztelés szükséges.
