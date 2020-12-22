---
title: Uitgestelde opbrengst toerekenen
description: Dit onderwerp bevat informatie over de functie voor opbrengsttoerekening.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: ace1d00ec25a57b26b1858369c32d9134a380977
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458774"
---
# <a name="recognize-deferred-revenue"></a>Uitgestelde opbrengst toerekenen

[!include [banner](../includes/banner.md)]

> [!NOTE]
> De functie voor opbrengsttoerekening kan niet worden ingeschakeld via Functiebeheer. Momenteel moet u configuratiesleutels gebruiken om deze functie in te schakelen.

In dit onderwerp wordt het proces beschreven voor het toerekenen van de opbrengst in het schema voor opbrengsttoerekening. Nadat een factuur voor een verkooporder is geboekt, wordt een schema voor opbrengsttoerekening gemaakt voor elke verkooporderregel waarvoor een opbrengstschema bestaat. Het opbrengstschema op een regel wordt gebruikt om te bepalen of voor de regel de opbrengst moet worden uitgesteld.

## <a name="view-revenue-recognition-schedule-details"></a>Details van het schema voor opbrengsttoerekening weergeven

Er zijn twee manieren om toegang te krijgen tot de details van het schema voor opbrengsttoerekening.

- U kunt het schema voor opbrengsttoerekening rechtstreeks vanuit een gefactureerde verkooporder openen. In dit geval wordt de informatie in het opbrengstschema gefilterd, zodat alleen de details voor de geselecteerde verkooporder worden weergegeven. Deze benadering is handig wanneer u de details van het schema voor een verkooporder wilt valideren.
- U kunt het schema voor opbrengsttoerekening openen via de pagina **Opbrengsttoerekening \> Periodieke taken**. Deze benadering wordt vaak gebruikt wanneer de opbrengst wordt toegerekend aan het einde van een periode. Wanneer de pagina voor het eerst wordt geopend, bevat deze geen gegevens. Gebruik de filters boven het raster om criteria te definiëren voor de schemadetails die moeten worden weergegeven. U kunt filteren op de factuurdatums door een datumbereik, verkooporder, klant, project-id of staat in te voeren.

