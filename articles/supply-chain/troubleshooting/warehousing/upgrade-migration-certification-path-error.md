---
title: Certificaatpadfout bij upgrade of migratie naar WMS
description: Als in de app het foutbericht 'Vertrouwensrelatie voor certificaatpad niet gevonden' wordt weergegeven bij het upgraden of migreren naar WMS, geeft deze pagina informatie over het oplossen van het probleem.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2cff41455268c43bdd99e285b9675f0c69be7de7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475986"
---
 # <a name="trust-anchor-for-certification-path-not-found-when-updating-and-migrating-to-wms"></a>Vertrouwensrelatie voor certificaatpad niet gevonden bij bijwerken en migreren naar WMS

## <a name="symptoms"></a>Symptomen

Bij het upgraden en migreren naar Advanced Warehouse Management (WMS) bevat de Warehouse Management-toepassing mogelijk het volgende foutbericht:

> java.security.cert.certPathValidatorException: Vertrouwensanker voor certificeringspad niet gevonden.

## <a name="cause"></a>Oorzaak

Dit komt doordat zelf ondertekende certificaten niet vertrouwd zijn op Android8+ in lokale omgevingen.

## <a name="resolution"></a>Oplossing

Gebruik een externe (openbare) certificeringsinstantie (CA). Er is een oplossing voor dit probleem beschikbaar in versie 1.9.0.0 van de Warehouse Management-app. Zie [Vertrouwensrelatie voor certificaatpad niet gevonden bij het instellen van een app-verbinding](certification-path-app-connection-error.md) voor meer informatie over dit probleem en het oplossen van dit probleem.
