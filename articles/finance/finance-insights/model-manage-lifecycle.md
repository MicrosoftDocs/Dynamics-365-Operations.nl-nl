---
title: Levenscyclus van modelbeheer
description: In dit artikel worden manieren beschreven om de machine learning-modellen van uw organisatie te onderhouden en zo de voorspelling te optimaliseren die ze genereren.
author: ShivamPandey-msft
ms.date: 07/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 526916929e4bc079f9cea82d8ea9f80813e89b83
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880869"
---
# <a name="model-management-lifecycle"></a>Levenscyclus van modelbeheer

[!include [banner](../includes/banner.md)]

In dit artikel worden manieren beschreven om de machine learning-modellen van uw organisatie te onderhouden en zo de voorspelling te optimaliseren die ze genereren.

Het is raadzaam om het AI-model te trainen in een sandbox-omgeving en vervolgens beheerde oplossingen te gebruiken om deze te implementeren in een productieomgeving. Door deze benadering zorgt u ervoor dat de juiste besturingselementen zijn gebruikt voor het beheer van de levenscyclus van het model.

Omdat het AI-model is gebaseerd op de beschikbare factuur- en klantgegevens, is het van belang dat de sandbox-omgeving over een recente kopie van de productiegegevens beschikt. U kunt beginnen met het trainen van het model door de stappen uit te voeren in [Voorspellingen voor klantbetalingen gebruiken](use-customer-payment-predictions.md). Nadat het model opnieuw is getraind, evalueert u de resultaten zoals beschreven in [Het aanvankelijke prognosemodel voor klantbetalingen evalueren](evaluate-payment-prediction.md). Gebruik de informatie in [Het voorspellingsmodel verbeteren](improve-model.md) om te experimenteren met combinaties van functies en filters waarmee het model kan worden verbeterd.

Als u tevreden bent over de trainingsresultaten, volgt u de stappen in [Uw AI-model verdelen](/ai-builder/distribute-model) om het model over te brengen naar uw productieomgeving.
