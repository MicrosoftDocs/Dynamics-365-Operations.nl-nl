--- 
title: Kortingen voor betaling verwerken
description: Deze procedure demonstreert hoe u goedgekeurde en verwerkte klantkortingen converteert naar creditnota's.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b2d97a59ae782af0a3d5ab71903961ef244a8e62
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="117f2-103">Kortingen voor betaling verwerken</span><span class="sxs-lookup"><span data-stu-id="117f2-103">Process rebates for payment</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="117f2-104">Deze procedure demonstreert hoe u goedgekeurde en verwerkte klantkortingen converteert naar creditnota's.</span><span class="sxs-lookup"><span data-stu-id="117f2-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="117f2-105">U kunt deze begeleiding gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="117f2-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="117f2-106">De preconditie voor deze begeleiding is dat u een of meer kortingsclaims hebt met de status Markeren.</span><span class="sxs-lookup"><span data-stu-id="117f2-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="117f2-107">Als u USMF gebruikt, moet u de begeleiding 'Klantkortingen genereren en verwerken' uitvoeren voordat u deze begeleiding start.</span><span class="sxs-lookup"><span data-stu-id="117f2-107">If you’re using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="117f2-108">Kortingsclaims converteren naar een creditnota</span><span class="sxs-lookup"><span data-stu-id="117f2-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="117f2-109">Ga naar Alle klanten.</span><span class="sxs-lookup"><span data-stu-id="117f2-109">Go to All customers.</span></span>
2. <span data-ttu-id="117f2-110">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="117f2-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="117f2-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="117f2-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="117f2-112">Klik in het actievenster op Incasso.</span><span class="sxs-lookup"><span data-stu-id="117f2-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="117f2-113">Klik op Transacties vereffenen.</span><span class="sxs-lookup"><span data-stu-id="117f2-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="117f2-114">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="117f2-114">Click Functions.</span></span>
7. <span data-ttu-id="117f2-115">Klik op Kortingsprogramma.</span><span class="sxs-lookup"><span data-stu-id="117f2-115">Click Rebate program.</span></span>
    * <span data-ttu-id="117f2-116">De pagina Kortingen bevat de kortingsclaims die u hebt verwerkt in de klantkortingsworkbench en die de status Markeren hebben.</span><span class="sxs-lookup"><span data-stu-id="117f2-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="117f2-117">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="117f2-117">Click Edit.</span></span>
    * <span data-ttu-id="117f2-118">Plaats vinkjes in het veld Markeren voor de claims die u wilt opnemen in de creditnota.</span><span class="sxs-lookup"><span data-stu-id="117f2-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="117f2-119">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="117f2-119">Click Functions.</span></span>
10. <span data-ttu-id="117f2-120">Klik op Creditnota maken.</span><span class="sxs-lookup"><span data-stu-id="117f2-120">Click Create credit note.</span></span>
    * <span data-ttu-id="117f2-121">Er wordt een bericht weergegeven dat aangeeft dat het journaal is geboekt. (Dit is het klantenverbruiksjournaal, zoals opgegeven op de pagina Parameters van module Klanten.)</span><span class="sxs-lookup"><span data-stu-id="117f2-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="117f2-122">Hierdoor wordt het echte creditbedrag verplaatst naar het saldo van de klant.</span><span class="sxs-lookup"><span data-stu-id="117f2-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="117f2-123">Dat betekent dat de rekening van de klant is gecrediteerd en dat de kortingstoerekeningsrekening is gedebiteerd.</span><span class="sxs-lookup"><span data-stu-id="117f2-123">This means that the customer’s account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="117f2-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="117f2-124">Close the page.</span></span>
12. <span data-ttu-id="117f2-125">Klik op Annuleren.</span><span class="sxs-lookup"><span data-stu-id="117f2-125">Click Cancel.</span></span>
    * <span data-ttu-id="117f2-126">Dit vernieuwt de pagina zodat u de updates kunt zien.</span><span class="sxs-lookup"><span data-stu-id="117f2-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="117f2-127">Klik in het actievenster op Incasso.</span><span class="sxs-lookup"><span data-stu-id="117f2-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="117f2-128">Klik op Transacties vereffenen.</span><span class="sxs-lookup"><span data-stu-id="117f2-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="117f2-129">Merk op dat een transactie voor een negatief bedrag, die het totale kortingsbedrag vertegenwoordigt, zonder factuurreferentie is toegevoegd aan het klantsaldo.</span><span class="sxs-lookup"><span data-stu-id="117f2-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="117f2-130">Klik op Annuleren.</span><span class="sxs-lookup"><span data-stu-id="117f2-130">Click Cancel.</span></span>


