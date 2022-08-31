---
title: Preview van Dynamics 365 Supply Chain Management 10.0.29 (oktober 2022)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management 10.0.29.
author: kamaybac
ms.date: 08/12/2022
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d95cd9b55f473bed2e3fe69e63837040385f03ac
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334740"
---
# <a name="preview-of-dynamics-365-supply-chain-management-10029-october-2022"></a>Preview van Dynamics 365 Supply Chain Management 10.0.29 (oktober 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management, previewversie 10.0.29. Deze versie heeft het buildnummer 10.0.1326 en is beschikbaar volgens de onderstaande planning:

- **Preview van versie:** augustus 2022
- **Algemene beschikbaarheid van versie (zelfupdate):** september 2022
- **Algemene beschikbaarheid van versie (automatische update):** oktober 2022

## <a name="features-included-in-this-release"></a>Functies in deze versie

De volgende tabel vermeldt de functies die deze versie bevat. Mogelijk wordt dit artikel gewijzigd om functies op te nemen die zijn toegevoegd na de oorspronkelijke publicatie van dit artikel.

| Functiegebied | Functie | Meer informatie | Ingeschakeld door   |
|---|---|---|---|
| Voorraad en logistiek | [WMS-artikelen toewijzen en reserveren in Zichtbaarheid voorraad](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/allocate-reserve-whs-items-inventory-visibility) | Binnenkort beschikbaar | Standaard ingeschakeld |
| Voorraad en logistiek | [Vooraf laden van gestroomlijnde lijsten van de voorhanden voorraad](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/query-inventory-visibility-summary-entity) | Binnenkort beschikbaar | Standaard ingeschakeld |
| Aanbodautomatisering voor maken-naar-order | [Aanbodautomatisering voor maken-naar-order](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-to-order-supply-automation) | [Aanbodautomatisering voor maken-naar-order](../master-planning/make-to-order-supply-automation.md) | Functiebeheer:<br>*Aanbodautomatisering voor maken-naar-order* |
| Planning | [Gedetailleerde inzichten voor DDMRP weergeven en toepassen](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/view-apply-detailed-insights-ddmrp) | [Overzicht van DDMRP (Demand Driven Material Requirements Planning)](../master-planning/planning-optimization/ddmrp-overview.md) | Functiebeheer:<br>*(Preview) DDMRP voor Planningsoptimalisatie* |
| Productiebeheer | [Eindproducten fysiek beschikbaar maken vóór boeking naar journalen](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/make-finished-goods-physically-before-posting) | [Eindproducten fysiek beschikbaar maken vóór boeking naar journalen](../production-control/deferred-posting.md) | Functiebeheer:<br>*(Preview) Eindproducten fysiek beschikbaar maken vóór boeking naar journalen* |
| Magazijnbeheer | [Relevante gegevens opzoeken in de Warehouse mobile app](/dynamics365-release-plan/2022wave2/finance-operations/dynamics365-supply-chain-management/look-up-relevant-data-within-warehouse-mobile-app) | [Gegevens opvragen met de omleidingen van de mobiele app Warehouse Management](../warehousing/warehouse-app-data-inquiry.md) | Functiebeheer:<br>*Gegevensonderzoeksstroom voor Warehouse management-app* |

## <a name="feature-enhancements-included-in-this-release"></a>Functieverbeteringen in deze versie

In de volgende tabel worden de functieverbeteringen weergegeven die deze versie bevat. Al deze functies bieden een incrementele verbetering van een bestaande functie. Aangezien het alleen verbeteringen zijn, worden ze niet weergegeven in het [releaseplan](/dynamics365-release-plan/2022wave1/finance-operations/dynamics365-supply-chain-management/planned-features). Om echter te voorkomen dat deze verbeteringen conflicteren met uw bestaande aanpassingen of voorkeuren, is elk van deze aanpassingen standaard uitgeschakeld (tenzij anders is aangegeven).

