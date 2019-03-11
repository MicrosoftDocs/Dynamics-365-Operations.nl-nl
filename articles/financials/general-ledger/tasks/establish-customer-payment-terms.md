---
title: Voorwaarden voor klantbetalingen vaststellen
description: Deze procedure definieert een contantkorting en een instelling voor vervaldatum.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49f4047ab4bff6bdfbe8326a6680f9d8f9762c95
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "312480"
---
# <a name="establish-customer-payment-terms"></a>Voorwaarden voor klantbetalingen vaststellen

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure definieert een contantkorting en een instelling voor vervaldatum. Bij deze taakbegeleiding wordt het demobedrijf USMF gebruikt.

1. Ga naar Klanten > Betalingsinstelling > Betalingsdagen.
    * De instelling voor de betalingstermijnen wordt gedeeld voor Klanten en Leveranciers. Als u deze in de ene module definieert, komen zij tevens beschikbaar in de andere module. Voor deze taakhandleiding worden alle betalingstermijnen ingesteld onder Klanten.  
2. Klik op Nieuw.
    * Maak een betalingsdag als uw betalingstermijnen een bepaalde dag van de week vereisen (Maandag, Dinsdag enzovoort) of een specifieke datum van de maand (vijfde, tiende enzovoort).  
3. Voer in het veld Betalingsdag een id voor de betalingsdag in het veld Betalingsdag in.
4. Voer in het veld Beschrijving een omschrijving van de betalingsdag in.
5. Selecteer in het veld Week/Maand de optie Week of Maand.
    * Als u een weekdag, zoals Maandag, wilt invoeren, selecteert u Week. Als u een datum in de maand wilt invoeren, zoals de tiende, selecteert u Maand. Selecteer Maand voor dit voorbeeld.  
6. Voer in het veld Dag van maand een datum in.
    * De datum moet als getal worden ingevoerd, zoals "10", en als "10e".  
7. Klik op Opslaan.
8. Sluit de pagina.
9. Ga naar Klanten > Betalingsinstelling > Betalingstermijnen.
10. Klik op Nieuw.
    * Betalingstermijnen wordt gebruikt om te bepalen hoe de vervaldatums worden berekend. De instelling van de datum voor contantkorting wordt op een aparte pagina gedefinieerd.  
11. Voer in het veld Betalingstermijnen een id in het veld de Betalingstermijnen in.
12. Voer in het veld Beschrijving een omschrijving in.
13. Selecteer een Betalingsmethode als Rembours, Netto, Huidige maand enzovoort.
    * De Betalingsmethode wordt gebruikt om het begin te definiëren voor het berekenen van de vervaldatum.  Zo wordt bijvoorbeeld Netto gebruikt als de vervaldatum altijd een vast aantal maanden of dagen na de factuurdatum ligt. Rembours kan worden gebruikt als betaling per factuur is vereist, dus geen vervaldatum wordt berekend. Selecteer Huidige maand voor deze taakhandleiding.  
14. Selecteer een Betalingsdag als een bepaalde dag van de week of datum is opgenomen in de berekening.
    * Afhankelijk van uw betalingstermijn kunt u een hoeveelheid invoeren in Maanden of Dagen. Of u kunt het betalingsschema of de betalingsdag gebruiken om op te tellen bij het einde van de betalingsmethode. Als de vervaldatum altijd op de tiende van de volgende maand valt selecteert u de tiende als betalingsdag.  
15. Klik op Opslaan.
16. Sluit de pagina.
17. Ga naar Klanten > Betalingsinstelling > Contantkortingen.
18. Klik op Nieuw.
    * Deze pagina wordt gebruikt om te bepalen hoe de datum voor contantkorting wordt berekend.  
19. Voer in het veld Contantkorting een id in het veld Contantkorting in.
20. Voer in het veld Beschrijving een omschrijving in.
21. Als een gelaagde contantkorting beschikbaar is, selecteert u de volgende kortingscode die na deze nieuwe contantkorting relevant is.
22. Voer het aantal dagen in dat wordt gebruikt om de datum voor contantkortingen te berekenen.
    * Als de methode Netto is geselecteerd, wordt het aantal dagen opgeteld bij de factuurdatum om de datum voor de contantkorting te bepalen.  
23. Voer het percentage van de contantkorting in.
24. Voer de hoofdrekening in waaraan de contantkorting wordt geboekt voor klantfacturen.
25. Selecteer een optie in het veld Korting tegenrekeningen.
    * Als u Rekeningen op de factuurregels selecteert, wordt de contantkorting geboekt naar dezelfde activa-/hoofdrekening als in de regels van de leveranciersfactuur staat vermeld. Als u Hoofdrekening voor leveranciersfacturen gebruiken selecteert, wordt de contantkorting geboekt naar de hoofdrekening die u definieert in Hoofdrekening voor leveranciersfacturen. Voor dit voorbeeld selecteert u "Hoofdrekening voor leveranciersfacturen gebruiken".  
26. Voer de hoofdrekening in waaraan de contantkorting wordt geboekt voor leveranciersfacturen.
27. Klik op Opslaan.

