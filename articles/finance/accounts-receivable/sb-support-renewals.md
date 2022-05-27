---
title: Ondersteuning en verlengingen
description: In dit onderwerp wordt uitgelegd hoe u het ondersteunings- en verlengingsproces voor verkooporders kunt instellen en gebruiken om een factureringsplanning voor verlengingsartikelen te maken.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 7de74f2b12e8e7201663ba78d936131b301b1ff9
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685765"
---
# <a name="support-and-renewals"></a>Ondersteuning en verlengingen 

In dit onderwerp wordt uitgelegd hoe u ondersteunings- of vernieuwingsartikelen kunt invoeren wanneer u verkooporders invoert. Deze artikelen worden gebruikt om het toeslagbedrag voor het oorspronkelijke ondersteuningscontract en/of het verlengingsbedrag te berekenen dat wordt gebruikt wanneer een factureringsplanning wordt gemaakt in Facturering van abonnementen. Stel dat uw bedrijf een server aan een klant verkoopt en u een abonnement voor databack-ups voor het eerste jaar aanbiedt met de optie om dat abonnement elk jaar te verlengen. Het *ondersteuningsartikel* is het abonnement voor het eerste jaar en het *verlengingsartikel* is de verlenging voor elk volgend jaar.

U kunt informatie invoeren voor het ondersteuningscontract, het verlengingscontract of beide. Wanneer u de gegevens van het ondersteuningscontract invoert, wordt alleen het ondersteuningsartikel aan de verkooporder toegevoegd. Wanneer u de gegevens van het verlengingscontract invoert, wordt het vernieuwingsartikel gebruikt om een factureringsplanning te maken.

## <a name="support-and-renewal-setup"></a>Ondersteuning en verlenging instellen

Op de pagina **Ondersteunings- en verlengingsniveaus** kunt u verschillende ondersteuningsniveaus instellen voor ondersteunings- en verlengingsartikelen. De ondersteuning of verlenging kan een percentage van het oorspronkelijke artikelbedrag zijn of een standaardbedrag.

U kunt de standaardondersteuningsniveaus selecteren op de pagina **Terugkerende contractfactureringsparameters**.

Een bedrijf kan bijvoorbeeld de volgende ondersteunings- en verlengingsniveaus bieden.

| Ondersteuningsniveau | Ondersteuningspercentage | Verlengingspercentage |
|---|---|---|
| Onbeperkt | 40% | 30% |
| Goud | 25% | 18% |
| Zilver | 20% | 14% |
| Brons | 15% | 10% |

Volg deze stappen om een ondersteunings- of verlengingsniveau te maken.

1. Selecteer **Nieuw** op de pagina **Ondersteunings- en verlengingsniveaus**.
2. Voer in het veld **Ondersteuningsniveau** een unieke naam in.
3. Voer in het veld **Beschrijving** een beschrijving in.
4. Selecteer de ondersteuningsberekeningsmethode in het veld **Berekeningsmethode ondersteuning**. Als u **Percentage** selecteert, voert u een ondersteuningspercentage in het veld **Ondersteuningspercentage** in.
5. Selecteer de verlengingsberekeningsmethode in het veld **Berekeningsmethode verlenging**. Als u **Percentage** selecteert, voert u een verlengingspercentage in het veld **Verlengingspercentage** in.
6. Selecteer **Opslaan**.

### <a name="fields"></a>Velden

De pagina **Ondersteunings- en verlengingsniveaus** bevat de volgende velden.

| Veld | Description |
|---|---|
| Ondersteuningsniveau | Een unieke id voor het ondersteunings- of verlengingsniveau (bijvoorbeeld **Goud** of **Zilver**). |
| Description | Een beschrijving van het ondersteunings- of verlengingsniveau. |
| Berekeningsmethode ondersteuning | Selecteer de ondersteuningsberekeningsmethode voor het niveau: **Percentage** of **Standaardbedrag**. |
| Ondersteuningspercentage | Als u **Percentage** hebt geselecteerd als ondersteuningsberekeningsmethode, geeft u het percentage op dat wordt gebruikt om de prijs van het ondersteuningsartikel te berekenen. Als u **Standaardbedrag** hebt geselecteerd als berekeningsmethode, wordt het bedrag opgegeven bij het maken van de transactie. |
| Berekeningsmethode verlenging | Selecteer de verlengingsberekeningsmethode voor het niveau: **Percentage** of **Standaardbedrag**. |
| Verlengingspercentage | Als u **Percentage** hebt geselecteerd als verlengingsberekeningsmethode, geeft u het percentage op dat wordt gebruikt om de prijs van het verlengingsartikel te berekenen. Als u **Standaardbedrag** hebt geselecteerd als berekeningsmethode, wordt het bedrag opgegeven bij het maken van de transactie. |