[![Pagina met opbrengstschema's](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)

Het sneltabblad **Financiële dimensie** onder het raster bevat de financiële dimensies van de verkooporderregel. Deze dimensies werden in aanmerking genomen toen er naar uitgestelde opbrengst werd geboekt. Ze worden ook in aanmerking genomen als de opbrengst wordt toegerekend. Welke dimensiewaarden worden gebruikt, is afhankelijk van de rekeningstructuur die is toegewezen aan de hoofdrekeningen voor de opbrengst en uitgestelde opbrengst.

## <a name="recognize-revenue"></a>Opbrengst toerekenen

U kunt de opbrengst toerekenen door het proces **Journaal maken** uit te voeren via de pagina **Opbrengst toerekenen**. U kunt deze pagina openen vanuit de verkooporder of via **Periodieke taken**. Als het proces vanuit de verkooporder wordt uitgevoerd, wordt alleen de opbrengst voor de geselecteerde verkooporder toegerekend. Meestal wordt het proces echter vanuit **Periodieke taken** uitgevoerd, zodat de opbrengsten voor alle geboekte verkooporderfacturen worden toegerekend.

Als u de criteria voor het selecteren en boeken van opbrengst wilt definiëren, selecteert u **Journaal maken** om het dialoogvenster **Journaal maken** te openen.

[![Opties voor het maken van journaalparameters](./media/revenue-recognition-create-journal.png)](./media/revenue-recognition-create-journal.png)

Gebruik in het dialoogvenster de opties in de veldgroep **Verwerkingsdatum** om de boekingsdatum te definiëren die wordt gebruikt als de opbrengst wordt toegerekend. Als u **Geselecteerde datum** selecteert, kunt u een boekingsdatum invoeren in het veld **Transactiedatum**. Als u de **Datum opbrengstschema** selecteert, wordt de transactiedatum niet gebruikt. In plaats daarvan wordt de waarde in het veld **Toerekeningsdatum** op elke regel van het schema als de boekingsdatum gebruikt.

Voer vervolgens in het veld **Begindatum** datum de "vanaf"-datum in waar vanaf de opbrengst moet worden toegerekend. Alle regels in het schema waarvan de toerekeningsdatum op of vóór de "vanaf"-datum valt, worden toegerekend, op voorwaarde dat ze niet in de wachtstand staan.

Nadat u de datums hebt gedefinieerd, selecteert u **OK** in het dialoogvenster om het journaal te maken. Er wordt een bericht met informatie weergegeven met daarin het aantal transacties dat is gemaakt en het journaal waarin ze zijn gemaakt. Het journaal wordt niet automatisch geboekt. Dat geeft de manager voor opbrengsttoerekening de tijd om te valideren welke regels van het schema worden toegerekend.

Nadat het proces is uitgevoerd, worden de regels op het schema die naar het journaal zijn overgeboekt, als **Verwerkt** gemarkeerd. De vlag **Verwerkt** geeft aan dat de regels naar het journaal zijn overgeboekt, maar dat ze kunnen worden geboekt of de boeking ongedaan kan worden gemaakt. Nadat het journaal voor opbrengsttoerekening is geboekt, blijft de vlag **Verwerkt** staan. Als het journaal voor opbrengsttoerekening wordt verwijderd of als een regel wordt verwijderd, wordt de vlag **Verwerkt** verwijderd. Op die manier kan de regel worden toegerekend wanneer het proces **Journaal maken** opnieuw wordt uitgevoerd.

[![Pagina met opbrengsttoerekeningsschema's](./media/revenue-recognition-rev-recog-schedule-02.png)](./media/revenue-recognition-rev-recog-schedule-02.png)

Op de pagina **Journaal voor opbrengsttoerekening** (**Opbrengsttoerekening \> Journaalboekingen \> Journaal voor opbrengsttoerekening**) opent u **Regels** om de details weer te geven van wat er wordt toegerekend. Er wordt altijd een afzonderlijke transactie gemaakt voor elke regel in het schema die wordt toegerekend, zelfs als alle regels op dezelfde datum worden geboekt en daarvoor dezelfde grootboekrekeningen zijn gebruikt.

[![Pagina Journaalboekstuk](./media/revenue-recognition-journal-voucher.png)](./media/revenue-recognition-journal-voucher.png)

In de kolom **Rekening** wordt de grootboekrekening voor uitgestelde opbrengst weergegeven. Deze grootboekrekening kan niet worden bewerkt. Deze beperking helpt te garanderen dat de juiste grootboekrekening voor uitgestelde opbrengst wordt vrijgegeven. Deze grootboekrekening wordt niet gevalideerd ten opzichte van de rekeningstructuur, omdat deze kan zijn gewijzigd sinds er voor de laatste keer boekingen naar de grootboekrekening voor uitgestelde opbrengst hebben plaatsgevonden.

In de kolom **Tegenrekening** wordt de grootboekrekening voor opbrengst weergegeven. De grootboekrekening voor opbrengst wordt standaard overgenomen uit voorraadboekingsprofielen en de financiële dimensies worden opgehaald uit de verkooporderregel. Deze grootboekrekening wordt gecontroleerd op basis van de huidige rekeningstructuur. Deze kan echter worden bewerkt als de rekeningstructuur is gewijzigd en extra financiële dimensies zijn vereist.

Het standaardbedrag is afkomstig uit de overeenkomstige regel in het schema en kan niet worden gewijzigd.

Als de verkooporder er een is met meerdere valuta's, wordt de wisselkoers standaard ingesteld op de wisselkoers van de factuur. Op deze manier weet u zeker dat de bedragen in de valuta voor boekhouding en de aangiftevaluta volledig in mindering worden gebracht. Vanwege afrondingsverschillen kan de wisselkoers voor de laatste regel in het schema enigszins verschillen van de koers op de factuur.

Nadat het journaal voor opbrengsttoerekening is geboekt, wordt het boekstuk in het schema ingevoerd. Als er meerdere boekstukken voor dezelfde regel van het schema voorkomen, wordt er een sterretje (\*) op de regel weergegeven. Als u de boekstukken wilt weergeven die voor die regel zijn geboekt, selecteert u **Boekstuktransacties**.

## <a name="modify-the-revenue-recognition-schedule-details"></a>Details van het schema voor opbrengsttoerekening wijzigen

De meeste gegevens in de details van het opbrengstschema kunnen niet worden bewerkt. Er kunnen geen nieuwe regels aan het schema worden toegevoegd en bestaande regels kunnen niet worden verwijderd. De details van het opbrengstschema moeten voor elke verkooporderregel moeten worden onderhouden om er zeker van te kunnen zijn dat een organisatie door de tijd heen hetzelfde bedrag toerekent als het bedrag dat is uitgesteld.

### <a name="edit-schedule-lines"></a>Schemaregels bewerken

Sommige bewerkingen zijn toegestaan op de regels van het schema. De volgende velden kunnen op de regels worden gewijzigd:

- **In wachtstand**: deze vlag kan worden ingesteld of uitgeschakeld voordat de regel wordt verwerkt. Als u de vlag wilt wissen, selecteert u de rij en selecteert u **Wachtstand verwijderen**. Opbrengst kan niet worden toegerekend voor regels die in de wachtstand staan. Regels kunnen automatisch in de wachtstand worden geplaatst als het opbrengstschema is ingesteld om met automatische wachtstanden te kunnen werken.

    [![Opbrengstschema's - schemaregels bewerken](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)

- **Toerekeningsdatum**: de toerekeningsdatum kan worden gewijzigd voordat de regel wordt verwerkt. Wanneer het proces waarmee het journaal voor toerekenen van de opbrengst wordt uitgevoerd, wordt een datum ingevoerd in het veld **Begindatum toerekening**. Deze datum wordt vergeleken met de datum in het veld **Toerekeningsdatum** om te bepalen welke regels moeten worden toegekend.
- **Vrij te geven bedrag**: het bedrag dat wordt vrijgegeven kan worden gewijzigd voordat de regel wordt verwerkt. U kunt het toegerekende bedrag van opbrengsten verlagen, maar u kunt het niet verhogen. Dit veld stelt een organisatie in staat om een deel van de opbrengst op de toerekeningsdatum toe te rekenen. Als het bedrag wordt gewijzigd, geeft het bedrag in het veld **Resterend bedrag** weer hoeveel opbrengst nog moet worden toegerekend.
- **Hoeveelheid voor vrijgave**: als het opbrengstschema voor één voorval of één maand is ingesteld, wordt in het veld **Hoeveelheid voor vrijgave** de hoeveelheid voor de verkooporderregel weergegeven. Dit veld kan ook worden bewerkt en biedt een andere manier om een deel van de opbrengst toe te rekenen. Als de hoeveelheid op de regel bijvoorbeeld 5 is, kunt u de hoeveelheid overschrijven zodat deze kleiner is dan 5. Het bedrag in het veld **Vrij te geven bedrag** wordt proportioneel bijgewerkt.

### <a name="update-contract-terms"></a>Contractvoorwaarden bijwerken

De details van het opbrengstschema worden gemaakt op basis van het opbrengstschema dat is toegewezen aan de verkooporderregel op het moment dat de factuur wordt geboekt. Als het opbrengstschema op de verkooporderregel onjuist is, kan deze niet worden gewijzigd op de verkooporder nadat de verkoop order is gefactureerd. In plaats daarvan moet u de knop **Contract voorwaarden bijwerken** gebruiken om het opbrengstschema te wijzigen. Het opbrengstschema kan worden gewijzigd voor- of nadat de opbrengst is toegerekend.

Als u het schema wilt wijzigen, selecteert u in het schema de regel voor het artikel dat u wilt wijzigen. In de volgende afbeelding is de regel voor artikel S0008 geselecteerd die is geboekt met een opbrengstschema van 12 maanden. Als u **Contractvoorwaarden bijwerken** selecteert, wordt een dialoogvenster weergegeven met daarin de begin- en einddatums, evenals het opbrengstschema.

[![Begin- en einddatum contract](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)

Wijzig de begin- en einddatum van het contract zodat deze het juiste datumbereik weergeven. Wanneer u het datumbereik wijzigt, moet de waarde in het veld **Aantal voorvallen** overeenkomen met een opbrengstschema dat in het systeem is gedefinieerd. In dit voorbeeld moet er een opbrengstschema van 24 maanden worden ingesteld omdat het contract is gewijzigd in een overeenkomst van 24 maanden. Omdat het opbrengstschema van 24 maanden bestaat, wordt dit standaard ingevoerd en kan het contract worden gewijzigd. Als er geen opbrengstschema met een overeenkomend aantal voorvallen bestaat, kan het contract niet worden gewijzigd. Nadat u de contractvoorwaarden en het opbrengstschema hebt bijgewerkt, selecteert u **OK** in het dialoogvenster om uw wijzigingen op te slaan.

[![Bijgewerkt datumbereik voor contract](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)

De wijzigingen in het contract hebben de volgende effecten op de details van het opbrengstschema:

- Als er geen opbrengsten voor het product zijn toegerekend, worden alle eerdere schemadetails verwijderd en vervangen door de nieuwe opbrengstschemadetails. Voor artikel S0008 kwamen oorspronkelijk 12 regels bij de schemadetails voor. Deze 12 regels worden verwijderd en op basis van het nieuwe opbrengstschema vervangen door 24 regels.
- Als de opbrengst voor het product is toegerekend, is een deel van de opbrengst onjuist toegerekend omdat de toerekening werd gebaseerd op het onjuiste opbrengstschema. Die regels moeten worden teruggeboekt en opnieuw toegerekend op basis van het nieuwe schema. In dit scenario worden er nieuwe regels voor het opbrengstschema gemaakt waarvoor negatieve bedragen op de oorspronkelijke toerekeningsdatum voorkomen. Vervolgens worden er nieuwe regels gemaakt om de bedragen toe te rekenen op basis van het nieuwe opbrengstschema. Op 8 augustus 2019 hebt u bijvoorbeeld een opbrengst van € 10,53 toegerekend. Op 8 september 2019 hebt u een opbrengst van € 13,16 toegerekend. Daarom worden er twee nieuwe regels gemaakt op dezelfde datums. Eén regel is voor -€ 10,53 en de andere regel is voor -€ 13,16. Er worden vierentwintig nieuwe regels gemaakt en de totale uitgestelde opbrengst van € 160,61 wordt aan al deze regels toegewezen. U kunt de terugboekingsregels boeken door het proces **Journaal maken** uit te voeren.

[![Opbrengsttoerekeningsschema](./media/revenue-recognition-rev-recog-schedule-03.png)](./media/revenue-recognition-rev-recog-schedule-03.png)
