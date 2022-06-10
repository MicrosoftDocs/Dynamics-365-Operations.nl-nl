---
title: Positieve betalingsbestanden instellen en genereren met behulp van Elektronische rapportage
description: In dit onderwerp wordt uitgelegd hoe u positieve betalingsbestanden instelt met Elektronische rapportage.
author: panolte
ms.date: 03/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankPositivePayFormat
audience: Application User
ms.reviewer: twheeloc
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: bc2f17d62b429b599d5ac5f2a521819275d36b64
ms.sourcegitcommit: 2b4ee1fe05792332904396b5f495d74f2a217250
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2022
ms.locfileid: "8770242"
---
# <a name="set-up-positive-pay-files-by-using-electronic-reporting"></a>Positieve betalingsbestanden instellen met behulp van Elektronische rapportage

In dit onderwerp wordt uitgelegd hoe u positieve betaling instelt en positieve betalingsbestanden genereert met Elektronische rapportage.

> [!NOTE] 
> Voordat u de functie **positief betalingsbestand voor een bank genereren** gebruikt, moet u eerst de entiteitslijst vernieuwen.
> Ga naar **Gegevensbeheer > Importeren/exporteren > Raamwerkparameters** 
> **Entiteitinstellingen** (sneltabblad) en selecteer **Entiteitslijst vernieuwen**.


U kunt positief betalen gebruiken om een electronische lijst met cheques te genereren die aan de bank wordt gegeven. Wanneer een cheque aan de bank wordt gepresenteerd, vergelijkt de bank deze met de lijst met cheques. Als de cheque overeenkomt met wat de bank op de lijst heeft, keert de bank de cheque uit. Als de cheque niet overeenkomt met een cheque in de lijst, gaat de bank de cheque controleren.

## <a name="security-for-positive-pay-files"></a>Beveiliging voor positieve betalingsbestanden
Positieve betalingsbestanden kunnen vertrouwelijke informatie over begunstigden bevatten en chequebedragen. Verzeker daarom dat u de juiste beveiligingsmaatregelen treft vanaf de tijd dat bestanden worden gegenereerd, totdat deze door de bank worden ontvangen. Positieve betalingsbestanden worden gedownload naar de locatie die door uw webbrowser is opgegeven. Omdat positieve betalingsbestanden vertrouwelijke informatie kunnen bevatten, is het belangrijk dat alleen geautoriseerde gebruikers toegang hebben om deze informatie in Microsoft Dynamics 365 Finance te genereren en te bekijken. Gebruik de volgende tabel om u te helpen de bevoegdheden te bepalen die zijn vereist.

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
<td><strong>Positief betalingsbestand intrekken</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-the-electronic-reporting-configuration"></a>De configuratie van Elektronische rapportage instellen

1. Ga naar **Werkgebieden \> Elektronische rapportage**.
2. Ga naar de tegel voor de configuratieprovider **Microsoft** en selecteer **Opslagplaatsen**.
3. Selecteer **Algemeen** en selecteer vervolgens **Openen**.
4. Als een verbinding met de opslagplaats tot stand moet worden gebracht, selecteert u de blauwe koppeling in het dialoogvenster.
5. Zoek en selecteer **Model positieve betaling \> Indeling positieve betaling** in de configuratielijst.
6. Selecteer op het sneltabblad **Versies** de nieuwste versie en selecteer vervolgens **Importeren**.

## <a name="set-up-a-positive-pay-format"></a>Indeling positieve betaling instellen

1. Ga naar **Contanten en bankbeheer \> Instellen \> Indelingen positieve betaling**.
2. Selecteer **Nieuw**.
3. Stel de velden **Betalingsindeling** en **Beschrijving** in.
4. Schakel het selectievakje **Algemene elektronische exportindeling** in.
5. Stel het veld **Indelingsconfiguratie exporteren** in op **Indeling positieve betaling**.

## <a name="assign-a-positive-pay-format-to-a-bank-account"></a>Een positieve betalingsindeling toewijzen aan een bankrekening
Wijs voor elke bankrekening waarvoor u positieve betalingsinformatie wilt genereren, de positieve betalingsindeling toe die in de vorige sectie is opgegeven. Op de pagina Bankrekeningen selecteert u de positieve betalingsindeling die overeenkomt met de bankrekening. In het veld **Begindatum positieve betaling** voert u de eerste datum voor het genereren van positieve betalingsbestanden in. 

