---
title: EU-invoercertificaten
description: Dit artikel biedt informatie over EU-invoercertificaten (Europese Unie).
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b3346a5229d0cc9e7af74f17ea6a327e5ba253a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "371385"
---
# <a name="eu-entry-certificates"></a><span data-ttu-id="c90bf-103">EU-invoercertificaten</span><span class="sxs-lookup"><span data-stu-id="c90bf-103">EU entry certificates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c90bf-104">Dit artikel biedt informatie over EU-invoercertificaten (Europese Unie).</span><span class="sxs-lookup"><span data-stu-id="c90bf-104">This article provides information about European Union (EU) entry certificates.</span></span>

<span data-ttu-id="c90bf-105">U kunt de volgende taken uitvoeren voor een EU (Europese Unie)-invoercertificaat:</span><span class="sxs-lookup"><span data-stu-id="c90bf-105">You can complete the following tasks for a European Union (EU) entry certificate:</span></span>

-   <span data-ttu-id="c90bf-106">Maak een EU-invoercertificaat en geef het uit samen met een pakbon of een klantfactuur voor de levering van artikelen of diensten aan EU-landen/-regio´s.</span><span class="sxs-lookup"><span data-stu-id="c90bf-106">Create and issue an EU entry certificate together with a packing slip or customer invoice for the delivery of items or services to EU countries/regions.</span></span>
-   <span data-ttu-id="c90bf-107">Ontvang het EU-invoercertificaat dat door een EU-klant is ondertekend.</span><span class="sxs-lookup"><span data-stu-id="c90bf-107">Receive the EU entry certificate that is signed by an EU customer.</span></span>
-   <span data-ttu-id="c90bf-108">Upload het ondertekende EU-invoercertificaat dat is ontvangen van de klant of een derde die verantwoordelijk is voor levering van de artikelen aan de klant.</span><span class="sxs-lookup"><span data-stu-id="c90bf-108">Upload the signed EU entry certificate that is received either from the customer or from a third party who is responsible for delivering items to the customer.</span></span>
-   <span data-ttu-id="c90bf-109">Koppel het geüploade EU-invoercertificaat met een klantfactuur.</span><span class="sxs-lookup"><span data-stu-id="c90bf-109">Associate the uploaded EU entry certificate with a customer invoice.</span></span>
-   <span data-ttu-id="c90bf-110">Werk de status van het geselecteerde EU-invoercertificaat bij.</span><span class="sxs-lookup"><span data-stu-id="c90bf-110">Update the status of the uploaded EU entry certificate.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c90bf-111">Vereisten</span><span class="sxs-lookup"><span data-stu-id="c90bf-111">Prerequisites</span></span>
<span data-ttu-id="c90bf-112">De volgende tabel geeft de vereisten weer waaraan moet worden voldaan voordat u start.</span><span class="sxs-lookup"><span data-stu-id="c90bf-112">The following table shows the prerequisites that must be in place before you start.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c90bf-113">Categorie</span><span class="sxs-lookup"><span data-stu-id="c90bf-113">Category</span></span></th>
<th><span data-ttu-id="c90bf-114">Vereiste</span><span class="sxs-lookup"><span data-stu-id="c90bf-114">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c90bf-115">Land/regio</span><span class="sxs-lookup"><span data-stu-id="c90bf-115">Country/region</span></span></td>
<td><span data-ttu-id="c90bf-116">Het primaire adres van de rechtspersoon moet in een EG-lidstaat zijn.</span><span class="sxs-lookup"><span data-stu-id="c90bf-116">The primary address of the legal entity must be in a EU member state.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c90bf-117">Verwante instellingstaken</span><span class="sxs-lookup"><span data-stu-id="c90bf-117">Related set up tasks</span></span></td>
<td><ul>
<li><span data-ttu-id="c90bf-118">Selecteer op de pagina <strong>Parameters van module Klanten</strong> de opties <strong>Certificaatbeheer inschakelen</strong> en <strong>Verstrekken van invoercertificaat inschakelen</strong>.</span><span class="sxs-lookup"><span data-stu-id="c90bf-118">On the <strong>Accounts receivable parameters</strong> page, select the <strong>Enable entry certificate management</strong> and <strong>Enable entry certificate issuing</strong> options.</span></span></li>
<li><span data-ttu-id="c90bf-119">Selecteer op de pagina <strong>Klanten</strong> op het sneltabblad <strong>Factuur en levering</strong> de optie <strong>Invoercertificaat vereist</strong> om aan te geven dat een EU-invoercertificaat voor de klant verplicht is.</span><span class="sxs-lookup"><span data-stu-id="c90bf-119">On the <strong>Customers</strong> page, on the <strong>Invoice and delivery</strong> FastTab, select the <strong>Entry certificate required</strong> option to indicate that an EU entry certificate is mandatory for the customer.</span></span> <span data-ttu-id="c90bf-120">Schakel het selectievakje <strong>Uitgifte van invoercertificaat</strong> in om een EU-invoercertificaat van de rechtspersoon voor de klant uit te geven.</span><span class="sxs-lookup"><span data-stu-id="c90bf-120">Select the <strong>Issue entry certificate</strong> option to issue an EU entry certificate of the legal entity to the customer.</span></span></li>
<li><span data-ttu-id="c90bf-121">Selecteer op de pagina <strong>Parameters van module Klanten</strong> een nummerreekscode voor de verwijzing <strong>Invoercertificaat</strong>.</span><span class="sxs-lookup"><span data-stu-id="c90bf-121">On the <strong>Accounts receivable parameters</strong> page, select a number sequence code for the <strong>Entry certificate</strong> reference.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c90bf-122">Gerelateerde transacties</span><span class="sxs-lookup"><span data-stu-id="c90bf-122">Related transactions</span></span></td>
<td><ul>
<li><span data-ttu-id="c90bf-123">Een klantaccount maken.</span><span class="sxs-lookup"><span data-stu-id="c90bf-123">Create a customer account.</span></span></li>
<li><span data-ttu-id="c90bf-124">Maak een verkooporder.</span><span class="sxs-lookup"><span data-stu-id="c90bf-124">Create a sales order.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a><span data-ttu-id="c90bf-125">Een EU-invoercertificaat maken, registreren en uploaden</span><span class="sxs-lookup"><span data-stu-id="c90bf-125">Creating, registering, and uploading an EU entry certificate</span></span>
<span data-ttu-id="c90bf-126">U kunt automatisch of handmatig een EU-invoercertificaat maken.</span><span class="sxs-lookup"><span data-stu-id="c90bf-126">You can create an EU entry certificate automatically or manually.</span></span> <span data-ttu-id="c90bf-127">Een EU-invoercertificaat wordt automatisch gemaakt en afgedrukt wanneer u een pakbon of factuur voor een klant boekt met de pagina **Pakbon boeken** of **Factuur boeken**.</span><span class="sxs-lookup"><span data-stu-id="c90bf-127">An EU entry certificate is created and printed automatically when you post a packing slip or invoice for a customer by using the **Packing slip posting** page or the **Posting invoice** page.</span></span> <span data-ttu-id="c90bf-128">Als u handmatig een EU-invoercertificaat wilt maken of opnieuw afdrukken voor een klantfactuur, kunt u de pagina **Factuurjournaal** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c90bf-128">To manually create or reprint an EU entry certificate for a customer invoice, use the **Invoice journal** page.</span></span> <span data-ttu-id="c90bf-129">U kunt bovendien op de pagina **Invoercertificaatlogboek** gegevens invoeren over een EU-invoercertificaat dat door een derde is uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="c90bf-129">Additionally, you can use the **Entry certificate journal** page to enter details about an EU entry certificate that is issued by a third party.</span></span>

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a><span data-ttu-id="c90bf-130">Automatisch of handmatig een EU-invoercertificaat maken</span><span class="sxs-lookup"><span data-stu-id="c90bf-130">Creating an EU entry certificate automatically or manually</span></span>

