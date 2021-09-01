---
title: Artikelhertoewijzing voor kort orderverzamelen instellen
description: In dit onderwerp wordt getoond hoe magazijnmedewerkers snel andere locaties kunnen vinden als er onvoldoende voorraad is voor de locatie waarnaar ze zijn gestuurd.
author: ShylaThompson
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84cefe723cff9566ed3004e49f1e829020bc0d416cd0b29258c21222fbeb05ab
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741879"
---
# <a name="set-up-short-picking-item-reallocation"></a>Artikelhertoewijzing voor kort orderverzamelen instellen

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe magazijnmedewerkers snel andere locaties kunnen vinden als er onvoldoende voorraad is voor de locatie waarnaar ze zijn gestuurd. 

Het hertoewijzingsproces wordt geregeld door een **Werkuitzondering** en wordt gebruikt door de magazijn **medewerker.**

Het is mogelijk om automatische of handmatige hertoewijzingsprocessen te gebruiken, of zelfs beide:

- Automatische hertoewijzing: Locatie-instructies wordt gebruikt om te bepalen of de goederen op een andere locatie beschikbaar zijn. Indien mogelijk wordt het werk bijgewerkt en wordt de magazijngebruiker naar de alternatieve locatie geleid.
- Handmatige hertoewijzing: Hiermee kan de magazijngebruiker een of meer locaties met niet-gereserveerde hoeveelheden goederen selecteren. 
- Automatisch en handmatig: Als het systeem geen automatische hertoewijzing kan uitvoeren, en locaties beschikbaar zijn met niet-gereserveerde hoeveelheden, wordt de gebruiker gevraagd een locatie te selecteren.

## <a name="set-up-work-exceptions"></a>Werkuitzonderingen instellen
Het is mogelijk om meerdere werkuitzonderingen te definiëren met verschillende beleidsregels voor artikelhertoewijzing zodat de magazijnwerknemer één regel kan kiezen op basis van de vereisten van de zending die wordt verwerkt.

Voor deze procedure is gebruikgemaakt van het demobedrijf USMF.

1. Ga in het **navigatievenster** naar **Magazijnbeheer > Instellingen > Werk >Werkuitzonderingen**.
2. Klik op **Nieuw** 
3. Typ een waarde in het veld **Werkuitzonderingscode**. Dit wordt de titel van deze uitzondering. Bijvoorbeeld Handmatige orderverzameling.
4. Typ een waarde in het veld **Beschrijving**. Dit is een korte beschrijving van het gebruik van deze uitzondering. Bijvoorbeeld: Kort orderverzamelen - artikel niet beschikbaar.
5. Selecteer in het veld **Type uitzondering** de waarde **Korte verzameling**.
6. Schakel het selectievakje **Voorraad aanpassen** in. Als deze optie is geselecteerd, betekent dit dat de voorraad automatisch tot 0 wordt aangepast op de locatie voor orderverzameling.
7. Typ of selecteer een waarde in het veld **Standaard correctietypecode**. In USMF kunt u bijvoorbeeld de optie **Res Adj Out verwijderen** selecteren. Elke code voor het correctietype bevat vier eigenschappen: naam, beschrijving, naam van voorraadjournaal en **Reserveringen verwijderen**. Als **Reserveringen verwijderen** is ingeschakeld, worden de reserveringen van de kort-verzamelde orderregel verwijderd.  
8. Selecteer in het veld **Artikelhertoewijzing** een waarde, zoals Handmatig. Als u Handmatig of Automatisch en handmatig selecteert, moet de magazijnwerknemer in staat zijn om handmatige hertoewijzing te gebruiken.

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a>Een werknemer instellen om handmatige artikelhertoewijzing te gebruiken

Voor deze procedure is gebruikgemaakt van het demobedrijf USMF.

1. Sluit de pagina.
2. Ga in het **navigatievenster** naar **Magazijnbeheer > Instellingen > Medewerker**.
3. Klik op **Bewerken**.
4. Selecteer een medewerker in de lijst. Bijvoorbeeld Julia Funderburk.
5. Vouw het sneltabblad **Gebruikers** uit.
6. Selecteer in de lijst een **gebruikers-id**. Bijvoorbeeld 24.
7. Vouw het sneltabblad **Werk** uit.
8. Selecteer **Ja** in het veld **Handmatige artikelhertoewijzing toestaan**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]