---
title: Onderhoudsverzoeken maken
description: In dit onderwerp wordt uitgelegd hoe u een onderhoudsverzoek maakt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 03e090633276cd264ad03f561ddb425a9816357e
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847500"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="a3095-103">Onderhoudsverzoeken maken</span><span class="sxs-lookup"><span data-stu-id="a3095-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="a3095-104">Onderhoudsverzoeken kunnen worden gebruikt als onderhoudsmedewerkers of productiemedewerkers ontdekken dat apparatuur moet worden gerepareerd, maar de reparatie niet meteen kan worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="a3095-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="a3095-105">**Voorbeeld:** terwijl een onderhoudsmedewerker een reparatie doet, ontdekt ze dat een ander activum op dezelfde locatie moet worden onderhouden.</span><span class="sxs-lookup"><span data-stu-id="a3095-105">**Example:** While a maintenance worker is making a repair, she discovers that another asset at the same location must be serviced.</span></span> <span data-ttu-id="a3095-106">De onderhoudsmedewerker heeft echter niet de tijd of de vereiste reserveonderdelen om de reparatietaak uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="a3095-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="a3095-107">Daarom maakt ze een onderhoudsverzoek voor het activum en voert ze een korte beschrijving van het probleem in.</span><span class="sxs-lookup"><span data-stu-id="a3095-107">Therefore, she creates a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="a3095-108">De sectie **Actieve onderhoudsverzoeken** van het deelvenster **Verwante informatie** aan de rechterkant van de pagina **Alle activa** of **Actieve activa** (**Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa** of **Actieve activa**) bevat de actieve onderhoudsverzoeken die aan het geselecteerde activum gekoppeld zijn.</span><span class="sxs-lookup"><span data-stu-id="a3095-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="a3095-109">Selecteer **Activabeheer** \> **Algemeen** \> **Onderhoudsverzoeken** \> **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="a3095-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="a3095-110">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="a3095-110">Select **New**.</span></span>
3. <span data-ttu-id="a3095-111">Selecteer het type onderhoudsverzoek in het dialoogvenster **Aanvraag maken** in het veld **Type onderhoudsverzoek**.</span><span class="sxs-lookup"><span data-stu-id="a3095-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="a3095-112">Er wordt een standaardtype voorgesteld.</span><span class="sxs-lookup"><span data-stu-id="a3095-112">A default type is suggested.</span></span>
4. <span data-ttu-id="a3095-113">Voer in het veld **Beschrijving** een naam of titel in die kort het onderhoudsverzoek beschrijft.</span><span class="sxs-lookup"><span data-stu-id="a3095-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="a3095-114">Selecteer in de velden **Functionele locatie** en **Activum** een functionele locatie of een activum, of een combinatie van een functionele locatie en een activum, indien nodig.</span><span class="sxs-lookup"><span data-stu-id="a3095-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="a3095-115">U kunt een onderhoudsverzoek maken zonder een activum te selecteren en het activum kan later aan het onderhoudsverzoek worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="a3095-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="a3095-116">Als de onderhoudsmedewerker die is aangemeld bij Microsoft Dynamics 365 for Finance and Operations, is gekoppeld aan een resource die is gerelateerd aan een activum, wordt het veld **Activum** automatisch ingesteld.</span><span class="sxs-lookup"><span data-stu-id="a3095-116">If the maintenance worker who is signed in to Microsoft Dynamics 365 for Finance and Operations is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="a3095-117">Als er al een onderhoudsverzoek is gekoppeld aan het geselecteerde activum, verschijnt een berichtenbalk boven aan het dialoogvenster **Aanvraag maken** met de id van het bestaande onderhoudsverzoek.</span><span class="sxs-lookup"><span data-stu-id="a3095-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="a3095-118">Een berichtenbalk waarschuwt u ook als het activum onder een garantieovereenkomst valt.</span><span class="sxs-lookup"><span data-stu-id="a3095-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="a3095-119">Selecteer in het veld **Serviceniveau** een serviceniveau dat de urgentie van de aanvraag aangeeft.</span><span class="sxs-lookup"><span data-stu-id="a3095-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="a3095-120">Als u een activum hebt geselecteerd in stap 5, kunt u de velden **Foutsymptoom**, **Foutgebied** en **Fouttype** gebruiken om een foutregistratie te maken.</span><span class="sxs-lookup"><span data-stu-id="a3095-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="a3095-121">Als het onderhoudsverzoek uitvaltijd voor onderhoud heeft veroorzaakt, voert u de begindatum en -tijd van de uitvaltijd in.</span><span class="sxs-lookup"><span data-stu-id="a3095-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="a3095-122">Het veld **Gestart door** wordt automatisch ingesteld op uw naam.</span><span class="sxs-lookup"><span data-stu-id="a3095-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="a3095-123">Het veld **Werkelijke begin** wordt automatisch ingesteld op de huidige datum en tijd.</span><span class="sxs-lookup"><span data-stu-id="a3095-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="a3095-124">U kunt deze waarde echter zo nodig wijzigen.</span><span class="sxs-lookup"><span data-stu-id="a3095-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="a3095-125">Voer in het veld **Notities** eventuele aanvullende notities in die vereist zijn.</span><span class="sxs-lookup"><span data-stu-id="a3095-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="a3095-126">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="a3095-126">Select **OK**.</span></span>

