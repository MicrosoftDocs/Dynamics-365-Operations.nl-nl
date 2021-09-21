---
title: Geïmporteerde inkooporders geven onjuiste regelnummers weer.
description: Wanneer inkooporders worden geïmporteerd via gegevensbeheer, volgen de nummers van de inkooporderregels niet de verhoging die is gedefinieerd in de systeemparameters.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: e1cf5cf1d04824213f495ac3ebf556796c96611a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475967"
---
# <a name="imported-purchase-orders-show-incorrect-line-numbers"></a>Geïmporteerde inkooporders geven onjuiste regelnummers weer.

## <a name="symptoms"></a>Symptomen

Automatisch gegenereerde regelnummers voor inkooporderregels die worden geïmporteerd via de gegevensentiteit *Inkooporderregels V2* gebruiken niet de systeemregelnummerverhoging die is opgegeven in systeemparameters. Als u handmatig een inkooporder maakt en regels toevoegt via de gebruikersinterface (UI), worden de regelnummers juist verhoogd. Als u echter het DMF (Data Management Framework) gebruikt, worden ze niet op de juiste wijze verhoogd.

Dit probleem treedt op omdat het systeem bij het importeren van regels via DMF de methode van het DMF gebruikt voor het toewijzen van regels als regelnummers nog niet zijn toegewezen in de geïmporteerde entiteit. Met deze methode worden regelnummers altijd met één verhoogd.

## <a name="workaround"></a>Tijdelijke oplossing

Zorg ervoor dat de gewenste regelnummers al zijn opgegeven in de regelnummervelden van de entiteit wanneer u de inkooporderregels importeert. In dit geval worden de regelnummers niet overschreven door DMF.
