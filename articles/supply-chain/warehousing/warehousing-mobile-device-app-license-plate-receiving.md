---
title: Nummerplaat ontvangen via de Warehouse Mobile App
description: In dit onderwerp wordt uitgelegd hoe u de Warehouse Mobile App kunt instellen om het ontvangstproces met nummerplaat in de fysieke voorraad te ondersteunen.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 98cd608edea1d5365d0d3532244f1fcdb6293d3c
ms.sourcegitcommit: 3a823444005d316bd95fc663e2dbc8252ac7d93a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261318"
---
# <a name="license-plate-receiving-via-the-warehousing-mobile-app"></a><span data-ttu-id="83b22-103">Nummerplaat ontvangen via de Warehouse Mobile App</span><span class="sxs-lookup"><span data-stu-id="83b22-103">License plate receiving via the Warehousing mobile app</span></span>

<span data-ttu-id="83b22-104">In dit onderwerp wordt uitgelegd hoe u de Warehouse Mobile App kunt instellen om het ontvangstproces met nummerplaat in de fysieke voorraad te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="83b22-104">This topic explains how to set up the Warehousing mobile app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="83b22-105">Met deze functie kunt u snel de ontvangst van de inkomende voorraad vastleggen die is gerelateerd aan een voorschotbericht (advance shipping notice, ASN).</span><span class="sxs-lookup"><span data-stu-id="83b22-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="83b22-106">Het systeem maakt automatisch een ASN wanneer magazijnbeheerprocessen worden gebruikt om een transferorder te verzenden.</span><span class="sxs-lookup"><span data-stu-id="83b22-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="83b22-107">Voor het inkooporderproces kan een ASN handmatig worden vastgelegd of kan deze automatisch worden geïmporteerd met behulp van een inkomend ASN-gegevensentiteitproces.</span><span class="sxs-lookup"><span data-stu-id="83b22-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="83b22-108">De ASN-gegevens worden gekoppeld aan ladingen en zendingen via *de verpakkingsstructuren*, waarbij pallets (bovenliggende nummerplaten) dozen kunnen bevatten (geneste nummerplaten).</span><span class="sxs-lookup"><span data-stu-id="83b22-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="83b22-109">Om het aantal voorraadtransacties te verminderen wanneer de verpakkingsstructuren met geneste nummerplaten worden gebruikt, registreert het systeem de fysieke voorhanden voorraad op de bovenliggende nummerplaat.</span><span class="sxs-lookup"><span data-stu-id="83b22-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="83b22-110">Om de verplaatsing van de fysieke voorhanden voorraad van de bovenliggende nummerplaat naar de geneste nummerplaat te activeren, op basis van de verpakkingsstructuurgegevens, moet het mobiele apparaat een menuopdracht geven die is gebaseerd op het werkaanmaakproces *Verpakken naar geneste nummerplaten*.</span><span class="sxs-lookup"><span data-stu-id="83b22-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="83b22-111">De pagina met het ontvangstoverzicht weergeven of overslaan</span><span class="sxs-lookup"><span data-stu-id="83b22-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="83b22-112">U kunt de functie *Bepalen of de pagina met het ontvangstoverzicht wordt weergegeven op mobiele apparaten* gebruiken om te profiteren van de extra gedetailleerde magazijnbeheer-appstroom als onderdeel van het nummerplaatontvangstproces.</span><span class="sxs-lookup"><span data-stu-id="83b22-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed Warehouse app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="83b22-113">Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="83b22-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="83b22-114">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="83b22-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="83b22-115">Schakel in het werkgebied **Functiebeheer** deze functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="83b22-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="83b22-116">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="83b22-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="83b22-117">**Functienaam:** *Bepalen of de pagina met het ontvangstoverzicht wordt weergegeven op mobiele apparaten*</span><span class="sxs-lookup"><span data-stu-id="83b22-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="83b22-118">Als deze functie is ingeschakeld, bevatten de menuopdrachten van het mobiele apparaat voor het ontvangen en opslaan van nummerplaten de instelling **Pagina met het ontvangstoverzicht weergeven**.</span><span class="sxs-lookup"><span data-stu-id="83b22-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="83b22-119">Deze instelling heeft de volgende opties:</span><span class="sxs-lookup"><span data-stu-id="83b22-119">This setting has the following options:</span></span>

