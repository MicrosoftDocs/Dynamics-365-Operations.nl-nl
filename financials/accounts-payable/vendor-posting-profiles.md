---
title: Boekingsprofielen van leverancier
description: Met boekingsprofielen van leveranciers worden boekingen van leverancierstransacties naar het grootboek beheerd.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 926ee087a0e0c4743f29315b1d82c7d37e95be28
ms.openlocfilehash: 76defe4dcb187ca948344ab9131eae981cbace3f
ms.lasthandoff: 03/31/2017


---

# <a name="vendor-posting-profiles"></a>Boekingsprofielen van leverancier

[!include[banner](../includes/banner.md)]


Met boekingsprofielen van leveranciers worden boekingen van leverancierstransacties naar het grootboek beheerd.

<a name="vendor-posting-profiles"></a>Boekingsprofielen van leverancier
-----------------------

Met boekingsprofielen van leveranciers kunt u grootboekrekeningen en documentinstellingen aan alle leveranciers, een groep leveranciers of één leverancier toewijzen. Deze instellingen worden gebruikt wanneer u inkooporders, leveranciersfacturen en contante betalingen maakt. Voor sommige transacties kunt u een boekingsprofiel selecteren dat afwijkt van en voorrang heeft op de boekingsprofielen die zijn ingesteld voor transacties op deze pagina. Het standaardboekingsprofiel wordt gedefinieerd op het sneltabblad Grootboek en btw op de pagina Parameters van module Leveranciers. Het standaardboekingsprofiel wordt vervolgens automatisch opgenomen in de koptekst van nieuwe documenten waarin u het vervolgens in een ander boekingsprofiel kunt wijzigen, indien nodig.

Op de pagina Boekdefinities voor transacties kunt u boekingsdefinities ook aan transactieboekingstypen koppelen. Boekingsdefinities regelen de boeking van leverancierstransacties naar het grootboek in plaats van boekingsprofielen.

## <a name="creating-a-posting-profile"></a>Een boekingsprofiel maken
### <a name="setup"></a>**Instellingen**

De grootboekrekeningen opgeven die bij het boeken van transacties met het geselecteerde boekingsprofiel worden gebruikt. Een rekeningcode en, voor zover mogelijk, een rekening of groep voor het geselecteerde boekingsprofiel selecteren. In het boekingsproces wordt het meest passende boekingsprofiel voor elke transactie gevonden door te zoeken naar de meest specifieke combinatie van rekeningcode, rekeningnummer of groepsnummer met de volgende prioriteit:

| De veldwaarde **Rekeningcode** | De veldwaarde **Rekening/groepsnummer**        | Zoekprioriteit |
|------------------------------|---------------------------------------------|-----------------|
| **Tabel**                    | Specifieke leveranciersrekening                     | 1               |
| **Groep**                    | leveranciersgroep die aan de leverancier is toegewezen | 2               |
| **Alle**                      | Leeg                                       | 3               |

