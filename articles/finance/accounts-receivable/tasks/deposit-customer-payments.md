---
title: Klantbetalingen storten
description: Stort klantbetalingen.
author: ShivamPandey-msft
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ed692d9c82fd496e31258a70415db1838d99313
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/05/2022
ms.locfileid: "8714028"
---
# <a name="deposit-customer-payments"></a>Klantbetalingen storten

[!include [banner](../../includes/banner.md)]

Stort klantbetalingen. Bij deze taak wordt het demobedrijf USMF gebruikt.

1. Ga naar het **Navigatiedeelvenster > Modules > Klanten > Betalingen > Betalingsjournaal**.
2. Selecteer **Nieuw**.
3. Selecteer in het veld **Naam** **CustPay** in het vervolgkeuzemenu.
4. Selecteer **Regels**
5. Voer in het veld **Rekening** de klant in voor wie u de betaling hebt vastgelegd.
6. Voer in het veld **Credit** het bedrag van de betaling in. U kunt ervoor kiezen het bedrag leeg te laten en dit door het systeem te laten berekenen door de facturen te selecteren die zijn betaald.  
7. Typ een waarde in het veld **Betalingsverwijzing**. De betalingsverwijzing kan het chequenummer zijn voor de betaling die u invoert. De betalingsverwijzing is vereist om de betaling op te nemen op een depositostrook.  
8. Schakel het selectievakje Depositostrook gebruiken in. Als de betaling in de storting moet worden opgenomen, wijzigt u deze instelling in Ja.  
9. Selecteer **Nieuw**.
10. Selecteer in het veld **Rekening** de klant voor de volgende betaling.
11. Voer in het veld **Credit** het betalingsbedrag in.
12. Typ een waarde in het veld **Betalingsverwijzing**.
13. Schakel het selectievakje **Depositostrook gebruiken** in.
14. Selecteer **Boeken**. Betalingen moeten worden geboekt voordat de depositostrook kan worden gegenereerd. Dit moet ervoor zorgen dat betalingen niet veranderen nadat de depositostrook is gegenereerd.  
15. Selecteer **Functies**.
16. Selecteer **Depositostrook**.
17. Selecteer **OK**. De eerste pagina wordt gebruikt om de depositostrook te maken.  
18. Selecteer **OK**. De tweede stap is het afdrukken van de depositostrook, maar deze stap is niet vereist.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
