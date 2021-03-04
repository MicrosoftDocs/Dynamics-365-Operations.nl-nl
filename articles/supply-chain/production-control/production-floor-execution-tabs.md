---
title: De uitvoeringsinterface voor de werkvloer ontwerpen
description: In dit onderwerp wordt beschreven hoe u de inhoud van de gebruikersinterface ontwerpt voor elke configuratie.
author: johanhoffmann
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 81c5c83128bb81523dee6ede549eece7b0d80e30
ms.sourcegitcommit: d9d1ddce6a334ade8b32b5ea3ac4c1e1a8f72715
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664267"
---
# <a name="design-the-production-floor-execution-interface"></a>De uitvoeringsinterface voor de werkvloer ontwerpen

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

U kunt de inhoud van de gebruikersinterface ontwerpen voor elke configuratie die wordt gebruikt door de uitvoeringsinterface van de werkvloer. Werknemers in de ene werkcel moeten bijvoorbeeld mogelijk taakinstructies kunnen openen op de productievloer, terwijl in een andere werkcel de instructies niet nodig zijn. In dat geval moeten er twee configuraties worden gemaakt, één met een knop voor het openen van documentbijlagen en één zonder deze knop.

## <a name="design-a-tab"></a>Een tabblad ontwerpen

Op de pagina **Uitvoering werkvloer configureren** kunt u tabbladen maken en configureren door **Tabbladen ontwerpen** te selecteren in het actievenster.

Elk tabblad is verdeeld in vier secties, zoals in de volgende afbeelding wordt weergegeven.

![Indeling van tabbladen](media/pfe-tab-layout.png "Indeling van tabbladen")

De volgende elementen worden in de afbeelding weergegeven:

1. Primaire werkbalk
1. Secundaire werkbalk
1. Hoofdweergave
1. Gedetailleerde weergave

Voer de volgende stappen uit om een nieuw tabblad te maken en te configureren:

1. Ga naar **Productiebeheer &gt; Instellingen &gt; Productie-uitvoering**.

1. Selecteer **Tabbladen ontwerpen** in het actievenster om de pagina **Tabbladen ontwerpen** te openen.

    ![De pagina Tabbladen ontwerpen](media/pfe-design-tabs.png "De pagina Tabbladen ontwerpen")

1. Selecteer **Nieuw** in het actievenster.

1. Geef de koptekst van de pagina de volgende instellingen:

    - **Tabbladnaam**: geef een naam op voor het tabblad.
    - **Hoofdweergave**: selecteer uit twee vooraf gedefinieerde takenlijsten (*Actieve taken* of *Alle taken*).
    - **Detailweergave**: selecteer uit een lege waarde of **Taakdetails**. Als u de lege waarde selecteert, wordt op het tabblad geen gedetailleerde weergave weergegeven. Als u **Taakdetails selecteert**, bevat de gedetailleerde weergave een gedetailleerde omschrijving van de taak die in de takenlijst in de hoofdweergave is geselecteerd.

1. Kies in de sectie **Primaire werkbalk** welke knoppen beschikbaar moeten zijn op de primaire werkbalk. De kolom **Beschikbare acties** geeft een lijst weer met alle knoppen die kunnen worden toegevoegd. De kolommen **Geselecteerde acties** geeft een lijst weer met alle knoppen die in de huidige configuratie zijn opgenomen. Gebruik de knoppen tussen de kolommen om geselecteerde artikelen naar wens tussen de kolommen te verplaatsen. Gebruik de knoppen omhoog en omlaag naast de kolom **Geselecteerde acties** om de volgorde te bepalen waarin de knoppen in de gebruikersinterface worden weergegeven.

1. Kies in de sectie **Secundaire** **werkbalk** welke knoppen beschikbaar moeten zijn op de secundaire werkbalk. De kolom **Beschikbare acties** geeft een lijst weer met alle knoppen die kunnen worden toegevoegd. De kolommen **Geselecteerde acties** geeft een lijst weer met alle knoppen die in de huidige configuratie zijn opgenomen. Gebruik de knoppen tussen de kolommen om geselecteerde artikelen naar wens tussen de kolommen te verplaatsen. Gebruik de knoppen omhoog en omlaag naast de kolom **Geselecteerde acties** om de volgorde te bepalen waarin de knoppen in de gebruikersinterface worden weergegeven.

## <a name="associate-a-tab-with-a-configuration"></a>Een tabblad aan een configuratie koppelen

Nadat u alle benodigde tabbladen hebt ontworpen, kunt u deze aan een configuratie koppelen.

1. Ga naar **Productiebeheer &gt; Instellingen &gt; Uitvoering werkvloer configureren**.

    ![Uitvoering productievloer configureren](media/pfe-config-prod-floor-execution.png "Uitvoering productievloer configureren")

1. Selecteer op de snelle tab **Tabblad selecteren** de optie **Toevoegen**.

1. Er wordt een nieuwe rij aan het raster toegevoegd. Selecteer voor deze nieuwe rij de naam van een tabblad dat u aan de configuratie wilt toevoegen.

1. Ga zo nodig verder om extra tabbladen toe te voegen.

1. Gebruik de knoppen **Omhoog verplaatsen** en **Omlaag verplaatsen** op de werkbalk om de tabbladen naar wens te rangschikken. De tabbladen worden van links naar rechts weergegeven in de volgorde die op de bovenstaande schermopname wordt weergegeven (het tabblad bovenaan wordt links weergegeven).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]