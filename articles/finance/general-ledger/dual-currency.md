---
title: Dubbele valuta
description: Dit onderwerp biedt informatie over dubbele valuta, waar de aangiftevaluta wordt gebruikt als een tweede valuta voor boekhouding voor Microsoft Dynamics 365 Finance.
author: kweekley
manager: AnnBe
ms.date: 04/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, Ledger, AssetTransReportingCurrencyAmountsWizard,BankAccountTransReportingCurrencyAmountsWizard, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: ''
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 8b71b571b03e8fa2648c90258bbcaa020baeabc0
ms.sourcegitcommit: 984604fd651d74aa49a2d7513f096faaf49f9f27
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/18/2020
ms.locfileid: "3270307"
---
# <a name="dual-currency"></a>Twee valuta's

[!include [banner](../includes/banner.md)]

Met functionaliteit die is geïntroduceerd in Microsoft Dynamics 365 for Finance and Operations versie 8.1 (oktober 2018) kan de aangiftevaluta worden ingezet als een tweede valuta voor boekhouding. Deze functionaliteit wordt soms ook wel *dubbele valuta* genoemd. De wijzigingen voor dubbele valuta kunnen niet worden uitgeschakeld via een configuratiesleutel of parameter. Aangezien de aangiftevaluta wordt gebruikt als een tweede valuta voor boekhouding, is de manier waarop de aangiftevaluta wordt berekend in de boekingslogica gewijzigd.

Bovendien zijn verschillende modules verbeterd om de aangiftevaluta in verschillende processen bij te houden, aan te geven en te gebruiken. De modules die worden beïnvloed zijn:

- Grootboek 
- Financiële rapportage 
- Leveranciers
- Klanten 
- Contanten en bankbeheer 
- Vaste activa 
- Consolidaties

Na een upgrade moet u bepaalde stappen uitvoeren voor Kas- en bankbeheer en Vaste activa. Daarom moet u de relevante onderdelen van dit onderwerp zorgvuldig lezen en begrijpen.

## <a name="posting-process"></a>Boekingsproces

De boekingslogica is gewijzigd voor alle transacties die een boekingspost naar het grootboek genereren. Hier ziet u hoe de aangiftevaluta eerder werd berekend:

Transactievalutabedrag \> Boekhoudingsvalutabedrag \> Aangiftevalutabedrag

Bijvoorbeeld een transactie wordt ingevoerd in de valuta Canadese dollar (CAD). Het CAD-bedrag wordt omgezet in de valuta voor boekhouding, namelijk de Amerikaanse dollar (USD). Het USD-bedrag wordt dan omgezet in de aangiftevaluta, namelijk de euro (EUR). Daarom moeten er wisselkoersen bestaan tussen CAD en USD en tussen USD en EUR.

Hier volgt de nieuwe berekening:

Transactievalutabedrag \> Boekhoudingsvalutabedrag

Transactievalutabedrag \> Aangiftevalutabedrag

Vanwege deze wijziging moeten er nu wisselkoersen bestaan tussen CAD en USD en tussen CAD en EUR.

## <a name="reports-and-inquiries"></a>Rapporten en query's

Verschillende rapporten en query's bevatten nu zowel aangiftevalutabedragen als boekhoudingsvalutabedragen. Niet elk rapport en elke query is bijgewerkt. Bijvoorbeeld rapporten die bedragen alleen in de transactievaluta weergeven, zijn niet gewijzigd.

De wijzigingen volgen een van twee patronen:

- Als het rapport of de query voldoende ruimte had om bedragen weer te geven in zowel de boekhoudingsvaluta als de aangiftevaluta, zijn de aangiftevalutabedragen toegevoegd.
- Als het rapport of de query niet voldoende ruimte had om bedragen in beide valuta's weer te geven, is een optie toegevoegd zodat gebruikers kunnen kiezen welke valuta wordt weergegeven.

Voor verschillende rapporten en query's is ook logica toegevoegd om aangiftevalutabedragen te onderdrukken als de aangiftevaluta hetzelfde is als de boekhoudingsvaluta of als de aangiftevaluta niet is gedefinieerd in het grootboek voor de rechtspersoon.

## <a name="financial-journals"></a>Financiële journalen