## <a name="support-and-renewal-process"></a>Ondersteunings- en verlengingsproces

Met de ondersteunings- en vernieuwingsfunctionaliteit kunnen verschillende ondersteuningsniveaus worden toegepast op artikelen en kan verlengingsinformatie worden bijgewerkt in Facturering van abonnementen.

Voordat u de ondersteunings- en verlengingsfunctie gebruikt, moeten de volgende taken zijn voltooid.

1. Maak op de pagina **Ondersteunings- en verlengingsniveaus** ten minste één ondersteunings- of verlengingsniveau.
2. Op de pagina **Artikelinstellingen** koppelt u een artikel aan ondersteunings- en verlengingsartikelen. Deze taak is alleen vereist als u standaardwaarden wilt instellen voor ondersteunings- en/of verlengingsartikelen.
3. Geef op de pagina **Terugkerende contractfactureringsparameters** de standaardondersteunings- en verlengingsinstellingen voor nieuwe factureringsplanningen op.

Volg deze stappen om verschillende ondersteuningsniveaus op artikelen toe te passen en verlengingsgegevens bij te werken.

1. Maak op de pagina **Alle verkooporders** een verkooporder.
2. Voeg een artikel toe op het sneltabblad **Verkooporderregels**.
3. Selecteer op het tabblad **Factuur** de optie **Ondersteuning en verlenging \> Ondersteuning en verlenging toevoegen**.
4. Op de pagina **Ondersteunings- en verlengingsproces** wordt de koptekstsectie bijgewerkt met de instellingen van de pagina **Terugkerende contractfactureringsparameters**. Deze waarden zijn van toepassing op alle ondersteunings- en verlengingsartikelen. (Als de factureringsfrequentie bijvoorbeeld is ingesteld op **Jaarlijks**, hebben alle verkoopregels die zijn gemaakt met een verlengingsartikel een jaarlijkse frequentie.) Als u de verkooporder wilt koppelen aan een bestaande factureringsplanning, selecteert u een waarde in het veld **Factureringsplanningsnummer**.
5. Als u de begindatum voor ondersteuning of verlenging wilt wijzigen, stelt u de optie **Begindatum overschrijven** in op **Ja**.
6. Schakel het selectievakje **Ondersteuning** in en voer vervolgens een ondersteuningsartikel in het veld **Ondersteuningsartikel** in om het ondersteuningsartikel toe te voegen of te bewerken. Het artikel wordt toegevoegd aan de verkooporder.
7. Schakel het selectievakje **Verlenging** in en voer vervolgens een verlengingsartikel in het veld **Verlengingsartikel** in om het verlengingsartikel toe te voegen of te bewerken. Wanneer de verkooporder wordt gefactureerd, wordt een factureringsplanning gemaakt dat het artikel bevat.
8. Selecteer **OK**.
9. Selecteer op het tabblad **Genereren** de optie **Factuur**. Wanneer de verkooporder wordt geboekt, wordt de factureringsplanning gemaakt. Een melding met de factuurplanningsgegevens wordt weergegeven in de berichtdetails.
10. Selecteer op de lijstpagina **Alle/Actieve factureringsplanningen** het nummer van de factureringsplanning om de details van de factureringsplanning op de pagina **Factureringsplanningen** te bekijken.
11. Selecteer op het sneltabblad **Factureringsplanningsregels** de optie **Ondersteuning en verlenging** om de details van de gemaakte regels te controleren.

