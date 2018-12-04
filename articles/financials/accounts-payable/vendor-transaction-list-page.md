---
title: Lijstpagina met leveranciertransacties
description: Dit onderwerp bevat informatie over de lijstpagina Leveranciertransacties voor Microsoft Dynamics 365 for Finance and Operations.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: c6502a6fb0ceaed75fd5bb6ec5b2f13db1879eea
ms.openlocfilehash: 45033b8b015d468b7ee0f6c3fba5e6fb6201433e
ms.contentlocale: nl-nl
ms.lasthandoff: 10/12/2018

---

# <a name="vendor-transactions-list-page"></a>Lijstpagina met leveranciertransacties

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Vereffeningen weergeven

De knop **Vereffeningen weergeven** in het actievenster biedt snelle toegang tot de vereffeningshistorie en gedetailleerde informatie over de gehele vereffeningstransactie. U kunt ook extra transacties weergeven die zijn gerelateerd aan de geselecteerde transactie, omdat ze deel uitmaakten van dezelfde vereffening of omdat dit betalingen zijn die zijn gemaakt in hetzelfde betalingsjournaal.

1. Selecteer **Leveranciers \> Alle leveranciers**.
2. Selecteer een leverancier die transacties heeft en selecteer vervolgens in het actievenster op het tabblad **Leverancier** de optie **Transacties**.
3. Selecteer een transactie om te onderzoeken en selecteer vervolgens in het actievenster **Vereffeningen weergeven**.

    Het dialoogvenster **Vereffeningen weergeven** weergegeven met de geselecteerde transactie en alle documenten die ervoor zijn vereffend. Dit dialoogvenster lijkt op de weergave van de vereffeningshistorie, maar het bevat alle gerelateerde documenten.

4. In het dialoogvenster kunt u verschillende taken uitvoeren. Selecteer een of meer boekstukken en selecteer een van de volgende knoppen:

    - **Gerelateerde weergeven**: alle betalingsjournaaltransacties weergeven die zijn gemaakt in het betalingsjournaal dat is gerelateerd aan het geselecteerde document. Bovendien worden alle vereffeningen weergegeven die zijn gerelateerd aan deze betalingen. Terwijl u gerelateerde betalingen weergeeft, wordt het label van deze knop gewijzigd in **Vereffeningen weergeven**. Selecteer **Vereffeningen weergeven** om alleen de transacties te tonen die werden weergegeven toen u voor het eerst het dialoogvenster **Vereffeningen weergeven** opende.
    - **Historie weergeven**: de vereffeningshistorie voor de boekstukken weergeven. Selecteer **Sluiten** om het dialoogvenster te sluiten.
    - **Boekhouding weergeven**: alle boekstukken weergeven die zijn gerelateerd aan de geselecteerde documenten. Selecteer **Sluiten** om het dialoogvenster te sluiten.
    - **Exporteren** : de geselecteerde boekstukken naar Microsoft Excel exporteren.
    - **Transacties vereffenen**: deze knop wordt alleen weergegeven als het oorspronkelijk geselecteerde document niet volledig is vereffend. Wanneer u deze knop selecteert, verschijnt het dialoogvenster **Transacties vereffenen**. Hierin kunt u transacties voor vereffening selecteren.
    - **Vereffening ongedaan maken**: deze knop wordt alleen weergegeven als het oorspronkelijk geselecteerde document volledig is vereffend. Wanneer u deze knop selecteert, verschijnt het dialoogvenster **Vereffening ongedaan maken**. Hierin kunt u de vereffeningen ongedaan maken die zijn uitgevoerd voor dat document.

## <a name="global-transactions"></a>Algemene transacties

De knop **Algemene transacties** wordt ook weergegeven op de lijstpagina **Leverancierstransacties**. Met deze knop kunt u alle transacties voor een leverancier voor alle rechtspersonen bekijken. Op de pagina **Leveranciertransacties** worden alleen transacties weergegeven voor de rechtspersonen waartoe de gebruiker toegang heeft, op basis van zijn of haar beveiligingsinstellingen.

Op de lijstpagina worden alle transacties weergegeven voor leveranciers met dezelfde partij-id als de leverancier waarmee u bent begonnen. Heeft leverancier US-001 in de ene rechtspersoon bijvoorbeeld dezelfde partij-id als leverancier DE-001 in een andere rechtspersoon, dan worden alle transacties voor beide leveranciers-id's weergegeven.

Welke menu's op de lijstpagina **Leveranciertransacties** worden weergegeven, is afhankelijk van de rechtspersoon voor de transactie. Als een functie alleen beschikbaar is voor Zwitserse rechtspersonen, worden de menuopties voor die functie bijvoorbeeld alleen weergegeven als een Zwitserse transactie wordt geselecteerd.

Voer deze stappen uit om toegang tot de functie te krijgen.

