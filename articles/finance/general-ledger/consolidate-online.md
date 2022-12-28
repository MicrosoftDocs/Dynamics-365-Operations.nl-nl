---
title: Online financiële consolidaties
description: Dit artikel beschrijft online financiële consolidaties in het grootboek.
author: aprilolson
ms.date: 12/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 5843ac78adf32e738d9882c7f4e9e04a79200700
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838251"
---
# <a name="online-financial-consolidations"></a>Online financiële consolidaties

[!include [banner](../includes/banner.md)]

Dit artikel beschrijft online financiële consolidaties in het grootboek. Voordat u dit artikel leest, moet u eerst het artikel [Overzicht van Financiële consolidaties en valutaomzetting](financial-consolidations-currency-translation.md) lezen.

Nadat u uw instellingen hebt voltooid, voert u de details van de consolidatie in op de pagina **Consolideren [online]**. Wanneer u klaar bent, kunt u klikken op **OK** of **Batch** om de consolidatie te verwerken.

## <a name="criteria"></a>Criteria
Op het tabblad **Criteria** van de pagina **Consolideren [online]** definieert u de rekeningen, de perioden en het type gegevens dat wordt geconsolideerd.

![Tabblad Criteria.](./media/criteria-consolidate-online.png "Tabblad Criteria")

Hier volgt een uitleg van de verschillende velden op dit tabblad:

- **Beschrijving**: voer een nauwkeurigere omschrijving in voor de periode die u consolideert.
- **Hoofdrekening**: gebruik de velden in deze sectie voor het definiëren van de hoofdrekeningen die worden verwerkt.

    - **Van** en **Tot**: geef een bereik rekeningen op die u wilt verwerken. Als u deze velden leeg laat, worden alle rekeningen van alle bedrijven verplaatst naar het consolidatiebedrijf. Als u vier bedrijven consolideert en elk bedrijf een ander rekeningschema heeft, worden daarom alle rekeningen van alle vier de bedrijven gemaakt in het consolidatiebedrijf.
    - **Consolidatierekening gebruiken**: als u deze optie instelt op **Ja**, wordt het veld **Consolidatierekening selecteren in** beschikbaar. Geef in dit veld aan of alle rekeningen moeten worden geconsolideerd naar de consolidatierekening die is ingesteld op de pagina **Hoofdrekeningen** of dat u de rekening wilt selecteren uit een van de groepen met consolidatierekeningen.
    - **Consolidatierekeninggroep**: selecteer de groep die moet worden gebruikt voor de toewijzing van de hoofdrekening voor de consolidatie.

- **Consolidatieperiode**: gebruik de velden in deze sectie voor het definiëren van de consolidatieperiode.

    - **Van** en **Tot**: geef een datumbereik voor de consolidatie op. Als u deze velden leeg laat, wordt de consolidatie verwerkt voor alle perioden die zijn gedefinieerd in de grootboekkalender voor het bedrijf. Het wordt afgeraden deze velden leeg te laten.
    - **Consolidatiebedrag selecteren van**: gebruik dit veld om op te geven of de bedragen in de boekhoudingsvaluta of de aangiftevalutabedragen van de bronbedrijven worden gebruikt om de bedragen in de boekhoudingsvaluta van het consolidatiebedrijf bij te werken.

        - Selecteer **Valuta voor boekhouding** om de bedragen van de boekhoudingsvaluta van de bronbedrijven te gebruiken om de bedragen van de boekhoudingsvaluta in het consolidatiebedrijf bij te werken. Als deze waarde is geselecteerd, gebruikt u het veld **Valuta voor boekhouding consolideren** om te definiëren hoe de valuta's voor boekhouding in het consolidatiebedrijf worden berekend.
        - Selecteer **Aangiftevaluta** om de bedragen van de aangiftevaluta van de bronbedrijven te gebruiken om de bedragen van de boekhoudingsvaluta in het consolidatiebedrijf te berekenen.

            - Als de aangiftevaluta van het bronbedrijf gelijk is aan de valuta voor boekhouding van het consolidatiebedrijf, worden de bedragen van de aangiftevaluta gekopieerd uit het bronbedrijf naar het consolidatiebedrijf.
            - Als de aangiftevaluta van het bronbedrijf verschilt van de valuta voor boekhouding van het consolidatiebedrijf, worden de waarden omgerekend met behulp van de koersgegevens die zijn gedefinieerd op het tabblad **Valutaomzetting** van deze pagina om de consolidatiebedrijfswaarden te berekenen.

    - **Valuta voor boekhouding consolideren**: dit veld is alleen beschikbaar als het veld **Consolidatiebedrag selecteren uit** is ingesteld op **Valuta voor boekhouding**. Gebruik dit om op te geven of de bedragen in de valuta voor boekhouding van de bronbedrijven worden omgerekend via wisselkoersen of worden gekopieerd naar het consolidatiebedrijf. Selecteer **Valutaomzetting gebruiken** om de wisselkoersgegevens te gebruiken die zijn gedefinieerd op het tabblad **Valutaomzetting** om de consolidatieboekhoudingsaldi te berekenen. Selecteer **Bedrag in valuta voor boekhouding gebruiken** om de bedragen van de boekhoudingsvaluta van de bronbedrijven te kopiëren naar het consolidatiebedrijf.

        - Als de valuta voor boekhouding van het bronbedrijf gelijk is aan de valuta voor boekhouding van het consolidatiebedrijf, worden de bedragen van de aangiftevaluta gekopieerd uit het bronbedrijf naar het consolidatiebedrijf.
        - Als de valuta voor boekhouding van het bronbedrijf verschilt van de valuta voor boekhouding van het consolidatiebedrijf, worden de waarden omgerekend met behulp van de koersgegevens die zijn gedefinieerd op het tabblad **Valutaomzetting** van deze pagina om de consolidatiebedrijfswaarden te berekenen.

    - **Werkelijke bedragen opnemen**: stel deze optie in op **Ja** om uw werkelijke gegevens te consolideren.
    - **Budgetbedragen opnemen**: stelt deze optie in op **Ja** om gegevens uit het budgetregister te consolideren.
    - **Saldi opnieuw opbouwen tijdens consolidatieproces**: het wordt afgeraden deze optie in te stellen op **Ja**. Bouw in plaats daarvan saldi opnieuw op als een afzonderlijke batchtaak.

