---
title: Automatisch bijwerken van activatellers
description: Dit onderwerp beschrijft het automatisch bijwerken van activatellers in Activabeheer.
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
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875595"
---
# <a name="automatic-update-of-asset-counters"></a><span data-ttu-id="6565a-103">Automatisch bijwerken van activatellers</span><span class="sxs-lookup"><span data-stu-id="6565a-103">Automatic update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="6565a-104">In het vorige gedeelte wordt de handmatige registratie van activatellers beschreven.</span><span class="sxs-lookup"><span data-stu-id="6565a-104">In the previous section, manual registration of asset counters is described.</span></span> <span data-ttu-id="6565a-105">Het instellen van activatellers wordt beschreven in [Tellers](../setup-for-objects/counters.md).</span><span class="sxs-lookup"><span data-stu-id="6565a-105">Setup of asset counters is described in [Counters](../setup-for-objects/counters.md).</span></span>

<span data-ttu-id="6565a-106">Tellerwaarden kunnen ook automatisch worden bijgewerkt vanuit productieregistraties, op basis van productie-uren of de productiehoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="6565a-106">Counter values can also be automatically updated from production registrations, based on production hours or production quantity.</span></span> <span data-ttu-id="6565a-107">Dit gebeurt in **Activumtellers bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="6565a-107">This is done in **Update asset counters**.</span></span> <span data-ttu-id="6565a-108">U kunt een of meer activa bijwerken door één parameter, **Begindatum**, in te voegen.</span><span class="sxs-lookup"><span data-stu-id="6565a-108">You can update one or several assets by inserting one parameter, **From date**.</span></span> <span data-ttu-id="6565a-109">Met deze parameter wordt de begin datum voor productieregistraties (uren of geproduceerde hoeveelheid) opgegeven. Dit betekent de begindatum vanaf welke de tellerwaarden moeten worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="6565a-109">This parameter specifies the start date for production registrations (hours or quantity produced), meaning the start date from which counter values should be updated.</span></span>

<span data-ttu-id="6565a-110">Alle activa die gerelateerd zijn aan een resource *en* activatellers hebben die zijn ingesteld om te worden bijgewerkt op basis van de geproduceerde hoeveelheid of productie-uren, worden opgenomen in een automatische update en nieuwe tellerwaarden worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6565a-110">All assets that are related to a resource *and* have asset counters, which are set up to be updated based on produced quantity or production hours, will be included in an automatic update, and new counter values will be created.</span></span>

<span data-ttu-id="6565a-111">Voor tellers op basis van de productiehoeveelheid wordt zowel de goede hoeveelheid als de geregistreerde fouthoeveelheid in de telling opgenomen.</span><span class="sxs-lookup"><span data-stu-id="6565a-111">Regarding counters based on production quantity, good quantity as well as error quantity registered are included in the count.</span></span> <span data-ttu-id="6565a-112">Als de eenheid die wordt gebruikt voor het registreren van geproduceerde hoeveelheden verschilt van de eenheid die wordt gebruikt voor de teller, wordt de hoeveelheid geconverteerd zodat deze overeenkomt met de tellereenheid.</span><span class="sxs-lookup"><span data-stu-id="6565a-112">If the unit used for produced quantity registration is different from the unit used on the counter, quantity is converted to correspond with the counter unit.</span></span>

<span data-ttu-id="6565a-113">Zoals hierboven aangegeven, kunnen automatische tellers worden bijgewerkt vanuit productieregistraties.</span><span class="sxs-lookup"><span data-stu-id="6565a-113">As mentioned above, automatic counters can be updated from production registrations.</span></span> <span data-ttu-id="6565a-114">Daarom moet het activum waarvoor u tellers automatisch wilt bijwerken aan een resource (machine) zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="6565a-114">Therefore, the asset for which you want to automatically update counters must be related to a resource (machine).</span></span> <span data-ttu-id="6565a-115">De volgende omschrijvingen geven een overzicht van de instellingen en verwerking van productieorders (in de module **Productiebeheer**), die als basis dient voor het automatisch bijwerken van tellers voor een activum in de module **Activabeheer**.</span><span class="sxs-lookup"><span data-stu-id="6565a-115">The following descriptions provide an overview of the setup and processing of production orders (in the **Production control** module), which is used as a basis for automatic update of counters on an asset in the **Asset management** module.</span></span>

<span data-ttu-id="6565a-116">Wanneer de geproduceerde hoeveelheden of productie-uren zijn geregistreerd voor de resource, kunt u de gerelateerde activatellers bijwerken.</span><span class="sxs-lookup"><span data-stu-id="6565a-116">When produced quantities or production hours have been registered on the resource, you can update the related asset counters.</span></span>