1. Selecteer **Leveranciers** \> **Alle leveranciers**.
2. Selecteer een leverancier en selecteer vervolgens in het actievenster op het tabblad **Leverancier** in de groep **Transacties** de optie **Algemene transacties**.

## <a name="more-transaction-filters"></a>Meer transactiefilters

Het filter voor het weergeven van openstaande transacties is vervangen door een nieuw filter waarmee u meer combinaties van transacties kunt weergeven. De volgende opties zijn beschikbaar in het veld **Weergeven**:

- **Alle**: alle transacties voor de geselecteerde leveranciers weergeven (openstaand en afgesloten).
- **Afgesloten**: alleen transacties weergeven die volledig zijn vereffend en afgesloten.
- **Openstaand**: alleen transacties weergeven die niet volledig zijn vereffend.
- **Open inclusief afgesloten op of na datum**: alleen transacties weergeven die nog niet volledig zijn vereffend op of na een datum die u opgeeft. Wanneer u deze optie selecteert, kunt u de datum wijzigen die wordt weergegeven naast het filter. Transacties met een waarde voor **laatste vereffeningsdatum** op of na de datum die u opgeeft, worden weergegeven in de lijst, zelfs als deze transacties volledig zijn vereffend op de huidige datum. Het saldo staat echter voor de saldi op de huidige datum, niet op de geselecteerde datum.

Selecteer het selectievakje **Herwaarderingen van valuta verbergen** om transacties van valuta-omzetting te verbergen.

## <a name="modify-due-dates-and-discount-dates"></a>Verval- en kortingsdatums wijzigen

U kunt verval- en kortingsdatums bijwerken voor openstaande klanttransacties. In release 8.1 kunt u nu vervaldatums toevoegen aan de lijstpagina **Leverancierstransacties**. Door te klikken op de vervaldatum op de lijstpagina **Leveranciertransacties**, kunt u ook vervaldatums, kortingsdatums, betalingsvoorwaarden en voorwaarden voor contantkorting wijzigen in het dialoogvenster **Vervaldatum en datums contantkorting bijwerken**.

### <a name="activate-the-feature"></a>De functie activeren

Voer deze stappen uit om vervaldatums toe te voegen aan de lijstpagina **Leveranciertransacties** en betalingsinstellingen voor een transactie te wijzigen in het dialoogvenster **Vervaldatum en datums contantkorting bijwerken**.

1. Selecteer **Leveranciers \> Instellen \> Parameters van Leveranciers**.
2. Stel op het tabblad **Vereffeningen** de optie **Vervaldatum weergeven en bewerken toestaan** in op **Ja**.
3. Aan leveranciertransacties zijn nieuwe functies toegevoegd zodat u deze functie kunt inschakelen. Deze velden worden ingevuld wanneer een nieuwe transactie wordt voltooid. Ze worden ook ingevuld wanneer u het dialoogvenster **Vervaldatum en datums contantkorting bijwerken** opent. Wanneer u de optie **Vervaldatum weergeven en bewerken toestaan** op **Ja** instelt, wordt het dialoogvenster **Betaalgegevens bijwerken** geopend.  Als u bestaande transacties onmiddellijk wilt bijwerken, selecteert u **Alle bestaande transacties bijwerken**. Als u alleen de velden voor nieuwe transacties wilt invullen, selecteert u **Doorgaan zonder bijwerken**.

De vervaldatum wordt nu toegevoegd aan de lijstpagina **Leverancierstransacties**, zodat u gemakkelijk de vervaldatum en datums voor contantkorting voor transacties kunt wijzigen.

### <a name="modify-the-payment-settings"></a>De betaalinstellingen wijzigen

Op de lijstpagina **Leveranciertransacties** worden alle transacties voor een leverancier weergegeven. Wanneer u de vervaldatum voor een transactie selecteert, verschijnt een dialoogvenster. Dit dialoogvenster bevat de basisdatum voor berekeningen van de vervaldatum en korting, de vervaldatum, de betalingsvoorwaarden, de voorwaarden voor contantkortingen en de datums van contantkortingen.

Elk veld heeft een ander effect op de transactie als u dit bewerkt:

- **De basisdatum bewerken:** de vervaldatum en kortingsdatum worden gewijzigd alsof de basisdatum de documentdatum is.
- **De vervaldatum bewerken:** alleen de vervaldatum wordt gewijzigd
- **De kortingsdatums bewerken:** alleen de kortingsdatums worden gewijzigd.
- **De betalingsvoorwaarden bewerken:** de vervaldatum wordt gewijzigd op basis van de basisdatum en de betalingsvoorwaarden.
- **De voorwaarden voor contantkorting bewerken:** de contantkortingen worden gewijzigd, op basis van de basisdatum en de voorwaarden voor contantkorting.

Wanneer u klaar bent met het bewerken van de betalingsinstellingen, selecteert u **Sluiten** om uw wijzigingen op te slaan.

