---
title: Geconsolideerde financiële overzichten genereren
description: Dit onderwerp beschrijft de verschillende scenario's waarin u geconsolideerde financiële overzichten kunt genereren.
author: aprilolson
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: dce0dd216d552d956ba7fdbcb4eebb6ed85b7115
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348957"
---
# <a name="generate-consolidated-financial-statements"></a>Geconsolideerde financiële overzichten genereren

[!include [banner](../includes/banner.md)]

Dit onderwerp beschrijft de verschillende scenario's waarin u geconsolideerde financiële overzichten kunt genereren.

## <a name="single-level-and-multilevel-consolidations-across-legal-entities"></a>Consolidaties op één niveau en meerdere niveaus voor rechtspersonen
De eenvoudigste methode voor consolidatie met behulp van Financiële rapportage is het gebruik van rapporteringsstructuren om gegevens te aggregeren voor bedrijven met hetzelfde rekeningschema en dezelfde boekperioden. Hier vindt u de hoofdstappen om te consolideren met behulp van een rapporteringsstructuur.

1. Maak een rijdefinitie en zorg ervoor dat alle juiste rekeningen in alle bedrijven in de rijen zijn opgenomen.
2. Maak een kolomdefinitie die bestaat uit alle kolommen die zijn vereist voor het rapport dat u maakt.
3. Maak een rapporteringsstructuur dat een rapporteringsknooppunt bevat voor elk bedrijf dat u in geconsolideerde rapporten gebruikt.

> [!TIP]
> Zie voor meer informatie over het maken en beheren van rijdefinities, kolomdefinities en rapporteringsstructuren [Onderdelen van een financieel rapport](../../fin-ops-core/dev-itpro/analytics/financial-report-components.md).

In de volgende afbeelding ziet u hoe u een rapporteringsstructuurdefinitie kunt gebruiken in Financiële rapportage om elk bedrijf te identificeren dat u consolideert.

![Rapportagestructuurdefinitie.](./media/reporting-tree-definition.png "Rapportagestructuurdefinitie")

Zoals het geconsolideerde rapport in de volgende afbeelding laat zien, kunt u wanneer u de rapporteringsstructuur samen met een rapportdefinitie gebruikt, elk bedrijf afzonderlijk weergeven. De geconsolideerde bedragen worden weergegeven op overzichtsniveau.

![Geconsolideerd bedrag op overzichtsniveau.](./media/consolidate-amount-summary-level.png "Geconsolideerd bedrag op overzichtsniveau")

Ook kunt u een rapporteringsstructuur met meerdere niveaus maken met zoveel niveaus als u nodig hebt. In de volgende afbeelding ziet u een rapporteringsstructuurdefinitie met meerdere niveaus, die getotaliseerde gegevens op basis van wereldwijd gebied bevat.

![Rapporteringsstructuurdefinitie met totalisaties met meerdere niveaus per regio.](./media/multilevel-reporting-tree-definition-roll-ups-worldwide-region.png "Rapporteringsstructuurdefinitie met totalisaties met meerdere niveaus per regio")

In de volgende afbeelding ziet u een rapporteringsstructuurdefinitie met meerdere niveaus, die getotaliseerde gegevens op basis van functie bevat.

![Rapporteringsstructuurdefinitie met totalisaties met meerdere niveaus per functie.](./media/multilevel-reporting-tree-definition-roll-ups-by-function.png "Rapporteringsstructuurdefinitie met totalisaties met meerdere niveaus per functie")

### <a name="viewing-companies-side-by-side"></a>Bedrijven naast elkaar weergeven
Veel klanten geven de voorkeur aan rapporten waarin de bedrijven naast elkaar worden weergegeven en waarin in een kolom het geconsolideerde totaal wordt getoond. Deze indeling is gemakkelijk voor elkaar te krijgen nadat u de rapporteringsstructuur hebt gemaakt. Hier worden de hoofdstappen beschreven om bedrijven naast elkaar weer te geven in geconsolideerde financiële overzichten.