Als u wilt dat alle leverancierstransacties hetzelfde boekingsprofiel hebben, stelt u slechts één boekingsprofiel in met de optie Alle in het veld Rekeningcode. Geef de volgende waarden op om uw boekingsprofiel in te stellen:

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Veld</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Boekingsprofiel</strong></td>
<td>Een code invoeren voor het boekingsprofiel. U kunt bijvoorbeeld twee boekingsprofielen maken om een rekening voor leverancierssaldi in de nationale valuta te verkrijgen en een andere voor leveranciersaldi in een vreemde valuta. U zou dan de ene rekening Nationaal kunnen noemen en de andere Internationaal.</td>
</tr>
<tr class="even">
<td><strong>Omschrijving</strong></td>
<td>Een omschrijving van het boekingsprofiel invoeren.</td>
</tr>
<tr class="odd">
<td><strong>Rekeningcode</strong></td>
<td>Opgeven of het boekingsprofiel van toepassing is op een specifieke leverancier, een groep leveranciers of alle leveranciers:
<ul>
<li><strong>Tabel</strong>: het boekingsprofiel is van toepassing op een enkele leverancier. Selecteer de leverancier in het veld Rekening/groepsnummer.</li>
<li><strong>Groep</strong>: het boekingsprofiel is van toepassing op een leveranciersgroep. Selecteer de leveranciersgroep in het veld Rekening/groepsnummer.</li>
<li><strong>Alle</strong>: het boekingsprofiel is van toepassing op alle leveranciers. Laat het veld Rekening/groepsnummer leeg.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Rekening/groepsnummer</strong></td>
<td>Als Tabel is geselecteerd in het veld Rekeningcode, selecteert u het rekeningnummer van de leverancier die aan het boekingsprofiel is gekoppeld. Als Groep is geselecteerd, selecteert u een leveranciersgroep. Als Alle is geselecteerd, laat u dit veld leeg.</td>
</tr>
<tr class="odd">
<td><strong>Totaalrekening</strong></td>
<td>Selecteer de grootboekrekening die gebruikt wordt als overzichtsrekening voor de leveranciers waarnaar het boekingsprofiel verwijst.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Opmerking</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Als de schakeloptie Boekdefinities gebruiken is geselecteerd op de pagina Grootboekparameters, wordt de transactieboekingsdefinitie voor leveranciersfacturen gebruikt in plaats van de overzichtsrekening.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Rekening vereffenen</strong></td>
<td>De liquiditeitsgrootboekrekening selecteren die wordt gebruikt voor cashflowprognoses. Deze velden zijn alleen beschikbaar als cashflowprognoses zijn ingeschakeld.</td>
</tr>
<tr class="odd">
<td><strong>Btw-vooruitbetalingen</strong></td>
<td>Selecteer de rekening voor btw-betalingen die vooruit ontvangen zijn.
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note" alt="Note" id="alert_note" class="cl_IC101471" /><strong>Opmerking</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Het boekingsprofiel dat wordt gebruikt wanneer de betaling is gemarkeerd als een vooruitbetaling is geselecteerd in het veld Boekingsprofiel met journaalboekstuk van vooruitbetaling in het gedeelte Grootboek en btw van de pagina Parameters van module Leveranciers.</td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><strong>Ontvangst</strong></td>
<td>Selecteer de grootboekrekening waarnaar informatie over niet-goedgekeurde leveranciersfacturen geboekt wordt. De informatie wordt ingevoerd in het facturenregisterjournaal. Een gebruiker voert bijvoorbeeld heel beperkte gegevens in over leveranciersfacturen als ze in het facturenregister worden ontvangen. Als het facturenregister wordt geboekt, worden de transacties geboekt naar de rekening die hier en in het veld Tegenrekening is ingevoerd. Als de facturen worden goedgekeurd, wordt de schuld overgeboekt van de ontvangstrekening naar de totaalrekening voor de leverancier.</td>
</tr>
<tr class="odd">
<td><strong>Tegenrekening</strong></td>
<td>Selecteer de grootboekrekening die gebruikt wordt voor het tegenboeken van niet-goedgekeurde leveranciersfacturen die bijgewerkt worden met het facturenregister. De tegenrekening fungeert als tegenrekening voor transacties die geboekt worden op binnenkomstrekeningen. Daarom bevat de rekening leveranciersaankopen die nog niet zijn goedgekeurd.</td>
</tr>
</tbody>
</table>
 

### <a name="table-restrictions"></a>**Tabelbeperkingen**

Voor transacties met het geselecteerde boekingsprofiel geeft u op of transacties automatisch worden vereffend, rente wordt berekend en aanmaningen worden uitgegeven. U kunt ook de rekening selecteren die wordt gebruikt wanneer transacties met het geselecteerde boekingsprofiel worden afgesloten.

Geef de volgende waarden op om uw boekingsprofiel in te stellen:

| Veld          | Beschrijving                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vereffening** | Selecteer deze optie om automatische vereffening in te schakelen van transacties die dit boekingsprofiel hebben. Als deze optie niet is geselecteerd, moet u transacties handmatig vereffenen via de pagina Openstaande transacties vereffenen. |
| **Annuleren**     | Selecteer deze optie als u transacties met dit boekingsprofiel wilt kunnen annuleren.                                                                                                               |
| **Sluiten**      | Selecteer een boekingsprofiel om naar over te gaan als transacties met dit boekingsprofiel gesloten zijn. Een transactie wordt als afgesloten beschouwd als deze volledig is vereffend.                                       |






