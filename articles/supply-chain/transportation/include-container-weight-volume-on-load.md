---
title: Containergewicht en -volume in lading opnemen
description: In dit onderwerp wordt beschreven hoe u functionaliteit instelt en toepast om containergewicht en -volume in ladingen op te nemen.
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b137db6f67da30d6ac3a973940c1df1fd7268a1a
ms.openlocfilehash: ac1df9b430feb025e4a544a7ecd7baa0c919cbe4
ms.contentlocale: nl-nl
ms.lasthandoff: 10/02/2017

---

# <a name="include-container-weight-and-volume-on-load"></a>Containergewicht en -volume in lading opnemen

[!include[banner](../includes/banner.md)]

De functionaliteit voor het opnemen van het containergewicht en -volume in een lading geeft een duidelijk beeld van het totale gewicht en volume van containers en artikelen in een lading.

Een lading bevat een enkele zending of meerdere zendingen en deze zendingen bevatten bepaalde artikelen die tot één verkooporder of meerdere verkooporders behoren. De artikelen zijn opgeslagen in een container en containers worden in een lading geladen. Artikelen buiten een container kunnen ook deel uitmaken van een lading. Op basis van deze voorwaarden berekent het systeem waarden voor het gewicht en volume van de lading door rekening te houden met het gewicht en volume van de containers en artikelen.

Als de berekende waarden niet nauwkeurig zijn, kunt u deze aanpassen door de werkelijke waarden voor het gewicht en volume in de lading in te voeren. De waarden voor het gewicht en volume worden gebruikt in transportbeheerprocessen. De waarden worden bijvoorbeeld gebruikt in de tariefroute-workbench, waar ze helpen bij het definiëren van het tarief en de route voor ladingen. Daarnaast worden ze gebruikt voor transportbetalingsmethoden en het inchecken van de chauffeur.

## <a name="where-it-applies"></a>Waar van toepassing

De functionaliteit voor het opnemen van het containergewicht en -volume in een lading wordt toegepast in transportbeheerprocessen, zoals de tariefroute-workbench, transportbetalingsmethoden en het inchecken van de chauffeur.

## <a name="how-it-is-set-up"></a>De instelling

Het aantal containers voor een lading wordt berekend op basis van het gewicht en volume van de container en het percentage van de container dat wordt gebruikt.

-   Als u het gewicht en volume voor een container wilt instellen, klikt u op **Magazijnbeheer** \> **Instellingen** \> **Containers** \> **Containertypen**.

-   U stelt het containergebruikspercentage in door te klikken op **Magazijnbeheer** \> **Instellingen** \> **Containers** \> **Containergroepen** en een waarde in te voeren in het veld **Containergebruikspercentage**.