1. Maak een kolomdefinitie die een kolom **Financiële dimensie** voor elk bedrijf bevat.
2. Gebruik het veld **Rapporteringseenheid** om de structuur en de rapporteringseenheid voor elke kolom te selecteren.
3. Optioneel: voeg kopteksten en totaal aantal kolommen toe.

In de volgende afbeelding ziet u een kolomdefinitie in een indeling naast elkaar.

![Kolomdefinitie in een indeling naast elkaar.](./media/column-definition-side-by-side-format.png "Kolomdefinitie in een indeling naast elkaar")

## <a name="consolidations-that-use-organization-structures-that-are-created-from-legal-entities"></a>Consolidaties waarin organisatiestructuren worden gebruikt die worden gemaakt van rechtspersonen
Met organisatiehiërarchieën die dimensies of rechtspersonen bevatten, worden op dynamische wijze rapporteringsstructuurdefinities gemaakt in Financiële rapportage. Een eenvoudige manier om consolidaties te stroomlijnen is een organisatiehiërarchie toe te voegen aan uw rapport in Financiële rapportage. Op basis van de rapportdatum wordt in Financial Reporting de organisatiehiërarchie op of vóór de ingangsdatum geselecteerd, zoals in de volgende afbeelding wordt weergegeven.

![Rapporteringsstructuurdefinitie op dynamische wijze maken.](./media/dynamically-create-reporting-tree-definitions.png "Rapporteringsstructuurdefinitie op dynamische wijze maken")

## <a name="consolidations-that-involve-eliminations"></a>Consolidaties die betrekking hebben op schrappingen
Schrappingstransacties vormen een veelvoorkomend onderdeel van het consolidatieproces. In dit voorbeeld worden vijf rekeningen tijdens de consolidatie geschrapt: 142600, 211400, 401420, 401180 en 510820. Bedrijven kunnen hun intercompany-rekeningen op een verschillende manier instellen. Een aantal bedrijven stelt bijvoorbeeld het laatste cijfer in op 9 als de rekening wordt gebruikt in intercompany-transacties. Ongeacht de methode kunt u schrappingen in uw geconsolideerde financiële overzichten weergeven als u de intercompany-rekeningen kent.

In de volgende afbeelding ziet u een kolomdefinitie voor een geconsolideerd inkomstenoverzicht. Er zijn drie intercompany-rekeningen voor winst en verlies gedefinieerd voor elk bedrijf met het dimensiefilter. In de kolommen F, G en H staan alleen de schrappingrekeningen voor de bedrijven USMF, USRT en DEMF. Deze kolommen zijn zo ingesteld dat ze **niet** in het financiële overzicht worden afgedrukt.

![Kolomdefinitie voor geconsolideerd inkomstenoverzicht.](./media/column-definition-consolidated-income-statement.png "Kolomdefinitie voor geconsolideerd inkomstenoverzicht")

Wanneer het rapport wordt gegenereerd, worden de schrappingsbedragen berekend in de kolommen F, G en H en worden ze getotaliseerd in kolom I. Kolom J bevat de geconsolideerde bedragen. Met deze consolidatiebedragen worden schrappingen voor de bedrijven USMF, USRT en DEMF uitgesloten.

> [!TIP]
> Maak een tweede rapport dat alleen de schrappingsvermeldingen bevat, en gebruik het in een rapportgroep die uw geconsolideerde rapport bevat. Op deze manier hebt u alle benodigde gegevens voor het maken van alle journaalboekingen die nodig zijn.

In de volgende afbeelding ziet u het geconsolideerde rapport.

![Geconsolideerd rapport voor inkomstenoverzicht.](./media/consolidated-report-income-statement.png "Geconsolideerd rapport voor inkomstenoverzicht")

