---
title: Redencodes instellen
description: Dynamics 365 Human Resources gebruikt redencodes om uit te leggen waarom de vergoedingen van een werknemer veranderen.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c799a81f38a5dbd5996afbda9529fa83d7fe5cf9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468390"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="bd9fc-103">Redencodes instellen</span><span class="sxs-lookup"><span data-stu-id="bd9fc-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="bd9fc-104">Dynamics 365 Human Resources gebruikt redencodes om uit te leggen waarom de vergoedingen van een werknemer veranderen.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="bd9fc-105">Met ingang van januari 2021 migreren redencodes naar het werkgebied **Personeelsbeheer** in plaats van het werkgebied **Vergoedingenbeheer**.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="bd9fc-106">Meer informatie vindt u in [Redencodes handmatig migreren naar Personeelsbeheer](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span><span class="sxs-lookup"><span data-stu-id="bd9fc-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="bd9fc-107">Redencodes maken</span><span class="sxs-lookup"><span data-stu-id="bd9fc-107">Create reason codes</span></span>

1. <span data-ttu-id="bd9fc-108">Selecteer in het werkgebied **Personeelsbeheer** (of het werkgebied **Vergoedingenbeheer** als uw redencodes nog niet zijn gemigreerd), de optie **Koppelingen** en selecteer vervolgens **Redencodes**.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="bd9fc-109">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-109">Select **New**.</span></span>

3. <span data-ttu-id="bd9fc-110">Geef de waarden op voor de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="bd9fc-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="bd9fc-111">Veld</span><span class="sxs-lookup"><span data-stu-id="bd9fc-111">Field</span></span> | <span data-ttu-id="bd9fc-112">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="bd9fc-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bd9fc-113">**Redencode**</span><span class="sxs-lookup"><span data-stu-id="bd9fc-113">**Reason code**</span></span> | <span data-ttu-id="bd9fc-114">Een unieke naam om de reden te identificeren die aangeeft waarom een werknemer een inschrijving van een vergoedingsplan wijzigt.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="bd9fc-115">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="bd9fc-115">**Description**</span></span> | <span data-ttu-id="bd9fc-116">Een beschrijving van de redencode.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="bd9fc-117">Stel onder **Toepasselijke scenario's** de optie **Vergoedingenbeheer** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="bd9fc-118">(Niet van toepassing als uw redencodes nog niet zijn gemigreerd naar het werkgebied **Personeelsbeheer**.)</span><span class="sxs-lookup"><span data-stu-id="bd9fc-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="bd9fc-119">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="bd9fc-120">Redencodes handmatig migreren naar Personeelsbeheer</span><span class="sxs-lookup"><span data-stu-id="bd9fc-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="bd9fc-121">In januari 2021 migreren redencodes naar het werkgebied **Personeelsbeheer** in plaats van het werkgebied **Vergoedingenbeheer**.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="bd9fc-122">De meeste redencodegegevens worden automatisch gemigreerd in uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="bd9fc-123">Sommige redencodegegevens worden mogelijk niet gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="bd9fc-124">Redencodes hebben nu bijvoorbeeld een maximum van 15 tekens, waardoor redencodes langer dan 15 tekens niet automatisch worden gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="bd9fc-125">Er wordt een banner weergegeven op de pagina **Koppelingen** van het werkgebied **Vergoedingenbeheer** die u op de hoogte stelt van de migratie en of er mogelijk redencodes niet zijn gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="bd9fc-126">Selecteer **Redencodes** voor meer informatie over de migratiestatus.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="bd9fc-127">[![Redencodes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="bd9fc-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="bd9fc-128">Selecteer een redencode die niet kon worden gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="bd9fc-129">[![Migratiestatus van redencode](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="bd9fc-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="bd9fc-130">Selecteer **Redencode migreren**.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="bd9fc-131">[![Redencode migreren](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="bd9fc-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="bd9fc-132">In het deelvenster **Migratie redencodes vergoedingen** hebt u twee opties voor toewijzing aan een redencode voor personeelsbeheer:</span><span class="sxs-lookup"><span data-stu-id="bd9fc-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="bd9fc-133">Als u een bestaande redencode wilt gebruiken in Personeelsbeheer, kiest u een code in de vervolgkeuzelijst **Bestaande redencode gebruiken**.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="bd9fc-134">U kunt alleen een bestaande redencode gebruiken in Personeelsbeheer als een andere redencode voor Vergoedingenbeheer er nog niet naartoe is gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="bd9fc-135">Als u een nieuwe redencode wilt maken in Personeelsbeheer, voert u een nieuwe code in het veld **Nieuwe redencode** in en voert u vervolgens een omschrijving in **Nieuwe omschrijving** in.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="bd9fc-136">[![Toewijzen aan een redencode voor Personeelsbeheer](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="bd9fc-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="bd9fc-137">Nadat redencodes naar Personeelsbeheer zijn gemigreerd, wordt de optie voor het gebruik ervan in Vergoedingenbeheer automatisch ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="bd9fc-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="bd9fc-138">[![Redencode gebruiken in Vergoedingenbeheer](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="bd9fc-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]