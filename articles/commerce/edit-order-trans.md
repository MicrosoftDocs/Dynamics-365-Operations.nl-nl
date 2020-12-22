---
title: Online orders en asynchrone ordertransacties van klanten bewerken en controleren
description: In dit onderwerp wordt beschreven hoe online orders en asynchrone ordertransacties van klanten in Microsoft Dynamics 365 Commerce kunnen worden bewerkt en gecontroleerd.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9f2db25c8897662baa177752d0c5fc4ac6178a4
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/04/2020
ms.locfileid: "4458805"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="50cf1-103">Online orders en asynchrone ordertransacties van klanten bewerken en controleren</span><span class="sxs-lookup"><span data-stu-id="50cf1-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50cf1-104">In dit onderwerp wordt beschreven hoe online orders en asynchrone ordertransacties van klanten in Microsoft Dynamics 365 Commerce kunnen worden bewerkt en gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="50cf1-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="50cf1-105">Overzicht</span><span class="sxs-lookup"><span data-stu-id="50cf1-105">Overview</span></span>

<span data-ttu-id="50cf1-106">Tussen Commerce-versies 10.0.5 en 10.0.6 is ondersteuning toegevoegd voor het bewerken van contante transacties (zoals verkopen en retouren) en beheertransacties in contant geld (zoals wisselgeld invoeren en verwijderen).</span><span class="sxs-lookup"><span data-stu-id="50cf1-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="50cf1-107">In Commerce versie 10.0.7 is ondersteuning toegevoegd voor het bewerken van online ordertransacties en asynchrone klantordertransacties.</span><span class="sxs-lookup"><span data-stu-id="50cf1-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="50cf1-108">Ordertransacties bewerken en controleren</span><span class="sxs-lookup"><span data-stu-id="50cf1-108">Edit and audit order transactions</span></span>

<span data-ttu-id="50cf1-109">Voer de volgende stappen uit om ordertransacties in Commerce Headquarters te bewerken en te controleren.</span><span class="sxs-lookup"><span data-stu-id="50cf1-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="50cf1-110">Installeer de [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span><span class="sxs-lookup"><span data-stu-id="50cf1-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="50cf1-111">Geef op de pagina **Detailhandelparameters** op het tabblad **Klantorders** op het sneltabblad **Order** een wachtcode op voor **Wachtcode voor ordersynchronisatiefouten**.</span><span class="sxs-lookup"><span data-stu-id="50cf1-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="50cf1-112">Open het werkgebied **Financiën van winkel**.</span><span class="sxs-lookup"><span data-stu-id="50cf1-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="50cf1-113">De tegels **Synchronisatiefouten voor online orders** en **Synchronisatiefouten voor klantorders** bieden een vooraf gefilterde weergave van de pagina met detailhandelstransacties.</span><span class="sxs-lookup"><span data-stu-id="50cf1-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="50cf1-114">Elke tegel toont de transactierecords die niet zijn gesynchroniseerd voor het bijbehorende ordertype.</span><span class="sxs-lookup"><span data-stu-id="50cf1-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="50cf1-115">Open de pagina **Synchronisatiefouten voor online orders** of de pagina **Synchronisatiefouten voor klantorders**.</span><span class="sxs-lookup"><span data-stu-id="50cf1-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="50cf1-116">Selecteer een record om de details van de synchronisatiefout weer te geven.</span><span class="sxs-lookup"><span data-stu-id="50cf1-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="50cf1-117">Het sneltabblad **Synchronisatiestatus** bevat de volgende foutdetails:</span><span class="sxs-lookup"><span data-stu-id="50cf1-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="50cf1-118">Orderstatus in behandeling</span><span class="sxs-lookup"><span data-stu-id="50cf1-118">Pending order status</span></span>
    - <span data-ttu-id="50cf1-119">Details orderfout</span><span class="sxs-lookup"><span data-stu-id="50cf1-119">Order error details</span></span>
    - <span data-ttu-id="50cf1-120">Wijzigingsdatum en -tijd</span><span class="sxs-lookup"><span data-stu-id="50cf1-120">Modified date and time</span></span>
    - <span data-ttu-id="50cf1-121">Aantal nieuwe pogingen</span><span class="sxs-lookup"><span data-stu-id="50cf1-121">Retry count</span></span>

