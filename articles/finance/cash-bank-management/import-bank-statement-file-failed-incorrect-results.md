---
title: Problemen oplossen met importeren van bankafschriftbestanden
description: Het is belangrijk dat het bankafschriftbestand van de bank overeenkomt met de indeling die Microsoft Dynamics 365 Finance ondersteunt. Vanwege strikte normen voor bankafschriften zullen de meeste integratie correct functioneren. Soms kan echter het afschriftbestand niet worden geïmporteerd of geeft onjuiste resultaten. Doorgaans worden deze problemen veroorzaakt door kleine verschillen in het bankafschriftbestand. In dit artikel wordt uitgelegd hoe u deze verschillen kunt oplossen.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0e01881a6b68526479d27014d49a718069cffc9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815879"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="08833-107">Problemen oplossen met importeren van bankafschriftbestanden</span><span class="sxs-lookup"><span data-stu-id="08833-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08833-108">Het is belangrijk dat het bankafschriftbestand van de bank overeenkomt met de indeling die Microsoft Dynamics 365 Finance ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="08833-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="08833-109">Vanwege strikte normen voor bankafschriften zullen de meeste integratie correct functioneren.</span><span class="sxs-lookup"><span data-stu-id="08833-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="08833-110">Soms kan echter het afschriftbestand niet worden geïmporteerd of geeft onjuiste resultaten.</span><span class="sxs-lookup"><span data-stu-id="08833-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="08833-111">Doorgaans worden deze problemen veroorzaakt door kleine verschillen in het bankafschriftbestand.</span><span class="sxs-lookup"><span data-stu-id="08833-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="08833-112">In dit artikel wordt uitgelegd hoe u deze verschillen kunt oplossen.</span><span class="sxs-lookup"><span data-stu-id="08833-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="08833-113">Wat is de fout?</span><span class="sxs-lookup"><span data-stu-id="08833-113">What is the error?</span></span>
------------------

<span data-ttu-id="08833-114">Nadat u hebt geprobeerd een bankafschriftbestand te importeren, gaat u naar de geschiedenis van de taak in Gegevensbeheer en zoekt u de fout op in de uitvoeringsdetails.</span><span class="sxs-lookup"><span data-stu-id="08833-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="08833-115">De foutmelding kan helpen door te verwijzen naar het afschrift, het saldo, of de afschriftregel.</span><span class="sxs-lookup"><span data-stu-id="08833-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="08833-116">Hij bevat waarschijnlijk onvoldoende informatie om u te helpen het veld of het element te identificeren dat het probleem veroorzaakt.</span><span class="sxs-lookup"><span data-stu-id="08833-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="08833-117">Geïmporteerde bankafschriften kunnen slechts één moment in de tijd overlappen.</span><span class="sxs-lookup"><span data-stu-id="08833-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="08833-118">Als een afschrijft bijvoorbeeld op 1 januari 2021 om 00:00 uur eindigt, kan de begindatum voor de volgende afschrift 00:00 uur zijn op 1 januari 2021.</span><span class="sxs-lookup"><span data-stu-id="08833-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="08833-119">Wat zijn de verschillen?</span><span class="sxs-lookup"><span data-stu-id="08833-119">What are the differences?</span></span>
<span data-ttu-id="08833-120">Vergelijk de indelingsdefinitie van het bankbestand met de importdefinitie van Finance en noteer eventuele verschillen tussen de velden en de elementen.</span><span class="sxs-lookup"><span data-stu-id="08833-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="08833-121">Vergelijk het bankafschriftbestand met het gerelateerde Finance-voorbeeldbestand.</span><span class="sxs-lookup"><span data-stu-id="08833-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="08833-122">Eventuele verschillen moeten gemakkelijk te zien zijn in de ISO20022-bestanden.</span><span class="sxs-lookup"><span data-stu-id="08833-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="08833-123">Verschillen in tijdzones op geïmporteerde bankafschriften</span><span class="sxs-lookup"><span data-stu-id="08833-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="08833-124">De datum-/tijdwaarden in het importbestand kunnen verschillen van de datum-/tijdwaarden die worden weergegeven in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="08833-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="08833-125">U kunt dit verschil voorkomen door een tijdzonevoorkeur in te voeren op de pagina **Gegevensbronnen configureren**.</span><span class="sxs-lookup"><span data-stu-id="08833-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="08833-126">Zie [Het importproces voor geavanceerde bankafstemming instellen](set-up-advanced-bank-reconciliation-import-process.md) voor meer informatie over het invoeren van een tijdzonevoorkeur.</span><span class="sxs-lookup"><span data-stu-id="08833-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="08833-127">Transformaties</span><span class="sxs-lookup"><span data-stu-id="08833-127">Transformations</span></span>
<span data-ttu-id="08833-128">Doorgaans moeten wijzigingen worden doorgevoerd in één van drie transformaties.</span><span class="sxs-lookup"><span data-stu-id="08833-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="08833-129">Elke transformatie is geschreven voor een specifieke standaard.</span><span class="sxs-lookup"><span data-stu-id="08833-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="08833-130">Naam van bron</span><span class="sxs-lookup"><span data-stu-id="08833-130">Resource name</span></span>                                         | <span data-ttu-id="08833-131">Bestandsnaam</span><span class="sxs-lookup"><span data-stu-id="08833-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="08833-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="08833-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="08833-133">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="08833-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="08833-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span><span class="sxs-lookup"><span data-stu-id="08833-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="08833-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="08833-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="08833-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="08833-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="08833-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="08833-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="08833-138">Foutopsporing in transformaties</span><span class="sxs-lookup"><span data-stu-id="08833-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="08833-139">De BAI2- en MT940-bestanden aanpassen</span><span class="sxs-lookup"><span data-stu-id="08833-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="08833-140">De BAI2- en MT940-bestanden zijn op tekst gebaseerde bestanden en moeten worden aangepast om foutopsporing van Extensible Stylesheet Language-transformaties mogelijk te maken.</span><span class="sxs-lookup"><span data-stu-id="08833-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="08833-141">Het programma voert deze aanpassing door wanneer een bestand wordt geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="08833-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="08833-142">Maak een XML-bestand en kopieer hier de volgende tekst in.</span><span class="sxs-lookup"><span data-stu-id="08833-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="08833-143">Kopieer de inhoud van het bankafschriftbestand en vervang de tekst **PASTESTATEMENTFILEHERE** in het XML-bestand door de gekopieerde tekst.</span><span class="sxs-lookup"><span data-stu-id="08833-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="08833-144">Foutopsporing van de XSLT</span><span class="sxs-lookup"><span data-stu-id="08833-144">Debug the XSLT</span></span>

