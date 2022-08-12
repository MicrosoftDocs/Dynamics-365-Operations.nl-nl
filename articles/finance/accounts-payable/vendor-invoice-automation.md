---
title: Factuurautomatisering voor gescande documenten
description: In dit artikel worden de functies beschreven die beschikbaar zijn voor end-to-end automatisering van leveranciersfacturen, zelfs facturen die bijlagen bevatten.
author: abruer
ms.date: 03/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoiceHeaderStagingListPage
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0449a13989bad45cf0456a2678e5724036d2af3d
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070689"
---
# <a name="invoice-automation-for-scanned-documents"></a>Factuurautomatisering voor gescande documenten

[!include [banner](../includes/banner.md)]

In dit artikel worden de gegevensentiteiten beschreven die beschikbaar zijn voor end-to-end automatisering van leveranciersfacturen, inclusief facturen met bijlagen.

Organisaties die hun crediteurprocessen willen stroomlijnen, wijzen het verwerken van facturen vaak aan als een van de belangrijke procesgebieden die efficiënter moeten worden gemaakt. In veel gevallen brengen deze organisaties de verwerking van papieren facturen onder bij met een externe OCR-provider (Optical Character Recognition). Ze ontvangen vervolgens machineleesbare factuurmetagegevens, samen met een gescande afbeelding van elke factuur. Ter ondersteuning van de automatisering wordt dan een oplossing voor het laatste stukje samengesteld, zodat deze artefacten in het factureringssysteem kunnen worden verwerkt Nu is dit laatste stukje automatisering standaard beschikbaar, door middel van een oplossing voor automatische factuurverwerking.

## <a name="solution-context"></a>Context van de oplossing

De oplossing voor factuurautomatisering schakelt een standaard-interface in, die factuurmetagegevens voor de factuurkoptekst en factuurregels kan accepteren, maar ook bijlagen die van toepassing op de factuur zijn. Alle externe systemen die artefacten genereren die compatibel zijn met deze interface, kunnen de feed zenden voor automatische verwerking van facturen en bijlagen.

In de volgende afbeelding ziet u een voorbeeldintegratiescenario, waarin Contoso samenwerkt met een OCR-provider voor verwerking van leverancierfacturen. De leveranciers van Contoso zenden hun facturen per e-mail naar de serviceprovider. Via de OCR-verwerking genereert de serviceprovider factuurmetagegevens (koptekst en/of regels) en een gescande afbeelding van de factuur. Een integratielaag zet deze artefacten vervolgens om, zodat deze verwerkt kunnen worden.

![Voorbeeldintegratiescenario.](media/vendor_invoice_automation_01.png)

Er zijn verschillende varianten van het voorgaande scenario mogelijk als factuurintegratie vereist is. Gegevensmigratie is een ander gebruiksvoorbeeld, waarbij deze interface kan worden gebruikt voor het maken van facturen en bijlagen.

### <a name="solution-components"></a>Onderdelen van de oplossing

De oplossing bestaat uit de volgende onderdelen:

+ Gegevensentiteiten voor de factuurkoptekst, de factuurregels en de factuurbijlagen
+ Uitzonderingsverwerking voor facturen
+ Een lezer voor het naast elkaar weergeven van bijlagen en facturen

De rest van dit artikel bevat gedetailleerde beschrijvingen van de onderdelen van deze oplossing.

## <a name="data-entities"></a>Gegevensentiteiten

Een gegevenspakket is de werkeenheid die moet worden verzonden, zodat factuurkopteksten, factuurregels en factuurbijlagen kunnen worden gemaakt. De volgende gegevensentiteiten worden gebruikt voor de artefacten waaruit het gegevenspakket bestaat:

+ Koptekst van leveranciersfactuur
+ leveranciersfactuurregel
+ Documentbijlage van leveranciersfactuur

De documentbijlage van de leveranciersfactuur is een nieuwe gegevensentiteit die als onderdeel van deze functie wordt geïntroduceerd. De entiteit koptekst van leveranciersfactuur is gewijzigd, zodat deze bijlagen ondersteunt. De entiteit leveranciersfactuurregel is niet voor deze functie gewijzigd.

Zie [Overzicht van Gegevensbeheer](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md) voor gedetailleerde informatie over gegevenspakketten. Zie [Gegevenspakketten verwerken en verbruiken in de oplossing Apps voor financiën en bedrijfsactiviteiten van Dynamics 365](../../fin-ops-core/dev-itpro/lcs-solutions/process-data-packages-lcs-solutions.md) voor informatie over het maken van gegevenspakketten met het werkgebied voor gegevensbeheer.

Als u snel testgegevens wilt genereren met facturen en bijlagen, voert u de volgende stappen uit.

