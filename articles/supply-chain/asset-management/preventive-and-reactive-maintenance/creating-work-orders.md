---
title: Werkorders maken
description: In dit onderwerp wordt uitgelegd hoe u werkorders maakt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
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
ms.openlocfilehash: f94f8bc20753e38ce1cb6eccdfbc85c2e491ffad
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425483"
---
# <a name="creating-work-orders"></a><span data-ttu-id="17062-103">Werkorders maken</span><span class="sxs-lookup"><span data-stu-id="17062-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="17062-104">Wanneer u preventieve onderhoudstaken hebt gepland, is de volgende stap het maken van werkorders voor de taken.</span><span class="sxs-lookup"><span data-stu-id="17062-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="17062-105">Dit kunt u doen in een van de onderhoudsschema's.</span><span class="sxs-lookup"><span data-stu-id="17062-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="17062-106">De geplande taken in een onderhoudsschema kunnen verschillende verwijzingstypen hebben:</span><span class="sxs-lookup"><span data-stu-id="17062-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="17062-107">Verwijzingstype</span><span class="sxs-lookup"><span data-stu-id="17062-107">Reference type</span></span> | <span data-ttu-id="17062-108">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="17062-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17062-109">Onderhoudsplannen</span><span class="sxs-lookup"><span data-stu-id="17062-109">Maintenance plans</span></span>     | <span data-ttu-id="17062-110">Taken voor preventief onderhoud op basis van de typen onderhoudsplan Tijd of Teller.</span><span class="sxs-lookup"><span data-stu-id="17062-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="17062-111">Onderhoudsrondes</span><span class="sxs-lookup"><span data-stu-id="17062-111">Maintenance rounds</span></span>    | <span data-ttu-id="17062-112">Taken voor preventief onderhoud met verschillende activa waarvoor een vergelijkbaar type onderhoud is vereist.</span><span class="sxs-lookup"><span data-stu-id="17062-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="17062-113">Onderhoudsverzoek</span><span class="sxs-lookup"><span data-stu-id="17062-113">Maintenance request</span></span>   | <span data-ttu-id="17062-114">Handmatig gemaakt verzoek om onderhoud of reparatie van een activum, dat kan worden omgezet in een werkorder.</span><span class="sxs-lookup"><span data-stu-id="17062-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="17062-115">Klik op **Activabeheer** > **Algemeen** > **Hele onderhoudsschema** of **Openstaande onderhoudsschemaregels** of **Openstaande onderhoudsschemagroepen**.</span><span class="sxs-lookup"><span data-stu-id="17062-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="17062-116">Selecteer de geplande onderhoudstaken waarvoor u een werkorder wilt maken en klik op **Werkorder**.</span><span class="sxs-lookup"><span data-stu-id="17062-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="17062-117">In het dialoogvenster **Werkorders maken** wordt het totaal aantal geraamde uren voor de geselecteerde regels weergegeven in het veld **Prognose voor onderhoudsuren**.</span><span class="sxs-lookup"><span data-stu-id="17062-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="17062-118">Selecteer in de sectie **Parameters** hoeveel werkorders er gemaakt moeten.</span><span class="sxs-lookup"><span data-stu-id="17062-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="17062-119">U kunt één werkorder per onderhoudsschemaregel maken of een aantal werkorders op basis van uw selecties in de sectie **Eén werkorder per**.</span><span class="sxs-lookup"><span data-stu-id="17062-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="17062-120">Selecteer een **Werkordertype** dat wordt gebruikt voor alle werkorders die u maakt.</span><span class="sxs-lookup"><span data-stu-id="17062-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="17062-121">In de onderstaande afbeelding ziet u een voorbeeld van het dialoogvenster **Werkorders maken**.</span><span class="sxs-lookup"><span data-stu-id="17062-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![Figuur 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="17062-123">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="17062-123">Click **OK**.</span></span> <span data-ttu-id="17062-124">Er worden een of meer werkorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="17062-124">One or more work orders are created.</span></span>

