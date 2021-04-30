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
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="01ab4-103">Bestemming voor printers</span><span class="sxs-lookup"><span data-stu-id="01ab4-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01ab4-104">U kunt een gegenereerd document rechtstreeks naar een netwerkprinter sturen om direct af te drukken.</span><span class="sxs-lookup"><span data-stu-id="01ab4-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="01ab4-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="01ab4-105">Prerequisites</span></span>

<span data-ttu-id="01ab4-106">Voordat u begint, moet u de documentrouteringsagent installeren en configureren en vervolgens de netwerkprinters registreren.</span><span class="sxs-lookup"><span data-stu-id="01ab4-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="01ab4-107">Zie voor meer informatie [De documentrouteringsagent installeren om afdrukken via het netwerk in te schakelen](./install-document-routing-agent.md).</span><span class="sxs-lookup"><span data-stu-id="01ab4-107">For more information, see [Install the Document Routing Agent to enable network printing](./install-document-routing-agent.md).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="01ab4-108">De printerbestemming beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="01ab4-108">Make the Printer destination available</span></span>

<span data-ttu-id="01ab4-109">Als u de bestemming **Printer** beschikbaar wilt maken in de huidige instantie van Microsoft Dynamics 365 Finance, gaat u naar het werkgebied **Functiebeheer** en schakelt u de volgende functies in deze volgorde in:</span><span class="sxs-lookup"><span data-stu-id="01ab4-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="01ab4-110">Voor elektronische rapportage uitgaande documenten met Microsoft Office-indelingen converteren naar PDF.</span><span class="sxs-lookup"><span data-stu-id="01ab4-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="01ab4-111">Documentrouteringsagent als bestemming voor elektronische rapportage voor uitgaande documenten</span><span class="sxs-lookup"><span data-stu-id="01ab4-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="01ab4-112">[![De bestemmingsfunctie ER-printer in Functiebeheer inschakelen](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="01ab4-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="01ab4-113">Toepasbaarheid</span><span class="sxs-lookup"><span data-stu-id="01ab4-113">Applicability</span></span>

<span data-ttu-id="01ab4-114">De bestemming **Printer** kan alleen worden geconfigureerd voor bestandsonderdelen die worden gebruikt voor het genereren van uitvoer in afdrukbare PDF-indeling (PDF Merger of PDF-bestandsindelingselementen) of Microsoft Office Excel/Word-indeling (Excel-bestand).</span><span class="sxs-lookup"><span data-stu-id="01ab4-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="01ab4-115">Wanneer de uitvoer wordt gegenereerd in PDF-indeling, wordt deze naar een printer verzonden.</span><span class="sxs-lookup"><span data-stu-id="01ab4-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="01ab4-116">Wanneer de uitvoer in Microsoft Office-indeling wordt gegenereerd, wordt deze automatisch geconverteerd naar de PDF-indeling en vervolgens naar een printer verzonden.</span><span class="sxs-lookup"><span data-stu-id="01ab4-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="01ab4-117">Beperkingen</span><span class="sxs-lookup"><span data-stu-id="01ab4-117">Limitations</span></span>

<span data-ttu-id="01ab4-118">De bestemming **Printer** is alleen geïmplementeerd voor cloudimplementaties.</span><span class="sxs-lookup"><span data-stu-id="01ab4-118">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="01ab4-119">De printerbestemming gebruiken</span><span class="sxs-lookup"><span data-stu-id="01ab4-119">Use the Printer destination</span></span>

1. <span data-ttu-id="01ab4-120">Stel de optie **ingeschakeld** in op **Ja** als u een gegenereerd document naar een printer wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="01ab4-120">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="01ab4-121">Selecteer in het veld **Printernaam** de gewenste netwerkprinter.</span><span class="sxs-lookup"><span data-stu-id="01ab4-121">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="01ab4-122">Stel de optie **Opslaan in afdrukarchief?** in op **Ja** om de gegenereerde uitvoer in het afdrukarchief op te slaan, zodat deze beschikbaar is voor verder afdrukken.</span><span class="sxs-lookup"><span data-stu-id="01ab4-122">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="01ab4-123">Als u de gearchiveerde uitvoer later wilt openen, gaat u naar **Organisatiebeheer** \> **Query's en rapporten** \> **Rapportarchief**.</span><span class="sxs-lookup"><span data-stu-id="01ab4-123">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="01ab4-124">[![De printerbestemming gebruiken](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="01ab4-124">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="01ab4-125">De optie **Converteren naar PDF** hoeft niet ingeschakeld te zijn wanneer u de bestemming **Printer** configureert.</span><span class="sxs-lookup"><span data-stu-id="01ab4-125">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="01ab4-126">De PDF-conversie wordt voor afdrukdoeleinden uitgevoerd, zelfs als de optie is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="01ab4-126">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="01ab4-127">Als u een bepaalde [afdrukstand](electronic-reporting-destinations.md#SelectPdfPageOrientation) wilt gebruiken wanneer u een uitgaand document afdrukt in Excel-indeling, moet u de optie **Converteren naar PDF** inschakelen.</span><span class="sxs-lookup"><span data-stu-id="01ab4-127">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="01ab4-128">Wanneer u de optie **Converteren naar PDF** instelt op **Ja**, wordt het veld **Afdrukstand** beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="01ab4-128">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="01ab4-129">Selecteer een afdrukstand in het veld **Afdrukstand**.</span><span class="sxs-lookup"><span data-stu-id="01ab4-129">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="01ab4-130">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="01ab4-130">Additional resources</span></span>

- [<span data-ttu-id="01ab4-131">Overzicht van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="01ab4-131">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="01ab4-132">Bestemmingen van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="01ab4-132">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]