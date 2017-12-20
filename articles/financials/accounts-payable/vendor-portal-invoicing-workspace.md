---
title: Werkgebied voor samenwerkingsfacturering van leveranciers
description: In dit onderwerp wordt beschreven hoe u leveranciersfacturen kunt weergeven en facturen indient vanuit het samenwerkingswerkgebied voor leveranciersfacturering.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 221534
ms.assetid: c4ed62f3-d351-41d7-a2ad-790576cde4ab
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: ff1818d927f7ab9212c4d5d9109c426be5e0e152
ms.openlocfilehash: 0d11e4fecc4c42636be63c1ce622f0b2f8e58f2c
ms.contentlocale: nl-nl
ms.lasthandoff: 11/29/2017

---

# <a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="6ae39-103">Werkgebied voor samenwerkingsfacturering van leveranciers</span><span class="sxs-lookup"><span data-stu-id="6ae39-103">Vendor collaboration invoicing workspace</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6ae39-104">In dit onderwerp wordt beschreven hoe u leveranciersfacturen kunt weergeven en facturen indient vanuit het samenwerkingswerkgebied voor leveranciersfacturering.</span><span class="sxs-lookup"><span data-stu-id="6ae39-104">This topic explains how you can view vendor invoices and submit invoices from the vendor collaboration invoicing workspace.</span></span>

<span data-ttu-id="6ae39-105">Het werkgebied **Leverancierssamenwerkingsfacturen** kan worden gebruikt om leveranciersfactuurinformatie weer te geven en facturen te verzenden naar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, door middel van workflowmogelijkheden.</span><span class="sxs-lookup"><span data-stu-id="6ae39-105">The **Vendor collaboration invoicing** workspace can be used to view vendor invoice information and to submit invoices to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition using workflow capabilities.</span></span>


<a name="vendor-collaboration-invoicing-workspace"></a><span data-ttu-id="6ae39-106">Werkgebied voor samenwerkingsfacturering van leveranciers</span><span class="sxs-lookup"><span data-stu-id="6ae39-106">Vendor collaboration invoicing workspace</span></span>
----------------------------------------

### <a name="summary-tiles"></a><span data-ttu-id="6ae39-107">Overzichtstegels</span><span class="sxs-lookup"><span data-stu-id="6ae39-107">Summary tiles</span></span>

<span data-ttu-id="6ae39-108">De tegels **Overzicht** geven een overzicht van de facturen voor de geselecteerde leverancier.</span><span class="sxs-lookup"><span data-stu-id="6ae39-108">The **Summary** tiles give an overview of the invoices for the selected vendor.</span></span> <span data-ttu-id="6ae39-109">U kunt facturen op hun status weergeven.</span><span class="sxs-lookup"><span data-stu-id="6ae39-109">You can view invoices by their state.</span></span>
-   <span data-ttu-id="6ae39-110">Conceptfacturen zijn niet ingediend bij de workflow.</span><span class="sxs-lookup"><span data-stu-id="6ae39-110">Draft invoices have not been submitted to workflow.</span></span>
-   <span data-ttu-id="6ae39-111">De verzonden, niet-goedgekeurde facturen zijn facturen die de leverancier heeft ingediend, maar die niet zijn geboekt in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ae39-111">Submitted, not approved invoices are those invoices that the vendor has submitted, but they have not been posted in Finance and Operations.</span></span>
-   <span data-ttu-id="6ae39-112">Goedgekeurde, niet-betaalde facturen zijn facturen die zijn geboekt in Finance and Operations maar die nog niet volledig zijn betaald.</span><span class="sxs-lookup"><span data-stu-id="6ae39-112">Approved, not paid invoices are those that have been posted in Finance and Operations, but they have not yet been fully paid.</span></span>
-   <span data-ttu-id="6ae39-113">Betaalde facturen zijn facturen die volledig zijn betaald in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="6ae39-113">Paid invoices are those that have been fully paid in Finance and Operations.</span></span>

<span data-ttu-id="6ae39-114">Klik op een tegel om een gefilterde weergave van de pagina **Facturenlijst** te openen.</span><span class="sxs-lookup"><span data-stu-id="6ae39-114">Clicking on a tile will open a filtered view of the **Invoices list** page.</span></span>
### <a name="tabular-lists"></a><span data-ttu-id="6ae39-115">Lijsten in tabelvorm</span><span class="sxs-lookup"><span data-stu-id="6ae39-115">Tabular lists</span></span>

