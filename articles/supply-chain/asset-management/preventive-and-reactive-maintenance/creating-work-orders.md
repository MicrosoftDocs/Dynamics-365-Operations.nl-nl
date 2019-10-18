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
ms.openlocfilehash: 0a348bc9b7f5a24c5a3ac57113d430a92020b893
ms.sourcegitcommit: 6476f27c8d3dced7c2e9a7344a4e378b51a1983e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/27/2019
ms.locfileid: "1922109"
---
# <a name="creating-work-orders"></a><span data-ttu-id="19618-103">Werkorders maken</span><span class="sxs-lookup"><span data-stu-id="19618-103">Creating work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="19618-104">Wanneer u preventieve onderhoudstaken hebt gepland, is de volgende stap het maken van werkorders voor de taken.</span><span class="sxs-lookup"><span data-stu-id="19618-104">When you have scheduled preventive maintenance jobs, next step is to create work orders for the jobs.</span></span> <span data-ttu-id="19618-105">Dit kunt u doen in een van de onderhoudsschema's.</span><span class="sxs-lookup"><span data-stu-id="19618-105">This is done in one of the maintenance schedules.</span></span> <span data-ttu-id="19618-106">De geplande taken in een onderhoudsschema kunnen verschillende verwijzingstypen hebben:</span><span class="sxs-lookup"><span data-stu-id="19618-106">The scheduled jobs in a maintenance schedule can have different reference types:</span></span>

| <span data-ttu-id="19618-107">Verwijzingstype</span><span class="sxs-lookup"><span data-stu-id="19618-107">Reference type</span></span> | <span data-ttu-id="19618-108">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="19618-108">Description</span></span>                    |
|-----------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19618-109">Onderhoudsplannen</span><span class="sxs-lookup"><span data-stu-id="19618-109">Maintenance plans</span></span>     | <span data-ttu-id="19618-110">Taken voor preventief onderhoud op basis van de typen onderhoudsplan Tijd of Teller.</span><span class="sxs-lookup"><span data-stu-id="19618-110">Preventive maintenance jobs based on maintenance plan types "Time" or "Counter".</span></span>                       |
| <span data-ttu-id="19618-111">Onderhoudsrondes</span><span class="sxs-lookup"><span data-stu-id="19618-111">Maintenance rounds</span></span>    | <span data-ttu-id="19618-112">Taken voor preventief onderhoud met verschillende activa waarvoor een vergelijkbaar type onderhoud is vereist.</span><span class="sxs-lookup"><span data-stu-id="19618-112">Preventive maintenance jobs containing several assets that require a similar type of maintenance.</span></span>           |
| <span data-ttu-id="19618-113">Onderhoudsverzoek</span><span class="sxs-lookup"><span data-stu-id="19618-113">Maintenance request</span></span>   | <span data-ttu-id="19618-114">Handmatig gemaakt verzoek om onderhoud of reparatie van een activum, dat kan worden omgezet in een werkorder.</span><span class="sxs-lookup"><span data-stu-id="19618-114">Manually created request for maintenance or repair of an asset, which can be converted into a work order.</span></span> |


1. <span data-ttu-id="19618-115">Klik op **Activabeheer** > **Algemeen** > **Hele onderhoudsschema** of **Openstaande onderhoudsschemaregels** of **Openstaande onderhoudsschemagroepen**.</span><span class="sxs-lookup"><span data-stu-id="19618-115">Click **Asset management** > **Common** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools**.</span></span>

2. <span data-ttu-id="19618-116">Selecteer de geplande onderhoudstaken waarvoor u een werkorder wilt maken en klik op **Werkorder**.</span><span class="sxs-lookup"><span data-stu-id="19618-116">Select the scheduled maintenance jobs for which you want to create a work order and click **Work order**.</span></span> <span data-ttu-id="19618-117">In het dialoogvenster **Werkorders maken** wordt het totaal aantal geraamde uren voor de geselecteerde regels weergegeven in het veld **Prognose voor onderhoudsuren**.</span><span class="sxs-lookup"><span data-stu-id="19618-117">In the **Create work orders** dialog, the total number of forecast hours for the selected lines is shown in the **Maintenance forecast hours** field.</span></span>

3. <span data-ttu-id="19618-118">Selecteer in de sectie **Parameters** hoeveel werkorders er gemaakt moeten.</span><span class="sxs-lookup"><span data-stu-id="19618-118">In the **Parameters** section, select how many work orders should be created.</span></span> <span data-ttu-id="19618-119">U kunt één werkorder per onderhoudsschemaregel maken of een aantal werkorders op basis van uw selecties in de sectie **Eén werkorder per**.</span><span class="sxs-lookup"><span data-stu-id="19618-119">You can create one work order per maintenance schedule line, or a number of work orders based on your selections in the **One work order per** section.</span></span>

4. <span data-ttu-id="19618-120">Selecteer een **Werkordertype** dat wordt gebruikt voor alle werkorders die u maakt.</span><span class="sxs-lookup"><span data-stu-id="19618-120">Select a **Work order type** that will be used on all the work orders you create.</span></span> <span data-ttu-id="19618-121">In de onderstaande afbeelding ziet u een voorbeeld van het dialoogvenster **Werkorders maken**.</span><span class="sxs-lookup"><span data-stu-id="19618-121">The illustration below shows an example of the **Create work orders** dialog.</span></span>

![Figuur 1](media/18-preventive-maintenance.png)

5. <span data-ttu-id="19618-123">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="19618-123">Click **OK**.</span></span> <span data-ttu-id="19618-124">Er worden een of meer werkorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="19618-124">One or more work orders are created.</span></span>

