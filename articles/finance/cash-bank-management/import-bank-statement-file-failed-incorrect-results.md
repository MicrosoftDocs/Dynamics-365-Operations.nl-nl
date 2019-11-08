---
title: Problemen oplossen met importeren van bankafschriftbestanden
description: Het is belangrijk dat het bankafschriftbestand van de bank overeenkomt met de indeling die Microsoft Dynamics 365 Finance ondersteunt. Vanwege strikte normen voor bankafschriften zullen de meeste integratie correct functioneren. Soms kan echter het afschriftbestand niet worden geïmporteerd of geeft onjuiste resultaten. Doorgaans worden deze problemen veroorzaakt door kleine verschillen in het bankafschriftbestand. In dit artikel wordt uitgelegd hoe u deze verschillen kunt oplossen.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 612ded1f68cc8e1b26b8046501bae1707175e23a
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188321"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="461b1-107">Problemen oplossen met importeren van bankafschriftbestanden</span><span class="sxs-lookup"><span data-stu-id="461b1-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="461b1-108">Het is belangrijk dat het bankafschriftbestand van de bank overeenkomt met de indeling die Microsoft Dynamics 365 Finance ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="461b1-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="461b1-109">Vanwege strikte normen voor bankafschriften zullen de meeste integratie correct functioneren.</span><span class="sxs-lookup"><span data-stu-id="461b1-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="461b1-110">Soms kan echter het afschriftbestand niet worden geïmporteerd of geeft onjuiste resultaten.</span><span class="sxs-lookup"><span data-stu-id="461b1-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="461b1-111">Doorgaans worden deze problemen veroorzaakt door kleine verschillen in het bankafschriftbestand.</span><span class="sxs-lookup"><span data-stu-id="461b1-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="461b1-112">In dit artikel wordt uitgelegd hoe u deze verschillen kunt oplossen.</span><span class="sxs-lookup"><span data-stu-id="461b1-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="461b1-113">Wat is de fout?</span><span class="sxs-lookup"><span data-stu-id="461b1-113">What is the error?</span></span>
------------------

<span data-ttu-id="461b1-114">Nadat u hebt geprobeerd een bankafschriftbestand te importeren, gaat u naar de geschiedenis van de taak in Gegevensbeheer en zoekt u de fout op in de uitvoeringsdetails.</span><span class="sxs-lookup"><span data-stu-id="461b1-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="461b1-115">De foutmelding kan helpen door te verwijzen naar het afschrift, het saldo, of de afschriftregel.</span><span class="sxs-lookup"><span data-stu-id="461b1-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="461b1-116">Hij bevat waarschijnlijk onvoldoende informatie om u te helpen het veld of het element te identificeren dat het probleem veroorzaakt.</span><span class="sxs-lookup"><span data-stu-id="461b1-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="461b1-117">Wat zijn de verschillen?</span><span class="sxs-lookup"><span data-stu-id="461b1-117">What are the differences?</span></span>
<span data-ttu-id="461b1-118">Vergelijk de indelingsdefinitie van het bankbestand met de importdefinitie van Finance en noteer eventuele verschillen tussen de velden en de elementen.</span><span class="sxs-lookup"><span data-stu-id="461b1-118">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="461b1-119">Vergelijk het bankafschriftbestand met het gerelateerde Finance-voorbeeldbestand.</span><span class="sxs-lookup"><span data-stu-id="461b1-119">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="461b1-120">Eventuele verschillen moeten gemakkelijk te zien zijn in de ISO20022-bestanden.</span><span class="sxs-lookup"><span data-stu-id="461b1-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="461b1-121">Verschillen in tijdzones op geïmporteerde bankafschriften</span><span class="sxs-lookup"><span data-stu-id="461b1-121">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="461b1-122">De datum-/tijdwaarden in het importbestand kunnen verschillen van de datum-/tijdwaarden die worden weergegeven in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="461b1-122">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="461b1-123">U kunt dit verschil voorkomen door een tijdzonevoorkeur in te voeren op de pagina **Gegevensbronnen configureren**.</span><span class="sxs-lookup"><span data-stu-id="461b1-123">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="461b1-124">Zie [Het importproces voor geavanceerde bankafstemming instellen](set-up-advanced-bank-reconciliation-import-process.md) voor meer informatie over het invoeren van een tijdzonevoorkeur.</span><span class="sxs-lookup"><span data-stu-id="461b1-124">See [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md) for more information about entering a time zone preference.</span></span>

## <a name="transformations"></a><span data-ttu-id="461b1-125">Transformaties</span><span class="sxs-lookup"><span data-stu-id="461b1-125">Transformations</span></span>
<span data-ttu-id="461b1-126">Doorgaans moeten wijzigingen worden doorgevoerd in één van drie transformaties.</span><span class="sxs-lookup"><span data-stu-id="461b1-126">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="461b1-127">Elke transformatie is geschreven voor een specifieke standaard.</span><span class="sxs-lookup"><span data-stu-id="461b1-127">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="461b1-128">Naam van bron</span><span class="sxs-lookup"><span data-stu-id="461b1-128">Resource name</span></span>                                         | <span data-ttu-id="461b1-129">Bestandsnaam</span><span class="sxs-lookup"><span data-stu-id="461b1-129">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="461b1-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="461b1-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="461b1-131">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="461b1-131">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="461b1-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="461b1-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="461b1-133">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="461b1-133">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="461b1-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="461b1-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="461b1-135">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="461b1-135">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="461b1-136">Foutopsporing in transformaties</span><span class="sxs-lookup"><span data-stu-id="461b1-136">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="461b1-137">De BAI2- en MT940-bestanden aanpassen</span><span class="sxs-lookup"><span data-stu-id="461b1-137">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="461b1-138">De BAI2- en MT940-bestanden zijn op tekst gebaseerde bestanden en moeten worden aangepast om foutopsporing van Extensible Stylesheet Language-transformaties mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="461b1-138">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="461b1-139">Het programma voert deze aanpassing door wanneer een bestand wordt geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="461b1-139">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="461b1-140">Maak een XML-bestand en kopieer hier de volgende tekst in.</span><span class="sxs-lookup"><span data-stu-id="461b1-140">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="461b1-141">Kopieer de inhoud van het bankafschriftbestand en vervang de tekst **PASTESTATEMENTFILEHERE** in het XML-bestand door de gekopieerde tekst.</span><span class="sxs-lookup"><span data-stu-id="461b1-141">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="461b1-142">Foutopsporing van de XSLT</span><span class="sxs-lookup"><span data-stu-id="461b1-142">Debug the XSLT</span></span>

