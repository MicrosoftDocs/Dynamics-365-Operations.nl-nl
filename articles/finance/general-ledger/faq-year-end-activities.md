---
title: Veelgestelde vragen over jaarafsluitingsactiviteiten
description: Dit artikel bevat vragen over de jaarafsluiting en antwoorden die kunnen helpen bij de jaarsluitingsactiviteiten.
author: moaamer
ms.date: 12/01/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2e33c1dcbfa4da74f2e8acc6e29f04fda3abd185
ms.sourcegitcommit: 9f3a60a583da21382a14f32ce146fc9ce03f2a09
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/15/2022
ms.locfileid: "9853035"
---
# <a name="year-end-activities-faq"></a>Veelgestelde vragen over jaarafsluitingsactiviteiten 

[!include [banner](../includes/banner.md)]

Dit artikel bevat vragen over de jaarafsluiting en antwoorden die kunnen helpen bij de jaarsluitingsactiviteiten. De informatie in dit artikel heeft hoofdzakelijk betrekking op vragen over jaarafsluitingsactiviteiten voor Grootboek en Leveranciers.

## <a name="general-ledger-year-end-enhancements"></a>Verbeteringen bij jaarafsluiting grootboek

Microsoft Dynamics Met 365 Finance versie 10.0.20 is een verbetering voor de jaarafsluiting geïntroduceerd. Deze verbetering is standaard ingeschakeld vanaf versie 10.0.25 en verplicht vanaf versie 10.0.29. Als uw organisatie een versie gebruikt van vóór 10.0.25, raden we u aan deze functie in te schakelen voordat u met het jaarafsluitingsproces begint. Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen de werkruimte **Functiebeheer** gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** Grootboek
- **Functienaam:** Verbeteringen bij jaarafsluiting grootboek

De instellingen voor de sjablonen voor de jaarafsluiting zijn verplaatst naar de nieuwe pagina **Configuratie van de jaarafsluitingssjabloon**. De bestaande jaarafsluitingspagina wordt vergelijkbaar met de pagina **Herwaardering van vreemde valuta voor grootboek**, waar bij het uitvoeren of het omkeren van de jaarafsluiting steeds een lijst wordt weergegeven. Op de pagina wordt geen historische informatie weergegeven over jaarafsluitingen die uitgevoerd zijn voordat de functie werd ingeschakeld. Een accounting manager kan de jaarafsluiting starten vanaf de nieuwe pagina.

Als u de jaarafsluiting wilt omkeren, selecteert u het meest recente fiscale jaar voor de betreffende rechtspersoon en daarna de knop **Jaarafsluiting omkeren**. Met de omkering worden de journaalregels voor de vorige jaarafsluiting verwijderd en wordt de jaarafsluiting niet automatisch opnieuw uitgevoerd. Als u de functie **Verbeteringen bij jaarafsluiting grootboek** hebt ingeschakeld nadat u het jaar hebt afgesloten en u de historische eindejaarsresultaten wilt omkeren, moet u de historische jaarsluiting opnieuw uitvoeren nadat u de grootboekparameter **Bestaande jaarafsluitingsposten verwijderen bij het opnieuw afsluiten van het jaar** hebt ingeschakeld.

U kunt de jaarafsluiting opnieuw starten door het proces voor het fiscale jaar en de rechtspersoon opnieuw te starten. Het proces blijft de instelling van de grootboekparameters gebruiken om te bepalen of bij de nieuwe uitvoering van de jaarafsluiting alleen rekening wordt gehouden met de nieuwe of gewijzigde transacties, of dat het proces voor alle transacties opnieuw wordt uitgevoerd en de vorige jaarafsluiting volledig wordt omgekeerd.

## <a name="general-ledger-the-general-ledger-year-end-enhancements-feature-is-enabled-why-cant-i-view-my-previous-year-closings-in-the-history-section-of-the-year-end-close-page"></a>Grootboek: de functie Verbeteringen bij jaarafsluiting grootboek is ingeschakeld. Waarom kan ik mijn vorige jaar afsluitingen niet weergeven in de sectie Historie van de pagina Jaarsluiting?

