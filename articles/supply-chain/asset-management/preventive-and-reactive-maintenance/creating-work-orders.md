---
title: Werkorders maken
description: In dit onderwerp wordt uitgelegd hoe u werkorders maakt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.openlocfilehash: 6e910b2400106baf9f9dc06f6bc0d3daee8e4a43
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570071"
---
# <a name="creating-work-orders"></a><span data-ttu-id="f0416-103">Werkorders maken</span><span class="sxs-lookup"><span data-stu-id="f0416-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="f0416-104">Wanneer u preventieve onderhoudstaken hebt gepland, is de volgende stap het maken van werkorders voor de taken.</span><span class="sxs-lookup"><span data-stu-id="f0416-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="f0416-105">Dit kunt u doen in een van de onderhoudsschema's.</span><span class="sxs-lookup"><span data-stu-id="f0416-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="f0416-106">De geplande taken in een onderhoudsschema kunnen verschillende verwijzingstypen hebben:</span><span class="sxs-lookup"><span data-stu-id="f0416-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="f0416-107">Verwijzingstype</span><span class="sxs-lookup"><span data-stu-id="f0416-107">Reference type</span></span> | <span data-ttu-id="f0416-108">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f0416-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0416-109">Onderhoudsplannen</span><span class="sxs-lookup"><span data-stu-id="f0416-109">Maintenance plans</span></span>     | <span data-ttu-id="f0416-110">Taken voor preventief onderhoud op basis van de typen onderhoudsplan Tijd of Teller.</span><span class="sxs-lookup"><span data-stu-id="f0416-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="f0416-111">Onderhoudsrondes</span><span class="sxs-lookup"><span data-stu-id="f0416-111">Maintenance rounds</span></span>    | <span data-ttu-id="f0416-112">Taken voor preventief onderhoud met verschillende activa waarvoor een vergelijkbaar type onderhoud is vereist.</span><span class="sxs-lookup"><span data-stu-id="f0416-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="f0416-113">Onderhoudsverzoek</span><span class="sxs-lookup"><span data-stu-id="f0416-113">Maintenance request</span></span>   | <span data-ttu-id="f0416-114">Handmatig gemaakt verzoek om onderhoud of reparatie van een activum, dat kan worden omgezet in een werkorder.</span><span class="sxs-lookup"><span data-stu-id="f0416-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="f0416-115">Klik op **Activabeheer** > **Algemeen** > **Hele onderhoudsschema** of **Openstaande onderhoudsschemaregels** of **Openstaande onderhoudsschemagroepen**.</span><span class="sxs-lookup"><span data-stu-id="f0416-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="f0416-116">Selecteer de geplande onderhoudstaken waarvoor u een werkorder wilt maken en klik op **Werkorder**.</span><span class="sxs-lookup"><span data-stu-id="f0416-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="f0416-117">In het dialoogvenster **Werkorders maken** wordt het totaal aantal geraamde uren voor de geselecteerde regels weergegeven in het veld **Prognose voor onderhoudsuren**.</span><span class="sxs-lookup"><span data-stu-id="f0416-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="f0416-118">Selecteer in de sectie **Parameters** hoeveel werkorders er gemaakt moeten.</span><span class="sxs-lookup"><span data-stu-id="f0416-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="f0416-119">U kunt één werkorder per onderhoudsschemaregel maken of een aantal werkorders op basis van uw selecties in de sectie **Eén werkorder per**.</span><span class="sxs-lookup"><span data-stu-id="f0416-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="f0416-120">Selecteer een **Werkordertype** dat wordt gebruikt voor alle werkorders die u maakt.</span><span class="sxs-lookup"><span data-stu-id="f0416-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="f0416-121">In de onderstaande afbeelding ziet u een voorbeeld van het dialoogvenster **Werkorders maken**.</span><span class="sxs-lookup"><span data-stu-id="f0416-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![Figuur 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="f0416-123">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0416-123">Click **OK**.</span></span> <span data-ttu-id="f0416-124">Er worden een of meer werkorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f0416-124">One or more work orders are created.</span></span>

