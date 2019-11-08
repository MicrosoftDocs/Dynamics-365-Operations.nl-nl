---
title: Automatisch bijwerken van activatellers
description: Dit onderwerp beschrijft het automatisch bijwerken van activatellers in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d51b9a7684e460d555632c3896e9dd8a4e10d92c
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626173"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="0c531-103">Automatisch bijwerken van activatellers</span><span class="sxs-lookup"><span data-stu-id="0c531-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c531-104">Zie [Handmatig bijwerken van activatellers](../work-orders/manual-update-of-asset-counters.md) voor meer informatie over de handmatige registratie van activatellers.</span><span class="sxs-lookup"><span data-stu-id="0c531-104">For information about manual registration of asset counters, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span> <span data-ttu-id="0c531-105">Zie [Tellers](../setup-for-objects/counters.md)voor meer informatie over het instellen van activatellers.</span><span class="sxs-lookup"><span data-stu-id="0c531-105">For information on how to set up asset counters, see [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="0c531-106">Tellerwaarden kunnen ook automatisch worden bijgewerkt vanuit productieregistraties, op basis van de productie-uren of de productiehoeveelheid (oftewel de hoeveelheid die is geproduceerd).</span><span class="sxs-lookup"><span data-stu-id="0c531-106">Counter values can also be automatically updated from production registrations, based on the production hours or production quantity (that is, the quantity that is produced).</span></span> <span data-ttu-id="0c531-107">Deze update wordt uitgevoerd op de pagina **Activatellers bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="0c531-107">This update is done on the **Update asset counters** page.</span></span> <span data-ttu-id="0c531-108">U kunt een of meer activa bijwerken door één parameter in te stellen: **Begindatum**.</span><span class="sxs-lookup"><span data-stu-id="0c531-108">You can update one or several assets by setting one parameter, **From date**.</span></span> <span data-ttu-id="0c531-109">Deze parameter geeft de begindatum voor productieregistraties (productie-uren of productiehoeveelheden) aan.</span><span class="sxs-lookup"><span data-stu-id="0c531-109">This parameter specifies the start date for production registrations (production hours or production quantities).</span></span> <span data-ttu-id="0c531-110">Met andere woorden, het geeft de datum aan vanaf wanneer de tellerwaarden moeten worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="0c531-110">In other words, it specifies the date that counter values should be updated from.</span></span>

<span data-ttu-id="0c531-111">Alle activa die gerelateerd zijn aan een resource *en* die activatellers hebben die zijn ingesteld om te worden bijgewerkt op basis van de productie-uren of geproduceerde hoeveelheid, worden opgenomen in een automatische update.</span><span class="sxs-lookup"><span data-stu-id="0c531-111">All assets that are related to a resource, *and* that have asset counters that are set up to be updated based on the production hours or production quantity, will be included in an automatic update.</span></span> <span data-ttu-id="0c531-112">Er worden nieuwe tellerwaarden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0c531-112">New counter values will be created.</span></span>

<span data-ttu-id="0c531-113">Voor tellers die zijn gebaseerd op de productiehoeveelheid, bevat de telling zowel de goede hoeveelheid als de foute hoeveelheid die is geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="0c531-113">For counters that are based on the production quantity, the count includes both the good quantity and the error quantity that are registered.</span></span> <span data-ttu-id="0c531-114">Als de eenheid die wordt gebruikt voor het registreren van de productiehoeveelheid verschilt van de eenheid die wordt gebruikt voor de teller, wordt de hoeveelheid geconverteerd zodat deze overeenkomt met de tellereenheid.</span><span class="sxs-lookup"><span data-stu-id="0c531-114">If the unit that is used for production quantity registration differs from the unit that is used for the counter, the quantity is converted so that it corresponds to the counter unit.</span></span>

<span data-ttu-id="0c531-115">Zoals hierboven aangegeven, kunnen automatische tellers worden bijgewerkt vanuit productieregistraties.</span><span class="sxs-lookup"><span data-stu-id="0c531-115">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="0c531-116">Daarom moet het activum waarvoor u tellers automatisch wilt bijwerken aan een resource (machine) zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="0c531-116">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="0c531-117">Wanneer de geproduceerde hoeveelheden of productie-uren zijn geregistreerd voor de resource, kunt u de gerelateerde activatellers bijwerken.</span><span class="sxs-lookup"><span data-stu-id="0c531-117">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="0c531-118">Selecteer **Activabeheer** > **Periodiek** > **Activa** > **Activumtellers bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="0c531-118">Select **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="0c531-119">Selecteer in het veld **Begindatum** de begindatum van de automatische update.</span><span class="sxs-lookup"><span data-stu-id="0c531-119">In the **From date** field, select the start date of the automatic update.</span></span>

