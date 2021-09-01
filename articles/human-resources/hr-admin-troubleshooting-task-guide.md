---
title: Taakbegeleiders opslaan in LCS en opnieuw afspelen
description: In dit artikel wordt uitgelegd hoe u taakbegeleiders opslaat in Microsoft Dynamics Lifecycle Services (LCS) en ze vervolgens opnieuw afspeelt.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e8cf6338e17c9d4f0f50e5c36291ce4f81800f76951e873f2e0cf435cc3cc97e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6713073"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Taakbegeleiders opslaan in LCS en opnieuw afspelen

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