---
title: Overzicht opdracht tot inkoop
description: In dit onderwerp wordt de workflow voor opdrachten tot inkoop beschreven en de verschillende statussen die een opdracht tot inkoop kan hebben.
author: RichardLuan
manager: tfehr
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqConsolidation, PurchReqCreate, PurchReqCreatePurchDetails, PurchReqCreatePurchListPage, PurchReqTable, PurchReqTableListPage, PurchReqConsolidationPartByVendor, PurchReqConsolidationLineDetail, PurchReqConsolidationCreate, PurchReqConsolidationBulkEdit, PurchReqConsolidationAddLine
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2174
ms.assetid: 77d07119-4d9f-4c0e-acbe-d319203571ab
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d3cc8043062fe304ef8127a2abbaeb787c4761f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215932"
---
# <a name="purchase-requisition-overview"></a>Overzicht opdracht tot inkoop

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt de workflow voor opdrachten tot inkoop beschreven en de verschillende statussen die een opdracht tot inkoop kan hebben.

Afhankelijk van hoe uw organisatie is opgezet, kunt u opdrachten tot inkoop maken voor producten die uw organisatie gebruikt. Een opdracht tot inkoop is een intern document dat de inkoopafdeling autoriseert om artikelen of diensten te kopen.  

Nadat een opdracht tot inkoop is goedgekeurd, kan deze worden gebruikt om een inkooporder te genereren. Inkooporders zijn de externe documenten die de inkoopafdeling aan leveranciers overhandigt.

## <a name="creating-purchase-requisitions"></a>Opdrachten tot inkoop maken
U kunt een opdracht tot inkoop maken op de pagina **Mijn opdrachten tot inkoop** en de artikelen en services selecteren die u nodig hebt. U kunt artikelen selecteren uit een aanschaffingscatalogus die uw organisatie maakte of u kunt artikelen vereisen die niet in een catalogus zijn gevonden door een aanschaffingscategorie te selecteren en de productgegevens in te voeren.  

Voordat u een opdracht tot inkoop ter controle kunt indienen, moeten werkstromen worden geconfigureerd. U gebruikt en workflow om een opdracht tot inkoop door het beoordelingsproces te sturen, vanaf de beginstatus **Concept** tot de definitieve status **Goedgekeurd**.

### <a name="purchase-requisition-statuses"></a>Status van inkoopbestelopdracht

Wanneer u een opdracht tot inkoop maakt, wordt hieraan een status toegewezen. Een status wordt ook toegewezen aan elke regel die u aan de opdracht tot inkoop toevoegt. Wanneer u een opdracht tot inkoop ter beoordeling indient bij een workflow, wordt de status van de opdracht tot inkoop en de status van elke regel bijgewerkt terwijl de regels het workflowproces doorlopen.  

U kunt het workflowproces voor de opdracht tot inkoop configureren om een opdracht tot inkoop door het controleproces te routeren als één document. Als alternatief kunnen de regels op een opdracht tot inkoop afzonderlijk naar de juiste controleurs worden gerouteerd. Als de regels van de opdracht tot inkoop afzonderlijk worden gecontroleerd, kan de status van elke regel in opdrachten tot inkoop worden bijgewerkt terwijl de regel het controleproces doorloopt. Wanneer alle regels het controleproces hebben voltooid en er geen controlestappen meer zijn voor de opdracht tot inkoop, wordt de status van de hele opdracht tot inkoop bijgewerkt.

### <a name="purchase-requisition-workflow"></a>Workflow voor opdrachten tot inkoop

Het volgende schema geeft de statussen weer die aan een opdracht tot inkoop en aan een regel in een opdracht tot inkoop worden toegewezen terwijl deze het controleproces doorlopen.  

[![Koptekst en regelstatussen van opdracht tot inkoop](./media/purchasereq_headerline_statuses.jpg)](./media/purchasereq_headerline_statuses.jpg)

