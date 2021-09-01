---
title: Waarom kan ik deze transactie niet ongedaan maken?
description: In dit onderwerp worden verschillende redenen beschreven waarom transacties niet kunnen worden omgekeerd. Er wordt ook een lijst met oplossingen voor dit probleem vermeld.
author: kweekley
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-07-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 869832f085ee91f6c1fee53dad508cf5e54535627dadd6fb59a7586b03c8ec3b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719728"
---
# <a name="why-cant-i-reverse-this-transaction"></a>Waarom kan ik deze transactie niet ongedaan maken?

[!include [banner](../includes/banner.md)]

In dit onderwerp worden verschillende redenen beschreven waarom transacties niet kunnen worden omgekeerd. Er wordt ook een lijst met oplossingen voor dit probleem vermeld.

## <a name="symptom"></a>Symptoom

Organisaties kunnen in situaties terechtkomen waarin ze een geboekte transactie moeten omkeren. Soms wordt dit verhinderd door het systeem. Dit gedrag kan tot twee vragen leiden:

- Waarom kan ik de transactie niet omkeren?
- Wat is de invloed van de functie voor massaal omkeren op dit gedrag?

## <a name="resolution"></a>Oplossing

Transacties moeten aan specifieke criteria voldoen voordat ze kunnen worden omgekeerd. De resterende secties van dit onderwerp bieden de validatie voor elke module. Hoewel dit onderwerp zich richt op transacties in Microsoft Dynamics 365 Finance, kunnen enkele van de concepten en validatie ook worden toegepast op andere toepassingen, zoals Dynamics 365 Supply Chain Management.

Bovendien kan de plaats waar een transactie wordt omgekeerd invloed hebben op de vraag of de transactie kan worden omgekeerd. Een leveranciersbetaling die als cheque is geboekt, kan bijvoorbeeld alleen worden omgekeerd via de sectie **Cheques** op de transactiepagina voor de bankrekeningen. Deze kan niet worden omgekeerd via de pagina **Boekstuktransacties** in Grootboek.

Als de functie **Massaal omkeren voor meerdere documenten** (ook wel de functie Massaal omkeren genoemd) is ingeschakeld in de werkruimte **Functiebeheer**, heeft dit invloed op het aantal transacties dat kan worden omgekeerd en op de plaats waar deze kunnen worden omgekeerd. Deze functie levert twee voordelen op wanneer deze is ingeschakeld:

- Voor sommige transactietypen kunt u meerdere transacties tegelijk selecteren en omkeren vanuit het journaal waarin de transactie is geboekt, of via de pagina **Boekstuktransacties**. De afzonderlijke transacties moesten echter omkeerbaar zijn voordat de functie werd ingeschakeld. Voordat deze functie werd geïntroduceerd, moesten transacties een voor een worden omgekeerd.
- *Sommige* subgrootboektransacties kunnen worden omgekeerd vanuit het journaal (algemeen journaal) of de pagina **Boekstuktransacties**. Ze hoeven niet te worden omgekeerd via de subgrootboekpagina. Een leveranciersfactuurjournaal kon eerder bijvoorbeeld alleen worden omgekeerd via de pagina **Leverancierstransacties**. Het kunt nu echter ook vanuit het grootboek worden gedaan, via de pagina **Boekstuktransacties**. In elke sectie van dit onderwerp wordt uitgelegd voor welke transactietypen dit voordeel niet van toepassing is.

Met de functie voor massaal omkeren kunnen **niet** meer typen transacties worden omgekeerd. Als een transactietype eerder niet kon worden omgekeerd, kan deze nog steeds niet worden omgekeerd als de functie is ingeschakeld. Leveranciersfacturen voor inkooporders kunnen bijvoorbeeld niet worden omgekeerd, ongeacht of de functie voor massaal omkeren is ingeschakeld.

Zie [Journaalboeking omkeren](reverse-journal-posting.md) voor meer informatie over de functie voor massaal omkeren.

## <a name="general-ledger"></a>Grootboek

Grootboekcorrecties worden alleen met grootboekrekeningen ingevoerd. Deze worden daarom alleen in Grootboek bijgewerkt.