Voordat de functie voor **Verbeteringen bij jaarafsluiting grootboek** ingeschakeld is, worden de datum en tijd bijgehouden waarop het vorige jaarafsluitingsproces is uitgevoerd. Er wordt geen historie bijgehouden voor elke jaarafsluiting. Vandaar dat niet van elke uitgevoerde jaarafsluiting details beschikbaar zijn. Na het inschakelen van de functie worden de procesgegevens van de daaropvolgende jaarafsluiting bijgehouden. Boekstukken van alle jaarafsluitingsprocessen, ook als ze zijn uitgevoerd voordat de functie was ingeschakeld, zijn te zien op de pagina **Boekstuktransacties**. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-cant-be-run-because-one-or-more-ledger-transactions-posted-into-the-fiscal-year-that-you-are-closing-were-settled-to-a-ledger-transaction-in-a-different-fiscal-year-what-does-this-error-mean"></a>Grootboek: het jaarafsluitingsproces kan niet worden uitgevoerd vanwege de volgende fout: 'De jaarafsluiting kan niet worden uitgevoerd omdat een of meer grootboektransacties die zijn geboekt naar het fiscale jaar dat u afsluit, vereffend zijn met een grootboektransactie in een ander fiscaal jaar'. Wat betekent deze fout?

Omdat de functie **Aandacht voor grootboekvereffening en jaarafsluiting** is ingeschakeld, worden alleen vereffende grootboektransacties van het fiscale jaar dat wordt afgesloten, uitgesloten van het openingssaldo. Dit gedrag veroorzaakt dat debet- en credit niet meer in balans zijn. Kijk voor meer informatie in [Bewustzijn tussen grootboekvereffening en jaarafsluiting](awareness-between-ledger-settlement-year-end-close.md).

## <a name="general-ledger-reversal-of-the-year-end-close-process-is-failing-because-of-the-following-error-the-year-end-close-for-112022-cant-be-reversed-because-beginning-balance-transaction-have-been-ledger-settled-in-fiscal-year-112023-what-does-this-error-mean"></a>Grootboek: het jaarafsluitingsproces kan niet worden omgekeerd vanwege de volgende fout: "De jaarafsluiting voor 1/1/2022 kan niet worden omgekeerd omdat het grootboek van openingssaldotransacties is vereffend in fiscaal jaar 1/1/2023." Wat betekent deze fout?

Aangezien de functie **Bewustzijn tussen grootboekvereffening en jaarafsluiting** is ingeschakeld, zijn omkeringen van de jaareindeverwerking niet toegestaan als de openingstransacties in het nieuwe fiscale jaar zijn vereffend. Boek de grootboekvereffening in het nieuwe fiscale jaar 2023 terug voordat u de jaarafsluiting voor 1 januari 2022 terugboekt. Anders sluit u het jaar voor 1 januari 2022 opnieuw af, maar alleen voor nieuwe correctieposten. Als u het jaar alleen opnieuw wilt afsluiten voor correcties, schakelt u de grootboekparameter **Bestaande posten bij jaarafsluiting verwijderen bij het opnieuw afsluiten van het jaar** uit.

## <a name="general-ledger-why-isnt-the-ledger-settlement-automation-processing-decembers-ledger-settlement-transactions"></a>Grootboek: waarom wordt het automatiseringsproces voor grootboekvereffening niet gebruikt voor de verwerking van de grootboekvereffeningstransacties van december?

Met de functie **Grootboekvereffeningen automatiseren** worden transacties die dateren van de eerste dag van het fiscale jaar tot aan de huidige datum automatisch uitgevoerd wanneer het exemplaar draait. Voor boekjaren die eindigen op 31 december moet u mogelijk de uitvoeringsdatum van uw exemplaar aanpassen om ervoor te zorgen dat dit in december wordt uitgevoerd. Automatisering wordt bijvoorbeeld ingesteld om te worden uitgevoerd op de eerste dag van elke maand. Deze automatisering wordt uitgevoerd op 1 december 2022 en volgens planning ook op 1 januari 2023. We raden u aan het exemplaar voor 1 januari 2023 te wijzigen, zodat het op 31 december 2022 wordt uitgevoerd. Door deze wijziging zorgt u ervoor dat de transacties van 2 tot en met 31 december in aanmerking worden genomen voor automatische vereffening.

