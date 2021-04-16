---
title: ER-configuraties ontwerpen om byte order mark (BOM) in gegenereerde bestanden te onderdrukken
description: In dit onderwerp wordt uitgelegd hoe u een ER-indeling (Electronic Reporting) configureert om rapporten te genereren die byte order mark (BOM) tekens onderdrukken.
author: NickSelin
ms.date: 01/04/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fabc308b1b0682c6fdce3e81e7335417846bebd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743528"
---
# <a name="design-er-configurations-to-suppress-bom-characters-in-generated-files"></a><span data-ttu-id="fe250-103">ER-configuraties ontwerpen om byte order mark (BOM) in gegenereerde bestanden te onderdrukken</span><span class="sxs-lookup"><span data-stu-id="fe250-103">Design ER configurations to suppress BOM characters in generated files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe250-104">U kunt een [Electronic reporting (ER)](general-electronic-reporting.md) [oplossing](er-quick-start1-new-solution.md) ontwerpen om uitgaande documenten te genereren.</span><span class="sxs-lookup"><span data-stu-id="fe250-104">You can design an [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md) to generate outgoing documents.</span></span> <span data-ttu-id="fe250-105">Als u documenten wilt genereren als tekst- of XML-bestanden, moet de oplossing een ER-[configuratie](general-electronic-reporting.md#Configuration) bevatten die een ER-[indelings](general-electronic-reporting.md#FormatComponentOutbound)component bevat.</span><span class="sxs-lookup"><span data-stu-id="fe250-105">To generate the documents as text or XML files, the solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="fe250-106">Als u de [tekenversleuteling](https://docs.microsoft.com/windows/win32/intl/character-sets) wilt opgeven die de set tekens in gegenereerde bestanden vertegenwoordigt, moet de ER-indeling het indelingselement **Common\\File** bevatten.</span><span class="sxs-lookup"><span data-stu-id="fe250-106">To specify the [character encoding](https://docs.microsoft.com/windows/win32/intl/character-sets) that represents the set of characters in generated files, the ER format must contain the **Common\\File** format element.</span></span> <span data-ttu-id="fe250-107">Om het ER-indelingsonderdeel te configureren, moet u de [concept](general-electronic-reporting.md#component-versioning)-versie van de ER-configuratie in de ER-indelingsontwerper openen en het element **Common\\File** toevoegen.</span><span class="sxs-lookup"><span data-stu-id="fe250-107">To configure the ER format component, open the [draft](general-electronic-reporting.md#component-versioning) version of the ER configuration in the ER format designer, and add the **Common\\File** element.</span></span> <span data-ttu-id="fe250-108">Geef in het veld **Codering** de codering op van uitgaande bestanden die tijdens runtime worden gegenereerd met dit onderdeel.</span><span class="sxs-lookup"><span data-stu-id="fe250-108">In the **Encoding** field, specify the encoding of outbound files that are generated at runtime by using this component.</span></span>

> [!NOTE]
> <span data-ttu-id="fe250-109">Als de indeling een onjuiste coderingsnaam bevat, ontstaat er een fout wanneer u de wijzigingen in de instellingen van de indeling opslaat.</span><span class="sxs-lookup"><span data-stu-id="fe250-109">If the format contains an incorrect encoding name, an error is thrown when you save your changes to the format's settings.</span></span>

![Een hoofdelement toevoegen op de pagina Indelingsontwerper](./media/er-suppress-bom-characters-image1.gif)

