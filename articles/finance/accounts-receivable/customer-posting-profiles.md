---
title: Boekingsprofielen van klant
description: Met klantprofielen wordt de boeking van klanttransacties naar het grootboek beheerd.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1bb2784d70e99c3c3443bed1b8cb040552b5b6f6
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189057"
---
# <a name="customer-posting-profiles"></a>Boekingsprofielen van klant

[!include [banner](../includes/banner.md)]

Met klantprofielen wordt de boeking van klanttransacties naar het grootboek beheerd.

<a name="customer-posting-profiles"></a>Boekingsprofielen van klant
-------------------------

Met boekingsprofielen van klanten kunt u grootboekrekeningen en documentinstellingen aan alle klanten, een groep klanten of één klant toewijzen. Deze instellingen worden gebruikt als u verkooporders, vrije-tekstfacturen, contante betalingen, aanmaningen en rentenota's maakt. Voor sommige transacties kunt u een boekingsprofiel selecteren dat afwijkt van en voorrang heeft op de boekingsprofielen die zijn ingesteld voor transacties op deze pagina. 

Het standaardboekingsprofiel wordt gedefinieerd op het sneltabblad Grootboek en btw op de pagina Parameters van module Klanten. Het standaardboekingsprofiel wordt vervolgens automatisch opgenomen in de koptekst van nieuwe documenten waarin u het vervolgens in een ander boekingsprofiel kunt wijzigen, indien nodig.

Op de pagina Boekdefinities voor transacties kunt u boekingsdefinities ook aan transactieboekingstypen koppelen. Boekingsdefinities regelen de boeking van klanttransacties naar het grootboek in plaats van boekingsprofielen.

## <a name="creating-a-posting-profile"></a>Een boekingsprofiel maken
De grootboekrekeningen opgeven die bij het boeken van transacties met het geselecteerde boekingsprofiel worden gebruikt. Een rekeningcode en, voor zover mogelijk, een rekening of groep voor het geselecteerde boekingsprofiel selecteren. In het boekingsproces wordt het meest passende boekingsprofiel voor elke transactie gevonden door te zoeken naar de meest specifieke combinatie van rekeningcode, rekeningnummer of groepsnummer met de volgende prioriteit:

| De veldwaarde **Rekeningcode** | De veldwaarde **Rekening/groepsnummer**            | Zoekprioriteit |
|------------------------------|-------------------------------------------------|-----------------|
| **Tabel**                    | Specifieke klantenrekening                       | 1               |
| **Groep**                    | Klantengroep die is toegewezen aan de klant | 2               |
| **Alle**                      | Leeg                                           | 3               |

Als u wilt dat alle klanttransacties hetzelfde boekingsprofiel hebben, stelt u slechts één boekingsprofiel in met de optie Alle in het veld Rekeningcode. Geef de volgende waarden op om uw boekingsprofiel in te stellen:

