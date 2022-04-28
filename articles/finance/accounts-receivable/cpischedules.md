---
title: Planning van consumentenprijsindex
description: In dit onderwerp wordt uitgelegd hoe u de lijst met CPI-planningen (consumentenprijsindex) maakt die u van internet haalt om de escalatiekosten in Facturering van abonnementen te bepalen.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 2a69e58095844286878e27a100fa49a44a4a71f4
ms.sourcegitcommit: 4d7bc52e6cdf6afce3793893ba2aa07176302314
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/11/2022
ms.locfileid: "8560474"
---
# <a name="consumer-price-index-schedule"></a>Planning van consumentenprijsindex

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u CPI-planningen maakt, verwijdert, controleert en verwerkt. Een CPI-planning kan worden gebruikt om de prijzen te bepalen voor consumptiegoederen en -diensten die u toevoegt als factureringsplanningsregels. De CPI-planning kan vervolgens worden gebruikt voor escalatie- en kortingsprijzen in een factureringsplanning of kan handmatig worden verwerkt om de factureringsbedragen in factureringsplanningen bij te werken. U kunt CPI-planningen handmatig invoeren of u kunt ze importeren met de samengestelde entiteit CPI-planning.

Volg deze stappen om een planning van een consumentenprijsindex toe te voegen.

1. Selecteer **Nieuw** op de pagina **Planning van consumentenprijsindex**.
2. Geef in het veld **Planning van consumentenprijsindex** een unieke naam op.
3. Voer in het veld **Beschrijving** een beschrijving in.
4. Selecteer **Toevoegen** op het tabblad **Planning van consumentenprijsindex**.
5. Geef in het veld **Datum consumentenprijsindex** de datum op waarop de nieuwe CPI-planning actief wordt.
6. Voer in het veld **Planning van consumentenprijsindex** de naam in die u in stap 2 hebt ingevoerd.
7. Selecteer **Opslaan**.

Voer de volgende stappen uit om een CPI-planningsdatum te verwijderen.

1. Selecteer op de pagina **Planning van consumentenprijsindex** een of meer regels die u wilt verwijderen en selecteer **Verwijderen**.
2. Als u de hele CPI-planning wilt verwijderen, selecteert u **Verwijderen** in het actievenster. U kunt de geselecteerde CPI-planning niet verwijderen als deze aan een factureringsplanning is gekoppeld.
3. In het actievenster selecteert u **Verwerken** om de factureringsplanningen bij te werken die gebruikmaken van de geselecteerde CPI-planning. De laatste CPI-datums en planningsbedragen worden gebruikt om de prijzen van de factureringsplanning bij te werken.
4. Controleer op het sneltabblad **Proces van consumentenprijsindex** de bijgewerkte velden **Nummer factureringsplanning**, **Artikelnummer**, **Begindatum facturering**, **Einddatum facturering**, **Escalatiedatum** en **Escalatiefrequentie**

Als CPI-planningen zijn ingesteld, kunnen deze worden gebruikt voor escalatie- en kortingsprijswijzigingen in factureringsplanningen.

## <a name="cpi-calculation"></a>CPI-berekening

Voor deze voorbeelden loopt de periode van 1 januari 2020 tot en met 31 december 2022. Het basis CPI-tarief (de CPI-waarde bij het starten van het contract) is 105,65. Op 1 januari 2021 is de huidige CPI 110,5. Op 1 januari 2022 is de huidige CPI 114,25. Het oorspronkelijk bedrag is $ 1000.

**Voorbeeld 1**

Op de pagina **Terugkerende contractfactureringsparameters** stelt u het veld **Berekening van consumentenprijsindex** in op **Basisindex consumentenprijs**.

Voor de periode 1 januari 2021 wordt het eerste escalatiebedrag als volgt berekend, op basis van het oorspronkelijke bedrag:

1000 + (110,5 – 105,65) &divide; 105,65 &times; 1000 = 1045,91

Voor de periode 1 januari 2022 wordt het escalatiebedrag als volgt berekend:

1000 + (114,25 – 105,65) &divide; 105,65 &times; 1000 = 1081,40

**Voorbeeld 2**

Op de pagina **Terugkerende contractfactureringsparameters** stelt u het veld **Berekening van consumentenprijsindex** in op **Eerdere consumentenprijsindex**.

Voor de periode 1 januari 2021 wordt het eerste escalatiebedrag als volgt berekend, op basis van het oorspronkelijke bedrag:

1000 + (110,5 – 105,65) &divide; 105,65 &times; 1000 = 1045,91

Voor de periode 1 januari 2022 wordt het escalatiebedrag als volgt berekend, op basis van het eerste escalatiebedrag:

1045,91 + (114,25 – 110,5) &divide; 110,5 &times; 1045,91 = 1081,40

> [!NOTE]
> Voor het escalatieproces wordt altijd de laatste CPI-waarde gebruikt, ongeacht de indexdatum. Als de escalatie bijvoorbeeld in september plaatsvindt en de laatste CPI-waarde voor juli is, wordt de index voor juli gebruikt. Er worden geen correcties aangebracht nadat de index voor september is ingevoerd.

## <a name="prorated-escalation"></a>Evenredige escalatie

Als de escalatie plaatsvindt in het midden van een factureringsperiode, wordt het bedrag aangepast. De factureringsperiode is bijvoorbeeld van 1 augustus 2020 tot en met 31 juli 2021. Op de CPI-datum 1 september 2019 is de CPI-waarde 244. Op de CPI-datum 1 september 2020 is deze CPI-waarde 250. Als het vorige tarief 1000 is, worden de volgende formules gebruikt voor het berekenen van het factureringsbedrag voor de periode:

* *CPI-wijzigingen* = (250 – 244) &divide; 244 = 2,459%
* *Huidig tarief* = 1000 &times; 2,459% = 1024,59
* *Aantal dagen tegen het huidige tarief* = 31 juli 2021 – 1 september 2020 = 334
* *Vorig tarief* = 1000
* *Aantal dagen tegen het vorige tarief* = 31 augustus 2020 – 1 augustus 2020 = 31
* *Totale aantal dagen in de factureringsperiode* = 31 juli 2021 – 1 augustus 2020 + 1 = 365 dagen
* *Factureringsbedrag voor deze periode* = (1000 &times; 31 &divide; 365) + (1024,59 &times; 334 &divide; 365) = 1022,50

## <a name="escalation-that-uses-the-cpi-and-percentage"></a>Escalatie met de CPI en het percentage

Escalaties kunnen worden uitgevoerd met behulp van de CPI. De CPI plus een escalatie van 3 procent begint op 1 januari 2020 en heeft een jaarlijkse frequentie.

- Het bedrag dat voor 1 januari 2019 tot en met 31 december 2020 wordt gefactureerd, is 4000.
- De factureringsperiode die wordt geëscaleerd is 1 januari 2020 tot en met 31 december 2020.
- Op de CPI-datum 1 december 2018 is de CPI-waarde 205,3. Op de CPI-datum 1 december 2019 is de CPI-waarde 219,6.

Als het vorige tarief 4000 is, wordt het factureringsbedrag voor deze periode als volgt berekend:

- *CPI-wijzigingen* = (219,6 – 205,3) &divide; 205,3 = 6,965%
- *Huidig tarief* = (4000 &times; 6,965%) – 4000 = 278,60
- *Wijziging in percentage* = (4000 &times; 1,03) – 4000 = 120
- *Factureringsbedrag* = 4000 + 278,6 + 120 = 4398,6