<span data-ttu-id="fe250-111">Als u **UTF-8**, **UTF-16** of **UTF-32** als codering opgeeft, komt de optie **BOM-tekens onderdrukken** beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="fe250-111">If you specify **UTF-8**, **UTF-16**, or **UTF-32** as the encoding, the **Suppress BOM characters** option becomes available.</span></span> <span data-ttu-id="fe250-112">Stel deze optie in op **Ja** om [BOM-tekens (byte order mark)](https://docs.microsoft.com/globalization/encoding/byte-order-mark) te onderdrukken in uitgaande bestanden die tijdens runtime worden gegenereerd wanneer de bewerkbare ER-indeling wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="fe250-112">Set this option to **Yes** to suppress [byte order mark (BOM) characters](https://docs.microsoft.com/globalization/encoding/byte-order-mark) in outbound files that are generated at runtime when the editable ER format is run.</span></span>

> [!NOTE]
> <span data-ttu-id="fe250-113">Als u het veld **Codering** leeg laat, wordt de standaardcodering **UTF-8** gebruikt.</span><span class="sxs-lookup"><span data-stu-id="fe250-113">If you leave the **Encoding** field blank, the default **UTF-8** encoding is used.</span></span>

![De optie BOM-tekens onderdrukken instellen op de pagina Indelingsontwerper](./media/er-suppress-bom-characters-image2.gif)

<span data-ttu-id="fe250-115">Voer de juiste procedure uit om de functionaliteit tijdens runtime te controleren.</span><span class="sxs-lookup"><span data-stu-id="fe250-115">To review the functionality at runtime, complete the appropriate procedure.</span></span> <span data-ttu-id="fe250-116">Voer bijvoorbeeld de stappen in het onderwerp [De uitvoering van XML-elementen in ER-indelingen uitstellen](er-defer-xml-element.md) uit.</span><span class="sxs-lookup"><span data-stu-id="fe250-116">For example, complete the steps in the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic.</span></span> <span data-ttu-id="fe250-117">Nadat u de stappen in het gedeelte [De indeling wijzigen zodat de berekening wordt gebaseerd op gegenereerde uitvoer](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) van dat onderwerp hebt uitgevoerd, voert u deze extra stappen uit.</span><span class="sxs-lookup"><span data-stu-id="fe250-117">After you've completed the steps in the [Modify the format so that the calculation is based on generated output](er-defer-xml-element.md#modify-the-format-so-that-the-calculation-is-based-on-generated-output) section of that topic, follow these additional steps.</span></span>

1. <span data-ttu-id="fe250-118">De UTF-codering opgeven:</span><span class="sxs-lookup"><span data-stu-id="fe250-118">Specify the UTF encoding:</span></span>

    1. <span data-ttu-id="fe250-119">Selecteer het element **Rapport** van het type **Common\\File**.</span><span class="sxs-lookup"><span data-stu-id="fe250-119">Select the **Report** element of the **Common\\File** type.</span></span>
    2. <span data-ttu-id="fe250-120">Geef in het veld **Codering** de codering **UTF-8** op.</span><span class="sxs-lookup"><span data-stu-id="fe250-120">In the **Encoding** field, specify the **UTF-8** encoding.</span></span>

2. <span data-ttu-id="fe250-121">Genereer een XML-bestand dat een BOM-teken bevat:</span><span class="sxs-lookup"><span data-stu-id="fe250-121">Generate an XML file that includes a BOM character:</span></span>

    1. <span data-ttu-id="fe250-122">Stel de optie **BOM-tekens onderdrukken** in op **Nee** om BOM-tekens op te nemen in gegenereerde XML-bestanden.</span><span class="sxs-lookup"><span data-stu-id="fe250-122">Set the **Suppress BOM characters** option to **No** to include BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="fe250-123">Voltooi de stappen in het gedeelte [De uitvoering van het samenvattings-XML-element uitstellen zodat het berekende totaal wordt gebruikt](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) van het onderwerp [De uitvoering van XML-elementen in ER-indelingen uitstellen](er-defer-xml-element.md) en sla het gegenereerde bestand op als **SampleXmlReport.xml**.</span><span class="sxs-lookup"><span data-stu-id="fe250-123">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport.xml**.</span></span>

3. <span data-ttu-id="fe250-124">Genereer een XML-bestand dat geen BOM-teken bevat:</span><span class="sxs-lookup"><span data-stu-id="fe250-124">Generate an XML file that doesn't include a BOM character:</span></span>

    1. <span data-ttu-id="fe250-125">Stel de optie **BOM-tekens onderdrukken** in op **Ja** om BOM-tekens te onderdrukken in gegenereerde XML-bestanden.</span><span class="sxs-lookup"><span data-stu-id="fe250-125">Set the **Suppress BOM characters** option to **Yes** to suppress BOM characters in generated XML files.</span></span>
    2. <span data-ttu-id="fe250-126">Voltooi de stappen in het gedeelte [De uitvoering van het samenvattings-XML-element uitstellen zodat het berekende totaal wordt gebruikt](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) van het onderwerp [De uitvoering van XML-elementen in ER-indelingen uitstellen](er-defer-xml-element.md) en sla het gegenereerde bestand op als **SampleXmlReport (1).xml**.</span><span class="sxs-lookup"><span data-stu-id="fe250-126">Complete the steps in the [Defer the execution of the summary XML element so that the calculated total is used](er-defer-xml-element.md#defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used) section of the [Defer the execution of XML elements in ER formats](er-defer-xml-element.md) topic, and save the generated file as **SampleXmlReport (1).xml**.</span></span>

4. <span data-ttu-id="fe250-127">Vergelijk de gegenereerde bestanden in een bestandsvergelijkingsprogramma.</span><span class="sxs-lookup"><span data-stu-id="fe250-127">In a file comparison utility, compare the generated files.</span></span>

    <span data-ttu-id="fe250-128">Het eerste verschil dat u ziet, is in de bestandskoptekst.</span><span class="sxs-lookup"><span data-stu-id="fe250-128">The first difference that you will notice is in the file header.</span></span> <span data-ttu-id="fe250-129">Het SampleXmlReport.xml-bestand bevat een BOM-teken, terwijl het bestand SampleXmlReport (1).xml dit niet bevat.</span><span class="sxs-lookup"><span data-stu-id="fe250-129">The SampleXmlReport.xml file contains a BOM character, where the SampleXmlReport (1).xml file doesn't.</span></span>

    ![Gegenereerde bestanden vergelijken met een bestandsvergelijkingsprogramma](./media/er-suppress-bom-characters-image3.png)

## <a name="see-also"></a><span data-ttu-id="fe250-131">Zie ook</span><span class="sxs-lookup"><span data-stu-id="fe250-131">See also</span></span>

- [<span data-ttu-id="fe250-132">De uitvoering van XML-elementen in ER-indelingen uitstellen</span><span class="sxs-lookup"><span data-stu-id="fe250-132">Defer the execution of XML elements in ER formats</span></span>](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]