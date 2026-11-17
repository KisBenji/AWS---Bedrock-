
## Hogyan kérhetünk hozzáférést az AI-modellekhez AWS-en?

Ahhoz, hogy egy AI-modellt használni tudjunk, szükségünk van a megfelelő AWS-jogosultságokra és adott esetben a modell aktiválására is.

### 1. Amazon Bedrock megnyitása

- Lépjünk be az AWS Management Console felületére.
- Keressük meg az Amazon Bedrock szolgáltatást.
- Válasszuk ki a használni kívánt régiót, például `eu-north-1`.

### 2. Modell kiválasztása

- A bal oldali menüben nyissuk meg a **Model catalog** részt.
- Válasszuk ki a használni kívánt AI-modellt.
- Nyissuk meg a modellt a Playground felületen.

A legtöbb modell esetében az első használat során az AWS automatikusan elindítja a szükséges aktiválást, ha minden jogosultság és feltétel rendelkezésre áll.

### 3. IAM jogosultságok beállítása

Az alkalmazásnak vagy az EC2 példánynak megfelelő IAM jogosultságokra van szüksége.

Például az alábbi AWS által kezelt policy használható:

`AmazonBedrockFullAccess`

Egyes modellek első aktiválásához további AWS Marketplace jogosultságokra is szükség lehet:

- `aws-marketplace:Subscribe`
- `aws-marketplace:Unsubscribe`
- `aws-marketplace:ViewSubscriptions`

Ezeket az IAM szerepkörhöz kell hozzárendelni, ha szükségesek.

### 4. Különleges modellek hozzáférése

Egyes szolgáltatóknál további feltételek is vannak.

Például bizonyos Anthropic Claude modellek használata előtt ki kell tölteni egy első használathoz szükséges adatlapot (First Time Use – FTU), amelyben meg kell adni a tervezett felhasználási célt.

Más modellek esetében külön fiókszintű hozzáférésre is szükség lehet. Ezt az IAM jogosultság önmagában nem feltétlenül biztosítja.

### 5. Modell elérhetőségének ellenőrzése

AWS CLI segítségével ellenőrizhetjük a modell hozzáférési állapotát:

```bash
aws bedrock get-foundation-model-availability \
  --region "eu-north-1" \
  --model-id "amazon.nova-micro-v1:0"
```

### 6. Modell kipróbálása

Ha a hozzáférés rendben van, az AWS CLI segítségével is meghívhatjuk a modellt:

```bash
aws bedrock-runtime converse \
  --region "eu-north-1" \
  --model-id "eu.amazon.nova-micro-v1:0" \
  --messages '[{"role":"user","content":[{"text":"Szia! Válaszolj magyarul!"}]}]' \
  --inference-config '{"maxTokens":100}'
```

Sikeres hívás esetén a modell visszaküldi a generált választ.

## Saját tapasztalatok és tesztelés

A projekt során egy Amazon EC2 példányról próbáltam elérni az Amazon Bedrock szolgáltatást AWS CLI segítségével.

A tesztek során:

- Beállítottam az EC2 példány IAM szerepkörét.
- Hozzárendeltem a szükséges Bedrock jogosultságokat.
- Kipróbáltam az Amazon Nova Micro modellt.
- Sikeresen végrehajtottam egy magyar nyelvű modellhívást.
- Megvizsgáltam az OpenAI és Anthropic modellek hozzáférési feltételeit is.

Az Amazon Nova Micro modell sikeresen működött az `eu-north-1` régióban, míg más modelleknél további fiókszintű hozzáférési problémák merültek fel.

