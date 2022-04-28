---
title: Actieberichten
description: Een actiebericht is een door het systeem gegenereerde suggestie om een bestaande geplande of gefiatteerde order te wijzigen.
author: t-benebo
ms.date: 03/18/2022
ms.topic: article
ms.search.form: ReqGroup, MCRSalesOrderMessages, MCRSalesTableDetailedStatus, TAMItemVendRebateGroup, TAMVendRebate, TAMVendRebateAgreementLineInfoPart, TAMVendRebateGroup, TAMVendRebateTable, TAMVendRebateTrans, ReqTransActionListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19411
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: e6df6cfd038383b3eeaa3659e0af3e469429f81e
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570249"
---
# <a name="action-messages"></a>Actieberichten

[!include [banner](../includes/banner.md)]

Een actiebericht is een door het systeem gegenereerde suggestie om een bestaande geplande, goedgekeurde of gefiatteerde order te wijzigen.

Actieberichten worden gegenereerd door de hoofdplanningberekening als reactie op vereisten die zijn gewijzigd. De verzenddatum of de hoeveelheid kan bijvoorbeeld zijn gewijzigd in een verkooporder nadat u al een inkooporder hebt gemaakt om aan de vraag voor die verkooporder te voldoen. In dit geval worden een of meerdere actieberichten gegenereerd door de hoofdplanningsberekening om de inkooporder bij te werken. U beslist of u de aanbevolen wijzigingen aanbrengt.

U kunt configureren hoe actieberichten worden berekend voor een behoefteplanningsgroep die u aan een artikel koppelt.

## <a name="select-action-messages"></a>Actieberichten selecteren

Op de pagina **Behoefteplanningsgroepen** kunt u de actieberichten selecteren die het systeem moet genereren, en de behoefteplanningsgroepen of items waar de berichten van toepassing op zijn. De volgende tabel bevat de actieberichten die u kunt selecteren.

| Bericht | Description |
|---|---|
| Vervroegen | Het systeem genereert wanneer nodig actieberichten om orders naar een eerdere datum te verplaatsen. In het veld **Marge voor vervroegen** kunt u het maximumaantal dagen opgeven dat zonder vervroegde actie tussen ontvangst en uitgifte kan zitten. |
| Uitstellen | Het systeem genereert wanneer nodig actieberichten om orders naar een latere datum te verplaatsen. In het veld **Marge voor uitstellen** kunt u het maximumaantal dagen opgeven dat zonder uitstelactie tussen ontvangst en uitgifte kan zitten. |
| Verlagen | Het systeem genereert actieberichten wanneer productieorders, inkooporders en andere ontvangsttransacties moeten worden verminderd om te hoge voorraadniveaus te voorkomen. |
| Verhoging | Het systeem genereert actieberichten wanneer productieorders, inkooporders en andere ontvangsttransacties moeten worden verhoogd om tekorten in de voorraden te voorkomen. |
| Afgeleide acties | Actieberichten die worden gemaakt voor ontvangsttransacties worden gepropageerd naar afgeleide vereisten en de nodige actieberichten worden gegenereerd voor de ontvangsttransacties die voldoen aan deze vereisten. |

De volgende secties bieden enkele gedetailleerde scenario's.

## <a name="increase-and-decrease-actions-with-product-default-order-quantities"></a>Acties met standaardorderhoeveelheden voor producten verhogen en verlagen

Op de pagina **Standaard orderinstellingen** voor een artikel kunt u een minimale orderhoeveelheid, maximale orderhoeveelheid en meerdere waarden instellen. Bij het voorstellen van acties wordt vervolgens rekening gehouden met deze instellingen, zodat er nooit onderaanbod ontstaat door de suggesties.

U hebt bijvoorbeeld een artikel met de volgende instellingen op de pagina **Standaard orderinstellingen**:

- **Minimale orderhoeveelheid:** *0*
- **Maximale orderhoeveelheid:** *90*
- **Veelvoud:** *20*