### <a name="purchase-requisition-header-and-line-status-relationships"></a>Koptekst en regelstatusrelaties van opdracht tot inkoop

De algemene status van een opdracht tot inkoop wordt bepaald door de status van de regels van de opdracht tot inkoop. Daarom moet het controleproces voor alle regels van de opdracht tot inkoop worden uitgevoerd voordat het controleproces voor de hele opdracht tot inkoop kan worden voltooid. De volgende tabel beschrijft de statussen die aan een koptekst en regels in de opdracht tot inkoop worden toegewezen terwijl de opdracht tot inkoop het workflowproces doorloopt.

<table>
<thead>
<tr class="header">
<th>Status van inkoopbestelopdracht</th>
<th>Regelstatus inkoopbestelopdracht</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Concept</td>
<td>Concept</td>
<td>De opdracht tot inkoop en de regel van de opdracht tot inkoop zijn gemaakt, maar zijn niet ter controle ingediend. Opdracht tot inkoop en regels in opdrachten tot inkoop met de status <strong>Concept</strong> kunnen worden gewijzigd. Een opdracht tot inkoop of regel in een opdracht tot inkoop kan ook de status <strong>Concept</strong> hebben als deze is ingetrokken en niet opnieuw ter controle is ingediend. <strong>Opmerking:</strong> u kunt een opdracht tot inkoop alleen indienen of intrekken op documentniveau. U kunt echter geen afzonderlijke regel in een opdracht tot inkoop intrekken.</td>
</tr>
<tr class="even">
<td>Wordt gecontroleerd</td>
<td><ul>
<li>Wordt gecontroleerd</li>
<li>Geweigerd</li>
</ul></td>
<td>Als de workflow is geconfigureerd om de regels in een opdracht tot inkoop naar individuele controleurs te routeren, dan kan elke regel de status <strong>Wordt gecontroleerd</strong> of <strong>Geweigerd</strong> hebben. De status van de opdracht tot inkoop wordt bijgewerkt wanneer het controleproces voor alle regels in de opdracht tot inkoop is voltooid en er geen controlestappen meer zijn voor de opdracht tot inkoop.
<ul>
<li><strong>Wordt gecontroleerd</strong> - De regels van de opdracht tot inkoop zijn ingediend ter beoordeling. Wanneer een regel in een opdracht tot inkoop het workflowproces heeft voltooid, blijft de status <strong>Wordt gecontroleerd</strong> totdat overige regels van de opdracht tot inkoop zijn beoordeeld.</li>
<li><strong>Geweigerd:</strong> Een regel van een inkoopopdracht is geweigerd. Regels van een opdracht tot inkoop die zijn geweigerd, kunnen worden aangepast en opnieuw ingediend.</li>
</ul>
Als u een regel in een opdracht tot inkoop die is afgewezen opnieuw indient, dan begint het controleproces voor alle regels in de opdracht tot inkoop die nog moeten worden gecontroleerd opnieuw. </br><strong>Opmerking:</strong> U kunt een opdracht tot inkoop intrekken die al is ingediend. Wanneer u een opdracht tot inkoop intrekt, worden alle andere regels in de opdracht tot inkoop ook ingetrokken. Regels van een opdracht tot inkoop die zijn ingetrokken, kunnen worden verwijderd.</td>
</tr>
<tr class="odd">
<td>Geweigerd</td>
<td>Geweigerd</td>
<td>De geselecteerde opdracht tot inkoop en alle opdracht tot inkoopregels zijn geweigerd. Opdrachten tot inkoop en regels in een opdracht tot inkoop die zijn geweigerd, kunnen opnieuw worden ingediend.</td>
</tr>
<tr class="even">
<td>Goedgekeurd</td>
<td><ul>
<li>Goedgekeurd</li>
<li>Geannuleerd</li>
<li>Gesloten</li>
</ul></td>
<td>Alle regels van de opdracht tot inkoop hebben het controleproces voltooid en er zijn geen controlestappen meer voor de opdracht tot inkoop.
<ul>
<li><strong>Goedgekeurd</strong> - Het controleproces voor de regel van de opdracht tot inkoop is voltooid en de regel is goedgekeurd.</li>
<li><strong>Geannuleerd</strong> - De regel in de opdracht tot inkoop is goedgekeurd, maar is geannuleerd omdat deze niet meer vereist is. Alleen regels van een opdracht tot inkoop die zijn goedgekeurd, kunnen worden geannuleerd.</li>
<li><strong>Afgesloten</strong> - De regel in de opdracht tot inkoop is goedgekeurd en de documenten zijn gegenereerd, afhankelijk van het bestelopdrachtdoel.
<ul>
<li>Als het doel van de bestelopdracht verbruik is, wordt er een inkooporder is gegenereerd voor de regel van de opdracht tot inkoop.</li>
<li>Als het doel van de opdracht aanvulling is, zijn een of meer fulfillment-documenten gegenereerd.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Geannuleerd</td>
<td>Geannuleerd</td>
<td>De geselecteerde opdracht tot inkoop en alle opdracht tot inkoopregels zijn geannuleerd.</br> <strong>Opmerking:</strong> als u een artikel op een regel in een opdracht tot inkoop niet meer nodig hebt, moet u de regel in de opdracht tot inkoop annuleren als deze al is goedgekeurd. Alleen regels van een opdracht tot inkoop die zijn goedgekeurd, kunnen worden geannuleerd. Als er regels in de opdracht tot inkoop nog moeten worden gecontroleerd, dan heeft de opdracht tot inkoop de status <strong>Wordt gecontroleerd</strong>. In dit geval kunt u de opdracht tot inkoop intrekken en de juiste regel in de opdracht tot inkoop verwijderen.</td>
</tr>
<tr class="even">
<td>Gesloten</td>
<td><ul>
<li>Gesloten</li>
<li>Geannuleerd</li>
</ul></td>
<td>De opdracht tot aankoop is afgesloten en een of meer voldoeningsdocumenten zijn gegenereerd.
<ul>
<li><strong>Afgesloten</strong> - De regel in de opdracht tot inkoop is goedgekeurd en de documenten zijn gegenereerd, afhankelijk van het bestelopdrachtdoel.
<ul>
<li>Als het doel van de bestelopdracht verbruik is, wordt er een inkooporder is gegenereerd voor de regel van de opdracht tot inkoop.</li>
<li>Als het doel van de opdracht aanvulling is, zijn een of meer fulfillment-documenten gegenereerd.</li>
</ul></li>
<li><strong>Geannuleerd</strong> - De regel in de opdracht tot inkoop is goedgekeurd, maar is geannuleerd omdat deze niet meer vereist is. Alleen regels van een opdracht tot inkoop die zijn goedgekeurd, kunnen worden geannuleerd.</li>
</ul>
<strong>Opmerking:</strong> Als u een artikel op een regel in een opdracht tot inkoop die als is afgesloten niet meer nodig hebt, moet u de regel op het verwerkingsdocument annuleren dat is gegeneerd voor de regel in de opdracht tot inkoop.</td>
</tr>
</tbody>
</table>

