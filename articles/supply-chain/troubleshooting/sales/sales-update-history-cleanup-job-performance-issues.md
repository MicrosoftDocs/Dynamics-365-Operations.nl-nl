---
title: Opschoning van verkoophistorie voor update is mislukt of werkt niet goed
description: De batchtaak voor het opschonen van de verkoophistorie kan mislukken of zeer lang duren als er veel verkoopupdategegevens zijn.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: c02273adf90afc67b7c0ae1b82c19d489bfbd3b1
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920069"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Opschoning van verkoophistorie voor update is mislukt of werkt niet goed

## <a name="symptoms"></a>Symptomen

De batchtaak **Opschoning van verkoophistorie voor update** is mislukt of werkt niet goed.  

## <a name="cause"></a>Oorzaak

Dit kan gebeuren wanneer het systeem een groot aantal verkoopupdates bevat, wat kan leiden tot een grote hoeveelheid verkoopupdategegevens. De opschoonactie probeert alle gegevens in één transactie op te schonen. Het resultaat is dat de taak zeer lang kan duren en zelfs kan mislukken.

## <a name="resolution"></a>Oplossing

Een nieuwe versie van de batchtaak **Opschoning van verkoophistorie** is beschikbaar voor Supply Chain Management 10.0.19 en hoger. Deze functie is niet standaard ingeschakeld. Zie [Prestatieverbeteringen bij opschonen van verkoophistorie](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md) voor meer informatie over hoe dit werkt en hoe u het inschakelt in functiebeheer.

