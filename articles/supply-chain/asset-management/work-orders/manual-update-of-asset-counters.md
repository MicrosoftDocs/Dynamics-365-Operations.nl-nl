---
title: Handmatig bijwerken van activatellers
description: Dit onderwerp beschrijft het handmatig bijwerken van activatellers in Activabeheer.
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
ms.openlocfilehash: 3072ab204b53b16988d2973b28a697041cb84c27
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626127"
---
# <a name="manual-update-of-asset-counters"></a><span data-ttu-id="2f4bd-103">Handmatig bijwerken van activatellers</span><span class="sxs-lookup"><span data-stu-id="2f4bd-103">Manual update of asset counters</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="2f4bd-104">Tellers worden gebruikt om registraties te maken voor een activum, zoals registraties over het aantal uren dat het activum in bewerking is geweest of de hoeveelheid die is geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-104">Counters are used to create registrations on an asset, such as registrations about the number of hours that the asset has been in operation or the quantity that has been produced.</span></span>

<span data-ttu-id="2f4bd-105">Het tellertype dat voor een teller is geselecteerd, kan worden ingesteld op het overnemen van tellerwaarden.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-105">The counter type that is selected for a counter might be set to inherit counter values.</span></span> <span data-ttu-id="2f4bd-106">Met andere woorden, de optie **Waarden van activumteller overnemen** wordt ingesteld op **Ja** op het sneltabblad **Algemeen** van de pagina **Tellers** (**Activabeheer** > **Instellen** > **Typen activa** > **Tellers**).</span><span class="sxs-lookup"><span data-stu-id="2f4bd-106">In other words, the **Inherit asset counter values** option is set to **Yes** on the **General** FastTab of the **Counters** page (**Asset management** > **Setup** > **Asset types** > **Counters**).</span></span> <span data-ttu-id="2f4bd-107">Wanneer u in dit geval een nieuwe tellerregel maakt van dat type, wordt elk onderliggend activum dat hetzelfde tellertype heeft, automatisch bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-107">In this case, when you create a new counter line of that type, every child asset that uses the same counter type is automatically updated.</span></span>

<span data-ttu-id="2f4bd-108">Op de pagina **Alle activa** kunt u waarden van uren- of hoeveelheidstellers voor een activum registreren op basis van uw tellingen voor het activum.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-108">On the **All assets** page, you create hours or quantity counter registrations on an asset, based on your readings on the asset.</span></span>

1. <span data-ttu-id="2f4bd-109">Selecteer **Activabeheer** > **Algemeen** > **Activa** > **Alle activa**.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-109">Select **Asset management** > **Common** > **Assets** > **All assets**.</span></span>

2. <span data-ttu-id="2f4bd-110">Selecteer het activum en selecteer vervolgens in het actievenster op het tabblad **Activa** in de groep **Preventief** de optie **Tellers**.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-110">Select the asset, and then, on the Action Pane, on the **Asset** tab, in the **Preventive** group, select **Counters**.</span></span> <span data-ttu-id="2f4bd-111">Op de pagina **Activatellers** ziet u een lijst met alle eerdere tellerregistraties voor het geselecteerde activum.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-111">The **Asset counters** page shows a list of all previous counter registrations that have been made on the selected asset.</span></span>

3. <span data-ttu-id="2f4bd-112">Selecteer **Nieuw** om een nieuwe registratie te maken.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-112">Select **New** to create a registration.</span></span> <span data-ttu-id="2f4bd-113">De activum-id wordt automatisch in het veld **Activum** ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-113">The asset ID is automatically entered in the **Asset** field.</span></span>

4. <span data-ttu-id="2f4bd-114">Selecteer de betreffende teller in het veld **Teller**.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-114">In the **Counter** field, select the relevant counter.</span></span> <span data-ttu-id="2f4bd-115">Alleen tellers die samenhangen met het geselecteerde activumtype in het activum zijn beschikbaar voor selectie.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-115">Only counters that are related to the asset type selected on the asset are available for selection.</span></span> <span data-ttu-id="2f4bd-116">De gerelateerde eenheid wordt automatisch in het veld **Eenheid** ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-116">The related unit is automatically entered in the **Unit** field.</span></span>

