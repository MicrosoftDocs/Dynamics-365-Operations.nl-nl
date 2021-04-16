---
title: Het kortetermijngedeelte van een leaseverplichting opnieuw classificeren
description: In dit onderwerp wordt uitgelegd hoe u een maandelijkse journaalboeking maakt om een gedeelte van de leaseverplichting opnieuw te classificeren als korte termijn.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7d98d66b5fe9d32a86eb75d937fedfdca6773ac4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823090"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="74f14-103">Het kortetermijngedeelte van een leaseverplichting opnieuw classificeren</span><span class="sxs-lookup"><span data-stu-id="74f14-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74f14-104">In dit onderwerp wordt uitgelegd hoe u een maandelijkse journaalboeking maakt om een gedeelte van de leaseverplichting opnieuw te classificeren als korte termijn.</span><span class="sxs-lookup"><span data-stu-id="74f14-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="74f14-105">Wanneer het schema dat is geselecteerd in het batchproces **Herclassificatie kortlopende leaseverplichtingen** is, wordt er een journaalboeking gemaakt.</span><span class="sxs-lookup"><span data-stu-id="74f14-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="74f14-106">Deze invoer wordt gebruikt om het huidige gedeelte van de leaseverplichtingen te boeken op de laatste dag van de maand.</span><span class="sxs-lookup"><span data-stu-id="74f14-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="74f14-107">Tegelijkertijd wordt een omkeerregel geboekt vanaf de eerste dag van de volgende maand.</span><span class="sxs-lookup"><span data-stu-id="74f14-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="74f14-108">Het kortetermijngedeelte van de leaseverplichting wordt vermeld in het aflossingsschema voor de passiva.</span><span class="sxs-lookup"><span data-stu-id="74f14-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="74f14-109">Wanneer de journaalboeking wordt geboekt, wordt de kolom **Journaal voor herclassificatie van verplichtingen gemaakt** beschikbaar en wordt de journaal-id ook in de planning ingevuld.</span><span class="sxs-lookup"><span data-stu-id="74f14-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="74f14-110">Voer de volgende stappen uit om de journaalboeking voor herclassificatie van kortlopende verplichtingen te maken en te boeken.</span><span class="sxs-lookup"><span data-stu-id="74f14-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="74f14-111">Ga naar **Activa leasen \> Periodiek \> Batchjournaal maken**.</span><span class="sxs-lookup"><span data-stu-id="74f14-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="74f14-112">Selecteer in het dialoogvenster **Batchjournaal maken** in het veld **Schema selecteren** en selecteer **Herclassificatie kortlopende leaseverplichtingen**.</span><span class="sxs-lookup"><span data-stu-id="74f14-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="74f14-113">Selecteer een leasegroep in het veld **Leasegroep**.</span><span class="sxs-lookup"><span data-stu-id="74f14-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="74f14-114">U kunt ook in het veld **Boek-id** de boek-id selecteren.</span><span class="sxs-lookup"><span data-stu-id="74f14-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="74f14-115">Schakel de parameter **Boeken** in.</span><span class="sxs-lookup"><span data-stu-id="74f14-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="74f14-116">Indien de invoer moet worden gemaakt, maar niet worden geboekt, dient u deze parameter uit te schakelen.</span><span class="sxs-lookup"><span data-stu-id="74f14-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="74f14-117">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="74f14-117">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