## <a name="distributing-costs-to-multiple-financial-accounts"></a>Kosten verdelen over meerdere financiële rekeningen
U kunt in een opdracht tot inkoop de kosten van een product over meerdere financiële rekeningen verspreiden. Als uw organisatie dimensies gebruikt, zoals kostencentra en afdelingen, kunt u de kosten van een product verspreiden over dimensies voor financiële rekeningen.

## <a name="requisition-purposes"></a>Bestelopdrachtdoelen
De bestelopdrachtdoelen maken het proces van de uitvoering van opdrachten tot vraag meer flexibel. Bij het maken van een opdracht kunt u er één van twee doelen aan toewijzen: verbruik of aanvulling. Afhankelijk van het bestelopdrachtdoel en hoe uw organisatie is geconfigureerd, kan aan een bestelvraag worden voldaan met een inkooporder, een transferorder, een productieorder of een kanban.  

In het inkoopbeleid kunt u de bestelopdrachtdoelen bepalen die beschikbaar zijn bij het maken van een opdracht voor uw organisatie.

### <a name="requisitions-that-have-a-purpose-of-consumption"></a>Opdrachten bestemd voor verbruik

Een opdracht die een verbruiksdoel heeft, vertegenwoordigt een vraag naar artikelen of services die intern worden gebruikt door uw organisatie. De vraag dat dit type opdracht maakt, wordt altijd voldaan door een inkooporder. Als Supply Chain Management zo is ingesteld dat er automatisch inkooporders worden gegenereerd, worden inkooporders gemaakt nadat de opdracht tot inkoop is goedgekeurd.