Als de functie Massaal omkeren is uitgeschakeld, kunnen de meeste grootboekcorrecties afzonderlijk worden omgekeerd via de pagina **Transacties voor \<main account\>** voor het grootboek (**LedgerTransAccount**). (De exacte titel van de pagina varieert, afhankelijk van de geselecteerde hoofdrekening.) Op de pagina wordt elke transactie weergegeven die naar de hoofdrekening is geboekt. Deze wordt meestal geopend via de lijstpagina **Proefbalans** of door **Transacties** te selecteren op de pagina **Boekstuktransacties**.

Als de functie Massaal omkeren is ingeschakeld, kunnen een of meer grootboekboekingen nu worden omgekeerd via de pagina **Boekstuktransacties** en vanuit het journaal waaruit de transactie is geboekt. De uitzonderingen zijn herwaarderingen van vreemde valuta, consolidaties en jaarafsluitingstransacties. Deze transacties worden omgekeerd vanaf de pagina's waarop de jaarafsluiting is uitgevoerd.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Redenen waarom transacties niet kunnen worden omgekeerd

Transacties kunnen om de volgende redenen niet worden omgekeerd:

- Algemeen journaal:

    - De boekperiode staat in de wachtstand of is definitief afgesloten:

        - Als de omkeringsdatum zich in een boekperiode bevindt die niet is geopend, kan de transactie niet worden omgekeerd.
        - Als de transactie de invoer van een terugboekingsdatum ondersteunt, kan de transactie nog worden teruggeboekt door de terugboekingsdatum in een openstaande periode te wijzigen.

    - Het jaarafsluitingsproces is uitgevoerd:

        - De boekingsdatum van de transactie valt in een boekjaar waarvoor een jaarafsluiting is uitgevoerd. Hoewel een periode in het boekjaar nog kan open staan, kan de transactie niet worden omgekeerd als het jaarafsluitingsproces voor het boekjaar is uitgevoerd. Het boekjaar heeft een andere status dan de perioden erin.
        - De jaarafsluiting kan ongedaan worden gemaakt. Vervolgens kan de transactie worden omgekeerd. Deze benadering is mogelijk geen optie. Afhankelijk van de status van het boekjaar kan het eenvoudiger zijn handmatig een terugboekingstransactie in een openstaande periode van het afgesloten boekjaar of het volgende boekjaar in te voeren. Als een nieuwe transactie wordt geboekt naar een openstaande periode van het boekjaar waarvoor het jaarafsluitingsproces is uitgevoerd, moet de jaarafsluiting opnieuw worden uitgevoerd.

    - De transactie wordt al omgekeerd:

        - Als de transactie al wordt omgekeerd, moet dit proces zijn voltooid. U kunt geen afzonderlijk omkeringsproces uitvoeren. 
        - Als de omkering is voltooid, kan een omgekeerde transactie opnieuw worden omgekeerd (dat wil zeggen dat de omkering kan worden omgekeerd).

    - Grootboekvereffening:

        - De transactie kan niet worden omgekeerd als een of meer regels van de transactie in het grootboek zijn vereffend met de periodieke taak **Grootboekvereffeningen** (**Grootboek \> Periodieke taken \> Grootboekvereffeningen**), zodat de record bestaat in de tabel LedgerTransSettlement.
        - De grootboekvereffening kan ongedaan worden gemaakt. Vervolgens kan het boekstuk worden omgekeerd.

    - Intercompany:

        - Als het om een intercompany-transactie gaat, kan deze niet worden omgekeerd.
        - De transactie is **geen** intercompany-transactie, maar wordt geboekt op een hoofdrekening voor 'verschuldigd aan' of 'verschuldigd van' die is gedefinieerd op de pagina **Intercompany-instellingen**.

    - Transitorische posten:

        - Als het transitorische grootboekboekstuk wordt omgekeerd, worden de transitorische invoer en alle bijbehorende toerekeningssubtransacties omgekeerd.
        - De afzonderlijke toerekeningssubtransacties kunnen niet worden omgekeerd.

