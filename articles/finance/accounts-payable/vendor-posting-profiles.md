---
title: Boekingsprofielen van leverancier
description: Met boekingsprofielen van leveranciers worden boekingen van leverancierstransacties naar het grootboek beheerd.
author: abruer
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43450c5f7ab8295b896b591880da9d0bddd955cf
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441795"
---
# <a name="vendor-posting-profiles"></a>Boekingsprofielen van leverancier

[!include [banner](../includes/banner.md)]

Met boekingsprofielen van leveranciers worden boekingen van leverancierstransacties naar het grootboek beheerd.

<a name="vendor-posting-profiles"></a>Boekingsprofielen van leverancier
-----------------------

Met boekingsprofielen van leveranciers kunt u grootboekrekeningen en documentinstellingen aan alle leveranciers, een groep leveranciers of één leverancier toewijzen. Deze instellingen worden gebruikt wanneer u inkooporders, leveranciersfacturen en contante betalingen maakt. Voor sommige transacties kunt u een boekingsprofiel selecteren dat afwijkt van en voorrang heeft op de boekingsprofielen die zijn ingesteld voor transacties op deze pagina. Het standaardboekingsprofiel wordt gedefinieerd op het sneltabblad **Grootboek en btw** op de pagina **Parameters van module Leveranciers**. Het standaardboekingsprofiel wordt vervolgens automatisch opgenomen in de koptekst van nieuwe documenten waarin u het vervolgens in een ander boekingsprofiel kunt wijzigen, indien nodig.

Op de pagina **Boekdefinities voor transacties** kunt u boekingsdefinities ook aan transactieboekingstypen koppelen. Boekingsdefinities regelen de boeking van leverancierstransacties naar het grootboek in plaats van boekingsprofielen.

## <a name="creating-a-posting-profile"></a>Een boekingsprofiel maken
### <a name="setup"></a>**Instellingen**

De grootboekrekeningen opgeven die bij het boeken van transacties met het geselecteerde boekingsprofiel worden gebruikt. Een rekeningcode en, voor zover mogelijk, een rekening of groep voor het geselecteerde boekingsprofiel selecteren. In het boekingsproces wordt het meest passende boekingsprofiel voor elke transactie gevonden door te zoeken naar de meest specifieke combinatie van rekeningcode, rekeningnummer of groepsnummer met de volgende prioriteit:

| De veldwaarde **Rekeningcode** | De veldwaarde **Rekening/groepsnummer**        | Zoekprioriteit |
|------------------------------|---------------------------------------------|-----------------|
| **Tabel**                    | Specifieke leveranciersrekening                     | 1               |
| **Groep**                    | Leveranciersgroep die aan de leverancier is toegewezen | 2               |
| **Alle**                      | Leeg                                       | 3               |

