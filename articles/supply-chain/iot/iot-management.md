---
title: IoT-intelligentie controleren en beheren
description: In dit onderwerp wordt uitgelegd hoe u IoT-intelligentie kunt controleren en beheren.
author: robinarh
manager: tfehr
ms.date: 08/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-04-04
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 15021281b9ec33cd0552bca16e3054d0d3cdd589
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/14/2020
ms.locfileid: "3803060"
---
# <a name="monitor-and-manage-iot-intelligence"></a><span data-ttu-id="6695a-103">IoT-intelligentie controleren en beheren</span><span class="sxs-lookup"><span data-stu-id="6695a-103">Monitor and manage IoT Intelligence</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6695a-104">In dit onderwerp wordt uitgelegd hoe u IoT-intelligentie kunt controleren en beheren.</span><span class="sxs-lookup"><span data-stu-id="6695a-104">This topic explains how to monitor and manage IoT Intelligence.</span></span>

## <a name="monitor-scenarios-in-microsoft-dynamics-365-supply-chain-management"></a><a id="monitor-scenarios"></a><span data-ttu-id="6695a-105">Controlescenario's in Microsoft Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6695a-105">Monitor scenarios in Microsoft Dynamics 365 Supply Chain Management</span></span>

<span data-ttu-id="6695a-106">U kunt de IoT-intelligentie-verwerking vanaf verschillende locaties controleren:</span><span class="sxs-lookup"><span data-stu-id="6695a-106">You can monitor IoT Intelligence processing from several places:</span></span>

+ <span data-ttu-id="6695a-107">**Modules \> Productiebeheer \> Query's en rapporten \> IoT-intelligentie \> Meldingen** – De lijst met niet-opgeloste meldingen weergeven.</span><span class="sxs-lookup"><span data-stu-id="6695a-107">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Notifications** – View the list of unresolved notifications.</span></span>
+ <span data-ttu-id="6695a-108">**Modules \> Productiebeheer \> Query's en rapporten \> IoT-intelligentie \> Afgesloten meldingen** – De lijst bekijken met meldingen die zijn opgelost of afgewezen.</span><span class="sxs-lookup"><span data-stu-id="6695a-108">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Closed notifications** – View the list of notifications that have been resolved or dismissed.</span></span>
+ <span data-ttu-id="6695a-109">**Modules \> Productiebeheer \> Query's en rapporten \> IoT-intelligentie \> Metrische sleutels** – Bekijk de metrische sleutels voor de tijdreeksdiagrammen **Resourcestatus**.</span><span class="sxs-lookup"><span data-stu-id="6695a-109">**Modules \> Production control \> Inquiries and reports \> IoT Intelligence \> Metric keys** – View the metric keys for the **Resource Status** times series charts.</span></span>
+ <span data-ttu-id="6695a-110">**Modules \> Productiebeheer \> Productieregistratie \> Resource status** – Houd specifieke metrische gegevens bij met behulp van het dialoogvenster **Configureren**.</span><span class="sxs-lookup"><span data-stu-id="6695a-110">**Modules \> Production control \> Manufacturing execution \> Resource status** – Track specific metrics by using the **Configure** dialog box.</span></span> <span data-ttu-id="6695a-111">Als een scenario een uitzondering detecteert, worden de details van de uitzondering weergegeven in een melding.</span><span class="sxs-lookup"><span data-stu-id="6695a-111">If a scenario detects an exception, a notification shows the details of the exception.</span></span>
+ <span data-ttu-id="6695a-112">**Werkgebieden \> Productiebeheer \> Meldingen** – Bekijk de lijst met niet-opgeloste meldingen.</span><span class="sxs-lookup"><span data-stu-id="6695a-112">**Workspaces \> Production floor management \> Notifications** – View the list of unresolved notifications.</span></span>

## <a name="modify-a-running-iot-intelligence-scenario"></a><span data-ttu-id="6695a-113">Een actief IoT-intelligentie-scenario wijzigen</span><span class="sxs-lookup"><span data-stu-id="6695a-113">Modify a running IoT Intelligence scenario</span></span>

