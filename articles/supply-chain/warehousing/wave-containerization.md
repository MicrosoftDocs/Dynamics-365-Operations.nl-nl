---
title: Containervorming
description: In dit onderwerp wordt beschreven hoe u de containervorming van ladingen kunt automatiseren. Bij automatische containervorming worden containers gecreëerd en wordt de orderverzameling uitgevoerd voor zendingen wanneer een wave wordt verwerkt.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable, WHSContainerizatonHistory, WHSContainerPackingPolicyChange, WHSManifestShipmentContainers, WHSAllowedContainerTypeGroup, WHSPostMethod, WHSContainerCreateDialog, WHSContainerCloseDiag, WHSContainer
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 2f738c0404a41ef862d4985a170a0eba991e4dd4
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686621"
---
# <a name="containerization"></a>Containervorming

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u de containervorming van ladingen kunt automatiseren. Bij automatische containervorming worden containers gecreëerd en wordt de orderverzameling uitgevoerd voor zendingen wanneer een wave wordt verwerkt.

U moet het volgende maken om containervorming in te stellen:

- **Containertype**: definieer de fysieke kenmerken van de containers. Gebruik containertypen om voorraadartikelen in een specifiek type en formaat verpakking in te pakken, zoals bakken of pallets.
- **Containergroepen**: maak groepen containertypes die gelijkaardig zijn. Een containergroep kan bijvoorbeeld containertypen bevatten die soortgelijke groottedimensies hebben. Een containergroep geeft de volgorde op waarin containers worden verpakt en het vulpercentage van elke container.
- **Containervormingsjabloon**: maak sjablonen die regels definiëren voor containervorming. Bijvoorbeeld regels voor het mengen van voorraad en andere verpakkingsstrategieën.
- **Wavesjablonen**: stel een of meer wavesjablonen in om het orderverzamelwerk voor containervorming te maken.

## <a name="create-wave-templates-for-containerization"></a>Wavesjablonen maken voor containervorming

U moet een of meer verzendwavesjablonen instellen voor containervorming. Wavesjablonen omvatten criteria die het volgende definiëren:

- Waves verwerken. Dit kan handmatig of automatisch zijn.
- Orderverzamelwerk maken. Dit wordt bepaald door de wavemethoden. De wavesjabloon moet de methode voor **containervorming** bevatten.
- Hoe artikelen of toewijzingsregels koppelen aan een wave.

Zie [Wavesjablonen](wave-templates.md) voor meer informatie.

## <a name="create-container-types"></a>Containertypen maken

Gebruik containertypen om beschrijvingen van containers te maken, waaronder maximumwaarden voor fysieke groottedimensies en gewichtcapaciteit. Wanneer een containerwave wordt verwerkt, worden de containers gemaakt op basis van de gegevens over het containertype.

Ga als volgt te werk om een containertype in te stellen:

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Containers** \> **Containertypen**.
1. Selecteer **Nieuw** om een nieuw containertype te maken.
1. Geef een unieke id en een beschrijving voor het containertype op.
1. Voer in het veld **Tarragewicht** het werkelijke of geschatte gewicht van de container in.
1. Voer in het veld **Maximumgewicht** het maximale gewicht dat de container kan bevatten.
1. Geef in de velden **Maximumvolume voor containervorming**, **Maximale lengte voor containervorming**, **Maximale breedte voor containervorming** en **Maximale hoogte voor containervorming** de dimensies van de container op.

    > [!NOTE]
    > De waarden voor lengte en breedte zijn uitwisselbaar. Dit betekent dat u artikelen lateraal of op de x-as kunt draaien, indien nodig. Als de lengte bijvoorbeeld 2 meter is, en de breedte is 1 meter, kunt u de lengte wijzigen naar 1 meter en de breedte naar 2 meter. Merk op dat dit niet geldt voor de hoogtedimensie. U kunt de hoogtewaarde niet wijzigen om een artikel verticaal te draaien.

1. Selecteer aangepaste kenmerkwaarden voor de container in de velden voor kenmerken. Kenmerken zijn aangepaste waarden die worden gebruikt om artikelen te filteren of te sorteren op basis van een waarde die anders niet beschikbaar is. Als u bijvoorbeeld artikelen wilt verpakken voor een bepaalde klant, kunt u een kenmerk voor de klantnaam maken. U maakt kenmerken op de pagina **Containerkenmerken**.

## <a name="create-container-groups"></a>Containergroepen maken

U kunt logische groepen containertypen instellen. Voor elke groep kunt u de volgorde opgeven waarin de containers moeten worden verpakt, en het vulpercentage van elke container. De groottedimensies van het artikel bepaalt of het in een container past. De container die het nauwst aansluit bij de groottedimensies van het artikel, wordt gebruikt. Als u meerdere containertypen in een groep hebt, is het raadzaam deze op grootte te rangschikken zodat de grootste container eerste is, nummer 1 is in de volgorde, en de kleinste container laatste is.

