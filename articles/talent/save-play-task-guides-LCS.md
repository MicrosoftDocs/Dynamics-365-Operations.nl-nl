---
title: Taakbegeleiders opslaan in LCS en opnieuw afspelen
description: In dit onderwerp wordt uitgelegd hoe u taakbegeleiders opslaat in Microsoft Dynamics Lifecycle Services (LCS) en ze vervolgens opnieuw afspeelt.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 40b4c3154a04a557b8a670e1f1ae3722c71122fe
ms.contentlocale: nl-nl
ms.lasthandoff: 12/04/2018

---

# <a name="save-task-guides-to-lcs-and-replay-them"></a>Taakbegeleiders opslaan in LCS en opnieuw afspelen

[!include [banner](includes/banner.md)]

**Omgevingsdetails** 

Microsoft Dynamics 365 for Talent, dat is geïmplementeerd via Microsoft Dynamics Lifecycle Services (LCS)

**Probleem**

De klant wil nieuwe taakregistraties in zijn of haar LCS-project opslaan en de opgeslagen taakbegeleiders vervolgens opnieuw afspelen.

**Resolutie**

Ga als volgt te werk om een taakregistratie in LCS op te slaan.

1. Meld u aan bij LCS en selecteer het project.
2. Selecteer de tegel **Modelleertool bedrijfsprocessen**.
3. Geef de pagina weer in de bijgewerkte BPM-ervaring.
4. Selecteer een bibliotheek en selecteer **Kopiëren**.
5. Voer een naam in voor het model van de modelleertool voor bedrijfsprocessen.
6. Meld u vanuit LCS aan bij Talent.
7. Voer in het veld **Zoeken** het woord **help** in. De Help van Lifecycle Services wordt geopend.
8. Selecteer de knop **Vernieuwen** voor Help-configuratie van Lifecycle Services.

    Uw nieuwe BPM-bibliotheek wordt weergegeven en is actief.

9. Sluit de pagina.
10. Maak een taakregistratie.
11. Wanneer u klaar bent, selecteert u **Opslaan in Lifecycle Services**.

    ![Opslaan in Lifecycle Services](media/task-guides.png)

12. Selecteer de BPM-bibliotheek en het knooppunt waarin u de taakregistratie wilt opslaan.

Ga als volgt te werk om een taakbegeleider opnieuw af te spelen vanuit LCS.

1. Start Taakregistratie.
2. Selecteer **Openen vanuit LCS**.
3. Selecteer de bibliotheek en het BPM-knooppunt met de opgeslagen taakbegeleider.
4. Open de taakbegeleider.

