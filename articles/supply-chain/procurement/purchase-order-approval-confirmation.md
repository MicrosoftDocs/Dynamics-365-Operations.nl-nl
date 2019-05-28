---
title: Inkooporders goedkeuren en bevestigen
description: In dit onderwerp worden de statussen beschreven die een inkooporder (IO) doorloopt nadat deze is gemaakt, en de gevolgen van het inschakelen van wijzigingsbeheer voor IO's.
author: FrankDahl
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.search.industry: ''
ms.author: fdahl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e274f52484d3fe1884152f155b6b7f0714f8842e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572691"
---
# <a name="approve-and-confirm-purchase-orders"></a>Inkooporders goedkeuren en bevestigen

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

In dit onderwerp worden de statussen beschreven die een inkooporder (IO) doorloopt nadat deze is gemaakt, en de gevolgen van het inschakelen van wijzigingsbeheer voor IO's.

Nadat een inkooporder (IO) is gemaakt, moet deze mogelijk een goedkeuringsproces doorlopen. Nadat de leverancier heeft ingestemd met de order, wordt de IO ingesteld op de status **Bevestigd**.

## <a name="approval-of-purchase-orders"></a>Goedkeuring van inkooporders
IO's die geen gebruikmaken van wijzigingsbeheer hebben de status **Goedgekeurd** zodra zij worden gemaakt, terwijl IO's die wel gebruikmaken van wijzigingsbeheer de status **Concept** hebben meteen nadat zij zijn gemaakt. Een IO die is gemaakt door een geplande order uit de hoofdplanning te bevestigen, wordt altijd ingesteld op de status **Goedgekeurd**, ongeacht de instellingen voor wijzigingsbeheer. Een IO maakt alleen voorraadtransacties als deze de status **Goedgekeurd** bereikt. Daarom wordt die voorraad pas weergegeven als beschikbaar voor reservering of markering nadat de order is geaccepteerd.  

U schakelt wijzigingsbeheer voor IO's in door de optie **Wijzigingsbeheer activeren** in te stellen op de pagina **Parameters voor inkoopbeheer**. Als wijzigingsbeheer is ingeschakeld, moeten IO's een goedkeuringsworkflow doorlopen nadat zij zijn voltooid. Microsoft Dynamics 365 for Finance and Operations heeft een werkstroomverwerkingseditor waarin u een werkstroom voor het goedkeuringsproces kunt definiëren. Deze workflow kan regels bevatten voor automatische goedkeuring, regels om te bepalen wie wordt aangewezen voor het goedkeuren van bepaalde IO's en regels voor het escaleren van een workflow die al lange tijd wacht op goedkeuring. U kunt het proces voor veranderingenbeheer inschakelen voor alle leveranciers of voor specifieke leveranciers. U kunt ook het proces instellen zodat dit kan worden overschreven voor afzonderlijke IO's.  

Als wijzigingsbeheer is ingeschakeld, doorlopen IO's zes goedkeuringsstatussen, van **Concept** tot **Voltooid**. Nadat een order is goedgekeurd, moeten gebruikers die deze willen wijzigen de actie **Wijziging aanvraag** gebruiken.

| Goedkeuringsstatus | Beschrijving                                                                      | Wijziging aanvraag is ingeschakeld |
|-----------------|----------------------------------------------------------------------------------|---------------------------|
| Concept           | De IO is een concept en is nog niet ingediend voor goedkeuring in de IO-workflow.     | Nee                        |
| Wordt gecontroleerd       | De IO is ingediend voor goedkeuring in de IO-workflow. In afwachting van goedkeuring.       | Nee                        |
| Geweigerd        | De IO is geweigerd tijdens het goedkeuringsproces.                                 | Nee                        |
| Goedgekeurd        | De IO is goedgekeurd.                                                             | Ja                       |
| Bevestigd       | De IO is bevestigd. Een IO kan pas worden bevestigd nadat deze is goedgekeurd.        | Ja                       |
| Voltooid       | De IO is definitief gemaakt. Deze is nu financieel afgesloten en kan niet meer worden gewijzigd. | Nee                        |

## <a name="confirming-purchase-orders"></a>Inkooporders bevestigen
IO's met de goedkeuringsstatus **Goedgekeurd** kunnen aanvullende stappen doorlopen voordat ze worden bevestigd. Zo moet u bijvoorbeeld mogelijk een inkooponderzoek naar de leverancier verzenden voor informatie over prijzen, kortingen of leverdatums. In dat geval kunt u de IO instellen op de status **Bij externe herziening** met behulp van de actie **Inkooponderzoek**.  

