---
title: Positieve betalingsbestanden instellen en genereren
description: Dit artikel beschrijft hoe u positieve betalingsbestanden instelt en genereert.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 408d08628da983a865e7eabc8ebe1ec05c390372
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="set-up-and-generate-positive-pay-files"></a>Positieve betalingsbestanden instellen en genereren

[!include[banner](../includes/banner.md)]


Dit artikel beschrijft hoe u positieve betalingsbestanden instelt en genereert. 

U kunt positief betalen gebruiken om een electronische lijst met cheques te genereren die aan de bank wordt gegeven. Wanneer vervolgens een cheque aan de bank wordt gepresenteerd, vergelijkt de bank deze met de lijst met cheques. Als de cheque overeenkomt met wat de bank op de lijst heeft, keert de bank de cheque uit. Als de cheque niet overeenkomt met een cheque in de lijst, gaat de bank de cheque controleren.

## <a name="security-for-positive-pay-files"></a>Beveiliging voor positieve betalingsbestanden
Positieve betalingsbestanden kunnen vertrouwelijke informatie over begunstigden bevatten en chequebedragen. Verzeker daarom dat u de juiste beveiligingsmaatregelen treft vanaf de tijd dat bestanden worden gegenereerd, totdat deze door de bank worden ontvangen. Positieve betalingsbestanden worden gedownload naar de locatie die door uw webbrowser is opgegeven. Omdat positieve betalingsbestanden vertrouwelijke informatie kunnen bevatten, is het belangrijk dat alleen de geautoriseerde gebruikers toegang hebben om deze informatie in Microsoft Dynamics 365 for Operations te genereren en te bekijken. Gebruik de volgende tabel om u te helpen de bevoegdheden te bepalen die zijn vereist.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Opdracht</th>
<th>Bevoegdheid</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Genereer positieve betalingsbestanden van de lijstpagina <strong>Bankrekeningen</strong> of de pagina <strong>Bankrekeningen</strong>.</td>
<td><ul>
<li><strong>Informatie over positieve betalingen voor bank onderhouden</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Genereer positieve betalingsbestanden voor meerdere rechtspersonen en bankrekeningen op de pagina <strong>Creëer een positief betalingsbestand</strong>.</td>
<td><ul>
<li><strong>Informatie over positieve betalingen voor bank onderhouden</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Geef positieve betalingsbestanden weer op de pagina <strong>Samenvatting van positief betalingsbestand</strong>.</td>
<td><strong>Positieve betalingsinformatie van bank weergeven voor meerdere rechtspersonen</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Bevestig een positief betalingsbestand voor de bank op de pagina <strong>Samenvatting van positief betalingsbestand</strong>.</td>
<td><strong>Bevestig positief betalingsbestand</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Trek een positief betalingsbestand voor de bank in op de pagina <strong>Samenvatting van positief betalingsbestand</strong>.</td>
<td><strong>Positief betalingsbestand terugroepen</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a>Indeling positieve betaling instellen
Positieve betalingsbestanden worden gemaakt door gegevensentiteiten te gebruiken. Voordat u een positief betalingsbestand kunt genereren, moet u een transformatie-invoerindeling instellen die wordt gebruikt om de chequegegevens in een indeling te vertalen die met de bank kan communiceren. Op de pagina **Indeling positieve betaling** kunt u een bestandsindelingidentificatie en omschrijving maken. De indeling van transformatie-invoer moet een XML-type zijn. De specifieke indeling is afhankelijk van het transformatiebestand dat u gebruikt. Bijvoorbeeld: het Extensible Stylesheet Language Transformations (XSLT)-bestand dat is geleverd gebruikt de indeling **XML-element**. Gebruik de actie **Bestand uploaden dat is gebruikt voor transformatie** om de locatie van het transformatiebestand voor de indeling op te geven die uw bank vereist.

