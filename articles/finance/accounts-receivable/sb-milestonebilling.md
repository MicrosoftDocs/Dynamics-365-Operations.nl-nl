---
title: Mijlpaalsjablonen
description: In dit artikel wordt uitgelegd hoe u de functionaliteit voor facturering van mijlpalen instelt in Facturering van abonnementen.
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
ms.openlocfilehash: d3c2cf751e4998c73bc3816e5b81e8d5963c8e53
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856765"
---
# <a name="milestone-billing"></a>Facturering van mijlpalen

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u sjablonen definieert voor de functionaliteit voor facturering van mijlpalen instelt in Facturering van abonnementen. Voor elke regel in de mijlpaalsjabloon kunt u het toewijzingspercentage of -bedrag definiëren. Vervolgens kunt u de mijlpaalsjabloon toewijzen aan factureringsplanningsartikelen die gebruikmaken van de functie voor facturering van mijlpalen.

## <a name="add-a-template"></a>Een sjabloon toevoegen

Als u een mijlpaalsjabloon wilt toevoegen, volgt u deze stappen.

1. Ga naar **Facturering van abonnementen \> Terugkerende contractfacturering \> Instellingen \> Mijlpaalsjablonen**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Mijlpaalsjabloon** een unieke id in voor de nieuwe sjabloon.
4. Voer in het veld **Beschrijving** een beschrijving in.
5. Selecteer een toewijzingsmethode in het veld **Toewijzingsmethode**.
6. Optioneel: geef in het veld **Totaalbedrag** het totale bedrag voor de sjabloon op.
7. U kunt een regel toevoegen door **Toevoegen** te selecteren. Selecteer vervolgens in het veld **Artikelnummer** het artikelnummer voor de nieuwe regel.
8. Voer een van de volgende stappen uit, afhankelijk van de waarde die u hebt geselecteerd in het veld **Toewijzingstype**:

    - Als u **Percentage** hebt geselecteerd als toewijzingsmethode, geeft u in het veld **Percentage** het toewijzingspercentage voor elke regel op. Als u percentages opgeeft, moet de som van de percentages die worden weergegeven in het veld **Totale percentage** gelijk zijn aan **100**.
    - Als u **Variabel bedrag** hebt geselecteerd als toewijzingsmethode, geeft u in het veld **Bedrag** het bedrag voor elke regel op.
    - Als u **Gelijk bedrag** hebt geselecteerd als toewijzingsmethode, hoeft u geen bedrag op te geven. Elke regel wordt bijgewerkt met het juiste percentage en bedrag op basis van het aantal artikelen dat aan de sjabloon is toegevoegd.

9. Selecteer **Opslaan**.

## <a name="delete-a-template"></a>Een sjabloon verwijderen

Als u een mijlpaalsjabloon wilt verwijderen, volgt u deze stappen.

1. Selecteer een of meer regels om te verwijderen en selecteer vervolgens **Verwijderen**.
2. Selecteer **Ja** als u wordt gevraagd de actie te bevestigen.

## <a name="milestone-template-fields"></a>Velden van mijlpaalsjabloon

De pagina **Mijlpaalsjabloon** bevat de volgende velden.

