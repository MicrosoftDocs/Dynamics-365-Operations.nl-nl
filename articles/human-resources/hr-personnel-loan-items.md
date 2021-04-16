---
title: Artikelen beheren die aan werknemers worden uitgeleend
description: Leenartikelen zijn records waarmee managers de artikelen die uw bedrijf aan werknemers uitleent, bijhouden.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmLoanItem, HcmLoanType, HcmPersonLoan, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 3581
ms.assetid: b14bdddb-f10e-4619-9f91-8c88439da862
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: dccab8cc2b166fe0ca22e05c14ae858f47aaf3e1
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803436"
---
# <a name="manage-items-that-are-lent-to-workers"></a><span data-ttu-id="4781e-103">Artikelen beheren die aan werknemers worden uitgeleend</span><span class="sxs-lookup"><span data-stu-id="4781e-103">Manage items that are lent to workers</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4781e-104">Leenartikelen zijn records waarmee managers de artikelen die uw bedrijf aan werknemers uitleent, bijhouden.</span><span class="sxs-lookup"><span data-stu-id="4781e-104">Loan items are records that help managers track the physical items that your company lends to its workers.</span></span> 

<span data-ttu-id="4781e-105">De volgende punten zijn voorbeelden van artikelen die een bedrijf aan werknemers kan uitlenen:</span><span class="sxs-lookup"><span data-stu-id="4781e-105">The following points list examples of items that a company might lend to workers:</span></span>
-   <span data-ttu-id="4781e-106">Mobiele telefoons</span><span class="sxs-lookup"><span data-stu-id="4781e-106">Mobile telephones</span></span>
-   <span data-ttu-id="4781e-107">Auto's</span><span class="sxs-lookup"><span data-stu-id="4781e-107">Automobiles</span></span>
-   <span data-ttu-id="4781e-108">Computerapparatuur</span><span class="sxs-lookup"><span data-stu-id="4781e-108">Computer equipment</span></span>

<span data-ttu-id="4781e-109">Elke fysiek artikel moet een bijbehorend leenartikel hebben.</span><span class="sxs-lookup"><span data-stu-id="4781e-109">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="4781e-110">Bij elke leenartikelrecord moet worden beschreven wat er precies wordt uitgeleend, wie ervoor verantwoordelijk is en het aantal dagen dat een artikel aan een medewerker kan worden geleend.</span><span class="sxs-lookup"><span data-stu-id="4781e-110">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can loaned to a worker.</span></span> <span data-ttu-id="4781e-111">U kunt meerdere uitleenartikelen maken, voor artikelen zoals sleutels, toegangskaarten of uniformen.</span><span class="sxs-lookup"><span data-stu-id="4781e-111">You can create multiple loan items, for items such as keys, access cards or uniforms, at the same time.</span></span> 

<span data-ttu-id="4781e-112">Wanneer een artikel wordt uitgeleend, noteert u de datum waarop het artikel is opgehaald, en de datum waarop het artikel naar verwachting zal worden teruggebracht.</span><span class="sxs-lookup"><span data-stu-id="4781e-112">When loaning an item, enter the date that the item was loaned, and the planned return date.</span></span> <span data-ttu-id="4781e-113">Als het geleende artikel weer wordt teruggebracht, noteert u de inleverdatum.</span><span class="sxs-lookup"><span data-stu-id="4781e-113">When the item is returned, enter the actual return date.</span></span>

<span data-ttu-id="4781e-114">Werknemers kunnen de records van de artikelen weergeven die aan hen zijn uitgeleend met het werkgebied Selfservice werknemer.</span><span class="sxs-lookup"><span data-stu-id="4781e-114">Employees can view the records of the items that have been loaned to them using the Employee self-service workspace.</span></span> <span data-ttu-id="4781e-115">Ze kunnen ook de bestaande records bewerken of nieuwe leenartikelen opgeven als ze extra fysieke artikelen hebben ontvangen.</span><span class="sxs-lookup"><span data-stu-id="4781e-115">They can also edit the existing records or enter new loan items, if they've received additional physical items.</span></span>  <span data-ttu-id="4781e-116">Workflow kan worden ingesteld om wijzigingen te routeren naar nieuwe of bestaande leenartikelen via een goedkeuringsproces.</span><span class="sxs-lookup"><span data-stu-id="4781e-116">Workflow can be set up to route changes to new or existing loan items through an approval process.</span></span> 

<span data-ttu-id="4781e-117">Managers kunnen geleende artikelen voor hun directe ondergeschikten weergeven.</span><span class="sxs-lookup"><span data-stu-id="4781e-117">Managers can view loaned items for their direct reports.</span></span> <span data-ttu-id="4781e-118">Ze kunnen ook gemachtigd worden om nieuwe leenartikelen namens hun werknemers toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="4781e-118">They can also be granted permission to add new loan items on behalf of their employees.</span></span>

 <a name="account-for-lost-or-misplaced-loan-items"></a><span data-ttu-id="4781e-119">Rekening voor verloren of beschadigde leenartikelen</span><span class="sxs-lookup"><span data-stu-id="4781e-119">Account for lost or misplaced loan items</span></span>
-----------------------------------------

<span data-ttu-id="4781e-120">Als een artikel beschadigd is of verloren raakt, noteert u een fictieve teruggave.</span><span class="sxs-lookup"><span data-stu-id="4781e-120">If an item becomes damaged or misplaced, enter a fictitious return record.</span></span> <span data-ttu-id="4781e-121">Vervolgens verwijdert u het artikel of laat u het artikel in het overzicht staan, maar vermeldt u dat het artikel niet meer beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="4781e-121">Then either delete the item or keep it in the overview and change the description to indicate that the item is not available.</span></span>


<a name="additional-resources"></a><span data-ttu-id="4781e-122">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="4781e-122">Additional resources</span></span>
--------

[<span data-ttu-id="4781e-123">HRM</span><span class="sxs-lookup"><span data-stu-id="4781e-123">Human resources</span></span>](index.md)





[!INCLUDE[footer-include](../includes/footer-banner.md)]