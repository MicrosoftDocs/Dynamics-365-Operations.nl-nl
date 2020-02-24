---
title: POS-machtigingsgroepen maken
description: In dit onderwerp wordt uitgelegd hoe u een POS-machtigingsgroep maakt.
author: scott-tucker
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailPosPermissionGroup, HcmJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6f9f8f970f336a0cce6bcac78e32a1b7fe0a252
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022127"
---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="5db68-103">POS-machtigingsgroepen maken</span><span class="sxs-lookup"><span data-stu-id="5db68-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="5db68-104">In dit onderwerp wordt uitgelegd hoe u een POS-machtigingsgroep maakt.</span><span class="sxs-lookup"><span data-stu-id="5db68-104">This topic explains how to create a POS permission group.</span></span> <span data-ttu-id="5db68-105">Het demobedrijf dat wordt gebruikt om deze taak te maken is USRT.</span><span class="sxs-lookup"><span data-stu-id="5db68-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="5db68-106">Deze taak is bedoeld voor de rol Commerce-bedrijfsbeheerder.</span><span class="sxs-lookup"><span data-stu-id="5db68-106">This task is intended for the Commerce operations manager role.</span></span>

1. <span data-ttu-id="5db68-107">Ga in het navigatievenster naar **Modules > Retail en Commerce > Medewerkers > Machtigingsgroepen**.</span><span class="sxs-lookup"><span data-stu-id="5db68-107">In the navigation pane, go to **Modules > Retail and Commerce > Employees > Permission groups**.</span></span>
2. <span data-ttu-id="5db68-108">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="5db68-108">Select **New**.</span></span>
3. <span data-ttu-id="5db68-109">Typ een waarde in het veld **POS-machtigingsgroeps-id**.</span><span class="sxs-lookup"><span data-stu-id="5db68-109">In the **POS permission group ID** field, type a value.</span></span>
4. <span data-ttu-id="5db68-110">Typ een waarde in het veld **Beschrijving**.</span><span class="sxs-lookup"><span data-stu-id="5db68-110">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="5db68-111">Selecteer **Ja** in het veld **Registraties tijdklok weergeven**.</span><span class="sxs-lookup"><span data-stu-id="5db68-111">Select **Yes** in the **View time clock entries** field.</span></span> <span data-ttu-id="5db68-112">U kunt nu diverse machtigingen voor uw POS-machtigingsgroep inschakelen of uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="5db68-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="5db68-113">Voor sommige machtigingen kunt u een waarde instellen die wordt gebruikt om te beoordelen of de POS-gebruiker de actie kan uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="5db68-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span> <span data-ttu-id="5db68-114">Deze taakregistratie activeert een paar machtigingen die aan een kassier kunnen worden gegeven.</span><span class="sxs-lookup"><span data-stu-id="5db68-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="5db68-115">Selecteer **Ja** in het veld **Order maken toestaan**.</span><span class="sxs-lookup"><span data-stu-id="5db68-115">Select **Yes** in the **Allow create order** field.</span></span>
7. <span data-ttu-id="5db68-116">Selecteer **Ja** in het veld **Order bewerken toestaan**.</span><span class="sxs-lookup"><span data-stu-id="5db68-116">Select **Yes** in the **Allow edit order** field.</span></span>
8. <span data-ttu-id="5db68-117">Selecteer **Ja** in het veld **Order ophalen toestaan**.</span><span class="sxs-lookup"><span data-stu-id="5db68-117">Select **Yes** in the **Allow retrieve order** field.</span></span>
9. <span data-ttu-id="5db68-118">Selecteer **Ja** in het veld **Wachtwoordwijziging toestaan**.</span><span class="sxs-lookup"><span data-stu-id="5db68-118">Select **Yes** in the **Allow password change** field.</span></span>
10. <span data-ttu-id="5db68-119">Selecteer **Ja** in het veld **Blind sluiten toestaan**.</span><span class="sxs-lookup"><span data-stu-id="5db68-119">Select **Yes** in the **Allow blind close** field.</span></span>
11. <span data-ttu-id="5db68-120">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="5db68-120">Select **Save**.</span></span> <span data-ttu-id="5db68-121">Nadat uw wijzigingen zijn opgeslagen, moet u de personeelsdistributieplanning uitvoeren om de wijzigingen naar Commerce te pushen.</span><span class="sxs-lookup"><span data-stu-id="5db68-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to commerce channels.</span></span> 
12. <span data-ttu-id="5db68-122">Ga in het navigatievenster naar **Modules > Human Resources > Taken > Taken**.</span><span class="sxs-lookup"><span data-stu-id="5db68-122">In the navigation pane, go to **Modules > Human resources > Jobs > Jobs**.</span></span>
13. <span data-ttu-id="5db68-123">Vervolgens wordt de POS-machtigingsgroep aan een taak toegewezen.</span><span class="sxs-lookup"><span data-stu-id="5db68-123">Next we will assign the POS permission group to a Job.</span></span> <span data-ttu-id="5db68-124">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="5db68-124">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="5db68-125">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="5db68-125">Select **Edit**.</span></span>
15. <span data-ttu-id="5db68-126">Vouw de sectie **Taakclassificatie** uit.</span><span class="sxs-lookup"><span data-stu-id="5db68-126">Expand the **Job classification** section.</span></span>
16. <span data-ttu-id="5db68-127">Typ of selecteer een waarde in het veld POS-machtigingsgroep.</span><span class="sxs-lookup"><span data-stu-id="5db68-127">In the POS permission group field, enter or select a value.</span></span> <span data-ttu-id="5db68-128">Alle werknemers in posities voor deze taak gebruiken de instellingen van deze POS-machtigingsgroep tenzij de POS-machtigingen van de werknemers zijn overschreven op hun positieniveau.</span><span class="sxs-lookup"><span data-stu-id="5db68-128">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
17. <span data-ttu-id="5db68-129">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="5db68-129">Select **Save**.</span></span> <span data-ttu-id="5db68-130">Nadat uw wijzigingen zijn opgeslagen, moet u de personeelsdistributieplanning uitvoeren om de wijzigingen naar kanalen te pushen.</span><span class="sxs-lookup"><span data-stu-id="5db68-130">After your changes are saved you need to run the Staff distribution schedule to push the changes to channels.</span></span>  