<span data-ttu-id="c90bf-131">U kunt automatisch een EU-invoercertificaat maken door een pakbon te gebruiken op de pagina **Alle verkooporders** of door een factuur te gebruiken op de pagina **Verkooporder**.</span><span class="sxs-lookup"><span data-stu-id="c90bf-131">You can create an EU entry certificate automatically by using a packing slip on the **All sales orders** page or by using an invoice on the **Sales order** page.</span></span> <span data-ttu-id="c90bf-132">Om handmatig een EU-invoercertificaat te maken, kunt u een factuur op de pagina **Factuurjournaal** gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c90bf-132">To manually create an EU entry certificate, you can use an invoice on the **Invoice journal** page.</span></span> <span data-ttu-id="c90bf-133">U moet echter de certificaatstatus van de factuur wijzigen voordat u handmatig maken een EU-invoercertificaat maakt.</span><span class="sxs-lookup"><span data-stu-id="c90bf-133">However, you must change the certification status of the invoice before you manually create an EU entry certificate.</span></span>

### <a name="registering-an-eu-entry-certificate"></a><span data-ttu-id="c90bf-134">Een EU-invoercertificaat registreren</span><span class="sxs-lookup"><span data-stu-id="c90bf-134">Registering an EU entry certificate</span></span>

<span data-ttu-id="c90bf-135">Als registratie vereist is kunt u de pagina **Invoercertificaatlogboek** gebruiken om een EU-invoercertificaat te registreren dat door een derde is uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="c90bf-135">If registration is required, you can use the **Entry certificate journal** page to register an EU entry certificate that is issued by a third party.</span></span>

