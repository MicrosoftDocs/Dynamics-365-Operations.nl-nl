--- 
title: " POS-machtigingsgroepen maken"
description: Deze procedure laat zien hoe u een POS-machtigingengroep maakt.
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e924dc59c3e4cb9b6979014852512453dd3d70db
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="a70e0-103"> POS-machtigingsgroepen maken</span><span class="sxs-lookup"><span data-stu-id="a70e0-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a70e0-104">Deze procedure laat zien hoe u een POS-machtigingengroep maakt.</span><span class="sxs-lookup"><span data-stu-id="a70e0-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="a70e0-105">Het demobedrijf dat wordt gebruikt om deze taak te maken is USRT.</span><span class="sxs-lookup"><span data-stu-id="a70e0-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="a70e0-106">Deze taak is bedoeld voor de rol Bedrijfsbeheerder detailhandel.</span><span class="sxs-lookup"><span data-stu-id="a70e0-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="a70e0-107">Ga naar Machtigingsgroepen.</span><span class="sxs-lookup"><span data-stu-id="a70e0-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="a70e0-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="a70e0-108">Click New.</span></span>
3. <span data-ttu-id="a70e0-109">Typ een waarde in het veld POS-machtigingsgroeps-id.</span><span class="sxs-lookup"><span data-stu-id="a70e0-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="a70e0-110">Typ een waarde in het veld Omschrijving.</span><span class="sxs-lookup"><span data-stu-id="a70e0-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a70e0-111">Selecteer Ja in het veld Registraties tijdklok weergeven.</span><span class="sxs-lookup"><span data-stu-id="a70e0-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="a70e0-112">U kunt nu diverse machtigingen voor uw POS-machtigingsgroep inschakelen of uitschakelen.</span><span class="sxs-lookup"><span data-stu-id="a70e0-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="a70e0-113">Voor sommige machtigingen kunt u een waarde instellen die wordt gebruikt om te beoordelen of de POS-gebruiker de actie kan uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="a70e0-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="a70e0-114">Deze taakregistratie activeert een paar machtigingen die aan een kassier kunnen worden gegeven.</span><span class="sxs-lookup"><span data-stu-id="a70e0-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="a70e0-115">Selecteer Ja in het veld Order maken toestaan.</span><span class="sxs-lookup"><span data-stu-id="a70e0-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="a70e0-116">Selecteer Ja in het veld Order bewerken toestaan.</span><span class="sxs-lookup"><span data-stu-id="a70e0-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="a70e0-117">Selecteer Ja in het veld Order ophalen toestaan.</span><span class="sxs-lookup"><span data-stu-id="a70e0-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="a70e0-118">Selecteer Ja in het veld Wachtwoordwijziging toestaan.</span><span class="sxs-lookup"><span data-stu-id="a70e0-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="a70e0-119">Selecteer Ja in het veld Blind sluiten toestaan.</span><span class="sxs-lookup"><span data-stu-id="a70e0-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="a70e0-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a70e0-120">Click Save.</span></span>
    * <span data-ttu-id="a70e0-121">Nadat uw wijzigingen zijn opgeslagen, moet u de personeelsdistributieplanning uitvoeren om de wijzigingen naar detailhandelkanalen te pushen.</span><span class="sxs-lookup"><span data-stu-id="a70e0-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="a70e0-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="a70e0-122">Close the page.</span></span>
13. <span data-ttu-id="a70e0-123">Ga naar Taken.</span><span class="sxs-lookup"><span data-stu-id="a70e0-123">Go to Jobs.</span></span>
    * <span data-ttu-id="a70e0-124">Vervolgens wordt de POS-machtigingsgroep aan een taak toegewezen.</span><span class="sxs-lookup"><span data-stu-id="a70e0-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="a70e0-125">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="a70e0-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="a70e0-126">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="a70e0-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="a70e0-127">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="a70e0-127">Click Edit.</span></span>
17. <span data-ttu-id="a70e0-128">Vouw de sectie Taakclassificatie uit.</span><span class="sxs-lookup"><span data-stu-id="a70e0-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="a70e0-129">Typ of selecteer een waarde in het veld POS-machtigingsgroep.</span><span class="sxs-lookup"><span data-stu-id="a70e0-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="a70e0-130">Alle werknemers in posities voor deze taak gebruiken de instellingen van deze POS-machtigingsgroep tenzij de POS-machtigingen van de werknemers zijn overschreven op hun positieniveau.</span><span class="sxs-lookup"><span data-stu-id="a70e0-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="a70e0-131">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="a70e0-131">Click Save.</span></span>
    * <span data-ttu-id="a70e0-132">Nadat uw wijzigingen zijn opgeslagen, moet u de personeelsdistributieplanning uitvoeren om de wijzigingen naar detailhandelkanalen te pushen.</span><span class="sxs-lookup"><span data-stu-id="a70e0-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  


