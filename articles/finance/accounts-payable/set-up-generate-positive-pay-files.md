---
title: Positieve betalingsbestanden instellen en genereren
description: In dit onderwerp wordt uitgelegd hoe u positieve betalingsbestanden instelt en genereert.
author: panolte
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 9f96e34b8d94f9e83afb39d6ad97aca85386b458
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830707"
---
# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="0de91-103">Positieve betalingsbestanden instellen en genereren</span><span class="sxs-lookup"><span data-stu-id="0de91-103">Set up and generate positive pay files</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0de91-104">In dit onderwerp wordt uitgelegd hoe u positieve betalingsbestanden instelt en genereert.</span><span class="sxs-lookup"><span data-stu-id="0de91-104">This topic explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="0de91-105">U kunt positief betalen gebruiken om een electronische lijst met cheques te genereren die aan de bank wordt gegeven.</span><span class="sxs-lookup"><span data-stu-id="0de91-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="0de91-106">Wanneer vervolgens een cheque aan de bank wordt gepresenteerd, vergelijkt de bank deze met de lijst met cheques.</span><span class="sxs-lookup"><span data-stu-id="0de91-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="0de91-107">Als de cheque overeenkomt met wat de bank op de lijst heeft, keert de bank de cheque uit.</span><span class="sxs-lookup"><span data-stu-id="0de91-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="0de91-108">Als de cheque niet overeenkomt met een cheque in de lijst, gaat de bank de cheque controleren.</span><span class="sxs-lookup"><span data-stu-id="0de91-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="0de91-109">Beveiliging voor positieve betalingsbestanden</span><span class="sxs-lookup"><span data-stu-id="0de91-109">Security for positive pay files</span></span>
<span data-ttu-id="0de91-110">Positieve betalingsbestanden kunnen vertrouwelijke informatie over begunstigden bevatten en chequebedragen.</span><span class="sxs-lookup"><span data-stu-id="0de91-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="0de91-111">Verzeker daarom dat u de juiste beveiligingsmaatregelen treft vanaf de tijd dat bestanden worden gegenereerd, totdat deze door de bank worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="0de91-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="0de91-112">Positieve betalingsbestanden worden gedownload naar de locatie die door uw webbrowser is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="0de91-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="0de91-113">Omdat positieve betalingsbestanden vertrouwelijke informatie kunnen bevatten, is het belangrijk dat alleen geautoriseerde gebruikers toegang hebben om deze informatie in Microsoft Dynamics 365 Finance te genereren en te bekijken.</span><span class="sxs-lookup"><span data-stu-id="0de91-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="0de91-114">Gebruik de volgende tabel om u te helpen de bevoegdheden te bepalen die zijn vereist.</span><span class="sxs-lookup"><span data-stu-id="0de91-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0de91-115">Opdracht</span><span class="sxs-lookup"><span data-stu-id="0de91-115">Task</span></span></th>
<th><span data-ttu-id="0de91-116">Bevoegdheid</span><span class="sxs-lookup"><span data-stu-id="0de91-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0de91-117">Genereer positieve betalingsbestanden van de lijstpagina <strong>Bankrekeningen</strong> of de pagina <strong>Bankrekeningen</strong>.</span><span class="sxs-lookup"><span data-stu-id="0de91-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="0de91-118"><strong>Informatie over positieve betalingen voor bank onderhouden</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="0de91-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="0de91-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="0de91-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0de91-120">Genereer positieve betalingsbestanden voor meerdere rechtspersonen en bankrekeningen op de pagina <strong>Creëer een positief betalingsbestand</strong>.</span><span class="sxs-lookup"><span data-stu-id="0de91-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="0de91-121"><strong>Informatie over positieve betalingen voor bank onderhouden</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="0de91-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="0de91-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="0de91-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0de91-123">Geef positieve betalingsbestanden weer op de pagina <strong>Samenvatting van positief betalingsbestand</strong>.</span><span class="sxs-lookup"><span data-stu-id="0de91-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="0de91-124"><strong>Positieve betalingsinformatie van bank weergeven voor meerdere rechtspersonen</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="0de91-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0de91-125">Bevestig een positief betalingsbestand voor de bank op de pagina <strong>Samenvatting van positief betalingsbestand</strong>.</span><span class="sxs-lookup"><span data-stu-id="0de91-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="0de91-126"><strong>Bevestig positief betalingsbestand</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="0de91-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0de91-127">Trek een positief betalingsbestand voor de bank in op de pagina <strong>Samenvatting van positief betalingsbestand</strong>.</span><span class="sxs-lookup"><span data-stu-id="0de91-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="0de91-128"><strong>Positief betalingsbestand intrekken</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="0de91-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="0de91-129">Indeling positieve betaling instellen</span><span class="sxs-lookup"><span data-stu-id="0de91-129">Set up a positive pay format</span></span>
<span data-ttu-id="0de91-130">Positieve betalingsbestanden worden gemaakt door gegevensentiteiten te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="0de91-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="0de91-131">Voordat u een positief betalingsbestand kunt genereren, moet u een transformatie-invoerindeling instellen die wordt gebruikt om de chequegegevens in een indeling te vertalen die met de bank kan communiceren.</span><span class="sxs-lookup"><span data-stu-id="0de91-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="0de91-132">Op de pagina **Indeling positieve betaling** kunt u een bestandsindelingidentificatie en omschrijving maken.</span><span class="sxs-lookup"><span data-stu-id="0de91-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="0de91-133">De indeling van transformatie-invoer moet een XML-type zijn.</span><span class="sxs-lookup"><span data-stu-id="0de91-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="0de91-134">De specifieke indeling is afhankelijk van het transformatiebestand dat u gebruikt.</span><span class="sxs-lookup"><span data-stu-id="0de91-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="0de91-135">Bijvoorbeeld: het Extensible Stylesheet Language Transformations (XSLT)-bestand dat is geleverd gebruikt de indeling **XML-element**.</span><span class="sxs-lookup"><span data-stu-id="0de91-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="0de91-136">Gebruik de actie **Bestand uploaden dat is gebruikt voor transformatie** om de locatie van het transformatiebestand voor de indeling op te geven die uw bank vereist.</span><span class="sxs-lookup"><span data-stu-id="0de91-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="0de91-137">Voorbeeld: XSLT-bestand voor positief betalingsbestand</span><span class="sxs-lookup"><span data-stu-id="0de91-137">Example: XSLT file for positive pay file</span></span>

