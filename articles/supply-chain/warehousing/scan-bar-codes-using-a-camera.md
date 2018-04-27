---
title: "Streepjescodes scannen met een camera in Dynamics 365 for Finance and Operations – Warehousing"
description: "In dit onderwerp wordt uitgelegd hoe u Dynamics 365 for Finance and Operations – Warehousing instelt voor het scannen van streepjescodes met een camera op een mobiel apparaat."
author: MarkusFogelberg
manager: AnnBe
ms.date: 01/03/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: f7fe3ab07578b09822fbfeaa4b07331b79f13610
ms.contentlocale: nl-nl
ms.lasthandoff: 03/09/2018

---

# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-for-finance-and-operations--warehousing"></a>Streepjescodes scannen met een camera in Dynamics 365 for Finance and Operations – Warehousing

[!INCLUDE [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u Dynamics 365 for Finance and Operations – Warehousing instelt voor het scannen van streepjescodes met een camera op een mobiel apparaat. 

## <a name="prerequisites"></a>Vereisten
Als u deze functie wilt gebruiken, moet u versie 1.2.0.0 van Warehousing hebben geïnstalleerd en moet u over een apparaat met camera beschikken. Wanneer u de app opent nadat u hebt bijgewerkt, wordt u gevraagd om de toepassing Dynamics 365 for Finance and Operations – Warehousing toe te staan de camera te gebruiken. Als uw apparaat geen camera heeft, wordt deze vraag niet weergegeven en kunt u geen camera als scanner gebruiken. 

## <a name="setup"></a>Instelling
In de weergave-instellingen van de toepassing Warehousing kunt u opgeven of de camera moet worden gebruikt voor het scannen van streepjescodes. Als u **De camera gebruiken als scanner** inschakelt, kunt u de camera gebruiken voor elk invoerveld waarvoor **Scannen** is ingesteld als voorkeursmethode voor invoer. 

U bepaalt of een invoerveld te scannen moet zijn door op de pagina **Veldnamen van magazijnapp** in Dynamics 365 for Finance and Operations **Geprefereerde invoermethode** in te stellen op **Scannen**. Wanneer deze optie is geselecteerd, kan een camera als scanner worden gebruikt in de app Warehousing. Zie [Veldnamen in magazijnapp configureren](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse) voor meer informatie over het configureren van appveldnamen in Warehousing.

## <a name="supported-bar-code-formats"></a>Ondersteunde indelingen voor streepjescodes
De meest gangbare streepjescode-indelingen worden ondersteund, waaronder Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A en QR-codes. 

## <a name="navigation"></a>Navigatie
De camerapagina wordt gestart op elke pagina waarop Scannen is ingesteld als de geprefereerde invoermodus. Gebruik op de pagina Camera de volgende opties om te navigeren:
- Klik op de knop Vorige om terug te gaan naar de pagina Taak en details. 
- Klik op het potlood op de pagina Taak en details om naar de pagina te gaan waarop u invoer handmatig kunt invoeren.
- Klik op de camera op de pagina Taak en details om terug te gaan naar de pagina Camera. 

| Pagina Taak en details | Pagina Camera | 
| :---------------------: | :--------------------: |
| ![camera-scanning-example-task-detail-page](./media/camera-scanning-example-task-detail-page50.png)          | ![camera-scanning-example-camera-page-smaller](./media/camera-scanning-example-camera-page50.png)          |

Wanneer u op de pagina Camera op de knop Camera klikt, wordt deze grijs weergegeven terwijl wordt geprobeerd een streepjescode te identificeren. Als niet binnen vijf seconden een streepjescode wordt geïdentificeerd, vindt er een procestime-out plaats en wordt de knop Camera weer beschikbaar. Vervolgens kunt u opnieuw proberen een streepjescode te scannen.

Wanneer u de camera op een streepjescode richt, krijgt u de beste resultaten als u de streepjescode uitgelijnd binnen de haakjes houdt. Wanneer een streepjescode is gescand, wordt het resultaat verwerkt en gaat u verder met de volgende stap. Als de volgende stap weer een invoerveld met Scannen als geprefereerde invoermodus omvat, wordt de pagina Camera opnieuw gestart. Als de volgende stap geen scanveld omvat, wordt de pagina Camera niet gestart.


