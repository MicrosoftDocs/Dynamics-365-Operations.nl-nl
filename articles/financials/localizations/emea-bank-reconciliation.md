---
title: Bankafschriften en betalingsafstemming voor de EU
description: Dit onderwerp bevat een overzicht van de functionaliteit die u kunt gebruiken om betalingsgegevens van banken af te stemmen in indelingen die door Europese landen worden gebruikt.
author: neserovleo
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankAccountTable, CustPaymMode, VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 267994
ms.search.region: Belgium, Norway, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 48cf0926cd8b440459f71e5a72044585cb73e5dc
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="bank-statement-and-payment-reconciliation-for-the-eu"></a>Bankafschriften en betalingsafstemming voor de EU

[!include[banner](../includes/banner.md)]


Dit onderwerp bevat een overzicht van de functionaliteit die u kunt gebruiken om betalingsgegevens van banken af te stemmen in indelingen die door Europese landen worden gebruikt.

In Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition kunt u transacties importeren vanuit banken en deze transacties vereffenen voor bestaande transacties. In Europa kunt u dit doen voor de volgende scenario's:

-   Bankafschriften importeren
-   Betalingen importeren
-   Retourbestanden importeren

## <a name="bank-statements"></a>Bankafschriften
Een *bankafschrift* of *rekeningoverzicht* is een overzicht van financiële transacties die hebben plaatsgevonden in een bepaalde periode op een bankrekening van een bedrijf met een financiële instelling. U kunt een bankafschrift importeren in Finance and Operations. Het is belangrijk om geïmporteerde transacties te vereffenen met bestaande transacties, en om het begin- en eindsaldo van de bankrekeningen te verifiëren. De volgende lijst bevat de ondersteunde Europese indelingen.

-   Europese bestandsindelingen geavanceerde bankafstemming. Zie voor meer informatie [Overzicht van geavanceerde bankafstemming](../cash-bank-management/advanced-bank-reconciliation-overview.md).
-   ISO 20022 camt.053 berichtbestandsindeling bankafschrift
-   Bestandsindeling CODA-bankafschrift Zie [CODA-bankafschrift](emea-bel-coda-bank-statement-import.md) voor meer informatie.

## <a name="customer-and-vendor-payments-import-and-return-messages"></a>Import- en retourberichten van klant- en leveranciersbetalingen
Naast een bankafschrift kunnen banken specifieke berichten verschaffen met informatie over betalingen van klanten en leveranciers, die kunnen worden geïmporteerd in Finance and Operations en afgestemd met klant- en leverancierstransacties. Wanneer een bedrijf informatie over inkomende klantbetalingstransacties van de bank moet ontvangen, kunnen de importindelingen worden gebruikt. Voor bedrijven die gebruikmaken van automatische afschrijving en kredietoverdracht, kunnen de retourberichten worden ontvangen om de status bij te werken van betalingen die eerder zijn geëxporteerd. Het verschil tussen importindelingen en retourindelingen is dat retouren meestal zijn bedoeld om al gemaakte betalingsjournaalregels bij te werken (ze kunnen worden gemaakt wanneer automatische afschrijvingen of kredietoverdrachten zijn geïnitieerd) in plaats van nieuwe regels te maken. Sommige complexe importindelingen kunnen ook retourscenario's omvatten. In het volgende voorbeeld wordt getoond hoe deze verdeling moet worden geïmplementeerd.

### <a name="import-formats"></a>Importindelingen

-   ISO 20022 [camt.054](emea-ISO20022-file-formats.md) bankmeldingsbericht
-   [Nets-importindeling](emea-nor-nets-import-format.md) - Complexe functie voor Noorse betalingsindelingen
-   [ESR](emea-che-esr-customer-payments-import.md)-klantbetalingen importeren
-   Importbetalingsindelingen voor Zweden - BankGirot Max- en BankGirot OCR-indelingen

### <a name="return-formats"></a>Retourindelingen

-   ISO 20022 [pain.002](emea-ISO20022-file-formats.md) betalingsstatusrapport
-   (DNK) BetalingsserviceBasis-returformat: retourindeling voor Betalingsservice-exportindeling voor klanten
-   [Importbetalingsindelingen voor Zweden](emea-swe-payment-formats-import.md) -Bankgirot Autogiro-retouren
-   (SWE) BankGirot-retour: retourindeling leveranciersbetalingen. Dit komt overeen met de Bankgirot-exportindeling



