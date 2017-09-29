--- 
title: Een leveranciersfactuur in het factuurjournaal registreren
description: Deze taakbegeleiding toont hoe leveranciersfacturen moeten worden geregistreerd die niet aan inkooporders zijn gekoppeld.
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 42f93e6d8fcf62babc3e3244bc1fe76d1efd9d13
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a><span data-ttu-id="c843a-103">Een leveranciersfactuur in het factuurjournaal registreren</span><span class="sxs-lookup"><span data-stu-id="c843a-103">Record a vendor invoice in the invoice journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c843a-104">Deze taakbegeleiding toont hoe leveranciersfacturen moeten worden geregistreerd die niet aan inkooporders zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="c843a-104">This task guide will show how to record vendor invoices that are not associated with purchase orders.</span></span> <span data-ttu-id="c843a-105">Voorbeelden van dit type factuur zijn onkosten voor levering of services.</span><span class="sxs-lookup"><span data-stu-id="c843a-105">Examples of this type of invoice include expenses for supplies or services.</span></span>  <span data-ttu-id="c843a-106">Bij deze registratie wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="c843a-106">This recording uses the USMF demo company.</span></span>

1. <span data-ttu-id="c843a-107">Ga naar Leveranciers > Werkruimten > Leveranciersfactuurregistratie.</span><span class="sxs-lookup"><span data-stu-id="c843a-107">Go to Accounts payable > Workspaces > Vendor invoice entry.</span></span>
2. <span data-ttu-id="c843a-108">Klik op Nieuw factuurjournaal.</span><span class="sxs-lookup"><span data-stu-id="c843a-108">Click New invoice journal.</span></span>
3. <span data-ttu-id="c843a-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="c843a-109">Click New.</span></span>
4. <span data-ttu-id="c843a-110">Voer in het veld Naam de journaalnaam in of klik op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="c843a-110">In the Name field, enter the journal name or click the drop down button to open the lookup.</span></span>
5. <span data-ttu-id="c843a-111">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="c843a-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="c843a-112">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="c843a-112">Click Lines.</span></span>
    * <span data-ttu-id="c843a-113">Voer in het datumveld de boekingsdatum in die Grootboek bijwerkt.</span><span class="sxs-lookup"><span data-stu-id="c843a-113">In the Date field, enter the posting date that will update General Ledger.</span></span>  
7. <span data-ttu-id="c843a-114">Geef in het veld Rekening de leveranciersrekening op.</span><span class="sxs-lookup"><span data-stu-id="c843a-114">In the Account field, specify the Vendor account.</span></span>
8. <span data-ttu-id="c843a-115">Voer in het veld Factuur het factuurnummer in.</span><span class="sxs-lookup"><span data-stu-id="c843a-115">In the Invoice field, enter the invoice number.</span></span>
9. <span data-ttu-id="c843a-116">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="c843a-116">In the Description field, type a value.</span></span>
10. <span data-ttu-id="c843a-117">Voer een nummer in het veld Credit in.</span><span class="sxs-lookup"><span data-stu-id="c843a-117">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="c843a-118">Voer in het veld Tegenrekening het rekeningnummer in of klik op de vervolgkeuzeknop om de zoekopdracht te openen</span><span class="sxs-lookup"><span data-stu-id="c843a-118">In the Offset account field, enter the account number or click the drop down button to open the lookup</span></span>
    * <span data-ttu-id="c843a-119">De btw-groep is afkomstig van de leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="c843a-119">The Sales tax group will default from the vendor account.</span></span>  
    * <span data-ttu-id="c843a-120">De btw-groep van het artikel is afkomstig van de hoofdrekening die is opgegeven in het veld Tegenrekening.</span><span class="sxs-lookup"><span data-stu-id="c843a-120">The Item sales tax group will default from the main account specified in the Offset account field.</span></span>  
    * <span data-ttu-id="c843a-121">De vervaldatum wordt berekend aan de hand van de betalingsvoorwaarden.</span><span class="sxs-lookup"><span data-stu-id="c843a-121">The Due date will be calculated based on the Terms of payment.</span></span>  
    * <span data-ttu-id="c843a-122">De contantkorting is afkomstig van de leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="c843a-122">The Cash discount will default from the Vendor account.</span></span>  
12. <span data-ttu-id="c843a-123">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="c843a-123">Click Post.</span></span>
13. <span data-ttu-id="c843a-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="c843a-124">Close the page.</span></span>


