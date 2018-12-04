---
title: Waarschuwingsregels maken
description: Dit onderwerp bevat informatie over waarschuwingen en uitleg over het maken van een waarschuwingsregel zodat u een bericht ontvangt over gebeurtenissen zoals een datum of een specifieke wijziging.
author: tjvass
manager: AnnBe
ms.date: 06/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 78e1e6f7be04e1d4fecae080cbd4a285358590fb
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="create-alert-rules"></a>Waarschuwingsregels maken

[!include [banner](../includes/banner.md)]

## <a name="getting-started"></a>Aan de slag
Bepaal voordat u een waarschuwingsregel instelt, wanneer of in welke situaties u waarschuwingen wilt ontvangen. Als u weet over welke gebeurtenis u wilt worden gewaarschuwd, gaat u in Microsoft Dynamics 365 for Finance and Operations naar de pagina met de gegevens die de gebeurtenis veroorzaken. De gebeurtenis kan een datum zijn die aanbreekt of een specifieke wijziging die plaatsvindt. Daarom moet u de pagina vinden waar de datum is gespecificeerd of die het veld bevat dat verandert of de nieuwe record. Wanneer u deze informatie hebt, kunt u de waarschuwingsregel maken.

Wanneer u een waarschuwingsregel maakt, geeft u de criteria op waaraan moet zijn voldaan voordat een waarschuwing wordt geactiveerd. De criteria zijn in feite de overeenkomst tussen het plaatsvinden van een gebeurtenis en het voldoen aan bepaalde voorwaarden. Wanneer er een gebeurtenis plaatsvindt, start het systeem een controle aan de hand van de voorwaarden die in Finance and Operations zijn ingesteld.

## <a name="events"></a>Gebeurtenissen
De gebeurtenis die een waarschuwingsregel activeert kan datum zijn die binnenkomt of een bepaalde wijziging die plaatsvindt. Triggers voor gebeurtenissen worden gedefinieerd op het sneltabblad **Waarschuw mij wanneer** van het dialoogvenster **Waarschuwingsregel maken**. Welke gebeurtenissen beschikbaar zijn voor een bepaald veld, is afhankelijk van de geselecteerde trigger.

Als u bijvoorbeeld een waarschuwingsregel wilt instellen voor het veld **Begindatum**, zijn gebeurtenissen met een vervaldatum geschikt. Daarom is het gebeurtenistype **vervalt in** beschikbaar voor dit veld. Voor een veld zoals **Kostenplaats** is een gebeurtenis met vervaldatum niet geschikt. Daarom is het gebeurtenistype **vervalt in** niet beschikbaar. In plaats daarvan is het gebeurtenistype **gewijzigd in** beschikbaar.

## <a name="event-types"></a>Gebeurtenistypen
Er kunnen drie typen gebeurtenissen optreden:

- **Gebeurtenissen voor maken en gebeurtenissen voor verwijderen**: deze gebeurtenissen activeren een waarschuwing wanneer een record wordt gemaakt of verwijderd.
- **Gebeurtenissen van het bijwerkingstype**: deze gebeurtenissen activeren een waarschuwing wanneer de gegevens in een bepaald veld worden gewijzigd.
- **Gebeurtenissen van het type vervaldatum**: deze gebeurtenissen activeren een waarschuwing als een datum aanbreekt.
    
Wijzigingen die optreden kunnen worden gestart door een gebruiker. Een gebruiker wijzigt bijvoorbeeld de leveringsdatum van een inkooporder. Wijzigingen kunnen ook optreden als onderdeel van een proces. Bijvoorbeeld, het veld **Status** van een pagina verandert om de levenscyclus van verschillende processen in het systeem te weerspiegelen.

## <a name="conditions"></a>Voorwaarden
Op het sneltabblad **Waarschuw mij voor** van het dialoogvenster **Waarschuwingsregel maken** kunt u voorwaarden gebruiken, om te bepalen wanneer u waarschuwingen over gebeurtenissen ontvangt.

U kunt bijvoorbeeld opgeven dat het systeem u moet waarschuwen als de status van inkooporders wijzigt, maar alleen als de status overeenkomt met een bepaalde set voorwaarden. U wilt bijvoorbeeld worden gewaarschuwd wanneer de status van een inkooporder verandert in **Ontvangen**. Deze wijziging in status is de gebeurtenis die de waarschuwing activeert.

Vervolgens moet u beslissen over welke inkooporders u wilt worden gewaarschuwd. U kunt bijvoorbeeld een van de volgende opties selecteren: Deze opties bepalen de voorwaarden voor de waarschuwingsregel.

- **Huidig geselecteerd record**: u ontvangt een waarschuwing als de status van een bepaalde inkooporder verandert in **Ontvangen**.
- **Alle records**: u ontvangt een waarschuwing wanneer de status van een inkooporder voor een artikel verandert in de weergave van de actieve pagina. Gebruik de geavanceerde filters die beschikbaar zijn op de pagina om regels voor een bepaalde set records te maken. U kunt bijvoorbeeld een waarschuwing maken die wordt geactiveerd voor alle inkooporders voor klanten in een bepaalde klantengroep.
    
## <a name="expiry-of-rule"></a>Verlopen van regel
Geef op het sneltabblad **Waarschuw mij tot** van het dialoogvenster **Waarschuwingsregel maken** op hoe lang de waarschuwingsregel actief moet zijn.

## <a name="alert-contents"></a>Inhoud van waarschuwing
Geef op het sneltabblad **Waarschuw mij met** van het dialoogvenster **Waarschuwingsregel maken** de onderwerptekst en de berichttekst op die in de waarschuwingsberichten wordt gebruikt.

## <a name="user-id"></a>Gebruikers-ID
Geef op het sneltabblad **Waarschuwing voor wie** van het dialoogvenster **Waarschuwingsregel maken** op welke gebruiker de waarschuwingsberichten moet ontvangen. Uw gebruikers-ID is standaard geselecteerd. Deze optie is beperkt tot beheerders van de organisatie.

## <a name="create-an-alert-rule"></a>Een waarschuwingsregel maken
1. Open de pagina met de te controleren gegevens.
2. Selecteer in het Actievenster op het tabblad **Opties** in de groep **Delen** de optie **Een waarschuwingsregel maken**.
3. Selecteer in het dialoogvenster **Waarschuwingsregel maken** in het veld **Veld** het veld dat gecontroleerd moet worden.
4. Selecteer in het veld **Gebeurtenis** het type gebeurtenis.
5. Selecteer een optie op het sneltabblad **Waarschuw mij voor**.
6. Als u wilt dat de waarschuwingsregel op een bepaalde datum inactief wordt, selecteert u een einddatum in het snelttabblad **Waarschuw mij tot**.
7. Accepteer op het sneltabblad **Waarschuw mij met** in het veld **Onderwerp** de standaard onderwerpkoptekst voor het e-mailbericht of voer een nieuw onderwerp in. De tekst wordt gebruikt als de onderwerpkoptekst voor het e-mailbericht dat u ontvangt als er een waarschuwing wordt geactiveerd.
8. Voer desgewenst een bericht in het veld **Bericht** in. De tekst wordt gebruikt als het bericht dat u ontvangt als er een waarschuwing wordt geactiveerd.
9. Selecteer **OK** om de instellingen op te slaan en de waarschuwingsregel te maken.

