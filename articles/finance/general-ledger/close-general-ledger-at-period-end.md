---
title: Het grootboek aan het einde van de periode afsluiten
description: In dit onderwerp worden de taken beschreven die meestal worden uitgevoerd bij het uitvoeren van een periodeafsluiting voor het grootboek.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5cabdce5e23704fbf12e631a138235174ebc5772
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441958"
---
# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="f38e9-103">Het grootboek aan het einde van de periode afsluiten</span><span class="sxs-lookup"><span data-stu-id="f38e9-103">Close the general ledger at period end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f38e9-104">In dit onderwerp worden de taken beschreven die meestal worden uitgevoerd bij het uitvoeren van een periodeafsluiting voor het grootboek.</span><span class="sxs-lookup"><span data-stu-id="f38e9-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="f38e9-105">In het grootboek kunt u afsluitingsprocedures voor een periode of een jaar uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="f38e9-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="f38e9-106">Afsluitingsprocessen bereiden het systeem voor op een nieuwe periode.</span><span class="sxs-lookup"><span data-stu-id="f38e9-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="f38e9-107">Als u het systeem op een nieuw jaar wilt voorbereiden, moet u het jaarafsluitingsproces uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="f38e9-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="f38e9-108">Elke organisatie kent verschillende processen en de stappen die worden uitgevoerd voor het einde van een periode.</span><span class="sxs-lookup"><span data-stu-id="f38e9-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="f38e9-109">Hieronder staan enkele optionele stappen voor periodeafsluitingen:</span><span class="sxs-lookup"><span data-stu-id="f38e9-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="f38e9-110">Voer alle taken voor alle overige modules uit, zoals Klanten, Leveranciers en Voorraad.</span><span class="sxs-lookup"><span data-stu-id="f38e9-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="f38e9-111">Controleer of alle journalen zijn geboekt.</span><span class="sxs-lookup"><span data-stu-id="f38e9-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="f38e9-112">Voer herwaardering van vreemde valuta uit om eventuele niet-gerealiseerde winst- of verliesbedragen te genereren.</span><span class="sxs-lookup"><span data-stu-id="f38e9-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="f38e9-113">Vereffen transacties voor elke grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="f38e9-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="f38e9-114">Verwerk alle vereiste toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="f38e9-114">Process any required allocations.</span></span>
-   <span data-ttu-id="f38e9-115">Boek handmatig periode-eindecorrecties.</span><span class="sxs-lookup"><span data-stu-id="f38e9-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="f38e9-116">Journaliseer transacties en controleer het **Grootboekjournaal** rapport.</span><span class="sxs-lookup"><span data-stu-id="f38e9-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="f38e9-117">Voer een consolidatie uit met behulp van een consolidatiebedrijf of een financiële rapportage.</span><span class="sxs-lookup"><span data-stu-id="f38e9-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="f38e9-118">Genereer financiële overzichten van het periode-einde met behulp van financiële rapportage.</span><span class="sxs-lookup"><span data-stu-id="f38e9-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="f38e9-119">Stel grootboekperioden in op **In wachtstand**, zodat geen verdere boeking plaatsvindt.</span><span class="sxs-lookup"><span data-stu-id="f38e9-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="f38e9-120">Voor een beter beheer kunt u een periode ook beperken tot een specifieke gebruikersgroep terwijl periode-eindeactiviteiten plaatsvinden.</span><span class="sxs-lookup"><span data-stu-id="f38e9-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="f38e9-121">Het is geen goed idee om perioden in te stellen op **Definitief afgesloten**, omdat u een periode die is afgesloten niet kunt heropenen.</span><span class="sxs-lookup"><span data-stu-id="f38e9-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="f38e9-122">De werkruimte Afgesloten financiële periode kan worden gebruikt om de taken die nodig zijn voor verschillende periodeafsluitingsprocessen te organiseren en bij te houden.</span><span class="sxs-lookup"><span data-stu-id="f38e9-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="f38e9-123">Zie de volgende onderwerpen voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f38e9-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="f38e9-124">Werkgebied voor afsluiten van financiële periode</span><span class="sxs-lookup"><span data-stu-id="f38e9-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="f38e9-125">Jaarafsluiting</span><span class="sxs-lookup"><span data-stu-id="f38e9-125">Year-end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="f38e9-126">Massale sluiting van financiële periode</span><span class="sxs-lookup"><span data-stu-id="f38e9-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)




