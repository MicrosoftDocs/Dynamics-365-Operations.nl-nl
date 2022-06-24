---
title: ER-bestemmingstype voor printer
description: In dit artikel wordt uitgelegd hoe u een printerbestemming kunt configureren voor elke MAP- of BESTAND-component van een ER-indeling (Electronic Reporting).
author: NickSelin
ms.date: 02/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 826455d0901a45ef26755fd323ee2a2737b5eec0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845565"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a>Bestemming voor printers

[!include [banner](../includes/banner.md)]

U kunt een gegenereerd document rechtstreeks naar een netwerkprinter sturen om direct af te drukken.

## <a name="prerequisites"></a>Vereisten

Voordat u begint, moet u de documentrouteringsagent installeren en configureren en vervolgens de netwerkprinters registreren. Zie voor meer informatie [De documentrouteringsagent installeren om afdrukken via het netwerk in te schakelen](./install-document-routing-agent.md).

## <a name="make-the-printer-destination-available"></a>De printerbestemming beschikbaar maken

Als u de bestemming **Printer** beschikbaar wilt maken in de huidige instantie van Microsoft Dynamics 365 Finance, gaat u naar het werkgebied **Functiebeheer** en schakelt u de volgende functies in deze volgorde in:

1. Voor elektronische rapportage uitgaande documenten met Microsoft Office-indelingen converteren naar PDF.
2. Documentrouteringsagent als bestemming voor elektronische rapportage voor uitgaande documenten

[![De bestemmingsfunctie ER-printer in Functiebeheer inschakelen.](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Toepasbaarheid

#### <a name="pdf-printing"></a>PDF afdrukken

In Finance-versie van vóór versie 10.0.18 kan de bestemming **Printer** kan alleen worden geconfigureerd voor bestandsonderdelen die worden gebruikt voor het genereren van uitvoer in afdrukbare PDF-indeling (**PDF Merger** of **PDF-bestandsindelingselementen**) of Microsoft Office Excel- en Word-indeling (**Excel-bestandsindelingselement**). Wanneer de uitvoer wordt gegenereerd in PDF-indeling, wordt deze naar een printer verzonden. Wanneer de uitvoer in Office-indeling wordt gegenereerd met het **Excel-bestandsindelingselement**, wordt deze automatisch geconverteerd naar de PDF-indeling en vervolgens naar een printer verzonden.

Vanaf versie 10.0.18 kunt u echter de **printerbestemming** configureren voor het indelingselement **Algemeen bestand**. Dit indelingselement wordt meestal gebruikt om uitvoer te genereren in TXT- of XML-indeling. U kunt een ER-indeling met het element **Algemene bestandsindeling** configureren als het element voor de hoofdindeling en het indelingselement **Binaire inhoud** als het enige geneste element er onder. In dit geval produceert het element **Algemene bestandsindeling** uitvoer in de indeling die is opgegeven door de binding die u configureert voor het element voor de **binaire inhoudsindeling**. U kunt deze binding bijvoorbeeld configureren om dit element [in te vullen](tasks/er-document-management-files-5.md#modify-the-format-to-populate-attachments-into-generating-messages-in-binary-format) met de inhoud van een [documentbeheerbijlage](../../fin-ops/organization-administration/configure-document-management.md) in PDF- of Office-indeling (Excel of Word). U kunt de uitvoer afdrukken met de geconfigureerde **printerbestemming**. 

> [!NOTE]
> Als u het indelingselement **Common\\File** selecteert om de **printerbestemming** te configureren, kunt u er op het moment van het ontwerp niet voor zorgen dat het geselecteerde element uitvoer zal produceren in PDF-indeling of uitvoer die kan worden geconverteerd naar PDF-indeling. Daarom ontvangt u het volgende waarschuwingsbericht: "Zorg ervoor dat de uitvoer die door het geselecteerde indelingsonderdeel wordt gegenereerd, kan worden geconverteerd naar PDF. Als u dit niet doet, moet u de optie 'Converteren naar PDF' niet selecteren.' U moet stappen ondernemen om runtimeproblemen te voorkomen wanneer uitvoer die niet in PDF's of niet-PDF-converteerbaar is, wordt geleverd voor afdrukken tijdens runtime. Als u uitvoer verwacht in de indeling Office (Excel of Word), moet u de optie **Converteren naar PDF** selecteren.
>
> Als u in versie 10.0.26 of hoger de optie **Converteren naar PDF** wilt gebruiken, moet u **PDF** selecteren voor de parameter **Documentrouteringstype** van de geconfigureerde **printerbestemming**.

#### <a name="zpl-printing"></a>ZPL afdrukken

In versie 10.0.26 en hoger kunt u de **printerbestemming** configureren voor het indelingselement **Common\\File** door **ZPL** te selecteren voor de parameter **Documentrouteringstype**. In dit geval wordt de optie **Converteren naar PDF** genegeerd tijdens runtime en wordt de TXT- of XML-uitvoer rechtstreeks naar een geselecteerde printer verzonden met behulp van het ZPL-contract (Xml Programming Language) van de [documentrouteringsagent (XML)](install-document-routing-agent.md). Gebruik deze functie voor een ER-indeling die een ZPL II-labelindeling vertegenwoordigt om verschillende etiketten af te drukken.

[![De parameter documentrouteringstype instellen in het dialoogvenster Doelinstellingen.](./media/ER_Destinations-SetDocumentRoutingType.png)](./media/ER_Destinations-SetDocumentRoutingType.png)

Zie [Een nieuwe ER-oplossing ontwerpen om ZPL-labels af te drukken](er-design-zpl-labels.md) voor meer informatie over deze functie .

### <a name="limitations"></a>Beperkingen

De bestemming **Printer** is alleen geïmplementeerd voor cloudimplementaties.

### <a name="use-the-printer-destination"></a>De printerbestemming gebruiken

1. Stel de optie **ingeschakeld** in op **Ja** als u een gegenereerd document naar een printer wilt verzenden.
2. Selecteer in het veld **Printernaam** de gewenste netwerkprinter.
3. Stel de optie **Opslaan in afdrukarchief?** in op **Ja** om de gegenereerde uitvoer in het afdrukarchief op te slaan, zodat deze beschikbaar is voor verder afdrukken. Als u de gearchiveerde uitvoer later wilt openen, gaat u naar **Organisatiebeheer** \> **Query's en rapporten** \> **Rapportarchief**.

[![De printerbestemming gebruiken.](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> De optie **Converteren naar PDF** hoeft niet ingeschakeld te zijn wanneer u de bestemming **Printer** configureert. De PDF-conversie wordt voor afdrukdoeleinden uitgevoerd, zelfs als de optie is uitgeschakeld.

Als u een bepaalde [afdrukstand](electronic-reporting-destinations.md#SelectPdfPageOrientation) wilt gebruiken wanneer u een uitgaand document afdrukt in Excel-indeling, moet u de optie **Converteren naar PDF** inschakelen. Wanneer u de optie **Converteren naar PDF** instelt op **Ja**, wordt het veld **Afdrukstand** beschikbaar. Selecteer een afdrukstand in het veld **Afdrukstand**.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)
- [Bestemmingen van elektronische rapportage (ER)](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
