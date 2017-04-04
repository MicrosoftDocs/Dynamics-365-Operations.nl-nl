---
title: Overzicht en betaling afstemming bankoverzicht voor de EU
description: Dit onderwerp biedt een overzicht van de functionaliteit die u gebruiken kunt om af te stemmen betalingsgegevens van de banken in indelingen die worden gebruikt door europese landen.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankAccountTable, CustPaymMode, VendPaymMode
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 267994
ms.assetid: 2bfb8ecc-e850-43cb-9a96-deb11716a391
ms.search.region: Belgium, Norway, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 22d93d7b3618d4f5931c6a7e39d681173734b0b9
ms.lasthandoff: 03/31/2017


---

# <a name="bank-statement-and-payment-reconciliation-overview-for-the-eu"></a>Overzicht en betaling afstemming bankoverzicht voor de EU

Dit onderwerp biedt een overzicht van de functionaliteit die u gebruiken kunt om af te stemmen betalingsgegevens van de banken in indelingen die worden gebruikt door europese landen.

In Microsoft Dynamics 365 voor bewerkingen, kunt u transacties importeren vanuit de banken en vereffen deze transacties tegen bestaande transacties. In europa, kunt u dit doen voor de volgende scenario's:

-   Importeren van bankafschriften
-   Het importeren van betalingen.
-   Retour-bestanden importeren.

## <a name="bank-statements"></a>Bankafschriften
A *bankafschrift* of *overzicht rekening* vindt u een overzicht van financiële transacties die hebben plaatsgevonden in een bepaalde periode op een bankrekening van een bedrijf met een financiële instelling. U kunt een bankafschrift importeren in Dynamics 365 voor bewerkingen. Het is belangrijk voor geïmporteerde transacties vereffenen met bestaande transacties en controleer of de begin- en saldo van de bankrekeningen. De volgende lijst bevat de ondersteunde indelingen van de europese.

-   Geavanceerde afstemming europese bestandsindelingen. Zie voor meer informatie [geavanceerde afstemming bankoverzicht](../cash-bank-management/advanced-bank-reconciliation-overview.md).
-   ISO 20022 camt.053 bericht bestandsindeling bankafschrift
-   Bestandsindeling voor CODA-banktransactie-instructie. Zie voor meer informatie [CODA-bankafschrift](emea-bel-coda-bank-statement-import.md).

## <a name="customer-and-vendor-payments-import-and-return-messages"></a>Klant- als leverancierbetalingen importeren en berichten geretourneerd
Naast een bankafschrift kunnen banken specifieke berichten, met informatie over betalingen van klanten en leveranciers, die kunnen worden geïmporteerd in Dynamics 365 for Operations en afgestemd met klant- en leverancierstransacties bevatten. Wanneer een bedrijf informatie over inkomende betalingen klanttransacties van de bank ontvangt moet, kunnen de Importindelingen worden gebruikt. Voor bedrijven die gebruikmaken van automatische afschrijvingen en kredietoverdracht, kunnen de retourberichten worden ontvangen om de status van betalingen die eerder zijn geëxporteerd. Het verschil tussen de indelingen importeren en retour indelingen is dat als resultaat gegeven gericht zijn meestal om bij te werken al gemaakt journaalregels van leverancierbetalingen (ze kunnen worden gemaakt als directe overdracht debet of credit zijn gestart) in plaats van nieuwe regels maakt. Sommige Importindelingen complexe kunnen ook retourscenario's bevatten. Het volgende voorbeeld ziet hoe deze divisie moet worden geïmplementeerd.

##### <a name="import-formats"></a>Indelingen importeren

-   ISO 20022 camt.054 bank Meldingsbericht
-   [Netten importindeling](emea-nor-nets-import-format.md) -Complex functie voor Noorse betalingsindelingen
-   Klantbetalingen ESR importeren
-   Betalingsindelingen voor Zweden - BankGirot Max en BankGirot OCR indelingen importeren

##### <a name="return-formats"></a>Indelingen retourneren

-   ISO 20022 pain.002 betaling statusrapport
-   (DNK) BetalingsserviceBasis-returformat: retourindeling voor klant Betalingsservice exportindeling
-   [Betalingsindelingen voor Zweden importeren](emea-swe-payment-formats-import.md) -Bankgirot Autogiro retourneert
-   (SWE) BankGirot retourneren: leveranciersbetalingen retourindeling die met de exportindeling Bankgirot overeenkomt

