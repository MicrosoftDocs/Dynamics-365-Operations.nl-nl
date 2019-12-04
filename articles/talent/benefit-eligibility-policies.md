---
title: Beleid voor geschiktheid vergoedingen
description: Dit artikel biedt informatie over het beleid voor geschiktheid voor vergoedingen, waarmee u kunt bepalen wie voor specifieke vergoedingen in aanmerking komt.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: b44287bf22f0b6c4e33a29b4b86aaae934505a43
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814688"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="5656d-103">Beleid voor geschiktheid vergoedingen</span><span class="sxs-lookup"><span data-stu-id="5656d-103">Benefit eligibility policies</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5656d-104">Dit onderwerp bevat informatie over het beleid voor geschiktheid voor vergoedingen, waarmee u kunt bepalen wie voor specifieke vergoedingen in aanmerking komt.</span><span class="sxs-lookup"><span data-stu-id="5656d-104">This topic provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="5656d-105">Als u vergoedingen maakt, bepaalt u welke vergoedingen beschikbaar zijn voor welke werknemers.</span><span class="sxs-lookup"><span data-stu-id="5656d-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="5656d-106">In de volgende tabel worden voorbeelden weergegeven van vergoedingen die u voor specifieke werknemers beschikbaar kunt maken.</span><span class="sxs-lookup"><span data-stu-id="5656d-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="5656d-107">Vergoeding</span><span class="sxs-lookup"><span data-stu-id="5656d-107">Benefit</span></span>          | <span data-ttu-id="5656d-108">Voor wie de vergoeding beschikbaar is</span><span class="sxs-lookup"><span data-stu-id="5656d-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="5656d-109">Ziektekostenverzekering</span><span class="sxs-lookup"><span data-stu-id="5656d-109">Health insurance</span></span> | <span data-ttu-id="5656d-110">Alle werknemers</span><span class="sxs-lookup"><span data-stu-id="5656d-110">All employees</span></span>                   |
| <span data-ttu-id="5656d-111">Mobiele telefoon</span><span class="sxs-lookup"><span data-stu-id="5656d-111">Mobile phone</span></span>     | <span data-ttu-id="5656d-112">Verkooppersoneel, leidinggevenden</span><span class="sxs-lookup"><span data-stu-id="5656d-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="5656d-113">Parkeervergunningen</span><span class="sxs-lookup"><span data-stu-id="5656d-113">Parking passes</span></span>   | <span data-ttu-id="5656d-114">Stafleden</span><span class="sxs-lookup"><span data-stu-id="5656d-114">Executives</span></span>                      |

<span data-ttu-id="5656d-115">De volgende onderdelen worden gebruikt om geschiktheidsbeleid te maken:</span><span class="sxs-lookup"><span data-stu-id="5656d-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="5656d-116">Beleidsregeltypen</span><span class="sxs-lookup"><span data-stu-id="5656d-116">Policy rule types</span></span>
-   <span data-ttu-id="5656d-117">Beleid voor geschiktheid vergoedingen</span><span class="sxs-lookup"><span data-stu-id="5656d-117">Benefit eligibility policies</span></span>

<span data-ttu-id="5656d-118">Met typen bedrijfsregels worden de queryparameters bepaald die worden gebruikt wanneer u specifieke bedrijfsregels ontwikkelt.</span><span class="sxs-lookup"><span data-stu-id="5656d-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="5656d-119">Nadat u typen beleidsregels hebt gemaakt, kunt u geschiktheidsbeleidsregels voor vergoedingen maken.</span><span class="sxs-lookup"><span data-stu-id="5656d-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="5656d-120">Met de beleidsregels kunt u een verzameling regels maken die op een of meer rechtspersonen van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="5656d-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="5656d-121">Binnen elk beleid kunt u alle eerder gemaakte geschiktheidsbeleidsregels voor vergoedingen weergeven.</span><span class="sxs-lookup"><span data-stu-id="5656d-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="5656d-122">U definieert het bereik van de regel binnen het beleid.</span><span class="sxs-lookup"><span data-stu-id="5656d-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="5656d-123">Als u bijvoorbeeld een type geschiktheidsbeleidsregel voor vergoedingen maakt met de naam **Leidinggevende**, kunt u opgeven wat de regel binnen dat beleid is.</span><span class="sxs-lookup"><span data-stu-id="5656d-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="5656d-124">In dit voorbeeld kan de regel aangeven dat elke functietitel die het woord 'leidinggevende' bevat in de regel moet worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="5656d-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="5656d-125">Nadat u de parameters van de regel of regels hebt gedefinieerd die in het beleid zijn opgenomen, kunt u een specifieke regel aan de vergoeding toewijzen.</span><span class="sxs-lookup"><span data-stu-id="5656d-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>

<a name="additional-resources"></a><span data-ttu-id="5656d-126">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="5656d-126">Additional resources</span></span>
--------

[<span data-ttu-id="5656d-127">Een vergoedingenprogramma definiëren en beheren</span><span class="sxs-lookup"><span data-stu-id="5656d-127">Define and manage a benefits program</span></span>](manage-benefit-program.md)



