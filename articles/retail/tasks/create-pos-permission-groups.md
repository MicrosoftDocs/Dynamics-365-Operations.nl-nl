--- 
title: Machtigingsgroepen voor verkooppunten (POS) maken
description: Deze procedure laat zien hoe u een POS-machtigingengroep maakt.
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 5098fb3339403b6f2779dfe3bb7ef5c4ca78051f
ms.openlocfilehash: a0d2041326856688caa3da01bfb50a2942232ada
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---
# <a name="create-point-of-sale-pos-permission-groups"></a><span data-ttu-id="4020f-103">Machtigingsgroepen voor verkooppunten (POS) maken</span><span class="sxs-lookup"><span data-stu-id="4020f-103">Create point of sale (POS) permission groups</span></span>

[!include [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="4020f-104">Deze procedure laat zien hoe u een POS-machtigingengroep maakt.</span><span class="sxs-lookup"><span data-stu-id="4020f-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="4020f-105">Het demobedrijf dat wordt gebruikt om deze taak te maken is USRT.</span><span class="sxs-lookup"><span data-stu-id="4020f-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="4020f-106">Deze taak is bedoeld voor de rol Bedrijfsbeheerder detailhandel.</span><span class="sxs-lookup"><span data-stu-id="4020f-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="4020f-107">Ga naar Machtigingsgroepen.</span><span class="sxs-lookup"><span data-stu-id="4020f-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="4020f-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="4020f-108">Click New.</span></span>
3. <span data-ttu-id="4020f-109">Typ een waarde in het veld POS-machtigingsgroeps-id.</span><span class="sxs-lookup"><span data-stu-id="4020f-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="4020f-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="4020f-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4020f-111">Selecteer Ja in het veld Registraties tijdklok weergeven.</span><span class="sxs-lookup"><span data-stu-id="4020f-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="4020f-112">U kunt nu diverse machtigingen voor uw POS-machtigingsgroep inschakelen of uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="4020f-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="4020f-113">Voor sommige machtigingen kunt u een waarde instellen die wordt gebruikt om te beoordelen of de POS-gebruiker de actie kan uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="4020f-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="4020f-114">Deze taakregistratie activeert een paar machtigingen die aan een kassier kunnen worden gegeven.</span><span class="sxs-lookup"><span data-stu-id="4020f-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="4020f-115">Selecteer Ja in het veld Order maken toestaan.</span><span class="sxs-lookup"><span data-stu-id="4020f-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="4020f-116">Selecteer Ja in het veld Order bewerken toestaan.</span><span class="sxs-lookup"><span data-stu-id="4020f-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="4020f-117">Selecteer Ja in het veld Order ophalen toestaan.</span><span class="sxs-lookup"><span data-stu-id="4020f-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="4020f-118">Selecteer Ja in het veld Wachtwoordwijziging toestaan.</span><span class="sxs-lookup"><span data-stu-id="4020f-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="4020f-119">Selecteer Ja in het veld Blind sluiten toestaan.</span><span class="sxs-lookup"><span data-stu-id="4020f-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="4020f-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4020f-120">Click Save.</span></span>
    * <span data-ttu-id="4020f-121">Nadat uw wijzigingen zijn opgeslagen, moet u de personeelsdistributieplanning uitvoeren om de wijzigingen naar detailhandelkanalen te pushen.</span><span class="sxs-lookup"><span data-stu-id="4020f-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="4020f-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="4020f-122">Close the page.</span></span>
13. <span data-ttu-id="4020f-123">Ga naar Taken.</span><span class="sxs-lookup"><span data-stu-id="4020f-123">Go to Jobs.</span></span>
    * <span data-ttu-id="4020f-124">Vervolgens wordt de POS-machtigingsgroep aan een taak toegewezen.</span><span class="sxs-lookup"><span data-stu-id="4020f-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="4020f-125">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="4020f-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="4020f-126">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="4020f-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="4020f-127">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="4020f-127">Click Edit.</span></span>
17. <span data-ttu-id="4020f-128">Vouw de sectie Taakclassificatie uit.</span><span class="sxs-lookup"><span data-stu-id="4020f-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="4020f-129">Typ of selecteer een waarde in het veld POS-machtigingsgroep.</span><span class="sxs-lookup"><span data-stu-id="4020f-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="4020f-130">Alle werknemers in posities voor deze taak gebruiken de instellingen van deze POS-machtigingsgroep tenzij de POS-machtigingen van de werknemers zijn overschreven op hun positieniveau.</span><span class="sxs-lookup"><span data-stu-id="4020f-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="4020f-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="4020f-131">Click Save.</span></span>
    * <span data-ttu-id="4020f-132">Nadat uw wijzigingen zijn opgeslagen, moet u de personeelsdistributieplanning uitvoeren om de wijzigingen naar detailhandelkanalen te pushen.</span><span class="sxs-lookup"><span data-stu-id="4020f-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  


