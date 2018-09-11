--- 
title: Een gepostdateerde cheque voor een leverancier vereffenen
description: Vereffen een gepostdateerde cheque die aan een leverancier is uitgeschreven wanneer de bank de chequetransactie heeft verrekend nadat de cheque achterstallig was en door de bank werd verrekend.
author: kweekley
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 7520f587f5fb05937047b814570c00f8212bad82
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="settle-a-postdated-check-for-a-vendor"></a>Een gepostdateerde cheque voor een leverancier vereffenen

[!include [task guide banner](../../includes/task-guide-banner.md)]

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