### <a name="requisitions-that-have-a-purpose-of-replenishment"></a>Opdrachten bestemd voor aanvulling

Een opdracht die een aanvullingsdoel heeft, vertegenwoordigt een verzoek voor het aanvullen van de voorraad. U maakt bijvoorbeeld een opdracht om producten aan te vullen zodat ze op een specifiek moment kunnen worden verkocht op een specifieke detailhandellocatie. De vraag die is gemaakt door dit soort opdracht kan worden voldaan door inkooporder, transferorder, productieorder of kanban.  

Wanneer de opdracht een aanvullingsdoel heeft, wordt vraag uitgedrukt als een aantal in plaats van een geldbedrag. Daarom zijn vorderingsboekhouding, budgettaire controle, bedrijfsregels voor vaststellen van vaste activa (BRAD), projectboekhouding en alle bijbehorende regels niet van toepassing. Alleen producten die zijn aangelegd en vrijgegeven voor de opgegeven rechtspersoon kunnen gebruikt worden om te voldoen aan een aanvullingsopdracht. Als u de producten wilt definiëren die beschikbaar zijn wanneer het bestelopdrachtdoel is vervuld, gebruikt u de pagina **Toegangsbeleidsregel voor aanvullingscategorie**.  

Als u opdrachten tot inkoop met een aanvullingsdoel wilt gebruiken, moet u een hoofdplanning opzetten om de opdrachtvraag op te nemen. De uitvoermethode voor de vraag die door dit soort opdracht is gecreëerd, wordt dan automatisch bepaald op basis van het leveringsbeleid dat is ingesteld voor de artikelen in uw organisatie en gepland via de hoofdplanning.

## <a name="purchase-requisitions-and-requests-for-quotation"></a>Opdrachten tot inkoop en offerteaanvragen
In sommige gevallen moet u een proces voor offerteaanvraag (RFQ) opstarten om de leverancier en de prijs te identificeren voor producten die in een opdracht tot inkoop worden aangevraagd. Een offerteaanvraag kan worden gegenereerd wanneer de opdracht tot inkoop wordt gecontroleerd. Als u een bod accepteert, wordt de informatie over de leverancier, prijs enzovoort overgeboekt naar de opdracht tot inkoop.  

U kunt een opdracht tot inkoop in de wachtstand plaatsen door het selecteren van het selectievakje **In wachtstand** op de pagina **Details opdracht tot inkoop**. Verwerking van de opdracht tot inkoop kan alleen worden voortgezet nadat u de blokkering hebt verwijderd door het selectievakje uit te schakelen.  

> [!NOTE]
> In eProcurement kan de offerteaanvraag voor uw opdracht tot inkoop leveranciers toestaan om alternatieve regels toe te voegen. In dit geval geeft uw opdracht tot inkoop goedgekeurd alternatieven weer.

## <a name="demand-consolidation"></a>Vraagconsolidatie
Door inkoopbestelopdrachtregels van meerdere inkoopbestelopdrachten samen te voegen, kunt u uw onderhandelingspositie met uw leveranciers verstevigen om betere prijzen, lagere verzendkosten en lagere overheadkosten te verkrijgen.  

