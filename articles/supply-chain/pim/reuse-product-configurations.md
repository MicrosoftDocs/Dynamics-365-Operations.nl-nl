---
title: Productconfiguraties opnieuw gebruiken
description: U kunt opgeven dat u automatisch een bestaande configuratie voor een product wilt hergebruiken. Wanneer een gebruiker vervolgens een configuratiesessie voltooit, controleert het systeem of een configuratie overeenkomt met de bestaande selecties van de gebruiker. Als een overeenkomende configuratie wordt gevonden, worden de configuratie-ID, bijbehorende stuklijst (BOM) en de route hergebruikt.
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: c447440c33c1f80c6056974086b90d3b43e8499e
ms.contentlocale: nl-nl
ms.lasthandoff: 02/07/2018

---

# <a name="reuse-product-configurations"></a>Productconfiguraties opnieuw gebruiken

[!include [banner](../includes/banner.md)]

U kunt opgeven dat u automatisch een bestaande configuratie voor een product wilt hergebruiken. Wanneer een gebruiker vervolgens een configuratiesessie voltooit, controleert het systeem of een configuratie overeenkomt met de bestaande selecties van de gebruiker. Als een overeenkomende configuratie wordt gevonden, worden de configuratie-ID, bijbehorende stuklijst (BOM) en de route hergebruikt.

<a name="requirements-for-reusing-configurations"></a>Vereisten voor het hergebruik van configuraties
---------------------------------------

Als u wilt inschakelen dat configuraties opnieuw worden gebruikt, moet u de volgende informatie opgeven voor de componenten en kenmerken op de detailpagina **Productconfiguratiemodel**:

-   **Componenten en onderdelen**: selecteer op het sneltabblad **Algemeen** in het veld **Configuraties opnieuw gebruiken** de optie **Ja**.
-   **Kenmerken**: selecteer op het sneltabblad **Kenmerken** de optie **Opnemen in hergebruik**. Deze optie wordt alleen weergegeven als het bijbehorende onderdeel is ingeschakeld voor hergebruik. Als u niet alle kenmerken voor hergebruik selecteert, wordt de configuratie altijd opnieuw gebruikt, ongeacht de selecties van de gebruiker tijdens een configuratiesessie. De kenmerkwaarden in de bestaande configuratie moeten overeenkomen met de selecties van de gebruiker. Als de gebruiker bijvoorbeeld de kleur **blauw** selecteert tijdens een configuratiesessie, controleert het systeem of een bestaande configuratie van het onderdeel een kenmerk voor de kleur blauw heeft.

## <a name="resetting-configuration-reuse"></a>Hergebruik van configuratie opnieuw instellen
Wanneer u configuratiehergebruik opnieuw instelt, worden eerder gemaakte configuraties niet meer toegepast. U kunt configuratiehergebruik bijvoorbeeld opnieuw instellen als de stuklijst of de route is gewijzigd, maar geen gerelateerde kenmerken zijn gewijzigd. U stelt configuratiehergebruik in op het sneltabblad **Algemeen** voor de component.




