---
title: Lijstpagina met klanttransacties
description: Dit artikel bevat informatie over de pagina met klantentransactielijsten voor Microsoft Dynamics 365 Finance.
author: abruer
ms.date: 08/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 2ca7aaa0ccea8f4936ae4a177ef9b9eba2282ae6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864449"
---
# <a name="customer-transactions-list-page"></a>Lijstpagina met klanttransacties

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Vereffeningen weergeven

De knop **Vereffeningen weergeven** in het actievenster biedt snelle toegang tot de vereffeningshistorie en gedetailleerde informatie over de gehele vereffeningstransactie. U kunt ook extra transacties weergeven die zijn gerelateerd aan de geselecteerde transactie, omdat ze deel uitmaakten van dezelfde vereffening of omdat dit betalingen zijn die zijn gemaakt in hetzelfde betalingsjournaal.

1. Selecteer **Klanten \> Alle klanten**.
2. Selecteer een klant die transacties heeft en selecteer vervolgens in het actievenster op het tabblad **Klant** de optie **Transacties**.
3. Selecteer een transactie om te onderzoeken en selecteer vervolgens in het actievenster **Vereffeningen weergeven**.

    Het dialoogvenster **Vereffeningen weergeven** weergegeven met de geselecteerde transactie en alle documenten die ervoor zijn vereffend. Dit dialoogvenster lijkt op de weergave van de vereffeningshistorie, maar het bevat alle gerelateerde documenten.

4. In het dialoogvenster kunt u verschillende taken uitvoeren. Selecteer een of meer boekstukken en selecteer een van de volgende knoppen:

    - **Gerelateerde weergeven**: de journaaltransacties voor betaling en algemene journaaltransacties weergeven voor de klanten die zijn gemaakt in de journalen waarin de documenten weergegeven in de lijst zijn gemaakt. Bijvoorbeeld: als een betaling wordt weergegeven, worden alle betalingen in het betalingsjournaal waarin deze is gemaakt weergegeven. Als een factuur of betaling wordt weergegeven en deze is gemaakt in een algemeen journaal, worden alle documenten in het algemene journaal waarin deze is gemaakt weergegeven. Alle vereffeningen die zijn gerelateerd aan de lijst van documenten worden ook weergegeven. Terwijl u gerelateerde betalingen weergeeft, wordt het label van deze knop gewijzigd in **Vereffeningen weergeven**. Selecteer **Vereffeningen weergeven** om alleen de transacties te tonen die werden weergegeven toen u voor het eerst het dialoogvenster **Vereffeningen weergeven** opende.
    - **Historie weergeven**: de vereffeningshistorie voor de boekstukken weergeven. Selecteer **Sluiten** om het dialoogvenster te sluiten.
    - **Boekhouding weergeven**: alle boekstukken weergeven die zijn gerelateerd aan de geselecteerde documenten. Selecteer **Sluiten** om het dialoogvenster te sluiten.
    - **Exporteren**: de geselecteerde boekstukken naar Microsoft Excel exporteren.
    - **Transacties vereffenen**: deze knop wordt alleen weergegeven als het oorspronkelijk geselecteerde document niet volledig is vereffend. Wanneer u deze knop selecteert, verschijnt het dialoogvenster **Transacties vereffenen**. Hierin kunt u transacties voor vereffening selecteren.
    - **Vereffening ongedaan maken**: deze knop wordt alleen weergegeven als het oorspronkelijk geselecteerde document volledig is vereffend. Wanneer u deze knop selecteert, verschijnt het dialoogvenster **Vereffening ongedaan maken**. Hierin kunt u de vereffeningen ongedaan maken die zijn uitgevoerd voor dat document.

## <a name="global-transactions"></a>Algemene transacties

De knop **Algemene transacties** wordt ook weergegeven op de lijstpagina **Klanttransacties**. Met deze knop kunt u alle transacties voor een klant voor alle rechtspersonen bekijken. Op de pagina **Klanttransacties** worden alleen transacties weergegeven voor de rechtspersonen waartoe de gebruiker toegang heeft, op basis van zijn/haar beveiligingsinstellingen.

Op de lijstpagina worden alle transacties weergegeven voor klanten met dezelfde partij-id als de klant waarmee u bent begonnen. Heeft klant US-001 in de ene rechtspersoon bijvoorbeeld dezelfde partij-id als klant DE-001 in een andere rechtspersoon, dan worden alle transacties voor beide klant-id's weergegeven.

Welke menu's op de lijstpagina **Klanttransacties** worden weergegeven, is afhankelijk van de rechtspersoon voor de transactie. Als een functie alleen beschikbaar is voor Zwitserse rechtspersonen, worden de menuopties voor die functie bijvoorbeeld alleen weergegeven als een Zwitserse transactie wordt geselecteerd.

Voer deze stappen uit om toegang tot de functie te krijgen.

