---
title: Het aanvankelijke voorspellingsmodel voor klantbetalingen evalueren (preview)
description: In dit onderwerp worden de stappen beschreven die u kunt uitvoeren om het voorspellingsmodel voor klantbetalingen te begrijpen en de effectiviteit ervan te beoordelen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 9cbe0308902071c066d18ce71e6e33422207e8ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245587"
---
# <a name="evaluate-the-initial-customer-payment-prediction-model-preview"></a>Het aanvankelijke voorspellingsmodel voor klantbetalingen evalueren (preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe u een voorspellingsmodel evalueert nadat u Financiële inzichten hebt ingeschakeld en vervolgens uw eerste model hebt gegenereerd en getraind. Dit onderwerp behandelt modellen voor het voorspellen van klantbetalingen. Het beschrijft de stappen die u kunt uitvoeren om het voorspellingsmodel voor klantbetalingen te begrijpen en de effectiviteit ervan te beoordelen.

## <a name="getting-details-about-the-model"></a>Details over het model ophalen

Op de pagina **Parameters voor financiële inzichten** in Microsoft Dynamics 365 Finance wordt een koppeling **Nauwkeurigheid van modellen verbeteren** naast de nauwkeurigheidsscore weergegeven.

[![Koppeling modelnauwkeurigheid verbeteren](./media/prediction-model.png)](./media/prediction-model.png)

Met deze koppeling kunt u naar AI Builder gaan, waar u meer over het huidige model kunt leren en stappen kunt ondernemen om het model te verbeteren. In de volgende afbeelding wordt de geopende pagina weergegeven.

[![AI Builder](./media/what-to-predict.png)](./media/what-to-predict.png)

In de geopende pagina wordt de volgende informatie weergegeven:

