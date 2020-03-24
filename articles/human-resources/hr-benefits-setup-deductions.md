---
title: Inhoudingen configureren
description: Met inhoudingen in Microsoft Dynamics 365 Human Resources kunt u bepalen hoeveel er eventueel moet worden ingehouden op het salaris van een werknemer voor elke vergoeding.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a5287161f352b386ae4e13067f40228d7c1bce62
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092724"
---
# <a name="configure-deductions"></a><span data-ttu-id="660a9-103">Inhoudingen configureren</span><span class="sxs-lookup"><span data-stu-id="660a9-103">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="660a9-104">Met inhoudingen in Microsoft Dynamics 365 Human Resources kunt u bepalen hoeveel er eventueel moet worden ingehouden op het salaris van een werknemer voor elke vergoeding.</span><span class="sxs-lookup"><span data-stu-id="660a9-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="660a9-105">Inhoudingen hebben een ingangsdatum, dus kunt u een historisch overzicht van de inhoudingen bijhouden.</span><span class="sxs-lookup"><span data-stu-id="660a9-105">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="660a9-106">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Inhoudingen**.</span><span class="sxs-lookup"><span data-stu-id="660a9-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="660a9-107">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="660a9-107">Select **New**.</span></span>

3. <span data-ttu-id="660a9-108">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="660a9-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="660a9-109">Veld</span><span class="sxs-lookup"><span data-stu-id="660a9-109">Field</span></span> | <span data-ttu-id="660a9-110">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="660a9-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="660a9-111">Aftrek</span><span class="sxs-lookup"><span data-stu-id="660a9-111">Deduction</span></span> | <span data-ttu-id="660a9-112">Een unieke id die wordt gebruikt om de vergoedingsinhouding te identificeren.</span><span class="sxs-lookup"><span data-stu-id="660a9-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="660a9-113">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="660a9-113">Description</span></span> | <span data-ttu-id="660a9-114">Een omschrijving voor de inhouding.</span><span class="sxs-lookup"><span data-stu-id="660a9-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="660a9-115">Geldig vanaf</span><span class="sxs-lookup"><span data-stu-id="660a9-115">Effective</span></span> | <span data-ttu-id="660a9-116">De begindatum.</span><span class="sxs-lookup"><span data-stu-id="660a9-116">The start date.</span></span> <span data-ttu-id="660a9-117">De standaardwaarde is de huidige systeemdatum.</span><span class="sxs-lookup"><span data-stu-id="660a9-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="660a9-118">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="660a9-118">Expiration</span></span> | <span data-ttu-id="660a9-119">De einddatum.</span><span class="sxs-lookup"><span data-stu-id="660a9-119">The end date.</span></span> <span data-ttu-id="660a9-120">De standaardwaarde is 12/31/2154, wat 'nooit' betekent.</span><span class="sxs-lookup"><span data-stu-id="660a9-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="660a9-121">Koptekst</span><span class="sxs-lookup"><span data-stu-id="660a9-121">Heading</span></span> | <span data-ttu-id="660a9-122">De koptekstcode uit de salarisadministratie die bij deze inhouding wordt gebruikt voor het werknemersdeel van de inhouding bij de verwerking van de vergoedingen in de salarisadministratie.</span><span class="sxs-lookup"><span data-stu-id="660a9-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="660a9-123">Deze code wordt gebruikt wanneer bij u een externe dienstverlener de salarisadministratie verzorgt.</span><span class="sxs-lookup"><span data-stu-id="660a9-123">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="660a9-124">Verwijzing van werknemer voor salarisinhouding</span><span class="sxs-lookup"><span data-stu-id="660a9-124">Employee payroll deduction reference</span></span> | <span data-ttu-id="660a9-125">De inhoudingscode van de salarisadministratie die in deze inhouding wordt gebruikt voor het werknemergedeelte van de inhouding bij het verwerken van de vergoedingen voor de salarisadministratie.</span><span class="sxs-lookup"><span data-stu-id="660a9-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="660a9-126">Kop voor bedrag</span><span class="sxs-lookup"><span data-stu-id="660a9-126">Amount heading</span></span> | <span data-ttu-id="660a9-127">De koptekstcode uit de salarisadministratie die bij dit inhoudingsbedrag wordt gebruikt voor het werknemersdeel van de inhouding bij de verwerking van de vergoedingen in de salarisadministratie.</span><span class="sxs-lookup"><span data-stu-id="660a9-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="660a9-128">Deze code wordt gewoonlijk gebruikt wanneer bij u een externe dienstverlener de salarisadministratie verzorgt.</span><span class="sxs-lookup"><span data-stu-id="660a9-128">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="660a9-129">Kan verwijderen</span><span class="sxs-lookup"><span data-stu-id="660a9-129">Can delete</span></span> | <span data-ttu-id="660a9-130">Hiermee geeft u aan of een geëxporteerde waarde uit Dynamics 365 for Finance and Operations ertoe kan leiden dat de waarde in de salarisadministratie wordt verwijderd.</span><span class="sxs-lookup"><span data-stu-id="660a9-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="660a9-131">Gekoppelde kolommen</span><span class="sxs-lookup"><span data-stu-id="660a9-131">Paired columns</span></span> | <span data-ttu-id="660a9-132">Hiermee geeft u aan of de koptekst en het inhoudingsbedrag in gekoppelde, aangrenzende kolommen naar de salarisadministratie moeten worden geëxporteerd.</span><span class="sxs-lookup"><span data-stu-id="660a9-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="660a9-133">Ingangsdatum wijzigen</span><span class="sxs-lookup"><span data-stu-id="660a9-133">Change effective date</span></span> | <span data-ttu-id="660a9-134">De datum waarop de wijziging van de vergoedingsinhouding van kracht wordt.</span><span class="sxs-lookup"><span data-stu-id="660a9-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="660a9-135">Op deze datum wordt de vergoedingsinhouding automatisch door het systeem gewijzigd en worden alle vergoedingsplannen die aan deze inhouding zijn gekoppeld, bijgewerkt zolang u de verwerking van de wijziging van de inhouding uitvoert.</span><span class="sxs-lookup"><span data-stu-id="660a9-135">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="660a9-136">Wijziging inhouding voltooid</span><span class="sxs-lookup"><span data-stu-id="660a9-136">Deduction change completed</span></span> | <span data-ttu-id="660a9-137">Het selectievakje 'Wijziging van inhouding voltooid' wordt automatisch ingeschakeld nadat de wijzigingen in de vergoedingsinhouding zijn voltooid door de verwerking van de wijziging van de inhouding.</span><span class="sxs-lookup"><span data-stu-id="660a9-137">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="660a9-138">Als u wijzigingen in de instellingen van het vergoedingstarief wilt bijhouden en beheren, selecteert u **Acties** en selecteert u vervolgens **Versies onderhouden**.</span><span class="sxs-lookup"><span data-stu-id="660a9-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="660a9-139">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="660a9-139">Select **Save**.</span></span> 
