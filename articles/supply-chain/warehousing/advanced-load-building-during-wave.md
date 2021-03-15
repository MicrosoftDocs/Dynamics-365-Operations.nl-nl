---
title: Geavanceerde ladingopbouw tijdens een wave
description: Dit onderwerp bevat informatie over het geavanceerde opbouwen van de wave-lading waarmee automatisch zendingen worden toegewezen aan bestaande waves tijdens het uitvoeren van de wave. Zo kunt u zinvolle ladingen maken die vrachtwagens voorstellen zonder dat u de werkbank voor ladingplanning hoeft te gebruiken.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod,WHSWaveTemplateTable,WHSLoadMixGroup,WHSLoadBuildTemplate, WHSWaveTableListPage, TMSLoadBuildTemplateApply, TMSLoadBuildTemplates, TMSLoadBuildTemplateCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: e4abe1a03997853053f60c750199874a61fc68c0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006386"
---
# <a name="advanced-load-building-during-wave"></a>Geavanceerde ladingopbouw tijdens een wave

[!include [banner](../includes/banner.md)]

Bij het geavanceerde opbouwen van de wave-lading worden automatisch zendingen toegewezen aan bestaande waves tijdens het uitvoeren van de wave. Zo kunt u zinvolle ladingen maken die vrachtwagens voorstellen zonder dat u de werkbank voor ladingplanning hoeft te gebruiken. Deze functionaliteit is nuttig voor bedrijven die het begrip van ladingen willen gebruiken om de zending van goederen in een vrachtwagen te volgen en te plannen, maar die deze ladingen niet elke dag handmatig willen maken.

Tijdens de wave-verwerking wordt in het systeem gewoonlijk een nieuwe lading gemaakt voor elke zending waaraan geen lading is toegewezen. Wanneer echter de functie voor geavanceerde ladingopbouw is ingeschakeld, wijst het systeem elke niet-toegewezen zending toe aan een bestaande lading (als een geschikte lading bestaat) en worden nieuwe ladingen alleen gemaakt wanneer deze nodig zijn. Bij de geavanceerde ladingopbouw worden de nieuwe ladingen automatisch gemaakt op basis van de criteria die u opgeeft.

Om de functie te gebruiken, moet u het systeem als volgt configureren:

- Maak *Wave-sjablonen* die de nieuwe methode **buildLoads** bevatten. Met deze methode komt de geavanceerde ladingopbouw beschikbaar voor waves die die sjablonen gebruiken.
- Configureer *ladingopbouwsjablonen* die elk zijn gekoppeld aan een bepaalde wave-sjabloon en methode. Met ladingopbouwsjablonen wordt aangestuurd aan welke lading (bestaande of nieuwe) de ladingsregels worden toegevoegd die in de wave worden verwerkt. U kunt zendingen combineren of splitsen op basis van criteria zoals de ladingssjabloon, apparatuur en andere veldwaarden op de ladingregel.
- Definieer *gemengde ladingsgroepen* om aan te sturen welke artikelen wel of niet in één lading mogen worden gecombineerd. U kunt ook opgeven of de beperking een waarschuwing of een fout moet veroorzaken en of de volumetrische beperking van de ladingssjabloon moet worden geëvalueerd.

## <a name="turn-on-advanced-wave-load-building-in-your-system"></a>Geavanceerde ladingopbouw inschakelen in uw systeem

Voordat u geavanceerd wave-ladingopbouw kunt gebruiken, moeten twee functies zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van deze functies te controleren en deze zo nodig in te schakelen. In het werkgebied **Functiebeheer** worden de functies als volgt vermeld:

- Functie voor waveladingopbouw:

    - **Module:** *Magazijnbeheer*
    - **Functienaam:** *Functie voor het maken van waveladingen*

- Organisatiebrede wave-stapcode inschakelen:

    - **Module:** *Magazijnbeheer*
    - **Functienaam:** *Organisatiebrede wave-stapcode*

### <a name="make-sample-data-available"></a>Voorbeeldgegevens beschikbaar maken

