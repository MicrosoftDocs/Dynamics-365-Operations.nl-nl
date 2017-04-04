---
title: Samenvoeging van waardemodellen en afschrijvingsboeken voor vaste activa
description: "In eerdere versies zijn er twee waardering concepten voor vaste activa - waardemodellen en afschrijvingsboeken. In de Microsoft Dynamics 365 voor bewerkingen 1611 versie van zijn de functionaliteit van waardemodel en afschrijvingsboek boek functionaliteit samengevoegd tot één begrip die een boek wordt genoemd."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 6c8c005c7f5ede54ce0b6c8114cac69e2551d467
ms.lasthandoff: 03/31/2017


---

# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a>Samenvoeging van waardemodellen en afschrijvingsboeken voor vaste activa

In eerdere versies zijn er twee waardering concepten voor vaste activa - waardemodellen en afschrijvingsboeken. In de Microsoft Dynamics 365 voor bewerkingen 1611 versie van zijn de functionaliteit van waardemodel en afschrijvingsboek boek functionaliteit samengevoegd tot één begrip die een boek wordt genoemd.

De nieuwe functionaliteit 'boek' is gebaseerd op bestaande functionaliteit van waardemodellen, maar omvat ook alle functionaliteit die voorheen alleen in afschrijvingsboeken beschikbaar was. [![Boek als een samenvoeging van de functionaliteit van waardemodel en het afschrijvingsboek boek](./media/fixed-assets.png)](./media/fixed-assets.png) vanwege deze samen te voegen, kunt u nu één enkele reeks pagina's, query's en rapporten gebruiken voor alle vaste activa-processen. De tabellen in dit onderwerp geven de bestaande functionaliteit van waardemodellen en afschrijvingsboeken weer, samen met de nieuwe functionaliteit van boeken.

## <a name="setup"></a>Instellen
Standaard boeken de boeken naar zowel het grootboek (GB) als ook het subgrootboek voor vaste activa. Boeken hebben een nieuwe optie **Boeken naar grootboek**, waarmee u het boeken naar het GB kunt uitschakelen en alleen laat boeken naar het vaste-activasubgrootboek. Deze functionaliteit lijkt op het vroegere boekingsgedrag voor afschrijvingsboeken. De instelling voor journaalnamen heeft een nieuwe boekingslaag met de naam Geen. Deze boekingslaag is specifiek toegevoegd voor vaste-activatransacties. Om transacties te boeken voor boeken die niet naar het GB boeken, moet u een journaalnaam gebruiken waarvoor de boekingslaag is ingesteld op **Geen**.

|                                                  |                                 |                                 |                                                         |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
|                                                  | Afschrijvingsboek               | Waardemodel                     | Boek (nieuw)                                              |
| Boeken naar het GB                                   | Nooit                           | Altijd                          | Optie om te boeken naar het GB                                |
| Boekingslagen                                   | Niet van toepassing                  | 3: Huidig, Bewerkingen en Btw | 11: Huidig, Bewerkingen, Btw, 7 aangepaste lagen en Geen |
| Journaalnamen                                    | Journaalnamen afschrijvingsboek | GB - Journaalnamen              | GB - Journaalnamen                                      |
| Afgeleide boeken                                    | Niet toegestaan                     | Toegestaan                         | Toegestaan                                                 |
| Afschrijvingsprofiel overschrijven op activumniveau | Toegestaan                         | Niet toegestaan                     | Toegestaan                                                 |

## <a name="processes"></a>Processen
Processen maken nu gebruik van een gemeenschappelijke pagina. Sommige processen zijn alleen toegestaan als de optie **Boeken naar grootboek** in de boekconfiguratie is ingesteld op **Nee**.

|                                |                           |                     |                                          |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
|                                | Afschrijvingsboek         | Waardemodel         | Boek (nieuw)                               |
| Transactie-invoer              | Afschrijvingsboekjournaal | Vaste-activajournaal | Vaste-activajournaal                      |
| Bonusafschrijving             | Toegestaan                   | Niet toegestaan         | Toegestaan                                  |
| Historische transacties verwijderen | Toegestaan                   | Niet toegestaan         | Toegestaan, tenzij u boekt naar het GB |
| Groepsgewijs bijwerken                    | Toegestaan                   | Niet toegestaan         | Toegestaan, tenzij u boekt naar het GB |

## <a name="inquiries-and-reports"></a>Query's en rapporten
Query's en rapporten ondersteunen alle boeken. Rapporten die niet in de volgende tabel worden vermeld, ondersteunden voorheen zowel afschrijvingsboeken als ook waardemodellen en ondersteunen verder alle boektypen. Het veld **Boekingslaag** is ook toegevoegd aan rapporten, zodat u eenvoudiger transactieboekingen kunt identificeren.

|                                       |                                |                          |                          |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
|                                       | Afschrijvingsboek              | Waardemodel              | Boek (nieuw)               |
| Query's                             | Afschrijvingsboektransacties | Vaste-activatransacties | Vaste-activatransacties |
| Vaste-activaoverzicht                 | Niet toegestaan                    | Toegestaan                  | Toegestaan                  |
| Basis van vaste activa                     | Toegestaan                        | Niet toegestaan              | Toegestaan                  |
| Toepasbaarheid van vaste activa in kwartaalmidden | Toegestaan                        | Niet toegestaan              | Toegestaan                  |

## <a name="upgrade"></a>Bijwerken
Met het upgradeproces verplaatst u uw bestaande instellingen en alle uw bestaande transacties naar de nieuwe boekstructuur. De waardemodellen worden in de huidige vorm behouden, in de vorm van een boek dat boekt naar het grootboek. Afschrijvingsboeken worden echter naar een boek verplaatst waarvoor de optie **Boeken naar grootboek** is ingesteld op **Nee**. De journaalnamen van afschrijvingsboeken worden verplaatst naar een grootboekjournaalnaam, waarvoor de boekingslaag is ingesteld op **Geen**.


