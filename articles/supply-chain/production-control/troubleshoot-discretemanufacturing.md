---
title: Problemen met afzonderlijke fabricage oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met afzonderlijke fabricage.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2004a48455939855df54c3087a11c8003d825566
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222748"
---
# <a name="troubleshoot-discrete-manufacturing"></a>Problemen met afzonderlijke fabricage oplossen

In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met afzonderlijke fabricage.

## <a name="i-receive-the-following-error-message-warehouse-management-processes-are-currently-being-used-if-work-lines-are-not-yet-registered-you-can-cancel-the-created-work-and-any-load-or-shipment-lines-and-then-continue-with-the-picking-or-shipping-process"></a>Het volgende foutbericht wordt weergegeven: "Magazijnbeheerprocessen worden momenteel gebruikt. Als er nog geen werkregels zijn geregistreerd, kunt u het gemaakte werk en eventuele ladings- of zendingsregels annuleren en doorgaan met het orderverzamel- of verzendproces."

### <a name="issue-description"></a>Probleembeschrijving

Dit probleem treedt op als u het werk voor een regel wilt reserveren of vrijgeven, maar de voorraadtransactie heeft de status *Opgenomen*. Dit betekent dat het materiaal is verzameld.

### <a name="issue-resolution"></a>Probleemoplossing

Volg een van deze stappen om dit probleem op te lossen.

- Wijzig de status van de productieorder weer in *Geraamd* of *Vrijgegeven*.
- Open de detailspagina voor de desbetreffende productieorder. Selecteer in het actievenster, op het tabblad **Magazijn** in de groep **Stoppen**, **Stoppen en verzameling opheffen** om alle verzamelde transacties op te opheffen. Selecteer vervolgens **Stop verwijderen** om de productieorder te verwerken.

Hier volgt een uitleg van de functies *Opheffen* en *Stoppen*:

- **Opheffen**: met deze functie wordt de status omgekeerd van voorraadtransacties voor stuklijstregels en formuleregels die een status hebben van *Opgenomen* tot en met *Op order*. Wanneer het werk voor het orderverzamelen van grondstoffen wordt voltooid, wordt de status van de regels ingesteld op *Opgenomen*. Deze status voorkomt dat de productieorder opnieuw wordt ingesteld op de status *Gemaakt*. In dat geval kunt u de functie *Opheffen* niet gebruiken om de transacties van de status *Opgenomen* terug te zetten en vervolgens de productieorder opnieuw in te stellen op de status *Gemaakt*.
- **Stoppen**: met deze functie stelt u een vlag **Gestopt** op de productieorder in om te voorkomen dat de orderstatus wordt bijgewerkt. U kunt de vlag **Gestopt** vinden op het sneltabblad **Magazijn** van de pagina Details van de productieorder.

> [!NOTE]
>
> - De knoppen zijn alleen zichtbaar wanneer de productieorder wordt gemaakt voor artikelen die zijn ingeschakeld voor magazijnprocessen.
> - De groep **Stoppen** is alleen zichtbaar op het tabblad **Magazijn** in het actievenster van de pagina Details van de productieorder. Het is niet zichtbaar op het sneltabblad **Magazijn** van de lijstpagina **Productieorder**.

## <a name="the-matching-resource-name-isnt-updated-after-i-change-a-worker-name-in-the-global-address-book"></a>De naam van de overeenkomende resource wordt niet bijgewerkt nadat ik de naam van een werknemer heb gewijzigd in het globale adresboek.

### <a name="issue-description"></a>Probleembeschrijving

Als u de naam van een werknemer in het globale adresboek bijwerkt, wordt de overeenkomende resourcenaam niet bijgewerkt in de resourcegroepmaster.

### <a name="issue-resolution"></a>Probleemoplossing

Dit scenario wordt momenteel niet ondersteund. Om het probleem op te lossen, moet u de resourcenaam handmatig bijwerken.

## <a name="when-i-create-a-new-production-order-i-dont-receive-the-following-message-insert-the-active-version-of-bill-of-material-and-route"></a>Wanneer ik een nieuwe productieorder maak, ontvang ik het volgende bericht niet: "De actieve versie van stuklijst en route invoegen?"

### <a name="issue-description"></a>Probleembeschrijving

