---
title: Resultaten van de automatisering van leveranciersfacturering weergeven (preview)
description: In dit onderwerp wordt uitgelegd hoe u de status van leveranciersfacturen kunt weergeven die zich in het geautomatiseerde proces voor indiening bij de werkstroom bevinden.
author: abruer
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: baa2f1f55dfb9bb93b4f27c45db563e39850dd37
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969721"
---
# <a name="view-vendor-invoice-automation-results"></a><span data-ttu-id="318d4-103">Resultaten van de automatisering van leveranciersfacturering weergeven</span><span class="sxs-lookup"><span data-stu-id="318d4-103">View vendor invoice automation results</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="318d4-104">In dit onderwerp wordt uitgelegd hoe u de status van leveranciersfacturen kunt weergeven die zich in het geautomatiseerde proces voor indiening bij de werkstroom bevinden.</span><span class="sxs-lookup"><span data-stu-id="318d4-104">This topic explains how to view the status of vendor invoices that are in the automated submit-to-workflow process.</span></span> <span data-ttu-id="318d4-105">Details van de automatiseringsgeschiedenis worden bijgehouden voor elke geïmporteerde leveranciersfactuur.</span><span class="sxs-lookup"><span data-stu-id="318d4-105">Details of the automation history are maintained for each imported vendor invoice.</span></span> <span data-ttu-id="318d4-106">Afhankelijk van de bedrijfsprocessen die u hebt geautomatiseerd, worden op de pagina **Leveranciersfacturen in behandeling** de waarden **Afstemmingsstatus van automatische ontvangst** en **Automatisch indienen bij werkstroomstatus** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="318d4-106">Depending on the business processes that you've automated, the **Pending vendor invoices** page shows **Automated receipt match status** and **Automated submit to workflow status** values.</span></span> <span data-ttu-id="318d4-107">U kunt de details bekijken en een plan maken om zich te concentreren op de facturen waarvoor een geautomatiseerde stap is mislukt.</span><span class="sxs-lookup"><span data-stu-id="318d4-107">You can view the details and make a plan to focus on the invoices that failed an automated step.</span></span> <span data-ttu-id="318d4-108">Nadat u het probleem hebt opgelost, kunt u het geautomatiseerde proces voor de geïmporteerde factuur hervatten.</span><span class="sxs-lookup"><span data-stu-id="318d4-108">Then, after you correct the issue, you can resume the automated process for the imported invoice.</span></span>

<span data-ttu-id="318d4-109">Voordat u een factuur kunt bewerken die is ingediend, moet u de geautomatiseerde verwerking onderbreken.</span><span class="sxs-lookup"><span data-stu-id="318d4-109">Before you can edit an invoice that has been submitted, you must pause the automated processing.</span></span> <span data-ttu-id="318d4-110">Als een factuur in het geautomatiseerde proces voor indiening bij de werkstroom moet worden onderbroken, stelt u het veld **Opnemen in geautomatiseerde verwerking** in op **Nee** op de pagina **Leveranciersfacturen**.</span><span class="sxs-lookup"><span data-stu-id="318d4-110">If an invoice in the automated submit-to-workflow process must be paused, set the **Include in Automated processing** field to **No** on the **Vendor invoices** page.</span></span> <span data-ttu-id="318d4-111">Automation wordt vervolgens pas uitgevoerd als **Opnemen in geautomatiseerde verwerking** is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="318d4-111">Automation then won't run until **Include in Automated processing** is set to **Yes**.</span></span> <span data-ttu-id="318d4-112">Een factuur kan worden onderbroken voor verdere automatisering als deze nog niet in het werkstroomsysteem is opgenomen en niet wordt gebruikt door het geautomatiseerde proces.</span><span class="sxs-lookup"><span data-stu-id="318d4-112">An invoice can be paused from further automation if it isn't yet in the workflow system and isn't used by the automated process.</span></span>

<span data-ttu-id="318d4-113">Als een geïmporteerde factuur afhankelijk is van het proces voor indiening bij de werkstroom, kunt u de waarde **Automatiseringsstatus** weergeven op de pagina **Leveranciersfacturen**.</span><span class="sxs-lookup"><span data-stu-id="318d4-113">If an imported invoice is subject to the submit-to-workflow process, you can view its **Automation status** value on the **Vendor invoices** page.</span></span> <span data-ttu-id="318d4-114">De volgende statussen worden bijgehouden:</span><span class="sxs-lookup"><span data-stu-id="318d4-114">The following statuses are tracked:</span></span>

- <span data-ttu-id="318d4-115">**Opgenomen**: de geautomatiseerde processen die op de pagina **Parameters van module Leveranciers** zijn gedefinieerd, worden correct uitgevoerd, maar zijn nog niet voltooid.</span><span class="sxs-lookup"><span data-stu-id="318d4-115">**Included** – The automated processes that are defined on the **Accounts payable parameters** page are running correctly but haven't yet been completed.</span></span>
- <span data-ttu-id="318d4-116">**Onderbroken**: de geautomatiseerde processen die zijn gedefinieerd op de pagina **Parameters van module Leveranciers** zijn uitgevoerd, maar ten minste één stap in het proces is mislukt.</span><span class="sxs-lookup"><span data-stu-id="318d4-116">**Paused** – The automated processes that are defined on the **Accounts payable parameters** page have run, but at least one step in the process failed.</span></span> <span data-ttu-id="318d4-117">De status **Onderbroken** wordt ook toegepast als het veld **Opnemen in geautomatiseerde verwerking** is ingesteld op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="318d4-117">The **Paused** status is also applied if the **Include in automated processing** field is set to **No**.</span></span> <span data-ttu-id="318d4-118">U kunt de fouten weergeven door **Meest recente resultaten weergeven** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="318d4-118">You can view the failures by selecting **View most recent results**.</span></span>
- <span data-ttu-id="318d4-119">**In werkstroom**: de geïmporteerde factuur is bij het werkstroomsysteem ingediend via het geautomatiseerde proces voor indiening bij de werkstroom of handmatig.</span><span class="sxs-lookup"><span data-stu-id="318d4-119">**In workflow** – The imported invoice has been submitted to the workflow system, either by the automated submit-to-workflow process or manually.</span></span>
- <span data-ttu-id="318d4-120">**Werkstroom voltooid**: het werkstroomproces is voltooid voor de geïmporteerde factuur.</span><span class="sxs-lookup"><span data-stu-id="318d4-120">**Workflow complete** – The workflow process has been completed for the imported invoice.</span></span>
