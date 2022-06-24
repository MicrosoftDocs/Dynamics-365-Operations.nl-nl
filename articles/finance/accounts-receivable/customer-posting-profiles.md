---
title: Boekingsprofielen van klant
description: Dit artikel beschrijft klantboekingsprofielen die de boeking van klanttransacties naar het grootboek regelen.
author: JodiChristiansen
ms.date: 12/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustVendExternalItem
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0563040590eefab57706b183281c47a82e46076
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891690"
---
# <a name="customer-posting-profiles"></a>Boekingsprofielen van klant

[!include [banner](../includes/banner.md)]

Dit artikel beschrijft klantboekingsprofielen die de boeking van klanttransacties naar het grootboek regelen.

## <a name="customer-posting-profiles"></a>Boekingsprofielen van klant

Met boekingsprofielen van klanten kunt u grootboekrekeningen en documentinstellingen aan alle klanten, een groep klanten of één klant toewijzen. Deze instellingen worden gebruikt als u verkooporders, facturen, vrije-tekstfacturen, projectfacturen, betalingsjournalen, aanmaningen en rentenota's maakt. 

Het standaardboekingsprofiel wordt gedefinieerd op het tabblad **Grootboek en btw** van de pagina **Parameters van module Klanten**. Het wordt dan automatisch opgenomen in de header van nieuwe documenten. U kunt het daar wijzigen als een ander boekingsprofiel is vereist. 

Organisaties die vooruitbetalingen van klanten accepteren, configureren vaak een tweede boekingsprofiel voor vooruitbetalingen en koppelen dit in de parameters als standaardboekingsprofiel voor vooruitbetalingen. Zie [Vooruitbetalingen door klanten](customer-prepayments.md) voor meer informatie.

Op de pagina **Boekdefinities voor transacties** kunt u boekingsdefinities ook aan transactieboekingstypen koppelen. Boekingsdefinities worden gebruikt in plaats van boekingsprofielen om de boeking van klanttransacties naar het grootboek te regelen. Zie voor meer informatie [Boekingsdefinities](../general-ledger/posting-definitions.md).

## <a name="creating-a-posting-profile"></a>Een boekingsprofiel maken
De grootboekrekeningen opgeven die bij het boeken van transacties met het geselecteerde boekingsprofiel worden gebruikt. Een rekeningcode en, voor zover mogelijk, een rekening of groep voor het geselecteerde boekingsprofiel selecteren. In het boekingsproces wordt het meest passende boekingsprofiel voor elke transactie gevonden door te zoeken naar de meest specifieke combinatie van rekeningcode, rekeningnummer of groepsnummer met de volgende prioriteit:

| De veldwaarde Rekeningcode | De veldwaarde Rekening/groepsnummer                | Zoekprioriteit |
|--------------------------|-------------------------------------------------|-----------------|
| Tabel                    | Specifieke klantenrekening                       | 1               |
| Groep                    | Klantengroep die is toegewezen aan de klant | 2               |
| Alle                      | Leeg                                           | 3               |

Als u wilt dat alle klanttransacties hetzelfde boekingsprofiel hebben, stelt u slechts één boekingsprofiel in waarbij **Alle** in het veld **Rekeningcode** wordt ingevoerd. Geef de volgende waarden op om uw boekingsprofiel in te stellen:

<table>
<thead>
<tr>
<th>Veld</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr>
<td>Boekingsprofiel</td>
<td>Een code invoeren voor het boekingsprofiel. U kunt bijvoorbeeld twee boekingsprofielen maken om één rekening te krijgen voor klantsaldi in de nationale valuta en een andere rekening voor klantsaldi in een vreemde valuta. U zou dan de ene rekening Nationaal kunnen noemen en de andere Internationaal.</td>
</tr>
<tr>
<td>Description</td>
<td>Een omschrijving van het boekingsprofiel invoeren. Dit wordt alleen gebruikt om het boekingsprofiel beter te identificeren wanneer u het op deze pagina weergeeft.</td>
</tr>
<tr>
<td>Rekeningcode</td>
<td>Opgeven of het boekingsprofiel van toepassing is op één klant, een groep klanten of op alle klanten:
<ul>
<li><b>Tabel</b>: het boekingsprofiel is van toepassing op een enkele klant. Selecteer de klantrekening in het veld <b>Rekening/groepsnummer</b>.</li>
<li><b>Groep</b>: het boekingsprofiel is van toepassing op een klantgroep. Selecteer de klantgroep in het veld <b>Rekening/groepsnummer</b>.</li>
<li><b>Alle</b>: het boekingsprofiel is van toepassing op alle klanten. Laat het veld <b>Rekening/groepsnummer</b> leeg.</li>
</ul>
</td>
</tr>
<tr>
<td>Rekening/groepsnummer</td>
<td>Als <b>Tabel</b> is geselecteerd in het veld <b>Rekeningcode</b>, selecteert u het rekeningnummer van de klant die aan het boekingsprofiel is gekoppeld. Selecteer de klantengroep als <b>Groep</b> is geselecteerd. Als <b>Alle</b> is geselecteerd, laat u dit veld leeg.</td>
</tr>
<tr>
<td>Totaalrekening</td>
<td>Selecteer de hoofdrekening die wordt gebruikt als de handelsrekening voor klanten die aan het boekingsprofiel zijn gekoppeld. Deze rekening is de rekening voor het boekingstype <b>Klantsaldo</b>.</td>
</tr>
<tr>
<td>Liquiditeitsrekening voor betalingen</td>
<td>De liquiditeitsgrootboekrekening selecteren die wordt gebruikt voor cashflowprognoses. Dit veld wordt alleen weergegeven als cashflowprognoses zijn ingeschakeld.</td>
</tr>
<tr>
<td>Btw-vooruitbetalingen</td>
<td><p>De rekening selecteren voor btw op ontvangen vooruitbetalingen.</p>
<p><strong>Opmerking:</strong> Gebruik de pagina <b>Parameters van module Klanten</b> om het boekingsprofiel op te geven dat wordt gebruikt wanneer een betaling is gemarkeerd als een vooruitbetaling.</p>
</td>
</tr>
<tr>
<td>Verplichtingen voor discontorekening</td>
<td>De grootboekrekening voor verplichtingen voor disconto selecteren.</td>
</tr>
<tr>
<td>Aanmaningsreeks</td>
<td>De identificatie selecteren van de aanmaningsreeks die wordt gebruikt voor klanten waaraan het boekingsprofiel is toegewezen.</td>
</tr>
<tr>
<td>Rentecode</td>
<td>De rentecode selecteren die u wilt gebruiken voor de berekening van rente voor klanten aan wie het boekingsprofiel is toegewezen.</td>
</tr>
</tbody>
</table>