Wanneer u een nieuwe productieorder maakt nadat u het artikelnummer hebt ingevoerd, worden de velden **Locatie** en **Magazijn** automatisch ingesteld op de standaardlocatie en het standaardmagazijn die zijn gedefinieerd op de pagina **Standaardorderinstellingen** voor het gerede artikel. Bovendien worden het actieve stuklijstnummer en routenummer automatisch ingevoerd. Het volgende bericht wordt niet weergegeven waarin u om deze waarden wordt gevraagd:

> Actieve versie voor stuklijst en route invoegen?

### <a name="issue-resolution"></a>Probleemoplossing

U wordt niet gevraagd om stuklijst- en routenummer in te voegen als u een product selecteert waarvoor een locatie en magazijn zijn gedefinieerd op de pagina **Standaardorderinstellingen**. U wordt er alleen om gevraagd als u deze waarden niet voor het geselecteerde product hebt gedefinieerd.

## <a name="production-orders-arent-shown-on-the-marking-page"></a>Productieorders worden niet weergegeven op de pagina Markering.

### <a name="issue-description"></a>Probleembeschrijving

Sommige productieorders worden niet weergegeven op de pagina **Markering**.

### <a name="issue-resolution"></a>Probleemoplossing

Producten met de volgende configuratie zijn niet beschikbaar voor markering. Deze worden daarom niet weergegeven op de pagina **Markering**:

- De producten worden gedefinieerd als producten van het type *catch weight*.
- Deze zijn ingeschakeld voor de geavanceerde magazijnprocessen.
- Deze zijn geconfigureerd om te worden geregeld door het *standaardkostprijsprincipe*.

## <a name="when-i-try-to-end-a-production-order-i-receive-the-following-error-message-calculating-bom-consumptioncost-value-must-be-negative-upon-issue-from-inventory"></a>Wanneer ik een productieorder probeer te beëindigen, wordt het volgende foutbericht weergegeven: "De berekende waarde van consumptionCost van de stuklijst moet negatief zijn bij voorraaduitgifte".

Dit probleem is opgelost in release 10.0.15.

## <a name="when-the-status-of-a-production-order-is-changed-from-reported-as-finished-to-end-i-receive-the-following-error-messages-update-conflict-the-standard-cost-does-not-match-with-the-financial-inventory-value-after-the-update-and-a-critical-error-has-occurred-in-function-inventcostmovementcheckvariance"></a>Wanneer de status van een productieorder wordt gewijzigd van Gereedgemeld in Beëindigd, worden de volgende foutberichten weergegeven: "Conflict tijdens bijwerken. De standaardkostprijs komt niet overeen met de financiële voorraadwaarde na de update" en "Er is een kritieke fout opgetreden in functie InventCostMovement.checkVariance."

Dit probleem treedt op omdat de onderliggende gegevens zijn gewijzigd door een ander proces. Tijdens het proces wordt geprobeerd de gegevens maximaal vijf keer bij te werken. Als het conflict na vijf pogingen nog steeds bestaat, worden de volgende foutberichten weergegeven:

> Conflict tijdens bijwerken. De standaardkosten komen niet overeen met de financiële voorraadwaarde na het bijwerken.

> Er is een kritieke fout opgetreden in functie InventCostMovement. checkVariance.

Dit is zo ontworpen. Als u het probleem wilt verhelpen, hervat u de batchtaak. De uitvoering wordt voltooid.

Als de batchtaak na het hervatten steeds mislukt, controleert u of de afrondingsprecisie voor de standaardvaluta van het grootboek voldoet aan de afronding die is toegepast op waarden in de tabel InventSum. Als de afrondingsprecisie is gewijzigd in een niet-compatibele waarde, moet u de waarde waarschijnlijk terugzetten naar een compatibele waarde. Zoek naar **ModifiedDateTime**. In dit geval geeft de waarde meestal aan dat de afrondingsprecisie onlangs is gewijzigd.

## <a name="when-i-release-to-a-warehouse-i-receive-the-following-error-message-item-rm-could-not-be-fully-reserved-ensure-that-the-full-quantity-is-available-or-reserve-the-items-manually-if-the-reservation-field-on-the-bom-line-is-set-to-manual-or-started-could-not-release-the-order-to-warehouse-because-some-materials-could-not-be-reserved-however-the-status-is-updated-to-released"></a>Wanneer ik vrijgeef naar een magazijn, krijg ik het volgende foutbericht: "Artikel RM kan niet volledig worden gereserveerd. Controleer of de volledige hoeveelheid beschikbaar is of reserveer de artikelen handmatig als het veld Reservering op de stuklijstregel is ingesteld op Handmatig of Begonnen. Kan de order niet vrijgeven aan magazijn omdat sommige materialen niet konden worden gereserveerd." De status wordt echter gewijzigd in Vrijgegeven.

