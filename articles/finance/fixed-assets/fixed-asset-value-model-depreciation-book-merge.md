---
title: Samenvoeging van waardemodellen en afschrijvingsboeken voor vaste activa
description: 'In eerdere versies waren er twee waardevaststellingsconcepten voor vaste activa: waardemodellen en afschrijvingsboeken. In versie 1611 van Microsoft Dynamics 365 for Operations zijn functionaliteiten van waardemodellen en afschrijvingsboeken samengevoegd in één concept dat de naam boek draagt.'
author: moaamer
ms.date: 10/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9b11edcbf03b0917e35d9cef03834629b7b67fad
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674921"
---
# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Samenvoeging van waardemodellen en afschrijvingsboeken voor vaste activa

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt de huidige boekfunctionaliteit in vaste activa beschreven. Deze nieuwe functionaliteit is gebaseerd de functionaliteit voor waardemodellen, die beschikbaar was in eerdere versies, maar omvat ook alle functionaliteit die voorheen alleen in afschrijvingsboeken beschikbaar was.

Met de boekfunctionaliteit kunt u één set pagina's, vragen en rapporten gebruiken voor alle vaste-activaprocessen van uw organisatie. De tabellen in dit onderwerp geven de bestaande functionaliteit voor waardemodellen en afschrijvingsboeken weer, samen met de nieuwe functionaliteit voor boeken.

## <a name="setup"></a>Instelling
Standaard boeken de boeken naar zowel het grootboek (GB) als ook de subadministratie voor vaste activa. Boeken hebben een nieuwe optie **Boeken naar grootboek**, waarmee u het boeken naar het grootboek kunt uitschakelen en alleen boekt naar de subadministratie voor vaste activa. Deze functionaliteit lijkt op het vroegere boekingsgedrag voor afschrijvingsboeken. De instelling voor journaalnamen heeft een nieuwe boekingslaag met de naam Geen. Deze boekingslaag is specifiek toegevoegd voor vaste-activatransacties. Om transacties te boeken voor boeken die niet naar het grootboek boeken, moet u een journaalnaam gebruiken waarvoor de boekingslaag is ingesteld op **Geen**.


| &nbsp;                                           | Afschrijvingsboek               | Waardemodel                     | Boek (nieuw)                                              |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
| Boeken naar het grootboek                                   | Nooit                           | Altijd                          | Optie om te boeken naar het grootboek                                |
| Boekingslagen                                   | Niet van toepassing                  | 3: Huidig, Bewerkingen en Btw | 11: Huidig, Bewerkingen, Btw, 7 aangepaste lagen en Geen |
| Journaalnamen                                    | Journaalnamen afschrijvingsboek | Grootboek - journaalnamen              | Grootboek - journaalnamen                                      |
| Afgeleide boeken                                    | Niet toegestaan                     | Toegestaan                         | Toegestaan                                                 |
| Afschrijvingsprofiel overschrijven op activumniveau | Toegestaan                         | Niet toegestaan                     | Toegestaan                                                 |

## <a name="processes"></a>Processen
Processen maken nu gebruik van een gemeenschappelijke pagina. Sommige processen zijn alleen toegestaan als de optie **Boeken naar grootboek** in de boekconfiguratie is ingesteld op **Nee**.

| &nbsp;                                           | Afschrijvingsboek               | Waardemodel                     | Boek (nieuw)                                              |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
| Transactie-invoer              | Afschrijvingsboekjournaal | Vaste-activajournaal | Vaste-activajournaal                      |
| Bonusafschrijving             | Toegestaan                   | Niet toegestaan         | Toegestaan                                  |
| Historische transacties verwijderen | Toegestaan                   | Niet toegestaan         | Toegestaan, tenzij u boekt naar het GB |
| Groepsgewijs bijwerken                    | Toegestaan                   | Niet toegestaan         | Toegestaan, tenzij u boekt naar het GB |

## <a name="inquiries-and-reports"></a>Query's en rapporten
Query's en rapporten ondersteunen alle boeken. Rapporten die niet in de volgende tabel worden vermeld, ondersteunden voorheen zowel afschrijvingsboeken als ook waardemodellen en ondersteunen verder alle boektypen. Het veld **Boekingslaag** is ook toegevoegd aan rapporten, zodat u eenvoudiger transactieboekingen kunt identificeren.

| &nbsp;                                           | Afschrijvingsboek               | Waardemodel                     | Boek (nieuw)                                              |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
| Query's                             | Afschrijvingsboektransacties | Vaste-activatransacties | Vaste-activatransacties |
| Vaste-activaoverzicht                 | Niet toegestaan                    | Toegestaan                  | Toegestaan                  |
| Basis van vaste activa                     | Toegestaan                        | Niet toegestaan              | Toegestaan                  |
| Toepasbaarheid van vaste activa in kwartaalmidden | Toegestaan                        | Niet toegestaan              | Toegestaan                  |

## <a name="upgrade"></a>Bijwerken
Met het upgradeproces verplaatst u uw bestaande instellingen en alle uw bestaande transacties naar de nieuwe boekstructuur. De waardemodellen worden in de huidige vorm behouden, in de vorm van een boek dat boekt naar het grootboek. Afschrijvingsboeken worden echter naar een boek verplaatst waarvoor de optie **Boeken naar grootboek** is ingesteld op **Nee**. De journaalnamen van afschrijvingsboeken worden verplaatst naar een grootboekjournaalnaam, waarvoor de boekingslaag is ingesteld op **Geen**.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
