---
title: Beperkingen voor kostprijsberekeningsversies voor standaardkosten.
description: Dit artikel beschrijft de beperkingen die voor een kostprijsberekeningsversie voor standaardkosten gelden.
author: JennySong-SH
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c5c00ae8952e2c80d97d039271a6f5c63e9a72f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867980"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Beperkingen voor kostprijsberekeningsversies voor standaardkosten.

[!include [banner](../includes/banner.md)]

Dit artikel beschrijft de beperkingen die voor een kostprijsberekeningsversie voor standaardkosten gelden. 

De volgende beperkingen helpen zorgen dat de standaardprincipes voor kostprijsberekening worden gevolgd:

-  De kosten van een artikel moeten inclusief de toeslagen zijn. De toeslagen voor een gefabriceerd artikel zijn de afgeschreven kosten in stuklijst- en routegegevens. Daarom moeten de kosten in de eenheidskosten worden opgenomen. De toeslagen voor een ingekocht artikel zijn ook in de eenheidskosten van het artikel opgenomen.

-  De berekening van de standaardkosten voor gefabriceerde artikelen moet zijn gebaseerd op de kostenrecords in een kostprijsberekeningsversie voor standaardkosten. Alternatieve bronnen van kostengegevens kunnen alleen worden gebruikt bij een kostprijsberekeningsversie voor geplande kosten, zoals inkoopprijsovereenkomsten voor ingekochte artikelen. Alternatieve bronnen van kostengegevens worden gedefinieerd door de stuklijstberekeningsgroep.

-  Stuklijstberekeningen moeten in een explosiemodus van een enkel niveau worden uitgevoerd.

De kostengegevens van een artikel voor standaardkosten kunnen worden gekopieerd naar een andere kostprijsberekeningsversie die standaardkosten of geplande kosten bevat. De kostengegevens van een artikel voor geplande kosten kunnen echter niet worden gekopieerd naar een kostprijsberekeningsversie die standaardkosten bevat, omdat de eerder genoemde beperkingen niet voor geplande kosten gelden.

## <a name="related-articles"></a>Gerelateerde artikelen

[Overzicht van Kostprijsberekeningsversies](costing-versions.md)

[Standaardkosten in een niet-productieomgeving bijwerken](update-standard-costs-non-manufacturing-environment.md)

[Voorbereiding van het onderhoud van standaardkosten voor gefabriceerde artikelen](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]