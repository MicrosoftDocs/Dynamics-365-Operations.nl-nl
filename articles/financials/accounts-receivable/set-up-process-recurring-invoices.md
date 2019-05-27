---
title: Terugkerende facturen instellen en verwerken
description: In dit artikel wordt beschreven hoe u terugkerende facturen instelt en verwerkt. U kunt terugkerende facturen gebruiken als u klanten regelmatig voor hetzelfde bedrag moet factureren.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustInvoiceTemplate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14011
ms.assetid: 9cc37003-adf1-413d-b2b2-2badcf512e3b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac9e836b0baa24c40554844ea4f3288b80e0c654
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571695"
---
# <a name="set-up-and-process-recurring-invoices"></a><span data-ttu-id="81551-104">Terugkerende facturen instellen en verwerken</span><span class="sxs-lookup"><span data-stu-id="81551-104">Set up and process recurring invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81551-105">In dit artikel wordt beschreven hoe u terugkerende facturen instelt en verwerkt.</span><span class="sxs-lookup"><span data-stu-id="81551-105">This article explains how to set up and process recurring invoices.</span></span> <span data-ttu-id="81551-106">U kunt terugkerende facturen gebruiken als u klanten regelmatig voor hetzelfde bedrag moet factureren.</span><span class="sxs-lookup"><span data-stu-id="81551-106">You can use recurring invoices if you must invoice customers for the same amount on a regular basis.</span></span>

<a name="create-a-recurring-free-text-invoice-template"></a><span data-ttu-id="81551-107">Een sjabloon maken voor een terugkerende vrije-tekstfactuur</span><span class="sxs-lookup"><span data-stu-id="81551-107">Create a recurring free text invoice template</span></span>
---------------------------------------------

<span data-ttu-id="81551-108">Als u klanten voor dezelfde services periodiek wilt factureren, moet u een sjabloon voor vrije-tekstfacturen definiëren die kan worden hergebruikt om de facturen te maken.</span><span class="sxs-lookup"><span data-stu-id="81551-108">To invoice customers for the same services on a regular basis, you must define a free text invoice template that can be reused to create the invoices.</span></span> <span data-ttu-id="81551-109">Deze sjabloon bevat de volgende gegevens:</span><span class="sxs-lookup"><span data-stu-id="81551-109">This template contains the following information:</span></span>

-   <span data-ttu-id="81551-110">Koptekstgegevens, zoals belastinggroepen, betalingsvoorwaarden en de betalingsmethode</span><span class="sxs-lookup"><span data-stu-id="81551-110">Header information, such as tax groups, terms of payment, and the method of payment</span></span>
-   <span data-ttu-id="81551-111">Regelgegevens, zoals serviceomschrijving, opbrengstenrekeningen, eenheidsprijs en factuurbedrag</span><span class="sxs-lookup"><span data-stu-id="81551-111">Line information, such as the service description, revenue accounts, unit price, and invoice amount</span></span>
-   <span data-ttu-id="81551-112">Toeslagen voor verpakken en verzenden</span><span class="sxs-lookup"><span data-stu-id="81551-112">Charges for shipping or handling</span></span>
-   <span data-ttu-id="81551-113">Boekhoudingsverdelingen samen met gegevens over financiële dimensies, zoals kostencentra en bedrijfseenheden</span><span class="sxs-lookup"><span data-stu-id="81551-113">Accounting distributions together with financial dimension information, such as cost centers and business units</span></span>

<span data-ttu-id="81551-114">In feite maakt u een volledige factuur en slaat u deze als een sjabloon op.</span><span class="sxs-lookup"><span data-stu-id="81551-114">In effect, you're creating an entire invoice and saving it as a template.</span></span> <span data-ttu-id="81551-115">U kunt de sjablonen instellen met de pagina **Terugkerende facturen**.</span><span class="sxs-lookup"><span data-stu-id="81551-115">You can set up the templates using the **Recurring invoices** page.</span></span>

## <a name="assign-a-free-text-invoice-template-to-a-customer-and-enter-recurrence-details"></a><span data-ttu-id="81551-116">Een sjabloon voor een vrije-tekstfactuur toewijzen aan een klant en terugkeergegevens invoeren</span><span class="sxs-lookup"><span data-stu-id="81551-116">Assign a free text invoice template to a customer and enter recurrence details</span></span>
<span data-ttu-id="81551-117">Nadat de sjabloon is gemaakt, moet u de sjabloon aan de klanten toewijzen die u wilt factureren.</span><span class="sxs-lookup"><span data-stu-id="81551-117">After the template is created, you must assign the template to the customers that you want to invoice.</span></span> <span data-ttu-id="81551-118">Bovendien moet u opgeven wanneer en hoe vaak de factuur wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="81551-118">Additionally, you must specify when and how often the invoice will be used.</span></span> <span data-ttu-id="81551-119">U kunt de sjablonen op het tabblad **Factuur** van de pagina **Klanten** toewijzen.</span><span class="sxs-lookup"><span data-stu-id="81551-119">You can assign the templates on the **Invoice** tab of the **Customers** page.</span></span> <span data-ttu-id="81551-120">Voeg de sjabloon aan de lijst toe en werk de volgende gegevens bij:</span><span class="sxs-lookup"><span data-stu-id="81551-120">Add the template to the list, and update the following information:</span></span>

