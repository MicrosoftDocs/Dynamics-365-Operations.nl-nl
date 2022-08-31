---
title: Berekeningsniveau voor kosten
description: Dit artikel beschrijft het stuklijstniveau met de naam Kostenberekeningsniveau. Op dit stuklijstniveau worden productie- en batchorders uitgesloten van de berekeningen.
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: e63a868696e36c1d4f5d19ea87bdf4d682c39f8c
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334950"
---
# <a name="cost-calculation-level"></a>Berekeningsniveau voor kosten

[!include [banner](../includes/banner.md)]

Voor het stuklijstniveau met de naam **Berekeningsniveau voor kosten** worden productieorders en batchorders uitgesloten van de berekeningen. Dit niveau wordt door het systeem gebruikt wanneer kostenberekeningen worden uitgevoerd in kostprijsberekeningsversies. In processen zoals herberekening en voorraadafsluiting gebruikt het systeem **Kostprijsberekeningsniveau** van het stuklijstniveau in plaats daarvan.

## <a name="turn-the-cost-calculation-level-feature-on-or-off"></a>De functie Berekeningsniveau voor kosten in- of uitschakelen

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.29 is deze functie standaard ingeschakeld. Beheerders kunnen deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Berekeningsniveau voor kosten* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="example-scenario"></a>Voorbeeldscenario

In het volgende eenvoudige scenario worden de verschillen weergegeven tussen het stuklijstniveau op het **Berekeningsniveau voor kosten** en het stuklijstniveau op het **Kostenniveau**.

U hebt drie producten: A, B en C. Product C is het onderdeel van product B en product B is het onderdeel van product A.

- Op **Kostenniveau** worden de volgende stuklijstniveaus toegewezen:

    - **Product A:** 0
    - **Product B:** 1
    - **Product C:** 2

- Op **Berekeningsniveau kosten** worden de volgende stuklijstniveaus toegewezen:

    - **Product A:** 0
    - **Product B:** 1
    - **Product C:** 2

Er wordt dan een productieorder voor product C gemaakt en product A wordt toegevoegd aan de productieorderstuklijst. Nadat de order is geraamd, worden stuklijstniveaus op de volgende manier bijgewerkt:

- Op **Kostenniveau** worden de volgende stuklijstniveaus toegewezen:

    - **Product B:** 1
    - **Product C:** 2
    - **Product A:** 3

- Op **Berekeningsniveau kosten** worden de volgende stuklijstniveaus toegewezen:

    - **Product A:** 0
    - **Product B:** 1
    - **Product C:** 2

Op deze manier worden wijzigingen in de stuklijst van de productieorder niet beïnvloed door de daaropvolgende kostenberekeningen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]