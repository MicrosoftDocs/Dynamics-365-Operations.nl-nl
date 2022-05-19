---
title: Veelgestelde vragen over jaarafsluitingsactiviteiten
description: Dit onderwerp bevat vragen over de jaarafsluiting en antwoorden die kunnen helpen bij de jaarsluitingsactiviteiten.
author: moaamer
ms.date: 12/21/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 19d23c2c5a8fabd6799c6240c25f3ede4064c001
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725591"
---
# <a name="year-end-activities-faq"></a>Veelgestelde vragen over jaarafsluitingsactiviteiten 

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat vragen over de jaarafsluiting en antwoorden die kunnen helpen bij de jaarsluitingsactiviteiten. De informatie in dit onderwerp heeft hoofdzakelijk betrekking op vragen over jaarafsluitingsactiviteiten voor Grootboek en Leveranciers.

## <a name="general-ledger-year-end-enhancements"></a>Verbeteringen bij jaarafsluiting grootboek 
In versie 10.0.20 is een verbetering voor de jaarafsluiting geïntroduceerd, die standaard wordt ingeschakeld vanaf versie 10.0.25. Als uw organisatie een versie gebruikt van vóór 10.0.25, raden we u aan deze functie in te schakelen voordat u met het jaarafsluitingsproces begint. Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen de werkruimte Functiebeheer gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

 - Module: Grootboek
 - Functienaam: Verbeteringen bij jaarafsluiting grootboek

De instellingen voor de sjablonen voor de jaarafsluiting zijn verplaatst naar de nieuwe pagina **Configuratie van de jaarafsluitingssjabloon**. De bestaande jaarafsluitingspagina verandert op een manier die lijkt op de Herwaardering van vreemde valuta voor grootboek, waar bij het uitvoeren of het omkeren van de jaarafsluiting steeds een lijst wordt weergegeven. Een accounting manager kan de jaarafsluiting starten vanaf de nieuwe pagina. 

Als u de jaarafsluiting wilt omkeren, selecteert u het meest recente fiscale jaar voor de betreffende rechtspersoon en kiest u de knop **Jaarafsluiting omkeren**. Met de omkering worden de journaalregels voor de vorige jaarafsluiting verwijderd en wordt de jaarafsluiting niet automatisch opnieuw uitgevoerd. 

U kunt de jaarafsluiting opnieuw starten door het proces voor het fiscale jaar en de rechtspersoon opnieuw te starten. Het proces blijft de instelling van de grootboekparameters gebruiken om te bepalen of bij de nieuwe uitvoering van de jaarafsluiting alleen rekening wordt gehouden met de nieuwe of gewijzigde transacties, of dat de vorige jaarafsluiting volledig wordt omgekeerd, waarbij het proces voor alle transacties opnieuw wordt uitgevoerd.  

## <a name="general-ledger-how-do-i-know-that-were-running-year-end-close-and-not-undoing-year-end-close"></a>Grootboek: Hoe weet ik of we het jaar afsluiten en niet de jaarafsluiting ongedaan maken?
Het komt wel voor dat organisaties een jaarafsluiting juist ongedaan maken terwijl ze de jaarafsluiting proberen uit te voeren. Als de jaarafsluiting heel snel wordt uitgevoerd of er geen openingssaldi worden geproduceerd, valideert u de instelling **Vorige afsluiting ongedaan maken** in **Jaarafsluiting** (**Grootboek > Afgesloten periode > Jaarafsluiting > Jaarafsluiting uitvoeren**). 

[![Jaarafsluiting uitvoeren versus jaarafsluiting ongedaan maken.](./media/faq-2020-yr-end-01.png)](./media/faq-2020-yr-end-01.png)

Als **Vorige afsluiting ongedaan maken** is ingesteld op **Ja**, wordt de vorige jaarafsluiting ongedaan gemaakt. Wanneer een jaarafsluiting ongedaan wordt gemaakt, worden alle eind- en openingssaldi verwijderd, alsof de jaarsluiting nooit is uitgevoerd. De boekstukken worden verwijderd. De jaarafsluiting wordt niet automatisch opnieuw uitgevoerd. U moet het proces opnieuw starten en deze keer **Vorige afsluiting ongedaan maken** instellen op **Nee**. 

> [!NOTE]
> Het eindsaldo kan desgewenst worden gemaakt in het jaar dat wordt afgesloten. Dit gebeurt alleen als de grootboekparameter **Afsluittransacties tijdens overboeking maken** is ingesteld op **Ja**. Het openingssaldo wordt altijd gemaakt omdat dit het beginsaldo voor het volgende jaar is.  
 
