---
title: "Definiëren en beheren van een programma vergoedingen"
description: Human resources biedt een reeks hulpmiddelen die kunnen worden gebruikt om vergoedingen, kortingen en compensatieplannen van werknemers die een organisatie zijn werknemers biedt in te stellen en onderhouden. Dit artikel biedt informatie over het instellen en beheren van vergoedingen.
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 81b5c9056001b26c33b2b42a95711ff5b50243e6
ms.openlocfilehash: 9d00d8f6dfa075f53473af31c257deb57c9efa86
ms.lasthandoff: 03/31/2017


---

# <a name="define-and-manage-a-benefits-program"></a>Definiëren en beheren van een programma vergoedingen

Human resources biedt een reeks hulpmiddelen die kunnen worden gebruikt om vergoedingen, kortingen en compensatieplannen van werknemers die een organisatie zijn werknemers biedt in te stellen en onderhouden. Dit onderwerp biedt informatie over het instellen van een vergoedingen beheren.

<a name="benefit-setup"></a>Vergoedingsinstellingen
-------------

Voordat werknemers voor vergoedingen kunnen worden geregistreerd, moet u de elementen van elke vergoeding maken. Deze elementen combineren vergelijkbare vergoedingsplannen en definiëren standaardinstellingen, zoals inhoudingstarieven en boekhoudingsdetails. Veel van deze instellingen kunnen worden aangepast wanneer werknemers later in de vergoeding worden geregistreerd. Voor elk vergoedingsplan kan een organisatie meerdere inschrijvingopties aanbieden. Een werknemer kan inschrijving in de planning kwijtschelden. 

[![Processtroom voor vergoeding](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)

## <a name="benefit-elements"></a>Vergoedingselementen
Voordat u vergoedingen begint te maken en daar werknemers voor wilt inschrijven, moet u de elementen definiëren waaruit een vergoeding bestaat: het type, het plan en de opties.

-   **Type** – Een verzameling van plannen voor een bepaalde vergoeding, zoals een medische of parkeervergoeding.
-   **Plan** – Een bepaalde vergoeding van een leverancier.
-   **Optie** – Het dekkingsniveau, zoals alleen werknemer, of werknemer en echtgeno(o)t(e)/partner.

Voor elk type vergoeding, zoals zicht- of tandartsverzekering, kan een organisatie zijn werknemers een of meerdere plannen aanbieden. Voor elk plan kan de organisatie verschillende opties bieden. Werknemers kunnen bijvoorbeeld extra levensverzekeringdekking kopen van één, twee of drie keer hun jaarlijks salaris. Elke combinatie van een plan en opties wordt een vergoeding waarvoor werknemers zich kunnen inschrijven. 

[![vergoeding pic](./media/benefit-pic.png)](./media/benefit-pic.png)

## <a name="eligibility"></a>Geschiktheid
Veel factoren bepalen de geschiktheid van werknemers voor de diverse soorten vergoedingen die een werkgever aanbiedt. Wanneer u een vergoeding in Microsoft Dynamics 365 voor bewerkingen maakt, kunt u het type recht dat voor die vergoeding geldt kunt instellen. 

U kunt een vergoeding beschikbaar maken voor alle werknemers. Sommige bedrijven bieden bijvoorbeeld parkeren stappen voor alle werknemers als een vergoedingen. Wanneer u deze vergoeding maakt, stelt u de geschiktheid in op **Alle medewerkers komen in aanmerking**. 

In aanmerking komen voor andere voordelen, zoals aanmoedigingen en fiscale heffingen niet van toepassing. Wei u dergelijke vergoedingen maken, u het recht ingesteld op **overslaan geschiktheidsproces**. 

Ten slotte, geschiktheid voor vergoeding kan worden op basis van een regel. Een bedrijf biedt bijvoorbeeld twee soorten levensverzekering vergoeding aan werknemers. Directie werknemers in aanmerking komen voor een levensverzekering plan, terwijl andere fulltime werknemers in aanmerking voor de andere regeling van de levensverzekering komen. In Dynamics 365 voor bewerkingen, kunt u een geschiktheidsregel vergoeding kunt u zoeken naar alle werknemers van de Directie en een andere regel kunt u zoeken naar andere fulltime werknemers maken en vervolgens deze regels toepassen op de juiste vergoeding.

## <a name="enrollment"></a>Inschrijving
Nadat u de vergoedingen hebt gemaakt die uw organisatie aanbiedt en de geschiktheid hebt bepaald, kunt u werknemers inschrijven voor de vergoedingen. U kunt één werknemer inschrijven voor vergoedingen of u kunt in één proces meerdere werknemers inschrijven voor een of meerdere vergoedingen. 

Soms stopt een organisatie met het aanbieden van bepaalde vergoedingen. In dit geval moet u de vergoeding en de werknemers die zijn ingeschreven voor bijwerken. Massaal vergoeding vervaldatum kunt u de vervaldatum van een vergoeding en van de inschrijvingen van de werknemer voor die vergoeding op hetzelfde moment wijzigen. U kunt ook meerdere werknemers selecteren die in een vergoeding zijn ingeschreven en de einddatum van hun dekking wijzigen. 

Op dezelfde manier kunt u met massale verlenging van vergoedingen de vervaldatum van zowel een vergoeding als de inschrijvingen van werknemers voor die vergoeding verlengen als u beslist om een vergoeding langer aan te bieden dan u oorspronkelijk had gepland.

<a name="see-also"></a>Zie ook
--------

[Benefit eligibility policies](benefit-eligibility-policies.md)


