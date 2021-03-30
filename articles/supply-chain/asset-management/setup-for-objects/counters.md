---
title: Activummetingen
description: In dit onderwerp wordt uitgelegd hoe u metingtypen voor activa maakt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 41bedaaace09f632ca7506f504c3086a1dabf193
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217144"
---
# <a name="counters"></a><span data-ttu-id="b793c-103">Tellers</span><span class="sxs-lookup"><span data-stu-id="b793c-103">Counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b793c-104">In dit onderwerp wordt uitgelegd hoe u tellertypen maakt in Activabeheer.</span><span class="sxs-lookup"><span data-stu-id="b793c-104">The topic explains how to create counter types in Asset Management.</span></span> <span data-ttu-id="b793c-105">Tellertypen worden gebruikt om tellerregistraties te maken voor activa, bijvoorbeeld met betrekking tot het aantal productie-uren of de hoeveelheid die op het activum wordt geproduceerd.</span><span class="sxs-lookup"><span data-stu-id="b793c-105">Counter types are used to make counter registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="b793c-106">De activatypen zijn gerelateerd aan de tellertypen.</span><span class="sxs-lookup"><span data-stu-id="b793c-106">Asset types are related to the counter types.</span></span> <span data-ttu-id="b793c-107">Dit betekent dat een teller alleen voor een activum kan worden gebruikt als de teller is ingesteld voor het activumtype dat met het activum wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b793c-107">This means that a counter can only be used on an asset if the counter is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="b793c-108">Voordat u tellerregistraties voor activa kunt maken, maakt u in **Tellers** eerst de tellertypen die u wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b793c-108">Before you can make counter registrations on assets, you first create the counter types you want to use in **Counters**.</span></span> <span data-ttu-id="b793c-109">Vervolgens kunt u tellerregistraties voor activa maken in **Tellers**.</span><span class="sxs-lookup"><span data-stu-id="b793c-109">Next, you can create counter registrations on assets in **Counters**.</span></span> 

<span data-ttu-id="b793c-110">Tellers kunnen worden gebruikt in onderhoudsplannen.</span><span class="sxs-lookup"><span data-stu-id="b793c-110">Counters can be used on maintenance plans.</span></span> <span data-ttu-id="b793c-111">Een onderhoudsplanregel kan van het type "Teller" zijn, bijvoorbeeld als het gaat om het aantal productie-uren of de geproduceerde hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="b793c-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="b793c-112">Een tellerregistratie kan handmatig of automatisch worden bijgewerkt op basis van productie-uren of de geproduceerde hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="b793c-112">A counter registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="b793c-113">Een teller kan worden ingesteld voor het gebruiken van een van deze drie bijwerkmethoden (geselecteerd in het veld **Bijwerken** in **Tellers**):</span><span class="sxs-lookup"><span data-stu-id="b793c-113">A counter can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="b793c-114">Handmatig: u moet de waarden van de teller handmatig registreren.</span><span class="sxs-lookup"><span data-stu-id="b793c-114">Manual - you must manually register counter values.</span></span>  
- <span data-ttu-id="b793c-115">Productie-uren: de teller wordt automatisch bijgewerkt op basis van het aantal productie-uren.</span><span class="sxs-lookup"><span data-stu-id="b793c-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="b793c-116">Productiehoeveelheid: de teller wordt automatisch bijgewerkt op basis van de geproduceerde hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="b793c-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="b793c-117">Als geproduceerde hoeveelheid wordt gebruikt, worden *alle* geregistreerde artikelen opgenomen in de tellerregistratie, zowel de goede artikelen als artikelen met fouten.</span><span class="sxs-lookup"><span data-stu-id="b793c-117">If quantity produced is used, *all* registered items are included in the counter registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="b793c-118">Het is altijd mogelijk om een handmatige registratie van de tellers te doen, als dat nodig is.</span><span class="sxs-lookup"><span data-stu-id="b793c-118">It is always possible to make manual counter registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="b793c-119">Tellertypen maken voor registraties van activatellers</span><span class="sxs-lookup"><span data-stu-id="b793c-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="b793c-120">Selecteer **Activabeheer** > **Instellen** > **Activumtypen** > **Tellers**.</span><span class="sxs-lookup"><span data-stu-id="b793c-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="b793c-121">Selecteer **Nieuw** om een nieuw tellertype te maken.</span><span class="sxs-lookup"><span data-stu-id="b793c-121">Select **New** to create a new counter type.</span></span>
3. <span data-ttu-id="b793c-122">Geef een id op in het veld **Teller** en een tellernaam in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="b793c-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="b793c-123">Selecteer op het sneltabblad **Algemeen** een tellereenheid in het veld **Eenheid**.</span><span class="sxs-lookup"><span data-stu-id="b793c-123">On the **General** FastTab, select a counter unit in the **Unit** field.</span></span>
5. <span data-ttu-id="b793c-124">Selecteer in het veld **Bijwerken** de bijwerkmethode die voor de teller moet worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b793c-124">In the **Update** field, select the update method to be used for the counter.</span></span>
6. <span data-ttu-id="b793c-125">Selecteer "Ja" op de wisselknop **Tellerwaarden overnemen** als onderliggende activa in een activastructuur automatisch tellerregistraties moeten overnemen van het bovenliggende activum.</span><span class="sxs-lookup"><span data-stu-id="b793c-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit counter registrations made on the parent asset.</span></span>
7. <span data-ttu-id="b793c-126">Selecteer in het veld **Totaal samengevoegd** de totaliseringsmethode die moet worden gebruikt voor een teller met dit tellertype.</span><span class="sxs-lookup"><span data-stu-id="b793c-126">In the **Total aggregate** field, select the summation method to be used for a counter using this counter type.</span></span> <span data-ttu-id="b793c-127">"Totaal" is de standaardselectie die wordt gebruikt om voortdurend geregistreerde waarden aan de totale waarde toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b793c-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="b793c-128">"Gemiddelde" kan worden gebruikt als een teller is ingesteld om een drempel te bewaken, bijvoorbeeld met betrekking tot temperatuur, trillingen of slijtage van een activum.</span><span class="sxs-lookup"><span data-stu-id="b793c-128">"Average" can be used if a counter is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="b793c-129">In het veld **Afwijking boven** voegt u in procenten het hoogste niveau voor validatie in als handmatige tellerregistraties binnen een verwacht bereik liggen.</span><span class="sxs-lookup"><span data-stu-id="b793c-129">In the **Deviation over** field, insert the upper level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="b793c-130">De validatie is gebaseerd op een lineaire toename van bestaande tellerregistraties.</span><span class="sxs-lookup"><span data-stu-id="b793c-130">The validation is based on a linear increase in existing counter registrations.</span></span>
9. <span data-ttu-id="b793c-131">In het veld **Afwijking onder** voegt u in procenten het laagste niveau voor validatie in als handmatige tellerregistraties binnen een verwacht bereik liggen.</span><span class="sxs-lookup"><span data-stu-id="b793c-131">In the **Deviation under** field, insert the lower level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="b793c-132">De validatie is gebaseerd op een lineaire afname van bestaande tellerregistraties.</span><span class="sxs-lookup"><span data-stu-id="b793c-132">The validation is based on a linear decrease in existing counter registrations.</span></span>
10. <span data-ttu-id="b793c-133">Selecteer in het veld **Type** het type bericht (informatie, waarschuwing, fout) dat moet worden weergegeven als afwijkingen buiten het gedefinieerde bereik optreden bij handmatige tellerregistraties.</span><span class="sxs-lookup"><span data-stu-id="b793c-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual counter registrations.</span></span>
11. <span data-ttu-id="b793c-134">Voeg op het sneltabblad **Activumtypen** de activumtypen toe die de teller kunnen gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b793c-134">On the **Asset types** FastTab, add the asset types that should be able to use the counter.</span></span>
12. <span data-ttu-id="b793c-135">Voeg op het sneltabblad **Gerelateerde activumtellers** de teller toe die u automatisch wilt bijwerken wanneer deze teller wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="b793c-135">On the **Related asset counters** FastTab, add the counter that you want to be automatically updated when this counter is updated.</span></span>


