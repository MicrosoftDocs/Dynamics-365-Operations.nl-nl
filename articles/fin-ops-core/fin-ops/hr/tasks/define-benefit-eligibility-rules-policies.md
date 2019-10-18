---
title: Regels en beleid van de vergoedingsgeschiktheid definiëren
description: Deze opname laat zien hoe u geschiktheidsregels en beleid voor vergoedingen kunt maken en vervolgens regels kunt toewijzen aan vergoedingen.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0d35266c95cfbf3473a14fec47a1c748229dd25
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190552"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="a4b28-103">Regels en beleid van de vergoedingsgeschiktheid definiëren</span><span class="sxs-lookup"><span data-stu-id="a4b28-103">Define benefit eligibility rules and policies</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a4b28-104">Deze opname laat zien hoe u geschiktheidsregels en beleid voor vergoedingen kunt maken en vervolgens regels kunt toewijzen aan vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="a4b28-104">This recording will show you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="a4b28-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze registratie te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="a4b28-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="a4b28-106">Regeltype van beleid om in aanmerking te komen voor een vergoeding maken</span><span class="sxs-lookup"><span data-stu-id="a4b28-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="a4b28-107">Ga naar Human resources > Vergoedingen > Geschiktheid > Regeltypen van beleid om in aanmerking te komen voor een vergoeding.</span><span class="sxs-lookup"><span data-stu-id="a4b28-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="a4b28-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a4b28-108">Click New.</span></span>
3. <span data-ttu-id="a4b28-109">Typ een waarde in het veld Regelnaam.</span><span class="sxs-lookup"><span data-stu-id="a4b28-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="a4b28-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="a4b28-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a4b28-111">Klik in het veld Querynaam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="a4b28-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="a4b28-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4b28-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="a4b28-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a4b28-113">Click Save.</span></span>
8. <span data-ttu-id="a4b28-114">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a4b28-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="a4b28-115">Beleid om in aanmerking te komen voor een vergoeding</span><span class="sxs-lookup"><span data-stu-id="a4b28-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="a4b28-116">Ga naar Human resources > Vergoedingen > Geschiktheid > Beleid voor geschiktheid vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="a4b28-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="a4b28-117">Selecteer een bestaand vergoedingsbeleid.</span><span class="sxs-lookup"><span data-stu-id="a4b28-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="a4b28-118">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4b28-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a4b28-119">Schakel de uitbreiding van de secties Beleidsorganisaties om.</span><span class="sxs-lookup"><span data-stu-id="a4b28-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="a4b28-120">Hier kunt u organisaties toevoegen of verwijderen die u wilt opnemen in het beleid.</span><span class="sxs-lookup"><span data-stu-id="a4b28-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="a4b28-121">Vouw de sectie Beleidsregels uit of samen.</span><span class="sxs-lookup"><span data-stu-id="a4b28-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="a4b28-122">Zoek in de lijst de beleidsregel die eerder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a4b28-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="a4b28-123">Klik op Beleidsregel maken.</span><span class="sxs-lookup"><span data-stu-id="a4b28-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="a4b28-124">Voer in het veld Ingangsdatum de datum in waarop u het beleid van kracht wilt laten worden.</span><span class="sxs-lookup"><span data-stu-id="a4b28-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="a4b28-125">Door ingangsdatums en einddatums in te stellen kunt u toekomstige wijzigingen aanbrengen in beleidsregels en terugkomen naar het beleid als u die wijzigingen van kracht wilt laten worden overbodig maken.</span><span class="sxs-lookup"><span data-stu-id="a4b28-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="a4b28-126">Als u bijvoorbeeld wilt dat de regel alleen van toepassing is op verkoopmanagers, kunt u het WHERE-onderdeel gebruiken om te zeggen: Waar de positieomschrijving gelijk is aan Verkoopmanager.</span><span class="sxs-lookup"><span data-stu-id="a4b28-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="a4b28-127">U kunt via En en Of meerdere Where-instructies opnemen in de regel.</span><span class="sxs-lookup"><span data-stu-id="a4b28-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="a4b28-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="a4b28-128">Click OK.</span></span>
11. <span data-ttu-id="a4b28-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a4b28-129">Close the page.</span></span>
12. <span data-ttu-id="a4b28-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a4b28-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="a4b28-131">Regel toewijzen aan vergoeding</span><span class="sxs-lookup"><span data-stu-id="a4b28-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="a4b28-132">Ga naar Human resources > Vergoedingen > Vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="a4b28-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="a4b28-133">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a4b28-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a4b28-134">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4b28-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a4b28-135">Vouw de sectie Geschiktheidsregels uit of samen.</span><span class="sxs-lookup"><span data-stu-id="a4b28-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="a4b28-136">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="a4b28-136">Click Edit.</span></span>
6. <span data-ttu-id="a4b28-137">Selecteer in het veld geschiktheid de optie Op basis van regels uit de lijst.</span><span class="sxs-lookup"><span data-stu-id="a4b28-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="a4b28-138">Klik in het veld Regeltype op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="a4b28-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="a4b28-139">Zoek en selecteer in de lijst de regel die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="a4b28-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="a4b28-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a4b28-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="a4b28-141">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a4b28-141">Click Save.</span></span>
11. <span data-ttu-id="a4b28-142">Het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="a4b28-142">Close the form.</span></span>
