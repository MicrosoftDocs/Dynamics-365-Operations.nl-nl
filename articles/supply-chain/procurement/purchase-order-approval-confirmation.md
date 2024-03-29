---
title: Inkooporders goedkeuren en bevestigen
description: In dit artikel worden de statussen beschreven die een inkooporder doorloopt nadat deze is gemaakt, en de gevolgen van het inschakelen van wijzigingsbeheer voor IO's.
author: GalynaFedorova
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchOrderInReview, PurchOrderApproved, PurchOrderInDraft, PurchOrderAssignedToMe, VendPurchOrderJournalListPage, PurchTableWorkflowDropDialog, VendPurchOrderJournal
audience: Application User
ms.reviewer: kamaybac
ms.custom: 93143
ms.assetid: cd12a944-c52c-4579-a301-7abe1d237c72
ms.search.region: Global
ms.search.industry: ''
ms.author: gfedorova
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: af33dbd38b1eb70e79392860e48c6943a4192f78
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016444"
---
# <a name="approve-and-confirm-purchase-orders"></a>Inkooporders goedkeuren en bevestigen

[!include [banner](../includes/banner.md)]

In dit artikel worden de statussen beschreven die een inkooporder (IO) doorloopt nadat deze is gemaakt, en de gevolgen van het inschakelen van wijzigingsbeheer voor IO's.

Nadat een inkooporder (IO) is gemaakt, moet deze mogelijk een goedkeuringsproces doorlopen. Nadat de leverancier heeft ingestemd met de order, wordt de IO ingesteld op de status **Bevestigd**.

## <a name="approval-of-purchase-orders"></a>Goedkeuring van inkooporders
IO's die geen gebruikmaken van wijzigingsbeheer hebben de status **Goedgekeurd** zodra zij worden gemaakt, terwijl IO's die wel gebruikmaken van wijzigingsbeheer meteen nadat zij zijn gemaakt de status **Concept** hebben. Een IO die is gemaakt door een geplande order uit de hoofdplanning te bevestigen, wordt altijd ingesteld op de status **Goedgekeurd**, ongeacht de instellingen voor wijzigingsbeheer. Een IO maakt alleen voorraadtransacties als deze de status **Goedgekeurd** bereikt. Daarom wordt die voorraad pas weergegeven als beschikbaar voor reservering of markering wanneer de order is geaccepteerd.

U schakelt wijzigingsbeheer voor IO's in door de optie **Wijzigingsbeheer activeren** in te stellen op de pagina **Parameters voor inkoopbeheer**. Als wijzigingsbeheer is ingeschakeld, moeten IO's een goedkeuringsworkflow doorlopen nadat zij zijn voltooid. Supply Chain Management heeft een werkstroomverwerkingseditor waarin u een werkstroom voor het goedkeuringsproces kunt definiëren. Deze workflow kan regels bevatten voor automatische goedkeuring, regels om te bepalen wie wordt aangewezen voor het goedkeuren van bepaalde IO's en regels voor het escaleren van een workflow die al lange tijd wacht op goedkeuring. U kunt het proces voor veranderingenbeheer inschakelen voor alle leveranciers of voor specifieke leveranciers. U kunt ook het proces instellen zodat dit kan worden overschreven voor afzonderlijke IO's.

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

Leveranciers die zijn ingesteld voor gebruik van de module voor leverancierssamenwerking kunnen orders in de portal controleren en deze goedkeuren of afwijzen. Tijdens dit controleproces, heeft de IO de status **Bij externe herziening**. De module voor leverancierssamenwerking kan zo worden geconfigureerd dat een bevestiging van de leverancier automatisch de order bevestigt in Supply Chain Management. U kunt ook handmatig een IO bevestigen nadat u een bevestiging van de leverancier hebt ontvangen. Als een leverancier een IO afwijst, wordt de afwijzing ontvangen samen met de reden voor de afwijzing en suggesties voor wijzigingen. In dat geval blijft de status van de IO **Bij externe herziening**.

Er is ook een optie om een pro forma-bevestiging voor een order te genereren voordat de werkelijke bevestiging is verwerkt. Deze optie maakt gewoon een rapport dat u met de leverancier kunt delen. Er wordt geen journaalinformatie gemaakt.

Nadat de leverancier akkoord is gegaan met de order, is de volgende stap het vastleggen van de IO als Toegezegd. U kunt deze stap uitvoeren met behulp van de actie **Bevestiging** of de actie **Bevestigen**. Deze beide acties stellen de goedkeuringsstatus van de order in op **Bevestigd**. Bij bevestiging van een order worden twee extra processen gestart:

