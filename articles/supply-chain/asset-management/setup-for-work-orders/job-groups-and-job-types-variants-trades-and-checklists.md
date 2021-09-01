---
title: Typen, categorieën, varianten, specialismen en controlelijsten voor onderhoudstaken
description: Dit onderwerp beschrijft categorieën van onderhoudstaaktypen en onderhoudstaaktypen, varianten van onderhoudstaaktypen, onderhoudstaakspecialismen en onderhoudscontrolelijsten in Activabeheer.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetJobTypeDefaultForecast, EntAssetJobTrade, EntAssetJobTypeDefaultCopy, EntAssetChecklistVariableValueLookup, EntAssetChecklistTemplateCreate, EntAssetJobVariant, EntAssetJobTypeDefaultReference, EntAssetJobTypeDefaultChecklist, EntAssetJobTypeDefault, EntAssetJobType, EntAssetJobTypeDefaultChecklistCopy, EntAssetChecklistTemplate, EntAssetJobTypeDefaultDescription, EntAssetJobTypeLookup, EntAssetJobTypeDefaultToolCopy, EntAssetJobTypePreviewPart, EntAssetJobTypeDefaultTool, EntAssetJobTypeDefaultForecastCopy, EntAssetChecklistTemplateLookup, EntAssetJobGroup, EntAssetChecklistVariable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 54bd489a3c9be5be298ef75893b7acad38104a1379d20f853dd700635a3e058e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742795"
---
# <a name="maintenance-job-types-categories-variants-trades-and-checklists"></a>Typen, categorieën, varianten, specialismen en controlelijsten voor onderhoudstaken

[!include [banner](../../includes/banner.md)]

Aan elk activum wordt een activatype gekoppeld. Activatypen bepalen de typen onderhoudstaken (en dus ook de onderhoudstaken) die op activa kunnen worden uitgevoerd. Wanneer u een werkorder maakt, moet u een onderhoudstaak selecteren. Op een activum kunt u alleen de typen onderhoudstaken selecteren die zijn gedefinieerd voor het activumtype dat voor het activum is ingesteld.

Zie [Functionele locaties en activa](../overview/functional-locations-and-objects.md) voor een grafisch overzicht van de typen activa en onderhoudstaken en de verbinding met werkorders.

Varianten van types onderhoudstaak kunnen worden ingesteld voor een type onderhoudstaak. Varianten van het type onderhoudstaak definiëren variaties van een taaktype, zoals grootten (klein, normaal of groot), perioden (wekelijks, tweewekelijks, één maand of drie maanden) en configuraties (laag standaard, flexibel of hoge prestaties).

Onderhoudstaakspecialismen bieden informatie over professionele specialismen, zoals mechanische, elektrische en hydraulische onderhoudstaakspecialismen. Competentie vereistenkunnen worden ingesteld voor een onderhoudstaakspecialisme. Alle onderhoudstaakspecialismen kunnen worden gebruikt met betrekking tot alle types onderhoudstaken. De selectie van een typevariant onderhoudstaak en/of onderhoudstaakspecialisme op een werkorder is optioneel.

Voor elk type onderhoudstaak kunnen variaties van de instellingen van het type onderhoudstaak worden gemaakt. Als u bijvoorbeeld een type onderhoudstaak hebt met de naam **Service**, kunt u de volgende variaties voor dat type onderhoudstaak maken **Vrachtwagen 30.000km**, **Auto´s 30.000 km** en **Bestelwagens 30.000 km**.

Categorieën voor types onderhoudstaken worden gebruikt om een groep onderhoudstaaktypen te verzamelen voor overzichtsdoeleinden. Voorbeelden van categorieën voor types onderhoudstaken kunnen zijn **Kalibratie**, **Inspectie**, **Revisie** en **Instrumentatie**.

Sjablonen voor onderhoudscontrolelijsten en variabelen voor onderhoudscontrolelijsten worden gebruikt om onderhoudscontrolelijsten in te stellen. Onderhoudscontrolelijsten worden ingesteld voor typen onderhoudstaken en worden gebruikt voor werkorders.

