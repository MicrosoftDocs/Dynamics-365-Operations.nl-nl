---
title: Aanvullingsstrategieën
description: Dit onderwerp bevat informatie over aanvullingsstrategieën en een uitleg over het gebruik van het veld Aanvullingsstrategie voor waveaanvraagregels van een aanvullingssjabloon om te selecteren hoe aanvulling wordt uitgevoerd.
author: mirzaab
manager: tfehr
ms.date: 10/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-29
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 9c23126c6ab15a1924b34f98d33a0661011ba8bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996093"
---
# <a name="replenishment-strategies"></a>Aanvullingsstrategieën

[!include [banner](../includes/banner.md)]

De sjablonen die op de pagina **Aanvullingssjablonen** zijn gedefinieerd, bevatten waveaanvraagregels voor de aanvullingssjabloon waarmee u kunt selecteren hoe aanvulling wordt uitgevoerd. Elke regel bevat nu een veld **Aanvullingsstrategie**.

De strategie bij *Hoeveelheid waveaanvraag* is de standaardstrategie. Dit is de aanvullingsstrategie die werd gebruikt vóór de introductie van het veld **Aanvullingsstrategie**. Hierdoor worden de aanvullingslocatie-instructies gebruikt om locaties te vinden die kunnen worden aangevuld. Vervolgens worden deze locaties aangevuld totdat de vraag is gedekt.

Met de strategie *Maximale capaciteit locatie* worden enkele nieuwe functies geïntroduceerd. Net zoals de strategie *Hoeveelheid waveaanvraag*, gebruikt deze strategie de aanvullingslocatie-instructies om locaties te vinden die kunnen worden aangevuld. Vervolgens worden deze locaties aangevuld totdat de vraag is gedekt. Het verschil met de strategie *Hoeveelheid waveaanvraag* is dat alle aangevulde locaties worden aangevuld tot de maximale capaciteit, zoals gedefinieerd door de locatievoorraadlimieten. Met de strategie *Maximale capaciteit locatie* wordt geprobeerd werk te creëren om te zorgen voor de gevraagde hoeveelheid, plus een extra hoeveelheid, om de locaties te vullen die worden aangevuld. In sommige gevallen kan deze poging echter mislukken. De bulklocaties hebben bijvoorbeeld mogelijk niet voldoende voorraad om de extra hoeveelheid te dekken. In deze gevallen detecteert het systeem de fout en probeert het te herstellen.

Een piekperiode is een voorbeeld van een situatie waarin de strategie *Maximale capaciteit locatie* de voorkeur geniet boven de strategie *Hoeveelheid waveaanvraag*. Tijdens piekperioden kunnen grote volumes van bepaalde artikelen worden verkocht. Daarom wilt u mogelijk de desbetreffende orderverzamellocaties zo veel mogelijk proactief aanvullen om het aantal werk-id's dat voor aanvulling wordt gemaakt, te verminderen.

> [!IMPORTANT]
> Als u de strategie *Maximale capaciteit locatie* volledig wilt benutten, moet u de voorraadlimieten opnieuw definiëren voor de relevante locaties. Anders werkt deze strategie net als de strategie *Hoeveelheid waveaanvraag*.

## <a name="turn-on-the-replenish-to-max-based-on-stocking-limits-feature"></a>De functie Aanvullen tot max. op basis van voorraadlimieten inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van het werkgebied [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van deze functie te controleren en de functie desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Aanvullen tot max. op basis van voorraadlimieten*

## <a name="set-up-replenishment-strategies"></a>Aanvullingsstrategieën instellen

Ga naar **Magazijnbeheer \> Instellingen \> Aanvulling \> Aanvullingssjablonen** om de sjablonen te openen. Selecteer of maak in de sectie **Overzicht** een aanvullingssjabloon voor een waveaanvraag, waarbij het veld **Aanvullingstype** is ingesteld op *Waveaanvraag*. Stel vervolgens de regels van de aanvullingssjabloon in de sectie **Details aanvullingssjabloon** in. Selecteer voor elke regel in het veld **Aanvullingsstrategie** de aanvullingsstrategie die u wilt gebruiken.

![De pagina Aanvullingssjablonen](media/ReplenTempWaveDmdMaxLocCap.png "De pagina Aanvullingssjablonen")

Als de kolom **Aanvullingsstrategie** niet wordt weergegeven in het raster in de sectie **Details van aanvullingssjabloon**, controleert u of de functie is ingeschakeld en of de geselecteerde aanvullingssjabloon het aanvullingstype *Waveaanvraag* heeft.

> [!NOTE]
> De strategie bij *Hoeveelheid waveaanvraag* is de standaardstrategie. Daarom hoeft u alleen de regels van de aanvullingssjabloon bij te werken waar u de strategie *Maximale capaciteit locatie* wilt gebruiken.

## <a name="example-scenarios"></a>Voorbeeldscenario's

### <a name="example-1"></a>Voorbeeld 1

