---
title: Beleid voor geschiktheid vergoedingen
description: Dit artikel biedt informatie over het beleid voor geschiktheid voor vergoedingen, waarmee u kunt bepalen wie voor specifieke vergoedingen in aanmerking komt.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a5046f1d32fb965c7cb3793daf1ba40b9c2a1d10
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805893"
---
# <a name="benefit-eligibility-policies"></a><span data-ttu-id="70dea-103">Beleid inzake geschiktheid voor vergoedingen</span><span class="sxs-lookup"><span data-stu-id="70dea-103">Benefit eligibility policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="70dea-104">Dit artikel biedt informatie over het beleid voor geschiktheid voor vergoedingen, waarmee u kunt bepalen wie voor specifieke vergoedingen in aanmerking komt.</span><span class="sxs-lookup"><span data-stu-id="70dea-104">This article provides information about benefit eligibility policies, which help you define who is eligible for specific benefits.</span></span>

<span data-ttu-id="70dea-105">Als u vergoedingen maakt, bepaalt u welke vergoedingen beschikbaar zijn voor welke werknemers.</span><span class="sxs-lookup"><span data-stu-id="70dea-105">When you create benefits, you decide which benefits will be available to which employees.</span></span> <span data-ttu-id="70dea-106">In de volgende tabel worden voorbeelden weergegeven van vergoedingen die u voor specifieke werknemers beschikbaar kunt maken.</span><span class="sxs-lookup"><span data-stu-id="70dea-106">The following table shows examples of benefits that you might make available to specific employees.</span></span>

| <span data-ttu-id="70dea-107">Vergoeding</span><span class="sxs-lookup"><span data-stu-id="70dea-107">Benefit</span></span>          | <span data-ttu-id="70dea-108">Voor wie de vergoeding beschikbaar is</span><span class="sxs-lookup"><span data-stu-id="70dea-108">Who the benefit is available to</span></span> |
|------------------|---------------------------------|
| <span data-ttu-id="70dea-109">Ziektekostenverzekering</span><span class="sxs-lookup"><span data-stu-id="70dea-109">Health insurance</span></span> | <span data-ttu-id="70dea-110">Alle werknemers</span><span class="sxs-lookup"><span data-stu-id="70dea-110">All employees</span></span>                   |
| <span data-ttu-id="70dea-111">Mobiele telefoon</span><span class="sxs-lookup"><span data-stu-id="70dea-111">Mobile phone</span></span>     | <span data-ttu-id="70dea-112">Verkooppersoneel, leidinggevenden</span><span class="sxs-lookup"><span data-stu-id="70dea-112">Sales staff, executives</span></span>         |
| <span data-ttu-id="70dea-113">Parkeervergunningen</span><span class="sxs-lookup"><span data-stu-id="70dea-113">Parking passes</span></span>   | <span data-ttu-id="70dea-114">Stafleden</span><span class="sxs-lookup"><span data-stu-id="70dea-114">Executives</span></span>                      |

<span data-ttu-id="70dea-115">De volgende onderdelen worden gebruikt om geschiktheidsbeleid te maken:</span><span class="sxs-lookup"><span data-stu-id="70dea-115">The following components in are used to create eligibility policies:</span></span>

-   <span data-ttu-id="70dea-116">Beleidsregeltypen</span><span class="sxs-lookup"><span data-stu-id="70dea-116">Policy rule types</span></span>
-   <span data-ttu-id="70dea-117">Beleid voor geschiktheid vergoedingen</span><span class="sxs-lookup"><span data-stu-id="70dea-117">Benefit eligibility policies</span></span>

<span data-ttu-id="70dea-118">Met typen bedrijfsregels worden de queryparameters bepaald die worden gebruikt wanneer u specifieke bedrijfsregels ontwikkelt.</span><span class="sxs-lookup"><span data-stu-id="70dea-118">Policy rule types define the query parameters that are used when you develop specific policy rules.</span></span> <span data-ttu-id="70dea-119">Nadat u typen beleidsregels hebt gemaakt, kunt u geschiktheidsbeleidsregels voor vergoedingen maken.</span><span class="sxs-lookup"><span data-stu-id="70dea-119">After you create policy rule types, you can create benefit eligibility policies.</span></span> <span data-ttu-id="70dea-120">Met de beleidsregels kunt u een verzameling regels maken die op een of meer rechtspersonen van toepassing zijn.</span><span class="sxs-lookup"><span data-stu-id="70dea-120">The policies let you create a collection of rules that apply to one or more legal entities.</span></span> <span data-ttu-id="70dea-121">Binnen elk beleid kunt u alle eerder gemaakte geschiktheidsbeleidsregels voor vergoedingen weergeven.</span><span class="sxs-lookup"><span data-stu-id="70dea-121">Within each policy, you can view any of the benefit eligibility policy rule types that you created earlier.</span></span> 

<span data-ttu-id="70dea-122">U definieert het bereik van de regel binnen het beleid.</span><span class="sxs-lookup"><span data-stu-id="70dea-122">You define the scope of the rule within the policy.</span></span> <span data-ttu-id="70dea-123">Als u bijvoorbeeld een type geschiktheidsbeleidsregel voor vergoedingen maakt met de naam **Leidinggevende**, kunt u opgeven wat de regel binnen dat beleid is.</span><span class="sxs-lookup"><span data-stu-id="70dea-123">For example, if you create a benefit eligibility policy rule type that is named **Executive**, you can specify what the rule is within that policy.</span></span> <span data-ttu-id="70dea-124">In dit voorbeeld kan de regel aangeven dat elke functietitel die het woord 'leidinggevende' bevat in de regel moet worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="70dea-124">In this example, the rule might state that any job title that contains the word "executive" should be included in the rule.</span></span> <span data-ttu-id="70dea-125">Nadat u de parameters van de regel of regels hebt gedefinieerd die in het beleid zijn opgenomen, kunt u een specifieke regel aan de vergoeding toewijzen.</span><span class="sxs-lookup"><span data-stu-id="70dea-125">After you've defined the parameters of the rule or rules that are included in the policy, you can assign a specific rule to the benefit.</span></span>






[!INCLUDE[footer-include](../includes/footer-banner.md)]