Eerst stelt u de vereiste categorieën van onderhoudstaaktypen, varianten van onderhoudstaaktype en onderhoudstaakspecialismen in. U maakt vervolgens onderhoudstaaktypen. Tot slot maakt u op de pagina **Standaardwaarden van onderhoudstaaktypen** alle variaties van onderhoudstaaktypen die zijn vereist voor uw apparatuur. Op deze pagina kunt u ook prognoses, onderhoudscontrolelijsten en hulpmiddelen instellen voor een combinatie van onderhoudstaaktypen.

> [!NOTE]
> Een onderhoudstaaktype kan aan slechts één categorie onderhoudstaaktype zijn gerelateerd.

## <a name="create-a-maintenance-job-type-category"></a>Een categorie onderhoudstaaktype maken

1. Selecteer **Activabeheer** \> **Instellingen** \> **Taken** \> **Categorieën Onderhoudstaaktypen**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Categorie Onderhoudstaaktype** een id in voor de categorie onderhoudstaaktype.
4. Voer in het veld **Naam** een naam in.

    Nadat u de categorieën onderhoudstaaktypen hebt gekoppeld aan onderhoudstaaktypen, wordt in het veld **Taaktypen** het aantal typen onderhoudstaken weer gegeven die zijn gerelateerd aan deze categorie van het type onderhoudstaak.

