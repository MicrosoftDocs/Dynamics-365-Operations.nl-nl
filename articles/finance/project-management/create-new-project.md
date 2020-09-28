---
title: Een nieuw project maken
description: Dit onderwerp biedt informatie over het maken van een nieuw project.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760513"
---
# <a name="create-a-new-project"></a>Een nieuw project maken

[!include [banner](../includes/banner.md)]

Voer de volgende stappen uit om een nieuw project te maken.

1. Selecteer op de pagina **Projectbeheer** de optie **Nieuw project** en voer de volgende waarden in:

    - **Projecttype:** Tijd en materiaal
    - **Projectnaam:** Xyz-upgrade fase 2
    - **Projectgroep:** TM\_WIP
    - **Projectcontract-id:** 00000002

2. Selecteer **Project maken**.

## <a name="assign-a-resource-to-a-project"></a>Een resource toewijzen aan een project

1. Selecteer op de pagina **Werknemers** in de lijst **Werknemers** de record van de werknemer waarvoor u eerder competenties hebt geconfigureerd. Open vervolgens de werknemerrecord.
2. Selecteer in het actievenster op het tabblad **Project** in de groep **Instellingen** de optie **Projecten toewijzen**.
3. Filter op de pagina **Projecttoewijzingen voor resourcevalidatie** op het tabblad **Projecten** het veld **Het project toevoegen aan geselecteerde projecten** op het project **XYZ-upgrade Fase 2**.
4. Selecteer een project in het deelvenster **Resterende projecten** en selecteer de pijlknop om het toe te voegen aan het deelvenster **Geselecteerde projecten**.

Indien nodig kunt u ook categorieën aan een resource toewijzen. Het categorietype is **Kosten** of **Opbrengst**. Uw organisatie bepaalt het categorietype. Als er geen categorieën zijn toegewezen voor een resource, wordt in Finance de standaardcategorie voor uurtarieven voor kosten en opbrengsten opgezocht.

## <a name="set-up-project-resource-and-role-characteristics"></a>Kenmerken voor projectresource en rollen configureren

Een projectmanager kan de resourcingfunctionaliteit van het project gebruiken om de rollen te maken die het project vereist. Rollen kunnen worden gebruikt als tijdens het reserveren van resources nog geen bevestigde resources bekend zijn. Met rollen kunt u resources tijdelijk reserveren als gepland, zodat u de projectplanningsfasen kunt voortzetten.

[![Voorbeeld van een rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso is aangezocht om een project van het type Tijd en materiaal uit te voeren, dat een goedgekeurd projectcharter heeft. De juniorprojectmanager is nog bezig de reikwijdte van het project te bepalen. De resourcemanager identificeert momenteel specifieke resources die worden gereserveerd om aan het nieuwe project te werken. Vanwege de kritieke aard van het project heeft de projectsponsor om de senior projectmanager gevraagd als een van de rollen. De resourcemanager moet de nieuwe resource verkrijgen en de rol in het systeem definiëren, voor het geval de junior projectmanager de resourcegegevens tijdens de projectplanning nodig heeft.

De volgende stappen geven weer hoe de resourcemanager rol Senior projectmanager kan configureren en er resourcekenmerken aan kan toewijzen. Later kan de worden gebruikt om te zoeken naar beschikbare resources die voldoen aan de vereiste resourcecompetenties.

1. Selecteer op de pagina **Rollen instellen** de optie **Nieuw** en voer de volgende waarden in:

    - **Rol-ID:** Senior projectmanager
    - **Beschrijving:** Senior projectmanager

2. Selecteer **Maken**.
3. Selecteer de rol **Senior projectmanager** en selecteer **Kenmerken configureren**.
4. Selecteer in het veld **Type kenmerk** de waarde **Vaardigheid**.
5. Voer in het veld **Beschikbare kenmerken** de vaardigheid in waarnaar u zoekt.
6. Selecteer in het veld **Type kenmerk** de waarde **Getuigschrift**.
7. Voer in het veld **Beschikbare kenmerken** het type getuigschrift in waarnaar u zoekt.

## <a name="assign-a-project-resource-to-a-project"></a>Een projectresource toewijzen aan een project

1. Op de pagina **Alle projecten** selecteert u het project **XYZ-upgrade Fase 2**.
2. Selecteer op het tabblad **Projectteam en planning** de optie **Toevoegen**.
3. Selecteer in het veld **Rol** de waarde **Teamlid**.
4. Selecteer **Boeken vanuit kalender**.
5. Selecteer op de pagina **Resourcebeschikbaarheid** de optie **Weergave-instellingen**.
6. Voer op de pagina **Weergave-instellingen aanpassen** de volgende waarden in:

    - **Indeling voor weergave datumbereik:** Dag
    - **Beschikbaarheidsomschrijvingen weergeven:** Ja
    - **Resterende capaciteit weergeven:** Ja

7. Selecteer in de lijst van resources een resource.
8. Selecteer **Vast boek** en **Volledige capaciteit**.

## <a name="assign-a-resource-to-a-default-role"></a>Een resource aan een standaardrol toewijzen

Om project- of resourcemanagers te helpen, kan verder worden ingezoomd op de resources die voor een project kunnen worden gereserveerd. U kunt een standaardrol aan een bestaande resource toewijzen of aan nieuw verworven resource. Toen bijvoorbeeld Daniel werd aangenomen, had hij de ervaring en vaardigheden voor de rol Bedrijfsanalist. De resourcemanager heeft deze rol toegewezen als Daniel's standaardrol. Daartoe heeft de resourcemanager Daniel toegevoegd aan een groep bedrijfsanalisten die beschikbaar zijn voor het werken aan projecten.

Tijdens resourcereservering kunnen de projectmanagers de rolresources filteren die beschikbaar zijn om aan projecten te werken. Ze kunnen deze informatie als een criterium gebruiken wanneer ze de beslissingsanalyse met meerdere criteria uitvoeren tijdens het vervullen van resources. Ze kunnen ook andere resourcekenmerken aan het filter toevoegen, om te zoeken naar resources die bepaalde vaardigheden, opleiding, en ervaring hebben voor een bepaald project.

**Scenario:** Een goedgekeurd project is van start gegaan en de rol Senior projectmanager is gereserveerd als geplande resource tijdens de projectplanningsfase. De resourcemanager heeft nu een resource verworven om de rol van Senior projectmanager te vervullen.

1. Selecteer op de pagina **Resourcelijst** de waarde **Daniel Goldschmidt**.
2. Selecteer op de pagina **Resourcerol** de optie **Nieuw** en voer de volgende waarden in:

    - **Ingangsdatum:** voer de huidige datum in.
    - **Vervaldatum:** voer **Nooit** in.
    - **Rol:** voer **Senior projectmanager** in.

3. Selecteer **Opslaan** en sluit de pagina.
4. Voeg op het tabblad **Competenties** de vaardigheid **Projectbeheer** en het getuigschrift **PMP** toe.