```xml
<xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
  <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
  <xsl:template match="/">
    <xsl:value-of select="'
'" />
    <Document>
      <xsl:value-of select="'
'" />
      <!--Header Begin-->
      <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
      <xsl:value-of select="'
'" />
      <!--Header End-->
      <xsl:for-each select="Document/BANKPOSITIVEPAYEXPORTENTITY">
        <!--Cheque Detail begin-->
        <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
            <xsl:value-of select='string("Yes")'/>
          </xsl:when>
          <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
            <xsl:value-of select='string("No")'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='string(" ")'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("Payment")'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='CHEQUENUM/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='AMOUNTCUR/text()'/>
        <xsl:value-of select="','" />
        <xsl:value-of select='string("BOA-#1812")'/>
        <xsl:value-of select="','" />
        <xsl:choose>
          <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
            <xsl:value-of select='VENDGROUP/text()'/>
          </xsl:when>
          <xsl:otherwise>
            <xsl:value-of select='CUSTGROUP/text()'/>
          </xsl:otherwise>
        </xsl:choose>
        <xsl:value-of select="','" />
        <xsl:value-of select='TRANSDATE/text()'/>
        <xsl:value-of select="'
'" />
      </xsl:for-each>
    </Document>
  </xsl:template>
</xsl:stylesheet>
```

