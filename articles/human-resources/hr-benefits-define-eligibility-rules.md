---
title: Regels en beleid van de vergoedingsgeschiktheid definiëren
description: In dit artikel leest u hoe u geschiktheidsregels en beleid voor vergoedingen kunt maken en vervolgens regels kunt toewijzen aan vergoedingen.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 39a9a1c96ae2a12a32b3c5fbc67571bcf983c898
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467982"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="ed172-103">Regels en beleid van de vergoedingsgeschiktheid definiëren</span><span class="sxs-lookup"><span data-stu-id="ed172-103">Define benefit eligibility rules and policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ed172-104">In dit onderwerp leest u hoe u geschiktheidsregels en beleid voor vergoedingen kunt maken en vervolgens regels kunt toewijzen aan vergoedingen.</span><span class="sxs-lookup"><span data-stu-id="ed172-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="ed172-105">Regeltype van beleid om in aanmerking te komen voor een vergoeding maken</span><span class="sxs-lookup"><span data-stu-id="ed172-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="ed172-106">Ga naar **Human Resources > Vergoedingen > Geschiktheid > Regeltypen van beleid om in aanmerking te komen voor een vergoeding**.</span><span class="sxs-lookup"><span data-stu-id="ed172-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="ed172-107">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="ed172-107">Select **New**.</span></span>
3. <span data-ttu-id="ed172-108">Voer een waarde in het veld **Regelnaam** in.</span><span class="sxs-lookup"><span data-stu-id="ed172-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="ed172-109">Voer een waarde in het veld **Beschrijving** in.</span><span class="sxs-lookup"><span data-stu-id="ed172-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="ed172-110">Klik in het veld **Querynaam** op de vervolgkeuzeknop om het opzoekveld te openen.</span><span class="sxs-lookup"><span data-stu-id="ed172-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ed172-111">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ed172-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="ed172-112">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ed172-112">Select **Save**.</span></span>
8. <span data-ttu-id="ed172-113">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ed172-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="ed172-114">Beleid om in aanmerking te komen voor een vergoeding</span><span class="sxs-lookup"><span data-stu-id="ed172-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="ed172-115">Ga naar **Human resources > Vergoedingen > Geschiktheid > Beleid voor geschiktheid vergoedingen**.</span><span class="sxs-lookup"><span data-stu-id="ed172-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="ed172-116">Selecteer een bestaand vergoedingsbeleid.</span><span class="sxs-lookup"><span data-stu-id="ed172-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="ed172-117">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ed172-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="ed172-118">Schakel het uitvouwen van de secties **Beleidsorganisaties** om.</span><span class="sxs-lookup"><span data-stu-id="ed172-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="ed172-119">U kunt organisaties toevoegen of verwijderen die u wilt opnemen in het beleid.</span><span class="sxs-lookup"><span data-stu-id="ed172-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="ed172-120">Vouw de sectie **Beleidsregels** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="ed172-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="ed172-121">Zoek in de lijst de beleidsregel die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ed172-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="ed172-122">Selecteer **Beleidsregel maken**.</span><span class="sxs-lookup"><span data-stu-id="ed172-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="ed172-123">Voer in het veld **Ingangsdatum** de datum in waarop u het beleid van kracht wilt laten worden.</span><span class="sxs-lookup"><span data-stu-id="ed172-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="ed172-124">Door ingangsdatums en einddatums in te stellen, kunt u in de toekomst wijzigingen aanbrengen in beleidsregels zodat u niet terug hoeft te gaan naar het beleid als u die wijzigingen van kracht wilt laten worden.</span><span class="sxs-lookup"><span data-stu-id="ed172-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="ed172-125">Voeg zo nodig een clausule toe aan het veld **Voorwaarde toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ed172-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="ed172-126">Als u bijvoorbeeld wilt dat de regel alleen van toepassing is op verkoopmanagers, kunt u de WHERE-clausule gebruiken om te zeggen: Waar de positieomschrijving gelijk is aan Verkoopmanager.</span><span class="sxs-lookup"><span data-stu-id="ed172-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="ed172-127">U kunt meerdere Where-instructies opnemen in de regel.</span><span class="sxs-lookup"><span data-stu-id="ed172-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="ed172-128">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed172-128">Select **OK**.</span></span>
11. <span data-ttu-id="ed172-129">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ed172-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="ed172-130">Regel toewijzen aan vergoeding</span><span class="sxs-lookup"><span data-stu-id="ed172-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="ed172-131">Ga naar **Human Resources > Vergoedingen > Vergoedingen**.</span><span class="sxs-lookup"><span data-stu-id="ed172-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="ed172-132">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="ed172-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ed172-133">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ed172-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="ed172-134">Vouw de sectie **Geschiktheidsregels** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="ed172-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="ed172-135">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="ed172-135">Select **Edit**.</span></span>
6. <span data-ttu-id="ed172-136">Selecteer de regel in het veld **Geschiktheid**.</span><span class="sxs-lookup"><span data-stu-id="ed172-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="ed172-137">Selecteer in het veld **Regeltype** de regel die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ed172-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="ed172-138">Selecteer in de lijst de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="ed172-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="ed172-139">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ed172-139">Select **Save**.</span></span>
11. <span data-ttu-id="ed172-140">Het formulier sluiten.</span><span class="sxs-lookup"><span data-stu-id="ed172-140">Close the form.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]