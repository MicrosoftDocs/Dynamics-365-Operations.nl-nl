---
title: Veelgestelde vragen over jaarafsluitingsactiviteiten
description: Dit onderwerp is samengesteld om u te helpen met uw jaarafsluitingsactiviteiten.
author: kweekley
ms.date: 01/25/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 379bb8a1f969a74618db0e57c84c2038db1b631c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822826"
---
# <a name="year-end-activities-faq"></a>Veelgestelde vragen over jaarafsluitingsactiviteiten 

[!include [banner](../includes/banner.md)]

Dit onderwerp is samengesteld om u te helpen met uw jaarafsluitingsactiviteiten. De informatie in dit onderwerp is hoofdzakelijk gericht op vragen over jaarafsluitingsactiviteiten voor Grootboek en Leveranciers.

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Grootboek: Hoe weet ik of we het jaar afsluiten en niet de jaarafsluiting ongedaan maken?
Het komt wel voor dat organisaties een jaarafsluiting juist ongedaan maken terwijl ze de jaarafsluiting proberen uit te voeren. Als de jaarafsluiting heel snel wordt uitgevoerd of er geen openingssaldi worden geproduceerd, valideert u de instelling **Vorige afsluiting ongedaan maken** in **Jaarafsluiting** (**Grootboek > Afgesloten periode > Jaarafsluiting > Jaarafsluiting uitvoeren**). 

