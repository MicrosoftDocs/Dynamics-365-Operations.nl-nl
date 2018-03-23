---
title: Externe catalogi gebruiken voor PunchOut eProcurement
description: In dit onderwerp wordt uitgelegd hoe u kunt externe catalogi maakt en inkoopopdrachten indient.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 30211
ms.assetid: 3c7e0e1c-703c-4bbf-b90c-84d29a131360
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 76d0c911bdddbc5a34644dc96ec13dd8fd53a338
ms.contentlocale: nl-nl
ms.lasthandoff: 03/07/2018

---

# <a name="use-external-catalogs-for-punchout-eprocurement"></a><span data-ttu-id="8b00e-103">Externe catalogi gebruiken voor PunchOut eProcurement</span><span class="sxs-lookup"><span data-stu-id="8b00e-103">Use external catalogs for PunchOut eProcurement</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8b00e-104">Als u externe catalogi voor PunchOut eProcurement gebruikt, hoeft u geen gegevens over producten van uw leveranciers in uw eigen hoofdgegevens te beheren.</span><span class="sxs-lookup"><span data-stu-id="8b00e-104">By using external catalogs for PunchOut e-procurement, you don't have to maintain information about your vendors' products in your own master data.</span></span> <span data-ttu-id="8b00e-105">In plaats daarvan wordt de winkelwagen op de website van de leverancier geconverteerd naar inkoopopdrachtregels met de juiste productinformatie.</span><span class="sxs-lookup"><span data-stu-id="8b00e-105">Instead, the shopping cart on a vendor's website is converted to requisition lines that have the correct product information.</span></span> 

<span data-ttu-id="8b00e-106">Zo vermijdt u dat u de beschrijvingen en prijzen van de producten van uw leveranciers in uw eigen producthoofdgegevens moet opslaan en onderhouden.</span><span class="sxs-lookup"><span data-stu-id="8b00e-106">You should avoid maintaining the descriptions and prices of your vendors’ products in your own product master data.</span></span> <span data-ttu-id="8b00e-107">In plaats daarvan gebruikt u externe catalogi voor PunchOut eProcurement.</span><span class="sxs-lookup"><span data-stu-id="8b00e-107">Instead, use external catalogs for PunchOut e-procurement.</span></span> <span data-ttu-id="8b00e-108">Wanneer werknemers dan inkoopopdrachten maken, kunnen ze "uitklokken" naar de externe catalogussite van een leverancier, dat wil zeggen dat ze uw systeem verlaten en naar de website van de leverancier gaan.</span><span class="sxs-lookup"><span data-stu-id="8b00e-108">Then, when employees create requisitions, they can “punch out” to a vendor’s external catalog site (in other words, they leave your system and go to the vendor’s site).</span></span> <span data-ttu-id="8b00e-109">De producten die worden toegevoegd aan de winkelwagen op de website van de leverancier, kunnen vervolgens worden geconverteerd naar inkoopopdrachtregels.</span><span class="sxs-lookup"><span data-stu-id="8b00e-109">The products that are added to the shopping cart on the vendor’s website can then be converted to requisition lines.</span></span> <span data-ttu-id="8b00e-110">U krijgt daarmee de juiste productinformatie: id, naam, prijs en andere gegevens van het product.</span><span class="sxs-lookup"><span data-stu-id="8b00e-110">Therefore, you get the correct product information: product ID, name, price, and so on.</span></span>

<span data-ttu-id="8b00e-111">Als u externe catalogi wilt gebruiken, moet een werknemer een bestelopdracht maken op de pagina **Mijn opdrachten tot inkoop**.</span><span class="sxs-lookup"><span data-stu-id="8b00e-111">To use external catalogs, an employee must create a requisition on the **My purchase requisitions** page.</span></span>

<span data-ttu-id="8b00e-112">De werknemer die een opdracht tot inkoop maakt, wordt de voorbereider van de inkoopopdracht genoemd.</span><span class="sxs-lookup"><span data-stu-id="8b00e-112">The employee who creates a requisition is referred to as the preparer of the requisition.</span></span> <span data-ttu-id="8b00e-113">Als voorbereider kunt u de volgende taken uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="8b00e-113">As a preparer, you can complete the following tasks.</span></span>

<span data-ttu-id="8b00e-114">De regelactie **Externe catalogi** gebruiken om een pagina te openen met alle externe catalogi die beschikbaar voor de opgegeven aanvrager zijn, kopende rechtspersoon en ontvangende operationele eenheid.</span><span class="sxs-lookup"><span data-stu-id="8b00e-114">Use the **External catalogs** line action to open a page that includes all external catalogs that are available for the specified requester, buying legal entity, and receiving operating unit.</span></span>