5. <span data-ttu-id="2f4bd-117">Selecteer in het veld **Geregistreerd** de datum en tijd voor de registratie van de teller.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-117">In the **Registered** field, select the date and time for the counter registration.</span></span>

6. <span data-ttu-id="2f4bd-118">Voer in het veld **Waarde** het aantal sinds de registratie van het laatste item in.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-118">In the **Value** field, enter the number since the last counter registration.</span></span> <span data-ttu-id="2f4bd-119">U kunt ook in het veld **Samengevoegde waarde** het aantal van de totale telling invoeren.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-119">Alternatively, in the **Aggregated value** field, enter the total count number.</span></span>

<span data-ttu-id="2f4bd-120">Let op de volgende punten:</span><span class="sxs-lookup"><span data-stu-id="2f4bd-120">Note the following points:</span></span>

- <span data-ttu-id="2f4bd-121">Als u fysiek een nieuwe teller voor een activum installeert, moet u de wijziging voor het activum registreren op de pagina **Activumtellers**.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-121">If you physically install a new counter on an asset, you must register the change on the asset on the **Asset counters** page.</span></span> <span data-ttu-id="2f4bd-122">Vervolgens moet u twee registratieregels maken met identieke tijdstempels.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-122">Next, you must create two registration lines that have identical timestamps.</span></span> <span data-ttu-id="2f4bd-123">De eerste regel moet de teller betreffen die u wilt vervangen.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-123">The first line must be for the counter that you're replacing.</span></span> <span data-ttu-id="2f4bd-124">Schakel op de regel die bij de nieuwe teller hoort het selectievakje **Teller op nul zetten** in.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-124">On the line that is related to the new counter, select the **Counter reset** check box.</span></span> <span data-ttu-id="2f4bd-125">In het veld **Totalen** is het totaal aantal tellingen de som van de tellertotalen van alle geregistreerde waarden voor dat tellertype.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-125">In the **Totals** field, the total count number is the sum of the counter totals of all registered values on that counter type.</span></span>

- <span data-ttu-id="2f4bd-126">Als het selectievakje **Teller op nul zetten** voor een activum met behulp van een onderhoudsplan is ingeschakeld met het intervaltype 'Eenmaal vanaf…' of 'Eenmaal bereikt…', is de teller nog steeds actief op de nieuwe tellerregel omdat u een afzonderlijke tellerregel maakt en opnieuw begint met een nieuwe teller.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-126">If the **Counter reset** check box is selected on an asset using a maintenance plan that has a "Once from..." or "Once reached..." interval type, the counter is still active on the new counter line, because you create a separate counter line and start over with a new counter.</span></span>

<span data-ttu-id="2f4bd-127">In de onderstaande afbeelding ziet u een voorbeeld van de pagina **Activumtellers**.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-127">The illustration below shows an example of the **Asset counters** page.</span></span>

![Figuur 1](media/11-work-orders.png)

<span data-ttu-id="2f4bd-129">Op de pagina **Activumtellers** (**Activabeheer** > **Query's** > **Activa** > **Activatellers**) kunt u zo nodig tellerregistraties maken voor meerdere activa tegelijk.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-129">On the **Asset counters** page (**Asset management** > **Inquiries** > **Assets** > **Asset counters**), you can make counter registrations on several assets at the same time, as you require.</span></span>

>[!NOTE]
><span data-ttu-id="2f4bd-130">U kunt een bereik instellen om afwijkingen in handmatige tellerregistraties te definiëren.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-130">You can set up a range to define deviations in manual counter registrations.</span></span> <span data-ttu-id="2f4bd-131">U kunt ook het type bericht opgeven dat wordt weergegeven als registraties buiten het gedefinieerde bereik vallen.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-131">You can also specify the type of message that is shown if registrations are outside the defined range.</span></span> <span data-ttu-id="2f4bd-132">Zie [Tellers](../setup-for-objects/counters.md) voor meer informatie over het instellen van tellers.</span><span class="sxs-lookup"><span data-stu-id="2f4bd-132">For more information about how to set up counters, see [Counters](../setup-for-objects/counters.md).</span></span>

