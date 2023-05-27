# Azure Notes

Tämä repositorio sisältää muistiinpanoja ja tietoja Microsoft Azure -pilvipalvelualustasta. Tiedot on jaettu useisiin .md-tiedostoihin, jotka käsittelevät erilaisia Azure-aiheita.

## Sisältö

1. [Azure Overview](01_azure.md)
2. [Azure Services](02_azure.md)
   * (ja niin edelleen jokaiselle tiedostolle repositoriossa)

## Käyttö

Voit käyttää näitä muistiinpanoja oppimateriaalina Azure-pilvipalvelualustasta tai viitteenä Azure-palveluiden käyttöön.

## Lisenssi

Tämä projekti on lisensoitu [MIT-lisenssillä](LICENSE).

## Contributing

Kaikki ehdotukset ja parannukset ovat tervetulleita! Lue [CONTRIBUTING.md](CONTRIBUTING.md) saadaksesi lisätietoja siitä, miten voit osallistua projektiin.

## Yhteystiedot

Jos sinulla on kysyttävää tai palautetta, ota yhteyttä (lisää yhteystietosi tähän).

## Tekoälyn käyttö sisällön luomiseen

Tämä tiedosto on luotu käyttämällä [Azure Cognitive Services](https://azure.microsoft.com/en-us/services/cognitive-services/) -palvelua nimeltä [Text Analytics](https://azure.microsoft.com/en-us/services/cognitive-services/text-analytics/). Tämä palvelu analysoi tekstin ja tunnistaa avainsanat, joita käytetään sitten tiedostojen luomiseen. Tämä on vain yksi esimerkki siitä, miten tekoälyä voidaan käyttää luomaan sisältöä.

Tässä on esimerkki Python-koodista, jota käytetään avainsanojen tunnistamiseen:

```python
import os
from azure.ai.textanalytics import TextAnalyticsClient
from azure.core.credentials import AzureKeyCredential

key = os.environ["TEXT_ANALYTICS_SUBSCRIPTION_KEY"]
endpoint = os.environ["TEXT_ANALYTICS_ENDPOINT"]

text_analytics_client = TextAnalyticsClient(endpoint=endpoint, credential=AzureKeyCredential(key))
```

## Tekijä

Nämä muistiinpanot on luotu lähes kokonaan ChatGPT-4:n ja sen käytämän **WebPilot**-lisäosan avulla.¨ 

### Loppusanat: vivaldev / Valtteri Virtanen

Muistiinpanojen kokonaisuutta kuitenkin hallitsen minä ja olen jonkin verran joutunut ohjaamaan AI:n
työskentelyä. Mielipide: **ChatGPT-4** plugineineen on uskomaton askel eteenpäin. 
Olen sanonut useasti, että jokaisen ohjelmistoalan (ja monen muun asiantuntijatyön) tulee kiireesti
opetella omanlaisensa oikea opiskelutyyli tekoälyn kanssa. Minulla siihen kului n. 1.5 kuukautta, mutta
nyt olen todella kiitollinen siitä kaikesta mentoroinnista ja asioiden juurtajaksain selittämisellä on
ollut oppimisnopeuteeni erittäin positiivinen vaikutus. 

Turha pelko pois, ainakin, sillä tekoäly vie niiden ihmisten työpaikat, jotka eivät kykene sopeutumaan 
rajusti muuttuvaan työelämään ja maailmaan ylipäätänsä. Kannattaa ottaa asiasta selvää ja pysytellä 
ns. aallon harjalla", ja hukkumisesta ei rehellisesti sanoen voi syyttää kuin itseään. Tekoäly on työ-
kalu siinä missä vaikka porakone on työmaalla. Jos et vaivaudu opettelemaan poran käyttöä, ei sinulla
siinäkään tule työsuhde jatkumaan, eikä se ollut porakoneen vika, vaan syyllinen löytyy sohvalta makaamasta.