---
title: Onkostenbeleid definiëren
description: In Microsoft Dynamics 365 Finance kunt u een beleid of regels definiëren waaraan uw werknemers zich moeten houden bij het invoeren en indienen van onkostennota's en reisopdrachten.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 22504e0e26c025d117f29dee3b59b41d508e7724
ms.sourcegitcommit: 4f90b9ddedf312e75a714e0ec7f7ee5fd43cac6a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/21/2020
ms.locfileid: "3389710"
---
# <a name="define-expense-policies"></a><span data-ttu-id="786a1-103">Onkostenbeleid definiëren</span><span class="sxs-lookup"><span data-stu-id="786a1-103">Define expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="786a1-104">U kunt beleid definiëren waaraan uw werknemers zich moeten houden bij het invoeren en indienen van onkostennota's en reisaanvragen.</span><span class="sxs-lookup"><span data-stu-id="786a1-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="786a1-105">Door het implementeren van onkostenbeleidsregels kunt u onkosten efficiënt beheren.</span><span class="sxs-lookup"><span data-stu-id="786a1-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="786a1-106">U kunt bijvoorbeeld een beleid instellen dat de onkosten voor een hotelovernachting in New York niet hoger mogen zijn dan USD 250.</span><span class="sxs-lookup"><span data-stu-id="786a1-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="786a1-107">Als een werknemer een onkostennota of een reisaanvraag indient waarin het tarief van de kamer dit bedrag overschrijdt, waarschuwt het systeem de</span><span class="sxs-lookup"><span data-stu-id="786a1-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="786a1-108">de werknemer dat het ingestelde bedrag voor de onkosten is overschreden.</span><span class="sxs-lookup"><span data-stu-id="786a1-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="786a1-109">U kunt het bericht dat de werknemer ontvangt, configureren bij het</span><span class="sxs-lookup"><span data-stu-id="786a1-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="786a1-110">definiëren van het beleid.</span><span class="sxs-lookup"><span data-stu-id="786a1-110">define the policy.</span></span>      
        
<span data-ttu-id="786a1-111">U kunt drie typen beleidsregels definiëren:</span><span class="sxs-lookup"><span data-stu-id="786a1-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="786a1-112">Waarschuwing – De werknemer mag een onkostennota of reisaanvraag indienen maar de onkosten worden gemarkeerd voor alle fiatteurs</span><span class="sxs-lookup"><span data-stu-id="786a1-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="786a1-113">en latere rapportage.</span><span class="sxs-lookup"><span data-stu-id="786a1-113">for later reporting.</span></span>        

- <span data-ttu-id="786a1-114">Fout – Vereist dat de werknemer de onkosten herziet om het beleid na te leven alvorens de onkostendeclaratie of reisopdracht wordt ingediend.</span><span class="sxs-lookup"><span data-stu-id="786a1-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="786a1-115">Verantwoording – Vereist dat de werknemer of een manager van een motivering opgeeft bedrag in het beleid te overschrijden alvorens de onkostennota of reisopdracht kan worden ingediend.</span><span class="sxs-lookup"><span data-stu-id="786a1-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="786a1-116">Beleidstips</span><span class="sxs-lookup"><span data-stu-id="786a1-116">Policy tips</span></span>
<span data-ttu-id="786a1-117">Hier volgen enkele suggesties die u kunnen helpen bij het maken van nieuw beleid voor onkostenbeheer.</span><span class="sxs-lookup"><span data-stu-id="786a1-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="786a1-118">Beleid heeft een ingangsdatum en wordt niet van kracht als het beleid wordt gemaakt met een datum na de datum waarop de onkosten zijn gemaakt.</span><span class="sxs-lookup"><span data-stu-id="786a1-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="786a1-119">Als u bijvoorbeeld vandaag een nieuw beleid maakt om de maximale maaltijdkosten van $ 50 af te dwingen, worden eventuele bestaande onkosten tot en met gisteren die zijn ingevoerd niet gecontroleerd aan de hand van dit beleid.</span><span class="sxs-lookup"><span data-stu-id="786a1-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="786a1-120">Wanneer u een beleid maakt voor een onkostencategorie die kan worden gespecificeerd, kunt u overwegen een voorwaarde toe te voegen voor het type onkostenregel.</span><span class="sxs-lookup"><span data-stu-id="786a1-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="786a1-121">Sommige beleidsregels, zoals het vereisen van een ontvangstbon, zijn mogelijk niet zinvol voor gespecificeerde regels en mogen alleen worden toegepast op de koptekstregel of een niet-gespecificeerde regel.</span><span class="sxs-lookup"><span data-stu-id="786a1-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="786a1-122">Beleid voor onkostenbeheer wordt standaard geëvalueerd op basis van de bronentiteit.</span><span class="sxs-lookup"><span data-stu-id="786a1-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="786a1-123">Voor intercompany-scenario's kunt u het beleid zo instellen dat het wordt geëvalueerd ten opzichte van de bestemmingsentiteit (lenende entiteit).</span><span class="sxs-lookup"><span data-stu-id="786a1-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="786a1-124">Als u de beleidsregels wilt uitvoeren op basis van de doelentiteit, schakelt u de functie "Onkostenbeleid evalueren op basis van lenende rechtspersoon" in het werkgebied **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="786a1-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="786a1-125">Wanneer u beleid moet evalueren</span><span class="sxs-lookup"><span data-stu-id="786a1-125">When to evaluate policies</span></span>

<span data-ttu-id="786a1-126">In parameters voor onkostenbeheer is er een optie waarmee u beleid voor onkostenbeheer kunt beoordelen wanneer een regel wordt opgeslagen of wanneer een onkostennota wordt ingediend.</span><span class="sxs-lookup"><span data-stu-id="786a1-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="786a1-127">Als u ervoor kiest om te beoordelen wanneer een regel wordt opgeslagen, zorgt u ervoor dat gebruikers eerder zicht hebben op wat zij moeten doen om hun onkostennota in één keer te voltooien.</span><span class="sxs-lookup"><span data-stu-id="786a1-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="786a1-128">Anders kunt u beleidsevaluatie uitstellen en tijd besparen als u de validatie uitvoert aan het einde, tijdens de indiening bij de werkstroom.</span><span class="sxs-lookup"><span data-stu-id="786a1-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
