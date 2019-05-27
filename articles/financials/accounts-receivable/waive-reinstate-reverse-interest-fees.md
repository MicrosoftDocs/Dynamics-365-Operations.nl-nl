---
title: Rentekosten kwijtschelden, opnieuw invoeren of omkeren
description: In dit artikel wordt beschreven hoe toeslagen voor rente en bijzondere kosten kunnen worden kwijtgescholden, opnieuw ingevoerd en omgekeerd.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustInterestJourList
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59461
ms.assetid: 25ec29f3-e3ea-4abb-bf6b-f6240873b315
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cfeab6f393b63b25d595067de3eb90fc899c508b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549168"
---
# <a name="waive-reinstate-or-reverse-interest-fees"></a>Rentekosten kwijtschelden, opnieuw invoeren of omkeren

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe toeslagen voor rente en bijzondere kosten kunnen worden kwijtgescholden, opnieuw ingevoerd en omgekeerd.

Met de knoppen op het tabblad **Verzamelen** van de lijstpagina **Alle klanten** kunt u kosten kwijtschelden, omkeren of opnieuw invoeren.

-   Kwijtgescholden kosten zijn vergeven. U kunt kosten bijvoorbeeld kwijtschelden als een klant deze kosten betwist en u uw goede relatie met die klant wilt behouden.
-   Opnieuw ingevoerde kosten moeten opnieuw worden betaald. U zou eerder kwijtgescholden kosten opnieuw kunnen invoeren. U moet mogelijk kosten opnieuw invoeren als u vaststelt dat deze ten onrechte zijn kwijtgescholden.
-   Omgekeerde kosten worden van de rekening van een klant verwijderd en hoeven niet meer te worden betaald. Kosten kunnen bijvoorbeeld worden omgekeerd als de verkeerde rentevoet is geselecteerd om het verschuldigde bedrag te berekenen. U kunt een afzonderlijk proces gebruiken om de rente opnieuw te berekenen en een rentenota te maken met de nieuwe kosten voor de klant.

Al deze acties wijzigen een rentenota. Een rentenota is een bedrijfsdocument dat klanten informeert wanneer rente of kosten in rekening worden gebracht aan hun rekening. Wanneer u rente of kosten kwijtscheldt of omkeert, wordt automatisch een rentenota of correctiefactuur gemaakt om de kosten te vereffenen. Als u kwijtgescholden kosten opnieuw invoert, wordt automatisch een factuur met een debetbedrag gemaakt om de kosten die de klant verschuldigd is, opnieuw in te voeren. De volgende tabel beschrijft de resultaten van elke actie.

| Actie                                                                                                                                                                                                            | Resultaat voor de klant                                                                                             | Verwerken                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hele rentenota's kwijtschelden samen met alle rente en kosten die deze bevatten. – of – Bijzondere kosten of rentetransacties die deel uitmaken van rentenota's selecteren en kwijtschelden.                                        | De kosten worden vergeven.                                                                                           | Er wordt een creditnota of correctiefactuur voor de klant gemaakt. De creditnota wordt niet automatisch gebruikt om de rentenota, of geselecteerde rentetransacties of kosten te vereffenen die u hebt geselecteerd. Het vereffende bedrag is gelijk aan het totaalbedrag van de kosten min eventuele voorgaande betalingen die door de klant zijn gedaan en min eventuele bedragen die eerder zijn kwijtgescholden of afgeschreven. Als het bedrag van de creditnota groter is dan het door de klant verschuldigde bedrag, kunt u de creditnota converteren naar een leveranciersfactuur. U kunt vervolgens het bedrag aan de klant terugbetalen.                                                       |
| Hele rentenota's opnieuw invoeren, samen met alle rente en kosten die deze bevatten. – of – De kosten of rentetransacties die deel uitmaken van rentenota's selecteren en opnieuw invoeren.                                | Het kwijtgescholden bedrag moet weer worden betaald.                                                                                     | Er wordt een factuur met een debetbedrag gemaakt en het bedrag wordt automatisch vereffend met de eerder kwijtgescholden kosten. De werkelijke rentenota's worden niet opnieuw ingevoerd. In plaats daarvan wordt een factuur gemaakt met het bedrag dat de klant nog moet betalen. De creditnota's of correctiefacturen die zijn gemaakt om kwijtgescholden rentenota's te vereffenen, kunnen nog bestaan als ze niet zijn gebruikt om de rentenota's te vereffenen. In dit geval worden de openstaande creditnota's geannuleerd. Openstaande creditnota's worden gewoonlijk automatisch vereffend wanneer rentenota's worden kwijtgescholden. Er kan echter een openstaande creditnota bestaan als een klant een rentenota heeft betaald, ook al betwist hij de kosten. |
| Hele rentenota's omkeren. – of – Geselecteerde rentetransacties omkeren die deel uitmaken van rentenota's. **Opmerking:** U kunt bijzondere kosten niet omkeren. U kunt echter een volledige rentenota omkeren die kosten bevat. | De klant is de kosten niet meer verschuldigd. De kosten moeten echter opnieuw worden betaald als u de rente herberekent. | Het proces is hetzelfde als het proces voor het kwijtschelden van rentenota's of geselecteerde rentetransacties. Er wordt een creditnota of correctiefactuur voor de klant gemaakt. Deze creditnota wordt gebruikt om de rentenota automatisch te vereffenen. Met een afzonderlijk proces kunt u rente opnieuw berekenen en een nieuwe rentenota maken.                                                                                                                                                                                                                                                                                                                                                                                              |

