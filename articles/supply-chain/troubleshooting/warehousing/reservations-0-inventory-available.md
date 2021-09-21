---
title: Er kunnen geen voorraadreserveringen worden gemaakt omdat er 0,00 beschikbaar zijn
description: U krijgt een foutmelding dat het systeem geen reserveringen kan maken omdat er slechts 0,00 beschikbaar zijn in de voorraad. Dit probleem wordt waarschijnlijk veroorzaakt door openstaand werk.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 75d72f7ee1bdecca5a087b75b1de9907b9d244ab
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476043"
---
# <a name="system-cant-make-reservations-because-000-are-available-in-the-inventory"></a>Er kunnen geen reserveringen worden gemaakt omdat er 0,00 beschikbaar zjn in de voorraad

## <a name="symptoms"></a>Symptomen

Dit probleem kan optreden als het systeem geen voorraadhoeveelheid kan bijwerken omdat er onvoldoende voorraadtransacties met de opgegeven dimensies zijn. Mogelijk wordt het volgende foutbericht weergegeven:

> Fysiek voorhanden Site=%1, Magazijn=%2, Voorraadstatus=beschikbaar, Batchnummer=%3, Eigenaar=%4: %5 kan niet worden gereserveerd omdat slechts 0,00 in de voorraad beschikbaar zijn.

## <a name="resolution"></a>Oplossing

Dit probleem wordt waarschijnlijk veroorzaakt door openstaand werk. Voltooi het werk of ontvang een taak zonder werk te maken. Zorg ervoor dat er geen voorraadtransacties zijn die de hoeveelheid fysiek reserveren. Deze transacties kunnen bijvoorbeeld openstaande kwaliteitsorders, voorraadblokkeringsrecords of uitvoerorders zijn.
