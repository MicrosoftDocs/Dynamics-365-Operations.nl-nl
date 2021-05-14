---
title: Preview van Dynamics 365 Supply Chain Management 10.0.19 (juli 2021)
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
ms.openlocfilehash: 8bb4a7c8085b40ab3eca72675dbe7a3be412d8c1
ms.sourcegitcommit: 2eb7a9ae544f504155657c5c584cbac66c21dba4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/29/2021
ms.locfileid: "5961676"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10019-july-2021"></a>Preview van Dynamics 365 Supply Chain Management 10.0.19 (juli 2021)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in de preview van Microsoft Dynamics 365 Supply Chain Management versie 10.0.19. Deze versie heeft een buildnummer van 10.0.837 en is als volgt beschikbaar:

- **Preview van versie:** april 2021
- **Algemene beschikbaarheid van versie (zelfupdate):** juni 2021
- **Algemene beschikbaarheid van versie (automatische update):** juli 2021

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. De kolom *Functie* bevat koppelingen naar het [releaseplan](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/planned-features) waar u de officiële vrijgavedatums voor elke functie kunt zien. De kolom *Meer informatie* bevat koppelingen naar gerelateerde documentatie.

De meeste functies moeten worden ingeschakeld via [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voordat u ze kunt gebruiken. Sommige van de functies in de lijst zijn nog steeds in preview, terwijl andere mogelijk al algemeen beschikbaar zijn.

| Functiegebied | Functie | Meer informatie |
|---|---|---|
| Voorraad en logistiek | [Optimalisatie van export van gegevensentiteit Contactpersoon](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization)  | *Niet beschikbaar* |
| Voorraad en logistiek | [Incrementele verbeteringen voor uitvoerbewerkingen van magazijn met schaaleenheden](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/incremental-enhancements-warehouse-execution-capabilities-scale-units) |[Berichten van berichtenverwerker](../cloud-edge/cloud-edge-message-processor-messages.md)<br><br>[Magazijnvoorraadcorrectie](../cloud-edge/cloud-edge-warehouse-inventory-adjustment.md)<br><br>[Werkbelasting van magazijnbeheer voor cloud- en randschaaleenheden](../cloud-edge/cloud-edge-workload-warehousing.md) |
| Voorraad en logistiek | [Opzoekfunctie voor velden voor documentintroductie en documentconclusie op de offertepagina van verkoop](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | *Niet beschikbaar* |
| Voorraad en logistiek | [Uitvoerbewerkingen van magazijn met schaaleenheden voor randapparatuur op uw aangepaste hardware](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-execution-edge-scale-units-custom-hardware) | [Schaaleenheden voor randapparatuur implementeren op aangepaste hardware met LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Productie | [Uitvoerbewerkingen van manufacturing met schaaleenheden voor randapparatuur op uw aangepaste hardware](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/manufacturing-execution-edge-scale-units-custom-hardware) | [Schaaleenheden voor randapparatuur implementeren op aangepaste hardware met LBD](../cloud-edge/cloud-edge-edge-scale-units-lbd.md) |
| Planning | Fiattering geplande order op basis van query | [Vast geplande orders](../master-planning/planning-optimization/planned-order-firming.md) |
| Productgegevensbeheer | [Verbeteringen voor pagina met variantsuggesties](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/variant-suggestions-page-improvements) | [Vooraf gedefinieerde productvarianten maken](../pim/tasks/create-predefined-product-variants.md) |

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

Microsoft Dynamics 365 Supply Chain Management 10.0.19 bevat platform updates. Zie [Platform updates voor versie 10.0.19 van Finance and Operations- apps (juli 2021)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19.md) voor meer informatie.

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
