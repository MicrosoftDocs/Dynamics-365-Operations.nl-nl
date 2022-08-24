---
title: Afbeeldingen en vormen insluiten in documenten die u genereert met ER
description: In dit artikel wordt uitgelegd hoe u het hulpmiddel voor elektronische rapportage kunt gebruiken om bedrijfsdocumenten te genereren met ingesloten afbeeldingen en vormen.
author: kfend
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.custom: 27621
ms.assetid: ''
ms.search.form: EROperationDesigner, ERParameters
ms.openlocfilehash: 0bb652f245db93424aeadcaadf2ad393945e616b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280983"
---
# <a name="embed-images-and-shapes-in-documents-that-you-generate-by-using-er"></a>Afbeeldingen en vormen insluiten in documenten die u genereert met ER

[!include [banner](../includes/banner.md)]

Met het hulpmiddel Elektronische rapportage (ER) kunt u rapporten ontwerpen die u kunt uitvoeren om vereiste elektronische documenten te genereren. U kunt Microsoft Excel- of Microsoft Word-documenten gebruiken om de indeling van een rapport op te geven. In de ER Operations-ontwerper kunt u het Excel- of Word-document als sjabloon voor het rapport bijvoegen. De benoemde elementen in de gekoppelde sjabloon hangen samen met de indelingselementen van het ER-rapport. Indelingselementen van het rapport zijn gebonden aan gegevensbronnen. In deze elementen worden tijdens runtime de gegevens ingevoerd die worden gegenereerd.

Deze nieuwe functionaliteit gaat verder dan bestaande ER-capaciteiten voor het maken van documenten in Microsoft Office-indelingen. Speel voor meer informatie de volgende taakbegeleidingen af. U vindt deze taakbegeleidingen onder het bedrijfsproces 7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677).

- Een ER-configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling
- ER Een configuratie ontwerpen voor het genereren van rapporten in Microsoft WORD-indeling

## <a name="embed-an-image-in-an-excel-document"></a>Een afbeelding insluiten in een Excel-document

### <a name="embed-an-image-in-an-excel-worksheet"></a>Een afbeelding insluiten in een Excel-werkblad

Eerst moet u een tijdelijke aanduiding voor de afbeelding in een Excel-document toevoegen. Open een Excel-werkmap en voeg een afbeelding toe als tijdelijke aanduiding voor de afbeelding die u later wilt toevoegen. Gebruik vervolgens het ER-hulpmiddel om een nieuwe ER-indelingsconfiguratie toe te voegen voor het rapport dat u ontwerpt. Koppel de Excel-werkmap als sjabloon voor de indeling van het rapport en importeer vervolgens de inhoud van de werkmap in de ER-indeling. De indelingsdefinitie wordt automatisch gemaakt. De tijdelijke aanduiding voor de afbeelding die u hebt toegevoegd, wordt in de ER-indelingsdefinitie opgenomen als een **CEL**-element.

> [!NOTE]
> U kunt de indelingsdefinitie handmatig opgeven in plaats van deze te importeren. Wanneer u de wijzigingen opslaat, wordt de indeling gevalideerd.

