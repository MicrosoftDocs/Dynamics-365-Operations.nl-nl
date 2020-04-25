---
title: Rapport Opslag artikelprijzen vergelijken
description: Informatie over het genereren van een opslagrapport voor het vergelijken van artikelprijzen en vervolgens het doorbladeren en/of exporteren van het resultaat.
author: AndersGirke
manager: tfehr
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 6c8c72a631d361d7dffb8d18e00636e51e7998d3
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201934"
---
# <a name="compare-item-prices-storage-report"></a>Rapport Opslag artikelprijzen vergelijken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een rapport **Opslag van artikelprijzen vergelijken** kunt uitvoeren en de uitvoer in digitale vorm beschikbaar kunt maken, als een interactieve pagina in Dynamics 365 Supply Chain Management of als een geëxporteerd document in verschillende indelingen.

Bij het bekijken van het rapport in uw browser worden kolommen en samengevoegde balansen dynamisch aangepast, afhankelijk van de indeling die u hebt geconfigureerd. U kunt de resultaten sorteren, filteren, details van de gegevens bekijken en nog veel meer.

Rapportresultaten worden opgeslagen in de gegevensentiteit **Artikelprijzen vergelijken**, waarmee u de resultaten kunt filteren en exporteren naar een indeling zoals CSV of Microsoft Excel.

Het rapport **Opslag van artikelprijzen vergelijken** kan handig zijn wanneer de uitvoer veel regels bevat. De uitvoer zal bijvoorbeeld een groot aantal regels bevatten als u meer dan 40.000 artikelen hebt die een artikelprijs in behandeling hebben in de kostprijsberekeningsversie.

## <a name="enable-compare-item-prices-storage"></a>Opslag van artikelprijzen vergelijken inschakelen

Voordat u deze functie kunt gebruiken, moet u deze inschakelen op uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en deze zo nodig in te schakelen. Hier ziet u de functie als:

- **Module** - Kostenbeheer
- **Functienaam** - Opslag van artikelprijzen vergelijken

## <a name="generate-a-compare-item-prices-storage-report"></a>Een rapport Opslag van artikelprijzen vergelijken genereren

Volg deze stappen om een rapport **Opslag van artikelprijzen vergelijken** te genereren en op te slaan:

1. Ga naar **Kostenbeheer > Query's en rapporten > Rapporten met vooraf bepaalde kosten > Opslag artikelprijzen vergelijken**.

1. Selecteer **Nieuw** om het deelvenster **Artikelprijzen vergelijken** te openen. Stel de volgende opties in om te definiëren welke prijzen moeten worden vergeleken in uw rapport:

    - Geef op het sneltabblad **Parameters** het rapport een unieke **Naam** en gebruik de velden in de secties **Prijzen in behandeling om te vergelijken** en **Gebruikte prijzen voor vergelijking** om te definiëren welke prijzen en datums moeten worden vergeleken.
    - Stel op het sneltabblad **Op te nemen records** filters en beperkingen in om op te geven welke gegevens u in het rapport wilt opnemen.
    - Stel op het sneltabblad **Op de achtergrond uitvoeren** in hoe, wanneer en hoe vaak u het rapport wilt genereren.
    > [!NOTE]
    > Dit rapport wordt altijd uitgevoerd als onderdeel van een batchtaak.

1. Selecteer **OK** om de instellingen toe te passen en het deelvenster te sluiten.

1. Nadat de batchtaak is voltooid, wordt deze vermeld op de pagina **Opslag artikelprijzen vergelijken**. U moet mogelijk de pagina vernieuwen om het rapport te kunnen bekijken.

## <a name="explore-the-compare-item-prices-storage-report"></a>Het rapport Opslag artikelprijzen vergelijken verkennen

Nadat u een rapport hebt gegenereerd, kunt u het als volgt op elk gewenst moment weergeven en verkennen:

1. Ga naar **Kostenbeheer > Query's en rapporten > Rapporten met vooraf bepaalde kosten > Opslag artikelprijzen vergelijken**.

1. Selecteer een rapport in de lijst.

1. U kunt een van de volgende dingen doen:

    - Selecteer **Overzicht** om een overzicht van de resultaten van uw rapport weer te geven.
    - Selecteer **Details weergeven** om een gedetailleerdere weergave van uw rapport te krijgen