Als u een van deze functies wilt in- of uitschakelen, moet u dat doen in [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

| Module | Functienaam in Functiebeheer | Meer informatie |
|---|---|---|
| Kostenbeheer | Optimalisatie van berekening van prijzen in behandeling voor co-producten | Deze functie lost een conflict op dat soms kan optreden wanneer prijzen van co-producten worden berekend met behulp van meerdere threads. Hierdoor controleert het systeem of elke co-productprijs slechts één keer wordt berekend. Het resultaat van de berekening wordt vervolgens gebruikt als invoer voor alle andere berekeningen. Als er al een prijs in behandeling bestaat, wordt deze prijs gebruikt. |
| Hoofdplanning | Transacties groeperen in Planningsoptimalisatie | Deze functie kan helpen het aantal geplande orders te verminderen dat wordt gegenereerd om een enkele verkooporderregel te bevoorraden wanneer u Planningsoptimalisatie gebruikt. Wanneer deze functie is ingeschakeld, groepeert Planningsoptimalisatie alle voorraadtransacties voor een orderregel in één vereiste voor de volledige hoeveelheid. (Dit gedrag komt overeen met het gedrag van de ingebouwde planning engine.) Vraag en aanbod worden afzonderlijk gegroepeerd. Daarom helpt de functie het transactievolume te verminderen wanneer u transacties hebt gesplitst en wanneer u dimensies gebruikt (zoals batchnummers of serienummers) die geen dekkingsdimensies zijn. |
| Inkoopbeheer | Leverancier in wachtstand zetten voor inkooporders | Met deze functie kan een leverancier in de wacht worden gezet voor inkooporders. Er wordt een nieuw blokkeringstype *Inkooporder* toegevoegd waarin een leverancier als in de wacht wordt gemarkeerd voor inkooporders. U kunt geen nieuwe inkooporders maken voor leveranciers die in de wacht staan voor inkooporders, maar u kunt wel doorgaan met openstaande facturen of betalingen voor die leveranciers. |
| Verkoopbeheer en marketing | Nettobedrag per regel berekenen bij import | Met deze functie kunt u bepalen of het systeem regeltotalen opnieuw moet berekenen wanneer u gegevens importeert via de entiteit *Verkooporderregels*, *Verkoopofferteregels* of *Retourorderregels* met behulp van OData of twee keer wegschrijven. Deze functie heeft alleen effect als ook evaluatiebeleid voor handelsovereenkomsten van toepassing is waarin wijzigingen aan het veld **Nettobedrag** voor verkooporderregels, verkoopofferteregels en/of retourorderregels worden beperkt. Er wordt een instelling toegevoegd met de naam met **Nettobedrag per regel berekenen** aan de pagina **Klanten > Instellingen > Parameters van klanten**. Wanneer deze instelling is ingesteld op *Ja* worden regelbedragen altijd opnieuw berekend wanneer dat nodig is (hiermee negeert u elk beleid voor evaluatie van handelsovereenkomsten voor het netto regelbedrag). Wanneer de instelling is ingesteld op *Nee* wordt het netto regelbedrag nooit automatisch berekend, zelfs niet wanneer inkomende wijzigingen in de prijs, hoeveelheid en/of korting van de regel zouden impliceren dat het nettobedrag voor de regel opnieuw moeten worden berekend. Deze functie is standaard ingeschakeld en stelt het **Netto regelbedrag berekenen** in op *Ja*. De instelling *Nee* komt overeen met het gedrag van het systeem vóór versie 10.0.23 en wordt met name geleverd ter ondersteuning van verouderde integratiescenario's.<br><br>Raadpleeg [Regelnettobedragen opnieuw berekenen bij het importeren van verkooporders, offertes en retouren](../sales-marketing/calc-line-net-amounts-import.md) voor meer informatie |
| Verkoopbeheer en marketing | Verkooptotalen berekenen met behulp van meerdere threads | Deze functie helpt prestaties te verbeteren doordat het systeem parallelle verwerking kan gebruiken bij het berekenen van verkooptotalen in een batch. De functie voegt een nieuw veld **Aantal threads** toe aan het dialoogvenster **Verkooptotaal berekenen**. Als u ervoor kiest de berekening in een batch uit te voeren, kunt u dit veld gebruiken om het maximum aantal threads in te stellen. Als u de waarde op *0* (nul) of *1* in stelt, wordt één thread gebruikt. Waarden boven 1 maken multithreading mogelijk. |
| Verkoopbeheer en marketing | Prijzen en kortingen bijwerken die handmatig voor intercompany zijn ingevoerd | Deze functie voegt ondersteuning toe voor handmatig wijzigingsbeleid voor intercompany-orders. De functie bevat ondersteuning voor het overzetten van handmatig wijzigingsbeleid tussen intercompany-verkooporders en -inkooporders. Eerder werd handmatig wijzigingsbeleid alleen ondersteund voor niet-intercompany-orders. Wanneer deze functie is ingeschakeld, geeft het systeem de optie om prijzen en kortingen bij te werken nadat wijzigingen in een intercompany-order zijn opgeslagen. Met deze optie kunt u kiezen of u de nieuwe prijzen en kortingen wilt toepassen op de intercompany-order of de order ongewijzigd wilt laten. |

## <a name="new-and-updated-documentation-resources"></a>Nieuwe en bijgewerkte documentatiebronnen

De volgende Help-artikelen zijn onlangs toegevoegd of ingrijpend bijgewerkt. Deze artikelen hoeven niet te zijn gerelateerd aan de nieuwe functies die voor deze versie zijn toegevoegd, zoals in de vorige secties is vermeld. Deze kunnen u echter helpen meer uit bestaande functies te halen.

| Functiegebied | Nieuwe of bijgewerkte artikelen |
|---|---|
| Hoofdplanning, CTP | [Leveringsdatums van verkooporders berekenen met behulp van CTP](../master-planning/planning-optimization/calculate-delivery-dates-using-ctp.md) |
| Hoofdplanning, DDMRP | [Overzicht van DDMRP (Demand Driven Material Requirements Planning)](../master-planning/planning-optimization/ddmrp-overview.md)<br>[De DDMRP-functie inschakelen voor uw systeem](../master-planning/planning-optimization/ddmrp-enable.md)<br>[Voorraadpositionering](../master-planning/planning-optimization/ddmrp-inventory-positioning.md)<br>[Bufferprofiel en -niveaus](../master-planning/planning-optimization/ddmrp-buffer-profile-and-levels.md)<br>[Vraaggestuurde planning](../master-planning/planning-optimization/ddmrp-planning.md)<br>[Visuele en samenwerkende uitvoering](../master-planning/planning-optimization/ddmrp-visual-and-collaborative-execution.md) |
| Magazijnbeheer | [Containers voor verzending inpakken](../warehousing/packing-containers.md)<br>[Verpakkingswerk voor het verpakken van uitgaande containers en het verwerken van zendingen](../warehousing/packing-work.md) |

## <a name="feature-state-changes-in-this-release"></a>Wijzigingen in status van functie in deze versie

In de volgende tabel worden functies weergegeven die verplicht zijn geworden of standaard zijn ingeschakeld in versie 10.0.29. Al deze functies worden automatisch voor uw systeem ingeschakeld zodra u een update uitvoert naar versie 10.0.29. Verplichte functies kunnen niet worden uitgeschakeld, maar functies die standaard zijn ingeschakeld, kunnen wel worden uitgeschakeld door gebruik te maken van [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

De tabel bevat ook functies die eerder in openbare preview waren, maar zijn gewijzigd om algemeen beschikbaar te worden in versie 10.0.29. Deze wijziging geeft aan dat de functies nu worden aanbevolen voor gebruik in productieomgevingen. Deze functies zijn standaard uitgeschakeld, tenzij anders wordt aangegeven. Daarom moet u [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om ze in te schakelen als u ze wilt gebruiken.

| Module | Functienaam | Nieuwe functiestatus |
| --- | --- | --- |
| Activabeheer | [Functionaliteit van activabeheer voor de uitvoeringsinterface voor de werkvloer](../production-control/production-floor-execution-configure.md) | Verplicht |
| Kostenbeheer | [Het label Annulering in Afsluiten en corrigeren wijzigen in Terugboeken](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/change-terminology-inventory-closing-cancellation-inventory-closing-reverse) | Verplicht |
| Kostenbeheer | Versies met onderlinge kostprijsberekening van details van stuklijstberekening opschonen | Verplicht |
| Kostenbeheer | [Opslag van artikelprijzen vergelijken](../cost-management/compare-item-price.md) | Verplicht |
| Kostenbeheer | [Berekeningsniveau voor kosten](../cost-management/cost-calculation-level.md) | Standaard ingeschakeld |
| Kostenbeheer | Door gebruiker gedefinieerde batchnummerinstellingen inschakelen voor omkeren van voorraadsluiting | Standaard ingeschakeld |
| Kostenbeheer | [Voortgangsdetails van voorraadsluiting](whats-new-scm-10-0-21.md) | Standaard ingeschakeld |
| Kostenbeheer | [Opslag voorraadwaardenrapport](../cost-management/inventory-value-report-storage.md) | Verplicht |
| Kostenbeheer | Voorraadwaardenrapport gegevens opschonen | Verplicht |
| Kostenbeheer | Zwevend gemiddelde, terugvalkostenreeks | Verplicht |
| Kostenbeheer | Logboek voor voorraadafsluiting in raster weergeven | Verplicht |
| Kostenbeheer | De artikelen met niet volledig vereffende transacties weergeven in overzichtsindeling | Verplicht |
| Voorraad- en magazijnbeheer | Lege batchkenmerkwaarden toestaan | Verplicht |
| Voorraad- en magazijnbeheer | Automatische verhoging van regelnummers van de regels van voorraadtransferorders | Verplicht |
| Voorraad- en magazijnbeheer | Transferorder maken op basis van verkoopregel | Verplicht |
| Voorraad- en magazijnbeheer | Veld voorraadjournaalregel in werkstroom uitschakelen | Verplicht |
| Voorraad- en magazijnbeheer | Waarschuwingsfunctie voor parameters voorraadkwaliteitsbeheer inschakelen | Verplicht |
| Voorraad- en magazijnbeheer | (China) Fysieke ontvangst- en uitgiftekosten uitsluiten van maandelijkse gemiddelde kosten | Standaard ingeschakeld |
| Voorraad- en magazijnbeheer | [Goedkeuringswerkstroom voorraadjournaal](../inventory/inventory-journal-workflow.md) | Verplicht |
| Voorraad- en magazijnbeheer | [Opslag voor rapporten voorhanden voorraad](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/inventory-on-hand-report-storage) | Verplicht |
| Voorraad- en magazijnbeheer | [Opgeslagen weergaven voor voorraadbeheer](saved-views-scm.md) | Verplicht |
| Voorraad- en magazijnbeheer | Annulering van transferorder | Verplicht |
| Voorraad- en magazijnbeheer | Het gebruik van maateenheid en eenheidshoeveelheid in voorraadjournalen | Verplicht |
| Voorraad- en magazijnbeheer | Voorraadjournaal ontgrendelen | Verplicht |
| Productie | [Automatisch verzamelen van materialen waarvoor magazijn is ingeschakeld voor automatisch geboekte orderverzamellijsten](whats-new-scm-10-0-23.md) | Algemeen beschikbaar |
| Productie | Weergave van voorraaddimensies in de materialenlijst voor productieroutebewerkingen inschakelen | Verplicht |
| Productie | [Schakel deze optie in als u batch- en serienummers wilt invoeren bij het gereedmelden vanaf het apparaat voor taakkaarten](../production-control/report-finished-job-device.md) | Standaard ingeschakeld |
| Productie | Verbeterd verzamelen van catch weight-hoeveelheid voor productie | Standaard ingeschakeld |
| Productie | [Taak zoeken voor de uitvoeringsinterface voor de werkvloer](../production-control/production-floor-execution-configure.md) | Verplicht |
| Productie | [Integratie van systeem voor productieuitvoering](../production-control/mes-integration.md) | Standaard ingeschakeld |
| Productie | [De weergave Mijn dag voor de uitvoeringsinterface voor de werkvloer](../production-control/production-floor-execution-configure.md) | Standaard ingeschakeld |
| Productie | [Controle voor beschikbaarheid van materiaal op aanvraag voor productieorders](whats-new-scm-10-0-24.md) | Standaard ingeschakeld |
| Productie | [Standaardproductiereservering overschrijven](../production-control/override-default-reservation-principle.md) | Verplicht |
| Productie | [Materiaalverbruik registreren in de uitvoeringsinterface van de werkvloer (niet-WMS)](../production-control/production-floor-execution-configure.md) | Algemeen beschikbaar |
| Productie | [Rapport over catch weight-artikelen uit de uitvoeringsinterface van de productievloer](../production-control/production-floor-execution-configure.md) | Algemeen beschikbaar |
| Productie | [Rapport over co- en bijproducten uit de uitvoeringsinterface op de productievloer](../production-control/production-floor-execution-configure.md) | Standaard ingeschakeld |
| Productie | [Rapporteren over planningsartikelen in de uitvoeringsinterface voor de werkvloer](/dynamics365-release-plan/2021wave2/finance-operations/dynamics365-supply-chain-management/enhanced-production-floor-execution-interface-process-manufacturing) | Standaard ingeschakeld |
| Productie | [Opgeslagen weergaven voor productiebeheer](saved-views-scm.md) | Verplicht |
| Productie | [Volledige serie-, batch- en nummerplaatnummers tonen in de uitvoeringsinterface van de productievloer](../production-control/production-floor-execution-configure.md) | Verplicht |
| Productie | [Vervaldatum van grondstoffen valideren tegen geplande verbruiksdatum](whats-new-scm-10-0-23.md) | Standaard ingeschakeld |
| Hoofdplanning | [Automatisch fiatteren voor Planningsoptimalisatie](../master-planning/planning-optimization/planned-order-firming.md) | Verplicht |
| Hoofdplanning | [Batchgewijs fiatteren en consolideren voor geplande batchorders voor bulk en verpakking](whats-new-scm-10-0-20.md) | Standaard ingeschakeld |
| Hoofdplanning | [Artikelen met voorhanden voorraad opnemen wanneer filters voor voorverwerking zijn ingeschakeld](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/master-planning-include-items-on-hand-when-pre-processing-filters-are-enabled) | Standaard ingeschakeld |
| Hoofdplanning | [Oneindige capaciteitsplanning voor Planningsoptimalisatie](../master-planning/planning-optimization/infinite-capacity-planning.md) | Standaard ingeschakeld |
| Hoofdplanning | [Marges voor Planningsoptimalisatie](../master-planning/planning-optimization/safety-margins.md) | Verplicht |
| Hoofdplanning | [Negatieve dagen voor Planningsoptimalisatie](../master-planning/planning-optimization/delay-tolerance.md) | Verplicht |
| Hoofdplanning | [Parallelle autorisatie van gecorrigeerde vraagprognose](whats-new-scm-10-0-20.md) | Verplicht |
| Hoofdplanning | [Geplande orders fiatteren met filters](../master-planning/planning-optimization/planned-order-firming.md) | Verplicht |
| Hoofdplanning | [Geplande productieorders voor Planningsoptimalisatie](../master-planning/planning-optimization/production-planning.md) | Verplicht |
| Hoofdplanning | [Inkoophandelsovereenkomsten voor planningsoptimalisatie](../master-planning/planning-optimization/purchase-trade-agreement.md) | Verplicht |
| Hoofdplanning | [Opgeslagen weergaven voor geplande orders](saved-views-scm.md) | Verplicht |
| Inkoopbeheer | Toeslagen van- en tot-bedragen op inkooporders | Verplicht |
| Inkoopbeheer | Knop Distributie van opdracht tot inkoop opnieuw instellen uitschakelen | Standaard ingeschakeld |
| Inkoopbeheer | [Het opnieuw instellen van inkoopgerelateerde werkstromen inschakelen](whats-new-scm-10-0-20.md) | Standaard ingeschakeld |
| Inkoopbeheer | [Het aantal inkooporderregels per batchtaak beperken](whats-new-scm-10-0-27.md) | Standaard ingeschakeld |
| Inkoopbeheer | [Financiële dimensies van de leverancier samenvoegen met financiële dimensies van actieve dimensiekoppeling op de inkooporder](whats-new-scm-10-0-25.md) | Verplicht |
| Inkoopbeheer | [Geregistreerde hoeveelheden van producten in voorraad en restanten van niet-voorraadproducten voor ontvangstbewijzen en leveranciersfacturen boeken](whats-new-scm-10-0-26.md) | Algemeen beschikbaar |
| Inkoopbeheer | [Oververbruik van algemene budgetreserveringen voorkomen als er meerdere opdrachten tot inkoop in een workflow zijn](whats-new-scm-10-0-21.md) | Standaard ingeschakeld |
| Inkoopbeheer | [Verantwoordelijke partij voor inkoopovereenkomst](../procurement/purchase-agreements.md) | Verplicht |
| Inkoopbeheer | [Opgeslagen weergaven voor inkooporders](saved-views-scm.md) | Verplicht |
| Productgegevensbeheer | Voorverwerking van stuklijstrapport om time-out te voorkomen | Verplicht |
| Productgegevensbeheer | Financiële dimensies standaard afzonderlijk bij gebruik van artikelsjablonen | Verplicht |
| Productgegevensbeheer | Productdimensiegroepen inschakelen voor artikelsjablonen | Verplicht |
| Productgegevensbeheer | Verbeteringen in entiteit voor artikel - streepjescode | Verplicht |
| Productgegevensbeheer | Productvariantnamen opnieuw genereren op basis van nomenclatuur | Verplicht |
| Productgegevensbeheer | [Opgeslagen weergaven voor vrijgegeven producten](saved-views-scm.md) | Verplicht |
| Productgegevensbeheer | [Verbeteringen voor pagina met variantsuggesties](../pim/tasks/create-predefined-product-variants.md) | Verplicht |
| Verkoopbeheer en marketing | [Toewijzing van toeslagen voor een verkooporder](/dynamics365-release-plan/2020wave1/dynamics365-supply-chain-management/miscellaneous-charges-enhancements) | Verplicht |
| Verkoopbeheer en marketing | Verkooporderhistorie voor update opschonen | Verplicht |
| Verkoopbeheer en marketing | [Verkoophistorie voor update opschonen op basis van ouderdom](../sales-marketing/sales-update-history-cleanup-performance-improvements.md) | Verplicht |
| Verkoopbeheer en marketing | [Optimalisatie van export van gegevensentiteit Contactpersoon](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/contact-person-data-entity-export-optimization) | Verplicht |
| Verkoopbeheer en marketing | Eindkortingsgroep voor verkoopcreditnota kopiëren | Verplicht |
| Verkoopbeheer en marketing | [Zoeken voor de velden Documentinleiding en Documentconclusie van verkoopoffertes inschakelen](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/lookup-functionality-document-introduction-document-conclusion-fields-sales-quotation-page) | Verplicht |
| Verkoopbeheer en marketing | [Prestaties van rapport 'Top 100 van klanten' verbeteren](whats-new-scm-10-0-23.md) | Verplicht |
| Verkoopbeheer en marketing | Wachtende records opnemen in geschiedenisopschoningstaken | Verplicht |
| Verkoopbeheer en marketing | Het aantal verkooporderregels per batchtaak beperken | Standaard ingeschakeld |
| Verkoopbeheer en marketing | [Het aantal verkooporders beperken dat kan worden geselecteerd voor boeking](whats-new-scm-10-0-21.md) | Verplicht |
| Verkoopbeheer en marketing | Geraamd klantsaldo opnieuw berekenen | Verplicht |
| Verkoopbeheer en marketing | [Registratie van verkoopretourregel met decimale precisie met en zonder catch weight](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/sales-return-order-line-registration-decimal-precision-without-catch-weight) | Verplicht |
| Verkoopbeheer en marketing | [Opgeslagen weergaven voor de module Verkoop en marketing](saved-views-scm.md) | Verplicht |
| Verkoopbeheer en marketing | [Verkooporderbevestiging met één klik](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/single-click-sales-order-confirmation) | Verplicht |
| Transportbeheer | Niet-afstemming van vrachtfacturen uit vrachtfactuurregels zonder een geboekt leveranciersfactuurjournaal toestaan | Standaard ingeschakeld |
| Transportbeheer | [Het maken van een leveranciersfactuurjournaal inschakelen wanneer een vrachtfactuur wordt genegeerd](whats-new-scm-10-0-20.md) | Standaard ingeschakeld |
| Transportbeheer | [Kleine pakketten verzenden](../warehousing/small-parcel-shipping.md) | Verplicht |
| Transportbeheer | [Document van USMCA-oorsprongscertificaat](../transportation/usmca-certification-of-origin.md) | Standaard ingeschakeld |
| Magazijnbeheer | [Extra locatiezone](../warehousing/additional-location-zones.md) | Verplicht |
| Magazijnbeheer | [Werk annuleren](../warehousing/cancel-warehouse-work.md) | Verplicht |
| Magazijnbeheer | [Verzending consolideren](../warehousing/configure-shipment-consolidation-policies.md) | Verplicht |
| Magazijnbeheer | [overboekingsorders maken en verwerken vanuit de magazijnapp](../warehousing/create-transfer-order-from-warehouse-app.md) | Verplicht |
| Magazijnbeheer | Sjablonen met locatie-instructies voor cross-docken | Standaard ingeschakeld |
| Magazijnbeheer | [Opslagwerk loskoppelen van ASN's](whats-new-scm-10-0-21.md) | Verplicht |
| Magazijnbeheer | [Uitgestelde put-bewerkingen](../warehousing/deferred-processing-manual-inventory-movement.md) | Verplicht |
| Magazijnbeheer | Uitgestelde plaatsingsbewerking - container | Standaard ingeschakeld |
| Magazijnbeheer | Uitgestelde plaatsingsverwerking – inschakelen voor auditsjabloonfunctie waarvan de triggergebeurtenis is ingesteld op Voorafgaand. | Verplicht |
| Magazijnbeheer | [Verwachte ontvangsten van kwaliteitsorders uitschakelen die een voorbeeld van geblokkeerde voorraad bieden](../inventory/inventory-blocking.md) | Standaard ingeschakeld |
| Magazijnbeheer | Snelle validatie voor mobiele magazijnapparaten inschakelen | Verplicht |
| Magazijnbeheer | [Verbeterde parser voor GS1-streepjescodes](../warehousing/gs1-barcodes.md) | Algemeen beschikbaar |
| Magazijnbeheer | [Flexibele reservering van voor order vastgelegde nummerplaat](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Verplicht |
| Magazijnbeheer | [Flexibele dimensiereservering op magazijnniveau](../warehousing/flexible-warehouse-level-dimension-reservation.md) | Verplicht |
| Magazijnbeheer | [Locatiegebruik artikelconsolidatie](../warehousing/item-consolidation-location-utilization.md) | Standaard ingeschakeld |
| Magazijnbeheer | Ontvangstgeschiedenis nummerplaat | Standaard ingeschakeld |
| Magazijnbeheer | [Handmatige zendingsconsolidatie](../warehousing/consolidate-shipments-manual-workbench.md) | Standaard ingeschakeld |
| Magazijnbeheer | [Handmatige orderverzamelactiviteit van transferregels voor beheerder of soortgelijke vertrouwde gebruikers](whats-new-scm-10-0-28.md) | Algemeen beschikbaar |
| Magazijnbeheer | [Interface voor materiaalverwerkingsapparatuur](../warehousing/mhax.md) | Verplicht |
| Magazijnbeheer | [Nieuwe workbenchpagina's voor ladingplanning](whats-new-scm-10-0-24.md) | Algemeen beschikbaar |
| Magazijnbeheer | [Visualisatie van uitgaande workload](../warehousing/outbound-workload-visualization.md) | Verplicht |
| Magazijnbeheer | [Gepland cross-docken](../warehousing/planned-cross-docking.md) | Verplicht |
| Magazijnbeheer | [Gebeurtenissen in magazijnapp verwerken](../warehousing/warehouse-app-events.md) | Verplicht |
| Magazijnbeheer | Verbetering in query's voor werksjabloon voor wegzetten van co- en bijproducten | Verplicht |
| Magazijnbeheer | [Hoeveelheden afronden naar dichtstbijzijnde verkoopeenheid bij vrijgave aan magazijn](whats-new-scm-10-0-19.md) | Verplicht |
| Magazijnbeheer | [Opgeslagen weergave voor de workbench voor ladingplanning](saved-views-scm.md) | Verplicht |
| Magazijnbeheer | [Opgeslagen weergave voor de pagina Werkgegevens](saved-views-scm.md) | Verplicht |
| Magazijnbeheer | [Opgeslagen weergave voor de verwerking van waves](saved-views-scm.md) | Verplicht |
| Magazijnbeheer | [Opgeslagen weergaven voor de verwerking van ladingen](saved-views-scm.md) | Verplicht |
| Magazijnbeheer | [Opgeslagen weergaven voor verzendingsverwerking](saved-views-scm.md) | Verplicht |
| Magazijnbeheer | [GS1-streepjescode scannen](../warehousing/gs1-barcodes.md) | Algemeen beschikbaar |
| Magazijnbeheer | Details van zendingswavelabels | Verplicht |
| Magazijnbeheer | [Ruimte met gemengde eenheden](whats-new-scm-10-0-21.md) | Verplicht |
| Magazijnbeheer | [Snellere API gebruiken voor het sluiten/heropenen van containers op inpakstation](whats-new-scm-10-0-21.md) | Standaard ingeschakeld |
| Magazijnbeheer | [Sjablonen valideren die zijn geselecteerd voor aanvullingstaken](whats-new-scm-10-0-20.md) | Standaard ingeschakeld |
| Magazijnbeheer | [Gepropageerde velden van magazijnapp](../warehousing/warehouse-app-promoted-fields.md) | Verplicht |
| Magazijnbeheer | [Stapinstructies van magazijnapp](../warehousing/mobile-app-titles-instructions.md) | Verplicht |
| Magazijnbeheer | [Status magazijnlocatie](../warehousing/warehouse-location-status.md) | Verplicht |
| Magazijnbeheer | [Omleidingen van Warehouse Management-app](../warehousing/warehouse-app-detours.md) | Standaard ingeschakeld |
| Magazijnbeheer | [Details van wavebatchtaken](../warehousing/wave-processing.md) | Verplicht |
| Magazijnbeheer | [Meldingen voor uitvoering van wave](../warehousing/wave-execution-notifications.md) | Verplicht |

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformupdates voor apps voor financiële en bedrijfsactiviteiten

Microsoft Dynamics 365 Supply Chain Management 10.0.29 bevat platform updates. Zie voor meer informatie [Platformupdates voor versie 10.0.29 van apps voor financiële en bedrijfsactiviteiten (juni 2022)](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-29.md). <!--KFM: Confirm link -->

### <a name="bug-fixes"></a>Correcties

Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van versie 10.0.29, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-1-plan"></a>Dynamics 365- en bedrijfsclouds: releasewave 1-plan van 2022

Bent u benieuwd naar de komende en onlangs uitgebrachte voorzieningen in een van onze bedrijfsapps of platforms?

Bekijk de [Dynamics 365- en bedrijfsclouds: releasewave 2-plan van 2022](/dynamics365-release-plan/2022wave2/). We hebben alle details in één document verzameld die u kunt gebruiken voor uw planning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Verwijderde en afgeschafte functies voor Supply Chain Management

In het artikel [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) worden functies beschreven die zijn of worden verwijderd voor Supply Chain Management.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Twaalf maanden voordat een functie uit het product wordt verwijderd, wordt de afschaffing aangekondigd in het artikel [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md).

Voor ingrijpende wijzigingen die alleen van invloed zijn op de compilatietijd, maar binair compatibel zijn met sandbox- en productieomgevingen, is de afschaffingstijd korter dan 12 maanden. Meestal zijn dit functionele updates die moeten worden doorgevoerd in de compiler.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
