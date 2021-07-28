---
title: Takenlijsten maken en taken toevoegen
description: In dit onderwerp wordt beschreven hoe u takenlijsten maakt en hieraan taken toewijst in Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e7964181a739a8138011abca77d0321d819e0a98
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6354488"
---
# <a name="create-task-lists-and-add-tasks"></a>Takenlijsten maken en taken toevoegen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u takenlijsten maakt en hieraan taken toewijst in Microsoft Dynamics 365 Commerce.

Een *taak* definieert een specifiek werkstuk of een actie die door iemand moet worden voltooid op of voor een bepaalde vervaldatum. In Dynamics 365 Commerce kan een taak gedetailleerde instructies en informatie over een contactpersoon bevatten. Het kan ook koppelingen bevatten naar bewerkingen in de back-office, bewerkingen op het verkooppunt (POS) of sitepagina's, om de productiviteit te helpen verbeteren en de context te bieden die de eigenaar van de taak nodig heeft om de taak efficiënt te kunnen uitvoeren.

Een *takenlijst* is een verzameling taken die moeten worden voltooid als onderdeel van een bedrijfsproces. Er kan bijvoorbeeld een takenlijst zijn die moet worden voltooid door een nieuwe werknemer tijdens de onboarding, een takenlijst voor kassiers die in de avonddienst werken of een takenlijst die moet worden voltooid om de winkel voor te bereiden op de komende feestdagen. In Commerce kan elke takenlijst met een doeldatum worden toegewezen aan een willekeurig aantal winkels of werknemers en worden geconfigureerd voor herhaaldelijke uitvoering.

Zowel managers als werknemers kunnen takenlijsten maken in Commerce Back Office en deze vervolgens toewijzen aan een set winkels.

## <a name="create-a-task-list"></a>Een takenlijst maken

Volg deze stappen om een takenlijst te maken.

1. Ga naar **Detailhandel en commerce \> Taakbeheer \> Taakbeheer beheren**.
1. Selecteer **Nieuw** en voer vervolgens waarden in de velden **Naam**, **Beschrijving** en **Eigenaar** in.
1. Selecteer **Opslaan**.

## <a name="add-tasks-to-a-task-list"></a>Taken toevoegen aan een takenlijst

Volg deze stappen om taken toe te voegen aan een takenlijst.
 
1. Selecteer **Nieuw** op het sneltabblad **Taken** van een bestaande takenlijst om een taak toe te voegen.
1. Voer in het dialoogvenster **Een nieuwe taak maken**, in het veld **Naam** een naam in voor de taak.
1. Voer in het veld **Verschuiving van vervaldatum vanaf doeldatum** een positief of negatief geheel getal in. Voer bijvoorbeeld **-2** in als de taak twee dagen vóór de vervaldatum van de takenlijst moet zijn voltooid.
1. Voer in het veld **Notities** gedetailleerde instructies in.
1. Voer in het veld **Contactpersoon** de naam in van een deskundige die contact kan opnemen met de eigenaar van de taak als deze hulp nodig heeft.
1. Voer in het veld **Taakkoppeling** een koppeling in op basis van de aard van de taak.

> [!TIP]
> Hoewel u het veld **Toegewezen aan** kunt gebruiken om taken aan iemand toe te wijzen terwijl u een takenlijst maakt, is het raadzaam om geen taken toe te wijzen tijdens het maken van een takenlijst. Wijs in plaats daarvan de taken toe nadat de lijst is geconcretiseerd voor afzonderlijke winkels.

## <a name="use-task-links-to-help-improve-worker-productivity"></a>Taakkoppelingen gebruiken om de productiviteit van werknemers te helpen verbeteren

Met Commerce kunt u taken koppelen aan specifieke POS-bewerkingen, zoals het uitvoeren van een verkooprapport, het weergeven van een online trainingsvideo voor de introductie van nieuwe werknemers of het uitvoeren van een bewerking in de back-office. Met deze functie krijgen de eigenaars van taken de gegevens die ze nodig hebben om een taak efficiënt uit te voeren.

Voer de volgende stappen uit om taakkoppelingen toe te voegen tijdens het maken van een taak.

1. Selecteer **Bewerken** op het sneltabblad **Taken** van een bestaande takenlijst.
1. Selecteer in het veld **Taakkoppeling** van het dialoogvenster **Taak bewerken** een of meer van de volgende opties:

    - Selecteer **Menuopdracht** om een bewerking in de back-office te configureren, zoals 'Productenkits'.
    - Selecteer **POS-bewerking** om een POS-bewerking te configureren, zoals 'Verkooprapporten'.
    - Selecteer **URL** om een absolute URL te configureren.

In de volgende afbeelding ziet u de selectie van taakkoppelingen in het dialoogvenster **Taak bewerken**.

![Taakkoppelingen selecteren in het dialoogvenster Taak bewerken.](media/HQ-POS-Tasks-Linking.png)

### <a name="configure-a-pos-operation-so-that-it-can-be-linked-to-a-task"></a>Een POS-bewerking zo configureren dat deze aan een taak kan worden gekoppeld

Ga als volgt te werk om een POS-bewerking zodanig te configureren dat deze aan een taak kan worden gekoppeld.

1. Ga naar **Detailhandel en commerce \> Afzetkanaalinstellingen \> POS-instellingen \> POS \> POS-bewerkingen**.
1. Selecteer **Bewerken**, zoek de POS-bewerking en schakel vervolgens het selectievakje **Taakbeheer inschakelen** in.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van taakbeheer](task-mgmt-overview.md)

[Taakbeheer configureren](task-mgmt-configure.md)

[Takenlijsten toewijzen aan winkels of werknemers](task-mgmt-assign-lists.md)

[Taakbeheer in POS](task-mgmt-POS.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
