---
title: " Callcenterorders maken"
description: Deze procedure doorloopt het opzoeken van een klant, het maken van een nieuwe order, het zoeken naar een product en het innen van betaling van de klant.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, SalesTable, MCRSourceIdTargetLookup, MCRSalesQuickQuote, MCRSalesOrderRecap, MCRCustPaymDialog, MCRCustPaymLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08a806514a92a99a9f0b18b36817f49a09516ab8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4964840"
---
# <a name="create-call-center-orders"></a><span data-ttu-id="e74c5-103"> Callcenterorders maken</span><span class="sxs-lookup"><span data-stu-id="e74c5-103">Create call center orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e74c5-104">Deze procedure doorloopt het opzoeken van een klant, het maken van een nieuwe order, het zoeken naar een product en het innen van betaling van de klant.</span><span class="sxs-lookup"><span data-stu-id="e74c5-104">This procedure walks through looking up a customer, creating a new order, searching for a product, and collecting payment from the customer.</span></span> <span data-ttu-id="e74c5-105">Deze procedure gebruikt het demobedrijf USRT en is bedoeld voor de verkoopordermedewerker.</span><span class="sxs-lookup"><span data-stu-id="e74c5-105">This procedure uses demo data company USRT and is intended for the Sales Order Clerk.</span></span> <span data-ttu-id="e74c5-106">Vereisten: de gebruiker die de procedure uitvoert, is ingesteld als een callcentergebruiker en de halfjaarlijkse catalogus van Fabrikam wordt gepubliceerd met minimaal één broncode.</span><span class="sxs-lookup"><span data-stu-id="e74c5-106">Pre-requisites:  The user who completes the procedure is set up as a Call center user and the Fabrikam Semi-Annual Catalog is published with at least one Source code on it.</span></span>

1. <span data-ttu-id="e74c5-107">Ga naar **Retail en Commerce \> Klanten \> Klantenservice**.</span><span class="sxs-lookup"><span data-stu-id="e74c5-107">Go to **Retail and Commerce \> Customers \> Customer service**.</span></span>
2. <span data-ttu-id="e74c5-108">Voer bij **Zoektekst** de zoekcriteria in om de klant te zoeken.</span><span class="sxs-lookup"><span data-stu-id="e74c5-108">For **SearchText**, enter the search criteria to look up the customer.</span></span>
    * <span data-ttu-id="e74c5-109">Voor deze voorbeeldprocedure voert u 'Karen' in en selecteert u **Tab**.</span><span class="sxs-lookup"><span data-stu-id="e74c5-109">For this example procedure, enter "Karen" and select **Tab**.</span></span>  
3. <span data-ttu-id="e74c5-110">Selecteer Zoeken.</span><span class="sxs-lookup"><span data-stu-id="e74c5-110">Select Search.</span></span>
    * <span data-ttu-id="e74c5-111">Aangezien er slechts één klant met de naam Karen voorkomt in de demogegevens, wordt het resultaat automatisch geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="e74c5-111">Since there is only one customer named "Karen" in demo data, the result will be automatically selected.</span></span>  
4. <span data-ttu-id="e74c5-112">Selecteer **Nieuwe verkooporder**.</span><span class="sxs-lookup"><span data-stu-id="e74c5-112">Select **New sales order**.</span></span>
5. <span data-ttu-id="e74c5-113">Vouw de koptekstsectie **Verkooporder** uit of samen.</span><span class="sxs-lookup"><span data-stu-id="e74c5-113">Expand or collapse the **Sales order** header section.</span></span>
6. <span data-ttu-id="e74c5-114">Selecteer de broncode voor de catalogus.</span><span class="sxs-lookup"><span data-stu-id="e74c5-114">Select the source code for the catalog.</span></span>
    * <span data-ttu-id="e74c5-115">Als er geen actieve broncodes zijn, kunt u deze stap overslaan.</span><span class="sxs-lookup"><span data-stu-id="e74c5-115">If there are no active source codes you can skip this step.</span></span>  
