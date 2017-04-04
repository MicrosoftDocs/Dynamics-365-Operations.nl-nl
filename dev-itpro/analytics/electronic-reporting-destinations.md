---
title: Bestemmingen voor elektronische rapportage
description: U kunt een bestemming voor elke ER-indelingsconfiguratie (Elektronische Rapportage) en de bijbehorende uitvoercomponent (een map of een bestand) configureren. Gebruikers aan wie de juiste toegangsrechten zijn verleend, kunnen tevens bestemmingsinstellingen wijzigen tijdens de uitvoeren. In dit artikel worden ER bestemmingsbeheer, de typen bestemmingen die worden ondersteund en beveiligingsoverwegingen beschreven.
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: d38d05fe445bf0326d408038dff84ccf8c0ff64c
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-destinations"></a>Bestemmingen voor elektronische rapportage

U kunt een bestemming voor elke ER-indelingsconfiguratie (Elektronische Rapportage) en de bijbehorende uitvoercomponent (een map of een bestand) configureren. Gebruikers aan wie de juiste toegangsrechten zijn verleend, kunnen tevens bestemmingsinstellingen wijzigen tijdens de uitvoeren. In dit artikel worden ER bestemmingsbeheer, de typen bestemmingen die worden ondersteund en beveiligingsoverwegingen beschreven.

Indelingconfiguraties voor Elektronische rapportage (ER) bevatten meestal minimaal één uitvoeronderdeel: een bestand. Configuraties bevatten gewoonlijk meerdere onderdelen voor bestandsuitvoer van verschillende typen (bijvoorbeeld XML, TXT of XLSX) die zijn gegroepeerd in een enkele map of in meerdere mappen. ER-bestemmingsbeheer stelt u in staat vooraf te configureren wat er gebeurt wanneer elk onderdeel wordt uitgevoerd. De standaardinstelling wanneer een configuratie wordt uitgevoerd, verschijnt een dialoogvenster waarmee de gebruiker het bestand opslaan of openen. Hetzelfde gedrag wordt ook gebruikt wanneer u een ER-configuratie importeert en geen specifieke bestemmingen hiervoor configureert. Nadat u een bestemming voor een hoofduitvoeronderdeel hebt gemaakt, overschrijft die bestemming het standaardgedrag en wordt de map of het bestand verzonden op basis van de instellingen van de bestemming.

## <a name="availability-and-general-prerequisites"></a>Beschikbaarheid en algemene vereisten
De functionaliteit van de bestemmingen Emergency Recovery is niet beschikbaar in de Microsoft Dynamics 365 voor vrijgave bewerkingen 7.0 (februari 2016). Daarom moet u Microsoft Dynamics 365 voor bewerkingen (November 2016 release) gebruik van de functies die in dit onderwerp worden beschreven. U kunt ook een van de volgende vereisten installeren. Bedenk echter dat deze plaats bieden beperkter Emergency Recovery bestemming.

