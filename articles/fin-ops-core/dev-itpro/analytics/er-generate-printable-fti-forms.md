---
title: Afdrukbare FTI-formulieren genereren
description: In dit onderwerp wordt uitgelegd hoe het raamwerk voor elektronische rapportage (ER) kan worden gebruikt voor het genereren van afdrukbare vrije-tekstfactuurformulieren (FTI) als Microsoft Office-documenten.
author: NickSelin
manager: AnnBe
ms.date: 07/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 168cef1b5f5d48cb739b08fa395c1bcd62089494
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686719"
---
# <a name="generate-printable-fti-forms"></a>Afdrukbare FTI-formulieren genereren

[!include[banner](../includes/banner.md)]

Met het raamwerk voor elektronische rapportage (ER) kunt u afdrukbare vrije-tekstfactuurformulieren (FTI) genereren als Microsoft Office-documenten. Dit onderwerp bevat informatie over het bouwen van uw eigen configuraties, evenals details van beschikbare configuratiesjablonen.

## <a name="overview"></a>Overzicht

Naast de bestaande mogelijkheid van het genereren van afdrukbare FTI-formulieren met behulp van Microsoft SQL Server Reporting Services (SSRS), kunt u hiervoor nu ook het ER-raamwerk gebruiken. U kunt afdrukbare FTI-formulieren beheren in Microsoft Office Excel en Word. U kunt ook de lay-out, gegevensstroom en opmaak wijzigen om in specifieke behoeften te voorzien zonder codewijzigingen uit te voeren.

> [!NOTE]
> Als u wilt beginnen met een overzicht van bestaande ER-configuraties voor dit voorbeeld van de oplossing voor afdrukbare FTI-formulieren, gaat u rechtstreeks naar de sectie **Voorbeelden van ER-configuraties voor het genereren van afdrukbare FTI-formulieren downloaden** verderop in dit onderwerp.

## <a name="create-customized-configurations-for-fti-printable-forms"></a>Aangepaste configuraties maken voor afdrukbare FTI-formulieren
Als onderdeel van uw aangepaste oplossing voor afdrukbare FTI-formulieren, moet u een reeks ER-configuraties maken.

### <a name="configure-the-er-data-model"></a>Het ER-gegevensmodel configureren
Uw toepassing moet de configuratie van het ER-gegevensmodel bevatten die een gegevensmodel bevat waarmee het bedrijfsdomein voor klantfacturering wordt beschreven. Als vereiste geldt dat de naam van het gegevensmodel **CustomersInvoicing** moet zijn. Zie [ER Ontwerp domeinspecifiek gegevensmodel](tasks/er-design-domain-specific-data-model-2016-11.md) voor informatie over het ontwerpen van ER-gegevensmodellen.

### <a name="configure-the-er-model-mapping"></a>De ER-modeltoewijzing configureren
Uw toepassing moet de toewijzing van het ER-model voor het gegevensmodel CustomersInvoicing bevatten. De modeltoewijzing kan plaatsvinden in de configuratie van het ER-gegevensmodel of in de configuratie van de ER-modeltoewijzing. De naam van de basisdescriptor van de modeltoewijzing moet echter **FreeTextInvoice** zijn.

De toewijzing moet de volgende gegevensbronnen bevatten:

- Type gegevensbron: **Tabelrecords**

    - Deze gegevensbron moet de naam **CustInvoiceJour** hebben.
    - Deze moet verwijzen naar de toepassingstabel CustInvoiceJour.
    - Deze wordt gebruikt tijdens de uitvoering om de lijst met facturen die zijn geselecteerd voor het afdrukken vanuit de toepassing door te geven aan de ER-modeltoewijzing.

- Type gegevensbron: **Object**

    - Deze gegevensbron moet de naam **PrintMgmtPrintSettingDetail** hebben.
    - Deze moet verwijzen naar de toepassingsklasse **PrintMgmtPrintSettingDetail**.
    - Deze wordt gebruikt tijdens de uitvoering om details van de instellingen voor afdrukbeheer voor de ER-indeling die wordt uitgevoerd door te geven vanuit de toepassing naar de ER-modeltoewijzing.