## <a name="general-ledger-whats-the-difference-between-the-reverse-year-end-close-action-and-the-delete-existing-year-end-entries-when-reclosing-parameter-for-year-end-close"></a>Grootboek: wat is voor de jaarafsluiting het verschil tussen de actie Jaarafsluiting terugdraaien en de parameter Bestaande eindejaarsposten verwijderen bij het opnieuw afsluiten?

Er kan verwarring bestaan over het verschil tussen de actie **Jaarafsluiting terugdraaien** en de parameter **Bestaande eindejaarsposten verwijderen bij het opnieuw afsluiten** in Grootboek (**Grootboek \> Grootboek instellen \> Grootboekparameters**).

Selecteer de actie **Jaarafsluiting terugdraaien** als het jaarafsluitingsproces wordt uitgevoerd om alle eind- en openingssaldi te verwijderen, alsof de jaarafsluiting nooit is uitgevoerd. In dit geval worden de boekstukken verwijderd. De jaarafsluiting wordt niet automatisch opnieuw uitgevoerd. Als u het jaar wilt afsluiten, selecteert u de actie **Jaarafsluiting uitvoeren**.

De parameter **Bestaande posten bij jaarafsluiting verwijderen bij het opnieuw afsluiten van het jaar** in grootboek wordt alleen gebruikt wanneer u de jaarafsluiting uitvoert (niet omkeert). Als de parameter is ingesteld op **Ja**, worden alle eind- en openingssaldi verwijderd en wordt de jaarafsluiting opnieuw uitgevoerd. Deze optie wordt gebruikt wanneer een organisatie wil dat alle transacties, inclusief correcties sinds de jaarafsluiting, in één journaalregel worden geboekt voor de eind- en openingssaldi. Als de parameter is ingesteld op **Nee**, blijven alle eind- en openingssaldi behouden. Ze worden niet verwijderd. In plaats daarvan wordt er alleen een nieuw eind- en openingssaldo gemaakt voor de delta- of nieuwe transacties die zijn geboekt sinds de jaarafsluiting voor dat fiscale jaar.

> [!NOTE]
> Het eindsaldo wordt gemaakt in het jaar dat wordt afgesloten. Dit gebeurt alleen als de parameter **Afsluittransacties tijdens overboeking maken** in Grootboek is ingesteld op **Ja**. Het openingssaldo wordt altijd gemaakt omdat dit het beginsaldo voor het volgende jaar is.

## <a name="general-ledger-what-is-the-difference-between-close-all-and-close-single-options-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process"></a>Grootboek: wat is het verschil tussen de opties 'Alles sluiten' en 'Eén sluiten' in de sectie Verlies- en winstdimensies overboeken van het jaarafsluitingsproces?

Met **Alles sluiten** worden de oorspronkelijke waarden voor financiële dimensies van geboekte transacties behouden en gebruikt voor het maken van de beginsaldi voor de rekening ingehouden winsten. Afzonderlijke beginsaldi voor ingehouden winsten worden gemaakt voor elke unieke combinatie van waarden voor financiële dimensies. Als **Eén sluiten** is geselecteerd, worden alle geboekte transacties die deze financiële dimensie hebben, samengevat in een beginsaldo voor ingehouden winsten voor de dimensiewaarde die is ingevoerd in het veld dat wordt weergegeven na **Eén sluiten**. 

Stel bijvoorbeeld dat alle transacties voor het fiscale jaar zijn geboekt met de rekeningstructuur Hoofdrekening - afdeling. Voor de financiële dimensie Afdeling in de sjabloon is **Eén sluiten geselecteerd** en is 100 ingevoerd als dimensiewaarde. Als de totale inkomsten van alle transacties die zijn geboekt naar afdelingen 200, 300 en 400 $100.000 zijn, wordt één beginsaldo gemaakt voor Ingehouden winsten - 100. Als u **Eén sluiten** selecteert, maar de waarde voor de financiële dimensie leeg laat, worden alle transacties geboekt naar ingehouden winsten en is de dimensiewaarde leeg.

## <a name="general-ledger-when-i-select-close-single-option-on-the-transfer-profit-and-loss-dimension-section-of-the-year-end-close-process-will-my-detailed-transactional-information-be-lost"></a>Grootboek: gaan mijn gedetailleerde transactiegegevens verloren wanneer ik de optie "Eén sluiten" selecteer in de sectie Verlies- en winstdimensies overboeken van het jaarafsluitingsproces?

