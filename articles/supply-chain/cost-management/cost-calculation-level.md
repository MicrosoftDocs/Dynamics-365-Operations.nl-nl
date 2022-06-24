---
title: Berekeningsniveau voor kosten
description: Dit artikel beschrijft het stuklijstniveau met de naam Kostenberekeningsniveau. Op dit stuklijstniveau worden productie- en batchorders uitgesloten van de berekeningen.
author: JennySong-SH
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 647ef4b13b864cfdbb7905fe7a0d340e85f6c1e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850868"
---
# <a name="cost-calculation-level"></a>Berekeningsniveau voor kosten

[!include [banner](../includes/banner.md)]

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