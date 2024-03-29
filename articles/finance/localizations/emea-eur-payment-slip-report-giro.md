---
title: Betalingsbonrapport voor Europa
description: Dit artikel bevat informatie over betalingsbonrapporten voor Europa.
author: mrolecki
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OMLegalEntities, ProjFormletterParameters, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 264604
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: mrolecki
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 99e06f383c94db6d2a1585d33d9f183b0984f5a3
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689589"
---
# <a name="payment-slip-report-for-europe"></a>Betalingsbonrapport voor Europa

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over betalingsbonrapporten voor Europa.

De functionaliteit voor betalingsbonrapporten is beschikbaar voor rechtspersonen die hun primaire adres in Denemarken, België, Zwitserland, Noorwegen of Finland hebben. Om klanten van dienst te zijn koppelen bedrijven vaak afgedrukte betalingsbonnen aan facturen en leveren een betalingsverwijzing voor het boeken en vereffenen. De betalingsbon kan naast verkoopfacturen en vrije-tekstfacturen worden gebruikt voor project- of servicefacturen, aanmaningen, rentenota's en rekeningoverzichten.

## <a name="set-up-a-creditor-id-number-denmark-only"></a>Een crediteur-ID-nummer instellen (alleen Denemarken)
Voer de volgende stappen uit om het crediteur-ID-nummer van uw bedrijf in te voeren. Uw financiële instelling verstrekt dit nummer. Dit nummer wordt gebruikt als verwijzing wanneer klantbetalingen via financiële instellingen worden ontvangen.

1.  Klik op **Organisatiebeheer** &gt; **Instellen** &gt; **Organisatie** &gt; **Rechtspersonen**.
2.  Voer op het sneltabblad **Bankrekeninggegevens** in het veld **FI-crediteur-ID** uw unieke achtcijferige crediteur-ID-nummer in.
3.  Sluit het formulier om de wijzigingen op te slaan.

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a>Een betalingsbonbijlage-indeling voor facturen, rentenota's, aanmaningen en overzichten instellen
Voer de volgende stappen uit om indeling voor betalingsbonbijlagen in te stellen die worden bijgevoegd bij verkoopfacturen, vrije-tekstfacturen, rentenota's, aanmaningen en rekeningoverzichten.

1.  Klik op **Klanten** &gt; **Instellen** &gt; **Formulieren** &gt; **Formulierinstelling**.
2.  Selecteer op het tabblad **Factuur** in het veld **Bijlage 'gekoppelde betaling' bij klantfactuur** de indeling voor betalingsbonbijlagen in.
3.  Selecteer op de tabbladen **Vrije-tekstfactuur**, **Rentenota**, **Aanmaning** en **Rekeningoverzicht** een indeling voor betalingsbonbijlagen voor elk documenttype.
4.  Sluit het formulier om de wijzigingen op te slaan.

Voer de volgende stappen uit om een indeling voor betalingsbonbijlagen in te stellen die bij projectfacturen worden bijgevoegd.

1.  Klik op **Projectbeheer en boekhouding** &gt; **Instellen** &gt; **Formulieren** &gt; **Formulierinstelling**.
2.  Selecteer in het veld **Bijlage gekoppelde betaling** de indeling voor betalingsbonbijlagen.

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a>Een indeling voor een betalingsbonbijlage aan een klantrekening toewijzen
Nadat u de indeling voor betalingsbonbijlagen hebt ingesteld voor verkoopfacturen, vrije-tekstfacturen, rentenota's, aanmaningen, projectfacturen en rekeningoverzichten, kunt u specifieke indelingen voor een geselecteerde klant toewijzen.

1.  Klik op **Klanten** &gt; **Algemeen** &gt; **Klanten** &gt; **Alle klanten**.
2.  Maak een nieuwe klant of selecteer een bestaande klant.
3.  Selecteer op het sneltabblad **Factuur en levering** in de velden **Op een klantfactuur**, **Op een vrije-tekstfactuur**, **Op een rentenota**, **Op een aanmaning**, **Op een projectfactuur** en **Op een rekeningoverzicht** de indeling voor betalingsbonbijlagen die worden bijgevoegd bij documenten van elk willekeurig type, die worden verzonden naar de geselecteerde klant.
4.  Sluit het formulier om de wijzigingen op te slaan.


Zie [NO-00002 Klantbetaling op basis van betalings-id](tasks/no-00002-customer-payment-based-payment-id.md) voor meer informatie over het instellen en onderhouden van betalings-id's.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
