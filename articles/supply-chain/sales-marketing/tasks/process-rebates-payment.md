---
title: Kortingen voor betaling verwerken
description: Deze procedure demonstreert hoe u goedgekeurde en verwerkte klantkortingen converteert naar creditnota's.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 412e7df299a419642018a62e6e8febd5d59c65e1
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148440"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="bb2fc-103">Kortingen voor betaling verwerken</span><span class="sxs-lookup"><span data-stu-id="bb2fc-103">Process rebates for payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bb2fc-104">Deze procedure demonstreert hoe u goedgekeurde en verwerkte klantkortingen converteert naar creditnota's.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="bb2fc-105">U kunt deze begeleiding gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="bb2fc-106">De preconditie voor deze begeleiding is dat u een of meer kortingsclaims hebt met de status Markeren.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="bb2fc-107">Als u USMF gebruikt, moet u de begeleiding Klantkortingen genereren en verwerken uitvoeren voordat u deze begeleiding start.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-107">If you're using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="bb2fc-108">Kortingsclaims converteren naar een creditnota</span><span class="sxs-lookup"><span data-stu-id="bb2fc-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="bb2fc-109">Ga naar Alle klanten.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-109">Go to All customers.</span></span>
2. <span data-ttu-id="bb2fc-110">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="bb2fc-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="bb2fc-112">Klik in het actievenster op Incasso.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="bb2fc-113">Klik op Transacties vereffenen.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="bb2fc-114">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-114">Click Functions.</span></span>
7. <span data-ttu-id="bb2fc-115">Klik op Kortingsprogramma.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-115">Click Rebate program.</span></span>
    * <span data-ttu-id="bb2fc-116">De pagina Kortingen bevat de kortingsclaims die u hebt verwerkt in de klantkortingsworkbench en die de status Markeren hebben.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="bb2fc-117">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-117">Click Edit.</span></span>
    * <span data-ttu-id="bb2fc-118">Plaats vinkjes in het veld Markeren voor de claims die u wilt opnemen in de creditnota.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="bb2fc-119">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-119">Click Functions.</span></span>
10. <span data-ttu-id="bb2fc-120">Klik op Creditnota maken.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-120">Click Create credit note.</span></span>
    * <span data-ttu-id="bb2fc-121">Er wordt een bericht weergegeven dat aangeeft dat het journaal is geboekt. (Dit is het klantenverbruiksjournaal, zoals opgegeven op de pagina Parameters van module Klanten.)</span><span class="sxs-lookup"><span data-stu-id="bb2fc-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="bb2fc-122">Hierdoor wordt het echte creditbedrag verplaatst naar het saldo van de klant.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="bb2fc-123">Dat betekent dat de rekening van de klant is gecrediteerd en dat de kortingstoerekeningsrekening is gedebiteerd.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-123">This means that the customer's account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="bb2fc-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-124">Close the page.</span></span>
12. <span data-ttu-id="bb2fc-125">Klik op Annuleren.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-125">Click Cancel.</span></span>
    * <span data-ttu-id="bb2fc-126">Dit vernieuwt de pagina zodat u de updates kunt zien.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="bb2fc-127">Klik in het actievenster op Incasso.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="bb2fc-128">Klik op Transacties vereffenen.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="bb2fc-129">Merk op dat een transactie voor een negatief bedrag, die het totale kortingsbedrag vertegenwoordigt, zonder factuurreferentie is toegevoegd aan het klantsaldo.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="bb2fc-130">Klik op Annuleren.</span><span class="sxs-lookup"><span data-stu-id="bb2fc-130">Click Cancel.</span></span>

