---
title: Overzicht van Workflows maken
description: In dit onderwerp wordt uitgelegd hoe u een workflow maakt.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: a643be553f3fcdfbe53f2024982a596e498830a8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811284"
---
# <a name="create-workflows-overview"></a>Overzicht van Workflows maken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een workflow maakt.

## <a name="open-the-workflow-editor"></a>Open de workfloweditor

De module waarin u werkt, bepaalt de typen werkstroom die u kunt maken. Volg deze stappen om het workflowtype te selecteren dat u wilt maken en open de workfloweditor.

1. Open de module waarvoor u een nieuwe workflow wilt maken. Als u bijvoorbeeld een workflow voor opdrachten tot inkoop wilt maken, klikt u op **Inkoopbeheer**.
2. Klik op **Instellen** &gt; **\[Naam van module\] workflows**.
3. Klik op **Nieuw** in de lijstpagina die verschijnt in het actievenster.
4. Selecteer op de pagina **Workflow maken** het type workflow en klik vervolgens op **Workflow maken**. De workfloweditor verschijnt. U kunt nu de volgende procedures gebruiken om de workflow te ontwerpen.

## <a name="drag-workflow-elements-onto-the-canvas"></a>Sleep workflowelementen op het tekenpapier

Het gebied **Workflowelementen** van de workfloweditor bevat de elementen die u aan uw workflow kunt toevoegen. Sleep de elementen die u aan de workflow wilt toevoegen naar het tekenpapier.

## <a name="connect-the-elements"></a>De elementen verbinden

Om het ene workflowelement met het andere te verbinden, houdt u de aanwijzer boven een element tot er verbindingspunten verschijnen. Klik op een verbindingspunt en sleep het naar een ander element. Zorg ervoor dat u alle elementen verbindt.

## <a name="configure-the-properties-of-the-workflow"></a>De eigenschappen van de workflow configureren

Volg deze stappen om de eigenschappen van de workflow te configureren.

1. Klik op het tekenpapier om ervoor te zorgen dat er geen workflowelement is geselecteerd.
2. Klik op **Eigenschappen** om het formulier **Eigenschappen** voor de workflow te openen.
3. Volg de procedures in het onderwerp [Workfloweigenschappen configureren](configure-workflow-properties.md).

## <a name="configure-the-elements-of-the-workflow"></a>De elementen van de workflow configureren

Configureer elk element dat u op het tekenpapier hebt gesleept. Zie de volgende onderwerpen voor meer informatie over het configureren van elk workflowelement:

- [Handmatige taken configureren in een workflow](configure-manual-task-workflow.md)
- [Geautomatiseerde taken configureren in een workflow](configure-automated-task-workflow.md)
- [Goedkeuringsprocessen configureren in een workflow](configure-approval-process-workflow.md)
- [Goedkeuringsstappen configureren in een workflow](configure-approval-step-workflow.md)
- [Handmatige beslissingen configureren in een workflow](configure-manual-decision-workflow.md)
- [Voorwaardelijke beslissingen configureren in een workflow](configure-conditional-decision-workflow.md)
- [Parallelle vertakkingen in een workflow configureren](configure-parallel-activity-workflow.md)
- [Een parallelle vertakking configureren](configure-parallel-branch-workflow.md)
- [Workflows voor regelitems configureren](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a>Eventuele fouten of waarschuwingen oplossen

Het deelvenster **Fouten en waarschuwingen** onderaan in de workfloweditor geeft berichten weer die voor de workflow zijn gegenereerd. Om het element te vinden waar een fout of waarschuwing optreedt, dubbelklikt u op het fout- of waarschuwingsbericht. U moet alle fouten en waarschuwingen oplossen voordat u de workflow kunt activeren.

## <a name="save-and-activate-the-workflow"></a>De workflow opslaan en activeren

Wanneer u klaar bent om de workflow op te slaan en te activeren, volgt u deze stappen.

1. Klik op **Opslaan en sluiten** om de workflow te sluiten en de pagina **Workflow opslaan** te openen.
2. Voer opmerkingen in over de wijzigingen die u in de workflow hebt aangebracht en klik op **OK**.
3. Als alle fouten en waarschuwingen zijn opgelost, verschijnt de pagina **Workflow activeren**. Een van de volgende opties selecteren:

    - Om deze versie van de workflow te activeren, klikt u op **De nieuwe versie activeren**. Wanneer een workflow actief is, kunnen gebruiker documenten ter verwerking bij de workflow aanbieden.
    - Als u deze versie niet wilt activeren, klikt op **De nieuwe versie niet activeren**. U kunt de workflow later activeren.