> [!NOTE] 
> U kunt ook een afzonderlijk proces gebruiken om oninbare vorderingen af te schrijven. Dit proces markeert alle klanttransacties voor vereffening in plaats van alleen de toeslagen kwijt te schelden die deel uitmaken van rentenota's.

## <a name="adjust-interest-for-invoices"></a>Rente voor facturen corrigeren
U kunt niet alleen rentenota's corrigeren, maar met een van de volgende processen kunt u de rentelasten uit facturen verwijderen. Met beide processen brengt u correcties aan in de desbetreffende rentenota's.

### <a name="correct-an-invoice-that-has-associated-interest"></a>Een factuur corrigeren die bijbehorende rente heeft

U kunt een geboekte factuur corrigeren die in een rentenota is opgenomen. Met dit proces kopieert u de details uit de bestaande factuur naar een nieuwe factuur om alleen de gewenste correcties aan te brengen. De factuur wordt geannuleerd en er wordt een nieuwe factuur gemaakt. Als de rentenota was geboekt, wordt ook de rente op de transactie op de rentenota omgekeerd. 

U kunt de correctie maken door de knop **Factuur corrigeren** in het actievenster van de vrije-tekstfactuur te gebruiken. Deze knop is alleen beschikbaar als de configuratiesleutel **Correctie van vrije-tekstfactuur** is geselecteerd.

### <a name="reverse-a-customer-transaction-that-has-associated-interest"></a>Een klanttransactie met bijbehorende rente omkeren

U kunt een klanttransactie in een factuur omkeren als een onjuiste factuur is gemaakt. Als de omgekeerde klanttransactie rente heeft die in een rentenota is opgenomen en als de rentenota is geboekt, kan ook de rente op de transactie op de rentenota worden omgekeerd. De rentenota wordt geannuleerd als deze nog niet is geboekt. 

U kunt klanttransacties omkeren via de knop **Omkeren** op de pagina **Klanttransacties**.

## <a name="waive-or-reinstate-interest-notes"></a>Rentenota's kwijtschelden of opnieuw invoeren
U kunt alle kosten op geselecteerde rentenota's kwijtschelden of opnieuw invoeren. Wanneer u kosten kwijtscheldt, kan het totaalbedrag van de kwijtschelding niet groter zijn dan ingestelde bedraglimieten U kunt een rentenota alleen opnieuw invoeren als deze eerder is kwijtgescholden. 

U kunt rentenota's kwijtschelden of opnieuw invoeren via de knop **Rentenota** op het tabblad **Verzamelen** van de pagina **Klant**.

## <a name="waive-or-reinstate-interest-transactions"></a>Rentetransacties kwijtschelden of opnieuw invoeren
U kunt specifieke rentetransacties op een rentenota kwijtschelden of opnieuw invoeren in plaats van alle kosten op die rentenota te corrigeren. Wanneer u kosten kwijtscheldt, kan het totaalbedrag van de kwijtschelding niet groter zijn dan ingestelde bedraglimieten U kunt een rentetransactie alleen opnieuw invoeren als deze eerder is kwijtgescholden. 

U kunt rentenota's kwijtschelden of opnieuw invoeren via de knop **Transactierente** op het tabblad **Verzamelen** van de pagina **Klant**.

## <a name="waive-or-reinstate-fees"></a>Bijzondere kosten kwijtschelden of opnieuw invoeren
U kunt specifieke bijzondere kosten op een rentenota kwijtschelden of opnieuw invoeren in plaats van alle kosten op die rentenota te corrigeren. Wanneer u kosten kwijtscheldt, kan het totaalbedrag van de kwijtschelding niet groter zijn dan ingestelde bedraglimieten U kunt bijzondere kosten alleen opnieuw invoeren als ze eerder zijn kwijtgescholden. 

U kunt rentenota's kwijtschelden of opnieuw invoeren via de knop **Kosten** op het tabblad **Verzamelen** van de pagina **Klant**.

## <a name="reverse-interest-notes"></a>Rentenota's omkeren
U kunt alle kosten op geselecteerde rentenota's omkeren. Omgekeerde kosten worden van de rekening van een klant verwijderd en hoeven niet meer te worden betaald. Nadat de rentenota is omgekeerd, kunt u rente opnieuw berekenen en een nieuwe rentenota maken. 

U kunt rentenota's omkeren via de knop **Rentenota** op het tabblad **Verzamelen** van de pagina **Klant**.

## <a name="reverse-interest-transactions"></a>Rentetransacties omkeren
U kunt alle geselecteerde rentetransacties omkeren. Omgekeerde kosten worden van de rekening van een klant verwijderd en hoeven niet meer te worden betaald. Nadat de transacties zijn omgekeerd, kunt u rente opnieuw berekenen en een nieuwe rentenota maken.

U kunt rentetransacties omkeren via de knop **Transactierente** op het tabblad **Verzamelen** van de pagina **Klant**.

## <a name="view-the-history-of-adjustments-for-charges-that-were-waived-reinstated-or-reversed"></a>De historie weergeven van correcties voor kosten die zijn kwijtgescholden, opnieuw ingevoerd of omgekeerd
U kunt de gedetailleerde historie weergeven van correcties die zijn doorgevoerd voor rentenota's, zoals de gebruiker die de correctie heeft ingevoerd, het type correctie, het bedrag en wanneer de correctie is ingevoerd. Voordat u een nieuwe rentenota maakt zou u bijvoorbeeld de vorige correcties kunnen bekijken die voor de rentenota zijn ingevoerd. 

U kunt rentetransacties omkeren via de knop **Geschiedenis** op het tabblad **Verzamelen** van de pagina **Klant**.