-   Er wordt een journaal gemaakt om een exacte kopie van wat in het systeem is bevestigd op te slaan. Soms moeten orders worden gewijzigd en worden andere journalen gemaakt nadat de bijgewerkte order is bevestigd. Via deze journalen kunt u de geschiedenis bekijken van de verschillende versies van de order die zijn bevestigd.
-   Als deze functionaliteit is ingeschakeld worden boekhoudingsverdelingen gemaakt en order- en budgetcontroles uitgevoerd. Als een van beide controles mislukt, ontvangt u een foutbericht waarin wordt gemeld dat wijzigingen moeten worden aangebracht in de IO voordat deze opnieuw kan worden bevestigd.

Een leverancier kan verzoeken om een bepaalde type zekerheid dat betaling voor een aankoop zal plaatsvinden. Er zijn verschillende methoden voor het verstrekken van deze garantie binnen de leveranciersprocessen. Zo worden bijvoorbeeld met de actie **Vooruitbetaling** fondsen gereserveerd voor de IO en deze vooruitbetaling wordt vastgelegd in de IO.

## <a name="changing-purchase-orders"></a>Inkooporders wijzigen
In sommige gevallen moet u mogelijk een IO wijzigen nadat deze de goedkeuringsstatus **Goedgekeurd** of **Bevestigd** heeft bereikt.

Als de IO is gemaakt met behulp van een proces voor wijzigingsbeheer, kunt u wijzigingen aanbrengen door de order in te trekken of, als de order al goedgekeurd is, door de actie **Wijziging aanvraag** te gebruiken. In dat geval wordt de goedkeuringsstatus terug gewijzigd in **Concept** en kunt u de order aanpassen. Nadat het aanbrengen van wijzigingen is voltooid, moet u wellicht de IO indienen om opnieuw te worden goedgekeurd. U kunt de typen wijzigingen configureren die hernieuwde goedkeuring vereisen door een beleidsregel **Regel voor het opnieuw goedkeuren van inkooporders** te gebruiken op de pagina **Inkoopbeleid**.

Als een deel van de bestelde hoeveelheid voor een IO-regel is geleverd, kunt u de bestelde hoeveelheid niet meer wijzigen wanneer de inkooporder de status **Concept** heeft. U kunt de hoeveelheid voor **Nog te leveren** echter wijzigen op de regel voor de inkooporder met de status **Concept**.

Nadat eeen order is bevestigd, kunt u deze niet langer verwijderen. U kunt echter wel de totale hoeveelheid of de eventuele resterende hoeveelheid voor een order annuleren, op voorwaarde dat de hoeveelheid nog niet is ontvangen of gefactureerd. U kunt dan de actie **Voltooien** gebruiken om verdere verwerking te voorkomen. 


## <a name="canceling-purchase-orders"></a>Inkooporders annuleren

Een IO kan worden geannuleerd met de actie **Annuleren** in de koptekst.

Als de hoeveelheid gedeeltelijk is geregistreerd, ontvangen of gefactureerd, kunt u alleen de resterende niet-geregistreerde, ontvangen of gefactureerde hoeveelheid annuleren. De orderhoeveelheid wordt vervolgens overeenkomstig verminderd. Wanneer de hoeveelheid op de regel is bijgewerkt, wordt ook de regelstatus bijgewerkt. Stel, de oorspronkelijke hoeveelheid op de regel is 5 en er wordt een hoeveelheid van 3 ontvangen. In dit geval kunnen er slechts twee worden geannuleerd. Vervolgens wordt de regel bijgewerkt naar de status **Ontvangen**.

Als er een leveringsrestant aan de orderregel wordt toegevoegd en hiermee de hoeveelheid op de orderregel wordt overschreden, wordt met de actie **Annuleren** niet de overtollige hoeveelheid geannuleerd. In plaats daarvan behoudt de regel de status **Openstaande order**, omdat deze een resterende hoeveelheid heeft. Stel, de oorspronkelijke hoeveelheid op de regel is 5 en het leveringsrestant is 7. Als de order wordt geannuleerd, worden er vijf geannuleerd en blijft er een hoeveelheid van 2 over, zoals u in de voorraadtransacties kunt zien.

Als u de hele hoeveelheid op een inkooporderregel wilt annuleren, moet u de hoeveelheid van het leveringsrestant op de regel annuleren. De regel wordt vervolgens bijgewerkt naar de status **Geannuleerd**.

Als een inkooporder onder wijzigingsbeheer valt, moeten wijzigingen, zoals het annuleren van de order of het leveringsrestant, worden ingediend bij het werkstroomsysteem en worden goedgekeurd voordat het proces kan worden voltooid en de voorraadtransacties kunnen worden bijgewerkt als geannuleerd.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van inkooporders](purchase-order-overview.md)

[Inkooporders maken](purchase-order-creation.md)

[Productontvangst tegen inkooporders](product-receipt-against-purchase-orders.md)

[Overzicht van Leveranciersfacturen](../../finance/accounts-payable/vendor-invoices-overview.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]