De details van de integratie van toepassingen met het ER-raamwerk zijn te vinden in de klasse **ERPrintMgmtReportFormatSubscriber** (integratiemodel voor ER-toepassingssuite) in de broncode van de toepassing.

Zie [ER-modeltoewijzingen definiëren en gegevensbronnen hiervoor selecteren](tasks/er-define-model-mapping-select-data-sources-2016-11.md) voor meer informatie over het ontwerp van ER-modeltoewijzingen.

### <a name="configure-the-er-format"></a>De ER-indeling configureren
In uw toepassingsexemplaar moet u over de configuratie van de ER-indeling beschikken die zal worden gebruikt voor het genereren van FTI formulieren. 

> [!NOTE]
> Deze indelingsconfiguratie moet worden gemaakt voor het gegevensmodel CustomersInvoicing en moet gebruikmaken van de modeltoewijzing met de basisdescriptor **FreeTextInvoice**.

Zie [ER: Een indelingsconfiguratie maken (november 2016)](tasks/er-format-configuration-2016-11.md) voor informatie over het configureren van ER-indelingen. Zie [ER: een configuratie ontwerpen voor het genereren van rapporten in OPENXML-indeling (november 2016)](tasks/er-design-reports-openxml-2016-11.md) voor informatie over het ontwerpen van ER-indelingen voor het genereren van rapporten in OpenXML-indeling.

## <a name="configure-print-management"></a>Afdrukbeheer configureren
Als u FTI-formulieren wilt genereren met behulp van het ER-raamwerk, kunt u ER-indelingen toewijzen op dezelfde manier als waarop u SSRS-rapporten toewijst. Als u de ER-indeling wilt koppelen aan alle FTI's voor Klanten, gaat u naar **Klanten** \> **Instelling** \> **ormulieren** \> **Formulierinstellingen** \> **Algemeen** \> **Afdrukbeheer** \> **Vrije-tekstfactuur** \> **Origineel**. Als u de ER-indeling wilt koppelen aan een bepaalde klant of factuur, voert u de volgende stappen uit.

1. Ga naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**.
2. Selecteer de FTI om de ER-indeling te koppelen en de pagina **Afdrukbeheerinstellingen** te openen.
3. Selecteer het documentniveau om het bereik van facturen voor verwerking op te geven.
4. Selecteer de ER-indeling voor het opgegeven documentniveau.