>[!Important]
> Voer in het veld **Begindatum positieve betaling** een datum in. Als het veld leeg wordt gelaten, worden in het eerste positieve betalingsbestand dat wordt gegenereerd alle cheques opgenomen die voor deze bankrekening zijn gemaakt.

1. Ga naar **Contanten en bankbeheer \> Bankrekeningen \> Bankrekeningen**.
2. Open de bankrekening.
3. Stel op het sneltabblad **Algemeen** het veld **Indeling positieve betaling** in op de indeling die eerder is gemaakt.
4. Stel het veld **Begindatum positieve betaling** in op de huidige datum.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Een nummerreeks voor positieve betalingsbestanden toewijzen
Elk positief betalingsbestand moet een uniek nummer hebben. Maak op de pagina **Parameters voor cash- en bankbeheer** een nummerreeks voor positieve betalingsbestanden op het tabblad **Nummerreeksen**.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Een positief betalingsbestand voor een enkele bankrekening genereren
U kunt een positief betalingsbestand genereren voor slechts één rechtspersoon en één bankrekening. Om positieve betalingsbestanden voor meerdere rechtspersonen en bankrekeningen tegelijkertijd te genereren, raadpleegt u de volgende sectie. Om een positief betalingsbestand voor één rechtspersoon en één bankrekening te genereren, opent u het dialoogvenster **Creëer een positief betalingsbestand** vanaf de pagina **Bankrekeningen**. Vul in het veld **Afsluitdatum** de laatste chequedatum in die u aan het positieve betalingsbestand wilt toevoegen. Alle cheques die niet aan een positief betalingsbestand zijn toegevoegd aan het eind van deze chequedatum worden opgenomen in het bestand.

1. Ga naar **Contanten en bankbeheer \> Bankrekeningen \> Bankrekeningen**.
2. Open een bankrekening waarvoor positieve betaling is ingesteld.
3. Selecteer **Betalingen beheren \> Positieve betaling \> Positief betalingsbestand**.
4. Stel het veld **Afsluitdatum** in. Cheques die voor deze datum zijn gegenereerd, worden opgenomen.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Een positief betalingsbestand voor meerdere bankrekeningen genereren
Als u een positief betalingsbestand voor meerdere bankrekeningen wilt genereren, gebruikt u de periodieke taak **Positief betalingsbestand**. Selecteer de positieve betalingsindeling voor het bestand en geef op of het bestand voor alle rechtspersonen wordt gegenereerd, of voor een geselecteerde rechtspersoon. U kunt ook het positief-betalingsbestand genereren voor alle bankrekeningen die de opgegeven positief betalingsindeling gebruiken of voor een specifieke bankrekening. Vul in het veld **Afsluitdatum** de laatste chequedatum in die u aan het positieve betalingsbestand wilt toevoegen. Alle cheques die niet aan een positief betalingsbestand zijn toegevoegd aan het eind van deze chequedatum worden opgenomen in het bestand.

## <a name="view-the-results-of-positive-pay-file-generation"></a>De resultaten weergeven van het genereren van positieve betalingsbestanden
Nadat het positieve betalingsbestand is gegenereerd, kunt u de resultaten op de pagina **Samenvatting van positief betalingsbestand** weergeven. Als u de details van de afzonderlijke cheques wilt weergeven, gaat u naar de pagina **Details positief betalingsbestand**.

## <a name="confirm-a-positive-pay-file"></a>Een positive pay-bestand bevestigen
Nadat de cheques betaald zijn die in een positive pay-bestand staan geregistreerd, ontvangt u een bevestigingsnummer van uw bank. U kunt het positief betalingsbestand dan bevestigen. Op de pagina **Samenvatting van positief betalingsbestand** selecteert u een positief betalingsbestand dat een status **Gemaakt** heeft en vervolgens selecteert u de actie **Bevestiging invoeren**. Wanneer u een positief betalingsbestand bevestigt, wordt het bevestigingsnummer dat u van de bank ontvangt vastgelegd.

## <a name="recall-a-positive-pay-file"></a>Een positive pay-bestand herroepen
Als u een positief betalingsbestand moet wijzigen, kunt u het intrekken. Selecteer op de pagina **Samenvatting van positief betalingsbestand** een positief betalingsbestand dat een status **Gemaakt** heeft en selecteer vervolgens de actie **Intrekken**. Voor elke cheque in het positieve betalingsbestand geeft het veld aan of die cheque is opgenomen in een positief betalingsbestand opnieuw ingesteld. Vervolgens kunt u een nieuw positieve betalingsbestand maken dat de ingetrokken cheque bevat.


Het resulterende XML-bestand wordt gedownload.
