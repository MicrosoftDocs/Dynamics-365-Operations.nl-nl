---
title: Een leveranciersfactuur in het factuurjournaal registreren
description: Deze taakbegeleiding toont hoe leveranciersfacturen moeten worden geregistreerd die niet aan inkooporders zijn gekoppeld.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace, LedgerJournalTable, LedgerJournalTransVendInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 775f3764d34cecbfc071ff7420d32c7832b42308
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "348935"
---
# <a name="record-a-vendor-invoice-in-the-invoice-journal"></a>Een leveranciersfactuur in het factuurjournaal registreren

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