1. Meld u aan bij uw exemplaar.
1. Ga naar **Leveranciers** > **Facturen** > **Openstaande leveranciersfacturen**.
1. Maak facturen met regels en bijlagen.

    > [!NOTE]
    > De bijlagen moeten koptekstbijlagen zijn. Momenteel ondersteunt de entiteit documentbijlage van leveranciersfactuur geen regelbijlagen.

1. Open het werkgebied **Gegevensbeheer**.
1. Maak een exporttaak die de entiteiten koptekst van leveranciersfactuur, leveranciersfactuurregel en documentbijlage van leveranciersfactuur bevat.
1. Exporteer de gegevens.
1. Download de geëxporteerde gegevens als een pakket. U kunt nu het pakket gebruiken om gegevens te importeren in doelexemplaren voor testdoeleinden.

### <a name="determining-the-legal-entity-for-an-invoice"></a>De rechtspersoon voor een factuur bepalen

Facturen die zijn geïmporteerd via de gegevenspakketten kunnen op twee manieren worden gekoppeld aan de rechtspersoon waartoe ze behoren:

+ De importtaak die de factuur verwerkt importeert deze in hetzelfde bedrijf waarin de taak is gepland in het werkgebied **Gegevensbeheer**. Met andere woorden, het bedrijf van de taak bepaalt tot welk bedrijf de factuur behoort.
+ Wanneer het gegevenspakket met facturen wordt verzonden naar Finance, kan de aanvrager (dat wil zeggen de integratietoepassing die wordt uitgevoerd buiten Finance) expliciet de id van het bedrijf noemen in de HTTP-aanvraag. In dit geval wordt de bedrijfscontext waarin de verwerkingstaak wordt uitgevoerd in Finance overschreven en de facturen worden geïmporteerd in het bedrijf dat is doorgegeven via de HTTP-aanvraag.

> [!NOTE]
> Dit gedrag is standaardgedrag voor gegevensbeheer. Hier wordt het in de context van facturen uitgelegd omwille van de volledigheid.

## <a name="exception-processing"></a>Uitzonderingen verwerken

In scenario's waarin leveranciersfacturen in apps voor financiën en bedrijfsactiviteiten komen door middel van integratie, moet er een eenvoudige manier zijn waarmee een lid van het team Crediteuren uitzonderingen of mislukte facturen kan verwerken en in behandeling zijnde facturen kan maken van mislukte facturen. Deze verwerking van uitzonderingen voor leveranciersfacturen maakt nu deel uit van apps voor financiën en bedrijfsactiviteiten.

### <a name="vendor-invoices-that-failed-to-import-list-page"></a>Lijstpagina Leveranciersfacturen waarvan import is mislukt

De nieuwe lijstpagina met factuuruitzonderingen is beschikbaar op **Leveranciers** > **Facturen** > **Importfouten** > **Leveranciersfacturen waarvan import is mislukt**. Op deze pagina ziet u alle leveranciersfactuurkoptekstrecords uit de faseringstabel van de gegevensentiteit Leveranciersfactuurkoptekst. U kunt dezelfde records weergeven vanuit de werkruimte **Gegevensbeheer**. Vanuit de werkruimte **Gegevensbeheer** kunt u ook dezelfde acties uitvoeren die beschikbaar zijn in de functie voor uitzonderingsverwerking. De functie voor het verwerken van uitzonderingen is geoptimaliseerd voor een functionele gebruiker, waardoor deze gemakkelijker te gebruiken is.

![Lijstpagina met uitzonderingen.](media/vendor_invoice_automation_02.png)

Deze pagina bevat de volgende velden die worden geleverd via de feed:

+ **Bedrijf**: het bedrijf waartoe de factuur behoort.
+ **Foutbericht**: het foutbericht dat het gegevensbeheerframework genereert om uit te leggen waarom de factuur niet kon worden gemaakt
+ **Nummer**: het factuurnummer.
+ **Factuurrekening**
+ **Naam**: de naam van de leverancier.
+ **Leveranciersrekening**
+ **Inkooporder**: het inkoopordernummer voor de factuur.
+ **Boekdatum**
+ **Factuurdatum**
+ **Factuuromschrijving**
+ **Valuta**
+ **Logboek**
+ **Regelverwijzing** : de id die afkomstig is van het externe systeem.

    > [!NOTE]
    > De regelverwijzing is niet de factuur-id.

Deze lijstpagina heeft ook een voorbeeldvenster dat u op de volgende manieren kunt gebruiken:

+ Het gehele foutbericht weergeven zodat u niet de kolom **Foutbericht** in het raster hoeft uit te vouwen.

De lijstpagina ondersteunt de volgende acties:

