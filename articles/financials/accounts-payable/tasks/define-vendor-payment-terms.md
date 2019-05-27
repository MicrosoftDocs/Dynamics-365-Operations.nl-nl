---
title: Voorwaarden voor leveranciersbetalingen definiëren
description: Stel de betalingsvoorwaarden in voor leveranciersfacturen.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68c69d5be5ccbdfb17fea7c61121cbf26fee48d4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569027"
---
# <a name="define-vendor-payment-terms"></a>Voorwaarden voor leveranciersbetalingen definiëren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Stel de betalingsvoorwaarden in voor leveranciersfacturen. Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga naar Leveranciers > Betalingsinstelling > Betalingstermijnen.
2. Klik op Nieuw.
    * De pagina Betalingstermijnen wordt gebruikt om te bepalen hoe de vervaldatum wordt berekend. Het wordt niet gebruikt om te bepalen hoe de datum contantkorting wordt berekend.  
3. Typ een waarde in het veld Betalingstermijnen.
4. Typ een waarde in het veld Omschrijving.
5. Voer een getal in het veld Dagen in.
    * Het hier ingevoerde getal wordt gebruikt om op te tellen bij de vervaldatum of bij het einde van de periode die wordt geïdentificeerd in Betalingsmethode. Als u bijvoorbeeld Netto selecteert, wordt het nummer opgeteld bij de vervaldatum. Als u Huidige maand selecteert, wordt het getal opgeteld bij de laatste dag van de huidige maand om de vervaldatum te berekenen.  
6. Klik op Opslaan.
7. Sluit de pagina.
8. Ga naar Leveranciers > Betalingsinstelling > Contantkortingen.
9. Klik op Nieuw.
10. Geef een id op in het veld Contantkorting.
11. Typ een waarde in het veld Omschrijving.
12. Als de leverancier een gelaagde korting aanbiedt, selecteert u de volgende contantkorting nadat de huidige is vervallen.
13. Sluit de pagina.
14. Voer een getal in het veld Dagen in.
    * De hoeveelheid die in het veld Dagen is ingevoerd wordt gebruikt voor het berekenen van de datum voor de contantkorting, op basis van de optie die is geselecteerd in het veld Netto/Huidig. Als Netto is geselecteerd, wordt de hoeveelheid opgeteld bij de factuurdatum om de datum voor de contantkorting te bepalen. Als Huidge maand is geselecteerd, wordt de hoeveelheid opgeteld bij het einde van de valutamaand om de datum voor de contantkorting te bepalen.  
15. Voer het percentage van de contantkorting in het veld Korting in. 
16. Voer de hoofdrekening in waaraan de contantkorting wordt geboekt voor klantfacturen.
17. Voer de hoofdrekening in waaraan de contantkorting wordt geboekt voor leveranciersfacturen.
    * Als Korting tegenrekeningen is ingesteld op Hoofdrekening voor leverancierskortingen gebruiken, wordt de hoofdrekening gebruikt.  Als de optie is ingesteld op Rekeningen op de factuurregels, wordt de contantkorting geboekt naar de activa-/onkostenrekeningen op de regels van de factuur.  
18. Klik op Opslaan.

