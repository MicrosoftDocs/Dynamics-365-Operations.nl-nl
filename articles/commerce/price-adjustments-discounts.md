---
title: Acties en kortingen
description: Dit artikel bevat informatie over prijscorrecties en kortingen in Dynamics 365 Commerce.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: dfaacfa7681258e3b2273083017c0c398d566651
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022178"
---
# <a name="price-adjustments-and-discounts"></a>Acties en kortingen

[!include [banner](includes/banner.md)]

Dit artikel bevat informatie over prijscorrecties en kortingen in Dynamics 365 Commerce.

U kunt in Commerce prijscorrecties uitvoeren voor producten en ook kortingen instellen die worden toegepast op een regelartikel of een transactie bij het POS, in een callcenter-verkooporder of in een online order. Zowel prijscorrecties als kortingen kunnen aan prijsgroepen worden gekoppeld. Voor zowel prijscorrecties als kortingen kunt u een enkele begindatum en einddatum of een terugkerende periode, een kortingscode en enkele aanvullende kenmerken opgeven. 

Prijscorrecties en kortingen kunnen worden toegepast op producten, varianten of categorieën. Als meer dan één korting op een product van toepassing is, kan een klant een van de kortingen of een gecombineerde korting ontvangen, afhankelijk van de configuratie van de korting. In Commerce wordt automatisch de korting of combinatie van kortingen toegepast die de beste prijs voor de klant oplevert. Wanneer u een prijscorrectie of een korting instelt, moet u controleren of de prijsgroepen zijn toegewezen aan de juiste kanalen, catalogi, aansluitingen of loyaliteitsprogramma's voor het toepassen van de korting. Bovendien stelt u, als u automatisch de korting-id wilt genereren, nummerreeksen in op de pagina **Commerce-parameters** voordat u een nieuwe prijscorrectie of korting definieert.

> [!NOTE]
> U kunt een prijscorrectie of korting verwijderen. Statistische informatie gaat echter verloren.

## <a name="types-of-discounts"></a>Typen korting

Er zijn vier typen korting:

- **Eenvoudige korting** - Eén percentage of bedrag.
- **Hoeveelheidskorting** – Een korting die wordt toegepast wanneer twee of meer producten worden aangeschaft.
- **Combinatiekorting** – Een korting die wordt toegepast als een specifieke combinatie van producten wordt aangeschaft.
- **Drempelkorting** – Een korting die wordt toegepast wanneer het transactietotaal hoger is dan een bepaald bedrag.

Zowel prijscorrecties als kortingen kunnen aan prijsgroepen worden gekoppeld. De prijsgroepen kunnen vervolgens aan kanalen, catalogi, aansluitingen en loyaliteitsprogramma's worden gekoppeld.
