---
title: Journalen met enkel boekstuk en herwaarderingen van valuta's upgraden
description: In dit onderwerp wordt beschreven hoe u journalen met één boekstuk en herwaarderingen van valuta's kunt upgraden
author: ShylaThompson
ms.date: 06/20/2017
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
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: feafcd5c309360467344618f7cec15235ddbe77df807f75873ac82c941073500
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735489"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a>Journalen met enkel boekstuk en herwaarderingen van valuta's upgraden

[!include [banner](../includes/banner.md)]

Sommige organisaties voeren journalen in met een enkel boekstuk dat meer dan één klant of leverancier bevat, waarbij ze ook het herwaarderingsproces voor vreemde valuta voor klanten of leveranciers uitvoeren. In dit onderwerp worden de stappen beschreven die deze organisaties moeten volgen wanneer ze een upgrade uitvoeren naar Microsoft Dynamics 365 for Operations, versie 1611.

Voer deze stappen uit voor een upgrade naar Microsoft Dynamics 365 for Operations versie 1611.

1.  Voordat u een upgrade naar Finance and Operations uitvoert, moet u de processen voor herwaardering van vreemde valuta uitvoeren voor klanten en leveranciers. Stel het veld **Methode** in op **Factuurdatum**. Een herwaarderingstransactie wordt gemaakt waarin de laatste herwaardering van vreemde valuta wordt omgekeerd. Daarom worden de openstaande transacties gewaardeerd tegen hun oorspronkelijke boekhoudingsvaluta.
2.  Upgraden naar versie 1611.
3.  Voer de herwaardering van vreemde valuta voor zowel Leveranciers als Klanten opnieuw uit. Stel deze keer het veld **Methode** in op **Standaard**. Een nieuwe herwaarderingstransactie wordt gemaakt op basis van de huidige wisselkoersen. Deze transactie legt de niet-gerealiseerde winst/verlies vast en het juiste bedrag in het totaalgrootboek.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]