<table>
<thead>
<tr class="header">
<th>Veld</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Boekingsprofiel</strong></td>
<td>Een code invoeren voor het boekingsprofiel. U kunt bijvoorbeeld twee boekingsprofielen maken om één rekening te krijgen voor klantsaldi in de nationale valuta en een andere rekening voor klantsaldi in een vreemde valuta. U zou dan de ene rekening Nationaal kunnen noemen en de andere Internationaal.</td>
</tr>
<tr class="even">
<td><strong>Omschrijving</strong></td>
<td>Een omschrijving van het boekingsprofiel invoeren. Dit wordt alleen gebruikt om het boekingsprofiel beter te identificeren wanneer u het op deze pagina weergeeft.</td>
</tr>
<tr class="odd">
<td><strong>Rekeningcode</strong></td>
<td>Opgeven of het boekingsprofiel van toepassing is op één klant, een groep klanten of op alle klanten:
<ul>
<li><strong>Tabel</strong>: het boekingsprofiel is van toepassing op een enkele klant. Selecteer de klantrekening in het veld Rekening/groepsnummer.</li>
<li><strong>Groep</strong>: het boekingsprofiel is van toepassing op een klantgroep. Selecteer de klantgroep in het veld Rekening/groepsnummer.</li>
<li><strong>Alle</strong>: het boekingsprofiel is van toepassing op alle klanten. Laat het veld Rekening/groepsnummer leeg.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Rekening/groepsnummer</strong></td>
<td>Als Tabel is geselecteerd in het veld Rekeningcode, selecteert u het rekeningnummer van de klant die aan het boekingsprofiel is gekoppeld. Selecteer de klantengroep als Groep is geselecteerd. Als Alle is geselecteerd, laat u dit veld leeg.</td>
</tr>
<tr class="odd">
<td><strong>Totaalrekening</strong></td>
<td>De grootboekrekening selecteren die wordt gebruikt als de klantoverzichtsrekening voor klanten die aan het boekingsprofiel zijn gekoppeld.</td>
</tr>
<tr class="even">
<td><strong>Rekening vereffenen</strong></td>
<td>De liquiditeitsgrootboekrekening selecteren die wordt gebruikt voor cashflowprognoses. Dit veld wordt alleen weergegeven als cashflowprognoses zijn ingeschakeld.</td>
</tr>
<tr class="odd">
<td><strong>Btw-vooruitbetalingen</strong></td>
<td>De rekening selecteren voor btw op ontvangen vooruitbetalingen.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Opmerking" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Opmerking</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gebruik de pagina Parameters van module Klanten om het boekingsprofiel op te geven dat u wilt gebruiken wanneer een betaling is gemarkeerd als een vooruitbetaling.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Aansprakelijkheden voor discontorekening</strong></td>
<td>De grootboekrekening voor verplichtingen voor disconto selecteren.</td>
</tr>
<tr class="odd">
<td><strong>Aanmaningsreeks</strong></td>
<td>De identificatie selecteren van de aanmaningsreeks die wordt gebruikt voor klanten waaraan het boekingsprofiel is toegewezen.</td>
</tr>
<tr class="even">
<td><strong>Rentecode</strong></td>
<td>De rentecode selecteren die u wilt gebruiken voor de berekening van rente voor klanten aan wie het boekingsprofiel is toegewezen.</td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a>**Tabelbeperkingen**

Voor transacties met het geselecteerde boekingsprofiel geeft u op of transacties automatisch worden vereffend, rente wordt berekend en aanmaningen worden uitgegeven. U kunt ook de rekening selecteren die wordt gebruikt wanneer transacties met het geselecteerde boekingsprofiel worden afgesloten.

Geef de volgende waarden op om uw boekingsprofiel in te stellen:

| Veld                 | Beschrijving                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vereffening**        | Selecteer deze schakeloptie om de automatische vereffening in te schakelen van transacties die dit boekingsprofiel hebben. Als deze schakeloptie niet is geselecteerd, moet u transacties handmatig op de pagina Openstaande transacties vereffenen of Klantbetalingen invoeren. |
| **Interesse**          | Selecteer deze schakeloptie als rente moet worden berekend over openstaande saldi voor klantrekeningen die dit profiel gebruiken. Als deze schakeloptie niet is geselecteerd, wordt voor deze klanten geen rente berekend.                                           |
| **Aanmaning** | Selecteer deze schakeloptie als aanmaningen moeten worden gegenereerd voor klantrekeningen die dit profiel gebruiken. Als deze schakeloptie niet is geselecteerd, worden voor deze klanten geen aanmaningen gegenereerd.                                                 |
| **Sluiten**             | Selecteer een boekingsprofiel om naar over te gaan als transacties met dit boekingsprofiel gesloten zijn. Een transactie wordt als afgesloten beschouwd als deze volledig is vereffend.                                                                           |



Zie [Overzicht van klantbetalingen](../cash-bank-management/tasks/customer-payment-overview.md) voor meer informatie.

