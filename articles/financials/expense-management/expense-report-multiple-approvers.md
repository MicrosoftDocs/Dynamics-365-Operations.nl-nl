---
title: Onkostennota's en meerdere goedkeurders
description: In dit onderwerp vindt u informatie over onkostennota's die moeten worden goedgekeurd door meer dan één persoon.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d83a473e2e894856c12b36b4d005c6cb06b765a
ms.sourcegitcommit: ef08bf1258aefb525d56bf85ef19311be26ab94c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/30/2019
ms.locfileid: "1795119"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="4fdf0-103">Onkostennota's en meerdere goedkeurders</span><span class="sxs-lookup"><span data-stu-id="4fdf0-103">Expense reports and multiple approvers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fdf0-104">Afhankelijk van het goedkeuringsbeleid voor onkosten van uw organisatie moet mogelijk meer dan één persoon een onkostendeclaratie goedkeuren die door een werknemer wordt ingediend.</span><span class="sxs-lookup"><span data-stu-id="4fdf0-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="4fdf0-105">Wanneer u de werkstroom voor goedkeuring van het onkostenrapport instelt, kunt u werkstroomelementen toevoegen die taken of stappen voor één of meerdere goedkeurders van onkostenrapporten bevatten.</span><span class="sxs-lookup"><span data-stu-id="4fdf0-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="4fdf0-106">U kan bijvoorbeeld vereisen dat alle onkostendeclaraties eerst worden goedgekeurd door de manager van de werknemer die het rapport ingediend heeft en vervolgens door de coördinator Crediteuren.</span><span class="sxs-lookup"><span data-stu-id="4fdf0-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="4fdf0-107">Indien u meerdere goedkeurders van onkostendeclaraties vereist, kunt u de workflowelementen op een van de volgende manieren toevoegen:</span><span class="sxs-lookup"><span data-stu-id="4fdf0-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="4fdf0-108">Voeg één goedkeuringselement toe dat één stap omvat.</span><span class="sxs-lookup"><span data-stu-id="4fdf0-108">Add one approval element that has one step.</span></span> <span data-ttu-id="4fdf0-109">In deze stap kan bijvoorbeeld vereist worden dat een onkostendeclaratie wordt toegewezen aan een gebruikersgroep en dat deze door 50% van de leden van de gebruikersgroep goedgekeurd moet worden.</span><span class="sxs-lookup"><span data-stu-id="4fdf0-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="4fdf0-110">Voeg één goedkeuringselement toe dat meerdere stappen omvat.</span><span class="sxs-lookup"><span data-stu-id="4fdf0-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="4fdf0-111">De stappen in het goedkeuringselement zijn bijvoorbeeld als volgt:</span><span class="sxs-lookup"><span data-stu-id="4fdf0-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="4fdf0-112">De manager van de werknemer die de onkostendeclaratie heeft ingediend keurt deze goed.</span><span class="sxs-lookup"><span data-stu-id="4fdf0-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="4fdf0-113">De medewerker Crediteuren controleert de items van de onkostendeclaratie.</span><span class="sxs-lookup"><span data-stu-id="4fdf0-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="4fdf0-114">De budgeteigenaar keurt de onkostendeclaratie goed.</span><span class="sxs-lookup"><span data-stu-id="4fdf0-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="4fdf0-115">Voeg meerdere goedkeuringselementen toe die allemaal één stap bevatten.</span><span class="sxs-lookup"><span data-stu-id="4fdf0-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="4fdf0-116">U kunt bijvoorbeeld een afzonderlijk goedkeuringselement toevoegen voor elk van de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="4fdf0-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="4fdf0-117">De manager van de werknemer keurt de onkostendeclaratie goed.</span><span class="sxs-lookup"><span data-stu-id="4fdf0-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="4fdf0-118">De budgeteigenaar keurt de onkostendeclaratie goed.</span><span class="sxs-lookup"><span data-stu-id="4fdf0-118">The budget owner approves the expense report.</span></span>