Ga als volgt te werk om een containergroep in te stellen:

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Containers** \> **Containergroepen**.
1. Selecteer **Nieuw** om een containergroep te maken.
1. Geef een unieke id en een beschrijving voor de containergroep op.
1. Selecteer op het sneltabblad **Details** de optie **Nieuw** om een containertype toe te voegen aan de groep.
1. Selecteer een containertype in het veld **Containertype**.
1. Selecteer **Omhoog** of **Omlaag** om de volgorde op te geven waarin de containertypen zijn verpakt.

## <a name="create-container-build-templates"></a>Containervormingssjablonen maken

U kunt regels instellen voor het containervormingsproces, zoals voorraadmengregels en andere verpakkingsstrategieën. U kunt bijvoorbeeld een regel zo instellen dat werknemers geen toewijzingsregels die verkooporders van verschillende klanten vertegenwoordigen, in dezelfde container kunnen plaatsen.

Ga als volgt te werk om een containervormingssjabloon in te stellen.

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Containers** \> **Containervormingssjablonen**.
1. Maak een nieuwe containervormingssjabloon.
1. Voer in de velden **Containervormingsnaam** en **Volgnummer** de naam in van de containervormingssjabloon en de order die aan toewijzingsregels is gekoppeld.

    > [!NOTE]
    > Het systeem zal de eerste sjabloon gebruiken waarvoor de toewijzingsregel voldoet aan de zoekcriteria. Daarom moet u de sjabloon met de meest specifieke criteria boven aan de lijst plaatsen. Hoe breder de criteria, hoe waarschijnlijker dat een toewijzingsregel voldoet aan de criteria. Dit kan leiden tot regels die aan de verkeerde container worden toegewezen. Indien nodig u **Omhoog** of **Omlaag** selecteren om de reeks sjablonen te wijzigen.

1. Selecteer in het veld **Containergroep-id** de containergroep waaruit u containers wilt maken.
1. Selecteer in het veld **Basisquerytypen** het type query dat bepaalt wat wordt verpakt en waar u de filterquery op moet baseren. De volgende opties zijn beschikbaar:

      - **Verkooptoewijzingsregel**: verpak toewijzingsregels die zijn gemaakt voor verkooporders.
      - **Transfertoewijzingsregel**: verpak toewijzingsregels die zijn gemaakt voor overboekingsorders.
      - **Container**: verpak een container die al was gemaakt door het containervormingsproces. Dit wordt bijvoorbeeld gebruikt voor het nestbare containers.

        > [!NOTE]
        > Als u nestbare containers wilt gebruiken, moet u de containervormingsmethode herhaalbaar maken. Zie [Wavesjablonen](wave-templates.md) voor meer informatie.

1. Voer op het sneltabblad **Algemeen** in het veld **Stapcode wave** de unieke id in van de waveverwerkingsmethode die de containervormingssjabloon koppelt aan stappen in een wavesjabloon.
1. Schakel het selectievakje **esplitst verzamelen toestaan** in om werknemers toe te staan artikelen van een werkorder in afzonderlijke containers te verpakken. Hiervoor moet de volledige hoeveelheid in de container passen. De grootste maateenheid in de toewijzingsregel wordt altijd gebruikt.
1. Selecteer in het veld **Verpakken per eenheid** de maateenheid die de container voorstelt. U kunt bijvoorbeeld, aangeven dat een verpakking een container is. Als u verpakt volgens maateenheid, kunt u geen containergroep opgeven omdat de maateenheid de container is.
1. Selecteer in het veld **Containerverpakkingsstrategie** de te gebruiken verpakkingsstrategie. De volgende opties zijn beschikbaar:

    > [!NOTE]
    > De strategie geldt voor verkoopstoewijzingsregels en transfertoewijzingsregels.

      - **Verpakken in alle open containers**: het systeem evalueert of de toewijzingsregel in een container past die tijdens de containervormingscyclus is gemaakt.
      - **Alleen in huidige container verpakken**: het systeem evalueert alleen of de toewijzingsregel in de zojuist gemaakte container past.

    Zie [Containerpakstrategieën](container-packing-strategy-overview.md) voor meer informatie en voorbeelden over het werken met containerverpakkingsstrategieën.

1. Selecteer **Logica-onderbrekingen mengen** om regels in te stellen voor het verpakken van toewijzingsregels in containers. U kunt bijvoorbeeld een regel maken waardoor werknemers toewijzingsregels voor twee verschillende artikelen in dezelfde container kunnen verpakken. Volg deze stappen om een mengregel te maken:

    1. Selecteer op de pagina **Logica-onderbrekingen mengen** de optie **Nieuw**.
    1. Selecteer in het veld **Tabel** de tabel met het veld dat moet worden gebruikt als criterium voor de opsplitsing van de menglogica.
    1. Selecteer in het veld **Veld selecteren** het veld dat moet worden gebruikt als criterium voor de opsplitsing van de menglogica.
    1. Herhaal deze stappen totdat u alle criteria voor het opsplitsen van de menglogica hebt toegevoegd.

    > [!NOTE]
    > Als u menglogica gebruikt, raden we u aan te rangschikken op dezelfde velden in de filtercriteriaquery. Dit beperkt het aantal containers dat wordt gemaakt.
