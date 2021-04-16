---
title: Geschiktheidsopties voor persoonlijke contactpersonen configureren
description: Configureer geschiktheidsopties voor persoonlijke contactpersonen in Microsoft Dynamics 365 Human Resources. Persoonlijke contactpersonen kunnen begunstigden of gezinsleden zijn.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 49a519aafc56c303765619a66d815d79b668d0f9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790879"
---
# <a name="configure-personal-contact-eligibility-options"></a><span data-ttu-id="6944c-104">Geschiktheidsopties voor persoonlijke contactpersonen configureren</span><span class="sxs-lookup"><span data-stu-id="6944c-104">Configure personal contact eligibility options</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6944c-105">In dit artikel wordt beschreven hoe u typen persoonlijke contactpersonen voor vergoedingen kunt configureren in Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6944c-105">This article shows you how to configure types of personal contacts to use in benefits in Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="6944c-106">Persoonlijke contactpersonen kunnen begunstigden of gezinsleden zijn.</span><span class="sxs-lookup"><span data-stu-id="6944c-106">Personal contacts can be beneficiaries or dependents.</span></span> 

1. <span data-ttu-id="6944c-107">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Geschiktheidsopties van persoonlijke contactpersonen**.</span><span class="sxs-lookup"><span data-stu-id="6944c-107">In the **Benefits management** workspace, under **Setup**, select **Personal contact eligibility options**.</span></span>

2. <span data-ttu-id="6944c-108">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="6944c-108">Select **New**.</span></span>

3. <span data-ttu-id="6944c-109">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="6944c-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="6944c-110">Veld</span><span class="sxs-lookup"><span data-stu-id="6944c-110">Field</span></span> | <span data-ttu-id="6944c-111">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="6944c-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="6944c-112">**Geschiktheidsoptie**</span><span class="sxs-lookup"><span data-stu-id="6944c-112">**Eligibility option**</span></span> | <span data-ttu-id="6944c-113">Een unieke naam of code van een geschiktheidsoptie om de geschiktheidsoptie te identificeren.</span><span class="sxs-lookup"><span data-stu-id="6944c-113">A unique eligibility option name or code to identify the eligibility option.</span></span> |
   | <span data-ttu-id="6944c-114">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="6944c-114">**Description**</span></span> | <span data-ttu-id="6944c-115">Een korte omschrijving van de geschiktheidsoptie.</span><span class="sxs-lookup"><span data-stu-id="6944c-115">A brief description of the eligibility option.</span></span> |
   | <span data-ttu-id="6944c-116">**Geschiktheidscode contactpersoon**</span><span class="sxs-lookup"><span data-stu-id="6944c-116">**Contact eligibility code**</span></span> | <span data-ttu-id="6944c-117">De systeemcode die het beste de persoonlijke geschiktheidsoptie beschrijft.</span><span class="sxs-lookup"><span data-stu-id="6944c-117">The system code that best describes the personal eligibility option.</span></span> <span data-ttu-id="6944c-118">U kunt kiezen uit:</span><span class="sxs-lookup"><span data-stu-id="6944c-118">You can choose from:</span></span> <ul><li><span data-ttu-id="6944c-119">Relatie</span><span class="sxs-lookup"><span data-stu-id="6944c-119">Relationship</span></span></li><li><span data-ttu-id="6944c-120">Student</span><span class="sxs-lookup"><span data-stu-id="6944c-120">Student</span></span></li><li><span data-ttu-id="6944c-121">Gezinsdekking</span><span class="sxs-lookup"><span data-stu-id="6944c-121">Overage dependent</span></span></li><li><span data-ttu-id="6944c-122">Afhankelijke persoon is te oud en uitgeschakeld</span><span class="sxs-lookup"><span data-stu-id="6944c-122">Over-aged disabled dependent</span></span></li></ul> |
   | <span data-ttu-id="6944c-123">**Status**</span><span class="sxs-lookup"><span data-stu-id="6944c-123">**Status**</span></span> | <span data-ttu-id="6944c-124">De status van de geschiktheidsoptie.</span><span class="sxs-lookup"><span data-stu-id="6944c-124">The status of the eligibility option.</span></span> <span data-ttu-id="6944c-125">Als de status voor een geschiktheidsoptie is ingesteld op inactief, kunt u die geschiktheidsoptie voor persoonlijke contactpersonen niet selecteren voor persoonlijke contactpersonen.</span><span class="sxs-lookup"><span data-stu-id="6944c-125">If the status for an eligibility option is set to inactive, then you can’t select that personal contact eligibility option for personal contacts.</span></span> |
   | <span data-ttu-id="6944c-126">**Relatie**</span><span class="sxs-lookup"><span data-stu-id="6944c-126">**Relationship**</span></span> | <span data-ttu-id="6944c-127">Geeft de relatie aan tussen de persoonlijke contactpersoon en de werknemer.</span><span class="sxs-lookup"><span data-stu-id="6944c-127">Specifies the relationship between the personal contact and the employee.</span></span> <span data-ttu-id="6944c-128">Dit veld is alleen actief als de geschiktheidscode van de contactpersoon is ingesteld op Relatie.</span><span class="sxs-lookup"><span data-stu-id="6944c-128">This field is only active if the contact eligibility code is set to Relationship.</span></span> |
   | <span data-ttu-id="6944c-129">**Leeftijd**</span><span class="sxs-lookup"><span data-stu-id="6944c-129">**Age**</span></span> | <span data-ttu-id="6944c-130">De maximale leeftijd van een geschikte persoonlijke contactpersoon voor het vergoedingsplan.</span><span class="sxs-lookup"><span data-stu-id="6944c-130">The maximum age of an eligible personal contact for the benefit plan.</span></span> <span data-ttu-id="6944c-131">Dit veld is alleen actief als u een relatie selecteert.</span><span class="sxs-lookup"><span data-stu-id="6944c-131">This field is only active if you select a relationship.</span></span> <span data-ttu-id="6944c-132">Deze leeftijd wordt vergeleken met de berekende leeftijd van de persoonlijke contactpersoon.</span><span class="sxs-lookup"><span data-stu-id="6944c-132">This age is compared with the calculated age of the personal contact.</span></span> <span data-ttu-id="6944c-133">Berekende leeftijd is: (dekkingsdatum – geboortedatum van persoonlijke contactpersoon/365).</span><span class="sxs-lookup"><span data-stu-id="6944c-133">Calculated age is: (Coverage date – personal contact birth date / 365).</span></span> <span data-ttu-id="6944c-134">Dit aantal is altijd een geheel getal.</span><span class="sxs-lookup"><span data-stu-id="6944c-134">This number is always an integer.</span></span> |

4. <span data-ttu-id="6944c-135">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="6944c-135">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]