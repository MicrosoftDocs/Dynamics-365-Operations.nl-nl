---
title: Voorraadhoeveelheid is niet bijgewerkt vanwege onvoldoende transacties
description: 'Voorraadhoeveelheid: 1% kan niet worden bijgewerkt omdat er onvoldoende voorraadtransacties met de opgegeven dimensies zijn voor artikel %2.'
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 88130a969039dd741c8ea4fbaabe81acf0e6fb6a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475963"
---
# <a name="system-cant-update-inventory-quantity-because-of-insufficient-transactions"></a>Het systeem kan de voorraadhoeveelheid niet bijwerken vanwege onvoldoende transacties

## <a name="symptoms"></a>Symptomen

Dit probleem kan optreden als het systeem geen voorraadhoeveelheid kan bijwerken omdat er onvoldoende voorraadtransacties met de opgegeven dimensies zijn. Mogelijk wordt het volgende foutbericht weergegeven:

> Voorraad hoeveelheid -%1 kan niet worden bijgewerkt vanwege onvoldoende voorraadtransacties voor artikel %2 met dimensies Grootte =%3, Kleur=%4, Toevoegingen=%5, Site=%6, Magazijn=%7, Locatie=%8, Voorraadstatus=beschikbaar, Nummerplaat=%9, Batchnummer=%10 voor verwijzing-id %11 op partij-id %12.

## <a name="resolution"></a>Oplossing

Zorg ervoor dat er geen voorraadtransacties zijn die de hoeveelheid fysiek reserveren. Deze transacties kunnen bijvoorbeeld openstaande kwaliteitsorders, voorraadblokkeringsrecords of uitvoerorders zijn.
