---
title: Beheer van handelstoeslag
description: In dit onderwerp wordt handelstoelagebeheer beschreven voor Dynamics 365 Supply Chain Management.
author: t-benebo
manager: tfehr
ms.date: 08/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: MCRBrokerClaims, MCRBrokerWriteOffReasonPrompt, MCRRoyaltyVendTable, MCRRoyaltyVendTrans, PdsCustRebateGroup, PdsRebateAgreement, TAMCopyTradePromotions, TAMDeduction, TAMDeductionCreate, TAMDeductionDenyReason, TAMDeductionParmDeny, TAMDeductionParmMassUpdate, TAMDeductionParmMatch, TAMDeductionParmSplit, TAMDeductionParmWriteOff, TAMDeductionType, TAMDeductionWriteOffReason, TAMFundManagement, TAMFundUsage, TAMListPage, TAMMarketingObjective, TAMMerchEventType, TAMOneTimePromotion, TAMPromoCompareGraph, TAMPromoStatistic, TAMPromotionAnalysisSummary, TAMPromotionParameters, TAMPromotionPeriod, TAMTemplateListPage, TAMTradePromotionAnalysis, TAMTradePromotions, TAMWhatIfPromotionAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: b7be74bbd1af4e67facc680edbee3a84470b5ed4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205780"
---
# <a name="trade-allowance-management"></a>Beheer van handelstoeslag

[!include [banner](../includes/banner.md)]

Beheer van handelstoeslag helpt bedrijven verkooppromotieprogramma's te beheren die monetaire vergoedingen in de vorm van 'betalen naar prestaties' bieden aan klanten die doelstellingen op gebied van volume en gedrag halen. De mogelijkheden van de functie zijn ontworpen voor bedrijven die zich op uitgebreide promote-to-profit processen richten, van promotiefondsbudgettering en -toewijzing tot vergoedingencontractinstellingen, maken en verwerken van claims, tot betalingsverwerking, tot analyse van effectiviteit van promotie.


Dit artikel biedt een uitgebreid overzicht van de functie Beheer handelstoeslag en maakt u vertrouwd met de gebruikelijke reeks taken die betrekking hebben op het beheren van een verkooppromotieprogramma. Verschillende typen gebruikers die operationele en besluitvormingsverantwoordelijkheden hebben, zullen deze functionaliteit naar verwachting gebruiken om hun respectieve doelen te bereiken:

- Toewijzing van concrete fondsen aan de geselecteerde rekeningen en handelstoeslagovereenkomsten instellen voor promoties, gebaseerd op terugbetalingen en eenmalige forfaitaire bedragen (voor een overeengekomen service)
- Uitvoering van de overeengekomen promotiecontracten door middel van lopende verkoop en het genereren van terugbetalingsvorderingen
- Berekening, goedkeuring en verwerking van de gegenereerde vorderingen, en doorgifte ervan aan Klanten als inhoudingen voor betalingsvereffening
- Afstemming van de betalingen op korte termijn van de klant met de inhouding die moet worden betaald
- Tracering van gebruik van het promotiefonds en evaluatie van winstgevendheid en effectiviteit van programma

## <a name="audience-and-purpose"></a>Doelgroep en doel

De informatie in dit document is bedoeld voor de besluitvormers in ondernemingen, bijvoorbeeld inkoopmanagers, CFO's (Chief Financial Officer) en accountmanagers, die de volgende verantwoordelijkheden hebben:

- Budgetten op hoog niveau en fondstoewijzing
- Planning en analyse van verkooppromoties
- Beheer van personeel dat terugbetalingsvorderingen verwerkt, betalingen uitvoert op basis van merchandisinggebeurtenissen en betalingen die op korte termijn moeten worden gedaan en inhoudingen vereffent

Personen met deze rollen zijn op zoek naar manieren om deze doelstellingen te halen:

- Een beter gebruik van marketingpromotiefondsen.
- Op flexibele wijze verschillende typen promotieprogramma's en vergoedingen bieden.
- De administratieve last en fouten gerelateerd aan het bewaken van de promotieprestaties en het verwerken van claims verminderen.
- Cashflowprognoses verbeteren door toekomstige schulden toe te rekenen.
- Een gekwantificeerde basis voor lopende en toekomstige onderhandelingen met klanten over promoties hebben.

