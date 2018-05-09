---
title: Standaardkosten in een niet-productieomgeving bijwerken
description: Dit artikel bevat richtlijnen voor het bijwerken van standaardkosten in een niet-productieomgeving.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79723
ms.assetid: 7ba0c408-2450-4042-9542-6fdf83c12e6c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8b12e37a82e81a32b560e212fe879dbe4b114969
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="update-standard-costs-in-a-non-manufacturing-environment"></a><span data-ttu-id="66af4-103">Standaardkosten in een niet-productieomgeving bijwerken</span><span class="sxs-lookup"><span data-stu-id="66af4-103">Update standard costs in a non-manufacturing environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66af4-104">Dit artikel bevat richtlijnen voor het bijwerken van standaardkosten in een niet-productieomgeving.</span><span class="sxs-lookup"><span data-stu-id="66af4-104">This article provides guidance for updating standard costs in a non-manufacturing environment.</span></span>

<span data-ttu-id="66af4-105">In de volgende richtlijnen wordt ervan uitgegaan dat u een methode met twee kostprijsberekeningsversies gebruikt voor het bijwerken van standaardkosten.</span><span class="sxs-lookup"><span data-stu-id="66af4-105">The following guidelines assume that you use a two-version approach to update standard cost.</span></span> <span data-ttu-id="66af4-106">Bij deze methode bevat één kostprijsberekeningsversie de standaardkosten die oorspronkelijk zijn gedefinieerd voor de bevriezingsperiode en de tweede kostprijsberekeningsversie bevat de incrementele updates.</span><span class="sxs-lookup"><span data-stu-id="66af4-106">In this approach, one costing version contains the standard costs that were originally defined for the frozen period, and the second costing version contains the incremental updates.</span></span> <span data-ttu-id="66af4-107">Elke update wordt als een kostenrecord ingevoerd die is ingesloten in de tweede kostprijsberekeningsversie en wordt uiteindelijk geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="66af4-107">Each update is entered as a cost record that is enclosed in the second costing version, and eventually it's enabled.</span></span> <span data-ttu-id="66af4-108">In een alternatieve methode met één kostprijsberekeningsversie wordt de oorspronkelijke gedefinieerde verzameling standaardkosten gebruikt.</span><span class="sxs-lookup"><span data-stu-id="66af4-108">An alternative, one-version approach uses the set of standard costs that was originally defined.</span></span> <span data-ttu-id="66af4-109">De methode met twee kostprijsberekeningsversies vereist dat u een tweede kostprijsberekeningsversie definieert.</span><span class="sxs-lookup"><span data-stu-id="66af4-109">The two-version approach requires that you define a second costing version.</span></span> <span data-ttu-id="66af4-110">Dit zijn de richtlijnen voor het definiëren van deze kostprijsberekeningsversie:</span><span class="sxs-lookup"><span data-stu-id="66af4-110">Here are the guidelines for defining this costing version:</span></span>

-   <span data-ttu-id="66af4-111">Wijs het kostprijsberekeningstype **Standaardkosten** toe.</span><span class="sxs-lookup"><span data-stu-id="66af4-111">Assign a costing type of **Standard costs**.</span></span>
-   <span data-ttu-id="66af4-112">Wijs een significante id aan de kostprijsberekeningsversie toe die iets zegt over de inhoud, bijvoorbeeld **2016-UPDATES**.</span><span class="sxs-lookup"><span data-stu-id="66af4-112">Assign a meaningful identifier that indicates the contents of the costing version, such as **2016-UPDATES**.</span></span>
-   <span data-ttu-id="66af4-113">Controleer of de inhoud kostenrecords bevat.</span><span class="sxs-lookup"><span data-stu-id="66af4-113">Make sure that the content includes cost records.</span></span>
-   <span data-ttu-id="66af4-114">Sta de invoer van kostenrecords toe voor alle sites.</span><span class="sxs-lookup"><span data-stu-id="66af4-114">Allow cost records to be entered for all sites.</span></span> <span data-ttu-id="66af4-115">Als u een site opgeeft, kunnen alleen kostenrecords voor die site worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="66af4-115">If you specify a site, cost records can be entered only for that site.</span></span>
-   <span data-ttu-id="66af4-116">Stel het terugvalprincipe **Geen** in.</span><span class="sxs-lookup"><span data-stu-id="66af4-116">Indicate a fallback principle of **None**.</span></span> <span data-ttu-id="66af4-117">Het terugvalprincipe is alleen van toepassing op kostenberekeningen voor gefabriceerde artikelen.</span><span class="sxs-lookup"><span data-stu-id="66af4-117">The fallback principle applies only to cost calculations for manufactured items.</span></span>

