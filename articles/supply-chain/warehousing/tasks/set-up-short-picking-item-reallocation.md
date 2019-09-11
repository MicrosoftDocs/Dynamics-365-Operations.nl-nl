---
title: Artikelhertoewijzing voor kort orderverzamelen instellen
description: Deze procedure laat zien hoe magazijnmedewerkers snel andere locaties kunnen vinden als er onvoldoende voorraad is voor de locatie waaraan ze zijn toegewezen.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 964302cb7e7835b6e619602ac7165c9e7adbcefb
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916749"
---
# <a name="set-up-short-picking-item-reallocation"></a>Artikelhertoewijzing voor kort orderverzamelen instellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe magazijnmedewerkers snel andere locaties kunnen vinden als er onvoldoende voorraad is voor de locatie waaraan ze zijn toegewezen. Het is mogelijk om een automatisch hertoewijzingsproces te gebruiken, dat locatierichtlijnen gebruikt voor het ophalen van de goederen als ze op een andere locatie beschikbaar zijn. Ook kan wanneer handmatige hertoewijzing wordt gebruikt, op het mobiele apparaat een lijst met locaties worden weergegeven met de beschikbare hoeveelheid, zodat de magazijnwerknemer de locatie kan kiezen waaruit de voorraad wordt gebruikt. U kunt deze procedure gebruiken in het demobedrijf USMF. Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.


## <a name="set-up-work-exceptions"></a>Werkuitzonderingen instellen
1. Ga in het **navigatievenster** naar **Magazijnbeheer > Instellingen > Werk >Werkuitzonderingen**.
2. Klik op **Nieuw**. Het is mogelijk om meerdere werkuitzonderingen te definiëren met verschillende beleidsregels voor artikelhertoewijzing zodat de magazijnwerknemer één regel kan kiezen op basis van de vereisten van de zending die wordt verwerkt.  
3. Typ een waarde in het veld **Werkuitzonderingscode**. Geef de werkuitzondering een titel om aan te geven waarvoor deze wordt gebruikt. Bijvoorbeeld Handmatige orderverzameling.  
4. Typ een waarde in het veld **Beschrijving**.
5. Selecteer Korte verzameling in het veld **Type uitzondering**.
6. Schakel het selectievakje **Voorraad aanpassen** in. Deze optie betekent dat de voorraad automatisch tot 0 wordt aangepast op de locatie voor orderverzameling.  
7. Typ of selecteer een waarde in het veld **Standaard correctietypecode**. Selecteer in USMF bijvoorbeeld Res Adj Out verwijderen.  
8. Selecteer Handmatig in het veld **Artikelhertoewijzing**. Als u Handmatig of Automatisch en handmatig selecteert, moet de magazijnwerknemer in staat zijn om handmatige hertoewijzing te gebruiken.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Een werknemer instellen om handmatige artikelhertoewijzing te gebruiken
1. Sluit de pagina.
2. Ga in het **navigatievenster** naar **Magazijnbeheer > Instellingen > Medewerker**.
3. Klik op **Bewerken**.
4. Selecteer medewerker 24 in de lijst.
5. Vouw het sneltabblad **Werk** uit.
6. Selecteer Ja in het veld **Handmatige artikelhertoewijzing toestaan**.

