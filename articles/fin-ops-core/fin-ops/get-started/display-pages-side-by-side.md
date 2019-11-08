---
title: Pagina's naast elkaar weergeven met de functie Openen in nieuw venster
description: In dit artikel wordt uitgelegd hoe u pagina's naast elkaar kunt weergeven.
author: aneesmsft
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7144f26c0977fbc420b804728151262b2f166bc0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180686"
---
# <a name="show-pages-side-by-side-by-using-the-open-in-new-window-feature"></a><span data-ttu-id="d41d4-103">Pagina's naast elkaar weergeven met de functie Openen in nieuw venster</span><span class="sxs-lookup"><span data-stu-id="d41d4-103">Show pages side by side by using the Open in new window feature</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d41d4-104">In dit artikel wordt uitgelegd hoe u pagina's naast elkaar kunt weergeven.</span><span class="sxs-lookup"><span data-stu-id="d41d4-104">This article explains how to display pages side-by-side.</span></span>

<span data-ttu-id="d41d4-105">U kunt meerdere pagina's naast elkaar bekijken om taken snel te voltooien.</span><span class="sxs-lookup"><span data-stu-id="d41d4-105">You may want to view multiple pages side-by-side to complete tasks quickly.</span></span> <span data-ttu-id="d41d4-106">Als voorbeeld kunt u regels in meer dan één journaal bijvoorbeeld valideren of invoeren.</span><span class="sxs-lookup"><span data-stu-id="d41d4-106">As an example, you might want to validate or enter lines in more than one journal.</span></span> <span data-ttu-id="d41d4-107">Doorgaans, om dit te doen moet u vooruit en terug gaan naar de pagina die een lijst met journalen weergeeft, en de pagina die regels voor een bepaald journaal weergeeft.</span><span class="sxs-lookup"><span data-stu-id="d41d4-107">Typically, to do this you would have to go back and forth between the page that displays a list of journals, and the page that displays lines for a given journal.</span></span> <span data-ttu-id="d41d4-108">Echter, met de functie **Openen in nieuw venster** kunt u deze pagina's naast elkaar weergeven zodat u snel uw taken kunt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="d41d4-108">However, the **Open in new window** feature enables you to display these pages side-by-side so that you can perform your tasks quickly.</span></span>

<span data-ttu-id="d41d4-109">Om door te gaan met het bovenstaande voorbeeld, klikt u tijdens het weergeven van de regels op het pictogram **Openen in nieuw venster**.</span><span class="sxs-lookup"><span data-stu-id="d41d4-109">Continuing with the example mentioned above, when viewing the lines, you can click the **Open in new window** icon.</span></span>

