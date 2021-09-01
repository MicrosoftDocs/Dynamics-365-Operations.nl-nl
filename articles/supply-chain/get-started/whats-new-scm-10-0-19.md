---
title: Wat is nieuw of gewijzigd in Dynamics 365 Supply Chain Management versie 10.0.19 (juni 2021)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Supply Chain Management 10.0.19.
author: kamaybac
ms.date: 04/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-04-23
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c1930a47bc133c411a0e6054aa766322a261064a06ac4cec8dcdd12c126dc7cd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773532"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-version-10019-june-2021"></a>Wat is nieuw of gewijzigd in Dynamics 365 Supply Chain Management versie 10.0.19 (juni 2021)

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management versie 10.0.19. Deze versie heeft een buildnummer van 10.0.837 en is als volgt beschikbaar:

- **Preview van versie:** april 2021
- **Algemene beschikbaarheid van versie (zelfupdate):** juni 2021
- **Algemene beschikbaarheid van versie (automatische update):** juni 2021

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. De kolom *Functie* bevat koppelingen naar het [releaseplan](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) waar u de officiële vrijgavedatums voor elke functie kunt zien. De kolom *Meer informatie* bevat meer details en/of koppelingen naar gerelateerde documentatie.

De meeste functies moeten worden ingeschakeld via [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voordat u ze kunt gebruiken.

| Functiegebied | Functie | Meer informatie |
|---|---|---|
| Voorraad en logistiek | [Door leverancier ingediende bankgegevens goedkeuren en opslaan](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/approve-save-vendor-submitted-bank-details) | [Bankrekeninggegevens van leverancier onderhouden](../../finance/accounts-payable/maintain-vendor-bank-info.md) |
| Voorraad en logistiek | [Optimalisatie van export van gegevensentiteit Contactpersoon](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | Wanneer deze functie is ingeschakeld, worden door wijzigingen in gegevens waarnaar wordt verwezen gerelateerde contactpersonen niet opgenomen in de volgende incrementele export. Wanneer deze functie is uitgeschakeld, worden door wijzigingen in gegevens waarnaar wordt verwezen gerelateerde contactpersonen niet opgenomen in de volgende incrementele export. |
| Voorraad en logistiek | [Incrementele verbeteringen voor uitvoerbewerkingen van magazijn met schaaleenheden](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[Berichten van berichtenverwerker](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Magazijnvoorraadcorrectie](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Werkbelasting van magazijnbeheer voor cloud- en randschaaleenheden](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Voorraad en logistiek | [Opzoekfunctie voor velden voor documentintroductie en documentconclusie op de offertepagina van verkoop](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Met deze functie wordt opzoekfunctionaliteit voor de velden **Documentintroductie** en **Documentconclusie** op de pagina **Verkoopofferte** toegevoegd.<br><br>Deze functie is standaard ingeschakeld. |
| Voorraad en logistiek | [Uitvoerbewerkingen van magazijn met schaaleenheden voor randapparatuur op uw aangepaste hardware](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Schaaleenheden voor randapparatuur implementeren op aangepaste hardware met LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Productie | [Uitvoerbewerkingen van manufacturing met schaaleenheden voor randapparatuur op uw aangepaste hardware](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Randschaaleenheden implementeren op aangepaste hardware met LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Planning | [Oneindige capaciteitsplanning voor Planningsoptimalisatie](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/schedule-infinite-capacity-support-planning-optimization) | Deze functie maakt capaciteitsplanning met onbeperkte capaciteit mogelijk voor planningsoptimalisatie. Zonder deze functie krijgen geplande productieorders de levertijd op basis van de voorraadlevertijd van vrijgegeven producten, ongeacht de time fence voor planning. |
| Planning | Fiattering geplande order op basis van query | [Vast geplande orders](../master-planning/planning-optimization/planned-order-firming.md) |
| Productgegevensbeheer | [Verbeteringen voor pagina met variantsuggesties](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Vooraf gedefinieerde productvarianten maken](../pim/tasks/create-predefined-product-variants.md) |

## <a name="feature-enhancements-included-in-this-release"></a>Functieverbeteringen in deze versie

In de volgende tabel worden de functieverbeteringen weergegeven die deze versie bevat. Al deze functies bieden een incrementele verbetering van een bestaande functie. Aangezien het alleen verbeteringen zijn, worden ze niet weergegeven in het [releaseplan](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Om echter te voorkomen dat deze verbeteringen conflicteren met uw bestaande aanpassingen of voorkeuren, is elk van deze aanpassingen standaard uitgeschakeld (tenzij anders is aangegeven). Als u een van deze functies wilt gebruiken, moet u deze expliciet inschakelen in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Functiegebied | Functie&nbsp;naam&nbsp;in Functie&nbsp;beheer | Meer informatie |
|---|---|---|
| Verkoopbeheer en marketing | Prestatieverbeteringen voor de opschoning van verkoophistorie | Opschoning van verkoophistorie kan veel tijd kosten als dit niet vaak in omgevingen wordt uitgevoerd met veel verkoopupdates. Om de duur te beperken en de betrouwbaarheid te verbeteren, wordt de opschoning opgesplitst in batches die maar een beperkte tijd worden uitgevoerd. Waar mogelijk wordt gebruik gemaakt van databasemogelijkheden om vergrendeling tot een minimum te beperken en samenvoeging van transactietabellen tijdens opschonen te voorkomen. |
| Verkoopbeheer en marketing | Aangevraagde ontvangstdatum bijwerken met bevestigde datum voor intercompany-orders | Met deze functie kunt u bepalen wat er gebeurt met de veldwaarden voor verkoop- en inkoopdatums bij het gebruik van directe intercompany-leveringen. U kunt kiezen of de aangevraagde datums worden bijgewerkt of dat u deze wilt overslaan. Als u de update overslaat, geven de gevraagde datums aan waar de klant om heeft gevraagd. Als u bijwerken inschakelt, geven de aangevraagde datums (wanneer de leveringsdatumcontrole wordt gebruikt) alleen aan wat de klant heeft aangevraagd. Met de leveringsdatumcontrole wordt, wanneer deze verschilt van *Geen*, wat oorspronkelijk is aangevraagd vervangen. U kunt deze optie instellen met de nieuwe instelling **Gevraagde ontvangstdatum bijwerken met bevestigde datum** in de instellingen van de intercompany-leverancier of -klant.<br><br>Als de functie is uitgeschakeld, wordt de aangevraagde ontvangstdatum op de oorspronkelijke verkooporders overschreven op basis van de controleregel voor de leveringsdatum, maar blijft de aangevraagde verzenddatum ongewijzigd. |
| Magazijnbeheer | Hoeveelheden afronden naar dichtstbijzijnde verkoopeenheid bij vrijgave aan magazijn | Met deze functie wordt een optie toegevoegd waarmee u orderhoeveelheden bij vrijgave aan het magazijn kunt beperken. Wanneer deze functie is ingeschakeld, worden orderhoeveelheden naar beneden afgerond naar de dichtstbijzijnde hele verkoopeenheid en worden orders met hoeveelheden van minder dan één verkoopeenheid afgewezen voor vrijgave. |
| Magazijnbeheer | Wavemethode Werk maken plannen in de hele organisatie | Bij inschakeling van deze functie wordt de wavemethode *Werk maken plannen* geconfigureerd om parallel te worden uitgevoerd voor alle rechtspersonen. Er wordt ook een aantal extra instellingen beïnvloed. Zie [Het maken van werk plannen tijdens wave](../warehousing/configure-wave-schedule-work-creation.md) voor de volledige details. |

## <a name="new-and-updated-documentation-resources"></a>Nieuwe en bijgewerkte documentatiebronnen

De volgende Help-onderwerpen zijn onlangs toegevoegd of ingrijpend bijgewerkt. Ze zijn niet noodzakelijkerwijs gerelateerd aan de nieuwe functies die zijn toegevoegd voor deze versie, zoals wordt beschreven in de vorige sectie, maar ze kunnen u helpen om meer uit bestaande functies te halen.

| Functiegebied | Nieuwe of bijgewerkte onderwerpen |
|---|---|
| Beheer voor technische wijzigingen | [Veelgestelde vragen over beheer van technische wijzigingen](../engineering-change-management/change-management-faq.md) |
| Inkoopbeheer | [Categorieaanvragen van leveranciers](../procurement/category-requests-from-vendors.md) |
| Productgegevensbeheer | [Maateenheid beheren](../pim/tasks/manage-unit-measure.md)<br><br>[Berekeningen van productconfiguratiemodel](../pim/config-model-calculations.md) |
| Productiebeheer | [Geïntegreerde nummerreeks voor taak-id's](../production-control/unified-job-ids.md) |
| Transportbeheer | [LTL-klassen](../transportation/ltl-class.md)<br><br>[NMFC-codes](../transportation/nmfc-codes.md) |
| Magazijnbeheer | [Problemen oplossen met hiërarchieën voor magazijnbatches en seriële reserveringen](../warehousing/troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) |
| Magazijnbeheer, aanmaken en verwerken van wave | [Wave maken en verwerken](../warehousing/wave-processing.md)<br><br>[Magazijnparameters voor waveverwerking](../warehousing/wave-warehouse-parameters.md)<br><br>[Wavesjablonen](../warehousing/wave-templates.md)<br><br>[Wavetoewijzing](../warehousing/wave-allocation-method.md)<br><br>[Het maken van werk tijdens wave plannen](../warehousing/configure-wave-schedule-work-creation.md)<br><br>[Containervorming](../warehousing/wave-containerization.md)<br><br>[Meldingen voor uitvoering van wave](../warehousing/wave-execution-notifications.md) |

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platform updates voor Finance and Operations-apps

Microsoft Dynamics 365 Supply Chain Management 10.0.19 bevat platform updates. Zie [Platformupdates voor versie 10.0.19 van Finance and Operations-apps (juni 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md) voor meer informatie.

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van 10.0.19, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=575415).

### <a name="dynamics-365-2021-release-wave-1-plan"></a>Dynamics 365: releasewave 1-plan van 2021

Bent u benieuwd naar de komende en onlangs uitgebrachte voorzieningen in een van onze bedrijfsapps of platforms?

Bekijk [Dynamics 365: releasewave 1-plan van 2021](/dynamics365-release-plan/2021wave1/). We hebben alle details in één document verzameld die u kunt gebruiken voor uw planning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Verwijderde en afgeschafte functies voor Supply Chain Management

In het onderwerp [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) worden functies beschreven die zijn of worden verwijderd voor Supply Chain Management.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Twaalf maanden voordat een functie uit het product wordt verwijderd, wordt de afschaffing aangekondigd in het onderwerp [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md).

Voor ingrijpende wijzigingen die alleen van invloed zijn op de compilatietijd, maar binair compatibel zijn met sandbox- en productieomgevingen, is de afschaffingstijd korter dan 12 maanden. Meestal zijn dit functionele updates die moeten worden doorgevoerd in de compiler.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
