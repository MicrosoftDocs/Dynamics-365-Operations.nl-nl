---
title: Productconfiguraties opnieuw gebruiken
description: U kunt opgeven dat u automatisch een bestaande configuratie voor een product wilt hergebruiken. Wanneer een gebruiker vervolgens een configuratiesessie voltooit, controleert het systeem of een configuratie overeenkomt met de bestaande selecties van de gebruiker. Als een overeenkomende configuratie wordt gevonden, worden de configuratie-ID, bijbehorende stuklijst (BOM) en de route hergebruikt.
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fb4c997e8cf8b2456ffe12a552577902da171cc1
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189839"
---
# <a name="reuse-product-configurations"></a>Productconfiguraties opnieuw gebruiken

[!include [banner](../includes/banner.md)]

U kunt opgeven dat u automatisch een bestaande configuratie voor een product wilt hergebruiken. Wanneer een gebruiker vervolgens een configuratiesessie voltooit, controleert het systeem of een configuratie overeenkomt met de bestaande selecties van de gebruiker. Als een overeenkomende configuratie wordt gevonden, worden de configuratie-ID, bijbehorende stuklijst (BOM) en de route hergebruikt.

## <a name="requirements-for-reusing-configurations"></a>Vereisten voor het hergebruik van configuraties

Als u wilt inschakelen dat configuraties opnieuw worden gebruikt, moet u de volgende informatie opgeven voor de componenten en kenmerken op de detailpagina **Productconfiguratiemodel**:

-   **Componenten en onderdelen**: selecteer op het sneltabblad **Algemeen** in het veld **Configuraties opnieuw gebruiken** de optie **Ja**.
-   **Kenmerken**: selecteer op het sneltabblad **Kenmerken** de optie **Opnemen in hergebruik**. Deze optie wordt alleen weergegeven als het bijbehorende onderdeel is ingeschakeld voor hergebruik. Als u niet alle kenmerken voor hergebruik selecteert, wordt de configuratie altijd opnieuw gebruikt, ongeacht de selecties van de gebruiker tijdens een configuratiesessie. De kenmerkwaarden in de bestaande configuratie moeten overeenkomen met de selecties van de gebruiker. Als de gebruiker bijvoorbeeld de kleur **blauw** selecteert tijdens een configuratiesessie, controleert het systeem of een bestaande configuratie van het onderdeel een kenmerk voor de kleur blauw heeft.

## <a name="resetting-configuration-reuse"></a>Hergebruik van configuratie opnieuw instellen
Wanneer u configuratiehergebruik opnieuw instelt, worden eerder gemaakte configuraties niet meer toegepast. U kunt configuratiehergebruik bijvoorbeeld opnieuw instellen als de stuklijst of de route is gewijzigd, maar geen gerelateerde kenmerken zijn gewijzigd. U stelt configuratiehergebruik in op het sneltabblad **Algemeen** voor de component.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]