---
title: Voorraadwaardenrapporten
description: In dit artikel wordt uitgelegd hoe u voorraadwaardenrapporten instelt, genereert en gebruikt. Deze rapporten geven informatie over de fysieke en financiële hoeveelheden en bedragen in uw voorraad.
author: JennySong-SH
ms.date: 08/05/2022
ms.topic: article
ms.search.form: InventValueProcess, InventValueReportSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: f97b5bd228c6f769438d50bb27950b8d8fbda3e8
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334920"
---
# <a name="inventory-value-reports"></a>Voorraadwaardenrapporten

[!include [banner](../includes/banner.md)]

Voorraadwaardenrapporten geven informatie over de fysieke en financiële hoeveelheden en bedragen in uw voorraad. U kunt de rapporten op verschillende manieren bekijken. U kunt bijvoorbeeld totalen of transacties weergeven, of filteren op artikelen of een tijdbereik. U kunt de waarden van de kosten van verkochte goederen (COGS) of van het onderhanden werk (OHW) bekijken, en andere opties instellen.

Met voorraadwaardenrapporten kunt u de volgende taken uitvoeren:

- Afstemming uitvoeren tussen het grootboek en de voorraad.
- De beschikbare voorraad en waarden voor een bepaalde periode raadplegen.
- Rapportconfiguraties maken die op een specifiek doel zijn afgestemd.
- Rapportconfiguraties opslaan, zodat ze meerdere keren kunnen worden gebruikt.
- Bereiken toevoegen om gegevens te filteren wanneer u een rapport uitvoert.

## <a name="types-of-inventory-value-report"></a>Typen voorraadwaardenrapporten

Er zijn twee soorten voorraadwaardenrapporten: **Voorraadwaarde** (het standaardrapport) en **Opslag voorraadwaardenrapport**.

### <a name="standard-inventory-value-report"></a>Standaard voorraadwaardenrapport

Het standaard **Voorraadwaardenrapport** is een eenvoudig rapport, waarin u de informatie kunt kiezen die erin wordt opgenomen, en dat die informatie vervolgens op het scherm toont. Het slaat de resultaten niet op. Het biedt ook geen interactieve mogelijkheden om te filteren, in te zoomen, te bladeren of te exporteren. Om deze redenen raden wij u aan om in de meeste gevallen in plaats daarvan het **Opslag voorraadwaardenrapport** te gebruiken.

### <a name="inventory-value-report-storage-report"></a>Een Opslag voorraadwaardenrapport exporteren

Het rapport **Opslag voorraadwaardenrapport** levert uitvoer op, hetzij als een interactieve pagina in Microsoft Dynamics 365 Supply Chain Management, hetzij als een geëxporteerd document in een van de verschillende indelingen.

Bij het bekijken van het rapport in uw browser worden kolommen en samengevoegde balansen dynamisch aangepast, afhankelijk van de indeling die u hebt geconfigureerd. U kunt de resultaten sorteren, filteren, details van de gegevens bekijken en nog veel meer.

Rapportresultaten worden opgeslagen in de gegevensentiteit **Voorraadwaarde**. Daarom kunt u de resultaten filteren en exporteren naar een indeling zoals door komma's gescheiden waarden (CSV) of de Microsoft Excel-indeling.

Het rapport **Opslag van voorraadwaardenrapport** is handig wanneer de uitvoer veel regels bevat. U hebt bijvoorbeeld 50.000 artikelen en er zijn 300 winkels gemaakt als magazijnen. Als u in dit geval voorraadeindsaldi opvraagt per artikel, locatie en magazijn, bevat de uitvoer veel regels.

> [!NOTE]
> In het rapport **Opslag van voorraadwaardenrapport** worden geen subtotalen opgenomen die zijn gedefinieerd in de rapportindeling. Ook bevat deze optie geen grootboeksaldi, zelfs wanneer deze saldi zijn gedefinieerd in de rapportindeling. U moet de afstemming in het grootboek uitvoeren met behulp van proefbalansen. Het standaardrapport **Voorraadwaarde** bevat echter wel deze subtotalen en saldi.