Of u rekeningen, dimensies of beide gebruikt, met Financiële rapportage kunt u de schrappingsvermeldingen filteren met behulp van de functies voor het filteren van dimensies.

## <a name="minority-interest"></a>Minderheidsbelang
Een bedrijf kan slechts een percentage van een ander bedrijf bezitten. In dit geval is het van belang dat u wanneer u een geconsolideerd rapport produceert, alleen het percentage meeneemt dat het bedrijf eigenaar is. Financiële rapportage heeft op meerdere manieren om minderheidsbelang weer te geven. Dit is afhankelijk van gebruikersvoorkeur. Eén manier is om een totalisatiespercentage te gebruiken in de rapporteringsstructuurdefinitie. Een andere manier is om minderheidsbelang als een aparte regel in een rapport weer te geven.

### <a name="using-the-reporting-tree-definition"></a>De rapporteringsstructuurdefinitie gebruiken
Voer in de rapporteringsstructuurdefinitie het percentage van eigendom in de kolom **Totalisatie %%** (kolom H) in, zoals in de volgende afbeelding. Wanneer het rapport wordt gegenereerd, wordt dit percentage gebruikt om het geconsolideerde bedrag te berekenen. Contoso bezit in dit voorbeeld slechts 80 procent van Contoso Duitsland. U kunt **80** of **0,8** in de kolom **Totalisatie %%** invoeren. Dan wordt 80 procent getotaliseerd naar het geconsolideerde niveau.

> [!NOTE]
> U kunt dit eigendomspercentage toepassen op elke rapporteringseenheid, niet alleen op bedrijfsniveau. 

![Percentage rapporteringsstructuurdefinitie gebruiken.](./media/Using-reporting-tree-definition-percentage.png "Percentage rapporteringsstructuurdefinitie gebruiken")

Wanneer het rapport wordt gegenereerd, bevat het rapport Contoso Duitsland 100 procent van de totale omzet en 80 procent van het bedrag wordt toegewezen en getotaliseerd naar het geconsolideerde niveau voor verkoop.

Als u minder dan 1 procent van een bedrijf in eigendom hebt, kunt u het selectievakje **Totaliseren minder dan 1% toestaan** inschakelen op het tabblad **Aanvullende opties** van de pagina **Rapportinstellingen**, zoals in de volgende afbeelding wordt weergegeven. In dit geval worden de waarden in de kolom **Totalisatie %%** in de rapporteringsstructuur behandeld als minder dan 1 procent. Als u bijvoorbeeld **0,8** invoert, wordt 0,8 procent getotaliseerd naar het geconsolideerde niveau en niet 80 procent. Ook kunt u hetzelfde resultaat bereiken door het selectievakje **Totaliseren minder dan 1%% toestaan** uitgeschakeld te laten en **0,008** in te voeren in de kolom **Totalisatie %%**.

![Opties voor rapportinstellingen.](./media/reporting-setting-options.png "Opties voor rapportinstellingen")

### <a name="showing-ownership-as-a-separate-row-on-the-consolidated-report"></a>Eigendom als een afzonderlijke rij weergeven in het geconsolideerde rapport
Een andere optie voor minderheidsbelang is 100 procent van de dochtermaatschappij weer te geven voor elke regel in het rapport, maar het niet-bepalende belang van de netto-inkomsten af te trekken.

Zoals u in de volgende afbeelding ziet, kunnen een **IF THEN ELSE**-instructie en kolombeperking in de rijdefinitie worden gebruikt om een minderheidsbelang te berekenen in financiële rapporten.

![Eigendom als een afzonderlijke rij weergeven in het geconsolideerde rapport.](./media/Showing-ownership-separate-row-consolidated-report.png "Eigendom als een afzonderlijke rij weergeven in het geconsolideerde rapport")

