---
title: Raming van productieorderkosten
description: Dit artikel biedt informatie over ramingen van productiekosten. Door de productiekosten te ramen, weet u wat de verwachte materiaal- en capaciteitverbruikskosten zijn van het fabriceren van een artikel in de geplande productieorderhoeveelheid.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93546fc170757ee2c39144842bae12d78400fd32
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2019
ms.locfileid: "350476"
---
# <a name="production-order-cost-estimation"></a>Raming van productieorderkosten

[!include [banner](../includes/banner.md)]

Dit artikel biedt informatie over ramingen van productiekosten. Door de productiekosten te ramen, weet u wat de verwachte materiaal- en capaciteitverbruikskosten zijn van het fabriceren van een artikel in de geplande productieorderhoeveelheid. 

Nadat u een productieorder hebt gemaakt, moet u productiekosten ramen. Het belangrijkste doel hiervan is het ramen van het artikel- en routeverbruik voor het productieproces, omdat deze ramingen de basis vormen voor volgende plannings- en productieprocessen.

## <a name="production-cost-estimation"></a>Raming van productiekosten
Ramingen van productiekosten zijn gebaseerd op de volgende informatie:

-   De hoeveelheid van de productieorder
-   De onderdelen in de productiestuklijsten
-   De routebewerkingen in de productieroute
-   de indirecte kosten die van toepassing zijn op deze onderdelen en bewerkingen
-   De actieve kostengegevens op de datum van berekening

Als er een phantom-regelartikel in de productiestuklijsten staat, weerspiegelen de berekeningen de onderdelen en routebewerkingen van het phantom-artikel. U kunt de ramingstaak gebruiken om geschatte kosten opnieuw te berekenen zodat bijgewerkte informatie wordt gereflecteerd. De bijgewerkte informatie kan bijvoorbeeld bestaan uit wijzigingen in de productieorderhoeveelheid, de onderdelen in de productiestuklijsten, de routebewerkingen in de productieroute, de indirecte kosten die van toepassing zijn op deze onderdelen en bewerkingen, of de actieve kostengegevens op de datum van herberekening. De berekeningen van de geschatte kosten stellen ook een verkoopprijs voor het productieartikel voor op basis van een kostprijs-plus-verhoging-benadering. De berekeningen van de kostenraming kunnen eventueel worden toegepast op referentieorders die andere productieorders reflecteren die aan de productieorder zijn gekoppeld.

## <a name="view-the-estimated-costs"></a>De kostenramingen weergeven
Nadat u de raming hebt uitgevoerd, kunt u de resultaten op de pagina **Prijsberekening** weergeven. Bij de raming worden de volgende waarden berekend:

-   **Productiekosten**: de bovenste regel van de raming. Hier worden de volledige kosten van het uitvoeren van de productieorder en de totale verkoopprijs voor de productie weergegeven. Dit is de som van alle kostenregels van de raming.
-   **Route- of resourcekosten**: de kosten voor de productiebewerkingen. Dit zijn onder andere de kosten van elementen als de insteltijd, de uitvoeringstijd en overhead.
-   **Materiaalkosten**: de kosten en prijzen van de stuklijstonderdelen die nodig zijn om het artikel te fabriceren. Deze kosten zijn al eerder gemaakt en ingevoerd in het systeem.

## <a name="other-uses-of-cost-estimation"></a>Andere functies van kostenramingen
Een kostenraming biedt ook de volgende informatie:

-   Onderbouwde prijsoffertes
-   Ramingen van de rentabiliteit van de order
-   Ramingen van het grondstofverbruik
-   Vergelijkingen van kostengegevens van eerdere producties
-   Budget- en prognosegegevens
-   Ramingen van de productiegrootte die nodig zijn om bepaalde kosten te beheren




