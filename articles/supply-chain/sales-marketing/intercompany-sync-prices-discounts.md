---
title: Intercompany-prijzen en -kortingen synchroniseren
description: In dit artikel wordt de synchronisatie van prijzen en kortingen voor intercompany-verkooporders en -inkooporders uitgelegd.
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 64130c400212a819f931cc36459667e4d7c83f32
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905684"
---
# <a name="synchronize-intercompany-prices-and-discounts"></a>Intercompany-prijzen en -kortingen synchroniseren

[!include [banner](../../includes/banner.md)]

Kortingen en prijzen worden altijd gesynchroniseerd tussen de intercompany-verkooporder en de intercompany-inkooporder. U kunt ook de prijs en kortingen naar of van de oorspronkelijke verkooporder synchroniseren, zodat op alle orders altijd dezelfde prijzen en kortingen worden weergegeven. U doet dit vanaf de pagina **Intercompany** die u kunt openen via het tabblad **Algemeen** op de lijstpagina **Alle klanten** vanuit **Verkoop en marketing** of vanuit **Inkoopbeheer**.

Het veld **Prijs en korting** wordt gesynchroniseerd naar de intercompany-verkooporderregel. Als u dus het veld **Bewerking van prijs toestaan** en het veld **Bewerking van korting toestaan** selecteert, staat u wijzigingen tussen de intercompany-verkooporder en de intercompany-inkooporder toe. Een wijziging in de eenheidsprijs, de prijseenheid of de verkooptoeslag op de intercompany-verkooporder bepaalt de prijs op de intercompany-inkooporderregel.

Als de velden **Bewerking van prijs toestaan** en **Bewerking van korting toestaan** zijn ingeschakeld op de intercompany-verkooporder of de intercompany-inkooporder, kunt u de prijs of korting op beide orders handmatig wijzigen. Als deze velden niet zijn geselecteerd, kunt u dit niet.

Als de velden **Bewerking van prijs toestaan** en **Bewerking van korting toestaan** niet zijn ingeschakeld op de intercompany-verkooporder, kunt u de prijs (of de toeslagen) of korting niet handmatig op een intercompany-verkooporder wijzigen.

Als de velden **Bewerking van prijs toestaan** en **Bewerking van korting toestaan** niet zijn ingeschakeld op de intercompany-inkooporder, kunt u de prijs (of de toeslagen) of korting niet handmatig op een intercompany-inkooporder wijzigen.

Als de velden **Bewerking van prijs toestaan** en **Bewerking van korting toestaan** zijn ingeschakeld op zowel de intercompany-inkooporder als de intercompany-verkooporder, kunt u beide orders handmatig wijzigen. Dit kan echter leiden tot een situatie waarin updates die door de ene persoon zijn doorgevoerd, worden overschreven door updates die door een andere persoon in een ander bedrijf worden doorgevoerd op dezelfde order.

> [!NOTE]
> Als u het veld **Prijs en korting** hebt ingeschakeld op zowel de intercompany-inkooporder als op de intercompany-verkooporder, hebt u geen controle over de prijzen.

Om dergelijke conflicten te voorkomen is het raadzaam om toe te staan dat prijzen en kortingen alleen op de intercompany-verkooporder of de intercompany-inkooporder kunnen worden gewijzigd. Hiervoor moet u de velden **Prijs bewerken toestaan** en **Korting bewerken toestaan** op een van deze orders inschakelen.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