Leveranciers die zijn ingesteld voor gebruik van het leveranciersportaal kunnen orders op de portal controleren en deze goedkeuren of afwijzen. Tijdens dit controleproces, heeft de IO de status **Bij externe herziening**. De leveranciersportal kan zo worden geconfigureerd dat een bevestiging van de leverancier automatisch de order bevestigt in Finance and Operations. U kunt ook handmatig een IO bevestigen nadat u een bevestiging van de leverancier hebt ontvangen. Als een leverancier een IO afwijst, wordt de afwijzing ontvangen samen met de reden voor de afwijzing en suggesties voor wijzigingen. In dat geval blijft de status van de IO **Bij externe herziening**.  

Er is ook een optie om een pro forma-bevestiging voor een order te genereren voordat de werkelijke bevestiging is verwerkt. Deze optie maakt gewoon een rapport dat u met de leverancier kunt delen. Er wordt geen journaalinformatie gemaakt.  

Nadat de leverancier akkoord is gegaan met de order, is de volgende stap het vastleggen van de IO als Toegezegd. U kunt deze stap uitvoeren met behulp van de actie **Bevestiging** of de actie **Bevestigen**. Deze beide acties stellen de goedkeuringsstatus van de order in op **Bevestigd**. Bij bevestiging van een order worden twee extra processen gestart:

-   Er wordt een journaal gemaakt om een exacte kopie van wat in het systeem is bevestigd op te slaan. Soms moeten orders worden gewijzigd en worden andere journalen gemaakt nadat de bijgewerkte order is bevestigd. Via deze journalen kunt u de geschiedenis bekijken van de verschillende versies van de order die zijn bevestigd.
-   Als deze functionaliteit is ingeschakeld worden boekhoudingsverdelingen gemaakt en order- en budgetcontroles uitgevoerd. Als een van beide controles mislukt, ontvangt u een foutbericht waarin wordt gemeld dat wijzigingen moeten worden aangebracht in de IO voordat deze opnieuw kan worden bevestigd.

Een leverancier kan verzoeken om een bepaalde type zekerheid dat betaling voor een aankoop zal plaatsvinden. Er zijn verschillende methoden voor het verstrekken van deze garantie binnen de leveranciersprocessen. Zo worden bijvoorbeeld met de actie **Vooruitbetaling** fondsen gereserveerd voor de IO en deze vooruitbetaling wordt vastgelegd in de IO.

## <a name="changing-purchase-orders"></a>Inkooporders wijzigen
In sommige gevallen moet u mogelijk een IO wijzigen nadat deze de goedkeuringsstatus **Goedgekeurd** of **Bevestigd** heeft bereikt.  

Als de IO is gemaakt met behulp van een proces voor wijzigingsbeheer, kunt u wijzigingen aanbrengen door de order in te trekken of, als de order al goedgekeurd is, door de actie **Wijziging aanvraag** te gebruiken. In dat geval wordt de goedkeuringsstatus terug gewijzigd in **Concept** en kunt u de order aanpassen. Nadat het aanbrengen van wijzigingen is voltooid, moet u wellicht de IO indien voor hernieuwde goedkeuring. U kunt de typen wijzigingen configureren die hernieuwde goedkeuring vereisen door een beleidsregel **Regel voor het opnieuw goedkeuren van inkooporders** te gebruiken op de pagina **Inkoopbeleid**.  

Als een deel van de bestelde hoeveelheid voor een IO-regel is geleverd, kunt u de bestelde hoeveelheid niet meer wijzigen. U kunt echter wel de hoeveelheid voor **Nog te leveren** op de regel aanpassen. U kunt dan de actie **Voltooien** gebruiken om regels te annuleren en verdere verwerking te voorkomen. 

Nadat eeen order is bevestigd, kunt u deze niet langer verwijderen. U kunt echter wel de totale hoeveelheid of de eventuele resterende hoeveelheid voor een order annuleren, op voorwaarde dat de hoeveelheid nog niet is ontvangen of gefactureerd.

<a name="additional-resources"></a>Aanvullende resources
--------

[Overzicht van inkooporders](purchase-order-overview.md)

[Inkooporder maken](purchase-order-creation.md)

[Productontvangst tegen inkooporders](product-receipt-against-purchase-orders.md)

[Overzicht van leveranciersfacturen](../../financials/accounts-payable/vendor-invoices-overview.md)



