---
title: Parallelle activiteiten in een workflow configureren
description: Voer de volgende procedures uit in de workfloweditor om een parallelle activiteit te configureren.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 054d62e2ff094aee987f8c6e04e2f2e173da633d
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068758"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>Parallelle activiteiten in een workflow configureren

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Voer de volgende procedures uit in de workfloweditor om een parallelle activiteit te configureren.

Een parallelle activiteit bestaat uit workflowvertakkingen die op hetzelfde moment worden uitgevoerd.

## <a name="name-a-parallel-activity"></a>Een parallelle activiteit een naam geven

Voer deze stappen uit om een naam op te geven voor een parallelle activiteit.

1. Klik met de rechtermuisknop op de parallelle activiteit en klik op **Eigenschappen** om het formulier **Eigenschappen** te openen.
2. Klik in het linkerdeelvenster op **Basisinstellingen**.
3. Voer in het veld **Naam** een unieke naam voor de parallelle activiteit in.
4. Klik op **Sluiten**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>De takken van een parallelle activiteit configureren

Voer deze stappen uit om de vertakkingen van deze parallelle activiteit toe te voegen en te configureren.

1. Dubbelklik op de parallelle activiteit om de vertakkingen van de parallelle activiteit weer te geven.
2. Om een vertakking toe te voegen, sleept u het element **Vertakking** van het gebied **Workflowelementen** naar een invoegpunt op het tekenpapier. De figuur hieronder geeft een invoegpunt weer.

    ![Invoegpunt.](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > De volgorde van de vertakkingen is niet belangrijk, omdat alle vertakkingen van een parallelle activiteit op hetzelfde moment worden uitgevoerd.

3. Zie [Parallelle vertakkingen in een workflow configureren](configure-parallel-branch-workflow.md) voor configureren van elke vertakking.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]