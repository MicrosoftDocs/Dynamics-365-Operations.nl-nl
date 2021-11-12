---
title: Handmatige afschrijving
description: Dit artikel biedt een overzicht van de methode voor handmatige afschrijving.
author: moaamer
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b5b62bbdd5d745bc9d0745cc6fa6d6e8034a61e3
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674822"
---
# <a name="manual-depreciation"></a>Handmatige afschrijving

[!include [banner](../includes/banner.md)]

Dit artikel biedt een overzicht van de methode voor handmatige afschrijving.

Wanneer u een profiel voor de afschrijving van vaste activa instelt en **Handmatig** selecteert in het veld **Methode** op de pagina **Afschrijvingsprofielen**, wordt de afschrijving van vaste activa die aan het afschrijvingsprofiel zijn toegewezen, bepaald door het percentage dat u opgeeft voor elk interval in het kalenderjaar. De intervallen waarvoor u percentages instelt, worden geboekt volgens de waarde die u selecteert in het veld **Periodefrequentie** op het sneltabblad **Algemeen** van de pagina **Afschrijvingsprofielen**. U kunt kiezen uit de volgende waarden:

- Jaarlijks
- Maandelijks
- Per kwartaal
- Zesmaandelijks
- Dagelijks

Nadat u een periodefrequentie hebt geselecteerd, klikt u op **Handmatige schema's** en stelt u percentages in voor elk van de boekingsintervallen. Het afschrijvingsbedrag wordt door de combinatie van handmatige schema's en de boekingsintervallen gedefinieerd, zoals in de voorbeelden verderop in dit artikel wordt getoond. De handmatige afschrijving wordt altijd berekend als een percentage van de aanschafprijs. Voor handmatige afschrijving hoeven de percentages die u invoert in de intervallen van de afschrijving niet samen 100 procent te zijn. Handmatige afschrijving is een flexibele afschrijvingsmethode, die vaak wordt gebruikt om een buitengewoon afschrijvingsprofiel te definiëren op de pagina **Boeken**, zoals een niet-periodieke afschrijving voor speciale doeleinden (bijvoorbeeld belastingen).

## <a name="examples"></a>Voorbeelden
Aanschafprijs: 11.000.00 Verwachte restwaarde: 1.000,00 In de volgende tabel worden de intervallen en percentages weergeven die u instelt op de pagina **Schema's afschrijvingsprofiel vaste activa**.

| Intervalnummer | Percentage |
|-----------------|------------|
| 1               | 10,00      |
| 2               | 50,00      |
| 3               | 8,00       |

In de volgende tabel ziet u hoe de afschrijving voor alle intervallen wordt berekend.

|  Intervalnummer | Berekening van het jaarlijkse afschrijvingsbedrag | Nettoboekwaarde aan het einde van het interval |
|------------------|-----------------------------------------------|-------------------------------------------|
| 1                | (11.000 – 1.000) × 10% = 1.000                | 10.000 (11.000 – 1.000)                   |
| 2                | (11.000 – 1.000) × 50% = 5.000                | 5.000 (10.000 – 5.000)                    |
| 3                | (11.000 – 1.000) × 8% = 800                   | 4.200 (5.000 – 800)                       |

Als u **Maandelijks** selecteert in het veld **Periodefrequentie**, moet u 12 handmatige planningsintervallen instellen. In de volgende tabel ziet u de afschrijvingsbedragen voor de eerste twee intervallen.

| Interval | Afschrijvingsbedrag            |
|----------|--------------------------------|
| januari  | (11.000 – 1.000) × 10% = 1.000 |
| februari | (11.000 – 1.000) × 50% = 5.000 |

Als u <strong>Zesmaandelijks</strong> selecteert in het veld *<strong><em>Periodefrequentie</em>*</strong>, stelt u twee handmatige planningsintervallen in. In de volgende tabel ziet u de afschrijvingsbedragen voor deze twee intervallen.

| Interval    | Afschrijvingsbedrag            |
|-------------|--------------------------------|
| 30 juni     | (11.000 – 1.000) × 10% = 1.000 |
| 31 december | (11.000 – 1.000) × 50% = 5.000 |

Het totaal van de percentages voor alle intervallen hoeft niet gelijk te zijn aan 100. U ontvangt echter een bericht als de waarde in het veld **Cumulatief percentage** op de pagina **Schema's afschrijvingsprofiel vaste activa** niet **100** is.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