## <a name="promotional-fund-and-trade-allowance-agreement"></a>Promotiefondsen en handelstoeslagovereenkomst

Een handelstoeslagovereenkomst is een aanmoedigingsprogramma waar monetaire vergoedingen in de vorm van betalen-naar-prestaties worden aangeboden aan klanten die specifieke volumedoelen en/of gedragsdoelstellingen halen. Promotiefondsen zijn gebudgetteerde uitgaven. Op die manier kunnen de promotiecampagnes worden vastgelegd.

### <a name="promotional-fund"></a>Promotiefonds

Fondsen die worden toegewezen aan toeslagovereenkomsten worden vastgelegd op de pagina **Fondsen**. Als u de pagina **Fondsen** wilt openen, selecteert u **Verkoop en marketing** \>**Handelstoeslagen** \> **Fondsen** \> **Fondsen**.

![Fondsenpagina](./media/trade-allowance-management-funds-page.png "Fondsenpagina")

Op de pagina **Fondsen** kunt u de details van promotiefondsen bekijken.

Op het sneltabblad **Algemeen** ziet u de periode waarin het fonds geldig is en het gebudgetteerde bedrag. Voor toewijzing van het fonds aan de promotieovereenkomst moet het veld **Status** de waarde **Goedgekeurd** hebben.

Het sneltabblad **Klanten** bevat de klantenhiërarchie. Om de klanten te selecteren waarop het fonds is gericht, sleept u ze zodat ze onder **Fondsklanten** staan. Dit sneltabblad geeft ook aan hoe het totale bedrag van het fonds wordt verdeeld.

Het sneltabblad **Artikelen** bevat de artikelen die zijn opgenomen in de promotie.

### <a name="trade-allowance-agreement"></a>Handelstoeslagovereenkomst

Nadat het fonds is gedefinieerd, is de volgende stap bij het plannen van promotie het registreren van promotiecontracten (die bekend staan als handelstoeslagovereenkomsten) registreren, het toewijzen van fondsen en het definiëren van prestatiedoelstellingen voor elke merchandisinggebeurtenis.

Handelstoeslagovereenkomsten worden vastgelegd op de pagina **Handelstoeslagovereenkomsten**. Als u de pagina **Handelstoeslagovereenkomsten** wilt openen, selecteert u **Verkoop en marketing** \> **Handelstoeslagen** \> **Handelstoeslagovereenkomsten**.

![Pagina Handelstoeslagovereenkomsten](./media/trade-allowance-management-agreements-page.png "Pagina Handelstoeslagovereenkomsten")

#### <a name="header"></a>Koptekst

Selecteer **Koptekst** om over te schakelen naar de koptekstweergave.

Definieer op het sneltabblad **Algemeen** de velden **Order aan** en **Order van** om de periode te definiëren waarin de overeenkomst geldig is. De goedkeuringsstatus **Intern goedgekeurd** voor de overeenkomst geeft aan dat de overeenkomst nog niet geldig en niet kan worden toegepast tijdens de verwerking van verkooporders.

De sectie **Analyse** van het sneltabblad **Algemeen** bevat belangrijke velden waarin de hoeveelheden en kosten die worden gebruikt voor de evaluatie van de promotie worden gedefinieerd:

- Met het veld **Basiseenheden** wordt het aantal producten opgegeven dat moet worden verkocht aan de geselecteerde klanten voordat de promotie wordt toegepast.
- De waarde **Berekende verzendhoeveelheid** wordt berekend op basis van de waarde **Opheffingspercentage**. Dit is een geplande doelverhoging voor deze promotie.
- Het veld **Handelstoeslagkosten** wordt berekend op basis van de hoeveelheden van de verschillende gebeurtenissen in de handelstoeslagovereenkomst.

Op het sneltabblad **Klanten** in de lijst aan de linkerkant kunt u klantengroepen selecteren en weergeven. Deze worden als vooraf gedefinieerde hiërarchieën ingesteld. U kunt vervolgens de gehele hiërarchie of specifieke rekeningen als doelen voor de toeslagovereenkomst selecteren.

Op het sneltabblad **Artikelen**, zoals het tabblad **Artikelen** van de pagina **Fondsen** worden producten toegevoegd aan de overeenkomst om de verkoop ervan te koppelen aan de overeengekomen toeslag.