![Pagina met categorieën voor onderhoudstaaktypen.](media/01-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type-variant"></a>Een variant onderhoudstaaktype maken

1. Selecteer **Activabeheer** \> **Instellingen** \> **Taken** \> **Varianten onderhoudstaaktypen**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Variant onderhoudstaaktype** een id in voor de variant onderhoudstaaktype.
4. Voer in het veld **Beschrijving** een beschrijving in.
5. Selecteer in het Sneltabblad **Onderhoudstaaktype** **Toevoegen** type onderhoudstaak toe te voegen.
6. Selecteer in het veld **Type onderhoudstaak** het type onderhoudstaak.
7. Herhaal stap 5 tot en met 6 om meer typen onderhoudstaken toe te voegen aan de variant van het type onderhoudstaak.

    Op het Sneltabblad **Details** toont het veld **Taaktypen** het aantal typen onderhoudstaken dat is toegevoegd aan de variant van het type onderhoudstaak.

![Pagina met varianten voor onderhoudstaaktypen.](media/02-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-trade"></a>Maak een specialisme onderhoudstaak aan

1. Selecteer **Activabeheer** \> **Instellingen** \> **Taken** \> **Specialisme onderhoudstaak**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Specialisme** een id in voor het onderhoudstaakspecialisme.
4. Voer in het veld **Beschrijving** een beschrijving in.
5. Selecteer in het tabblad **Vaardigheden** de optie **Toevoegen** om een nieuwe kwalificatie toe te voegen die gerelateerd moet worden aan het onderhoudstaakspecialisme/
6. Selecteer de vaardigheid in het veld **Vaardigheid**.
7. Selecteer het niveau in het veld **Niveau**.
8. Herhaal stap 5 tot en met 7 om meer kwalificaties toe te voegen aan het onderhoudstaakspecialisme.

    In het Sneltabblad **Details** toont het veld **Vaardigheden** het aantal vaardigheden dat is toegevoegd aan dit onderhoudstaakspecialisme.

9. Selecteer in het Sneltabblad **Certificaten** **Toevoegen** om een certificaat aan het onderhoudstaakspecialisme toe te voegen.
10. Selecteer in het veld **Certificaattype** het certificaat.
11. Herhaal stap 9 tot en met 10 om meer certificaten toe te voegen aan het onderhoudstaakspecialisme.

    In het Sneltabblad **Details** toont het veld **Certificaten** het aantal certificaten dat is toegevoegd aan dit onderhoudstaakspecialisme.

![Pagina met specialisme onderhoudstaak.](media/03-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-variable"></a>Een variabele onderhoudscontrolelijst maken

Wanneer u regels voor onderhoudscontrolelijsten maakt in het standaard onderhoudstaaktype, moet u een type onderhoudscontrolelijst selecteren. **Variabele** is één type onderhoudscontrolelijst. Deze wordt gebruikt om een mogelijk resultaat te definiëren in een bereik op een onderhoudscontrolelijstregel die is gekoppeld aan een werkorderregel. Met een variabele kunt u een set vooraf gedefinieerde uitkomsten maken zonder een exacte meting te hoeven maken.

**Voorbeeld 1** : u kunt het oliepeil meten door drie waarden te definiëren: **Peil te hoog**, **Peil te laag** en **Peil binnen bereik**. Voor elke waarde definieert u of het resultaat van de waarde **Geslaagd**, **Mislukt** of **Geen** is.

**Voorbeeld 2:** U doet een visueel onderzoek van een apparaat om slijtage te beoordelen.

1. Selecteer **Activabeheer** \> **Instellen** \> **Onderhoudscontrolelijsten** \> **Variabelen onderhoudscontrolelijsten**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Variabele** een id in voor de variabele onderhoudscontrolelijsten.
4. Voer in het veld **Naam** een naam in.
5. Selecteer op Sneltabblad **Algemeen** de optie **Toevoegen** om een regel voor een variabele toe te voegen.

    In het veld **Regelnummer** wordt automatisch een volgnummer voor de regel ingevoerd. Nadat u alle regels hebt toegevoegd, kunt u de regelnummers wijzigen zoals u dat nodig hebt. Wanneer u regel selecteert en vervolgens op de toets **Pijl-omlaag** drukt, wordt het volgende nummer in de reeks automatisch op de volgende regel ingevoerd.

6. Voer een beschrijving voor de waarde in het veld **Waarde** in.
7. Selecteer een resultaat voor de regel in het veld **Resultaat**.

![Pagina met variabelen voor onderhoudscontrolelijst.](media/04-setup-for-work-orders.png)

## <a name="create-a-maintenance-checklist-template"></a>Een sjabloon voor een onderhoudscontrolelijst maken

Sjablonen voor onderhoudscontrolelijsten kunnen worden gebruikt als algemene set taken die een werknemer moet uitvoeren om een werkorder correct te voltooien. Naar de sjablonen wordt verwezen vanuit regels van onderhoudscontrolelijsten in het standaard type onderhoudstaak. U kunt naar sjablonen verwijzen via meerdere standaardregels voor typen onderhoudstaken . U kunt een set algemene taken in de onderhoudscontrolelijst dus eenvoudig opnieuw gebruiken. Voorbeelden van sjablonen voor onderhoudscontrolelijsten zijn algemene veiligheidsinstructies en een lijst met artikelen en voorwaarden die moeten worden gecontroleerd op een bepaalde pomp of soortgelijke modellen van een transportband.

1. Selecteer **Activabeheer** \> **Instellen** \> **Onderhoudscontrolelijsten** \> **Sjablonen onderhoudscontrolelijsten**.
2. Selecteer **Nieuw**.

    Er wordt automatisch een sjabloon-ID ingevoerd in het veld **Sjabloon onderhoudscontrolelijst**.

3. Geef in het veld **Naam** een naam op voor de nieuwe sjabloon voor de onderhoudscontrolelijst.
4. Selecteer in het Sneltabblad **Regels onderhoudscontrolelijsten** **Toevoegen** om een sjabloonregel toe te voegen.

    In het veld **Regelnummer** wordt automatisch een volgnummer voor de regel ingevoerd. Nadat u alle regels hebt toegevoegd, kunt u de regelnummers wijzigen zoals u dat nodig hebt. Wanneer u regel selecteert en vervolgens op de toets **Pijl-omlaag** drukt, wordt het volgende nummer in de reeks automatisch op de volgende regel ingevoerd.

5. Typ een naam voor de regel voor de onderhoudscontrolelijst in het veld **Type**. Voor elk type onderhoudscontrolelijst worden de gerelateerde velden weergegeven op het Sneltabblad **Regeldetails**. De volgende waarden zijn beschikbaar:

    - **Tekst** – de regel bevat tekst die beschrijft wat u moet doen. U kunt dit type onderhoudscontrolelijst gebruiken als u wilt dat een medewerker iets controleert of inspecteert, zonder een specifiek (meetbaar) resultaat te verwachten. Nadat u dit type hebt geselecteerd, voert u een naam of header in het veld **Naam** in. Voer in het veld **Instructies** een omschrijving in voor wat moet worden gedaan. Als de stap verplicht is voor de onderhoudscontrolelijst, stelt u de optie **Verplicht** in op **Ja**.
    - **Header** - De regel wordt gebruikt als header voor het groeperen van de onderhoudscontrolelijstregels die eronder worden weergegeven. Dit type is handig als u verschillende onderhoudscontrolelijstregels hebt die in specifieke gebieden kunnen worden onderverdeeld. Headers bieden een overzicht voor de werknemer die een onderhoudscontrolelijst met veel regels voor onderhoudscontrole moet voltooien. Nadat u dit type hebt geselecteerd, voert u een beschrijvende naam in het veld **Naam** in.
    - **Sjabloon** - de regel wordt gebruikt om een verwijzing naar een bestaande sjabloon te maken. Nadat u dit type hebt geselecteerd, voert u een naam voor de sjabloon in het veld **Naam** in. Selecteer in het veld **Sjabloon** cd sjabloon.
    - **Variabele** – De regel wordt gebruikt om een mogelijk resultaat in een bereik te definiëren. Zie de sectie [Een variabele controlelijst voor onderhoud maken](#create-a-maintenance-checklist-variable) voor informatie over het instellen van variabelen voor onderhoudscontrolelijsten. Nadat u dit type hebt geselecteerd, voert u een beschrijvende naam voor de variabele in het veld **Naam** in. Selecteer de variabele in het veld **Variabele**. Voer in het veld **Instructies** een omschrijving in voor wat moet worden gedaan. Als de stap verplicht is voor de onderhoudscontrolelijst, stelt u de optie **Verplicht** in op **Ja**.
    - **Meting** - De regel wordt gebruikt om een specifieke meting vast te leggen. U kunt de meting instellen die moet worden gerelateerd aan een vooraf gedefinieerde teller. Nadat u dit type hebt geselecteerd, voert u een naam voor de sjabloon in het veld **Naam** in. Als deze stap verplicht is voor de onderhoudscontrolelijst, stelt u de optie **Verplicht** in op **Ja**. Als u de metingsregel wilt gebruiken als een tellerregistratie, selecteert u de teller in het veld **Teller**. Het gerelateerde veld **Eenheid** wordt automatisch bijgewerkt. Als u een teller hebt geselecteerd, selecteert u de bijwerkmethode in het veld **Waarde**. Voer in de velden **Min. waarde** en **Max. waarde** het toegestane waardebereik in. Voer in het veld **Instructies** een omschrijving in voor wat moet worden gedaan.

        > [!NOTE]
        > Elke regel van het type **Meting** waarvoor geen tellerinstellingen worden ingesteld, wordt behandeld als een onafhankelijke metingsregistratie waarvoor in Activabeheer geen automatische follow-up wordt uitgevoerd. Dito, als het geselecteerde metertype niet aanwezig is in het activum dat is gerelateerd aan de werkorder, wordt de taakcontrolelijst voor onderhoud behandeld als een onafhankelijke meting. De itemwaarde kan meerdere keren worden gewijzigd. Deze wordt niet geboekt totdat [de levenscyclusstatus van de werkorder](work-order-lifecycle-states.md) wordt gewijzigd in een status waarin de **Controlelijst voor procesonderhoud** is ingesteld op **Ja**.

    Op het Sneltabblad **Details** wordt in veld **Controles** het totale aantal controleregels in de sjabloon weergegeven. Dit aantal bevat de geneste regels in een bestaande sjabloon waarnaar u in uw sjabloon verwijst.

![Pagina met sjablonen voor onderhoudscontrolelijst.](media/05-setup-for-work-orders.png)

## <a name="create-a-maintenance-job-type"></a>Een type onderhoudstaak aanmaken

1. Selecteer **Activabeheer** \> **Instellingen** \> **Taken** \> **Types onderhoudstaak**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Type onderhoudstaak** een id in voor het type onderhoudstaak.
4. Voer in het veld **Naam** een naam in.

    Op het Sneltabblad **Details** vindt u een overzicht van het aantal varianten, vaardig heden, certificaten, geslaagde taken en activatypen van het onderhoudstaken dat is gemaakt voor dit type onderhoudstaak. In het veld **Instellingenregels** wordt het aantal standaard regels van het type onderhoudstaak weergegeven dat is ingesteld voor dit type onderhoudstaak. Het veld **Activa** toont het aantal actieve activa dat op dit moment gebruik heeft van dit type onderhoudstaak.

5. Voer in het Sneltabblad **Algemeen** in het veld **Categorie onderhoudstaaktype** een id in voor de categorie onderhoudstaaktype.
6. Stel de optie **Uitvaltijd onderhoudsactiviteiten** in op **Ja** als voor het type onderhoudstaak een onderhoudsstop van de apparatuur nodig is voordat de taak kan worden uitgevoerd.
7. Voer in het Sneltabblad **Omschrijving** een omschrijving van het type onderhoudstaak in.
8. In het Sneltabblad **Varianten onderhoudstaaktype** kunt u varianten toevoegen voor het type onderhoudstaak.
9. Op de Sneltabbladen **Vereiste vaardigheden** en **Vereiste certificaten** kunt u kwalificaties en getuigschriften toevoegen aan het type onderhoudstaak.
10. Als een bepaald type onderhoudstaak moet worden uitgevoerd, voegt u deze toe in het Sneltabblad **Succesvolle taken**. U kunt ook een type onderhoudstaak -variant en specialisme instellen die betrekking hebben op het type onderhoudstaak. Als de volgende taak een bepaald aantal dagen voor of na het begin van de taak waarvoor dit type onderhoudstaak wordt gebruikt, is gestart, geeft u het aantal dagen op in het veld **Vertraging in dagen**. Positieve getallen vertegenwoordigen dagen na het begin van de gerelateerde taak en negatieve getallen staan voor dagen vóór de geplande begindatum van de gerelateerde taak. Als u bijvoorbeeld 5 **invoert**, begint de taak die wordt uitgevoerd vijf dagen na het begin van de taak die is gerelateerd aan het taak type onderhoudstaak. Als u bijvoorbeeld **-3** invoert, begint de taak die wordt uitgevoerd vijf dagen voor het begin van de taak die is gerelateerd aan het type onderhoudstaak.

    > [!NOTE]
    > Als u meer dan één regel van het type onderhoudstaak toevoegt, geeft de volgorde van de regels aan wanneer ze moeten worden uitgevoerd. De volgorde begint bovenaan de lijst.

11. Op het Sneltabblad **Activatypen** kunt u activatypen toevoegen aan het type onderhoudstaak.

![Pagina met typen onderhoudstaken.](media/06-setup-for-work-orders.png)

## <a name="create-maintenance-job-type-default-lines-and-related-forecasts-maintenance-checklists-tools-description-and-attachments"></a>Maak standaardregels voor typen onderhoudstaken en gerelateerde prognoses, onderhoudscontrolelijsten , hulpmiddelen, beschrijving en bijlagen

1. Selecteer **Activabeheer** \> **Instellingen** \> **Taken** \> **Standaard onderhoudstaaktypen**.

    – of –

    Selecteer **Activabeheer** \> **Instellingen** \> **Taken** \> **Typen onderhoudstaken**, selecteer een type onderhoudstaak en selecteer vervolgens **Standaard typen onderhoudstaken**.

2. Selecteer **Nieuw**.
3. Selecteer in de velden **Functionele locatie**, **Activatype**, **Fabrikant**, **Model** en **Activum** de gewenste waarden, afhankelijk van hoe specifiek de standaardwaarde van het type onderhoudstaak moet zijn.
4. Selecteer in veld **Type onderhoudstaak** een type onderhoudstaak, als dit niet automatisch is ingeschakeld.
5. Selecteer in de velden **Variant type onderhoudstaak** en **Specialisme** een variant type onderhoudstaak type en een onderhoudstaak specialisme als dat nodig is.
6. **Prognose** selecteren.
7. Op de pagina **Standaard type onderhoudstaak prognose** kunt u prognoses maken op uren, artikelen en onkosten. Selecteer **Toevoegen** op de relevante tabbladen en maak selecties om de vereiste prognoses voor het type onderhoudstaak te maken.
8. Op het tabblad **Artikelprognose** kunt u voorraaddimensies selecteren die op de artikelregel moeten worden weergegeven. Selecteer **Voorraad** \> **Dimensies**, selecteer de dimensies die u wilt weergeven, stel de optie **Instellingen opslaan** op **Ja** en selecteer vervolgens **OK** i.
9. Selecteer op het tabblad **Artikelprognose** **Artikel waar gebruikt** voor een overzicht van waar het artikel op de geselecteerde regel in Activabeheer wordt gebruikt in relatie tot activa, standaardwaarden voor onderhoudstaaktypen, reserveonderdelen en werkorders. 

    Het Sneltabblad **Onderhoudsprognose totalen** geeft een overzicht van prognosetotalen. Dit overzicht bevat het totale aantal uren en prognoseregels dat is gemaakt.

    > [!NOTE]
    > Als u de prognose-instellingen wilt kopiëren van een ander type Onderhoudstaak, selecteert u **Prognose kopiëren** en selecteert u vervolgens het taak type onderhoudstaak waaruit u de instellingen wilt kopiëren.

11. Klik op **Opslaan** om uw wijzigingen op te slaan.
12. Sluit de pagina **Standaard type onderhoudstaak prognose** om terug te keren naar de pagina **Standaard type onderhoudstaken**.
13. Selecteer **Onderhoudscontrolelijst**.
14. Op de pagina **Standaard controlelijsten voor onderhoudstaken** kunt u regels voor onderhoudscontrolelijsten toevoegen aan het geselecteerde standaard type onderhoudstaak. Selecteer in het Sneltabblad **Regels onderhoudscontrolelijsten** **Nieuw** om een regel voor een onderhoudscontrolelijst toe te voegen.

    Regelnummers worden automatisch ingevoerd in het veld **Regelnummer** om de volgorde van de regels voor onderhoudscontrolelijsten aan te geven. U kunt de regelnummers bewerken als dat nodig is. Nadat u de eerste regel in de onderhoudscontrolelijst hebt gemaakt, selecteert u de regel en drukt u op de toets **pijl-omlaag** om een onderliggende regel toe te voegen. U kunt ook een regel voor onderhoudscontrolelijsten selecteren en vervolgens **Nieuw** selecteren. In dat geval wordt er een nieuwe regel toegevoegd boven de geselecteerde regel in de onderhoudscontrolelijst.

15. Selecteer in veld **Type** het regeltype en voeg vervolgens informatie toe die is gerelateerd aan het type onderhoudscontrolelijst. Zie het gedeelte [Een sjabloon voor onderhoudscontrolelijsten maken](#create-a-maintenance-checklist-template) voor een beschrijving van de beschikbare typen en gerelateerde velden.

    > [!NOTE]
    > Als u de onderhoudscontrolelijst-instellingen wilt kopiëren van een ander type onderhoudstaak, selecteert u **Onderhoudscontrolelijst kopiëren** en selecteert u vervolgens het taak type onderhoudstaak waaruit u de instellingen wilt kopiëren.
    >
    > U kunt makkelijk een nieuwe sjabloon te maken van een bestaande onderhoudscontrolelijst. U kunt de sjabloon vervolgens opnieuw gebruiken in meerdere onderhoudscontrolelijsten. De nieuwe sjabloon is een exacte kopie van de actieve onderhoudscontrolelijst. Selecteer **Sjabloon maken** en voer vervolgens een naam in voor de sjabloon. Als u de bestaande Sjabloon wilt vervangen door één regel waarmee naar de nieuwe sjabloon wordt verwezen, stelt u de optie **Vervangen** in op **Ja**. U kunt de inhoud van de sjabloon weergeven in de detailpagina **Sjablonen voor onderhoudscontrolelijsten**.

16. Klik op **Opslaan** om uw wijzigingen op te slaan.
17. Ga terug naar de pagina **Standaard type onderhoudstaken**.
18. Selecteer **Hulpmiddelen**.
19. Op de pagina **Hulpmiddelen voor standaard type onderhoudstaken** kunt u de hulpmiddelen (resources) toevoegen die moeten worden gebruikt voor het type onderhoudstaak. Selecteer **Nieuw** en selecteer vervolgens het hulpmiddel in het veld **Resource**.

    > [!NOTE]
    > Als u de instellingen voor hulpmiddelen wilt kopiëren van een ander type onderhoudstaak, selecteert u **Hulpmiddelen kopiëren** en selecteert u vervolgens het type onderhoudstaak waaruit u de instellingen wilt kopiëren.

20. Klik op **Opslaan** om uw wijzigingen op te slaan.
21. Ga terug naar de pagina **Standaard type onderhoudstaken**.
22. Selecteer **Werkomschrijving**.
23. Selecteer op de pagina **Werkomschrijving** **Bewerken** en voeg vervolgens een omschrijving toe die is gerelateerd aan het geselecteerde standaard type onderhoudstaak.
24. Selecteer **Opslaan** om de omschrijving op te slaan.

    Als u hier een werkomschrijving toevoegt, wordt elke omschrijving overschreven die is ingesteld voor het type onderhoudstaak op de pagina **Typen onderhoudstaken**. Als u hier geen werkomschrijving toevoegt, wordt de omschrijving gebruikt die is ingesteld voor het type onderhoudstaak. Omschrijvingen worden automatisch overgebracht naar werkorders die het type onderhoudstaak of standaard type onderhoudstaak gebruiken.

25. Ga terug naar de pagina **Standaard type onderhoudstaken**.
26. Als u bijlagen wilt instellen voor een geselecteerde regel voor standaard type onderhoudstaken, selecteert u **Documenten bijvoegen**. Bijlagen die zijn ingesteld op een reel voor standaard type onderhoudstaken worden automatisch opgenomen op werkorderregels die de regel van het standaard type onderhoudstaak gebruiken.
27. Selecteer **Nieuw** en selecteer vervolgens een documenttype.
28. Upload het document of bestand.
29. Stel de velden in op pagina **Bijlagen**. Bij de instelling voor bijlagen wordt de standaard functionaliteit voor documentinstellingen gebruikt.
30. Selecteer **Opslaan** om de bijlage op te slaan.

    > [!NOTE]
    > Bijlagen bij een regel voor standaardtype onderhoudstaken worden samen met een werkorderrapport afgedrukt als de documenttypen van de bijlagen zijn geselecteerd op het tabblad **Documenttypen** van de pagina **Activabeheerparameters** (**Activabeheer** \> **Instellingen** \> **Activabeheerparameters**). Voorbeelden van bijlagen zijn richtlijnen waarin wordt uitgelegd hoe een bepaalde taak of een vooraf gedefinieerde controlelijst voor onderhoud kan worden uitgevoerd (als u de functionaliteit voor onderhoudscontrolelijsten gebruikt voor standaardregels voor typen onderhoudstaken).

    Op de pagina **Standaardtypen onderhoudstaken** wordt elke regel weergegeven met het aantal geraamde uren, en ook het aantal regels dat is gemaakt voor artikelen, onkosten, onderhoudscontrolijsten en hulpmiddelen. Het veld **Activa** toont het aantal actieve activa dat gerelateerd is aan de regel voor standaardtype onderhoudstaak.

31. Als u een standaard type onderhoudstaak wilt kopiëren naar een ander standaard type onderhoudstaak, selecteert u het standaard type onderhoudstaak om een andere instelling naar te kopiëren, selecteert u **Instellingen** en selecteert u vervolgens het standaard type onderhoudstaak dat u wilt kopiëren.
32. Als u een lijst wilt weergeven met de activa, onderhoudsplannen of onderhoudsbeurten die op dit moment een regel voor standaard type onderhoudstaak gebruiken, selecteert u de regel en selecteert u vervolgens **Gebruikt door**.

![Pagina met standaardinstellingen voor onderhoudstaaktypen.](media/07-setup-for-work-orders.png)

Wanneer het systeem het beschikbare standaard type onderhoudstaak selecteert dat moet worden gebruikt op een werkorderregel, wordt de selectie gebaseerd op de activa en de gerelateerde instellingen van het activumtype. Activabeheer gaat door alle standaard records voor onderhoudstaken die zijn gerelateerd aan het type onderhoudstaak dat is gerelateerd aan het activatype om te controleren of er een overeenkomst is. De meest specifieke combinatie wordt altijd als eerste gecontroleerd. Met andere woorden, als u de meest specifieke combinatie wilt zoeken, controleert Activabeheer eerst of er een mogelijke overeenkomst voor het veld **Specialisme** bestaat. Als er geen overeenkomst wordt gevonden, wordt er gecontroleerd op een overeenkomst voor het veld **Variant op type onderhoudstaak**. Als er geen overeenkomst wordt gevonden, wordt gecontroleerd op een overeenkomst voor het veld **Type onderhoudstaak**, enzovoort (**Specialisme**, vervolgens **Variant type onderhoudstaak**, dan **Type onderhoudstaak**, vervolgens **Activum**, vervolgens **Model**, **Fabrikant**, en vervolgens **Type Activum**). Als er geen overeenkomst wordt gevonden, wordt het standaardrecord gebruikt waarin alleen het type onderhoudstaak wordt geselecteerd.

De ID van een projectactiviteit wordt automatisch gekoppeld aan elke regel voor standaard type onderhoudstaak die u maakt. De projectactiviteit wordt gemaakt in het prognoseproject dat is geselecteerd in het veld **Prognoseproject voor onderhoud** op het tabblad **Activa** van de pagina **Activabeheer**. Het doel van de projectactiviteit is het beheren van prognoses op uren, artikelen en onkosten in relatie tot werkorders. Prognoses voor typen onderhoudstaken worden automatisch overgebracht naar de werkorderregel en worden gekopieerd vanuit het prognoseproject naar het werkorderproject dat voor de werkorderregel is gemaakt. Het doel van de projectactiviteit is het beheren van prognoses in relatie tot werkorders.

U kunt een batchtaak instellen om verwijzingen naar het standaard type onderhoudstaak met regelmatige intervallen bij te werken, of u kunt de taak handmatig uitvoeren. Om een batchtaak te maken of een handmatige update uit te voeren, selecteert u **Activabeheer** \> **Periodiek** \> **Preventief onderhoud** \> **Verwijzingen naar het standaard type onderhoudstaak bijwerken**.

## <a name="overview-of-maintenance-job-types-that-are-related-to-assets"></a>Overzicht van typen onderhoudstaken die te maken hebben met activa

Nadat u de vereiste combinaties hebt gemaakt voor het vereiste type onderhoudstaak, kunt u de pagina **Alle activa** gebruiken om een overzicht weer te geven van het huidige type onderhoudstaak dat is gekoppeld aan een specifiek activum. Het overzicht toont alle standaard combinaties van typen onderhoudstaken die kunnen worden gebruikt voor het activatype dat voor de activa is geselecteerd, voor alle typen onderhoudstaken. Deze combinaties omvatten combinaties met verschillende typen onderhoudstaken en specialismen voor onderhoudstaken.

1. Selecteer **Activabeheer** \> **Algemeen** \> **Activa** \> **Alle activa** of **Actieve activa**.
2. Selecteer in de lijst de activa waarvoor u een overzicht van de combinaties van typen onderhoudstaken wilt weer geven.
3. Klik in het Actievenster op het tabblad **Algemeen** in de groep **Verwante informatie**, selecteer **Typen onderhoudstaken**.

    In het linkerdeelvenster van de pagina **Activa typen onderhoudstaken** wordt een lijst weer gegeven met alle combinaties van onderhoudstaken die zijn gerelateerd aan het geselecteerde activum.

4. Selecteer een combinatie van typen onderhoudstaken om de gerelateerde instellingen voor onderhoudscontrolelijsten, prognoses en hulpmiddelen te zien. De sectie **Details** op het Sneltabblad **Standaard type onderhoudstaak** bevat het aantal verwante onderhoudscontrolelijsten, verwachte uren, artikelen, enzovoort, die zijn gerelateerd aan de geselecteerde combinatie van het type onderhoudstaken.
5. U kunt de details van het geselecteerde type onderhoudstaak weergeven door **Typen onderhoudstaken** te selecteren.

![Pagina met typen onderhoudstaken voor activa.](media/08-setup-for-work-orders.png)

## <a name="automatic-update-of-maintenance-job-type-forecasts"></a>Prognoses van het type onderhoudstaak automatisch bijwerken

In Activabeheer kunt u eventuele wijzigingen in prognoses voor typen onderhoudstaken die betrekking hebben op uurkosten, artikelkosten en onkosten, automatisch bijwerken als ze zijn bijgewerkt in andere modules. Op deze manier zorgt u ervoor dat prognoses van het type onderhoudstaak altijd de laatste kostprijzen gebruiken.

1. Selecteer **Activabeheer** \> **Periodiek** \> **Prognose** \> **Prognose type onderhoudstaken bijwerken**
2. In het dialoogvenster **Prognose type onderhoudstaken bijwerken**, op het Sneltabblad **Records om op te nemen**, kunt u selecties voor specifieke typen onderhoudstaken toevoegen als u deze nodig hebt. Selecteer **Filter** en selecteer vervolgens **selecteren** om de selecties te maken.
3. Indien nodig kunt u de automatische update op het Sneltabblad **Op de achtergrond uitvoeren** instellen als een batchtaak.
4. Selecteer **OK** om de update van de prognose te starten.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]