---
title: Werkorder verzenden
description: In dit onderwerp wordt uitgelegd hoe u werkorders verzendt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3b1621cf0f1e47d7bd5fe2fa0b41fbcd61f14def
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887200"
---
# <a name="dispatch-work-order"></a><span data-ttu-id="3fb3b-103">Werkorder verzenden</span><span class="sxs-lookup"><span data-stu-id="3fb3b-103">Dispatch work order</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="3fb3b-104">U kunt één werkorder of werkordertaken voor één medewerker plannen met behulp van de functionaliteit **Verzenden**.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-104">You can schedule one work order or work order jobs to one worker using the **Dispatch** functionality.</span></span>

1. <span data-ttu-id="3fb3b-105">Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="3fb3b-106">Selecteer de werkorder in de lijst.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-106">Select the work order in the list.</span></span>

3. <span data-ttu-id="3fb3b-107">Klik op het tabblad **Algemeen** op **Verzenden**.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-107">On the **General** tab, click **Dispatch**.</span></span>

4. <span data-ttu-id="3fb3b-108">Selecteer in het dialoogvenster **Werkorders plannen** de medewerker in het veld **Medewerker**.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-108">n the **Schedule work order** dialog, select the worker in the **Worker** field.</span></span>

5. <span data-ttu-id="3fb3b-109">In het veld **Uren plannen** kunt u verwachte werkuren invoegen voor het geval verwachte werkuren afwijken van prognose-uren.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-109">In the **Schedule hours** field, you can insert expected work hours in case expected work hours differ from forecast hours.</span></span>

6. <span data-ttu-id="3fb3b-110">In het veld **Gepland begin** kunt u zo nodig de begindatum en -tijd bewerken.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-110">In the **Scheduled start** field, you can edit start date and time, if required.</span></span>

7. <span data-ttu-id="3fb3b-111">Als in het planningsproces capaciteitsbeperkingen in acht moeten worden genomen voor resources die al zijn gepland voor andere taken, moet u ervoor zorgen dat de wisselknoppen **Activum**, **Hulpmiddel** en **Medewerker** zijn ingesteld op Ja.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-111">If the scheduling process should observe capacity limitations regarding resources already scheduled on other jobs, make sure that the **Asset**, **Tool**, and **Worker** toggle buttons are set to "Yes".</span></span> <span data-ttu-id="3fb3b-112">Als u gedetailleerde informatie over het planningsproces wilt weergeven, stelt u de wisselknop in op **Uitgebreid**.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-112">If you want to see detailed information about the scheduling process, select "Yes" on the **Verbose** toggle button.</span></span> <span data-ttu-id="3fb3b-113">Dit betekent dat er gedetailleerde informatie over de berekende scores voor de werkorder wordt weergegeven in het infologboek.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-113">This means detailed information about the calculated scores on the work order is shown in the Infolog.</span></span>

8. <span data-ttu-id="3fb3b-114">Selecteer Ja voor de wisselknop **Schema negeren** om gesloten dagen in de kalender te negeren (van toepassing op activum, medewerker en hulpprogramma's).</span><span class="sxs-lookup"><span data-stu-id="3fb3b-114">Select "Yes" on the **Ignore schedule** toggle button to ignore closed days in the calendar (applies to asset, worker, and tools).</span></span> <span data-ttu-id="3fb3b-115">Selecteer Ja voor de wisselknop **Geplande uitvoering negeren** om beperkingen te negeren die mogelijk zijn geselecteerd voor de werkorder met betrekking tot de planning.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-115">Select "Yes" on the **Ignore scheduled execution** toggle button to ignore limitations that may have been selected on the work order regarding scheduling.</span></span> <span data-ttu-id="3fb3b-116">Zie de sectie [Geplande uitvoering](../setup-for-work-orders/scheduled-execution.md) voor informatie over het instellen van de geplande uitvoering.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-116">Refer to the [Scheduled execution](../setup-for-work-orders/scheduled-execution.md) section for information on the setup of scheduled execution.</span></span>

9. <span data-ttu-id="3fb3b-117">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-117">Click **OK**.</span></span> <span data-ttu-id="3fb3b-118">De levenscyclusstatus van de werkorder wordt automatisch bijgewerkt naar de geplande levenscyclusstatus opgegeven via **Activabeheer** > **Instellingen** > **Werkorders** > **Levenscyclusmodellen**.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-118">The work order lifecycle state is automatically updated to the "Scheduled" lifecycle state specified **Asset management** > **Setup** > **Work orders** > **Lifecycle models**.</span></span>

<span data-ttu-id="3fb3b-119">In de volgende afbeelding ziet u een voorbeeld van selecties voor verzending in het dialoogvenster **Werkorder plannen**.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-119">The figure below shows an example of dispatch selections in the **Schedule work order** dialog.</span></span>

![Figuur 1](media/04-work-order-scheduling.png)

>[!NOTE]
><span data-ttu-id="3fb3b-121">Als u de planning voor een werkorder wilt verwijderen, selecteert u de werkorder in **Alle werkorders** en klikt u op **Planning verwijderen** op het tabblad **Algemeen**. Werk de levenscyclusstatus voor de werkorder handmatig bij als u de planning verwijdert.</span><span class="sxs-lookup"><span data-stu-id="3fb3b-121">If you want to delete the schedule on a work order, this is done by selecting the work order in **All work orders** and clicking **Delete schedule** on the **General** tab. Remember to manually update the work order lifecycle state if you delete the schedule.</span></span>