- Journaal voor opbrengsttoerekening:

    - Opbrengsttoerekeningstransacties kunnen niet worden omgekeerd.
    - Wanneer opbrengst wordt toegerekend via het journaal voor opbrengsttoerekening, wordt het boekstuk alleen naar grootboekrekeningen geboekt. Daarom worden de transacties op pagina's zoals **Boekstuktransacties** weergegeven alsof ze alleen grootboekposten zijn.

- Herwaardering van vreemde valuta:

    - Herwaarderingstransacties voor vreemde valuta's kunnen worden omgekeerd, maar alleen via de grootboekpagina **Herwaardering van vreemde valuta** waarop de herwaardering is uitgevoerd.
    - De omkering kan alleen worden uitgevoerd als deze is geboekt naar een openstaande boekperiode.

- Consolidatie:

    - Consolidatietransacties kunnen worden omgekeerd, maar alleen via de pagina **Consolidatietransacties**.
    - De omkering kan alleen worden uitgevoerd als deze is geboekt naar een openstaande boekperiode.

- Jaarafsluiting:

    - Jaarafsluitingstransacties (zowel afsluitings- als openingstransacties) kunnen op de volgende manieren worden omgekeerd:

        - Als de functie voor verbeteringen voor de jaarafsluiting van grootboeken is uitgeschakeld, selecteert u de optie **Vorige afsluiting ongedaan maken** in het dialoogvenster **Jaarafsluiting**.
        - Als de functie voor verbeteringen voor de jaarafsluiting van grootboeken is ingeschakeld, selecteert u de records voor het bedrijf en het boekjaar die zijn gemaakt voor de jaarafsluiting op de pagina **Jaarafsluiting** en selecteert u **Jaarafsluiting omkeren**.

    - Bij een omkering van de jaarsluiting worden de afsluitings- en openingstransacties daadwerkelijk verwijderd. Een terugboekingsboekstuk wordt nooit geboekt.

## <a name="accounts-payable"></a>Crediteuren

De subadministratie Leveranciers wordt bijgewerkt met meerdere transactietypen. Voorbeelden zijn leveranciersfacturen, leveranciersfactuurjournalen en onkostenrapporten.

Als de functie voor massaal omkeren is uitgeschakeld, kunnen transacties afzonderlijk worden omgekeerd via de pagina **Leverancierstransacties** voor facturen of de pagina **Bankrekening** voor chequebetalingen.

Als de functie Massaal omkeren is ingeschakeld, kunnen een of meer leverancierstransacties ook worden omgekeerd via de pagina **Boekstuktransacties** en vanuit het journaal waaruit de transacties zijn geboekt. Leveranciersbetalingen kunnen echter nog steeds alleen vanaf de bankrekening worden omgekeerd. Daarnaast kunnen leverancierstransacties niet worden omgekeerd via de pagina **Transacties voor \<main account\>** voor het grootboek. Deze kunnen alleen worden omgekeerd via de pagina **Boekstuktransacties**.

Sommige transacties kunnen helemaal niet worden omgekeerd. Voorbeelden hiervan zijn inkooporderleveranciersfacturen en elektronische leveranciersbetalingen.

### <a name="reasons-why-vouchers-cant-be-reversed"></a>Redenen waarom boekstukken niet kunnen worden omgekeerd

Boekstukken kunnen om de volgende redenen niet worden omgekeerd:

- De boekperiode staat in de wachtstand of is afgesloten:

    - Als de omkeringsdatum zich in een boekperiode bevindt die niet is geopend, kan de transactie niet worden omgekeerd.
    - Als de transactie de invoer van een terugboekingsdatum ondersteunt, kan de transactie nog worden teruggeboekt door de terugboekingsdatum in een openstaande periode te wijzigen.

- Het jaarafsluitingsproces voor het grootboek is uitgevoerd:

    - De boekingsdatum van de transactie valt in een boekjaar dat is afgesloten in Grootboek. Hoewel een periode in het boekjaar nog kan open staan, kan de transactie niet worden omgekeerd als het jaarafsluitingsproces voor het boekjaar is uitgevoerd. Het boekjaar heeft een andere status dan de perioden erin.
    - De jaarafsluiting kan ongedaan worden gemaakt. Vervolgens kan de transactie worden omgekeerd. Deze benadering is mogelijk geen optie. Afhankelijk van de status van het boekjaar kan het eenvoudiger zijn handmatig een terugboekingstransactie in een openstaande periode van het afgesloten boekjaar of het volgende boekjaar in te voeren. Als een nieuwe transactie wordt geboekt naar een openstaande periode van het boekjaar waarvoor het jaarafsluitingsproces is uitgevoerd, moet de jaarafsluiting opnieuw worden uitgevoerd.

