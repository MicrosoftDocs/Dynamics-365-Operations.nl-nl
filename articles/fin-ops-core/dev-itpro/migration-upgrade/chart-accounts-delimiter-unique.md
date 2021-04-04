---
title: Het scheidingsteken in het rekeningschema uniek maken
description: In dit onderwerp wordt toegelicht waarom het niet mogelijk is om hetzelfde scheidingsteken te gebruiken voor het rekenschema en dimensiewaarden. Na de upgrade moet u het scheidingsteken wijzigen.
author: panolte
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 183980651a811ef30a49461ff5a5f649d94b079c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565257"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a>Het scheidingsteken in het rekeningschema uniek maken

[!include [banner](../includes/banner.md)]

In Microsoft Dynamics AX 2012 kunt u hetzelfde scheidingsteken gebruiken voor het rekeningschema en dimensiewaarden. In de huidige versies van Finance and Operations is niet toegestaan dat hetzelfde scheidingsteken wordt gebruikt voor het rekeningschema en dimensiewaarden. Als er een dubbele scheidingsteken is, kunt u dit wijzigen na de upgrade. 

Deze functie is niet beschikbaar in de volgende versies:
- Finance and Operations versie 8.0
- Finance and Operations versie 7.1, KB 4094701 Kan de financiële dimensies niet invoeren als de dimensiewaarden het scheidingsteken voor het rekeningschema bevatten
- Finance and Operations versie 7.2, KB 4092967 Kan subproject niet als dimensie kiezen wanneer de indeling van het subproject het dimensiescheidingsteken bevat

## <a name="update-delimiter"></a>Scheidingsteken bijwerken
Als er een conflict is met het rekeningschema, kan het scheidingsteken voor het rekeningschema en de indeling van de project/subproject-ID worden gewijzigd. Geen andere scheidingstekens voor de dimensie kunnen worden gewijzigd. 
- U kunt het scheidingsteken voor het rekeningschema wijzigen na de upgrade in **Grootboekparameters** > **Rekeningschema en dimensies** > **Scheidingsteken wijzigen**. 
- Als het enige conflict betrekking heeft op de indeling van de project/subproject-ID, kunt u die waarde wijzigen in **Projectbeheer- en boekhoudingsparameters** > **Algemeen** > **Indeling subproject wijzigen**. 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a>Bepalen of uw omgeving bijgewerkte scheidingstekens vereist 
Als scheidingstekens in uw bijgewerkte omgeving conflicten veroorzaken, kan het instabiel zijn wanneer u waarden invoert in een besturingselement voor het invoeren van segmenten of dimensies. Dit houdt in dat u altijd zoekopdrachten of een flyout-menu moet gebruiken voor het invoeren van combinaties van rekeningen en dimensies.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]