- In de sectie **Prestaties** ziet u de kwaliteit van het model. Zie voor meer informatie over deze beoordeling [Prestaties van het voorspellingsmodel](https://docs.microsoft.com/ai-builder/prediction-performance) in de AI Builder-documentatie.
- De sectie **Meest invloedrijke gegevens** laat zien hoe belangrijk verschillende invoertypen van gegevens voor uw model waren. U kunt deze lijst en de bijbehorende percentages evalueren om te bepalen of de gegevens consistent zijn met wat u van uw bedrijf en markt weet.

    [![Secties Prestaties en Meest invloedrijke gegevens voor het voorspellingsmodel](./media/models.png)](./media/models.png)

- Selecteer in de sectie **Prestaties** de optie **Details weergeven** voor meer informatie over de kwaliteit en andere overwegingen. In de volgende afbeelding laten de details zien dat het model minder informatie gebruikt dan wordt aanbevolen. Daarom heeft het systeem een waarschuwingsbericht gegenereerd.

    [![Waarschuwingen over de prestaties van het model](./media/details.png)](./media/details.png)

## <a name="digging-deeper"></a>Dieper graven

Hoewel nauwkeurigheid een goed uitgangspunt is voor het evalueren van een model en de prestatiebeoordeling informatie verschaft, biedt AI Builder gedetailleerder metrische gegevens die u kunt gebruiken voor uw evaluatie. Als u de details wilt downloaden, selecteert u in de sectie **Prestaties** de knop met het weglatingsteken (**...**) naast de knop **Model gebruiken** en selecteert u **Gedetailleerde metrische gegevens downloaden**.

[![Opdracht Gedetailleerde metrische gegevens downloaden](./media/performance.png)](./media/performance.png)

In de volgende afbeelding ziet u de indeling waarin u de gegevens kunt downloaden.

[![Indeling van gedownloade gegevens](./media/data-format.png)](./media/data-format.png)

Een goed uitgangspunt voor een betere analyse van de resultaten is het controleren van de metrische gegevens van de verwarringsmatrix. Hier ziet u deze gegevens voor de vorige afbeelding.

`{"name": "Confusion Matrix", "value": {"schema_type": "confusion_matrix", "schema_version": "1.0.0", "data": {"class_labels": ["0", "1", "2"], "matrix": [[71, 9, 21], [5, 0, 27], [2, 0, 45]]}}, "type": "dictionaryNumericalList", "isGlobalScore": false}`

U kunt deze gegevens op de volgende manier uitbreiden.

|                          | Voorspeld op tijd | Voorspeld te laat | Voorspeld zeer laat |
|--------------------------|-------------------|----------------|---------------------|
| Werkelijke op tijd-betaling   | **71**            | 0              | 21                  |
| Werkelijke te late betaling      | 5                 | **0**          | 27                  |
| Werkelijke zeer late betaling | 2                 | 0              | **45**              |

De verwarringsmatrix toont de resultaten van een willekeurig geselecteerde testgegevensset uit het trainingsproces. Omdat deze gesloten facturen niet zijn gebruikt om het model te trainen, zijn het goede testcases voor het model. Bovendien kunnen ook de prestaties van het model worden gezien, omdat de werkelijke status van de factuur bekend is.

Het eerste wat u moet opzoeken is de meest voorkomende werkelijke waarde. Hoewel deze waarde mogelijk niet perfect is afgestemd op de algehele gegevensset, is deze een redelijke benadering. In dit geval vindt **Werkelijke op tijd-betaling** plaats voor 92 van het totaal aan 171 facturen en is dit de meest voorkomende werkelijke waarde. Daarom is het een goede basislijn voor uw model. Als u zojuist hebt geschat dat alle facturen op tijd zouden zijn, zou u 92 van 171 maal gelijk hebben, dat wil zeggen 54 procent van de tijd.

Het is belangrijk dat u begrijpt hoe evenwichtig uw gegevensset is. In dit geval zijn 92 van de 171 facturen op tijd betaald, 32 te laat en 47 zeer laat. Deze waarden geven een redelijk evenwichtige gegevensset aan, omdat er niet-triviale resultaten zijn voor elke classificatie. Een situatie waarin een van de statussen zeer weinig resultaten heeft, kan lastig zijn voor een machine learning model.

De nauwkeurigheid van het model geeft het aantal juiste voorspellingen voor de test-gegevensset aan. Deze juiste voorspellingen zijn de waarden die vet worden weergegeven in het vorige voorbeeld. In dit geval genereren de waarden een berekende nauwkeurigheid van 67,8 procent (= \[71 + 0 + 45\] ÷ 171). Deze waarde vertegenwoordigt een verbetering van 14 procent over de basislijn van 54 procent en is één indicator van de kwaliteit van het model.

Als u beter naar de verwarringsmatrix kijkt, zult u zien dat het model goed werkt voor het voorspellen van de tijdige en zeer late factuurbetalingen. Het is echter niet correct voor alle 32 facturen die in werkelijkheid te laat zijn betaald (maar niet zeer laat). Dit resultaat suggereert dat extra verkenning en verbetering van het model nodig zijn.

Een getal dat de prestaties van het model beter weergeeft dan nauwkeurigheid is de F1-macroscore. Deze score houdt rekening met de resultaten van elke classificatiestatus (op tijd, te laat en zeer laat). U ziet bijvoorbeeld hier de gegevens die worden weergegeven voor de F1-macro-metriek in de vorige afbeelding.

`{"name": "F1 Macro", "value": 0.4927170868347339, "type": "percentage", "isGlobalScore": false}`

In dit geval geeft de F1-macroscore van circa 49,3 procent aan dat het model geen doeltreffende voorspellingen oplevert voor elke status, ondanks een algehele nauwkeurigheidscore die redelijk hoog lijkt.

## <a name="improving-the-model"></a>Het model verbeteren

Wanneer u de resultaten van uw eerste model beter begrijpt, kunt u het model verbeteren door functiekolommen toe te voegen of te verwijderen of door delen van de gegevensset te filteren die accurate voorspellingen niet ondersteunen. Sluit AI Builder en gebruik de koppeling **Model verbeteren** in Dynamics 365 Finance om het AI Builder-proces opnieuw te starten. U kunt experimenteren met verschillende kenmerken zonder dat dit van invloed is op het gepubliceerde model. Het gepubliceerde model wordt alleen beïnvloed als u de optie **Publiceren** kiest. Houd er rekening mee dat een enkel model wordt gebruikt voor uw exemplaar van Dynamics 365 Finance. U moet daarom zorgvuldig elk nieuw model controleren voordat u het publiceert.

## <a name="for-more-information"></a>Meer informatie

Voor meer informatie over het evalueren van voorspellingsmodellen, [Resultaten van machine learning modellen](/confusion-matrix.md)

#### <a name="privacy-notice"></a>Privacyverklaring
Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]