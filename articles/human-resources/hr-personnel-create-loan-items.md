---
title: Leenartikelen maken
description: Leenartikelen zijn records waarmee u fysieke artikelen, zoals telefoons of computers die uw bedrijf aan werknemers uitleent, bijhoudt.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 28fb201f7951384d847058b05668a7f3e366700a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800232"
---
# <a name="create-loan-items"></a><span data-ttu-id="4fc81-103">Leenartikelen maken</span><span class="sxs-lookup"><span data-stu-id="4fc81-103">Create loan items</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="4fc81-104">Leenartikelen zijn records waarmee u fysieke artikelen, zoals telefoons of computers die uw bedrijf aan werknemers uitleent, bijhoudt.</span><span class="sxs-lookup"><span data-stu-id="4fc81-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="4fc81-105">Elke fysiek artikel moet een bijbehorend leenartikel hebben.</span><span class="sxs-lookup"><span data-stu-id="4fc81-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="4fc81-106">Bij elk leenartikelrecord moet worden beschreven wat er precies wordt uitgeleend, wie ervoor verantwoordelijk is en het aantal dagen dat een artikel kan worden geleend.</span><span class="sxs-lookup"><span data-stu-id="4fc81-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="4fc81-107">U kunt meerdere uitleenartikelen zoals sleutels, toegangskaarten of uniformen tegelijk maken.</span><span class="sxs-lookup"><span data-stu-id="4fc81-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="4fc81-108">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="4fc81-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="4fc81-109">Leningtypen maken</span><span class="sxs-lookup"><span data-stu-id="4fc81-109">Create Loan types</span></span>
1. <span data-ttu-id="4fc81-110">Ga naar Human resources > Werknemers > Leenartikelen > Leningtypen.</span><span class="sxs-lookup"><span data-stu-id="4fc81-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="4fc81-111">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4fc81-111">Click New.</span></span>
3. <span data-ttu-id="4fc81-112">Typ een waarde in het veld Leningtype.</span><span class="sxs-lookup"><span data-stu-id="4fc81-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="4fc81-113">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="4fc81-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4fc81-114">Voer het aantal dagen in dat artikelen die zijn toegewezen aan dit leningtype over tijd mogen zijn.</span><span class="sxs-lookup"><span data-stu-id="4fc81-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="4fc81-115">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4fc81-115">Click Save.</span></span>
7. <span data-ttu-id="4fc81-116">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4fc81-116">Close the page.</span></span>
8. <span data-ttu-id="4fc81-117">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="4fc81-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="4fc81-118">Leenartikelen maken</span><span class="sxs-lookup"><span data-stu-id="4fc81-118">Create Loan items</span></span>
1. <span data-ttu-id="4fc81-119">Ga naar Human resources > Werknemers > Leenartikelen > Leenartikelen.</span><span class="sxs-lookup"><span data-stu-id="4fc81-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="4fc81-120">Klik op Leenartikelen maken.</span><span class="sxs-lookup"><span data-stu-id="4fc81-120">Click Create loan items.</span></span>
3. <span data-ttu-id="4fc81-121">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="4fc81-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="4fc81-122">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="4fc81-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4fc81-123">Klik in het veld Leningtype op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="4fc81-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4fc81-124">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="4fc81-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="4fc81-125">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4fc81-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4fc81-126">Het aantal dagen invoeren dat het artikel kan worden uitgeleend.</span><span class="sxs-lookup"><span data-stu-id="4fc81-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="4fc81-127">De standaardwaarde van het veld Geplande teruggave op de pagina Geleende uitrusting wordt berekend als de huidige datum plus dit getal.</span><span class="sxs-lookup"><span data-stu-id="4fc81-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="4fc81-128">Klik in het veld Verantwoordelijke persoon op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="4fc81-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="4fc81-129">Klik op Selecteren.</span><span class="sxs-lookup"><span data-stu-id="4fc81-129">Click Select.</span></span>
11. <span data-ttu-id="4fc81-130">Typ een waarde in het veld Beginwaarde.</span><span class="sxs-lookup"><span data-stu-id="4fc81-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="4fc81-131">Typ een getal in het veld Interval.</span><span class="sxs-lookup"><span data-stu-id="4fc81-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="4fc81-132">Typ een waarde in het veld Notatie.</span><span class="sxs-lookup"><span data-stu-id="4fc81-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="4fc81-133">Als het beginnummer voor een leenartikel bijvoorbeeld 10 is, voert u twee hekjes in het veld Notatie in.</span><span class="sxs-lookup"><span data-stu-id="4fc81-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="4fc81-134">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="4fc81-134">Click OK.</span></span>
15. <span data-ttu-id="4fc81-135">Vernieuw de pagina.</span><span class="sxs-lookup"><span data-stu-id="4fc81-135">Refresh the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]