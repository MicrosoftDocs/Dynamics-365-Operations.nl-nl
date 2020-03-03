---
title: Online kanaal maken en kanaalkenmerken definiëren
description: Deze procedure doorloopt het maken van een nieuw online kanaal en het toevoegen ervan aan de organisatiehiërarchie.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4bac365217c20bececa1b4ff2b9de12288326dcc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022128"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="eea4b-103">Online kanaal maken en kanaalkenmerken definiëren</span><span class="sxs-lookup"><span data-stu-id="eea4b-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="eea4b-104">Deze procedure doorloopt het maken van een nieuw online kanaal en het toevoegen ervan aan de organisatiehiërarchie.</span><span class="sxs-lookup"><span data-stu-id="eea4b-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="eea4b-105">U moet de organisatiehiërarchie maken voordat u een nieuw online kanaal kunt maken.</span><span class="sxs-lookup"><span data-stu-id="eea4b-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="eea4b-106">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="eea4b-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="eea4b-107">Een nieuw online kanaal maken</span><span class="sxs-lookup"><span data-stu-id="eea4b-107">Create a new online channel</span></span>
1. <span data-ttu-id="eea4b-108">Ga naar Retail en Commerce > Kanalen > Online winkels.</span><span class="sxs-lookup"><span data-stu-id="eea4b-108">Go to Retail and Commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="eea4b-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="eea4b-109">Click New.</span></span>
3. <span data-ttu-id="eea4b-110">Typ een waarde in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="eea4b-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="eea4b-111">Typ of selecteer een waarde in het veld Magazijn.</span><span class="sxs-lookup"><span data-stu-id="eea4b-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="eea4b-112">Selecteer een optie in het veld Winkeltijdzone.</span><span class="sxs-lookup"><span data-stu-id="eea4b-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="eea4b-113">Typ of selecteer een waarde in het veld Standaardklant.</span><span class="sxs-lookup"><span data-stu-id="eea4b-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="eea4b-114">Typ of selecteer een waarde in het veld Adresboek van klant.</span><span class="sxs-lookup"><span data-stu-id="eea4b-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="eea4b-115">Typ of selecteer een waarde in het veld Betalingstermijnen.</span><span class="sxs-lookup"><span data-stu-id="eea4b-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="eea4b-116">Typ of selecteer een waarde in het veld Betalingsmethode.</span><span class="sxs-lookup"><span data-stu-id="eea4b-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="eea4b-117">Typ of selecteer een waarde in het veld Profiel voor e-mailmelding.</span><span class="sxs-lookup"><span data-stu-id="eea4b-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="eea4b-118">Vouw de sectie Financiële dimensies uit.</span><span class="sxs-lookup"><span data-stu-id="eea4b-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="eea4b-119">Typ of selecteer een waarde in het veld Bedrijfseenheid.</span><span class="sxs-lookup"><span data-stu-id="eea4b-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="eea4b-120">Stel ook de waarde in voor alle andere standaarddimensies.</span><span class="sxs-lookup"><span data-stu-id="eea4b-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="eea4b-121">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="eea4b-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="eea4b-122">Het online kanaal toevoegen aan de organisatiehiërarchie</span><span class="sxs-lookup"><span data-stu-id="eea4b-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="eea4b-123">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="eea4b-123">Close the page.</span></span>
2. <span data-ttu-id="eea4b-124">Ga naar Organisatiebeheer > Organisaties > Organisatiehiërarchieën.</span><span class="sxs-lookup"><span data-stu-id="eea4b-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="eea4b-125">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="eea4b-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="eea4b-126">Klik op Weergeven.</span><span class="sxs-lookup"><span data-stu-id="eea4b-126">Click View.</span></span>
5. <span data-ttu-id="eea4b-127">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="eea4b-127">Click Edit.</span></span>
    * <span data-ttu-id="eea4b-128">U kunt elk hiërarchieknooppunt selecteren waaronder u het nieuwe kanaal wilt invoegen.</span><span class="sxs-lookup"><span data-stu-id="eea4b-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="eea4b-129">Klik op Invoegen.</span><span class="sxs-lookup"><span data-stu-id="eea4b-129">Click Insert.</span></span>
7. <span data-ttu-id="eea4b-130">Klik op Commerce-kanaal.</span><span class="sxs-lookup"><span data-stu-id="eea4b-130">Click Commerce channel.</span></span>
8. <span data-ttu-id="eea4b-131">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="eea4b-131">Click OK.</span></span>
9. <span data-ttu-id="eea4b-132">Klik op Publiceren om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="eea4b-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="eea4b-133">Typ in het veld Begindatum de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="eea4b-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="eea4b-134">Klik op Publiceren.</span><span class="sxs-lookup"><span data-stu-id="eea4b-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-real-time-notification"></a><span data-ttu-id="eea4b-135">Orders configureren voor meldingen in bijna realtime</span><span class="sxs-lookup"><span data-stu-id="eea4b-135">Configure orders for near real-time notification</span></span>
1. <span data-ttu-id="eea4b-136">Ga naar Retail en Commerce > Instelling van hoofdkantoor > Parameters > Commerce-parameters.</span><span class="sxs-lookup"><span data-stu-id="eea4b-136">Go to Retail and Commerce  > Headquarters setup > Parameters > Commerce parameters.</span></span>
2. <span data-ttu-id="eea4b-137">Stel Real-time service gebruiken om eCommerce-orders te maken in op Ja.</span><span class="sxs-lookup"><span data-stu-id="eea4b-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="eea4b-138">Voer de distributieplanning 1070 uit om wijzigingen te synchroniseren naar de kanaaldatabase.</span><span class="sxs-lookup"><span data-stu-id="eea4b-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 

