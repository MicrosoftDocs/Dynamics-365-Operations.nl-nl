---
title: Acties en kortingen
description: Dit artikel bevat informatie over prijscorrecties en kortingen in Detailhandel en commerce in Microsoft Dynamics 365 for Operations.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: a942f7876ab08598a019892056ce6be152d56985
ms.contentlocale: nl-nl
ms.lasthandoff: 05/25/2017


---

# <a name="price-adjustments-and-discounts"></a>Acties en kortingen

[!include[banner](includes/banner.md)]


Dit artikel bevat informatie over prijscorrecties en kortingen in Detailhandel en commerce in Microsoft Dynamics 365 for Operations.

In Dynamics 365 for Operations - Retail kunt u prijscorrecties voor producten doorvoeren en ook kortingen instellen die op een regelitem of transactie worden toegepast op het punt van verkoop (POS), in een verkooporder via een callcenter of in een online order. Zowel prijscorrecties als kortingen kunnen aan prijsgroepen worden gekoppeld. Voor zowel prijscorrecties als kortingen kunt u een enkele begindatum en einddatum of een terugkerende periode, een kortingscode en enkele aanvullende kenmerken opgeven. Prijscorrecties en kortingen kunnen worden toegepast op producten, varianten of categorieën. Als meer dan één korting op een product van toepassing is, kan een klant een van de kortingen of een gecombineerde korting ontvangen, afhankelijk van de configuratie van de korting. In Dynamics 365 for Operations wordt automatisch de korting of combinatie van kortingen toegepast die de beste prijs voor de klant oplevert. Wanneer u een prijscorrectie of een korting instelt, moet u controleren of de prijsgroepen zijn toegewezen aan de juiste kanalen, catalogi, aansluitingen of loyaliteitsprogramma's voor het toepassen van de korting. Bovendien stelt u, als u automatisch de korting-id wilt genereren, nummerreeksen in op de pagina **Detailhandelparameters** voordat u een nieuwe prijscorrectie of korting definieert. **Opmerking:** U kunt een prijscorrectie of korting verwijderen. Statistische informatie gaat echter verloren.

### <a name="types-of-discounts"></a>Typen korting

Er zijn vier typen detailhandelkorting:

-   **Eenvoudige korting** - Eén percentage of bedrag.
-   **Hoeveelheidskorting** – Een korting die wordt toegepast wanneer twee of meer producten worden aangeschaft.
-   **Combinatiekorting** – Een korting die wordt toegepast als een specifieke combinatie van producten wordt aangeschaft.
-   **Drempelkorting** – Een korting die wordt toegepast wanneer het transactietotaal hoger is dan een bepaald bedrag.

Zowel prijscorrecties als kortingen kunnen aan prijsgroepen worden gekoppeld. De prijsgroepen kunnen vervolgens aan kanalen, catalogi, aansluitingen en loyaliteitsprogramma's worden gekoppeld.




