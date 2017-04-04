---
title: Productconfiguraties hergebruiken
description: U kunt opgeven dat u automatisch een bestaande configuratie voor een product wilt hergebruiken. Wanneer een gebruiker vervolgens een configuratiesessie voltooit, controleert het systeem of een configuratie overeenkomt met de bestaande selecties van de gebruiker. Als een overeenkomende configuratie wordt gevonden, worden de configuratie-ID, bijbehorende stuklijst (BOM) en de route hergebruikt.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: a846c5fee2736fb8f137f7c2bdd759be43220d14
ms.lasthandoff: 03/31/2017


---

# <a name="reuse-product-configurations"></a>Productconfiguraties hergebruiken

U kunt opgeven dat u automatisch een bestaande configuratie voor een product wilt hergebruiken. Wanneer een gebruiker vervolgens een configuratiesessie voltooit, controleert het systeem of een configuratie overeenkomt met de bestaande selecties van de gebruiker. Als een overeenkomende configuratie wordt gevonden, worden de configuratie-ID, bijbehorende stuklijst (BOM) en de route hergebruikt.

<a name="requirements-for-reusing-configurations"></a>Vereisten voor het hergebruik van configuraties
---------------------------------------

Als u wilt inschakelen dat configuraties opnieuw worden gebruikt, moet u de volgende informatie opgeven voor de componenten en kenmerken op de detailpagina **Productconfiguratiemodel**:

-   **Componenten en onderdelen**: selecteer op het sneltabblad **Algemeen** in het veld **Configuraties opnieuw gebruiken** de optie **Ja**.
-   **Kenmerken**: selecteer op het sneltabblad **Kenmerken** de optie **Opnemen in hergebruik**. Deze optie wordt alleen weergegeven als het bijbehorende onderdeel is ingeschakeld voor hergebruik. Als u niet alle kenmerken voor hergebruik selecteert, wordt de configuratie altijd opnieuw gebruikt, ongeacht de selecties van de gebruiker tijdens een configuratiesessie. De kenmerkwaarden in de bestaande configuratie moeten overeenkomen met de selecties van de gebruiker. Als de gebruiker bijvoorbeeld de kleur **blauw** selecteert tijdens een configuratiesessie, controleert het systeem of een bestaande configuratie van het onderdeel een kenmerk voor de kleur blauw heeft.

## <a name="resetting-configuration-reuse"></a>Hergebruik van configuratie opnieuw instellen
Wanneer u configuratiehergebruik opnieuw instelt, worden eerder gemaakte configuraties niet meer toegepast. U kunt configuratiehergebruik bijvoorbeeld opnieuw instellen als de stuklijst of de route is gewijzigd, maar geen gerelateerde kenmerken zijn gewijzigd. U stelt configuratiehergebruik in op het sneltabblad **Algemeen** voor de component.