-   <span data-ttu-id="81551-121">De begindatum en desgewenst de einddatum voor de terugkerende facturering.</span><span class="sxs-lookup"><span data-stu-id="81551-121">The start date and, optionally, the end date for the recurring billing</span></span>
-   <span data-ttu-id="81551-122">De frequentie van de terugkerende facturering (bijvoorbeeld elke dag of eens per maand)</span><span class="sxs-lookup"><span data-stu-id="81551-122">The frequency of the recurring billing (for example, every day or once a month)</span></span>
-   <span data-ttu-id="81551-123">Het maximale factureringsbedrag (als deze gegevens vereist zijn)</span><span class="sxs-lookup"><span data-stu-id="81551-123">The maximum billing amount (if this information is required)</span></span>

<span data-ttu-id="81551-124">Een klant kan meerdere sjablonen hebben die verschillende frequenties hebben.</span><span class="sxs-lookup"><span data-stu-id="81551-124">A customer can have multiple templates that have different frequencies.</span></span>

## <a name="generate-the-recurring-invoices"></a><span data-ttu-id="81551-125">De terugkerende facturen genereren</span><span class="sxs-lookup"><span data-stu-id="81551-125">Generate the recurring invoices</span></span>
<span data-ttu-id="81551-126">De pagina **Terugkerende facturen** bevat een taak waarmee sjablonen voor terugkerende facturen worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="81551-126">On the **Recurring invoices** page, there is a task that processes recurring invoice templates.</span></span> <span data-ttu-id="81551-127">U geeft de factuurdatum en de sjabloon op op basis waarvan u de facturen wilt genereren.</span><span class="sxs-lookup"><span data-stu-id="81551-127">You specify the invoice date and the template to generate the invoices from.</span></span> <span data-ttu-id="81551-128">Facturen worden gegenereerd en worden als één herhalings-ID toegewezen voor elke groep facturen die wordt verwerkt.</span><span class="sxs-lookup"><span data-stu-id="81551-128">Invoices will be generated and assigned a single recurrence ID number for each group of invoices that is processed.</span></span>

<a name="post-recurring-free-text-invoices"></a><span data-ttu-id="81551-129">Terugkerende vrije-tekstfacturen boeken</span><span class="sxs-lookup"><span data-stu-id="81551-129">Post recurring free text invoices</span></span>
---------------------------------

<span data-ttu-id="81551-130">Nadat terugkerende facturen zijn gegenereerd, wordt de factuurherhalings-ID weergegeven in een boekingstaak op de pagina **Terugkerende facturen**.</span><span class="sxs-lookup"><span data-stu-id="81551-130">After recurring invoices are generated, the invoice recurrence IDs appear in a posting task on the **Recurring invoices** page.</span></span> <span data-ttu-id="81551-131">U kunt alle facturen voor een herhalings-ID weergeven door op de koppeling te klikken.</span><span class="sxs-lookup"><span data-stu-id="81551-131">You can view all of the invoices for a recurrence ID by clicking the link.</span></span> <span data-ttu-id="81551-132">Tijdens de controle van de facturen voor de herhalings-ID kunt u afzonderlijke facturen verwijderen.</span><span class="sxs-lookup"><span data-stu-id="81551-132">During your review of the invoices for the recurrence ID, you can delete individual invoices.</span></span> <span data-ttu-id="81551-133">De herhalingsinstellingen van de klant worden voor die sjabloon opnieuw ingesteld, zodat deze later opnieuw kan worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="81551-133">The customer's recurrence settings will be reset for that template, so that it can be regenerated later.</span></span> <span data-ttu-id="81551-134">U kunt één factuur, een groot aantal facturen of alle facturen voor een herhalings-ID boeken.</span><span class="sxs-lookup"><span data-stu-id="81551-134">You can post one, many, or all of the invoices for a recurrence ID.</span></span> <span data-ttu-id="81551-135">Als workflows worden ingeschakeld, moet u klikken op **Verzenden** voordat u de facturen kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="81551-135">If workflows are enabled, you must click **Submit** before you can post the invoices.</span></span>

<a name="print-recurring-free-text-invoices"></a><span data-ttu-id="81551-136">Terugkerende vrije-tekstfacturen afdrukken</span><span class="sxs-lookup"><span data-stu-id="81551-136">Print recurring free text invoices</span></span>
----------------------------------

<span data-ttu-id="81551-137">Nadat terugkerende facturen zijn geboekt, kunt u de facturen op de pagina met de lijst vrije-tekstfacturen afdrukken.</span><span class="sxs-lookup"><span data-stu-id="81551-137">After recurring invoices are posted, you can print the invoices from the free text invoice list page.</span></span> <span data-ttu-id="81551-138">U kunt de geselecteerde facturen afdrukken of u kunt een bereik facturen selecteren die u wilt afdrukken.</span><span class="sxs-lookup"><span data-stu-id="81551-138">You can print the invoices that are selected, or you can select a range of invoices to print.</span></span>