+ **Bewerken**: de uitzonderingsrecord openen in bewerkingsmodus, zodat u de problemen kunt oplossen.
+ **Opties**: toegang tot de standaardopties die beschikbaar zijn op de lijstpagina's. U kunt de optie **Toevoegen aan werkgebied** gebruiken om de lijstpagina met uitzonderingen aan uw werkgebied vast te maken als een lijst of tegel.

### <a name="vendor-invoices-that-failed-to-import-details-page"></a>Detailpagina Leveranciersfacturen waarvan import is mislukt

Wanneer u de bewerkingsmodus start, wordt de detailpagina **Leveranciersfacturen waarvan import is mislukt** voor de factuur met problemen geopend. Als er problemen zijn met een factuur die een bijlage bevat, wordt de bijlage niet weergegeven. De bijlage moet opnieuw aan de factuur worden toegevoegd.

Via de detailpagina **Leveranciersfacturen waarvan import is mislukt** kunt u een factuur in behandeling maken. Nadat u de problemen voor een factuur hebt opgelost als onderdeel van de verwerking van een uitzondering, kunt u de knop **Factuur in behandeling maken** selecteren om de factuur in behandeling te maken. De factuur in behandeling wordt op de achtergrond gemaakt. 

### <a name="shared-service-vs-organization-based-exception-processing"></a>Uitzonderingen verwerken met gedeelde service of op basis van organisatie

De lijstpagina met uitzonderingen ondersteunt de standaardbeveiligingsconcepten die het werkgebied **Gegevensbeheer** ondersteunt voor de verwerking van de faseringsrecords. De factuurimporttaak kan worden beveiligd op de volgende manieren:

+ Door gebruikersrol
+ Door gebruiker
+ Per rechtspersoon

![Importtaak die wordt beveiligd door de gebruikersrol en rechtspersoon.](media/vendor_invoice_automation_04.png)

Als beveiliging voor de factuurimporttaak is geconfigureerd, neemt de lijstpagina met uitzonderingen die instellingen over. Gebruikers kunnen alleen de factuuruitzonderingsrecords zien die zij volgens de configuratie mogen zien.

Contoso besluit bijvoorbeeld factuuruitzonderingen te verwerken op rechtspersoon. Daarom is beveiliging geconfigureerd op de factuurimporttaak, zodanig dat een gebruiker in rechtspersoon A alleen factuuruitzonderingen in rechtspersoon A kan zien en een gebruiker in rechtspersoon B alleen factuuruitzonderingen in rechtspersoon B. Met deze instelling brengt u scheiding van taken aan voor het beheer van factuuruitzonderingen.

Contoso zou ook kunnen besluiten om geen beveiliging in te stellen, zodat een gebruiker factuuruitzonderingen voor alle rechtspersonen kan verwerken. Deze instelling maakt een scenario met gedeelde services mogelijk voor voor beheer van de factuuruitzonderingen.

## <a name="side-by-side-attachment-viewer"></a>Viewer voor het naast facturen weergeven van bijlagen

Om u te helpen eenvoudig de bijlagen van leveranciersfacturen weer te geven, bevatten de volgende pagina's die worden gebruikt in het factureringsproces nu een bijlageviewer:

+ **Afhandeling van uitzonderingen**
+ Pagina **Leveranciersfacturen in behandeling** (ook beschikbaar in het controleproces voor de factuur)
+ Querypagina **Facturenjournaal** (voor geboekte facturen)

Dit is de belangrijkste functionaliteit die de bijlage-viewer biedt:

+ Alle typen bijlagen weergeven die Documentbeheer ondersteunt (bestanden, afbeeldingen, URL's en notities).
+ TIFF-bestanden met meerdere pagina's weergeven.
+ De volgende acties uitvoeren op afbeeldingsbestanden:
  + Delen van de afbeelding markeren.
  + Delen van de afbeelding blokkeren.
  + Notities toevoegen aan de afbeelding.
  + In- en uitzoomen op de afbeelding.
  + De afbeelding pannen.
  + Acties ongedaan maken en opnieuw uitvoeren.
  + Afbeelding aanpassen aan grootte.

> [!NOTE]
> Deze acties zijn alleen beschikbaar voor afbeeldingsbestanden (JPEG, TIFF, PNG, enzovoort). Eventuele wijzigingen die u in een afbeelding aanbrengt met behulp van deze acties worden opgeslagen in het afbeeldingsbestand. Op dit moment biedt de viewer bijlage geen versiebeheer of controlemogelijkheden.

### <a name="default-attachment"></a>Standaardbijlage

Als een leveranciersfactuur meerdere bijlagen heeft, kunt u een van de documenten instellen als de standaardbijlage op de pagina **Bijlagen**. De optie **Is standaardbijlage** is een nieuwe optie, die als onderdeel van deze functie is toegevoegd. Deze optie wordt ook weergegeven in de gegevensentiteit Documentbijlage van leveranciersfactuur. Daarom kan de standaardbijlage worden ingesteld via integraties.

U kunt slechts één document instellen als de standaard-bijlage. Nadat u een document hebt ingesteld als de standaardbijlage, wordt dit automatisch weergegeven in de bijlageviewer wanneer de factuur wordt geopend. Als u geen document instelt als de standaardbijlage, geeft de viewer niet automatisch een bijlage weer wanneer de factuur wordt geopend.

### <a name="showhide-invoice-attachments"></a>Factuurbijlagen weergeven/verbergen

Met een nieuwe knop die beschikbaar is op de querypagina's **Uitzonderingen verwerken**, **Factuur in behandeling** en **Facturenjournaal** kunt u de bijlage-viewer zichtbaar maken of verbergen.

## <a name="security"></a>Beveiliging

De volgende acties in de bijlageviewer worden gecontroleerd door middel van op rollen gebaseerde beveiliging:

+ Markeren
+ Blokkeren
+ Aantekeningen

### <a name="pending-vendor-invoices-page"></a>Pagina Leveranciersfacturen in behandeling

De volgende bevoegdheden bieden alleen-lezentoegang of lees-/schrijftoegang tot de bijlageviewer voor de acties markeren, blokkeren en aantekeningen:

+ **Afbeelding van leveranciersfactuur onderhouden**: deze bevoegdheid biedt toegang voor lezen/schrijven.
+ **Afbeelding van leveranciersfactuur bekijken**: deze bevoegdheid biedt alleen-lezentoegang.

De volgende functies bieden alleen-lezentoegang of lees-/ schrijftoegang tot de bijlageviewer voor deze acties:

+ **Leveranciersfacturen onderhouden**: de bevoegdheid Afbeelding van leveranciersfactuur onderhouden is toegewezen aan deze functie.
+ **Informeren naar status van leveranciersfacturen**: de bevoegdheid Afbeelding van leveranciersfactuur bekijken is toegewezen aan deze functie.

De volgende rollen bieden alleen-lezentoegang of lees-/ schrijftoegang tot de bijlageviewer voor deze acties:

+ **Leveranciersmedewerker** en **Leveranciersmanager** : de functie Leveranciersfacturen onderhouden is toegewezen aan deze rollen.
+ **Leveranciersmedewerker**, **Leveranciersmanager**, **Medewerker gecentraliseerde klantenbetalingen** en **Leveranciersadministrateur**: de functie Informeren naar status van leveranciersfacturen is toegewezen aan deze rollen.

### <a name="vendor-invoice-attachment"></a>Leveranciersfactuurbijlage

De volgende bevoegdheden bieden alleen-lezentoegang of lees-/schrijftoegang tot de bijlageviewer voor de acties markeren, blokkeren en aantekeningen.

> [!NOTE]
> Standaard bieden de rollen die worden vermeld in deze sectie alleen-lezen toegang tot de factuurafbeeldingen in de bijlage-viewer. Als een rol ook schrijftoegang tot de afbeeldingen moet hebben, kunt u schrijftoegang aan die rol verlenen door middel van de machtiging en functie die hier worden beschreven.

+ **Afbeelding van entiteit koptekst van leveranciersfactuur onderhouden**: deze bevoegdheid geeft lees-/schrijftoegang tot de factuurafbeeldingen in de bijlage-viewer.
+ **Afbeelding van entiteit koptekst van leveranciersfactuur bekijken**: deze bevoegdheid geeft alleen-lezentoegang tot de factuurafbeelding in de bijlage-viewer.

De volgende functies bieden alleen-lezentoegang of tot de bijlageviewer voor deze acties:

+ **Leveranciersfacturen onderhouden**: de bevoegdheid Afbeelding van entiteit koptekst van leveranciersfactuur onderhouden is toegewezen aan deze functie.

De volgende rollen bieden alleen-lezentoegang of tot de bijlageviewer voor deze acties:

+ **Leveranciersmedewerker** en **Leveranciersmanager** : de functie Leveranciersfacturen onderhouden is toegewezen aan deze rollen.

Als de gebruikersrol bewerkingsrechten op een pagina biedt, heeft de gebruiker standaard ook bewerkingsrechten voor de bijlagenviewer voor de acties markeren, blokkeren en aantekeningen. Als er echter scenario's zijn waarin een specifieke rol moet beschikken over bewerkingsrechten voor de pagina, maar niet voor de bijlageviewer, kunnen de betreffende bevoegdheden uit de voorgaande lijst worden gebruikt om te voldoen aan de use-case.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

