---
title: Bestemmingen van elektronische rapportage (ER)
description: Dit onderwerp biedt informatie over het beheer van ER-bestemmingen (elektronische rapportage), de ondersteunde typen bestemmingen en beveiligingsoverwegingen.
author: nselin
manager: tfehr
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 0fe0992412edf6f78be4ed293052e3501a7224ad
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569714"
---
# <a name="electronic-reporting-er-destinations"></a>Bestemmingen van elektronische rapportage (ER)

[!include [banner](../includes/banner.md)]

U kunt een bestemming voor elke ER-indelingsconfiguratie (Elektronische Rapportage) en de bijbehorende uitvoercomponent (een map of een bestand) configureren. Gebruikers die over de juiste toegangsrechten beschikken, kunnen tevens bestemmingsinstellingen wijzigen tijdens de uitvoering. In dit onderwerp worden ER-bestemmingsbeheer, de typen bestemmingen die worden ondersteund en beveiligingsoverwegingen beschreven.

Indelingsconfiguraties voor Elektronische rapportage (ER) bevatten meestal minimaal één uitvoeronderdeel: een bestand. Configuraties bevatten gewoonlijk meerdere onderdelen voor bestandsuitvoer van verschillende typen (bijvoorbeeld XML, TXT, XLSX, DOCX of PDF) die zijn gegroepeerd in een enkele map of in meerdere mappen. ER-bestemmingsbeheer stelt u in staat vooraf te configureren wat er gebeurt wanneer elk onderdeel wordt uitgevoerd. Wanneer een configuratie wordt uitgevoerd, wordt standaard een dialoogvenster weergegeven waarin u het bestand kunt opslaan of openen. Hetzelfde gedrag doet zich ook voor wanneer u een ER-configuratie importeert en geen specifieke bestemmingen hiervoor configureert. Nadat u een bestemming voor een hoofduitvoeronderdeel hebt gemaakt, overschrijft die bestemming het standaardgedrag en wordt de map of het bestand verzonden op basis van de instellingen van de bestemming.

## <a name="availability-and-general-prerequisites"></a>Beschikbaarheid en algemene vereisten

De functionaliteit voor ER-bestemmingen is niet beschikbaar in Microsoft Dynamics AX 7.0 (februari 2016). Daarom moet u Microsoft Dynamics 365 for Operations versie 1611 (november 2016) of hoger installeren als u de volgende bestemmingstypen wilt gebruiken:

- [E-mailadres](er-destination-type-email.md)
- [Archiveren](er-destination-type-archive.md)
- [Bestand](er-destination-type-file.md)
- [Scherm](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)

U kunt ook een van de volgende vereisten installeren. Houd er echter rekening mee dat deze alternatieven een beperktere versie van ER-bestemmingen biedt.