## <a name="multiple-charts-of-accounts-across-legal-entities"></a>Meerdere rekeningschema's voor rechtspersonen
Verschillende rechtspersonen hebben vaak verschillende rekeningschema's, maar willen wel geconsolideerde financiële overzichten maken. In dit geval kan Financiële rapportage worden gebruikt voor het consolideren van de gegevens, zodat u geconsolideerde financiële rapporten kunt genereren. Hier vindt u de hoofdstappen voor consolidatie wanneer er verschillende rekeningschema's bestaan voor rechtspersonen.

1. Maak een rijdefinitie die meerdere koppelingen naar financiële dimensies heeft. Er moet één koppeling voor elk rekeningschema zijn.
2. Gebruik de rapporteringseenheidbeperking in de kolomdefinitie om elk bedrijf aan de betreffende kolom toe te wijzen.


Meerdere koppelingen naar financiële dimensies kunnen worden toegevoegd aan elke rij in de rijdefinitie voor elk rekeningschema van elk uniek bedrijf. In de volgende afbeelding gebruikt het bedrijf USMF de set rekeningen in de eerste kolom **Koppeling naar financiële dimensies** (kolom J) en gebruikt het bedrijf DEMF de rekeningen in de tweede kolom **Koppeling naar financiële dimensies** (kolom K).

> [!TIP]
> Zie De cel Koppeling naar financiële dimensies specificeren voor meer informatie over de cel **Koppeling naar financiële dimensies specificeren**.

![Set rekeningen eerst koppelen naar financiële dimensies.](./media/set-accounts-first-Link-to-Financial-Dimensions.png "Set rekeningen eerst koppelen naar financiële dimensies")

U kunt een rapporteringsstructuur gebruiken om te definiëren welke koppeling naar financiële dimensies uit de rijdefinitie wordt gebruikt voor elk bedrijf. Selecteer de rijdefinitie in kolom E en selecteer vervolgens de juiste rijkoppeling in kolom F, zoals in de volgende afbeelding wordt weergegeven.

![Koppeling naar financiële dimensies uit gebruikte rijdefinitie.](./media/link-financial-dimensions-row-definition-used.png "Koppeling naar financiële dimensies uit gebruikte rijdefinitie")

> [!TIP]
> Wanneer u koppelingen naar financiële dimensies maakt, gebruikt u de omschrijving ter identificatie van de bedrijven waarop elke koppeling van toepassing is. Op deze manier kunt u gemakkelijker het juiste bedrijf selecteren bij het maken van een rapporteringsstructuur. In de kolomdefinitie kunt u met het veld **Rapporteringseenheid** elke kolom beperken tot een eenheid van de rapporteringsstructuur, zodat u de gegevens naast elkaar kunt weergeven. Als u geen specifiek bedrijf voor een kolom opgeeft, worden geconsolideerde gegevens voor alle bedrijven weergegeven.

## <a name="different-fiscal-calendars-across-multiple-legal-entities"></a>Verschillende fiscale kalenders voor meerdere rechtspersonen
Verschillende rechtspersonen kunnen verschillende fiscale kalenders hebben, maar moeten nog steeds geconsolideerde financiële overzichten maken. Er zijn twee manieren om te consolideren wanneer er verschillende boekperioden voor rechtspersonen bestaan:

- Maak een kolomdefinitie en gebruik de periode en het jaar om de juiste perioden voor elk bedrijf toe te wijzen.
- Geef bij **Instellingen** \> **Overige** \> **Aanvullende opties** aan of u wilt consolideren met behulp van de einddatum van de periode of het periodenummer.

Wanneer u de kolomdefinitie ontwerpt voor meerdere bedrijven met verschillende boekperioden, is het belangrijk dat u overweegt welk bedrijf wordt toegewezen aan het veld **Bedrijfsnaam** in de rapportdefinitie. De fiscale kalender van dat bedrijf wordt gebruikt als de fiscale basiskalender voor de rapportdefinitie. In de volgende tabel ziet u bijvoorbeeld de instelling van de boekperiode die is ingesteld voor de bedrijven USMF en INMF. Voor geconsolideerde rapporten wilt u de fiscale kalender gebruiken die USMF gebruikt. De kolom 'Toewijzen' geeft de equivalente duur en het jaar voor elk bedrijf weer als een rapport wordt gegenereerd voor 30 juni 2018.

