---
title: Een vrije-tekstfactuur corrigeren
description: In dit artikel wordt beschreven hoe u een geboekte vrije-tekstfactuur corrigeert en opnieuw uitgeeft als gecorrigeerde factuur.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8c1b90b7b2c02a53e53cc13d70445a237b126d4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "364598"
---
# <a name="correct-a-free-text-invoice"></a><span data-ttu-id="c1588-103">Een vrije-tekstfactuur corrigeren</span><span class="sxs-lookup"><span data-stu-id="c1588-103">Correct a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1588-104">In dit artikel wordt beschreven hoe u een geboekte vrije-tekstfactuur corrigeert en opnieuw uitgeeft als gecorrigeerde factuur.</span><span class="sxs-lookup"><span data-stu-id="c1588-104">This article explains how to correct a free text invoice that has been posted and reissue it as a corrected invoice.</span></span>

<span data-ttu-id="c1588-105">Als u een vrije-tekstfactuur wilt corrigeren die al is geboekt, opent u de geboekte vrije-tekstfactuur.</span><span class="sxs-lookup"><span data-stu-id="c1588-105">To correct a free text invoice that has already been posted, open the posted free text invoice.</span></span> <span data-ttu-id="c1588-106">Selecteer op de pagina **Factuur** **Annuleren** en selecteer vervolgens **Factuur corrigeren**.</span><span class="sxs-lookup"><span data-stu-id="c1588-106">On the **Invoice** page, select **Cancel**, and then select **Correct invoice**.</span></span> <span data-ttu-id="c1588-107">Selecteer een redencode, voeg opmerkingen toe en selecteer de datum voor de nieuwe, gecorrigeerde factuur.</span><span class="sxs-lookup"><span data-stu-id="c1588-107">Select a reason code, add comments, and select the date for new corrected invoice.</span></span> <span data-ttu-id="c1588-108">U kunt de gecorrigeerde factuur wijzigen en boeken.</span><span class="sxs-lookup"><span data-stu-id="c1588-108">You can modify the corrected invoice, and post it.</span></span> 

<span data-ttu-id="c1588-109">Wanneer u de gecorrigeerde factuur boekt, wordt er een annuleringsfactuur gemaakt voor een creditbedrag dat gelijk is aan het oorspronkelijke factuurbedrag.</span><span class="sxs-lookup"><span data-stu-id="c1588-109">When you post the corrected invoice, a canceling invoice is created for a credit amount that equals the original invoice amount.</span></span> <span data-ttu-id="c1588-110">Hierdoor is het gecombineerde saldo van de oorspronkelijke en de annuleringsfactuur gelijk aan 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="c1588-110">Therefore, the combined balance of the original invoice and the canceling invoice is 0 (zero).</span></span> <span data-ttu-id="c1588-111">De annuleringsfactuur wordt vereffend met de oorspronkelijke factuur.</span><span class="sxs-lookup"><span data-stu-id="c1588-111">The canceling invoice is settled against the original invoice.</span></span> 

<span data-ttu-id="c1588-112">Als u de gecorrigeerde factuur boekt, hebt u drie facturen:</span><span class="sxs-lookup"><span data-stu-id="c1588-112">After you post the corrected invoice, you will have three invoices:</span></span>

-   <span data-ttu-id="c1588-113">**Oorspronkelijke factuur** – De factuur die de informatie bevat die u corrigeert.</span><span class="sxs-lookup"><span data-stu-id="c1588-113">**Original invoice** – The invoice that includes the information that you're correcting.</span></span>
-   <span data-ttu-id="c1588-114">**Annuleringsfactuur** – De creditnota die door het systeem is gegenereerd om de factuur te annuleren die zonet is gecorrigeerd.</span><span class="sxs-lookup"><span data-stu-id="c1588-114">**Canceling invoice** – The system-generated credit invoice that was created to cancel the invoice that was most recently corrected.</span></span>
-   <span data-ttu-id="c1588-115">**Gecorrigeerde factuur** – De factuur die de gecorrigeerde factuurgegevens bevat.</span><span class="sxs-lookup"><span data-stu-id="c1588-115">**Corrected invoice** – The invoice that contains the corrected invoice information.</span></span>

<span data-ttu-id="c1588-116">U kunt annulerings- en correctiefacturen op twee manieren identificeren:</span><span class="sxs-lookup"><span data-stu-id="c1588-116">You can identify canceling and correcting invoices in two ways:</span></span>

-   <span data-ttu-id="c1588-117">De pagina **Alle vrije-tekstfacturen** bevat een kolom **Correctie** waarin u kunt zien welke facturen annuleringsfacturen en gecorrigeerde facturen zijn.</span><span class="sxs-lookup"><span data-stu-id="c1588-117">The **All free text invoices** page includes a **Correction** column, where you can see which invoices are canceling invoices and corrected invoices.</span></span>
-   <span data-ttu-id="c1588-118">In de koptekst van de vrije-tekstfactuur wordt de status **Annuleringsfactuur** \[factuurnummer]\] of **Gecorrigeerde factuur '\[factuurnummer\]'** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c1588-118">The header of the free text invoice shows a status of **Cancelling invoice '\[invoice number\]'** or **Corrected invoice '\[invoice number\]'**.</span></span>

> [!NOTE]
> <span data-ttu-id="c1588-119">Deze functie is alleen beschikbaar als de configuratiesleutel **Correctie van vrije-tekstfactuur** is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="c1588-119">This feature is available only if the **Free text invoice correction** configuration key is selected.</span></span>