<span data-ttu-id="66af4-118">Als u de standaardkosten voor nieuwe artikelen wilt corrigeren, aanpassen of bijwerken, gaat u als volgt te werk.</span><span class="sxs-lookup"><span data-stu-id="66af4-118">To correct, adjust, or update standard costs for new items, follow these steps.</span></span>

1.  <span data-ttu-id="66af4-119">Gebruik de pagina **Instellingen** **kostprijsberekeningsversie** om kostengegevens in te schakelen die in de tweede kostprijsberekeningsversie moeten worden ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="66af4-119">Use the **Costing version** **setup** page to enable cost data to be entered into the second costing version.</span></span> <span data-ttu-id="66af4-120">Voorkom desgewenst de activering van kosten die in behandeling zijn, zodat activering pas is toegestaan nadat de kosten die in behandeling zijn, volledig en correct zijn gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="66af4-120">Optionally, prevent the activation of pending costs, so that activation will be allowed after pending costs have been completely and accurately defined.</span></span> <span data-ttu-id="66af4-121">U kunt desgewenst ook een datum in het veld **Begindatum** invoeren.</span><span class="sxs-lookup"><span data-stu-id="66af4-121">You can also optionally enter a date in the **From date** field.</span></span> <span data-ttu-id="66af4-122">Normaal gesproken kunt u het beste de datum gebruiken vanaf wanneer u de incrementele updates wilt activeren.</span><span class="sxs-lookup"><span data-stu-id="66af4-122">As a general guideline, use the date when you intend to enable the incremental updates.</span></span> <span data-ttu-id="66af4-123">U kunt ook het veld **Begindatum** leeg laten voor de kostprijsberekeningsversie en vervolgens een datum invoeren in het veld **Begindatum** voor elke kostprijsrecord.</span><span class="sxs-lookup"><span data-stu-id="66af4-123">Alternatively, leave the **From date** field blank for the costing version, and then enter a date in the **From date** field for each cost record.</span></span>
2.  <span data-ttu-id="66af4-124">Gebruik de pagina **Artikelprijs** als u updates als artikelkostenrecords wilt invoeren die zijn ingesloten in de tweede kostprijsberekeningsversie.</span><span class="sxs-lookup"><span data-stu-id="66af4-124">Use the **Item price** page to enter updates as item cost records that are enclosed in the second costing version.</span></span>
3.  <span data-ttu-id="66af4-125">Gebruik het rapport **Artikelprijzen** als u de nauwkeurigheid en volledigheid van de artikelkostenrecords wilt opgeven die zijn ingesloten in de tweede kostprijsberekeningsversie.</span><span class="sxs-lookup"><span data-stu-id="66af4-125">Use the **Item prices** report to verify the completeness and accuracy of the item cost records that are enclosed in the second costing version.</span></span>
4.  <span data-ttu-id="66af4-126">Gebruik het formulier **Onderhoud kostprijsberekeningsversie** om de blokkeringsvlag te wijzigen om activering toe te staan van kostenrecords die in behandeling zijn en die zijn ingesloten in de tweede kostprijsberekeningsversie.</span><span class="sxs-lookup"><span data-stu-id="66af4-126">Use the **Costing version maintenance** page to change the blocking flag to allow activation of the pending cost records that are enclosed in the second costing version.</span></span>
5.  <span data-ttu-id="66af4-127">Gebruik de pagina **Prijzen activeren** (die u opent vanaf de pagina **Onderhoud kostprijsberekeningsversie**) om alle artikelkostenrecords die in behandeling zijn en die zijn ingesloten in de tweede kostprijsberekeningsversie, te activeren.</span><span class="sxs-lookup"><span data-stu-id="66af4-127">Use the **Activate prices** page (which you open from the **Costing version maintenance** page) to activate all pending item cost records that are enclosed in the second costing version.</span></span> <span data-ttu-id="66af4-128">U kunt ook de kostenrecords die in behandeling zijn voor afzonderlijke artikelen, activeren door op de knop **Activeren** te klikken op de pagina **Artikelprijs**.</span><span class="sxs-lookup"><span data-stu-id="66af4-128">You can also activate the pending cost records for individual items by clicking the **Activate pending price** button on the **Item price** page.</span></span>
6.  <span data-ttu-id="66af4-129">Gebruik de pagina **Instellingen kostprijsberekeningsversie** om de blokkeringsvlaggen te wijzigen die zijn ingesloten in de tweede kostprijsberekeningsversie.</span><span class="sxs-lookup"><span data-stu-id="66af4-129">To prevent additional data maintenance, use the **Costing version setup** page to change the blocking flags that are enclosed in the second costing version.</span></span> <span data-ttu-id="66af4-130">Met het blokkeringsbeleid voorkomt u de invoer van nieuwe kosten die in behandeling zijn en de activering van kosten die in behandeling zijn.</span><span class="sxs-lookup"><span data-stu-id="66af4-130">The blocking policies will prevent the entry of new pending costs and the activation of pending costs.</span></span>