Als u deze scenario's wilt doorlopen met de hier opgegeven voorbeeldrecords en -waarden, moet u een systeem gebruiken waarop de standaard [demogegevens](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) zijn geïnstalleerd. U moet daarnaast ook de rechtspersoon **USMF** selecteren voordat u begint.

U kunt deze demo ook gebruiken als instructie voor het gebruik van deze functie wanneer u met een productiesysteem werkt. In dat geval moet u echter uw eigen waarden vervangen en hebt u mogelijk niet de beschikking over bepaalde typen vereiste records die met de standaard demogegevens worden verstrekt.

### <a name="make-sure-that-the-scenario-setup-includes-enough-available-inventory"></a>Controleren of in de scenarioconfiguratie voldoende voorhanden voorraad is opgenomen

Als u werkt met de **USMF-** voorbeeldgegevens, moet u eerst controleren of uw systeem zo is geconfigureerd dat op elke relevante locatie voldoende voorraad aanwezig is. Voor deze demo wordt er vanuit gegaan dat de volgende voorraad beschikbaar is in magazijn *62*:

- **Artikel A0001:** 10 stuks
- **Artikel A0002:** 10 stuks
- **Artikel M9200:** 10 losse eenheden

Artikel **M9200** moet aan het magazijn worden toegevoegd. Voer de procedures in de volgende subsecties uit om de artikelvoorraad toe te voegen.

#### <a name="create-a-new-license-plate-id"></a>Een nieuwe nummerplaat-id maken

1. Ga naar **Magazijnbeheer** \> **Instellingen** \> **Magazijn** \> **Nummerplaten**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer op de nieuwe regel in het veld **Nummerplaat** de waarde *LP6203* in.
1. Selecteer **Opslaan**.

#### <a name="create-a-standard-cost-for-item-m9200-in-site-6"></a>Maak een standaardkostprijs voor artikel M9200 op site 6

1. Ga naar **Productgegevensbeheer** \> **Producten** \> **Vrijgegeven producten**.
1. Zoek naar **M9200**.
1. Selecteer de rij voor het artikel en selecteer vervolgens in het actievenster op het tabblad **Kosten beheren** in de groep **Instellen** de waarde **Artikelprijs**.
1. Selecteer op de pagina **Artikelprijs** het tabblad **Prijzen in behandeling**.
1. Selecteer **Nieuw** in het actievenster.
1. Stel op de nieuwe regel de volgende waarden in:

    - **Kostprijsberekeningstype:** *Geplande kosten*
    - **Prijstype:** *Kosten*
    - **Versie:** *10*
    - **Locatie:** *6*
    - **Prijs:** *1,60*

1. Selecteer **Opslaan** in het actievenster.
1. Selecteer in het actievenster de optie **Prijzen in behandeling activeren**.
1. Selecteer het tabblad **Actieve prijzen** om te controleren of de nieuwe kostprijs voor site *6* is toegevoegd.

#### <a name="create-inventory-in-warehouse-62"></a>Voorraad in magazijn 62 maken

1. Ga naar **Voorraadbeheer** \> **Journaalboekingen** \> **Artikelen** \> **Voorraadcorrectie**.
1. Selecteer **Nieuw** in het actievenster.
1. Ga naar het dialoogvenster **Voorraadjournaal maken** op het sneltabblad **Overzicht** en voer in het veld **Magazijn** de waarde *62* in. Accepteer de standaardwaarden in alle overige velden.
1. Selecteer **OK** om het dialoogvenster te sluiten.
1. De pagina **Voorraadcorrectie** wordt geopend. Selecteer op het sneltabblad **Journaalregels** de optie **Nieuw** om een nieuwe regel te maken.
1. Stel op de nieuwe regel de volgende waarden in. Accepteer de standaardwaarden in alle overige velden.

    - **Artikelnummer:** *M9200*
    - **Locatie:** *bulk-003*
    - **Hoeveelheid:** wijzig de waarde in *10*.

