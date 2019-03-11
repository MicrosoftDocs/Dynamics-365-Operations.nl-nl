---
title: Een magazijn instellen op basis van een magazijnconfiguratiesjabloon
description: In dit onderwerp wordt uitgelegd hoe u een magazijn instelt op basis van een magazijnconfiguratiesjabloon.
author: perlynne
manager: AnnBe
ms.date: 11/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 17016d015925cd31117231799b8741ffddb793f7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "338056"
---
# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a>Een magazijn instellen op basis van een magazijnconfiguratiesjabloon

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een magazijn instelt op basis van een magazijnconfiguratiesjabloon. Er zijn verschillende vooraf gedefinieerde sjablonen die u kunt gebruiken. Zie voor informatie over het gebruik van deze sjablonen [Gegevenssjablonen voor configuratie](../../dev-itpro/data-entities/configuration-data-templates.md).

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a>Scenario's waarin configuratiesjablonen nuttig kunnen zijn

Configuratiesjablonen kunnen in veel scenario's nuttig zijn. Hieronder vindt u enkele voorbeelden:

- U hebt configuratie-instellingen in een testomgeving voltooid en getest, en nu wilt u de instellingen kopiëren naar een productieomgeving.
- U wilt de magazijninstellingen Implementeren voor meerdere rechtspersonen of een nieuw magazijn maken in dezelfde rechtspersoon.
- U wilt u snel voorbereiden voor een demonstratie van de magazijnfunctionaliteit.
- U wilt dat bestaande artikelen en magazijnen de functionaliteit in Magazijnbeheer gebruiken in plaats van de functionaliteit in Voorraadbeheer.

Dit onderwerp is gericht op de eerste van deze scenario's. Hier ziet u hoe u een configuratiesjabloon kunt gebruiken om configuratie-instellingen van een testomgeving naar een productieomgeving te kopiëren.

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a>Configuratie-instellingen van een testomgeving naar een productieomgeving kopiëren

Voor dit scenario bestaan de configuratie-instellingen voor een magazijn en enkele transactieprocessen al in een testomgeving. Nu wilt u de configuratie-instellingen voor het magazijn van de testomgeving kopiëren naar een productieomgeving.

> [!NOTE]
> Het is belangrijk dat u andere gerelateerde instellingsgegevens opneemt wanneer u configuratie-instellingen kopieert. Stel dat u producten wilt instellen door de instellingen vanuit een testomgeving te kopiëren. U kunt echter geen vaste afhaallocatie voor een product instellen voordat dit product is gemaakt. Hoewel afzonderlijke configuratiesjablonen dit soort afhankelijkheden niet ondersteunen, zijn er standaardgegevenssjablonen die deze wel ondersteunen. U kunt deze standaardgegevenssjablonen eenvoudig opnemen in een configuratieproces.

### <a name="export-a-default-warehouse-template"></a>Een standaardmagazijnsjabloon exporteren 

1. Open het werkgebied **Gegevensbeheer**.

    > [!NOTE]
    > Als u dit werkgebied voor het eerst gebruikt, moet u alle gegevensentiteiten laden voordat u doorgaat.

2. Selecteer de tegel **Sjablonen** en selecteer vervolgens **Standaardsjablonen laden** om de standaardsjablonen te laden.

    > [!NOTE]
    > **Standaardsjablonen laden** is alleen beschikbaar in de weergave **Uitgebreid**. Selecteer **Raamwerkparameters** en selecteer in het veld **Standaardwaarden weergeven** de optie **Uitgebreide weergave**.

3. Wanneer de standaardsjablonen zijn geladen, kunt u deze aanpassen aan uw bedrijfsvereisten.

    > [!NOTE]
    > Voor het laden van standaardsjablonen en het importeren van sjablonen hebt u systeembeheerderstoegang nodig. Deze vereiste zorgt ervoor dat alle entiteiten correct worden geladen in de sjabloon.

