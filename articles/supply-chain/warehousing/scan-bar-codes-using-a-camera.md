---
title: Streepjescodes scannen met een camera in de Dynamics 365 Supply Chain Management - Warehousing-app
description: In dit onderwerp wordt uitgelegd hoe u Dynamics 365 Supply Chain Management – Warehousing-app instelt voor het scannen van streepjescodes met een camera op een mobiel apparaat.
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 8062a981f792bcfed2713d3cb6a42f414394f6a4
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251450"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-supply-chain-management---warehousing-app"></a><span data-ttu-id="d0768-103">Streepjescodes scannen met een camera in de Dynamics 365 Supply Chain Management - Warehousing-app</span><span class="sxs-lookup"><span data-stu-id="d0768-103">Scan bar codes using a camera in Dynamics 365 Supply Chain Management - Warehousing app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0768-104">In dit onderwerp wordt uitgelegd hoe u Dynamics 365 Supply Chain Management – Warehousing-app instelt voor het scannen van streepjescodes met een camera op een mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="d0768-104">This topic explains how to set up Dynamics 365 Supply Chain Management - Warehousing app to scan bar codes using a camera on a mobile device.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="d0768-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="d0768-105">Prerequisites</span></span>
<span data-ttu-id="d0768-106">Als u deze functie wilt gebruiken, moet u versie 1.2.0.0 van de Warehousing-app hebben geïnstalleerd en moet u over een apparaat met camera beschikken.</span><span class="sxs-lookup"><span data-stu-id="d0768-106">To use this feature, you need to have version 1.2.0.0 of the Warehousing app installed, and your device must have a camera.</span></span> <span data-ttu-id="d0768-107">Wanneer u de app opent nadat u deze hebt bijgewerkt, wordt u gevraagd om de app toe te staan de camera te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d0768-107">When you open the app after updating, you will be prompted to allow the app to use the camera.</span></span> <span data-ttu-id="d0768-108">Als uw apparaat geen camera heeft, wordt deze vraag niet weergegeven en kunt u geen camera als scanner gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d0768-108">If your device doesn’t have a camera, no prompt will be shown, and you will not be able to use a camera as a scanner.</span></span> 

## <a name="setup"></a><span data-ttu-id="d0768-109">Instelling</span><span class="sxs-lookup"><span data-stu-id="d0768-109">Setup</span></span>
<span data-ttu-id="d0768-110">In de weergave-instellingen van de toepassing Warehousing kunt u opgeven of de camera moet worden gebruikt voor het scannen van streepjescodes.</span><span class="sxs-lookup"><span data-stu-id="d0768-110">In the Display settings of the Warehousing application, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="d0768-111">Als u **De camera gebruiken als scanner** inschakelt, kunt u de camera gebruiken voor elk invoerveld waarvoor **Scannen** is ingesteld als voorkeursmethode voor invoer.</span><span class="sxs-lookup"><span data-stu-id="d0768-111">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span> 

