---
title: Vereffeningsoverzicht
description: Dit onderwerp biedt algemene informatie over het vereffeningsproces. Het beschrijft welke transactietypen kunnen worden vereffend en de timing en het proces om deze te vereffenen. Ook worden de resultaten van het vereffeningsproces beschreven.
author: kweekley
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a4ad8a124b2de2d364e11b6a32f8845ef438e1d1
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989158"
---
# <a name="settlement-overview"></a>Vereffeningsoverzicht

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt algemene informatie over het vereffeningsproces. Het beschrijft welke transactietypen kunnen worden vereffend en de timing en het proces om deze te vereffenen. Ook worden de resultaten van het vereffeningsproces beschreven.

Tijdens vereffening worden de transacties op één document toegepast op de transacties voor een ander document om het saldo van elk document te verhogen of te verlagen. Bijvoorbeeld, een betaling kan worden toegepast voor een factuur. Diverse transactietypen kunnen op verschillende tijden en door verschillende methoden worden vereffend. Het vereffeningsproces kan ook nieuwe transacties genereren.

## <a name="what-transactions-can-be-settled"></a>Welke transacties kunnen worden vereffend

De vereffening in Leveranciers en Klanten kan plaatsvinden tussen alle transactietypen die van invloed zijn voor het leverancierssaldo of klantsaldo. Deze transactietypen kunnen facturen, betalingen, creditnota's en bijzondere kosten zijn. Elk transactietype kan met een ander transactietype worden vereffend. Bijvoorbeeld, u kunt een betaling met een factuur vereffenen, een creditnota met een factuur, een factuur met een andere factuur, en een betaling met een andere betaling.

U kunt betalingen met een transactie in dezelfde rechtspersoon of in een andere rechtspersoon vereffenen. In organisaties die een gecentraliseerd betalingsmodel gebruiken, kunnen [gecentraliseerde betalingen](set-up-centralized-payments.md) het betalingsproces helpen stroomlijnen.

## <a name="when-to-settle-transactions"></a>Wanneer transacties vereffenen

Transacties kunnen worden vereffend wanneer betalingen worden ingevoerd. Bijvoorbeeld, wanneer u een leverancier betaalt, selecteert u normaal gesproken welke facturen worden betaald. Door facturen te selecteren, markeert u deze voor vereffening voor de betaling. Wanneer de medewerkers van klantbetalingen klantbetalingen registreren, kunnen ze de gewenste facturen voor vereffening markeren, op basis van de informatie die bij de betaling van de klant is opgenomen. Gebruik de pagina **Transacties vereffenen** om transacties voor vereffening te markeren. U kunt deze pagina openen vanuit elke niet-geboekte factuur of betaling worden geopend. Wanneer de transactie wordt geboekt, wordt ook de vereffening geboekt. 

De transacties kunnen ook worden vereffend nadat ze zijn geboekt. U kunt een klantbetaling invoeren en boeken zonder deze met enige facturen te vereffenen. U moet misschien eerst onderzoek doen om ervoor te zorgen dat de betaling wordt vereffend voor de juiste factuur voordat u de vereffening boekt. De pagina **Transacties vereffenen** kan worden geopend van de pagina **Alle klanten** of **Alle leveranciers**, of van de pagina **Transacties** voor elke klant of leverancier.

U kunt ook geboekte vooruitbetalingen voor een factuur reserveren door de betaling voor vereffening met een inkooporder of verkooporder te markeren. In dit geval heeft de betaling nog een openstaande saldo, maar kan deze niet met een andere factuur worden vereffend. De betaling wordt automatisch vereffend met de factuur die van de inkooporder of de verkooporder is gemaakt.

## <a name="how-to-settle-transactions"></a>Hoe transacties vereffenen

De transacties kunnen handmatig of automatisch worden vereffend, of met een combinatie van beide methoden. De keuze van een vereffeningsmethode hangt af van uw bedrijfsprocessen. Op de pagina's **Parameters van module Leveranciers** en **Parameters van module Klanten** kunt u het vereffeningsproces zo configureren dat het wordt afgestemd op deze bedrijfsprocessen.

