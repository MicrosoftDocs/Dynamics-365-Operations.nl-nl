---
title: Een ER-indeling ontwerpen om rijen bij elkaar te houden op dezelfde Excel-pagina
description: In dit onderwerp wordt uitgelegd hoe u een ER-indeling (elektronische rapportage) ontwerpt waarbij de rijen op dezelfde Microsoft Excel-pagina worden gehouden.
author: NickSelin
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-03-01
ms.dyn365.ops.version: Version 10.0.26
ms.openlocfilehash: 711681ab38fb24b57a83f008f86a8261176aa5a5
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388585"
---
# <a name="design-an-er-format-to-keep-rows-together-on-the-same-excel-page"></a>Een ER-indeling ontwerpen om rijen bij elkaar te houden op dezelfde Excel-pagina

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

In dit onderwerp wordt uitgelegd hoe een gebruiker in de rol Systeembeheerder of Functioneel consultant een [ER](general-electronic-reporting.md)-[indeling](er-overview-components.md#format-component) (Electronic Reporting) kan configureren om uitgaande documenten te genereren in Microsoft Excel en paginering van documenten te beheren zodat de rijen op dezelfde pagina blijven.

In dit voorbeeld wijzigt u de door Microsoft geleverde ER-indeling die wordt gebruikt om vrije-tekstfacturen af te drukken in Excel. Met de wijzigingen kunt u de paginanummering van een gegenereerd vrije-tekstfactuurrapport beheren, zodat alle rijen van één factuurregel waar mogelijk op dezelfde pagina blijven staan.

De procedures in dit onderwerp kunnen in het bedrijf **USMF** worden uitgevoerd. U hoeft hiervoor geen code te schrijven.

In dit voorbeeld maakt u de vereiste ER-[configuraties](general-electronic-reporting.md#Configuration) voor het voorbeeldbedrijf, **Litware, Inc.**. Controleer of de configuratieprovider voor het voorbeeldbedrijf **Litware, Inc.** (`http://www.litware.com`) wordt vermeld voor het ER-raamwerk en of het is gemarkeerd is als **Actief**. Als deze configuratieprovider niet wordt vermeld of als deze niet is gemarkeerd als **Actief**, volgt u de stappen in het onderwerp [Een configuratieprovider maken en als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="enter-a-new-free-text-invoice"></a>Een nieuwe vrije-tekstfactuur invoeren

1. Volg de stappen in [Een vrije-tekstfactuur maken](../../../finance/accounts-receivable/create-free-text-invoice-new.md#create-a-free-text-invoice-1) om een vrije-tekstfactuur toe te voegen.

    1. Voeg één regel toe aan de factuur.
    2. Voeg vijf notities toe voor de factuurregel.

    ![De factuurregelnotities controleren op de pagina Bijlagen.](./media/er-keep-excel-rows-together-notes.png)

2. Volg de stappen in [Regels kopiëren](../../../finance/accounts-receivable/create-free-text-invoice-new.md#copy-lines) om vijf extra factuurregels te maken die de factuurregel kopiëren die u in de vorige stap hebt toegevoegd.

    ![De vrije-tekstfactuurregels controleren op de pagina Vrije-tekstfactuur.](./media/er-keep-excel-rows-together-invoice.png)

## <a name="configure-the-er-framework"></a>Het ER-raamwerk configureren

Voer de stappen in [Het ER-raamwerk configureren](er-quick-start2-customize-report.md#ConfigureFramework) uit om de minimale set ER-parameters in te stellen. U moet deze instellingen voltooien voordat u het ER-framework gaat gebruiken om een aangepaste versie van een standaard ER-indeling te ontwerpen.

## <a name="import-the-standard-er-format-configuration"></a>Standaardconfiguratie voor ER-indeling importeren

Volg de stappen in [Standaardconfiguratie voor ER-indeling importeren](er-quick-start2-customize-report.md#ImportERSolution1) om de standaard ER-configuraties toe te voegen aan de actuele instantie van Dynamics 365 Finance. Importeer bijvoorbeeld versie **252.116** van de indelingsconfiguratie voor **Vrije-tekstfactuur (Excel)**. Basisversie **252** van de basisconfiguratie **Factuurmodel** wordt automatisch uit de opslagplaats geïmporteerd samen met de vereiste configuratie voor **Factuurmodeltoewijzing**.

## <a name="set-up-print-management-to-use-the-standard-er-format"></a>Afdrukbeheer instellen om de standaard ER-indeling te gebruiken

Volg de stappen in [Afdrukbeheer instellen](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement1) om afdrukbeheer te configureren voor de module **Klanten**, zodat de standaard ER-indeling wordt gebruikt voor het afdrukken van vrije-tekstfacturen.

## <a name="configure-a-format-destination-for-the-standard-er-format"></a>Een indelingsbestemming configureren voor de standaard ER-indeling

Volg de stappen in [Een indelingsbestemming voor een schermvoorbeeld configureren](er-quick-start1-new-solution.md#ConfigureDestination) om de ER-bestemming [Scherm](er-destination-type-screen.md) van de standaard ER-indeling te configureren, zodat gegenereerde rapporten worden geconverteerd naar de standaard ER-indeling en als voorbeeld worden weergegeven op een nieuwe browsertabblad.

## <a name="print-a-free-text-invoice-by-using-the-standard-er-format"></a>Een vrije-tekstfactuur afdrukken met de standaard ER-indeling

1. Volg de stappen in [Een vrije-tekstfactuur afdrukken](er-embed-images-header-footer-excel-reports.md#ProcessInvoice1) om de standaard ER-indeling te gebruiken voor het genereren van een vrije-tekstfactuurrapport in Excel-indeling voor de toegevoegde factuur.
2. Download de gegenereerde Excel-werkmap en bekijk deze in de Excel-bureaubladtoepassing.

    De zesde regel van de factuur begint op de eerste pagina van het rapport en wordt op de tweede pagina voortgezet. De laatste notitie verschijnt op de tweede pagina en is niet onderdeel van de zesde factuurregel. Daarom maakt de paginaovergang in het midden van de inhoud voor de factuurregel dit document moeilijk te lezen.

    ![De paginering controleren van de gegenereerde vrije-tekstfactuur in de Excel-bureaubladtoepassing.](./media/er-keep-excel-rows-together-invoice1.gif)

De resterende procedures in dit onderwerp geven aan hoe u de standaard ER-indeling kunt afstemmen om de weergave en leesbaarheid van het factuurrapport te verbeteren door alle inhoud voor één factuurregel op dezelfde pagina te houden.

## <a name="create-a-custom-format"></a>Een aangepaste indeling maken

Volg de stappen in [Een aangepaste indeling maken](er-embed-images-header-footer-excel-reports.md#DeriveProvidedFormat) om een indeling af te leiden van de geïmporteerde ER-indeling en een aangepaste ER-configuratie **Vrije-tekstfactuur (Excel)** te maken die beschikbaar is voor bewerken en wijzigen.

## <a name="edit-the-custom-format"></a>De aangepaste indeling bewerken

1. Volg de stappen in [Een aangepaste indeling maken](er-embed-images-header-footer-excel-reports.md#ConfigureDerivedFormat) om de afgeleide ER-indeling te openen voor bewerking in de ER-indelingsontwerper.
2. Vouw op de pagina **Indelingsontwerper**, in de opmaakstructuur in het linkervenster **Vrije-tekstfactuur \> Werkblad \> InvoiceLines** uit en selecteer het onderdeel **InvoiceLines_Values**.
3. Stel op het tabblad **Indeling** de optie **Regels bij elkaar houden** in op **Ja**.

    ![De optie Rijen bij elkaar houden instellen voor de bewerkbare ER-indeling op de pagina Opmaakontwerper.](./media/er-keep-excel-rows-together-format.png)

4. Selecteer **Opslaan** en sluit de pagina.

## <a name="mark-the-custom-format-as-runnable"></a>De aangepaste indeling markeren als uitvoerbaar

Volg de stappen in [De aangepaste indeling markeren als uitvoerbaar](er-embed-images-header-footer-excel-reports.md#MarkFormatRunnable) om de gewijzigde versie van de aangepaste ER-indeling uitvoerbaar te maken.

## <a name="set-up-print-management-to-use-the-custom-er-format"></a>Afdrukbeheer instellen om de aangepaste ER-indeling te gebruiken

Volg de stappen in [Afdrukbeheer instellen](er-embed-images-header-footer-excel-reports.md#ConfigurePrintManagement2) om afdrukbeheer te configureren voor de module **Klanten**, zodat de aangepaste ER-indeling wordt gebruikt voor het afdrukken van vrije-tekstfacturen.

## <a name="configure-a-format-destination-for-the-custom-er-format"></a>Een indelingsbestemming configureren voor de aangepaste ER-indeling

Volg de stappen in [Een indelingsbestemming voor een schermvoorbeeld configureren](er-quick-start1-new-solution.md#ConfigureDestination) om de ER-bestemming **Scherm** van de standaard ER-indeling te configureren, zodat gegenereerde rapporten worden geconverteerd naar aangepaste ER-indeling en als voorbeeld worden weergegeven op een nieuwe browsertabblad.

## <a name="print-a-free-text-invoice-by-using-the-custom-er-format"></a>Een vrije-tekstfactuur afdrukken met de aangepaste ER-indeling

1. Volg de stappen in [Een vrije-tekstfactuur afdrukken](er-embed-images-header-footer-excel-reports.md#ProcessInvoice2) om de aangepaste ER-indeling te gebruiken voor het genereren van een vrije-tekstfactuurrapport in Excel-indeling voor de toegevoegde factuur.
2. Download de gegenereerde Excel-werkmap en bekijk deze in de Excel-bureaubladtoepassing.

    De zesde regel van de factuur begint op de tweede pagina, en alle Excel-rijen die deze factuurregel vertegenwoordigen, worden op die pagina samen weergegeven.

    ![De bijgewerkte paginering controleren van de gegenereerde vrije-tekstfactuur in de Excel-bureaubladtoepassing.](./media/er-keep-excel-rows-together-invoice2.gif)

## <a name="additional-resources"></a>Aanvullende bronnen

[Een configuratie ontwerpen voor het genereren van documenten in Excel-indeling](er-fillable-excel.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
