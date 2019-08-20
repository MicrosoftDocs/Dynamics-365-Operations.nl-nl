---
title: Klantbetalingen storten
description: Stort klantbetalingen.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: afbf74d1cf3dc87e97dda0873115b5c7fa49ca3d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834458"
---
# <a name="deposit-customer-payments"></a>Klantbetalingen storten

[!include [task guide banner](../../includes/task-guide-banner.md)]

Stort klantbetalingen. Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga naar Klanten > Betalingen > Betalingsjournaal.
2. Klik op Nieuw.
3. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Selecteer het betalingsjournaal. 
5. Klik op Regels.
6. Voer in het veld Rekening de klant in voor wie u de betaling hebt vastgelegd.
7. Voer in het veld Credit het bedrag van de betaling in.
    * U kunt ervoor kiezen het bedrag leeg te laten en dit door het systeem te laten berekenen door de facturen te selecteren die zijn betaald.  
8. Typ een waarde in het veld Betalingsverwijzing.
    * De betalingsverwijzing kan het chequenummer zijn voor de betaling die u invoert. De betalingsverwijzing is vereist om de betaling op te nemen op een depositostrook.  
9. Schakel het selectievakje Depositostrook gebruiken in.
    * Als de betaling in de storting moet worden opgenomen, wijzigt u deze instelling in Ja.  
10. Klik op Nieuw.
11. Selecteer in het veld Rekening de klant voor de volgende betaling.
12. Voer in het veld Credit het betalingsbedrag in.
13. Typ een waarde in het veld Betalingsverwijzing.
14. Schakel het selectievakje Depositostrook gebruiken in.
15. Klik op Boeken.
    * Betalingen moeten worden geboekt voordat de depositostrook kan worden gegenereerd. Dit moet ervoor zorgen dat betalingen niet veranderen nadat de depositostrook is gegenereerd.  
16. Klik op Functies.
17. Klik op Depositostrook.
18. Klik op OK.
    * De eerste pagina wordt gebruikt om de depositostrook te maken.  
19. Klik op OK.
    * De tweede stap is het afdrukken van de depositostrook, maar deze stap is niet vereist.  

