---
title: Een nieuwe leveranciersbankrekening maken
description: Deze procedure laat u zien hoe u een bankrekening maakt voor een leverancier.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: deb3587667ac13b95617ec219995bfef931df00c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "360619"
---
# <a name="create-a-vendor-bank-account"></a>Een nieuwe leveranciersbankrekening maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat u zien hoe u een bankrekening maakt voor een leverancier. U kunt deze procedure gebruiken in het demobedrijf USMF.

1. Ga naar Inkoop en sourcing > Leveranciers > Alle leveranciers.
2. Selecteer de leverancier waarvoor u een bankrekening wilt maken en klik vervolgens op de koppeling van de id van de leveranciersrekening.
3. Klik in het actievenster op Leverancier.
4. Klik op Bankrekeningen.
5. Klik op Nieuw.
6. Typ een waarde in het veld Bankrekening.
    * Deze id wordt gebruikt om de bankrekening in de leverancierrecord te identificeren.  
7. Typ een waarde in het veld Naam.
8. Typ of selecteer een waarde in het veld Bankgroepen.
9. Selecteer een optie in het veld Routenummertype.
    * Dit is het type routenummer dat wordt gebruikt voor internationale betalingen.  
10. Typ een waarde in het veld Bankrekeningnummer.
11. Typ een waarde in het veld SWIFT-code.
12. Typ een waarde in het veld IBAN.
    * Het IBAN-nummer moet de juiste indeling hebben. U kunt bijvoorbeeld DE89370400440532013000 gebruiken.  
    * De status van de bankrekening is Actief als de begindatum is bereikt en de vervaldatum niet is overschreden. De bankrekening is tevens actief als zowel het veld Begindatum als het veld Vervaldatum leeg is gelaten. Als de datums in de velden Begindatum en Vervaldatum beide in de toekomst liggen, zijn er geen elektronische betalingen beschikbaar. Andere betalingstypen zijn wel beschikbaar en de bankrekening is actief.  
13. Vouw de sectie Instellingen uit.
14. Typ een waarde in het veld Tekstcode.
    * Dit veld bevat een code die op het bankafschrift van de ontvanger wordt weergegeven.  
15. Typ een waarde in het veld Bericht aan bank.
16. Typ een waarde in het veld Verwijzing uitwisseling.
    * Dit is het verwijzingsnummer voor een eventuele termijnkoers of vaste wisselkoers  
17. Typ of selecteer een waarde in het veld Valuta.
    * Wanneer voorafmeldingen worden afgegeven, bevat deze sectie een overzicht van hun status (in behandeling of goedgekeurd).  
18. Vouw de sectie Adres uit.
19. Vouw de sectie Voorafmeldingen uit.
20. Vouw de sectie Contactpersoon uit.
21. Typ een waarde in het veld Telefoon.
22. Sluit de pagina.
23. Klik op Bewerken.
24. Vouw de sectie Betaling uit.
25. Selecteer in het veld Bankrekening de rekening die u zojuist hebt gemaakt.
26. Klik op Opslaan.
    * Het adres kan worden overgenomen vanuit de bankgroep, als deze is opgegeven, of u kunt het hier toevoegen.  