Als u wilt dat alle leverancierstransacties hetzelfde boekingsprofiel hebben, stelt u slechts één boekingsprofiel in met de optie **Alle** in het veld **Rekeningcode**. Geef de volgende waarden op om uw boekingsprofiel in te stellen:

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
<li><strong>Tabel</strong>: het boekingsprofiel is van toepassing op een enkele leverancier. Selecteer de leverancier in het veld <strong>Rekening/groepsnummer</strong>.</li>
<li><strong>Groep</strong>: het boekingsprofiel is van toepassing op een leveranciersgroep. Selecteer de leveranciersgroep in het veld <strong>Rekening/groepsnummer</strong>.</li>
<li><strong>Alle</strong>: het boekingsprofiel is van toepassing op alle leveranciers. Laat het veld <strong>Rekening/groepsnummer</strong> leeg.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Rekening/groepsnummer</strong></td>
<td>Als <strong>Tabel</strong> is geselecteerd in het veld <strong>Rekeningcode</strong>, selecteert u het rekeningnummer van de leverancier die aan het boekingsprofiel is gekoppeld. Als <strong>Groep</strong> is geselecteerd, selecteert u een leveranciersgroep. Als <strong>Alle</strong> is geselecteerd, laat u dit veld leeg.</td>
</tr>
<tr class="odd">
<td><strong>Totaalrekening</strong></td>
<td>Selecteer de grootboekrekening die gebruikt wordt als overzichtsrekening voor de leveranciers waarnaar het boekingsprofiel verwijst. De parameter <strong>Handmatige invoer niet toestaan</strong> voor deze hoofdrekening wordt gemarkeerd. Als u deze rekening vervolgens uit het boekingsprofiel verwijdert, moet u de instelling <strong>Handmatige invoer niet toestaan</strong> op de pagina <strong>Hoofdrekeningen</strong> valideren. 
<p><strong>Opmerking:</strong> als de optie <strong>Boekdefinities gebruiken</strong> is geselecteerd op de pagina <strong>Grootboekparameters</strong>, wordt de transactieboekingsdefinitie voor leveranciersfacturen gebruikt in plaats van de overzichtsrekening.</p>
</td>
</tr>
<tr class="even">
<td><strong>Rekening vereffenen</strong></td>
<td>De liquiditeitsgrootboekrekening selecteren die wordt gebruikt voor cashflowprognoses. Deze velden zijn alleen beschikbaar als cashflowprognoses zijn ingeschakeld.</td>
</tr>
<tr class="odd">
<td><strong>Btw-vooruitbetalingen</strong></td>
<td>Selecteer de rekening voor btw-betalingen die vooruit ontvangen zijn.
<p><strong>Opmerking:</strong> het boekingsprofiel dat wordt gebruikt wanneer de betaling is gemarkeerd als een vooruitbetaling is geselecteerd in het veld <strong>Boekingsprofiel</strong> met <strong>journaalboekstuk van vooruitbetaling</strong> in het gedeelte <strong>Grootboek en btw</strong> van de pagina <strong>Parameters van module Leveranciers</strong>.</p>
</td>
</tr>
<tr class="even">
<td><strong>Ontvangst</strong></td>
<td>Selecteer de grootboekrekening waarnaar informatie over niet-goedgekeurde leveranciersfacturen geboekt wordt. De informatie wordt ingevoerd in het facturenregisterjournaal. Een gebruiker voert bijvoorbeeld heel beperkte gegevens in over leveranciersfacturen als ze in het facturenregister worden ontvangen. Als het facturenregister wordt geboekt, worden de transacties geboekt naar de rekening die hier en in het veld <strong>Tegenrekening</strong> is ingevoerd. Als de facturen worden goedgekeurd, wordt de schuld overgeboekt van de ontvangstrekening naar de totaalrekening voor de leverancier.</td>
</tr>
<tr class="odd">
<td><strong>Tegenrekening</strong></td>
<td>Selecteer de grootboekrekening die gebruikt wordt voor het tegenboeken van niet-goedgekeurde leveranciersfacturen die bijgewerkt worden met het facturenregister. De tegenrekening fungeert als tegenrekening voor transacties die geboekt worden op binnenkomstrekeningen. Daarom bevat de rekening leveranciersaankopen die nog niet zijn goedgekeurd.</td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a>**Tabelbeperkingen**

Voor transacties met het geselecteerde boekingsprofiel geeft u op of transacties automatisch worden vereffend, rente wordt berekend en aanmaningen worden uitgegeven. U kunt ook de rekening selecteren die wordt gebruikt wanneer transacties met het geselecteerde boekingsprofiel worden afgesloten.

Geef de volgende waarden op om uw boekingsprofiel in te stellen

| Veld          | Beschrijving                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Vereffening** | Selecteer deze optie om automatische vereffening in te schakelen van transacties die dit boekingsprofiel hebben. Als deze optie niet is geselecteerd, moet u transacties handmatig vereffenen via de pagina **Openstaande transacties vereffenen**. |
| **Annuleren**     | Selecteer deze optie als u transacties met dit boekingsprofiel wilt kunnen annuleren.                                                                                                               |
| **Sluiten**      | Selecteer een boekingsprofiel om naar over te gaan als transacties met dit boekingsprofiel gesloten zijn. Een transactie wordt als afgesloten beschouwd als deze volledig is vereffend.                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]