---
title: Verkoopprovisies registreren
description: In dit artikel wordt beschreven hoe verkoopprovisies worden berekend en geregistreerd.
author: Henrikan
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  CustInvoiceJournal, CommissionTrans, LedgerTransVoucher, CustClassificationGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b15ca78da14068fd2f3275e7aff04852625db7ee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862506"
---
# <a name="register-sales-commissions"></a>Verkoopprovisies registreren

[!include [banner](../../includes/banner.md)]

In dit artikel wordt beschreven hoe verkoopprovisies worden berekend en geregistreerd. U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens. Voordat u deze guide start, voert u de guide 'Regels voor verkoopprovisie instellen' uit om ervoor te zorgen dat u alle vereiste instellingen van de provisieberekening hebt.

Noteer de klant- en artikelnummers die u voor het provisieproces hebt geselecteerd en gebruik deze wanneer u wordt aangevraagd om een verkooporder in deze guide te maken.


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a>Een verkooporder factureren die een verkoper in aanmerking brengt voor provisie
1. Ga in het navigatievenster naar **Modules > Verkoop en marketing > Verkooporders > Alle verkooporders**.
2. Selecteer **Nieuw**.
3. Selecteer in het veld **Klantrekening** de gewenste record in het vervolgkeuzemenu.
4. Selecteer **OK**.
5. Selecteer **Opties** in het actievenster.
6. Selecteer **Weergave wijzigen**.
7. Selecteer **Weergave kopteksten**.
8. Vouw de sectie **Instellingen** uit.

    - De waarde in het veld **Verkoopgroep** vertegenwoordigt een groep waaraan een of meer verkopers zijn toegewezen. De personen in de groep zijn diegene die provisies zullen ontvangen wanneer de order wordt gefactureerd, volgens vooraf gedefinieerde tarieven en distributie.   
    - De waarde wordt gekopieerd van de Klantkaart, maar u kunt deze desgewenst wijzigen.  
    - De verkoopgroep wordt ook gekopieerd naar de verkooporderregel. U kunt deze wijzigen zodat deze verschilt van deze in de koptekst en/of tussen de regels.  
    - De waarde in het veld **Provisiegroep** vertegenwoordigt een groep die u voor een of meer klanten hebt gemaakt om provisies bij te houden.   
    - De waarde wordt gekopieerd van de Klantkaart, maar u kunt deze desgewenst wijzigen.   

9. Selecteer **Opties** in het actievenster.
10. Selecteer **Weergave wijzigen**.
11. Selecteer **Regelweergave**.
12. Selecteer in de vervolgkeuzelijst van het veld **Artikelnummer** het artikel dat u voor commissies hebt ingesteld. 
13. Voer een getal in het veld **Hoeveelheid** in. Let op het nettobedrag van de regel. Dit vertegenwoordigt de verkoopopbrengst, die in dit voorbeeld de basis voor provisieberekening is.  
14. Selecteer **Opslaan**.
15. Selecteer **Factuur** in het actievenster.
16. Selecteer **Factuur**.
17. Vouw de sectie **Parameters** uit.
18. Selecteer in het veld **Hoeveelheid** de optie **Alle**.
19. Selecteer **Ja** in het veld **Boeking**.
20. Selecteer **OK** en selecteer **OK** in het volgende venster. Het kan even duren om de transactie te boeken. Wacht tot de verwerking is voltooid en sluit de pagina niet.  

## <a name="review-the-registered-sales-commissions"></a>De geregistreerde verkoopprovisies controleren
1. Selecteer **Factuur** in het actievenster en selecteer vervolgens opnieuw **Factuur**.
2. Selecteer **Factuur** in het actievenster en selecteer vervolgens **Provisietransacties**.

    - Het tabblad **Overzicht** geeft regels weer die de provisiebedragen vertegenwoordigen die aan vertegenwoordigers moeten worden betaald die aan de gefactureerde verkooporder zijn gekoppeld. Laten we de gegevens bekijken.  
    - Als u de guide 'Regels voor verkoopprovisie instellen' gebruikte om de groep **Provisieverkoop** in te stellen, zullen twee verkopers een verkoopprovisie ontvangen en is de provisie onder hen gelijk verdeeld.  
    - In dit voorbeeld wordt het totaalbedrag van de provisie berekend als een percentage van de verkoopopbrengst (het nettobedrag van de orderregel).  
3. Sluit de pagina.
4. Selecteer **Boekstuk**. U kunt de boekstuktransacties voor de provisiebedragen controleren die op de vooraf gedefinieerde rekeningen voor provisie-uitgave en te betalen provisie zijn geboekt.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]