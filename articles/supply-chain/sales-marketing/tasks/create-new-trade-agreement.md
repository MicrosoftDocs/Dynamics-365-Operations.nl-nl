---
title: Een nieuwe handelsovereenkomst maken
description: Deze procedure laat zien hoe u een handelsovereenkomst maakt waarin u een nieuwe productverkoopprijs registreert die u met een specifieke klant bent overeengekomen.
author: Henrikan
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24290ec873da9e871c001bcdc97e14dcad0e3d1e
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111102"
---
# <a name="create-a-new-trade-agreement"></a>Een nieuwe handelsovereenkomst maken

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een handelsovereenkomst maakt waarin u een nieuwe productverkoopprijs registreert die u met een specifieke klant bent overeengekomen. U kunt deze procedure uitvoeren in het demogegevensbedrijf USMF of met uw eigen gegevens. Als u uw eigen gegevens gebruikt, moet u voordat u deze guide start ervoor zorgen dat er een handelsovereenkomstjournaal bestaat met de naam Standaard, waarvan de relatie is ingesteld op "Prijs (verkoop)".

## <a name="create-and-post-a-new-trade-agreement-journal"></a>Een nieuw handelsovereenkomstjournaal maken en boeken

1. Ga naar **Navigatievenster > Modules > Verkoop en marketing > Prijzen en kortingen > Handelsovereenkomstjournalen**.
2. Klik op **Nieuw**.
3. Klik in het veld **Naam** op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek en selecteer de gewenste record in de lijst.
5. Klik in het **actievenster** op **Regels**.
6. Selecteer Tabel in het veld **Rekeningcode**.
    
    In dit voorbeeld werkt u de prijs voor een specifieke klant bij, wat betekent dat u mogelijk Tabel moet kiezen. Als u de catalogusprijs van het product zou bijwerken, zou u Alle selecteren, zodat de nieuwe prijs voor alle klanten geldt. Als u onderscheid zou maken tussen verschillende prijzen uit verschillende klantsegmenten, zou u Groep selecteren. Als u Groep wilt selecteren, moet u klantprijsgroepen hebben ingesteld.  

7. Klik in het veld **Account selecteren** op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Zoek en selecteer de gewenste record in de lijst.
9. Selecteer Tabel in het veld **Artikelcode**.
    
    Wanneer u een handelsovereenkomst van het type Prijs (verkoop) invoert, moet u alleen Tabel selecteren in het veld **Artikelcode**. Dit komt doordat een prijs een absolute waarde is en niet voor alle producten of groep producten hetzelfde kan zijn.
    
10. Klik in het veld **Artikelrelatie** op de vervolgkeuzeknop om de zoekopdracht te openen.
11. Selecteer in de lijst het product dat u in de overeenkomst wilt opnemen. Maak een notitie van het product dat u hebt geselecteerd.  
12. Voer in het veld **Van** een minimumhoeveelheid in.
    - Als de klant een minimumhoeveelheid moet bestellen voordat deze voor de nieuwe prijs in aanmerking komt, moet u die hoeveelheid hier opgeven.  
    - Voer een waarde in het veld **Tot** in om de maximale hoeveelheid op te geven waarboven de prijs van de overeenkomst niet geldig is. Als u prijzen en kortingen aanbiedt op basis van meerdere hoeveelheidscategorieën, geeft u elke hoeveelheidsbracket op als een minimum- en een maximumwaarde in het veld **Van** en het veld **Tot**.
13. Voer in het veld **Bedrag in valuta** een prijs in.
14. Voer in de sectie **Details** in het veld **Begindatum** een datum in waarop deze overeenkomst geldig is.
15. Klik op **Opslaan**.
16. Klik op **Valideren**.
17. Klik op **Geselecteerde regels valideren**.
18. Klik op **OK**.
19. Klik op **Boeken**.
20. Klik op **OK**.

## <a name="view-trade-agreements-for-a-product"></a>Handelsovereenkomsten voor een product weergeven

1. Ga naar **Navigatievenster > Modules > Productgegevensbeheer > Producten > Vrijgegeven producten**.
2. Zoek en selecteer in de lijst het product waarvan u de prijs zojuist hebt bijgewerkt.
3. Klik in het **actievenster** op **Verkopen**.
4. Klik op **Handelsovereenkomsten weergeven**.
    
    Controleer de gegevens van de prijshandelsovereenkomst die u zojuist hebt gemaakt.

5. Sluit de pagina.

## <a name="additional-resources"></a>Aanvullende bronnen

### <a name="whitepaper"></a>Whitepaper

Download de volgende whitepaper (geschreven ter ondersteuning van AX2012, maar is nog steeds van toepassing op Dynamics 365 Supply Chain Management) voor meer informatie.

- [Handelsovereenkomsten](https://download.microsoft.com/download/0/2/9/02972c8b-0159-4936-a3ef-1e64252b2d2f/TradeAgreementsInAX.pdf)

### <a name="community-blogs"></a>Community-blogs

- [Verkoopprijzen in Finance + Operations](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