Als er vraag is naar een hoeveelheid van 60 van dit artikel, wordt door de hoofdplanning een geplande inkooporder gemaakt voor een hoeveelheid van 60. Als de vraag met 30 wordt verhoogd, wordt door de hoofdplanning een verhoging van 40 voorgesteld, omdat hierdoor het veelvoud van 20 wordt aangehouden en er nooit een onderaanbod wordt veroorzaakt.

## <a name="action-messages-for-orders-related-to-safety-stock"></a>Actieberichten voor orders die betrekking hebben op veiligheidsvoorraad

In actieberichten voor orders die veiligheidsvoorraad leveren, wordt nooit voorgesteld om de hoeveelheid te verlagen tot onder de benodigde hoeveelheid voor de veiligheidsvoorraad. Met andere woorden, als er een order is die veiligheidsvoorraad en klantvraag levert en de vraag wordt verlaagd of geannuleerd, stelt de hoofdplanning voor om de geplande order te verlagen met de verlaagde vraag. Er wordt echter nooit een waarde voorgesteld die lager is dan de veiligheidsvoorraad die nodig is.

Er wordt niet voorgesteld om acties uit te stellen voor de levering van veiligheidsvoorraad, omdat ervan wordt uitgegaan dat de veiligheidsvoorraad op de vereiste tijd en datum moet worden geleverd.

### <a name="advance-and-postpone-actions-related-to-boms"></a>Acties met betrekking tot stuklijsten vervroegen en uitstellen

Acties met betrekking tot stuklijsten moeten vóór de acties van hun bovenliggende artikelen worden toegepast, omdat dit mogelijk gevolgen kan hebben voor verdere orders gerelateerd aan stuklijsten op een hoger niveau. Vervolgens moet u de hoofdplanning opnieuw uitvoeren om de juiste acties opnieuw te berekenen en voor te stellen.

Stel dat zich de volgende situatie voordoet:

- Het eindproduct *EP* van het type *productie* heeft een stuklijst die de grondstof *GS* bevat.
- De huidige datum is 21 januari.
- Een bestaande, vrijgegeven productieorder voor *EP* is gepland voor 25 januari.
- Ter ondersteuning van de bestaande productieorder heeft de hoofdplanning een geplande inkooporder gemaakt voor de vereiste grondstof *GS*. Voor deze order is de behoeftedatum 25 januari.
- Er wordt vandaag een nieuwe verkooporder gemaakt *EP*. De behoeftedatum is vandaag (21 januari).
- 21 januari is gesloten voor levering in de *GS-kalender*, maar 22 januari is geopend.

Wanneer de hoofdplanning wordt uitgevoerd, worden actieberichten gegenereerd waarin wordt voorgesteld de eerder geplande productie te verplaatsen, zodat u de order van vandaag kunt afhandelen.

- Om aan de nieuwe vraag te voldoen, wordt voorgesteld om de productieorder voor *EP* te verplaatsen naar 21 januari. (Hierbij wordt geen rekening gehouden met de gesloten datum voor *GS*.)
- Omdat *GS* nog steeds vereist is voor de productieorder, wordt voorgesteld om de geplande inkooporder ook te vervroegen. Deze keer wordt echter de *GS-kalender* gecontroleerd. Daarom wordt voorgesteld de geplande inkooporder voor *GS* te verplaatsen naar 22 januari (omdat 21 januari is gesloten).

Zoals u ziet, komt de vereiste grondstof *GS* nu te laat voor de geplande productie van *EP*. Daarom moet u eerst de vervroegingsactie toepassen op de geplande inkooporder voor *GS* en vervolgens de hoofdplanning opnieuw uitvoeren. Op dat moment wordt via de hoofdplanning een nieuw actiebericht gegenereerd waarin wordt voorgesteld de productieorder voor *EP* te verplaatsen naar 22 januari.