Bind vervolgens het **CEL**-element van de ER-indeling aan het veld vanuit de gegevensbron van de indeling die de gegevens van de afbeelding in binaire indeling levert tijdens runtime. Wanneer een ER-gegevensmodel wordt gebruikt als de gegevensbron van een indeling, moet het gegevenstype van het veld [Container](er-formula-supported-data-types-composite.md#container) zijn. Een veld van het ER-gegevensmodel met het gegevenstype [Container](er-formula-supported-data-types-composite.md#container) kan op dit moment worden gebonden aan verschillende typen gegevensbronnen die afbeeldingen retourneren in binaire indeling. U kunt toegang krijgen tot een veld in een gegevenstabel en een bestand dat aan de record van de gegevenstabel is gekoppeld met behulp van het raamwerk voor documentbeheer.

> [!IMPORTANT]
> - Als u de tijdelijke aanduiding voor de afbeelding wilt invoegen in het document dat u maakt met de Excel-sjabloon, moet de ER-indeling het **CEL**-element bevatten dat verwijst naar het benoemde afbeeldingselement in de Excel-sjabloon. Anders worden er geen tijdelijke aanduidingen voor afbeeldingen in de uitvoer van het rapport weergegeven. Als de binding van een **CEL**-element geen gegevens retourneert tijdens runtime, wordt in het gegenereerde document de tijdelijke aanduiding van de sjabloon weergegeven. Als u een afbeelding in het document dat u genereert wilt verbergen, definieert u een **CEL**-element en geeft u op dat de expressie **Inschakelen** de waarde **FALSE** moet retourneren.
> - Gebruik in de Excel-sjabloon een unieke naam voor elk element. Deze elementen bevatten afbeeldingen en cellen. Als u een elementnaam dupliceert, is de inhoud van het gegenereerde rapport dubbelzinnig en verwarrend.

### <a name="embed-images-in-the-header-and-footer-of-an-excel-worksheet"></a>Afbeeldingen in de kop- en voettekst van een Excel-werkblad insluiten

Gebruik het Excel-werkmapdocument als sjabloon om de indeling van een rapport op te geven. De werkmap kan meerdere werkbladen bevatten, die elk ontworpen kunnen worden met een kop- en voettekst. Excel ondersteunt maximaal drie afbeeldingen in de kop- en voetteksten van elk werkblad. De afbeeldingen kunnen links, rechts of in het midden worden uitgelijnd.

In versie 10.0.21 van Finance kunt u de kop- en voettekstafbeeldingen beheren die worden gegenereerd door een ER-oplossing met een Excel-sjabloon.

Als u wilt dat er een standaardafbeelding wordt weergegeven in de kop- of voettekst van een gegenereerd document, kunt u een afbeelding toevoegen aan de kop- of voettekst van een werkblad van een ER-sjabloon. Voor toegang tot deze afbeelding in uw ER-indeling moet u het onderdeel **Afbeelding** toevoegen onder het onderdeel [Koptekst](er-fillable-excel.md#header-component) of [Voettekst](er-fillable-excel.md#footer-component) van de indeling. Configureer de uitlijning van het onderdeel **Afbeelding**. 

U kunt het onderdeel **Afbeelding** ook gebruiken om een afbeelding in de koptekst of voettekst van een gegenereerd document te zetten tijdens runtime, zelfs als de sjabloon geen standaardafbeelding bevat. Als u de media-inhoud wilt opgeven die in de koptekst of voettekst van een gegenereerd document moet worden geplaatst als een nieuwe afbeelding of als een vervanging voor een standaardafbeelding, moet u het onderdeel **Afbeelding** verbinden met een gegevensbron van het type [Container](er-formula-supported-data-types-composite.md#container) die een afbeelding in binaire indeling vertegenwoordigt.

Elke onderdeel **Koptekst** of **Voettekst** kan voor elke ondersteunde uitlijning één onderdeel **Afbeelding** gebruiken: **Links**, **Midden** en **Rechts**.

Met de eigenschap **Hoogte schalen** van het onderdeel **Afbeelding** kunt u de geconfigureerde binding gebruiken om de grootte van een afbeelding te bepalen:

- Selecteer **Oorspronkelijk** om de oorspronkelijke grootte van de afbeelding te behouden.
- Selecteer **Relatief** om de hoogte van de afbeelding te schalen in verhouding tot de hoogte van de kop- of voettekst met die afbeelding.

    - In dit geval moet de hoogte van de afbeelding worden gedefinieerd als een percentage van de bovenliggende kop- of voettekst.
    - Als de schaalwaarde 100 procent overschrijdt, overlapt de afbeelding mogelijk het gegevensgebied van het bijbehorende werkblad.
    - Als de hoogte van de afbeelding wordt gewijzigd wanneer de schaal wordt toegepast, wordt de breedte ook gewijzigd om de oorspronkelijke hoogte-breedteverhouding van de afbeelding te behouden.

- Selecteer **Absoluut** om de grootte van de afbeelding te wijzigen in de hoogte- en breedtewaarden (in pixels) die tijdens het ontwerp worden opgegeven.

    - Als de opgegeven hoogte hoger is dan de hoogte van de bovenliggende kop- of voettekst, overlapt de afbeelding mogelijk het gegevensgebied van het bijbehorende werkblad.

U kunt ook de eigenschap **Ingeschakeld** van het onderdeel **Afbeelding** gebruiken om de zichtbaarheid te controleren van een afbeelding die met dit onderdeel in een gegenereerd document wordt gemaakt.

> [!NOTE]
> U moet de ontwerper van de ER-indeling gebruiken om een onderdeel **Afbeelding** toe te voegen aan de bewerkbare ER-indeling. U kunt het onderdeel niet toevoegen wanneer u het werkgebied [Bedrijfsdocumentbeheer](er-business-document-management.md) gebruikt om de sjabloon van een bedrijfsdocument te bewerken.

Volg de stappen in [Een ER-indeling ontwerpen om een rapport in Excel-indeling te genereren met ingesloten afbeeldingen in paginakop- of voetteksten](er-embed-images-header-footer-excel-reports.md) voor meer informatie over deze functionaliteit.

## <a name="embed-a-shape-in-an-excel-document"></a>Een vorm insluiten in een Excel-document

Eerst moet u een tijdelijke aanduiding voor de vorm in een Excel-document toevoegen. Open een Excel-werkmap en selecteer **Vorm**, **Tekstvak** of **WordArt** als tijdelijke aanduiding voor de vorm. Gebruik vervolgens het ER-hulpmiddel om een nieuwe ER-indelingsconfiguratie toe te voegen voor het rapport dat u ontwerpt. Koppel de Excel-werkmap als sjabloon voor de indeling van het rapport en importeer vervolgens de inhoud van de werkmap in de ER-indeling. De indelingsdefinitie wordt automatisch gemaakt. De tijdelijke aanduiding voor de vorm die u hebt toegevoegd, wordt in de ER-indelingsdefinitie opgenomen als een **CEL**-element dat verwijst naar het benoemde Excel-vormelement.

> [!NOTE]
> U kunt de indelingsdefinitie handmatig opgeven in plaats van deze te importeren. Wanneer u de wijzigingen opslaat, wordt de indeling gevalideerd.

Bind vervolgens het **CEL**-element in de ER-indeling aan het veld vanuit de gegevensbron van de indeling die de gegevens levert tijdens runtime. Deze gegevens kunnen worden geconverteerd naar een tekstreeks. Wanneer het **CEL**-element in de ER-indeling verwijst naar een vormelement in de Excel-sjabloon dat tekst ondersteunt, wordt de tekst die door deze binding wordt geleverd tijdens runtime weergegeven in een vorm in het gegenereerde document.

> [!IMPORTANT]
> - Als u de Excel-sjabloon wilt gebruiken die de tijdelijke aanduiding voor de vorm bevat, moet de ER-indeling een **CEL**-element bevatten dat verwijst naar het Excel-vormelement. Anders worden er geen tijdelijke aanduidingen voor vormen in de uitvoer van het rapport weergegeven. Als de binding van een **CEL**-element dat verwijst naar het benoemde Excel-vormelement, tijdens runtime geen gegevens retourneert, wordt in het gegenereerde document de tekst van de tijdelijke aanduiding voor de vorm uit de Excel-sjabloon gegeven. Als u een vorm in het document dat u genereert wilt verbergen, definieert u een **CEL**-element dat verwijst naar het benoemde Excel-vormelement en geeft u op dat de expressie **Inschakelen** de waarde **FALSE** moet retourneren.
> - Gebruik in de Excel-sjabloon een unieke naam voor elk element. Deze elementen bevatten vormen en cellen. Als u een elementnaam dupliceert, is de inhoud van het gegenereerde rapport dubbelzinnig en verwarrend.

## <a name="embed-an-image-in-a-word-document"></a>Een afbeelding insluiten in een Word-document
> [!IMPORTANT]
> U kunt de ER-indeling die gebruikmaakt van een Excel-sjabloon opnieuw gebruiken om documenten met ingesloten afbeeldingen te maken. Zorg in de ER-indeling dat er een naam is opgegeven voor het **CEL**-element dat verwijst naar een benoemd afbeeldingselement in Excel, en dat dit is verbonden met een gegevensbron die een afbeelding tijdens runtime retourneert.

Eerst moet u de indeling van het Word-document configureren. Gebruik het besturingselement **Afbeeldingsinhoud** om een tijdelijke aanduiding te maken voor de ingesloten afbeelding. Voor toegang tot dit besturingselement moet u eerst het tabblad **Ontwikkelaar** zichtbaar maken in het Word-lint.

Verwijder vervolgens de Excel-sjabloon uit de ER-indeling en koppel het Word-sjabloondocument. Werk de verwijzing naar de sjabloon bij en sla de wijzigingen op. De structuur van de huidige ER-indeling wordt opgeslagen in de Word-sjabloon als een nieuw aangepast XML-onderdeel met de naam **Rapport**.

Sla vervolgens de Word-sjabloon voor de huidige ER-indeling op uw lokale computer op. Open de sjabloon en open het deelvenster **XML-toewijzing**. Zoek het aangepaste XML-gedeelte met de naam **Rapport** en wijs vervolgens naar het **CEL**-element in het ER-rapport aan dat is gebonden aan een gegevensbron die een afbeelding in binaire indeling retourneert. Wijs het artikel van dit XML-onderdeel toe aan het geselecteerde besturingselement **Afbeeldingsinhoud** en sla de wijzigingen op.

[![afbeeldingen insluiten.](./media/embed-images-shapes-01.png)](./media/embed-images-shapes-01.png)

Verwijder tot slot de Word-sjabloon uit de ER-indeling en koppel het Word-document dat de toegewezen aangepaste XML-onderdelen bevat. Werk de indelingsverwijzing naar de sjabloon bij en sla de wijzigingen op die u in deze ER-indeling hebt aangebracht.

## <a name="more-information"></a>Meer informatie
Om vertrouwd te worden met de details van deze functie, kunt u de set taakbegeleidingen **ER Rapporten in MS Office-indelingen maken met ingesloten afbeeldingen** gebruiken. In deze taakbegeleidingen wordt beschreven hoe u de afbeeldingen van een bedrijfslogo en de handtekening van een geautoriseerde persoon kunt insluiten in de betalingscheques die worden gegenereerd met behulp van het ER-hulpmiddel in Excel- en Word-documenten.

In de volgende tabel staan de bestanden die nodig zijn om de taakbegeleidingen **ER Rapporten in MS Office-indelingen maken met ingesloten afbeeldingen** te voltooien. Download de bestanden en sla deze op uw lokale computer op.

| Beschrijving                                          | Bestandsnaam                   |
|------------------------------------------------------|-----------------------------|
| Configuratie van model voor ER-gegevens                          | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| ER-indelingsconfiguratie                              | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Afbeelding met bedrijfslogo                                   | [png-bestand met bedrijfslogo](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Afbeelding met handtekening                                      | [png-bestand met afbeelding met handtekening](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Afbeelding met alternatieve handtekening                          | [Signature image 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Microsoft Word-sjabloon voor het afdrukken van betalingscheques  | [Cheque template Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |
| Microsoft Excel-sjabloon voor het afdrukken van betalingscheques | [Chequesjabloon.xlsx](https://download.microsoft.com/download/1/f/6/1f671963-73aa-48d5-ae69-45f21fe7dfb4/Cheque%20template.xlsx)        |

In de volgende afbeelding vindt u een voorbeeld van de proefafdruk voor een betalingscheque die is gegenereerd op basis van de Excel-sjabloon.

[![Proefafdruk van betalingscheque.](./media/embed-images-shapes-02.png)](./media/embed-images-shapes-02.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
