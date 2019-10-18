---
title: Een organisatiehiërarchie maken
description: Gebruik de volgende procedure om een organisatiehiërarchie te maken.
author: sericks007
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48c8564694b22a5110341d853a79096fbe805c91
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177246"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="e998e-103">Een organisatiehiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="e998e-103">Create an organization hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e998e-104">Gebruik de volgende procedure om een organisatiehiërarchie te maken.</span><span class="sxs-lookup"><span data-stu-id="e998e-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="e998e-105">Met organisatiehiërarchieën kunt u vanuit verschillende gezichtspunten kijken naar en rapporteren over uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="e998e-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="e998e-106">U kunt bijvoorbeeld een hiërarchie instellen voor belastingaangifte.</span><span class="sxs-lookup"><span data-stu-id="e998e-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="e998e-107">Vervolgens kunt u een andere hiërarchie instellen voor het rapporteren van financiële gegevens die niet wettelijk vereist zijn, maar die voor interne rapportage worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e998e-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="e998e-108">Voordat u een organisatiehiërarchie maakt, moet u organisaties maken.</span><span class="sxs-lookup"><span data-stu-id="e998e-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="e998e-109">Zie voor meer informatie de taak "Een rechtspersoon maken" of "Een operationele eenheid maken".</span><span class="sxs-lookup"><span data-stu-id="e998e-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="e998e-110">U kunt ook afdelingen en teams maken.</span><span class="sxs-lookup"><span data-stu-id="e998e-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="e998e-111">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="e998e-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="e998e-112">Een hiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="e998e-112">Create a hierarchy</span></span>
1. <span data-ttu-id="e998e-113">Ga naar **Navigatievenster > Modules > Organisatiebeheer > Organisaties > Organisatiehiërarchieën**.</span><span class="sxs-lookup"><span data-stu-id="e998e-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="e998e-114">Klik in het **actievenster** op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e998e-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="e998e-115">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="e998e-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="e998e-116">Klik in de sectie **Doel** op **Doel toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="e998e-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="e998e-117">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e998e-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="e998e-118">Selecteer een doel om aan uw organisatiehiërarchie toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="e998e-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="e998e-119">Klik in de sectie **Toegewezen hiërarchieën** op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e998e-119">In the **Assigned hierarchies** sectiom, click **Add**.</span></span>
7. <span data-ttu-id="e998e-120">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e998e-120">In the list, mark the selected row.</span></span> <span data-ttu-id="e998e-121">Zoek de hiërarchie u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e998e-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="e998e-122">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="e998e-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="e998e-123">Organisaties aan de hiërarchie toevoegen</span><span class="sxs-lookup"><span data-stu-id="e998e-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="e998e-124">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e998e-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="e998e-125">Selecteer uw hiërarchie.</span><span class="sxs-lookup"><span data-stu-id="e998e-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="e998e-126">Klik in de sectie **Toegewezen hiërarchieën** op **Hiërarchie weergeven**.</span><span class="sxs-lookup"><span data-stu-id="e998e-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="e998e-127">Voer zo nodig organisaties toe.</span><span class="sxs-lookup"><span data-stu-id="e998e-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="e998e-128">Als u een organisatie wilt toevoegen, klikt u op **Bewerken** en vervolgens op **Invoegen** om de organisatie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e998e-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="e998e-129">Wanneer u klaar bent met het aanbrengen van wijzigingen, kunt u een concept **opslaan** en/of de wijzigingen **publiceren**.</span><span class="sxs-lookup"><span data-stu-id="e998e-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  