<span data-ttu-id="d41d4-110">[![Pictogram Openen in nieuw venster](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span><span class="sxs-lookup"><span data-stu-id="d41d4-110">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span></span>

<span data-ttu-id="d41d4-111">Als u klikt op het pictogram **Openen in nieuw venster**, wordt de regelspagina geopend in een nieuwe pop-upbrowser en navigeert vervolgens naar de oorspronkelijke browser terug naar de pagina die de lijst met journalen toonde.</span><span class="sxs-lookup"><span data-stu-id="d41d4-111">Clicking the **Open in new window** icon opens the lines page in a new, pop-up browser, and then navigates the original browser back in history to the page that displayed the list of journals.</span></span> <span data-ttu-id="d41d4-112">U kunt beide pagina's naast elkaar weergeven.</span><span class="sxs-lookup"><span data-stu-id="d41d4-112">You can then display both pages side-by-side.</span></span> <span data-ttu-id="d41d4-113">Wanneer u een journaal hebt bekeken, kunt u het geselecteerde journaal wijzigen op de pagina met de journaallijst, en de regelspagina in het pop-upvenster geeft automatisch de regels van het geselecteerde journaal weer.</span><span class="sxs-lookup"><span data-stu-id="d41d4-113">When you are done viewing a journal, you can change the selected journal on the journal list page, and the lines page in the pop-up window will automatically display the lines of the newly selected journal.</span></span>

<span data-ttu-id="d41d4-114">[![Pagina's naast elkaar weergeven](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span><span class="sxs-lookup"><span data-stu-id="d41d4-114">[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span></span>

<span data-ttu-id="d41d4-115">De dynamische koppeling en vernieuwing gebeurt vanwege de relaties tussen de gegevens die deze pagina's ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="d41d4-115">The dynamic linking and refreshing happens due to the relations that exist between the data that is backing these pages.</span></span> <span data-ttu-id="d41d4-116">Als het systeem niet bewust is van de relatie tussen de gegevens, wordt het pop-upvenster niet automatisch vernieuwd in reactie op een wijziging in het venster waaruit het afkomstig is.</span><span class="sxs-lookup"><span data-stu-id="d41d4-116">If the system is not aware of the relation between the data, the pop-up window will not refresh automatically in response to a change in the window it originated from.</span></span>

<span data-ttu-id="d41d4-117">Sommige pagina's hebben meerdere weergaven zoals de Rasterweergave, Kopweergave en Detailsweergave.</span><span class="sxs-lookup"><span data-stu-id="d41d4-117">Some pages have multiple views such as the Grid view, Header view, and Details view.</span></span> <span data-ttu-id="d41d4-118">Het pictogram **Openen in nieuw venster** zorgt ervoor dat de volledige pagina wordt geopend in het nieuwe browservenster.</span><span class="sxs-lookup"><span data-stu-id="d41d4-118">The **Open in new window** icon causes the entire page to be opened in the new browser window.</span></span> <span data-ttu-id="d41d4-119">Daarom kunt u niet twee weergaven van dezelfde pagina naast elkaar behouden met de functie **Openen in nieuw venster**.</span><span class="sxs-lookup"><span data-stu-id="d41d4-119">Therefore, you cannot keep two views of the same page side-by-side using the **Open in new window** feature.</span></span> <span data-ttu-id="d41d4-120">Echter, bijna alle pagina's hebben een navigatielijst die u kunt gebruiken om tussen records te schakelen om een vergelijkbare ervaring te bereiken.</span><span class="sxs-lookup"><span data-stu-id="d41d4-120">However, almost all such pages have a navigation list that you can use to switch between records and achieve a similar experience.</span></span>

<span data-ttu-id="d41d4-121">Voordat u de functie **Openen in nieuw venster** kunt gebruiken, moet u de pop-upblokkering van uw browser zo instellen dat pop-ups van de URL van de site zijn toegestaan.</span><span class="sxs-lookup"><span data-stu-id="d41d4-121">Before using the **Open in new window** feature, you should configure your browser's pop-up blocker to allow pop-ups from the URL of the site.</span></span> <span data-ttu-id="d41d4-122">U kunt bijvoorbeeld pop-ups van "\*.dynamics.com" toestaan.</span><span class="sxs-lookup"><span data-stu-id="d41d4-122">As an example, you could allow pop-ups from "\*.dynamics.com".</span></span>

<span data-ttu-id="d41d4-123">De functie **Openen in nieuw venster** is alleen beschikbaar wanneer er meer dan een pagina is geopend in het venster.</span><span class="sxs-lookup"><span data-stu-id="d41d4-123">The **Open in new window** feature is only available when there is more than one page open in the window.</span></span> <span data-ttu-id="d41d4-124">Het pop-upvenster wordt ook automatisch gesloten wanneer er geen pagina's meer open zijn (dat wil zeggen wanneer de laatste pagina in dat venster wordt gesloten).</span><span class="sxs-lookup"><span data-stu-id="d41d4-124">Also, the pop-up window automatically closes when there are no more pages open (that is, when the last page in that window is closed).</span></span> <span data-ttu-id="d41d4-125">Het systeem sluit ook open pagina´s wanneer u navigeert naar een ander gedeelte in de toepassing.</span><span class="sxs-lookup"><span data-stu-id="d41d4-125">The system also closes open pages when you navigate to a different area in the application.</span></span> <span data-ttu-id="d41d4-126">Als u dus open pop-upvensters hebt en naar een ander gedeelte in de toepassing navigeert, worden de pop-upvensters automatisch afgesloten omdat de pagina's in die venster door het systeem werden gesloten.</span><span class="sxs-lookup"><span data-stu-id="d41d4-126">Therefore, if you have pop-up windows open and navigate to a different area in the application, the pop-up windows are automatically closed because the pages in those windows were closed by the system.</span></span>

<span data-ttu-id="d41d4-127">De bovenste balk in de pop-upvensters tonen informatie over het bedrijf waarin de pagina is geopend en is alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="d41d4-127">The top bar in the pop-up windows displays information about the company the page was opened in and is read-only.</span></span> <span data-ttu-id="d41d4-128">De pop-upvensters zijn ook afhankelijk van het hoofdbrowservenster.</span><span class="sxs-lookup"><span data-stu-id="d41d4-128">The pop-up windows also rely on the main browser window.</span></span> <span data-ttu-id="d41d4-129">Als het hoofdvenster wordt gesloten of vernieuwd, worden alle openstaande pop-upvensters alleen-lezen.</span><span class="sxs-lookup"><span data-stu-id="d41d4-129">If the main window is closed or refreshed, all open pop-up windows will become read only.</span></span> <span data-ttu-id="d41d4-130">Dit betekent dat u de informatie in deze vensters kunt nog steeds kunt bekijken, maar er is geen interactie mogelijk.</span><span class="sxs-lookup"><span data-stu-id="d41d4-130">This means that you can still view the information in these windows, but you will not be able to interact with it.</span></span>