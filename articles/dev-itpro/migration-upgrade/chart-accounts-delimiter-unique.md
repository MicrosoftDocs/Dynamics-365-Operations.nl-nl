---
title: Het scheidingsteken in het rekeningschema uniek maken
description: In Dynamics 365 for Finance and Operations, is het niet mogelijk hetzelfde scheidingsteken te gebruiken voor het rekenschema en dimensiewaarden. Na de upgrade moet u het scheidingsteken wijzigen.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: e197a1b44e038a97b8bf6db692dcc2eef2bc5f7b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559523"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Het scheidingsteken in het rekeningschema uniek maken

[!include [banner](../includes/banner.md)]

In Microsoft Dynamics AX 2012 kunt u hetzelfde scheidingsteken gebruiken voor het rekeningschema en dimensiewaarden. In Dynamics 365 for Finance and Operations, is het niet mogelijk hetzelfde scheidingsteken te gebruiken voor het rekenschema en dimensiewaarden. Als er een dubbele scheidingsteken is, kunt u dit wijzigen na de upgrade. 

Deze functie is beschikbaar in:
- Dynamics 365 for Finance and Operations versie 8.0
- Dynamics 365 for Finance and Operations versie 7.1, KB 4094701 Kan de financiële dimensies niet invoeren als de dimensiewaarden het scheidingsteken voor het rekeningschema bevatten
- Dynamics 365 for Finance and Operations versie 7.2, KB 4092967 Kan subproject niet als dimensie kiezen wanneer de indeling van het subproject het dimensiescheidingsteken bevat

## <a name="update-delimiter"></a>Scheidingsteken bijwerken
Als er een conflict is met het rekeningschema, kan het scheidingsteken voor het rekeningschema en de indeling van de project/subproject-ID worden gewijzigd. Geen andere scheidingstekens voor de dimensie kunnen worden gewijzigd. 
- U kunt het scheidingsteken voor het rekeningschema wijzigen na de upgrade voor Finance and Operations in **Grootboekparameters** > **Rekeningschema en dimensies** > **Scheidingsteken wijzigen**. 
- Als het enige conflict betrekking heeft op de indeling van de project/subproject-ID, kunt u die waarde wijzigen in **Projectbeheer- en boekhoudingsparameters** > **Algemeen** > **Indeling subproject wijzigen**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Bepalen of uw omgeving bijgewerkte scheidingstekens vereist 
Als scheidingstekens in uw bijgewerkte omgeving conflicten veroorzaken, kan het instabiel zijn wanneer u waarden invoert in een besturingselement voor het invoeren van segmenten of dimensies. Dit houdt in dat u altijd zoekopdrachten of een flyout-menu moet gebruiken voor het invoeren van combinaties van rekeningen en dimensies.
