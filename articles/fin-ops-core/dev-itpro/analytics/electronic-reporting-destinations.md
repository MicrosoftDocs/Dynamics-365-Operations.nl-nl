---
title: Bestemmingen van elektronische rapportage (ER)
description: Dit onderwerp biedt informatie over het beheer van ER-bestemmingen (elektronische rapportage), de ondersteunde typen bestemmingen en beveiligingsoverwegingen.
author: nselin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
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
ms.openlocfilehash: 8a6536c82cd3407626fc0d8e102e3819c80cfd4b
ms.sourcegitcommit: 0d9ca44b48fb2e33d8160faccc1e6bd932e58934
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150810"
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

U kunt alleen bestemmingen instellen voor ER-configuraties die zijn [geïmporteerd](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) in het huidige Finance-exemplaar en voor de indelingen die beschikbaar zijn op de pagina **Configuraties van elektronische rapportage**. De functionaliteit voor het beheer van ER-bestemmingen is beschikbaar onder **Organisatiebeheer** \> **Elektronische rapportage** \>**Bestemming voor elektronische rapportage**. Op de pagina **Bestemming voor elektronische rapportage** kunt u het standaardgedrag voor een configuratie vervangen. Geïmporteerde configuraties worden op deze pagina niet weergegeven totdat u **Nieuw** selecteert en vervolgens in het veld **Verwijzing** een configuratie selecteert waarvoor u bestemmingsinstellingen wilt maken.

[![Een configuratie in het veld Verwijzing selecteren](./media/ER_Destinations-SelectFormat.png)](./media/ER_Destinations-SelectFormat.png)

Nadat u een verwijzing hebt gemaakt, kunt u een bestandsbestemming maken voor elke **Map**- of **Bestand**-uitvoeronderdeel van de ER-indeling waarnaar wordt verwezen.

[![Een bestandsbestemming maken](./media/ER_Destinations-ConfigureElementDestination.png)](./media/ER_Destinations-ConfigureElementDestination.png)

Vervolgens kunt u in het dialoogvenster **Bestemmingsinstellingen** de afzonderlijke bestemmingen voor de bestandsbestemming in- en uitschakelen. De knop **instellingen** wordt gebruikt voor het bepalen van alle bestemmingen voor een geselecteerde bestandsbestemming. In het dialoogvenster **Bestemmingsinstellingen** kunt u elke bestemming afzonderlijk bepalen door de optie **Ingeschakeld** hiervoor in te stellen.

In eerdere versies van Finance **dan versie 10.0.9** kunt **één bestandsbestemming** maken voor elk uitvoeronderdeel met dezelfde indeling, zoals een map of een bestand, dat is geselecteerd in het veld **Bestandsnaam**. In **versie 10.0.9 en hoger**kunt u echter **meerdere bestandsbestemmingen**maken voor elk uitvoeronderdeel van dezelfde indeling.