Inkoopbestelopdrachtregels komen enkel in aanmerking voor samenvoegen als de volgende beweringen waar zijn:

-   De inkoopbestelopdracht is goedgekeurd.
-   De inkoopbestelopdracht voldoet aan de criteria van het inkoopbeleid voor handmatige verwerking en samenvoegen.

Goedgekeurde regels voor opdracht tot inkoop die aan de criteria voor handmatige verwerking voldoen worden op de pagina **Goedgekeurde opdrachten tot inkoop vrijgeven** weergegeven. Als een regel in de opdracht tot inkoop ook voldoet aan de criteria voor vraagconsolidatie, kan de regel worden toegevoegd aan een samenvoegingsmogelijkheid.  

Een samenvoegingsmogelijkheid is een reeks regels in de opdracht voor inkoop die samen worden gegroepeerd zodat inkoper met leveranciers kan onderhandelenv voor de beste deal. Regels in de opdracht tot inkoop die u selecteert voor een samenvoegingsmogelijkheid worden op de pagina **Consolidatie opdracht tot inkoop** weergegeven. U kunt de regels op deze pagina wijzigen, als er wijzigingen nodig zijn. U kunt ook nieuwe regels toevoegen aan de samenvoegingsmogelijkheid of bestaande regels verwijderen.  

Nadat u opdrachtregels aan een samenvoegingsmogelijkheid hebt toegevoegd en vereiste wijzigingen hebt aangebracht, kunt u een inkooporder maken voor de samengevoegde regels in de opdracht tot inkoop.  

> [!NOTE]
> Wijzigingen die u aanbrengt aan een opdracht tot inkoop op de pagina **Consolidatie opdracht tot inkoop** worden weergegeven op de inkooporder die u maakt. In de opdracht tot inkoop blijft de regel ongewijzigd, zodat de geschiedenis wordt behouden.  

Als u een inkooporder wilt maken voor regels in de opdracht tot inkoop die niet in aanmerking komen voor consolidatie of die niet zijn geselecteerd voor een samenvoegingsmogelijkheid, moet u de regels handmatig verwerken.

### <a name="consolidating-purchase-requisition-lines"></a>Inkoopbestelopdrachtregels samenvoegen

Het proces voor consolidatie van de vraag wordt gestart wanneer een opdracht tot inkoop is goedgekeurd in een werkstroom en, als budgetbeheer is geconfigureerd voor uw organisatie, wanneer de budgetreserveringen en voorvorderingen zijn opgenomen. Het volgende schema geeft de processtroom voor consolidatie van de vraag weer.  

[![Processtroom voor vraagconsolidatie](./media/demand-consolidation.gif)](./media/demand-consolidation.gif)  

Om goedgekeurde inkoopbestelopdrachtregels samen te voegen, volgt u deze stappen:

1.  Controleer de goedgekeurde opdrachtregels voor handmatige verwerking en die in aanmerking komen voor samenvoeging.
2.  Selecteer regels die u wilt toevoegen aan een samenvoegingsmogelijkheid.
3.  Maak een nieuwe samenvoegingsmogelijkheid of voeg opdrachtregels toe aan een bestaande samenvoegingsmogelijkheid.
4.  Breng vereiste wijzigingen toe aan de opdrachtregels en verwijder opdrachtregelartikelen die u niet langer wilt opnemen in de samenvoegingsmogelijkheid.
5.  Inkooporders maken voor geconsolideerde opdrachtregels of inkoopbestelopdrachtregels in een samenvoegingsmogelijkheid.


<a name="additional-resources"></a>Aanvullende resources
--------

[Een bestelaanvraag voor verbruik maken](tasks/create-requisition-consumption.md)

[Workflow voor opdrachten tot inkoop](purchase-requisitions-workflow.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]