>[!NOTE]
><span data-ttu-id="b793c-136">Een gerelateerde activummeting wordt alleen automatisch bijgewerkt als voor de bijbehorende teller het activumtype, waaraan deze is gerelateerd, is vermeld in de instellingen voor de teller.</span><span class="sxs-lookup"><span data-stu-id="b793c-136">A related counter is automatically updated only if the related counter has the asset type, to which it is related, in the counter setup.</span></span> <span data-ttu-id="b793c-137">Bijvoorbeeld: u stelt een teller in voor "Productie-uren" en voegt het activumtype "Truckmotor" toe.</span><span class="sxs-lookup"><span data-stu-id="b793c-137">For example: You set up a counter for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="b793c-138">Wanneer de teller wordt bijgewerkt, wordt een samenhangende teller "Olie" ook bijgewerkt met dezelfde tellerwaarden.</span><span class="sxs-lookup"><span data-stu-id="b793c-138">When that counter is updated, a related counter "Oil" is also updated with the same counter values.</span></span> <span data-ttu-id="b793c-139">De instellingen in **Tellers** omvatten de instellingen voor "Uren".</span><span class="sxs-lookup"><span data-stu-id="b793c-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="b793c-140">Ook moet voor de teller "Olie" het activumtype "Truckmotor" worden toegevoegd aan het sneltabblad **Activumtypen** om de relatie met de teller te garanderen.</span><span class="sxs-lookup"><span data-stu-id="b793c-140">Also, on the "Oil" counter, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the counter relation.</span></span> <span data-ttu-id="b793c-141">Zie de onderstaande schermafbeeldingen voor een voorbeeld van de instellingen voor de tellers voor Uren en Olie.</span><span class="sxs-lookup"><span data-stu-id="b793c-141">See the screenshots below for an example of the setup on the Hours and Oil counters.</span></span>

<span data-ttu-id="b793c-142">Wanneer activumtypen worden toegevoegd aan een teller van het type **Tellers**, wordt die teller automatisch toegevoegd aan de activumtypen op het sneltabblad **Tellers** in [Activumtypen](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="b793c-142">When asset types are added to a counter type in **Counters**, that counter is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![Figuur 1](media/071-setup-for-objects.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]