De financiële journalen, zoals het algemene journaal en het leveranciersfacturenjournaal, zijn bijgewerkt zodat ze extra informatie over de aangiftevaluta bevatten. Totalen voor het boekstuk en het journaal worden nu weergegeven in de aangiftevaluta. Bovendien wordt informatie over de wisselkoers van de aangiftevaluta nu weergegeven op het tabblad **Algemeen** van de journaalregels. Daarom kunt u de wisselkoers voor de aangiftevaluta overschrijven wanneer u transacties invoert.

## <a name="vendor-invoices-sales-orders-and-sales-agreements"></a>Leveranciersfacturen, verkooporders en verkoopovereenkomsten
Leveranciersfacturen, verkooporders en verkoopovereenkomsten zijn bijgewerkt met een vaste wisselkoers voor de aangiftevaluta. Voor zowel de valuta voor boekhouding als voor de aangiftevaluta kan een vaste wisselkoers worden gedefinieerd wanneer de transactievaluta afwijkt. Wanneer de valuta voor de boekhouding en de aangiftevaluta gelijk zijn, wordt de vaste wisselkoers gesynchroniseerd door het vaste tarief van de valuta voor de boekhouding te gebruiken als vast tarief voor de aangiftevaluta. De vaste wisselkoers voor de aangiftevaluta kan niet worden gewijzigd voor deze configuratie. Wanneer de valuta voor de boekhouding en de aangiftevaluta verschillen, kan een vaste wisselkoers worden gedefinieerd voor zowel de valuta voor de boekhouding als de aangiftevaluta tijdens het invoeren van de transactie. Als de aangiftevaluta niet is gedefinieerd in het grootboek, is het veld **Vaste wisselkoers voor aangiftevaluta** niet ingeschakeld en wordt er geen bedrag voor de aangiftevaluta berekend.

## <a name="module-changes"></a>Modulewijzigingen

De volgende modules gebruiken de aangiftevaluta als een tweede valuta voor boekhouding:

