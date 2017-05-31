---
title: Overzicht van bankafschriften en betalingsafstemming voor de EU
description: Dit onderwerp bevat een overzicht van de functionaliteit die u kunt gebruiken om betalingsgegevens van banken af te stemmen in indelingen die door Europese landen worden gebruikt.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c59bec4493612f7cd62ca3ed9583e400ccda32c6
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="bank-statement-and-payment-reconciliation-overview-for-the-eu"></a>Overzicht van bankafschriften en betalingsafstemming voor de EU

[!include[banner](../includes/banner.md)]


Dit onderwerp bevat een overzicht van de functionaliteit die u kunt gebruiken om betalingsgegevens van banken af te stemmen in indelingen die door Europese landen worden gebruikt.

In Microsoft Dynamics 365 for Operations kunt u transacties importeren vanuit banken en deze transacties vereffenen voor bestaande transacties. In Europa kunt u dit doen voor de volgende scenario's:

-   Bankafschriften importeren
-   Betalingen importeren
-   Retourbestanden importeren

## <a name="bank-statements"></a>Bankafschriften
Een *bankafschrift* of *rekeningoverzicht* is een overzicht van financiële transacties die hebben plaatsgevonden in een bepaalde periode op een bankrekening van een bedrijf met een financiële instelling. U kunt een bankafschrift importeren in Dynamics 365 for Operations. Het is belangrijk om geïmporteerde transacties te vereffenen met bestaande transacties, en om het begin- en eindsaldo van de bankrekeningen te verifiëren. De volgende lijst bevat de ondersteunde Europese indelingen.

-   Europese bestandsindelingen geavanceerde bankafstemming. Zie voor meer informatie [Overzicht van geavanceerde bankafstemming](../cash-bank-management/advanced-bank-reconciliation-overview.md).
-   ISO 20022 camt.053 berichtbestandsindeling bankafschrift
-   Bestandsindeling CODA-bankafschrift Zie [CODA-bankafschrift](emea-bel-coda-bank-statement-import.md) voor meer informatie.

## <a name="customer-and-vendor-payments-import-and-return-messages"></a>Import- en retourberichten van klant- en leveranciersbetalingen
Naast een bankafschrift kunnen banken specifieke berichten verschaffen met informatie over betalingen van klanten en leveranciers, die kunnen worden geïmporteerd in Dynamics 365 for Operations en afgestemd met klant- en leverancierstransacties. Wanneer een bedrijf informatie over inkomende klantbetalingstransacties van de bank moet ontvangen, kunnen de importindelingen worden gebruikt. Voor bedrijven die gebruikmaken van automatische afschrijving en kredietoverdracht, kunnen de retourberichten worden ontvangen om de status bij te werken van betalingen die eerder zijn geëxporteerd. Het verschil tussen importindelingen en retourindelingen is dat retouren meestal zijn bedoeld om al gemaakte betalingsjournaalregels bij te werken (ze kunnen worden gemaakt wanneer automatische afschrijvingen of kredietoverdrachten zijn geïnitieerd) in plaats van nieuwe regels te maken. Sommige complexe importindelingen kunnen ook retourscenario's omvatten. In het volgende voorbeeld wordt getoond hoe deze verdeling moet worden geïmplementeerd.

##### <a name="import-formats"></a>Importindelingen

-   ISO 20022 camt.054 bankmeldingsbericht
-   [Nets-importindeling](emea-nor-nets-import-format.md) - Complexe functie voor Noorse betalingsindelingen
-   Import ESR-klantbetalingen
-   Importbetalingsindelingen voor Zweden - BankGirot Max- en BankGirot OCR-indelingen

##### <a name="return-formats"></a>Retourindelingen

-   ISO 20022 pain.002 betalingsstatusrapport
-   (DNK) BetalingsserviceBasis-returformat: retourindeling voor Betalingsservice-exportindeling voor klanten
-   [Importbetalingsindelingen voor Zweden](emea-swe-payment-formats-import.md) -Bankgirot Autogiro-retouren
-   (SWE) BankGirot-retour: retourindeling leveranciersbetalingen. Dit komt overeen met de Bankgirot-exportindeling