### <a name="uploading-a-received-eu-entry-certificate"></a><span data-ttu-id="c90bf-136">Een ontvangen EU-invoercertificaat uploaden</span><span class="sxs-lookup"><span data-stu-id="c90bf-136">Uploading a received EU entry certificate</span></span>

<span data-ttu-id="c90bf-137">Gebruik de pagina **Bijlagen** om een ontvangen EU-invoercertificaat te uploaden dat is getekend door een EU-klant.</span><span class="sxs-lookup"><span data-stu-id="c90bf-137">Use the **Attachments** page to upload a received EU entry certificate that is signed by an EU customer.</span></span> <span data-ttu-id="c90bf-138">Nadat het certificaat is geüpload, kunt u het aan een factuur koppelen als bewijs dat de artikelen zijn geleverd.</span><span class="sxs-lookup"><span data-stu-id="c90bf-138">After the certificate is uploaded, you can associate it with an invoice as proof that the items were delivered.</span></span> <span data-ttu-id="c90bf-139">Dit bewijs is vereist als u een factuur moet uitgeven die geen belasting toegevoegde waarde (btw) bevat, en het wordt ook gebruikt tijdens de controle.</span><span class="sxs-lookup"><span data-stu-id="c90bf-139">This proof is required if you must issue an invoice that doesn't include value-added tax (VAT), and it's also used during auditing.</span></span>

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a><span data-ttu-id="c90bf-140">Optioneel: de certificaat- en afdrukstatus van een factuur bijwerken</span><span class="sxs-lookup"><span data-stu-id="c90bf-140">Optional: Updating the certification status and printing status of an invoice</span></span>

<span data-ttu-id="c90bf-141">U kunt de invoercertificaatstatus en de afdrukstatus van een klantfactuur bijwerken op de pagina **Factuurjournaal**.</span><span class="sxs-lookup"><span data-stu-id="c90bf-141">You can update the entry certification status and printing status of a customer invoice by using the **Invoice journal** page.</span></span>

## <a name="technical-information-for-system-administrators"></a><span data-ttu-id="c90bf-142">Technische informatie voor systeembeheerders</span><span class="sxs-lookup"><span data-stu-id="c90bf-142">Technical information for system administrators</span></span>
<span data-ttu-id="c90bf-143">Als u geen toegang hebt tot de pagina's waarmee u deze taak kunt voltooien, moet u contact opnemen met uw systeembeheerder en de informatie opgeven die wordt beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="c90bf-143">If you don't have access to the pages that are used to complete this task, contact your system administrator, and provide the information that is shown in the following table.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c90bf-144">Categorie</span><span class="sxs-lookup"><span data-stu-id="c90bf-144">Category</span></span></th>
<th><span data-ttu-id="c90bf-145">Vereiste</span><span class="sxs-lookup"><span data-stu-id="c90bf-145">Prerequisite</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c90bf-146">Veiligheidstaken en -rollen</span><span class="sxs-lookup"><span data-stu-id="c90bf-146">Security roles and duties</span></span></td>
<td><span data-ttu-id="c90bf-147">Om EU-invoercertificaten in te stellen en te maken voor artikelen of services, moet u lid zijn van een beveiligingsrol die de volgende functies bevat:</span><span class="sxs-lookup"><span data-stu-id="c90bf-147">To set up and create EU entry certificates for items or services, you must be a member of a security role that includes the following duties:</span></span>
<ul>
<li><span data-ttu-id="c90bf-148"><strong>Debiteurenadministrateur</strong> (CustInvoiceAccountsReceivableClerk)</span><span class="sxs-lookup"><span data-stu-id="c90bf-148"><strong>Accounts receivable clerk</strong> (CustInvoiceAccountsReceivableClerk)</span></span></li>
<li><span data-ttu-id="c90bf-149"><strong>Medewerker klantenservice</strong> (TradeCustomerServiceRepresentative)</span><span class="sxs-lookup"><span data-stu-id="c90bf-149"><strong>Customer service representative</strong> (TradeCustomerServiceRepresentative)</span></span></li>
<li><span data-ttu-id="c90bf-150"><strong>Verkoopmedewerker</strong> (TradeSalesClerk)</span><span class="sxs-lookup"><span data-stu-id="c90bf-150"><strong>Sales clerk</strong> (TradeSalesClerk)</span></span></li>
<li><span data-ttu-id="c90bf-151"><strong>Verzendadministrateur</strong> (InventShippingClerk)</span><span class="sxs-lookup"><span data-stu-id="c90bf-151"><strong>Shipping clerk</strong> (InventShippingClerk)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>





