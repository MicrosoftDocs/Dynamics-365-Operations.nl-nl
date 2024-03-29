---
title: Een nieuwe leveranciersbankrekening maken
description: Deze procedure laat u zien hoe u een bankrekening maakt voor een leverancier.
author: GalynaFedorova
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, LogisticsPostalAddressSingle
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b201f5eb2bf8eb496a761b6fc6ca729a46a85ce
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677837"
---
# <a name="create-a-vendor-bank-account"></a>Een nieuwe leveranciersbankrekening maken

[!include [banner](../../includes/banner.md)]

Deze procedure laat u zien hoe u een bankrekening maakt voor een leverancier. U kunt deze procedure gebruiken in het demobedrijf USMF.

1. Ga naar **Navigatievenster > Modules > Inkoopbeheer > Leveranciers > Alle leveranciers**.
2. Selecteer de leverancier waarvoor u een bankrekening wilt maken en klik vervolgens op de koppeling van de **id van de leveranciersrekening**.
3. Klik in het **actievenster** op **Leverancier**.
4. Klik op **Bankrekeningen**.
5. Klik in het **actievenster** op **Nieuw**.
6. Typ een waarde in het veld **Bankrekening**. Deze id wordt gebruikt om de bankrekening in de leverancierrecord te identificeren.  
7. Typ een waarde in het veld **Naam**.
8. Typ of selecteer een waarde in het veld **Bankgroepen**.
9. Selecteer een optie in het veld **Routenummertype**. Dit is het type routenummer dat wordt gebruikt voor internationale betalingen.  
10. Typ een waarde in het veld **Bankrekeningnummer**.
11. Typ een waarde in het veld **SWIFT-code**.
12. Typ een waarde in het veld **IBAN**.
    - Het IBAN-nummer moet de juiste indeling hebben. U kunt bijvoorbeeld DE89370400440532013000 gebruiken.  
    - De status van de bankrekening is Actief als de begindatum is bereikt en de vervaldatum niet is overschreden. De bankrekening is tevens actief als zowel het veld Begindatum als het veld Vervaldatum leeg is gelaten. Als de datums in de velden Begindatum en Vervaldatum beide in de toekomst liggen, zijn er geen elektronische betalingen beschikbaar. Andere betalingstypen zijn wel beschikbaar en de bankrekening is actief.  
13. Vouw de sectie **Instellingen** uit.
14. Typ een waarde in het veld **Tekstcode**. Dit veld bevat een code die op het bankafschrift van de ontvanger wordt weergegeven.  
15. Typ een waarde in het veld **Bericht aan bank**.
16. Typ een waarde in het veld **Verwijzing uitwisseling**. Dit is het verwijzingsnummer voor een eventuele termijnkoers of vaste wisselkoers
17. Typ of selecteer een waarde in het veld **Valuta**. Wanneer voorafmeldingen worden afgegeven, bevat deze sectie een overzicht van hun status (in behandeling of goedgekeurd).  
18. Vouw de sectie **Adres** uit.
19. Vouw de sectie **Voorafmeldingen** uit.
20. Vouw de sectie **Contactgegevens** uit.
21. Typ een waarde in het veld **Telefoon**.
22. Sluit de pagina.
23. Klik op **Bewerken**.
24. Vouw de sectie **Betaling** uit.
25. Selecteer in het veld **Bankrekening** de rekening die u zojuist hebt gemaakt.
26. Klik op **Opslaan**. Het adres kan worden overgenomen vanuit de bankgroep, als deze is opgegeven, of u kunt het hier toevoegen.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]