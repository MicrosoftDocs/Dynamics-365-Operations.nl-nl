---
title: Acties en kortingen
description: Dit artikel bevat informatie over prijscorrecties en kortingen in de detailhandel en commerce in Microsoft Dynamics 365 voor bewerkingen.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 01f249cbdabc6febf23dcd7103d4587cecdaad08
ms.lasthandoff: 03/31/2017


---

# <a name="price-adjustments-and-discounts"></a>Acties en kortingen

Dit artikel bevat informatie over prijscorrecties en kortingen in de detailhandel en commerce in Microsoft Dynamics 365 voor bewerkingen.

In Dynamics 365 for Operations - detailhandel, kunt u prijscorrecties producten, en kunnen ook kortingen instellen die worden toegepast op een regelartikel of een transactie bij het verkooppunt (POS) in een oproep center-verkooporder of in een on line bestelling. Zowel prijscorrecties als kortingen kunnen aan prijsgroepen worden gekoppeld. Voor zowel prijscorrecties als kortingen kunt u een enkele begindatum en einddatum of een terugkerende periode, een kortingscode en enkele aanvullende kenmerken opgeven. Prijscorrecties en kortingen kunnen worden toegepast op producten, varianten of categorieën. Als meer dan één korting op een product van toepassing is, kan een klant een van de kortingen of een gecombineerde korting ontvangen, afhankelijk van de configuratie van de korting. Dynamics 365 voor bewerkingen past u de korting of combinatie van de kortingen die aan de klant de beste prijs. Wanneer u een prijscorrectie of een korting instelt, moet u controleren of de prijsgroepen zijn toegewezen aan de juiste kanalen, catalogi, aansluitingen of loyaliteitsprogramma's voor het toepassen van de korting. Bovendien stelt u, als u automatisch de korting-id wilt genereren, nummerreeksen in op de pagina **Detailhandelparameters** voordat u een nieuwe prijscorrectie of korting definieert. **Opmerking:** U kunt een prijscorrectie of korting verwijderen. Statistische informatie gaat echter verloren.

### <a name="types-of-discounts"></a>Typen korting

Er zijn vier typen detailhandelkorting:

-   **Eenvoudige korting** - Eén percentage of bedrag.
-   **Hoeveelheidskorting** – Een korting die wordt toegepast wanneer twee of meer producten worden aangeschaft.
-   **Combinatiekorting** – Een korting die wordt toegepast als een specifieke combinatie van producten wordt aangeschaft.
-   **Drempelkorting** – Een korting die wordt toegepast wanneer het transactietotaal hoger is dan een bepaald bedrag.

Zowel prijscorrecties als kortingen kunnen aan prijsgroepen worden gekoppeld. De prijsgroepen kunnen vervolgens aan kanalen, catalogi, aansluitingen en loyaliteitsprogramma's worden gekoppeld.


