---
title: Werkorder op specifieke datum en tijd plannen
description: In dit onderwerp wordt uitgelegd hoe u een werkorder op een specifieke datum en tijd in Activabeheer kunt plannen.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: e81ea13a3463965c6e4785dac32f536d2e94a7ba
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215258"
---
# <a name="schedule-work-order-on-specific-date-and-time"></a><span data-ttu-id="0a217-103">Werkorder op specifieke datum en tijd plannen</span><span class="sxs-lookup"><span data-stu-id="0a217-103">Schedule work order on specific date and time</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0a217-104">Als een werkorder op een bepaalde datum *en* tijd moet worden gepland, kunt u het standaardplanningsproces in Activabeheer negeren en een specifieke planning voor een werkorder maken.</span><span class="sxs-lookup"><span data-stu-id="0a217-104">If a work order must be scheduled on a specific date *and* time, you can override the standard scheduling process in Asset Management and create a specific schedule for a work order.</span></span>

1. <span data-ttu-id="0a217-105">Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.</span><span class="sxs-lookup"><span data-stu-id="0a217-105">Click **Asset management** > **Common** > **Work orders** > **All Work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="0a217-106">Klik in de lijst met werkorders op de werkorder-ID in de kolom **Werkorder**.</span><span class="sxs-lookup"><span data-stu-id="0a217-106">In the work order list, click on the Work order ID in the **Work order** column.</span></span>

3. <span data-ttu-id="0a217-107">Klik op **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="0a217-107">Click **Edit**.</span></span>

4. <span data-ttu-id="0a217-108">Voeg op het sneltabblad **Koptekst van werkorder** begin- en einddatums en begin- en eindtijden in de velden voor **verwachte begindatums en -tijden** en **verwachte einddatums en -tijden** in.</span><span class="sxs-lookup"><span data-stu-id="0a217-108">On the **Work order header** FastTab, insert start and end dates and times in the **Expected start** and **Expected end** fields.</span></span>

    ![Figuur 1](media/05-work-order-scheduling.png)

5. <span data-ttu-id="0a217-110">Klik op het tabblad **Algemeen** op **Plannen** om het standaardplanningsproces te gebruiken of klik op **Verzenden** als u de werkorder wilt toewijzen aan een bepaalde medewerker.</span><span class="sxs-lookup"><span data-stu-id="0a217-110">On the **General** tab, click **Schedule** to use the standard scheduling process, or click **Dispatch** if you want to assign the work order to a specific worker.</span></span>

6. <span data-ttu-id="0a217-111">Als u bestaande capaciteitsreserveringen wilt negeren om ervoor te zorgen dat de werkorder wordt gepland in de verwachte periode, maakt u de selecties zoals weergegeven in de onderstaande afbeelding in de sectie **Eindige capaciteit** van het dialoogvenster **Werkorder plannen**.</span><span class="sxs-lookup"><span data-stu-id="0a217-111">In order to override any existing capacity reservations to ensure that the work order is scheduled in the expected period, make the selections as shown in the figure below in the **Schedule work order** dialog > **Finite capacity** section.</span></span> <span data-ttu-id="0a217-112">Dit houdt in dat bestaande capaciteitsreserveringen door het planningsproces worden genegeerd omdat de werkorder op de verwachte begintijd moet beginnen.</span><span class="sxs-lookup"><span data-stu-id="0a217-112">This means that the scheduling process will ignore existing capacity reservations because the work order must start on the expected start time.</span></span>

    ![Figuur 2](media/06-work-order-scheduling.png)

7. <span data-ttu-id="0a217-114">Klik op **OK** om het plannen te starten.</span><span class="sxs-lookup"><span data-stu-id="0a217-114">Click **OK** to start scheduling.</span></span>

8. <span data-ttu-id="0a217-115">Als het planningsproces dubbele boekingen oplevert, wordt er een bericht weergegeven op het scherm en kunt u de gerelateerde werkorders aanpassen.</span><span class="sxs-lookup"><span data-stu-id="0a217-115">If the scheduling process results in double bookings, you will see a message on the screen, and you can adjust the related work orders.</span></span>

>[!NOTE]
><span data-ttu-id="0a217-116">Als u een onderhoudsmedewerker voor de werkorder wilt plannen, moet deze onderhoudsmedewerker beschikbaar zijn op de verwachte begindatum en -tijd.</span><span class="sxs-lookup"><span data-stu-id="0a217-116">In order to schedule a maintenance worker for the work order, that maintenance worker must be available at the expected start date and time.</span></span> <span data-ttu-id="0a217-117">De beschikbaarheid van medewerkers wordt ingesteld in de [medewerkerskalender](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span><span class="sxs-lookup"><span data-stu-id="0a217-117">Worker availability is set up in the [worker calendar](../work-order-scheduling/maintenance-worker-calendar-and-scheduling.md).</span></span> 

