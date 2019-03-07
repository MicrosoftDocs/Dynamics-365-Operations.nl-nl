---
title: Geboekte journaalposten journaliseren
description: Deze procedure laat zien hoe u geboekte journaalposten journaliseert.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b50809cf9eb59475856f91d9f1ddfe28ecfd8de6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "318529"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="d00b9-103">Geboekte journaalposten journaliseren</span><span class="sxs-lookup"><span data-stu-id="d00b9-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d00b9-104">Deze procedure laat zien hoe u geboekte journaalposten journaliseert.</span><span class="sxs-lookup"><span data-stu-id="d00b9-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="d00b9-105">Deze procedure gebruikt het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="d00b9-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="d00b9-106">Valideer de instellingen voor het journaliseren onder Grootboek > Grootboek instellen > Grootboekparameters.</span><span class="sxs-lookup"><span data-stu-id="d00b9-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="d00b9-107">Het veld Uitgebreid grootboekjournaal kan worden ingesteld op Ja of Nee.</span><span class="sxs-lookup"><span data-stu-id="d00b9-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="d00b9-108">Als het is ingesteld op Ja, wordt andere rapportuitvoer aangemaakt.</span><span class="sxs-lookup"><span data-stu-id="d00b9-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="d00b9-109">Geef aan of de periode kan worden afgesloten als het journaalproces niet is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d00b9-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="d00b9-110">Als deze optie is ingesteld op Ja, kan een periode niet worden gesloten tot het journaalproces voor die periode is voltooid.</span><span class="sxs-lookup"><span data-stu-id="d00b9-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="d00b9-111">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d00b9-111">Close the page.</span></span>
5. <span data-ttu-id="d00b9-112">Ga naar Grootboek > Periodieke taken > Journalisering.</span><span class="sxs-lookup"><span data-stu-id="d00b9-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="d00b9-113">Klik op Filter.</span><span class="sxs-lookup"><span data-stu-id="d00b9-113">Click Filter.</span></span>
7. <span data-ttu-id="d00b9-114">Markeer de rij met de filtercriteria die u wilt definiëren.</span><span class="sxs-lookup"><span data-stu-id="d00b9-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="d00b9-115">Typ of selecteer de filtercriteria in het veld Criteria.</span><span class="sxs-lookup"><span data-stu-id="d00b9-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="d00b9-116">Klik op OK om de filterpagina te sluiten.</span><span class="sxs-lookup"><span data-stu-id="d00b9-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="d00b9-117">Klik op OK om het journaalproces te starten.</span><span class="sxs-lookup"><span data-stu-id="d00b9-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="d00b9-118">Een rapport wordt gegenereerd nadat het proces is voltooid.</span><span class="sxs-lookup"><span data-stu-id="d00b9-118">A report will be generated after the process is complete.</span></span>  

