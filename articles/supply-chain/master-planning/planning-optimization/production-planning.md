---
title: Productieplanning
description: In dit artikel wordt de planning voor de productie beschreven en wordt uitgelegd hoe u geplande productieorders wijzigt met behulp van Planningsoptimalisatie.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-12-15
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 43da249637c44b3f56e8b5e210a0e44d9ac6cb9d
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740544"
---
# <a name="production-planning"></a>Productieplanning

[!include [banner](../../includes/banner.md)]

De volgende video geeft een korte inleiding op enkele van de concepten die in dit artikel worden besproken: [Dynamics 365 Supply Chain Management: verbeteringen in planningsoptimalisatie](https://youtu.be/u1pcmZuZBTw).

## <a name="turn-this-feature-on-or-off-for-your-system"></a>Deze functie in- of uitschakelen voor uw systeem

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.29 is de functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.29 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Geplande productieorders voor Planningsoptimalisatie* in de werkruimte [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="planned-production-orders"></a>Geplande productieorders

Wanneer tijdens de hoofdplanning geplande orders worden gemaakt om aan behoeften te voldoen, wordt het ordertype bepaald door de waarde van het veld **Gepland ordertype**. Als het veld **Gepland ordertype** is ingesteld op *Productie*, worden geplande productieorders gemaakt. Deze geplande productieorders bevatten informatie over de actieve stuklijst en de route-id van de gerelateerde productie-instellingen.

## <a name="requirements-from-boms"></a>Behoeften van stuklijsten

Met stuklijstinformatie wordt rekening gehouden tijdens de hoofdplanning. De planuitvoer omvat materiaallevering om de gerelateerde materiaalvraag voor productie te dekken.

Tijdens de hoofdplanning wordt de huidige, actieve stuklijst gebruikt om de materialen te bepalen die nodig zijn voor de productie. Deze stap wordt uitgevoerd via alle niveaus van de stuklijststructuur die is gerelateerd aan de vereiste productieorder. Aan de materiaalbehoefte wordt voldaan door de beschikbare voorhanden voorraad, bestaande voorraad op bestelling en goedgekeurde geplande orders te gebruiken. Als er ergens extra materiaal nodig is, wordt een geplande order gemaakt om aan de vraag te voldoen.

## <a name="scheduling-during-firming"></a>Plannen tijdens fiatteren

Geplande productieorders bevatten de route-id die nodig is voor de productieplanning. De planningsondersteuning tijdens de planningsuitvoering voor geplande orders is echter in behandeling. De route-id wordt gebruikt om geplande productieorders te plannen tijdens de fiattering. Dat betekent dat de doorlooptijd voor geplande productieorders kan afwijken van de doorlooptijd voor gerelateerde geplande, gefiatteerde productieorders die op basis ervan worden gegenereerd, zoals hier wordt beschreven:

- **Geplande productieorder**: de doorlooptijd wordt gebaseerd op de statische doorlooptijd van het vrijgegeven product.
- **Gefiatteerde productieorder**: de doorlooptijd wordt gebaseerd op planning die routegegevens en gerelateerde resourcebeperkingen gebruikt.

## <a name="delays"></a>Vertragingen

Als de doorlooptijd voor benodigd materiaal langer is dan de periode tussen de datum van vandaag en de materiaalbehoeftedatum, wordt de geplande order voor het benodigde materiaal en de bijbehorende productieorder uitgesteld. Voor geplande orders wordt de vertraging (in dagen) berekend op basis van de doorlooptijd van het vrijgegeven product. De vertragingsinformatie wordt vervolgens via alle niveaus van de stuklijststructuur doorgegeven. Daarom kunt u de impact van vertraagde grondstoffen helemaal volgen tot aan de verkooporder van de klant.

## <a name="modifying-planned-orders"></a>Geplande orders wijzigen

Wanneer u de gegevens van een geplande order wijzigt, wordt het volgende bericht weergegeven: "De gevolgen van handmatige wijzigingen voor geplande orders worden pas in de rest van het plan weergegeven als de volgende hoofdplanning wordt uitgevoerd."

Als u informatie over een geplande order wilt wijzigen en de gevolgen ervan op de gerelateerde materiaalbehoeften wilt bekijken, voert u de volgende stappen uit.

1. Werk de geplande order bij.
2. Keur de geplande order goed.
3. Voer de hoofdplanning uit.

Wanneer u de hoofdplanning uitvoert, moet u geen filters gebruiken als geplande productieorders worden opgenomen. Zie de sectie [Filters](#filters), verderop in dit artikel voor meer informatie.

> [!NOTE]
> Als de leveringsdatum van de geplande order wordt gewijzigd in een latere datum, kan de vraag worden getraceerd voor een nieuwe geplande order. Dit gedrag treedt op wanneer de nieuwe leveringsdatum een vertraging veroorzaakt voor de getraceerde vraag, maar deze vertraging kan worden voorkomen volgens de doorlooptijdinstellingen.

## <a name="explosion-page"></a>Pagina Explosie

U kunt op de pagina **Explosie** de vraag analyseren die nodig is voor een bepaalde productieorder of geplande productieorder, de gerelateerde behoefteplanning en informatie over behoeftetracering. De informatie op de pagina **Explosie** wordt bijgewerkt tijdens de hoofdplanning. U kunt de informatie niet rechtstreeks vanaf de pagina **Explosie** bijwerken.

## <a name="filters"></a><a name="filters"></a>Filters

Als u er zeker van wilt zijn dat de hoofdplanning de vereiste informatie voor het berekenen van het juiste resultaat bevat, moet u alle producten die een relatie hebben met producten in de gehele stuklijststructuur van de geplande order opnemen. Voor planningsscenario's die productie omvatten, wordt u daarom aangeraden gefilterde hoofdplanningsuitvoeringen te vermijden.

Hoewel afhankelijke onderliggende artikelen automatisch worden gedetecteerd en opgenomen in hoofdplanningsuitvoeringen wanneer de afgeschafte hoofdplanningsengine wordt gebruikt, wordt deze actie momenteel niet uitgevoerd via Planningsoptimalisatie.

Als bijvoorbeeld één bout uit de stuklijststructuur van product A ook wordt gebruikt om product B te produceren, moeten alle producten in de stuklijststructuur van producten A en B in het filter worden opgenomen. Omdat het complex kan zijn ervoor te zorgen dat alle producten deel uitmaken van het filter, raden we u aan om gefilterde hoofdplanningsuitvoeringen te vermijden wanneer het gaat om productieorders. Als u dit niet doet, levert de hoofdplanning ongewenste resultaten op.

### <a name="reasons-to-avoid-filtered-master-planning-runs"></a>Redenen om gefilterde hoofdplanningsuitvoeringen te vermijden

Wanneer u een gefilterde hoofdplanning voor een product hebt uitgevoerd, worden met Planningsoptimalisatie (in tegenstelling tot de afgeschafte hoofdplanningsengine) niet alle subproducten en grondstoffen in de stuklijststructuur van dat product gedetecteerd en worden deze dus niet meegenomen in de hoofdplanningsuitvoering. Hoewel met Planningsoptimalisatie het eerste niveau in de stuklijststructuur van het product wordt aangegeven, worden er geen productinstellingen (zoals het standaardordertype of de artikelbehoefteplanning) uit de database geladen.

Bij Planningsoptimalisatie worden gegevens voor de uitvoering van tevoren geladen en worden de filters toegepast. Dit betekent dat als een subproduct of grondstof in een specifiek product geen deel uitmaakt van het filter, er geen informatie over wordt vastgelegd voor de uitvoering. Daarbij komt dat als het subproduct of de grondstof ook in een ander product is opgenomen, met een gefilterde uitvoering die alleen het oorspronkelijke product en de onderdelen bevat, de bestaande geplande vraag wordt verwijderd die voor dat andere product is gemaakt.

Door deze logica kunnen gefilterde hoofdplanningsuitvoeringen onverwachte resultaten opleveren. In de volgende gedeelten worden voorbeelden gegeven die de onverwachte resultaten illustreren die kunnen optreden.

### <a name="example-1"></a>Voorbeeld 1

Eindproduct *FG* bestaat uit de volgende onderdelen:

- Grondstof *R*
- Subproduct *S1* dat uit subproduct *S2* bestaat

Er is voorhanden voorraad voor de grondstof *R*, terwijl subproduct *S1* niet op voorraad is.

Wanneer u een gefilterde hoofdplanning voor eindproduct *FG* hebt uitgevoerd, krijgt u een geplande productieorder voor het eindproduct *FG*, een geplande inkooporder voor de grondstof *R* en een geplande inkooporder voor het subproduct *S1*. Dit is een ongewenst resultaat, omdat bij Planningsoptimalisatie een bestaand aanbod voor grondstof *R* wordt genegeerd en subproduct *S1* moet worden geproduceerd met *S2* in plaats van direct besteld. Dit is gebeurd omdat bij Planningsoptimalisatie alleen de lijst met onderdelen voor het eindproduct *FG* zonder bijbehorende informatie beschikbaar is, zoals het bestaande aanbod van de bijbehorende onderdelen of de bijbehorende standaardorderinstellingen.

### <a name="example-2"></a>Voorbeeld 2

Verdergaand met het vorige voorbeeld wordt voor een extra eindproduct, *FG2*, ook subproduct *S1* gebruikt. Er bestaat een geplande order voor eindproduct *FG2* en er bestaat een geplande vraag voor alle onderdelen ervan, waaronder *S1*.

U besluit de ongewenste resultaten van de gefilterde hoofdplanningsuitvoering uit het vorige voorbeeld te ondervangen door alle subproducten en grondstoffen uit de stuklijststructuur van eindproduct *FG* toe te voegen aan het filter en vervolgens een volledige nieuwe generatie uit te voeren.

Wanneer u de volledige nieuwe generatie uitvoert, worden alle bestaande resultaten voor alle opgenomen producten verwijderd en worden resultaten vervolgens opnieuw gemaakt op basis van de nieuwe berekeningen. Dit betekent dat de bestaande geplande vraag naar product *S1* wordt verwijderd en vervolgens opnieuw wordt gemaakt, waarbij alleen rekening wordt gehouden met de vereisten van eindproduct *FG*, terwijl vereisten voor eindproduct *FG2* worden genegeerd. Dit gebeurt omdat bij uitvoering van Planningsoptimalisatie de geplande vraag van andere geplande productieorders niet wordt meegenomen. Alleen de geplande vraag die tijdens de uitvoering is gegenereerd, wordt gebruikt.

> [!NOTE]
> Als de status van de bestaande geplande order voor eindproduct *FG2* *Goedgekeurd* is, wordt de goedgekeurde geplande vraag opgenomen, ook als het bovenliggende product niet aan het filter is toegevoegd.

Tenzij u dus alle onderdelen van het eindproduct *FG*, eindproduct *FG2* en alle andere producten waarvan deze onderdelen (samen met de bijbehorende onderdelen) deel uitmaken toevoegt, levert de gefilterde hoofdplanningsuitvoering ongewenste resultaten op.

Omdat het complex kan zijn ervoor te zorgen dat alle producten deel uitmaken van het filter, raden we u aan om gefilterde hoofdplanningsuitvoeringen te vermijden wanneer het gaat om productieorders.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
