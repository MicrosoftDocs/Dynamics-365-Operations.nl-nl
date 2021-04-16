---
title: Een organisatiehiërarchie maken
description: Gebruik de volgende procedure om een organisatiehiërarchie te maken.
author: sericks007
ms.date: 12/15/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d27bec86302f3e6cef8318a0d846f31d2d9c6a5
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747388"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="e6676-103">Een organisatiehiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="e6676-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e6676-104">Gebruik de volgende procedure om een organisatiehiërarchie te maken.</span><span class="sxs-lookup"><span data-stu-id="e6676-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="e6676-105">Met organisatiehiërarchieën kunt u vanuit verschillende gezichtspunten kijken naar en rapporteren over uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="e6676-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="e6676-106">U kunt bijvoorbeeld een hiërarchie instellen voor belastingaangifte.</span><span class="sxs-lookup"><span data-stu-id="e6676-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="e6676-107">Vervolgens kunt u een andere hiërarchie instellen voor het rapporteren van financiële gegevens die niet wettelijk vereist zijn, maar die voor interne rapportage worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e6676-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="e6676-108">Voordat u een organisatiehiërarchie maakt, moet u organisaties maken.</span><span class="sxs-lookup"><span data-stu-id="e6676-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="e6676-109">Zie voor meer informatie de taak "Een rechtspersoon maken" of "Een operationele eenheid maken".</span><span class="sxs-lookup"><span data-stu-id="e6676-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="e6676-110">U kunt ook afdelingen en teams maken.</span><span class="sxs-lookup"><span data-stu-id="e6676-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="e6676-111">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="e6676-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="e6676-112">Een hiërarchie maken</span><span class="sxs-lookup"><span data-stu-id="e6676-112">Create a hierarchy</span></span>
1. <span data-ttu-id="e6676-113">Ga naar **Navigatievenster > Modules > Organisatiebeheer > Organisaties > Organisatiehiërarchieën**.</span><span class="sxs-lookup"><span data-stu-id="e6676-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="e6676-114">Klik in het **actievenster** op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e6676-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="e6676-115">Typ een waarde in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="e6676-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="e6676-116">Klik in de sectie **Doel** op **Doel toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="e6676-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="e6676-117">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e6676-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="e6676-118">Selecteer een doel om aan uw organisatiehiërarchie toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="e6676-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="e6676-119">Klik in de sectie **Toegewezen hiërarchieën** op **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="e6676-119">In the **Assigned hierarchies** section, click **Add**.</span></span>
7. <span data-ttu-id="e6676-120">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e6676-120">In the list, mark the selected row.</span></span> <span data-ttu-id="e6676-121">Zoek de hiërarchie u zojuist hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="e6676-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="e6676-122">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="e6676-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="e6676-123">Organisaties aan de hiërarchie toevoegen</span><span class="sxs-lookup"><span data-stu-id="e6676-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="e6676-124">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e6676-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="e6676-125">Selecteer uw hiërarchie.</span><span class="sxs-lookup"><span data-stu-id="e6676-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="e6676-126">Klik in de sectie **Toegewezen hiërarchieën** op **Hiërarchie weergeven**.</span><span class="sxs-lookup"><span data-stu-id="e6676-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="e6676-127">Voer zo nodig organisaties toe.</span><span class="sxs-lookup"><span data-stu-id="e6676-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="e6676-128">Als u een organisatie wilt toevoegen, klikt u op **Bewerken** en vervolgens op **Invoegen** om de organisatie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="e6676-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="e6676-129">Wanneer u klaar bent met het aanbrengen van wijzigingen, kunt u een concept **opslaan** en/of de wijzigingen **publiceren**.</span><span class="sxs-lookup"><span data-stu-id="e6676-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]