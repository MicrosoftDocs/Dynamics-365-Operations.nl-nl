---
title: Een configuratie ontwerpen voor het genereren van documenten in Excel-indeling
description: Dit onderwerp bevat informatie over het ontwerpen van een ER-indeling (Elektronische rapportage) voor het invullen van een Excel-sjabloon en het genereren van uitgaande Excel-documenten.
author: NickSelin
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e889b08f10c5d0c95fed7c9e422340706bdd154a
ms.sourcegitcommit: 67ce81c57194afb26a04ae4c0b7509e0efa32afc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/14/2020
ms.locfileid: "3375808"
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

![Pagina Configuraties](./media/er-excel-format-add-format.png)

## <a name="excel-file-component"></a>Excel-bestandsonderdeel

### <a name="manual-entry"></a>Handmatige invoer

U moet een onderdeel **Excel\\Bestand** toevoegen aan de geconfigureerde ER-indeling om een uitgaand document in Excel-indeling te genereren.

![Onderdeel Excel\Bestand](./media/er-excel-format-add-file-component.png)

Als u de indeling van het uitgaande document wilt opgeven, voegt u een Excel-werkmap met de extensie .xlsx toe aan het onderdeel **Excel\\Bestand** als sjabloon voor uitgaande documenten.

> [!NOTE]
> Wanneer u handmatig een sjabloon toevoegt, moet u een [documenttype](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) gebruiken dat in de [ER-parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) voor dat doel is geconfigureerd.

![Een bijlage toevoegen aan het onderdeel Excel\Bestand](./media/er-excel-format-add-file-component2.png)

Als u wilt opgeven hoe de toegevoegde sjabloon wordt ingevuld wanneer u de geconfigureerde ER-indeling uitvoert, moet u geneste onderdelen **Werkblad**, **Bereik** en **Cel** toevoegen aan het onderdeel **Excel\\Bestand**. Elk genest onderdeel moet worden gekoppeld aan een benoemd Excel-item.

### <a name="template-import"></a>Sjabloonimport

U kunt **Importeren uit Excel** selecteren op het tabblad **Importeren** van het actievenster om een nieuwe sjabloon te importeren in een lege ER-indeling. In dit voorbeeld wordt automatisch een onderdeel **Excel\\Bestand** gemaakt en de geïmporteerde sjabloon wordt hieraan toegevoegd. Alle vereiste ER-onderdelen worden ook automatisch gemaakt, op basis van de lijst met Excel-artikelen die worden ontdekt.

![Importeren uit Excel selecteren](./media/er-excel-format-import-template.png)

> [!NOTE]
> Als u het optionele element **Werkblad** wilt maken in de bewerkbare ER-indeling, stelt u de optie **Indelingselement Excel-werkblad maken** in op **Ja**.

## <a name="sheet-component"></a>Het onderdeel Werkblad

Het onderdeel **Werkblad** geeft een werkblad aan van de bijgevoegde Excel-werkmap die moet worden ingevuld. De naam van het werkblad in een Excel-sjabloon wordt gedefinieerd in het eigenschap **Werkblad** van dit onderdeel.

> [!NOTE]
> Dit onderdeel is optioneel voor Excel-werkmappen die één werkblad bevatten.

Op het tabblad **Toewijzing** van de ER Operations-ontwerper kunt u de eigenschap **Ingeschakeld** voor een onderdeel **Werkblad** configureren om op te geven of het onderdeel in een gegenereerd document moet worden geplaatst:

- Als een expressie van de eigenschap **Ingeschakeld** is geconfigureerd om **Waar** te retourneren tijdens runtime, of als er helemaal geen expressie is geconfigureerd, wordt het betreffende werkblad in het gegenereerde document geplaatst.
- Als een expressie van de eigenschap **Ingeschakeld** is ingesteld om **Onwaar** te retourneren tijdens runtime, bevat het gegenereerde document geen werkblad.

![Voorbeeld van een onderdeel Werkblad](./media/er-excel-format-sheet-component.png)

## <a name="range-component"></a>Het onderdeel Bereik

Het onderdeel **Bereik** geeft een Excel-bereik aan dat moet worden beheerd door dit ER-onderdeel. De naam van het bereik wordt gedefinieerd in het eigenschap **Excel-bereik** van dit onderdeel.

De eigenschap **Replicatierichting** geeft aan of en hoe het bereik wordt herhaald in een gegenereerd document:

- Als de eigenschap **Replicatierichting** is ingesteld op **Geen replicatie**, wordt het betreffende Excel-bereik niet herhaald in het gegenereerde document.
- Als de eigenschap **Replicatierichting** is ingesteld op **Verticaal**, wordt het betreffende Excel-bereik herhaald in het gegenereerde document. Elk gerepliceerd bereik wordt onder het oorspronkelijke bereik in een Excel-sjabloon geplaatst. Het aantal herhalingen wordt gedefinieerd door het aantal records in een gegevensbron van het type **Recordlijst** dat is gekoppeld aan dit ER-onderdeel.
- Als de eigenschap **Replicatierichting** is ingesteld op **Horizontaal**, wordt het betreffende Excel-bereik herhaald in het gegenereerde document. Elk gerepliceerd bereik wordt rechts van het oorspronkelijke bereik in een Excel-sjabloon geplaatst. Het aantal herhalingen wordt gedefinieerd door het aantal records in een gegevensbron van het type **Recordlijst** dat is gekoppeld aan dit ER-onderdeel.

Als u meer wilt weten over horizontale replicatie, volgt u de stappen in [Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen](tasks/er-horizontal-1.md).

