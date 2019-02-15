---
title: Consistentiecontrole voor detailhandeltransacties
description: In dit onderwerp wordt de functie voor de consistentiecontrole voor detailhandeltransacties in Microsoft Dynamics 365 for Retail beschreven.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: db01a12b92574b41f1f4fe7281c23992e0d36027
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "302127"
---
# <a name="retail-transaction-consistency-checker"></a>Consistentiecontrole voor detailhandeltransacties


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

In dit onderwerp wordt de nieuwe functie voor de consistentiecontrole voor detailhandeltransacties in Microsoft Dynamics 365 for Finance and Operations versie 8.1.3 beschreven. In de consistentiecontrole worden inconsistente transacties geïdentificeerd en geïsoleerd voordat ze worden verzameld door het boekingsproces voor overzichten.

Wanneer een overzicht wordt geboekt in Retail, kan de boeking mislukken vanwege inconsistente gegevens in de tabellen met detailhandeltransacties. Het gegevensprobleem kan worden veroorzaakt door onvoorziene problemen in de verkooppunttoepassing of door incorrect geïmporteerde transacties uit verkooppuntsystemen van derden. Enkele voorbeelden van hoe deze inconsistenties kunnen worden weergegeven: 

  - Het transactietotaal in de kopteksttabel komt niet overeen met het transactietotaal op de regels.
  - Het aantal regels in de kopteksttabel komt niet overeen met het aantal regels in de transactietabel.
  - De btw in de kopteksttabel komen niet overeen met het btw-bedrag op de regels. 
  
Wanneer er inconsistente transacties worden verzameld door het boekingsproces voor overzichten, worden er inconsistente verkoopfacturen en betalingsjournalen gemaakt en mislukt het gehele boekingsproces voor overzichten. Dergelijke overzichten kunnen alleen nog worden hersteld door middel van gecompliceerde gegevenscorrecties via meerdere transactietabellen. Met de consistentiecontrole voor detailhandeltransacties kunnen dit soort problemen worden voorkomen.

Het volgende diagram biedt inzicht in het boekingsproces met de consistentiecontrole voor detailhandeltransacties.

![Boekingsproces voor overzichten met consistentiecontrole voor detailhandeltransacties](./media/validchecker.png "Boekingsproces voor overzichten met consistentiecontrole voor detailhandeltransacties")

Met het batchproces **Winkeltransacties valideren** wordt de consistentie van de tabellen met detailhandeltransacties gecontroleerd voor de volgende scenario's.

- Klantrekening: hiermee wordt gevalideerd of de klantrekening in de tabellen met detailhandeltransacties bestaat in het HQ-klantmodel.
- Regeltelling: hiermee wordt gevalideerd of het aantal regels, zoals vastgelegd in de transactiekopteksttabel, overeenkomt met het aantal regels in de verkooptransactietabellen.

## <a name="set-up-the-consistency-checker"></a>De consistentiecontrole instellen
Configureer het batchproces Winkeltransacties valideren via **Detailhandel \> IT detailhandel \> POS-boekingen** voor periodieke uitvoering. De batchverwerking kan worden gepland op basis van de organisatiehiërarchie van de winkel, op dezelfde wijze als de processen Overzichten in batch berekenen en Overzichten in batch boeken zijn ingesteld. We raden u aan dit batchproces zo te configureren dat het meerdere keren per dag wordt uitgevoerd en zo te plannen dat het na elke P-taak wordt uitgevoerd.

## <a name="results-of-validation-process"></a>Resultaten van validatieproces
De resultaten van de validatie door het batchproces worden toegevoegd aan de betreffende detailhandeltransactie. Het veld **Validatiestatus** in de record van de detailhandeltransactie wordt ingesteld op **Geslaagd** of **Fout** en de datum van de laatste validatie wordt weergegeven in het veld **Laatste validatietijd**.

Als u meer beschrijvende fouttekst voor een validatiefout wilt weergeven, selecteert u de betreffende transactierecord voor de detailhandelwinkel en klikt u op de knop **Validatiefouten**.

Transacties die de validatie niet doorstaan en transacties die nog niet zijn gevalideerd, worden niet in overzichten opgenomen. Tijdens het proces Overzicht berekenen wordt voor gebruikers een melding weergegeven als er transacties zijn die door een validatiefout niet in het overzicht zijn opgenomen.

Als een validatiefout wordt gevonden, kunt u de fout alleen herstelen door contact op te nemen met Microsoft Support. In een toekomstige versie wordt het voor gebruikers mogelijk om de betreffende records te herstellen via de gebruikersinterface. Daarnaast worden functies voor logboekregistratie en controle toegevoegd, zodat de geschiedenis van de wijzigingen kan worden bijgehouden.

> [!NOTE]
> In een toekomstige versie worden extra validatieregels toegevoegd om meer scenario's te ondersteunen.
