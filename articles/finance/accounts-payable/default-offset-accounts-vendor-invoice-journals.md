---
title: Standaardtegenrekeningen voor leveranciersfactuur- en factuurgoedkeuringsjournalen
description: Gebruik dit onderwerp om te bepalen waar u het beste standaardrekeningen voor factuurjournalen kunt toewijzen.
author: abruer
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3b2ad808d5008d9a4b2d3ee975d15fa1ee13ed7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003476"
---
# <a name="default-offset-accounts-for-vendor-invoice-and-invoice-approval-journals"></a><span data-ttu-id="43e59-103">Standaardtegenrekeningen voor leveranciersfactuur- en factuurgoedkeuringsjournalen</span><span class="sxs-lookup"><span data-stu-id="43e59-103">Default offset accounts for vendor invoice and invoice approval journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43e59-104">Standaardtegenrekeningen worden gebruikt op de volgende pagina's voor leveranciersfactuurjournalen:</span><span class="sxs-lookup"><span data-stu-id="43e59-104">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="43e59-105">Factuurjournaal</span><span class="sxs-lookup"><span data-stu-id="43e59-105">Invoice journal</span></span>
-   <span data-ttu-id="43e59-106">Factuurgoedkeuringsjournaal</span><span class="sxs-lookup"><span data-stu-id="43e59-106">Invoice approval journal</span></span>

