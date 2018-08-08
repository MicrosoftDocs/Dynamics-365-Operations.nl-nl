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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 18a3e5fb583ed620c825164f2628a26b6b0cb469
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---

# <a name="reuse-product-configurations"></a><span data-ttu-id="b96ba-105">Productconfiguraties opnieuw gebruiken</span><span class="sxs-lookup"><span data-stu-id="b96ba-105">Reuse product configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b96ba-106">U kunt opgeven dat u automatisch een bestaande configuratie voor een product wilt hergebruiken.</span><span class="sxs-lookup"><span data-stu-id="b96ba-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="b96ba-107">Wanneer een gebruiker vervolgens een configuratiesessie voltooit, controleert het systeem of een configuratie overeenkomt met de bestaande selecties van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="b96ba-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="b96ba-108">Als een overeenkomende configuratie wordt gevonden, worden de configuratie-ID, bijbehorende stuklijst (BOM) en de route hergebruikt.</span><span class="sxs-lookup"><span data-stu-id="b96ba-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="b96ba-109">Vereisten voor het hergebruik van configuraties</span><span class="sxs-lookup"><span data-stu-id="b96ba-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="b96ba-110">Als u wilt inschakelen dat configuraties opnieuw worden gebruikt, moet u de volgende informatie opgeven voor de componenten en kenmerken op de detailpagina **Productconfiguratiemodel**:</span><span class="sxs-lookup"><span data-stu-id="b96ba-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="b96ba-111">**Componenten en onderdelen**: selecteer op het sneltabblad **Algemeen** in het veld **Configuraties opnieuw gebruiken** de optie **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b96ba-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="b96ba-112">**Kenmerken**: selecteer op het sneltabblad **Kenmerken** de optie **Opnemen in hergebruik**.</span><span class="sxs-lookup"><span data-stu-id="b96ba-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="b96ba-113">Deze optie wordt alleen weergegeven als het bijbehorende onderdeel is ingeschakeld voor hergebruik.</span><span class="sxs-lookup"><span data-stu-id="b96ba-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="b96ba-114">Als u niet alle kenmerken voor hergebruik selecteert, wordt de configuratie altijd opnieuw gebruikt, ongeacht de selecties van de gebruiker tijdens een configuratiesessie.</span><span class="sxs-lookup"><span data-stu-id="b96ba-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="b96ba-115">De kenmerkwaarden in de bestaande configuratie moeten overeenkomen met de selecties van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="b96ba-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="b96ba-116">Als de gebruiker bijvoorbeeld de kleur **blauw** selecteert tijdens een configuratiesessie, controleert het systeem of een bestaande configuratie van het onderdeel een kenmerk voor de kleur blauw heeft.</span><span class="sxs-lookup"><span data-stu-id="b96ba-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="b96ba-117">Hergebruik van configuratie opnieuw instellen</span><span class="sxs-lookup"><span data-stu-id="b96ba-117">Resetting configuration reuse</span></span>
<span data-ttu-id="b96ba-118">Wanneer u configuratiehergebruik opnieuw instelt, worden eerder gemaakte configuraties niet meer toegepast.</span><span class="sxs-lookup"><span data-stu-id="b96ba-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="b96ba-119">U kunt configuratiehergebruik bijvoorbeeld opnieuw instellen als de stuklijst of de route is gewijzigd, maar geen gerelateerde kenmerken zijn gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="b96ba-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="b96ba-120">U stelt configuratiehergebruik in op het sneltabblad **Algemeen** voor de component.</span><span class="sxs-lookup"><span data-stu-id="b96ba-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>




