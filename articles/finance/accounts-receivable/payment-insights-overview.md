---
title: Inzichten in klantbetalingen (voorbeeld)
description: In dit onderwerp wordt beschreven hoe u inzichten in betalingen kunt gebruiken om de gebruikelijke betalingsmethoden van individuele klanten beter te begrijpen. De functie kan u helpen om omstandigheden te identificeren die kunnen rechtvaardigen dat incassoprocessen eerder worden begonnen dan normaal gesproken.
author: ShivamPandey-msft
ms.date: 11/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2019-11-06
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: a1b3b6540a03dc85d5dcd813e8c41ac49ab36728
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822390"
---
# <a name="customer-payment-insights-preview"></a>Inzichten in klantbetalingen (voorbeeld)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp wordt beschreven hoe u inzichten in betalingen kunt gebruiken om de gebruikelijke betalingsmethoden van individuele klanten beter te begrijpen. De functie kan u helpen om omstandigheden te identificeren die kunnen rechtvaardigen dat incassoprocessen eerder worden begonnen dan normaal gesproken. 

## <a name="overview"></a>Overzicht

Het kan moeilijk zijn om te voorspellen wanneer klanten hun facturen betalen. Dit gebrek aan inzichten leidt tot minder nauwkeurige cashflowprognoses, incassoprocessen die te laat beginnen en orders die aan klanten worden vrijgegeven die mogelijk verzuimen om te betalen. Inzichten in klantbetalingen (preview) helpt organisaties te voorspellen wanneer een klantfactuur wordt betaald. Deze informatie kan organisaties helpen bij het maken van incassostrategieën die de kans verbeteren dat op tijd wordt betaald. 

## <a name="predictions"></a>Voorspellingen

Met behulp van betalingsvoorspellingen kunnen organisaties hun bedrijfsprocessen verbeteren omdat ze gemakkelijk kunnen herkennen welke facturen waarschijnlijk te laat worden betaald en passende maatregelen kunnen nemen om de kans op tijdige betaling te vergroten.

Met behulp van een model voor machine learning, dat historische facturen, betalingen en klantgegevens gebruikt, voorspelt Inzichten in klantbetalingen (preview) nauwkeuriger wanneer een klant een openstaande factuur betaalt.

Voor elke openstaande factuur kan Inzichten in klantbetalingen (preview) drie waarschijnlijkheden ten aanzien van betalingen voorspellen:

-   De waarschijnlijkheid dat de betaling op tijd wordt uitgevoerd 
-   De waarschijnlijkheid dat de betaling te laat wordt uitgevoerd
-   De waarschijnlijkheid dat de betaling zeer laat wordt uitgevoerd

Inzichten in klantbetalingen (preview) biedt ook een totaaloverzicht van verwachte betalingen. Dit kan organisaties helpen het totale verschuldigde bedrag te begrijpen dat zij kunnen verwachten van een klant in een van de drie buckets Op tijd, Te laat en Zeer laat.

[![Samengevoegde weergave van betalingsvoorspellingen](./media/graphic-payment-reports.png)](./media/graphic-payment-reports.png)

Bovendien wordt aan elke factuur een waarschijnlijkheid van tijdige betaling toegewezen. Als de waarschijnlijkheid van tijdige betaling minder dan 50% is, worden de facturen gelabeld met een rode cirkel om aan te geven dat voor deze facturen mogelijk aanmaningen moeten worden verzonden. 

[![Lijst met betalingswaarschijnlijkheden](./media/customer-pymnt-probability-list.png)](./media/customer-pymnt-probability-list.png)

Inzichten in klantbetalingen (preview) biedt ook contextuele informatie om de voorspelling uit te leggen, bijvoorbeeld de belangrijkste factoren die invloed hebben op de voorspellingen, de huidige status van zaken met de klant en details over het historische klantbetalingsgedrag. In veel bedrijven is het incassoproces een reactieve activiteit. Het proces begint pas als er facturen verschuldigd zijn. 

Met Inzichten in klantbetalingen (preview) kunnen organisaties proactiever omgaan met incasso's. Ze hoeven niet meer te wachten tot de transacties verschuldigd zijn om het incassoproces te starten. In plaats daarvan kunnen ze de functie voor betalingsvoorspellingen gebruiken om te bepalen of proactieve incasso's de kans op tijdige betaling vergroten. Met betalingsvoorspellingen krijgen bedrijven ook de informatie die nodig is om een eerdere start van het incassoproces te rechtvaardigen.

## <a name="methodology"></a>Methodologie

Het ontwikkelen en implementeren van een AI-oplossing is moeilijk. Een team van gegevenswetenschappers, deskundigen en ingenieurs moeten gedurende langere tijd samenwerken om een bruikbare AI-oplossing te formuleren, te ontwikkelen, te implementeren en te onderhouden. We maken het eenvoudig om AI-oplossingen te implementeren in Finance. We nemen AI-oplossingen in Finance op die zijn gebouwd op basis van Microsoft AI Builder. Een eindgebruiker kan met één muisklik de AI-oplossing implementeren en de voordelen van intelligente voorspellingen benutten. Als een organisatie niet tevreden is over de nauwkeurigheid van voorspellingen, kan een hoofdgebruiker met één klik opnieuw een uitbreiding AI Builder opnemen en vervolgens de velden voor het genereren van voorspellingen selecteren of deselecteren. Vervolgens kunnen ze de wijzigingen trainen en publiceren. Het nieuwe getrainde model wordt vervolgens automatisch opgehaald voor prognoses in Finance.

## <a name="how-to-get-customer-payment-insights-preview"></a>Hoe u aan Inzichten in klantbetalingen (preview) komt

Als u geïnteresseerd bent in het uitproberen van Inzichten in klantbetalingen (preview), stuurt u een e-mail naar [Inzichten in klantbetalingen (preview)](mailto:fiap@microsoft.com).

## <a name="privacy-notice"></a>Privacyverklaring

Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden mogelijk niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]