4. Zorg ervoor dat u zich in de rechtspersoon bevindt waaruit u de bedrijfsspecifieke gegevens wilt exporteren.
5. Selecteer **Exporteren** in het werkgebied.
6. Maak een nieuw exportproject.
7. Selecteer **+ Sjabloon toevoegen** en zoek de standaardmagazijnsjabloon **400 - WMS**. Met deze sjabloon voegt u gegevensentiteiten voor de magazijnconfiguratie toe.

    > [!NOTE]
    > Als de gegevens die u wilt exporteren, moeten worden gefilterd (bijvoorbeeld als u alleen de gegevens wilt exporteren die betrekking hebben op een bepaald magazijn), moet u elke gegevensentiteit evalueren en filters via een query toevoegen. U kunt ook alle gegevens exporteren en vervolgens de records verwijderen die niet vereist zijn in de doelbestanden.

8. Selecteer **Exporteren**. Gegevens die zijn gerelateerd aan alle gegevensentiteiten in het project worden geëxporteerd.

U kunt een zipbestand voor het gegevenspakket downloaden. Dit bestand bevat alle gegevens in de geselecteerde indeling (bijvoorbeeld een Excel-indeling). Zoals aangegeven moet een aantal records in de gegevenspakketbestanden wellicht worden bijgewerkt voordat u deze in de productieomgeving kunt importeren. Als u een record bijwerkt, moet u ervoor zorgen dat u de bestandsnaam niet wijzigt.

### <a name="import-a-warehouse-configuration-setup"></a>Magazijnconfiguratie-instellingen importeren

1. Zorg ervoor dat u zich in de doelomgeving in het bedrijf bevindt waarin u de magazijngegevens wilt importeren.

    > [!NOTE]
    > Voordat u de import uitvoert, moet u eventuele gegevensafhankelijkheden identificeren. De sjabloon **Magazijnbeheer** bevat bijvoorbeeld een gegevensentiteit met de naam **Magazijnbeschikkingscodes**. Deze entiteit bevat gegevens die gerelateerd zijn aan de pagina **Beschikkingscodes** (**Magazijnbeheer** > **Instelling** > **Mobiel apparaat** > **Beschikkingscodes**). Als het retourproces voor verkooporders al wordt verwerkt door bestaande instellingen, bevat het veld **Beschikkingscode retourneren** een waarde. De beschikkingscode in dit veld is gerelateerd aan de gegevensentiteit **Beschikkingscode**, die deel uitmaakt van de sjabloon **Verkoop en marketing**. Als de gegevens uit de gegevensentiteit **Beschikkingscode** niet worden geïmporteerd vóór de gegevens uit het veld **Magazijnbeschikkingscodes**, mislukt de import.

2. Selecteer **Importeren** in het werkgebied **Gegevensbeheer**.
3. Maak een nieuw importproject.
4. Selecteer **+ Bestand toevoegen** en upload het zipbestand voor het gegevenspakket.
5. Selecteer **Importeren**. In de weergave **Uitgebreid** kunt u de optie **Filteren** gebruiken om snel een overzicht te krijgen van problemen die tijdens het importeren kunnen optreden.

Met **Uitvoeringslogboek weergeven** kunt u gedetailleerde informatie weergeven over elk gegevensitem dat wordt geïmporteerd. U kunt de weergave Faseringsgegevens gebruiken om snel naar de doelgegevens te gaan. Op deze manier ziet u hoe de geïmporteerde gegevens eruitzien op de gerelateerde pagina's in de toepassing. Wanneer u de standaardgegevenssjablonen gebruikt, werkt de importvolgorde voor elke gegevensentiteit op de vooraf gedefinieerde manier om ervoor te zorgen dat alle afhankelijke gegevens eerst worden geïmporteerd. Als aangepaste gegevensentiteiten deel uitmaken van het project, moet u ervoor zorgen dat de juiste volgorde is gedefinieerd. Zie [Gegevenssjablonen voor configuratie](../../dev-itpro/data-entities/configuration-data-templates.md) voor meer informatie.

Bekijk deze video van 3 minuten op YouTube: [Het magazijnsjabloon gebruiken om configuratie te kopiëren in Microsoft Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=K2WIfFlqJYs) voor meer informatie over het gebruik van magazijnsjablonen om de configuratie van een magazijn van het ene bedrijf naar een nieuw bedrijf in dezelfde instantie te kopiëren.

## <a name="related-topic"></a>Verwant onderwerp

[Gegevenssjablonen voor configuratie](../../dev-itpro/data-entities/configuration-data-templates.md)