Op het sneltabblad **Fondsen** kunt u de promotiefondsen weergeven die aan dit contract zijn gekoppeld. U kunt ook de gebeurteniskostentoewijzing van het contract weergeven. Een gebeurteniskostentoewijzing van 100 procent betekent dat deze promotie uitsluitend uit één fonds wordt gefinancierd. Een promotieovereenkomst kan ook geld uit verschillende fondsen halen en gelijke of differentiële percentagetoewijzing gebruiken.

#### <a name="lines"></a>Regels

Selecteer vervolgens **Regels** om over te schakelen naar de regelweergave.

Het tabblad **Merchandisinggebeurtenissen** bevat de typen gebeurtenissen die door een overeenkomst worden gedekt. Er zijn drie typen: terugbetaling, forfaitair bedrag en factuuraftrek.

Wanneer u de merchandisinggebeurtenis selecteert en vervolgens het tabblad **Bedragen** selecteert, vindt u de details voor de gebeurtenis.

![Regels van handelstoeslagovereenkomst](./media/trade-allowance-management-agreements-lines.png "Regels van handelstoeslagovereenkomst")

In de sectie **Handelstoeslagregels** geeft u de hoeveelheids- of bedragbereiken op die de klant moet realiseren voor definities om de beloningen te verkrijgen.

In het geval van een merchandisinggebeurtenis van het type **Terugbetaling**, worden met het bovenste gedeelte van het tabblad **Bedragen** de regels gedefinieerd op basis waarvan de terugbetaling wordt toegepast, gegenereerd en betaald. De regels kunnen bijvoorbeeld de volgende voorwaarden voor de terugbetalingsvordering opgeven:

- De terugbetaling is gebaseerd op de aanmaakdatum van de verkooporder (de waarde van **Berekeningsdatumtype** is **Gemaakt**).
- De terugbetaling wordt berekend op basis van het bedrag van de verkooporderregel vóór kortingen, niet het nettobedrag, dat kortingen omvat (de waarde van **Opgehaald uit** is **Bruto**).
- De terugbetaling is gebaseerd op het volume van de verkochte producten, niet het bedrag (de waarde van **Regelafbrekingstype van korting** is **Hoeveelheid**).
- De terugbetaling wordt berekend per periode van een maand (de waarde van **Verkoop cumuleren met** is **Maand**). 
- De terugbetaling wordt vereffend als een inhouding, niet met behulp van Leveranciers (de waarde van **Betalingstype** is **Klantinhoudingen**).

In het geval van een merchandisinggebeurtenis van het type **Forfaitair bedrag** wordt met het tabblad **Bedragen** de hoeveelheid aangegeven die aan de klant wordt betaald in de vorm van een inhouding wanneer de klant bepaalde prestaties behaalt. De goedkeuringsstatus **Open** geeft aan dat het forfaitaire bedrag nog niet is betaald.

Als u de overeenkomst wilt toepassen op verkooporders die voldoen aan de voorwaarden van de overeenkomst, moet de status van de overeenkomst **Bevestigd** zijn. 

## <a name="perform-sales-under-the-planned-merchandising-event-and-generate-bill-back-claims"></a>Verkopen onder de geplande merchandisinggebeurtenis uitvoeren en terugbetalingsvorderingen genereren

Wanneer u een verkooporder maakt met regels die voldoen aan de vereisten van de overeenkomst, kunt u de gerelateerde informatie weergeven op de pagina **Verkooporder** door **Verkooporderregel** \> **Weergeven** \> **Prijsdetails** te selecteren.

Op de pagina **Prijsdetails** op het sneltabblad **Kortingen** kan de verkoopmedewerker een terugbetaling van de geldige handelstoeslagovereenkomst zien (de kortingsprogramma-ID wordt weergegeven) en het totaalbedrag dat wordt toegepast op de regel. Het bedrag wordt ook weergegeven in het veld **Kortingsbedrag** in de sectie **Margeschatting** van de pagina **Prijsdetails**.

Wanneer de verkoopfactuur wordt geboekt, wordt een bijbehorende terugbetalingsvordering gegenereerd voor elke factuurregel.