## <a name="turn-the-inventory-value-report-storage-feature-on-or-off"></a>De functie Opslag voorraadwaardenrapport in- of uitschakelen

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.25 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management versie 10.0.29 is de functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.29 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Opslag voorraadwaardenrapport* in de werkruimte [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="define-inventory-value-report-configurations"></a><a name="report-configuration"></a>Configuraties van het voorraadwaardenrapport definiëren

Gebruik de pagina **Voorraadwaardenrapporten** om de inhoud in te stellen die in de verschillende soorten voorraadwaardenrapporten wordt opgenomen. U kunt elk gewenst aantal rapporttypen definiëren. Telkens wanneer u een van beide typen voorraadwaardenrapporten genereert, kiest u een rapporttype.

1. Ga naar **Cost Management \> Instelling voor boekhoudingbeleid voorraad \> Voorraadwaardenrapporten**.
1. Volg één van deze stappen:

    - Als u een bestaand rapport wilt bewerken, selecteert u dit in het lijstdeelvenster en selecteert u **Bewerken** in het actievenster.
    - Selecteer in het actievenster **Nieuw** om een nieuw rapport te maken.

1. Stel in de koptekst van het nieuwe of geselecteerde rapport de volgende velden in:

    - **Id**: voer een korte id in voor het rapport. Deze waarde moet uniek zijn voor alle configuraties van voorraadwaardenrapporten. Deze kan niet meer worden bewerkt nadat u een nieuwe configuratie hebt opgeslagen.
    - **Naam**: voer een beschrijvende naam in voor het rapport.

1. Als u een nieuwe rapportconfiguratie maakt, selecteert u **Opslaan** in het actievenster om de resterende velden beschikbaar te maken.
1. Stel op het sneltabblad **Algemeen** de volgende velden in:

    - **Datuminterval**: selecteer een vooraf gedefinieerd datuminterval. U kunt dit datuminterval overschrijven wanneer u het rapport uitvoert.
    - **Bereik**: selecteer *Boekingsdatum* of *Transactietijd*, afhankelijk van de datum en tijd die moeten worden gebruikt wanneer records worden opgehaald voor het rapport.
    - **Dimensieset**: selecteer de set dimensies om de gegevens voor uit te voeren. (De dimensies worden gedefinieerd in het grootboek.) U kunt bijvoorbeeld de gegevens uitvoeren voor *Hoofdrekening* of *Hoofdrekening + Bedrijfseenheid*. De dimensieset die u selecteert, mag niet meer dan twee dimensies hebben. Zie voor meer informatie het onderwerp [Financiële dimensiesets](../../finance/general-ledger/financial-dimension-sets.md).

1. Stel op het sneltabblad **Kolommen** de volgende velden in. Deze velden bepalen welke kolommen uw rapport bevat, en de gegevenstypen die deze kolommen bevatten.

    - **Voorraad**: stel deze optie in op *Ja* om de voorraadwaarden weer te geven. U kunt deze waarden vervolgens afstemmen op de grootboekrekeningsaldi.
    - **OHW**: stel deze optie in op *Ja* om de OHW-waarden weer te geven. U kunt deze waarden vervolgens afstemmen op de OHW-rekeningsaldi in het grootboek. Wanneer u deze optie hebt ingesteld op *Ja*, worden in het rapport alleen de fysieke hoeveelheden en bedragen van de voorraad met de status OHW weergegeven. Productieorders met de status OHW zijn gepicked of gereed gemeld, maar nog niet beëindigd.
    - **Uitgestelde COGS**: stel deze optie in op *Ja* om een kolom weer te geven met de fysieke hoeveelheden en bedragen van de voorraad voor uitgestelde COGS. Uitgestelde COGS worden weergegeven met fysieke hoeveelheden en bedragen, omdat deze pakbonhoeveelheden en -bedragen compenseren.
    - **COGS**: stel deze optie in op *Ja* om een kolom weer te geven met de financiële hoeveelheden en bedragen voor COGS. COGS worden weergegeven met financiële hoeveelheden en bedragen, omdat deze factuurhoeveelheden en -bedragen compenseren.
    - **Winst en verlies**: stel deze optie in op *Ja* als u een kolom wilt weergeven met het financiële bedrag dat is geboekt naar de verlies-en-winstrekeningen voor de voorraad.
    - **Cumulatieve rekeningwaarden afdrukken voor vergelijking**: stel deze optie in op *Ja* om een kolom weer te geven waarin het saldo van de grootboekrekening wordt weergegeven. Op deze manier hoeft u de proefbalans niet te controleren. Deze optie werkt alleen met het standaard **Voorraadwaardenrapport**, niet met het rapport **Opslag voor voorraadwaardenrapport**. Nadat u deze optie op *Ja* hebt ingesteld, moet u de volgende velden gebruiken om elke grootboekrekening op te geven die u wilt vermelden, afhankelijk van de opties voor **Financiële positie** die u hebt ingeschakeld.

        > [!NOTE]
        > Als u een *totaal* rekening selecteert voor een van deze velden, wordt zowel het bedrag van elke voorraadrekening die in de totaalrekening is opgenomen als het bedrag van de totaalrekening weergegeven.

        - **Voorraadrekening**: geef de grootboekrekening op waar voorraadgegevens voor moeten worden vermeld. (Zowel de optie **Voorraad** als de optie **Cumulatieve rekeningwaarden afdrukken ter vergelijking** moeten op *Ja* zijn ingesteld).
        - **OHW-rekening**: geef de grootboekrekening op waar de OHW-gegevens voor moeten worden vermeld. (Zowel de optie **OHW** als de optie **Cumulatieve rekeningwaarden afdrukken ter vergelijking** moeten op *Ja* zijn ingesteld).
        - **Uitgestelde COGS-rekening**: geef de grootboekrekening op waar de uitgestelde COGS-gegevens voor moeten worden vermeld. (Zowel de optie **Uitgestelde COGS** als de optie **Cumulatieve rekeningwaarden afdrukken ter vergelijking** moeten op *Ja* zijn ingesteld).
        - **COGS-rekening**: geef de grootboekrekening op waar de COGS-gegevens voor moeten worden vermeld. (Zowel de optie **COGS** als de optie **Cumulatieve rekeningwaarden afdrukken ter vergelijking** moeten op *Ja* zijn ingesteld).

    - **Fysieke en financiële waarden samenvatten**: stel deze optie in op *Ja* om een kolom weer te geven met de totale voorraadhoeveelheid en het totale voorraadbedrag (een overzicht van zowel fysieke als financiële voorraadwaarden). Als deze optie is ingesteld op *Nee*, geeft het rapport zowel fysieke als financiële voorraadwaarden weer.
    - **Niet naar grootboek geboekt opnemen**: stel deze optie in op *Ja* om een kolom weer te geven met de transacties die nooit naar het grootboek zijn geboekt. Transacties voor de volgende typen artikelen worden mogelijk niet naar het grootboek geboekt:

        - Ontvangen en nog niet gefactureerde artikelen wanneer de optie **Fysieke voorraad boeken** is uitgeschakeld voor de relevante artikelmodelgroep.
        - Ontvangen en nog niet gefactureerde artikelen wanneer de optie **Productontvangstbon in grootboek boeken** is uitgeschakeld op het sneltabblad **Productontvangstbon** op het tabblad **Algemeen** van de pagina **Leveranciersparameters** (**Leveranciers \> Instellingen \> Leveranciersparameters**).

    - **Gemiddelde eenheidskosten** berekenen: stel deze optie in op *Ja* als u een kolom met de gemiddelde eenheidskosten wilt weergeven. De gemiddelde eenheidskosten is het totale bedrag gedeeld door de totale hoeveelheid.
    - **Totale hoeveelheid en waarde**: stel deze optie in op *Ja* om kolommen weer te geven met de totale hoeveelheid fysieke voorraad (en financiële hoeveelheden) en de totale hoeveelheid fysieke voorraad (en financiële bedragen). U kunt deze optie alleen op *Ja* instellen als de optie **Fysieke en financiële waarden samenvatten** is ingesteld op *Nee*.
    - **Voorraaddimensies**: schakel in dit raster het selectievakje **Weergeven** in voor elke dimensie die u in het rapport wilt weergeven. Alleen dimensies waarin de optie **Financiële voorraad** is ingeschakeld, geven waarden weer in het rapport. Andere dimensies geven alleen lege kolommen weer. Voor de dimensies die u selecteert om weer te geven, kunt u het selectievakje **Totaal** inschakelen om ook totalen op te nemen.
    - **Resource-id**: stel de optie **Weergeven** in op *Ja* om een kolom weer te geven waarin het artikel voor elke rij wordt aangegeven. Stel de optie **Totaal** in op *Ja* als u ook totalen wilt opnemen. Afhankelijk van het type artikel dat in elke rij wordt vermeld, bevat de kolom een van de volgende typen informatie:

        - **Materiaal**: de kolom geeft de `ItemID`-veldwaarde voor de relevante materiaalrecord weer.
        - **Arbeid**: de kolom geeft de `WorkCenterID`-veldwaarde voor de relevante arbeidsrecord weer.
        - **Indirecte kosten**: de kolom geeft de `CodeID`-veldwaarde voor de relevante kostenrecord weer.

        Als de optie **Weergeven** is ingesteld op *Nee* voor zowel het veld **Resource-id** als het veld **Resourcegroep**, wordt alleen een totale voorraadwaarde weergeven die is gebaseerd op de voorraaddimensie die u hebt geselecteerd.

    - **Resource-groep**: stel de optie **Weergeven** in op *Ja* om een kolom weer te geven waarin de resourcegroep voor elke rij wordt aangegeven. Stel de optie **Totaal** in op *Ja* als u ook totalen wilt opnemen. Afhankelijk van het type artikel dat in elke rij wordt vermeld, bevat de kolom een van de volgende typen informatie:

        - **Materiaal**: de kolom geeft de `ItemGroup`-veldwaarde voor de relevante materiaalrecord weer.
        - **Arbeid**: de kolom geeft de `WorkcenterGroup`-veldwaarde voor de relevante arbeidsrecord weer.
        - **Indirecte kosten**: de kolom geeft de `CostGroup`-veldwaarde voor de relevante kostenrecord weer. (De `CostGroupType`-waarde moet *indirect* zijn.)

        Als de optie **Weergeven** is ingesteld op *Nee* voor zowel het veld **Resource-id** als het veld **Resourcegroep**, wordt alleen een totale voorraadwaarde weergeven die is gebaseerd op de voorraaddimensie die u hebt geselecteerd.

1. Stel op het sneltabblad **Rijen** de volgende velden in. Met deze velden kunt u corresponderende OHW-subsecties aan het rapport toevoegen of verwijderen.

    - **Materiaal**: stel deze optie in op *Ja* om informatie over materialen weer te geven. *Materiaal* is een standaardbrontype omdat materialen in alle rapportconfiguraties moeten worden opgenomen voor betrouwbare uitvoer.
    - **Arbeid**: stel deze optie in op *Ja* om arbeidskosten van OHW weer te geven.
    - **Indirecte kosten**: stel deze optie in op *Ja* om indirecte kosten van OHW weer te geven.
    - **Rechtstreekse uitbesteding**: stel deze optie in op *Ja* om de kosten van rechtstreekse uitbesteding van OHW weer te geven. Deze informatie is nuttig als u werk uitbesteedt.
    - **Detailniveau**: selecteer een weergaveoptie voor het rapport:

        - *Transacties*: alle relevante transacties in het rapport weergeven. Het is mogelijk dat er prestatieproblemen optreden wanneer u rapporten weergeeft die een groot volume aan transacties bevatten. Als u deze weergaveoptie wilt gebruiken, raden we u daarom aan het rapport **Opslag voor voorraadwaardenrapport** te gebruiken.
        - *Totalen*: het totale resultaat weergeven.

    - **Beginsaldo opnemen**: stel deze optie in op *Ja* om het beginsaldo weer te geven. Deze optie is alleen beschikbaar wanneer het veld **Detailniveau** is ingesteld op *Transacties*.

## <a name="generate-an-inventory-value-report-storage-report"></a>Een rapport Opslag voor voorraadwaardenrapport genereren

Volg deze stappen om een rapport **Opslag van voorraadwaardenrapport** te genereren en op te slaan.

1. Ga naar **Kostenbeheer \> Query's en rapporten \> Rapport Opslag van voorraadwaarden**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Voorraadwaarde** op het sneltabblad **Parameters** de volgende velden in:

    - **Naam**: voer een unieke naam in voor het rapport.
    - **Id**: de [configuratie van het voorraadwaardenrapport](#report-configuration) selecteren die voor het rapport moet worden gebruikt. De configuratie legt opties vast voor de kolommen en rijen die in het rapport worden opgenomen.
    - **Datuminterval**: gebruik de velden in deze sectie om te definiëren welke records in het rapport worden opgenomen. Als u het datuminterval wilt definiëren, kunt u een vooraf ingesteld bereik (ten opzichte van de rapportaanmaakdatum) selecteren in het veld **Datumintervalcode** of specifieke datums selecteren in de velden **Begindatum** en **Einddatum**.

1. Stel op het sneltabblad **Op te nemen records** filters en beperkingen in om op te geven welke gegevens u in het rapport wilt opnemen. Selecteer **Filter** om een standaarddialoogvenster voor de query-editor te openen, waarin u selectiecriteria, sorteercriteria en joins kunt definiëren. De velden werken op dezelfde manier als bij andere typen query's in Supply Chain Management. Al deze filters worden toegepast op de voorraadtransacties, maar niet op het grootboeksaldo. Houd dit gedrag in gedachten bij het instellen van de filters. Anders ontstaat er mogelijk een verschil tussen de voorraad en het grootboek.
1. Geef op het sneltabblad **Uitvoeren op de achtergrond** op hoe, wanneer en hoe vaak het rapport wordt gegenereerd. De velden werken op dezelfde manier als bij andere typen [achtergrondtaken](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) in Supply Chain Management.

    > [!NOTE]
    > Dit rapport wordt altijd uitgevoerd als onderdeel van een batchtaak.

1. Selecteer **OK** om de instellingen toe te passen en het dialoogvenster te sluiten.

Nadat de batchtaak is voltooid, wordt het rapport vermeld op de pagina **Rapport opslag van voorraadwaarden**. U moet de pagina mogelijk vernieuwen om het rapport te bekijken.

> [!IMPORTANT]
> In de geselecteerde rapportconfiguratie voor voorraadwaarde wordt er mogelijk een onjuist beginsaldo gevonden als u in zowel het veld **Begindatum** als het veld **Einddatum** dezelfde datum selecteert en als u ook de optie **Beginsaldo opnemen** op *Ja* instelt.

## <a name="explore-an-inventory-value-report-storage-report"></a>Een rapport Opslag voor voorraadwaardenrapport bekijken

Nadat u een rapport hebt gegenereerd, kunt u het op elk gewenst moment weergeven en verkennen met de volgende stappen.

1. Ga naar **Kostenbeheer \> Query's en rapporten \> Rapport Opslag van voorraadwaarden**.
1. Selecteer een rapport in de lijst. De pagina toont de details van de [configuratie voor het voorraadwaardenrapport](#report-configuration) die is gebruikt om het geselecteerde rapport te genereren.
1. Selecteer in het actievenster de optie **Details weergeven** om de inhoud van het rapport weer te geven.
1. Bekijk het rapport door een van de volgende stappen uit te voeren:

    - Net als voor de meeste standaardpagina's in Supply Chain Management, kunt u vrijwel elke kolomkop selecteren om het raster te sorteren of te filteren op de waarden in die kolom.
    - Gebruik het veld **Filteren** om het rapport te filteren op elke waarde in een of meer van de beschikbare kolommen.
    - Gebruik het weergavemenu (boven het veld **Filteren**) om uw favoriete combinaties van sorteer- en filteropties op te slaan en te laden.

## <a name="export-an-inventory-value-report-storage-report"></a>Een rapport Opslag voor voorraadwaardenrapport exporteren

Elk rapport dat u genereert wordt opgeslagen in gegevensentiteit **Voorraadwaarde**. U kunt de standaardfuncties voor gegevensbeheer van Supply Chain Management gebruiken om gegevens van deze entiteit te exporteren naar elke ondersteunde gegevensindeling, inclusief CSV of Excel.

In het volgende voorbeeld ziet u hoe een rapport **Opslag voor voorraadwaardenrapport** wordt geëxporteerd.

1. Ga naar **Systeembeheer \> Werkruimten \> Gegevensbeheer**.
1. Selecteer in de sectie **Importeren/exporteren** de tegel **Exporteren**.
1. Op de pagina **Exporteren** die wordt weergegeven, stelt u de exporttaak in. Voer eerst een groepsnaam voor de taak in.
1. Selecteer **Entiteit toevoegen** in de sectie **Geselecteerde entiteiten**.
1. Stel in het dialoogvenster dat verschijnt de volgende velden in:

    - **Naam entiteit:** selecteer *Voorraadwaarde*.
    - **Indeling doelgegevens**: selecteer de indeling waarnaar u gegevens wilt exporteren.

1. Selecteer **Toevoegen** om de nieuwe rij toe te voegen en selecteer vervolgens **Sluiten** om het dialoogvenster te sluiten.
1. Gewoonlijk exporteert u één rapport tegelijk. Als u één rapport wilt exporteren, stelt u een filter in voor de rij die u zojuist hebt toegevoegd aan het dialoogvenster **Query**. Op deze manier kunt u definiëren welk rapport uit de entiteit **Voorraadwaarde** wordt opgenomen in de export. Volg deze stappen om de volgende filteropties in te stellen om een enkel rapport te exporteren:

    1. Selecteer op het tabblad **Bereik** de optie **Toevoegen** om een rij toe te voegen.
    2. Stel het veld **Tabel** in op *Voorraadwaarde*.
    3. Stel het veld **Afgeleide tabel** in op *Voorraadwaarde*.
    4. Stel het veld **Veld** in op het veld waarop u wilt filteren. Gewoonlijk gebruikt u de velden **Uitvoeringsnaam** en/of **Uitvoeringstijd**.
    5. Stel het veld **Criteria** in op de waarde die u wilt zoeken in het geselecteerde veld. (Als u het veld **Uitvoeringsnaam** in de vorige stap hebt geselecteerd, is deze waarde de naam van het rapport. Als u het veld **Uitvoeringstijd** hebt geselecteerd, wordt dit het tijdstip waarop het rapport is gegenereerd.)
    6. Voeg meer rijen toe aan het tabblad **Bereik** totdat u een unieke identificatie hebt voor het gewenste rapport.

1. Selecteer **OK** om de instellingen op te slaan en het dialoogvenster te sluiten.
1. Selecteer **Opslaan** om de instellingen voor exporteren op te slaan.
1. Selecteer op het tabblad **Exportopties** de optie **Nu exporteren** om het exportbestand te genereren.
1. Op de pagina **Uitvoeringsoverzicht** die wordt geopend, kunt u de status van uw exporttaak en een lijst met entiteiten zien die zijn geëxporteerd. Selecteer de entiteit **Voorraadwaarde** in de sectie **Verwerkingsstatus entiteit** en selecteer vervolgens **Bestand downloaden** om de geëxporteerde gegevens van die entiteit te downloaden.

Zie [Overzicht van Gegevensimport- en exporttaken](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) voor meer informatie over het gebruik van gegevensbeheer voor het exporteren van gegevens.

## <a name="generate-a-standard-inventory-value-report"></a>Een standaard voorraadwaardenrapport genereren

Genereer met de volgende procedure een standaardrapport **Voorraadwaarden**.

1. Ga naar **Cost management \> Query's en rapporten \> Voorraadboekhouding - statusrapporten \> Voorraadwaarde**.
1. Stel in het dialoogvenster **Voorraadwaardenrapport** op het sneltabblad **Parameters** de volgende velden in:

    - **Naam**: voer een unieke naam in voor het rapport.
    - **Id**: de [configuratie van het voorraadwaardenrapport](#report-configuration) selecteren die voor het rapport moet worden gebruikt. De configuratie legt opties vast voor de kolommen en rijen die in uw rapport worden opgenomen.
    - **Datuminterval**: gebruik de velden in deze sectie om te definiëren welke records in het rapport worden opgenomen. Als u het datuminterval wilt definiëren, kunt u een vooraf ingesteld bereik (ten opzichte van de rapportaanmaakdatum) selecteren in het veld **Datumintervalcode** of specifieke datums selecteren in de velden **Begindatum** en **Einddatum**.

1. Stel op het sneltabblad **Op te nemen records** filters en beperkingen in om op te geven welke gegevens u in het rapport wilt opnemen. Selecteer **Filter** om een standaarddialoogvenster voor de query-editor te openen, waarin u selectiecriteria, sorteercriteria en joins kunt definiëren. De velden werken op dezelfde manier als bij andere typen query's in Supply Chain Management.
1. Geef op het sneltabblad **Uitvoeren op de achtergrond** op hoe, wanneer en hoe vaak het rapport wordt gegenereerd. De velden werken op dezelfde manier als bij andere typen [achtergrondtaken](../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) in Supply Chain Management.
1. Selecteer **OK** om de instellingen toe te passen en het dialoogvenster te sluiten. Het rapport wordt weergegeven.

## <a name="reading-inventory-value-reports"></a>Voorraadwaardenrapporten lezen

Deze sectie bevat richtlijnen voor het lezen en begrijpen van een voorraadwaardenrapport.

Supply Chain Management ondersteunt de volgende twee belangrijke concepten die betrekking hebben op de voorraadstatus:

- **Financieel bijgewerkt**: dit concept geeft aan dat de voorraadtransacties al zijn gefactureerd. Voor productieorders geeft dit het einde van een productieorder aan.
- **Fysiek bijgewerkt**: dit concept geeft aan dat de voorraadtransacties nog niet zijn gefactureerd, maar dat ze wel zijn ontvangen of verzonden. Voor productieorders geeft het aan dat materiaal is gepicked of dat de productieorder is gereed gemeld.

Wanneer u deze twee concepten begrijpt, is het eenvoudig om de volgende kolommen in de rapportuitvoer te begrijpen:

- **Voorraad: financiële hoeveelheid**: de hoeveelheid is financieel bijgewerkt.
- **Voorraad: financieel bedrag**: de bedragwaarde van de voorraad die financieel bijgewerkt is.
- **Voorraad: fysieke hoeveelheid geboekt**: de hoeveelheid is fysiek bijgewerkt.
- **Voorraad: fysiek bedrag geboekt**: de bedragwaarde van de voorraad die fysiek bijgewerkt is.
- **Voorraad: fysieke hoeveelheid niet geboekt**: de hoeveelheid die voorraadtransacties heeft, maar die niet naar het grootboek is geboekt. U hebt bijvoorbeeld een artikelmodelgroep waar de opties **Fysieke voorraad boeken** en **Financiële voorraad boeken** zijn uitgeschakeld, en u hebt een artikel dat aan die groep is gekoppeld. Vervolgens maakt u een inkooporder, ontvangt deze en factureert u deze. Als u nu het voorraadwaardenrapport voor het artikel bekijkt, ziet u dat de hoeveelheid en de waarde op de inkooporder worden weergegeven in de kolommen **Voorraad: fysieke hoeveelheid niet geboekt** en **Voorraad: fysiek bedrag niet geboekt**.
- **Voorraad: fysiek bedrag niet geboekt**: u kunt uw rapporten zo instellen dat er niet-geboekte bedragen worden weergegeven. Als u het rapport voor voorraadafstemming gebruikt, moet u deze waarde echter niet gebruiken. Anders wordt het bedrag niet naar het grootboek geboekt.
- **Voorraad: hoeveelheid**: de totale hoeveelheid van alle hoeveelheidskolommen in het rapport.
- **Voorraad: bedrag**: de totale hoeveelheid van alle bedragkolommen in het rapport. Wanneer u voorraadafstemming doet, gebruikt u deze kolom niet als uw rapport de kolom **Voorraad: fysiek bedrag niet geboekt** bevat. In dit geval moet u het bedrag van **Voorraad: fysiek bedrag niet geboekt** uitsluiten van het totale bedrag.
- **Gemiddelde eenheidskosten**: het totale bedraag gedeeld door de totale hoeveelheid.

Doorgaans gebruikt u een voorraadwaardenrapport om de voorraadwaarde en -hoeveelheid weer te geven. Soms worden echter niet alle relevante voorraaddimensies in het rapport opgenomen. Als u de dimensies die u verwacht niet ziet, valideert u de volgende instellingen:

- Bekijk de dimensiegroepen voor het opslaan en volgen van artikelen. Alleen dimensies waarin de optie **Financiële voorraad** is ingeschakeld, kunnen in het rapport worden weergegeven.
- Ga naar **Cost Management \> Instelling voor boekhoudingbeleid voorraad \> Voorraadwaardenrapporten**, selecteer de rapportconfiguratie die u hebt gebruikt om het rapport te genereren, en zorg ervoor dat de vereiste voorraaddimensies zijn geselecteerd in de kolom **Weergeven**.

U hebt bijvoorbeeld een artikel met het artikelnummer *A0001*. In de opslagdimensiegroep is alleen de locatie ingeschakeld voor financiële voorraad. Zowel de locatie als het magazijn zijn ingeschakeld voor fysieke voorraad. In de traceringsdimensiegroep is het batchnummer ingeschakeld voor de fysieke voorraad, maar niet voor financiële voorraad. Vervolgens gebruikt u een rapportconfiguratie waarin de locatie, het magazijn en het batchnummer zijn geselecteerd. Wanneer u het rapport bekijkt, wordt alleen een waarde voor de locatie weergeven. De kolommen voor het magazijn en batchnummer zijn leeg. Zoals dit voorbeeld laat zien, kunnen voorraadwaardenrapporten alleen voorraaddimensies tonen die voor financiële voorraad zijn ingeschakeld.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