<span data-ttu-id="6ae39-116">In de sectie **Lijsten in tabelvorm** wordt de factureringsstatus onderverdeeld als de overzichtstegels: Concept en Verzonden, niet-goedgekeurde lijsten.</span><span class="sxs-lookup"><span data-stu-id="6ae39-116">In the **Tabular lists** section, the status of the invoicing is broken down in similar ways as the summary tiles: Draft and Submitted, not approved lists.</span></span> <span data-ttu-id="6ae39-117">In de Conceptstatus kan een factuur naar de workflow zijn verzonden of zijn verwijderd.</span><span class="sxs-lookup"><span data-stu-id="6ae39-117">While in the Draft state, an invoice can be submitted to workflow or deleted.</span></span> <span data-ttu-id="6ae39-118">De laatste lijst in tabelvorm is een optie om facturen te zoeken.</span><span class="sxs-lookup"><span data-stu-id="6ae39-118">The last tabular list is an option to find invoices.</span></span> <span data-ttu-id="6ae39-119">U kunt filteren tijdens het zoeken, zodat het zoeken sneller verloopt.</span><span class="sxs-lookup"><span data-stu-id="6ae39-119">You can filter as you search, to allow for faster searches.</span></span>
<span data-ttu-id="6ae39-120">Lijstpagina met alle leveranciersfacturen</span><span class="sxs-lookup"><span data-stu-id="6ae39-120">All vendor invoices list page</span></span>
-----------------------------

<span data-ttu-id="6ae39-121">U kunt alle geboekte en niet-geboekte leveranciersfacturen weergeven op de lijstpagina **Samenwerkingsfacturen van leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="6ae39-121">You can view all posted and unposted vendor invoices on the **Vendor collaboration invoices** list page.</span></span> <span data-ttu-id="6ae39-122">Gebruik deze lijstpagina om de betalingsstatus van de facturen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="6ae39-122">You can use this list page to view the payment status of the invoices.</span></span> <span data-ttu-id="6ae39-123">De betalingsstatussen zijn Niet-geboekt, Onbetaald, Gedeeltelijk betaald en Volledig betaald.</span><span class="sxs-lookup"><span data-stu-id="6ae39-123">The payment statuses include Unposted, Unpaid, Partially paid, and Fully paid.</span></span>
<span data-ttu-id="6ae39-124">Een nieuwe factuur maken van een inkooporder</span><span class="sxs-lookup"><span data-stu-id="6ae39-124">Creating a new invoice from a purchase order</span></span>
--------------------------------------------

<span data-ttu-id="6ae39-125">U kunt een nieuwe leveranciersfactuur maken door **Nieuwe** actie te selecteren in het werkgebied **Samenwerkingsfacturering van leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="6ae39-125">You can create a new vendor invoice by selecting the **New** action on the **Vendor collaboration invoicing** workspace.</span></span> <span data-ttu-id="6ae39-126">Het inkoopordernummer en het factuurnummer moeten door de leverancier worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="6ae39-126">The purchase order number and invoice number must be provided by the vendor.</span></span> <span data-ttu-id="6ae39-127">Standaard worden alle regels van de inkooporder van de leverancier op de nieuwe factuur weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6ae39-127">By default, all of the lines from the vendor's purchase order will appear on the new invoice.</span></span> <span data-ttu-id="6ae39-128">Gegevens over de hoeveelheid en de kostprijs kunnen worden bewerkt vóór het verzenden van de leveranciersfactuur naar de workflow.</span><span class="sxs-lookup"><span data-stu-id="6ae39-128">The quantity and cost information can be edited prior to submitting the vendor invoice to workflow.</span></span> <span data-ttu-id="6ae39-129">U kunt bestanden, notities, afbeeldingen en URL's aan een factuur koppelen voordat deze wordt verzenden.</span><span class="sxs-lookup"><span data-stu-id="6ae39-129">You can attach files, notes, images, and URLs to an invoice before submitting it.</span></span>



<span data-ttu-id="6ae39-130">Zie voor meer informatie [Leverancierssamenwerking met externe leveranciers](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="6ae39-130">For more information, see [Vendor collaboration with external vendors](../../supply-chain/procurement/vendor-collaboration-work-external-vendors.md)</span></span>




