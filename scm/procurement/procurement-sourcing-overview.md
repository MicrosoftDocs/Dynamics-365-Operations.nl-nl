---
title: Overzicht van inkoopbeheer
description: Dit artikel bevat een overzicht van de functionaliteit die in de module Inkoop en sourcing beschikbaar is.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58021
ms.assetid: eea24e23-a803-4de0-a218-6485757cde1b
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: e8a12f846bb24c9fc79c3533d4e65a2d3ece257b
ms.openlocfilehash: 6d4d476e294e1b5cbe91a61a7ffe151a6c865ea6
ms.contentlocale: nl-nl
ms.lasthandoff: 04/26/2017


---

# <a name="procurement-and-sourcing-overview"></a>Overzicht van inkoopbeheer

[!include[banner](../includes/banner.md)]


Dit artikel bevat een overzicht van de functionaliteit die in de module Inkoop en sourcing beschikbaar is.

De inkoop en sourcing dekken alle stappen van het identificeren van een behoefte aan producten en services tot het aanschaffen van het product, de ontvangst, facturatie, verwerking en betaling van leveranciers. De verwervingsprocessen kunnen naar specifieke behoeften worden geconfigureerd door inkoopbeleid en workflows te definiëren.

## <a name="identifying-a-need-for-product-and-services"></a>Een behoefte aan een product en services bepalen
De vereiste voor producten of services kan het resultaat zijn van *inkopen*, bijvoorbeeld, wanneer een werknemer een product vereist. *Productcatalogi* kunnen worden ingesteld om de selectie te begeleiden van beschikbare producten waaruit kan worden geselecteerd of er kunnen aanvragen worden gedaan van producten die nog niet beschikbaar zijn gemaakt in een catalogus, zodat de inkoopafdeling kan overwegen hoe het product kan worden geleverd.  

*Uitgavenlimieten* kunnen worden gebruikt om inkoopuitgaven te beperken en de *inkoopwerkstroom* voegt de optie toe om goedkeuring toe te vereisen voordat wordt besteld. Het is ook mogelijk toewijzing van budgetfondsen op te geven, indien nodig.  
  
De verwervingsafdeling kiest leveranciers voor vereiste producten en services, en hierbij kan een *offerteaanvraag* naar meerdere potentiële leveranciers worden verzonden. Het is mogelijk om de specificaties van het product te delen dat is aangevraagd en potentiële leveranciers kunnen deze bekijken om te zien of ze een product kunnen leveren dat hieraan voldoet. Leveranciers kunnen hun biedingen retourneren. Vervolgens worden deze door de verwervingsafdeling gecontroleerd, voordat ze de leverancier selecteren van wie ze willen aanschaffen.  

De inkooporders bevatten een optie om een *inkoopquery* te sturen aan de leverancier als alternatief voor een uitgebreider offerteaanvraagproces. De aankoopquery kan worden gebruikt om voorwaarden, zoals prijzen, kortingen en leveringsdatums voor de order plaatsen. Als leveranciers worden ingesteld met de **Leveranciersportal**, wordt de functionaliteit van de aankoopquery uitgeschakeld. In plaats daarvan wordt de order gedeeld in de **Leveranciersportal** en wanneer een *bevestigingsaanvraag* wordt verzonden, kan de leverancier de order direct bevestigen.  

*Leverancierscatalogi* kunnen worden gebruikt om gegevens te verzamelen over het productassortiment dat leveranciers kunnen leveren. Leveranciers kunnen hun eigen catalogus publiceren, zodat is het eenvoudiger is om de catalogus bijgewerkt te houden. Het is mogelijk om een *goedkeurde leverancierslijst* te koppelen aan een product en dat kan helpen leveranciersselectie te begeleiden wanneer nieuwe inkooporders worden geopend en kan het gebruik voorkomen van onbedoelde leveranciers.

## <a name="procurement"></a>Inkoop
*Inkooporders* kunnen worden gemaakt op een aantal verschillende manieren waaronder:

-   Als een uitkomst van hoofdplanning die vraag heeft geïdentificeerd die inkoop vereist. Dit proces genereert geplande inkooporders en wanneer deze worden vrijgegeven, worden inkooporders gegenereerd.
-   Via de verwerking van opdrachten tot inkoop die resulteren in inkoop.
-   Via de verwerking van inkoopovereenkomsten, waarbij inkooporders worden gemaakt als vrijgegeven orders op basis van de overeenkomsten. Dit wordt vaak gebruikt wanneer inkoopovereenkomsten worden gebruikt om afroeporders weer te geven.
-   Handmatig, wanneer de inkooporder die wordt gemaakt, niet is gebaseerd op een ander document.

De inkooporders die zijn geconfigureerd met *inkoopgoedkeuringsworkflows* moeten worden geregistreerd, voordat ze kunnen worden opgenomen als goedgekeurd en dit is vereist voordat de order verder kan worden verwerkt.  

Inkooporders worden *bevestigd* om aan te geven dat overeenkomst is gesloten met de leverancier. De inkooporder doorloopt vervolgens verschillende statussen totdat deze uiteindelijk wordt gefactureerd of geannuleerd.  

Wanneer u een inkooporder maakt, worden veel van de velden van tevoren ingevuld met waarden die standaard komen uit de informatie die over de leverancier is opgeslagen op de pagina **Leveranciers**. Dit betekent dat er een beperkt aantal velden is dat u moet invullen op de inkooporder, hoewel u kunt besluiten de standaardwaarden te negeren.

