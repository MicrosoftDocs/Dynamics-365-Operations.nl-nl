---
title: Een voorraadblokkering maken en beheren
description: In dit onderwerp wordt beschreven hoe u met een voorraadblokkering voorkomt dat fysieke voorhanden voorraad wordt gereserveerd door andere uitgaande brondocumenten.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventBlocking, InventItemIdLookupSimple, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e9aa38ca52da577fff258bb330922ad7f4044330
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956153"
---
# <a name="create-and-maintain-an-inventory-blocking"></a><span data-ttu-id="f33c8-103">Een voorraadblokkering maken en beheren</span><span class="sxs-lookup"><span data-stu-id="f33c8-103">Create and maintain an inventory blocking</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f33c8-104">In dit onderwerp wordt beschreven hoe u met een voorraadblokkering voorkomt dat fysieke voorhanden voorraad wordt gereserveerd door andere uitgaande brondocumenten.</span><span class="sxs-lookup"><span data-stu-id="f33c8-104">This topic describes how to use an inventory blocking to prevent physical on-hand inventory from being reserved by other outbound source documents.</span></span> <span data-ttu-id="f33c8-105">Voordat u met deze procedure begint, moet u een artikel met fysieke, beschikbare voorhanden voorraad hebben.</span><span class="sxs-lookup"><span data-stu-id="f33c8-105">Before you start the procedures in this topic, you must have an item that physical on-hand inventory is available for.</span></span>

## <a name="block-inventory"></a><span data-ttu-id="f33c8-106">Voorraad blokkeren</span><span class="sxs-lookup"><span data-stu-id="f33c8-106">Block inventory</span></span>

<span data-ttu-id="f33c8-107">Volg deze stappen om een voorraadblokkeringsrecord te maken zodat voorraad wordt geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="f33c8-107">To create an inventory blocking record so that inventory is blocked, follow these steps.</span></span>

1. <span data-ttu-id="f33c8-108">Ga naar **Voorraadbeheer \> Periodieke taken \> Voorraadblokkering**.</span><span class="sxs-lookup"><span data-stu-id="f33c8-108">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="f33c8-109">Selecteer **Nieuw** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="f33c8-109">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="f33c8-110">Stel in de header van de nieuwe blokkeringsrecord het veld **Artikelnummer** in op het artikel dat u wilt blokkeren en voer een beschrijving in.</span><span class="sxs-lookup"><span data-stu-id="f33c8-110">On the header of the new blocking record, set the **Item number** field to the item that you want to block, and enter a description.</span></span>
1. <span data-ttu-id="f33c8-111">Typ op het sneltabblad **Algemeen** in het veld **Hoeveelheid** het aantal in dat u wilt blokkeren van het artikel.</span><span class="sxs-lookup"><span data-stu-id="f33c8-111">On the **General** FastTab, in the **Quantity** field, enter the number of items to block.</span></span>
1. <span data-ttu-id="f33c8-112">Geef op het sneltabblad **Voorraaddimensies** de locatie en het magazijn op waar de artikelen zich momenteel bevinden die u wilt blokkeren.</span><span class="sxs-lookup"><span data-stu-id="f33c8-112">On the **Inventory dimensions** FastTab, specify the site and warehouse where the items that you want to block are currently located.</span></span>
1. <span data-ttu-id="f33c8-113">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="f33c8-113">On the Action Pane, select **Save**.</span></span>

## <a name="update-the-conditions-of-the-inventory-blocking"></a><span data-ttu-id="f33c8-114">De voorwaarden van de voorraadblokkering bijwerken</span><span class="sxs-lookup"><span data-stu-id="f33c8-114">Update the conditions of the inventory blocking</span></span>

<span data-ttu-id="f33c8-115">Volg deze stappen om een voorraadblokkeringsrecord bij te werken.</span><span class="sxs-lookup"><span data-stu-id="f33c8-115">To update an inventory blocking record, follow these steps.</span></span>

1. <span data-ttu-id="f33c8-116">Ga naar **Voorraadbeheer \> Periodieke taken \> Voorraadblokkering**.</span><span class="sxs-lookup"><span data-stu-id="f33c8-116">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="f33c8-117">Selecteer in het lijstvenster de betreffende blokkeringsrecord.</span><span class="sxs-lookup"><span data-stu-id="f33c8-117">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="f33c8-118">Bewerk de record waar nodig.</span><span class="sxs-lookup"><span data-stu-id="f33c8-118">Edit the record as required.</span></span> <span data-ttu-id="f33c8-119">U kunt bijvoorbeeld de waarde van het veld **Verwachte datum** wijzigen om aan te geven wanneer de geblokkeerde voorraad naar verwachting beschikbaar komt voor reservering.</span><span class="sxs-lookup"><span data-stu-id="f33c8-119">For example, you might change the value of the **Expected date** field to indicate when the blocked inventory is expected to become available for reservation.</span></span> <span data-ttu-id="f33c8-120">Als de optie **Verwachte ontvangsten** is geselecteerd, wordt de datum bij de verwachte transactie weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f33c8-120">If the **Expected receipts** option is selected, the date will appear on the expected transaction.</span></span> <span data-ttu-id="f33c8-121">(De optie **Verwachte ontvangsten** is standaard geselecteerd wanneer u handmatig een blokkeringsrecord maakt.)</span><span class="sxs-lookup"><span data-stu-id="f33c8-121">(The **Expected receipts** option is selected by default when you manually create a blocking record.)</span></span>
1. <span data-ttu-id="f33c8-122">Selecteer **Opslaan** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="f33c8-122">On the Action Pane, select **Save**.</span></span>

## <a name="unblock-inventory"></a><span data-ttu-id="f33c8-123">Voorraad deblokkeren</span><span class="sxs-lookup"><span data-stu-id="f33c8-123">Unblock inventory</span></span>

<span data-ttu-id="f33c8-124">Volg deze stappen om een voorraadblokkeringsrecord te verwijderen, zodat voorraad wordt vrijgegeven.</span><span class="sxs-lookup"><span data-stu-id="f33c8-124">To remove an inventory blocking record so that inventory is unblocked, follow these steps.</span></span>

1. <span data-ttu-id="f33c8-125">Ga naar **Voorraadbeheer \> Periodieke taken \> Voorraadblokkering**.</span><span class="sxs-lookup"><span data-stu-id="f33c8-125">Go to **Inventory management \> Periodic tasks \> Inventory blocking**.</span></span>
1. <span data-ttu-id="f33c8-126">Selecteer in het lijstvenster de betreffende blokkeringsrecord.</span><span class="sxs-lookup"><span data-stu-id="f33c8-126">In the list pane, select the relevant blocking record.</span></span>
1. <span data-ttu-id="f33c8-127">Selecteer in het actievenster **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="f33c8-127">On the Action Pane, select **Delete**.</span></span>
1. <span data-ttu-id="f33c8-128">U wordt gevraagd om de bewerking te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="f33c8-128">You're prompted to confirm the operation.</span></span> <span data-ttu-id="f33c8-129">Selecteer **Ja** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="f33c8-129">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="f33c8-130">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f33c8-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
