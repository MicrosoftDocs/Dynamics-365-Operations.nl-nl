---
title: Kortingen voor betaling verwerken
description: Deze procedure demonstreert hoe u goedgekeurde en verwerkte klantkortingen converteert naar creditnota's.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2e9af7167e4a4209b708d00493b8866f6d5f7e0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209922"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="597cf-103">Kortingen voor betaling verwerken</span><span class="sxs-lookup"><span data-stu-id="597cf-103">Process rebates for payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="597cf-104">Deze procedure demonstreert hoe u goedgekeurde en verwerkte klantkortingen converteert naar creditnota's.</span><span class="sxs-lookup"><span data-stu-id="597cf-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="597cf-105">U kunt deze begeleiding gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="597cf-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="597cf-106">De preconditie voor deze begeleiding is dat u een of meer kortingsclaims hebt met de status Markeren.</span><span class="sxs-lookup"><span data-stu-id="597cf-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="597cf-107">Als u USMF gebruikt, moet u de begeleiding Klantkortingen genereren en verwerken uitvoeren voordat u deze begeleiding start.</span><span class="sxs-lookup"><span data-stu-id="597cf-107">If you're using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="597cf-108">Kortingsclaims converteren naar een creditnota</span><span class="sxs-lookup"><span data-stu-id="597cf-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="597cf-109">Ga naar Alle klanten.</span><span class="sxs-lookup"><span data-stu-id="597cf-109">Go to All customers.</span></span>
2. <span data-ttu-id="597cf-110">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="597cf-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="597cf-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="597cf-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="597cf-112">Klik in het actievenster op Incasso.</span><span class="sxs-lookup"><span data-stu-id="597cf-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="597cf-113">Klik op Transacties vereffenen.</span><span class="sxs-lookup"><span data-stu-id="597cf-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="597cf-114">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="597cf-114">Click Functions.</span></span>
7. <span data-ttu-id="597cf-115">Klik op Kortingsprogramma.</span><span class="sxs-lookup"><span data-stu-id="597cf-115">Click Rebate program.</span></span>
    * <span data-ttu-id="597cf-116">De pagina Kortingen bevat de kortingsclaims die u hebt verwerkt in de klantkortingsworkbench en die de status Markeren hebben.</span><span class="sxs-lookup"><span data-stu-id="597cf-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="597cf-117">Klik op Bewerken.</span><span class="sxs-lookup"><span data-stu-id="597cf-117">Click Edit.</span></span>
    * <span data-ttu-id="597cf-118">Plaats vinkjes in het veld Markeren voor de claims die u wilt opnemen in de creditnota.</span><span class="sxs-lookup"><span data-stu-id="597cf-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="597cf-119">Klik op Functies.</span><span class="sxs-lookup"><span data-stu-id="597cf-119">Click Functions.</span></span>
10. <span data-ttu-id="597cf-120">Klik op Creditnota maken.</span><span class="sxs-lookup"><span data-stu-id="597cf-120">Click Create credit note.</span></span>
    * <span data-ttu-id="597cf-121">Er wordt een bericht weergegeven dat aangeeft dat het journaal is geboekt. (Dit is het klantenverbruiksjournaal, zoals opgegeven op de pagina Parameters van module Klanten.)</span><span class="sxs-lookup"><span data-stu-id="597cf-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="597cf-122">Hierdoor wordt het echte creditbedrag verplaatst naar het saldo van de klant.</span><span class="sxs-lookup"><span data-stu-id="597cf-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="597cf-123">Dat betekent dat de rekening van de klant is gecrediteerd en dat de kortingstoerekeningsrekening is gedebiteerd.</span><span class="sxs-lookup"><span data-stu-id="597cf-123">This means that the customer's account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="597cf-124">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="597cf-124">Close the page.</span></span>
12. <span data-ttu-id="597cf-125">Klik op Annuleren.</span><span class="sxs-lookup"><span data-stu-id="597cf-125">Click Cancel.</span></span>
    * <span data-ttu-id="597cf-126">Dit vernieuwt de pagina zodat u de updates kunt zien.</span><span class="sxs-lookup"><span data-stu-id="597cf-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="597cf-127">Klik in het actievenster op Incasso.</span><span class="sxs-lookup"><span data-stu-id="597cf-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="597cf-128">Klik op Transacties vereffenen.</span><span class="sxs-lookup"><span data-stu-id="597cf-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="597cf-129">Merk op dat een transactie voor een negatief bedrag, die het totale kortingsbedrag vertegenwoordigt, zonder factuurreferentie is toegevoegd aan het klantsaldo.</span><span class="sxs-lookup"><span data-stu-id="597cf-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="597cf-130">Klik op Annuleren.</span><span class="sxs-lookup"><span data-stu-id="597cf-130">Click Cancel.</span></span>