| Bedrijf   | Boekjaar                                  | Toewijzing                     |
|-----------|----------------------------------------------|-----------------------------|
| USMF      | Boekjaar van 1 juli tot en met 30 juni          | Periode 12, boekjaar 2018 | 
| INMF      | Kalenderjaar, 1 januari tot en met 31 december | Periode 6, boekjaar 2018  |

In de volgende afbeelding is het bedrijf USMF opgegeven in het veld **Bedrijfsnaam** in de rapportdefinitie. Daarom wordt de fiscale kalender van het bedrijf USMF gebruikt als de fiscale basiskalender. In dit voorbeeld gebruikt het bedrijf USMF wanneer een rapport wordt gegenereerd voor 30 juni 2018, de basisperiode, die is gedefinieerd als periode 12 in de rapportdefinitie. Het bedrijf INMF gebruikt BASE-6 en dit is periode 6. Beide kolommen bevatten gegevens voor juni 2018.

![Basisperiode voor rapport.](./media/report-base-period.png "Basisperiode voor rapport")

In de volgende afbeelding ziet u de opties in de rapportdefinitie waarmee u kunt aangeven of het periodenummer of de einddatum van de periode wordt gebruikt voor de consolidatie.

![Opties voor periodenummer rapportdefinitie.](./media/options-report-definition-period-number.png "Opties voor periodenummer rapportdefinitie")

## <a name="business-unit-consolidations"></a>Bedrijfseenheidsconsolidaties
Dit onderwerp is gericht op het gebruik van rapporteringsstructuurdefinities en organisatiehiërarchieën in Financiële rapportage voor consolidatiedoeleinden. U kunt ook de rapporteringsstructuur gebruiken om de bedrijfseenheidsconsolidatierapporten te maken, zoals rapporten over wereldwijde verkoop of activiteiten. Deze rapporten zijn een algemeen vereiste. Als u de rapporten wilt maken, selecteert u een bedrijf en een dimensie voor elke eenheid waarvoor u een consolidatie wilt uitvoeren. In de volgende afbeelding wordt bijvoorbeeld de bedrijfseenheidstotalisatie uitgevoerd door elk bedrijf in de kolom **Bedrijf** (kolom A) te herhalen en een groep van Afdeling-dimensiewaarden per bedrijf in de kolom **Dimensies** (kolom D) te identificeren.

![Rapporten voor bedrijfseenheidsconsolidatie.](./media/business-unit-consolidation-reports.png "Rapporten voor bedrijfseenheidsconsolidatie")

## <a name="consolidations-that-involve-multiple-reporting-currencies"></a>Consolidaties die betrekking hebben op meerdere rapportagevaluta's
Financiële rapportage biedt meer flexibiliteit wanneer u werkelijke, budget-, budgetbeheer- en budgetplanningsgegevens in meerdere valuta's weergeeft. Als u belangrijke instellingsgegevens invoert, hoeft u geen aanvullende instellingen in Financiële rapportage te maken om een rapport in een willekeurige valuta op elk gewenst moment voor elke gebruiker weer te geven.

### <a name="prerequisites"></a>Vereisten
Om omgerekende saldi correct te berekenen, is voor Financiële rapportage vereist dat de categorie **Rekening ingehouden winsten** wordt toegewezen aan de rekening Ingehouden winsten in de lijst **Hoofdrekening**. In Financiële rapportage wordt boeking naar de rekening Ingehouden winsten niet ondersteund. Als transacties worden geboekt naar de rekening Ingehouden winsten, worden de omgerekende saldi niet juist berekend. Het wordt aangeraden dat gebruikers een aanvullende rekening voor ingehouden winsten instellen om correcties naar de rekening Ingehouden winsten te boeken.