1. Selecteer **Klanten \> Alle klanten**.
2. Selecteer een klant en selecteer vervolgens in het actievenster op het tabblad **Klant** in de groep **Transacties** de optie **Algemene transacties**.

## <a name="more-transaction-filters"></a>Meer transactiefilters 

Het filter voor het weergeven van openstaande transacties is vervangen door een nieuw filter waarmee u meer combinaties van transacties kunt weergeven. De volgende opties zijn beschikbaar in het veld **Weergeven**:

- **Alle**: alle transacties voor de geselecteerde klanten weergeven (openstaand en afgesloten).
- **Afgesloten**: alleen transacties weergeven die volledig zijn vereffend en afgesloten.
- **Openstaand**: alleen transacties weergeven die niet volledig zijn vereffend.
- **Open inclusief afgesloten op of na datum**: alleen transacties weergeven die nog niet volledig zijn vereffend op of na een datum die u opgeeft. Wanneer u deze optie selecteert, kunt u de datum wijzigen die wordt weergegeven naast het filter. Transacties met een waarde voor **laatste vereffeningsdatum** op of na de datum die u opgeeft, worden weergegeven in de lijst, zelfs als deze transacties volledig zijn vereffend op de huidige datum. Het saldo staat echter voor de saldi op de huidige datum, niet op de geselecteerde datum.

Selecteer het selectievakje **Herwaarderingen van valuta verbergen** om transacties van valuta-omzetting te verbergen.

## <a name="modify-due-dates-and-discount-dates"></a>Verval- en kortingsdatums wijzigen

U kunt verval- en kortingsdatums bijwerken voor openstaande klanttransacties. In release 8.1 kunt u nu vervaldatums toevoegen aan de lijstpagina **Klanttransacties**. Door te klikken op de vervaldatum op de lijstpagina **Klanttransacties**, kunt u ook vervaldatums, kortingsdatums, betalingsvoorwaarden en voorwaarden voor contantkorting wijzigen in het dialoogvenster **Vervaldatum en datums contantkorting bijwerken**.

### <a name="activate-the-feature"></a>De functie activeren

Voer deze stappen uit om vervaldatums toe te voegen aan de lijstpagina **Klanttransacties** en betalingsinstellingen voor een transactie te wijzigen in het dialoogvenster **Vervaldatum en datums contantkorting bijwerken**.

1. Selecteer **Klanten \> Instellen \> Parameters van module Klanten**.
2. Stel op het tabblad **Vereffeningen** de optie **Vervaldatum weergeven en bewerken toestaan** in op **Ja**.
3. Aan klanttransacties zijn nieuwe functies toegevoegd zodat u deze functie kunt inschakelen. Deze velden worden ingevuld wanneer een nieuwe transactie wordt voltooid. Ze worden ook ingevuld wanneer u het dialoogvenster **Vervaldatum en datums contantkorting bijwerken** opent. Wanneer u de optie **Vervaldatum weergeven en bewerken toestaan** op **Ja** instelt, wordt het dialoogvenster **Betaalgegevens bijwerken** geopend.  Als u bestaande transacties onmiddellijk wilt bijwerken, selecteert u **Alle bestaande transacties bijwerken**. Als u alleen de velden voor nieuwe transacties wilt invullen, selecteert u **Doorgaan zonder bijwerken**.

De vervaldatum wordt nu toegevoegd aan de lijstpagina **Klanttransacties**, zodat u gemakkelijk de vervaldatum en datums voor contantkorting voor transacties kunt wijzigen.

### <a name="modify-the-payment-settings"></a>De betaalinstellingen wijzigen

Op de lijstpagina **Klanttransacties** worden alle transacties voor een klant weergegeven. Wanneer u de vervaldatum voor een transactie selecteert, wordt het dialoogvenster **Vervaldatum en datums contantkorting bijwerken** weergegeven. Dit dialoogvenster bevat de basisdatum voor berekeningen van de vervaldatum en korting, de vervaldatum, de betalingsvoorwaarden, de voorwaarden voor contantkortingen en de datums van contantkortingen.

Elk veld heeft een ander effect op de transactie als u dit bewerkt:

- **De basisdatum bewerken:** de vervaldatum en kortingsdatum worden gewijzigd alsof de basisdatum de documentdatum is.
- **De vervaldatum bewerken:** alleen de vervaldatum wordt gewijzigd.
- **De kortingsdatums bewerken:** alleen de kortingsdatums worden gewijzigd.
- **De betalingsvoorwaarden bewerken:** de vervaldatum wordt gewijzigd op basis van de basisdatum en de betalingsvoorwaarden.
- **De voorwaarden voor contantkorting bewerken:** de contantkortingen worden gewijzigd, op basis van de basisdatum en de voorwaarden voor contantkorting.

Wanneer u klaar bent met het bewerken van de betalingsinstellingen, selecteert u **Sluiten** om uw wijzigingen op te slaan.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