## <a name="example-xslt-file-for-positive-pay-file"></a>Voorbeeld: XSLT-bestand voor positief betalingsbestand
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
          <xsl:for-each select="Document/BankPositivePayExportEntity">
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

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>Een positieve betalingsindeling toewijzen aan bankrekeningen
Wijs voor elke bankrekening waarvoor u positieve betalingsinformatie wilt genereren, de positieve betalingsindeling toe die in de vorige sectie is opgegeven. Op de pagina **Bankrekeningen** selecteert u de positieve betalingsindeling die overeenkomt met de bankrekening. In het veld **Begindatum positieve betaling** voert u de eerste datum voor het genereren van positieve betalingsbestanden in. Het is belangrijk dat u een datum invoert in dit veld. Anders neemt het eerste positieve betalingsbestand dat u genereert alle cheques op die u ooit voor deze bankrekening hebt gemaakt.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Een nummerreeks voor positieve betalingsbestanden toewijzen
Elk positief betalingsbestand moet een uniek nummer hebben. Gebruik het tabblad **Nummerreeksen** op de pagina **Parameters voor cash- en bankbeheer** om een nummerreeks te maken voor het positieve betalingsbestanden.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Een positief betalingsbestand voor een enkele bankrekening genereren
U kunt een positief betalingsbestand genereren voor slechts één rechtspersoon en één bankrekening. Om positieve betalingsbestanden voor meerdere rechtspersonen en bankrekeningen tegelijkertijd te genereren, raadpleegt u de volgende sectie. Om een positief betalingsbestand voor één rechtspersoon en één bankrekening te genereren, opent u het dialoogvenster **Creëer een positief betalingsbestand** vanaf de pagina **Bankrekeningen**. Vul in het veld **Afsluitdatum** de laatste chequedatum in die u aan het positieve betalingsbestand wilt toevoegen. Alle cheques die niet aan een positief betalingsbestand zijn toegevoegd aan het eind van deze chequedatum worden opgenomen in het bestand.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Een positief betalingsbestand voor meerdere bankrekeningen genereren
Genereer positieve betalingsbestanden voor meerdere bankrekeningen met de periodieke taak **Creëer een positief betalingsbestand**. Selecteer de positieve betalingsindeling voor het bestand en geef op of het bestand voor alle rechtspersonen wordt gegenereerd, of voor een geselecteerde rechtspersoon. U kunt ook het positief-betalingsbestand genereren voor alle bankrekeningen die de opgegeven positief betalingsindeling gebruiken of voor een specifieke bankrekening. Vul in het veld **Afsluitdatum** de laatste chequedatum in die u aan het positieve betalingsbestand wilt toevoegen. Alle cheques die niet aan een positief betalingsbestand zijn toegevoegd aan het eind van deze chequedatum worden opgenomen in het bestand.

## <a name="view-the-results-of-positive-pay-file-generation"></a>De resultaten weergeven van het genereren van positieve betalingsbestanden
Nadat het positieve betalingsbestand is gegenereerd, kunt u de resultaten op de pagina **Samenvatting van positief betalingsbestand** weergeven. Om de details van afzonderlijke cheques weer te geven, gebruikt u de detailpagina **Positief betalingsbestand**.

## <a name="confirm-a-positive-pay-file"></a>Een positive pay-bestand bevestigen
Nadat de cheques betaald zijn die in een positive pay-bestand staan geregistreerd, ontvangt u een bevestigingsnummer van uw bank. U kunt het positief betalingsbestand dan bevestigen. Op de pagina **Samenvatting van positief betalingsbestand** selecteert u een positief betalingsbestand dat een status **Gemaakt** heeft en vervolgens selecteert u de actie **Bevestiging invoeren**. Wanneer u een positief betalingsbestand bevestigt, wordt het bevestigingsnummer dat u van de bank ontvangt vastgelegd.

## <a name="recall-a-positive-pay-file"></a>Een positive pay-bestand herroepen
Als u een positief betalingsbestand moet wijzigen, kunt u het intrekken. Selecteer op de pagina **Samenvatting van positief betalingsbestand** een positief betalingsbestand dat een status **Gemaakt** heeft en selecteer vervolgens de actie **Intrekken**. Voor elke cheque in het positieve betalingsbestand geeft het veld aan of die cheque is opgenomen in een positief betalingsbestand opnieuw ingesteld. Vervolgens kunt u een nieuw positieve betalingsbestand maken dat de ingetrokken cheque bevat.