- Het journaal in de subadministratie is niet overgeboekt naar het grootboek:

    - Deze reden is alleen van toepassing op leveranciersfacturen voor niet-inkooporders.
    - Gebruik de pagina **Nog niet overgeboekte journaalposten in subadministratie** om de invoer over te boeken naar het grootboek. De leveranciersfactuur voor niet-inkooporders kan vervolgens worden omgekeerd via de pagina **Leverancierstransacties**.

- Vereffening:

    - De transactie (zoals een factuur of betaling) wordt vereffend of gemarkeerd voor vereffening.

        - U kunt controleren of een transactie is vereffend of gemarkeerd voor vereffening door **Vereffeningen weergeven** of **Vereffening \> Vereffeningshistorie** op de pagina **Leverancierstransacties** te selecteren.
        - U kunt een vereffening ook omkeren via de pagina **Leverancierstransacties** (**Vereffening \> Vereffening ongedaan maken**) als een van de transacties moet worden omgekeerd.

- Het boekstuk bevat meer dan één subboektransactie die is ingevoerd met hetzelfde boekstuknummer (probleem met één boekstuk).
- De factuur is niet goedgekeurd:

    - Als het selectievakje **Goedkeuring** niet is ingeschakeld op de factuur, kan de factuur niet worden omgekeerd.

        - In dit geval verwijst goedkeuring niet naar goedkeuringen in het werkstroomproces, maar naar de optie **Goedkeuring** op de factuur. Deze optie wordt gebruikt om te voorkomen dat een factuur wordt betaald. Deze wordt meestal gebruikt voor facturen voor het leveranciersfactuurregister.

- De transactie bevindt zich in de facturenpool:

    - Een factuur in de pool kan niet direct worden omgekeerd via de pagina **Leverancierstransacties**. In plaats daarvan moet deze worden omgekeerd via het annuleringsproces op de pagina **Factuurgoedkeuringsjournaal**.

- De transactie heeft een bovenliggende factuur die is gecorrigeerd (Indiase lokalisatie).
- De transactie heeft de promessestatus **Factuur geremitteerd**.
- De transactie wordt gebruikt voor een gedeeltelijke belastingvereffening.
- De transactie bevat een leveranciersrekening, maar wordt omgekeerd via een onjuiste pagina, zoals de pagina **Transacties voor \<main account\>**:

    - Zoals deze reden al suggereert, kunnen sommige grootboektransacties alleen via specifieke pagina's worden omgekeerd, zelfs als de functie Massaal omkeren is ingeschakeld.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Typen transacties die niet kunnen worden omgekeerd

De volgende typen transacties kunnen niet worden omgekeerd:

- Herwaardering van vreemde valuta:

    - In tegenstelling tot herwaarderingen van vreemde valuta in Grootboek kunnen herwaarderingen van vreemde valuta in Klanten en Crediteuren niet worden omgekeerd. In plaats daarvan moet de herwaardering opnieuw worden uitgevoerd op basis van de factuurdatum. In dit geval wordt bij de herwaardering de wisselkoers van de datum van de factuur gebruikt en worden niet-gerealiseerde winsten of verliezen in feite op 0 (nul) gezet. Het resultaat lijkt dus op het resultaat van het terugdraaien van de vorige herwaardering. Hetzelfde bedrag wordt echter niet omgekeerd als de standaardwisselkoers op de factuur is gewijzigd.

- Leveranciersfactuur voor inkooporder:

    - Er moet een creditnota worden gemaakt om de leveranciersfactuur om te keren. Zie [Een inkoopretourorder maken](../../supply-chain/procurement/tasks/create-purchase-return-order.md) voor meer informatie over het maken van een terugboekingstransactie.

- Promesse
- Verzending van export van bankkredietbrief

## <a name="accounts-receivable"></a>Debiteuren

