---
title: Configuratieregels
description: "Dit artikel geeft algemene informatie over configuratieregels. Configuratieregels definiëren relaties tussen artikelen in een stuklijst (BOM) voor producten die op dimensies gebaseerde configuratietechnologie gebruiken."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 19761
ms.assetid: e4c6622d-1e2d-4a4d-8047-c553a25d4f87
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 37f70d2620023915b23425d41dfb0043ef856492
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="configuration-rules"></a><span data-ttu-id="86fac-104">Configuratieregels</span><span class="sxs-lookup"><span data-stu-id="86fac-104">Configuration rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="86fac-105">Dit artikel geeft algemene informatie over configuratieregels.</span><span class="sxs-lookup"><span data-stu-id="86fac-105">This article provides general information about configuration rules.</span></span> <span data-ttu-id="86fac-106">Configuratieregels definiëren relaties tussen artikelen in een stuklijst (BOM) voor producten die op dimensies gebaseerde configuratietechnologie gebruiken.</span><span class="sxs-lookup"><span data-stu-id="86fac-106">Configuration rules define relationships between items in a bill of materials (BOM) for products that use the dimension-based configuration technology.</span></span>

<span data-ttu-id="86fac-107">Configuratieregels zijn beschikbaar wanneer u op dimensies gebaseerde configuratiemodellen definieert.</span><span class="sxs-lookup"><span data-stu-id="86fac-107">Configuration rules are available when you define dimension-based configuration models.</span></span> <span data-ttu-id="86fac-108">Configuratieregels worden gebruikt om specifieke artikelcombinaties in een stuklijst af te dwingen of te verbieden.</span><span class="sxs-lookup"><span data-stu-id="86fac-108">Configuration rules are used to either enforce or prohibit specific item combinations in a bill of materials (BOM).</span></span> <span data-ttu-id="86fac-109">Nadat een stuklijst is gemaakt en de relevante artikelen aan hun respectievelijke configuratiegroepen zijn toegewezen, kunnen een of meer configuratieregels worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="86fac-109">After a BOM has been created and the relevant items have been assigned to their respective configuration groups, one or more configuration rules can be defined.</span></span> <span data-ttu-id="86fac-110">Als twee artikelen bij elkaar horen, wordt de operator **Selecteren** gebruikt om opname te garanderen.</span><span class="sxs-lookup"><span data-stu-id="86fac-110">If two items belong together, the **Select** operator is used to ensure inclusion.</span></span> <span data-ttu-id="86fac-111">Als twee artikelen elkaar wederzijds uitsluiten, wordt de operator **Selectie opheffen** gebruikt om uitsluiting te garanderen.</span><span class="sxs-lookup"><span data-stu-id="86fac-111">If two items are mutually exclusive, the **Deselect** operator is used to ensure exclusion.</span></span>  

<span data-ttu-id="86fac-112">**Opmerking:** Deze informatie is alleen van toepassing op productmodellen die gebruikmaken van de technologie van op dimensies gebaseerde configuratie.</span><span class="sxs-lookup"><span data-stu-id="86fac-112">**Note:** This information applies only to product masters that use the dimension-based configuration technology.</span></span>  

<span data-ttu-id="86fac-113">Het wijzigen van configuratieregels heeft geen invloed op bestaande configuraties.</span><span class="sxs-lookup"><span data-stu-id="86fac-113">Existing configurations aren't affected by subsequent changes to the configuration rules.</span></span> <span data-ttu-id="86fac-114">Het is echter wel belangrijk de regels in te stellen voordat u een nieuwe configuratie gaat definiëren en om die regels te controleren als u er niet zeker van bent of deze wel of niet zijn gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="86fac-114">However, it's important that you set the rules before you define a new configuration, and that you check the rules if you think they have been changed.</span></span>  

<span data-ttu-id="86fac-115">**Opmerking:** Bij de methode **Selecteren** worden de afgeleide configuratiegroep, het artikelnummer en de configuratie automatisch geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="86fac-115">**Note:** For the **Select** method, the derived configuration group, item number, and configuration are automatically selected.</span></span> <span data-ttu-id="86fac-116">Bij de methode **Selectie opheffen** kunnen de afgeleide configuratiegroep, het artikelnummer en de configuratie niet worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="86fac-116">For the **Deselect** method, the derived configuration group, item number, and configuration can't be selected.</span></span>

<a name="see-also"></a><span data-ttu-id="86fac-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="86fac-117">See also</span></span>
--------

[<span data-ttu-id="86fac-118">Op dimensie gebaseerde productconfiguratie</span><span class="sxs-lookup"><span data-stu-id="86fac-118">Dimension-based product configuration</span></span>](dimension-based-product-configuration.md)




