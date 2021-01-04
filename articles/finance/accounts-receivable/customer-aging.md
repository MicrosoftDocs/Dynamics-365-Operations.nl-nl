---
title: Naar ouderdom gerangschikt rapport voor klanten
description: In het naar ouderdom gerangschikt rapport voor klanten worden de saldi weergegeven die door klanten verschuldigd zijn, gesorteerd op datuminterval of ouderdomsperiode.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3a1bba4596c7b645c20a790a6cbe8725ab665d
ms.sourcegitcommit: d77e902b1ab436e5ff3e78c496f5a70ef38e737c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/15/2020
ms.locfileid: "4442130"
---
# <a name="customer-aging-report"></a>Naar ouderdom gerangschikt rapport voor klanten 

In het **naar ouderdom gerangschikt** rapport voor klanten worden de saldi weergegeven die door klanten verschuldigd zijn, gesorteerd op datuminterval of ouderdomsperiode.

Wanneer u dit rapport genereert, worden de volgende standaardparameters weergegeven. U kunt deze parameters gebruiken om de gegevens te filteren die in het rapport worden weergegeven. Zie [Verzamelingen instellen](set-up-collections.md) voor meer informatie.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Veld</p></th>
<th><p>Beschrijving</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Factureringsclassificatie</strong></p></td>
<td><p>Selecteer een of meer factureringsclassificaties die u in het rapport wilt opnemen.</p>
<div class="alert">

**Opmerking**: dit besturingselement is alleen beschikbaar als de configuratiesleutel <STRONG>Openbare sector</STRONG> is geselecteerd.</P>


</div></td>
</tr>
<tr class="even">
<td><p><strong>Transacties opnemen zonder een factureringsclassificatie</strong></p></td>
<td><p>Als dit selectievakje is ingeschakeld, worden alle transacties waaraan geen factureringsclassificatie is toegewezen, weergegeven in het rapport.</p>
<div class="alert">

**Opmerking**: dit besturingselement is alleen beschikbaar als de configuratiesleutel <STRONG>Openbare sector</STRONG> is geselecteerd.</P>

</div></td>
</tr>
<tr class="odd">
<td><p><strong>Ouderdom vanaf</strong></p></td>
<td><p>Voer de datum in die wordt gebruikt in de huidige ouderdomsperiode.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Saldo per</strong></p></td>
<td><p>Voer de datum in waarvoor de klantsaldi moeten worden weergegeven. Deze datum staat ook bekend als de afsluitdatum voor transacties.</p></td>
</tr>
<tr class="even">
<td><p><strong>Begindatum</strong></p></td>
<td><p>Voer een datum in die binnen het eerste periode-interval of de ouderdomsperiode valt die in het rapport moet worden opgenomen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Criteria</strong></p></td>
<td><p>Selecteer het type datum waarop u het rapport wilt baseren.</p>
<ul>
<li><p><strong>Transactiedatum</strong>: de boekingsdatum van de transacties. Dit kan bijvoorbeeld een factuurdatum zijn die de basis vormt voor de berekening van de vervaldatum.</p></li>
<li><p><strong>Vervaldatum</strong>: de vervaldatum van de transacties die is gebaseerd op de betalingsvoorwaarden.</p></li>
<li><p><strong>Documentdatum</strong>: een datum van het door de gebruiker gedefinieerde document, die wordt gebruikt als basis voor het berekenen van de vervaldatum.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Definitie van ouderdomsperiode</strong></p></td>
<td><p>Selecteer een ouderdomsperiodedefinitie. Het veld <strong>Interval</strong> wordt niet gebruikt als u een ouderdomsperiodedefinitie selecteert.</p>
<p>Ouderdomsperiodedefinities met meer dan zes ouderdomsperioden kunnen niet worden gebruikt in het afgedrukte rapport.</p>
<div class="alert">

**Opmerking**: u kunt ouderdomsperioden instellen op de pagina <STRONG>Ouderdomsperiodedefinities</STRONG>.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Omschrijving van ouderdomsperiode afdrukken</strong></p></td>
<td><p>Selecteer <strong>Ja</strong> om omschrijvingen van ouderdomsperioden boven aan elke ouderdomsperiodekolom in het rapport op te nemen. Selecteer <strong>Nee</strong> om het rapport zonder kolomkoppen af te drukken.</p></td>
</tr>
<tr class="even">
<td><p><strong>Interval</strong></p></td>
<td><p>Definieer de gewenste periode door het aantal dag- of maandeenheden in elke periode in te voeren. On bijvoorbeeld de naar ouderdom gerangschikte informatie per week te bekijken, voert u een 7 in dit veld in en selecteert u <strong>Dag</strong> in het veld <strong>Dag/maand</strong>.</p>
<div class="alert">

**Opmerking:** de informatie die u in dit veld invoert, wordt alleen gebruikt als u geen ouderdomsperiodedefinitie hebt geselecteerd. Anders wordt de afdrukrichting gedefinieerd in de ouderdomsperiodedefinitie.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Dag/mnd.</strong></p></td>
<td><p>Selecteer de eenheid, <strong>Dag</strong> of <strong>Maand</strong>, waarmee de periode wordt gedefinieerd in het veld <strong>Interval</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Afdrukrichting</strong></p></td>
<td><p>Geef aan of saldi moeten worden berekend en het naar ouderdom gerangschikte rapport moet worden afgedrukt voor perioden in het verleden of in de toekomst. De datums zijn relatief ten opzichte van de datum die in het veld <strong>Saldo vanaf</strong> is geselecteerd. Selecteer <strong>Achterwaarts</strong> om informatie voor perioden in het verleden weer te geven. Selecteer <strong>Voorwaarts</strong> om informatie voor perioden in de toekomst weer te geven.</p>
<div class="alert">
  
<STRONG>Opmerking:</STRONG> de informatie die u in dit veld invoert, wordt alleen gebruikt als u geen ouderdomsperiodedefinitie hebt geselecteerd.</P>


</div></td>
</tr>
<tr class="odd">
<td><p><strong>Gegevens</strong></p></td>
<td><p>Selecteer deze optie om transacties weer te geven die zijn opgenomen in de saldi die in het rapport worden weergegeven.</p></td>
</tr>
<tr class="even">
<td><p><strong>Bedragen in transactievaluta opnemen</strong></p></td>
<td><p>Selecteer deze optie om bedragen in de transactievaluta op te nemen naast bedragen in de valuta voor boekhouding. Als dit selectievakje niet is ingeschakeld, worden de bedragen in het rapport alleen in de valuta voor boekhouding weergegeven.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Negatief saldo</strong></p></td>
<td><p>Selecteer deze optie om klantrekeningen met negatieve saldi op te nemen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Rekeningen met nulsaldo uitsluiten</strong></p></td>
<td><p>Selecteer deze optie om klantrekeningen met een nulsaldo uit te sluiten.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Betalingspositionering</strong></p></td>
<td><p>Selecteer deze optie om betalingen weer te geven die niet zijn vereffend. Deze worden in de eerste kolom van het rapport weergegeven.</p></td>
</tr>
</tbody>
</table>