-   Microsoft Dynamics 365 voor de versie van de toepassing bewerkingen 7.0.1 (mei 2016)
-   [Toepassingshotfix](https://fix.lcs.dynamics.com/issue/results/?q=3160213) voor ER-bestemmingsbeheer

U kunt alleen bestemmingen instellen voor ER-configuraties die zijn geïmporteerd en voor de indelingen die beschikbaar zijn op de pagina **Configuraties van elektronische rapportage**.

## <a name="overview"></a>Overzicht
De Emergency Recovery-functionaliteit voor het beheer van bestemming is beschikbaar op **Organisatiebeheer**&gt;**elektronische aangifte**. Hier kunt u het standaardgedrag voor een configuratie overschrijven. Geïmporteerde configuraties worden niet weergegeven totdat u op **Nieuw** klikt en vervolgens in het veld **Verwijzing** een configuratie selecteert waarvoor u bestemmingsinstellingen wilt maken.

[![Een configuratie selecteren in het veld verwijzing](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Nadat u een verwijzing hebt gemaakt, kunt u een bestemming voor elke map of voor een bestand maken. 

[![De bestemming van een bestand maken](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

**Opmerking:** u kunt één bestandsbestemming maken voor elk uitvoeronderdeel met dezelfde indeling, zoals een map of een bestand, dat is geselecteerd in het veld **Bestandsnaam**. U kunt vervolgens- en uitschakelen van afzonderlijke bestemmingen voor de bestemming in de **instellingen afdrukbestemming** in het dialoogvenster. De knop **instellingen** wordt gebruikt voor het bepalen van alle bestemmingen voor een geselecteerde bestandsbestemming. In het dialoogvenster **Bestemmingsinstellingen** kunt u elke bestemming afzonderlijk bepalen door de optie **Ingeschakeld** hiervoor in te stellen.

[![In het dialoogvenster bestemming-instellingen](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Bestemmingstypen
Er worden verschillende typen bestemmingen ondersteund. U kunt alle typen tegelijkertijd uit- of inschakelen. Op die manier kunt u niets doen of het onderdeel naar alle geconfigureerde bestemmingen verzenden. In de volgende secties worden de bestemmingen beschreven die worden ondersteund.

### <a name="email-destination"></a>E-mailbestemming

Stel **Ingeschakeld **in op **Ja** om een uitvoerbestand per e-mail te verzenden. Nadat u deze optie is ingeschakeld, kunt u de geadresseerden opgeven en bewerken van het onderwerp en de hoofdtekst van het e-mailbericht. U kunt constante teksten voor de e-onderwerp en de hoofdtekst instellen of kunt u ER formules dynamisch e-teksten maken. U kunt e-mailadressen voor Emergency Recovery op twee manieren configureren. De configuratie kan worden uitgevoerd op dezelfde manier als deze door de functie voor het beheer van af te drukken in Dynamics 365 for Operations is voltooid. U kunt ook een e-mailadres oplossen met behulp van een directe verwijzing naar de Emergency Recovery-configuratie via een formule.

### <a name="email-address-types"></a>E-mailadres typen

Wanneer u klikt op **bewerken** voor de **naar** of **Cc** veld, de **per e-mail naar** in het dialoogvenster wordt weergegeven. Vervolgens kunt u het type e-mailadres wilt gebruiken.

[![Per e-mail aan in het dialoogvenster](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Afdrukbeheer

Als u de **e-mailadres afdrukbeheer** type, kunt u vaste e-mailadressen in de **naar** veld. Als u wilt gebruiken in e-mailadressen die niet zijn opgelost, moet u het e-brontype voor de bestemming van een bestand. De volgende waarden worden ondersteund: **klant**, **leverancier**, **Prospect**, **Contact**, **concurrent**, **werknemer**, **sollicitant**, **potentiële leverancier**, en **niet-toegestane leverancier**. Nadat u een e-brontype selecteert, gebruikt u de knop naast de **-e-mailaccount bron** veld opent de ** Formuleontwerper ** formulier. Gebruik dit formulier kunt u een formule die staat voor de geselecteerde rekening naar de bestemming van de e-mailbericht koppelen.

[![afdrukbeheer van e-type configureren](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Houd er rekening mee dat formules specifiek zijn voor de ER-configuratie. Voer in het veld **Formule** een documentspecifieke verwijzing naar een klant- of leverancierspartijtype in. In plaats van te typen kunt u ook het gegevensbronknooppunt zoeken waarmee de klant- of leveranciersrekening wordt voorgesteld. Klik vervolgens op **Gegevensbron toevoegen** om de formule bij te werken. Als u bijvoorbeeld de configuratie ISO 20022 Kredietoverdracht gebruikt, is het knooppunt waarmee een leveranciersrekening wordt voorgesteld **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. Voer anders een tekenreekswaarde naar keuze in, zoals **DE-001**, om een formule op te slaan.

[![Formula designer](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

In de **per e-mail naar** in het dialoogvenster, klikt u op het recyclen bak volgende om door te de **-e-mailaccount bron** veld u de formule voor de e-bronrekening permanent wilt verwijderen. U kunt ook openen in de Formuleontwerper als een formule die eerder is opgeslagen wilt wijzigen. Voor het toewijzen van e-mailadressen, klikt u op **bewerken** opent de **toewijzen e-mailadressen** in het dialoogvenster.

[![e-mailadressen voor een e-doellocatie toewijzen](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Configuratie-e-mail

Gebruik dit type e-als de configuratie die u gebruikt een knooppunt in de gegevensbronnen waarmee een e-mailadres heeft. U kunt gegevensbronnen en functies in de Formuleontwerper krijgen een goed opgemaakte e-mailadres.

[![Een gegevensbron voor e-mailadres voor de bestemming van een e-toewijzen](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Opmerking:** er moet een SMTP-server (Simple Mail Transfer Protocol) worden geconfigureerd en beschikbaar besteld. Kunt u de SMTP-server in Dynamics 365 voor bewerkingen, op **Systeembeheer**&gt;**Setup**&gt;**e-mailadres**&gt;**e-parameters**.

### <a name="archive-destination"></a>Archiefbestemming

Met deze optie kunt u uitvoer naar een Microsoft SharePoint-map of naar de opslag van Microsoft Azure verzenden. Stel **Ingeschakeld** in op **Ja **om uitvoer naar een bestemming te verzenden die is gedefinieerd door het geselecteerde documenttype. Alleen documenttypen waarvan de groep is ingesteld op **Bestand** zijn beschikbaar voor selectie. Definieert u documenttypen op **Organisatiebeheer**&gt;**documentbeheer**&gt;**documenttypen**. De configuratie voor ER-bestemmingen is hetzelfde als de configuratie voor het documentbeheersysteem.

[![De pagina typen document](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

De locatie bepaalt waar het bestand wordt opgeslagen. Na de **archief** bestemming is ingeschakeld, zijn de resultaten van de uitvoering van de configuratie kunnen worden opgeslagen in het archief van de taak. Ziet u de resultaten op **Organisatiebeheer**&gt;**elektronische aangifte**&gt;**taken elektronische aangifte gearchiveerd**. **opmerking:** kunt u een documenttype voor het archief van de taak in Dynamics 365 voor bewerkingen, op **Organisatiebeheer**&gt;**werkruimten**&gt;**elektronische aangifte**&gt;**elektronische rapportparameters**.

#### <a name="sharepoint"></a>SharePoint

U kunt een bestand opslaan in een aangewezen SharePoint-map. U definieert de standaard SharePoint-server op **Organisatiebeheer**&gt;**documentbeheer**&gt;**management documentparameters**op de **SharePoint** tabblad. Nadat de SharePoint-map is geconfigureerd, kunt u deze kunt selecteren als de map waar de Emergency Recovery-uitvoer wordt opgeslagen voor het documenttype. 

[![Als u een SharePoint-map](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure-opslag

Als de locatie van het documenttype is ingesteld op **Archiefmap**, kunt u een bestand opslaan in Azure-opslag.

### <a name="file-destination"></a>Bestandsbestemming

Als u **ingeschakeld** naar **Ja**, een openen of opslaan in het dialoogvenster wordt weergegeven wanneer de configuratie is voltooid.

### <a name="screen-destination"></a>Scherm bestemming

Als u **ingeschakeld** naar **Ja**, een voorbeeld van de uitvoer wordt gemaakt. U kunt sommige bestandstypen, zoals XML, *.txt of PDF, rechtstreeks in een browservenster weergeven. Voor andere bestandstypen, zoals Microsoft Excel of Word, wordt Microsoft Office Online-service gebruikt.

### <a name="power-bi-destination"></a>Power BI bestemming

Stel **ingeschakeld** naar **Ja** uw Emergency Recovery-configuratie gebruiken om te bepalen van de overdracht van gegevens van uw exemplaar van Dynamics 365 voor bewerkingen naar Microsoft Power BI-services. De overgebrachte bestanden worden opgeslagen op een Microsoft SharePoint Server-exemplaar dat moet worden geconfigureerd voor dat doel. Zie voor meer informatie [u de configuratie van een elektronische aangifte voor Power BI gegevens uit Dynamics 365 voor bewerkingen](general-electronic-reporting-report-configuration-get-data-powerbi.md). **Tip:** als u het standaardgedrag wilt negeren (dat wil zeggen het dialoogvenster voor een configuratie), kunt u een bestemmingsverwijzing en een bestandsbestemming voor het hoofduitvoeronderdeel maken en vervolgens alle bestemmingen uitschakelen.

## <a name="security-considerations"></a>Beveiligingsoverwegingen
Twee typen machtigingen en rechten worden gebruikt voor ER-bestemmingen. Een bepaald type bepaalt of de algehele bestemmingen die zijn geconfigureerd voor een rechtspersoon te onderhouden (dat wil zeggen, controleert de toegang tot de **elektronische aangifte bestemmingen** pagina). Het andere type regelt de mogelijkheid van een toepassingsgebruiker om, tijdens de uitvoering, de bestemmingsinstellingen die zijn geconfigureerd door een ER-ontwikkelaar of functionele ER-consultant te negeren.

| Rol (AOT-naam)                     | Rolnaam                                  | Functie (AOT-naam)                     | Functienaam                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Ontwikkelaar elektronische rapportage             | ERFormatDestinationConfigure        | Bestemming van indeling voor elektronische rapportage configureren                |
| ERFunctionalConsultant              | Functioneel consultant elektronische rapportage | ERFormatDestinationConfigure        | Bestemming van indeling voor elektronische rapportage configureren                |
| PaymAccountsPayablePaymentsClerk    | Leveranciersadministrateur            | ERFormatDestinationRuntimeConfigure | Bestemming van indeling voor elektronische rapportage tijdens runtime configureren |
| PaymAccountsReceivablePaymentsClerk | Klantenadministrateur         | ERFormatDestinationRuntimeConfigure | Bestemming van indeling voor elektronische rapportage tijdens runtime configureren |

**Opmerking:** er worden twee bevoegdheden gebruikt in de voorafgaande taken. Deze bevoegdheden hebben dezelfde naam als de corresponderende rechten: **ERFormatDestinationConfigure** en **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Ik heb elektronische configuraties geïmporteerd en ik zie ze op de pagina Configuraties van elektronische rapportage. Maar waarom ik Zie ze niet op de elektronische aangifte bestemmingen pagina?

Zorg ervoor dat u klikt op **New** en selecteer vervolgens een configuratie in de **verwijzing** veld. Op de pagina **Bestemmingen voor elektronische rapportage** ziet u alleen configuraties waarvoor bestemmingen zijn geconfigureerd.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Is er een manier om te definiëren welke Azure opslag- en Azure blobopslag worden gebruikt?

Nr. De standaard Azure blobopslag die is gedefinieerd en gebruikt voor het documentbeheersysteem wordt gebruikt.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Wat is het doel van de bestemming in de instellingen afdrukbestemming? Wat doet die instelling?

De bestemming **Bestand** wordt gebruikt voor het besturen van een dialoogvenster. Als u deze bestemming inschakelt of als er geen bestemming voor een configuratie is gedefinieerd, kunt u een open Zie of in het dialoogvenster Opslaan als een uitvoerbestand is gemaakt.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Kunt u een voorbeeld geven van de formule die verwijst naar een leveranciersrekening waarnaar ik e-mail kan sturen?

De formule is specifiek voor de ER-configuratie. Als u bijvoorbeeld de configuratie ISO 20022 Kredietoverdracht gebruikt, kunt u **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** of **model.Payments.Creditor.Identification.SourceID** gebruiken om een gekoppelde leveranciersrekening te verkrijgen.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Een van mijn indelingsconfiguraties bevat meerdere bestanden die zijn gegroepeerd in één map (bijvoorbeeld Map1 bevat Bestand1, Bestand2 en Bestand3). Hoe kan ik op zodanige wijze bestemmingen instellen dat Map1.zip helemaal niet wordt gemaakt, Bestand1 per e-mail wordt verzonden, Bestand2 naar SharePoint wordt verzonden en Bestand3 direct kan worden geopend nadat configuratie is uitgevoerd?

De vereiste is dat de indeling beschikbaar in de Emergency Recovery-configuraties zijn moet. Als u uw indeling hebt, opent u de pagina **Bestemming elektronische rapportage** en maakt u een nieuwe verwijzing naar deze configuratie. Vervolgens moet u vier bestandsbestemmingen hebben, één voor elk uitvoeronderdeel. Maak de eerste bestemming, geeft deze een naam, zoals **Map**, en selecteer een bestandsnaam die een map in uw configuratie vertegenwoordigt. Klik vervolgens op **Instellingen** en zorg ervoor dat alle bestemmingen zijn uitgeschakeld. Voor deze bestandsbestemming wordt de map niet gemaakt. Standaard gedragen bestanden zich op dezelfde manier, vanwege de hiërarchische afhankelijkheden tussen bestanden en bovenliggende mappen. Met andere woorden, zij worden helemaal niet verzonden. Als u dit standaardgedrag wilt overschrijven, moet u nog drie bestandsbestemmingen maken, één voor elk bestand. In de bestandsinstellingen voor elk daarvan, moet u de bestemming inschakelen waar het bestand naartoe moet worden verzonden.

# <a name="see-also"></a>Zie ook

[Overzicht van elektronische rapportage](general-electronic-reporting.md)