![Figuur 1](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="a3095-128">Daaropvolgende verwerking van onderhoudsverzoeken</span><span class="sxs-lookup"><span data-stu-id="a3095-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="a3095-129">Nadat een onderhoudsverzoek is gemaakt, maar voordat deze wordt omgezet in een werkorder, moeten er verschillende gegevens worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="a3095-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="a3095-130">Normaal gesproken voert een planner of een andere administratieve medewerker deze taak uit.</span><span class="sxs-lookup"><span data-stu-id="a3095-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="a3095-131">Op de pagina **Alle onderhoudsverzoeken** of **Actieve onderhoudsverzoeken** selecteert u de aanvraag waarmee moet worden gewerkt en vervolgens **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="a3095-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="a3095-132">In de detailweergave u diverse gegevens bijwerken.</span><span class="sxs-lookup"><span data-stu-id="a3095-132">In the details view, you can update various information.</span></span> <span data-ttu-id="a3095-133">Hieronder vindt u enkele voorbeelden:</span><span class="sxs-lookup"><span data-stu-id="a3095-133">Here are some examples:</span></span>

- <span data-ttu-id="a3095-134">Selecteer en verifieer het activum.</span><span class="sxs-lookup"><span data-stu-id="a3095-134">Select and verify the asset.</span></span> <span data-ttu-id="a3095-135">Als u later een ander activum moet selecteren, kunt u de optie **Activum geverifieerd** instellen op **Nee**.</span><span class="sxs-lookup"><span data-stu-id="a3095-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="a3095-136">Selecteer een verantwoordelijke groep onderhoudsmedewerkers en/of een verantwoordelijke onderhoudsmedewerker.</span><span class="sxs-lookup"><span data-stu-id="a3095-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="a3095-137">Zie [Verantwoordelijke onderhoudsmedewerkers](../setup-for-maintenance-requests/responsible-workers.md) voor meer informatie over de vereiste stap.</span><span class="sxs-lookup"><span data-stu-id="a3095-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="a3095-138">Selecteer een type onderhoudstaak en, als deze informatie relevant is, een gerelateerde onderhoudstaakvariant en een vakgebied.</span><span class="sxs-lookup"><span data-stu-id="a3095-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="a3095-139">Voer in de velden **Breedtegraad** en **Lengtegraad** de geografische coördinaten in.</span><span class="sxs-lookup"><span data-stu-id="a3095-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="a3095-140">Alle coördinaten die aan een onderhoudsverzoek worden toegevoegd, worden automatisch overgebracht naar een gerelateerde werkorder.</span><span class="sxs-lookup"><span data-stu-id="a3095-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![Figuur 2](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="a3095-142">Als u een activum selecteert wanneer u een onderhoudsverzoek maakt, kunt u één fout aan het activum toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a3095-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="a3095-143">Nadat het onderhoudsverzoek is gemaakt, kunt u zo nodig meer fouten toevoegen.</span><span class="sxs-lookup"><span data-stu-id="a3095-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="a3095-144">Als u fouten wilt toevoegen, selecteert u **Activafout** op de pagina **Alle onderhoudsverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="a3095-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>