1. <span data-ttu-id="6565a-117">Klik op **Activabeheer** > **Periodiek** > **Activa** > **Activumtellers bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="6565a-117">Click **Asset management** > **Periodic** > **Assets** > **Update asset counters**.</span></span>

2. <span data-ttu-id="6565a-118">Selecteer de begindatum van de automatische update in het veld **Begindatum**.</span><span class="sxs-lookup"><span data-stu-id="6565a-118">Select the start date of the automatic update in the **From date** field.</span></span>

>[!NOTE]
><span data-ttu-id="6565a-119">De datum in dit veld is de datum voor onderhanden werk uit **Routetransacties** (**Productiebeheer** > **Query's en rapporten** > **Productie** > **Routetransacties** > **Fysieke datum**).</span><span class="sxs-lookup"><span data-stu-id="6565a-119">The date in this field is the "work in progress" date from **Route transactions** (**Production control** > **Inquiries and reports** > **Production** > **Route transactions** > **Physical date** field).</span></span>

3. <span data-ttu-id="6565a-120">Als u specifieke activa, activumtypen of resources wilt selecteren, klikt u op **Filteren** op het sneltabblad **Records die moeten worden opgenomen** en selecteert u de betreffende items.</span><span class="sxs-lookup"><span data-stu-id="6565a-120">If you want to select specific assets, asset types, or resources for the automatic update, click **Filter** on the **Records to include** FastTab, and make the relevant selections.</span></span>

4. <span data-ttu-id="6565a-121">Indien nodig kunt u de automatische update op het sneltabblad **Op de achtergrond uitvoeren** instellen als een batchtaak.</span><span class="sxs-lookup"><span data-stu-id="6565a-121">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

![Figuur 1](media/12-work-orders.png)

5. <span data-ttu-id="6565a-123">Klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="6565a-123">Click **OK**.</span></span> <span data-ttu-id="6565a-124">Wanneer de automatische update van de activumteller is uitgevoerd, ziet u de tellerregistraties die gerelateerd zijn aan het activum in **Activumtellers** (**Activabeheer** > **Algemeen** > **Activa** > **Alle activa** > het activum selecteren > de knop **Teller**).</span><span class="sxs-lookup"><span data-stu-id="6565a-124">When the automatic asset counter update is done, you can see the counter registrations related to the asset in **Asset counters** (**Asset management** > **Common** > **Assets** > **All assets** > select asset > **Counters** button).</span></span>

<span data-ttu-id="6565a-125">In **Totalen van activateller** kunt u een overzicht krijgen van de laatste gemaakte registratie voor alle tellertypen voor alle activa.</span><span class="sxs-lookup"><span data-stu-id="6565a-125">In **Asset counter totals**, you can get an overview of the latest registration made on all counter types on all assets.</span></span> <span data-ttu-id="6565a-126">Klik op **Activabeheer** > **Query's** > **Activa** > **Samengevoegde waarde van activa**.</span><span class="sxs-lookup"><span data-stu-id="6565a-126">Click **Asset management** > **Inquiries** > **Assets** > **Asset aggregated value**.</span></span> <span data-ttu-id="6565a-127">De weergave is vergelijkbaar met **Activumtellers**, maar u kunt geen registraties toevoegen of bewerken in **Samengevoegde waarde van activa**.</span><span class="sxs-lookup"><span data-stu-id="6565a-127">The view is very similar to **Asset counters**, but you cannot add or edit registrations in **Asset aggregated value**.</span></span> <span data-ttu-id="6565a-128">Deze is alleen bedoeld als overzicht.</span><span class="sxs-lookup"><span data-stu-id="6565a-128">It is for overview only.</span></span>

![Figuur 2](media/13-work-orders.png)


- <span data-ttu-id="6565a-130">Het is nog steeds mogelijk om handmatige registraties voor tellerwaarden te maken voor tellertypen die automatisch worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="6565a-130">It is still possible to create manual counter value registrations for counter types that are automatically updated.</span></span> <span data-ttu-id="6565a-131">Zie Handmatig bijwerken van activatellers voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="6565a-131">Refer to the "Manual update of asset counters" section for more information.</span></span>
- <span data-ttu-id="6565a-132">U kunt tellers instellen die gerelateerd zijn aan een andere teller. Dit betekent dat gerelateerde tellers automatisch tegelijkertijd worden bijgewerkt wanneer een teller wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="6565a-132">You can set up counters related to another counter, which means that when a counter is updated, related counters are automatically updated at the same time.</span></span> <span data-ttu-id="6565a-133">Zie het onderwerp [Tellers](../setup-for-objects/counters.md) voor het instellen van gerelateerde tellers.</span><span class="sxs-lookup"><span data-stu-id="6565a-133">Refer to [Counters](../setup-for-objects/counters.md) regarding setup of related counters.</span></span>
