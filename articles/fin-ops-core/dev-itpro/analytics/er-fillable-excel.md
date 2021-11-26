---
title: Een configuratie ontwerpen voor het genereren van documenten in Excel-indeling
description: Dit onderwerp bevat informatie over het ontwerpen van een ER-indeling (Elektronische rapportage) voor het invullen van een Excel-sjabloon en het genereren van uitgaande Excel-documenten.
author: NickSelin
ms.date: 10/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cfacc2232201b85a49068ee724b55e71b60eb2be
ms.sourcegitcommit: 1cc56643160bd3ad4e344d8926cd298012f3e024
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/02/2021
ms.locfileid: "7731633"
---
# <a name="design-a-configuration-for-generating-documents-in-excel-format"></a>Een configuratie ontwerpen voor het genereren van documenten in Excel-indeling

[!include[banner](../includes/banner.md)]

U kunt een [ER](general-electronic-reporting.md)-indelingsconfiguratie ontwerpen met een ER-[indelingsonderdeel](general-electronic-reporting.md#FormatComponentOutbound) dat u kunt configureren om een uitgaand document in een Microsoft Excel-werkmapindeling te genereren. Hiervoor moeten specifieke ER-indelingsonderdelen worden gebruikt.

Volg de stappen in het onderwerp [Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling](tasks/er-design-reports-openxml-2016-11.md) voor meer informatie over deze functie.

## <a name="add-a-new-er-format"></a>Een nieuwe ER-indeling toevoegen

Wanneer u een nieuwe ER-indelingsconfiguratie toevoegt om een uitgaand document in een Excel-werkmapindeling te genereren, moet u de waarde **Excel** voor het kenmerk **Type indeling** van de indeling selecteren of het kenmerk **Type indeling** leeg laten.

- Als u **Excel** selecteert, kunt u de indeling zo configureren dat een uitgaand document alleen in de Excel-indeling wordt gegenereerd.
- Als u het kenmerk leeg laat, kunt u de indeling configureren om een uitgaand document te genereren in elke indeling die wordt ondersteund door het ER-raamwerk.

Als u het ER-indelingsonderdeel van de configuratie wilt configureren, selecteert u **Ontwerper** in het actievenster en opent u het ER-indelingsonderdeel in de ER Operations-ontwerper.

![Pagina Configuraties.](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Excel-bestandsonderdeel

### <a name="manual-entry"></a>Handmatige invoer

U moet een onderdeel **Excel\\Bestand** toevoegen aan de geconfigureerde ER-indeling om een uitgaand document in Excel-indeling te genereren.

![Onderdeel Excel\Bestand.](./media/er-excel-format-add-file-component.png)

Als u de indeling van het uitgaande document wilt opgeven, voegt u een Excel-werkmap met de extensie .xlsx toe aan het onderdeel **Excel\\Bestand** als sjabloon voor uitgaande documenten.

> [!NOTE]
> Wanneer u handmatig een sjabloon toevoegt, moet u een [documenttype](../../../fin-ops-core/fin-ops/organization-administration/configure-document-management.md#configure-document-types) gebruiken dat in de [ER-parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) voor dat doel is geconfigureerd.

![Een bijlage toevoegen aan het onderdeel Excel\Bestand.](./media/er-excel-format-add-file-component2.png)

Als u wilt opgeven hoe de toegevoegde sjabloon wordt ingevuld wanneer u de geconfigureerde ER-indeling uitvoert, moet u geneste onderdelen **Werkblad**, **Bereik** en **Cel** toevoegen aan het onderdeel **Excel\\Bestand**. Elk genest onderdeel moet worden gekoppeld aan een benoemd Excel-item.

### <a name="template-import"></a>Sjabloonimport

U kunt **Importeren uit Excel** selecteren op het tabblad **Importeren** van het actievenster om een nieuwe sjabloon te importeren in een lege ER-indeling. In dit voorbeeld wordt automatisch een onderdeel **Excel\\Bestand** gemaakt en de geïmporteerde sjabloon wordt hieraan toegevoegd. Alle vereiste ER-onderdelen worden ook automatisch gemaakt, op basis van de lijst met Excel-artikelen die worden ontdekt.

![Importeren uit Excel selecteren.](./media/er-excel-format-import-template.png)

> [!NOTE]
> Als u het optionele element **Werkblad** wilt maken in de bewerkbare ER-indeling, stelt u de optie **Indelingselement Excel-werkblad maken** in op **Ja**.

## <a name="sheet-component"></a>Het onderdeel Werkblad

Het onderdeel **Werkblad** geeft een werkblad aan van de bijgevoegde Excel-werkmap die moet worden ingevuld. De naam van het werkblad in een Excel-sjabloon wordt gedefinieerd in het eigenschap **Werkblad** van dit onderdeel.

> [!NOTE]
> Dit onderdeel is optioneel voor Excel-werkmappen die één werkblad bevatten.

Op het tabblad **Toewijzing** van de ER Operations-ontwerper kunt u de eigenschap **Ingeschakeld** voor een onderdeel **Werkblad** configureren om op te geven of het onderdeel in een gegenereerd document moet worden geplaatst:

- Als een expressie van de eigenschap **Ingeschakeld** is geconfigureerd om **Waar** te retourneren tijdens runtime, of als er helemaal geen expressie is geconfigureerd, wordt het betreffende werkblad in het gegenereerde document geplaatst.
- Als een expressie van de eigenschap **Ingeschakeld** is ingesteld om **Onwaar** te retourneren tijdens runtime, bevat het gegenereerde document geen werkblad.

![Voorbeeld van een onderdeel Werkblad.](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Het onderdeel Bereik

Het onderdeel **Bereik** geeft een Excel-bereik aan dat moet worden beheerd door dit ER-onderdeel. De naam van het bereik wordt gedefinieerd in het eigenschap **Excel-bereik** van dit onderdeel.

### <a name="replication"></a>Replicatie

De eigenschap **Replicatierichting** geeft aan of en hoe het bereik wordt herhaald in een gegenereerd document:

- Als de eigenschap **Replicatierichting** is ingesteld op **Geen replicatie**, wordt het betreffende Excel-bereik niet herhaald in het gegenereerde document.
- Als de eigenschap **Replicatierichting** is ingesteld op **Verticaal**, wordt het betreffende Excel-bereik herhaald in het gegenereerde document. Elk gerepliceerd bereik wordt onder het oorspronkelijke bereik in een Excel-sjabloon geplaatst. Het aantal herhalingen wordt gedefinieerd door het aantal records in een gegevensbron van het type **Recordlijst** dat is gekoppeld aan dit ER-onderdeel.
- Als de eigenschap **Replicatierichting** is ingesteld op **Horizontaal**, wordt het betreffende Excel-bereik herhaald in het gegenereerde document. Elk gerepliceerd bereik wordt rechts van het oorspronkelijke bereik in een Excel-sjabloon geplaatst. Het aantal herhalingen wordt gedefinieerd door het aantal records in een gegevensbron van het type **Recordlijst** dat is gekoppeld aan dit ER-onderdeel.

Als u meer wilt weten over horizontale replicatie, volgt u de stappen in [Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen](tasks/er-horizontal-1.md).

### <a name="nested-components"></a>Geneste onderdelen

Het onderdeel **Bereik** kan andere geneste ER-onderdelen bevatten die worden gebruikt om waarden op te geven in de toepasselijke benoemde Excel-bereiken.

- Als een deel van de groep **Tekst** wordt gebruikt om waarden in te voeren, wordt de waarde in een Excel-bereik ingevoerd als tekstwaarde.

    > [!NOTE]
    > Gebruik dit patroon om ingevoerde waarden op te maken op basis van de landinstelling die in de toepassing is gedefinieerd.

- Als het onderdeel **Cel** van de groep **Excel** wordt gebruikt om waarden in te voeren, wordt de waarde in een Excel-bereik ingevoerd als een waarde van het gegevens type dat wordt gedefinieerd door de binding van dat onderdeel **Cel** (bijvoorbeeld **Tekenreeks**, **Werkelijk** of **Geheel getal**).

    > [!NOTE]
    > Gebruik dit patroon om de ingevoerde waarden in de Excel-toepassing op te maken op basis van de landinstelling van de lokale computer waarop het uitgaande document wordt geopend.

### <a name="enabling"></a>Inschakelen

Op het tabblad **Toewijzing** van de ER Operations-ontwerper kunt u de eigenschap **Ingeschakeld** voor een onderdeel **Bereik** configureren om op te geven of het onderdeel in een gegenereerd document moet worden geplaatst:

- Als een expressie van de eigenschap **Ingeschakeld** is geconfigureerd om **Waar** te retourneren tijdens runtime, of als er helemaal geen expressie is geconfigureerd, wordt het betreffende bereik in het gegenereerde document ingevuld.
- Als een expressie van de eigenschap **Ingeschakeld** is geconfigureerd om **Onwaar** te retourneren tijdens runtime en als dit bereik niet alle rijen of kolommen vertegenwoordigt, wordt het betreffende bereik niet in het gegenereerde document ingevuld.
- Als een expressie van de eigenschap **Ingeschakeld** is geconfigureerd om **Onwaar** te retourneren tijdens runtime en als dit bereik alle rijen of kolommen vertegenwoordigt, bevat het gegenereerde document die rijen en kolommen als verborgen rijen en kolommen.

### <a name="resizing"></a>Formaat wijzigen

U kunt de Excel-sjabloon configureren, zodat cellen worden gebruikt om tekstgegevens te presenteren. Om er zeker van te zijn dat de gehele tekst in een cel zichtbaar is in een gegenereerd document, kunt u die cel zo configureren dat de tekst binnen het document automatisch terugloopt. U kunt de rij met die cel ook zo configureren dat de hoogte ervan automatisch wordt aangepast als de doorlopende tekst niet volledig zichtbaar is. Zie de sectie "Teruglooptekst in een cel" in [Gegevens repareren die worden afgekapt in cellen](https://support.microsoft.com/office/fix-data-that-is-cut-off-in-cells-e996e213-6514-49d8-b82a-2721cef6144e) voor meer informatie.

> [!NOTE]
> Wegens een bekende [beperking van Excel](https://support.microsoft.com/topic/you-cannot-use-the-autofit-feature-for-rows-or-columns-that-contain-merged-cells-in-excel-34b54dd7-9bfc-6c8f-5ee3-2715d7db4353) is het mogelijk dat, zelfs als u cellen configureert om tekst terug te laten lopen, en u de rijen die deze cellen bevatten configureert om de hoogte ervan automatisch aan te passen aan de teruglopende tekst, u de Excel-functies **AutoAanpassen** en **Tekstterugloop** niet kunt gebruiken voor samengevoegde cellen en de rijen die deze cellen bevatten. 

Vanaf versie 10.0.23 van Dynamics 365 Finance kunt u ER dwingen om in een gegenereerd document de hoogte van elke rij te berekenen die zo is geconfigureerd dat de hoogte ervan automatisch wordt aangepast aan de inhoud van geneste cellen wanneer die rij minimaal één samengevoegde cel bevat die is geconfigureerd om de tekst binnen de rij terug te laten lopen. De berekende hoogte wordt vervolgens gebruikt om de grootte van de rij te wijzigen, zodat alle cellen in de rij zichtbaar zijn in het gegenereerde document. Volg deze stappen om deze functionaliteit te gaan gebruiken wanneer u een ER-indeling uitvoert die geconfigureerd was om Excel-sjablonen te gebruiken om uitgaande documenten te genereren.

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Parameters van elektronische rapportage**.
3. Stel op de pagina **Parameters van elektronische rapportage** op het tabblad **Runtime** de optie **Rijhoogte AutoAanpassen** in op **Ja**.

Als u deze regel voor één ER-indeling wilt wijzigen, moet u de conceptversie van die indeling met de volgende stappen bijwerken.

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuraties** de optie **Rapportconfiguraties**.
3. Selecteer op de pagina **Configuraties** in de configuratieboomstructuur in het linkerdeelvenster een ER-configuratie die is ontworpen om een Excel-sjabloon te gebruiken om uitgaande documenten te genereren.
4. Selecteer op het sneltabblad **Versies** de configuratieversie met de status **Concept**.
5. Selecteer **Ontwerper** in het actievenster.
6. Selecteer op de pagina **Indelingsontwerper**, in de indelingsboomstructuur in het linkerdeelvenster, het Excel-onderdeel dat is gekoppeld aan een Excel-sjabloon.
7. Selecteer op het tabblad **Opmaak** in het veld **Rijhoogte aanpassen** een waarde om op te geven of ER moet worden verplicht om tijdens runtime de hoogte van rijen te wijzigen in een uitgaand document dat wordt gegenereerd door de bewerkte ER-indeling:

    - **Standaard**: gebruik de algemene instelling die is geconfigureerd in het veld **Rijhoogte AutoAanpassen** op de pagina **Parameters voor elektronische rapportage**.
    - **Ja**: de algemene instelling overschrijven en de rijhoogte wijzigen tijdens runtime.
    - **Nee**: de algemene instelling overschrijven en de rijhoogte niet wijzigen tijdens runtime.

## <a name="cell-component"></a>Het onderdeel Cel

Het onderdeel **Cel** wordt gebruikt om benoemde cellen, vormen en figuren in Excel in te vullen. Als u een benoemd Excel-object wilt aanduiden dat moet worden ingevuld door een ER-onderdeel **Cel**, moet u de naam van dat object opgeven in de eigenschap **Excel-bereik** van het onderdeel **Cel**.

Op het tabblad **Toewijzing** van de ER Operations-ontwerper kunt u de eigenschap **Ingeschakeld** voor een onderdeel **Cel** configureren om op te geven of het object in een gegenereerd document moet worden ingevuld:

- Als een expressie van de eigenschap **Ingeschakeld** is geconfigureerd om **Waar** te retourneren tijdens runtime, of als er helemaal geen expressie is geconfigureerd, wordt het betreffende object in het gegenereerde document ingevuld. De binding van dit onderdeel **Cel** geeft een waarde aan die in het betreffende object wordt geplaatst.
- Als een expressie van de eigenschap **Ingeschakeld** is ingesteld om **Onwaar** te retourneren tijdens runtime, wordt het betreffende object niet ingevuld in het gegenereerde document.

Wanneer een onderdeel **Cel** is geconfigureerd om een waarde in een cel in te voeren, kan deze worden gekoppeld aan een gegevensbron waarmee de waarde van een primitief gegevenstype wordt geretourneerd (bijvoorbeeld **Tekenreeks**, **Werkelijk** of **Geheel getal**). In dit geval wordt de waarde in de cel ingevoerd als waarde van hetzelfde gegevenstype.

Wanneer een onderdeel **Cel** is geconfigureerd om een waarde in een Excel-vorm in te voeren, kan deze worden gekoppeld aan een gegevensbron waarmee een waarde van een primitief gegevenstype wordt geretourneerd (bijvoorbeeld **Tekenreeks**, **Werkelijk** of **Geheel getal**). In dit geval wordt de waarde in de Excel-vorm ingevoerd als de tekst van die vorm. Voor waarden van andere gegevenstypen dan **Tekenreeks** wordt de conversie naar tekst automatisch uitgevoerd.

> [!NOTE]
> U kunt een onderdeel **Cel** zo configureren dat alleen een vorm wordt ingevuld wanneer een eigenschap voor vormtekst wordt ondersteund.

Wanneer een onderdeel **Cel** is geconfigureerd om een waarde in een Excel-afbeelding cel in te voeren, kan deze worden gekoppeld aan een gegevensbron waarmee een waarde van het gegevenstype **Container** wordt geretourneerd die staat voor een afbeelding in binaire indeling. In dit geval wordt de waarde in de Excel-afbeelding als een afbeelding ingevoerd.

> [!NOTE]
> Elke Excel-afbeelding en -vorm wordt als verankerd aan de linkerbovenhoek van een bepaalde Excel-cel of een bepaald bereik beschouwd. Als u een Excel-afbeelding of -vorm wilt repliceren, moet u de cel of het bereik waaraan deze is verankerd, configureren als een gerepliceerde cel of een gerepliceerd bereik.

Zie [Afbeeldingen en vormen insluiten in documenten die u genereert met ER](electronic-reporting-embed-images-shapes.md) voor meer informatie over het insluiten van afbeeldingen en vormen.

## <a name="page-break-component"></a>Het onderdeel Pagina-einde

Het onderdeel **Pagina-einde** zorgt ervoor dat er een nieuwe pagina wordt gestart in Excel. Dit onderdeel is niet vereist als u de standaardpaginering van Excel wilt gebruiken, maar u moet deze functie gebruiken wanneer u wilt dat Excel uw ER-indeling volgt om de paginering te structureren.

## <a name="page-component"></a><a name="page-component"></a>Paginaonderdeel

### <a name="overview"></a>Overzicht

U kunt het onderdeel **Pagina** gebruiken wanneer u wilt dat Excel de ER-indeling en structuurpaginering volgt in een gegenereerd uitgaand document. Wanneer in een ER-indeling onderdelen worden uitgevoerd die onder het onderdeel **Pagina** vallen, worden de vereiste pagina-eindes automatisch toegevoegd. Tijdens dit proces wordt rekening gehouden met de grootte van de gegenereerde inhoud, de pagina-instelling van de Excel-sjabloon en het papierformaat dat is geselecteerd in de Excel-sjabloon.

Als u een gegenereerd document wilt opsplitsen in verschillende secties (die elk een andere paginering hebben), kunt u verschillende onderdelen **Pagina** configureren in elk onderdeel [Werkblad](er-fillable-excel.md#sheet-component).

### <a name="structure"></a><a name="page-component-structure"></a>Structuur

Als de eerste component onder het onderdeel **Pagina** een onderdeel [Bereik](er-fillable-excel.md#range-component) is waarbij de eigenschap **Replicatierichting** is ingesteld op **Geen replicatie**, wordt dit bereik beschouwd als paginakoptekst voor paginering die is gebaseerd op de instellingen van het huidige onderdeel **Pagina**. Het Excel-bereik dat aan dit opmaakonderdeel is gekoppeld, wordt herhaald boven aan elke pagina die wordt gegenereerd op basis van de instellingen van het huidige onderdeel **Pagina**.

> [!NOTE]
> Voor correcte paginering, als het bereik [Te herhalen rijen bovenaan](https://support.microsoft.com/office/repeat-specific-rows-or-columns-on-every-printed-page-0d6dac43-7ee7-4f34-8b08-ffcc8b022409) is geconfigureerd in uw Excel-sjabloon, moet het adres van dit Excel-bereik gelijk zijn aan het adres van het Excel-bereik dat is gekoppeld aan het eerder beschreven onderdeel **Bereik**.

Als de laatste component onder het onderdeel **Pagina** een onderdeel **Bereik** is waarbij de eigenschap **Replicatierichting** is ingesteld op **Geen replicatie**, wordt dit bereik beschouwd als paginavoettekst voor paginering die is gebaseerd op de instellingen van het huidige onderdeel **Pagina**. Het Excel-bereik dat aan dit opmaakonderdeel is gekoppeld, wordt herhaald onder aan elke pagina die wordt gegenereerd op basis van de instellingen van het huidige onderdeel **Pagina**.

> [!NOTE]
> Voor juiste paginering moeten de Excel-bereiken die zijn gekoppeld aan de onderdelen **Bereik**, niet van grootte worden veranderd tijdens runtime. Het is niet aan te raden cellen van dit bereik op te maken met behulp van de Excel-[opties](https://support.microsoft.com/office/wrap-text-in-a-cell-2a18cff5-ccc1-4bce-95e4-f0d4f3ff4e84) **Teruglooptekst in een cel** en **Rijhoogten automatisch aanpassen**.

U kunt meerdere andere onderdelen **Bereik** toevoegen tussen de optionele onderdelen **Bereik** om op te geven hoe een gegenereerd document wordt ingevuld.

Als de set geneste onderdelen **Bereik** onder het onderdeel **Pagina** niet voldoet aan de eerder beschreven structuur, treedt er een [validatiefout](er-components-inspections.md#i17) op tijdens het ontwerp in de ER-indelingsontwerper. In het foutbericht staat dat het probleem problemen kan veroorzaken tijdens runtime.

> [!NOTE]
> Als u de juiste uitvoer wilt genereren, geeft u geen binding op voor enig onderdeel **Bereik** onder het onderdeel **Pagina** als de eigenschap **Replicatierichting** voor dit onderdeel **Bereik** is ingesteld op **Geen replicatie** en het bereik zo is geconfigureerd dat paginakopteksten of paginavoetteksten worden gegenereerd.

Als u wilt paginagerelateerde totalen en tellingen lopende totalen en totalen per pagina berekenen, raden we de vereiste gegevensbronnen voor [Gegevensverzameling](er-data-collection-data-sources.md) te configureren. Als u wilt weten hoe u het onderdeel **Pagina** kunt gebruiken om een gegenereerd Excel-document te pagineren, voert u de procedures uit in [Een ER-indeling ontwerpen om gegenereerde documenten in Excel te pagineren](er-paginate-excel-reports.md).

### <a name="limitations"></a><a name="page-component-limitations"></a>Beperkingen

Wanneer u het onderdeel **Pagina** voor Excel-paginering gebruikt, weet u het definitieve aantal pagina's in een gegenereerd document pas als de paginering is voltooid. Het is dus niet mogelijk om het totale aantal pagina's te berekenen via ER-formules en het juiste aantal pagina's van gegenereerd document af te drukken op elke pagina vóór de laatste pagina.

> [!TIP]
> Dit resultaat wordt bereikt in een Excel-kop- of voettekst met behulp van de speciale [Excel-opmaak](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) voor kop- en voetteksten.

Er wordt geen rekening gehouden met geconfigureerde onderdelen **Pagina** wanneer u een Excel-sjabloon bijwerkt in de bewerkbare indeling in Dynamics 365 Finance versie 10.0.22. Deze functionaliteit wordt overwogen voor verdere releases van Finance.

Als u de Excel-sjabloon configureert voor het gebruik van [voorwaardelijke opmaak](/office/dev/add-ins/excel/excel-add-ins-conditional-formatting), werkt deze in sommige gevallen mogelijk niet zoals wordt verwacht.

### <a name="applicability"></a>Toepasbaarheid

Het onderdeel **Pagina** werkt alleen voor het indelingsonderdeel van het [Excel-bestand](er-fillable-excel.md#excel-file-component) als dat onderdeel is geconfigureerd voor gebruik van een sjabloon in Excel. Als u de Excel-sjabloon [vervangt](tasks/er-design-configuration-word-2016-11.md) door een Word-sjabloon en vervolgens de bewerkbare ER-indeling uitvoert, wordt het onderdeel **Pagina** genegeerd.

Het onderdeel **Pagina** werkt alleen als de functie **Gebruik van EPPlus-bibliotheek inschakelen in het ER-raamwerk** is ingeschakeld. Er verschijnt een uitzondering tijdens runtime als ER probeert het onderdeel **Pagina** te verwerken terwijl deze functie is uitgeschakeld.

> [!NOTE]
> Er verschijnt een uitzondering tijdens runtime als een ER-indeling het onderdeel **Pagina** verwerkt voor een Excel-sjabloon die minimaal één formule bevat die verwijst naar een cel die niet geldig is. Als u runtimefouten wilt voorkomen, corrigeert u de Excel-sjabloon zoals beschreven in [Het corrigeren van #REF! fout](https://support.microsoft.com/office/how-to-correct-a-ref-error-822c8e46-e610-4d02-bf29-ec4b8c5ff4be).

## <a name="footer-component"></a>Voettekstonderdeel

Het onderdeel **Voettekst** wordt gebruikt om voetteksten in te vullen onder aan een gegenereerd werkblad in een Excel-werkmap.

> [!NOTE]
> U kunt dit onderdeel voor elk onderdeel **Werkblad** toevoegen als u verschillende voetteksten voor verschillende werkbladen wilt opgeven in een gegenereerde Excel-werkmap.

Wanneer u een afzonderlijk onderdeel **Voettekst** configureert, kunt u de eigenschap **Vormgeving kop-/voettekst** gebruiken om de pagina's op te geven waarop het onderdeel wordt gebruikt. De volgende waarden zijn beschikbaar:

- **Alle**: voer het geconfigureerde onderdeel **Voettekst** uit voor alle pagina's van het bovenliggende Excel-werkblad.
- **Eerste**: voer het geconfigureerde onderdeel **Voettekst** uit voor alleen de eerste pagina van het bovenliggende Excel-werkblad.
- **Even**: voer het geconfigureerde onderdeel **Voettekst** uit voor alleen de even pagina's van het bovenliggende Excel-werkblad.
- **Oneven**: voer het geconfigureerde onderdeel **Voettekst** uit voor alleen de oneven pagina's van het bovenliggende Excel-werkblad.

Voor een enkel onderdeel **Werkblad** kunt u verschillende onderdelen **Voettekst** toevoegen. Deze onderdelen hebben een andere waarde voor de eigenschap **Vormgeving kop-/voettekst**. Op deze manier kunt u verschillende voetteksten genereren voor verschillende typen pagina's in een Excel-werkblad.

> [!NOTE]
> Zorg ervoor dat elk onderdeel **Voettekst** dat u toevoegt aan een enkel onderdeel **Werkblad** een andere waarde heeft voor de eigenschap **Vormgeving kop-/voettekst**. Als dit niet het geval is, treedt er een [validatiefout](er-components-inspections.md#i16) op. Het foutbericht dat u ontvangt, informeert u over de inconsistentie.

Voeg onder het onderdeel **Voettekst** de vereiste geneste onderdelen van de **Tekst\\Tekenreeks**, **Tekst\\Datum/tijd** of een ander type toe. Configureer de bindingen voor deze onderdelen om op te geven hoe de voettekst van uw pagina wordt ingevuld.

U kunt ook speciale [opmaakcodes](/office/vba/excel/concepts/workbooks-and-worksheets/formatting-and-vba-codes-for-headers-and-footers) gebruiken om de inhoud van een gegenereerde voettekst correct op te maken. Volg de stappen in [Voorbeeld 1](#example-1), verderop in dit onderwerp, om te weten te komen hoe u deze methode moet gebruiken.

> [!NOTE]
> Wanneer u ER-indelingen configureert, moet u rekening houden met de Excel-[limiet](https://support.microsoft.com/office/excel-specifications-and-limits-1672b34d-7043-467e-8e27-269d656771c3) en het maximale aantal tekens voor een enkele kop- of voettekst.

## <a name="header-component"></a>Koptekstonderdeel

Het onderdeel **Koptekst** wordt gebruikt om kopteksten in te vullen boven aan een gegenereerd werkblad in een Excel-werkmap. Dit wordt op dezelfde wijze gebruikt als het onderdeel **Voettekst**.

## <a name="edit-an-added-er-format"></a>Een toegevoegde ER-indeling bewerken

### <a name="update-a-template"></a>Een sjabloon bewerken

U kunt **Bijwerken vanuit Excel** selecteren op het tabblad **Importeren** van het actievenster om een bijgewerkte sjabloon te importeren in een bewerkbare ER-indeling. Tijdens dit proces wordt een sjabloon van het geselecteerde onderdeel **Excel\\Bestand** vervangen door een nieuwe sjabloon. De inhoud van de bewerkbare ER-indeling wordt gesynchroniseerd met de inhoud van de bijgewerkte ER-sjabloon.

- Er wordt automatisch een nieuw ER-indelingsonderdeel gemaakt voor elke Excel-naam als het ER-indelingsonderdeel niet wordt gevonden in de bewerkbare indeling.
- Elk ER-indelingsonderdeel wordt verwijderd uit de bewerkbare ER-indeling als de geschikte Excel-naam niet wordt gevonden.

> [!NOTE]
> Als u het optionele element **Werkblad** wilt maken in de bewerkbare ER-indeling, stelt u de optie **Indelingselement Excel-werkblad maken** in op **Ja**.
>
> Als de bewerkbare ER-indeling oorspronkelijk elementen van het type **Werkblad** bevatte, wordt u aangeraden de optie **Indelingselement Excel-werkblad maken** op **Ja** in te stellen wanneer u een bijgewerkte sjabloon importeert. Anders worden alle geneste elementen van het oorspronkelijke element **Werkblad** helemaal opnieuw gemaakt. Alle bindingen van de opnieuw gemaakte indelingselementen gaan in dat geval verloren in de bijgewerkte ER-indeling.

![De optie Indelingselement Excel-werkblad maken in het dialoogvenster Bijwerken vanuit Excel.](./media/er-excel-format-update-template.png)

Volg de stappen in de [Indelingen voor elektronische rapportage wijzigen door Excel-sjablonen opnieuw toe te passen](modify-electronic-reporting-format-reapply-excel-template.md) voor meer informatie over deze functie.

## <a name="validate-an-er-format"></a>Een ER-indeling valideren

Wanneer u een ER-indeling valideert die kan worden bewerkt, wordt een consistentiecontrole uitgevoerd om er zeker van te zijn dat de Excel-naam aanwezig is in de Excel-sjabloon die momenteel wordt gebruikt. U wordt op de hoogte gebracht van eventuele inconsistenties. Voor sommige inconsistenties wordt de optie voor het automatisch oplossen van problemen aangeboden.

![Foutbericht over validatie.](./media/er-excel-format-validate.png)

## <a name="control-the-calculation-of-excel-formulas"></a>De berekening van Excel-formules beheren

Wanneer een uitgaand document in een Microsoft Excel-werkmapindeling wordt gegenereerd, bevatten sommige cellen in dit document mogelijk Excel-formules. Wanneer de functie **Gebruik van EPPlus-bibliotheek inschakelen in het ER-raamwerk** is ingeschakeld, kunt u bepalen wanneer de formules worden berekend door de waarde van de [parameter](https://support.microsoft.com/office/change-formula-recalculation-iteration-or-precision-in-excel-73fc7dac-91cf-4d36-86e8-67124f6bcce4#ID0EAACAAA=Windows) **Berekeningsopties** te wijzigen in de Excel-sjabloon die wordt gebruikt:

- Selecteer **Automatisch** als u alle afhankelijke formules telkens opnieuw wilt berekenen wanneer een gegenereerd document wordt toegevoegd door nieuwe bereiken, cellen enzovoort.

    >[!NOTE]
    > Dit kan leiden tot een prestatieprobleem voor Excel-sjablonen die meerdere gerelateerde formules bevatten.

- Selecteer **Handmatig** om te voorkomen dat formuleherberekening wordt uitgevoerd wanneer een document wordt gegenereerd.

    >[!NOTE]
    > Herberekening van formules wordt handmatig uitgevoerd wanneer een gegenereerd document wordt geopend voor preview met Excel.
    > Gebruik deze optie niet als u een ER-bestemming configureert die uitgaat van het gebruik van een gegenereerd document zonder de preview in Excel (PDF-conversie, e-mailing enz.) omdat het gegenereerde document mogelijk geen waarden bevat in cellen die formules bevatten.

## <a name="example-1-format-footer-content"></a><a name="example-1"></a>Voorbeeld 1: inhoud van de voettekst opmaken

1. Gebruik de geleverde ER-configuraties om afdrukbaar FTI-document (vrije-tekstfactuur) te [genereren](er-generate-printable-fti-forms.md).
2. Controleer de voettekst van het gegenereerde document. De pagina bevat informatie over het huidige paginanummer en het totale aantal pagina's in het document.

    ![De voettekst van een gegenereerd document controleren in Excel-indeling.](./media/er-fillable-excel-footer-1.gif)

3. [Open](er-generate-printable-fti-forms.md#features-that-are-implemented-in-the-sample-er-format) in de ontwerper van de ER-indeling het voorbeeld van een ER-indeling voor controledoeleinden.

    De voettekst van het werkblad **Factuur** wordt gegenereerd op basis van de instellingen van twee onderdelen **Tekenreeks** die zich onder het onderdeel **Voettekst** bevinden:

    - Het eerste onderdeel **Tekenreeks** vult de volgende speciale opmaakcodes in om het toepassen van specifieke opmaak af te dwingen in Excel:

        - **&C**: hiermee lijnt u de voettekst in het midden uit.
        - **&"Segoe UI,Regular"&8**: de voettekst wordt weergegven in het lettertype "Segoe UI Regular" met een grootte van 8 punten.

    - Het tweede onderdeel **Tekenreeks** vult de tekst in die het huidige paginanummer en het totale aantal pagina's in het huidige document bevat.

    ![Het ER-indelingsonderdeel voor de voettekst valideren op de pagina Indelingsontwerper.](./media/er-fillable-excel-footer-2.png)

4. Pas de voorbeeld-ER-indeling aan om de voettekst van de huidige pagina te wijzigen:

    1. [Maak](er-quick-start2-customize-report.md#DeriveProvidedFormat) een afgeleide ER-indeling **Vrije-tekstfactuur (Excel) aangepast** op basis van de voorbeeld-ER-indeling.
    2. Voeg het eerste nieuwe stel onderdelen **Tekenreeks** toe voor het onderdeel **Voettekst** van het werkblad **Factuur**:

        1. Voeg een onderdeel **Tekenreeks** toe die de bedrijfsnaam links uitlijnt en deze weergeeft in het 8-punts lettertype "Segoe UI Regular" (**"&L&"Segoe UI,Regular"&8"**).
        2. Voeg een onderdeel **Tekenreeks** toe waarmee de bedrijfsnaam wordt ingevuld (**model.InvoiceBase.CompanyInfo.Name**).

    3. Voeg het tweede nieuwe stel onderdelen **Tekenreeks** toe voor het onderdeel **Voettekst** van het werkblad **Factuur**:

        1. Voeg een onderdeel **Tekenreeks** toe die de verwerkingsdatum rechts uitlijnt en deze weergeeft in het 8-punts lettertype "Segoe UI Regular" (**"&R&"Segoe UI,Regular"&8"**).
        2. Voeg een onderdeel **Tekenreeks** toe om de verwerkingsdatum in te vullen in een aangepaste notatie (**"&nbsp;"&DATEFORMAT(SESSIONTODAY(), "yyyy-MM-dd")**).

        ![Het ER-indelingsonderdeel voor de voettekst controleren op de pagina Indelingsontwerper.](./media/er-fillable-excel-footer-3.png)

    4. [Voltooi](er-quick-start2-customize-report.md#CompleteDerivedFormat) de conceptversie van de afgeleide ER-indeling **Vrije-tekstfactuur (Excel) aangepast**.

5. [Configureer](er-generate-printable-fti-forms.md#configure-print-management) afdrukbeheer om de afgeleide aangepaste ER-indeling **Vrije-tekstfactuur (Excel)** te gebruiken in plaats van de voorbeeld-ER-indeling.
6. Genereer een afdrukbaar FTI-document en controleer de voettekst van het gegenereerde document.

    ![De voettekst van een gegenereerd document controleren in Excel-indeling.](./media/er-fillable-excel-footer-4.gif)

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van elektronische rapportage](general-electronic-reporting.md)

[Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling](tasks\er-design-reports-openxml-2016-11.md)

[Indelingen voor elektronische rapportage wijzigen door Excel-sjablonen opnieuw toe te passen](modify-electronic-reporting-format-reapply-excel-template.md)

[Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen](tasks/er-horizontal-1.md)

[Afbeeldingen en vormen insluiten in documenten die u genereert met ER](electronic-reporting-embed-images-shapes.md)

[Elektronische rapportage (ER) configureren om gegevens op te halen in Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
