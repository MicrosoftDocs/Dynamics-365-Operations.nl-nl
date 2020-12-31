---
title: ER-bestemmingstype voor printer
description: Dit onderwerp bevat informatie over het configureren van een printerbestemming voor elke MAP- of BESTAND-component van een ER-indeling (elektronische rapportage) die wordt geconfigureerd voor het genereren van uitgaande documenten in PDF- of Microsoft Office-indeling (Excel\Word).
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: b7a279dcb30e7681ae654ab17d898a5364391d57
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679601"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="8fb97-103">Printerbestemming</span><span class="sxs-lookup"><span data-stu-id="8fb97-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fb97-104">U kunt een gegenereerd document rechtstreeks naar een netwerkprinter sturen om direct af te drukken.</span><span class="sxs-lookup"><span data-stu-id="8fb97-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8fb97-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="8fb97-105">Prerequisites</span></span>

<span data-ttu-id="8fb97-106">Voordat u begint, moet u de documentrouteringsagent installeren en configureren en vervolgens de netwerkprinters registreren.</span><span class="sxs-lookup"><span data-stu-id="8fb97-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="8fb97-107">Zie voor meer informatie [De documentrouteringsagent installeren om afdrukken via het netwerk in te schakelen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="8fb97-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="8fb97-108">De printerbestemming beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="8fb97-108">Make the Printer destination available</span></span>

<span data-ttu-id="8fb97-109">Als u de bestemming **Printer** beschikbaar wilt maken in de huidige instantie van Microsoft Dynamics 365 Finance, gaat u naar het werkgebied **Functiebeheer** en schakelt u de volgende functies in deze volgorde in:</span><span class="sxs-lookup"><span data-stu-id="8fb97-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="8fb97-110">Voor elektronische rapportage uitgaande documenten met Microsoft Office-indelingen converteren naar PDF.</span><span class="sxs-lookup"><span data-stu-id="8fb97-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="8fb97-111">Documentrouteringsagent als bestemming voor elektronische rapportage voor uitgaande documenten</span><span class="sxs-lookup"><span data-stu-id="8fb97-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="8fb97-112">[![De bestemmingsfunctie ER-printer in Functiebeheer inschakelen](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="8fb97-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="8fb97-113">Toepasbaarheid</span><span class="sxs-lookup"><span data-stu-id="8fb97-113">Applicability</span></span>

<span data-ttu-id="8fb97-114">De bestemming **Printer** kan alleen worden geconfigureerd voor bestandsonderdelen die worden gebruikt voor het genereren van uitvoer in afdrukbare PDF-indeling (PDF Merger of PDF-bestandsindelingselementen) of Microsoft Office Excel/Word-indeling (Excel-bestand).</span><span class="sxs-lookup"><span data-stu-id="8fb97-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="8fb97-115">Wanneer de uitvoer wordt gegenereerd in PDF-indeling, wordt deze naar een printer verzonden.</span><span class="sxs-lookup"><span data-stu-id="8fb97-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="8fb97-116">Wanneer de uitvoer in Microsoft Office-indeling wordt gegenereerd, wordt deze automatisch geconverteerd naar de PDF-indeling en vervolgens naar een printer verzonden.</span><span class="sxs-lookup"><span data-stu-id="8fb97-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="8fb97-117">Beperkingen</span><span class="sxs-lookup"><span data-stu-id="8fb97-117">Limitations</span></span>

<span data-ttu-id="8fb97-118">Deze functie is een voorbeeldfunctie en is onderworpen aan de gebruiksvoorwaarden die worden beschreven in [aanvullende gebruiksvoorwaarden voor Microsoft Dynamics 365-voorbeelden](https://go.microsoft.com/fwlink/?linkid=2105274).</span><span class="sxs-lookup"><span data-stu-id="8fb97-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="8fb97-119">De bestemming **Printer** is alleen geïmplementeerd voor cloudimplementaties.</span><span class="sxs-lookup"><span data-stu-id="8fb97-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="8fb97-120">De printerbestemming gebruiken</span><span class="sxs-lookup"><span data-stu-id="8fb97-120">Use the Printer destination</span></span>

1. <span data-ttu-id="8fb97-121">Stel de optie **ingeschakeld** in op **Ja** als u een gegenereerd document naar een printer wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="8fb97-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="8fb97-122">Selecteer in het veld **Printernaam** de gewenste netwerkprinter.</span><span class="sxs-lookup"><span data-stu-id="8fb97-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="8fb97-123">Stel de optie **Opslaan in afdrukarchief?** in op **Ja** om de gegenereerde uitvoer in het afdrukarchief op te slaan, zodat deze beschikbaar is voor verder afdrukken.</span><span class="sxs-lookup"><span data-stu-id="8fb97-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="8fb97-124">Als u de gearchiveerde uitvoer later wilt openen, gaat u naar **Organisatiebeheer** \> **Query's en rapporten** \> **Rapportarchief**.</span><span class="sxs-lookup"><span data-stu-id="8fb97-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="8fb97-125">[![De printerbestemming gebruiken](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="8fb97-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="8fb97-126">De optie **Converteren naar PDF** hoeft niet ingeschakeld te zijn wanneer u de bestemming **Printer** configureert.</span><span class="sxs-lookup"><span data-stu-id="8fb97-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="8fb97-127">De PDF-conversie wordt voor afdrukdoeleinden uitgevoerd, zelfs als de optie is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="8fb97-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="8fb97-128">Als u een bepaalde [afdrukstand](electronic-reporting-destinations.md#SelectPdfPageOrientation) wilt gebruiken wanneer u een uitgaand document afdrukt in Excel-indeling, moet u de optie **Converteren naar PDF** inschakelen.</span><span class="sxs-lookup"><span data-stu-id="8fb97-128">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="8fb97-129">Wanneer u de optie **Converteren naar PDF** instelt op **Ja**, wordt het veld **Afdrukstand** beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="8fb97-129">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="8fb97-130">Selecteer een afdrukstand in het veld **Afdrukstand**.</span><span class="sxs-lookup"><span data-stu-id="8fb97-130">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8fb97-131">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="8fb97-131">Additional resources</span></span>

- [<span data-ttu-id="8fb97-132">Overzicht van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="8fb97-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="8fb97-133">Bestemmingen van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="8fb97-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
