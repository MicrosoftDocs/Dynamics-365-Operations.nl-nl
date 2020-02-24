---
title: ER-bestemmingstype voor printer
description: Dit onderwerp bevat informatie over het configureren van een printerbestemming voor elke MAP- of BESTAND-component van een ER-indeling (elektronische rapportage) die wordt geconfigureerd voor het genereren van uitgaande documenten in PDF- of Microsoft Office-indeling (Excel\Word).
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019707"
---
# <a name="PrinterDestinationType"></a>Printerbestemming

[!include [banner](../includes/banner.md)]

U kunt een gegenereerd document rechtstreeks naar een netwerkprinter sturen om direct af te drukken.

## <a name="prerequisites"></a>Vereisten

Voordat u begint, moet u de documentrouteringsagent installeren en configureren en vervolgens de netwerkprinters registreren. Zie voor meer informatie [De documentrouteringsagent installeren om afdrukken via het netwerk in te schakelen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).

## <a name="make-the-printer-destination-available"></a>De printerbestemming beschikbaar maken

Als u de bestemming **Printer** beschikbaar wilt maken in de huidige instantie van Microsoft Dynamics 365 Finance, gaat u naar het werkgebied **Functiebeheer** en schakelt u de volgende functies in deze volgorde in:

1. Voor elektronische rapportage uitgaande documenten met Microsoft Office-indelingen converteren naar PDF.
2. Documentrouteringsagent als bestemming voor elektronische rapportage voor uitgaande documenten

[![De bestemmingsfunctie ER-printer in Functiebeheer inschakelen](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)

### <a name="applicability"></a>Toepasbaarheid

De bestemming **Printer** kan alleen worden geconfigureerd voor bestandsonderdelen die worden gebruikt voor het genereren van uitvoer in afdrukbare PDF-indeling (PDF Merger of PDF-bestandsindelingselementen) of Microsoft Office Excel/Word-indeling (Excel-bestand). Wanneer de uitvoer wordt gegenereerd in PDF-indeling, wordt deze naar een printer verzonden. Wanneer de uitvoer in Microsoft Office-indeling wordt gegenereerd, wordt deze automatisch geconverteerd naar de PDF-indeling en vervolgens naar een printer verzonden.

### <a name="limitations"></a>Beperkingen

Deze functie is een voorbeeldfunctie en is onderworpen aan de gebruiksvoorwaarden die worden beschreven in [aanvullende gebruiksvoorwaarden voor Microsoft Dynamics 365-voorbeelden](https://go.microsoft.com/fwlink/?linkid=2105274).

De bestemming **Printer** is alleen geïmplementeerd voor cloudimplementaties.

### <a name="use-the-printer-destination"></a>De printerbestemming gebruiken

1. Stel de optie **ingeschakeld** in op **Ja** als u een gegenereerd document naar een printer wilt verzenden.
2. Selecteer in het veld **Printernaam** de gewenste netwerkprinter.
3. Stel de optie **Opslaan in afdrukarchief?** in op **Ja** om de gegenereerde uitvoer in het afdrukarchief op te slaan, zodat deze beschikbaar is voor verder afdrukken. Als u de gearchiveerde uitvoer later wilt openen, gaat u naar **Organisatiebeheer** \> **Query's en rapporten** \> **Rapportarchief**.

[![De printerbestemming gebruiken](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)

> [!NOTE]
> De optie **Converteren naar PDF** hoeft niet ingeschakeld te zijn wanneer u de bestemming **Printer** configureert. De PDF-conversie wordt voor afdrukdoeleinden uitgevoerd, zelfs als de optie is uitgeschakeld.

## <a name="additional-resources"></a>Aanvullende resources

- [Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)
- [Bestemmingen van elektronische rapportage (ER)](electronic-reporting-destinations.md)
