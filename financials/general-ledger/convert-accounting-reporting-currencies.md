---
title: Valuta voor boekhouding of aangiftevaluta converteren
description: 
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 78223
ms.assetid: 31c56f9a-9c64-40a2-90e3-1969a760614b
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: c4f5dae90c5fcaaa52a7087d7c20b2de343b7da0
ms.openlocfilehash: c738207f3088da151ec2317ce2b445f83278ec79
ms.contentlocale: nl-nl
ms.lasthandoff: 08/01/2017

---

# <a name="convert-accounting-or-reporting-currencies"></a>Valuta voor boekhouding of aangiftevaluta converteren

[!include[banner](../includes/banner.md)]


Een bedrijf dat zijn valuta voor boekhouding of aangiftevaluta moet wijzigen heeft twee opties. De eerste optie is een nieuw bedrijf te maken en van voren af aan te beginnen. De tweede optie is het conversieproces voor de valuta voor boekhouding en aangiftevaluta uit te voeren. Dit is een zeer langdurig proces dat elke transactie in het systeem verandert. Er kunnen ook instellingen vereist zijn voordat het proces kan worden uitgevoerd.

## <a name="preparing-the-legal-entity-for-currency-conversion"></a>De rechtspersoon voorbereiden op een valutaomrekening
Voordat u de valuta van de rechtspersoon kunt converteren, moet u alle herwaarderingsbedragen van vreemde valuta voor klant- en leveranciersrekeningen terugdraaien en vorige boekjaren afsluiten. U moet ook de database voor de conversie voorbereiden en de vereiste wijzigingen aanbrengen aan de rekening van de rechtspersoon die de valutaconversie ondergaat. Nadat u een valutaomrekening hebt voltooid, moet u enkele aanvullende procedures uitvoeren. U moet afrondingsverschillen in geconverteerde bedragen afstemmen, bedrijfsstatistieken opnieuw berekenen, de grootboektransacties journaliseren, toegang tot de omrekeningsfunctie beperken, en bedragen in vreemde valuta herwaarderen voor klant- en leveranciersrekeningen.

## <a name="setting-up-accounts-for-automatic-transactions"></a>Rekeningen voor automatische transacties instellen
Tijdens het valutaomrekeningsproces worden winst of verlies of afrondingsverschillen naar de rekeningen geboekt die op de pagina **Rekeningen voor automatische transacties** zijn gedefinieerd. De hoofdrekeningen moeten aan de volgende typen transacties worden toegewezen voordat het conversieproces wordt uitgevoerd:

-   Omrekeningswinst in valuta voor boekhouding
-   Omrekeningsverlies in valuta voor boekhouding
-   Afronding in valuta voor boekhouding
-   Afronding in aangiftevaluta
-   Resultaat per jaareinde

## <a name="posting-rounding-differences-and-sum-recalculations"></a>Afrondingsverschillen boeken en het totaal herberekenen
Met de volgende informatie wordt uitgelegd waar afrondingsverschillen kunnen optreden:

-   Als productprijzen zijn omgerekend naar 0 (nul), wordt er een rapport gegenereerd met vermelding van het productnummer, het moduletype, de prijs die gold voor de omrekening, en de eenheid.
-   Afrondingsverschillen tussen btw en het grootboek worden naar het algemene journaal geboekt.
-   Herwaarderingsbedragen van vreemde valuta worden herberekend en bedragen van klant- en leverancierstransacties worden herberekend.
-   Voor elke klant- en leveranciertransactie worden klant- en leveranciervereffeningsrecords gemaakt voor afrondingsverschillen.
-   Afrondingsverschillen voor klanten en leveranciers worden naar het algemene journaal geboekt.
-   Vereffende kostenbedragen en de vereffende correcties van de kostenbedragen in de afgesloten voorraadtransacties worden opnieuw berekend.
-   Afrondingsverschillen in Voorraadbeheer worden naar het algemene journaal geboekt.
-   Voorhanden voorraad wordt opnieuw berekend.
-   Totaalbedragen in de grootboekjournalen worden opnieuw berekend.
-   Grootboekafsluitwerkbladen worden opnieuw berekend.
-   Grootboeksaldi worden opnieuw berekend.
-   Afrondingsverschillen in Grootboek worden naar het algemene journaal geboekt.
-   Openingsgrootboektransacties worden opnieuw berekend.
-   Het uiteindelijke bedrag in de grootboeksaldi wordt berekend.

Als u converteert naar een nieuwe boekhoudingsvaluta voor het grootboek en er een fout optreedt tijdens de herberekening van totaalbedragen of de boeking van afrondingsverschillen, moet u de pagina **Valutaconversie grootboekrekening** sluiten. De totaalbedragen worden dan opnieuw berekend en de afrondingsverschillen worden geboekt.

## <a name="processing-the-currency-conversion"></a>De valutaomrekening verwerken
Wanneer u het valutaconversieproces start, wordt alle gebruikers gevraagd zich af te melden. U moet de nieuwe grootboek- of aangiftevaluta en wisselkoersen bepalen. Wanneer u klikt op **OK**, wordt het proces uitgevoerd en wordt elke transactie in het systeem bijgewerkt. De valutaomrekening is een zeer lang proces. Wanneer deze is voltooid, kunt u zien dat de boekhoudings- of aangiftevaluta is bijgewerkt op de pagina **Grootboek**.

## <a name="completing-the-currency-conversion"></a>De valutaomrekening voltooien
Na de valutaomrekening, moet u alle afstemmingsrapporten opnieuw genereren om er zeker van te zijn dat alle omgerekende bedragen correct zijn.

-   Wanneer er bij de omrekening van de boekhoudingsvaluta verschillen in de afronding zijn ontstaan, worden deze verschillen niet geboekt met het boekstuk waar die verschillen zich hebben voorgedaan. Zij worden in plaats daarvan geboekt met het boekstuk dat is ingevoerd voor de omrekeningsboekingen. Na de omrekening bevatten alle rapporten die op boekstuk en datum controleren, deze afrondingsverschillen. Dit gedrag is correct en kan worden genegeerd.
-   Als de klant- en leveranciersafstemmingsrapporten een ander bedrag op de totaalregel weergeven en er geen verschilbedrag bestond voor de conversie, moet dit verschilbedrag worden geboekt. De rekening is de totaalrekening voor klanten en leverancier. De tegenrekening is de grootboekrekening voor omrekeningswinst of -verlies.

Wanneer alle grootboektransactiejournalen zijn verwijderd, kunt u de grootboektransacties journaliseren. Klik op **Grootboek** &gt; **Periodiek** &gt; **Journalen** &gt; **Journalisering**. U kunt bedragen in vreemde valuta herwaarderen na de valutaomrekening, als de herwaardering is vereist. U herwaardeert bedragen in vreemde valuta door **Standaard** in het veld **Methode** voor de herwaardering te selecteren.

Zie voor meer informatie [Geboekte journaalposten journaliseren](tasks/journalize-posted-journal-entries.md).