1. Nadat de geselecteerde weergave is geopend, kunt u het volgende doen:

    - Vrijwel elke kolomkop selecteren om de tabel te sorteren of filteren op waarden in die kolom, net als bij de meeste standaardformulieren in Supply Chain Management. U kunt de kolom **Netto wijzigingsprijs%** niet sorteren of filteren omdat het een berekend veld is.
    - De **dimensieweergave** selecteren om een deelvenster te openen waarin u kunt kiezen welke dimensiekolom u in het formulier wilt opnemen. De optie **Instellingen opslaan** instellen op **Ja** als u deze instellingen wilt opslaan, zodat deze behouden blijven wanneer u het rapport de volgende keer opent. Selecteer **OK** om de instellingen toe te passen en te sluiten.
    - Een willekeurige rij in het formulier selecteren en vervolgens **Details weergeven** om meer informatie over het geselecteerde artikel weer te geven. U kunt van hieruit inzoomen op de gegevens.
    - Een willekeurige rij in het formulier selecteren en vervolgens **Vergelijkingsdiagram weergeven** selecteren om een interactieve grafische weergave van de resultaten te bekijken die betrekking hebben op het geselecteerde artikel. U kunt deze resultaten verkennen door verschillende grafische elementen te selecteren in de grafiek- en diagramlegenda.
    - Een willekeurige rij in het formulier selecteren en vervolgens **Berekeningsdetails weergeven** om meer informatie over berekeningen met betrekking tot het geselecteerde artikel weer te geven. U kunt van hieruit inzoomen op de gegevens.

## <a name="export-the-compare-item-prices-storage-report"></a>Het rapport Opslag artikelprijzen vergelijken exporteren

Elk rapport dat u genereert wordt opgeslagen in gegevensentiteit **Artikelprijzen vergelijken**. U kunt de standaardfuncties voor gegevensbeheer van Supply Chain Management gebruiken om gegevens van deze entiteit te exporteren naar elke ondersteunde gegevensindeling, inclusief CSV of Microsoft Excel.

Hierna volgt een voorbeeld van het exporteren van een rapport **Opslag artikelprijzen vergelijken**:

1. Ga naar **Systeembeheer > Werkgebieden > Gegevensbeheer**.

1. Selecteer de knop **Exporteren** in de sectie **Gegevensbeheer**.

1. De pagina **Exporteren** wordt geopend, waarmee u uw exporttaak kunt instellen. Begin door uw taak een **groepsnaam** te geven.

1. Selecteer in de sectie **Geselecteerde entiteiten** de optie **Entiteit toevoegen** om een dialoogvenster te openen waarin u de volgende opties kunt instellen:

    - **Entiteitnaam** - Selecteer **Artikelprijzen vergelijken**.
    - **Indeling van doelgegevens**: kies de indeling waarnaar u wilt exporteren.

1. Selecteer **Toevoegen** om de nieuwe rij toe te voegen en selecteer vervolgens **Sluiten** om het dialoogvenster te sluiten.

1. Gewoonlijk exporteert u één rapport tegelijk. Hiervoor stelt u een **filter** in voor de rij die u zojuist hebt toegevoegd aan het deelvenster **Query**. Hiermee kunt u definiëren welke rapporten uit de entiteit **Artikelprijzen vergelijken** u wilt opnemen in de export. Stel de volgende filteropties in om een enkel rapport te exporteren:

    - Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een nieuwe rij toe te voegen.
    - Stel **Tabel** in op **Artikelprijzen vergelijken**.
    - Stel **Afgeleid tabel** in op **Artikelprijzen vergelijken**.
    - Stel **Veld** in op het veld waarop u wilt filteren. Meestal zult u **Uitvoeringsnaam** of **Uitvoeringstijd** gebruiken.
    - Stel **Criteria** in voor de waarde van het geselecteerde veld waarnaar u wilt zoeken (de naam van het rapport of het tijdstip waarop het rapport is gegenereerd).
    - Voeg zo nodig meer rijen toe aan de tabel **Bereik** totdat u een unieke identificatie hebt voor het gewenste rapport.

1. Selecteer **OK** om de instellingen op te slaan en te sluiten.

1. Selecteer **Opslaan** om de instellingen voor exporteren op te slaan.

1. Open het tabblad **Exportopties** en selecteer **Nu exporteren** om het exportbestand te genereren.

1. De pagina **Uitvoeringsoverzicht** wordt geopend, waar u de status van uw exporttaak en een lijst met entiteiten kunt zien die zijn geëxporteerd. Selecteer de entiteit **Artikelprijzen vergelijken** die worden vermeld in het gebied **Verwerkingsstatus entiteit** en selecteer vervolgens **Bestand downloaden** om de geëxporteerde gegevens van die entiteit te downloaden.

Zie [Overzicht van Gegevensimport- en exporttaken](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) voor meer informatie over het gebruik van gegevensbeheer voor het exporteren van gegevens.