1. Selecteer **Opslaan** in het actievenster.
1. Selecteer in het actievenster de optie **Valideren** om te zien of er fouten zijn.
1. Selecteer in het dialoogvenster **Journaal controleren** de optie **OK** om de controle te starten. U ontvangt een melding wanneer de controle is voltooid.
1. Selecteer in het actievenster de optie **Boeken** om de voorraadcorrectie door te voeren.
1. Selecteer in het dialoogvenster **Journaal boeken** de optie **OK** om het boekingsproces te starten. U ontvangt een melding wanneer het boeken is voltooid.

## <a name="set-up-advanced-wave-load-building"></a>Geavanceerde waveladingopbouw configureren

### <a name="regenerate-wave-process-methods"></a>Waveverwerkingsmethoden opnieuw genereren

Mogelijk moet u uw waveverwerkingsmethoden opnieuw genereren om de methode voor ladingopbouw (**buildLoads**) beschikbaar te maken.

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Waves** \> **Methoden voor verwerking van waves**.
2. Controleer of **buildLoads** in de lijst staat. Als deze niet aanwezig is, selecteert u **Methoden opnieuw genereren** in het actievenster om deze toe te voegen.

### <a name="set-up-wave-templates"></a>Wavesjablonen instellen

Als u wilt profiteren van de voordelen van geavanceerde wave-ladingopbouw, moet u de methode **buildLoads** opnemen in elke relevante [wave-sjabloon](tasks/configure-wave-processing.md).

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Waves** \> **Wavesjablonen**.
1. Selecteer een wavesjabloon.

    Als u werkt met de **USMF**-voorbeeldgegevens, selecteert u de sjabloon **62 Shipping Default**.

1. Selecteer in het actievenster de optie **Bewerken** om de pagina in de bewerkingsmodus te openen.
1. Selecteer op het sneltabblad **Methoden** in het raster **Resterende methoden** de methode **buildLoads**.
1. Selecteer de knop pijl-rechts om de methode **buildLoads** te verplaatsen naar het raster **Geselecteerde methoden**.
1. Als u een waarde van **Wavestapcode** wilt toewijzen aan de methode **buildLoads**, moet u eerst een code maken op de pagina **Wavestapcodes**. U kunt elke gewenste waarde gebruiken, maar u moet deze wel even noteren omdat u deze later nog nodig hebt. Volg deze stappen om de code **WSC2112** te maken:

    1. Klik in de rij voor de methode **buildLoads** met de rechter muisknop op de pijl-omlaag in het veld **Wavestapcode** en selecteer **Details weergeven**.
    1. Ga naar de pagina **Wavestapcodes** en selecteer in het actievenster de optie **Nieuw**.
    1. Voer in het veld **Wavestapcode** de tekst *WSC2112* in.
    1. Voer in het veld **Beschrijving wavestap** de tekst *WSC2112* in.
    1. Selecteer in het veld **Wavestaptype** de optie *Lading opbouwen*.

1. Selecteer **Opslaan** en sluit de pagina.
1. Selecteer in de rij voor de methode **buildLoads** in het veld **Wavestapcode** de code die u zojuist hebt gemaakt (**WSC2112**).
1. Selecteer **Opslaan** in het actievenster.

> [!NOTE]
> Wavestapcodes zijn codes die gebruikers kunnen instellen en gebruiken om specifieke instanties van wavemethoden aan bijbehorende sjablonen te koppelen. De sjablonen bevatten sjablonen voor aanvulling, containers, afdrukken van etiketten, lading opbouwen en sorteren.
>
> Wanneer er geen wave-stapcodes worden gebruikt, moeten gebruikers vrije tekst invoeren om naar een bepaalde sjabloon te verwijzen vanuit het wave-methode-exemplaar. Vrije tekst is gevoelig voor fouten, omdat gebruikers ervoor moeten zorgen dat de tekst met de wavestap die zij toevoegen voor een specifieke wavestapmethode in een wavesjabloon exact overeenkomt met de tekst van de wavestap in de doelsjabloon.
>
> Wave-stapcodes voor een specifiek wave-staptype worden ingesteld op een afzonderlijke pagina. Voor elke instantie van een wavestapmethode in een wavesjabloon waarvoor een wavestapcode moet worden gebruikt, moet de wavestapcode worden geselecteerd in een vervolgkeuzelijst. De selectie in een vervolgkeuzelijst vervangt vrije tekstinvoer en vermindert het risico en de impact van de menselijke fout. Met instellingscodes wordt een wave-stapmethode in een wave-sjabloon gekoppeld aan een doelsjabloon voor de methode.

