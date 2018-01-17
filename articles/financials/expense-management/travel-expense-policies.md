---
title: "Onkostenbeleid definiëren"
description: "U kunt onkostenbeleid definiëren waaraan uw werknemers zich moeten houden bij het invoeren en indienen van onkostennota's en reisaanvragen in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: saraschi2
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicyListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: b0f9a5ca275944aeb27798a2f3377356319589c7
ms.contentlocale: nl-nl
ms.lasthandoff: 01/17/2018

---

# <a name="expense-policies"></a><span data-ttu-id="125a1-103">Onkostenbeleid</span><span class="sxs-lookup"><span data-stu-id="125a1-103">Expense policies</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="125a1-104">U kunt beleid definiëren waaraan uw werknemers zich moeten houden bij het invoeren en indienen van onkostennota's en reisaanvragen.</span><span class="sxs-lookup"><span data-stu-id="125a1-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span> <span data-ttu-id="125a1-105">Door het implementeren van onkostenbeleidsregels kunt u onkosten efficiënt beheren.</span><span class="sxs-lookup"><span data-stu-id="125a1-105">Implementing expense policies can help you manage expenses effectively.</span></span> 

<span data-ttu-id="125a1-106">U kunt bijvoorbeeld een beleid instellen dat de onkosten voor een hotelovernachting in New York niet hoger mogen zijn dan USD 250.</span><span class="sxs-lookup"><span data-stu-id="125a1-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span> <span data-ttu-id="125a1-107">Een werknemer die een onkostennota of reisaanvraag met een hotelovernachting boven dit bedrag indient, wordt door het systeem gewaarschuwd dat het in het beleid ingestelde maximumbedrag wordt overschreden.</span><span class="sxs-lookup"><span data-stu-id="125a1-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="125a1-108">U kunt het bericht dat de werknemer ontvangt, configureren bij het definiëren van het beleid.</span><span class="sxs-lookup"><span data-stu-id="125a1-108">You can configure the message that the worker will receive when you define the policy.</span></span> 

<span data-ttu-id="125a1-109">U kunt drie typen beleidsregels definiëren:</span><span class="sxs-lookup"><span data-stu-id="125a1-109">You can define three types of policies:</span></span> 

 - <span data-ttu-id="125a1-110">Waarschuwing – De werknemer mag een onkostennota of reisaanvraag indienen maar de onkosten worden gemarkeerd voor alle fiatteurs</span><span class="sxs-lookup"><span data-stu-id="125a1-110">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>  
 <span data-ttu-id="125a1-111">en latere rapportage.</span><span class="sxs-lookup"><span data-stu-id="125a1-111">for later reporting.</span></span> 
 - <span data-ttu-id="125a1-112">Fout – Vereist dat de werknemer de onkosten herziet om het beleid na te leven alvorens de onkostendeclaratie of reisopdracht wordt ingediend.</span><span class="sxs-lookup"><span data-stu-id="125a1-112">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span> 
 - <span data-ttu-id="125a1-113">Verantwoording – Vereist dat de werknemer of een manager van een motivering opgeeft bedrag in het beleid te overschrijden alvorens de onkostennota of reisopdracht kan worden ingediend.</span><span class="sxs-lookup"><span data-stu-id="125a1-113">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span> 

<span data-ttu-id="125a1-114">Het is ook mogelijk om te definiëren gedurende welk datumbereik de onkostenbeleidsregels geldig zijn.</span><span class="sxs-lookup"><span data-stu-id="125a1-114">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="125a1-115">Tijdens de piekperiode in de zomervakantie gelden bijvoorbeeld mogelijk hogere tarieven voor vluchten tussen Denemarken en New York.</span><span class="sxs-lookup"><span data-stu-id="125a1-115">For example, airline fares for flights between Denmark and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="125a1-116">U kunt een regel definiëren dat voor ticketkosten naar New York een limiet van DKK 5000 geldt en u kunt opgeven dat deze regel geldt van 15 mei tot 15 september.</span><span class="sxs-lookup"><span data-stu-id="125a1-116">You can define a flight expense rule that restricts the cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and September 15.</span></span> 