## <a name="posting-examples"></a>Voorbeelden van boekingen

In de volgende tabel ziet u voorbeelden van de standaardboekingstypen met voorbeeldhoofdrekeningen en omschrijvingen. De kolom **Debet/Credit** geeft aan of de transactie meestal debet of credit is of in sommige gevallen ook een kan worden geboekt. De kolom **Vereffeningsrekening** geeft aan of het boekingstype een vereffeningsrekening is. Dit betekent dat het bedrag dat in deze rekening wordt geboekt, automatisch wordt teruggeboekt wanneer een latere transactie wordt geboekt. 

| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit | Vereffeningsrekening | Description |
|--------------|----------------------|---------------------------|--------------|--------------|------------------|-------------|
| Klantsaldo | 130100 | Handel klanten | Activum | Beide | Nee | Geef in het veld **Totaalrekening** de rekening op.|
| Geen | 110110 | Bankrekening | Activum | Beide | Nee | Geef de hoofdrekening op in het veld **Liquiditeitsrekening voor betalingen**. Deze rekening wordt niet gebruikt voor boeking. Deze wordt alleen gebruikt voor cashflowprognoses. |
| Btw-vooruitbetalingen | 202900 | Btw-vereffening | Aansprakelijkheid | Beide | Ja | De rekening selecteren voor btw op ontvangen vooruitbetalingen. |
| Verplichtingen voor discontorekening | 250600 | Uitgestelde opbrengst en kortingen | Aansprakelijkheid | Beide | Ja | De grootboekrekening voor verplichtingen voor kortingen selecteren.|     

### <a name="table-restrictions"></a>Tabelbeperkingen

Voor transacties met het geselecteerde boekingsprofiel geeft u op of transacties automatisch worden vereffend, rente wordt berekend en aanmaningen worden uitgegeven. U kunt ook de rekening selecteren die wordt gebruikt wanneer transacties met het geselecteerde boekingsprofiel worden afgesloten.

Geef de volgende waarden op om uw boekingsprofiel in te stellen:

| Veld                 | Beschrijving                                           |
|-----------------------|-------------------------------------------------------|
| Vereffening        | Selecteer deze schakeloptie om de automatische vereffening in te schakelen van transacties die dit boekingsprofiel hebben. Als deze schakeloptie niet is geselecteerd, moet u transacties handmatig op de pagina **Openstaande transacties vereffenen** of **Klantbetalingen invoeren** vereffenen. |
| Interesse          | Selecteer deze schakeloptie als rente moet worden berekend over openstaande saldi voor klantrekeningen die dit profiel gebruiken. Als deze schakeloptie niet is geselecteerd, wordt voor deze klanten geen rente berekend.                                           |
| Aanmaning | Selecteer deze schakeloptie als aanmaningen moeten worden gegenereerd voor klantrekeningen die dit profiel gebruiken. Als deze schakeloptie niet is geselecteerd, worden voor deze klanten geen aanmaningen gegenereerd.                                                 |
| Sluiten             | Selecteer een boekingsprofiel om naar over te gaan als transacties met dit boekingsprofiel gesloten zijn. Een transactie wordt als afgesloten beschouwd als deze volledig is vereffend.             |



Zie [Overzicht van klantbetalingen](../cash-bank-management/tasks/customer-payment-overview.md) voor meer informatie.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
