---
title: "Één boekstuk en herwaardering van valuta-upgrade voor Microsoft Dynamics 365 voor bewerkingen versie 1611"
description: "Sommige organisaties journalen met één boekstuk met meer dan één klant of leverancier, en ze ook voert u uit de module klanten of het herwaarderingsproces voor vreemde valuta te betalen rekeningen. Dit onderwerp beschrijft de stappen die deze organisaties volgen moeten wanneer ze een naar Microsoft Dynamics 365 voor bewerkingen versie 1611 upgrade."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-28 16 - 04 - 17
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: d42c753d0dc8b8efc2a0d2a26da32a4951d85503
ms.lasthandoff: 03/31/2017


---

# <a name="single-voucher-and-currency-revaluation-upgrade-for-microsoft-dynamics-365-for-operations-version-1611"></a>Één boekstuk en herwaardering van valuta-upgrade voor Microsoft Dynamics 365 voor bewerkingen versie 1611

Sommige organisaties journalen met één boekstuk met meer dan één klant of leverancier, en ze ook voert u uit de module klanten of het herwaarderingsproces voor vreemde valuta te betalen rekeningen. Dit onderwerp beschrijft de stappen die deze organisaties volgen moeten wanneer ze een naar Microsoft Dynamics 365 voor bewerkingen versie 1611 upgrade.

Voer deze stappen als u een naar Microsoft Dynamics 365 voor bewerkingen versie 1611 upgrade.

1.  Voordat u een naar Dynamics 365 voor bewerkingen upgrade, moet u de processen van de herwaardering van vreemde valuta uitvoeren voor klanten en leveranciers. Stel de **methode** veld **factuurdatum**. Een herwaarderingstransactie gemaakt waarin de laatste herwaardering van vreemde valuta wordt omgekeerd. Daarom kan de openstaande transacties worden gewaardeerd tegen hun oorspronkelijke valuta voor boekhouding.
2.  Een upgrade uitvoert naar Dynamics 365 voor bewerkingen versie 1611.
3.  De module Klanten en de rekeningen te betalen vreemde valuta herwaardering processen opnieuw uitvoeren. Dit keer de **methode** veld **standaard**. Een nieuwe herwaarderingstransactie wordt gemaakt op basis van de huidige wisselkoersen. Deze transactie wordt vastgelegd op de niet-gerealiseerde winst/verlies- en de juiste grootboekrekening voor een overzicht.