<span data-ttu-id="8b00e-115">Afhankelijk van uw machtigingen, de aanvrager, kopende rechtspersoon en ontvangende operationele eenheid aanpassen.</span><span class="sxs-lookup"><span data-stu-id="8b00e-115">Depending on your permissions, change the requester, buying legal entity, and receiving operating unit.</span></span> <span data-ttu-id="8b00e-116">Een wijziging in deze waarden kan de lijst wijzigen met externe catalogi die beschikbaar voor een aanvrager zijn.</span><span class="sxs-lookup"><span data-stu-id="8b00e-116">A change in those values might change the list of external catalogs that are available to a requester.</span></span> <span data-ttu-id="8b00e-117">Welke externe catalogi beschikbaar zijn, is afhankelijk van het huidige actieve inkoopbeleid voor de kopende rechtspersoon of de ontvangende operationele eenheid.</span><span class="sxs-lookup"><span data-stu-id="8b00e-117">The external catalogs that are available depend on the current active purchasing policies for the buying legal entity or the receiving operating unit.</span></span> <span data-ttu-id="8b00e-118">Dit beleid kan toegang tot specifieke aanschaffingscategorieën toestaan of voorkomen.</span><span class="sxs-lookup"><span data-stu-id="8b00e-118">These policies can allow or prevent access to specific procurement categories.</span></span> <span data-ttu-id="8b00e-119">Daardoor kan de lijst met externe catalogi die zijn toegewezen aan deze inkoopcategorieën worden beïnvloed.</span><span class="sxs-lookup"><span data-stu-id="8b00e-119">Therefore, the list of external catalogs that are mapped to these procurement categories can be affected.</span></span>

<span data-ttu-id="8b00e-120">Zie voor meer informatie over het beleid het onderwerp [Inkoopbeleid](../procurement/purchase-policies.md).</span><span class="sxs-lookup"><span data-stu-id="8b00e-120">For more information about policies, see [Purchasing policies](../procurement/purchase-policies.md).</span></span>

- <span data-ttu-id="8b00e-121">Voer tekst in het cataloguszoekveld in om externe catalogi voor specifieke inkoopcategorieën te vinden.</span><span class="sxs-lookup"><span data-stu-id="8b00e-121">To find external catalogs for specific procurement categories, enter text in the catalog search field.</span></span>
- <span data-ttu-id="8b00e-122">Als u producten wilt toevoegen uit een externe leverancierscatalogus op de website van de leverancier, klikt u op de externe catalogus.</span><span class="sxs-lookup"><span data-stu-id="8b00e-122">To add products from a vendor’s external catalog on the vendor’s website, click the external catalog.</span></span> <span data-ttu-id="8b00e-123">Vervolgens voegt u producten toe aan de winkelwagen en checkt u ze uit. De winkelwagenregels worden overgebracht naar Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8b00e-123">Then add products to the shopping cart, and check out. The shopping cart lines will be transferred to Microsoft Dynamics 365.</span></span>

<span data-ttu-id="8b00e-124">Als er meerdere opties voor aanschaffingscategorieën zijn, selecteert u de juiste aanschaffingscategorie voordat u de regels aan de inkoopopdracht toevoegt.</span><span class="sxs-lookup"><span data-stu-id="8b00e-124">If there are multiple options for procurement categories, select the correct procurement category before you add the lines to the requisition.</span></span>
<span data-ttu-id="8b00e-125">Nadat de regels zijn toegevoegd aan een inkoopopdracht, kunt u meer regels toevoegen zonder externe catalogi te hoeven gebruiken.</span><span class="sxs-lookup"><span data-stu-id="8b00e-125">After lines have been added to a requisition, you can add more lines without using external catalogs.</span></span> <span data-ttu-id="8b00e-126">U kunt ook doorgaan met het toevoegen van regels vanuit externe catalogi.</span><span class="sxs-lookup"><span data-stu-id="8b00e-126">Alternatively, you can continue to use external catalogs to add lines.</span></span>

<span data-ttu-id="8b00e-127">Wanneer de inkoopopdracht klaar is, gebruikt u de actie **Workflow** > **Verzenden** om de opdracht ter goedkeuring aan te bieden.</span><span class="sxs-lookup"><span data-stu-id="8b00e-127">When the requisition is ready, use the **Workflow** > **Submit** action to submit it for approval.</span></span>

