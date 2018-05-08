--- 
title: Artikelhertoewijzing voor kort orderverzamelen instellen
description: Deze procedure laat zien hoe magazijnmedewerkers snel andere locaties kunnen vinden als er onvoldoende voorraad is voor de locatie waaraan ze zijn toegewezen.
author: YuyuScheller
manager: AnnBe
ms.date: 10/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b67965b6c8641b5d91ab3c5b0a7a7fd28a07cba6
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-short-picking-item-reallocation"></a>Artikelhertoewijzing voor kort orderverzamelen instellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe magazijnmedewerkers snel andere locaties kunnen vinden als er onvoldoende voorraad is voor de locatie waaraan ze zijn toegewezen. Het is mogelijk om een automatisch hertoewijzingsproces te gebruiken, dat locatierichtlijnen gebruikt voor het ophalen van de goederen als ze op een andere locatie beschikbaar zijn. Ook kan wanneer handmatige hertoewijzing wordt gebruikt, op het mobiele apparaat een lijst met locaties worden weergegeven met de beschikbare hoeveelheid, zodat de magazijnwerknemer de locatie kan kiezen waaruit de voorraad wordt gebruikt. U kunt deze procedure gebruiken in het demobedrijf USMF. Deze procedure is voor een functie die in versie 1611 van Dynamics 365 for Operations is toegevoegd.


## <a name="set-up-work-exceptions"></a>Werkuitzonderingen instellen
1. Ga naar Magazijnbeheer > Instellen > Werk > Werkuitzonderingen.
2. Klik op Nieuw.
    * Het is mogelijk om meerdere werkuitzonderingen te definiëren met verschillende beleidsregels voor artikelhertoewijzing zodat de magazijnwerknemer één regel kan kiezen op basis van de vereisten van de zending die wordt verwerkt.  
3. Typ een waarde in het veld Werkuitzonderingscode.
    * Geef de werkuitzondering een titel om aan te geven waarvoor deze wordt gebruikt. Bijvoorbeeld Handmatige orderverzameling.  
4. Typ een waarde in het veld Omschrijving.
5. Selecteer Korte verzameling in het veld Type uitzondering.
6. Schakel het selectievakje Voorraad aanpassen in.
    * Deze optie betekent dat de voorraad automatisch tot 0 wordt aangepast op de locatie voor orderverzameling.  
7. Typ of selecteer een waarde in het veld Standaard correctietypecode.
    * Selecteer in USMF bijvoorbeeld Res Adj Out verwijderen.  
8. Selecteer Handmatig in het veld Artikelhertoewijzing.
    * Als u Handmatig of Automatisch en handmatig selecteert, moet de magazijnwerknemer in staat zijn om handmatige hertoewijzing te gebruiken.  

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Een werknemer instellen om handmatige artikelhertoewijzing te gebruiken
1. Sluit de pagina.
2. Ga naar Magazijnbeheer > Instellen > Medewerker.
3. Klik op Bewerken.
4. Selecteer medewerker 24 in de lijst.
5. Vouw de sectie Werk uit.
6. Selecteer Ja in het veld Handmatige artikelhertoewijzing toestaan.


