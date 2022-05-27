---
title: Taakbegeleiders opslaan in LCS en opnieuw afspelen
description: In dit onderwerp wordt uitgelegd hoe u taakbegeleidingen opslaat in Microsoft Dynamics Lifecycle Services (LCS) en ze vervolgens opnieuw afspeelt.
author: twheeloc
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1147189d1a7668219b5611744483caba0ccac8e
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692333"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Taakbegeleiders opslaan in LCS en opnieuw afspelen


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Omgevingsdetails** 

Microsoft Dynamics 365 Human Resources is geïmplementeerd via Microsoft Dynamics Lifecycle Services (LCS)

**Uitgeven**

De klant wil nieuwe taakregistraties in het LCS-project opslaan en de opgeslagen taakbegeleiders vervolgens opnieuw afspelen.

**Oplossing**

Ga als volgt te werk om een taakregistratie in LCS op te slaan.

1. Meld u aan bij LCS en selecteer het project.
2. Selecteer de tegel **Modelleertool bedrijfsprocessen**.
3. Geef de pagina weer in de bijgewerkte BPM-ervaring.
4. Selecteer een bibliotheek en selecteer **Kopiëren**.
5. Voer een naam in voor het model van de modelleertool voor bedrijfsprocessen.
6. Meld u aan bij Human resources vanuit LCS.
7. Voer in het veld **Zoeken** het woord **help** in. De Help van Lifecycle Services wordt geopend.
8. Selecteer de knop **Vernieuwen** voor Help-configuratie van Lifecycle Services.

    Uw nieuwe BPM-bibliotheek wordt weergegeven en is actief.

9. Sluit de pagina.
10. Maak een taakregistratie.
11. Wanneer u klaar bent, selecteert u **Opslaan in Lifecycle Services**.

    ![Opslaan in Lifecycle Services.](media/task-guides.png)

12. Selecteer de BPM-bibliotheek en het knooppunt waarin u de taakregistratie wilt opslaan.

Ga als volgt te werk om een taakbegeleider opnieuw af te spelen vanuit LCS.

1. Start Taakregistratie.
2. Selecteer **Openen vanuit LCS**.
3. Selecteer de bibliotheek en het BPM-knooppunt met de opgeslagen taakbegeleider.
4. Open de taakbegeleider.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
