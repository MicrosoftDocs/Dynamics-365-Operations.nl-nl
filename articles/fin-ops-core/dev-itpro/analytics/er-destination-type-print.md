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
# <a name="PrinterDestinationType"></a><span data-ttu-id="2b457-103">Printerbestemming</span><span class="sxs-lookup"><span data-stu-id="2b457-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b457-104">U kunt een gegenereerd document rechtstreeks naar een netwerkprinter sturen om direct af te drukken.</span><span class="sxs-lookup"><span data-stu-id="2b457-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2b457-105">Vereisten</span><span class="sxs-lookup"><span data-stu-id="2b457-105">Prerequisites</span></span>

<span data-ttu-id="2b457-106">Voordat u begint, moet u de documentrouteringsagent installeren en configureren en vervolgens de netwerkprinters registreren.</span><span class="sxs-lookup"><span data-stu-id="2b457-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="2b457-107">Zie voor meer informatie [De documentrouteringsagent installeren om afdrukken via het netwerk in te schakelen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span><span class="sxs-lookup"><span data-stu-id="2b457-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="2b457-108">De printerbestemming beschikbaar maken</span><span class="sxs-lookup"><span data-stu-id="2b457-108">Make the Printer destination available</span></span>

<span data-ttu-id="2b457-109">Als u de bestemming **Printer** beschikbaar wilt maken in de huidige instantie van Microsoft Dynamics 365 Finance, gaat u naar het werkgebied **Functiebeheer** en schakelt u de volgende functies in deze volgorde in:</span><span class="sxs-lookup"><span data-stu-id="2b457-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="2b457-110">Voor elektronische rapportage uitgaande documenten met Microsoft Office-indelingen converteren naar PDF.</span><span class="sxs-lookup"><span data-stu-id="2b457-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="2b457-111">Documentrouteringsagent als bestemming voor elektronische rapportage voor uitgaande documenten</span><span class="sxs-lookup"><span data-stu-id="2b457-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="2b457-112">[![De bestemmingsfunctie ER-printer in Functiebeheer inschakelen](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="2b457-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="2b457-113">Toepasbaarheid</span><span class="sxs-lookup"><span data-stu-id="2b457-113">Applicability</span></span>

<span data-ttu-id="2b457-114">De bestemming **Printer** kan alleen worden geconfigureerd voor bestandsonderdelen die worden gebruikt voor het genereren van uitvoer in afdrukbare PDF-indeling (PDF Merger of PDF-bestandsindelingselementen) of Microsoft Office Excel/Word-indeling (Excel-bestand).</span><span class="sxs-lookup"><span data-stu-id="2b457-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="2b457-115">Wanneer de uitvoer wordt gegenereerd in PDF-indeling, wordt deze naar een printer verzonden.</span><span class="sxs-lookup"><span data-stu-id="2b457-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="2b457-116">Wanneer de uitvoer in Microsoft Office-indeling wordt gegenereerd, wordt deze automatisch geconverteerd naar de PDF-indeling en vervolgens naar een printer verzonden.</span><span class="sxs-lookup"><span data-stu-id="2b457-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="2b457-117">Beperkingen</span><span class="sxs-lookup"><span data-stu-id="2b457-117">Limitations</span></span>

<span data-ttu-id="2b457-118">Deze functie is een voorbeeldfunctie en is onderworpen aan de gebruiksvoorwaarden die worden beschreven in [aanvullende gebruiksvoorwaarden voor Microsoft Dynamics 365-voorbeelden](https://go.microsoft.com/fwlink/?linkid=2105274).</span><span class="sxs-lookup"><span data-stu-id="2b457-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="2b457-119">De bestemming **Printer** is alleen geïmplementeerd voor cloudimplementaties.</span><span class="sxs-lookup"><span data-stu-id="2b457-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="2b457-120">De printerbestemming gebruiken</span><span class="sxs-lookup"><span data-stu-id="2b457-120">Use the Printer destination</span></span>

1. <span data-ttu-id="2b457-121">Stel de optie **ingeschakeld** in op **Ja** als u een gegenereerd document naar een printer wilt verzenden.</span><span class="sxs-lookup"><span data-stu-id="2b457-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="2b457-122">Selecteer in het veld **Printernaam** de gewenste netwerkprinter.</span><span class="sxs-lookup"><span data-stu-id="2b457-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="2b457-123">Stel de optie **Opslaan in afdrukarchief?** in op **Ja** om de gegenereerde uitvoer in het afdrukarchief op te slaan, zodat deze beschikbaar is voor verder afdrukken.</span><span class="sxs-lookup"><span data-stu-id="2b457-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="2b457-124">Als u de gearchiveerde uitvoer later wilt openen, gaat u naar **Organisatiebeheer** \> **Query's en rapporten** \> **Rapportarchief**.</span><span class="sxs-lookup"><span data-stu-id="2b457-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="2b457-125">[![De printerbestemming gebruiken](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="2b457-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="2b457-126">De optie **Converteren naar PDF** hoeft niet ingeschakeld te zijn wanneer u de bestemming **Printer** configureert.</span><span class="sxs-lookup"><span data-stu-id="2b457-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="2b457-127">De PDF-conversie wordt voor afdrukdoeleinden uitgevoerd, zelfs als de optie is uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="2b457-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b457-128">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="2b457-128">Additional resources</span></span>

- [<span data-ttu-id="2b457-129">Overzicht van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="2b457-129">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="2b457-130">Bestemmingen van elektronische rapportage (ER)</span><span class="sxs-lookup"><span data-stu-id="2b457-130">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
