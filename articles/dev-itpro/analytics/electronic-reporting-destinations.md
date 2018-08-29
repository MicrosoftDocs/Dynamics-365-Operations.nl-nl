---
title: Bestemmingen van elektronische rapportage (ER)
description: U kunt een bestemming voor elke ER-indelingsconfiguratie (Elektronische Rapportage) en de bijbehorende uitvoercomponent (een map of een bestand) configureren. Gebruikers aan wie de juiste toegangsrechten zijn verleend, kunnen tevens bestemmingsinstellingen wijzigen tijdens de uitvoeren. In dit artikel worden ER bestemmingsbeheer, de typen bestemmingen die worden ondersteund en beveiligingsoverwegingen beschreven.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 3aa27b3ac263c6c952de7e4b508f48f21ba489ad
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---

# <a name="electronic-reporting-er-destinations"></a>Bestemmingen van elektronische rapportage (ER)

[!include [banner](../includes/banner.md)]

U kunt een bestemming voor elke ER-indelingsconfiguratie (Elektronische Rapportage) en de bijbehorende uitvoercomponent (een map of een bestand) configureren. Gebruikers aan wie de juiste toegangsrechten zijn verleend, kunnen tevens bestemmingsinstellingen wijzigen tijdens de uitvoeren. In dit artikel worden ER bestemmingsbeheer, de typen bestemmingen die worden ondersteund en beveiligingsoverwegingen beschreven.

Indelingconfiguraties voor Elektronische rapportage (ER) bevatten meestal minimaal één uitvoeronderdeel: een bestand. Configuraties bevatten gewoonlijk meerdere onderdelen voor bestandsuitvoer van verschillende typen (bijvoorbeeld XML, TXT of XLSX) die zijn gegroepeerd in een enkele map of in meerdere mappen. ER-bestemmingsbeheer stelt u in staat vooraf te configureren wat er gebeurt wanneer elk onderdeel wordt uitgevoerd. Wanneer een configuratie wordt uitgevoerd, wordt standaard een dialoogvenster weergegeven waarin de gebruiker het bestand kan opslaan of openen. Hetzelfde gedrag wordt ook gebruikt wanneer u een ER-configuratie importeert en geen specifieke bestemmingen hiervoor configureert. Nadat u een bestemming voor een hoofduitvoeronderdeel hebt gemaakt, overschrijft die bestemming het standaardgedrag en wordt de map of het bestand verzonden op basis van de instellingen van de bestemming.

## <a name="availability-and-general-prerequisites"></a>Beschikbaarheid en algemene vereisten
De functionaliteit ER-bestemmingen is niet beschikbaar in de versie van Microsoft Dynamics AX 7.0 (februari 2016). Daarom moet u Microsoft Dynamics 365 for Operations versie 1611 (november 2016) installeren om gebruik te kunnen maken van alle functies die in dit onderwerp worden beschreven. U kunt ook een van de volgende vereisten installeren. Houd er echter rekening mee dat dit alternatief een beperktere versie van ER-bestemmingen biedt.

