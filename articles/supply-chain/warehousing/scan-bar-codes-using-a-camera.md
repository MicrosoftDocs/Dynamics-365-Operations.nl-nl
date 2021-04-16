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
# <a name="scan-bar-codes-using-a-camera-in-the-warehouse-management-mobile-app"></a>Streepjescodes scannen met een camera in de mobiele app Magazijnbeheer

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de mobiele app Magazijnbeheer instelt voor het scannen van streepjescodes met een camera op een mobiel apparaat.

## <a name="setup"></a>Instelling

In de weergave-instellingen van de mobiele app Magazijnbeheer kunt u opgeven of de camera moet worden gebruikt voor het scannen van streepjescodes. Als u **De camera gebruiken als scanner** inschakelt, kunt u de camera gebruiken voor elk invoerveld waarvoor **Scannen** is ingesteld als voorkeursmethode voor invoer.

U bepaalt of een invoerveld te scannen moet zijn door op de pagina **Veldnamen van Warehouse-app** de **Geprefereerde invoermethode** in te stellen op **Scannen**. Wanneer deze optie is geselecteerd, kan een camera als scanner worden gebruikt in de mobiele app Magazijnbeheer. Zie [Velden configureren voor de mobiele app Magazijnbeheer](configure-app-field-names-priorities-warehouse.md) voor meer informatie.

## <a name="supported-bar-code-formats"></a>Ondersteunde indelingen voor streepjescodes

De meest gangbare streepjescode-indelingen worden ondersteund, waaronder Code 128, Code 39, Code 93, EAN-8, EAN-13, UPC-E, UPC-A en QR-codes.

## <a name="navigation"></a>Navigatie

De camerapagina wordt gestart op elke pagina waarop *Scannen* is ingesteld als de **geprefereerde invoermodus**. Gebruik op de camerapagina de volgende opties om te navigeren:

- Selecteer de knop Vorige om terug te gaan naar de pagina **Taak en details**.
- Selecteer het potlood op de pagina **Taak en details** om naar de pagina te gaan waarop u invoer handmatig kunt invoeren.
- Selecteer de camera op de pagina **Taak en details** om terug te gaan naar de camerapagina.

Wanneer u op de camerapagina de cameraknop selecteert, wordt deze grijs weergegeven terwijl wordt geprobeerd een streepjescode te identificeren. Als niet binnen vijf seconden een streepjescode wordt geïdentificeerd, vindt er een procestime-out plaats en wordt de cameraknop weer beschikbaar. Vervolgens kunt u opnieuw proberen een streepjescode te scannen.

Wanneer u de camera op een streepjescode richt, krijgt u de beste resultaten als u de streepjescode uitgelijnd binnen de haakjes houdt. Wanneer een streepjescode is gescand, wordt het resultaat verwerkt en gaat u verder met de volgende stap. Als de volgende stap weer een invoerveld met Scannen als geprefereerde invoermodus omvat, wordt de pagina Camera opnieuw gestart. Als de volgende stap geen scanveld omvat, wordt de pagina Camera niet gestart.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]