| Veld | Description |
|-------|-------------| 
| Mijlpaalsjabloon | De unieke id van de mijlpaalsjabloon. |
| Description | De beschrijving van de mijlpaalsjabloon. |
| Toewijzingsmethode | <p>Selecteer de toewijzingssmethode:</p><ul><li>**Voltooiingspercentage:** voor elke regel wordt een cumulatieve voltooiingswaarde gebruikt.</li><li>**Percentage**: er kan een percentagebedrag worden opgegeven voor de toewijzing. De som van alle percentages moet gelijk zijn aan 100.</li><li>**Variabel bedrag**: er kan een bedrag worden opgegeven voor de toewijzing. Het toewijzingsbedrag wordt opgegeven op transactieniveau.</li><li>**Gelijk bedrag**: de toewijzingspercentages worden automatisch berekend en gelijk verdeeld over de artikelen in de sjabloon.</li></ul> |
| Totaalbedrag | Geef het mijlpaalbedrag voor de sjabloon op. |
| **Regels** | |
| Artikelnummer | Selecteer het artikelnummer voor de mijlpaalsjabloon. |
| Productnaam | De naam van het artikel. |
| Percentage | <p>Voer het toewijzingspercentage voor de regel in:</p><ul><li>Als het veld **Toewijzingsmethode** is ingesteld op **Percentage**, geeft u het percentage voor de regel op.</li><li>Als het veld **Toewijzingsmethode** is ingesteld op **Gelijk bedrag**, wordt het percentage automatisch opgesplitst in gelijke percentages, gebaseerd op het aantal artikelen in de sjabloon.</li></ul><p>De som van alle percentages moet gelijk zijn aan 100.</p><p>Als er een waarde **Totaalbedrag** is opgegeven in de koptekst en u de waarde voor **Percentage** voor de regel wijzigt, wordt de waarde voor **Bedrag** bijgewerkt. Omgekeerd wordt de waarde voor **Percentage** bijgewerkt als de waarde voor **Bedrag** wordt gewijzigd.</p> |
| Bedrag | <p>Het toewijzingsbedrag voor de regel:</p><ul><li>Als het veld **Toewijzingsmethode** is ingesteld op **Variabel bedrag**, geeft u het bedrag voor de regel op.</li><li>Als het veld **Toewijzingsmethode** is ingesteld op **Gelijk bedrag**, wordt het bedrag automatisch opgesplitst in gelijke bedragen op basis van het aantal artikelen in de sjabloon en de waarde voor **Totaalbedrag** die in de koptekst is opgegeven.</li></ul><p>De som van alle bedragen moet gelijk zijn aan de waarde voor **Totaalbedrag** die in de koptekst is opgegeven.</p><p>Als er een waarde **Totaalbedrag** is opgegeven in de koptekst en u de waarde voor **Bedrag** voor de regel wijzigt, wordt de waarde voor **Percentage** bijgewerkt. Omgekeerd wordt de waarde voor **Bedrag** bijgewerkt als de waarde voor **Percentage** wordt gewijzigd.</p> |
| **Totalen** | |
| Totaal percentage | De som van de percentages. De som van alle percentages moet gelijk zijn aan 100. |
| Totaalbedrag | De som van waarden voor **Bedrag** voor alle regels. Deze som moet gelijk zijn aan de waarde voor **Totaalbedrag** die in de koptekst is opgegeven. |
| Restbedrag | Het resterende bedrag. De waarde wordt berekend als de waarde voor **Totaalbedrag** van de koptekst min de som van de waarden voor **Bedrag** op alle regels.|

## <a name="milestone-allocation"></a>Mijlpaaltoewijzing

Voordat u mijlpaalfunctionaliteit gaat gebruiken, moet u deze taken uitvoeren.

1. Een of meer mijlpaalsjablonen toevoegen.
2. Een Factureringsplanningsgroep maken. **Mijlpaal** opgeven als artikeltype en een sjabloon selecteren.
3. Selecteer op de pagina **Artikelinstellingen** (**Facturering \> Terugkerende contractfacturering \> Instellingen \> Artikelen**) een artikelrelatie en een mijlpaalsjabloon voor de artikelinstelling.

Nadat u de mijlpaalsjablonen, factureringsplanningsgroep en artikelen hebt gemaakt, kunt u een factureringsplanning opstellen die gebruikmaakt van de mijlpaalfunctie.

Volg deze stappen om een factureringsplanning in te stellen die gebruikmaakt van mijlpalen.

1. Selecteer **Nieuw** in de lijst **Alle/Actieve factureringsplanningen** op de pagina **Factureringsplanningen**.
2. Maak op de pagina **Alle factureringsplanningen** een nieuwe factureringsplanning en geef een klantrekening en een begindatum op.
3. Selecteer **Regel toevoegen** in de sectie **Factureringsplanningsregels**. Voeg vervolgens een artikelnummer toe en stel het veld **Artikeltype** in op **Mijlpaal**.

    Als er een standaardmijlpaalsjabloon is ingesteld voor het artikel, worden de mijlpaalgebeurtenissen automatisch toegevoegd aan de factureringsplanningsregels. Einddatums zijn leeg voor mijlpaalregels.

    Selecteer **Mijlpaaltoewijzing** als er geen mijlpaalsjabloon is ingesteld voor het artikel. Selecteer vervolgens op de pagina **Mijlpaaltoewijzing** een mijlpaalsjabloon en voer de gewenste updates uit. Selecteer vervolgens **Sluiten** om terug te keren naar de factureringsplanning en voltooi het maken van de factureringsplanning.

