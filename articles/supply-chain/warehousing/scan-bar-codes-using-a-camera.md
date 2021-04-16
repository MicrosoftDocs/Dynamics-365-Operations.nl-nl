---
title: Streepjescodes scannen met een camera in de mobiele app Magazijnbeheer
description: In dit onderwerp wordt uitgelegd hoe u de mobiele app Magazijnbeheer instelt voor het scannen van streepjescodes met een camera op een mobiel apparaat.
author: MarkusFogelberg
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2f61f9c45b95b730a7f1743963658ec00abfbb56
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831213"
---
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a><span data-ttu-id="2a75f-103">Streepjescodes scannen met een camera in de mobiele app Magazijnbeheer</span><span class="sxs-lookup"><span data-stu-id="2a75f-103">Scan bar codes using a camera in the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a75f-104">In dit onderwerp wordt uitgelegd hoe u de mobiele app Magazijnbeheer instelt voor het scannen van streepjescodes met een camera op een mobiel apparaat.</span><span class="sxs-lookup"><span data-stu-id="2a75f-104">This topic explains how to set up the Warehouse Management mobile app to scan bar codes using a camera on a mobile device.</span></span>

## <a name="setup"></a><span data-ttu-id="2a75f-105">Instelling</span><span class="sxs-lookup"><span data-stu-id="2a75f-105">Setup</span></span>

<span data-ttu-id="2a75f-106">In de weergave-instellingen van de mobiele app Magazijnbeheer kunt u opgeven of de camera moet worden gebruikt voor het scannen van streepjescodes.</span><span class="sxs-lookup"><span data-stu-id="2a75f-106">In the display settings of the Warehouse Management mobile app, you can select if the camera should be used for bar code scanning.</span></span> <span data-ttu-id="2a75f-107">Als u **De camera gebruiken als scanner** inschakelt, kunt u de camera gebruiken voor elk invoerveld waarvoor **Scannen** is ingesteld als voorkeursmethode voor invoer.</span><span class="sxs-lookup"><span data-stu-id="2a75f-107">If you enable **Use the camera as scanner**, you can use the camera on every input field that has the preferred input mode set to **Scanning**.</span></span>

<span data-ttu-id="2a75f-108">U bepaalt of een invoerveld te scannen moet zijn door op de pagina **Veldnamen van Warehouse-app** de **Geprefereerde invoermethode** in te stellen op **Scannen**.</span><span class="sxs-lookup"><span data-stu-id="2a75f-108">To control whether an input field should be scannable, on the **Warehouse app field names** page, set **Preferred input mode** to **Scanning**.</span></span> <span data-ttu-id="2a75f-109">Wanneer deze optie is geselecteerd, kan een camera als scanner worden gebruikt in de mobiele app Magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="2a75f-109">When this option is selected, a camera can be used for scanning in the Warehouse Management mobile app.</span></span> <span data-ttu-id="2a75f-110">Zie [Velden configureren voor de mobiele app Magazijnbeheer](configure-app-field-names-priorities-warehouse.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="2a75f-110">For more information, see [Configure fields for the Warehouse Management mobile app](configure-app-field-names-priorities-warehouse.md).</span></span>

## <a name="supported-bar-code-formats"></a><span data-ttu-id="2a75f-111">Ondersteunde indelingen voor streepjescodes</span><span class="sxs-lookup"><span data-stu-id="2a75f-111">Supported bar code formats</span></span>

<span data-ttu-id="2a75f-112">De meest gangbare streepjescode-indelingen worden ondersteund, waaronder Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A en QR-codes.</span><span class="sxs-lookup"><span data-stu-id="2a75f-112">The most common bar code formats are supported, including Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A, and QR codes.</span></span>

## <a name="navigation"></a><span data-ttu-id="2a75f-113">Navigatie</span><span class="sxs-lookup"><span data-stu-id="2a75f-113">Navigation</span></span>

<span data-ttu-id="2a75f-114">De camerapagina wordt gestart op elke pagina waarop *Scannen* is ingesteld als de **geprefereerde invoermodus**. Gebruik op de camerapagina de volgende opties om te navigeren:</span><span class="sxs-lookup"><span data-stu-id="2a75f-114">The camera page will be initiated on each page where the input field has its **Preferred input mode** set to *Scanning*, when you are on the camera page use the following options to navigate:</span></span>

- <span data-ttu-id="2a75f-115">Selecteer de knop Vorige om terug te gaan naar de pagina **Taak en details**.</span><span class="sxs-lookup"><span data-stu-id="2a75f-115">Select the back button to go back to the **Task and details** page.</span></span>
- <span data-ttu-id="2a75f-116">Selecteer het potlood op de pagina **Taak en details** om naar de pagina te gaan waarop u invoer handmatig kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="2a75f-116">Select the pencil on the **Task and details** page to go to the page where you can type input manually.</span></span>
- <span data-ttu-id="2a75f-117">Selecteer de camera op de pagina **Taak en details** om terug te gaan naar de camerapagina.</span><span class="sxs-lookup"><span data-stu-id="2a75f-117">Select the camera on the **Task and details** page to go back to the camera page.</span></span>

<span data-ttu-id="2a75f-118">Wanneer u op de camerapagina de cameraknop selecteert, wordt deze grijs weergegeven terwijl wordt geprobeerd een streepjescode te identificeren.</span><span class="sxs-lookup"><span data-stu-id="2a75f-118">On the camera page, when you select the camera button, it will appear dimmed while trying to identify a bar code.</span></span> <span data-ttu-id="2a75f-119">Als niet binnen vijf seconden een streepjescode wordt geïdentificeerd, vindt er een procestime-out plaats en wordt de cameraknop weer beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="2a75f-119">If a bar code is not identified within 5 seconds, the process will time out and the camera button will become available again.</span></span> <span data-ttu-id="2a75f-120">Vervolgens kunt u opnieuw proberen een streepjescode te scannen.</span><span class="sxs-lookup"><span data-stu-id="2a75f-120">You will then be able to try to scan a bar code again.</span></span>

<span data-ttu-id="2a75f-121">Wanneer u de camera op een streepjescode richt, krijgt u de beste resultaten als u de streepjescode uitgelijnd binnen de haakjes houdt.</span><span class="sxs-lookup"><span data-stu-id="2a75f-121">When you aim the camera at a bar code, keep the bar code aligned within the brackets for best result.</span></span> <span data-ttu-id="2a75f-122">Wanneer een streepjescode is gescand, wordt het resultaat verwerkt en gaat u verder met de volgende stap.</span><span class="sxs-lookup"><span data-stu-id="2a75f-122">When a bar code is scanned successfully, the result will be processed, and you will be taken to the next step.</span></span> <span data-ttu-id="2a75f-123">Als de volgende stap weer een invoerveld met Scannen als geprefereerde invoermodus omvat, wordt de pagina Camera opnieuw gestart.</span><span class="sxs-lookup"><span data-stu-id="2a75f-123">If the next step contains another input field with the preferred input mode set to Scanning, the camera page will start again.</span></span> <span data-ttu-id="2a75f-124">Als de volgende stap geen scanveld omvat, wordt de pagina Camera niet gestart.</span><span class="sxs-lookup"><span data-stu-id="2a75f-124">If the next step is not a scanning field, then the camera page will not be initiated.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]