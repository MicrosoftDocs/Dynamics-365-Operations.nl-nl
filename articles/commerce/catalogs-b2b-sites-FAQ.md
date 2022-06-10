---
title: Veelgestelde vragen over Commercecatalogi voor B2B-sites
description: Dit onderwerp biedt antwoorden op veelgestelde vragen over Microsoft Dynamics 365 Commerce-catalogi.
author: ashishmsft
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 5bdc7dfcb0e48aa85db2db4d178c5bf62ea0411b
ms.sourcegitcommit: bca0cb730307948368a9aabe322cf963688ed8b1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/19/2022
ms.locfileid: "8782857"
---
# <a name="commerce-catalogs-for-b2b-faq"></a>Veelgestelde vragen over Commercecatalogi voor B2B-sites

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dit onderwerp biedt antwoorden op veelgestelde vragen over Microsoft Dynamics 365 Commerce [B2B-catalogi (business-to-business)](catalogs-b2b-sites.md).

## <a name="why-cant-i-configure-a-catalog-specific-navigation-hierarchy-or-see-an-option-to-associate-a-customer-hierarchy"></a>Waarom kan ik geen catalogusspecifieke navigatiehiërarchie configureren of waarom zie ik geen optie om een klanthiërarchie te koppelen?

Zorg ervoor dat de functie **Gebruik van meerdere catalogi in detailhandelkanalen inschakelen** is ingeschakeld in de werkruimte **Functiebeheer** in Commerce Headquarters. In uw omgeving moet verder Commerce versie 10.0.27 of hoger worden gebruikt.

## <a name="can-i-view-the-catalog-specific-hierarchy-and-enrich-category-pages-in-commerce-site-builder"></a>Kan ik de catalogusspecifieke hiërarchie weergeven en categoriepagina's in Commerce Site Builder verrijken?

Ja, gebruikers van Commerce Site Builder die toegang hebben tot de pagina **Producten** in Site Builder kunnen een catalogus selecteren en de catalogusspecifieke hiërarchie weergeven. Vanaf de pagina **Producten** kunnen gebruikers ook een categoriepagina voor een specifieke categorie in de catalogus verrijken. Zie [Een landingspagina voor een categorie verrijken](enrich-category-page.md) voor meer informatie. Als u een catalogusspecifieke verrijking wilt hebben, raden we u aan om te zorgen voor een verschillende en unieke navigatiehiërarchie voor die catalogus.

## <a name="can-a-b2b-shopper-purchase-from-multiple-catalogs-in-a-single-checkout"></a>Kan een B2B-klant in meerdere catalogi kopen in één uitchecksessie?

Ja, aankopen in meerdere catalogi in één uitchecksessie zijn toegestaan. B2B-klanten kunnen de catalogusindicator in de winkelwagenweergave gebruiken om te bepalen welke artikelen uit welke catalogi zijn toegevoegd.

## <a name="if-a-b2b-shopper-purchases-the-same-item-from-different-catalogs-what-is-the-expected-behavior"></a>Wat is het verwachte gedrag als een B2B-klant hetzelfde artikel in verschillende catalogi koopt?

Hoewel een bepaalde gebruiker toegang kan hebben tot meerdere catalogi tegelijk, is het de verwachting dat producten in die catalogi elkaar uitsluiten. Met andere woorden zou hetzelfde product idealiter niet in meerdere catalogi voor een bepaalde gebruiker moeten zijn opgenomen.

Als zich echter een situatie voordoet waarbij hetzelfde product tot meerdere catalogi behoort, dan zal het systeem meerdere winkelwagenregels voor dat product onderhouden. Elke catalogus krijgt een aparte regel. Hetzelfde product uit twee verschillende catalogi wordt niet samengevoegd bij het uitchecken.

## <a name="when-a-b2b-shopper-is-shopping-is-there-any-validation-for-catalog-availability"></a>Is er een validatie voor de beschikbaarheid van catalogi voor B2B-klanten?

Ja. Een B2B-pagina mag alleen doorgaan met uitchecken als alle artikelen in de winkelwagen uit geldige catalogi komen. Als er winkelwagenartikelen uit vervallen of verouderde catalogi afkomstig zijn, worden deze verwijderd en wordt de gebruiker op de hoogte gebracht.

## <a name="during-the-shopping-experience-are-search-and-product-discovery-including-related-and-recommended-product-collections-catalog-specific"></a>Zijn de zoekfunctie en de productdetectie (inclusief verwante en aanbevolen productverzamelingen) catalogusspecifiek tijdens het winkelen?

Ja. Zodra een gebruiker een specifieke catalogus selecteert, wordt de hele winkelervaring catalogusspecifiek. Deze reis bevat detectie voor producten, zoals zoeksuggesties, zoekresultaten, categorieresultaten, verfijningen, prijzen, kenmerken en aanbevolen producten (zoals nieuwe, best verkopende, trending, vaak gekochte producten en gerelateerde producten).

## <a name="can-a-b2b-shopper-purchase-from-the-default-assortment-catalogid0"></a>Kan een B2B-klant kopen uit het standaardassortiment (catalogID=0)?

Nee, een B2B-klant mag niet inkopen uit het standaardassortiment. Dat assortiment is alleen bedoeld voor anoniem browsen. Als er catalogustoewijzingen ontbreken voor B2B-klanten (in afwachting van updates van hun administratie), kunnen ze geen catalogi zien waaruit ze kunnen kiezen en is er geen categoriehiërarchie zichtbaar.

## <a name="can-marketing-content-be-curated-for-a-product-that-is-specific-to-a-catalog"></a>Kan marketinginhoud worden samengesteld voor een product dat specifiek is voor een catalogus?

Op dit moment wordt productverrijking alleen ondersteund op site- en kanaalniveau. Met andere woorden, als een product wordt verrijkt, wordt het gedeeld over meerdere catalogi en wordt de bijbehorende pagina met productgegevens (PDP) voor dat product op dezelfde manier weergegeven in alle catalogi voor een bepaalde site.

## <a name="is-catalog-support-available-for-both-b2b-and-business-to-consumer-b2c-online-channels"></a>Is catalogusondersteuning beschikbaar voor online B2B- en B2C-kanalen (business-to-consumer) ?

Op dit moment zijn Commercecatalogi alleen bedoeld voor gebruik met B2B-kanalen.

## <a name="can-we-set-up-catalog-specific-upsellcross-sell-items"></a>Kunnen catalogusspecifieke meerverkoop en bijverkoop van artikelen worden ingesteld?

Momenteel wordt alleen de functionaliteit voor gerelateerde producten ondersteund. De configuraties voor meerverkoop en bijverkoop van artikelen zijn echter beschikbaar voor callcenters.

De volgende functies worden ook alleen ondersteund voor callcenters:

- Catalogusbroncodes
- De bron-id's gebruiken voor het bijhouden van kosten en responspercentages
- Catalogusspecifieke order- en artikelscripts
- Analyse van cataloguspagina's
- Catalogusaanvragen
- Betalingsschema's
- Gratis producten op basis van broncodes

## <a name="can-we-use-catalog-source-codes-for-b2b-orders-through-the-e-commerce-portal"></a>Kunnen we catalogusbroncodes voor B2B-orders gebruiken via de e-commerceportal?

Nummer Catalogusbroncodes worden alleen ondersteund voor callcenterkanalen.

## <a name="additional-resources"></a>Aanvullende bronnen

[Commercecatalogi maken voor B2B-sites](catalogs-b2b-sites.md)

[Impact van uitbreidbaarheid van Commerce-catalogi voor B2B-aanpassingen](catalogs-b2b-sites-dev.md)