<span data-ttu-id="6695a-114">Wanneer een scenario wordt uitgevoerd, kunt u de volgende wijzigingen aanbrengen:</span><span class="sxs-lookup"><span data-stu-id="6695a-114">When a scenario is running, you can make these changes:</span></span>

+ <span data-ttu-id="6695a-115">Voeg nieuwe definities voor sensorschema's toe.</span><span class="sxs-lookup"><span data-stu-id="6695a-115">Add new sensor schema definitions.</span></span>
+ <span data-ttu-id="6695a-116">Selecteer nieuwe waarden voor signaalgegevens.</span><span class="sxs-lookup"><span data-stu-id="6695a-116">Select new signal data values.</span></span>
+ <span data-ttu-id="6695a-117">Annuleer de selectie van bestaande waarden voor signaalgegevens.</span><span class="sxs-lookup"><span data-stu-id="6695a-117">Cancel the selection of existing signal data values.</span></span>
+ <span data-ttu-id="6695a-118">Voeg nieuwe waarden voor signaalgegevens toe en wijs deze toe.</span><span class="sxs-lookup"><span data-stu-id="6695a-118">Add and map new signal data values.</span></span>
+ <span data-ttu-id="6695a-119">Werk drempelwaarden bij.</span><span class="sxs-lookup"><span data-stu-id="6695a-119">Update threshold values.</span></span>

<span data-ttu-id="6695a-120">Wanneer een scenario wordt uitgevoerd, zijn de volgende wijzigingen niet toegestaan:</span><span class="sxs-lookup"><span data-stu-id="6695a-120">When a scenario is running, these changes are prohibited:</span></span>

+ <span data-ttu-id="6695a-121">Schemadefinities die momenteel worden gebruikt in een ingeschakeld scenario verwijderen of wijzigen.</span><span class="sxs-lookup"><span data-stu-id="6695a-121">Delete or modify any schema definitions that are currently consumed by an enabled scenario.</span></span>
+ <span data-ttu-id="6695a-122">De geselecteerde schemapaden voor het ingeschakelde scenario wijzigen.</span><span class="sxs-lookup"><span data-stu-id="6695a-122">Change the enabled scenario's selected schema paths.</span></span>

## <a name="simulation-options"></a><span data-ttu-id="6695a-123">Simulatieopties</span><span class="sxs-lookup"><span data-stu-id="6695a-123">Simulation options</span></span>

<span data-ttu-id="6695a-124">U kunt de signalen van fabrieksmachines simuleren.</span><span class="sxs-lookup"><span data-stu-id="6695a-124">You can simulate factory machine signals.</span></span> <span data-ttu-id="6695a-125">Voor meer informatie wordt verwezen naar deze onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="6695a-125">For more information, see these topics:</span></span>

+ [<span data-ttu-id="6695a-126">IoT DevKit AZ3166 verbinden met Azure IoT-hub</span><span class="sxs-lookup"><span data-stu-id="6695a-126">Connect IoT DevKit AZ3166 to Azure IoT Hub</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-arduino-iot-devkit-az3166-get-started)
+ [<span data-ttu-id="6695a-127">Raspberry Pi online simulator verbinden met Azure IoT-hub (Node.js)</span><span class="sxs-lookup"><span data-stu-id="6695a-127">Connect Raspberry Pi online simulator to Azure IoT Hub (Node.js)</span></span>](https://docs.microsoft.com/azure/iot-hub/iot-hub-raspberry-pi-web-simulator-get-started)
+ [<span data-ttu-id="6695a-128">Overzicht van oplossingsversneller voor apparaatsimulatie</span><span class="sxs-lookup"><span data-stu-id="6695a-128">Device Simulation solution accelerator overview</span></span>](https://docs.microsoft.com/azure/iot-accelerators/iot-accelerators-device-simulation-overview)