<span data-ttu-id="43e59-107">Gebruik de volgende tabel om u te helpen kiezen waar u het beste standaardrekeningen voor factuurjournalen kunt toewijzen.</span><span class="sxs-lookup"><span data-stu-id="43e59-107">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="43e59-108">Geef hier standaardrekeningen op</span><span class="sxs-lookup"><span data-stu-id="43e59-108">Set up default accounts here</span></span></th>
<th><span data-ttu-id="43e59-109">Waar standaardrekeningen worden opgegeven</span><span class="sxs-lookup"><span data-stu-id="43e59-109">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="43e59-110">Hoe deze optie de verwerking beïnvloedt</span><span class="sxs-lookup"><span data-stu-id="43e59-110">How this option affects processing</span></span></th>
<th><span data-ttu-id="43e59-111">Wanneer u deze optie moet gebruiken</span><span class="sxs-lookup"><span data-stu-id="43e59-111">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43e59-112"><strong>Leveranciersgroep</strong> – Stel standaardtegenrekeningen in voor leveranciersgroepen op de pagina <strong>Instellen van standaardaccount</strong>, die u vanaf de pagina <strong>Leveranciersgroepen</strong> kunt openen.</span><span class="sxs-lookup"><span data-stu-id="43e59-112"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="43e59-113">Leveranciersrekening</span><span class="sxs-lookup"><span data-stu-id="43e59-113">Vendor account</span></span></li>
<li><span data-ttu-id="43e59-114">Journaalboekingen voor leveranciersrekeningen in de leveranciersgroep, als standaardrekeningen niet zijn opgegeven voor leveranciersrekeningen</span><span class="sxs-lookup"><span data-stu-id="43e59-114">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="43e59-115">De standaardtegenrekeningen voor leveranciersgroepen worden weergegeven als standaardtegenrekeningen voor leveranciers op de pagina <strong>Instellen van standaardaccount</strong>.</span><span class="sxs-lookup"><span data-stu-id="43e59-115">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="43e59-116">U kunt deze pagina openen vanaf de lijstpagina <strong>Alle leveranciers</strong>.</span><span class="sxs-lookup"><span data-stu-id="43e59-116">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="43e59-117">Gebruik deze optie als u normaal gesproken betaalt voor dezelfde typen artikelen van dezelfde leveranciersgroepen.</span><span class="sxs-lookup"><span data-stu-id="43e59-117">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43e59-118"><strong>Leverancierrekening</strong> – Stel standaardtegenrekeningen in voor leverancierrekeningen op de pagina <strong>Instellen van standaardaccount</strong>, die u vanaf de pagina <strong>Leveranciers</strong> kunt openen.</span><span class="sxs-lookup"><span data-stu-id="43e59-118"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="43e59-119">Journaalboekingen voor de leveranciersrekening</span><span class="sxs-lookup"><span data-stu-id="43e59-119">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="43e59-120">De standaardtegenrekeningen voor leveranciersrekeningen worden als standaardtegenrekeningen voor journaalboekingen weergegeven voor de leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="43e59-120">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="43e59-121">Gebruik deze optie als u normaal gesproken betaalt voor dezelfde typen artikelen van dezelfde leveranciers.</span><span class="sxs-lookup"><span data-stu-id="43e59-121">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43e59-122"><strong>Journaalnamen</strong> – Stel standaardtegenrekeningen in voor journalen op de pagina <strong>Journaalnamen</strong>.</span><span class="sxs-lookup"><span data-stu-id="43e59-122"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="43e59-123">Selecteer de optie <strong>Vaste tegenrekening</strong>.</span><span class="sxs-lookup"><span data-stu-id="43e59-123">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="43e59-124">Merk op dat u geen standaardtegenrekeningen op journaalnamen kunt opgeven als het journaaltype van de journaalnamen of <strong>Facturenregister</strong> of <strong>Goedkeuring</strong> is.</span><span class="sxs-lookup"><span data-stu-id="43e59-124">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="43e59-125">Journaalkop die de journaalnaam gebruikt</span><span class="sxs-lookup"><span data-stu-id="43e59-125">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="43e59-126">Journaalboekingen in journalen die de journaalnaam gebruiken</span><span class="sxs-lookup"><span data-stu-id="43e59-126">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="43e59-127">Als de optie <strong>Vaste tegenrekening</strong> op de pagina <strong>Journaalnamen</strong> is geselecteerd, krijgt de tegenrekening van de journaalnaam voorrang op de standaardtegenrekening voor de leverancier of leveranciersgroep.</span><span class="sxs-lookup"><span data-stu-id="43e59-127">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="43e59-128">Gebruik deze optie om journalen in te stellen voor specifieke kosten en uitgaven die aan specifieke rekeningen worden aangerekend, ongeacht wie de leverancier of leveranciersgroep is waarvan de leverancier deel uitmaakt.</span><span class="sxs-lookup"><span data-stu-id="43e59-128">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="43e59-129"><strong>Journaalnamen</strong> – Stel standaardtegenrekeningen in voor journalen op de pagina <strong>Journaalnamen</strong>.</span><span class="sxs-lookup"><span data-stu-id="43e59-129"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="43e59-130">Schakel de optie <strong>Vaste tegenrekening</strong> uit.</span><span class="sxs-lookup"><span data-stu-id="43e59-130">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="43e59-131">Merk op dat u geen standaardtegenrekeningen op journaalnamen kunt opgeven als het journaaltype van de journaalnamen of <strong>Facturenregister</strong> of <strong>Goedkeuring</strong> is.</span><span class="sxs-lookup"><span data-stu-id="43e59-131">Note that you can&#39;t specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="43e59-132">Journaalkoptekst</span><span class="sxs-lookup"><span data-stu-id="43e59-132">Journal header</span></span></li>
<li><span data-ttu-id="43e59-133">Journaalboekingen in journalen die de journaalnaam gebruiken</span><span class="sxs-lookup"><span data-stu-id="43e59-133">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="43e59-134">Deze standaardboekingen worden gebruikt op pagina's voor journaalkopteksten, en de tegenrekening op de pagina voor de journaalkoptekst wordt als standaardboeking gebruikt op de pagina's voor journaalboekstukken.</span><span class="sxs-lookup"><span data-stu-id="43e59-134">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="43e59-135">Standaardrekeningen op de pagina <strong>Journaalnamen </strong>worden alleen gebruikt als er geen standaardrekeningen zijn ingesteld voor de leveranciersrekening.</span><span class="sxs-lookup"><span data-stu-id="43e59-135">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="43e59-136">Gebruik deze optie om standaardrekeningen in te stellen die worden gebruikt wanneer geen standaard tegenrekening voor de leverancier is toegewezen.</span><span class="sxs-lookup"><span data-stu-id="43e59-136">Use this option to set up default accounts that are used when a default vendor offset account isn&#39;t assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="43e59-137"><strong>Journaalkoptekst</strong> – Stel een standaardtegenrekening in die een journaal kan gebruiken als standaardboeking op de pagina's voor journaalboekstukken.</span><span class="sxs-lookup"><span data-stu-id="43e59-137"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="43e59-138">Merk op dat u geen standaardtegenrekeningen op de journaalkoptekst kunt opgeven als het journaaltype van de journaalnamen of <strong>Facturenregister</strong> of <strong>Goedkeuring</strong> is.</span><span class="sxs-lookup"><span data-stu-id="43e59-138">Note that you can&#39;t specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="43e59-139">Journaalboekingen in het journaal</span><span class="sxs-lookup"><span data-stu-id="43e59-139">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="43e59-140">De standaard tegenrekening voor een journaal wordt gebruikt als de standaardboeking op de pagina's voor journaalboekstukken.</span><span class="sxs-lookup"><span data-stu-id="43e59-140">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="43e59-141">Gebruik deze optie om het invoeren van gegevens te versnellen als de meeste boekingen in een journaal dezelfde tegenrekening hebben.</span><span class="sxs-lookup"><span data-stu-id="43e59-141">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>