### <a name="set-up-load-mix-groups"></a>Gemengde ladingsgroepen instellen

Met gemengde ladingsgroepen stelt u regels in voor de typen artikelen die in één lading kunnen worden gecombineerd. U kunt zo veel gemengde ladingsgroepen instellen als nodig. Voor het gebruik van geavanceerde waveladingopbouw moet u echter ten minste één maken. Volg deze stappen om een gemengde ladingsgroep te maken:

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Containers** \> **Gemengde ladingsgroep**.
1. Selecteer in het actievenster **Nieuw** om een ladingsgroep te maken.
1. Voer in het veld **Id gemengde ladingsgroep** een naam in voor de nieuwe groep.

    Als u werkt met de **USMF**-voorbeeldgegevens, stelt u de volgende waarden in:

    - **Id gemengde ladingsgroep:** *TV*
    - **Beschrijving:** *TV*

1. Selecteer in het actievenster de optie **Opslaan** om het sneltabblad **Criteria voor gemengde ladingsgroepen** beschikbaar te maken.
1. Selecteer op het sneltabblad **Criteria voor gemengde ladingsgroepen** de optie **Nieuw** om een rij toe te voegen aan het raster.
1. Stel in de nieuwe rij in elk veld de gewenste waarden in. Deze waarden bepalen de artikelengroepen die in aanmerking komen voor de gemengde lading.

    Als u werkt met de **USMF**-voorbeeld gegevens, selecteert u *TV & video* in het veld **Artikelgroep**.

1. Selecteer in het actievenster de optie **Opslaan** om het sneltabblad **Beperkingen voor gemengde ladingsgroepen** beschikbaar te maken.
1. Selecteer op het sneltabblad **Beperkingen voor gemengde ladingsgroepen** de optie **Nieuw** om een rij toe te voegen aan het raster.
1. Stel in de nieuwe rij in elk veld de gewenste waarden in.

    Als u werkt met de **USMF**-voorbeeldgegevens, stelt u de volgende waarden in:

    - **Artikelgroep:** *CarAudio*
    - **Ladingopbouwactie:** *Beperken* (deze waarde voorkomt dat artikelen die horen tot de artikelengroep **CarAudio** aan dezelfde lading worden toegevoegd als de artikelen die deel uitmaken van de artikelengroep **TV & video**.)

1. Ga verder met de regels totdat u alle criteria en beperkingen hebt toegevoegd die u nodig hebt voor de gemengde ladingsgroep.

Als u werkt met de **USMF**-voorbeeldgegevens, hebt u deze configuratie nu voltooid.

### <a name="set-up-load-build-templates"></a>Ladingopbouwsjablonen instellen

U kunt zo veel ladingopbouwsjablonen instellen als nodig. Voor het gebruik van geavanceerde waveladingopbouw moet u echter ten minste één maken. Volg deze stappen om een ladingopbouwsjabloon te maken.