>[!NOTE]
><span data-ttu-id="0c531-120">De datum in dit veld is de datum voor onderhanden werk uit **Routetransacties** (**Productiebeheer** > **Query's en rapporten** > **Productie** > **Routetransacties** > **Fysieke datum**).</span><span class="sxs-lookup"><span data-stu-id="0c531-120">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="0c531-121">Op het sneltabblad **Op te nemen records** kunt u specifieke activa, activatypen of resources voor de automatische update selecteren.</span><span class="sxs-lookup"><span data-stu-id="0c531-121">On the **Records to include** FastTab, you can select specific assets, asset types, or resources for the automatic update.</span></span> <span data-ttu-id="0c531-122">Selecteer **Filter**en selecteer de relevante selecties.</span><span class="sxs-lookup"><span data-stu-id="0c531-122">Select **Filter**, and make the relevant selections.</span></span>

4. <span data-ttu-id="0c531-123">Indien nodig kunt u de automatische update op het Sneltabblad **Op de achtergrond uitvoeren** instellen als een batchtaak.</span><span class="sxs-lookup"><span data-stu-id="0c531-123">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

<span data-ttu-id="0c531-124">In de onderstaande afbeelding ziet u een voorbeeld van het dialoogvenster **Activumtellers bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="0c531-124">The illustration below shows an example of the **Update asset counters** dialog.</span></span>

![Figuur 1](media/12-work-orders.png)

5. <span data-ttu-id="0c531-126">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="0c531-126">Select **OK**.</span></span> 

<span data-ttu-id="0c531-127">Nadat de automatische update van de activumteller is uitgevoerd, kunt u de tellerregistraties bekijken die zijn gerelateerd aan het activum op de pagina **Activumtellers**.</span><span class="sxs-lookup"><span data-stu-id="0c531-127">After the automatic asset counter update is done, you can view the counter registrations that are related to the asset on the **Asset counters** page.</span></span> <span data-ttu-id="0c531-128">Selecteer **Activabeheer** > **Algemeen** > **Activa** > **Alle activa**, selecteer het activum en selecteer daarna in het actievenster op het tabblad **Activum** in de groep **Preventief** de optie **Tellers**.</span><span class="sxs-lookup"><span data-stu-id="0c531-128">Select **Asset management** > **Common** > **Assets** > **All assets**, select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span>

<span data-ttu-id="0c531-129">Op de pagina **Samengevoegde waarde van activa** kunt u een overzicht krijgen van de als laatste gemaakte registratie voor alle tellertypen voor alle activa.</span><span class="sxs-lookup"><span data-stu-id="0c531-129">On the **Asset aggregated value** page, you can get an overview of the latest registration that have been made on all counter types on all assets.</span></span> <span data-ttu-id="0c531-130">Selecteer **Activabeheer** > **Query's** > **Activa** > **Samengevoegde waarde van activa**.</span><span class="sxs-lookup"><span data-stu-id="0c531-130">Select **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="0c531-131">Deze pagina lijkt op de pagina **Activatellers**, maar u kunt geen registraties toevoegen of bewerken.</span><span class="sxs-lookup"><span data-stu-id="0c531-131">This page resembles the **Asset counters** page, but you can't add or edit registrations.</span></span> <span data-ttu-id="0c531-132">Deze is alleen bedoeld als overzicht.</span><span class="sxs-lookup"><span data-stu-id="0c531-132">It's for overview only.</span></span>

<span data-ttu-id="0c531-133">In de onderstaande afbeelding ziet u een voorbeeld van de pagina **Samengevoegde waarde van activa**.</span><span class="sxs-lookup"><span data-stu-id="0c531-133">The illustration below shows an example of the **Asset aggregated value** page.</span></span>

![Figuur 2](media/13-work-orders.png)

<span data-ttu-id="0c531-135">Let op de volgende punten:</span><span class="sxs-lookup"><span data-stu-id="0c531-135">Note the following points:</span></span>

- <span data-ttu-id="0c531-136">U kunt nog steeds handmatige registraties voor tellerwaarden maken voor tellertypen die automatisch worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="0c531-136">You can still create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="0c531-137">Zie [Handmatig bijwerken van activatellers](../work-orders/manual-update-of-asset-counters.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="0c531-137">For more information, see [Manual update of asset counters](../work-orders/manual-update-of-asset-counters.md).</span></span>

- <span data-ttu-id="0c531-138">U kunt tellers instellen die zijn gerelateerd aan een andere teller.</span><span class="sxs-lookup"><span data-stu-id="0c531-138">You can set up counters that are related to another counter.</span></span> <span data-ttu-id="0c531-139">In dit geval worden gerelateerde tellers tegelijkertijd automatisch bijgewerkt wanneer een teller wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="0c531-139">In this case, when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="0c531-140">Zie [Tellers](../setup-for-objects/counters.md) voor meer informatie over het instellen van gerelateerde tellers.</span><span class="sxs-lookup"><span data-stu-id="0c531-140">For more information about how to set up related counters, see [Counters](../setup-for-objects/counters.md).</span></span>

