---
title: Acties en kortingen
description: Dit artikel bevat informatie over prijscorrecties en kortingen in Dynamics 365 Commerce.
author: scott-tucker
ms.date: 06/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 96a695df250cda514b7bd8b9716c0f03fb2bfd28d3af4daedaf1335c3099fbb6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748493"
---
# <a name="price-adjustments-and-discounts"></a>Acties en kortingen

[!include [banner](includes/banner.md)]

Dit artikel bevat informatie over prijscorrecties en kortingen in Dynamics 365 Commerce.

U kunt in Commerce prijscorrecties uitvoeren voor producten en ook kortingen instellen die worden toegepast op een regelartikel of een transactie bij het POS, in een callcenter-verkooporder of in een online order. Zowel prijscorrecties als kortingen kunnen aan prijsgroepen worden gekoppeld. Voor zowel prijscorrecties als kortingen kunt u een enkele begindatum en einddatum of een terugkerende periode, een kortingscode en enkele aanvullende kenmerken opgeven. 

Prijscorrecties en kortingen kunnen worden toegepast op producten, varianten of categorieën. Als meer dan één korting op een product van toepassing is, kan een klant een van de kortingen of een gecombineerde korting ontvangen, afhankelijk van de configuratie van de korting. In Commerce wordt automatisch de korting of combinatie van kortingen toegepast die de beste prijs voor de klant oplevert. Wanneer u een prijscorrectie of een korting instelt, moet u controleren of de prijsgroepen zijn toegewezen aan de juiste kanalen, catalogi, aansluitingen of loyaliteitsprogramma's voor het toepassen van de korting. Bovendien stelt u, als u automatisch de korting-id wilt genereren, nummerreeksen in op de pagina **Commerce-parameters** voordat u een nieuwe prijscorrectie of korting definieert.

> [!NOTE]
> U kunt een prijscorrectie of korting verwijderen. Statistische informatie gaat echter verloren.

## <a name="types-of-discounts"></a>Typen korting

Er zijn veel typen korting:

- **Eenvoudige korting** - Eén percentage of bedrag.
- **Hoeveelheidskorting** – Een korting die wordt toegepast wanneer twee of meer producten worden aangeschaft.
- **Combinatiekorting** – Een korting die wordt toegepast als een specifieke combinatie van producten wordt aangeschaft.
- **Drempelkorting** – Een korting die wordt toegepast wanneer het transactietotaal hoger is dan een bepaald bedrag.
- **Korting op basis van betalingsmethode** - een korting die wordt toegepast wanneer het transactietotaal meer dan een opgegeven bedrag is en een bepaalde betalingsmethode (bijvoorbeeld contant, creditcard of bankpas) wordt gebruikt voor de betaling.
- **Korting op verzendkosten** : een korting die wordt toegepast wanneer het transactietotaal meer is dan een opgegeven bedrag en een specifieke leveringsmethode (bijvoorbeeld een verzending van twee dagen of een nachtverzending) wordt gebruikt voor de order.

Zowel prijscorrecties als kortingen kunnen aan prijsgroepen worden gekoppeld. De prijsgroepen kunnen vervolgens aan kanalen, catalogi, aansluitingen en loyaliteitsprogramma's worden gekoppeld.

> [!NOTE]
> De combinatiekorting en de drempelkorting hebben de eigenschappen 'Niet-kortingsproducten tellen' en 'Niet-kortingsproducten tellen naar drempel'. Als deze eigenschappen zijn ingeschakeld, kan een artikel dat niet voor korting in aanmerking komt nog steeds een transactie kwalificeren voor de korting, maar krijgt het artikel dat niet in aanmerking komt de korting niet. 
> 
> Als u bijvoorbeeld een combinatiekorting met twee regels maakt, A en B, waarbij een klant 10% korting krijgt voor beide artikelen maar voor artikel A de configuratie 'Alle kortingen voorkomen' is ingeschakeld, wordt hierdoor meestal artikel A niet in de korting opgenomen. Als de eigenschap 'Niet-kortingsproducten tellen' echter is ingeschakeld, kan artikel A worden gebruikt voor kwalificatie voor de combinatiekorting. De korting van 10% wordt echter alleen toegepast op artikel B. Op de drempelkorting is vergelijkbare logica van toepassing. 
>
> De eigenschap 'Niet-kortingsproducten tellen naar drempel' heeft echter een extra mogelijkheid in vergelijking met de eigenschap 'Niet-kortingsproducten tellen' van de combinatiekortingen. Als de drempelkorting is ingeschakeld en als er een artikel met een bestaande korting is waarmee een artikel geen andere kortingen zou kunnen krijgen, kan de betaalde prijs voor dit artikel voldoen aan de drempel, maar krijgt dit artikel niet de aanvullende korting.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