- **Budgetmodellen**: als u hebt aangegeven dat budgetgegevens moeten worden geconsolideerd, gebruikt u de velden in deze sectie om de budgetmodellen te definiëren.

    - **Van** en **Tot**: geef het bereik modellen op die u wilt gebruiken.
    - **Koerstype budget**: selecteer het koerstype voor het budget dat moet worden gebruikt voor valutaomrekening van budgetgegevens.

## <a name="financial-dimensions"></a>Financiële dimensies
Op het tabblad **Financiële dimensies** definieert u de dimensies die moeten worden opgenomen in het consolidatiebedrijf. Als u een dimensie wilt selecteren, stelt u het veld **Specificatie** in op **Dimensie**, en definieert u vervolgens de volgorde van de dimensie in het consolidatiebedrijf.

![Tabblad Financiële dimensies.](./media/financial-dimensions-cons.png "Tabblad Financiële dimensies")

Ongeacht de volgorde die u definieert, is **Hoofdrekening** altijd het eerste segment.

## <a name="legal-entities"></a>Rechtspersonen
Op het tabblad **Rechtspersonen** definieert u de bedrijven die moeten worden opgenomen in het consolidatiebedrijf. U definieert ook het eigendomspercentage van die bedrijven. Als u eigendom van minder dan 100 procent opgeeft, wordt het opgegeven percentage opgeteld voor het consolidatiebedrijf. Voor omrekeningsverschillen wordt het veld **Rekeningtype voor omrekeningsverschillen** gebruikt om de hoofdrekening te selecteren uit de instellingen op de pagina **Rekeningen voor automatische transacties**.

![Tabblad Rechtspersonen.](./media/legal-entities-cons.png "Tabblad Rechtspersonen")

![Pagina Rekeningen voor automatische transacties.](./media/accounts-for-automatic-cons.png "Pagina Rekeningen voor automatische transacties")

## <a name="elimination"></a>Schrapping
Op het tabblad **Schrapping** hebt u drie opties voor de verwerking van de schrappingen:

- Selecteer de schrappingsregel en selecteer vervolgens in het veld **Voorstelopties** **Alleen voorstel**. Met deze optie wordt de schrapping tijdens het consolidatieproces verwerkt, maar niet alles wordt in één stap geboekt. U kunt het journaal later boeken.
- Selecteer de schrappingsregel en selecteer vervolgens in het veld **Voorstelopties** **Alleen boeken**. Met deze optie wordt de schrapping tijdens het consolidatieproces verwerkt en wordt alles in één stap geboekt.
- Voer een schrappingsvoorstel apart van het consolidatieproces uit met behulp van het schrappingsjournaal.

![Tabblad Schrapping.](./media/elimination-cons-onl.png "Tabblad Schrapping")

Zie voor meer informatie over schrappingen [Schrappingsregels](./elimination-rules.md).

## <a name="currency-translation"></a>Valutaomzetting
Op het tabblad **Valutaomrekening** definieert u de rechtspersoon, de rekening, het wisselkoerstype en het tarief. Als het consolidatiebedrijf is toegewezen aan andere hoofdrekeningen dan het bronbedrijf, moet de hoofdrekening van het consolidatiebedrijf worden ingevoerd in de velden **Begindatum** en **Einddatum**, niet in de hoofdrekeningen van het bronbedrijf. Voor elke rij met rechtspersoon en hoofdrekeningen zijn drie opties beschikbaar in het veld **Wisselkoers toepassen van**:

- **Consolidatiedatum**: de datum die is gedefinieerd in het veld **Einde consolidatieperiode** op het tabblad **Criteria** voor de consolidatie wordt gebruikt om de wisselkoers op te halen. Dit tarief is gelijk aan het plaatstarief of eindemaandtarief. U ziet een voorbeeld van het tarief, maar u kunt het niet bewerken.
- **Transactiedatum**: de datum van elke transactie wordt gebruikt voor het selecteren van een wisselkoers. Deze optie wordt meestal gebruikt voor vaste activa en wordt vaak een historische wisselkoers genoemd. U kunt geen voorbeeld van het tarief zien, omdat er veel tarieven voor de verschillende transacties in het rekeningbereik zijn.
- **Door gebruiker gedefinieerde tarief**: nadat u deze optie hebt geselecteerd, kunt u de gewenste wisselkoers invoeren. Deze optie kan handig zijn voor gemiddelde wisselkoersen of als u consolideert met een vaste wisselkoers.

![Tabblad Valutaomzetting.](./media/currency-translation-cons-online.png "Tabblad Valutaomzetting")

## <a name="additional-resources"></a>Aanvullende bronnen

Zie het bovenliggende artikel van dit artikel [Overzicht van Financiële consolidaties en valutaomzetting](./financial-consolidations-currency-translation.md) voor meer informatie over consolidatie en valutaomrekeningen.

Zie voor informatie over scenario's waarin u mogelijk geconsolideerde financiële overzichten genereert [Geconsolideerde financiële overzichten genereren](./generating-consolidated-financial-statements.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