- <span data-ttu-id="83b22-120">**Een gedetailleerd overzicht weergeven**: tijdens het ontvangen van een nummerplaat krijgen de werknemers een extra pagina te zien waarop de volledige ASN-informatie wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="83b22-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="83b22-121">**Het overzicht overslaan**: werknemers kunnen de volledige ASN-informatie niet zien.</span><span class="sxs-lookup"><span data-stu-id="83b22-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="83b22-122">Magazijnmedewerkers kunnen ook geen beschikkingscode instellen of uitzonderingen toevoegen tijdens het ontvangstproces.</span><span class="sxs-lookup"><span data-stu-id="83b22-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="83b22-123">Verhinderen dat met transferorder verzonden nummerplaten worden gebruikt voor andere magazijnen dan het doelmagazijn</span><span class="sxs-lookup"><span data-stu-id="83b22-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="83b22-124">Een ontvangstproces voor een nummerplaat kan niet worden gebruikt als een ASN een nummerplaat-id bevat die al bestaat en fysieke voorraadgegevens bevat op een magazijnlocatie anders dan de magazijnlocatie waar de nummerplaatregistratie wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="83b22-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="83b22-125">Voor transferorderscenario's waarbij het transitmagazijn geen nummerplaten volgt (en dus ook geen fysieke voorhanden voorraad per nummerplaat bijhoudt), kunt u de functie *Verhinderen dat met transferorder verzonden nummerplaten worden gebruikt voor andere magazijnen dan het doelmagazijn* gebruiken om fysieke voorraadupdates te voorkomen in nummerplaten in transit.</span><span class="sxs-lookup"><span data-stu-id="83b22-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="83b22-126">Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem.</span><span class="sxs-lookup"><span data-stu-id="83b22-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="83b22-127">Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="83b22-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="83b22-128">Schakel in het werkgebied **Functiebeheer** deze functie als volgt in:</span><span class="sxs-lookup"><span data-stu-id="83b22-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="83b22-129">**Module:** *Magazijnbeheer*</span><span class="sxs-lookup"><span data-stu-id="83b22-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="83b22-130">**Functienaam:** *Verhinderen dat met transferorder verzonden nummerplaten worden gebruikt voor andere magazijnen dan het doelmagazijn*</span><span class="sxs-lookup"><span data-stu-id="83b22-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="83b22-131">Voer de volgende stappen uit om de functionaliteit te beheren wanneer deze functie beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="83b22-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="83b22-132">Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.</span><span class="sxs-lookup"><span data-stu-id="83b22-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="83b22-133">Stel op het tabblad **Algemeen** op het sneltabblad **Nummerplaten** het veld **Beleid voor nummerplaten transitmagazijn** in op een van de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="83b22-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="83b22-134">**Hergebruik toestaan van niet-getraceerde nummerplaat**: het systeem werkt op dezelfde manier als wanneer functie de *Verhinderen dat met transferorder verzonden nummerplaten worden gebruikt voor andere magazijnen dan het doelmagazijn* niet beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="83b22-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="83b22-135">Deze waarde is de standaardinstelling wanneer u de functie voor het eerst activeert.</span><span class="sxs-lookup"><span data-stu-id="83b22-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="83b22-136">**Hergebruik verhinderen van niet-getraceerde nummerplaat**: alleen voorhanden updates die zijn gerelateerd aan een geleverde nummerplaat worden toegestaan in het doelmagazijn totdat de transferorder is ontvangen.</span><span class="sxs-lookup"><span data-stu-id="83b22-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="83b22-137">Meer informatie</span><span class="sxs-lookup"><span data-stu-id="83b22-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="83b22-138">Zie [Mobiele apparaten instellen voor magazijnwerk](configure-mobile-devices-warehouse.md) voor meer informatie over menuopties voor mobiele apparaten.</span><span class="sxs-lookup"><span data-stu-id="83b22-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