Het onderdeel **Bereik** kan andere geneste ER-onderdelen bevatten die worden gebruikt om waarden op te geven in de toepasselijke benoemde Excel-bereiken.

- Als een deel van de groep **Tekst** wordt gebruikt om waarden in te voeren, wordt de waarde in een Excel-bereik ingevoerd als tekstwaarde.

    > [!NOTE]
    > Gebruik dit patroon om ingevoerde waarden op te maken op basis van de landinstelling die in de toepassing is gedefinieerd.

- Als het onderdeel **Cel** van de groep **Excel** wordt gebruikt om waarden in te voeren, wordt de waarde in een Excel-bereik ingevoerd als een waarde van het gegevens type dat wordt gedefinieerd door de binding van dat onderdeel **Cel** (bijvoorbeeld **Tekenreeks**, **Werkelijk** of **Geheel getal**).

    > [!NOTE]
    > Gebruik dit patroon om de ingevoerde waarden in de Excel-toepassing op te maken op basis van de landinstelling van de lokale computer waarop het uitgaande document wordt geopend.

Op het tabblad **Toewijzing** van de ER Operations-ontwerper kunt u de eigenschap **Ingeschakeld** voor een onderdeel **Bereik** configureren om op te geven of het onderdeel in een gegenereerd document moet worden geplaatst:

- Als een expressie van de eigenschap **Ingeschakeld** is geconfigureerd om **Waar** te retourneren tijdens runtime, of als er helemaal geen expressie is geconfigureerd, wordt het betreffende bereik in het gegenereerde document ingevuld.
- Als een expressie van de eigenschap **Ingeschakeld** is geconfigureerd om **Onwaar** te retourneren tijdens runtime en als dit bereik niet alle rijen of kolommen vertegenwoordigt, wordt het betreffende bereik niet in het gegenereerde document ingevuld.
- Als een expressie van de eigenschap **Ingeschakeld** is geconfigureerd om **Onwaar** te retourneren tijdens runtime en als dit bereik alle rijen of kolommen vertegenwoordigt, bevat het gegenereerde document die rijen en kolommen als verborgen rijen en kolommen.

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

## <a name="edit-an-added-er-format"></a>Een toegevoegde ER-indeling bewerken

### <a name="update-a-template"></a>Een sjabloon bewerken

U kunt **Bijwerken vanuit Excel** selecteren op het tabblad **Importeren** van het actievenster om een bijgewerkte sjabloon te importeren in een bewerkbare ER-indeling. Tijdens dit proces wordt een sjabloon van het geselecteerde onderdeel **Excel\\Bestand** vervangen door een nieuwe sjabloon. De inhoud van de bewerkbare ER-indeling wordt gesynchroniseerd met de inhoud van de bijgewerkte ER-sjabloon.

- Er wordt automatisch een nieuw ER-indelingsonderdeel gemaakt voor elke Excel-naam als het ER-indelingsonderdeel niet wordt gevonden in de bewerkbare indeling.
- Elk ER-indelingsonderdeel wordt verwijderd uit de bewerkbare ER-indeling als de geschikte Excel-naam niet wordt gevonden.

> [!NOTE]
> Als u het optionele element **Werkblad** wilt maken in de bewerkbare ER-indeling, stelt u de optie **Indelingselement Excel-werkblad maken** in op **Ja**.
>
> Als de bewerkbare ER-indeling oorspronkelijk elementen van het type **Werkblad** bevatte, wordt u aangeraden de optie **Indelingselement Excel-werkblad maken** op **Ja** in te stellen wanneer u een bijgewerkte sjabloon importeert. Anders worden alle geneste elementen van het oorspronkelijke element **Werkblad** helemaal opnieuw gemaakt. Alle bindingen van de opnieuw gemaakte indelingselementen gaan in dat geval verloren in de bijgewerkte ER-indeling.

![De optie Indelingselement Excel-werkblad maken in het dialoogvenster Bijwerken vanuit Excel](./media/er-excel-format-update-template.png)

Volg de stappen in de [Indelingen voor elektronische rapportage wijzigen door Excel-sjablonen opnieuw toe te passen](modify-electronic-reporting-format-reapply-excel-template.md) voor meer informatie over deze functie.

## <a name="validate-an-er-format"></a>Een ER-indeling valideren

Wanneer u een ER-indeling valideert die kan worden bewerkt, wordt een consistentiecontrole uitgevoerd om er zeker van te zijn dat de Excel-naam aanwezig is in de Excel-sjabloon die momenteel wordt gebruikt. U wordt op de hoogte gebracht van eventuele inconsistenties. Voor sommige inconsistenties wordt de optie voor het automatisch oplossen van problemen aangeboden.

![Foutbericht over validatie](./media/er-excel-format-validate.png)


## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van elektronische rapportage](general-electronic-reporting.md)

[Een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling](tasks\er-design-reports-openxml-2016-11.md)

[Indelingen voor elektronische rapportage wijzigen door Excel-sjablonen opnieuw toe te passen](modify-electronic-reporting-format-reapply-excel-template.md)

[Horizontaal uitvouwbare bereiken gebruiken om kolommen in Excel-rapporten dynamisch toe te voegen](tasks/er-horizontal-1.md)

[Afbeeldingen en vormen insluiten in documenten die u genereert met ER](electronic-reporting-embed-images-shapes.md)

[Elektronische rapportage (ER) configureren om gegevens op te halen in Power BI](general-electronic-reporting-report-configuration-get-data-powerbi.md)