U kunt deze mogelijkheid bijvoorbeeld gebruiken om bestandsbestemmingen te configureren voor een bestandsonderdeel dat wordt gebruikt voor het genereren van een uitgaand document in Excel-indeling. Eén bestemming ([Archief](er-destination-type-archive.md)) kan zo worden geconfigureerd dat het oorspronkelijke Excel-bestand in het ER-takenarchief wordt opgeslagen en een andere bestemming ([E-mail](er-destination-type-email.md)) kan worden geconfigureerd om het Excel-bestand tegelijk te [converteren](#OutputConversionToPDF) naar PDF-indeling en het PDF-bestand via e-mail te verzenden.

[![Meerdere bestemmingen configureren voor een enkel indelingselement](./media/ER_Destinations-SampleDestinations.png)](./media/ER_Destinations-SampleDestinations.png)

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

Tegelijkertijd kunt u meerdere [versies](general-electronic-reporting.md#component-versioning) van de indeling hebben die zijn geïmporteerd in het huidige Finance-exemplaar. U kunt deze weergeven als u de **Configuratie**koppeling selecteert die wordt aangeboden wanneer u het veld **Verwijzing** selecteert.

[![Configuratieversies](./media/ER_Destinations-ConfigurationVersions.png)](./media/ER_Destinations-ConfigurationVersions.png)

Geconfigureerde bestemmingen worden standaard alleen toegepast wanneer u een ER-indelingsversie uitvoert die de status **Voltooid** of **Gedeeld** heeft. U moet echter soms ook geconfigureerde bestemmingen gebruiken wanneer de conceptversie van een ER-indeling wordt uitgevoerd. U wijzigt bijvoorbeeld een conceptversie van uw indeling en u wilt geconfigureerde bestemmingen gebruiken om te testen hoe gegenereerde uitvoer wordt geleverd. Volg deze stappen om bestemmingen toe te passen op een ER-indeling wanneer de conceptversie wordt uitgevoerd.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. Stel de optie **Bestemmingen gebruiken voor conceptstatus**in op **Ja**.

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

De optie PDF-conversie kan alleen worden ingeschakeld voor bestandsonderdelen die worden gebruikt om uitvoer in Microsoft Office Excel- of Word-indeling (**Excel-bestand**) te genereren. Wanneer deze optie is ingeschakeld, wordt de uitvoer die in de Office-indeling is gegenereerd, automatisch geconverteerd naar PDF-indeling.

### <a name="limitations"></a>Beperkingen

> [!NOTE]
> Deze functie is een voorbeeldfunctie en is onderworpen aan de gebruiksvoorwaarden die worden beschreven in [aanvullende gebruiksvoorwaarden voor Microsoft Dynamics 365-voorbeelden](https://go.microsoft.com/fwlink/?linkid=2105274).

> [!NOTE]
> De optie PDF-conversie is alleen beschikbaar voor cloudimplementaties.
>
> De geproduceerde PDF is beperkt tot een maximum van 300 pagina's.
>
> Op dit moment wordt alleen de liggende afdrukstand ondersteund in het PDF-document dat wordt gegenereerd uit een Excel-uitvoer.
>
> Alleen de algemene systeemlettertypen van het Windows-besturingssysteem worden gebruikt voor de conversie van een uitvoer die geen ingesloten lettertypen bevat.

### <a name="use-the-pdf-conversion-option"></a>De optie PDF-conversie gebruiken

Als u PDF-conversie voor een bestandsbestemming wilt inschakelen, schakelt u het selectievakje **Converteren naar PDF** in.

[![PDF-conversie voor een bestandsbestemming inschakelen](./media/ER_Destinations-TurnOnPDFConversion.png)](./media/ER_Destinations-TurnOnPDFConversion.png)

### <a name=""></a><a name="SelectPdfPageOrientation">Een afdrukstand voor PDF-conversie selecteren</a>

Als u een ER-configuratie genereert in Excel-indeling en deze wilt converteren naar PDF-indeling, kunt u de afdrukstand van de PDF opgeven. Wanneer u het selectievakje **Converteren naar PDF** inschakelt om PDF-conversie in te schakelen voor een bestandsbestemming die een uitvoerbestand produceert in Excel-indeling, wordt het veld **Afdrukstand** beschikbaar op het sneltabblad **Instellingen PDF-conversie**. Selecteer de gewenste afdrukstand in het veld **Afdrukstand**.

[![Een afdrukstand voor PDF-conversie selecteren](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)](./media/ER_Destinations-SelectPDFConversionPageOrientation.png)

> [!NOTE]
> Als u de afdrukstand van de PDF wilt inschakelen, moet u Microsoft Dynamics 365 Finance versie 10.0.10 (mei 2020) of hoger installeren.
>
> De geselecteerde afdrukstand wordt toegepast op alle ER-configuraties die in de Excel-indeling worden gegenereerd en worden vervolgens geconverteerd naar de PDF-indeling.
>
> Als een geconverteerde PDF wordt gemaakt van een ER-configuratie in Word-indeling, wordt de afdrukstand van de PDF uit het Word-document opgehaald.

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

De bestemming **Bestand** wordt gebruikt voor het besturen van een dialoogvenster. Als u deze bestemming inschakelt of als er geen bestemming voor een configuratie is gedefinieerd, wordt een dialoogvenster voor opslaan of openen weergegeven nadat er een uitvoerbestand is gemaakt.

### <a name="can-you-give-an-example-of-the-formula-that-refers-to-a-vendor-account-that-i-can-send-email-to"></a>Kunt u een voorbeeld geven van de formule die verwijst naar een leveranciersrekening waarnaar ik e-mail kan sturen?

De formule is specifiek voor de ER-configuratie. Als u bijvoorbeeld de configuratie ISO 20022 Kredietoverdracht gebruikt, kunt u **'$PaymentsForCoveringLetter'.Creditor.Identification.SourceID** of **model.Payments.Creditor.Identification.SourceID** gebruiken om een gekoppelde leveranciersrekening te verkrijgen.

### <a name="one-of-my-format-configurations-contains-multiple-files-that-are-grouped-into-one-folder-for-example-folder1-contains-file1-file2-and-file3-how-do-i-set-up-destinations-so-that-folder1zip-isnt-created-at-all-file1-is-sent-by-email-file2-is-sent-to-sharepoint-and-i-can-open-file3-immediately-after-the-configuration-is-run"></a>Een van mijn indelingsconfiguraties bevat meerdere bestanden die zijn gegroepeerd in één map (bijvoorbeeld Map1 bevat Bestand1, Bestand2 en Bestand3). Hoe kan ik op zodanige wijze bestemmingen instellen dat Map1.zip helemaal niet wordt gemaakt, Bestand1 per e-mail wordt verzonden, Bestand2 naar SharePoint wordt verzonden en Bestand3 direct kan worden geopend nadat configuratie is uitgevoerd?

Uw indeling moet eerst beschikbaar zijn in de ER-configuraties. Als aan deze voorwaarde is voldaan, opent u de pagina **Bestemming elektronische rapportage** en maakt u een nieuwe verwijzing naar de configuratie. Vervolgens moet u vier bestandsbestemmingen hebben, één voor elk uitvoeronderdeel. Maak de eerste bestemming, geeft deze een naam, zoals **Map**, en selecteer een bestandsnaam die een map in uw configuratie vertegenwoordigt. Selecteer **Instellingen** en zorg ervoor dat alle bestemmingen zijn uitgeschakeld. Voor deze bestandsbestemming wordt de map niet gemaakt. Standaard gedragen bestanden zich op dezelfde manier, vanwege de hiërarchische afhankelijkheden tussen bestanden en bovenliggende mappen. Met andere woorden, zij worden helemaal niet verzonden. Als u dit standaardgedrag wilt overschrijven, moet u nog drie bestandsbestemmingen maken, één voor elk bestand. In de bestandsinstellingen voor elk daarvan, moet u de bestemming inschakelen waar het bestand naartoe moet worden verzonden.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)
