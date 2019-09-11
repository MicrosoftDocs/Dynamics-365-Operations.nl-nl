---
title: Handmatig bijwerken van activatellers
description: Dit onderwerp beschrijft het handmatig bijwerken van activatellers in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875590"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="ae380-103">Handmatig bijwerken van activatellers</span><span class="sxs-lookup"><span data-stu-id="ae380-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="ae380-104">Tellers worden gebruikt om registraties voor een activum te maken over bijvoorbeeld het aantal uren van bewerking of het aantal geproduceerde hoeveelheden.</span><span class="sxs-lookup"><span data-stu-id="ae380-104">Counters are used to create registrations on an asset regarding, for example, number of hours in operation, or the number of quantities produced.</span></span>

<span data-ttu-id="ae380-105">Als het type dat voor een teller is geselecteerd, is ingesteld op het overnemen van tellerwaarden (**Activabeheer** > **Instellen** > **Activatypen** > **Tellers** > sneltabblad **Algemeen** > wisselknop **Waarden van activumteller overnemen** ingesteld op Ja), dan wordt elk onderliggend activum dat hetzelfde tellertype gebruikt, automatisch bijgewerkt wanneer u een nieuwe tellerregel van dat type maakt.</span><span class="sxs-lookup"><span data-stu-id="ae380-105">If the counter type selected for a counter is set to inherit counter values (**Asset management** > **Setup** > **Asset types** > **Counters** > **General** FastTab > **Inherit asset counter values** toggle button set to "Yes"), then, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="ae380-106">In **Alle activa** kunt u waarden van uren- of hoeveelheidstellers voor een activum registreren op basis van uw tellingen voor het activum.</span><span class="sxs-lookup"><span data-stu-id="ae380-106">In **All assets**, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="ae380-107">Klik op **Activabeheer** > **Algemeen** > **Activa** > **Alle activa**.</span><span class="sxs-lookup"><span data-stu-id="ae380-107">Click **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="ae380-108">Selecteer het activum in de lijst en klik op **Tellers**.</span><span class="sxs-lookup"><span data-stu-id="ae380-108">Select the asset in the list, and click **Counters**.</span></span> <span data-ttu-id="ae380-109">In het formulier **Activatellers** ziet u een lijst met alle eerdere tellerregistraties voor het geselecteerde activum.</span><span class="sxs-lookup"><span data-stu-id="ae380-109">In the **Asset counters** form, you see a list of all previous counter registrations on the selected asset.</span></span>

3. <span data-ttu-id="ae380-110">Klik op **Nieuw** om een nieuwe registratie te maken.</span><span class="sxs-lookup"><span data-stu-id="ae380-110">Click **New** to create a new registration.</span></span> <span data-ttu-id="ae380-111">De activum-id wordt automatisch ingevoegd.</span><span class="sxs-lookup"><span data-stu-id="ae380-111">The asset ID is automatically inserted.</span></span>

4. <span data-ttu-id="ae380-112">Selecteer de betreffende teller in het veld **Teller**.</span><span class="sxs-lookup"><span data-stu-id="ae380-112">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="ae380-113">Alleen tellers voor het geselecteerde activumtype in het activum zijn beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="ae380-113">Only counters related to the asset type selected on the asset are available.</span></span> <span data-ttu-id="ae380-114">De gerelateerde eenheid wordt automatisch in het veld **Eenheid** ingevoegd.</span><span class="sxs-lookup"><span data-stu-id="ae380-114">The related unit is automatically inserted in the **Unit** field.</span></span>

5. <span data-ttu-id="ae380-115">Selecteer de datum en tijd voor de registratie van de teller.</span><span class="sxs-lookup"><span data-stu-id="ae380-115">Select date and time for the counter registration.</span></span>

6. <span data-ttu-id="ae380-116">Voer in het veld **Waarde** de numerieke waarde na de laatste tellerregistratie in of voer in het veld **Samengevoegde waarde** de totale tellerwaarde in.</span><span class="sxs-lookup"><span data-stu-id="ae380-116">In the **Value** field, insert the number since the last counter registration, or, in the **Aggregated value** field, insert the total count number.</span></span>

- <span data-ttu-id="ae380-117">Als u fysiek een nieuwe teller voor een activum installeert, moet u de wijziging voor het activum registreren in **Activumtellers**.</span><span class="sxs-lookup"><span data-stu-id="ae380-117">If you physically install a new counter on an asset, you need to register the change on the asset in **Asset counters**.</span></span> <span data-ttu-id="ae380-118">Vervolgens moet u twee registratieregels met identieke tijdstempels maken. Op de regel voor de nieuwe teller schakelt u het selectievakje **Teller op nul zetten** in.</span><span class="sxs-lookup"><span data-stu-id="ae380-118">Next, you must create two registration lines with identical timestamps, and on the line regarding the new counter, you select the **Counter reset** check box.</span></span> <span data-ttu-id="ae380-119">Wanneer u de twee registratieregels maakt, moet de eerste regel de regel zijn voor de teller die u wilt vervangen.</span><span class="sxs-lookup"><span data-stu-id="ae380-119">When you create the two registration lines, the first line must be for the counter that you are replacing.</span></span> <span data-ttu-id="ae380-120">In het veld **Totalen** is het totaal aantal tellingen de som van het tellertotaal van alle geregistreerde waarden voor dat tellertype.</span><span class="sxs-lookup"><span data-stu-id="ae380-120">In the **Totals** field, the total count number is the sum of the counter total of all registered values on that counter type.</span></span>  
- <span data-ttu-id="ae380-121">Als het selectievakje **Teller op nul zetten** voor een activum met behulp van een onderhoudsplan is ingeschakeld met het intervaltype 'Eenmaal vanaf…' of 'Eenmaal bereikt…', is de teller nog steeds actief op de nieuwe tellerregel omdat u een afzonderlijke tellerregel maakt en opnieuw begint met een nieuwe teller.</span><span class="sxs-lookup"><span data-stu-id="ae380-121">If the **Counter reset** check box is selected on an asset using a maintenance plan with a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line because you create a separate counter line and start over with a new counter.</span></span>

![Figuur 1](media/11-work-orders.png)


<span data-ttu-id="ae380-123">Als u tellerregistraties voor verschillende activa moet maken, kunt u dit doen in **Activabeheer** > **Query's** > **Activa** > **Activumtellers**.</span><span class="sxs-lookup"><span data-stu-id="ae380-123">If you need to make counter registrations on several assets, that can be done in **Asset management** > **Inquiries** > **Assets** > **Asset counters**.</span></span>

>[!NOTE]
><span data-ttu-id="ae380-124">U kunt een bereik instellen voor het definiëren van afwijkingen in handmatige registraties van tellers en het type bericht dat moet worden weergegeven als registraties buiten het gedefinieerde bereik vallen.</span><span class="sxs-lookup"><span data-stu-id="ae380-124">You can set up a range to define deviations in manual counter registrations, and the type of message that should be displayed if registrations are outside the defined range.</span></span> <span data-ttu-id="ae380-125">Zie het onderwerp [Tellers](../setup-for-objects/counters.md) voor het instellen van tellers.</span><span class="sxs-lookup"><span data-stu-id="ae380-125">Refer to the [Counters](../setup-for-objects/counters.md) topic regarding setup of counters.</span></span>