1. Ga naar **Magazijnbeheer** \> **Instellen** \> **Aanvulling** \> **Waveladingopbouwsjablonen**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster.
1. Stel in de nieuwe rij de volgende waarden in.

    | Veld | Omschrijving | Waarde in de USMF-voorbeeldgegevens |
    |---|---|---|
    | Volgnummer | De volgorde waarin de sjabloon wordt geëvalueerd. | *1* |
    | Naam van ladingopbouwsjabloon | Voer de unieke id van de ladingopbouwsjabloon in. U moet de naam invoeren van de sjabloon die u eerder in deze instellingen hebt gemaakt of bijgewerkt. | *62 Shipping Default* |
    | Stapcode wave | Voer de wavestapcode in waarmee de sjabloon wordt gekoppeld aan een wavemethode. U moet de code invoeren die u voor de methode **buildLoads** hebt geselecteerd toen u eerder in deze procedure de wavesjabloon hebt geconfigureerd. | *WSC2112* |
    | Ladingssjabloon-id | Selecteer de ladingssjabloon waarmee nieuwe ladingen worden gemaakt en waarmee wordt vergeleken bij het toewijzen van bestaande ladingen. De ladingssjabloon definieert het maximale gewicht en volume dat voor de gehele lading is toegestaan. | *Standaardladingssjabloon* |
    | Apparatuur | De apparatuur waartegen wordt afgestemd bij het toewijzen van bestaande ladingen en die wordt ingevuld bij nieuw gemaakte ladingen. | Laat dit veld leeg. |
    | Id gemengde ladingsgroep | Selecteer de gemengde ladinggroep die wordt gebruikt als het artikel is toegestaan in de lading. Met de gemengde ladinggroep stelt u regels in voor de typen artikelen die in één lading kunnen worden gecombineerd. U moet een van de gemengde groepen selecteren die u eerder in deze configuratie hebt gemaakt. | *TV* |
    | Openstaande ladingen gebruiken | Geef aan of bestaande openstaande ladingen moeten worden toegevoegd. De volgende opties zijn beschikbaar:<ul><li>**Geen**: Voeg geen openstaande landingen toe aan bestaande ladingen.</li><li>**Elke**: Openstaande ladingen worden toegevoegd aan bestaande ladingen die geldig zijn voor de regel.</li><li>**Toegewezen**: Openstaande ladingen worden toegevoegd aan de lading die is toegewezen aan de wave.</li></ul> | *Elke* |
    | Ladingen maken | Geef op of nieuwe ladingen moeten worden gemaakt als geen bestaande lading aan de criteria voldoet. | Geselecteerd (= *Ja*) |
    | Splitsen van verzendregel toestaan | Geef op of een enkele ladingregel kan worden gesplitst over meerdere ladingen als deze groter is dan de maximale capaciteit van de ladingssjabloon. | Uitgeschakeld (= *Nee*) |
    | Volumemaatstaven valideren | Geef op of ladingopbouw het gewicht en het volume moet controleren wanneer een ladingregel wordt toegevoegd, om ervoor te zorgen dat de volumelimieten van de ladingssjabloon in acht worden genomen. | Uitgeschakeld (= *Nee*) |

1. Selecteer in het actievenster de optie **Opslaan** om de optie **Query bewerken** beschikbaar te maken.
1. Selecteer in het actievenster de optie **Query bewerken** om een dialoogvenster te openen waarin u de query kunt bewerken.
1. Selecteer in het dialoogvenster op het tabblad **Sorteren** de optie **Toevoegen** om een rij aan het raster toe te voegen.
1. Definieer in de nieuwe rij de sorteerregels die u wilt gebruiken. Stel bijvoorbeeld de volgende waarden in om de zoekresultaten in oplopende volgorde te sorteren op ordernummer:

    - **Tabel:** *Gegevens lading*
    - **Afgeleide tabel:** *Gegevens lading*
    - **Veld:** *Ordernummer*
    - **Zoekrichting:** *Oplopend*

1. Selecteer **OK** om de wijzigingen op te slaan en het dialoogvenster te sluiten.
1. Stel op het sneltabblad **Opbreken op** regels in om te bepalen hoe u de lading wilt laten opsplitsen. Normaal gesproken kunt u opbreken op aangepaste velden die zijn uitgebreid naar de ladingregel, zoals **Route**, **Tour** of **Uitvoeren**. Als u bijvoorbeeld één lading per ordernummer wilt maken, schakelt u het selectievakje **Opbreken op** in voor de rij met de volgende waarden:

    - **Naam verwijzingstabel:** *Gegevens lading*
    - **Naam verwijzingsveld:** *Ordernummer*

## <a name="scenario"></a>Scenario's

