---
title: Verwijzingen naar oorspronkelijke facturen in creditnota's
description: In dit onderwerp wordt uitgelegd hoe u de oorspronkelijke factuurnummers in gerelateerde creditnota's kunt instellen en afdrukken.
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 04a4fc96cb7de60052b17e36c33ad5d5be322be4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207346"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="19c83-103">Verwijzingen naar oorspronkelijke facturen in creditnota's</span><span class="sxs-lookup"><span data-stu-id="19c83-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="19c83-104">In sommige landen en regio's is er een wettelijke vereiste dat afgedrukte creditnota's verwijzingen naar de oorspronkelijke facturen bevatten.</span><span class="sxs-lookup"><span data-stu-id="19c83-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="19c83-105">In dit onderwerp wordt uitgelegd hoe u de oorspronkelijke factuurnummers in gerelateerde creditnota's kunt instellen en afdrukken.</span><span class="sxs-lookup"><span data-stu-id="19c83-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="19c83-106">Vereisten</span><span class="sxs-lookup"><span data-stu-id="19c83-106">Prerequisites</span></span>

- <span data-ttu-id="19c83-107">Schakel in de werkruimte **Functiebeheer** de functie **Creditfactuurindeling voor verkoop- en projectfactuurrapporten** in.</span><span class="sxs-lookup"><span data-stu-id="19c83-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="19c83-108">Zie [Overzicht van functiebeheer](../../fin-and-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="19c83-108">For more information, see [Feature management overview](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="19c83-109">De afdrukbare indelingen van de vereiste documenten moeten in Afdrukbeheer worden geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="19c83-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="19c83-110">De functionaliteit die in dit onderwerp wordt beschreven, is van toepassing op de volgende documenten:</span><span class="sxs-lookup"><span data-stu-id="19c83-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="19c83-111">**Klanten**</span><span class="sxs-lookup"><span data-stu-id="19c83-111">**Accounts receivable**</span></span>

- <span data-ttu-id="19c83-112">Vrije-tekstcreditnota</span><span class="sxs-lookup"><span data-stu-id="19c83-112">Free text credit note</span></span>
- <span data-ttu-id="19c83-113">Creditnota van de klant</span><span class="sxs-lookup"><span data-stu-id="19c83-113">Customer credit note</span></span>

<span data-ttu-id="19c83-114">**Projectbeheer en boekhouding**</span><span class="sxs-lookup"><span data-stu-id="19c83-114">**Project management and accounting**</span></span>

- <span data-ttu-id="19c83-115">Creditnota van project</span><span class="sxs-lookup"><span data-stu-id="19c83-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="19c83-116">De parameters van Klanten configureren</span><span class="sxs-lookup"><span data-stu-id="19c83-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="19c83-117">Volg deze stappen om de parameter in te stellen die bepaalt of verwijzingen naar de oorspronkelijke facturen worden afgedrukt in gerelateerde creditnota's.</span><span class="sxs-lookup"><span data-stu-id="19c83-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="19c83-118">Ga naar **Klanten** \> **Instellen** \> **Parameters van module Klanten**.</span><span class="sxs-lookup"><span data-stu-id="19c83-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="19c83-119">Stel op het tabblad **Updates** op het sneltabblad **Factuur** de optie **Creditfactuurindeling toepassen op verkoop- en projectfactuurrapporten** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="19c83-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![De parameters van Klanten configureren](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="19c83-121">Verwijzingen naar oorspronkelijke facturen definiëren</span><span class="sxs-lookup"><span data-stu-id="19c83-121">Define references to original invoices</span></span>

<span data-ttu-id="19c83-122">Gebruik de volgende procedures om verwijzingen naar oorspronkelijke facturen te definiëren op basis van het documenttype.</span><span class="sxs-lookup"><span data-stu-id="19c83-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="19c83-123">Vrije-tekstcreditnota</span><span class="sxs-lookup"><span data-stu-id="19c83-123">Free text credit note</span></span>