### <a name="prices-and-discounts"></a>Prijzen en kortingen

De prijzen en kortingen bevatten informatie over de prijzen, kortingen, en de kortingsvoorwaarden die bieden. De prijzen en kortingen kunnen worden weergegeven als *handels**overeenkomsten*. De handelsovereenkomsten bevatten leveranciersprijslijsten met prijzen of kortingen, en hebben een specifieke reeks datums waarvoor de overeenkomst geldig is. De prijzen en kortingen kunnen worden onderhandel en weergegeven in *inkoopovereenkomsten*, met voorwaarden zoals toezeggingen om bepaalde volumes te komen of monetaire bedragen als preconditie voor de overeengekomen voorwaarden. *Kortingsovereenkomsten* kunnen met leveranciers worden gemaakt waarin de inkoop van specifieke producten of groepen producten een korting van de leverancier kan opleveren, afhankelijk van het inkoopbedrag of volume.

### <a name="delivery-options"></a>Leveringsopties

Er zijn verschillende opties voor het leveringsproces dat aan een inkooporder is gekoppeld. De bestelde producten kunnen in *afleveringsschema's* worden opgesplitst, waarin de bestelde hoeveelheid kan worden gepland voor levering op verschillende datums. De levering kan ook *directe levering* omvatten, uitgevoerd vanuit een verkooporder, die het genereren van de pakbon op de verkooporder automatiseert op hetzelfde moment dat de productontvangst wordt vastgelegd op de inkooporder. De inkooporders kunnen ook onderdeel zijn van een *intercompany-orderketen*, ook wel intercompany-inkooporders genoemd. Hierin worden producten besteld vanuit een overeenstemmende intercompany-verkooporder. In deze situatie zijn sommige stappen geautomatiseerd over de twee gerelateerde intercompany-orders.

### <a name="supplementary-items"></a>Bijkomende artikelen

De producten kunnen worden ingesteld om *bijkomende artikelen* te bevatten. Dit diens om producten voor te stellen die zijn gerelateerd aan het product dat wordt besteld. De extra producten kunnen mogelijk vereist zijn of kunnen optioneel zijn. In sommige gevallen kunnen bijkomende artikelen worden toegevoegd als gratis producten bij de aankoop van andere producten.

### <a name="purchase-order-charges"></a>Inkoopordertoeslagen

Kosten kunnen aan de inkooporder worden toegewezen. Dit kan automatisch gebeuren via het instellen van automatische toeslagen of door de toeslagen handmatig toe te voegen. Kosten kunnen aan de order worden toegewezen op koptekstniveau of op het niveau van de order. Toeslagenboekhouding kan op verschillende manieren worden ingesteld. U kunt bijvoorbeeld een toeslag instellen die als productkosten moet worden meegenomen. Als u dit doet, moeten de kosten op het niveau van de orderregel worden toegewezen voordat de order kan worden bevestigd. Er is een optie die kan helpen bij het toewijzen van toeslagen vanuit de orderkoptekst aan de regels.

## <a name="product-receipt-and-invoicing"></a>Productontvangstbon en facturering
Inkooporders die fysieke producten bevatten vereisen doorgaans *aankomstregistratie* in het magazijn en vervolgens de registratie van een *productontvangstbon* voor de order. De inkooporders met producten voor bestelopdrachten kunnen worden geconfigureerd zodat de werknemer die de producten heeft aangevraagd ook een *ontvangstbevestiging* moet versturen.  

Sommige inkooporders bevatten producten die diensten of andere niet-fysische producten zijn waarvoor ontvangst in een magazijn niet nodig is. De producten kunnen als services worden gemaakt of *inkoopcategorieën* kunnen rechtstreeks op de inkooporder voor dergelijke orders worden gebruikt. Met deze orders, wordt de boekhouding voor de productontvangstbon soms overgeslagen en wordt de order direct gefactureerd, of wordt de productontvangstbonregistratie uitgevoerd op de inkooporder zonder eerdere aankomstregistratie.  

De ontvangst van producten kan resulteren in automatisch verbruik voor een specifiek doel. Dit omvat impliciet verbruik met directe levering, verbruik voor een project of boekhoudkundige verwerking van het product als een vast activum.  

Wanneer *leveranciersfacturen* van de leverancier aankomen, kunnen ze eerst afzonderlijk van de inkooporder worden geregistreerd in het *facturenregister* en naderhand worden goedgekeurd als record tegen de inkooporder. Het registreren van de leveranciersfactuur voor de inkooporder bevat het vergelijken van de productontvangstbon met de factuur.  

*Boekhoudingsverdelingen* kan op de inkooporder worden opgegeven om te beschrijven hoe de boekhouding in het grootboek moet worden uitgevoerd en kan ook definiëren hoe de toewijzing van de budgetfondsen wordt verkregen wanneer dit in uw configuratie is opgenomen.  

Gefactureerde inkooporders leggen de schuld vast in de leveranciersrekening in leveranciers, van waaruit de *l*e*veranciersbetaling* wordt verwerkt.

## <a name="vendor-performance"></a>Leverancierprestaties
De prestaties en de controle van inkopen worden ondersteund met *inkoop- en leveranciersrapporten,* waarin uitgavenanalyses en leveranciersprestatieanalyses zijn opgenomen.