> [!NOTE]
> Als de begindatum voor verlenging voor een factureringsplanningsregel moet worden gewijzigd, kunt u de waarde voor **Begindatum** voor de regel bewerken op de pagina **Factureringsplanningen**. Wanneer u de pagina **Factureringsdetails weergeven** voor de regel opent, wordt het veld **Begindatum facturering** bijgewerkt met de nieuwe datum. De waarde voor **Einddatum facturering** wordt opnieuw berekend op basis van de factureringsfrequentie. De begindatum voor verlenging kan alleen worden bijgewerkt als de eerste factuur voor de verlenging van de factureringsplanning niet is gemaakt en geboekt. Als de eerste factuur is gemaakt en geboekt, kan de begindatum niet meer worden bewerkt.

Het ondersteunings- en verlengingsproces is alleen beschikbaar voor de verkooporder. Wanneer u ondersteunings- en verlengingsartikelen aan een verkooporder toevoegt, kunt u een nieuwe factureringsplanning maken of het verlengingsartikel toevoegen aan een bestaande factureringsplanning.

## <a name="support-and-renewal-audit"></a>Audit ondersteuning en verlenging

Op de pagina **Audit ondersteuning en verlenging** kunt u de details bekijken van de factureringsplanningsregels die zijn gemaakt op basis van het verlengingsartikel op een verkooporder. Deze optie is alleen beschikbaar wanneer het regelartikel voor factureringsplanningen een verlengingsartikel is.

Als u ondersteunings- en vernieuwingsgegevens voor een factureringsplanningsregel wilt bewerken, gaat u als volgt te werk.

1. Selecteer het factureringsplanningsnummer op de pagina **Alle factureringsplanningen**.
2. Selecteer in de sectie **Factureringsplanningsregels** een regel en selecteer **Ondersteuning en verlenging**.
3. Controleer alle gegevens voor het ondersteunings- of verlengingsartikel.
4. Voer de vereiste wijzigingen in het ondersteuningsniveau of het vernieuwingspercentage of -bedrag in en voer vervolgens een waarde in het veld **Reden voor wijziging** in.
5. Selecteer **Verwerken**.

### <a name="fields"></a>Velden

De pagina **Audit ondersteuning en verlenging** bevat de volgende velden.

| Veld | Description |
|-------|-------------|
| Artikelnummer | Het artikelnummer voor de factureringsplanningsregel. |
| Productnaam | De productnaam. |
| Niveau ondersteuningsplan | Bekijk of wijzig het ondersteuningsniveau voor het verlengingsartikel. |
| Verlengingspercentage | Voer het verlengingspercentage in dat wordt gebruikt wanneer de eenheidsprijs wordt berekend voor een verlengingsartikel in een factureringsplanning. |
| Verlengingsbedrag | Voer het verlengingsbedrag in dat wordt gebruikt wanneer de eenheidsprijs wordt berekend voor een verlengingsartikel in een factureringsplanning. |
| Reden voor wijziging | Voer de reden in voor het wijzigen van de ondersteunings- en verlengingsgegevens. U moet een reden invoeren wanneer u de waarde voor **Verlengingspercentage**, **Verlengingsbedrag** of **Niveau ondersteuningsplan** wijzigt. |
| Oorspronkelijk verkoopartikel | Het oorspronkelijke artikelnummer uit de verkooporder. |
| Oorspronkelijk nettobedrag | Het oorspronkelijke nettobedrag voor het artikel. |
| Oorspronkelijk ondersteuningsniveau | Het oorspronkelijke ondersteuningsniveau voor het artikel. |
| Oorspronkelijk verlengingspercentage | Het oorspronkelijke verlengingspercentage voor het artikel. |
| Oorspronkelijk verlengingsbedrag | Het oorspronkelijke verlengingsbedrag voor het artikel. |
| **Raster** | |
| Oorspronkelijk ondersteuningsniveau | Het vorige ondersteuningsniveau. |
| Oorspronkelijk verlengingspercentage | Het vorige verlengingspercentage. |
| Oorspronkelijk verlengingsbedrag | Het vorige verlengingsbedrag. |
| Gewijzigd door | De gebruikersnaam van de gebruiker die de wijziging heeft aangebracht. |
| Wijzigingsdatum en -tijd | De datum waarop de wijziging is opgetreden. |
| Reden | De reden voor de wijziging. |
