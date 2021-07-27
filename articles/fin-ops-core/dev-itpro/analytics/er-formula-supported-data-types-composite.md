---
title: Ondersteunde samengestelde gegevenstypen voor formules voor elektronische rapportage
description: Dit onderwerp biedt informatie over de samengestelde gegevenstypen die worden ondersteund in ER-formules (Elektronische rapportage).
author: NickSelin
ms.date: 06/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2593f3128ec103248e109f3c80f48b9d7a035f54
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6355341"
---
# <a name="supported-composite-data-types-for-electronic-reporting-formulas"></a>Ondersteunde samengestelde gegevenstypen voor formules voor elektronische rapportage

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt informatie over de samengestelde gegevenstypen die worden ondersteund in expressies voor [Elektronische rapportage (ER)](general-electronic-reporting.md). De samengestelde gegevenstypen zijn [klasse](#class), [container](#container), [record](#record), [recordlijst](#record-list) en [object](#object).

## <a name="class"></a><a name="class"></a>Klasse

Het gegevenstype *klasse* verwijst naar een klasse voor een openbare toepassing. In ER wordt dit voorgesteld als een [*record*](#record) die een afzonderlijk veld bevat voor elke openbare methode van de klasse waarnaar wordt verwezen. Wanneer de parameteraanroep van de methode wordt uitgevoerd, moet u ook de vereiste argumenten van de juiste typen opgeven in een ER-expressie die is geconfigureerd voor het aanroepen van de methode.

In [toewijzing](general-electronic-reporting.md#data-model-and-model-mapping-components)s- en [indeling](general-electronic-reporting.md#FormatComponentOutbound)sonderdelen voor ER kunt u de gegevensbron **Klasse** toevoegen die wordt weergegeven als gegevensbron en die een waarde van het type *klasse* retourneert. Deze gegevensbron maakt openbare methoden van de klasse beschikbaar die tijdens runtime kunnen worden aangeroepen.

> [!NOTE]
> Alleen methoden die een waarde retourneren, kunnen worden aangeroepen vanuit ER-expressies.
>
> Alleen methoden met een bereik van nul tot acht argumenten kunnen worden aangeroepen vanuit ER-expressies.

De standaardwaarde van een *klasse* is **null**.

Hieronder ziet u een voorbeeld van hoe de gegevensbron **Systeeminformatie (xInfo)** van het type **Klasse** wordt toegevoegd om het exemplaar van de **xInfo**-toepassingsklasse te maken en de methode **productName()** aan te roepen om de naam van de huidige toepassing te ontvangen. De naam van de huidige toepassing wordt opgehaald tijdens runtime door de binding `xInfo.productName` uit te voeren die is geconfigureerd voor het veld **Softwarenaam (SoftwareName)** van het ER-gegevensmodel. Via deze binding wordt de methode `productName()` van de **xInfo**-toepassingsklasse aangeroepen die in de huidige modeltoewijzing wordt weergegeven als de gegevensbron **Systeeminformatie (xInfo)**.

[![De gegevensbron Klasse configureren in de ontwerper van ER-modeltoewijzingen.](./media/er-formula-supported-data-types-composite-class1.gif)](./media/er-formula-supported-data-types-composite-class1.gif)

In de volgende afbeelding wordt getoond hoe de ER-indeling wordt geconfigureerd om de opgegeven toepassingsnaam in gegenereerde documenten te plaatsen. Het veld **Softwarenaam (SoftwareName)** van het gebruikte gegevensmodel is gebonden aan het onderdeel **Tekenreeks** dat is genest onder het XML-element **softwareUsed** van de ER-indeling. Daarom wordt de naam van de huidige toepassing tijdens runtime in het XML-element **softwareUsed** van een gegenereerd document in XML-indeling geplaatst.

[![De structuur van een elektronisch uitgaand document configureren in de ontwerper van de ER-indeling.](./media/er-formula-supported-data-types-composite-class2.png)](./media/er-formula-supported-data-types-composite-class2.png)

## <a name="container"></a><a name="container"></a>Container

Het gegevenstype *container* bevat binaire inhoud. De waarde voor *container* kan worden gebruikt om specifieke informatie door te geven vanuit de opslag naar een gegenereerd document. In het ER-raamwerk wordt dit gegevenstype vaak gebruikt om mediainhoud zoals een bedrijfslogo in gegenereerde documenten te plaatsen.

> [!NOTE]
> Hoewel elk media-item kan worden weergegeven als een *container*-waarde, vertegenwoordigt niet elke *container*-waarde een media-item. Als u daarom een ER-indeling configureert zodat met een *container* een afbeelding in gegenereerde documenten wordt geplaatst, maar de *container* waarnaar wordt verwezen geen mediainhoud retourneert, kan een uitzondering optreden vergelijkbaar met het volgende voorbeeld: "Fout bij uitvoeren van code: binair (object), methode constructFromContainer aangeroepen met ongeldige parameters".

De standaardwaarde van een *container* is **null**.

In de volgende afbeelding wordt weergegeven hoe het veld **Bitmap (afbeelding)** van het type *Container* wordt gebonden aan het veld **Logo** van het gegevensmodel van het type **Container** in de modeltoewijzing **Verkoopfactuur**. Deze binding zorgt ervoor dat het bedrijfslogo beschikbaar is voor elke ER-indeling die is ontworpen voor de basisdefinitie **SalesInvoice** en die deze modeltoewijzing gebruikt tijdens runtime.

[![Een veld van het type Container in de ontwerper van ER-modeltoewijzingen verbinden.](./media/er-formula-supported-data-types-composite-container.png)](./media/er-formula-supported-data-types-composite-container.png)

## <a name="record"></a><a name="record"></a>Registreren

Een *record* is een verzameling benoemde velden die elk zijn gekoppeld aan een waarde van een [primitief](er-formula-supported-data-types-primitive.md) gegevenstype of een samengesteld gegevenstype. Meestal wordt een *record* gebruikt om één record van een recordlijst weer te geven. In dit geval vertegenwoordigt elk item afzonderlijke velden, methoden en relaties.

De standaardwaarde van een *record* is **leeg**.

> [!NOTE]
> Wanneer u de waarde van een veld van een lege *record* ophaalt, wordt de standaardwaarde van het betreffende gegevenstype geretourneerd.

U kunt een *record* verkrijgen met de volgende functies:

- [FIRST](er-functions-list-first.md)
- [FIRSTORNULL](er-functions-list-firstornull.md)
- [EMPTYRECORD](er-functions-record-emptyrecord.md)
- [NULLCONTAINER](er-functions-record-nullcontainer.md)

Zie [Lijst met ER-functies in de lijstcategorie](er-functions-category-list.md) voor meer informatie over de transformatie van waarden voor *record*.

## <a name="record-list"></a><a name="record-list"></a>Recordlijst

Een *recordlijst* is een lijst met items van het type *record*. Meestal wordt een *recordlijst* gebruikt om de lijst met records weer te geven die uit een databasetabel zijn opgehaald.

Records van een *recordlijst* zijn standaard opeenvolgend toegankelijk. Voor toegang tot een specifieke record kunt u de functie [INDEX](er-functions-list-index.md) gebruiken en de index voor *geheel getal* opgeven.

De standaardwaarde van een *recordlijst* is **leeg**. Met de functie [ISEMPTY](/er-functions-list-isempty.md) kunt u beoordelen of een *recordlijst* leeg is.

> [!NOTE]
> Als een *recordlijst* leeg is, zorgt elke poging om een veldwaarde op te halen voor een *record* in de record ervoor dat tijdens runtime een uitzondering optreedt. Zie [Controle op lege lijstcases](er-components-inspections.md#i9) om te weten te komen hoe u runtime-uitzonderingen van dit type kunt voorkomen.

U kunt een *recordlijst* initiëren met de volgende functies:

- [ALLITEMS](er-functions-list-allitems.md)
- [ALLITEMSQUERY](er-functions-list-allitemsquery.md)
- [EMPTYLIST](er-functions-list-emptylist.md)
- [LIST](er-functions-list-list.md)
- [LISTDISTINCT](er-functions-list-listdistinct.md)

Zie [Lijst met ER-functies in de lijstcategorie](er-functions-category-list.md) voor meer informatie over de transformatie van waarden voor *recordlijst*. Als u wilt weten hoe u items van *recordlijst* moet introduceren, vult u deze in met de toepassingsgegevens en gebruikt u de gegevens om bedrijfsdocumenten te genereren. Zie [Een nieuwe ER-oplossing ontwerpen om een aangepast rapport af te drukken](er-quick-start1-new-solution.md).

## <a name="object"></a><a name="object"></a>Object

Een *object* verwijst naar een stateful exemplaar van een *klasse*. Meestal wordt een *object* gestart in broncode. Vervolgens wordt het doorgegeven aan een ER-modeltoewijzing en worden details over de uitvoeringcontext verschaft.

De standaardwaarde van een *object* is **null**.

In de volgende afbeelding ziet u hoe de **ReportDataContract**-gegevensbron van het type *Object* wordt toegevoegd om informatie over een gegenereerde factuur vanuit de broncode door te geven aan de modeltoewijzing **Projectfactuur**. De tekst van het factuurexemplaar wordt bijvoorbeeld doorgegeven als onderdeel van de uitvoeringcontext. Deze tekst wordt ontleend aan de broncode tijdens runtime door de binding `ReportDataContract.parmInvoiceInstanceText` uit te voeren die voor het veld **Notitie** van het ER-gegevensmodel is geconfigureerd. Via deze binding wordt de methode `parmInvoiceInstanceText()` van de toepassingsklasse **PSAProjInvoiceContract** aangeroepen die in de huidige modeltoewijzing wordt weergegeven als de gegevensbron **ReportDataContract**.

[![De gegevensbron Object configureren in de ontwerper van ER-modeltoewijzingen.](./media/er-formula-supported-data-types-composite-object.gif)](./media/er-formula-supported-data-types-composite-object.gif)

Zie [Toepassingsobjecten ontwikkelen voor het aanroepen van het ontworpen rapport](er-quick-start1-new-solution.md#DevelopCustomCode) voor meer informatie over het doorgeven van details van de uitvoeringscontext vanuit broncode naar de actieve ER-oplossing.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage](general-electronic-reporting.md)
- [Formuletaal in Elektronische rapportage](er-formula-language.md)
- [Ondersteunde primitieve gegevenstypen](er-formula-supported-data-types-primitive.md)
