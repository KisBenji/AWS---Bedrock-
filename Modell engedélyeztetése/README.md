## Hogyan kérhetünk hozzáférést az AI-modellekhez AWS-en?

Ahhoz, hogy egy AI-modellt használni tudjunk, szükségünk van a megfelelő AWS-jogosultságokra és adott esetben a modell aktiválására is.

### 1. IAM jogosultságok beállítása

Az alkalmazásnak vagy az EC2 példánynak megfelelő IAM jogosultságokra van szüksége.

Például az alábbi AWS által kezelt policy használható:

`AmazonBedrockFullAccess`

### 2. Modell hozzáférése

Egyes szolgáltatóknál további feltételek is vannak.

Például bizonyos Anthropic Claude modellek használata előtt ki kell tölteni egy első használathoz szükséges adatlapot (First Time Use – FTU), amelyben meg kell adni a tervezett felhasználási célt.

Más modellek esetében külön fiókszintű hozzáférésre is szükség lehet. Ezt az IAM jogosultság önmagában nem biztosítja.

### 3. Modell elérhetőségének ellenőrzése

Ellenőrizhetjük a modell hozzáférési állapotát:

```bash
aws bedrock get-foundation-model-availability \
  --region "$REGION" --model-id "$MODEL_ID"
```
### 4. Offer Token lekérdezése 

OFFER_TOKEN=$(aws bedrock list-foundation-model-agreement-offers \
  --region "$REGION" --model-id "$MODEL_ID" \
  --query 'offers[0].offerToken' --output text)
echo "$OFFER_TOKEN"

### 5. Szerződés elfogadása

```bash
aws bedrock create-foundation-model-agreement \
  --region "$REGION" --model-id "$MODEL_ID" \
  --offer-token "$OFFER_TOKEN"
```

### 4. Modell kipróbálása

Ha a hozzáférés rendben van, a terminál segítségével meghívhatjuk a modellt:

```bash
aws bedrock-runtime converse \
  --region "$REGION" \
  --model-id "$MODEL_ID" \
  --messages '[{"role":"user","content":[{"text":"Üdv! Mondj egy viccet magyarul!"}]}]' \
  --inference-config '{"maxTokens":100}'
```

Sikeres hívás esetén a modell visszaküldi a generált választ.

## Saját tapasztalatok és tesztelés

A teszt során egy EC2 példányról próbáltam elérni az Amazon Bedrock szolgáltatást AWS CLI segítségével.

A tesztek során:

- Beállítottam az EC2 példány IAM szerepkörét.
- Hozzárendeltem a szükséges Bedrock jogosultságokat.
- Kipróbáltam az Amazon Nova Micro modellt.
- Sikeresen végrehajtott egy magyar nyelvű modellhívást.
- Megvizsgáltam az OpenAI és Anthropic modellek hozzáférési feltételeit is.

Az Amazon Nova Micro modell sikeresen működött az `eu-north-1` régióban, míg más modelleknél további fiókszintű hozzáférési problémák merültek fel.


### 🔗 Hivatalos AWS dokumentáció

- [Amazon Bedrock – Request access to models](https://docs.aws.amazon.com/bedrock/latest/userguide/model-access.html)
- [Amazon Bedrock – IAM permissions](https://docs.aws.amazon.com/bedrock/latest/userguide/security-iam-awsmanpol.html)