1. <span data-ttu-id="19c83-124">Ga naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**.</span><span class="sxs-lookup"><span data-stu-id="19c83-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="19c83-125">Maak een nieuwe creditnota of selecteer een bestaande creditnota.</span><span class="sxs-lookup"><span data-stu-id="19c83-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="19c83-126">Open de factuur.</span><span class="sxs-lookup"><span data-stu-id="19c83-126">Open the invoice.</span></span>
4. <span data-ttu-id="19c83-127">Selecteer in het actievenster op het tabblad **Factuur** in de groep **Functies** de optie **Factuurcreditering**.</span><span class="sxs-lookup"><span data-stu-id="19c83-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="19c83-128">Voer de verwijzing naar de oorspronkelijke factuur in en selecteer de reden voor de correctie.</span><span class="sxs-lookup"><span data-stu-id="19c83-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![De verwijzing voor een vrije-tekstfactuur definiëren](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="19c83-130">Creditnota van de klant</span><span class="sxs-lookup"><span data-stu-id="19c83-130">Customer credit note</span></span>

1. <span data-ttu-id="19c83-131">Ga naar **Klanten** \> **Orders** \> **Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="19c83-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="19c83-132">Selecteer en open de gefactureerde verkooporder die moet worden gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="19c83-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="19c83-133">Ga in het actievenster naar het tabblad **Verkopen** in de groep **Creditnota** en klik op **Creditnota**.</span><span class="sxs-lookup"><span data-stu-id="19c83-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="19c83-134">Voer de reden voor de correctie in.</span><span class="sxs-lookup"><span data-stu-id="19c83-134">Enter the reason for the correction.</span></span> <span data-ttu-id="19c83-135">De verwijzing naar de oorspronkelijke factuur wordt automatisch gemaakt.</span><span class="sxs-lookup"><span data-stu-id="19c83-135">The reference to the original invoice is automatically established.</span></span>

![De verwijzing voor een verkooporder definiëren](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="19c83-137">Creditnota van project</span><span class="sxs-lookup"><span data-stu-id="19c83-137">Project credit note</span></span>

1. <span data-ttu-id="19c83-138">Ga naar **Projectbeheer en boekhouding** \> **Projectfacturen** \> **Projectfacturen**.</span><span class="sxs-lookup"><span data-stu-id="19c83-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="19c83-139">Selecteer en open de projectfactuur die moet worden gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="19c83-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="19c83-140">Selecteer in het actievenster op het tabblad **Projectfactuur** in de groep **Functies** de optie **Selecteren voor creditnota**.</span><span class="sxs-lookup"><span data-stu-id="19c83-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="19c83-141">Selecteer **Factuurcreditering**.</span><span class="sxs-lookup"><span data-stu-id="19c83-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="19c83-142">Voer de reden voor de correctie in.</span><span class="sxs-lookup"><span data-stu-id="19c83-142">Enter the reason for the correction.</span></span> <span data-ttu-id="19c83-143">De verwijzing naar de oorspronkelijke factuur wordt automatisch gemaakt.</span><span class="sxs-lookup"><span data-stu-id="19c83-143">The reference to the original invoice is automatically established.</span></span>

![De verwijzing voor een projectfactuur definiëren](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="19c83-145">Creditnota's afdrukken</span><span class="sxs-lookup"><span data-stu-id="19c83-145">Printing credit notes</span></span>

<span data-ttu-id="19c83-146">Wanneer u vrije tekst, klanten en projectcreditnota's afdrukt, bevatten deze de verwijzing naar de oorspronkelijke factuur en de reden van de correctie.</span><span class="sxs-lookup"><span data-stu-id="19c83-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![Afgedrukte creditnota](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="19c83-148">Zorg ervoor dat de afdrukbare indelingen van de documenten correct zijn geconfigureerd, op basis van de veronderstelling dat verwijzingen naar oorspronkelijke facturen worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="19c83-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]