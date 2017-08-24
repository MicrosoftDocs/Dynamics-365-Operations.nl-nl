--- 
title: Een leveranciersfactuur in het factuurjournaal registreren
description: Deze taakbegeleiding toont hoe leveranciersfacturen moeten worden geregistreerd die niet aan inkooporders zijn gekoppeld.
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 127875443da1d43783440083b11afd423f2a12fe
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Een leveranciersfactuur in het factuurjournaal registreren

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze taakbegeleiding toont hoe leveranciersfacturen moeten worden geregistreerd die niet aan inkooporders zijn gekoppeld. Voorbeelden van dit type factuur zijn onkosten voor levering of services.  Bij deze registratie wordt het demobedrijf USMF gebruikt.

1. Ga naar Leveranciers > Werkruimten > Leveranciersfactuurregistratie.
2. Klik op Nieuw factuurjournaal.
3. Klik op Nieuw.
4. Voer in het veld Naam de journaalnaam in of klik op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Typ een waarde in het veld Omschrijving.
6. Klik op Regels.
    * Voer in het datumveld de boekingsdatum in die Grootboek bijwerkt.  
7. Geef in het veld Rekening de leveranciersrekening op.
8. Voer in het veld Factuur het factuurnummer in.
9. Typ een waarde in het veld Omschrijving.
10. Voer een nummer in het veld Credit in.
11. Voer in het veld Tegenrekening het rekeningnummer in of klik op de vervolgkeuzeknop om de zoekopdracht te openen
    * De btw-groep is afkomstig van de leveranciersrekening.  
    * De btw-groep van het artikel is afkomstig van de hoofdrekening die is opgegeven in het veld Tegenrekening.  
    * De vervaldatum wordt berekend aan de hand van de betalingsvoorwaarden.  
    * De contantkorting is afkomstig van de leveranciersrekening.  
12. Klik op Boeken.
13. Sluit de pagina.


