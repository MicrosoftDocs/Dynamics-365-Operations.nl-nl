---
title: "Een vergoedingenprogramma definiëren en beheren"
description: Human resources biedt een reeks hulpmiddelen die kunnen worden gebruikt om vergoedingen, kortingen en compensatieplannen van werknemers die een organisatie zijn werknemers biedt in te stellen en onderhouden. Dit artikel biedt informatie over het instellen en beheren van vergoedingen.
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 1d972f2d6bacf6f60ab3ce3bab2fcfaeb8d2e524
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="define-and-manage-a-benefits-program"></a>Een vergoedingenprogramma definiëren en beheren

[!include[banner](includes/banner.md)]


Human resources biedt een reeks hulpmiddelen die kunnen worden gebruikt om vergoedingen, kortingen en compensatieplannen van werknemers die een organisatie zijn werknemers biedt in te stellen en onderhouden. Dit onderwerp biedt informatie over het instellen en beheren van vergoedingen.

<a name="benefit-setup"></a>Vergoedingen instellen
-------------

Voordat werknemers voor vergoedingen kunnen worden geregistreerd, moet u de elementen van elke vergoeding maken. Deze elementen combineren vergelijkbare vergoedingsplannen en definiëren standaardinstellingen, zoals inhoudingstarieven en boekhoudingsdetails. Veel van deze instellingen kunnen worden aangepast wanneer werknemers later in de vergoeding worden geregistreerd. Voor elk vergoedingsplan kan een organisatie meerdere inschrijvingopties aanbieden. Een werknemer kan inschrijving in de planning kwijtschelden. 

[![Processtroom van vergoeding](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Vergoedingselementen
Voordat u vergoedingen begint te maken en daar werknemers voor wilt inschrijven, moet u de elementen definiëren waaruit een vergoeding bestaat: het type, het plan en de opties.

-   **Type** – Een verzameling van plannen voor een bepaalde vergoeding, zoals een medische of parkeervergoeding.
-   **Plan** – Een bepaalde vergoeding van een leverancier.
-   **Optie** – Het dekkingsniveau, zoals alleen werknemer, of werknemer en echtgeno(o)t(e)/partner.

Voor elk type vergoeding, zoals zicht- of tandartsverzekering, kan een organisatie zijn werknemers een of meerdere plannen aanbieden. Voor elk plan kan de organisatie verschillende opties bieden. Werknemers kunnen bijvoorbeeld extra levensverzekeringdekking kopen van één, twee of drie keer hun jaarlijks salaris. Elke combinatie van een plan en opties wordt een vergoeding waarvoor werknemers zich kunnen inschrijven. 

[![afbeelding vegoeding](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Geschiktheid
Veel factoren bepalen de geschiktheid van werknemers voor de diverse soorten vergoedingen die een werkgever aanbiedt. Wanneer u een vergoeding maakt in Microsoft Dynamics 365 for Operations, kunt u het type van geschiktheid instellen dat op die vergoeding van toepassing is. 

U kunt een vergoeding beschikbaar maken voor alle werknemers. Sommige bedrijven bieden bijvoorbeeld alle werknemers parkeervergunningen aan als vergoeding. Wanneer u deze vergoeding maakt, stelt u de geschiktheid in op **Alle medewerkers komen in aanmerking**. 

Voor andere vergoedingen, zoals aanmoedigingen en belastingheffingen, geldt de geschiktheid niet. Wanneer u deze soorten vergoedingen maakt, stelt u de geschiktheid in op **Geschiktheidsproces overslaan**. 

Tot slot kan de geschiktheid voor vergoeding regelgebaseerd zijn. Een bedrijf biedt werknemers bijvoorbeeld twee typen levensverzekeringsvergoeding. Stafleden komen in aamerking voor één levensverzekeringsplan, terwijl alle andere voltijds werkende werknemers in aanmerking komen voor het andere levensverzekeringsplan. In Dynamics 365 for Operations kunt u een geschiktheidsregel van een vergoeding maken om alle stafleden te vinden en een andere regel om alle andere voltijds werkende werknemers te vinden, en vervolgens die regels toepassen op de juiste vergoeding.

## <a name="enrollment"></a>Inschrijving
Nadat u de vergoedingen hebt gemaakt die uw organisatie aanbiedt en de geschiktheid hebt bepaald, kunt u werknemers inschrijven voor de vergoedingen. U kunt één werknemer inschrijven voor vergoedingen of u kunt in één proces meerdere werknemers inschrijven voor een of meerdere vergoedingen. 

Soms stopt een organisatie met het aanbieden van bepaalde vergoedingen. In dit geval moet u de vergoeding en werknemers die ervoor zijn ingeschreven bijwerken. Met massaal vergoedingsverval kunt u de vervaldatum van zowel een vergoeding als de inschrijvingen van werknemers voor die vergoeding tegelijk wijzigen. U kunt ook meerdere werknemers selecteren die in een vergoeding zijn ingeschreven en de einddatum van hun dekking wijzigen. 

Op dezelfde manier kunt u met massale verlenging van vergoedingen de vervaldatum van zowel een vergoeding als de inschrijvingen van werknemers voor die vergoeding verlengen als u beslist om een vergoeding langer aan te bieden dan u oorspronkelijk had gepland.

<a name="see-also"></a>Zie ook
--------

[Beleid voor geschiktheid vergoedingen](benefit-eligibility-policies.md)