![Instelling afdrukbeheer](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> Alleen ER-indelingen die gebruikmaken van de basisdescriptor **FreeTextInvoice** van het gegevensmodel **CustomersInvoicing** worden weergegeven in het veld **Rapportindeling zoeken** voor de geselecteerde indeling.

## <a name="generate-fti-forms"></a>FTI-formulieren genereren
FTI-formulieren worden gegenereerd in het ER-raamwerk op dezelfde manier als waarop SSRS-rapporten worden gegenereerd.

U kunt FTI-formulieren genereren door facturen te selecteren per bereik of per selectie. 

![Factuurselectie](media/FTIbyGER-InvoiceSelection.png)

![Voorbeeld van factuur](media/FTIbyGER-InvoiceExcelPreview.png)

Wanneer u ER-indelingen gebruikt voor het op deze manier afdrukken van FTI-formulieren, worden de standaard ER-bestandsbestemmingen gebruikt. U kunt de bestemming niet wijzigen. Zie [Bestemmingen van elektronische rapportage (ER)](electronic-reporting-destinations.md) voor meer informatie over het configureren van de ER-bestemmingen voor ER-indelingen.

U kunt ook FTI-formulieren genereren wanneer u een FTI boekt door **Factuur afdrukken** in te schakelen en **Bestemmingen van afdrukbeheer gebruiken** uit te schakelen.

> [!NOTE]
> Wanneer u ER-indelingen gebruikt voor het op deze manier afdrukken van FTI-formulieren, worden de standaard ER-bestandsbestemmingen gebruikt. U kunt de standaardbestemming wijzigen tijdens de uitvoering als de bestemming al is geconfigureerd. Als u de bestemming wilt wijzigen, moet u de volgende beveiligingsbevoegdheid hebben:
>
> - **Naam:** ERFormatDestinationRuntimeMaintain
> - **Label:** bestemming van indeling voor elektronische rapportage tijdens uitvoering onderhouden

![Bestemming elektronische rapportage](media/FTIbyGER-ERFileDestinationSetting.png)

![Bestemming van indeling voor elektronische rapportage](media/FTIbyGER-ERFileDestinationUsage.png)

Het ER-raamwerk ondersteunt momenteel de volgende bestemmingen voor gegenereerde documenten:

- **Gedownload bestand** – Gegenereerde formulieren worden aangeboden als downloads die u kunt opslaan met de browser.
- **Scherm** – Microsoft 365 Excel wordt gebruikt voor het weergeven van een voorbeeld van gegenereerde FTI-formulieren in Excel-indeling.
- **SharePoint-map** – Gegenereerde formulieren worden opgeslagen op basis van de instellingen van het raamwerk voor documentbeheer.
- **Toepassingsarchief** – Gegenereerde formulieren worden opgeslagen als bijlagen van records in het uitvoeringslogboek in de Microsoft Azure-opslag.
- **E-mail** – Gegenereerde formulieren worden verzonden als e-mailbijlagen.

> [!NOTE]
> U kunt de FTI-formulieren die zijn gegenereerd niet rechtstreeks naar de printer verzenden omdat direct afdrukken met de Dynamics Printer Routing Agent momenteel niet wordt ondersteund.

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a>Voorbeelden van ER-configuraties voor het genereren van afdrukbare FTI-formulieren downloaden
U kunt voorbeelden van ER-configuraties downloaden voor gebruik als sjabloon voor uw FTI-oplossing. De configuraties worden opgeslagen in de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS). De configuraties omvatten:

- De configuratie **Klantfactureringsmodel** bevat het vereiste gegevensmodel en de modeltoewijzing.
- De configuratie **FTI-rapport klant (GER)** bevat de voorbeeldindeling.

> [!NOTE]
> Deze configuraties zijn gemaakt als voorbeelden om mogelijke scenario's toe te lichten. De toekomst van deze configuraties is afhankelijk van de resultaten van deze evaluatie en eventuele feedback die is ontvangen.

### <a name="features-that-are-implemented-in-the-sample-er-format"></a>Functies die zijn geïmplementeerd in de ER-voorbeeldindeling
In de configuratie van de ER-voorbeeldindeling wordt een Excel-bestand gebruikt als sjabloon voor het genereren van FTI-formulieren.

![Indelingsontwerper](media/FTIbyGER-ERFormat.png)

Momenteel ondersteunt deze ER-voorbeeldindeling de volgende functies voor het genereren van FTI formulieren:

