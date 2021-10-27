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
ms.openlocfilehash: 4f04dc204c705b40ed25fadc75118feaef4d6b6e
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641453"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Opschoning van verkoophistorie voor update is mislukt of werkt niet goed

## <a name="symptoms"></a>Symptomen

De batchtaak **Opschoning van verkoophistorie voor update** is mislukt of werkt niet goed.  

## <a name="cause"></a>Oorzaak

Dit kan gebeuren wanneer het systeem een groot aantal verkoopupdates bevat, wat kan leiden tot een grote hoeveelheid verkoopupdategegevens. De opschoonactie probeert alle gegevens in één transactie op te schonen. Het resultaat is dat de taak zeer lang kan duren en zelfs kan mislukken.

## <a name="resolution"></a>Oplossing

Een nieuwe versie van de batchtaak **Opschoning van verkoophistorie** is beschikbaar voor Supply Chain Management 10.0.19 en hoger. Deze functie is niet standaard ingeschakeld. Zie [Prestatieverbeteringen bij opschonen van verkoophistorie](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md) voor meer informatie over hoe dit werkt en hoe u het inschakelt in functiebeheer.

