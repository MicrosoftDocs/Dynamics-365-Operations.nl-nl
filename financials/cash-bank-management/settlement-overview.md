---
title: Vereffeningsoverzicht
description: Dit artikel geeft algemene informatie over het vereffeningsproces. Het beschrijft de transactietypen die kunnen worden vereffend, wanneer en hoe de transacties kunnen worden vereffend, en de resultaten van het vereffeningsproces.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: adbfa6f99c481129e8cbf4a2dc4b23b4be1e8b34
ms.lasthandoff: 03/31/2017


---

# <a name="settlement-overview"></a>Vereffeningsoverzicht

Dit artikel geeft algemene informatie over het vereffeningsproces. Het beschrijft de transactietypen die kunnen worden vereffend, wanneer en hoe de transacties kunnen worden vereffend, en de resultaten van het vereffeningsproces.

Tijdens vereffening worden de transacties op één document toegepast op de transacties voor een ander document om het saldo van elk document te verhogen of te verlagen. Een betaling kan bijvoorbeeld worden toegepast op een factuur. Diverse transactietypen kunnen worden vereffend op verschillende tijden en via verschillende methoden. De vereffening kan ook veroorzaken dat nieuwe transacties worden gegenereerd.

## <a name="what-transactions-can-be-settled"></a>Welke transacties kunnen worden vereffend
De vereffening in Leveranciers en Klanten kan plaatsvinden tussen alle transactietypen die van invloed zijn voor het leverancierssaldo of klantsaldo, zoals facturen, betalingen, creditnota's en kosten. Elk transactietype kan met een ander transactietype worden vereffend. Bijvoorbeeld, u kunt een betaling met een factuur vereffenen, een creditnota met een factuur, een factuur met een factuur, en een betaling met een betaling. U kunt betalingen met een transactie in dezelfde rechtspersoon of in een andere rechtspersoon vereffenen. In organisaties die gebruikmaken van een model gecentraliseerde betaling [gecentraliseerde betalingen](set-up-centralized-payments.md) het betalingsproces kan stroomlijnen.

## <a name="when-to-settle-transactions"></a>Wanneer transacties vereffenen
Transacties kunnen op het moment van betalingsinvoer worden vereffend. Bijvoorbeeld, wanneer u een leverancier betaalt, selecteert u normaal gesproken de facturen om te betalen. Als u facturen selecteert, markeren u deze voor vereffening met de betaling. Wanneer klanten betaling clerks een klantbetaling vastlegt, kunnen ze de juiste facturen voor de vereffening op basis van de informatie die deel uitmaakt van de betaling van de klant markeren. De pagina **Transacties vereffenen** wordt gebruikt om transacties voor vereffening te markeren. Deze pagina kan vanuit elke niet-geboekte factuur of betaling worden geopend. Wanneer de transactie wordt geboekt, wordt ook de vereffening geboekt. De transacties kunnen ook worden vereffend nadat ze zijn geboekt. U kunt een klantbetaling invoeren en boeken zonder deze met enige facturen te vereffenen. U moet misschien eerst onderzoek doen om ervoor te zorgen dat de betaling wordt vereffend voor de juiste factuur. De pagina **Transacties vereffenen** kan worden geopend van de pagina **Alle klanten** of **Alle leveranciers**, of van de pagina **Transacties** voor elke klant of leverancier. U kunt ook geboekte vooruitbetalingen voor een factuur reserveren door de betaling voor vereffening met een inkooporder of verkooporder te markeren. In dit geval wordt de betaling nog steeds een openstaande saldo, maar deze kan niet worden vereffend met een andere factuur. De betaling wordt automatisch worden vereffend met de factuur die is gemaakt op basis van de inkooporder of verkooporder.

## <a name="how-to-settle-transactions"></a>Hoe transacties vereffenen
De transacties kunnen handmatig of automatisch worden vereffend, of met een combinatie van beide methoden. De keuze van een vereffeningsmethode is afhankelijk van bedrijfsprocessen, die vervolgens door de instelling van vereffening in Parameters voor Leveranciers en Parameters voor Klanten kunnen worden geïmplementeerd. U kunt leveranciersbetalingen en automatische afschrijvingen van de bankrekening van een klant maken via een betalingsvoorstel, dat wordt gebruikt om facturen te selecteren om te betalen. Het betalingsvoorstel handmatig wordt gestart, maar vervolgens Microsoft Dynamics 365 voor bewerkingen automatisch gemarkeerd voor vereffening geselecteerde facturen wanneer de betalingen worden gemaakt. Als betalingen handmatig worden gemaakt, kunt u de pagina **Transacties vereffenen** gebruiken om facturen te selecteren voor vereffening. U kunt de facturen handmatig selecteren, of u kunt de optie **Markeren op prioriteit** gebruiken om facturen automatisch te laten markeren voor vereffening. De optie **Markeren op prioriteit** is alleen beschikbaar voor Klanten. Als u deze optie wilt inschakelen, gebruikt u de pagina **Vereffeningsprioriteit** in Parameters van module Klanten. Als een betalingsmedewerker een betaling invoert, maar die betaling niet vereffent voordat hij of zij deze boekt, kan de betaling automatisch worden vereffend. U kunt automatische vereffening in klantparameters en parameters van module Leveranciers activeren. Wanneer u automatische vereffening gebruikt, kunt u de vooraf gedefinieerde vereffeningsorder of u kunt uw eigen vereffeningsorder prioriteit definiëren in parameters van module Klanten. Deze functionaliteit is alleen beschikbaar voor Klanten.

## <a name="results-of-settlement"></a>Resultaten van vereffening
Als de transacties zijn vereffend, wordt het openstaande saldo van elke transactie waar van toepassing verhoogd of verlaagd. In een typisch scenario, waar een factuur en een betaling worden vereffend, worden de status en het saldo van elke transactie bijgewerkt volgens de volgende regels:

-   Als het betalingsbedrag meer is dan het factuurbedrag, wordt het factuursaldo verminderd tot 0,00, en de factuur is afgesloten. De betaling blijft openstaan en het saldo is het bedrag waarmee de betaling het factuurbedrag overschrijdt.
-   Als het betalingsbedrag minder is dan het factuurbedrag, wordt het betalingssaldo verminderd tot 0,00, en de betaling is afgesloten. De factuur blijft openstaan en het saldo is het bedrag waarmee de betaling tekortschoot voor de factuur.
-   Als het betalingsbedrag gelijk is aan het factuurbedrag, worden zowel de betaling als de factuur afgesloten en is het saldo van beide 0,00.

Als een [betaling lager is dan het factuurbedrag](../accounts-payable/vendor-payments-partial-amount.md) vanwege een contantkorting, afschrijving, of onderbetaling, kunnen de factuur en de betaling nog steeds worden afgesloten, afhankelijk van de instelling van vereffening in Parameters voor Leveranciers en Parameters voor Klanten. De vereffening kan ook transacties genereren. Bijvoorbeeld, de vereffening van een factuur en betaling kunnen een contantkorting, een gerealiseerde winst of een verlies, btw-correcties, afschrijvingen of afrondingsverschillen veroorzaken.


