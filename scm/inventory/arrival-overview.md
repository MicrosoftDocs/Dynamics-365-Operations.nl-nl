---
title: Overzicht aankomst
description: Dit onderwerp biedt informatie over de functie Overzicht aankomst. De pagina Overzicht aankomst maakt deel uit van deze functie en biedt een overzicht van alle atikelen die naar verwachting zullen arriveren als binnenkomende artikelen.
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSArrivalOverview, WMSArrivalOverviewProfile, WMSJournalTable
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: d6910d3a960c22f8515276ef9a2229957e5d6f11
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="arrival-overview"></a>Overzicht aankomst

[!include[banner](../includes/banner.md)]


Dit onderwerp biedt informatie over de functie Overzicht aankomst. De pagina Overzicht aankomst maakt deel uit van deze functie en biedt een overzicht van alle atikelen die naar verwachting zullen arriveren als binnenkomende artikelen.

De pagian **Overzicht aankomst** bevat een overzicht van alle verwachte binnenkomende artikelen. Hier worden tevens ontvangsten weergegeven die kunnen worden geïnitialiseerd op basis van het overzicht. In dit onderwerp ligt de nadruk op het ontvangstproces.

## <a name="business-scenario"></a>Zakelijke scenario
Neem het volgende scenario in de inkomende processen in overweging. 

[![Zakelijke scenario](./media/arrival-overview-scenario.png)](./media/arrival-overview-scenario.png) 

Sammy, een ontvangstadministrateur, wil weten welke ontvangsten worden verwacht op de huidige dag. Op de pagina **Overzicht aankomst** krijgt Sammy een overzicht van de huidige taken en een ruwe schatting van hoeveelheden, volume, gewicht, verschillende ordertypen enzovoort. Later, komt een levering binnen bij een van de inbound docks aankomt en ontvangt Sammy een lijst met de levering. Op de pagina **Overzicht aankomst** kan Sammy de volgende taken uitvoeren:

-   De overeenkomende ontvangstorder identificeren en de ontvangst registreren als **In uitvoering**. De regels die zijn vereist voor een registratie worden automatisch gegenereerd en de ontvangst kan worden gecontroleerd, zelfs als de transacties nog niet zijn geboekt als **Geregistreerd**.
-   Toegang krijgen tot de juiste verwijzing in het journaal voor artikelontvangst (dat wil zeggen, het journaal **Artikelontvangst** of het journaal **Productie-invoer**) en journalen identificeren die gereed zijn voor het bijwerken van een productontvangstbon.

## <a name="arrival-overview-page"></a>Pagina Overzicht aankomst
U kunt de pagina **Overzicht aankomst** openen door op **Voorraadbeheer** &gt; **Inkomende orders** &gt; **Overzicht aankomst** te klikken. U kunt een lijst bekijken met orders die naar verwachting zullen worden ontvangen. Het overzicht is onderverdeeld in een koptekst en regels. De koptekstgegevens zijn gegroepeerd per ordertype, verwachte ontvangstdatum en plaats van bestemming. Wanneer een koptekstregel wordt geselecteerd voor ontvangst, worden alle detailregels die betrekking hebben op de ontvangstverwijzing geselcteerd voor ontvangst in het gedeelte voor regeldetails van de pagina. Wanneer alle gerelateerde journaalregels zijn geboekt, wordt deze informatie niet weergegeven.

### <a name="arrival-overview-profiles"></a>Aankomstoverzichtsprofielen

De pagina **Overzicht aankomst** bevat een overzicht van artikelen die naar verwachting zullen worden ontvangen en de datum waarop de ontvangst wordt verwacht. Als onderdeel van het ontvangstproces kunnen meerdere sets met persoonlijke instellingen worden gebruikt. Afzonderlijke gebruikers kunnen hun persoonlijke instellingen definiëren op de pagina **Aankomstoverzichtsprofielen**.

### <a name="set-up-item-arrival"></a>Artikelontvangst instellen

In ons voorbeeld wil Sammy een nieuwe computer opzetten op een locatie die zal worden gebruikt voor het ontvangen van eindproducten die afkomstig van de productie op locatie 1. Op de pagina **Aankomstoverzichtsprofielen** maakt Sammy een nieuwe instelling met de naam **Productie Site 1** en geeft deze de volgende instellingen.