4. Als u facturen wilt maken voor de factureringsplanning, moet u de einddatum voor elke mijlpaalgebeurtenis bijwerken. Voor een enkele factureringsplanning kunt u de einddatum voor de mijlpaalgebeurtenis bijwerken op de factureringsplanningsregels. Als u meerdere factureringsplanningen wilt bijwerken, selecteert u **Voltooiingsdatumproces bijwerken**.
5. Nadat de einddatum is bijgewerkt, kunt u de factuur maken. Selecteer voor een enkele factureringsplanning de optie **Factuur genereren** op de pagina **Alle factureringsplanningen**. Als u facturen wilt maken voor meerdere factureringsplanningen, selecteert u **Factuur genereren** of **Factuurbatchverwerking genereren** onder **Periodieke taken**.

## <a name="edit-milestone-allocation-on-a-billing-schedule-line"></a>Mijlpaaltoewijzing op een factureringsplanningsregel bewerken

Volg deze stappen om een mijlpaaltoewijzing op een factureringsplanningsregel te bewerken.

1. Selecteer op de pagina **Factureringsplanningen** > **Alle of actieve factureringsplanningen** in het veld **Planningsnummer** het nummer van de factureringsplanning die u wilt bewerken.
2. Voer in de sectie **Factureringsplanningsregels** een artikel in, geef **Mijlpaal** op als artikel en selecteer **Mijlpaaltoewijzing**.
3. Selecteer een mijlpaalsjabloon in het veld **Mijlpaalsjabloon**.
4. Selecteer **Verwerken**. De mijlpaalsjabloonregels worden automatisch toegevoegd aan de factureringsplanningsregels.

## <a name="milestone-allocation-fields"></a>Velden voor mijlpaaltoewijzing

De pagina **Mijlpaaltoewijzing** bevat de volgende velden.

| Veld | Description |
|-------|-------------|
| Bovenliggend artikel | Het artikelnummer van het bovenliggende artikel. |
| Uitgebreide prijs | <p>De totaalprijs van het artikel. De waarde komt overeen met de waarde voor **Nettobedrag** van de factureringsplanningsregel.</p></p>Voor een bovenliggend mijlpaalartikel is de standaardwaarde de waarde voor **Totaalbedrag** die is opgegeven voor de mijlpaalsjabloon. Als het totaalbedrag 0 (nul) bedraagt, is de standaardwaarde gelijk aan de waarde voor **Nettobedrag** van de factureringsplanningsregel.</p> |
| Mijlpaalsjabloon | De mijlpaalsjabloon-id van het regelartikel. |
| Beschrijving van sjabloon | De beschrijving van de mijlpaalsjabloon. |
| Toewijzingsmethode | De toewijzingsmethode die wordt gebruikt voor de mijlpaalsjabloon. |
| **Regels** | De standaardwaarden voor alle regels zijn gebaseerd op de geselecteerde mijlpaalsjabloon. U kunt deze desgewenst wijzigen. |
| Artikelnummer | Het artikelnummer voor de mijlpaaltoewijzingssjabloon. |
| Productnaam | De productnaam. |
| Percentage | <p>Het toewijzingspercentage voor de regel. De som van alle percentages moet gelijk zijn aan 100.</p><p>Als u de waarde voor **Percentage** voor de regel wijzigt, wordt de waarde voor **Nettobedrag** bijgewerkt. Omgekeerd wordt de waarde voor **Percentage** bijgewerkt als de waarde voor **Nettobedrag** wordt gewijzigd.</p> |
| Nettobedrag | <p>Het toewijzingsbedrag voor de regel. De som van de nettobedragen voor alle regels moet gelijk zijn aan de waarde voor **Totaalprijs** die in de koptekst is opgegeven.</p><p>Als u de waarde voor **Nettobedrag** voor de regel wijzigt, wordt de waarde voor **Percentage** bijgewerkt. Omgekeerd wordt de waarde voor **Nettobedrag** bijgewerkt als de waarde voor **Percentage** wordt gewijzigd.</p> |
| **Totalen** | |
| Totaal percentage | De som van waarden voor **Percentage** voor alle regels. Dit totaal moet gelijk zijn aan 100. |
| Totaalbedrag | De som van waarden voor **Nettobedrag** voor alle regels. Deze som moet gelijk zijn aan de waarde voor **Totaalprijs** die in de koptekst is opgegeven. |
| Restbedrag | Het resterende bedrag. De waarde wordt berekend als de waarde voor **Totaalprijs** van de koptekst min de som van de waarden voor **Nettobedrag** op alle regels. Het eindbedrag moet 0 (nul) zijn. |