- Microsoft Dynamics AX-toepassingsversie 7.0.1 (mei 2016)
- [Hotfix voor bestemmingsbeheer van toepassing voor elektronische rapportage](https://fix.lcs.dynamics.com/issue/results/?q=3160213)

Er is ook een bestemmingstype [Afdrukken](er-destination-type-print.md). Als u deze wilt gebruiken, moet u Microsoft Dynamics 365 Finance versie 10.0.9 (april 2020) installeren.

## <a name="overview"></a>Overzicht

U kunt alleen bestemmingen instellen voor ER-configuraties die zijn [geïmporteerd](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) in het huidige Finance-exemplaar en voor de indelingen die beschikbaar zijn op de pagina **Configuraties van elektronische rapportage**. De functionaliteit voor het beheer van ER-bestemmingen is beschikbaar onder **Organisatiebeheer** \> **Elektronische rapportage** \> **Bestemming voor elektronische rapportage**.

### <a name="default-behavior"></a>Standaardgedrag

Het standaardgedrag voor een ER-indelingsconfiguratie is afhankelijk van het type uitvoering dat u opgeeft wanneer een ER-indeling wordt gestart.

Als u de optie voor **Batchverwerking** instelt op **Nee**, wordt in het dialoogvenster **Intrastat-rapport** op het sneltabblad **Op de achtergrond uitvoeren** een ER-indeling direct in de interactieve modus uitgevoerd. Wanneer deze uitvoering is voltooid, wordt een gegenereerd uitgaand document beschikbaar gemaakt voor downloaden.

Als u de optie **Batchverwerking** instelt op **Ja**, wordt er een ER-indeling uitgevoerd in [batch](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/batch-processing-overview)modus. De desbetreffende batchtaak wordt gemaakt op basis van de parameters die u opgeeft op het tabblad **Op de achtergrond uitvoeren** van het dialoogvenster **ER-parameters**.

> [!NOTE]
> De taakomschrijving informeert u over de uitvoering van een ER-indelingstoewijzing. Ook bevat deze de naam van de ER-component die wordt uitgevoerd.

[![Een ER-indeling uitvoeren](./media/ER_Destinations-RunInBatchMode.png)](./media/ER_Destinations-RunInBatchMode.png)

U kunt op verschillende plaatsen informatie over deze taak vinden:

- Ga naar **Algemeen** \> **Query's** \> **Batchtaken** \> **Mijn batchtaken** om de status van de geplande taak te controleren.
- Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Elektronische rapportagetaken** om de status van de geplande taak en de uitvoeringsresultaten van de voltooide taak te controleren. Wanneer de taakuitvoering is voltooid, selecteert u **Bestanden weergeven** op de pagina **Elektronische rapportagetaken** om een gegenereerd uitgaand document op te halen.

    > [!NOTE]
    > Dit document wordt opgeslagen als een bijlage van de huidige taakrecord en wordt aangestuurd door het raamwerk voor [documentbeheer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management). Het [documenttype](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-document-management#configure-document-types) dat wordt gebruikt voor het opslaan van ER-artefacten van dit type, wordt geconfigureerd in de [ER-parameters](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents).

- Selecteer op de pagina **Elektronische rapportagetaken** de optie **Bestanden weergeven** om de lijst met fouten en waarschuwingen weer te geven die tijdens de uitvoering van de taak zijn gegenereerd.

    [![De lijst met ER-taken bekijken](./media/ER_Destinations-ReviewERJobs.png)](./media/ER_Destinations-ReviewERJobs.png)

### <a name="user-configured-behavior"></a>Door gebruiker geconfigureerd gedrag

Op de pagina **Bestemming voor elektronische rapportage** kunt u het standaardgedrag voor een configuratie vervangen. Geïmporteerde configuraties worden op deze pagina niet weergegeven totdat u **Nieuw** selecteert en vervolgens in het veld **Verwijzing** een configuratie selecteert waarvoor u bestemmingsinstellingen wilt maken.

[![Een configuratie in het veld Verwijzing selecteren](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

Nadat u een verwijzing hebt gemaakt, kunt u een bestandsbestemming maken voor elke **Map**- of **Bestand**-uitvoeronderdeel van de ER-indeling waarnaar wordt verwezen.

[![Een bestandsbestemming maken](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

Vervolgens kunt u in het dialoogvenster **Bestemmingsinstellingen** de afzonderlijke bestemmingen voor de bestandsbestemming in- en uitschakelen. De knop **instellingen** wordt gebruikt voor het bepalen van alle bestemmingen voor een geselecteerde bestandsbestemming. In het dialoogvenster **Bestemmingsinstellingen** kunt u elke bestemming afzonderlijk bepalen door de optie **Ingeschakeld** hiervoor in te stellen.

In eerdere versies van Finance **dan versie 10.0.9** kunt **één bestandsbestemming** maken voor elk uitvoeronderdeel met dezelfde indeling, zoals een map of een bestand, dat is geselecteerd in het veld **Bestandsnaam**. In **versie 10.0.9 en hoger** kunt u echter **meerdere bestandsbestemmingen** maken voor elk uitvoeronderdeel van dezelfde indeling.

U kunt deze mogelijkheid bijvoorbeeld gebruiken om bestandsbestemmingen te configureren voor een bestandsonderdeel dat wordt gebruikt voor het genereren van een uitgaand document in Excel-indeling. Eén bestemming ([Archief](er-destination-type-archive.md)) kan zo worden geconfigureerd dat het oorspronkelijke Excel-bestand in het ER-takenarchief wordt opgeslagen en een andere bestemming ([E-mail](er-destination-type-email.md)) kan worden geconfigureerd om het Excel-bestand tegelijk te [converteren](#OutputConversionToPDF) naar PDF-indeling en het PDF-bestand via e-mail te verzenden.

[![Meerdere bestemmingen configureren voor een enkel indelingselement](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

Wanneer u een ER-indeling uitvoert, worden alle bestemmingen die zijn geconfigureerd voor componenten van de indeling altijd uitgevoerd. In Finance **versie 10.0.17 en hoger** is de functionaliteit van ER-bestemmingen bovendien verbeterd en kunt u nu verschillende sets bestemmingen configureren voor één ER-indeling. Deze configuratie markeert elke set als geconfigureerd voor een bepaalde gebruikersactie. De ER API is [uitgebreid](er-apis-app10-0-17.md), zodat een actie kan worden geleverd die de gebruiker uitvoert door een ER-indeling uit te voeren. De geleverde actiecode wordt doorgegeven aan ER-bestemmingen. U kunt verschillende bestemmingen van een ER-indeling uitvoeren, afhankelijk van de opgegeven actiecode. Zie [ER-bestemmingen configureren die afhankelijk zijn van acties](er-action-dependent-destinations.md) voor meer informatie.

## <a name="destination-types"></a>Bestemmingstypen

De volgende bestemmingen worden momenteel ondersteund voor ER-indelingen. U kunt alle typen tegelijkertijd uit- of inschakelen. Op die manier kunt u niets doen of het onderdeel naar alle geconfigureerde bestemmingen verzenden.

- [E-mailadres](er-destination-type-email.md)
- [Archiveren](er-destination-type-archive.md)
- [Bestand](er-destination-type-file.md)
- [Scherm](er-destination-type-screen.md)
- [Power BI](er-destination-type-powerbi.md)
- [Afdrukken](er-destination-type-print.md)

## <a name="applicability"></a>Toepasbaarheid

U kunt alleen bestemmingen instellen voor ER-configuraties die zijn geïmporteerd en voor de indelingen die beschikbaar zijn op de pagina **Configuraties van elektronische rapportage**.

> [!NOTE]
> Geconfigureerde bestemmingen zijn bedrijfsspecifiek. Als u van plan bent een ER-indeling te gebruiken in verschillende bedrijven van het huidige Finance-exemplaar, moet u voor elk van deze bedrijven bestemmingen configureren voor die ER-indeling.

Wanneer u bestandsbestemmingen voor een geselecteerde indeling configureert, configureert u deze voor de gehele indeling.

[![Configuratiekoppeling](./media/ER_Destinations-ConfigurationLink.png)](./media/ER_Destinations-ConfigurationLink.png)

Tegelijkertijd kunt u meerdere [versies](general-electronic-reporting.md#component-versioning) van de indeling hebben die zijn geïmporteerd in het huidige Finance-exemplaar. U kunt deze weergeven als u de koppeling **Configuratie** selecteert die wordt aangeboden wanneer u het veld **Verwijzing** selecteert.

[![Configuratieversies](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

Geconfigureerde bestemmingen worden standaard alleen toegepast wanneer u een ER-indelingsversie uitvoert die de status **Voltooid** of **Gedeeld** heeft. U moet echter soms ook geconfigureerde bestemmingen gebruiken wanneer de conceptversie van een ER-indeling wordt uitgevoerd. U wijzigt bijvoorbeeld een conceptversie van uw indeling en u wilt geconfigureerde bestemmingen gebruiken om te testen hoe gegenereerde uitvoer wordt geleverd. Volg deze stappen om bestemmingen toe te passen op een ER-indeling wanneer de conceptversie wordt uitgevoerd.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. Stel de optie **Bestemmingen gebruiken voor conceptstatus** in op **Ja**.

[![Optie Bestemmingen voor conceptstatus](./media/ER_Destinations-UserSetting1.png)](./media/ER_Destinations-UserSetting1.png)

Als u de conceptversie van een ER-indeling wilt gebruiken, moet u de ER-indeling dienovereenkomstig markeren.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. Stel de optie **Instelling uitvoeren** in op **Ja**.

[![Optie Instelling uitvoeren](./media/ER_Destinations-UserSetting2.png)](./media/ER_Destinations-UserSetting2.png)

Nadat u deze instellingen hebt voltooid, wordt de optie **Concept uitvoeren** beschikbaar voor ER-indelingen die u wijzigt. Stel deze optie in op **Ja** als u de conceptversie van de indeling wilt gaan gebruiken wanneer de indeling wordt uitgevoerd.

[![Optie Concept uitvoeren](./media/ER_Destinations-FormatSetting.png)](./media/ER_Destinations-FormatSetting.png)

## <a name="destination-failure-handling"></a><a name="DestinationFailure"></a>Afhandeling van bestemmingsfouten

Meestal wordt een ER-indeling uitgevoerd binnen een specifiek bedrijfsproces. De levering van een uitgaand document dat tijdens het uitvoeren van een ER-indeling wordt gegenereerd, moet echter soms worden beschouwd als onderdeel van dat bedrijfsproces. Als in dit geval de levering van een gegenereerd uitgaand document naar een geconfigureerde bestemming mislukt, moet de uitvoering van het bedrijfsproces worden geannuleerd. Selecteer de optie **Verwerking stoppen bij fout** om de gewenste ER-bestemming te configureren.

U kunt bijvoorbeeld de verwerking van leveranciersbetalingen zodanig configureren dat de ER-indeling **ISO20022-kredietoverdracht** wordt uitgevoerd om het betalingsbestand en aanvullende documenten te genereren (bijvoorbeeld de begeleidende brief en het controlerapport). Als een betaling alleen als correct verwerkt moet worden beschouwd als de begeleidende brief via e-mail is afgeleverd, schakelt u het selectievakje **Verwerking stoppen bij fout** in voor het onderdeel **Begeleidende brief** in de betreffende bestandsbestemming, zoals in de volgende afbeelding wordt weergegeven. In dit geval wordt de status van de betaling die is geselecteerd voor verwerking, gewijzigd van **Geen** in **Verzonden** wanneer de begeleidende brief die is gegenereerd, wordt geaccepteerd voor levering door een e-mailprovider die in het Finance-exemplaar is geconfigureerd.

[![Procesverwerking voor fout met bestandsbestemming configureren](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)](./media/ER_Destinations-StopProcessingAtDestinationFailure.png)

Als u het selectievakje **Verwerking stoppen bij fout** hebt ingeschakeld voor het onderdeel **Begeleidende brief** in de bestemming, wordt een betaling als correct verwerkt beschouwd, zelfs als de begeleidende brief niet via e-mail is afgeleverd. De status van de betaling wordt gewijzigd van **Geen** in **Verzonden**, zelfs als de begeleidende brief niet kan worden verzonden, omdat bijvoorbeeld het e-mailadres van de ontvanger of afzender ontbreekt of onjuist is.

## <a name="output-conversion-to-pdf"></a><a name="OutputConversionToPDF"></a>Uitvoerconversie naar PDF

U kunt de optie PDF-conversie gebruiken om de uitvoer in Microsoft Office-indeling (Excel/Word) te converteren naar PDF-indeling.

### <a name="make-pdf-conversion-available"></a>PDF-conversie beschikbaar maken

Om de PDF-conversie optie beschikbaar te maken in het huidige Finance-exemplaar, opent u het werkgebied **Functiebeheer** en schakelt u de functie **Uitgaande ER-documenten van Microsoft Office-indelingen converteren naar PDF** in.

[![De functie PDF-conversie van uitgaande documenten in Functiebeheer inschakelen](./media/ER_Destinations-EnablePdfConversionFeature.png)](./media/ER_Destinations-EnablePdfConversionFeature.png)

### <a name="applicability"></a>Toepasbaarheid

De optie PDF-conversie kan alleen worden ingeschakeld voor bestandsonderdelen die worden gebruikt om uitvoer in Office- (Excel of Word) indeling (**Excel-bestand**) te genereren. Wanneer deze optie is ingeschakeld, wordt de uitvoer die in de Office-indeling is gegenereerd, automatisch geconverteerd naar PDF-indeling. In versies van Finance **vóór 10.0.18** kunt u deze optie alleen inschakelen voor onderdelen van het type **Excel\\File** waarmee uitvoer in [Excel](er-fillable-excel.md)- of [Word](er-design-configuration-word.md)-indeling wordt gegenereerd. In versie **10.0.18 en hoger** kunt u deze optie echter ook inschakelen voor onderdelen van het type **Common\\File**.

> [!NOTE]
> Let goed op het waarschuwingsbericht dat u ontvangt wanneer u de PDF-conversieoptie inschakelt voor een ER-onderdeel van het type **Common\\File**. In dit bericht wordt aangegeven dat u bij het ontwerpen niet kunt garanderen dat het geselecteerde bestandsonderdeel de inhoud in PDF-indeling of de naar PDF converteerbare inhoud tijdens runtime beschikbaar zal maken. U moet de optie daarom alleen instellen als u zeker weet dat het geselecteerde bestandsonderdeel is geconfigureerd om de inhoud in PDF-indeling of de naar PDF converteerbare inhoud tijdens runtime beschikbaar te maken.
> 
> Als u de PDF-conversieoptie instelt voor een onderdeel van het type **Excel\\File**, als dat onderdeel inhoud in een andere indeling dan PDF beschikbaar maakt en als de beschikbaar gestelde inhoud niet naar PDF-indeling kan worden geconverteerd, treedt er een uitzondering op tijdens runtime. Het bericht dat u ontvangt, geeft aan dat de gegenereerde inhoud niet kan worden geconverteerd naar PDF-indeling.

### <a name="limitations"></a>Beperkingen

De optie PDF-conversie is alleen beschikbaar voor cloudimplementaties.

De geproduceerde PDF is beperkt tot een maximumlengte van 300 pagina's.

In Finance **versie 10.0.9** wordt alleen de liggende afdrukstand ondersteund in het PDF-document dat wordt gegenereerd uit een Excel-uitvoer. In Finance **versie 10.0.10 (mei 2020) en hoger** kunt u [de afdrukstand opgeven](#SelectPdfPageOrientation) in het PDF-document dat wordt gemaakt op basis van de Excel-uitvoer als u de ER-bestemming configureert.

Alleen de algemene systeemlettertypen van het Windows-besturingssysteem worden gebruikt om uitvoer te converteren die geen ingesloten lettertypen bevat.

### <a name="use-the-pdf-conversion-option"></a>De optie PDF-conversie gebruiken

Als u PDF-conversie voor een bestandsbestemming wilt inschakelen, schakelt u het selectievakje **Converteren naar PDF** in.

[![PDF-conversie voor een bestandsbestemming inschakelen](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

### <a name=""></a><a name="SelectPdfPageOrientation">Een afdrukstand voor PDF-conversie selecteren</a>

Als u een ER-configuratie genereert in Excel-indeling en deze wilt converteren naar PDF-indeling, kunt u de afdrukstand van het PDF-document opgeven. Wanneer u het selectievakje **Converteren naar PDF** inschakelt om PDF-conversie in te schakelen voor een bestandsbestemming die een uitvoerbestand produceert in Excel-indeling, wordt het veld **Afdrukstand** beschikbaar op het sneltabblad **Instellingen PDF-conversie**. Selecteer de gewenste afdrukstand in het veld **Afdrukstand**.

[![Een afdrukstand voor PDF-conversie selecteren](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)

> [!NOTE]
> Als u de afdrukstand van de PDF wilt kunnen kiezen, moet u Finance versie 10.0.10 of hoger installeren.
>
> De geselecteerde afdrukstand wordt toegepast op alle ER-configuraties die in de Excel-indeling worden gegenereerd en worden vervolgens geconverteerd naar de PDF-indeling.
>
> Als een ER-configuratie in Word-indeling wordt geconverteerd naar PDF-indeling, wordt de afdrukstand van de PDF uit het Word-document opgehaald.

## <a name="security-considerations"></a>Beveiligingsoverwegingen

Twee typen machtigingen en rechten worden gebruikt voor ER-bestemmingen. Eén type regelt de algemene mogelijkheid voor gebruikers om de bestemmingen te onderhouden die worden geconfigureerd voor een rechtspersoon (dat wil zeggen, dat dit toegang tot de pagina **Bestemmingen voor elektronische rapportage** beheert). Het andere type regelt de mogelijkheid van een toepassingsgebruiker om, tijdens de uitvoering, de bestemmingsinstellingen die zijn geconfigureerd door een ER-ontwikkelaar of functionele ER-consultant te vervangen.

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

Klik op **Nieuw** en selecteer een configuratie in het veld **Verwijzing**. Op de pagina **Bestemmingen voor elektronische rapportage** ziet u alleen configuraties waarvoor bestemmingen zijn geconfigureerd.

### <a name="is-there-any-way-to-define-which-microsoft-azure-storage-account-and-azure-blob-storage-are-used"></a>Is er een manier om te bepalen welk Microsoft Azure-opslagaccount en welke Azure Blob-opslag worden gebruikt?

Nr. Er wordt gebruikgemaakt van de standaard Microsoft Azure Blob-opslag die is gedefinieerd en gebruikt voor het documentbeheersysteem.

### <a name="what-is-the-purpose-of-the-file-destination-in-the-destination-settings-what-does-that-setting-do"></a>Wat is het doel van de bestandsbestemming in de bestemmingsinstellingen? Wat doet die instelling?

De bestemming **Bestand** wordt gebruikt om een dialoogvenster van uw webbrowser te beheren wanneer u een ER-indeling in de interactieve modus uitvoert. Als u deze bestemming inschakelt of als er geen bestemming voor een configuratie is gedefinieerd, wordt een dialoogvenster voor opslaan of openen in uw webbrowser weergegeven nadat er een uitvoerbestand is gemaakt.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Kunt u een voorbeeld geven van de formule die verwijst naar een leveranciersrekening waarnaar ik e-mail kan sturen?

De formule is specifiek voor de ER-configuratie. Als u bijvoorbeeld de configuratie ISO 20022 Kredietoverdracht gebruikt, kunt u **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** of **model.Payments.Creditor.Identification.SourceID** gebruiken om een gekoppelde leveranciersrekening te verkrijgen.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Een van mijn indelingsconfiguraties bevat meerdere bestanden die zijn gegroepeerd in één map (bijvoorbeeld Map1 bevat Bestand1, Bestand2 en Bestand3). Hoe kan ik op zodanige wijze bestemmingen instellen dat Map1.zip helemaal niet wordt gemaakt, Bestand1 per e-mail wordt verzonden, Bestand2 naar SharePoint wordt verzonden en Bestand3 direct kan worden geopend nadat configuratie is uitgevoerd?

Uw indeling moet eerst beschikbaar zijn in de ER-configuraties. Als aan deze voorwaarde is voldaan, opent u de pagina **Bestemming elektronische rapportage** en maakt u een nieuwe verwijzing naar de configuratie. Vervolgens moet u vier bestandsbestemmingen hebben, één voor elk uitvoeronderdeel. Maak de eerste bestemming, geeft deze een naam, zoals **Map**, en selecteer een bestandsnaam die een map in uw configuratie vertegenwoordigt. Selecteer **Instellingen** en zorg ervoor dat alle bestemmingen zijn uitgeschakeld. Voor deze bestandsbestemming wordt de map niet gemaakt. Standaard gedragen bestanden zich op dezelfde manier, vanwege de hiërarchische afhankelijkheden tussen bestanden en bovenliggende mappen. Met andere woorden, zij worden helemaal niet verzonden. Als u dit standaardgedrag wilt overschrijven, moet u nog drie bestandsbestemmingen maken, één voor elk bestand. In de bestandsinstellingen voor elk daarvan, moet u de bestemming inschakelen waar het bestand naartoe moet worden verzonden.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)

[Actieafhankelijke ER-bestemmingen configureren](er-action-dependent-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
