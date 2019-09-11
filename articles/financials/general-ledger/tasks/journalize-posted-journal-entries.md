---
title: Geboekte journaalposten journaliseren
description: Deze procedure laat zien hoe u geboekte journaalposten journaliseert.
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e20229ca910aa0d7d820434c22edf5a27030bba5
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916248"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="ec217-103">Geboekte journaalposten journaliseren</span><span class="sxs-lookup"><span data-stu-id="ec217-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ec217-104">Deze procedure laat zien hoe u geboekte journaalposten journaliseert.</span><span class="sxs-lookup"><span data-stu-id="ec217-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="ec217-105">Deze procedure gebruikt het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="ec217-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="ec217-106">Ga in het **navigatievenster** naar **Modules > Grootboek > Grootboek instellen > Grootboekparameters**.</span><span class="sxs-lookup"><span data-stu-id="ec217-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="ec217-107">Het veld **Uitgebreid grootboekjournaal** kan worden ingesteld op Ja of Nee.</span><span class="sxs-lookup"><span data-stu-id="ec217-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="ec217-108">Als het is ingesteld op Ja, wordt andere rapportuitvoer aangemaakt.</span><span class="sxs-lookup"><span data-stu-id="ec217-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="ec217-109">Geef aan of de periode kan worden afgesloten als het journaalproces niet is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ec217-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="ec217-110">Als deze optie is ingesteld op Ja, kan een periode niet worden gesloten tot het journaalproces voor die periode is voltooid.</span><span class="sxs-lookup"><span data-stu-id="ec217-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="ec217-111">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ec217-111">Close the page.</span></span>
5. <span data-ttu-id="ec217-112">Ga in het **navigatievenster** naar **Modules > Grootboek > Periodieke taken > Journalisering**.</span><span class="sxs-lookup"><span data-stu-id="ec217-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="ec217-113">Klik op **Filter**.</span><span class="sxs-lookup"><span data-stu-id="ec217-113">Click **Filter**.</span></span>
7. <span data-ttu-id="ec217-114">Markeer de rij met de filtercriteria die u wilt definiëren.</span><span class="sxs-lookup"><span data-stu-id="ec217-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="ec217-115">Typ of selecteer de filtercriteria in het veld **Criteria**.</span><span class="sxs-lookup"><span data-stu-id="ec217-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="ec217-116">Klik op **OK** om de filterpagina te sluiten.</span><span class="sxs-lookup"><span data-stu-id="ec217-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="ec217-117">Klik op **OK** om het journaalproces te starten.</span><span class="sxs-lookup"><span data-stu-id="ec217-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="ec217-118">Een rapport wordt gegenereerd nadat het proces is voltooid.</span><span class="sxs-lookup"><span data-stu-id="ec217-118">A report will be generated after the process is complete.</span></span>  

