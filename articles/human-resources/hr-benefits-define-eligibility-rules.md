---
title: Regels en beleid van de vergoedingsgeschiktheid definiëren
description: In dit artikel leest u hoe u geschiktheidsregels en beleid voor vergoedingen kunt maken en vervolgens regels kunt toewijzen aan vergoedingen.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: fa507591fc89eaebf617deedb15b15a0f93f971d
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008687"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="26b4d-103">Regels en beleid van de vergoedingsgeschiktheid definiëren</span><span class="sxs-lookup"><span data-stu-id="26b4d-103">Define benefit eligibility rules and policies</span></span>

<span data-ttu-id="26b4d-104">In dit artikel leest u hoe u geschiktheidsregels en beleid voor vergoedingen kunt maken en vervolgens regels kunt toewijzen aan vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="26b4d-104">This article shows you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="26b4d-105">Het bedrijf van de demogegevens dat wordt gebruikt om deze registratie te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="26b4d-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="26b4d-106">Regeltype van beleid om in aanmerking te komen voor een vergoeding maken</span><span class="sxs-lookup"><span data-stu-id="26b4d-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="26b4d-107">Ga naar Human resources > Vergoedingen > Geschiktheid > Regeltypen van beleid om in aanmerking te komen voor een vergoeding.</span><span class="sxs-lookup"><span data-stu-id="26b4d-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="26b4d-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="26b4d-108">Click New.</span></span>
3. <span data-ttu-id="26b4d-109">Typ een waarde in het veld Regelnaam.</span><span class="sxs-lookup"><span data-stu-id="26b4d-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="26b4d-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="26b4d-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="26b4d-111">Klik in het veld Querynaam op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="26b4d-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="26b4d-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="26b4d-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="26b4d-113">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="26b4d-113">Click Save.</span></span>
8. <span data-ttu-id="26b4d-114">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="26b4d-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="26b4d-115">Beleid om in aanmerking te komen voor een vergoeding</span><span class="sxs-lookup"><span data-stu-id="26b4d-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="26b4d-116">Ga naar Human resources > Vergoedingen > Geschiktheid > Beleid voor geschiktheid vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="26b4d-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="26b4d-117">Selecteer een bestaand vergoedingsbeleid.</span><span class="sxs-lookup"><span data-stu-id="26b4d-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="26b4d-118">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="26b4d-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="26b4d-119">Schakel de uitbreiding van de secties Beleidsorganisaties om.</span><span class="sxs-lookup"><span data-stu-id="26b4d-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="26b4d-120">Hier kunt u organisaties toevoegen of verwijderen die u wilt opnemen in het beleid.</span><span class="sxs-lookup"><span data-stu-id="26b4d-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="26b4d-121">Vouw de sectie Beleidsregels uit of samen.</span><span class="sxs-lookup"><span data-stu-id="26b4d-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="26b4d-122">Zoek in de lijst de beleidsregel die eerder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="26b4d-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="26b4d-123">Klik op Beleidsregel maken.</span><span class="sxs-lookup"><span data-stu-id="26b4d-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="26b4d-124">Voer in het veld Ingangsdatum de datum in waarop u het beleid van kracht wilt laten worden.</span><span class="sxs-lookup"><span data-stu-id="26b4d-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="26b4d-125">Door ingangsdatums en einddatums in te stellen kunt u toekomstige wijzigingen aanbrengen in beleidsregels en terugkomen naar het beleid als u die wijzigingen van kracht wilt laten worden overbodig maken.</span><span class="sxs-lookup"><span data-stu-id="26b4d-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="26b4d-126">Als u bijvoorbeeld wilt dat de regel alleen van toepassing is op verkoopmanagers, kunt u het WHERE-onderdeel gebruiken om te zeggen: Waar de positieomschrijving gelijk is aan Verkoopmanager.</span><span class="sxs-lookup"><span data-stu-id="26b4d-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="26b4d-127">U kunt via En en Of meerdere Where-instructies opnemen in de regel.</span><span class="sxs-lookup"><span data-stu-id="26b4d-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="26b4d-128">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="26b4d-128">Click OK.</span></span>
11. <span data-ttu-id="26b4d-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="26b4d-129">Close the page.</span></span>
12. <span data-ttu-id="26b4d-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="26b4d-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="26b4d-131">Regel toewijzen aan vergoeding</span><span class="sxs-lookup"><span data-stu-id="26b4d-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="26b4d-132">Ga naar Human resources > Vergoedingen > Vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="26b4d-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="26b4d-133">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="26b4d-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="26b4d-134">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="26b4d-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="26b4d-135">Vouw de sectie Geschiktheidsregels uit of samen.</span><span class="sxs-lookup"><span data-stu-id="26b4d-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="26b4d-136">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="26b4d-136">Click Edit.</span></span>
6. <span data-ttu-id="26b4d-137">Selecteer in het veld geschiktheid de optie Op basis van regels uit de lijst.</span><span class="sxs-lookup"><span data-stu-id="26b4d-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="26b4d-138">Klik in het veld Regeltype op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="26b4d-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="26b4d-139">Zoek en selecteer in de lijst de regel die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="26b4d-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="26b4d-140">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="26b4d-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="26b4d-141">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="26b4d-141">Click Save.</span></span>
11. <span data-ttu-id="26b4d-142">Het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="26b4d-142">Close the form.</span></span>