Subjournalen voor klanten worden bijgewerkt met verschillende transactietypen. Voorbeelden zijn onder andere klantfacturen uit verkooporders, klantfacturen die via het algemene journaal worden ingevoerd, vrije-tekstfacturen, klantbetalingen en afschrijvingen.

Als de functie voor massaal omkeren is uitgeschakeld, kunnen transacties afzonderlijk worden omgekeerd via de pagina **Klanttransacties** voor facturen of de pagina **Bankrekeningen** voor stortingen. Zie het gedeelte [Contanten en bankbeheer](cant-reverse-transctns.md#cash-and-bank-management) verderop in dit onderwerp voor informatie over het omkeren van een betaling.

Als de functie Massaal omkeren is ingeschakeld, kunnen een of meer klanttransacties ook worden omgekeerd via de pagina **Boekstuktransacties** en vanuit het journaal waaruit de transacties zijn geboekt. Stortingen kunnen nog steeds alleen vanaf de bankrekening worden omgekeerd en vrije-tekstfacturen kunnen alleen via de oorspronkelijke pagina worden omgekeerd (als de functie voor het toestaan van correcties is ingeschakeld). Daarnaast kunnen klanttransacties nog steeds niet worden omgekeerd via de pagina **Transacties voor \<main account\>** voor het grootboek. Deze kunnen wel worden omgekeerd via de pagina **Boekstuktransacties**.

Sommige transacties kunnen niet worden omgekeerd. Voorbeelden zijn klantfacturen en afschrijvingen van verkooporders.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Redenen waarom transacties niet kunnen worden omgekeerd

Transacties kunnen om de volgende redenen niet worden omgekeerd:

- De boekperiode staat in de wachtstand of is definitief afgesloten:

    - Als de omkeringsdatum zich in een boekperiode bevindt die niet is geopend, kan de transactie niet worden omgekeerd.
    - Als de transactie de invoer van een terugboekingsdatum ondersteunt, kan de transactie nog worden teruggeboekt door de terugboekingsdatum in een openstaande periode te wijzigen.

- Het jaarafsluitingsproces voor het grootboek is uitgevoerd:

    - De boekingsdatum van de transactie valt in een boekjaar waarvoor een jaarafsluiting van het grootboek is uitgevoerd. Hoewel een periode in het boekjaar nog kan open staan, kan de transactie niet worden omgekeerd als het jaarafsluitingsproces voor het boekjaar is uitgevoerd. Het boekjaar heeft een andere status dan de perioden erin.
    - De jaarafsluiting kan ongedaan worden gemaakt. Vervolgens kan de transactie worden omgekeerd. Deze benadering is mogelijk geen optie. Afhankelijk van de status van het boekjaar kan het eenvoudiger zijn handmatig een terugboekingstransactie in een openstaande periode van het afgesloten boekjaar of het volgende boekjaar in te voeren. Als een nieuwe transactie wordt geboekt naar een openstaande periode van het boekjaar waarvoor het jaarafsluitingsproces is uitgevoerd, moet de jaarafsluiting opnieuw worden uitgevoerd.

- Het journaal in de subadministratie is niet overgeboekt naar het grootboek:

    - Deze reden geldt alleen voor vrije-tekstfacturen.
    - Gebruik de pagina **Nog niet overgeboekte journaalposten in subadministratie** om de invoer over te boeken naar het grootboek. De vrije-tekstfactuur kan vervolgens worden omgekeerd of gecorrigeerd als de correctiefunctionaliteit is ingeschakeld.

- Vereffening:

    - De transactie (zoals een factuur of betaling) wordt vereffend of gemarkeerd voor vereffening.

        - U kunt controleren of een transactie is vereffend of gemarkeerd voor vereffening door **Vereffeningen weergeven** of **Vereffening \> Vereffeningshistorie** op de pagina **Klanttransacties** te selecteren.
        - U kunt een vereffening ook omkeren via de pagina **Klanttransacties** (**Vereffening \> Vereffening ongedaan maken**) als een van de transacties moet worden omgekeerd.

- De transactie bevat meer dan één subboektransactie die is ingevoerd met hetzelfde boekstuknummer (probleem met één boekstuk).
- De factuur is niet goedgekeurd:

    - Als het selectievakje **Goedkeuring** niet is ingeschakeld op de factuur, kan de factuur niet worden omgekeerd.

        - In dit geval verwijst goedkeuring niet naar goedkeuringen in het werkstroomproces, maar naar de optie **Goedkeuring** op de boekstukregels. Deze optie wordt gebruikt om te voorkomen dat een factuur wordt betaald. Hoewel deze optie meestal wordt gebruikt in Crediteuren, is deze ook beschikbaar voor klantfacturen die via journalen worden ingevoerd.

- De transactie heeft een bovenliggende factuur die is gecorrigeerd (Indiase lokalisatie).
- De transactie bevat een klantrekening, maar wordt omgekeerd via een onjuiste pagina, zoals de pagina **Transacties voor \<main account\>**:

    - Zoals deze reden al suggereert, kunnen sommige grootboektransacties alleen via specifieke pagina's worden omgekeerd, zelfs als de functie Massaal omkeren is ingeschakeld.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Typen transacties die niet kunnen worden omgekeerd

De volgende typen transacties kunnen niet worden omgekeerd:

- Herwaardering van vreemde valuta:

    - In tegenstelling tot herwaarderingen van vreemde valuta in Grootboek kunnen herwaarderingen van vreemde valuta in Klanten en Crediteuren niet worden omgekeerd. In plaats daarvan moet de herwaardering opnieuw worden uitgevoerd op basis van de factuurdatum. In dit geval wordt bij de herwaardering de wisselkoers van de datum van de factuur gebruikt en worden niet-gerealiseerde winsten of verliezen in feite op 0 (nul) gezet. Het resultaat lijkt dus op het resultaat van het terugdraaien van de vorige herwaardering. Hetzelfde bedrag wordt echter niet omgekeerd als de standaardwisselkoers op de factuur is gewijzigd.

- Een transactie met gecorrigeerde bronbelasting
- Klantfactuur voor verkooporder:

    - Er moet een creditnota of retour worden gemaakt om de transactie om te keren. Zie [Verkoopretouren](../../supply-chain/warehousing/sales-returns.md) voor informatie over het maken van de terugboekingstransactie.

- Wissel
- Kassatransactie
- Geavanceerde correctie
- Rentenota
- Aanmaning
- Bankkredietbrief
- Verzending exporteren
- Journaal voor opbrengsttoerekening:

    - Wanneer u opbrengst toerekent via het journaal voor opbrengsttoerekening, worden de boekstukken naar grootboekrekeningen geboekt. Daarom worden ze weergegeven alsof het alleen grootboekposten zijn. Deze posten kunnen niet worden omgekeerd omdat het opbrengstschema niet opnieuw wordt geopend om de opbrengst opnieuw toe te rekenen.

## <a name="cash-and-bank-management"></a>Contanten en bankbeheer

Met verschillende transactietypen wordt de subboeking van de bank bijgewerkt via het algemene journaal. Voorbeelden zijn leveranciersbetalingen, klantbetalingen en bankoverboekingen.

Als de functie voor massaal omkeren is uitgeschakeld, kunnen transacties afzonderlijk worden omgekeerd via de pagina **Bankrekeningen** voor cheques of stortingen of de pagina **Klantrekeningen** voor klantbetalingen.

Als de functie Massaal omkeren is ingeschakeld, kunnen een of meer betalingstransacties ook worden omgekeerd via de pagina **Boekstuktransacties** en vanuit het journaal waaruit de transacties zijn geboekt. Stortingen kunnen echter nog steeds alleen vanaf de bankrekening worden omgekeerd. Daarnaast kunnen banktransacties nog steeds niet worden omgekeerd via de pagina **Transacties voor \<main account\>** voor het grootboek. Deze kunnen wel worden omgekeerd via de pagina **Boekstuktransacties**.

Sommige transacties kunnen niet worden omgekeerd. Voorbeelden zijn elektronische leveranciersbetalingen.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Redenen waarom transacties niet kunnen worden omgekeerd

Transacties kunnen om de volgende redenen niet worden omgekeerd:

- De boekperiode staat in de wachtstand of is definitief afgesloten:

    - Als de omkeringsdatum zich in een boekperiode bevindt die niet is geopend, kan de transactie niet worden omgekeerd.
    - Als de transactie de invoer van een terugboekingsdatum ondersteunt, kan de transactie nog worden teruggeboekt door de terugboekingsdatum in een openstaande periode te wijzigen.

- Het jaarafsluitingsproces voor het grootboek is uitgevoerd:

    - De boekingsdatum van de transactie valt in een boekjaar waarvoor een jaarafsluiting van het grootboek is uitgevoerd. Hoewel een periode in het boekjaar nog kan open staan, kan de transactie niet worden omgekeerd als het jaarafsluitingsproces voor het boekjaar is uitgevoerd. Het boekjaar heeft een andere status dan de perioden erin.
    - De jaarafsluiting kan ongedaan worden gemaakt. Vervolgens kan de transactie worden omgekeerd. Deze benadering is mogelijk geen optie. Afhankelijk van de status van het boekjaar kan het eenvoudiger zijn handmatig een terugboekingstransactie in een openstaande periode van het afgesloten boekjaar of het volgende boekjaar in te voeren. Als een nieuwe transactie wordt geboekt naar een openstaande periode van het boekjaar waarvoor het jaarafsluitingsproces is uitgevoerd, moet de jaarafsluiting opnieuw worden uitgevoerd.

- Vereffening:

    - De transactie (betaling) wordt vereffend of gemarkeerd voor vereffening.

        - U kunt controleren of een transactie is vereffend of gemarkeerd voor vereffening door **Vereffeningen weergeven** of **Vereffening \> Vereffeningshistorie** op de pagina **Leverancierstransacties** of **Klanttransacties** te selecteren.
        - U kunt een vereffening ook omkeren via de pagina **Leverancierstransacties** of **Klanttransacties** (**Vereffening \> Vereffening ongedaan maken**) als een van de transacties moet worden omgekeerd.

- De transactie bevat meer dan één subboektransactie die is ingevoerd met hetzelfde boekstuknummer (probleem met één boekstuk).
- Overbruggingstransacties:

    - Als de transactie is gerelateerd aan een overbruggingsbetaling, kan deze niet worden omgekeerd.
    - Als de overbruggingsbetaling moet worden omgekeerd, moet de betaling eerst worden overgeboekt van de overbruggingsrekening naar de bank. De betaling kan vervolgens worden omgekeerd, mits deze voldoet aan de andere validatiecriteria.

- De transactie bevat een bankrekening, maar wordt omgekeerd via de pagina **Transacties voor \<main account\>** of vanuit een onjuiste subadministratie, zoals Klanten of Crediteuren:

    - Zoals deze reden al suggereert, kunnen sommige grootboektransacties alleen via specifieke pagina's worden omgekeerd, zelfs als de functie Massaal omkeren is ingeschakeld.

- Herwaardering van vreemde valuta van bank:

    - De herwaardering van vreemde valuta van de bank kan worden omgekeerd. Het is echter mogelijk dat omkering niet mogelijk is als u de omkeringsstappen niet in chronologische volgorde voltooit. Als u de herwaardering in maart en april hebt omgekeerd, kan de herwaardering van maart bijvoorbeeld pas worden omgekeerd als de herwaardering van april is omgekeerd.

### <a name="types-of-transactions-that-cant-be-reversed"></a>Typen transacties die niet kunnen worden omgekeerd

De volgende typen transacties kunnen niet worden omgekeerd:

- Leveranciersbetalingen die zijn gedaan als elektronische betalingen
- Promessen
- Wissel

## <a name="fixed-assets"></a>Vaste activa

De subadministratie voor vaste activa wordt bijgewerkt met verschillende transactietypen. Voorbeelden zijn verwervingen en afschrijving.

Als de functie Massaal omkeren is uitgeschakeld, kunnen transacties afzonderlijk worden omgekeerd via de pagina **Leverancierstransacties**, vanaf de pagina **Vaste-activatransacties**, of via Activa leasen, afhankelijk van het transactietype.

Als de functie Massaal omkeren is ingeschakeld, kunnen een of meer vaste-activatransacties ook worden omgekeerd via de pagina **Boekstuktransacties** in het journaal waaruit de transacties zijn geboekt.

### <a name="reasons-why-transactions-cant-be-reversed"></a>Redenen waarom transacties niet kunnen worden omgekeerd

Transacties kunnen om de volgende redenen niet worden omgekeerd:

- De boekperiode staat in de wachtstand of is definitief afgesloten:

    - Als de omkeringsdatum zich in een boekperiode bevindt die niet is geopend, kan de transactie niet worden omgekeerd.
    - Als de transactie de invoer van een terugboekingsdatum ondersteunt, kan de transactie nog worden teruggeboekt door de terugboekingsdatum in een openstaande periode te wijzigen.

- Het jaarafsluitingsproces voor het grootboek is uitgevoerd:

    - De boekingsdatum van de transactie valt in een boekjaar dat is afgesloten in Grootboek. Hoewel een periode in het boekjaar nog kan open staan, kan de transactie niet worden omgekeerd als het jaarafsluitingsproces voor het boekjaar is uitgevoerd. Het boekjaar heeft een andere status dan de perioden erin.
    - De jaarafsluiting kan ongedaan worden gemaakt. Vervolgens kan de transactie worden omgekeerd. Deze benadering is mogelijk geen optie. Afhankelijk van de status van het boekjaar kan het eenvoudiger zijn handmatig een terugboekingstransactie in een openstaande periode van het afgesloten boekjaar of het volgende boekjaar in te voeren. Als een nieuwe transactie wordt geboekt naar een openstaande periode van het boekjaar waarvoor het jaarafsluitingsproces is uitgevoerd, moet de jaarafsluiting opnieuw worden uitgevoerd.

- Verwervingen:

    - Als de verwerving is uitgevoerd via een leveranciersfactuur voor inkooporders, moet de omkering worden uitgevoerd door een creditnota voor leveranciers in te stellen. Zie [Een inkoopretourorder maken](../../supply-chain/procurement/tasks/create-purchase-return-order.md) voor meer informatie over het invoeren van de terugboekingstransactie.
    - De verwerving is uitgevoerd via een projecttransactie.
    - De verwerving kan niet worden omgekeerd als de afschrijving voor het activum is geboekt. De afschrijving moet worden omgekeerd voordat de aanschaf kan worden omgekeerd.
    - Als de status van het waardemodel of afschrijvingsboek voor een vast activum niet is geopend, kan de transactie niet worden omgekeerd.

- Afstotingen:

    - De afstoting wordt uitgevoerd via een vrije-tekstfactuur:

        - De correctie van een vrije-tekstfactuur wordt geblokkeerd als deze een vast activum bevat. Als het activum echter via een journaal wordt afboekt, kan de vrije-tekstfactuur worden omgekeerd via de vaste-activarecord.

    - Als de status van het waardemodel of afschrijvingsboek voor een vast activum niet is geopend, kan de transactie niet worden omgekeerd.

- Afschrijving:

    - De afschrijving **kan** worden omgekeerd als de volgende afschrijving ook wordt geboekt. U ontvangt echter een waarschuwing omdat deze benadering geen best practice is.
    - Als de status van het waardemodel of afschrijvingsboek voor een vast activum niet is geopend, kan de transactie niet worden omgekeerd.

- Er bestaan transacties (of omgekeerde transacties) voor een bepaald activum en activaboek voor de transactiedatum of later van het boekstuk.
- De transactie bevat een activumrekening, maar wordt omgekeerd via de pagina **Transacties voor \<main account\>** of vanuit een onjuiste subadministratie, zoals Klanten of Crediteuren:

    - Zoals deze reden al suggereert, kunnen sommige grootboektransacties alleen via specifieke pagina's worden omgekeerd, zelfs als de functie Massaal omkeren is ingeschakeld.
    - Als een werving plaatsvindt via een leveranciersfactuur voor niet-inkooporders of een leveranciersfactuurjournaal, kan deze alleen worden omgekeerd via de pagina **Leverancierstransacties** in Leveranciers.
    - Als een activum wordt verworven via de Activa leasen, kan dit worden omgekeerd via de pagina **Transacties verplichtingen** in Activa leasen.
