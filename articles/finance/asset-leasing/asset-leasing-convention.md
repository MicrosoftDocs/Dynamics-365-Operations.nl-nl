---
title: Conventies voor het leasen van activa
description: In dit onderwerp worden conventies voor geleasde activa beschreven.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLease
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2021-1-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 67c4d2b7162cf6bda2eedfecef43ff0b216e6e6c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881803"
---
# <a name="asset-leasing-conventions"></a><span data-ttu-id="66c7c-103">Conventies voor het leasen van activa</span><span class="sxs-lookup"><span data-stu-id="66c7c-103">Asset leasing conventions</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="66c7c-104">In dit onderwerp worden conventies voor geleasde activa beschreven.</span><span class="sxs-lookup"><span data-stu-id="66c7c-104">This topic describes conventions for leased assets.</span></span> <span data-ttu-id="66c7c-105">Leasingconventies worden gebruikt om de aanvangsdatum van een leaseboek te bepalen.</span><span class="sxs-lookup"><span data-stu-id="66c7c-105">Leasing conventions are used to determine the commencement date of a lease book.</span></span> <span data-ttu-id="66c7c-106">Als de leasingconventie is ingesteld op **Geen**, is de aanvangsdatum gelijk aan de begindatum voor de lease (dat wil zeggen de waarde van het veld **Begindatum lease**).</span><span class="sxs-lookup"><span data-stu-id="66c7c-106">If the leasing convention is set to **None**, the commencement date is the same as the start date for the lease (that is, the value of the **Lease start date** field).</span></span> <span data-ttu-id="66c7c-107">Als de leasingconventie is ingesteld op **Volledige maand**, is de aanvangsdatum de eerste dag van de maand waarin de begindatum van de lease valt.</span><span class="sxs-lookup"><span data-stu-id="66c7c-107">If the leasing convention is set to **Full month**, the commencement date is the first day of the month that the lease's start date falls in.</span></span>

<span data-ttu-id="66c7c-108">De aanvangsdatum bepaalt de begindatum van de periode voor de afschrijvingsschema's voor de verplichting en de afschrijving van de activa.</span><span class="sxs-lookup"><span data-stu-id="66c7c-108">The commencement date determines the start date of the period for the liability amortization and asset depreciation schedules.</span></span> <span data-ttu-id="66c7c-109">Rente- en afschrijvingskosten worden geboekt op de einddatum van de periode van de overeenkomstige schema's.</span><span class="sxs-lookup"><span data-stu-id="66c7c-109">Interest expenses and depreciation expenses are posted on the period end date of the corresponding schedules.</span></span> <span data-ttu-id="66c7c-110">De eerste inboeking en correctie worden geboekt op de aanvangsdatum.</span><span class="sxs-lookup"><span data-stu-id="66c7c-110">The initial recognition and adjustment journal entry are posted on the commencement date.</span></span>

> [!NOTE]
> <span data-ttu-id="66c7c-111">De functie voor leasingconventies moet worden ingeschakeld via Functiebeheer.</span><span class="sxs-lookup"><span data-stu-id="66c7c-111">The feature for leasing conventions must be turned on through Feature Management.</span></span> <span data-ttu-id="66c7c-112">Zoek in de werkruimte voor **functiebeheer** de functie **Leasingconventie voor activaleasing** en selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="66c7c-112">In the **Feature management** workspace, find and select the feature that is named **Leasing convention for asset leasing** feature, and then select **Enable now**.</span></span>

<span data-ttu-id="66c7c-113">Leasingconventies worden toegewezen aan de instellingen voor een lease-activaboek.</span><span class="sxs-lookup"><span data-stu-id="66c7c-113">Leasing conventions are assigned to the setup for a lease asset book.</span></span>

<span data-ttu-id="66c7c-114">Volg deze stappen om de leasingconventie weer te geven of toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="66c7c-114">To view or assign the leasing convention, follow these steps.</span></span>

1. <span data-ttu-id="66c7c-115">Ga naar **Activa leasen \> Instellen \> Leaseboeken**.</span><span class="sxs-lookup"><span data-stu-id="66c7c-115">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="66c7c-116">Selecteer in het veld **Leasingconventie** een van de volgende waarden.</span><span class="sxs-lookup"><span data-stu-id="66c7c-116">In the **Leasing convention** field, select one of the following values.</span></span>

    | <span data-ttu-id="66c7c-117">Leaseconventie</span><span class="sxs-lookup"><span data-stu-id="66c7c-117">Leasing convention</span></span> | <span data-ttu-id="66c7c-118">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="66c7c-118">Description</span></span> |
    |--------------------|-------------|
    | <span data-ttu-id="66c7c-119">None</span><span class="sxs-lookup"><span data-stu-id="66c7c-119">None</span></span>               | <span data-ttu-id="66c7c-120">De afschrijvingsschema's voor de verplichting en de afschrijving van de activa begint op de begindatum van de lease, omdat de aanvangsdatum gelijk is aan de begindatum van de lease.</span><span class="sxs-lookup"><span data-stu-id="66c7c-120">The liability amortization and asset depreciation schedules start on the lease's start date, because the commencement date equals the lease's start date.</span></span> <span data-ttu-id="66c7c-121">De einddatum is één maand later.</span><span class="sxs-lookup"><span data-stu-id="66c7c-121">The end date is one month later.</span></span> <span data-ttu-id="66c7c-122">Deze leasingconventie garandeert niet dat de rente op de laatste dag van elke maand wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="66c7c-122">This leasing convention doesn't guarantee that the interest will be posted on the last day of each month.</span></span> |
    | <span data-ttu-id="66c7c-123">Hele maand</span><span class="sxs-lookup"><span data-stu-id="66c7c-123">Full month</span></span>         | <span data-ttu-id="66c7c-124">Voor lease-overeenkomsten met een begindatum op een willekeurig tijdstip in de maand, beginnen de afschrijvingsschema's voor de verplichting en de afschrijving van de activa met de opbouw van de kosten op de eerste dag van die maand.</span><span class="sxs-lookup"><span data-stu-id="66c7c-124">For leases that have a start date that occurs at any time during the month, the liability amortization and asset depreciation schedules start to accrue expenses on the first day of that month.</span></span> <span data-ttu-id="66c7c-125">Deze leasingconventie zorgt ervoor dat de rente wordt opgebouwd op de laatste dag van elke maand voor de hele maand.</span><span class="sxs-lookup"><span data-stu-id="66c7c-125">This leasing convention ensures that interest is accrued on the last day of each month for the whole month.</span></span> |

3. <span data-ttu-id="66c7c-126">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="66c7c-126">Select **Save**.</span></span>

<span data-ttu-id="66c7c-127">Wanneer een lease wordt gemaakt, wordt de aanvangsdatum van elk boek automatisch ingevoerd op basis van de begindatum die is ingevoerd voor de lease en de leasingconventie die is opgegeven voor het boek.</span><span class="sxs-lookup"><span data-stu-id="66c7c-127">When a lease is created, the commencement date of each book is automatically entered based on the start date that is entered for the lease and the leasing convention that is specified for the book.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
