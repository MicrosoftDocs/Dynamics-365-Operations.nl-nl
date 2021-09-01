---
title: Berekeningsniveau voor kosten
description: Dit onderwerp beschrijft het stuklijstniveau met de naam Kostenberekeningsniveau. Op dit stuklijstniveau worden productie- en batchorders uitgesloten van de berekeningen.
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 41f2550ff22b838aa5d85022582fd9715917fe462aa34dbfc833941f5ada3325
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6717385"
---
# <a name="cost-calculation-level"></a>Berekeningsniveau voor kosten

Voor het stuklijstniveau met de naam **Berekeningsniveau voor kosten** worden productieorders en batchorders uitgesloten van de berekeningen. Dit niveau wordt door het systeem gebruikt wanneer kostenberekeningen worden uitgevoerd in kostprijsberekeningsversies. In processen zoals herberekening en voorraadafsluiting gebruikt het systeem **Kostprijsberekeningsniveau** van het stuklijstniveau in plaats daarvan.

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