<span data-ttu-id="461b1-143">Zie <https://msdn.microsoft.com/library/ms255605.aspx> voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="461b1-143">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="461b1-144">Start Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="461b1-144">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="461b1-145">Maak een consoletoepassing aan.</span><span class="sxs-lookup"><span data-stu-id="461b1-145">Create a console application.</span></span>
3.  <span data-ttu-id="461b1-146">Open de betreffende XSLT.</span><span class="sxs-lookup"><span data-stu-id="461b1-146">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="461b1-147">Klik op de XLST en de eigenschappenpagina ervan.</span><span class="sxs-lookup"><span data-stu-id="461b1-147">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="461b1-148">Stel de invoer in op de locatie van het bankafschriftbestand.</span><span class="sxs-lookup"><span data-stu-id="461b1-148">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="461b1-149">Definieer een locatie en een bestandsnaam voor de uitvoer.</span><span class="sxs-lookup"><span data-stu-id="461b1-149">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="461b1-150">Stel de vereiste onderbrekingspunten in.</span><span class="sxs-lookup"><span data-stu-id="461b1-150">Set the required break points.</span></span>
8.  <span data-ttu-id="461b1-151">Klik in het menu op **XML** &gt; **XSLT-foutopsporing starten**.</span><span class="sxs-lookup"><span data-stu-id="461b1-151">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="461b1-152">De XSLT-uitvoer opmaken</span><span class="sxs-lookup"><span data-stu-id="461b1-152">Format the XSLT output</span></span>

<span data-ttu-id="461b1-153">Tijdens het uitvoeren van de transformatie wordt een uitvoerbestand aangemaakt dat u in Visual Studio kunt weergeven.</span><span class="sxs-lookup"><span data-stu-id="461b1-153">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="461b1-154">Door middel van Ctrl+A, Ctrl+K en Ctrl+D kunt u het outputbestand snel opmaken.</span><span class="sxs-lookup"><span data-stu-id="461b1-154">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="461b1-155">De transformatie aanpassen</span><span class="sxs-lookup"><span data-stu-id="461b1-155">Adjust the transformation</span></span>

<span data-ttu-id="461b1-156">Pas de transformatie aan om het gewenste veld of element in het bankafschriftbestand te krijgen.</span><span class="sxs-lookup"><span data-stu-id="461b1-156">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="461b1-157">Wijs vervolgens dat veld of element toe aan het juiste Finance-element.</span><span class="sxs-lookup"><span data-stu-id="461b1-157">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="461b1-158">Debet- of creditindicator</span><span class="sxs-lookup"><span data-stu-id="461b1-158">Debit/credit indicator</span></span>

<span data-ttu-id="461b1-159">Soms komt het voor dat debetbedragen worden geïmporteerd als creditbedragen en andersom.</span><span class="sxs-lookup"><span data-stu-id="461b1-159">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="461b1-160">Om dit probleem op te lossen, moet u de betreffende XSLT aanpassen.</span><span class="sxs-lookup"><span data-stu-id="461b1-160">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="461b1-161">Als u bankafschriften van meerdere banken ontvangt, controleer dan of ze allemaal dezelfde debet-/creditbenadering gebruiken, of maak afzonderlijke transformaties aan.</span><span class="sxs-lookup"><span data-stu-id="461b1-161">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="461b1-162">BAI2XML-to-Reconciliation.xlst sjabloon GetAmountCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="461b1-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="461b1-163">ISO20022XML-to-Reconcilation.xslt sjabloon GetCreditDebit</span><span class="sxs-lookup"><span data-stu-id="461b1-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="461b1-164">MT940XML-to-Reconcilation.xslt sjabloon GetCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="461b1-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="461b1-165">Voorbeelden van bankafschriftindelingen en technische indelingen</span><span class="sxs-lookup"><span data-stu-id="461b1-165">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="461b1-166">In de onderstaande tabel ziet u voorbeelden van de technische indelingsdefinities voor geavanceerde bankafstemmingsimportbestanden en drie bijbehorende voorbeeldbestanden van bankafschriften:</span><span class="sxs-lookup"><span data-stu-id="461b1-166">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="461b1-167">U kunt de voorbeeldbestanden en technische indelingen hier downloaden: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="461b1-167">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="461b1-168">Technische indelingsdefinitie</span><span class="sxs-lookup"><span data-stu-id="461b1-168">Technical layout definition</span></span>                             | <span data-ttu-id="461b1-169">Voorbeeldbestand van bankafschrift</span><span class="sxs-lookup"><span data-stu-id="461b1-169">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="461b1-170">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="461b1-170">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="461b1-171">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="461b1-171">MT940StatementExample</span></span>                |
| <span data-ttu-id="461b1-172">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="461b1-172">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="461b1-173">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="461b1-173">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="461b1-174">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="461b1-174">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="461b1-175">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="461b1-175">BAI2StatementExample</span></span>                 |




