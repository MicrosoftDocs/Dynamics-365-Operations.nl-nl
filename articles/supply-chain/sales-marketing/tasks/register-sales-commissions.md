--- 
title: Verkoopprovisies registreren
description: Deze procedure toont hoe verkoopprovisies worden berekend en geregistreerd.
author: omulvad
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 5535f1627526b97ddc9ca2c210db4e332782d656
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="register-sales-commissions"></a>Verkoopprovisies registreren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure toont hoe verkoopprovisies worden berekend en geregistreerd. U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens. Voordat u deze handleiding start, voert u de handleiding 'Regels voor verkoopprovisie instellen' uit om ervoor te zorgen dat u alle vereiste instellingen van de provisieberekening hebt.

Noteer de klant- en artikelnummers die u voor het provisieproces hebt geselecteerd en gebruik deze wanneer u wordt aangevraagd om een verkooporder in deze handleiding te maken.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Een verkooporder factureren die een verkoper in aanmerking brengt voor provisie
1. Ga naar Verkoop en marketing > Verkooporders > Alle verkooporders.
2. Klik op Nieuw.
3. Klik in het veld Klantrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek en selecteer de gewenste record in de lijst.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik op OK.
7. Klik in het actievenster op Opties.
8. Klik op Weergave wijzigen.
9. Klik op Weergave kopteksten.
10. Vouw de sectie Instellingen uit.
    * De waarde in het veld Verkoopgroep vertegenwoordigt een groep waaraan een of meer verkopers zijn toegewezen. De personen in de groep zijn diegene die provisies zullen ontvangen wanneer de order wordt gefactureerd, volgens vooraf gedefinieerde tarieven en distributie.   De waarde wordt gekopieerd van de Klantkaart, maar u kunt deze desgewenst wijzigen.  De verkoopgroep wordt ook gekopieerd naar de verkooporderregel. U kunt deze wijzigen zodat deze verschilt van deze in de koptekst en/of tussen de regels.  
    * De waarde in het veld Provisiegroep vertegenwoordigt een groep die u voor een of meer klanten hebt gemaakt om provisies bij te houden.   De waarde wordt gekopieerd van de Klantkaart, maar u kunt deze desgewenst wijzigen.   
11. Klik in het actievenster op Opties.
12. Klik op Weergave wijzigen.
13. Klik op Regelweergave.
14. Klik in het veld Artikelnummer op de vervolgkeuzeknop om de zoekopdracht te openen.
15. Selecteer in de lijst het artikel waarvoor u provisies hebt ingesteld. 
16. Voer in het veld Hoeveelheid een getal in.
    * Let op het nettobedrag van de regel. Dit vertegenwoordigt de verkoopopbrengst, die in dit voorbeeld de basis voor provisieberekening is.  
17. Klik op Opslaan.
18. Klik in het actievenster op Factuur.
19. Klik op Factuur.
20. Vouw de sectie Parameters uit.
21. Selecteer in het veld Hoeveelheid de optie 'Alle'.
22. Selecteer Ja in het veld Boeking.
23. Klik op OK.
24. Klik op OK.
    * Het kan even duren om de transactie te boeken. Wacht tot de verwerking is voltooid en sluit de pagina niet.  

## <a name="review-the-registered-sales-commissions"></a>De geregistreerde verkoopprovisies controleren
1. Klik in het actievenster op Factuur.
2. Klik op Factuur.
3. Klik in het actievenster op Factuur.
4. Klik op Provisietransacties.
    * Het tabblad Overzicht geeft regels weer die de provisiebedragen vertegenwoordigen die aan vertegenwoordigers moeten worden betaald die aan de gefactureerde verkooporder zijn gekoppeld. Laten we de gegevens bekijken.     
    * Als u de handleiding 'Regels voor verkoopprovisie instellen' gebruikte om de provisieverkoopgroep in te stellen, zullen twee verkopers een verkoopprovisie ontvangen en is de provisie onder hen gelijk verdeeld.  
    * In dit voorbeeld wordt het totaalbedrag van de provisie berekend als een percentage van de verkoopopbrengst (het nettobedrag van de orderregel).   
5. Sluit de pagina.
6. Klik op Boekstuk.
    * U kunt de boekstuktransacties voor de provisiebedragen controleren die op de vooraf gedefinieerde rekeningen voor provisie-uitgave en te betalen provisie zijn geboekt.  