Op de hoofdrekening moeten de velden **Wisselkoerstype voor financiële rapportage** en **Type valutaomrekening** op het sneltabblad **Financiële rapportage** worden ingesteld voor elke rekening, zoals in de volgende afbeelding. U kunt dit per rekening doen of u kunt de rekeningsjablonen gebruiken om eenvoudig wijzigingen door te voeren.

- Selecteer in het veld **Wisselkoerstype voor financiële rapportage** het wisselkoerstype dat de valuta's en wisselkoersen bevat voor toepassing op de rekening. Deze tabel met valuta's en wisselkoersen wordt toegepast op de werkelijke gegevens in Financiële rapportage.
- Selecteer in het veld **Type valutaomrekening** de methode waarmee de wisselkoers voor de rekening wordt berekend. Deze valutamethode wordt gebruikt voor zowel werkelijke als gebudgetteerde gegevens in Financiële rapportage.

![Hoofdrekeningen voor Financiële rapportage.](./media/Financial-reporting-main-accounts.png "Hoofdrekeningen voor Financiële rapportage")

Voor budget-, budgetbeheer- en budgetplanningsgegevens wordt het wisselkoerstype gedefinieerd op de pagina **Grootboek**. Die tabel wordt gebruikt voor het ophalen van de wisselkoersen, en het type valutaomrekening dat is toegewezen aan de rekening, wordt gebruikt.

### <a name="currency-translation-methods"></a>Methoden voor valutaomrekening
Er zijn vier opties voor het berekenen van de wisselkoersen in Financiële rapportage:

- **Gewogen gemiddelde**: deze methode wordt het vaakst gebruikt voor winst- en verliesrekeningen. De volgende formule wordt hierbij gebruikt:

    (Wisselkoers × dagen van kracht) ÷ dagen in periode

- **Gemiddelde**: deze methode is een alternatief voor winst- en verliesrekeningen. De volgende formule wordt hierbij gebruikt:

    Totaal van wisselkoersen ÷ aantal wisselkoersen

- **Huidig**: deze methode wordt het vaakst gebruikt voor balansrekeningen. De wisselkoers die wordt gebruikt, is de koers op of vóór de datum van het rapport of de kolom in Financiële rapportage.
- **Transactiedatum**: deze methode wordt gebruikt voor rekeningen voor vaste activa. De wisselkoers die wordt gebruikt, is de koers op de dag waarop het activum is verworven. Als een koers voor die datum niet is ingevoerd, wordt de vorige koers gebruikt die het dichtst bij de verwervingsdatum van het activum is ingevoerd.

### <a name="report-designer-options-for-currency-translation"></a>Rapportontwerperopties voor valutaomrekening
In Financiële rapportage kunnen rapporten worden weergegeven in een willekeurig aantal aangiftevaluta's. De volgende velden in de rapportdefinitie ondersteunen deze functionaliteit:

- De sectie **Valutagegevens** op de pagina **Rapportdefinitie**. Deze sectie bevat de valuta waarin de waarden worden weergegeven wanneer een rapport wordt gegenereerd.
- Het nieuwe selectievakje **Alle aangiftevaluta´s opnemen**. Wanneer dit selectievakje is ingeschakeld, wordt een rapport voor elke rapportagevaluta naar de rapportenwachtrij toegevoegd nadat het rapport dat gebruikmaakt van de functionele valuta van het bedrijf is gegenereerd. Als het selectievakje is uitgeschakeld, kunt u nog steeds een aangiftevaluta selecteren in Webweergave. In dit geval wordt de aangiftevaluta alleen verwerkt wanneer u deze selecteert.

