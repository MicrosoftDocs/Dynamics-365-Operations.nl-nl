---
title: Voorwaarden voor leveranciersbetalingen definiëren
description: In dit onderwerp wordt uitgelegd u betalingstermijnen voor instelt voor leveranciersfacturen.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6432d04aa821e76d67e2c430e514f4b9056d8228
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177224"
---
# <a name="define-vendor-payment-terms"></a>Voorwaarden voor leveranciersbetalingen definiëren

[!include [task guide banner](../../includes/task-guide-banner.md)]

In dit onderwerp wordt uitgelegd u betalingstermijnen voor instelt voor leveranciersfacturen. Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga naar **Navigatievenster > Modules > Leveranciers > Betalingsinstelling > Betalingstermijnen**.
2. Selecteer **Nieuw**. De pagina Betalingstermijnen wordt gebruikt om te bepalen hoe de vervaldatum wordt berekend. Het wordt niet gebruikt om te bepalen hoe de datum contantkorting wordt berekend.  
3. Typ een waarde in het veld **Betalingstermijn**.
4. Typ een waarde in het veld **Beschrijving**.
5. Voer in het veld **Dagen** een getal in. Het hier ingevoerde getal wordt gebruikt om op te tellen bij de vervaldatum of bij het einde van de periode die wordt geïdentificeerd in Betalingsmethode. Als u bijvoorbeeld **Netto** selecteert, wordt de waarde opgeteld bij de vervaldatum. Als u **Huidige maand** selecteert, wordt de waarde opgeteld bij de laatste dag van de huidige maand om de vervaldatum te berekenen.  
6. Selecteer **Opslaan**.
7. Sluit de pagina.
8. Ga naar **Leveranciers > Betalingsinstelling > Contantkortingen**.
9. Selecteer **Nieuw**.
10. Typ een id iin het veld **Contantkorting**.
11. Typ een waarde in het veld **Beschrijving**.
12. Als de leverancier een gelaagde korting aanbiedt, selecteert u de volgende contantkorting nadat de huidige is vervallen.
13. Sluit de pagina.
14. Voer in het veld **Dagen** een getal in. De hoeveelheid die in het veld **Dagen** is ingevoerd, wordt gebruikt voor het berekenen van de datum voor de contantkorting, op basis van de optie die is geselecteerd in het veld **Netto/Huidige maand**. Als **Netto** is geselecteerd, wordt de hoeveelheid opgeteld bij de factuurdatum om de datum voor de contantkorting te bepalen. Als **Huidige maand** is geselecteerd, wordt de hoeveelheid opgeteld bij het einde van de valutamaand om de datum voor de contantkorting te bepalen.  
15. Voer het percentage van de contantkorting in het veld **Korting** in. 
16. Voer de hoofdrekening in waarnaar de contantkorting voor klantfacturen wordt geboekt, en voer vervolgens de hoofdrekening in waarnaar de contantkorting voor leveranciersfacturen wordt geboekt. Als **Korting tegenrekeningen** is ingesteld op **Hoofdrekening voor leverancierskortingen gebruiken**, wordt de hoofdrekening gebruikt. Als de optie is ingesteld op **Rekeningen op de factuurregels**, wordt de contantkorting geboekt naar de activa-/onkostenrekeningen op de regels van de factuur.  
17. Selecteer **Opslaan**.

