---
title: Een gepostdateerde cheque voor een leverancier vereffenen
description: Vereffen een gepostdateerde cheque die aan een leverancier is uitgeschreven wanneer de bank de chequetransactie heeft verrekend nadat de cheque achterstallig was en door de bank werd verrekend.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89acad0c9421960ff4d07ed8eec798b9068424d5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834566"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a>Een gepostdateerde cheque voor een leverancier vereffenen

[!include [banner](../../includes/banner.md)]

Vereffen een gepostdateerde cheque die aan een leverancier is uitgeschreven wanneer de bank de chequetransactie heeft verrekend nadat de cheque achterstallig was en door de bank werd verrekend. 

Voer de volgende procedures uit voordat u deze start.

1) Gepostdateerde cheques instellen

2) Een gepostdateerde cheque voor een leverancier registreren en boeken



De rol van deze procedure is penningmeester. Bij deze procedure wordt het demobedrijf USMF gebruikt.

1. Ga naar Leveranciers > Betalingen > Gepostdateerde cheques van leverancier.
2. Klik op Vereffenen.
3. Klik op Aflossingstransacties vereffenen.
    * Vereffen de leveranciersrekening voor de chequetransactie.  
4. Sluit de pagina.
5. Ga naar Grootboek > Journaalboekingen > Algemene journalen.
6. Selecteer 'Alle' in het veld Weergeven.
7. Schakel het selectievakje Alleen door de gebruiker gemaakte journalen weergeven in of uit.
8. Markeer in de lijst de geselecteerde rij.
9. Klik op Regels.
10. Klik op Boekstuk.
11. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]