---
title: Het voorspellingsmodel verbeteren (preview)
description: In dit onderwerp worden de functies beschreven die u kunt gebruiken om de prestaties van voorspellingsmodellen te verbeteren.
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
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 23c9062dcc13951792306c955b54cae6f656fec5
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4646074"
---
# <a name="improve-the-prediction-model-preview"></a>Het voorspellingsmodel verbeteren (preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp worden de functies beschreven die u kunt gebruiken om de prestaties van voorspellingsmodellen te verbeteren. U begint uw model te verbeteren in het werkgebied **Voorspellingen voor klantbetalingen** in Microsoft Dynamics 365 Finance. De stappen voor verbetering worden vervolgens uitgevoerd in de AI Builder.

## <a name="select-historical-outcomes"></a>Historische resultaten selecteren

U selecteert eerst een of meer van de drie mogelijke resultaten voor facturen: **op tijd**, **te laat** en **zeer laat**. Alle drie de resultaten moeten worden geselecteerd. Als u de selectie van een van de resultaten wist, worden facturen uit het trainingsproces gefilterd en wordt de nauwkeurigheid van de voorspelling verlaagd.

[![Resultaten bevestigen](./media/confirm-3-outcomes.png)](./media/confirm-3-outcomes.png)

Als uw organisatie slechts twee resultaten nodig heeft, wijzigt u de drempels **te laat** en **zeer laat** in 0 (nul) dagen. Op deze manier vouwt u de voorspelling samen tot een binaire status **op tijd** of **te laat**.

## <a name="select-fields"></a>Velden selecteren

Wanneer u velden selecteert die u in het model wilt opnemen, moet u er rekening mee houden dat de lijst alle beschikbare velden bevat in de Common Data Service-entiteit die is toegewezen aan de gegevens in de Azure data lake. Sommige van deze velden mogen **niet** zijn geselecteerd. De velden die niet mogen worden geselecteerd, vallen in een van de volgende drie categorieën:

- Het veld is vereist voor de Common Data Service-entiteit, maar er zijn geen gegevens voor in de data lake.
- Het veld is een ID en is daarom niet zinvol voor een machine learning-functie.
- Het veld bevat informatie die niet beschikbaar is tijdens de voorspelling.

In de volgende secties worden de velden weergegeven die beschikbaar zijn voor de factuur- en klantentiteiten, en worden de velden weergegeven die **niet** voor de training moeten worden geselecteerd. De categorie die voor elk van deze velden is opgegeven, verwijst naar de categorieën in de voorgaande lijst.
 
### <a name="invoice-common-data-model-entity"></a>Factuur Common Data Model-entiteit

In de volgende afbeelding ziet u de velden die beschikbaar zijn voor de factuurentiteit.

[![Beschikbare velden voor de factuurentiteit](./media/available-fields.png)](./media/available-fields.png)

De volgende velden moeten niet zijn geselecteerd voor training:

- **Factuurrekening** (categorie 2)
- **Is gesloten** (categorie 3): dit veld wordt gebruikt om facturen te filteren voor training (gesloten) en voorspelling (niet afgesloten).
- **Naam** (categorie 1)
- **Bron-ID** (categorie 2)
- **Bronrecord** (categorie 2)
- **Brontabel** (categorie 2)

### <a name="customer-common-data-model-entity"></a>Klant Common Data Model-entiteit

In de volgende afbeelding ziet u de velden die beschikbaar zijn voor de klantentiteit.

[![Beschikbare velden voor de klantentiteit](./media/related-entities.png)](./media/related-entities.png)

Het volgende veld moet niet zijn geselecteerd voor training:

- **Unieke sleutel rij** (categorie 2)

## <a name="filters"></a>Filters

De filters ondersteunen momenteel het voorspellingsscenario voor klantbetalingen niet. Selecteer daarom **Deze stap overslaan** en ga naar de overzichtspagina.

[![Focusmodel met filters](./media/focus-model-with-filters.png)](./media/focus-model-with-filters.png)

#### <a name="privacy-notice"></a>Privacyverklaring
Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]