<span data-ttu-id="d0768-112">U bepaalt of een invoerveld te scannen moet zijn door op de pagina **Veldnamen van Warehouse-app** de **Geprefereerde invoermethode** in te stellen op **Scannen**.</span><span class="sxs-lookup"><span data-stu-id="d0768-112">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="d0768-113">Wanneer deze optie is geselecteerd, kan een camera als scanner worden gebruikt in de app Warehousing.</span><span class="sxs-lookup"><span data-stu-id="d0768-113">When this option is selected, a camera can be used for scanning in the Warehousing app.</span></span> <span data-ttu-id="d0768-114">Zie [Veldnamen in magazijnapp configureren](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse) voor meer informatie over het configureren van appveldnamen in Warehousing.</span><span class="sxs-lookup"><span data-stu-id="d0768-114">For information about how to configure app field names in Warehousing, see [Configure app field names in Warehousing app](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="d0768-115">Ondersteunde indelingen voor streepjescodes</span><span class="sxs-lookup"><span data-stu-id="d0768-115">Supported bar code formats</span></span>
<span data-ttu-id="d0768-116">De meest gangbare streepjescode-indelingen worden ondersteund, waaronder Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A en QR-codes.</span><span class="sxs-lookup"><span data-stu-id="d0768-116">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span> 

## <a name="navigation"></a><span data-ttu-id="d0768-117">Navigatie</span><span class="sxs-lookup"><span data-stu-id="d0768-117">Navigation</span></span>
<span data-ttu-id="d0768-118">De camerapagina wordt gestart op elke pagina waarop Scannen is ingesteld als de geprefereerde invoermodus. Gebruik op de pagina Camera de volgende opties om te navigeren:</span><span class="sxs-lookup"><span data-stu-id="d0768-118">The camera page will be initiated on each page where the input field has the preferred input mode set to Scanning, when you are on the Camera page use the following options to navigate:</span></span>
- <span data-ttu-id="d0768-119">Klik op de knop Vorige om terug te gaan naar de pagina Taak en details.</span><span class="sxs-lookup"><span data-stu-id="d0768-119">Click the back button to go back to the Task and details page.</span></span> 
- <span data-ttu-id="d0768-120">Klik op het potlood op de pagina Taak en details om naar de pagina te gaan waarop u invoer handmatig kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="d0768-120">Click the pencil on the Task and details page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="d0768-121">Klik op de camera op de pagina Taak en details om terug te gaan naar de pagina Camera.</span><span class="sxs-lookup"><span data-stu-id="d0768-121">Click the camera on the Task and details page to go back to the Camera page.</span></span> 

| <span data-ttu-id="d0768-122">Pagina Taak en details</span><span class="sxs-lookup"><span data-stu-id="d0768-122">Task and details page</span></span> | <span data-ttu-id="d0768-123">Pagina Camera</span><span class="sxs-lookup"><span data-stu-id="d0768-123">Camera page</span></span> | 
| :---------------------: | :--------------------: |
| ![camera-scanning-example-task-detail-page](./media/camera-scanning-example-task-detail-page50.png)          | ![camera-scanning-example-camera-page-smaller](./media/camera-scanning-example-camera-page50.png)          |

<span data-ttu-id="d0768-126">Wanneer u op de pagina Camera op de knop Camera klikt, wordt deze grijs weergegeven terwijl wordt geprobeerd een streepjescode te identificeren.</span><span class="sxs-lookup"><span data-stu-id="d0768-126">On the camera page, when you click the Camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="d0768-127">Als niet binnen vijf seconden een streepjescode wordt geïdentificeerd, vindt er een procestime-out plaats en wordt de knop Camera weer beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="d0768-127">If a bar code is not identified within 5 seconds, the process will time out and the Camera button will become available again.</span></span> <span data-ttu-id="d0768-128">Vervolgens kunt u opnieuw proberen een streepjescode te scannen.</span><span class="sxs-lookup"><span data-stu-id="d0768-128">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="d0768-129">Wanneer u de camera op een streepjescode richt, krijgt u de beste resultaten als u de streepjescode uitgelijnd binnen de haakjes houdt.</span><span class="sxs-lookup"><span data-stu-id="d0768-129">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="d0768-130">Wanneer een streepjescode is gescand, wordt het resultaat verwerkt en gaat u verder met de volgende stap.</span><span class="sxs-lookup"><span data-stu-id="d0768-130">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="d0768-131">Als de volgende stap weer een invoerveld met Scannen als geprefereerde invoermodus omvat, wordt de pagina Camera opnieuw gestart.</span><span class="sxs-lookup"><span data-stu-id="d0768-131">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="d0768-132">Als de volgende stap geen scanveld omvat, wordt de pagina Camera niet gestart.</span><span class="sxs-lookup"><span data-stu-id="d0768-132">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>

