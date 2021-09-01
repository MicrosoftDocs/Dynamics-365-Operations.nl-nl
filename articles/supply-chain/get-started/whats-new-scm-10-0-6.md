---
title: Wat is nieuw of gewijzigd in Dynamics 365 Supply Chain Management 10.0.6 (november 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Supply Chain Management 10.0.6.
author: josaw1
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: d72bc060685fa5d4bd49043a29249717786e2b46b5572f2b127023e016ba4c49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773460"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 Supply Chain Management 10.0.6 (november 2019)

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Supply Chain Management 10.0.6. Deze versie heeft buildnummer 10.0.234. Hoewel de datum voor algemene beschikbaarheid in november is, zijn de nieuwe functies beschikbaar voor vroege vrijgave in oktober. Zie voor meer informatie over versie 10.0.6 [Aanvullende resources](whats-new-scm-10-0-6.md#additional-resources).

## <a name="product-configuration-models-v2-data-entity"></a>V2 van gegevensentiteit productconfiguratiemodellen

Er wordt een tweede versie voor de gegevensentiteit productconfiguratiemodellen vrijgegeven (productconfiguratiemodellen V2). Voor de standaardsjabloon 418-productconfiguratiemodellen moet ook de nieuwe gegevensentiteit productconfiguratiemodellen V2 worden gebruikt in de import- en exportraamwerksjablonen. De sjabloon wordt niet automatisch bijgewerkt, zodat u de sjabloon handmatig op basis van de standaard moet laden. De V2-entiteit exporteert één rij als afzonderlijk bestand in een bijlage in plaats van inline, waarbij de groottebeperkingen van de V1-entiteit worden opgelost. 
 
Wat moet u doen om deze wijziging door te voeren?
-    Aangezien de V1-entiteit is afgeschaft, moet u beginnen met de migratie van V1 naar V2. Als u de sjabloon 418-productconfiguratiemodellen gebruikt, kunt u op de knop standaardsjablonen laden klikken en de sjabloon 418-productconfiguratiemodellen opnieuw laden.
-    Als u de compatibiliteit met bestaande systemen wilt behouden, kunt u voorlopig de bestaande sjabloon en de (afgeschafte) V1-entiteit blijven gebruiken totdat u uw integraties naar de nieuwe sjabloon verplaatst. 

## <a name="feature-management-enhancements"></a>Verbeteringen in Functiebeheer
Met Functiebeheer kunt u nu standaard alle nieuwe functies inschakelen, bevestiging vereisen om een functie in te schakelen en alle functies inschakelen die nog niet zijn ingeschakeld. 


## <a name="purchase-agreement-responsible-party"></a>Verantwoordelijke partij voor inkoopovereenkomst
U hebt nu de mogelijkheid om primaire en secundaire verantwoordelijke partijen te definiëren in het formulier Classificatie van inkoopovereenkomst en resulterende inkoopovereenkomsten.  Zo krijgt de gebruiker toegang tot de gebruiker die de overeenkomsten overziet.

## <a name="rfq-link-on-the-purchase-order-line"></a>De koppeling Offerteaanvraag op de inkooporderregel
U kunt vanuit de inkooporderregels een verwijzingskoppeling toevoegen die weer verwijst naar de offerteaanvraagregels waaruit deze afkomstig zijn, zodat de gebruiker eenvoudig kan worden voorzien van het ondersteunende offertedocument.

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="bug-fixes"></a>Correcties
Voor informatie over de correcties die zijn opgenomen in alle updates die deel uitmaken van 10.0.6, meldt u zich aan bij Lifecycle Services (LCS) en bekijkt u het [KB-artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).

### <a name="platform-update-30"></a>Platformupdate 30
Microsoft Dynamics 365 Supply Chain Management 10.0.6 bevat platformupdate 30. Zie [Nieuw of gewijzigd in platformupdate 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md) voor meer informatie over platformupdate 30.

### <a name="dynamics-365-2019-release-wave-2-plan"></a>Dynamics 365: releasewave 2-plan van 2019
Bent u benieuwd naar de komende en onlangs uitgebrachte voorzieningen in een van onze bedrijfsapps of platforms?

Bekijk [Dynamics 365: releasewave 2-plan van 2019](/dynamics365-release-plan/2019wave2/). We hebben alle details in één document verzameld die u kunt gebruiken voor uw planning.

### <a name="removed-and-deprecated-supply-chain-management-features"></a>Verwijderde en afgeschafte functies voor Supply Chain Management

In het onderwerp [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) worden functies beschreven die zijn of worden verwijderd voor Supply Chain Management.

- Een *verwijderde* functie is niet langer beschikbaar in het product.
- Een *afgeschafte* functie wordt niet meer actief ontwikkeld en kan in een toekomstige update worden verwijderd.

Twaalf maanden voordat een functie uit het product wordt verwijderd, wordt de afschaffing aangekondigd in het onderwerp [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md).

Voor ingrijpende wijzigingen die alleen van invloed zijn op de compilatietijd, maar binair compatibel zijn met sandbox- en productieomgevingen, is de afschaffingstijd korter dan 12 maanden. Meestal zijn dit functionele updates die moeten worden doorgevoerd in de compiler.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]