In dit scenario wordt toegelicht hoe de instellingen die eerder in dit onderwerp zijn beschreven, van invloed zijn op magazijnbewerkingen terwijl een verkooporder wordt verwerkt. In dit scenario worden de **USMF**-voorbeeldgegevens gebruikt, samen met andere voorbeeldwaarden die in de configuratie-instructies zijn opgenomen.

### <a name="create-sales-orders"></a>Verkooporders maken

1. Ga naar **Verkoop en marketing** \> **Verkooporders** \> **Alle verkooporders**.
1. Selecteer in het actievenster de optie **Nieuw** om het dialoogvenster **Verkooporder maken** te openen.
1. Stel in het dialoogvenster de volgende waarden in:

    - Stel op het sneltabblad **Klant** het veld **Klantaccount** in op *US-007*.
    - Stel op het sneltabblad **Algemeen** het veld **Magazijn** in op *62*.

1. Selecteer **OK** om het dialoogvenster te sluiten en de verkooporder te maken.
1. De nieuwe verkooporder wordt geopend. Deze moet een nieuwe, lege regel bevatten in het raster op het sneltabblad **Verkooporderregels**. Stel op deze nieuwe regel het veld **Artikelnummer** in op *A0001* en het veld **Hoeveelheid** op *1*.
1. Selecteer in het menu **Voorraad** boven het raster de waarde **Reservering**.
1. Ga naar de pagina **Reservering** en selecteer in het actievenster de optie **Partij reserveren**.
1. Klik op de knop **Sluiten** (**X**) in de rechterbovenhoek van de pagina om terug te gaan naar de verkooporder.
1. Selecteer in het actievenster op het tabblad **Magazijn** in de groep **Acties** de optie **Vrijgeven aan magazijn**. Het systeem maakt een zending aan en voegt deze toe aan een nieuwe lading, omdat geen bestaande lading de laadregels met dit ordernummer bevat.

    U ontvangt informatieve berichten waarin het werk, de wave en de zending worden vermeld die voor deze order zijn gemaakt.

1. Om de details van de lading, de zending en het werk te bevestigen op de verkoopregel, selecteert u de regel en selecteert u in het menu **Magazijn** boven het raster de optie **Gegevens lading**, **Details van zending** of **Werkdetails**.
1. Selecteer in de verkooporder die u zojuist hebt gemaakt op het sneltabblad **Verkooporderregels** de optie **Regel toevoegen** om nog een regel toe te voegen.
1. Stel op de nieuwe regel het veld **Artikelnummer** in op *A0002* en het veld **Hoeveelheid** op *1*.
1. Herhaal regels 6 tot en met 9 om de regel te reserveren en vrij te geven naar het magazijn. Het systeem maakt een **nieuwe** zending aan voor de regel die u hebt toegevoegd. Omdat u echter gebruik maakt van geavanceerde waveladingopbouw, voegt het systeem deze zending en ladingregel toe aan de bestaande wave. Als u geen gebruik maakt van geavanceerde waveladingopbouw, zou het systeem een nieuwe lading maken voor de zending.
1. Selecteer in de verkooporder die u zojuist hebt gemaakt op het sneltabblad **Verkooporderregels** de optie **Regel toevoegen** om nog een regel toe te voegen.
1. Stel op de nieuwe regel het veld **Artikelnummer** in op *M9200* en het veld **Hoeveelheid** op *1*.
1. Herhaal regels 6 tot en met 9 om de regel te reserveren en vrij te geven naar het magazijn. Net zoals eerder maakt het systeem een **nieuwe** zending aan voor de regel die u hebt toegevoegd. Maaromdat het artikel afkomstig is van de artikel groep **CarAudio**, **kan het niet de beperkingen doorgeven die u hebt ingesteld voor de gemengde ladingsgroep**. Daarom wordt deze **toegevoegd aan een nieuwe lading**. Als u geen gemengde ladingsgroep had opgegeven op de ladingsopbouwsjabloon, zou deze zending zijn toegevoegd aan de eerste lading.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]