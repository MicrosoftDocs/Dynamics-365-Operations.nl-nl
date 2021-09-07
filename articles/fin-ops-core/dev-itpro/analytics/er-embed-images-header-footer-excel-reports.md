---
title: Een ER-indeling ontwerpen om een rapport in Excel-indeling te genereren met ingesloten afbeeldingen in paginakopteksten of -voetteksten
description: In dit onderwerp wordt uitgelegd hoe u het hulpmiddel voor elektronische rapportage (ER) kunt gebruiken om bedrijfsdocumenten te genereren met ingesloten afbeeldingen en vormen in paginakopteksten of -voetteksten.
author: NickSelin
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-06-01
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 20bcf26e1510634c5ee7043576a480ce15889923
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344115"
---
# <a name="design-an-er-format-to-generate-a-report-in-excel-format-with-embedded-images-in-page-headers-or-footers"></a>Een ER-indeling ontwerpen om een rapport in Excel-indeling te genereren met ingesloten afbeeldingen in paginakopteksten of -voetteksten

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe een gebruiker in de rol Systeembeheerder of Functioneel consultant elektronische rapportage deze taken kan uitvoeren:

- Parameters configureren voor het [ER-raamwerk (elektronische rapportage)](general-electronic-reporting.md).
- ER-[configuraties](general-electronic-reporting.md#Configuration) die door Microsoft worden [geleverd](general-electronic-reporting.md#Provider) en worden gebruikt om [vrije-tekstfacturen](../../../finance/accounts-receivable/create-free-text-invoice-new.md) te genereren op basis van een [sjabloon](er-fillable-excel.md#excel-file-component) in Microsoft Excel-indeling.
- Een [aangepaste (afgeleide)](general-electronic-reporting.md#building-a-format-selecting-another-format-as-a-base-customization) versie maken van een standaardconfiguratie voor een ER-indeling die door Microsoft wordt geleverd.
- Wijzig de aangepaste ER-indelingsconfiguratie, zodat er een vrije-tekstfactuurrapport wordt gegenereerd met een afbeelding van het bedrijfslogo in de voettekst.

De procedures in dit onderwerp kunnen in het bedrijf **USMF** worden uitgevoerd. U hoeft hiervoor geen code te schrijven. Voordat u begint, moet u het volgende bestand downloaden en opslaan.

| Beschrijving        | Bestandsnaam |
|--------------------|-----------|
| Afbeelding met bedrijfslogo | [png-bestand met bedrijfslogo](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png) |

## <a name="content"></a>Inhoud

- [De rechtspersoon configureren](#ConfigureLegalEntity)
- [Het ER-raamwerk configureren](#ConfigureFramework)

    - [ER-parameters configureren](#ConfigureParameters)
    - [Een ER-configuratieprovider activeren](#ActivateProvider)

        - [De lijst met ER-configuratie providers bekijken](#ReviewProvidersList)
        - [Een nieuwe ER-configuratieprovider toevoegen](#AddProvider)
        - [De nieuwe ER-configuratieprovider activeren](#ActivateAddedProvider)

- [De standaardconfiguraties voor ER-indeling importeren](#ImportERSolution1)

    - [De standaard-ER-configuraties importeren](#ImportERFormat)
    - [De geïmporteerde ER-configuraties bekijken](#ReviewImportedERSolution)

- [Een vrije-tekstfactuur afdrukken met de standaard ER-indeling](#PrintInvoice1)

    - [Afdrukbeheer instellen](#ConfigurePrintManagement1)
    - [Een vrije-tekstfactuur afdrukken](#ProcessInvoice1)

- [De standaard-ER-indeling aanpassen](#CustomizeProvidedFormat)

    - [Een aangepaste indeling maken](#DeriveProvidedFormat)
    - [De aangepaste indeling bewerken](#ConfigureDerivedFormat)
    - [De aangepaste indeling markeren als uitvoerbaar](#MarkFormatRunnable)

- [Een vrije-tekstfactuur afdrukken met de aangepaste ER-indeling](#PrintInvoice2)

    - [Afdrukbeheer instellen](#ConfigurePrintManagement2)
    - [Een vrije-tekstfactuur afdrukken](#ProcessInvoice2)

- [Aanvullende bronnen](#References)

## <a name="configure-the-legal-entity"></a><a id="ConfigureLegalEntity"></a>De rechtspersoon configureren

1. Ga naar **Organisatiebeheer** \> **Organisaties** \> **Rechtspersonen**.
2. Selecteer **Wijzigen** op de pagina **Rechtspersonen** op het sneltabpagina **Rapportbedrijfslogo**.
3. Selecteer **Bladeren** in het dialoogvenster **Afbeelding selecteren om te uploaden** en selecteer het bestand **Bedrijfslogo.png** dat u eerder hebt gedownload.
4. Selecteer **Opslaan** en sluit de pagina **Rechtspersonen**.

![Afbeelding van bedrijfslogo die is geselecteerd op de pagina Rechtspersonen.](./media/er-embed-images-header-footer-excel-reports-company-logo-image.png)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a>Het ER-raamwerk configureren

Als u een gebruiker bent in de rol Functioneel consultant elektronische rapportage, moet u de minimale set ER-parameters configureren voordat u het ER-framework kunt gaan gebruiken om een aangepaste versie van een standaard-ER-indeling te ontwerpen.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>ER-parameters configureren

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Parameters van elektronische rapportage**.
3. Stel op de pagina **Parameters van elektronische rapportage** op het tabblad **Algemeen** de optie **Ontwerpmodus inschakelen** in op **Ja**.
4. Stel op het tabblad **Bijlagen** de volgende parameters in:

    - Selecteer in het veld **Configuraties** het type **Bestand** voor het bedrijf **USMF**.
    - Selecteer in de velden **Taakarchief**, **Tijdelijk**, **Basislijn** en **Overige** het type **Bestand**.

Meer informatie over het configureren van ER-parameters vindt u in [Het ER-raamwerk configureren](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Een ER-configuratieprovider activeren

Elke ER-configuratie die wordt toegevoegd, wordt gemarkeerd als het eigendom van een ER-configuratieprovider. De ER-configuratieprovider die is geactiveerd in de werkruimte **Elektronische rapportage** wordt hiervoor gebruikt. Daarom moet u een ER-configuratieprovider activeren in de werkruimte **Elektronische rapportage** voordat u ER-configuraties gaat toevoegen of bewerken.

> [!NOTE]
> Een ER-configuratie kan alleen worden bewerkt door de eigenaar van de configuratie. Voordat een ER-configuratie kan worden bewerkt, moet een geschikte ER-configuratieprovider worden geactiveerd in het werkgebied **Elektronische rapportage**.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>De lijst met ER-configuratie providers bekijken

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Configuratieproviders**.
3. Op de tabelpagina **Configuratieproviders** heeft elke providerrecord een unieke naam en een unieke URL. Bekijk de inhoud van deze pagina. Als er al een record bestaat voor **Litware, Inc.** (`https://www.litware.com`), kunt u de volgende procedure, [Een nieuwe ER-configuratieprovider toevoegen](#AddProvider), overslaan.

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Een nieuwe ER-configuratieprovider toevoegen

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Configuratieproviders**.
3. Selecteer **Nieuw** op de pagina **Configuratieproviders**.
4. Voer in het veld **Naam** de tekst **Litware, Inc.** in.
5. Voer in het veld **Internetadres** de tekst `https://www.litware.com` in.
6. Selecteer **Opslaan**.

#### <a name="activate-the-new-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>De nieuwe ER-configuratieprovider activeren

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** de tegel **Litware, Inc.** en selecteer **Instellen als actief**.

Meer informatie over ER-configuratieproviders vindt u in [Configuratieproviders maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a>De standaardconfiguraties voor ER-indeling importeren

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat"></a>De standaard-ER-configuraties importeren

Als u de standaard-ER-configuraties wilt toevoegen aan uw huidige exemplaar van Microsoft Dynamics 365 Finance, moet u deze importeren vanuit de ER-[opslagplaats](general-electronic-reporting.md#Repository) die voor dat exemplaar is geconfigureerd.

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** de tegel **Microsoft** en selecteer vervolgens **Opslagplaatsen** om de lijst met opslagplaatsen voor de provider **Microsoft** weer te geven.
3. Selecteer op de pagina **Opslagplaats van configuraties** de opslagplaats van het type **Algemeen** en selecteer vervolgens **Openen**. Als u wordt gevraagd om toestemming te geven om verbinding te maken met de [Regulatory Configuration Service](../../../finance/localizations/rcs-overview.md), volgt u de instructies voor autorisatie.
4. Selecteer op de pagina **Opslagplaats van configuratie** in de configuratiestructuur in het linkerdeelvenster de indelingsconfiguratie **Vrije-tekstfactuur (Excel)**.
5. Selecteer op het sneltabblad **Versies** de meest recente versie (bijvoorbeeld **240.112**) van de geselecteerde ER-indelingsconfiguratie.
6. Selecteer **Importeren** om de geselecteerde versie vanuit de algemene opslagplaats te downloaden naar het huidige Finance-exemplaar.

![De standaard ER-configuraties importeren op de pagina Opslagplaats van configuratie.](./media/er-embed-images-header-footer-excel-reports-import-solution.png)

> [!TIP]
> Als u problemen ondervindt met de toegang tot de [globale opslagplaats](er-download-configurations-global-repo.md), kunt u in plaats daarvan [configuraties downloaden](download-electronic-reporting-configuration-lcs.md) van Microsoft Dynamics Lifecycle Services (LCS).

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a>De geïmporteerde ER-configuraties bekijken

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuraties** de tegel **Rapportconfiguraties**.
3. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster **Factuurmodel** uit.
4. Naast de geselecteerde ER-indeling **Vrije-tekstfactuur (Excel)** zijn er andere vereiste ER-configuraties geïmporteerd. Controleer of de volgende ER-configuraties beschikbaar zijn in de configuratiestructuur:

    - **Factuurmodel**: Deze configuratie bevat het ER-onderdeel [Gegevensmodel](general-electronic-reporting.md#data-model-and-model-mapping-components) dat de gegevensstructuur van het bedrijfsdomein voor facturering vertegenwoordigt.
    - **Factuurmodeltoewijzing**: deze configuratie bevat het ER-onderdeel [Modeltoewijzing](general-electronic-reporting.md#data-model-and-model-mapping-components) dat aangeeft hoe het gegevensmodel tijdens runtime wordt ingevuld met toepassingsgegevens.
    - **Vrije-tekstfactuur (Excel)**: deze configuratie bevat de ER-onderdelen [Indeling](general-electronic-reporting.md#FormatComponentOutbound) en Indelingstoewijzing. Het indelingsonderdeel specificeert de rapportlay-out op basis van een sjabloon in Excel-indeling. Het onderdeel voor indelingstoewijzing bevat de modelgegevensbron en geeft aan hoe deze gegevensbron wordt gebruikt om de rapportindeling tijdens de uitvoering in te vullen.

![Geïmporteerde ER-configuraties op de pagina Configuratie.](./media/er-embed-images-header-footer-excel-reports-imported-solution.png)

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a><a id="PrintInvoice1"></a>Een vrije-tekstfactuur afdrukken met de standaard ER-indeling

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement1"></a>Afdrukbeheer instellen

1. Ga naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**.
2. Selecteer op de pagina **Vrije-tekstfactuur** de factuur **FTI-00000002** en selecteer vervolgens **Afdrukbeheer** in de groep **Afdrukbeheer** in het actievenster op het tabblad **Factuur**.
3. Vouw op de pagina **Afdrukbeheerinstellingen**, in de structuur aan de linkerkant, **Module - klanten \> Documenten \> Vrije-tekstfactuur** uit en selecteer vervolgens het item **Oorspronkelijk \<Default\>**.
4. Selecteer **Vrije-tekstfactuur (Excel)** in het veld **Rapportindeling**.
5. Selecteer de **Esc**-toets om de pagina **Afdrukbeheerinstellingen** te verlaten en terug te gaan naar de pagina **Vrije-tekstfactuur**.

![Afdrukbeheerinstellingen voor een vrije-tekstfactuur in de standaard ER-indeling op de pagina Afdrukbeheerinstellingen.](./media/er-embed-images-header-footer-excel-reports-print-management.png)

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice1"></a>Een vrije-tekstfactuur afdrukken

1. Controleer op de pagina **Vrije-tekstfactuur** of de factuur **FTI-00000002** nog steeds is geselecteerd en selecteer vervolgens **Afdrukken** \> **Geselecteerd** op het tabblad **Factuur** in de groep **Document** in het actievenster.
2. Download de gegenereerde factuur in de Excel-indeling en open deze voor voorbeeldweergave.
3. In overeenstemming met de structuur van de Excel-sjabloon voor de geleverde ER-indeling, bevat de paginavoettekst van de gegenereerde factuur informatie over het huidige paginanummer en het totale aantal pagina's in het rapport.

![Gegenereerde vrije-tekstfactuur.](./media/er-embed-images-header-footer-excel-reports-print-invoice1.gif)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a>De standaard-ER-indeling aanpassen

In het voorbeeld in deze sectie kunt u de ER-configuraties die door Microsoft worden geleverd, gebruiken om een vrije-tekstfactuur in Excel-indeling te genereren. U moet echter een aanpassing toevoegen om een afbeelding van een bedrijfslogo in de voettekst van gegenereerde facturen te plaatsen.

In dit geval moet u als vertegenwoordiger van Litware, Inc. een nieuwe ER-indelingsconfiguratie maken (afleiden) die is gebaseerd op de door Microsoft geleverde configuratie **Vrije-tekstfactuur (Excel)**.

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a>Een aangepaste indeling maken

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster de optie **Factuurmodel** uit en selecteer vervolgens **Vrije-tekstfactuur (Excel)**. Litware, Inc. gebruikt de geïmporteerde versie (bijvoorbeeld **240.112**) van deze ER-indelingsconfiguratie als basis voor de aangepaste versie.
3. Klik op **Configuratie maken** om het dialoogvenster met de vervolgkeuzelijst te openen. Gebruik dit dialoogvenster om een nieuwe configuratie voor een aangepaste betalingsindeling te maken.
4. Selecteer in de veldgroep **Nieuw** de optie **Afleiden van naam: Vrije-tekstfactuur (Excel), Microsoft**.
5. Voer in het veld **Naam** de tekst **Vrije-tekstfactuur (Excel) aangepast** in.
6. Selecteer **Configuratie maken**.

![Een configuratie maken voor een aangepaste betalingsindeling in het vervolgkeuzemenu Configuratie maken.](./media/er-embed-images-header-footer-excel-reports-add-derived-format.png)

Versie 240.112.1 van de ER-indelingsconfiguratie **Vrije-tekstfactuur (Excel) aangepast** wordt gemaakt. Deze versie heeft de [status](general-electronic-reporting.md#component-versioning) **Concept** en kan worden bewerkt. De huidige inhoud van uw aangepaste ER-indeling komt overeen met de inhoud van de indeling die wordt geleverd door Microsoft.

![Nieuwe versie van de ER-indelingsconfiguratie die is gemaakt op de pagina Configuraties.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration1.png)

### <a name="edit-the-custom-format"></a><a id="ConfigureDerivedFormat"></a>De aangepaste indeling bewerken

Configureer uw aangepaste indeling zodat op elke pagina van het rapport een bedrijfslogo in de voettekst wordt geplaatst.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Vouw op de pagina **Configuraties** in de configuratiestructuur in het linkerdeelvenster de optie **Betalingsmodel** uit en selecteer vervolgens **Vrije-tekstfactuur (Excel) aangepast**.
3. Selecteer op het sneltabblad **Versies** de versie **240.112.1** van de geselecteerde configuratie.
4. Selecteer **Ontwerper**.
5. Selecteer op de pagina **Indelingsontwerper** de optie **Details weergeven** om meer informatie over de indelingselementen weer te geven.
6. Vouw de volgende elementen uit en bekijk ze:

    - Het element **Vrije-tekstfactuur** van het type **Excel**. Dit element wordt gebruikt om een factuur te genereren in Excel-werkmapindeling.
    - Het element **Vrije-tekstfactuur \\ Factuur** van het type **Werkblad**. Dit element wordt gebruikt om een werkblad van de gegenereerde Excel-werkmap te genereren.
    - Het element **Vrije-tekstfactuur \\ Factuur \\ Voettekst** van het type **Voettekst**. Dit element wordt gebruikt om een voettekst van een factuur in te vullen.

7. Selecteer het element **Vrije-tekstfactuur \\ Factuur \\ Voettekst**.

    ![Voettekstelement in de ER Operations-ontwerper.](./media/er-embed-images-header-footer-excel-reports-derived-format0.png)

    > [!NOTE]
    > Elke paginavoettekst van een gegenereerde factuur bevat informatie over het huidige paginanummer en het totale aantal pagina's in het rapport. Zoals u kunt zien, bevat het element **Vrije-tekstfactuur \\ Factuur \\ Voettekst** geen onderliggende elementen. Daarom wordt de Excel-sjabloon die wordt gebruikt zodanig geconfigureerd dat er paginadetails worden weergegeven in het midden van de voettekst van elk rapport.

8. Selecteer **Toevoegen** en selecteer vervolgens het type **Excel \\ Afbeelding** van het indelingselement dat u wilt toevoegen:

    1. Selecteer **Rechts** in het veld **Uitlijning**.
    2. Selecteer **Relatief** in het veld **Hoogte schalen**.
    3. Voer **70** in het veld **Percentage schalen** in.
    4. Selecteer **OK**.

        > [!NOTE]
        > Het element **Excel \\ Afbeelding** wordt gebruikt om een afbeelding van het bedrijfslogo toe te voegen en deze rechts van de paginavoettekst uit te lijnen.

    ![Eigenschappen van het element Afbeelding in het dialoogvenster Onderdeeleigenschappen.](./media/er-embed-images-header-footer-excel-reports-derived-format1.png)

9. Selecteer in de indelingsstructuur aan de linkerkant het element **Afbeelding** dat u zojuist hebt toegevoegd en vouw vervolgens op het tabblad **Toewijzing** de gegevensbron **model** uit.
10. Vouw **model.Payment** \> **model. InvoiceBase \> model.InvoiceBase.CompanyInfo** uit en selecteer vervolgens het gegevensbronveld **model.InvoiceBase.CompanyInfo.Logo**. Het gegevensbronveld van het type [Container](er-formula-supported-data-types-composite.md#container) stelt de afbeelding van het bedrijfslogo beschikbaar als media-inhoud.
11. Selecteer **Binden**. Het indelingselement **Afbeelding** is nu gebonden aan het gegevensbronveld **model.InvoiceBase.CompanyInfo.Logo**. Daarom wordt tijdens runtime een afbeelding van het bedrijfslogo in de voettekst van gegenereerde facturen geplaatst.

    ![Het indelingselement Afbeelding is nu gebonden aan het gegevensbronveld model.InvoiceBase.CompanyInfo.Logo in de ER Operations-ontwerper.](./media/er-embed-images-header-footer-excel-reports-derived-format2.png)

12. Selecteer **Opslaan** en sluit de pagina **Ontwerper**.

### <a name="mark-the-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a>De aangepaste indeling markeren als uitvoerbaar

Aangezien de eerste versie van de aangepaste indeling is gemaakt en deze de status **Concept** heeft, kunt u de indeling uitvoeren voor testdoeleinden. Om het rapport uit te voeren, verwerkt u een leveranciersbetaling met behulp van de betalingsmethode die verwijst naar door u aangepaste ER-indeling. Wanneer u een ER-indeling aanroept vanuit de toepassing, worden standaard alleen de versies met de status **Voltooid** en **Gedeeld** [meegenomen](general-electronic-reporting.md#component-versioning). Dit gedrag voorkomt dat ER-indelingsprofielen met niet-voltooide ontwerpen worden gebruikt. Voor het testen kunt u de toepassing dwingen de versie van de ER-indeling te gebruiken met de status **Concept**. Op deze manier kunt u de versie van de huidige indelingsversie aanpassen als er wijzigingen nodig zijn. Meer informatie over dit onderwerp vindt u in [Toepasbaarheid](electronic-reporting-destinations.md#applicability).

Als u de conceptversie van een ER-indeling wilt gebruiken, moet u de ER-indeling expliciet markeren.

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in het actievenster op het tabblad **Configuraties** in de groep **Geavanceerde instellingen** de optie **Gebruikersparameters**.
3. Stel in het dialoogvenster **Gebruikersparameters** de optie **Uitvoeringsinstellingen** in op **Ja** en selecteer **OK**.
4. Selecteer **Bewerken** om de huidige pagina bewerkbaar te maken en selecteer vervolgens in de configuratiestructuur in het linkerdeelvenster de optie **Vrije-tekstfactuur (Excel) aangepast**.
5. Stel de optie **Concept uitvoeren** in op **Ja**.

![De aangepaste opmaak markeren als uitgevoerd op de pagina Configuraties.](./media/er-embed-images-header-footer-excel-reports-derived-format-configuration2.png)

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a><a id="PrintInvoice2"></a>Een vrije-tekstfactuur afdrukken met de aangepaste ER-indeling

### <a name="set-up-print-management"></a><a id="ConfigurePrintManagement2"></a>Afdrukbeheer instellen

1. Ga naar **Klanten** \> **Facturen** \> **Alle vrije-tekstfacturen**.
2. Selecteer op de pagina **Vrije-tekstfactuur** de factuur **FTI-00000002** en selecteer vervolgens **Afdrukbeheer** in de groep **Afdrukbeheer** in het actievenster op het tabblad **Factuur**.
3. Vouw op de pagina **Afdrukbeheerinstellingen**, in de structuur aan de linkerkant, **Module - klanten** \> **Documenten** \> **Vrije-tekstfactuur** uit en selecteer vervolgens het item **Oorspronkelijk** **\<Default\>**.
4. Selecteer **Vrije-tekstfactuur (Excel) aangepast** in het veld **Rapportindeling**.
5. Selecteer **Esc** om de pagina **Afdrukbeheerinstellingen** te verlaten en terug te gaan naar de pagina **Vrije-tekstfactuur**.

### <a name="print-a-free-text-invoice"></a><a id="ProcessInvoice2"></a>Een vrije-tekstfactuur afdrukken

1. Controleer op de pagina **Vrije-tekstfactuur** of de factuur **FTI-00000002** nog steeds is geselecteerd en selecteer vervolgens **Afdrukken** \> **Geselecteerd** op het tabblad **Factuur** in de groep **Document** in het actievenster.
2. Download de gegenereerde factuur in de Excel-indeling en open deze voor voorbeeldweergave.
3. In overeenstemming met de structuur van de aangepaste ER-indeling, bevat de paginavoettekst van de gegenereerde factuur een afbeelding van het bedrijfslogo en informatie over de paginering van het rapport.

![Gegenereerde vrije-tekstfactuur met een afbeelding van het bedrijfslogo in de paginavoettekst.](./media/er-embed-images-header-footer-excel-reports-print-invoice2.gif)

## <a name="additional-resources"></a><a id="References"></a>Aanvullende bronnen

- [Een configuratie ontwerpen voor het genereren van documenten in Excel-indeling](er-fillable-excel.md)
- [Afbeeldingen en vormen insluiten in documenten die u genereert met ER](electronic-reporting-embed-images-shapes.md)