- FTI-formulieren worden gegenereerd voor zowel originele facturen die zijn geboekt als originele facturen die nog niet zijn geboekt. Gecorrigeerde facturen en creditnota's worden niet ondersteund.
- FTI-formulieren worden gegenereerd in de taal van de factuur. De notatie van waarden en datums in de gegenereerde formulieren is gebaseerd op de instellingen van de gebruiker voor de landinstelling van de client.
- Gegenereerde facturen geven aan dat er geen gegevens beschikbaar zijn als de facturen die worden verwerkt geen regels bevatten.
- Kopteksten van gegenereerde facturen zijn gebaseerd op het papierformaat dat is geselecteerd voor het FTI-formulier op de pagina **Parameters voor Klanten**. Bedrijfsgegevens worden alleen weergegeven in de koptekst van het gegenereerde formulier als het papierformaat leeg is.
- Gegenereerde factuurformulieren geven btw-nummers van bedrijf en klant aan als de desbetreffende gewenste optie is geselecteerd voor het FTI-formulier op de pagina **Parameters voor Klanten**.
- De gegenereerde factuurregels en secties voor factuurtotalen tonen de monetaire details van de standaardfactuur in de registratievaluta van de factuur.
- De sectie met gegenereerde factuurtotalen kan monetaire details bevatten in de valuta euro en in de registratievaluta van de factuur als de optie **Bedrag afdrukken in valuta die de euro vertegenwoordigt** is ingeschakeld op de pagina **Parameters voor Klanten**.
- Gegenereerde factuurformulieren bevatten alle notities voor factuurverwerking die beschikbaar zijn, op basis van instellingen op de pagina **Parameters voor Klanten**. Er worden notities opgenomen voor zowel de hele factuur als elke factuurregel.
- Gegenereerde factuurformulieren bevatten notities voor het FTI-formulier van de klant en de taal voor factuurverwerking wanneer deze zijn geconfigureerd in de lijst met notities voor AR-formulieren.
- Afhankelijk van de instellingen voor afdrukbeheer bevatten gegenereerde facturen aangepaste voettekst wanneer deze is geconfigureerd voor de taal van de factuur, de ER-indeling en het bereik van het FTI-document.
- De totalensectie van gegenereerde factuurformulieren bevat eventuele informatie over contantkortingen die beschikbaar is.
- De sectie voor betalingsplanning van gegenereerde factuurformulieren bevat eventuele details van het betalingsschema die beschikbaar zijn.
- De opmaaksectie van gegenereerde factuurformulieren bevat eventuele transacties met toeslagen die beschikbaar zijn.
- Gegenereerde factuurformulieren bevatten btw-gegevens op basis van de instelling **Btw-specificatie** op de pagina **Parameters voor Klanten**. Deze sectie kan belastinggegevens bevatten in alleen de registratievaluta voor de factuur of in zowel de registratievaluta voor de factuur als de valuta voor de boekhouding van het bedrijf.
- Gegenereerde factuurformulieren bevatten meldingsdetails voor automatische incasso. Zij geven bijvoorbeeld aan wanneer de betalingsmethode met de verplichte mandaat-id voor automatische incasso is geselecteerd voor de factuur , wanneer de verwerkingsfactuur is geregistreerd in de eurovaluta en wanneer de mandaat-id voor automatische incasso is gedefinieerd voor de factuur.
- Gegenereerde facturen geven eventuele details van vooruitbetalingen aan die beschikbaar zijn voor geboekte facturen.
- Gegenereerde factuurformulieren kunnen als e-mailbijlage naar een factuurklant worden verzonden. De juiste bestemming voor ER-bestanden moet worden geconfigureerd voor de ER-indeling die wordt gebruikt.

### <a name="countryregion-specific-features"></a>Land-/regioafhankelijke functies 
De volgende land-/regiospecifieke functies zijn opgenomen in de ER-voorbeeldindeling om te laten zien hoe specifieke behoeften kunnen worden afgehandeld in ER-configuraties.

#### <a name="norway"></a>Noorwegen
De term Ondernemingsregister wordt in de kop van het gegenereerde factuurformulier opgenomen als de factuur wordt verwerkt voor een rechtspersoon die op de volgende manier is geconfigureerd:

- Er wordt gebruikgemaakt van de land-/regiocontext voor Noorwegen.
- De parameter **Foretaksregisteret afdrukken** is actief in verkoopdocumenten.

#### <a name="spain"></a>Spanje
De term **Speciaal regime voor methode contantboekhouding** wordt in de kop van het gegenereerde factuurformulier opgenomen als de factuur wordt verwerkt voor een rechtspersoon die op de volgende manier is geconfigureerd:

- Er wordt gebruikgemaakt van de land-/regiocontext voor Spanje.
- Het speciale regime voor de methode contantboekhouding is ingeschakeld op de datum van factuurverwerking.

Wanneer details van contantkortingen, zoals het kortingsbedrag voor contante betaling en het nettobedrag van de factuurregel, beschikbaar zijn, worden deze weergegeven in de sectie met factuurtotalen van het gegenereerde factuurformulier wanneer dit is verwerkt voor een rechtspersoon die op de volgende manier is geconfigureerd:

- Er wordt gebruikgemaakt van de land-/regiocontext voor Spanje.
- **Korting voor contante betaling wordt toegepast op de factuur** is ingeschakeld in de factuuroptie (**Grootboekparameters** \> **Sectie van btw**).

