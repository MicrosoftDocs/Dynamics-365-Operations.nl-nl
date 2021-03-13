---
title: Rapport opslag van voorraadwaarden
description: In dit onderwerp wordt uitgelegd hoe u een rapport Opslag van voorraadwaarden kunt uitvoeren en de uitvoer in digitale vorm beschikbaar kunt maken, als een interactieve pagina in Microsoft Dynamics 365 Supply Chain Management of als een geëxporteerd document in verschillende indelingen.
author: AndersGirke
manager: tfehr
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-17
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 0f54c02fc828d60f4ddb28be932bbf8eb137ee92
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5008152"
---
# <a name="inventory-value-storage-report"></a>Rapport opslag van voorraadwaarden

In dit onderwerp wordt uitgelegd hoe u een rapport **Opslag van voorraadwaarden** kunt uitvoeren en de uitvoer in digitale vorm beschikbaar kunt maken, als een interactieve pagina in Microsoft Dynamics 365 Supply Chain Management of als een geëxporteerd document in verschillende indelingen.

Bij het bekijken van het rapport in uw browser worden kolommen en samengevoegde balansen dynamisch aangepast, afhankelijk van de indeling die u hebt geconfigureerd. U kunt de resultaten sorteren, filteren, details van de gegevens bekijken en nog veel meer.

Rapportresultaten worden opgeslagen in de gegevensentiteit **Voorraadwaarde**. Daarom kunt u de resultaten filteren en exporteren naar een indeling zoals door komma's gescheiden waarden (CSV) of de Microsoft Excel-indeling.

Het rapport **Opslag van voorraadwaarden** is handig wanneer de output veel regels bevat. U hebt bijvoorbeeld 50.000 artikelen en er zijn 300 winkels gemaakt als magazijnen. Als u in dit geval voorraadeindsaldi opvraagt per artikel, locatie en magazijn, bevat de uitvoer veel regels.

> [!NOTE]
> In het rapport worden geen subtotalen opgenomen die zijn gedefinieerd in de rapportindeling. Ook bevat deze optie geen grootboeksaldi, zelfs wanneer deze zijn gedefinieerd in de rapportindeling. U moet de afstemming in het grootboek uitvoeren met behulp van proefbalansen.

## <a name="turn-on-the-inventory-value-storage-feature"></a>De functie voor opslag van voorraadwaarden inschakelen

Voordat u een rapport **Opslag van voorraadwaarden** kunt genereren, moet u de functie in uw systeem inschakelen. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en desgewenst in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module** - Kostenbeheer
- **Functienaam**: opslag van voorraadwaarden

## <a name="generate-an-inventory-value-storage-report"></a>Een rapport Opslag van voorraadwaarden genereren

Volg deze stappen om een rapport **Opslag van voorraadwaarden** te genereren en op te slaan.

1. Ga naar **Kostenbeheer \> Query's en rapporten \> Rapport Opslag van voorraadwaarden**.
1. Selecteer **Nieuw**.
1. In het dialoogvenster **Voorraadwaarde** dat wordt weergegeven, stelt u de volgende waarden in om aan te geven welke records in uw rapport moeten worden opgenomen:

    - Voer op het sneltabblad **Parameters** een unieke naam voor het rapport in en gebruik de velden in de sectie **Datuminterval** om te definiëren welke records in het rapport worden opgenomen. Als u het datuminterval wilt definiëren, kunt u een vooraf ingesteld bereik (ten opzichte van de rapportaanmaakdatum) selecteren in het veld **Datumintervalcode** of specifieke datums selecteren in de velden **Begindatum** en **Einddatum**.
    - Stel op het sneltabblad **Op te nemen records** filters en beperkingen in om op te geven welke gegevens u in het rapport wilt opnemen.
    - Geef op het sneltabblad **Uitvoeren op de achtergrond** op hoe, wanneer en hoe vaak het rapport wordt gegenereerd.

    > [!NOTE]
    > Dit rapport wordt altijd uitgevoerd als onderdeel van een batchtaak.

1. Selecteer **OK** om de instellingen toe te passen en het dialoogvenster te sluiten.

Nadat de batchtaak is voltooid, wordt het rapport vermeld op de pagina **Rapport opslag van voorraadwaarden**. U moet de pagina mogelijk vernieuwen om het rapport te bekijken.

## <a name="explore-an-inventory-value-storage-report"></a>Een rapport Opslag van voorraadwaarden bekijken

