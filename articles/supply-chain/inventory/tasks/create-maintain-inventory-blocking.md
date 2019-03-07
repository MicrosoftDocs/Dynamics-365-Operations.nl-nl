---
title: Een voorraadblokkering maken en beheren
description: Deze procedure laat zien hoe wordt voorkomen dat fysieke voorhanden voorraad kan worden gereserveerd door andere uitgaande brondocumenten met behulp van de voorraadblokkering.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 09789dc0b89f8bd36cca9b3e5be366bf17246243
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "322255"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="806fa-103">Een voorraadblokkering maken en beheren</span><span class="sxs-lookup"><span data-stu-id="806fa-103">Create and maintain an inventory blocking</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="806fa-104">Deze procedure laat zien hoe wordt voorkomen dat fysieke voorhanden voorraad kan worden gereserveerd door andere uitgaande brondocumenten met behulp van de voorraadblokkering.</span><span class="sxs-lookup"><span data-stu-id="806fa-104">This procedure shows how to prevent physical on-hand inventory from being reserved by other outbound source documents by using the inventory blocking.</span></span> <span data-ttu-id="806fa-105">U kunt de procedure uitvoeren in het demobedrijf USMF met de voorbeeldwaarden die worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="806fa-105">You can run the procedure in demo data company USMF using the example values that are shown.</span></span> <span data-ttu-id="806fa-106">U moet een artikel met fysieke beschikbare voorhanden voorraad hebben voordat u deze procedure start.</span><span class="sxs-lookup"><span data-stu-id="806fa-106">You need to have an item with physical on-hand inventory available before you start this procedure.</span></span>


## <a name="create-an-inventory-blocking"></a><span data-ttu-id="806fa-107">Een voorraadblokkering maken</span><span class="sxs-lookup"><span data-stu-id="806fa-107">Create an inventory blocking</span></span>
1. <span data-ttu-id="806fa-108">Ga naar Voorraadbeheer > Periodieke taken > Voorraadblokkering.</span><span class="sxs-lookup"><span data-stu-id="806fa-108">Go to Inventory management > Periodic tasks > Inventory blocking.</span></span>
2. <span data-ttu-id="806fa-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="806fa-109">Click New.</span></span>
3. <span data-ttu-id="806fa-110">Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="806fa-110">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="806fa-111">Selecteer in de lijst het artikel dat u wilt kiezen.</span><span class="sxs-lookup"><span data-stu-id="806fa-111">In the list, select the item you want to choose.</span></span> 
    * <span data-ttu-id="806fa-112">Selecteer een artikelnummer met fysieke voorhanden voorraad die u wilt blokkeren.</span><span class="sxs-lookup"><span data-stu-id="806fa-112">Select an item number with physical on-hand inventory that you want to block.</span></span> <span data-ttu-id="806fa-113">Als u USMF gebruikt, kunt u artikel M9201 selecteren.</span><span class="sxs-lookup"><span data-stu-id="806fa-113">If you’re using USMF you can select item M9201.</span></span>  
5. <span data-ttu-id="806fa-114">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="806fa-114">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="806fa-115">Als u artikel M9201 gebruikt, moet u minder dan 200 selecteren.</span><span class="sxs-lookup"><span data-stu-id="806fa-115">If you’re using item M9201, you need to select less than 200.</span></span>  
6. <span data-ttu-id="806fa-116">Schakel de uitbreiding van de sectie Voorraaddimensies om.</span><span class="sxs-lookup"><span data-stu-id="806fa-116">Toggle the expansion of the Inventory dimensions section.</span></span>
7. <span data-ttu-id="806fa-117">Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="806fa-117">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="806fa-118">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="806fa-118">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="806fa-119">Als u artikel M9201 gebruikt, kunt u magazijn 51 selecteren.</span><span class="sxs-lookup"><span data-stu-id="806fa-119">If you’re using item M9201, you can select warehouse 51.</span></span>  
9. <span data-ttu-id="806fa-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="806fa-120">Click Save.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="806fa-121">De voorwaarden van de voorraadblokkering bijwerken</span><span class="sxs-lookup"><span data-stu-id="806fa-121">Update the conditions of the inventory blocking</span></span>
1. <span data-ttu-id="806fa-122">Voer in het veld Hoeveelheid een getal in.</span><span class="sxs-lookup"><span data-stu-id="806fa-122">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="806fa-123">Werk het veld van de voorraadhoeveelheid bij om de te blokkeren hoeveelheid aan te geven.</span><span class="sxs-lookup"><span data-stu-id="806fa-123">Update the inventory quantity field to reflect the quantity to block.</span></span>  
2. <span data-ttu-id="806fa-124">Voer in het veld Verwachte datum een datum in.</span><span class="sxs-lookup"><span data-stu-id="806fa-124">In the Expected date field, enter a date.</span></span>
    * <span data-ttu-id="806fa-125">U kunt bijvoorbeeld aangeven wanneer de geblokkeerde voorraad naar verwachting beschikbaar komt voor reservering door een verwachte datum toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="806fa-125">You might want to indicate when the blocked inventory is expected to become available for reservation by assigning an expected date.</span></span> <span data-ttu-id="806fa-126">Als de optie Verwachte ontvangsten is geselecteerd voor de voorraadblokkering, zoals standaard het geval is wanneer u handmatig een blokkering uitvoert, wordt deze datum op de verwachte transactie weergegeven.</span><span class="sxs-lookup"><span data-stu-id="806fa-126">If the Expected receipts option is selected for the inventory blocking, as it is by default when you manually create a blocking, this date will appear on the expected transaction.</span></span>  
3. <span data-ttu-id="806fa-127">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="806fa-127">Click Save.</span></span>

## <a name="remove-the-inventory-blocking"></a><span data-ttu-id="806fa-128">De voorraadblokkering verwijderen</span><span class="sxs-lookup"><span data-stu-id="806fa-128">Remove the inventory blocking</span></span>
1. <span data-ttu-id="806fa-129">Klik op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="806fa-129">Click Delete.</span></span>
2. <span data-ttu-id="806fa-130">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="806fa-130">Click Yes.</span></span>
3. <span data-ttu-id="806fa-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="806fa-131">Close the page.</span></span>

