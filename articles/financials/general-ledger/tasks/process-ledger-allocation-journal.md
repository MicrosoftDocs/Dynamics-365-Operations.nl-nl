---
title: Grootboektoewijzingsjournaal verwerken
description: Gebruik de pagina Toewijzingsaanvraag verwerken om een toewijzingsjournaal te maken dat kan worden gecontroleerd en goedgekeurd voordat dit naar het grootboek wordt geboekt. Het toewijzingjournaal kan ook rechtstreeks naar het grootboek worden geboekt.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 087bd4f203e8762447e823b19076b79296a390d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846362"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="e786b-103">Grootboektoewijzingsjournaal verwerken</span><span class="sxs-lookup"><span data-stu-id="e786b-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e786b-104">Gebruik de pagina Toewijzingsaanvraag verwerken om een toewijzingsjournaal te maken dat kan worden gecontroleerd en goedgekeurd voordat dit naar het grootboek wordt geboekt. Het toewijzingjournaal kan ook rechtstreeks naar het grootboek worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="e786b-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="e786b-105">Voordat u een toewijzingsjournaal kunt maken, moet u minstens één actieve Grootboektoewijzingsregel maken.</span><span class="sxs-lookup"><span data-stu-id="e786b-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="e786b-106">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="e786b-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="e786b-107">Ga naar Grootboek > Toewijzingen > Toewijzingsaanvraag verwerken.</span><span class="sxs-lookup"><span data-stu-id="e786b-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="e786b-108">Klik in het veld Regel op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e786b-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e786b-109">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e786b-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="e786b-110">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="e786b-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e786b-111">Voer in het veld Begindatum een datum in.</span><span class="sxs-lookup"><span data-stu-id="e786b-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="e786b-112">De Begindatum is zeer belangrijk wanneer het Grootboek de Gegevensbron voor de regel is.</span><span class="sxs-lookup"><span data-stu-id="e786b-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="e786b-113">Deze datum bepaalt welke grootboeksaldi voor toewijzing worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="e786b-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="e786b-114">Selecteer Stoppen in het veld Nul bron.</span><span class="sxs-lookup"><span data-stu-id="e786b-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="e786b-115">Hierdoor wordt het toewijzingsproces gestopt en wordt een bericht weergegeven waarin wordt gemeld dat er een bronbedrag is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="e786b-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="e786b-116">Selecteer 'Alleen voorstel' in het veld Voorstelopties.</span><span class="sxs-lookup"><span data-stu-id="e786b-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="e786b-117">Selecteer Alleen voorstel om het resultaat in Toewijzingsjournalen te controleren en eventueel goed te keuren vóór het boeken van de toewijzing naar het Grootboek.</span><span class="sxs-lookup"><span data-stu-id="e786b-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="e786b-118">Voer in het veld Boekingsdatum GB een datum in.</span><span class="sxs-lookup"><span data-stu-id="e786b-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="e786b-119">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="e786b-119">Click OK.</span></span>
9. <span data-ttu-id="e786b-120">Ga naar Grootboek > Toewijzingen > Toewijzingsjournalen.</span><span class="sxs-lookup"><span data-stu-id="e786b-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="e786b-121">Klik op Regels.</span><span class="sxs-lookup"><span data-stu-id="e786b-121">Click Lines.</span></span>
11. <span data-ttu-id="e786b-122">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="e786b-122">Click Post.</span></span>
12. <span data-ttu-id="e786b-123">Klik op Boeken.</span><span class="sxs-lookup"><span data-stu-id="e786b-123">Click Post.</span></span>

