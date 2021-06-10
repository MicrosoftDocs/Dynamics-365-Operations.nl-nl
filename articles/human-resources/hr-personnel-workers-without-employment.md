---
title: Medewerkers zonder dienstverband
description: Medewerkers zonder toekomstig, actief of historisch dienstverband bij uw organisatie worden weergegeven in het formulier Medewerkers zonder dienstverband.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f6fbada6feb55b8627b1aa1ddfe367177edb7a0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051708"
---
# <a name="workers-without-employment"></a><span data-ttu-id="194fe-103">Medewerkers zonder dienstverband</span><span class="sxs-lookup"><span data-stu-id="194fe-103">Workers without employment</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="194fe-104">Medewerkers zonder toekomstig, actief of historisch dienstverband bij uw organisatie worden weergegeven in het formulier **Medewerkers zonder dienstverband**.</span><span class="sxs-lookup"><span data-stu-id="194fe-104">Workers with no future, active, or historical employment with your organization appear in the **Workers without employment** form.</span></span> <span data-ttu-id="194fe-105">Medewerkers met deze status kunnen worden weergegeven wanneer u medewerkers importeert zonder dienstverbandrecord, of wanneer u het dienstverband van een medewerker verwijdert via **Medewerkers > Historie dienstverband**.</span><span class="sxs-lookup"><span data-stu-id="194fe-105">Workers with this status can appear when you import workers without an employment record, or when you delete a worker's employment via **Workers > Employment history**.</span></span>

<span data-ttu-id="194fe-106">Het formulier **Medewerkers zonder dienstverband** is standaard beschikbaar voor de volgende rollen:</span><span class="sxs-lookup"><span data-stu-id="194fe-106">By default, the **Workers without employment** form is available to the following roles:</span></span>

- <span data-ttu-id="194fe-107">HR-assistent</span><span class="sxs-lookup"><span data-stu-id="194fe-107">Human Resources Assistant</span></span>
- <span data-ttu-id="194fe-108">HR-manager</span><span class="sxs-lookup"><span data-stu-id="194fe-108">Human Resources Manager</span></span>
- <span data-ttu-id="194fe-109">Werver</span><span class="sxs-lookup"><span data-stu-id="194fe-109">Recruiter</span></span>
- <span data-ttu-id="194fe-110">Manager Compensatie en vergoedingen</span><span class="sxs-lookup"><span data-stu-id="194fe-110">Comp and Benefits Manager</span></span>
- <span data-ttu-id="194fe-111">Salarisadministrateur</span><span class="sxs-lookup"><span data-stu-id="194fe-111">Payroll Administrator</span></span>
- <span data-ttu-id="194fe-112">Salarismanager</span><span class="sxs-lookup"><span data-stu-id="194fe-112">Payroll Manager</span></span>
- <span data-ttu-id="194fe-113">Opleidingsmanager</span><span class="sxs-lookup"><span data-stu-id="194fe-113">Training Manager</span></span>

<span data-ttu-id="194fe-114">In de lijst **Medewerkers zonder dienstverband** kunt u de vermelde personen verwijderen.</span><span class="sxs-lookup"><span data-stu-id="194fe-114">In the **Workers without employment** list, you can delete the individuals listed.</span></span> <span data-ttu-id="194fe-115">Deze bevoegdheid wordt standaard gegeven aan de rol HR-assistent.</span><span class="sxs-lookup"><span data-stu-id="194fe-115">By default, this privilege is given to the Human Resources Assistant role.</span></span> <span data-ttu-id="194fe-116">U kunt deze bevoegdheid aan andere rollen toewijzen met de volgende stappen:</span><span class="sxs-lookup"><span data-stu-id="194fe-116">You can give this privilege to other roles with the following steps:</span></span>

1. <span data-ttu-id="194fe-117">Selecteer **Systeembeheer** en selecteer vervolgens **Beveiligingsconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="194fe-117">Select **System administration**, and then select **Security configuration**.</span></span>

2. <span data-ttu-id="194fe-118">Filter op het tabblad **Bevoegdheden** de lijst **Bevoegdheden** op **Medewerkers onderhouden**.</span><span class="sxs-lookup"><span data-stu-id="194fe-118">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>

   <span data-ttu-id="194fe-119">[![Lijst met bevoegdheden filteren](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span><span class="sxs-lookup"><span data-stu-id="194fe-119">[![Filter Privileges list](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)</span></span>

3. <span data-ttu-id="194fe-120">Selecteer in de kolom **Verwijzingen** de optie **Opdrachten in weergavemenu**.</span><span class="sxs-lookup"><span data-stu-id="194fe-120">In the **References** column, select **Display menu items**.</span></span>

4. <span data-ttu-id="194fe-121">Selecteer onder **Opdrachten in weergavemenu** de optie **HcmWorkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="194fe-121">In **Display menu items**, select **HcmWorkersWithoutEmployment**.</span></span>

   <span data-ttu-id="194fe-122">[![Formulier selecteren](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span><span class="sxs-lookup"><span data-stu-id="194fe-122">[![Select form](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)</span></span>

5. <span data-ttu-id="194fe-123">Stel de machtiging **Verwijderen** in op **Toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="194fe-123">Set the **Delete** permission to **Grant**.</span></span>

6. <span data-ttu-id="194fe-124">Selecteer het tabblad **Niet-gepubliceerde objecten**.</span><span class="sxs-lookup"><span data-stu-id="194fe-124">Select the **Unpublished objects** tab.</span></span>

7. <span data-ttu-id="194fe-125">Selecteer **Alles publiceren**.</span><span class="sxs-lookup"><span data-stu-id="194fe-125">Select **Publish all**.</span></span>

   <span data-ttu-id="194fe-126">[![Wijzigingen publiceren](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span><span class="sxs-lookup"><span data-stu-id="194fe-126">[![Publish changes](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]