1. <span data-ttu-id="50cf1-122">Als de foutdetails aangeven dat de record moet worden hersteld, selecteert u **Office Add-in** en vervolgens **Geselecteerde transactie bewerken**.</span><span class="sxs-lookup"><span data-stu-id="50cf1-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="50cf1-123">Er wordt een Excel-bestand geopend met de details van de geselecteerde transactie.</span><span class="sxs-lookup"><span data-stu-id="50cf1-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="50cf1-124">Als de transactie die wordt bewerkt een online ordertransactie is, bevat het Excel-bestand de volgende werkbladen:</span><span class="sxs-lookup"><span data-stu-id="50cf1-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="50cf1-125">**Transactie:** dit werkblad bevat de details over de koptekst voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="50cf1-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="50cf1-126">**Verkooptransactie:** dit werkblad bevat de regeldetails voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="50cf1-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="50cf1-127">**Betalingstransacties**: dit werkblad bevat de details van de betalingsregels voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="50cf1-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="50cf1-128">**Kortingstransacties**: dit werkblad bevat de details over de kortingen voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="50cf1-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="50cf1-129">**Belastingsstransacties**: dit werkblad bevat de details over de belasting voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="50cf1-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="50cf1-130">**Toeslagtransacties**: dit werkblad bevat de gegevens over de toeslagen voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="50cf1-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="50cf1-131">Als de transactie die wordt bewerkt een asynchrone klantordertransactie is, bevat het Excel-bestand de volgende werkbladen:</span><span class="sxs-lookup"><span data-stu-id="50cf1-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="50cf1-132">**Regels:** dit werkblad bevat de koptekst- en regeldetails voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="50cf1-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="50cf1-133">**Betalingen**: dit werkblad bevat de details van de betalingsregels voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="50cf1-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="50cf1-134">**Kortingen**: dit werkblad bevat de details over de kortingen voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="50cf1-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="50cf1-135">**Belastingen**: dit werkblad bevat de details over de belastingen voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="50cf1-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="50cf1-136">**Toeslagen**: dit werkblad bevat de gegevens over de toeslagen voor de transactie.</span><span class="sxs-lookup"><span data-stu-id="50cf1-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="50cf1-137">Voer in het Excel-bestand in het veld **Orderstatus in behandeling** **Bewerken** in en publiceer de wijziging.</span><span class="sxs-lookup"><span data-stu-id="50cf1-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="50cf1-138">Op deze manier voorkomt u dat deze record tijdens de verwerking wordt overgeslagen door de taak **Order synchroniseren** die wordt uitgevoerd in batchmodus.</span><span class="sxs-lookup"><span data-stu-id="50cf1-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="50cf1-139">In het Excel-bestand wijzigt u de betreffende velden en uploadt u de gegevens weer naar Commerce Headquarters met de publicatiefunctionaliteit van de Dynamics Excel-invoegtoepassing.</span><span class="sxs-lookup"><span data-stu-id="50cf1-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="50cf1-140">Na de publicatie van de gegevens worden de wijzigingen weergegeven in het systeem.</span><span class="sxs-lookup"><span data-stu-id="50cf1-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="50cf1-141">Tijdens het publiceren worden er geen validaties uitgevoerd voor wijzigingen door gebruikers.</span><span class="sxs-lookup"><span data-stu-id="50cf1-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="50cf1-142">U kunt een volledig audittrail van de wijzigingen bekijken door **Audittrail weergeven** te selecteren in de koptekst **Detailhandelstransactie** voor wijzigingen op koptekstniveau en in de relevante sectie en record op de desbetreffende transactiepagina.</span><span class="sxs-lookup"><span data-stu-id="50cf1-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="50cf1-143">Alle wijzigingen die betrekking hebben op verkoopregels worden bijvoorbeeld weergegeven op de pagina **Verkooptransacties** en alle wijzigingen die verband houden met betalingen worden weergegeven op de pagina **Betalingstransacties**.</span><span class="sxs-lookup"><span data-stu-id="50cf1-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="50cf1-144">Voor de wijzigingen worden de volgende controlegegevens bijgehouden:</span><span class="sxs-lookup"><span data-stu-id="50cf1-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="50cf1-145">Wijzigingsdatum en -tijd</span><span class="sxs-lookup"><span data-stu-id="50cf1-145">Modified date and time</span></span>
    - <span data-ttu-id="50cf1-146">Veld</span><span class="sxs-lookup"><span data-stu-id="50cf1-146">Field</span></span>
    - <span data-ttu-id="50cf1-147">Oude waarde</span><span class="sxs-lookup"><span data-stu-id="50cf1-147">Old value</span></span>
    - <span data-ttu-id="50cf1-148">Nieuwe waarde</span><span class="sxs-lookup"><span data-stu-id="50cf1-148">New value</span></span>
    - <span data-ttu-id="50cf1-149">Gewijzigd door</span><span class="sxs-lookup"><span data-stu-id="50cf1-149">Modified by</span></span>

1. <span data-ttu-id="50cf1-150">Nadat u de wijzigingen hebt aangebracht en gepubliceerd, selecteert u **Order synchroniseren** om het synchronisatieproces onmiddellijk te starten.</span><span class="sxs-lookup"><span data-stu-id="50cf1-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="50cf1-151">U kunt ook wachten tot het synchronisatieproces dat in batchmodus wordt uitgevoerd, de transactie heeft verwerkt.</span><span class="sxs-lookup"><span data-stu-id="50cf1-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="50cf1-152">Nadat de orders met succes zijn gesynchroniseerd, worden ze standaard in een wachtstatus geplaatst op basis van de wachtcode die is gedefinieerd in de Commerce-parameters.</span><span class="sxs-lookup"><span data-stu-id="50cf1-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="50cf1-153">De blokkering van de orders moet worden verwijderd voordat de orders verder kunnen worden verwerkt voor afhandeling of andere bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="50cf1-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="50cf1-154">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="50cf1-154">Additional resources</span></span>

[<span data-ttu-id="50cf1-155">Beheer van contante transacties bewerken en controleren</span><span class="sxs-lookup"><span data-stu-id="50cf1-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="50cf1-156">Financiële dimensies voor detailhandelstransacties bewerken</span><span class="sxs-lookup"><span data-stu-id="50cf1-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="50cf1-157">Een Excel-werkmap maken om detailhandelstransacties te bewerken</span><span class="sxs-lookup"><span data-stu-id="50cf1-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="50cf1-158">Velden toevoegen aan een Excel-werkmap om detailhandelstransacties te bewerken</span><span class="sxs-lookup"><span data-stu-id="50cf1-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
