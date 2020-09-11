---
title: Parameters voor verlof en verzuim configureren
description: Definieer Human resources-parameters voor verlof en verzuim in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 196c3901b5bc19f73b882bac7d3361e5bcc37e07
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712371"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="7aecb-103">Parameters voor verlof en verzuim configureren</span><span class="sxs-lookup"><span data-stu-id="7aecb-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="7aecb-104">Voordat u verlof- en verzuimplannen instelt in Dynamics 365 Human Resources, kunt u het beste de instellingen controleren voor alle verwante Human resources-parameters, waaronder:</span><span class="sxs-lookup"><span data-stu-id="7aecb-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="7aecb-105">Nummerreeks voor verlofaanvragen</span><span class="sxs-lookup"><span data-stu-id="7aecb-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="7aecb-106">FMLA-instellingen (Family and Medical Leave Act)</span><span class="sxs-lookup"><span data-stu-id="7aecb-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="7aecb-107">Selfservice-instellingen voor werknemers voor verlof- en verzuimaanvragen</span><span class="sxs-lookup"><span data-stu-id="7aecb-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="7aecb-108">Verlof- en verzuimparameters</span><span class="sxs-lookup"><span data-stu-id="7aecb-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="7aecb-109">Human resources-parameters weergeven en wijzigen</span><span class="sxs-lookup"><span data-stu-id="7aecb-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="7aecb-110">Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="7aecb-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7aecb-111">Selecteer onder **Instellen** de optie **Human resources-parameters**.</span><span class="sxs-lookup"><span data-stu-id="7aecb-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="7aecb-112">Controleer op het tabblad **Nummerreeksen** de optie **Nummerreekscode** voor **Verlofaanvraag-id** en wijzig deze indien nodig.</span><span class="sxs-lookup"><span data-stu-id="7aecb-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="7aecb-113">Deze instelling bepaalt de volgorde waarin id's voor verlofaanvragen automatisch worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="7aecb-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="7aecb-114">Controleer op het tabblad **FMLA** de FMLA instellingen en wijzig deze indien nodig.</span><span class="sxs-lookup"><span data-stu-id="7aecb-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="7aecb-115">Geef op het tabblad **Selfservice werknemer** aan of managers verlof- en verzuimaanvragen kunnen invoeren namens hun werknemers.</span><span class="sxs-lookup"><span data-stu-id="7aecb-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="7aecb-116">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="7aecb-116">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="7aecb-117">Parameters voor verlof en verzuim weergeven en aanpassen</span><span class="sxs-lookup"><span data-stu-id="7aecb-117">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="7aecb-118">Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="7aecb-118">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7aecb-119">Selecteer onder **Instellingen** de optie **Parameters voor verlof en verzuim**.</span><span class="sxs-lookup"><span data-stu-id="7aecb-119">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="7aecb-120">Stel op het tabblad **Algemeen** de volgende parameters in:</span><span class="sxs-lookup"><span data-stu-id="7aecb-120">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="7aecb-121">Stel **Eenheid voor verlof en verzuim** in op uren of dagen.</span><span class="sxs-lookup"><span data-stu-id="7aecb-121">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="7aecb-122">Bij dagen kunt u de optie **Definitie halve dag inschakelen** om werknemers in staat te stellen om de eerste of de tweede helft van de dag te kiezen in hun verlofaanvraag.</span><span class="sxs-lookup"><span data-stu-id="7aecb-122">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="7aecb-123">Selecteer **Ingangsdatum servicemaanden** om in te stellen wanneer de toerekeningspercentages van kracht worden voor verlofplannen met servicemaanden.</span><span class="sxs-lookup"><span data-stu-id="7aecb-123">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="7aecb-124">Selecteer **Saldoberekening** om saldi weer te geven vanaf vandaag of vanaf de toerekeningsperiode.</span><span class="sxs-lookup"><span data-stu-id="7aecb-124">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="7aecb-125">Als u vandaag **Saldo vanaf vandaag** selecteert, wordt in het saldo het totaal van alle transitorische posten, correcties en aanvragen vanaf vandaag weergegeven.</span><span class="sxs-lookup"><span data-stu-id="7aecb-125">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="7aecb-126">Als u **Saldo vanaf toerekeningsperiode** selecteert, wordt in het saldo het totaal van alle transitorische posten, correcties en aanvragen weergegeven vanaf de toerekeningsperiode die is gedefinieerd door de frequentie in het verlofplan.</span><span class="sxs-lookup"><span data-stu-id="7aecb-126">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="7aecb-127">Stel de begintijd in voor de batchtaak voor het transporteren van vervaldatums.</span><span class="sxs-lookup"><span data-stu-id="7aecb-127">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="7aecb-128">Selecteer **Ja** om **Werknemers toestaan om verlof te kopen** en **Werknemers toestaan om verlof te verkopen**.</span><span class="sxs-lookup"><span data-stu-id="7aecb-128">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="7aecb-129">Als u **Ja** selecteert voor deze opties, kunt u een inkoop- en verkoopbeleid maken en werknemers in staat stellen om aanvragen voor het kopen en verkopen van verlof in te dienen.</span><span class="sxs-lookup"><span data-stu-id="7aecb-129">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="7aecb-130">Kalenderparameters configureren</span><span class="sxs-lookup"><span data-stu-id="7aecb-130">Configure calendar parameters</span></span>

1. <span data-ttu-id="7aecb-131">Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="7aecb-131">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7aecb-132">Selecteer onder **Instellingen** de optie **Parameters voor verlof en verzuim**.</span><span class="sxs-lookup"><span data-stu-id="7aecb-132">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="7aecb-133">Wijzig op het tabblad **Kalender** de kalenderinstellingen indien nodig.</span><span class="sxs-lookup"><span data-stu-id="7aecb-133">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="7aecb-134">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="7aecb-134">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="7aecb-135">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7aecb-135">See also</span></span>

- [<span data-ttu-id="7aecb-136">Overzicht van verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="7aecb-136">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
