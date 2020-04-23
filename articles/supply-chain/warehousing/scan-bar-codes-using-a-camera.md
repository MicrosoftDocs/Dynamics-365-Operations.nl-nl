---
title: Streepjescodes scannen met een camera in de Dynamics 365 for Finance and Operations - Warehousing-app
description: In dit onderwerp wordt uitgelegd hoe u Dynamics 365 for Finance and Operations – Warehousing-app instelt voor het scannen van streepjescodes met een camera op een mobiel apparaat.
author: MarkusFogelberg
manager: tfehr
ms.date: 01/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSMobileAppField
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2017-01-03
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 9d3b807b18a0a9c7d24763a2a2a7ea9eccf9c2bb
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3205849"
---
# <a name="scan-bar-codes-using-a-camera-in-dynamics-365-supply-chain-management---warehousing-app"></a>Streepjescodes scannen met een camera in de Dynamics 365 Supply Chain Management - Warehousing-app

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u Dynamics 365 for Finance and Operations – Warehousing-app instelt voor het scannen van streepjescodes met een camera op een mobiel apparaat. 

## <a name="prerequisites"></a>Vereisten
Als u deze functie wilt gebruiken, moet u versie 1.2.0.0 van de Warehousing-app hebben geïnstalleerd en moet u over een apparaat met camera beschikken. Wanneer u de app opent nadat u deze hebt bijgewerkt, wordt u gevraagd om de app toe te staan de camera te gebruiken. Als uw apparaat geen camera heeft, wordt deze vraag niet weergegeven en kunt u geen camera als scanner gebruiken. 

## <a name="setup"></a>Instelling
In de weergave-instellingen van de toepassing Warehousing kunt u opgeven of de camera moet worden gebruikt voor het scannen van streepjescodes. Als u **De camera gebruiken als scanner** inschakelt, kunt u de camera gebruiken voor elk invoerveld waarvoor **Scannen** is ingesteld als voorkeursmethode voor invoer. 

U bepaalt of een invoerveld te scannen moet zijn door op de pagina **Veldnamen van Warehouse-app** de **Geprefereerde invoermethode** in te stellen op **Scannen**. Wanneer deze optie is geselecteerd, kan een camera als scanner worden gebruikt in de app Warehousing. Zie [Veldnamen in magazijnapp configureren](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/warehousing/configure-app-field-names-priorities-warehouse) voor meer informatie over het configureren van appveldnamen in Warehousing.

## <a name="supported-bar-code-formats"></a>Ondersteunde indelingen voor streepjescodes
De meest gangbare streepjescode-indelingen worden ondersteund, waaronder Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A en QR-codes. 

## <a name="navigation"></a>Navigatie
De camerapagina wordt gestart op elke pagina waarop Scannen is ingesteld als de geprefereerde invoermodus. Gebruik op de pagina Camera de volgende opties om te navigeren:
- Klik op de knop Vorige om terug te gaan naar de pagina Taak en details. 
- Klik op het potlood op de pagina Taak en details om naar de pagina te gaan waarop u invoer handmatig kunt invoeren.
- Klik op de camera op de pagina Taak en details om terug te gaan naar de pagina Camera. 

| Pagina Taak en details | Pagina Camera | 
| :---------------------: | :--------------------: |
| ![Camera die detailpagina van voorbeeldtaak scant](./media/camera-scanning-example-task-detail-page50.png)          | ![Voorbeeld van scannen met camera - kleinere camerapagina](./media/camera-scanning-example-camera-page50.png)          |

Wanneer u op de pagina Camera op de knop Camera klikt, wordt deze grijs weergegeven terwijl wordt geprobeerd een streepjescode te identificeren. Als niet binnen vijf seconden een streepjescode wordt geïdentificeerd, vindt er een procestime-out plaats en wordt de knop Camera weer beschikbaar. Vervolgens kunt u opnieuw proberen een streepjescode te scannen.

Wanneer u de camera op een streepjescode richt, krijgt u de beste resultaten als u de streepjescode uitgelijnd binnen de haakjes houdt. Wanneer een streepjescode is gescand, wordt het resultaat verwerkt en gaat u verder met de volgende stap. Als de volgende stap weer een invoerveld met Scannen als geprefereerde invoermodus omvat, wordt de pagina Camera opnieuw gestart. Als de volgende stap geen scanveld omvat, wordt de pagina Camera niet gestart.