Met opties **Alles sluiten** en **Eén sluiten** kunt u opgeven welke financiële dimensies van transacties die zijn geboekt naar verlies-en-winstrekeningen, worden overgeboekt naar de hoofdrekening voor ingehouden winst. De historische, gedetailleerde boeking naar de verlies-en-winstrekeningen wordt niet beïnvloed en blijft een detail. Deze optie is van invloed op het detailniveau dat wordt overgeboekt naar de ingehouden winstrekeningen als openingssaldo in het nieuwe jaar. 

## <a name="general-ledger-the-year-end-close-process-is-failing-because-the-reporting-currency-for-the-year-does-not-balance-what-does-this-mean"></a>Grootboek: het jaarafsluitingsproces mislukt omdat de aangiftevaluta voor het jaar niet in balans is. Wat betekent dit?

Deze fout kan optreden nadat u de functie **Bewustzijn tussen grootboekvereffening en jaarafsluiting** hebt ingeschakeld (de functie Bewustzijn). Wanneer de functie is ingeschakeld, worden grootboektransacties die zijn vereffend, niet meer opgenomen in het openingssaldo van het volgende fiscale jaar wanneer u het grootboekjaar afsluit. Als grootboektransacties worden uitgesloten die worden vereffend, kan dit een nieuwe waarde zijn voor klanten aan het einde van het jaar als het grootboek is gedefinieerd met een aangiftevaluta.   
Grootboekvereffening wordt alleen voor de valuta voor boekhouding uitgevoerd.  Wanneer de grootboektransacties worden vereffend, zorgt validatie er alleen voor dat de debettransacties in valuta voor boekhouding gelijk zijn aan de creditrekeningvaluta. De aangiftevalutabedragen voor die grootboektransacties worden niet gevalideerd en hebben mogelijk geen debet = credit.  Bovendien wordt bij een grootboekvereffening niet automatisch een winst/verlies berekend en in de aangiftevaluta overboekt.  Vanwege deze beperkingen moet er een winst-/verliestransactie bestaan in de aangiftevaluta bij het uitvoeren van een grootboekvereffening.  Als de winst/verliesrekening niet is opgenomen in de grootboekvereffening, leidt de jaarafsluiting tot een bericht dat het uit balans is.  Lees voor meer informatie [Bewustzijn tussen de functie grootboekvereffening en de aangiftevaluta is niet in balans](reporting-currency-yec.md).

## <a name="general-ledger-what-can-be-changed-to-help-enhance-the-performance-of-year-end-processing"></a>Grootboek: wat kan worden gewijzigd om de verwerking van jaarafsluitingen te verbeteren?

U kunt een diverse wijzigingen aanbrengen om de jaarafsluiting te verbeteren. We raden u aan deze voorgestelde wijzigingen te evalueren om te bepalen of ze geschikt zijn voor uw organisatie.

### <a name="optimize-year-end-close-service"></a>Service jaarafsluiting optimaliseren

Met de service **Jaarafsluiting optimaliseren** kunnen gebruikers van Microsoft Dynamics 365 Finance hun jaarafsluiting versnellen door de zware jaarafsluitingsprocessen over te dragen aan een microservice. Dankzij de tijd die u bespaart met een efficiënte jaarafsluiting kan elk financieel team tijdig te reageren op vereiste correcties, zodat de financiële rapporten worden opgemaakt. Door de jaarafsluiting door een microservice te laten uitvoeren, komen waardevolle resources vrij. De verbeterde verwerking legt minder druk op de SQL-server en geeft klanten de kans de verwerking van jaarafsluitingen te versnellen.

De service **Jaarafsluiting optimaliseren** is beschikbaar in versie 10.0.31, zodat meer klanten de nieuwe service kunnen gebruiken voor de afsluiting van het seizoen 2022. Daarnaast is de service gebackport naar versies 10.0.30 en 10.0.29. Lees voor meer informatie [Jaarafsluiting optimaliseren](optimize-year-end-close.md).

### <a name="dimension-sets"></a>Dimensiesets

