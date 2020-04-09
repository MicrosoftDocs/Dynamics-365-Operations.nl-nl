---
title: Een vast activum overboeken
description: Deze taakbegeleiding boekt de financiële gegevens voor het vaste-activaboek over van een set financiële dimensies naar een nieuwe set financiële dimensies.
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetTransfer, DimensionLookup, AssetTransferConfirmation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eb38483d3ac61acb4513e87d8c36ddd0f8863a10
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138042"
---
# <a name="transfer-a-fixed-asset"></a><span data-ttu-id="6495c-103">Een vast activum overboeken</span><span class="sxs-lookup"><span data-stu-id="6495c-103">Transfer a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6495c-104">Deze taakbegeleiding boekt de financiële gegevens voor het vaste-activaboek over van een set financiële dimensies naar een nieuwe set financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="6495c-104">This task guide will transfer the financial information for a fixed asset book from one financial dimension set to a new financial dimension set.</span></span>  <span data-ttu-id="6495c-105">Het gebruikt de accountantsrol en demogegevens voor de USMF-rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="6495c-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="6495c-106">Ga in het navigatievenster naar **Modules > Vaste activa > Vaste activa > Vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="6495c-106">In the Navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="6495c-107">Zoek en selecteer in de lijst het vaste activum om over te boeken.</span><span class="sxs-lookup"><span data-stu-id="6495c-107">In the list, find and select the fixed asset to transfer.</span></span>
3. <span data-ttu-id="6495c-108">Klik in het actievenster op **Vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="6495c-108">On the Action Pane, click **Fixed asset**.</span></span>
4. <span data-ttu-id="6495c-109">Klik op **Vaste activa overboeken**.</span><span class="sxs-lookup"><span data-stu-id="6495c-109">Click **Transfer fixed assets**.</span></span>
5. <span data-ttu-id="6495c-110">Voer een datum in het veld **Overdrachtsdatum** in.</span><span class="sxs-lookup"><span data-stu-id="6495c-110">In the **Transfer date** field, enter a date.</span></span>
6. <span data-ttu-id="6495c-111">Voer een opmerking in om de overboeking te beschrijven.</span><span class="sxs-lookup"><span data-stu-id="6495c-111">Enter comments to describe the transfer.</span></span>
    
    <span data-ttu-id="6495c-112">Deze lijst bevat alle boeken voor de vaste activa.</span><span class="sxs-lookup"><span data-stu-id="6495c-112">This list shows all books for the fixed asset.</span></span>  
7. <span data-ttu-id="6495c-113">Markeer de boeken die u naar een nieuwe set financiële dimensies wilt overboeken.</span><span class="sxs-lookup"><span data-stu-id="6495c-113">Mark the books you want to transfer to a new financial dimension set.</span></span>
    * <span data-ttu-id="6495c-114">Deze lijst toont de bestaande financiële dimensiewaarden voor het geselecteerde boek.</span><span class="sxs-lookup"><span data-stu-id="6495c-114">This list shows the existing financial dimension values for the selected book.</span></span>  
    * <span data-ttu-id="6495c-115">Selecteer de financiële dimensie die u voor het geselecteerde vaste activumboek wilt bijwerken.</span><span class="sxs-lookup"><span data-stu-id="6495c-115">Select the financial dimension you want to update for the selected fixed asset book.</span></span>  
8. <span data-ttu-id="6495c-116">Klik in het veld **Financiële dimensie** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="6495c-116">In the **Financial dimension** field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="6495c-117">Stel andere financiële dimensiewaarden in.</span><span class="sxs-lookup"><span data-stu-id="6495c-117">Set other financial dimension values as appropriate.</span></span>  
    * <span data-ttu-id="6495c-118">Alle financiële dimensiewaarden wijzigen wanneer een overboeking plaatsvindt, ongeacht of een waarde is ingevoerd of niet.</span><span class="sxs-lookup"><span data-stu-id="6495c-118">All financial dimension values change when a transfer occurs, whether a value has been entered or left blank.</span></span> <span data-ttu-id="6495c-119">Bijvoorbeeld, als u een waarde voor de BusinessUnit hebt ingevoerd en de financiële dimensies CostCenter en Department leeg laat.</span><span class="sxs-lookup"><span data-stu-id="6495c-119">For example, if you entered a value for the BusinessUnit and left the CostCenter and Department financial dimensions blank.</span></span> <span data-ttu-id="6495c-120">Als uw rekeningstructuur lege waarden toestaat voor CostCenter en Department, resulteert de overboeking in elk waardemodel met de nieuwe waarde voor BusinessUnit en een lege waarde voor CostCenter en Department.</span><span class="sxs-lookup"><span data-stu-id="6495c-120">If your account structure allows blank values for CostCenter and Department, the transfer would result in each value model having the new value for BusinessUnit and a blank value for CostCenter and Department.</span></span>  
9. <span data-ttu-id="6495c-121">Klik op **Bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="6495c-121">Click **Update**.</span></span>
    * <span data-ttu-id="6495c-122">U kunt de wijzigingen bekijken voordat de overboeking wordt voltooid.</span><span class="sxs-lookup"><span data-stu-id="6495c-122">You have the opportunity to preview the changes before finalizing the transfer.</span></span>  
    * <span data-ttu-id="6495c-123">Controleer resultaten voordat de vaste-activumboeken worden overgeboekt.</span><span class="sxs-lookup"><span data-stu-id="6495c-123">Review results before transferring the fixed asset books.</span></span>  
10. <span data-ttu-id="6495c-124">Klik op **Overboeken**.</span><span class="sxs-lookup"><span data-stu-id="6495c-124">Click **Transfer**.</span></span>