-   Microsoft Dynamics AX-toepassing versie 7.0.1 (mei 2016)
-   [Toepassingshotfix](https://fix.lcs.dynamics.com/issue/results/?q=3160213) voor ER-bestemmingsbeheer

U kunt alleen bestemmingen instellen voor ER-configuraties die zijn geïmporteerd en voor de indelingen die beschikbaar zijn op de pagina **Configuraties van elektronische rapportage**.

## <a name="overview"></a>Overzicht
De functionaliteit voor het beheer van ER-bestemmingen is beschikbaar onder **Organisatiebeheer** &gt; **Elektronische rapportage**. Hier kunt u het standaardgedrag voor een configuratie overschrijven. Geïmporteerde configuraties worden niet weergegeven totdat u op **Nieuw** klikt en vervolgens in het veld **Verwijzing** een configuratie selecteert waarvoor u bestemmingsinstellingen wilt maken.

[![Een configuratie in het veld Verwijzing selecteren](./media/ger-destinations-2-1611-1024x574.jpg)](./media/ger-destinations-2-1611.jpg) 

Nadat u een verwijzing hebt gemaakt, kunt u een bestandsbestemming maken voor elke map of voor een bestand. 

[![Een bestandsbestemming maken](./media/ger-destinations-1611-1024x586.jpg)](./media/ger-destinations-1611.jpg)

> [!NOTE] 
> U kunt één bestandsbestemming maken voor elk uitvoeronderdeel met dezelfde indeling, zoals een map of een bestand, dat is geselecteerd in het veld **Bestandsnaam**. Vervolgens kunt u de afzonderlijke bestemmingen voor de bestandsbestemming in- en uitschakelen in het dialoogvenster **Bestemmingsinstellingen**. De knop **instellingen** wordt gebruikt voor het bepalen van alle bestemmingen voor een geselecteerde bestandsbestemming. In het dialoogvenster **Bestemmingsinstellingen** kunt u elke bestemming afzonderlijk bepalen door de optie **Ingeschakeld** hiervoor in te stellen.

[![Dialoogvenster Bestemmingsinstellingen](./media/ger-destinations-settings-1611-1024x589.jpg)](./media/ger-destinations-settings-1611.jpg)

## <a name="destination-types"></a>Bestemmingstypen
Er worden verschillende typen bestemmingen ondersteund. U kunt alle typen tegelijkertijd uit- of inschakelen. Op die manier kunt u niets doen of het onderdeel naar alle geconfigureerde bestemmingen verzenden. In de volgende secties worden de bestemmingen beschreven die worden ondersteund.

### <a name="email-destination"></a>E-mailbestemming

Stel **Ingeschakeld** in op **Ja** om een uitvoerbestand per e-mail te verzenden. Nadat deze optie is ingeschakeld, kunt u de ontvangers van het e-mailbericht opgeven en het onderwerp en de tekst van het e-mailbericht bewerken. U kunt constante teksten voor het onderwerp en de hoofdtekst van het e-mailbericht instellen of u kunt ER-formules gebruiken om e-mailteksten dynamisch te maken. U kunt e-mailadressen voor ER op twee manieren configureren. De configuratie kan op dezelfde manier worden uitgevoerd als met de functie voor afdrukbeheer in Finance and Operations. U kunt een e-mailadres ook herleiden met behulp van een directe verwijzing naar de ER-configuratie via een formule.

### <a name="email-address-types"></a>E-mailadrestypen

Als u klikt op **Bewerken** voor het veld **Aan** of **Cc**, wordt het dialoogvenster **E-mail naar** weergegeven. Vervolgens kunt u het type te gebruiken e-mailadres selecteren.

[![Dialoogvenster E-mail naar](./media/ger-destinations-email-1-1611-1024x588.jpg)](./media/ger-destinations-email-1-1611.jpg)

#### <a name="print-management"></a>Afdrukbeheer

Als u het type **E-mail van Afdrukbeheer** selecteert, kunt u vaste e-mailadressen invoeren in het veld **Aan**. Als u niet-vaste e-mailadressen wilt gebruiken, moet u het brontype voor e-mail selecteren voor een bestandsbestemming. De volgende waarden worden ondersteund: **Klant**, **Leverancier**, **Prospect**, **Contact**, **Concurrent**, **Werknemer**, **Sollicitant**, **Potentiële leverancier** en **Niet-toegestane leverancier**. Nadat u een e-mailbrontype hebt geselecteerd, gebruikt u de knop naast het veld **E-mail van bronrekening** om het formulier **Formuleontwerper** te openen. U kunt dit formulier gebruiken om een formule te koppelen die de geselecteerde partijrekening vertegenwoordigd voor de e-mailbestemming.

[![E-mailtype afdrukbeheer configureren](./media/ger-destinations-email-2-1611-1024x588.jpg)](./media/ger-destinations-email-2-1611.jpg) 

Houd er rekening mee dat formules specifiek zijn voor de ER-configuratie. Voer in het veld **Formule** een documentspecifieke verwijzing naar een klant- of leverancierspartijtype in. In plaats van te typen kunt u ook het gegevensbronknooppunt zoeken waarmee de klant- of leveranciersrekening wordt voorgesteld. Klik vervolgens op **Gegevensbron toevoegen** om de formule bij te werken. Als u bijvoorbeeld de configuratie ISO 20022 Kredietoverdracht gebruikt, is het knooppunt waarmee een leveranciersrekening wordt voorgesteld **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID**. Voer anders een tekenreekswaarde naar keuze in, zoals **DE-001**, om een formule op te slaan.

[![Formuleontwerper](./media/ger_formuladesignerfordestination-1024x541.jpg)](./media/ger_formuladesignerfordestination.jpg)

Klik in het dialoogvenster **E-mail naar** op de prullenbak naast het veld **E-mailbronaccount** om de formule voor de e-mailbronaccount permanent te verwijderen. U kunt ook de Formuleontwerper openen om een formule te wijzigen die eerder is opgeslagen. Als u e-mailadressen wilt toewijzen, klikt u op **Bewerken** om het dialoogvenster **E-mailadressen toewijzen** te openen.

[![E-mailadressen toewijzen voor een e-mailbestemming](./media/ger-destinations-email-3-1611-1024x587.jpg)](./media/ger-destinations-email-3-1611.jpg)

#### <a name="configuration-email"></a>Configuratie-e-mail

Gebruik dit e-mailtype als de configuratie die u gebruikt, een knooppunt heeft in de gegevensbronnen waarmee een e-mailadres wordt vertegenwoordigd. U kunt gegevensbronnen en functies in de Formuleontwerper gebruiken om een correct opgemaakt e-mailadres te krijgen.

[![Een e-mailadresgegevensbron toewijzen voor een e-mailbestemming](./media/ger-destinations-email-4-1611-1024x587.jpg)](./media/ger-destinations-email-4-1611.jpg) 

**Opmerking:** er moet een SMTP-server (Simple Mail Transfer Protocol) worden geconfigureerd en beschikbaar besteld. U kunt uw SMTP-server opgeven in Finance and Operations bij **Systeembeheer** &gt; **Instellen** &gt; **E-mail** &gt; **E-mailparameters**.

### <a name="archive-destination"></a>Archiefbestemming

Met deze optie kunt u uitvoer naar een Microsoft SharePoint-map of naar de opslag van Microsoft Azure verzenden. Stel **Ingeschakeld** in op **Ja** om uitvoer naar een bestemming te verzenden die is gedefinieerd door het geselecteerde documenttype. Alleen documenttypen waarvan de groep is ingesteld op **Bestand** zijn beschikbaar voor selectie. U definieert documenttypen onder **Organisatiebeheer** &gt; **Documentbeheer** &gt; **Documenttypen**. De configuratie voor ER-bestemmingen is hetzelfde als de configuratie voor het documentbeheersysteem.

[![Pagina Documenttypen](./media/ger_documenttypefile-1024x542.jpg)](./media/ger_documenttypefile.jpg) 

De locatie bepaalt waar het bestand wordt opgeslagen. Nadat de bestemming **Archief** is ingeschakeld, kunnen de resultaten van de uitvoering van de configuratie worden opgeslagen in het taakarchief. U kunt de resultaten weergeven via **Organisatiebeheer** &gt; **Elektronische aangifte** &gt; **Gearchiveerde taken elektronische aangifte**. **Opmerking:** u kunt een documenttype voor het taakarchief in Finance and Operations selecteren via **Organisatiebeheer** &gt; **Werkgebieden** &gt; **Elektronische aangifte** &gt; **Elektronische rapportparameters**.

#### <a name="sharepoint"></a>SharePoint

U kunt een bestand opslaan in een aangewezen SharePoint-map. U definieert de standaard SharePoint-server onder **Organisatiebeheer** &gt; **Documentbeheer** &gt; **Parameters voor documentbeheer** op het tabblad **SharePoint**. Nadat de SharePoint-map is geconfigureerd, kunt u deze selecteren als de map waarin de ER-uitvoer wordt opgeslagen voor het documenttype. 

[![Een SharePoint-map selecteren](./media/ger_sharepointfolderselection-1024x543.jpg)](./media/ger_sharepointfolderselection.jpg) 

#### <a name="azure-storage"></a>Azure-opslag

Als de locatie van het documenttype is ingesteld op **Archiefmap**, kunt u een bestand opslaan in Azure-opslag.

### <a name="file-destination"></a>Bestandsbestemming

Als u **Ingeschakeld** instelt op **Ja**, wordt een dialoogvenster voor openen of opslaan weergegeven wanneer de uitvoering van de configuratie is voltooid.

### <a name="screen-destination"></a>Schermbestemming

Als u **Ingeschakeld** instelt op **Ja**, wordt een voorbeeld van de uitvoer gemaakt. U kunt sommige bestandstypen, zoals XML, TXT of PDF, rechtstreeks in een browservenster weergeven. Voor andere bestandstypen, zoals Microsoft Excel of Word, wordt de Microsoft Office Online-service gebruikt.

### <a name="power-bi-destination"></a>Power BI-bestemming

Stel **Ingeschakeld** in op **Ja** als u uw ER-configuratie wilt gebruiken om gegevens van uw exemplaar van Finance and Operations over te dragen aan Microsoft Power BI-services. De overgebrachte bestanden worden opgeslagen op een Microsoft SharePoint Server-exemplaar dat voor dit doel moet worden geconfigureerd. Zie [Een configuratie van Elektronische rapportage gebruiken om Power BI van gegevens uit Finance and Operations te voorzien](general-electronic-reporting-report-configuration-get-data-powerbi.md) voor meer informatie. **Tip:** als u het standaardgedrag wilt negeren (dat wil zeggen het dialoogvenster voor een configuratie), kunt u een bestemmingsverwijzing en een bestandsbestemming voor het hoofduitvoeronderdeel maken en vervolgens alle bestemmingen uitschakelen.

## <a name="security-considerations"></a>Beveiligingsoverwegingen
Twee typen machtigingen en rechten worden gebruikt voor ER-bestemmingen. Eén type regelt de mogelijkheid om de algehele bestemmingen te onderhouden die worden geconfigureerd voor een rechtspersoon (dat wil zeggen, toegang tot de pagina **Bestemmingen voor elektronische rapportage** wordt beheerd). Het andere type regelt de mogelijkheid van een toepassingsgebruiker om, tijdens de uitvoering, de bestemmingsinstellingen die zijn geconfigureerd door een ER-ontwikkelaar of functionele ER-consultant te negeren.

| Rol (AOT-naam)                     | Rolnaam                                  | Functie (AOT-naam)                     | Functienaam                                                        |
|-------------------------------------|--------------------------------------------|-------------------------------------|------------------------------------------------------------------|
| ERDeveloper                         | Ontwikkelaar elektronische rapportage             | ERFormatDestinationConfigure        | Bestemming van indeling voor elektronische rapportage configureren                |
| ERFunctionalConsultant              | Functioneel consultant elektronische rapportage | ERFormatDestinationConfigure        | Bestemming van indeling voor elektronische rapportage configureren                |
| PaymAccountsPayablePaymentsClerk    | Leveranciersadministrateur            | ERFormatDestinationRuntimeConfigure | Bestemming van indeling voor elektronische rapportage tijdens runtime configureren |
| PaymAccountsReceivablePaymentsClerk | Klantenadministrateur         | ERFormatDestinationRuntimeConfigure | Bestemming van indeling voor elektronische rapportage tijdens runtime configureren |

> [!NOTE]
> Er worden twee bevoegdheden gebruikt in de voorafgaande taken. Deze bevoegdheden hebben dezelfde naam als de corresponderende rechten: **ERFormatDestinationConfigure** en **ERFormatDestinationRuntimeConfigure**.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen
### <a name="i-have-imported-electronic-configurations-and-i-see-them-on-the-electronic-reporting-configurations-page-but-why-dont-i-see-them-on-the-electronic-reporting-destinations-page"></a>Ik heb elektronische configuraties geïmporteerd en ik zie ze op de pagina Configuraties van elektronische rapportage. Maar waarom zie ik ze niet op de pagina Bestemmingen voor elektronische rapportage?

Zorg ervoor dat u op **Nieuw** klikt en vervolgens een configuratie selecteert in het veld **Verwijzing**. Op de pagina **Bestemmingen voor elektronische rapportage** ziet u alleen configuraties waarvoor bestemmingen zijn geconfigureerd.

### <a name="is-there-any-way-to-define-which-azure-storage-account-and-azure-blob-storage-are-used"></a>Is er een manier om te bepalen welke Azure-opslagaccount en Azure Blob-opslag worden gebruikt?

Nr. Er wordt gebruikgemaakt van de standaard Azure Blob-opslag die is gedefinieerd en gebruikt voor het documentbeheersysteem.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Wat is het doel van de bestandsbestemming in de bestemmingsinstellingen? Wat doet die instelling?

De bestemming **Bestand** wordt gebruikt voor het besturen van een dialoogvenster. Als u deze bestemming inschakelt of als er geen bestemming voor een configuratie is gedefinieerd, ziet u een dialoogvenster voor opslaan of openen nadat er een uitvoerbestand is gemaakt.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Kunt u een voorbeeld geven van de formule die verwijst naar een leveranciersrekening waarnaar ik e-mail kan sturen?

De formule is specifiek voor de ER-configuratie. Als u bijvoorbeeld de configuratie ISO 20022 Kredietoverdracht gebruikt, kunt u **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** of **model.Payments.Creditor.Identification.SourceID** gebruiken om een gekoppelde leveranciersrekening te verkrijgen.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-group-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Een van mijn indelingsconfiguraties bevat meerdere bestanden die zijn gegroepeerd in één map (bijvoorbeeld Map1 bevat Bestand1, Bestand2 en Bestand3). Hoe kan ik op zodanige wijze bestemmingen instellen dat Map1.zip helemaal niet wordt gemaakt, Bestand1 per e-mail wordt verzonden, Bestand2 naar SharePoint wordt verzonden en Bestand3 direct kan worden geopend nadat configuratie is uitgevoerd?

Voorwaarde is dat uw indeling beschikbaar moet zijn in de ER-configuraties. Als u uw indeling hebt, opent u de pagina **Bestemming elektronische rapportage** en maakt u een nieuwe verwijzing naar deze configuratie. Vervolgens moet u vier bestandsbestemmingen hebben, één voor elk uitvoeronderdeel. Maak de eerste bestemming, geeft deze een naam, zoals **Map**, en selecteer een bestandsnaam die een map in uw configuratie vertegenwoordigt. Klik vervolgens op **Instellingen** en zorg ervoor dat alle bestemmingen zijn uitgeschakeld. Voor deze bestandsbestemming wordt de map niet gemaakt. Standaard gedragen bestanden zich op dezelfde manier, vanwege de hiërarchische afhankelijkheden tussen bestanden en bovenliggende mappen. Met andere woorden, zij worden helemaal niet verzonden. Als u dit standaardgedrag wilt overschrijven, moet u nog drie bestandsbestemmingen maken, één voor elk bestand. In de bestandsinstellingen voor elk daarvan, moet u de bestemming inschakelen waar het bestand naartoe moet worden verzonden.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van elektronische rapportage](general-electronic-reporting.md)