Wanneer u het de jaarafsluiting uitvoert, wordt elk dimensiesetsaldo opnieuw opgebouwd. Dit gedrag heeft direct invloed op de prestaties. Sommige organisaties maken overbodige dimensiesets omdat ze op een bepaald punt zijn gebruikt of misschien in de toekomst worden gebruikt. Deze overbodige dimensiesets worden tijdens de jaarafsluiting nog steeds opnieuw opgebouwd, waardoor het proces langer duurt. Neem de tijd om uw dimensiesets te beoordelen en overbodige dimensiesets te verwijderen.

De overbodige dimensiesets zijn ook van invloed op de batchtaak **BudgetDimensionfocusInitializeBalance** (**Grootboek \> Rekeningschema \> Dimensies \> Financiële-dimensiesets**).

[![Financiële-dimensiesets.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Configuratie van de jaarafsluitingssjabloon

Met de jaarafsluitingssjabloon kunnen de organisaties het financiële-dimensieniveau selecteren dat moet worden aangehouden wanneer winst- en verliessaldi worden overgeboekt naar ingehouden winst. Met de instellingen kan een organisatie de gedetailleerde financiële dimensies (**Alles sluiten**) aanhouden wanneer de saldi worden verplaatst naar ingehouden winst. De organisatie kan er ook voor kiezen de bedragen samen te voegen in één dimensiewaarde (**Eén sluiten**). Dit kan voor elke financiële dimensie worden gedefinieerd. Zie het artikel [Jaarafsluiting](year-end-close.md) voor meer informatie over deze instellingen.

Het is raadzaam om de vereisten van uw organisatie te evalueren en, indien mogelijk, zo veel mogelijk dimensies te sluiten met de jaarafsluitingsoptie **Eén sluiten** om de prestaties te verbeteren. Wanneer u afsluit op één dimensiewaarde (wat ook een lege waarde kan zijn), worden er minder details berekend bij het bepalen van de saldi voor journaalregels voor ingehouden winst.

### <a name="degenerate-dimensions"></a>Gedegenereerde dimensies

Een gedegenereerde dimensie kan zelden of nooit alleen of in combinatie met andere dimensies worden hergebruikt. Er zijn twee typen gedegenereerde dimensies. Het eerste type is een losstaande gedegenereerde dimensie. Dit type gedegenereerde dimensie verschijnt meestal in slechts één transactie of in kleine reeksen transacties. Het tweede type is een dimensie die gedegenereerd raakt in combinatie met een of meer aanvullende dimensies die hetzelfde potentieel vertonen op basis van de mogelijke permutaties die kunnen worden gegenereerd. Een gedegenereerde dimensie kan veel invloed hebben op de prestaties van het jaarafsluitingsproces. Als u prestatieproblemen wilt voorkomen, definieert u alle gedegenereerde dimensies als **Eén sluiten** in de instellingen voor de jaarafsluiting die worden beschreven in de voorgaande sectie.

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2022"></a>Leveranciers: Welke wijzigingen zijn aangebracht om de 1099-eindejaarsaangifte voor 2022 te ondersteunen?

#### <a name="update-to-all-1099-forms"></a>Bijwerken naar alle 1099-formulieren

In alle 1099-formulieren voor het belastingjaar 2022 zijn de volgende wijzigingen aangebracht:

- In 2021 was het jaar vast ingesteld op 1099-formulieren. Vanaf 2022 wordt het jaar ingevuld door het rapport.

#### <a name="1099-misc"></a>1099-MISC

Op formulier 1099-MISC voor het belastingjaar 2022 zijn de volgende updates doorgevoerd:

- Box 13: geeft nu de aanvraagvereiste van de Foreign Account Tax Compliance Act (FATCA) aan.
- Vak 14: nu gebruikt om de betaling van overtollige gouden handdrukken te melden.
- Vak 15: wordt nu gebruikt om de betaling te rapporteren onder niet-gekwalificeerde compensatieplannen (NQDC).
- Vak 16: nu gebruikt om aangifte te doen van ingehouden belasting voor de staat.
- Vak 17: nu gebruikt om het staatsnummer van de betaler aan te geven.
- Vak 18: nu gebruikt om aangifte te doen van de staatsinkomsten.

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Leveranciers: 1099 – Hoe wijzig ik het 1099-vak en waarden voor een leverancier die niet het hele jaar 1099-gegevens heeft bijgehouden?

Gebruik de functie **1099 bijwerken** om eerder betaalde factuurtransacties door te nemen en de 1099-gegevens op de juiste manier opnieuw toe te wijzen op basis van de instellingen op het tabblad **1099-belasting** van de pagina **Leverancier**. Als u de functie **1099 bijwerken** wilt gebruiken, gaat u naar **Leveranciers \> Leverancier \> Alle leveranciers**, selecteert u een leverancier en dan in het actievenster, op het tabblad **Leverancier**, kiest u **1099 bijwerken**.

## <a name="can-i-run-the-update-1099-functionality-for-all-my-vendors-at-once"></a>Kan ik de functionaliteit 1099 bijwerken voor al mijn leveranciers tegelijk uitvoeren?

U kunt de pagina **1099-gegevens voor meerdere leveranciers bijwerken** gebruiken om het 1099-vak op een leveranciersrecord bij te werken en om transacties bij te werken met de informatie uit het 1099-vak. Ga naar **Leveranciers \> Periodieke taak \> 1099-belasting** om deze pagina te openen. Als u de pagina wilt openen, moet de beveiligingsbevoegdheid **1099-vak en transacties voor meerdere leveranciers bijwerken** aan u toegewezen zijn.

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Leveranciers: 1099 – Bestaande 1099-bedragen opnieuw berekenen versus Alles bijwerken in het hulpprogramma 1099-formulier bijwerken

Met het selectievakje **Bestaande 1099-bedragen opnieuw berekenen** wordt het 1099-bedrag weer ingesteld op de totaal betaalde waarden als het wordt gebruikt in combinatie met het selectievakje **Alles bijwerken**.

[![Transacties met 1099-belasting: voordat de updateroutine wordt uitgevoerd.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Het selectievakje **Bestaande 1099-bedragen opnieuw berekenen** speelt pas een rol als de factuur gedeeltelijke 1099-waarden bevat of als de factuur is gewijzigd in het 1099-belastingformulier. Stel dat u een factuur met een waarde van $ 1000,00 hebt, maar de gebruiker handmatig een 1099-bedrag ter waarde van $ 500,00 op de factuur invult.

[![Transacties met 1099-belasting: zowel Alles bijwerken als Bestaande 1099-bedragen opnieuw berekenen selecteren.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Wanneer deze factuur wordt betaald, is $ 500,00 het betaalde 1099-bedrag. Als u de herberekeningsroutine uitvoert, wordt het 1099-bedrag gewijzigd in $ 1000,00, het totale betaalde bedrag.

[![Transacties met 1099-belasting: nadat de 1099-routine is uitgevoerd.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Leveranciers: 1099 – Handmatig 1099-transacties maken

Het kan voorkomen dat een organisatie handmatig 1099-transacties moet maken die niet aan een factuur zijn gekoppeld. U kunt handmatig 1099-transacties toevoegen door naar **Leveranciers \> Periodieke taken \> 1099-belasting \> Vereffening van leverancier voor 1099-aangiften** te gaan. Selecteer de knop **Handmatige 1099-transacties**.

Handmatig gemaakte 1099-transacties worden niet bijgewerkt met het proces **Alles bijwerken** of **Bestaande 1099-bedragen opnieuw berekenen** in het hulpprogramma **1099 bijwerken**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Leveranciers: 1099 – Ondersteunt Dynamics 365 Finance het 1096-formulier?

In Dynamics 365 Finance wordt het 1096-formulier voor het jaaroverzicht en de indiening van Amerikaanse gegevens niet afgedrukt.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Leveranciers: 1099 – Zijn er nieuwe functies die 1099-aangifte voor de openbare sector ondersteunen?

Voor de openbare sector is de nieuwe functie **1099-gegevens bijwerken per hoofdrekening** toegevoegd. U kunt deze inschakelen in het werkgebied **Functiebeheer**. Met deze functie kunt u de 1099-waarden voor een leverancier koppelen aan de hoofdrekening in de boekhoudingsverdeling in plaats van aan de standaardrekening in de leveranciersrecord.

Zie [Leveranciers voor 1099-aangifte instellen](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md) voor meer informatie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