[![Jaarafsluiting uitvoeren versus jaarafsluiting ongedaan maken](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Als **Vorige afsluiting ongedaan maken** is ingesteld op **Ja**, wordt de vorige jaarafsluiting ongedaan gemaakt. Wanneer een jaarafsluiting ongedaan wordt gemaakt, worden alle eind- en openingssaldi verwijderd, alsof de jaarsluiting nooit is uitgevoerd. De boekstukken worden verwijderd. De jaarafsluiting wordt niet automatisch opnieuw uitgevoerd. U moet het proces opnieuw starten en deze keer **Vorige afsluiting ongedaan maken** instellen op **Nee**. 

> [!NOTE]
> Het eindsaldo kan desgewenst worden gemaakt in het jaar dat wordt afgesloten. Dit gebeurt alleen als de grootboekparameter **Afsluittransacties tijdens overboeking maken** is ingesteld op **Ja**. Het openingssaldo wordt altijd gemaakt omdat dit het beginsaldo voor het volgende jaar is.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Grootboek: Wat is het verschil tussen de parameters Ongedaan maken en Verwijderen voor jaarafsluiting?
Er kan verwarring ontstaan over het verschil tussen de parameter **Vorige afsluiting ongedaan maken**, die zich in het dialoogvenster **Jaarafsluiting** bevindt, en de parameter **Jaareindetransacties verwijderen tijdens overboeking** in Grootboek (**Grootboek > Afgesloten periode > Jaarafsluiting > Jaarafsluiting uitvoeren**).  

[![Verschil tussen de parameters Ongedaan maken en Verwijderen voor jaarafsluiting](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Selecteer **Vorige afsluiting ongedaan maken** in het vervolgkeuzemenu in het dialoogvenster terwijl het jaarafsluitingsproces wordt uitgevoerd om alle eind- en openingssaldi te verwijderen alsof de jaarafsluiting nooit is uitgevoerd. De boekstukken worden verwijderd. De jaarafsluiting wordt niet automatisch opnieuw uitgevoerd. Als u de jaarafsluiting wilt uitvoeren, moet u dit proces opnieuw starten, deze keer met **Vorige afsluiting ongedaan maken** ingesteld op **Nee** (**Grootboek > Grootboek instellen > Grootboekparameters**). 

[![De instelling Grootboekparameters](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

De parameter **Jaareindetransacties verwijderen tijdens overboeking** in Grootboek wordt alleen gebruikt bij het uitvoeren (niet het ongedaan maken) van de jaarafsluiting (**Vorige afsluiting ongedaan maken** is ingesteld op **Nee**). Als deze parameter is ingesteld op **Ja**, worden alle eind- en openingssaldi verwijderd en wordt de jaarafsluiting opnieuw uitgevoerd. Dit proces wordt gebruikt wanneer de organisatie wil dat alle transacties, inclusief correcties sinds de jaarafsluiting, in één journaalregel worden geboekt voor de eind- en openingssaldi. 

Als deze optie is ingesteld op **Nee**, blijven alle eind- en openingssaldi behouden. Ze worden niet verwijderd. In plaats daarvan wordt een nieuw eind- en openingssaldo gemaakt voor de delta- of nieuwe transacties die zijn geboekt sinds de jaarafsluiting voor dat boekjaar.  

> [!NOTE]
> Het eindsaldo wordt gemaakt in het jaar dat wordt afgesloten. Dit gebeurt alleen als de parameter **Afsluittransacties tijdens overboeking maken** in Grootboek is ingesteld op **Ja**. Het openingssaldo wordt altijd gemaakt omdat dit het beginsaldo voor het volgende jaar is. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Grootboek: Wat kan worden gewijzigd om de verwerking van jaarafsluitingen te verbeteren? 
U kunt een aantal wijzigingen aanbrengen om de jaarafsluiting te verbeteren. We raden u aan deze voorgestelde wijzigingen te evalueren om te bepalen of de wijziging geschikt is voor uw organisatie.  

### <a name="dimension-sets"></a>Dimensiesets
Wanneer de jaarafsluiting wordt uitgevoerd, wordt elk dimensiesetsaldo opnieuw opgebouwd, wat direct invloed heeft op de prestaties. Sommige organisaties maken overbodige dimensiesets omdat ze op een bepaald punt zijn gebruikt of misschien in de toekomst worden gebruikt.  Deze overbodige dimensiesets worden tijdens de jaarafsluiting nog steeds opnieuw opgebouwd, waardoor het proces langer duurt. Neem de tijd om uw dimensiesets te beoordelen en eventuele overbodige dimensiesets te verwijderen.

De overbodige dimensiesets zijn ook van invloed op de batchtaak **BudgetDimensionfocusInitializeBalance** (**Grootboek > Rekeningschema > Dimensies > Financiële-dimensiesets**).

[![Financiële-dimensiesets](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Configuratie van jaarafsluitingssjabloon
Met de jaarafsluitingssjabloon kunnen de organisaties het financiële-dimensieniveau selecteren dat moet worden aangehouden wanneer winst- en verliessaldi worden overgeboekt naar ingehouden winst. Met de instellingen kan een organisatie de gedetailleerde financiële dimensies (**Alles sluiten**) aanhouden wanneer de saldi worden verplaatst naar ingehouden winst. De organisatie kan er ook voor kiezen de bedragen samen te voegen in één dimensiewaarde (**Eén sluiten**). Dit kan voor elke financiële dimensie worden gedefinieerd. Zie het onderwerp [Jaarafsluiting](year-end-close.md) voor meer informatie over deze instellingen.

Het is raadzaam om de vereisten van uw organisatie te evalueren en, indien mogelijk, zo veel mogelijk dimensies te sluiten met de jaarafsluitingsoptie **Eén sluiten** om de prestaties te verbeteren. Wanneer u afsluit op één dimensiewaarde (wat ook een lege waarde kan zijn), worden er minder details berekend bij het bepalen van de saldi voor journaalregels voor ingehouden winst.

### <a name="10013-update-or-later"></a>10.0.13-update of hoger
Als u hebt bijgewerkt naar versie 10.0.13 of hoger sinds de laatste keer dat uw organisatie een jaarafsluiting heeft uitgevoerd, kan het jaarafsluitingsproces langer duren vanwege de [implementatie van de HashV2-functie](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/verify-hash-function-changes-after-update-to-dynamics-365-finance-2020-release-wave-2). (De term *hash* verwijst naar een veld dat wordt berekend op basis van andere tekenreeksvelden. De API voor het berekenen van de GUID-waarde voor hash is bijgewerkt om de beveiliging te verbeteren.) Om het jaarafsluitingsproces te versnellen, kunt u het beste de saldi van de dimensiesets opnieuw opbouwen voordat u de jaarafsluiting uitvoert. Als u de dimensiesetsaldi al opnieuw hebt opgebouwd nadat u de 10.0.13-update hebt uitgevoerd, hoeft u het proces niet opnieuw uit te voeren.
 
## <a name="general-ledger--what-does-the-period-close--year-end-close-do"></a>Grootboek: Wat gebeurt er met Afgesloten periode - Jaarafsluiting?
 
[![Afgesloten periode, Jaarafsluiting](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets-new-feature"></a>Prestatieverbeteringen bij het opnieuw opbouwen van financiële-dimensiesets (nieuwe functie)
Een nieuwe functie die is toegevoegd in versie 10.0.16 verbetert de prestaties van de jaarafsluitings- en consolidatieprocessen. De naam van de functie is Prestatieverbeteringen bij het opnieuw opbouwen van financiële-dimensiesets. Deze functie wijzigt de manier waarop dimensiesets opnieuw worden opgebouwd, zodat ze alleen voor een relevante periode opnieuw worden opgebouwd. In eerdere versies werden dimensiesets opnieuw opgebouwd voor alle datums. Als u het jaar 2020 afsluit, worden bijvoorbeeld alleen de saldi voor transacties in het boekjaar 2020 opnieuw opgebouwd. Als u consolidatie uitvoert voor een datumbereik van 1 tot 30 november 2020, worden de saldi alleen voor dat datumbereik opnieuw opgebouwd.

Aangezien deze functie wordt beschouwd als een wijziging die fouten veroorzaakt, moet u deze inschakelen via de werkruimte **Functiebeheer**.
 
[![Jaarafsluiting](./media/faq-2020-yr-end-06.png)](./media/faq-2020-yr-end-06.png)

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2020"></a>Leveranciers: Welke wijzigingen zijn aangebracht om 1099-eindejaarsaangifte voor 2020 te ondersteunen?

Er zijn twee nieuwe wettelijk voorgeschreven functies toegevoegd voor 1099-eindejaarswijzigingen in 2020. De eerste functie, **Wijzigingen toepassen op de formulieren 1099-NEC en 1099-MISC voor 2020**, is halverwege het jaar vrijgegeven als verplichte functie. Hiermee moet ervoor worden gezorgd dat 1099-transactiegegevens voor het jaar 2020 kunnen worden bijgehouden voor het nieuwe 1099-NEC-formulier. Met deze functie zijn de 1099-velden toegevoegd die nodig zijn om de nieuwe 1099-NEC-velden te ondersteunen en zijn de 1099-MISC-velden bijgewerkt. In deze update zijn ook gegevens van leveranciersrecords bijgewerkt voor de 1099-vakgegevens. 

De tweede wettelijk voorgeschreven functie, **1099-overzichten bijgewerkt voor belastingwetgeving van 2020**, omvat de volgende wijzigingen.

- 1099-OID: het formulier is door de belastingdienst (IRS) omgezet voor continu gebruik.
   - Het derde en vierde cijfer van het aangiftejaar moeten worden ingevuld wanneer het wordt afgedrukt. Gebruik het derde en vierde cijfer uit het veld **Aangiftejaar** onder **Afdrukopties 1099-belasting**. 

- 1099-NEC: een nieuw formulier voor 2020. Hierin wordt compensatie voor niet-werknemers vastgelegd. 

-   1099-MISC: vanwege het nieuwe formulier heeft de belastingdienst (IRS) formulier 1099-MISC gereviseerd en de vaknummers opnieuw gerangschikt voor het aangeven van bepaalde inkomsten.
Wijzigingen in de aangifte van inkomsten en de vaknummers van het formulier worden hieronder vermeld.
   - De betaler heeft via directe verkoop minstens $ 5000 verdiend (selectievakje) in vak 7.
   - Opbrengsten uit oogstverzekering worden aangegeven in vak 9.
   - Bruto-opbrengsten voor een advocaat worden aangegeven in vak 10.
   - Uitgestelde posten volgens sectie 409A worden aangegeven in vak 12.
   - Inkomsten uit niet-gekwalificeerde compensatie worden in vak 14 aangegeven.
   - In de vakken 15, 16 en 17 worden respectievelijk de ingehouden staatsbelasting, het staatidentificatienummer en het bedrag aan verdiende inkomsten in de staat vermeld.

- Geen wijzigingen in 1099-DIV of 1099-INT in 2020.

- Elektronische aangifte: de indeling is gewijzigd voor het nieuwe ERW-formulier en de bovenstaande wijzigingen in de MISC-vakken. Zie [IRS-publicatie 1220](https://www.irs.gov/pub/irs-pdf/p1220.pdf) voor specifieke informatie over vereisten voor elektronische aangifte.

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Leveranciers: 1099 – Hoe wijzig ik het 1099-vak en waarden voor een leverancier die niet het hele jaar 1099-gegevens heeft bijhouden?
Gebruik de functionaliteit voor het bijwerken van 1099-transacties (**Leveranciers > Leveranciers > Alle leveranciers, selecteer een leverancier, ga naar het tabblad Leverancier in het lint en selecteer 1099-formulier bijwerken**) om eerder betaalde factuurtransacties te bekijken en de 1099-gegevens correct opnieuw toe te wijzen volgens de instellingen op het tabblad **1099-belasting** op de pagina **Leverancier**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Kan ik de routine 1099-formulier bijwerken voor al mijn leveranciers tegelijk uitvoeren?
Nee. De routine 1099-formulier bijwerken wordt uitgevoerd voor één leverancier tegelijk. Als deze vereiste nodig is voor uw organisatie, kunt u stemmen voor het idee [Batchproces voor update van 1099-gegevens van leverancier](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-vs-update-all-in-the-update-1099-utility"></a>Leveranciers: 1099 – Bestaande 1099-bedragen opnieuw berekenen versus Alles bijwerken in het hulpprogramma 1099-formulier bijwerken.
Met het selectievakje **Bestaande 1099-bedragen opnieuw berekenen** wordt het 1099-bedrag weer ingesteld op de totaal betaalde waarden indien gebruikt in combinatie met het selectievakje **Alles bijwerken**. 

[![Transacties met 1099-belasting: voordat de updateroutine wordt uitgevoerd](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Het selectievakje **Bestaande 1099-bedragen opnieuw berekenen** speelt pas een rol als de factuur gedeeltelijke 1099-waarden bevat of als de factuur is gewijzigd in het 1099-belastingformulier. Stel dat u een factuur met een waarde van $ 1000,00 hebt, maar de gebruiker handmatig een 1099-bedrag ter waarde van $ 500,00 typt in de factuur.

[![Transacties met 1099-belasting: zowel Alles bijwerken als Bestaande 1099-bedragen opnieuw berekenen selecteren](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Wanneer dit bedrag wordt betaald, is $ 500,00 het betaalde 1099-bedrag. Als u de herberekeningsroutine voert, wordt het 1099-bedrag gewijzigd in $ 1000,00, het totale betaalde bedrag.

[![Transacties met 1099-belasting: nadat de 1099-routine is uitgevoerd](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Leveranciers: 1099 – Handmatig 1099-transacties maken
Het kan voorkomen dat een organisatie handmatig 1099-transacties moet maken die niet aan een factuur zijn gekoppeld. U kunt handmatig 1099-transacties toevoegen door naar **Leveranciers > Periodieke taken > 1099-belasting > Vereffening van leverancier voor 1099-aangiften** te gaan. Selecteer de knop **Handmatige 1099-transacties**. 

Handmatig gemaakte 1099-transacties worden niet bijgewerkt met het proces **Alles bijwerken** of **Bestaande 1099-bedragen opnieuw berekenen** in het hulpprogramma **1099-formulier bijwerken**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Leveranciers: 1099 – Ondersteunt Dynamics 365 Finance het 1096-formulier? 

In Dynamics 365 Finance wordt het 1096-formulier voor het jaaroverzicht en de indiening van Amerikaanse gegevens niet afgedrukt.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Leveranciers: 1099 – Zijn er nieuwe functies die 1099-aangifte voor de openbare sector ondersteunen? 
Voor de openbare sector is de nieuwe functie **1099-gegevens bijwerken per hoofdrekening** toegevoegd. U kunt deze inschakelen in de werkruimte **Functiebeheer**. Met deze functie kunt u de 1099-waarden voor een leverancier koppelen aan de hoofdrekening in de boekhoudingsverdeling in plaats van aan de standaardrekening in de leveranciersrecord.

Zie [Leveranciers voor 1099-aangifte instellen](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md) voor meer informatie.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
