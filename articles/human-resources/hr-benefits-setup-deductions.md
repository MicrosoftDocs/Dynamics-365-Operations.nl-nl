---
title: Inhoudingen configureren
description: ''
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
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008640"
---
# <a name="configure-deductions"></a><span data-ttu-id="820c6-102">Inhoudingen configureren</span><span class="sxs-lookup"><span data-stu-id="820c6-102">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="820c6-103">Met inhoudingen in Microsoft Dynamics 365 Human Resources kunt u bepalen hoeveel er eventueel moet worden ingehouden op het salaris van een werknemer voor elke vergoeding.</span><span class="sxs-lookup"><span data-stu-id="820c6-103">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="820c6-104">Inhoudingen hebben een ingangsdatum, dus kunt u een historisch overzicht van de inhoudingen bijhouden.</span><span class="sxs-lookup"><span data-stu-id="820c6-104">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="820c6-105">Selecteer in het werkgebied **Vergoedingenbeheer** onder **Instellen** de optie **Inhoudingen**.</span><span class="sxs-lookup"><span data-stu-id="820c6-105">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="820c6-106">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="820c6-106">Select **New**.</span></span>

3. <span data-ttu-id="820c6-107">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="820c6-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="820c6-108">Veld</span><span class="sxs-lookup"><span data-stu-id="820c6-108">Field</span></span> | <span data-ttu-id="820c6-109">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="820c6-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="820c6-110">Aftrek</span><span class="sxs-lookup"><span data-stu-id="820c6-110">Deduction</span></span> | <span data-ttu-id="820c6-111">Een unieke id die wordt gebruikt om de vergoedingsinhouding te identificeren.</span><span class="sxs-lookup"><span data-stu-id="820c6-111">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="820c6-112">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="820c6-112">Description</span></span> | <span data-ttu-id="820c6-113">Een omschrijving voor de inhouding.</span><span class="sxs-lookup"><span data-stu-id="820c6-113">A description for the deduction.</span></span> |
   | <span data-ttu-id="820c6-114">Geldig vanaf</span><span class="sxs-lookup"><span data-stu-id="820c6-114">Effective</span></span> | <span data-ttu-id="820c6-115">De begindatum.</span><span class="sxs-lookup"><span data-stu-id="820c6-115">The start date.</span></span> <span data-ttu-id="820c6-116">De standaardwaarde is de huidige systeemdatum.</span><span class="sxs-lookup"><span data-stu-id="820c6-116">The default value is the current system date.</span></span> |
   | <span data-ttu-id="820c6-117">Vervaldatum</span><span class="sxs-lookup"><span data-stu-id="820c6-117">Expiration</span></span> | <span data-ttu-id="820c6-118">De einddatum.</span><span class="sxs-lookup"><span data-stu-id="820c6-118">The end date.</span></span> <span data-ttu-id="820c6-119">De standaardwaarde is 12/31/2154, wat 'nooit' betekent.</span><span class="sxs-lookup"><span data-stu-id="820c6-119">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="820c6-120">Koptekst</span><span class="sxs-lookup"><span data-stu-id="820c6-120">Heading</span></span> | <span data-ttu-id="820c6-121">De koptekstcode uit de salarisadministratie die bij deze inhouding wordt gebruikt voor het werknemersdeel van de inhouding bij de verwerking van de vergoedingen in de salarisadministratie.</span><span class="sxs-lookup"><span data-stu-id="820c6-121">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="820c6-122">Deze code wordt gebruikt wanneer bij u een externe dienstverlener de salarisadministratie verzorgt.</span><span class="sxs-lookup"><span data-stu-id="820c6-122">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="820c6-123">Verwijzing van werknemer voor salarisinhouding</span><span class="sxs-lookup"><span data-stu-id="820c6-123">Employee payroll deduction reference</span></span> | <span data-ttu-id="820c6-124">De inhoudingscode van de salarisadministratie die in deze inhouding wordt gebruikt voor het werknemergedeelte van de inhouding bij het verwerken van de vergoedingen voor de salarisadministratie.</span><span class="sxs-lookup"><span data-stu-id="820c6-124">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="820c6-125">Kop voor bedrag</span><span class="sxs-lookup"><span data-stu-id="820c6-125">Amount heading</span></span> | <span data-ttu-id="820c6-126">De koptekstcode uit de salarisadministratie die bij dit inhoudingsbedrag wordt gebruikt voor het werknemersdeel van de inhouding bij de verwerking van de vergoedingen in de salarisadministratie.</span><span class="sxs-lookup"><span data-stu-id="820c6-126">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="820c6-127">Deze code wordt gewoonlijk gebruikt wanneer bij u een externe dienstverlener de salarisadministratie verzorgt.</span><span class="sxs-lookup"><span data-stu-id="820c6-127">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="820c6-128">Kan verwijderen</span><span class="sxs-lookup"><span data-stu-id="820c6-128">Can delete</span></span> | <span data-ttu-id="820c6-129">Hiermee geeft u aan of een geëxporteerde waarde uit Dynamics 365 for Finance and Operations ertoe kan leiden dat de waarde in de salarisadministratie wordt verwijderd.</span><span class="sxs-lookup"><span data-stu-id="820c6-129">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="820c6-130">Gekoppelde kolommen</span><span class="sxs-lookup"><span data-stu-id="820c6-130">Paired columns</span></span> | <span data-ttu-id="820c6-131">Hiermee geeft u aan of de koptekst en het inhoudingsbedrag in gekoppelde, aangrenzende kolommen naar de salarisadministratie moeten worden geëxporteerd.</span><span class="sxs-lookup"><span data-stu-id="820c6-131">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="820c6-132">Ingangsdatum wijzigen</span><span class="sxs-lookup"><span data-stu-id="820c6-132">Change effective date</span></span> | <span data-ttu-id="820c6-133">De datum waarop de wijziging van de vergoedingsinhouding van kracht wordt.</span><span class="sxs-lookup"><span data-stu-id="820c6-133">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="820c6-134">Op deze datum wordt de vergoedingsinhouding automatisch door het systeem gewijzigd en worden alle vergoedingsplannen die aan deze inhouding zijn gekoppeld, bijgewerkt zolang u de verwerking van de wijziging van de inhouding uitvoert.</span><span class="sxs-lookup"><span data-stu-id="820c6-134">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="820c6-135">Wijziging inhouding voltooid</span><span class="sxs-lookup"><span data-stu-id="820c6-135">Deduction change completed</span></span> | <span data-ttu-id="820c6-136">Het selectievakje 'Wijziging van inhouding voltooid' wordt automatisch ingeschakeld nadat de wijzigingen in de vergoedingsinhouding zijn voltooid door de verwerking van de wijziging van de inhouding.</span><span class="sxs-lookup"><span data-stu-id="820c6-136">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="820c6-137">Als u wijzigingen in de instellingen van het vergoedingstarief wilt bijhouden en beheren, selecteert u **Acties** en selecteert u vervolgens **Versies onderhouden**.</span><span class="sxs-lookup"><span data-stu-id="820c6-137">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="820c6-138">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="820c6-138">Select **Save**.</span></span> 
