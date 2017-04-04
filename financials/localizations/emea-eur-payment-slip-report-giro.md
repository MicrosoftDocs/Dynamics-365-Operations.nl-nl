---
title: Slip-betalingsrapport voor europa
description: Dit onderwerp biedt informatie over betaling slip rapporten voor europa.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 264604
ms.assetid: 551e047b-4581-4a77-b470-c4f8d395c375
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 6bb98cc72c2ec0c1551412dd39d5bea3ce10e2cd
ms.openlocfilehash: c795466753ca1515790b7961b989aac6e7d63c2c
ms.lasthandoff: 03/31/2017


---

# <a name="payment-slip-report-for-europe"></a>Slip-betalingsrapport voor europa

Dit onderwerp biedt informatie over betaling slip rapporten voor europa.

De functionaliteit voor betaling slip rapporten is beschikbaar voor rechtspersonen die hun primaire adres in Denemarken, België, Zwitserland, Noorwegen of Finland. Bedrijven koppelen vaak afgedrukte betalingsbonnen aan facturen om aan te leveren een betalingsverwijzing voor boeken en vereffenen. De betalingsbon kan naast verkoopfacturen en vrije-tekstfacturen worden gebruikt voor project- of servicefacturen, aanmaningen, rentenota's en rekeningoverzichten.

## <a name="set-up-a-creditor-id-number-denmark-only"></a>Instellen van een crediteur-ID-nummer (alleen voor Denemarken)
Volg deze stappen om op te geven van uw bedrijf crediteur-ID (ID)-nummer. Uw financiële instelling, geeft dit getal. Deze wordt gebruikt als verwijzing wanneer klantbetalingen via financiële instellingen worden ontvangen.

1.  Klik op **Organisatiebeheer**&gt;**Setup**&gt;**organisatie**&gt;**rechtspersonen**.
2.  Op de **bankrekeninggegevens** sneltabblad in de **FI-crediteur-ID** uw unieke achtcijferige crediteur-ID- nummer.
3.  Sluit het formulier om de wijzigingen op te slaan.

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a>Een indeling voor betalingsbonbijlagen voor facturen, rentenota's, aanmaningen en rekeningoverzichten instellen
Volg deze stappen om in te stellen een indeling voor betaling slip bijlagen die bijgevoegd bij verkoopfacturen, vrije-tekstfacturen, rentenota's, aanmaningen en rekeningoverzichten.

1.  Klik op **klanten**&gt;**Setup**&gt;**formulieren**&gt;**formulierinstellingen**.
2.  Op de **factuur** tabblad in het **gekoppelde betaling op klantfactuur** veld, selecteert u de indeling voor betalingsbonbijlagen.
3.  Op de **vrije-tekstfactuur**, **rentenota**, **aanmaning**, en **overzicht rekening** tabbladen, selecteer een indeling voor betalingsbonbijlagen voor elk documenttype.
4.  Sluit het formulier om de wijzigingen op te slaan.

Volg deze stappen om in te stellen een indeling voor betaling slip bijlagen die projectfacturen.

1.  Klik op **projectbeheer en boekhouding**&gt;**Setup**&gt;**formulieren**&gt;**formulierinstellingen**.
2.  In de **gekoppelde betaling** veld, selecteert u de indeling voor betalingsbonbijlagen.

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a>Een indeling voor betalingsbonbijlagen toewijzen aan een klant maken
Nadat u de indeling voor betalingsbonbijlagen voor verkoopfacturen, vrije-tekstfacturen, rentenota's, aanmaningen, rekeningoverzichten en projectfacturen instelt, kunt u specifieke indelingen voor een geselecteerde klant toewijzen.

1.  Klik op **klanten**&gt;**veelgebruikte**&gt;**klanten**&gt;**alle klanten**.
2.  Een nieuwe klant maken of Selecteer een bestaande klant.
3.  Op de **factuur- en** sneltabblad in de **op een klantfactuur**, **op een vrije-tekstfactuur**, **op een rentenota**, **op een aanmaning**, **op een projectfactuur**, en **op een rekeningoverzicht** velden, selecteer de indeling voor betaling slip bijlagen en documenten van elk type die worden verzonden naar de geselecteerde klant worden gevormd.
4.  Sluit het formulier om de wijzigingen op te slaan.