<span data-ttu-id="08833-145">Zie <https://msdn.microsoft.com/library/ms255605.aspx> voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="08833-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="08833-146">Start Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="08833-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="08833-147">Maak een consoletoepassing aan.</span><span class="sxs-lookup"><span data-stu-id="08833-147">Create a console application.</span></span>
3.  <span data-ttu-id="08833-148">Open de betreffende XSLT.</span><span class="sxs-lookup"><span data-stu-id="08833-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="08833-149">Klik op de XLST en de eigenschappenpagina ervan.</span><span class="sxs-lookup"><span data-stu-id="08833-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="08833-150">Stel de invoer in op de locatie van het bankafschriftbestand.</span><span class="sxs-lookup"><span data-stu-id="08833-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="08833-151">Definieer een locatie en een bestandsnaam voor de uitvoer.</span><span class="sxs-lookup"><span data-stu-id="08833-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="08833-152">Stel de vereiste onderbrekingspunten in.</span><span class="sxs-lookup"><span data-stu-id="08833-152">Set the required break points.</span></span>
8.  <span data-ttu-id="08833-153">Klik in het menu op **XML** &gt; **XSLT-foutopsporing starten**.</span><span class="sxs-lookup"><span data-stu-id="08833-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="08833-154">De XSLT-uitvoer opmaken</span><span class="sxs-lookup"><span data-stu-id="08833-154">Format the XSLT output</span></span>

<span data-ttu-id="08833-155">Tijdens het uitvoeren van de transformatie wordt een uitvoerbestand aangemaakt dat u in Visual Studio kunt weergeven.</span><span class="sxs-lookup"><span data-stu-id="08833-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="08833-156">Door middel van Ctrl+A, Ctrl+K en Ctrl+D kunt u het outputbestand snel opmaken.</span><span class="sxs-lookup"><span data-stu-id="08833-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="08833-157">De transformatie aanpassen</span><span class="sxs-lookup"><span data-stu-id="08833-157">Adjust the transformation</span></span>

<span data-ttu-id="08833-158">Pas de transformatie aan om het gewenste veld of element in het bankafschriftbestand te krijgen.</span><span class="sxs-lookup"><span data-stu-id="08833-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="08833-159">Wijs vervolgens dat veld of element toe aan het juiste Finance-element.</span><span class="sxs-lookup"><span data-stu-id="08833-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="08833-160">Debet- of creditindicator</span><span class="sxs-lookup"><span data-stu-id="08833-160">Debit/credit indicator</span></span>

<span data-ttu-id="08833-161">Soms komt het voor dat debetbedragen worden geïmporteerd als creditbedragen en andersom.</span><span class="sxs-lookup"><span data-stu-id="08833-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="08833-162">Om dit probleem op te lossen, moet u de betreffende XSLT aanpassen.</span><span class="sxs-lookup"><span data-stu-id="08833-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="08833-163">Als u bankafschriften van meerdere banken ontvangt, controleer dan of ze allemaal dezelfde debet-/creditbenadering gebruiken, of maak afzonderlijke transformaties aan.</span><span class="sxs-lookup"><span data-stu-id="08833-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="08833-164">BAI2XML-to-Reconciliation.xlst sjabloon GetAmountCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="08833-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="08833-165">ISO20022XML-to-Reconcilation.xslt sjabloon GetCreditDebit</span><span class="sxs-lookup"><span data-stu-id="08833-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="08833-166">MT940XML-to-Reconcilation.xslt sjabloon GetCreditDebitIndicator</span><span class="sxs-lookup"><span data-stu-id="08833-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="08833-167">Voorbeelden van bankafschriftindelingen en technische indelingen</span><span class="sxs-lookup"><span data-stu-id="08833-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="08833-168">In de onderstaande tabel ziet u voorbeelden van de technische indelingsdefinities voor geavanceerde bankafstemmingsimportbestanden en drie bijbehorende voorbeeldbestanden van bankafschriften:</span><span class="sxs-lookup"><span data-stu-id="08833-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="08833-169">U kunt de voorbeeldbestanden en technische indelingen hier downloaden: [Voorbeelden van importbestanden](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="08833-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="08833-170">Technische indelingsdefinitie</span><span class="sxs-lookup"><span data-stu-id="08833-170">Technical layout definition</span></span>                             | <span data-ttu-id="08833-171">Voorbeeldbestand van bankafschrift</span><span class="sxs-lookup"><span data-stu-id="08833-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="08833-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="08833-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="08833-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="08833-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="08833-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="08833-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="08833-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="08833-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="08833-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="08833-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="08833-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="08833-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