1.  Voer op het sneltabblad **Aankomstopties** in de veldgroep **Bereik**, gegevens over een daginterval in en de magazijnen die moeten worden opgenomen in het overzicht.
2.  Voer op het sneltabblad **Aankomstopties** in de veldgroep **Journaal** een magazijn van ontvangst, een locatie en een journaalnaam (artikelontvangst/productie-invoer) in.
3.  Voer op het sneltabblad **Aankomstquerygegevens** in de veldgroep **Vestiging** in het veld **Beperken tot vestiging** een vestiging in om de weergave in het overzichtsgebied te beperken.
4.  Voer op het sneltabblad **Aankomstquerygegevens** in de veldgroep **Getoonde transactietypen** de optie **Productieorders** in op **Ja**.
5.  Stel op het sneltabblad **Aankomstquerygegevens** sneltabblad in de groep **Diversen** de optie **Bijwerken bij opstarten** in op **Ja** als de weergave automatisch moet worden bijgewerkt bij het opstarten. Stel de optie **Bijwerken bij bereikwijziging** in op **Ja** als de weergave automatisch moet worden bijgewerkt wanneer bereikwaarden worden gewijzigd.

In dit voorbeeld is het veld **Naam aankomstoverzichtsprofiel** op het sneltabblad **Aankomstopties** van de pagina **Overzicht aankomst** ingesteld op **Productie Site 1**.

### <a name="prerequisites-for-arrival-journals"></a>Vereisten voor ontvangstjournalen

Als u automatisch ontvangstjournalen wilt maken vanaf de pagina **Overzicht aankomst**, moet u relevante gegevens definiëren in de veldgroep **Journaal** op het sneltabblad **Aankomstopties**.

-   U moet een journaalnaam opgeven om een journaal te maken. 

[![Een journaalnaam opgeven](./media/arrival-overview-journal.png)](./media/arrival-overview-journal.png)

-   Als u waarden opgeeft in de velden **Magazijn** en **Locatie**, worden die waarden toegepast op de journaalregels. Als u geen waarden opgeeft, gebruikt het systeem de waarden van de dimensie die is opgegeven in de voorraadtransacties.

#### <a name="items-that-are-received-from-one-expected-receipt-order"></a>Artikelen die worden ontvangen van één verwachte ontvangstorder

Op het sneltabblad **Ontvangsten** selecteert Sammy een regel en klikt vervolgens op **Begin aankomst**. Alle gerelateerde regels in het opgegeven bereik die een te registeren hoeveelheid hebben worden automatisch geselecteerd. Er wordt een artikelontvangstjournaal gegenereerd met een overeenkomst tussen de verwachte ontvangstorder en het journaal. De hoeveelheid wordt automatisch geïnitialiseerd voor alle regels die zijn gemaakt.

#### <a name="items-that-are-received-from-more-than-one-expected-receipt-order"></a>Artikelen die worden ontvangen van meer dan één verwachte ontvangstorder

Op het sneltabblad **Ontvangsten** selecteert Sammy meerdere regels en klikt vervolgens op **Begin aankomst**. Er wordt een artikelontvangstjournaal gegenereerd met een overeenkomst tussen alle verwachte ontvangstorders en het journaal. Alle regels worden gemaakt onder één koptekst voor artikelontvangstjournaal en de hoeveelheid wordt automatisch geïnitialiseerd.

### <a name="receive-items-from-one-or-more-expected-receipt-orders"></a>Artikelen ontvangen van een of meer verwachte ontvangstorders

#### <a name="view-information"></a>Informatie weergeven

Als Sammy een overzicht van verwachte ontvangsten in een datuminterval wil ontvangen, moet hij de volgende informatie invoeren in de velden op het sneltabblad **Aankomstopties** op de pagina **Overzicht aankomst** en vervolgens op **Bijwerken** klikken om de weergave bij te werken:

-   Naam aankomstoverzichtsprofiel: **Query**
-   Regels tonen: **Alle**
-   Dagen terug: (leeg)
-   Dagen vooruit: **0**
-   Magazijnen: **GW, MW**

Sammy kan de volgende gegevens bekijken:

-   Alle gerelateerde ontvangstorders voor de systeemdatum en een onbeperkt aantal dagen voorafgaand hieraan (het interval **InventTrans.StatusDate**) en ontvangsten voor magazijnen GW en MW, ongeacht de status.
-   Gedetailleerde regelgegevens voor meerdere orders. Sammy kan meerdere koptekstregels in het overzicht selecteren en vervolgens op **Alle geselecteerde tonen** klikken om alle bijbehorende gedetailleerde regelinformatie weer te geven voor alle geselecteerde orders.
-   Informatie over een specifieke inkooporder. Als hij alleen informatie wil weergeven die is gerelateerd aan een specifiek referentienummer in het overzicht, kan Sammy een rekeningnummer opgeven in het veld **Rekeningnummer** en een ordernummer in het veld **Referentienummer**.
-   Een overzicht van de registratietaken die moeten worden uitgevoerd voor alle orderregels waarvoor een artikelontvangstjournaal is gemaakt maar nog niet geboekt. Sammy kan deze informatie bekijken door **In uitvoering** te selecteren in het veld **Regels tonen**.

### <a name="update-journals"></a>Journalen bijwerken

Voor het registreren van een of meer regels die moeten worden verwerkt, kan Sammy de regels in het overzichtsraster of in het raster van de regel selecteren en vervolgens op **Journalen** &gt; **Aankomsten van ontvangsten tonen** klikken. De kopteksten voor artikelontvangst die overeenkomen met de regels worden weergegeven. Als Sammy een update van de productontvangst wilt uitvoeren voor de inkooporder voor de geregistreerde artikelen, kan hij de journaalkopteksten van de artikelontvangst openen die gereed zijn om te worden bijgewerkt. Als hij deze journaalkopteksten van artikelontvangst wil openen, klikt hij op **Journalen** &gt; **Journalen gereed voor productontvangstbon**. Alle koptekstregels die gereed zijn voor het bijwerken van de productontvangstbon in het opgegeven magazijnbereik worden weergegeven. (De koptekstregels die worden weergegeven zijn niet gerelateerd aan het daginterval).

### <a name="start-an-arrival-registration"></a>Een aankomstregistratie starten

Door meerdere regels te selecteren op de pagina **Overzicht aankomst** kan Sammy de ontvangst van meer dan één ontvangstverwijzing starten. Wanneer hij een regel uit het overzicht van ontvangsten selecteert, worden de bijbehorende regeldetails geselecteerd. Als een hoeveelheid voor registratie bestaat, is de knop **Begin aankomst** beschikbaar. Sammy kan twee methoden gebruiken om de aankomstregistratie te starten:

-   Hij kan de pagina filteren zodat alleen records worden weergegeven die voldoen aan bepaalde criteria, kan hij in het veld **Leverancierreferentie** een referentienummer van een leverancier scannen, zoals de streepjescode voor een afleveringsbewijs.
-   Hij kan in het overzichtsgedeelte of het detailgedeelte van de pagina **Overzicht aankomst** handmatig records voor aankomstregistratie selecteren of de selectie hiervan ongedaan maken. Vervolgens worden, als Sammy op **Begin aankomst** klikt, de geselecteerde records automatisch gemaakt in een artikelontvangstjournaal. De records bevatten regelgegevens en alle unieke veldgegevens wordt toegewezen.

## <a name="update-arrival-information-and-process-a-product-receipt"></a>Ontvangstgegevens bijwerken en een productontvangstbon verwerken
Wanneer alle goederen zijn geregistreerd, kan de magazijnbeheerder of inkoopmanager de ontvangen artikelen bijwerken met een productontvangstbon om de fysieke kosten toe te voegen. Ga als volgt te werk om de ontvangstgegevens bij te werken en een productontvangstbon te boeken.

1.  Klik op **Voorraadbeheer** &gt; **Inkomende orders** &gt; **Overzicht aankomst**.
2.  Klik op de pagina **Overzicht aankomst** op **Journalen** &gt; **Journalen gereed voor productontvangstbon** om een lijst weer te geven van de journalen die klaar zijn voor het bijwerken van de productontvangstbon.
3.  Selecteer de journalen die moeten worden bijgewerkt en klik vervolgens op **Functies** &gt; **Productontvangstbon**.
4.  Voer op de pagina **Boeken** het nummer van de productontvangstbon in als dit nog niet beschikbaar is in het journaal en klik vervolgens op **OK** om de productontvangstbon te verwerken.

## <a name="summary"></a>Overzicht
De pagina **Overzicht aankomst** kan de magazijnbeheerder en magazijnmedewerkers helpen een overzicht te krijgen van verwacht werk dat moet worden uitgevoerd als onderdeel van een inkomend proces. De pagina kan ook worden gebruikt om het proces van artikelontvangst te starten en te helpen garanderen dat de artikelen worden bijgehouden bij de eerste invoer in het magazijn.




