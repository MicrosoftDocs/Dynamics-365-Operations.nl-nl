---
title: Problemen oplossen met importeren van bankafschriftbestanden
description: Het is belangrijk dat het bankafschriftbestand van de bank overeenkomt met de indeling die Microsoft Dynamics 365 for Finance and Operations ondersteunt. Vanwege strikte normen voor bankafschriften zullen de meeste integratie correct functioneren. Soms kan echter het afschriftbestand niet worden geïmporteerd of geeft onjuiste resultaten. Doorgaans worden deze problemen veroorzaakt door kleine verschillen in het bankafschriftbestand. In dit artikel wordt uitgelegd hoe u deze verschillen kunt oplossen.
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
ms.openlocfilehash: 4275a4d77b03c55decbf161df8f2115183cac3d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1842396"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="b6a2f-107">Problemen oplossen met importeren van bankafschriftbestanden</span><span class="sxs-lookup"><span data-stu-id="b6a2f-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6a2f-108">Het is belangrijk dat het bankafschriftbestand van de bank overeenkomt met de indeling die Microsoft Dynamics 365 for Finance and Operations ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Finance and Operations supports.</span></span> <span data-ttu-id="b6a2f-109">Vanwege strikte normen voor bankafschriften zullen de meeste integratie correct functioneren.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="b6a2f-110">Soms kan echter het afschriftbestand niet worden geïmporteerd of geeft onjuiste resultaten.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="b6a2f-111">Doorgaans worden deze problemen veroorzaakt door kleine verschillen in het bankafschriftbestand.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="b6a2f-112">In dit artikel wordt uitgelegd hoe u deze verschillen kunt oplossen.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="b6a2f-113">Wat is de fout?</span><span class="sxs-lookup"><span data-stu-id="b6a2f-113">What is the error?</span></span>
------------------

<span data-ttu-id="b6a2f-114">Nadat u hebt geprobeerd een bankafschriftbestand te importeren, gaat u naar de geschiedenis van de taak in Gegevensbeheer en zoekt u de fout op in de uitvoeringsdetails.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="b6a2f-115">De foutmelding kan helpen door te verwijzen naar het afschrift, het saldo, of de afschriftregel.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="b6a2f-116">Hij bevat waarschijnlijk onvoldoende informatie om u te helpen het veld of het element te identificeren dat het probleem veroorzaakt.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="b6a2f-117">Wat zijn de verschillen?</span><span class="sxs-lookup"><span data-stu-id="b6a2f-117">What are the differences?</span></span>
<span data-ttu-id="b6a2f-118">Vergelijk de indelingsdefinitie van het bankbestand met de importdefinitie van Finance and Operations en noteer eventuele verschillen tussen de velden en de elementen.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-118">Compare the bank file layout definition to the Finance and Operations import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="b6a2f-119">Vergelijk het bankafschriftbestand met het gerelateerde Finance and Operations-voorbeeldbestand.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-119">Compare the bank statement file to the related sample Finance and Operations file.</span></span> <span data-ttu-id="b6a2f-120">Eventuele verschillen moeten gemakkelijk te zien zijn in de ISO20022-bestanden.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="transformations"></a><span data-ttu-id="b6a2f-121">Transformaties</span><span class="sxs-lookup"><span data-stu-id="b6a2f-121">Transformations</span></span>
<span data-ttu-id="b6a2f-122">Doorgaans moeten wijzigingen worden doorgevoerd in één van drie transformaties.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-122">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="b6a2f-123">Elke transformatie is geschreven voor een specifieke standaard.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-123">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="b6a2f-124">Naam van bron</span><span class="sxs-lookup"><span data-stu-id="b6a2f-124">Resource name</span></span>                                         | <span data-ttu-id="b6a2f-125">Bestandsnaam</span><span class="sxs-lookup"><span data-stu-id="b6a2f-125">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="b6a2f-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="b6a2f-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="b6a2f-127">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="b6a2f-127">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="b6a2f-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="b6a2f-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="b6a2f-129">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="b6a2f-129">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="b6a2f-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="b6a2f-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="b6a2f-131">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="b6a2f-131">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="b6a2f-132">Foutopsporing in transformaties</span><span class="sxs-lookup"><span data-stu-id="b6a2f-132">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="b6a2f-133">De BAI2- en MT940-bestanden aanpassen</span><span class="sxs-lookup"><span data-stu-id="b6a2f-133">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="b6a2f-134">De BAI2- en MT940-bestanden zijn op tekst gebaseerde bestanden en moeten worden aangepast om foutopsporing van Extensible Stylesheet Language-transformaties mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-134">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="b6a2f-135">Het programma voert deze aanpassing door wanneer een bestand wordt geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-135">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="b6a2f-136">Maak een XML-bestand en kopieer hier de volgende tekst in.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-136">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="b6a2f-137">Kopieer de inhoud van het bankafschriftbestand en vervang de tekst **PASTESTATEMENTFILEHERE** in het XML-bestand door de gekopieerde tekst.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-137">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="b6a2f-138">Foutopsporing van de XSLT</span><span class="sxs-lookup"><span data-stu-id="b6a2f-138">Debug the XSLT</span></span>