Nadat u een rapport hebt gegenereerd, kunt u het op elk gewenst moment weergeven en verkennen met de volgende stappen.

1. Ga naar **Kostenbeheer \> Query's en rapporten \> Rapport Opslag van voorraadwaarden**.
1. Selecteer een rapport in de lijst.
1. Selecteer **Details weergeven** om de inhoud van het rapport weer te geven.
1. Bekijk het rapport door een van de volgende stappen uit te voeren:

    - Net als voor de meeste standaardpagina's in Supply Chain Management, kunt u vrijwel elke kolomkop selecteren om het raster te sorteren of te filteren op de waarden in die kolom.
    - Gebruik het veld **Filteren** om het rapport te filteren op elke waarde in een of meer van de beschikbare kolommen.
    - Gebruik het weergavemenu (boven het veld **Filteren**) om uw favoriete combinaties van sorteer- en filteropties op te slaan en te laden.

## <a name="export-an-inventory-value-storage-report"></a>Een rapport Opslag van voorraadwaarden exporteren

Elk rapport dat u genereert wordt opgeslagen in gegevensentiteit **Voorraadwaarde**. U kunt de standaardfuncties voor gegevensbeheer van Supply Chain Management gebruiken om gegevens van deze entiteit te exporteren naar elke ondersteunde gegevensindeling, inclusief CSV of Excel.

In het volgende voorbeeld ziet u hoe een **rapport met voorraadwaarden** wordt geëxporteerd.

1. Ga naar **Systeembeheer \> Werkruimten \> Gegevensbeheer**.
1. Selecteer in de sectie **Importeren/exporteren** de tegel **Exporteren**. 
1. Op de pagina **Exporteren** die wordt weergegeven, stelt u de exporttaak in. Voer eerst een groepsnaam voor de taak in.
1. Selecteer **Entiteit toevoegen** in de sectie **Geselecteerde entiteiten**.
1. Stel in het dialoogvenster dat verschijnt de volgende velden in:

    - **Naam entiteit:** selecteer **Voorraadwaarde**.
    - **Indeling doelgegevens**: selecteer de indeling waarnaar u gegevens wilt exporteren.

1. Selecteer **Toevoegen** om de nieuwe rij toe te voegen en selecteer vervolgens **Sluiten** om het dialoogvenster te sluiten.
1. Gewoonlijk exporteert u één rapport tegelijk. Als u één rapport wilt exporteren, stelt u een filter in voor de rij die u zojuist hebt toegevoegd aan het dialoogvenster **Query**. Op deze manier kunt u definiëren welk rapport uit de entiteit **Voorraadwaarde** wordt opgenomen in de export. Volg deze stappen om de volgende filteropties in te stellen om een enkel rapport te exporteren:

    1. Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een rij toe te voegen.
    2. Stel het veld **Tabel** in op **Voorraadwaarde**.
    3. Stel het veld **Afgeleide tabel** in op **Voorraadwaarde**.
    4. Stel het veld **Veld** in op het veld waarop u wilt filteren. Gewoonlijk gebruikt u de velden **Uitvoeringsnaam** en/of **Uitvoeringstijd**.
    5. Stel het veld **Criteria** in op de waarde die u wilt zoeken in het geselecteerde veld. (Als u het veld **Uitvoeringsnaam** in de vorige stap hebt geselecteerd, is deze waarde de naam van het rapport. Als u het veld **Uitvoeringstijd** hebt geselecteerd, wordt dit het tijdstip waarop het rapport is gegenereerd.)
    6. Voeg meer rijen toe aan het tabblad **Bereik** totdat u een unieke identificatie hebt voor het gewenste rapport.

1. Selecteer **OK** om de instellingen op te slaan en het dialoogvenster te sluiten.
1. Selecteer **Opslaan** om de instellingen voor exporteren op te slaan.
1. Selecteer op het tabblad **Exportopties** de optie **Nu exporteren** om het exportbestand te genereren.
1. Op de pagina **Uitvoeringsoverzicht** die wordt geopend, kunt u de status van uw exporttaak en een lijst met entiteiten zien die zijn geëxporteerd. Selecteer de entiteit **Voorraadwaarde** in de sectie **Verwerkingsstatus entiteit** en selecteer vervolgens **Bestand downloaden** om de geëxporteerde gegevens van die entiteit te downloaden.

Zie [Overzicht van Gegevensimport- en exporttaken](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) voor meer informatie over het gebruik van gegevensbeheer voor het exporteren van gegevens.