> [!NOTE]
> Als u de pagina **Prijsdetails** op de pagina **Parameters voor Klanten** op het tabblad **Prijzen** wilt zien, schakelt u het selectievakje **Prijsdetails inschakelen** in. I

## <a name="process-claims-and-pass-them-as-deductions-to-ar"></a>Vorderingen verwerken en deze doorgeven als inhoudingen aan Klanten

De volgende stappen in het proces voor het verwerken van terugbetalingen bestaan eruit vorderingen te controleren, te berekenen en goed te keuren en deze vervolgens omzetten in inhoudingen.

De terugbetalingsworkbench is de plek waar de eigenaar van de promotieovereenkomst de vorderingen die worden gegenereerd periodiek controleert en verwerkt. Hier zet de beheerder van Klanten ook de goedgekeurde vorderingen om in inhoudingen of reguliere betalingen, afhankelijk van de betalingsmethode voor de vordering.

Op de pagina **Terugbetalingsworkbench** kunt u de vorderingsregels bekijken. Als de vorderingen de status **Opnieuw te berekenen** hebben, moeten ze opnieuw worden berekend voor enig cumulatief effect.

### <a name="recalculate-claims"></a>Vorderingen herberekenen

Als u de vorderingen opnieuw wilt berekenen, selecteert u **Cumuleren**. Selecteer de klant in het dialoogvenster **Kortingen cumuleren**.

Als gevolg van de herberekening genereert het programma nieuwe vorderingen voor de bedragen om de oorspronkelijke vorderingen aan te passen aan het toepasselijke bedrag per eenheid. Een correctievordering wordt gegenereerd voor elke unieke combinatie van een klant, een artikel, een valuta, een maateenheid, voorraaddimensies, financiële dimensies en een btw-groep. Deze correctievorderingen hebben dezelfde verwijzing naar de verkooporder en het factuurnummer als de vorderingen die worden gecorrigeerd (dat wil zeggen de vorderingen die oorspronkelijk zijn gemaakt in het verkoopdocument). In tegenstelling tot de oorspronkelijke vordering heeft de correctievordering geen waarden in de velden waarin de bedragen en de hoeveelheid van de oorspronkelijke verkooporderregel worden beschreven.

Nadat de herberekening is voltooid, wordt de status van de vorderingen gewijzigd in **Berekend**. Als u de vorderingen wilt goedkeuren, selecteert u **Goedkeuren**.

### <a name="process-claims-and-pass-them-to-ar"></a>Vorderingen verwerken en doorgeven aan Klanten

De vorderingen zijn nu gereed voor verwerking van Klanten. Als u ze wilt verwerken, selecteert u in het actievenster **Verwerken**. 

Bij het verwerken van de vorderingen is de status in **Markeren** en geeft dit aan dat een journaalboeking (het journaal dat wordt geboekt, is het Kortingstoenamejournaal), zoals opgegeven in de parameters voor Klanten ervoor heeft gezorgd dat de volgende gebeurtenissen optreden: 

- De vorderingen zijn overgeboekt naar het tijdelijke klantsaldo als inhoudingen.
- De kortingstoenamerekening is gecrediteerd als aanduiding van de toekomstige verplichting voor de klant.
- De kortingsonkostenrekening is gedebiteerd om de kosten te herkennen die zijn gemaakt in verband met de verkoop.

Om het proces te voltooien, moet de medewerker Klanten nu de toename-inhoudingen verwerken door ze over te boeken naar het klantsaldo als creditnota (verplichting). 

Als u de taak wilt starten, selecteert u in het actievenster van de pagina **Klant** **Incasso** \> **Transacties vereffenen**. Selecteer vervolgens op de **Transacties vereffenen** **Functies** \> **Terugbetalingsprogramma**. Deze kortingspagina bevat alle terugbetalingsvorderingen die eerder zijn verwerkt.

Als u een creditnota wilt maken, schakelt u het selectievakje **Markeren** voor alle regels in en selecteert u vervolgens **Functies** \> **Creditnota maken**.

Bij het maken van creditnota's wordt een journaal geboekt. (Het journaal dat wordt geboekt, is het verbruiksjournaal van Klanten, zoals is opgegeven in de parameters voor Klanten.) Hierdoor is het werkelijke creditbedrag verplaatst naar het klantsaldo. Financieel houdt deze situatie in dat de volgende gebeurtenissen zich hebben voorgedaan:

- De rekening van de klant is gecrediteerd.
- De kortingstoenamerekening is gedebiteerd.

Als u een merchandisinggebeurtenis van het type **Forfaitair bedrag** goedkeurt, selecteert u de gebeurtenis op de pagina **Handelstoeslagovereenkomsten** en vervolgens selecteert u op het tabblad **Bedrag** **Goedkeuren**.

## <a name="settle-the-deduction-that-is-due-and-the-customer-short-pay-by-using-the-deduction-workbench"></a>De inhouding die moet worden betaald en de korte betaling van de klant vereffenen met de inhoudingsworkbench

Vaak kiezen klanten, in afwachting van terugbetalingen, voor korte betalingen van geselecteerde facturen. Als u betalingsafstemmingsproblemen in de toekomst wilt voorkomen, registreert de medewerker Klanten deze korte betalingen als inhoudingen wanneer hij of zij de werkelijke klantbetalingen vastlegt. Vervolgens kunnen in de workbench voor inhoudingen deze klantinhoudingen eenvoudig worden vereffend met de vorderingsbedragen die invorderbaar zijn van het bedrijf.

Selecteer voor het registreren van een korte betaling van een klant in het betalingsjournaal **Klanten** \> **Betalingen** \> **Betalingsjournaal** en maak een nieuw betalingsjournaal. Selecteer vervolgens in het actievenster **Inhoudingen**. Op de pagina **Inhouding** kunt u het bedrag van de korte betaling maken en bijhouden.

De incassomanager is nu verantwoordelijk voor het vereffenen van de openstaande creditnotatransactie en de korte-betalingstransactie met elkaar in de workbench voor inhoudingen.

Als u inhoudingen wilt beheren, selecteert u **Verkoop en marketing** \> **Handelstoeslagen** \> **Inhoudingen** \> **Inhoudingsworkbench**. Het bovenste gedeelte van de pagina bevat regels die de korte betalingen van de klant vertegenwoordigen. Het onderste gedeelte van de pagina bevat de openstaande creditnotatransacties van klanten. 

Als u de inhouding met de openstaande transactie wilt vereffenen, markeert u de inhoudingsregel en markeert u vervolgens op het tabblad Openstaande transacties de regel. Klik in het actievenster op Onderhouden > Afstemmen.

De status van de oorspronkelijke vorderingen is nu ingesteld op **voltooid**.

## <a name="analyze-the-effectiveness-of-the-promotion-and-fund-consumption"></a>De effectiviteit van de promotie en fondsverbruik analyseren

Als u een overzicht van belangrijke statistische gegevens van het programma en het gebruik van fondsen wilt, kunt u verschillende rapporten en analytische weergaven gebruiken die beschikbaar zijn in beheer van handelstoeslagen.

Op de pagina **Handelstoeslagactiviteit** bevat het tabblad **Overzicht** toont de belangrijkste gegevens van de handelstoeslagovereenkomst. De andere tabbladen bevatten specifiekere details over de gekoppelde documenten, betalingen en andere gebeurtenissen die zijn gerelateerd aan het programma.

Het tabblad **Overzicht** geeft de totale hoeveelheid van producten weer die zijn verkocht op basis van de promotie, het verkoopbedrag dat is gefactureerd en de terugbetalingen en forfaitaire bedragen die zijn betaald.

Het tabblad **Terugbetalingkredieten** bevat de details van afzonderlijke terugbetalingen die zijn gecrediteerd bij de klant.

Als u een meer analytisch overzicht van de verschillende prestatiemetingen voor de promotie wilt, kunt u de analyseweergave gebruiken. Als u naar de analyseweergave wilt gaan, klikt u op **Verkoop en marketing** \> **Handelstoeslagen** \> **Handelstoeslagovereenkomsten**. Klik in het actievenster op **Analyse**.  

Als u een meer analytisch overzicht van de verschillende prestatiemetingen voor de promotie wilt, kunt u de analyseweergave gebruiken. Als u naar de analyseweergave wilt gaan, klikt u op **Verkoop en marketing** \> **Handelstoeslagen** \> **Handelstoeslagovereenkomsten**. Klik in het actievenster op **Analyse**. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]