## <a name="general-ledger-what-is-the-difference-between-undo-and-delete-gl-parameter-for-year-end-close"></a>Grootboek: Wat is het verschil tussen de parameters Ongedaan maken en Verwijderen voor jaarafsluiting?
Er kan verwarring ontstaan over het verschil tussen de parameter **Vorige afsluiting ongedaan maken**, die zich in het dialoogvenster **Jaarafsluiting** bevindt, en de parameter **Jaareindetransacties verwijderen tijdens overboeking** in Grootboek (**Grootboek > Afgesloten periode > Jaarafsluiting > Jaarafsluiting uitvoeren**).  

[![Verschil tussen de parameters Ongedaan maken en Verwijderen voor jaarafsluiting.](./media/faq-2020-yr-end-02.png)](./media/faq-2020-yr-end-02.png)

Selecteer **Vorige afsluiting ongedaan maken** in het vervolgkeuzemenu in het dialoogvenster terwijl het jaarafsluitingsproces wordt uitgevoerd om alle eind- en openingssaldi te verwijderen alsof de jaarafsluiting nooit is uitgevoerd. De boekstukken worden verwijderd. De jaarafsluiting wordt niet automatisch opnieuw uitgevoerd. Als u de jaarafsluiting wilt uitvoeren, moet u dit proces opnieuw starten, deze keer met **Vorige afsluiting ongedaan maken** ingesteld op **Nee** (**Grootboek > Grootboek instellen > Grootboekparameters**). 

[![De instelling Grootboekparameters.](./media/faq-2020-yr-end-03.png)](./media/faq-2020-yr-end-03.png)

De parameter **Jaareindetransacties verwijderen tijdens overboeking** in Grootboek wordt alleen gebruikt bij het uitvoeren (niet het ongedaan maken) van de jaarafsluiting (**Vorige afsluiting ongedaan maken** is ingesteld op **Nee**). Als deze parameter is ingesteld op **Ja**, worden alle eind- en openingssaldi verwijderd en wordt de jaarafsluiting opnieuw uitgevoerd. Dit proces wordt gebruikt wanneer de organisatie wil dat alle transacties, inclusief correcties sinds de jaarafsluiting, in één journaalregel worden geboekt voor de eind- en openingssaldi. 

Als deze optie is ingesteld op **Nee**, blijven alle eind- en openingssaldi behouden. Ze worden niet verwijderd. In plaats daarvan wordt een nieuw eind- en openingssaldo gemaakt voor de delta- of nieuwe transacties die zijn geboekt sinds de jaarafsluiting voor dat boekjaar.  

> [!NOTE]
> Het eindsaldo wordt gemaakt in het jaar dat wordt afgesloten. Dit gebeurt alleen als de parameter **Afsluittransacties tijdens overboeking maken** in Grootboek is ingesteld op **Ja**. Het openingssaldo wordt altijd gemaakt omdat dit het beginsaldo voor het volgende jaar is. 

## <a name="general-ledger-what-can-be-changed-to-enhance-performance-of-year-end-processing"></a>Grootboek: Wat kan worden gewijzigd om de verwerking van jaarafsluitingen te verbeteren? 
U kunt een aantal wijzigingen aanbrengen om de jaarafsluiting te verbeteren. We raden u aan deze voorgestelde wijzigingen te evalueren om te bepalen of de wijziging geschikt is voor uw organisatie.  

### <a name="dimension-sets"></a>Dimensiesets
Wanneer de jaarafsluiting wordt uitgevoerd, wordt elk dimensiesetsaldo opnieuw opgebouwd, wat direct invloed heeft op de prestaties. Sommige organisaties maken overbodige dimensiesets omdat ze op een bepaald punt zijn gebruikt of misschien in de toekomst worden gebruikt.  Deze overbodige dimensiesets worden tijdens de jaarafsluiting nog steeds opnieuw opgebouwd, waardoor het proces langer duurt. Neem de tijd om uw dimensiesets te beoordelen en eventuele overbodige dimensiesets te verwijderen.

De overbodige dimensiesets zijn ook van invloed op de batchtaak **BudgetDimensionfocusInitializeBalance** (**Grootboek > Rekeningschema > Dimensies > Financiële-dimensiesets**).

[![Financiële-dimensiesets.](./media/faq-2020-yr-end-04.png)](./media/faq-2020-yr-end-04.png)

