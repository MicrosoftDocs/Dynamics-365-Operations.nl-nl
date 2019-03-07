---
title: Onkostenbeleid definiëren
description: In Microsoft Dynamics 365 for Finance and Operations kunt u een beleid of regels definiëren waaraan uw werknemers zich moeten houden bij het invoeren en indienen van onkostennota's en reisopdrachten.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 04eaff110fea021ddee32be650be540894eb703b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "342426"
---
# <a name="expense-policies"></a><span data-ttu-id="b5882-103">Onkostenbeleid</span><span class="sxs-lookup"><span data-stu-id="b5882-103">Expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5882-104">U kunt beleid definiëren waaraan uw werknemers zich moeten houden bij het invoeren en indienen van onkostennota's en reisaanvragen.</span><span class="sxs-lookup"><span data-stu-id="b5882-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="b5882-105">Door het implementeren van onkostenbeleidsregels kunt u onkosten efficiënt beheren.</span><span class="sxs-lookup"><span data-stu-id="b5882-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="b5882-106">U kunt bijvoorbeeld een beleid instellen dat de onkosten voor een hotelovernachting in New York niet hoger mogen zijn dan USD 250.</span><span class="sxs-lookup"><span data-stu-id="b5882-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="b5882-107">Als een werknemer een onkostennota of een reisaanvraag indient waarin het tarief van de kamer dit bedrag overschrijdt, waarschuwt het systeem de</span><span class="sxs-lookup"><span data-stu-id="b5882-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="b5882-108">de werknemer dat het ingestelde bedrag voor de onkosten is overschreden.</span><span class="sxs-lookup"><span data-stu-id="b5882-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="b5882-109">U kunt het bericht dat de werknemer ontvangt, configureren bij het</span><span class="sxs-lookup"><span data-stu-id="b5882-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="b5882-110">definiëren van het beleid.</span><span class="sxs-lookup"><span data-stu-id="b5882-110">define the policy.</span></span>      
        
<span data-ttu-id="b5882-111">U kunt drie typen beleidsregels definiëren:</span><span class="sxs-lookup"><span data-stu-id="b5882-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="b5882-112">Waarschuwing – De werknemer mag een onkostennota of reisaanvraag indienen maar de onkosten worden gemarkeerd voor alle fiatteurs</span><span class="sxs-lookup"><span data-stu-id="b5882-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="b5882-113">en latere rapportage.</span><span class="sxs-lookup"><span data-stu-id="b5882-113">for later reporting.</span></span>        

- <span data-ttu-id="b5882-114">Fout – Vereist dat de werknemer de onkosten herziet om het beleid na te leven alvorens de onkostendeclaratie of reisopdracht wordt ingediend.</span><span class="sxs-lookup"><span data-stu-id="b5882-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
  - <span data-ttu-id="b5882-115">Verantwoording – Vereist dat de werknemer of een manager van een motivering opgeeft bedrag in het beleid te overschrijden alvorens de onkostennota of reisopdracht kan worden ingediend.</span><span class="sxs-lookup"><span data-stu-id="b5882-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        
 
  <span data-ttu-id="b5882-116">Het is ook mogelijk om te definiëren gedurende welk datumbereik de onkostenbeleidsregels geldig zijn.</span><span class="sxs-lookup"><span data-stu-id="b5882-116">You can also set up a date range for which expense policies are in effect.</span></span> <span data-ttu-id="b5882-117">Tijdens de piekperiode in de zomervakantie gelden bijvoorbeeld</span><span class="sxs-lookup"><span data-stu-id="b5882-117">For example, airline fares for flights between Denmark</span></span>      
  <span data-ttu-id="b5882-118">mogelijk hogere tarieven voor vluchten tussen Denemarken en New York.</span><span class="sxs-lookup"><span data-stu-id="b5882-118">and New York City can be expensive during the peak holiday travel season.</span></span> <span data-ttu-id="b5882-119">U kunt een regel definiëren dat voor ticketkosten naar New York een limiet</span><span class="sxs-lookup"><span data-stu-id="b5882-119">You can define a flight expense rule that restricts the</span></span>      
  <span data-ttu-id="b5882-120">van DKK 5000 geldt en u kunt opgeven dat deze regel geldt van 15 mei</span><span class="sxs-lookup"><span data-stu-id="b5882-120">cost of flights to New York City to a limit of DKK 5000, and you can specify that this rule be in effect between March 15 and</span></span>      
  <span data-ttu-id="b5882-121">tot 15 september.</span><span class="sxs-lookup"><span data-stu-id="b5882-121">September 15.</span></span>
