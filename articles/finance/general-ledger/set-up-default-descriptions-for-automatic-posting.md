---
title: Standaard beschrijvingen voor automatische boeking instellen
description: Dit onderwerp verklaart hoe u de standaardtekst kunt instellen die wordt gebruikt om boekhoudinvoeringen te beschrijven die automatisch in het grootboek zijn geboekt. U kunt een standaard beschrijvingstekst instellen met vrije tekst of door vaste variabelen te selecteren.
author: aprilolson
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: ''
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: eb89f50a3d227cad80226ce30f71c4f210129245
ms.sourcegitcommit: 0262a19e32b2c0c84c731d9f4fbe8ba91822afa3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/15/2019
ms.locfileid: "2622684"
---
# <a name="set-up-default-descriptions-for-automatic-posting"></a><span data-ttu-id="6dd00-104">Standaard beschrijvingen voor automatische boeking instellen</span><span class="sxs-lookup"><span data-stu-id="6dd00-104">Set up default descriptions for automatic posting</span></span>

<span data-ttu-id="6dd00-105">Dit onderwerp verklaart hoe u de standaardtekst kunt instellen die wordt gebruikt om boekhoudinvoeringen te beschrijven die automatisch in het grootboek zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="6dd00-105">This topic explains how to set up default text that is used to describe accounting entries that are posted automatically to the general ledger.</span></span> <span data-ttu-id="6dd00-106">U kunt een standaard beschrijvingstekst instellen met vrije tekst of door vaste variabelen te selecteren.</span><span class="sxs-lookup"><span data-stu-id="6dd00-106">You can set up default description text by using free-form text or by selecting fixed variables.</span></span>

