---
title: Een parallelle activiteit in een workflow configureren
description: Voer de volgende procedures uit in de workfloweditor om een parallelle activiteit te configureren.
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ce3fca9d2dbca046232365b1375bfd920d5b10fd
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Een parallelle activiteit in een workflow configureren

[!include[banner](../includes/banner.md)]


Voer de volgende procedures uit in de workfloweditor om een parallelle activiteit te configureren.

Een parallelle activiteit bestaat uit workflowvertakkingen die op hetzelfde moment worden uitgevoerd.

## <a name="name-a-parallel-activity"></a>Een parallelle activiteit een naam geven
Voer deze stappen uit om een naam op te geven voor een parallelle activiteit.
1.  Klik met de rechtermuisknop op de parallelle activiteit en klik op **Eigenschappen** om het formulier **Eigenschappen** te openen.
2.  Klik in het linkerdeelvenster op **Basisinstellingen**.
3.  Voer in het veld **Naam** een unieke naam voor de parallelle activiteit in.
4.  Klik op **Sluiten**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>De takken van een parallelle activiteit configureren
Voer deze stappen uit om de vertakkingen van deze parallelle activiteit toe te voegen en te configureren.
1.  Dubbelklik op de parallelle activiteit om de vertakkingen van de parallelle activiteit weer te geven.
2.  Om een vertakking toe te voegen, sleept u het element **Vertakking**van het gebied **Workflowelementen** naar een invoegpunt op het tekenpapier. De volgende afbeelding geeft een invoegpunt weer.![Invoegpunt](./media/workflow_insertionpoint.gif)
    | **Opmerking**                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | De volgorde van de vertakkingen is niet belangrijk, omdat alle vertakkingen van een parallelle activiteit op hetzelfde moment worden uitgevoerd. |

3.  Zie voor configureren van elke vertakking [Een parallelle vertakking configureren](configure-parallel-branch-workflow.md).






