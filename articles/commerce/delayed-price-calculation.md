---
title: Exacte prijs- en kortingsberekening uitstellen voor betere prestaties
description: In dit onderwerp wordt de functionaliteit voor uitgestelde prijsberekening beschreven die beschikbaar is in het Microsoft Dynamics 365 Commerce POS (Point of Sale) en callcenter.
author: boycezhu
ms.date: 09/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 8c4264c3a4c71e6aab0e1ef8d7d8cfffad065a46
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488358"
---
# <a name="delay-exact-price-and-discount-calculation-for-improved-performance"></a>Exacte prijs- en kortingsberekening uitstellen voor betere prestaties

[!include [banner](includes/banner.md)]

In dit onderwerp wordt de functionaliteit voor uitgestelde prijsberekening beschreven die beschikbaar is in het Microsoft Dynamics 365 Commerce POS (Point of Sale) en callcenter.

Dynamics 365 Commerce ondersteunt het maken van meerregelkortingen die worden toegepast wanneer meerdere verkoopregels van een verkooporder of verkoopofferte worden gecombineerd. Deze kortingen omvatten combinatiekortingen, drempelkortingen en hoeveelheidskortingen.

Elke keer dat er een nieuwe regel aan een order wordt toegevoegd, beoordeelt de Commerce-prijsengine de hele winkelwagen om te bepalen of een van deze meerregelkortingen kan worden toegepast. Door deze herberekening kan de toevoeging van nieuwe regels invloed hebben op de prestaties wanneer een verkooporder groter wordt.

Maar B2B-bedrijven (business-to-business) en sommige B2C-bedrijven (business--customer) hebben vaak grote ordergrootten. Het kan dus veel tijd kosten om te wachten tot de prijsengine alles opnieuw heeft berekend na elk artikel dat aan de winkelwagen wordt toegevoegd. Bovendien is het voor grote orders gewoonlijk niet erg belangrijk dat de exacte prijs en korting elke keer worden weergegeven wanneer een artikel aan de winkelwagen wordt toegevoegd. Het is belangrijker dat gebruikers artikelen snel kunnen toevoegen. De mogelijkheid om de exacte prijs- en kortingsberekening pas te tonen als een gebruiker hierom vraagt of als een order is afgerond, kan de prestaties aanzienlijk verbeteren. Het kan ook de tijd korter maken die nodig is om een order te voltooien.

Het uitstellen van een exacte prijs- en kortingsberekening is al lange tijd beschikbaar in POS. Vanaf de release Commerce versie 10.0.22 is het ook beschikbaar voor callcenter.

## <a name="enable-delayed-price-and-discount-calculation-for-pos"></a>Uitgestelde prijs- en kortingsberekening inschakelen voor POS

Voer de volgende stappen uit om uitgestelde prijs- en kortingsberekening in te schakelen voor POS.

1. Ga in Commerce Headquarters naar het functionaliteitsprofiel dat aan de fysieke winkel is gekoppeld.
1. Schakel op het sneltabblad **Bedrag** de configuratie **Handmatig meerdere artikelkortingen berekenen** in.
1. De ontwerper van de schermindeling openen voor de kassa's waarvoor de vertraagde berekening moet worden ingeschakeld.
1. Voeg een knop toe voor de bewerking **Totaal berekenen** aan het gewenste knoppenraster.
1. Voer de taken **1070** en **1090** uit.

Wanneer artikelen aan een transactie worden toegevoegd, worden meerregelkortingen pas berekend als de kassier de knop **Totaal berekenen** selecteert. Nadat **Totaal berekenen** is geselecteerd voor een transactie, worden meerregelkortingen altijd berekend voor die transactie. De kassamedewerker hoeft de knop niet opnieuw te selecteren, ook niet als er extra artikelen aan de winkelwagen worden toegevoegd. De kassamedewerker kan betalingen pas vastleggen als **Totaal berekenen** is geselecteerd.

## <a name="enable-delayed-price-and-discount-calculation-for-call-center"></a>Uitgestelde prijs- en kortingsberekening inschakelen voor callcenter

Voer de volgende stappen uit om uitgestelde prijs- en kortingsberekening in te schakelen voor callcenter.

1. Ga in Commerce Headquarters naar **Werkruimtes \> Functiebeheer**.
1. Schakel de functie **Onbedoelde prijsberekening voor commerce-orders voorkomen** in. Deze functie is een vereiste voor het uitgesteld berekenen van prijzen en kortingen.

    > [!NOTE]
    > Voor nieuwe implementaties is de functie **Onbedoelde prijsberekening voor commerceorders voorkomen** standaard ingeschakeld.

1. Ga naar **Commerce-parameters \> Prijzen en kortingen**.
1. Schakel in het gedeelte **Divers** de configuratie **Meerregelprijzen en kortingen handmatig berekenen** in.

Als er nu een verkooporder of verkoopofferte wordt gemaakt of bewerkt in het callcenter, wordt de berekening van de exacte prijs en kortingen ervoor uitgesteld. Bij de prijsbepaling wordt alleen rekening gehouden met de verkoopregel die wordt toegevoegd of bewerkt. Alle andere verkoopregels worden genegeerd. Het nettobedrag voor een artikel bevat de prijsberekening en eenvoudige kortingen (kortingspercentage of kortingsbedrag op een afzonderlijk artikel). Combinatiekortingen, drempelkortingen en hoeveelheidskortingen worden echter niet toegepast. Gebruikers van callcenters die de exacte prijs inclusief alle kortingen willen bekijken, kunnen een van de drie knoppen selecteren: **Herberekenen**, **Totalen** of **Voltooien**.

> [!NOTE]
> Voor callcenterorders verschijnt er een waarschuwing die de gebruiker eraan herinnert dat deze de knop **Herberekenen**, **Totalen** of **Voltooien** moet selecteren om de berekening van de exacte prijs en kortingen uit te voeren. Voor orders waarbij de knop **Voltooien** beschikbaar is, kan de callcentergebruiker op geen enkele manier de exacte prijs- en kortingsberekening weglaten, omdat deze de optie **Voltooien** moet selecteren om de order vast te leggen. Voor orders waarbij de knop **Voltooien** niet beschikbaar is, is er geen actie waarmee de voltooiing van de order wordt aangegeven. De callcentergebruiker moet dus zelf de knop **Herberekenen** of **Totalen** selecteren voordat deze het vastleggen van de order afsluit.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