#### <a name="italy"></a>Italië
De markering voor goederenkorting wordt opgenomen op de factuurregels van de gegenereerde factuur wanneer deze wordt verwerkt voor een rechtspersoon die is geconfigureerd met behulp van de land-/regiocontext voor Italië.

#### <a name="finland"></a>Finland
Naast het gegenereerde factuurformulier, worden acceptgirostroken als volgt gegenereerd:

- Voor de rechtspersoon die de land-/regiocontext voor Finland gebruikt en die ten minste één bankrekening heeft die is gemarkeerd als **Girorekening** en **Streepjescode bank**. 
- Voor een factuur die is gemarkeerd als vereist voor de **Finse** gekoppelde betalingsbijlage.

![Girostrookje](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> De ER-voorbeeldindeling is geconfigureerd voor het optioneel genereren van de acceptgirostroken op een afzonderlijk werkblad.

> [!NOTE]
> U moet eerst het lettertype installeeren dat wordt gebruikt om de streepjescode te genereren op de lokale computer waar het gegenereerde formulier in Excel-indeling als voorbeeld wordt weergegeven.

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a>De ER-voorbeeldindeling gebruiken voor het configureren van e-mailbestemmingen
Gebruik de volgende element van de ER-voorbeeldindeling om e-mailbestemmingen te configureren:

- Het e-mailadres van een contactpersoon bij de klant kan worden geopend via de ER-expressie: **model.InvoiceBase.Contact.ElectronicMail**.
- De tekst van het e-mailonderwerp is toegankelijk via de volgende ER-expressie: **Emailing.TxtToUse.Subject**.
- De hoofdtekst van het e-mailbericht is toegankelijk via de volgende ER-expressie: **Emailing.TxtToUse.Body**.

![Bestemmingsinstellingen](media/FTIbyGER-ERFileDestinationSettingEmail.png)

De standaardtekst van het onderwerp en de hoofdtekst van het e-mailbericht wordt gedefinieerd in de ER-voorbeeldindeling. De taal is afhankelijk van de labels van de indeling. Deze standaardtekst wordt gebruikt voor e-mailberichten als geen aangepaste e-mailsjabloon voor de organisatie met de vooraf gedefinieerde **ERFTITMP**-id is toegevoegd.

> [!NOTE]
> De **ERFTITMP**-e-mailsjabloon-id is gedefinieerd in de ER-voorbeeldindeling. Deze kan naar behoefte worden gewijzigd in een nieuwe ER-indeling die is gemaakt op basis van deze voorbeeldindeling.

Als de e-mailsjabloon voor de organisatie met de vooraf gedefinieerde **ERFTITMP**-id is toegevoegd voor de rechtspersoon waarvoor u de factuur verwerkt, wordt de sjabloon voor het onderwerp en de hoofdtekst van het e-mailbericht gebruikt voor het genereren van het e-mailbericht. 

![E-mailsjablonen van organisatie](media/FTIbyGER-EmailTemplate.png)

![E-mailsjabloon uploaden](media/FTIbyGER-EmailTemplateBody.png)

De ER-expressie **Emailing.TxtToUse.Subject** van de ER-expressie van de ER-voorbeeldindeling is geconfigureerd om alle exemplareen van de tijdelijke aanduiding %1 te vervangen door de id van de verwerkingsfactuur.

De expressie **Emailing.TxtToUse.Body** van de voorbeeldindeling is geconfigureerd voor de volgende vervangingen voor tijdelijke aanduidingen:

- '%1' wordt vervangen door de naam van de contactpersoon van de klant.
- '%2' wordt vervangen door de naam van het bedrijf.
- '%3' wordt vervangen door de naam van de klant.
- '%4' wordt vervangen door de naam van de contactpersoon van het bedrijf.
- '%5' wordt vervangen door de functietitel van de contactpersoon van het bedrijf.
- '%6' wordt vervangen door het e-mailadres van de contactpersoon van het bedrijf.

![E-mailadres](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a>Aanvullende resources
[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]