U kunt leveranciersbetalingen en automatische afschrijvingen van de bankrekening van een klant maken via een betalingsvoorstel. Een betalingsvoorstel wordt gebruikt voor het selecteren van te betalen facturen. Het betalingsvoorstel wordt handmatig gestart, en vervolgens markeert het systeem automatisch de geselecteerde facturen voor vereffening wanneer de betalingen worden gemaakt.

Als betalingen handmatig worden gemaakt, kunt u de pagina **Transacties vereffenen** gebruiken om facturen te selecteren voor vereffening. U kunt de facturen handmatig selecteren, of u kunt de optie **Markeren op prioriteit** gebruiken om facturen automatisch te laten markeren voor vereffening. De optie **Markeren op prioriteit** is alleen beschikbaar voor Klanten. U kunt deze optie inschakelen op het tabblad **Vereffeningsprioriteit** van de pagina **Parameters van module Klanten**.

Als een betalingsmedewerker een betaling invoert, maar die betaling niet vereffent voordat deze wordt geboekt, kan de betaling automatisch worden vereffend. U kunt automatische vereffening inschakelen op de pagina's **Parameters van module Klanten** en **Parameters van module Leveranciers**. Automatische vereffening vereffent alleen transacties in dezelfde rechtspersoon. Er worden geen transacties over meerdere rechtspersonen vereffend.

Wanneer u automatische vereffening gebruikt, kunt u de vooraf vastgestelde vereffeningsprioriteit gebruiken, of u kunt uw eigen vereffeningsprioriteit op de pagina **Parameters van module Klanten** definiëren. Deze functionaliteit is alleen beschikbaar voor Klanten.

## <a name="results-of-settlement"></a>Resultaten van vereffening

Als de transacties zijn vereffend, wordt het openstaande saldo van elke transactie waar van toepassing verhoogd of verlaagd. In een typisch scenario, waar een factuur en een betaling worden vereffend, worden de status en het saldo van elke transactie bijgewerkt volgens de volgende regels:

- Als het betalingsbedrag meer is dan het factuurbedrag, wordt het factuursaldo verminderd tot 0,00, en de factuur is afgesloten. De betaling blijft openstaan en het saldo is het verschil waarmee het betalingsbedrag het factuurbedrag overschrijdt.
- Als het betalingsbedrag minder is dan het factuurbedrag, wordt het betalingssaldo verminderd tot 0,00, en de betaling is afgesloten. De betaling blijft openstaan en het saldo is het verschil waarmee het betalingsbedrag het factuurbedrag overschrijdt.
- Als het betalingsbedrag gelijk is aan het factuurbedrag, worden zowel de betaling als de factuur afgesloten en is het saldo van beide verminderd tot 0,00.

Als het [betalingsbedrag lager is dan het factuurbedrag](../accounts-payable/vendor-payments-partial-amount.md) vanwege een contantkorting, afschrijving, of onderbetaling, kunnen de factuur en de betaling nog steeds worden afgesloten, afhankelijk van de configuratie voor vereffeningen op de pagina's **Parameters van module Leveranciers** en **Parameters van module Klanten**.

Vereffeningen kunnen ook transacties genereren. Bijvoorbeeld, de vereffening van een factuur en een betaling kunnen een contantkorting, een gerealiseerde winst of een verlies, btw-correcties, afschrijvingen of afrondingsverschillen veroorzaken.

## <a name="identifying-marked-transactions-during-settlement"></a>Gemarkeerde transacties tijdens vereffening identificeren

Wanneer u een transactie probeert te vereffenen, ziet u mogelijk een symbool dat aangeeft dat de transactie is gemarkeerd op een andere locatie. In dat geval kunt u de transactie selecteren op de pagina **Transacties vereffenen** en vervolgens **Query \> Vereffening** selecteren in het venster Vereffening. De weergave voor deze query toont journalen, verkooporders, facturen, betalingsvoorstellen en klantlocaties die mogelijk de transactie vanuit de vereffening blokkeren. Om het probleem op te lossen, kunt u de koppeling selecteren om rechtstreeks van de query naar de geblokkeerde locatie te gaan. U kunt het document vervolgens bijwerken met de correcties die nodig zijn om het document te vereffenen. U kunt ook de indicator **Gemarkeerd** gebruiken om andere documenten aan te duiden die op dezelfde blokkeerlocatie zijn opgenomen.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Restbedrag vereffenen](settle-remainder.md)
