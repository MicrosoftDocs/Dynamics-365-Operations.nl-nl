---
title: Overzicht van Ladingen plannen via hubconsolidatie
description: In dit artikel wordt de functie beschreven voor het consolideren van zendingen in een hub bij het leveren van goederen vanuit verschillende magazijnen aan dezelfde klant, of wanneer u goederen ontvangt van meerdere leveranciers in hetzelfde magazijn.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSHistory, WHSLoadTable, WHSLoadPlanningListPage, TMSParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d61527113746e76889d097e963f70ced24fd241
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425836"
---
# <a name="plan-loads-using-hub-consolidation-overview"></a>Overzicht van Ladingen plannen via hubconsolidatie

[!include [banner](../includes/banner.md)]

In dit artikel wordt de functie beschreven voor het consolideren van zendingen in een hub bij het leveren van goederen vanuit verschillende magazijnen aan dezelfde klant, of wanneer u goederen ontvangt van meerdere leveranciers in hetzelfde magazijn.

Kan het handig zijn om zendingen te consolideren in een hub bij het leveren van goederen vanuit verschillende magazijnen aan dezelfde klant, of wanneer goederen van meerdere leveranciers aan het magazijn worden geleverd.

## <a name="building-loads"></a>Ladingen opbouwen
Voordat u de hubconsolidatie kunt gebruiken, moet u de optie **Planning in transit** inschakelen op de pagina **Transportbeheerparameters**. Ook moet u de hubs maken waar de consolidatie zal plaatsvinden. In het volgende diagram ziet u een voorbeeld van hubconsolidatie. In dit geval gaan verkooporders uit verschillende magazijnen naar dezelfde klant. De basisladingen worden op de gebruikelijke manier gemaakt op basis van verkooporders met behulp van de pagina **Workbench ladingplanning**. Als u de twee ladingen wilt samenvoegen in een hub voordat ze aan de klant worden geleverd, selecteert u op de pagina **Workbench ladingplanning**, in het veld **Transport**, de optie **Hubconsolidatie**. Wanneer u de juiste hub selecteert voor elke lading, hebben de ladingen de hub als afleverbestemming. Ook hebt u twee "aanvraagregels van transport" in de sectie **Vraag en aanbod** van de pagina **Workbench ladingplanning**. Vervolgens kunt u deze twee lijnen toevoegen aan een nieuwe lading. Deze nieuwe lading bevat beide verkooporderregels en bevat ook de hub als ophaaladres en klant A als afleverbestemming. De drie ladingen zijn vervolgens gereed om te worden beoordeeld en doorgestuurd, net als elke andere lading. U kunt voor elke lading iedere vervoerder selecteren die in het systeem wordt voorgesteld. [![Hubconsolidatie](./media/hubconsol.jpg)](./media/hubconsol.jpg) U kunt dezelfde methode ook gebruiken voor het consolideren van ladingen voor meerdere transferorders. In dit geval is klant A in het voorgaande diagram een magazijn. U kunt ook ladingen samenvoegen voor meerdere inkooporders, waarbij de ladingen door verschillende leveranciers in het magazijn worden afgeleverd. U kunt meer dan één consolidatiehub hebben en kunt consolideren in meerdere hubs voor meer ladingen die afkomstig zijn uit verschillende magazijnen. Nadat u uw basisladingen hebt opgebouwd en de optie voor hubconsolidatie gebruikt, bouwt u de nieuwe ladingen op door de geconsolideerde aanvraagregels van transport te gebruiken. Vervolgens beoordeelt u uw ladingen en stuurt u deze door.



