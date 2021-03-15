---
title: Workbench voor ladingopbouw
description: In dit onderwerp wordt beschreven hoe u werkt met de workbench voor ladingopbouw.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1ed91adba5c7accf9a18d7a754d33b2b35b848f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974217"
---
# <a name="load-building-workbench"></a>Workbench voor ladingopbouw

Met de workbench voor ladingopbouw kunt u strategieën voor ladingopbouw toepassen wanneer u ladingen maakt.

## <a name="create-a-load-building-strategy"></a>Een strategie voor ladingopbouw maken

U gebruikt strategieën voor ladingopbouw om automatisch ladingen op te bouwen. Deze mogelijkheid kan nuttig zijn in de volgende situaties:

- Als u regelmatig een specifieke set producten verzendt, helpen laadstrategieën tijd te besparen, omdat u niet elke keer dezelfde lading hoeft op te bouwen.
- Als u half volle ladingen wilt vermijden om de efficiëntie te maximaliseren, kunnen laadstrategieën helpen elke lading zo veel mogelijk te vullen.

Een klasse voor een strategie voor ladingopbouw met de naam `TMSLoadBuildingVolumeStrategy` biedt een strategie voor ladingopbouw die *de op volume gebaseerde ladingopbouwstrategie* wordt genoemd. Met deze strategie kunt u de maximumwaarden gebruiken die worden opgegeven voor hoogte en gewicht in de ladingsjabloon. U kunt ook de instellingen overschrijven door nieuwe waarden in te voeren. Deze strategie is de enige strategie die kant en klaar wordt meegeleverd. (Misschien hebt u wel een aantal aangepaste strategieën.)

Als u de kant-en-klare *op volume gebaseerde ladingopbouwstrategie* wilt gebruiken, selecteert u deze strategie in het veld **Ladingopbouwstrategie** op de pagina **Workbench voor ladingopbouw** (**Transportbeheer &gt; Planning &gt; Workbench voor ladingopbouw**).

Volg deze stappen om een ladingopbouwstrategie te maken.

1. Ga naar **Transportbeheer &gt; Instellen &gt; Lading opbouwen &gt; Ladingopbouwstrategieën**.
1. Selecteer in het actievenster de optie **Lijst met klassen genereren** om er zeker van te zijn dat u beschikt over de meest recente versies van alle beschikbare klassen.
1. Selecteer **Nieuw** in het actievenster.
1. Voer een unieke naam in voor de strategie, selecteer de klasse voor de strategie voor ladingopbouw en voer een omschrijving in.
1. Selecteer **Opslaan** in het actievenster.
1. Selecteer **Parameters** in het actievenster.
1. Selecteer op de pagina **De parameters van de belastingsbouwstrategie** de optie **Volumecapaciteit** in de lijst en voer vervolgens in het veld **Waarde** het percentage van de totale volumecapaciteit van de lading in dat moet worden toegepast voor de nieuwe strategie voor ladingopbouw.
1. Selecteer **Gewichtcapaciteit** in de lijst en voer vervolgens in het veld **Waarde** het percentage van de totale gewichtcapaciteit van de lading in dat moet worden toegepast voor de nieuwe strategie voor ladingopbouw.
1. Sluit de pagina **De parameters van de belastingsbouwstrategie**.
1. Sluit de pagina **Ladingopbouwstrategieën**.

U kunt nu de ladingopbouwstrategie toewijzen aan een sjabloon voor ladingopbouw. U kunt deze ook rechtstreeks gebruiken in de workbench voor ladingplanning.

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a>Een strategie voor ladingopbouw gebruiken in de workbench voor ladingopbouw

1. Ga naar **Transportbeheer &gt; Planning &gt; Workbench voor ladingopbouw**.
1. Volg één van deze stappen:

    - Selecteer een strategie in het veld **Strategie voor ladingopbouw**.
    - Als u een sjabloon voor ladingopbouw hebt gedefinieerd en hieraan de strategie voor ladingopbouw hebt toegewezen, selecteert u in het actievenster op het tabblad **Sjablonen beheren** de optie **Sjabloon toepassen**. Selecteer vervolgens in het dialoogvenster met vervolgkeuzemenu **Sjabloon voor ladingopbouw toepassen** een sjabloon in het veld **Naam van ladingopbouwsjabloon**.

1. Selecteer in het sneltabblad **Volgorde laadsjablonen** een of meer [laadsjablonen](load-template.md). De workbench zal de lading proberen in te passen in deze typen containers, in de hier opgegeven volgorde. Normaal gesproken moet u de kleinste containers boven aan de lijst plaatsen, zodat u zeker weet dat de kleinst mogelijke container als eerste wordt geselecteerd.
1. Selecteer **Ladingen voorstellen** in het actievenster.
1. Controleer de voorgestelde ladingen en de voorgestelde ladingsregels.
1. Selecteer in het actievenster de optie **Ladingen maken** om ladingen te maken die zijn gebaseerd op de brondocumentregels op het sneltabblad **Voorgestelde ladingregels**.
1. Sluit de pagina **Workbench voor ladingopbouw**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]