> [!NOTE]
> <span data-ttu-id="6dd00-107">Voor een aantal transactietypes in een aantal landen of regio's kunt u ook tekst invoegen uit velden in de Microsoft Dynamics AX-database die aan deze transactietypes zijn gerelateerd.</span><span class="sxs-lookup"><span data-stu-id="6dd00-107">For some transaction types in some countries or regions, you can also include text from fields in the Microsoft Dynamics AX database that are related to those transaction types.</span></span> <span data-ttu-id="6dd00-108">Zie voor een lijst met transactietypen en de landen en regio's de sectie [Optioneel: Andere tekst aan standaardbeschrijvingen toevoegen](#optional-add-other-text-to-default-descriptions), verderop in dit onderwerp.</span><span class="sxs-lookup"><span data-stu-id="6dd00-108">For a list of the transaction types, and the countries and regions, see the [Optional: Add other text to default descriptions](#optional-add-other-text-to-default-descriptions) section later in this topic.</span></span>

## <a name="set-up-default-descriptions"></a><span data-ttu-id="6dd00-109">Standaardbeschrijvingen opzetten</span><span class="sxs-lookup"><span data-stu-id="6dd00-109">Set up default descriptions</span></span>

1. <span data-ttu-id="6dd00-110">Ga naar **Organisatiebeheer** \> **Instellen** \> **Standaardbeschrijvingen**.</span><span class="sxs-lookup"><span data-stu-id="6dd00-110">Go to **Organization administration** \> **Setup** \> **Default descriptions**.</span></span>
2. <span data-ttu-id="6dd00-111">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="6dd00-111">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="6dd00-112">Selecteer in het veld **Beschrijving** het transactietype waarvoor een standaardbeschrijving moet worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6dd00-112">In the **Description** field, select the type of transaction to create a default description for.</span></span>
4. <span data-ttu-id="6dd00-113">Selecteer in het veld **Taal** de taal waarop de beschrijving van toepassing is.</span><span class="sxs-lookup"><span data-stu-id="6dd00-113">In the **Language** field, select the language that the description applies to.</span></span>
5. <span data-ttu-id="6dd00-114">Voer in het veld **Tekst** de standaardbeschrijving in.</span><span class="sxs-lookup"><span data-stu-id="6dd00-114">In the **Text** field, enter the default description.</span></span> <span data-ttu-id="6dd00-115">U kunt ook tekst in het veld typen of u kunt een of meer van de volgende tekstvariabelen gebruiken:</span><span class="sxs-lookup"><span data-stu-id="6dd00-115">You can type text in the field, or you can use one or more of the following free-text variables:</span></span>

    - <span data-ttu-id="6dd00-116">**%1**: hiermee voegt u de transactiedatum toe.</span><span class="sxs-lookup"><span data-stu-id="6dd00-116">**%1** – Add the transaction date.</span></span>
    - <span data-ttu-id="6dd00-117">**%2**: hiermee voegt u een id toe die overeenkomt met het type document dat naar het grootboek wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="6dd00-117">**%2** – Add an identifier that corresponds to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="6dd00-118">Voor transactietypes die zijn gerelateerd aan facturen, voegt u met de variabele **%2** bijvoorbeeld het factuurnummer toe.</span><span class="sxs-lookup"><span data-stu-id="6dd00-118">For example, for transaction types that are related to invoices, the **%2** variable adds the invoice number.</span></span>
    - <span data-ttu-id="6dd00-119">**%3**: hiermee voegt u een id toe die is gerelateerd aan het type document dat naar het grootboek wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="6dd00-119">**%3** – Add an identifier that is related to the document type that is being posted to the general ledger.</span></span> <span data-ttu-id="6dd00-120">Voor transactietypes die zijn gerelateerd aan facturen, voegt u met de variabele **%3** bijvoorbeeld het klantaccountnummer toe.</span><span class="sxs-lookup"><span data-stu-id="6dd00-120">For example, for transaction types that are related to invoices, the **%3** variable adds the customer account number.</span></span>

## <a name="optional-add-other-text-to-default-descriptions"></a><span data-ttu-id="6dd00-121">Optioneel: Voeg andere tekst aan standaard beschrijvingen</span><span class="sxs-lookup"><span data-stu-id="6dd00-121">Optional: Add other text to default descriptions</span></span>

<span data-ttu-id="6dd00-122">Voor een aantal transactietypes in een aantal landen of regio's kunnen standaardbeschrijvingen tekst bevatten die afkomstig is uit velden in de database die zijn gerelateerd aan deze transactietypes.</span><span class="sxs-lookup"><span data-stu-id="6dd00-122">For some transaction types in some countries or regions, default descriptions can include text that comes from fields in your data that are related to those transaction types.</span></span> <span data-ttu-id="6dd00-123">De volgende lijsten bevatten de transactietypes en de landen en regio's waarvoor deze optie beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="6dd00-123">The following lists show the transaction types, and the countries and regions, that this option is available for.</span></span>

<span data-ttu-id="6dd00-124">**Transactietypen**</span><span class="sxs-lookup"><span data-stu-id="6dd00-124">**Transaction types**</span></span>

<span data-ttu-id="6dd00-125">U kunt andere tekst voor standaardbeschrijvingen toevoegen voor transactietypen die aan de volgende documenttypes worden gekoppeld:</span><span class="sxs-lookup"><span data-stu-id="6dd00-125">You can add other text to default descriptions for transaction types that are related to the following document types:</span></span>

- <span data-ttu-id="6dd00-126">Klantfacturen</span><span class="sxs-lookup"><span data-stu-id="6dd00-126">Customer invoices</span></span>
- <span data-ttu-id="6dd00-127">Creditnota's van de klant</span><span class="sxs-lookup"><span data-stu-id="6dd00-127">Customer credit notes</span></span>
- <span data-ttu-id="6dd00-128">Contact betalingen van de klant</span><span class="sxs-lookup"><span data-stu-id="6dd00-128">Customer cash payments</span></span>
- <span data-ttu-id="6dd00-129">Leveranciersbetalingen</span><span class="sxs-lookup"><span data-stu-id="6dd00-129">Vendor payments</span></span>
- <span data-ttu-id="6dd00-130">Verkooporders</span><span class="sxs-lookup"><span data-stu-id="6dd00-130">Sales orders</span></span>
- <span data-ttu-id="6dd00-131">Inkooporders</span><span class="sxs-lookup"><span data-stu-id="6dd00-131">Purchase orders</span></span>
- <span data-ttu-id="6dd00-132">Voorraadjournalen</span><span class="sxs-lookup"><span data-stu-id="6dd00-132">Inventory journals</span></span>
- <span data-ttu-id="6dd00-133">Hoofdplanning (MRP)</span><span class="sxs-lookup"><span data-stu-id="6dd00-133">Master planning (MRP)</span></span>
- <span data-ttu-id="6dd00-134">Vaste activa</span><span class="sxs-lookup"><span data-stu-id="6dd00-134">Fixed assets</span></span>

<span data-ttu-id="6dd00-135">**Landen en regio's**</span><span class="sxs-lookup"><span data-stu-id="6dd00-135">**Countries and regions**</span></span>

<span data-ttu-id="6dd00-136">Deze optie is beschikbaar voor de volgende landen en regio's:</span><span class="sxs-lookup"><span data-stu-id="6dd00-136">This option is available for the following countries and regions:</span></span>

- <span data-ttu-id="6dd00-137">Brazilië</span><span class="sxs-lookup"><span data-stu-id="6dd00-137">Brazil</span></span>
- <span data-ttu-id="6dd00-138">China</span><span class="sxs-lookup"><span data-stu-id="6dd00-138">China</span></span>
- <span data-ttu-id="6dd00-139">Tsjechische Republiek</span><span class="sxs-lookup"><span data-stu-id="6dd00-139">Czech Republic</span></span>
- <span data-ttu-id="6dd00-140">Oost-Europa</span><span class="sxs-lookup"><span data-stu-id="6dd00-140">Eastern Europe</span></span>
- <span data-ttu-id="6dd00-141">Hongarije</span><span class="sxs-lookup"><span data-stu-id="6dd00-141">Hungary</span></span>
- <span data-ttu-id="6dd00-142">India</span><span class="sxs-lookup"><span data-stu-id="6dd00-142">India</span></span>
- <span data-ttu-id="6dd00-143">Japan</span><span class="sxs-lookup"><span data-stu-id="6dd00-143">Japan</span></span>
- <span data-ttu-id="6dd00-144">Litouwen</span><span class="sxs-lookup"><span data-stu-id="6dd00-144">Lithuania</span></span>
- <span data-ttu-id="6dd00-145">Letland</span><span class="sxs-lookup"><span data-stu-id="6dd00-145">Latvia</span></span>
- <span data-ttu-id="6dd00-146">Polen</span><span class="sxs-lookup"><span data-stu-id="6dd00-146">Poland</span></span>
- <span data-ttu-id="6dd00-147">Rusland</span><span class="sxs-lookup"><span data-stu-id="6dd00-147">Russia</span></span>

### <a name="add-text-to-default-descriptions"></a><span data-ttu-id="6dd00-148">Voeg tekst toe aan standaard beschrijvingen</span><span class="sxs-lookup"><span data-stu-id="6dd00-148">Add text to default descriptions</span></span>

<span data-ttu-id="6dd00-149">Wanneer u de stappen in de sectie [Standaardbeschrijvingen instellen](#set-up-default-descriptions), eerder in dit onderwerp hebt voltooid, volgt u deze stappen om andere tekst aan de standaardbeschrijvingen toe te voegen:</span><span class="sxs-lookup"><span data-stu-id="6dd00-149">After you complete the steps in the [Set up default descriptions](#set-up-default-descriptions) section earlier in this topic, follow these steps to add other text to the default descriptions.</span></span>

1. <span data-ttu-id="6dd00-150">Selecteer op het sneltabblad **Parameters** de optie **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="6dd00-150">On the **Parameters** FastTab, select **Add**.</span></span>
2. <span data-ttu-id="6dd00-151">Selecteer in het veld **Referentietabel** de databasetabel met de parametergegevens die u aan de beschrijving wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6dd00-151">In the **Reference table** field, select the database table from which to add parameter data to the description.</span></span>
3. <span data-ttu-id="6dd00-152">Selecteer in het veld **Referentieveld** het veld met de parametergegevens die u aan de beschrijving wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6dd00-152">In the **Reference field** field, select the field from which to add parameter data to the description.</span></span>
4. <span data-ttu-id="6dd00-153">Herhaal stappen 1 tot 3 als u nog meer parameters wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="6dd00-153">Repeat steps 1 through 3 to add more parameters.</span></span>