- [Grootboek](#general-ledger)
- [Financiële rapportage](#financial-reporting)
- [Leveranciers](#accounts-payable-and-accounts-receivable)
- [Klanten](#accounts-payable-and-accounts-receivable)
- [Contanten en bankbeheer](#cash-and-bank-management)
- [Vaste activa](#fixed-assets)
- [Consolidaties](#consolidations)

### <a name="general-ledger"></a>Grootboek

Als een aangiftevaluta is gedefinieerd in het grootboek, hield het grootboek al aangiftevalutabedragen bij voor elke boekhoudingspost. Deze bedragen worden echter nu vertaald vanuit de transactievalutabedragen.

De volgende aanvullende wijzigingen zijn aangebracht in de module **Grootboek**:

- Een afzonderlijk wisselkoerstype voor de aangiftevaluta kan worden gedefinieerd in het grootboek. Als een organisatie geen ander wisselkoerstype wil gebruiken, kunt u het veld voor het wisselkoerstype voor de aangiftevaluta leeg laten. U kunt ook hetzelfde wisselkoerstype selecteren dat wordt gebruikt voor de boekhoudingsvaluta. Als u het veld leeg laat, wordt het wisselkoerstype gebruikt voor de boekhoudingsvaluta.
- Met een nieuw journaal, het Correctiejournaal aangiftevaluta, kunnen correcties worden geboekt naar grootboekrekeningen in alleen de aangiftevaluta. Met dit journaal kan alleen naar grootboekrekeningen worden geboekt. Intercompany wordt niet ondersteund en de valuta moet de aangiftevaluta van de rechtspersoon zijn waar het journaal wordt geboekt. Wanneer het journaal wordt geboekt, zijn het transactievalutabedrag en het aangiftevalutabedrag 0 (nul) en wordt het aangiftevalutabedrag geboekt met het bedrag dat in de transactie is ingevoerd. Omdat de manier waarop de aangiftevaluta wordt gebruikt in de modules **Leveranciers**, **Klanten** en **Vaste activa** is gewijzigd, kan dit journaal worden gebruikt voor correcties na een upgrade. Zie de secties voor deze modules voor voorbeelden die laten zien hoe dit journaal kan worden gebruikt.
- Het proces voor periodetoewijzing is bijgewerkt zodat het bedragen toewijst in de transactie-, boekhoudings- en aangiftevaluta. Bedragen werden eerder toegewezen in de transactie- en de boekhoudingsvaluta en vervolgens werd het boekhoudingsvalutabedrag vertaald naar de aangiftevaluta. Dat gedrag kan leiden tot een resterend saldo op de grootboekrekening in de aangiftevaluta. Wanneer bedragen worden berekend en gebruikt in de boekhoudingspost, vindt nu geen vertaling plaats.
- Het proces voor herwaardering van vreemde valuta's herwaardeert bedragen in de aangiftevaluta. Het aangiftevalutabedrag wordt nu echter berekend via het transactievalutabedrag, zoals beschreven in de sectie [Boekingsproces](#posting-process) eerder in dit onderwerp.
- Veel rapporten en query's in het Grootboek bevatten al de aangiftevaluta, maar enkele niet. Eén voorbeeld is de lijstpagina **Proefbalans**. Deze lijstpagina bevat nu kolommen voor de boekhoudingsvaluta en de aangiftevaluta. De kolommen voor de aangiftevaluta worden verborgen als de boekhoudingsvaluta en de aangiftevaluta hetzelfde zijn of als geen aangiftevaluta is gedefinieerd in het grootboek.

### <a name="financial-reporting"></a>Financiële rapportage

Dankzij een verbetering van de module **Financiële rapportage** kunt u aangiftevalutabedragen op twee manieren opnemen in een financieel overzicht. In de kolomdefinitie kunt u rechtstreeks rapporteren in de aangiftevalutabedragen die naar het grootboek worden geboekt (nieuwe functionaliteit). U kunt ook doorgaan met vertalen van bedragen van de boekhoudingsvaluta naar de aangiftevaluta (bestaande functionaliteit).

Deze wijziging is beschikbaar via de instelling **Weergegeven valuta** in de kolomdefinitie. Als u **Rapportvaluta uit grootboek** selecteert, worden bedragen in de kolom niet vertaald. In plaats daarvan worden deze rechtstreeks vanuit het grootboek aangegeven. Als u wilt dat de kolom vertaalde bedragen weergeeft, selecteert u de optie **Omrekenen naar XXXX**, waarbij *XXXX* de aangiftevaluta is die in de kolom moet worden weergegeven. In dit geval worden boekhoudingsvalutabedragen vertaald naar de geselecteerde valuta met behulp van de bestaande omrekenfunctionaliteit.

### <a name="accounts-payable-and-accounts-receivable"></a>Leveranciers en Klanten

De modules **Leveranciers** en **Klanten** hielden al aangiftevalutabedragen bij. De bedragen werden echter niet weergegeven of gebruikt voor verschillende processen. De volgende wijzigingen zijn aangebracht:

- Aangiftevalutabedragen worden nu in transacties weergegeven voor klanten en leveranciers. Aangiftevalutabedragen worden ook weergegeven voor het openstaande saldo van elke transactie.
- Het ouderdomsrangschikkingsproces is bijgewerkt zodat een organisatie de naar ouderdom gerangschikte verzamelingen in de valuta voor boekhouding of de aangiftevaluta kan weergeven.
- Verschillende query's en rapporten zijn bijgewerkt zodat ze aangiftevalutabedragen tonen. Voorbeelden zijn de rapporten **Afstemming van klant met grootboek** en **Afstemming leverancier met grootboek**.
- Het proces voor herwaardering van vreemde valuta's herwaardeert bedragen in de aangiftevaluta. Het aangiftevalutabedrag wordt nu echter berekend via het transactievalutabedrag, zoals beschreven in de sectie [Boekingsproces](#posting-process).
- **Overweging bij de upgrade:** vóór een upgrade worden de aangiftevalutabedragen voor documenten (facturen, betalingen, enzovoort) berekend via de valuta voor boekhouding. Bijvoorbeeld een factuur wordt geboekt vóór de upgrade van een organisatie en de factuur is niet betaald. Tijdens de upgrade wordt de boekhoudingspost van de factuur niet gewijzigd. Na de upgrade zijn de wijzigingen voor dubbele valuta's echter van kracht. Dus wanneer een betaling wordt gedaan voor de factuur, wordt het aangiftevalutabedrag van de betaling nu berekend via het transactievalutabedrag. Als de betaling en de factuur worden vereffend, kan een gering verschil worden berekend in het bedrag van gerealiseerde winst/verlies, omdat aangiftevalutabedragen nu anders worden berekend. Als het verschil dat wordt berekend als belangrijk wordt beschouwd, kan het nieuwe correctiejournaal voor aangiftevaluta worden gebruikt om het saldo van de gerealiseerde winst/verlies en de leveranciers/klanten-grootboekrekeningen alleen in de aangiftevaluta aan te passen.

### <a name="cash-and-bank-management"></a>Contanten en bankbeheer

Eerder hield de module **Kas- en bankbeheer** geen aangiftevalutabedragen bij voor transacties die zijn geboekt voor elke bankrekening. Na een upgrade worden de bedragen in de aangiftevaluta automatisch bijgehouden voor eventuele nieuwe transacties die worden geboekt. Aangiftevalutabedragen moeten echter worden toegevoegd aan eerder geboekte transacties in de subadministratie.

- **Overweging bij de upgrade:** omdat bankrekeningtransacties eerder geen aangiftevalutabedragen bijhielden in de subadministratie, is een wizard toegevoegd zodat u aangiftevalutabedragen kunt toevoegen aan bankrekeningtransacties. Deze wizard boekt **niet** opnieuw naar het grootboek. In plaats daarvan worden de aangiftevalutabedragen uit het grootboek overgenomen en worden deze bijgewerkt in de subadministratietabellen.

    - Als u de wizard wilt starten, selecteert u **Kas- en bankbeheer** \> **Instellen** \> **Bedragen in aangiftevaluta toevoegen aan bankrekeningtransacties**.
    - De wizard toont transacties voor alle bankrekeningen in het huidige bedrijf met een aangiftevalutabedrag van 0 (nul). Alleen transacties die zijn geboekt vóór de upgrade, worden opgenomen.
    - Voor elke bankrekeningtransactie zoekt de wizard de overeenkomende boekhoudingsposten in het grootboek en wordt een standaardaangiftevalutabedrag ingevoerd. Hoewel de bedragen kunnen worden bewerkt, wordt u aangeraden deze **niet** te bewerken. Anders kunt u de bankrekeningsaldi mogelijk niet reconciliëren met het grootboek. De enige keer dat u een bedrag moet bewerken is als het aangiftevalutabedrag niet kan worden gevonden in het grootboek. In dat geval geeft de wizard een bedrag van 0 (nul) voor de aangiftevaluta weer.
    - Als u **Annuleren** selecteert in de wizard, worden de bankrekeningtransacties en wijzigingen in de aangiftevalutabedragen opgeslagen tot de volgende keer dat u de wizard uitvoert. De aangiftevalutabedragen worden echter niet bijgewerkt in de bankrekeningtransacties. Die update gebeurt alleen wanneer u **Voltooien** selecteert in de wizard. U kunt de wizard meerdere keren uitvoeren. U kunt daarom onjuiste aangiftevalutabedragen corrigeren als u een fout hebt gemaakt.

- Er zijn geen processen in Kas- en bankbeheer gewijzigd, maar verschillende rapporten en query's zijn bijgewerkt, zodat ze aangiftevalutabedragen tonen. De cashflowprognoserapporten vormen een uitzondering. Ze zijn niet bijgewerkt voor het opnemen van de aangiftevalutabedragen.

### <a name="fixed-assets"></a>Vaste activa

Eerder hield de module **Vaste activa** geen aangiftevalutabedragen bij voor transacties die werden geboekt voor elk vaste-activaboek. Na een upgrade worden de bedragen in de aangiftevaluta automatisch bijgehouden voor eventuele nieuwe transacties die worden geboekt. Aangiftevalutabedragen moeten echter worden toegevoegd aan eerder geboekte transacties in de subadministratie.

Bovendien zijn belangrijke wijzigingen aangebracht in het afschrijvingsproces. Deze wijzigingen vereisen gebruikersactie na een upgrade. Het is belangrijk dat u de volgende wijzigingen leest en begrijpt, zelfs als u Vaste activa nog niet gebruikt.

- De manier waarop het afschrijvingsproces het aangiftevalutabedrag bepaalt is gewijzigd. Het volgende scenario vergelijkt hoe afschrijving eerder het aangiftevalutabedrag bepaalde en hoe het nu het aangiftevalutabedrag bepaalt.



    **Afschrijvingsscenario**

    Een activum wordt verworven en geboekt met de volgende bedragen. Houd er rekening mee dat het aangiftevalutabedrag in het grootboek wordt geboekt, maar niet wordt opgeslagen in Vaste activa-subadministratietabellen.

    | Transactietype | Transactiebedrag | Wisselkoers | Bedrag in valuta voor boekhouding | Wisselkoers | Aangiftevalutabedrag |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Verwerving      | 1.000.000 DKK      | 2,0           | 500.000 USD                | 2.5           | 200.000 EUR               |

    **Vorige afschrijving voor de aangiftevaluta**

    Aan het einde van het jaar wordt het afschrijvingsvoorstel uitgevoerd en worden de volgende bedragen berekend.

    | Transactietype | Transactiebedrag | Wisselkoers | Bedrag in valuta voor boekhouding | Wisselkoers | Aangiftevalutabedrag |
    |------------------|--------------------|---------------|----------------------------|---------------|---------------------------|
    | Afschrijving     | 50.000 USD         | 1.0           | 50.000 USD                 | 2.6           | 19.230,77 EUR             |

    Wanneer het afschrijvingsvoorstel wordt uitgevoerd, wordt het bedrag van de valuta voor boekhouding berekend met behulp van de afschrijvingsmethode. Vervolgens wordt dit bedrag naar de aangiftevaluta omgerekend met behulp van de huidige wisselkoers voor USD en EUR. Deze omrekening veroorzaakt problemen, omdat het activum niet volledig in de aangiftevaluta kan worden afgeschreven wanneer de contante koers wordt gebruikt.

    **Nieuwe afschrijving voor de aangiftevaluta**

    Het afschrijvingsproces is gewijzigd zodat het bedrag van de aangiftevaluta ook wordt berekend met behulp van de afschrijvingsmethode. Hier zijn de resultaten wanneer afschrijving wordt uitgevoerd op het activum.

    | Transactietype | Transactiebedrag | Wisselkoers | Bedrag in valuta voor boekhouding | Wisselkoers                                                       | Aangiftevalutabedrag |
    |------------------|--------------------|---------------|----------------------------|---------------------------------------------------------------------|---------------------------|
    | Afschrijving     | 50.000 USD         | 1.0           | 50.000 USD                 | 2.5<blockquote>[!NOTE] Hoewel deze wisselkoers wordt weergegeven, wordt deze niet gebruikt om om te rekenen naar de aangiftevaluta.</blockquote> | 20.000 EUR                |

    Wanneer het afschrijvingsvoorstel wordt uitgevoerd, wordt zowel het bedrag van de valuta voor boekhouding als het bedrag van de aangiftevaluta met de afschrijvingsmethode berekend. De bedragen worden vervolgens gebruikt in de boekhoudpost in het grootboek. Er wordt geen omrekening uitgevoerd om het aangiftevalutabedrag te bepalen.

- **Overweging bij de upgrade:** omdat vaste-activaboektransacties eerder de aangiftevaluta niet bijhielden, is een wizard toegevoegd zodat u aangiftevalutabedragen kunt toevoegen aan vaste-activaboektransacties. Deze wizard boekt **niet** opnieuw naar het grootboek. Omdat de manier waarop het afschrijvingsvoorstel aangiftevalutabedragen berekent is gewijzigd, **moet** de wizard worden uitgevoerd en voltooid voor elk bedrijf voordat een organisatie afschrijvingstransacties kan invoeren.

    - Als u de wizard wilt starten, selecteert u **Vaste activa** \> **Instellen** \> **Bedragen in aangiftevaluta toevoegen aan vaste-activaboeken**.
    - De wizard toont transacties voor alle vaste-activaboeken in het huidige bedrijf met een aangiftevalutabedrag van 0 (nul). Alleen transacties die zijn geboekt vóór de upgrade, worden opgenomen.
    - De wizard haalt **niet** de aangiftevalutabedragen uit het grootboek. Zoals is beschreven in het vorige scenario, gebruikten de aangiftevalutabedragen die oorspronkelijk zijn geboekt naar het grootboek, de contante koers. Deze bedragen moeten niet in de vaste-activasubadministratie worden weergegeven, omdat de volgende afschrijvingsberekening de onjuiste bedragen gebruikt. De wizard vindt in plaats daarvan de wisselkoers op de datum van de eerste aankoop. Vervolgens wordt die wisselkoers gebruikt om het aangiftevalutabedrag aan te bevelen dat moet worden geboekt in de subadministratie. Dit is bijvoorbeeld wat de wizard kan weergeven voor het vorige scenario.

        | Vaste activa | Boek      | Transactietype | Transactiedatum | Valuta | Bedrag in transactievaluta | Bedrag  | Wisselkoers | Aangiftevalutabedrag |
        |-------------|-----------|------------------|------------------|----------|--------------------------------|---------|-----------|---------------------------|
        | BUIL-00001  | 200\_SLLT | Verwerving      | 6/3/2016         | DKK      | 1.000.000                      | 500,000 | 2.5       | 250,000                   |
        | BUIL-00001  | 200\_SLLT | Afschrijving     | 6/3/2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | Afschrijving     | 6/3/2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |
        | BUIL-00001  | 200\_SLLT | Afschrijving     | 6/3/2016         | USD      | 50,000                         | 50,000  | 2.5       |  25,000                   |

    - Veel klanten hielden hun activatransactiedetails bij in werkmappen. Deze gegevens omvatten de wisselkoersen en bedragen. Als u deze gegevens in een werkmap hebt, kunt u een aangepast wisselkoerstype maken en bijwerken met de wisselkoersen van de werkmap. Dit wisselkoerstype wordt vervolgens gebruikt om een standaardwisselkoers in te voeren op de verwervingsdatum en het aangiftevalutabedrag te berekenen. Als geen wisselkoerstype is geselecteerd, gebruikt de wizard het wisselkoerstype dat voor het grootboek was gedefinieerd.
    - De wisselkoers en de aangiftevalutabedragen kunnen worden gewijzigd. Als de wisselkoers wordt gewijzigd, wordt het aangiftevalutabedrag opnieuw berekend met behulp van het nieuwe tarief.
    - Als u **Annuleren** selecteert in de wizard, worden de vaste-activatransacties en wijzigingen in de wisselkoers of aangiftevalutabedragen opgeslagen tot de volgende keer dat u de wizard uitvoert. De aangiftevalutabedragen worden echter niet bijgewerkt in de vaste-activaboektransacties. Die update gebeurt alleen wanneer u **Voltooien** selecteert in de wizard. U kunt de wizard meerdere keren uitvoeren. U kunt daarom onjuiste aangiftevalutabedragen corrigeren als u een fout hebt gemaakt.
    - Wanneer de aangiftevalutabedragen volledig zijn bijgewerkt in de subadministratie, **moet** u de optie **Hebt u alle bedragen in de aangiftevaluta bijgewerkt in de vaste-activaboektransacties?** op **Ja** instellen en vervolgens **Voltooien** selecteren. Afschrijvingsberekeningen kunnen niet worden voltooid totdat u de optie **Hebt u alle bedragen in de aangiftevaluta bijgewerkt in de vaste-activaboektransacties?** op **Ja** hebt ingesteld. Nadat deze optie is ingesteld op **Ja**, is de wizard niet langer beschikbaar.
    - Nadat de vaste-activatransacties in de subadministratie zijn bijgewerkt met de aangiftevalutabedragen, komen deze bedragen niet overeen met de bedragen die oorspronkelijk zijn geboekt naar het grootboek. Het correctiejournaal voor aangiftevaluta kan echter worden gebruikt voor het bijwerken van de saldi van de afschrijvingsgrootboekrekeningen in het grootboek, zodat deze overeenkomen met de bedragen die oorspronkelijk zijn geboekt.
    - Er is een nieuwe entiteit **Bedragen in de aangiftevaluta voor activatransacties** toegevoegd aan het werkgebied **Gegevensbeheer**, waarmee u de gegevens uit de wizard kunt exporteren. U kunt de gegevens vervolgens gebruiken om het saldo in de subadministratie te bepalen voor de vaste-activatransacties. Dat saldo kan vervolgens worden gebruikt om het bedrag te bepalen van de aanpassing van de aangiftevaluta in het grootboek.

- **Overweging bij de upgrade:** er zijn nieuwe instellingsvelden toegevoegd aan vaste activa en deze worden gebruikt bij de berekening van de afschrijving. U moet deze velden mogelijk bijwerken vóór de volgende afschrijvingsberekening.

    - In het vaste-activaboek (**Vaste activa** \> **boeken**) heeft het sneltabblad **Algemeen** een nieuw veld **Aanschafprijs in aangiftevaluta**.
    - In het vaste-activaboek (**Vaste activa** \> **boeken**) heeft het sneltabblad **Afschrijving** een nieuw veld **Verwachte restwaarde in aangiftevaluta**.
    - In de parameters voor vaste activa (**Vaste activa** \> **Instellen** \> **Vaste-activaparameters**) heeft het sneltabblad **Algemeen** een nieuw veld **Minimaal afschrijvingsbedrag in aangiftevaluta**.
    - In boeken (**Vaste activa** \> **Instellen** \> **Boeken**) heeft het sneltabblad **Algemeen** twee nieuwe velden: **Afschrijving in aangiftevaluta afronden** en **Nettoboekwaarde op aangiftevaluta laten staan**.

- Omdat het afschrijvingsvoorstel nu bedragen in zowel de boekhoudingsvaluta als de aangiftevaluta berekent, is het vaste-activajournaal bijgewerkt zodat het afschrijvingsbedragen in de aangiftevaluta toont. Voor afschrijvingstransacties is de transactievaluta altijd de boekhoudingsvaluta. Daarom blijven deze bedragen weergegeven in de kolommen **Debet** en **Credit**. Twee nieuwe kolommen, **Debet in aangiftevaluta** en **Credit in aangiftevaluta**, zijn toegevoegd aan het raster.

    - De nieuwe velden zijn alleen beschikbaar als het transactietype een van de vier typen afschrijving is: **Afschrijving**, **Afschrijvingscorrectie**, **Buitengewone afschrijving** of **Speciale afschrijvingsaftrek**.
    - Als een transactietype voor afschrijving wordt ingevoerd in het vaste-activajournaal, worden de aangiftevalutabedragen in de nieuwe kolommen weergegeven. Deze bedragen kunnen worden gewijzigd.
    - Als de boekhoudingsvaluta en de rapportagevaluta's in het grootboek hetzelfde zijn, worden de bedragen synchroon gehouden. Als u het **Credit**-bedrag wijzigt, wordt het bedrag **Credit in aangiftevaluta** automatisch gewijzigd zodat het ermee overeenkomt.
    - Als een ander transactietype is ingevoerd in het vaste-activajournaal, worden de bedragen **Debet in aangiftevaluta** en **Credit in aangiftevaluta** nooit weergegeven, niet vóór en niet na de boeking. De boekhoudingsvaluta- en aangiftevalutabedragen zijn nog steeds beschikbaar in het boekstuk dat naar het grootboek wordt geboekt.
    
### <a name="consolidations"></a>Consolidaties
    
De functionaliteit die is geïntroduceerd in Dynamics 365 Finance versie 10.0.5 (oktober 2019), omvat functiebeheer voor een verbeterde flexibiliteit voor consolidatie en een dubbele valuta. Om deze functionaliteit in te schakelen gaat u naar het werkgebied **Functiebeheer** en selecteert u **Functionaliteit voor twee valuta inschakelen voor consolidatie in het Grootboek**.

Bij de consolidatie van het grootboek is een nieuwe optie toegevoegd om de boekhoudings- of rapporteringsvalutabedragen van de bronbedrijven te consolideren. Als de boekhoudings- of rapporteringsvaluta overeenkomt met de boekhoudings- of rapporteringsvaluta in het consolidatiebedrijf, worden de bedragen direct gekopieerd in plaats van vertaald.

-  U kunt nu kiezen of de boekhoudings- of de rapporteringsvaluta van het bronbedrijf moet worden gebruikt als de transactievaluta in het consolidatiebedrijf.

- De boekhoudings- of rapporteringsvalutabedragen van het bronbedrijf worden rechtstreeks gekopieerd naar de boekhoudings- of rapporteringsvalutabedragen in het consolidatiebedrijf, als een van de valuta's hetzelfde is. De valutabedragen voor de boekhouding en de rapportering in het consolidatiebedrijf worden berekend met behulp van de wisselkoers als geen van beide valuta's hetzelfde is.
