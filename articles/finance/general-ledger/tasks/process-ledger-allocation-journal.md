---
title: Grootboektoewijzingsjournaal verwerken
description: In dit onderwerp wordt uitgelegd hoe u een toewijzingsaanvraag in Dynamics 365 Finance kunt verwerken.
author: aprilolson
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e89aa21f988d50bc1a922e053be0ff2dcd196268
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834406"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="928ed-103">Grootboektoewijzingsjournaal verwerken</span><span class="sxs-lookup"><span data-stu-id="928ed-103">Process ledger allocation journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="928ed-104">In dit onderwerp wordt uitgelegd hoe u een toewijzingsaanvraag kunt verwerken.</span><span class="sxs-lookup"><span data-stu-id="928ed-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="928ed-105">Gebruik de pagina Toewijzingsaanvraag verwerken om een toewijzingsjournaal te maken dat kan worden gecontroleerd en goedgekeurd voordat dit naar het grootboek wordt geboekt. Het toewijzingjournaal kan ook rechtstreeks naar het grootboek worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="928ed-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="928ed-106">Voordat u een toewijzingsjournaal kunt maken, moet u minstens één actieve Grootboektoewijzingsregel maken.</span><span class="sxs-lookup"><span data-stu-id="928ed-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="928ed-107">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="928ed-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="928ed-108">Ga in het navigatievenster naar **Modules > Grootboek > Toewijzingen > Toewijzingsaanvraag verwerken**.</span><span class="sxs-lookup"><span data-stu-id="928ed-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="928ed-109">Selecteer in het veld **Regel** de gewenste record in het vervolgkeuzemenu.</span><span class="sxs-lookup"><span data-stu-id="928ed-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="928ed-110">Voer in het veld **Begindatum** een datum in.</span><span class="sxs-lookup"><span data-stu-id="928ed-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="928ed-111">De **Begindatum** is zeer belangrijk wanneer het Grootboek de Gegevensbron voor de regel is.</span><span class="sxs-lookup"><span data-stu-id="928ed-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="928ed-112">Deze datum bepaalt welke grootboeksaldi voor toewijzing worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="928ed-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="928ed-113">Selecteer **Stoppen** in het veld **Nul bron**.</span><span class="sxs-lookup"><span data-stu-id="928ed-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="928ed-114">Hierdoor wordt het toewijzingsproces gestopt en wordt een bericht weergegeven waarin wordt gemeld dat er een bronbedrag is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="928ed-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="928ed-115">Selecteer **Alleen voorstel** in het veld **Voorstelopties**.</span><span class="sxs-lookup"><span data-stu-id="928ed-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="928ed-116">Selecteer **Alleen voorstel** om het resultaat in Toewijzingsjournalen te controleren en eventueel goed te keuren vóór het boeken van de toewijzing naar het Grootboek.</span><span class="sxs-lookup"><span data-stu-id="928ed-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="928ed-117">Voer in het veld Boekingsdatum GB een datum in.</span><span class="sxs-lookup"><span data-stu-id="928ed-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="928ed-118">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="928ed-118">Select **OK**.</span></span>
7. <span data-ttu-id="928ed-119">Ga in het navigatievenster naar **Modules > Grootboek > Toewijzingen > Toewijzingsjournalen**.</span><span class="sxs-lookup"><span data-stu-id="928ed-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="928ed-120">Selecteer **Regels**</span><span class="sxs-lookup"><span data-stu-id="928ed-120">Select **Lines**.</span></span>
9. <span data-ttu-id="928ed-121">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="928ed-121">Select **Post**.</span></span>
10. <span data-ttu-id="928ed-122">Selecteer **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="928ed-122">Select **Post**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]