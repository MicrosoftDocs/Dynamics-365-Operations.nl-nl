---
title: Een gepostdateerde cheque van een klant vereffenen
description: U kunt een gepostdateerde cheque vereffenen nadat de cheque is verrekend door de bank.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 635a1c50390bca59cd1c9ba0cf0421c510b2998c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841844"
---
# <a name="settle-a-postdated-check-from-a-customer"></a>Een gepostdateerde cheque van een klant vereffenen

[!include [task guide banner](../../includes/task-guide-banner.md)]

U kunt een gepostdateerde cheque vereffenen nadat de cheque is verrekend door de bank. Met deze financiële transactie boekt u ook de overbruggingsrekeningtransactie over voor de gepostdateerde cheque. 

De volgende taken moeten zijn voltooid voordat u deze start.

1) Gepostdateerde cheques instellen

2) Een gepostdateerde cheque voor een klant registreren en boeken 



De rol van deze taakbegeleidingen is penningmeester.



Bij deze procedure wordt het demobedrijf USMF gebruikt.

1. Ga naar Crediteringen en aanmaningen > Query's en rapporten > Betalingen > Gepostdateerde cheques van klant.
2. Klik op Vereffenen.
3. Klik op Aflossingstransacties vereffenen.
    * Vereffen de klantrekening voor de chequetransactie.  
4. Sluit de pagina.
5. Ga naar Grootboek > Journaalboekingen > Algemene journalen.
6. Selecteer een optie in het veld Weergeven.
7. Schakel het selectievakje Alleen door de gebruiker gemaakte journalen weergeven in of uit.
8. Zoek en selecteer de gewenste record in de lijst.
9. Klik op Regels.
10. Klik op Boekstuk.
11. Sluit de pagina.