Met de opties in de rapportdefinitie kunt u eenvoudig een rapport omrekenen in al uw aangiftevaluta's. Daarom kunt u mogelijk dubbele rapportdefinities verwijderen die alleen verschillen in de valuta's die worden gebruikt. Als u een rapport nodig hebt dat meerdere valuta's naast elkaar bevat, kunt u het veld **Valuta weergeven** op de pagina **Kolomdefinitie** blijven gebruiken om alleen die kolom van het rapport naar een alternatieve aangiftevaluta om te zetten.

### <a name="currency-translation-adjustment"></a>Correctie valutaomrekening
De correctie van de valutaomrekening is het verschil tussen de koersen die worden gebruikt voor het berekenen van de balansrekeningen en de koers die wordt gebruikt voor de rekeningen voor inkomstenoverzichten. Dit verschil zorgt ervoor dat de balans uit balans is. U kunt Financiële rapportage op twee manieren gebruiken voor het berekenen van de correctie van de valutaomrekening:

- Gebruik de pagina **Afrondingscorrecties** in de rijdefinitie, zoals in de volgende afbeelding wordt weergegeven.

    ![Afrondingscorrecties voor correctie valutaomrekening.](./media/Currency-translation-adjustment-rounding-adjustments.png "Afrondingscorrecties voor correctie valutaomrekening")

    Wanneer u de rij opgeeft waarin de afrondingscorrectie, de rij voor het totaal aantal activa, de rij voor het totaal aantal passiva en het eigen vermogen en uw gewenste drempel worden weergegeven, wordt met Financiële rapportage het verschil berekend en in de gewenste rij geplaatst. Er wordt een regel met de naam **Afrondingscorrectie** gemaakt en weergegeven bij het inzoomen, zoals in de volgende afbeelding wordt weergegeven.

    ![Inzoomen afrondingscorrectie.](./media/rounding-adjustment-drill-down.png "Inzoomen afrondingscorrectie")

- Plaats alle accounts in een bereik, van activa tot onkosten. Zoals in de volgende afbeelding wordt weergegeven, is het verschil hetzelfde bedrag als de afronding correctie. Daarom kunt u het als een controletotaal gebruiken om ervoor te zorgen dat de afrondingscorrectiepagina geen rekeningsaldi bevat die zijn gemist.

    ![Formuliercontrole afrondingscorrectie.](./media/rounding-adjustment-form-check.png "Formuliercontrole afrondingscorrectie")

### <a name="balance-calculation-approach"></a>Methode van saldoberekening
Om correct omgerekende bedragen te verkrijgen als valuta's worden gebruikt, worden in Financiële de volgende berekeningsmethoden voor de saldi gebruikt:

- **Gewogen gemiddelde en gemiddelde**: elke periode wordt berekend op basis van gewogen gemiddelde en wordt voor kolommen, zoals per kwartaal en jaar tot heden, getotaliseerd.
- **Historisch**: elke rekening waarvoor de historische omrekeningsmethode wordt gebruikt, wordt altijd teruggegaan naar de transactiedatum. Als een verwervingsdatum is gekoppeld aan de transactie, wordt die datum gebruikt bij het ophalen van de wisselkoers. Elke periode wordt vervolgens getotaliseerd en opgeslagen voor een betere berekeningstijd.
- **Huidig**: berekende kolommen en kolommen met totalen, zoals kolommen per kwartaal en jaar tot heden, worden berekend tegen het plaatstarief dat wordt bepaald in de kolom of in het rapport. Bijvoorbeeld: de kolom **Kwartaal 1** gebruikt het tarief van 31 maart als een kalenderjaar wordt gebruikt.

## <a name="additional-resources"></a>Aanvullende resources

Zie het bovenliggende onderwerp van dit onderwerp [Overzicht van Financiële consolidaties en valutaomzetting](./financial-consolidations-currency-translation.md) voor meer informatie over consolidatie en valutaomrekeningen.

Zie voor informatie over het invoeren van details van online consolidaties [Online financiële consolidaties](./consolidate-online.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]