> [!NOTE]
> <span data-ttu-id="0de91-138">Voor XML-namen in de XSLT moet het hoofdlettergebruik overeenkomen met dat van de knooppunten in de XML.</span><span class="sxs-lookup"><span data-stu-id="0de91-138">XML names in the XSLT must match the casing of the nodes in the XML.</span></span> <span data-ttu-id="0de91-139">Zowel de XSLT- als XML-bestanden zijn hoofdlettergevoelig.</span><span class="sxs-lookup"><span data-stu-id="0de91-139">Both the XSLT and XML files are case sensitive.</span></span> 

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="0de91-140">Een positieve betalingsindeling toewijzen aan bankrekeningen</span><span class="sxs-lookup"><span data-stu-id="0de91-140">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="0de91-141">Wijs voor elke bankrekening waarvoor u positieve betalingsinformatie wilt genereren, de positieve betalingsindeling toe die in de vorige sectie is opgegeven.</span><span class="sxs-lookup"><span data-stu-id="0de91-141">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="0de91-142">Op de pagina **Bankrekeningen** selecteert u de positieve betalingsindeling die overeenkomt met de bankrekening.</span><span class="sxs-lookup"><span data-stu-id="0de91-142">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="0de91-143">In het veld **Begindatum positieve betaling** voert u de eerste datum voor het genereren van positieve betalingsbestanden in.</span><span class="sxs-lookup"><span data-stu-id="0de91-143">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="0de91-144">Het is belangrijk dat u een datum invoert in dit veld.</span><span class="sxs-lookup"><span data-stu-id="0de91-144">It's important that you enter a date in this field.</span></span> <span data-ttu-id="0de91-145">Anders neemt het eerste positieve betalingsbestand dat u genereert alle cheques op die u ooit voor deze bankrekening hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="0de91-145">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="0de91-146">Een nummerreeks voor positieve betalingsbestanden toewijzen</span><span class="sxs-lookup"><span data-stu-id="0de91-146">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="0de91-147">Elk positief betalingsbestand moet een uniek nummer hebben.</span><span class="sxs-lookup"><span data-stu-id="0de91-147">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="0de91-148">Gebruik het tabblad **Nummerreeksen** op de pagina **Parameters voor cash- en bankbeheer** om een nummerreeks te maken voor het positieve betalingsbestanden.</span><span class="sxs-lookup"><span data-stu-id="0de91-148">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="0de91-149">Een positief betalingsbestand voor een enkele bankrekening genereren</span><span class="sxs-lookup"><span data-stu-id="0de91-149">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="0de91-150">U kunt een positief betalingsbestand genereren voor slechts één rechtspersoon en één bankrekening.</span><span class="sxs-lookup"><span data-stu-id="0de91-150">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="0de91-151">Om positieve betalingsbestanden voor meerdere rechtspersonen en bankrekeningen tegelijkertijd te genereren, raadpleegt u de volgende sectie.</span><span class="sxs-lookup"><span data-stu-id="0de91-151">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="0de91-152">Om een positief betalingsbestand voor één rechtspersoon en één bankrekening te genereren, opent u het dialoogvenster **Creëer een positief betalingsbestand** vanaf de pagina **Bankrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="0de91-152">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="0de91-153">Vul in het veld **Afsluitdatum** de laatste chequedatum in die u aan het positieve betalingsbestand wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0de91-153">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="0de91-154">Alle cheques die niet aan een positief betalingsbestand zijn toegevoegd aan het eind van deze chequedatum worden opgenomen in het bestand.</span><span class="sxs-lookup"><span data-stu-id="0de91-154">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="0de91-155">Een positief betalingsbestand voor meerdere bankrekeningen genereren</span><span class="sxs-lookup"><span data-stu-id="0de91-155">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="0de91-156">Genereer positieve betalingsbestanden voor meerdere bankrekeningen met de periodieke taak **Creëer een positief betalingsbestand**.</span><span class="sxs-lookup"><span data-stu-id="0de91-156">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="0de91-157">Selecteer de positieve betalingsindeling voor het bestand en geef op of het bestand voor alle rechtspersonen wordt gegenereerd, of voor een geselecteerde rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="0de91-157">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="0de91-158">U kunt ook het positief-betalingsbestand genereren voor alle bankrekeningen die de opgegeven positief betalingsindeling gebruiken of voor een specifieke bankrekening.</span><span class="sxs-lookup"><span data-stu-id="0de91-158">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="0de91-159">Vul in het veld **Afsluitdatum** de laatste chequedatum in die u aan het positieve betalingsbestand wilt toevoegen.</span><span class="sxs-lookup"><span data-stu-id="0de91-159">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="0de91-160">Alle cheques die niet aan een positief betalingsbestand zijn toegevoegd aan het eind van deze chequedatum worden opgenomen in het bestand.</span><span class="sxs-lookup"><span data-stu-id="0de91-160">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="0de91-161">De resultaten weergeven van het genereren van positieve betalingsbestanden</span><span class="sxs-lookup"><span data-stu-id="0de91-161">View the results of positive pay file generation</span></span>
<span data-ttu-id="0de91-162">Nadat het positieve betalingsbestand is gegenereerd, kunt u de resultaten op de pagina **Samenvatting van positief betalingsbestand** weergeven.</span><span class="sxs-lookup"><span data-stu-id="0de91-162">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="0de91-163">Om de details van afzonderlijke cheques weer te geven, gebruikt u de detailpagina **Positief betalingsbestand**.</span><span class="sxs-lookup"><span data-stu-id="0de91-163">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="0de91-164">Een positive pay-bestand bevestigen</span><span class="sxs-lookup"><span data-stu-id="0de91-164">Confirm a positive pay file</span></span>
<span data-ttu-id="0de91-165">Nadat de cheques betaald zijn die in een positive pay-bestand staan geregistreerd, ontvangt u een bevestigingsnummer van uw bank.</span><span class="sxs-lookup"><span data-stu-id="0de91-165">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="0de91-166">U kunt het positief betalingsbestand dan bevestigen.</span><span class="sxs-lookup"><span data-stu-id="0de91-166">You can then confirm the positive pay file.</span></span> <span data-ttu-id="0de91-167">Op de pagina **Samenvatting van positief betalingsbestand** selecteert u een positief betalingsbestand dat een status **Gemaakt** heeft en vervolgens selecteert u de actie **Bevestiging invoeren**.</span><span class="sxs-lookup"><span data-stu-id="0de91-167">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="0de91-168">Wanneer u een positief betalingsbestand bevestigt, wordt het bevestigingsnummer dat u van de bank ontvangt vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="0de91-168">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="0de91-169">Een positive pay-bestand herroepen</span><span class="sxs-lookup"><span data-stu-id="0de91-169">Recall a positive pay file</span></span>
<span data-ttu-id="0de91-170">Als u een positief betalingsbestand moet wijzigen, kunt u het intrekken.</span><span class="sxs-lookup"><span data-stu-id="0de91-170">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="0de91-171">Selecteer op de pagina **Samenvatting van positief betalingsbestand** een positief betalingsbestand dat een status **Gemaakt** heeft en selecteer vervolgens de actie **Intrekken**.</span><span class="sxs-lookup"><span data-stu-id="0de91-171">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="0de91-172">Voor elke cheque in het positieve betalingsbestand geeft het veld aan of die cheque is opgenomen in een positief betalingsbestand opnieuw ingesteld.</span><span class="sxs-lookup"><span data-stu-id="0de91-172">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="0de91-173">Vervolgens kunt u een nieuw positieve betalingsbestand maken dat de ingetrokken cheque bevat.</span><span class="sxs-lookup"><span data-stu-id="0de91-173">You can then create a new positive pay file that includes the check that was recalled.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