### <a name="year-end-close-template-configuration"></a>Configuratie van de jaarafsluitingssjabloon
Met de jaarafsluitingssjabloon kunnen de organisaties het financiële-dimensieniveau selecteren dat moet worden aangehouden wanneer winst- en verliessaldi worden overgeboekt naar ingehouden winst. Met de instellingen kan een organisatie de gedetailleerde financiële dimensies (**Alles sluiten**) aanhouden wanneer de saldi worden verplaatst naar ingehouden winst. De organisatie kan er ook voor kiezen de bedragen samen te voegen in één dimensiewaarde (**Eén sluiten**). Dit kan voor elke financiële dimensie worden gedefinieerd. Zie het onderwerp [Jaarafsluiting](year-end-close.md) voor meer informatie over deze instellingen.

Het is raadzaam om de vereisten van uw organisatie te evalueren en, indien mogelijk, zo veel mogelijk dimensies te sluiten met de jaarafsluitingsoptie **Eén sluiten** om de prestaties te verbeteren. Wanneer u afsluit op één dimensiewaarde (wat ook een lege waarde kan zijn), worden er minder details berekend bij het bepalen van de saldi voor journaalregels voor ingehouden winst.

## <a name="degenerate-dimensions"></a>Gedegenereerde dimensies

Een gedegenereerde dimensie kan zelden of nooit alleen of in combinatie met andere dimensies worden hergebruikt. Er zijn twee typen gedegenereerde dimensies. Het eerste type is een losstaande gedegenereerde dimensie. Dit type gedegenereerde dimensie verschijnt meestal in slechts één transactie of in kleine reeksen transacties. Het tweede type is een dimensie die gedegenereerd raakt in combinatie met een of meer aanvullende dimensies die hetzelfde potentieel vertonen op basis van de mogelijke permutaties die kunnen worden gegenereerd. Een gedegenereerde dimensie kan veel invloed hebben op de prestaties van het jaarafsluitingsproces. Als u prestatieproblemen wilt voorkomen, definieert u alle gedegenereerde dimensies als **Eén sluiten** in de instellingen voor de jaarafsluiting die worden beschreven in de voorgaande sectie.

## <a name="general-ledger-what-does-the-period-close-year-end-close-do"></a>Grootboek: Wat gebeurt er met de afgesloten periode bij de jaarafsluiting?
 
[![Afgesloten periode, Jaarafsluiting.](./media/faq-2020-yr-end-05.png)](./media/faq-2020-yr-end-05.png)

### <a name="performance-improvements-for-rebuilding-financial-dimension-sets"></a>Prestatieverbeteringen voor het opnieuw opbouwen van sets met financiële dimensies
Een nieuwe functie die is toegevoegd in versie 10.0.16 verbetert de prestaties van de jaarafsluitings- en consolidatieprocessen. De naam van de functie is Prestatieverbeteringen bij het opnieuw opbouwen van financiële-dimensiesets. Deze functie wijzigt de manier waarop dimensiesets opnieuw worden opgebouwd, zodat ze alleen voor een relevante periode opnieuw worden opgebouwd. In eerdere versies werden dimensiesets opnieuw opgebouwd voor alle datums. Als u het jaar 2020 afsluit, worden bijvoorbeeld alleen de saldi voor transacties in het boekjaar 2020 opnieuw opgebouwd. Als u consolidatie uitvoert voor een datumbereik van 1 tot 30 november 2020, worden de saldi alleen voor dat datumbereik opnieuw opgebouwd.

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen de werkruimte Functiebeheer gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:
 
- Module: Grootboek
- Functienaam: Prestatieverbeteringen bij het opnieuw opbouwen van financiële-dimensiesets

## <a name="accounts-payable-what-changes-have-been-made-to-support-1099-year-end-reporting-for-2021"></a>Leveranciers: Welke wijzigingen zijn aangebracht om de 1099-eindejaarsaangifte voor 2021 te ondersteunen?

In 2021 zijn kleine wijzigingen doorgevoerd in de formulieren DIV, NEC en MISC en zijn enkele extra vakken toegevoegd.

#### <a name="div-new-box2e-2f"></a>DIV: nieuw vak 2e, 2f
 
- Vak 2e. Bevat het gedeelte van het bedrag in vak 1a dat in sectie 897 als winst wordt toegeschreven voor Amerikaanse eigendomsbelangen (USRPI).  
- Vak 2f. Bevat het gedeelte van het bedrag in vak 2a dat in sectie 897 als winst wordt toegeschreven voor USRPI. De vakken 2e en 2f zijn alleen van toepassing op buitenlandse personen en entiteiten waarvan het inkomenstype hetzelfde blijft wanneer dit wordt doorberekend of gedistribueerd aan de directe of indirecte buitenlandse eigenaren of begunstigden. Dit wordt in het algemeen behandeld als daadwerkelijk verbonden met een handel of bedrijf in de Verenigde Staten. Bekijk de instructies voor uw belastingaangifte. 
 