7. <span data-ttu-id="e74c5-116">Selecteer **Regel toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e74c5-116">Select **Add line**.</span></span>
8. <span data-ttu-id="e74c5-117">Voer voor **Artikelnummer** de zoekterm voor het artikel in.</span><span class="sxs-lookup"><span data-stu-id="e74c5-117">For **Item number**, enter the item search term.</span></span>
    * <span data-ttu-id="e74c5-118">Voor deze voorbeeldprocedure voert u het gedeeltelijke artikelnummer 8111 in en drukt u op Tab. Het venster voor het zoeken van artikelen wordt dan weergegeven.</span><span class="sxs-lookup"><span data-stu-id="e74c5-118">For this sample procedure, enter a partial item number of '8111' and press tab. This action will bring up the item search window.</span></span>  
9. <span data-ttu-id="e74c5-119">Selecteer het product dat aan de verkooporder moet worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="e74c5-119">Select the product to add to the sales order.</span></span>
10. <span data-ttu-id="e74c5-120">Voer de verkoophoeveelheid in.</span><span class="sxs-lookup"><span data-stu-id="e74c5-120">Enter the sales quantity.</span></span>
11. <span data-ttu-id="e74c5-121">Selecteer **Maken**.</span><span class="sxs-lookup"><span data-stu-id="e74c5-121">Select **Create**.</span></span>
12. <span data-ttu-id="e74c5-122">Selecteer **Voltooien** om de betaling van de klant vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="e74c5-122">Select **Complete** to capture the customer payment.</span></span>
13. <span data-ttu-id="e74c5-123">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e74c5-123">Select **Add**.</span></span>
    * <span data-ttu-id="e74c5-124">De koppeling Toevoegen bevindt zich op het tabblad Betalingen. Vouw het tabblad Betalingen uit als het is samengevouwen.</span><span class="sxs-lookup"><span data-stu-id="e74c5-124">The Add link is in the Payments tab. Expand the Payments tab if it is collapsed.</span></span>  
14. <span data-ttu-id="e74c5-125">Selecteer de betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="e74c5-125">Select the payment method.</span></span>
    * <span data-ttu-id="e74c5-126">Selecteer voor deze procedure de contante betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="e74c5-126">For this procedure, select the cash payment method.</span></span>  
15. <span data-ttu-id="e74c5-127">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="e74c5-127">Close the page.</span></span>
16. <span data-ttu-id="e74c5-128">Geef het bedrag op.</span><span class="sxs-lookup"><span data-stu-id="e74c5-128">Enter the amount.</span></span>
    * <span data-ttu-id="e74c5-129">Voor deze procedure voert u een bedrag in dat gelijk is aan het ordersaldo dat wordt weergegeven op de pagina Overzicht van verkooporder, links van het bedragveld.</span><span class="sxs-lookup"><span data-stu-id="e74c5-129">For this procedure, enter an amount equal to the order balance that can be seen in the Sales order summary page to the left of the amount field.</span></span> <span data-ttu-id="e74c5-130">U kunt de order dan voltooien als volledig betaald.</span><span class="sxs-lookup"><span data-stu-id="e74c5-130">This action will allow you to complete the order as fully paid.</span></span>  
17. <span data-ttu-id="e74c5-131">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="e74c5-131">Select **OK**.</span></span>
18. <span data-ttu-id="e74c5-132">Selecteer **Indienen**.</span><span class="sxs-lookup"><span data-stu-id="e74c5-132">Select **Submit**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e74c5-133">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="e74c5-133">Additional resources</span></span>

[<span data-ttu-id="e74c5-134">Transactionele e-mails aanpassen per leveringsmethode</span><span class="sxs-lookup"><span data-stu-id="e74c5-134">Customize transactional emails by mode of delivery</span></span>](../customize-email-delivery-mode.md)

[<span data-ttu-id="e74c5-135">Leveringsmethode wijzigen in POS</span><span class="sxs-lookup"><span data-stu-id="e74c5-135">Change mode of delivery in POS</span></span>](../pos-change-delivery-mode.md)

