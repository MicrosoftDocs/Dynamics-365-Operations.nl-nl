---
title: ER-bestemmingstype voor printer
description: In dit onderwerp wordt uitgelegd hoe u een printerbestemming kunt configureren voor elke MAP- of BESTAND-component van een ER-indeling (Electronic Reporting).
author: NickSelin
ms.date: 02/24/2021
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
ms.openlocfilehash: 7749a458020de664d00e81ccf0e480ae459da617
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893999"
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

[![De bestemmingsfunctie ER-printer in Functiebeheer inschakelen](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Toepasbaarheid

De bestemming **Printer** kan alleen worden geconfigureerd voor bestandsonderdelen die worden gebruikt voor het genereren van uitvoer in afdrukbare PDF-indeling (PDF Merger of PDF-bestandsindelingselementen) of Microsoft Office Excel/Word-indeling (Excel-bestand). Wanneer de uitvoer wordt gegenereerd in PDF-indeling, wordt deze naar een printer verzonden. Wanneer de uitvoer in Microsoft Office-indeling wordt gegenereerd, wordt deze automatisch geconverteerd naar de PDF-indeling en vervolgens naar een printer verzonden.

### <a name="limitations"></a>Beperkingen

De bestemming **Printer** is alleen geïmplementeerd voor cloudimplementaties.

### <a name="use-the-printer-destination"></a>De printerbestemming gebruiken

1. Stel de optie **ingeschakeld** in op **Ja** als u een gegenereerd document naar een printer wilt verzenden.
2. Selecteer in het veld **Printernaam** de gewenste netwerkprinter.
3. Stel de optie **Opslaan in afdrukarchief?** in op **Ja** om de gegenereerde uitvoer in het afdrukarchief op te slaan, zodat deze beschikbaar is voor verder afdrukken. Als u de gearchiveerde uitvoer later wilt openen, gaat u naar **Organisatiebeheer** \> **Query's en rapporten** \> **Rapportarchief**.

[![De printerbestemming gebruiken](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> De optie **Converteren naar PDF** hoeft niet ingeschakeld te zijn wanneer u de bestemming **Printer** configureert. De PDF-conversie wordt voor afdrukdoeleinden uitgevoerd, zelfs als de optie is uitgeschakeld.

Als u een bepaalde [afdrukstand](electronic-reporting-destinations.md#SelectPdfPageOrientation) wilt gebruiken wanneer u een uitgaand document afdrukt in Excel-indeling, moet u de optie **Converteren naar PDF** inschakelen. Wanneer u de optie **Converteren naar PDF** instelt op **Ja**, wordt het veld **Afdrukstand** beschikbaar. Selecteer een afdrukstand in het veld **Afdrukstand**.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)
- [Bestemmingen van elektronische rapportage (ER)](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]