Voor dit voorbeeld is er slechts één aanvullingssjabloon die slechts één aanvullingssjabloonregel heeft.

U maakt een verkooporder voor 130 stuks van artikel A0001. Voordat u de order vrijgeeft aan het magazijn, wordt het magazijn op de volgende manier ingesteld:

- Er is slechts één bulklocatie en deze heeft 500 stuks beschikbaar in de voorhanden voorraad.
- Er zijn drie orderverzamellocaties met elk een voorraadlimiet van 100 stuks. (Onthoud dat voorraadlimieten zijn vereist voor de strategie *Maximale capaciteit locatie*.)
- De wegzetlocaties voor aanvulling zijn dezelfde als de verzamellocaties voor verkoop.
- De aanvullingseenheid is een doos (1 doos = 20 stuks).

Op het moment van de order is de volgende voorraad voorhanden in de verzamellocaties voor verkoop:

- **Orderverzamellocatie-001:** 20 stuks (1 doos)
- **Orderverzamellocatie-002:** 0 stuks
- **Orderverzamellocatie-003:** 0 stuks

In eerste instantie wordt de aanvullingsstrategie ingesteld op *Hoeveelheid waveaanvraag*.

Nadat u de verkooporder hebt vrijgegeven aan het magazijn en de waveverwerking voor de wave wordt uitgevoerd, krijgt u het volgende aanvullingswerk:

- **Aanvullingswerk 1:** haal vier dozen op van de bulklocatie en zet deze op verzamellocatie-001.
- **Aanvullingswerk 2:** haal twee dozen op van de bulklocatie en zet deze op verzamellocatie-002.

U krijgt twee aanvullingswerk-id's, omdat u twee locaties moet aanvullen en meerdere wegzetlocaties niet worden ondersteund.

Als u in plaats daarvan de aanvullingsstrategie instelt op *Maximale capaciteit locatie*, krijgt u het volgende aanvullingswerk:

- **Aanvullingswerk 1:** haal vier dozen op van de bulklocatie en zet deze op verzamellocatie-001.
- **Aanvullingswerk 2:** haal vijf dozen op van de bulklocatie en zet deze op verzamellocatie-002.

[![Voorbeeld 1](media/ReplenTemp_example_1.png "Voorbeeld 1")](media/ReplenTemp_example_1_large.png)

### <a name="example-2"></a>Voorbeeld 2

In dit voorbeeld ziet u wat er gebeurt wanneer de bulklocatie onvoldoende voorraad heeft om de extra hoeveelheid te dekken. Hetzelfde scenario als voorbeeld 1 wordt gebruikt, maar de bulklocatie heeft 160 stuks (8 dozen).

De strategie *Hoeveelheid waveaanvraag* maakt hetzelfde werk als in voorbeeld 1.

Aangezien de strategie *Maximale capaciteit locatie* probeert om de werk-id's te maken zoals in voorbeeld 1, kan het mislukken. Het systeem probeert op dat moment te herstellen.

Afhankelijk van de instelling van de optie **Splitsen toestaan** in de locatie-instructies voor het verzamelen van de aanvulling, zijn twee resultaten mogelijk:

- Als de optie **Splitsen toestaan** is ingesteld op *Ja*, wordt het volgende aanvullingswerk gemaakt:

    - **Aanvullingswerk 1:** haal vier dozen op van de bulklocatie en zet deze op verzamellocatie-001.
    - **Aanvullingswerk 2:** haal vier dozen op van de bulklocatie en zet deze op verzamellocatie-002.

- Als de optie **Splitsen toestaan** is ingesteld op *Nee*, wordt het volgende aanvullingswerk gemaakt:

    - **Aanvullingswerk 1:** haal vier dozen op van de bulklocatie en zet deze op verzamellocatie-001.
    - **Aanvullingswerk 2:** haal twee dozen op van de bulklocatie en zet deze op verzamellocatie-002.

De resultaten verschillen vanwege de informatie die beschikbaar is wanneer u het werk maakt. Wanneer de optie **Splitsen toestaan** is ingesteld op *Ja* in de locatie-instructies voor het verzamelen van de aanvulling, weet u dat u 160 stuks hebt gevonden. Daarom kunt u werk voor die hoeveelheid maken. Als de optie **Splitsen toestaan** echter is ingesteld op *Nee*, weet u niet dat er 160 stuks bestaan. Omdat de extra hoeveelheid die u wilde aanvullen drie dozen groot was, verwijdert u die extra hoeveelheid en probeert u de oorspronkelijke hoeveelheid opnieuw.

[![Voorbeeld 2](media/ReplenTemp_example_2.png "Voorbeeld 2")](media/ReplenTemp_example_2_large.png)

Als u de maximumhoeveelheid wilt ophalen voor de aangevulde locaties, moet u daarom de optie **Splitsen toestaan** op *Ja* instellen in de locatie-instructies voor het verzamelen van de aanvulling.