<span data-ttu-id="b6a2f-139">Zie <https://msdn.microsoft.com/library/ms255605.aspx> voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-139">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="b6a2f-140">Start Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-140">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="b6a2f-141">Maak een consoletoepassing aan.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-141">Create a console application.</span></span>
3.  <span data-ttu-id="b6a2f-142">Open de betreffende XSLT.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-142">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="b6a2f-143">Klik op de XLST en de eigenschappenpagina ervan.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-143">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="b6a2f-144">Stel de invoer in op de locatie van het bankafschriftbestand.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-144">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="b6a2f-145">Definieer een locatie en een bestandsnaam voor de uitvoer.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-145">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="b6a2f-146">Stel de vereiste onderbrekingspunten in.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-146">Set the required break points.</span></span>
8.  <span data-ttu-id="b6a2f-147">Klik in het menu op **XML** &gt; **XSLT-foutopsporing starten**.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-147">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="b6a2f-148">De XSLT-uitvoer opmaken</span><span class="sxs-lookup"><span data-stu-id="b6a2f-148">Format the XSLT output</span></span>

<span data-ttu-id="b6a2f-149">Tijdens het uitvoeren van de transformatie wordt een uitvoerbestand aangemaakt dat u in Visual Studio kunt weergeven.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-149">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="b6a2f-150">Door middel van Ctrl+A, Ctrl+K en Ctrl+D kunt u het outputbestand snel opmaken.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-150">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="b6a2f-151">De transformatie aanpassen</span><span class="sxs-lookup"><span data-stu-id="b6a2f-151">Adjust the transformation</span></span>

<span data-ttu-id="b6a2f-152">Pas de transformatie aan om het gewenste veld of element in het bankafschriftbestand te krijgen.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-152">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="b6a2f-153">Wijs vervolgens dat veld of element toe aan het juiste Finance and Operations-element.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-153">Then map that field or element to the appropriate Finance and Operations element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="b6a2f-154">Debet- of creditindicator</span><span class="sxs-lookup"><span data-stu-id="b6a2f-154">Debit/credit indicator</span></span>

<span data-ttu-id="b6a2f-155">Soms komt het voor dat debetbedragen worden geïmporteerd als creditbedragen en andersom.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-155">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="b6a2f-156">Om dit probleem op te lossen, moet u de betreffende XSLT aanpassen.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-156">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="b6a2f-157">Als u bankafschriften van meerdere banken ontvangt, controleer dan of ze allemaal dezelfde debet-/creditbenadering gebruiken, of maak afzonderlijke transformaties aan.</span><span class="sxs-lookup"><span data-stu-id="b6a2f-157">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="b6a2f-158">BAI2XML-to-Reconciliation.xlst sjabloon GetAmountCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="b6a2f-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="b6a2f-159">ISO20022XML-to-Reconcilation.xslt sjabloon GetCreditDebit</span><span class="sxs-lookup"><span data-stu-id="b6a2f-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="b6a2f-160">MT940XML-to-Reconcilation.xslt sjabloon GetCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="b6a2f-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="b6a2f-161">Voorbeelden van bankafschriftindelingen en technische indelingen</span><span class="sxs-lookup"><span data-stu-id="b6a2f-161">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="b6a2f-162">In de onderstaande tabel ziet u voorbeelden van de technische indelingsdefinities voor geavanceerde bankafstemmingsimportbestanden en drie bijbehorende voorbeeldbestanden van bankafschriften:</span><span class="sxs-lookup"><span data-stu-id="b6a2f-162">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="b6a2f-163">U kunt de voorbeeldbestanden en technische indelingen hier downloaden: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="b6a2f-163">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="b6a2f-164">Technische indelingsdefinitie</span><span class="sxs-lookup"><span data-stu-id="b6a2f-164">Technical layout definition</span></span>                             | <span data-ttu-id="b6a2f-165">Voorbeeldbestand van bankafschrift</span><span class="sxs-lookup"><span data-stu-id="b6a2f-165">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="b6a2f-166">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="b6a2f-166">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="b6a2f-167">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="b6a2f-167">MT940StatementExample</span></span>                |
| <span data-ttu-id="b6a2f-168">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="b6a2f-168">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="b6a2f-169">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="b6a2f-169">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="b6a2f-170">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="b6a2f-170">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="b6a2f-171">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="b6a2f-171">BAI2StatementExample</span></span>                 |