### <a name="issue-description"></a>Probleembeschrijving

Als niet alle stuklijstregelartikelen fysiek beschikbaar zijn wanneer een productieorder wordt vrijgegeven en het beleid **Vrijgave naar magazijn** is ingesteld op *Volledige reservering vereisen* voor de productieorder, wordt het volgende foutbericht weergegeven:

> Artikel RM kan niet volledig worden gereserveerd. Controleer of de volledige hoeveelheid beschikbaar is of reserveer de artikelen handmatig als het veld Reservering op de stuklijstregel is ingesteld op Handmatig of Begonnen. Kon de order niet vrijgeven aan magazijn omdat sommige materialen niet konden worden gereserveerd.

### <a name="issue-resolution"></a>Probleemoplossing

Dit gedrag is inherent aan het ontwerp en is zoals verwacht.

## <a name="when-i-try-to-end-a-production-order-and-report-as-finished-i-receive-the-following-error-message-total-good-quantity-reported-as-finished-for-the-production-will-be-1-feedback-for-the-last-operation-is-000-in-total"></a>Wanneer ik een productieorder probeer te beëindigen en de gereedmelding te voltooien, wordt het volgende foutbericht weergegeven: "Totale gereedgemelde goede hoeveelheid voor de productie is %1. Feedback voor de laatste bewerking is 0,00 in totaal."

### <a name="issue-description"></a>Probleembeschrijving

Wanneer u een gereedmeldingsjournaal voor een productieorder probeert te boeken, wordt het volgende foutbericht weergegeven:

> Totale goede hoeveelheid die voor de productie is gereedgemeld, is %1. Feedback voor de laatste bewerking is 0,00 in totaal.

### <a name="possible-cause"></a>Mogelijke oorzaak

Dit probleem doet zich voor als de hoeveelheden die in de laatste bewerkingen zijn geboekt, onjuist waren. Als de productie bijvoorbeeld wordt gestart, maar de hoeveelheid die moet worden gestart niet is toegewezen, wordt het routekaartjournaal zonder regels geboekt. Om de situatie te bevestigen, opent u de productieorder en selecteert u vervolgens in het actievenster op het tabblad **Weergave** de optie **Routekaart**.

### <a name="workaround"></a>Tijdelijke oplossing

U kunt dit probleem oplossen door aanvullende journalen te boeken voor de bewerkingen waarvoor de journalen niet juist geboekt zijn. Start de productieorder opnieuw en geef op dat u de aanvullende journalen wilt boeken. Met deze actie wordt de productieorder niet gestart, maar worden de journalen geboekt. De routekaart moet vervolgens de hoeveelheden weergeven die zijn geboekt en u moet de productieorders kunnen beëindigen.

## <a name="can-i-report-a-production-order-as-finished-while-i-report-the-error-quantity-but-not-while-i-report-the-time-or-material-quantity"></a>Kan ik een productieorder gereedmelden terwijl ik de fouthoeveelheid rapporteer, maar niet terwijl ik de tijd of de materiaalhoeveelheid rapporteer?

U kunt de fouthoeveelheid van een productieorder niet rapporteren, tenzij u ook de goede hoeveelheid rapporteert. Dit scenario wordt **niet** ondersteund. De update van de gereedmelding zal uiteindelijk mislukken wanneer u probeert de productieorder te beëindigen en dan wordt het volgende foutbericht weergegeven:

> Gereedgemelde hoeveelheid ontbreekt.

## <a name="can-i-trace-the-serial-numbers-of-finished-goods-against-the-serial-numbers-of-consumed-goods"></a>Kan ik de serienummers van eindproducten traceren op basis van de serienummers van verbruikte goederen?

U kunt de serienummers van eindproducten niet traceren op basis van de serienummers van het materiaal dat een productieorder verbruikt om die eindproducten te maken. Dit scenario wordt momenteel niet ondersteund. U kunt dit probleem omzeilen door productieorders te maken voor een hoeveelheid van 1.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]