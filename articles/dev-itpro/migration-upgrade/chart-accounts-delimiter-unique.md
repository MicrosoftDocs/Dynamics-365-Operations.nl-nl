---
title: Het scheidingsteken moet uniek zijn in elk rekeningschema
description: In Dynamics 365 for Finance and Operations is niet toegestaan dat hetzelfde scheidingsteken wordt gebruikt voor het rekeningschema en dimensiewaarden. Na de upgrade moet u het scheidingsteken wijzigen.
author: ryansandness
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c9728714944b54f3bff1e2a8b43c7adcf5200f08
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="chart-of-accounts-delimiter-must-be-unique"></a>Het scheidingsteken moet uniek zijn in elk rekeningschema

[!INCLUDE [banner](../includes/banner.md)]

In Microsoft Dynamics AX 2012 kunt u hetzelfde scheidingsteken gebruiken voor het rekeningschema en dimensiewaarden. In Dynamics 365 for Finance and Operations is niet toegestaan dat hetzelfde scheidingsteken wordt gebruikt voor het rekeningschema en dimensiewaarden. Als er een dubbele scheidingsteken is, kunt u dit wijzigen na de upgrade. 

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
