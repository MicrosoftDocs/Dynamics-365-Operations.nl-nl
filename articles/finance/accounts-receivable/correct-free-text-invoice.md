---
title: Een vrije-tekstfactuur corrigeren
description: In dit artikel wordt beschreven hoe u een geboekte vrije-tekstfactuur corrigeert en opnieuw uitgeeft als gecorrigeerde factuur.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f04e70c9afb66be015ce18cebebd711f00d764b7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827573"
---
# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="437e4-103">Een vrije-tekstfactuur corrigeren</span><span class="sxs-lookup"><span data-stu-id="437e4-103">Correct a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="437e4-104">In dit artikel wordt beschreven hoe u een geboekte vrije-tekstfactuur corrigeert en opnieuw uitgeeft als gecorrigeerde factuur.</span><span class="sxs-lookup"><span data-stu-id="437e4-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="437e4-105">Als u een vrije-tekstfactuur wilt corrigeren die al is geboekt, opent u de geboekte vrije-tekstfactuur.</span><span class="sxs-lookup"><span data-stu-id="437e4-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="437e4-106">Selecteer op de pagina **Factuur** **Annuleren** en selecteer vervolgens **Factuur corrigeren**.</span><span class="sxs-lookup"><span data-stu-id="437e4-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="437e4-107">Selecteer een redencode, voeg opmerkingen toe en selecteer de datum voor de nieuwe, gecorrigeerde factuur.</span><span class="sxs-lookup"><span data-stu-id="437e4-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="437e4-108">U kunt de gecorrigeerde factuur wijzigen en boeken.</span><span class="sxs-lookup"><span data-stu-id="437e4-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="437e4-109">Wanneer u de gecorrigeerde factuur boekt, wordt er een annuleringsfactuur gemaakt voor een creditbedrag dat gelijk is aan het oorspronkelijke factuurbedrag.</span><span class="sxs-lookup"><span data-stu-id="437e4-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="437e4-110">Hierdoor is het gecombineerde saldo van de oorspronkelijke en de annuleringsfactuur gelijk aan 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="437e4-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="437e4-111">De annuleringsfactuur wordt vereffend met de oorspronkelijke factuur.</span><span class="sxs-lookup"><span data-stu-id="437e4-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="437e4-112">Als u de gecorrigeerde factuur boekt, hebt u drie facturen:</span><span class="sxs-lookup"><span data-stu-id="437e4-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="437e4-113">**Oorspronkelijke factuur** – De factuur die de informatie bevat die u corrigeert.</span><span class="sxs-lookup"><span data-stu-id="437e4-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="437e4-114">**Annuleringsfactuur** – De creditnota die door het systeem is gegenereerd om de factuur te annuleren die zonet is gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="437e4-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="437e4-115">**Gecorrigeerde factuur** – De factuur die de gecorrigeerde factuurgegevens bevat.</span><span class="sxs-lookup"><span data-stu-id="437e4-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="437e4-116">U kunt annulerings- en correctiefacturen op twee manieren identificeren:</span><span class="sxs-lookup"><span data-stu-id="437e4-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="437e4-117">De pagina **Alle vrije-tekstfacturen** bevat een kolom **Correctie** waarin u kunt zien welke facturen annuleringsfacturen en gecorrigeerde facturen zijn.</span><span class="sxs-lookup"><span data-stu-id="437e4-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="437e4-118">In de koptekst van de vrije-tekstfactuur wordt de status **Annuleringsfactuur** \[factuurnummer\] of **Gecorrigeerde factuur '\[factuurnummer\]'** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="437e4-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="437e4-119">Deze functie is alleen beschikbaar als de configuratiesleutel **Correctie van vrije-tekstfactuur** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="437e4-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span> <span data-ttu-id="437e4-120">Voor meer informatie over het inschakelen van configuratiesleutels zie de sectie Configuratiesleutels inschakelen (of uitschakelen) in het onderwerp [onderhoudsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="437e4-120">For more information on how to enable Configuration keys refer to the Enable (or disable) configuration keys section in the [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md) topic.</span></span> 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]