#### <a name="nec-new-box-2"></a>NEC: nieuw vak 2 
 
Als vak 2 is ingeschakeld, moet u consumentenproducten van in totaal USD 5.000 of meer aangeven die aan u zijn verkocht voor wederverkoop op basis van inkoop-verkoop, deposito-provisie of een andere basis. Over het algemeen kunt u alle inkomsten uit de verkoop van deze producten aangeven in schema C (formulier 1040). 
 
De formuliergrootte van NEC is gewijzigd. Tijdens het afdrukken zijn er drie formulieren per pagina. 
 
#### <a name="misc-new-box-11"></a>MISC: nieuw vak 11 
 
In vak 11 wordt het bedrag weergegeven dat is betaald voor de aankoop van vis voor wederverkoop van een persoon die werkzaam is bij een visserijhandel of -bedrijf. Zie de instructies voor uw belastingaangifte voor het rapporteren van dit inkomen. 
 
#### <a name="electronic-filing"></a>Elektronische aangifte 
Zie [Publicatie voor vereisten voor elektronische aangifte](https://www.irs.gov/pub/irs-pdf/p1220.pdf) voor informatie over elektronische aangifte.

Update van indelingsspecificaties en recordindelingen voor elektronische aangifte over 2021 
- Sec. 2 Uitgever "A"-record. 
- Bedragcodes - Verhoogde veldpositie 28-45, lengte tot 18. 
 
#### <a name="sec-2-issuer-a-record-for-reporting-payments-on-form-1099-div"></a>Sec. 2 Uitgever "A"-record, voor aangifte van betalingen op formulier 1099-DIV: 
- Bedragtype – Toegevoegd Sectie 897 Gewone dividenden en toegevoegd Bedragcode H. 
- Bedragtype – Toegevoegd Sectie 897 Vermogenswinst en toegevoegd Bedragcode J. 
 
#### <a name="sec-3-payee-b-record"></a>Sec. 3 Begunstigde "B"-record 
- Algemene informatierecords – Derde opsommingsitem is bijgewerkt van 16 naar 18 velden met betalingsbedragen. 
- Veldtitel betaling H – Veldpositie 247-258, veldtitel, lengte en omschrijving van het algemene veld bijgewerkt. 
- Veldtitel betaling J – Veldpositie 259-270, veldtitel, lengte en omschrijving van het algemene veld bijgewerkt. 
- Leeg veld bijgewerkt naar veldpositie 271-286. 
- Indicator buitenland bijgewerkt naar veldpositie 287. 
- Veldregel met naam van eerste begunstigde bijgewerkt naar veldpositie 288-327. 
- Veldregel met naam van tweede begunstigde bijgewerkt naar veldpositie 328-367. 
- Posities in recordindeling, formulier 1099-MISC – Veldpositie 548 en veldtitel FATCA-indicator aangiftevereiste verwijderd. 
- Recordindelingsposities, formulier 1099-NEC – 545-546 bijgewerkt naar leeg, veld 547 bijgewerkt met indicator voor directe verkoop, lengte en beschrijving en opmerkingen Veld 548-722 bijgewerkt naar leeg. 
 
#### <a name="sec-4-end-of-issuer-c-record"></a>Sec. 4 Einde van uitgever "C"-record 
- Veldtitel betaling H – Veldpositie 304-321, veldtitel, lengte en omschrijving van het algemene veld bijgewerkt. 
- Veldtitel betaling L – Veldpositie 322-339, veldtitel, lengte en omschrijving van het algemene veld bijgewerkt. 
- Veldtitel 340-499 – Lengte bijgewerkt naar 160. 
 
#### <a name="sec-5-state-totals-k-record"></a>Sec. 5 Statustotalen “K”-record 
- Veldtitel betaling H – Veldpositie 304-321, veldtitel, lengte en omschrijving van het algemene veld bijgewerkt. 
- Veldtitel betaling L – Veldpositie 322-339, veldtitel, lengte en omschrijving van het algemene veld bijgewerkt. 
- Veldtitel 340-499 – Lengte bijgewerkt naar 160.  

## <a name="accounts-payable-1099--how-do-i-change-the-1099-box-and-values-for-a-vendor-that-wasnt-tracking-1099-information-throughout-the-year"></a>Leveranciers: 1099 – Hoe wijzig ik het 1099-vak en waarden voor een leverancier die niet het hele jaar 1099-gegevens heeft bijhouden?
Gebruik de functionaliteit voor het bijwerken van 1099-transacties (**Leveranciers > Leveranciers > Alle leveranciers, selecteer een leverancier, ga naar het tabblad Leverancier in het lint en selecteer 1099-formulier bijwerken**) om eerder betaalde factuurtransacties te bekijken en de 1099-gegevens correct opnieuw toe te wijzen volgens de instellingen op het tabblad **1099-belasting** op de pagina **Leverancier**.

## <a name="can-i-run-the-update-1099-for-all-my-vendors-at-once"></a>Kan ik de routine 1099-formulier bijwerken voor al mijn leveranciers tegelijk uitvoeren?
Nee. De routine 1099-formulier bijwerken wordt uitgevoerd voor één leverancier tegelijk. Als deze vereiste nodig is voor uw organisatie, kunt u stemmen voor het idee [Batchproces voor update van 1099-gegevens van leverancier](https://experience.dynamics.com/ideas/idea/?ideaid=5493d608-350e-eb11-b5d9-0003ff68ded8).

## <a name="accounts-payable-1099--recalculate-existing-1099-amounts-versus-update-all-in-the-update-1099-utility"></a>Leveranciers: 1099 – Bestaande 1099-bedragen opnieuw berekenen versus Alles bijwerken in het hulpprogramma 1099-formulier bijwerken
Met het selectievakje **Bestaande 1099-bedragen opnieuw berekenen** wordt het 1099-bedrag weer ingesteld op de totaal betaalde waarden als het wordt gebruikt in combinatie met het selectievakje **Alles bijwerken**. 

[![Transacties met 1099-belasting: voordat de updateroutine wordt uitgevoerd.](./media/faq-2020-yr-end-07.png)](./media/faq-2020-yr-end-07.png)

Het selectievakje **Bestaande 1099-bedragen opnieuw berekenen** speelt pas een rol als de factuur gedeeltelijke 1099-waarden bevat of als de factuur is gewijzigd in het 1099-belastingformulier. Stel dat u een factuur met een waarde van $ 1000,00 hebt, maar de gebruiker handmatig een 1099-bedrag ter waarde van $ 500,00 typt in de factuur.

[![Transacties met 1099-belasting: zowel Alles bijwerken als Bestaande 1099-bedragen opnieuw berekenen selecteren.](./media/faq-2020-yr-end-08.png)](./media/faq-2020-yr-end-08.png)

Wanneer dit bedrag wordt betaald, is $ 500,00 het betaalde 1099-bedrag. Als u de herberekeningsroutine uitvoert, wordt het 1099-bedrag gewijzigd in $ 1000,00, wat het totale betaalde bedrag is.

[![Transacties met 1099-belasting: nadat de 1099-routine is uitgevoerd.](./media/faq-2020-yr-end-09.png)](./media/faq-2020-yr-end-09.png)

## <a name="accounts-payable-1099--manually-create-1099-transactions"></a>Leveranciers: 1099 – Handmatig 1099-transacties maken
Het kan voorkomen dat een organisatie handmatig 1099-transacties moet maken die niet aan een factuur zijn gekoppeld. U kunt handmatig 1099-transacties toevoegen door naar **Leveranciers > Periodieke taken > 1099-belasting > Vereffening van leverancier voor 1099-aangiften** te gaan. Selecteer de knop **Handmatige 1099-transacties**. 

Handmatig gemaakte 1099-transacties worden niet bijgewerkt met het proces **Alles bijwerken** of **Bestaande 1099-bedragen opnieuw berekenen** in het hulpprogramma **1099-formulier bijwerken**.

## <a name="accounts-payable-1099--does-dynamics-365-finance-support-the-1096-form"></a>Leveranciers: 1099 – Ondersteunt Dynamics 365 Finance het 1096-formulier? 

In Dynamics 365 Finance wordt het 1096-formulier voor het jaaroverzicht en de indiening van Amerikaanse gegevens niet afgedrukt.

## <a name="accounts-payable-1099--are-there-any-new-features-that-support-1099-reporting-for-public-sector"></a>Leveranciers: 1099 – Zijn er nieuwe functies die 1099-aangifte voor de openbare sector ondersteunen? 
Voor de openbare sector is de nieuwe functie **1099-gegevens bijwerken per hoofdrekening** toegevoegd. U kunt deze inschakelen in het werkgebied **Functiebeheer**. Met deze functie kunt u de 1099-waarden voor een leverancier koppelen aan de hoofdrekening in de boekhoudingsverdeling in plaats van aan de standaardrekening in de leveranciersrecord.

Zie [Leveranciers voor 1099-aangifte instellen](../localizations/noam-usa-set-up-vndrs-1099-rprtg.md) voor meer informatie.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
