---
title: Scheidingsteken van rekeningschema uniek maken
description: In dit artikel wordt toegelicht waarom het niet mogelijk is om hetzelfde scheidingsteken te gebruiken voor het rekenschema en dimensiewaarden. Na de upgrade moet u het scheidingsteken wijzigen.
author: RyanCCarlson2
ms.date: 04/13/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: RCarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.openlocfilehash: 2184d26e104f803ae1bf59155cf18f560652f318
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9292491"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Het scheidingsteken in het rekeningschema uniek maken

[!include [banner](../includes/banner.md)]

In Microsoft Dynamics AX 2012 kunt u hetzelfde scheidingsteken gebruiken voor het rekeningschema en dimensiewaarden. In de huidige versies van Finance + Operations is het niet toegestaan dat hetzelfde scheidingsteken wordt gebruikt voor het rekeningschema en dimensienamen of -waarden. Als er een dubbele scheidingsteken is, kunt u dit wijzigen na de upgrade. 

## <a name="update-delimiter"></a>Scheidingsteken bijwerken
Als er een conflict is met het rekeningschema, kan het scheidingsteken voor het rekeningschema en de indeling van de project/subproject-ID worden gewijzigd. Geen andere scheidingstekens voor de dimensie kunnen worden gewijzigd. 
- U kunt het scheidingsteken voor het rekeningschema wijzigen na de upgrade in **Grootboekparameters** > **Rekeningschema en dimensies** > **Scheidingsteken wijzigen**. 
- Als het enige conflict betrekking heeft op de indeling van de project/subproject-ID, kunt u die waarde wijzigen in **Projectbeheer- en boekhoudingsparameters** > **Algemeen** > **Indeling subproject wijzigen**. 

### <a name="other-considerations"></a>Andere overwegingen
Net als bij project-/subproject-id mogen andere hoofdgegevensrecords die worden gebruikt als financiële dimensies, zoals leveranciers of klanten, geen rekening-id-waarden hebben die hetzelfde teken gebruiken als het scheidingsteken voor het rekeningschema. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Bepalen of uw omgeving bijgewerkte scheidingstekens vereist 
Als scheidingstekens in uw bijgewerkte omgeving conflicten veroorzaken, kan het instabiel zijn wanneer u waarden invoert in een besturingselement voor het invoeren van segmenten of dimensies. Dit houdt in dat u altijd zoekopdrachten of een flyout-menu moet gebruiken voor het invoeren van combinaties van rekeningen en dimensies.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

