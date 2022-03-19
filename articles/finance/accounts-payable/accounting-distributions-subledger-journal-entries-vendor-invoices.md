---
title: Boekhoudingsverdelingen en journaalposten voor leveranciersfacturen
description: Boekhoudingsverdelingen worden gebruikt om te bepalen hoe een bedrag zal worden verwerkt, zoals hoe de onkosten, BTW of heffingen zullen worden verwerkt op een leveranciersfactuur. Elk bedrag dat moet worden verwerkt wanneer de leveranciersfactuur in het boekhoudingsjournaal wordt vastgelegd, heeft een of meerdere boekhoudingsverdelingen.
author: sunfzam
ms.date: 02/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f10ddf113f59da4800a97a48300ab1310bfb42dd
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358176"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Boekhoudingsverdelingen en journaalposten voor leveranciersfacturen

[!include [banner](../includes/banner.md)]

Boekhoudingsverdelingen worden gebruikt om te bepalen hoe een bedrag zal worden verwerkt, zoals hoe de onkosten, BTW of heffingen zullen worden verwerkt op een leveranciersfactuur. Elk bedrag dat moet worden verwerkt wanneer de leveranciersfactuur in het boekhoudingsjournaal wordt vastgelegd, heeft een of meerdere boekhoudingsverdelingen. 

## <a name="accounting-distributions"></a>Boekhoudingsverdelingen 

U kunt de volgende knoppen op de pagina Leveranciersfactuur gebruiken voor het weergeven en mogelijk wijzigen van de boekhoudingsverdelingen voor elk bedrag op de leveranciersfactuur.
-   **Bedragen verdelen** – De boekhoudingsverdelingen weergeven en wijzigen voor een afzonderlijke regel en alle onderliggende regels, zoals belastingen of heffingen. U kunt de boekhoudingsverdeling voor de onderliggende regel rechtstreeks weergeven en wijzigen op de pagina **Btw-transacties** of de pagina **Transacties met toeslagen**.
    -   Bedragen in de koptekst van leveranciersfacturen wijzigen, zoals heffingen of valuta-afrondingsbedragen.
    -   Bedragen op factuurregels van leveranciersfacturen wijzigen.
-   **Verdelingen weergeven** – Voor alle regels op het document de boekhoudingsverdelingen weergeven. Vanuit deze weergave kunt u de boekhoudingsverdelingen niet wijzigen.
    -   Bedragen in de koptekst en op de regel weergeven.

Als de leveranciersfactuur naar een inkooporder verwijst, kunt u de boekhoudingsverdelingen splitsen en wijzigen voor regels met een item dat niet is opgeslagen. Indien de leveranciersfactuurregel niet verwijst naar een inkooporderregel, kunt u ook een boekhoudingsverdeling verwijderen. U kunt geen regels splitsen of verwijderen voor heffingen, belastingen en regelkortingen. U kunt de grootboekrekening wijzigen, maar niet bedragen of percentages.
> [!NOTE]                                                                                                                                 
> Indien de bovenliggende regel een artikel bevat dat niet in voorraad wordt opgeslagen en de boekhoudingsverdelingen worden gesplitst, wordt de onderliggende regel automatisch gesplitst om overeen te komen met de financiële dimensies van de bovenliggende regel. De boekhoudingsverdelingen voor de onderliggende regel kunnen niet aanvullend worden gesplitst of verwijderd, maar afhankelijk van de instelling van de onderliggende regel kunt u mogelijk de grootboekrekening voor de boekhoudingsverdelingen van de onderliggende regel wijzigen.

## <a name="distributing-amounts"></a>Bedragen verdelen
Wanneer u een leveranciersfactuur invoert, wordt elk bedrag als volgt verdeeld.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Soort leveranciersfactuurregel</th>
<th>Volgorde van prioriteit die bepaalt waar de hoofdrekening uit wordt weergegeven</th>
<th>Volgorde van prioriteit die bepaalt welke standaard financiële dimensie wordt weergegeven</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Product in voorraad</td>
<td><ol>
<li>De boekhoudingsverdeling voor de inkooporderregel.</li>
<li>Het veld <strong>Hoofdrekening</strong> wanneer Inkoopuitgave voor product is geselecteerd op de pagina <strong>Boeking</strong>.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>De standaard financiële dimensiewaarden gebruiken op de leveranciersfactuur.</li>
</ol></td>
</tr>
<tr class="even">
<td>Een aanschaffingscategorie of een product dat niet op voorraad is</td>
<td><ol>
<li>De boekhoudingsverdeling voor de inkooporderregel indien de leveranciersfactuurregel verwijst naar een inkooporderregel.</li>
<li>Het veld <strong>Hoofdrekening</strong> wanneer Inkoopuitgave voor onkosten is geselecteerd op de pagina <strong>Boeking</strong>.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>Indien de hoofdrekening een toewijzingsrekening is, gebruikt u de standaardwaarde van de definitie van de toewijzingsrekening.</li>
<li>De standaard financiële dimensiewaarden gebruiken op de leveranciersfactuur.</li>
<li>De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina <strong>Rekeningschema</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Vaste activa</td>
<td><ol>
<li>De boekhoudingsverdeling voor de inkooporderregel indien de leveranciersfactuurregel verwijst naar een inkooporderregel.</li>
<li>Als <strong>Verwerving</strong> is geselecteerd in het veld <strong>Transactietype</strong> op de pagina <strong>Leveranciersfactuur</strong>: het veld <strong>Hoofdrekening</strong> wanneer <strong>Verwerving</strong> is geselecteerd op de pagina <strong>Boekingsprofielen voor vaste activa</strong>.</li>
<li>Als <strong>Verwervingscorrectie</strong> is geselecteerd in het veld <strong>Transactietype</strong>: het veld <strong>Hoofdrekening</strong> wanneer <strong>Verwervingscorrectie</strong> is geselecteerd op de pagina <strong>Boekingsprofielen voor vaste activa</strong>.</li>
</ol></td>
<td><ol>
<li>Gebruik de boekhoudingsverdeling voor de inkooporderregel als de factuurregel verwijst naar een inkooporderregel.</li>
<li>De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina <strong>Rekeningschema</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Project gedefinieerd op de leveranciersfactuurregel</td>
<td><ol>
<li>De boekhoudingsverdeling voor de inkooporderregel als de factuurregel verwijst naar een inkooporderregel.</li>
<li>Als <strong>Saldo</strong> is geselecteerd in het veld <strong>Kosten boeken - Artikel</strong> op de pagina <strong>Projectgroepen</strong>: het veld <strong>Hoofdrekening</strong> wanneer <strong>Kosten</strong> is geselecteerd op de pagina <strong>Boeking in grootboek instellen</strong>.</li>
<li>Als <strong>Verlies-en-winstrekening</strong> is geselecteerd in het veld <strong>Kosten boeken - Artikel</strong> op de pagina <strong>Projectgroepen</strong>:, het veld <strong>Hoofdrekening</strong> wanneer <strong>Kosten - artikel</strong> is geselecteerd op de pagina <strong>Boeking in grootboek instellen</strong>.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Regelkorting</td>
<td><ol>
<li>De boekhoudingsverdeling voor de inkooporderregel als de factuurregel verwijst naar een inkooporderregel.</li>
<li>Het veld <strong>Hoofdrekening</strong> wanneer <strong>Korting</strong> is geselecteerd op de pagina <strong>Boeking</strong>.</li>
<li>Als een hoofdrekening voor een korting niet is gedefinieerd in het boekingsprofiel, de boekhoudingsverdeling van de totaalprijs op de inkooporderregel.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>De financiële dimensies gebruiken voor de boekhoudingsverdelingen voor de totaalprijs van de leveranciersfactuurregel.</li>
<li>De financiële dimensiewaarden voor de leveranciersfactuurregel gebruiken.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina <strong>Rekeningschema</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Aankooptoeslag, ingevoerd op het tabblad <strong>Prijs en korting</strong> van de inkooporderregel</td>
<td><ol>
<li>De boekhoudingsverdeling voor de inkooporderregel als de factuurregel verwijst naar een inkooporderregel.</li>
<li>De boekhoudingsverdeling van de totaalprijs op de inkooporderregel.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>De financiële dimensies gebruiken voor de boekhoudingsverdelingen voor de totaalprijs van de leveranciersfactuurregel.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Regeltoeslag</td>
<td><ol>
<li>De boekhoudingsverdeling voor de inkooporderregel als de factuurregel verwijst naar een inkooporderregel.</li>
<li>Als <strong>Grootboekrekening</strong> is geselecteerd in het veld <strong>Debettype</strong> van de pagina <strong>Toeslagcode</strong>: het veld <strong>Debetrekening</strong> op de pagina <strong>Toeslagcode</strong>.</li>
<li>Als <strong>Artikel</strong> is geselecteerd in het veld <strong>Debettype</strong> op de pagina <strong>Toeslagcode</strong>: de boekhoudingsverdeling voor de totaalprijs op de inkooporderregel.</li>
<li>Als <strong>Klant/leverancier</strong> is geselecteerd in het veld <strong>Debettype</strong> op de pagina <strong>Toeslagcode</strong>: het veld <strong>Creditrekening</strong> op de pagina <strong>Toeslagcode</strong>.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>De financiële dimensies gebruiken voor de boekhoudingsverdelingen voor de totaalprijs van de leveranciersfactuurregel.</li>
<li>De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina <strong>Rekeningschema</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>BTW, met de volgende status:
<ul>
<li>De optie <strong>Amerikaanse belastingregels toepassen</strong> wordt geselecteerd op de pagina <strong>Grootboekparameters</strong>.</li>
</ul></td>
<td><ol>
<li>De boekhoudingsverdeling voor de inkooporderregel als de factuurregel verwijst naar een inkooporderregel.</li>
<li>De boekhoudingsverdelingen van de totaalprijs of de toeslag.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>De financiële dimensies gebruiken voor de boekhoudingsverdelingen voor de totaalprijs van de leveranciersfactuurregel.</li>
<li>De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</li>
</ol></td>
</tr>
<tr class="odd">
<td>BTW, met de volgende status:
<ul>
<li>De optie <strong>Amerikaanse belastingregels</strong> wordt uitgeschakeld op de pagina <strong>Grootboekparameters</strong>.</li>
<li>Het veld <strong>Gebruiksbelasting</strong> voor de btw-groep wordt uitgeschakeld op de pagina <strong>Btw-groepen</strong>.</li>
</ul></td>
<td><ol>
<li>Als het btw-percentage terug te vorderen is: het veld <strong>Te ontvangen btw</strong> op de pagina <strong>Groepen boekingen in grootboek</strong>.</li>
<li>Als het btw-bedrag niet recupereerbaar is, de totaalprijs of de boekhoudingsverdeling voor de toeslag.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>De financiële dimensies gebruiken voor de totaalprijs of de boekhoudingsverdelingen voor de kost van de leveranciersfactuurregel.</li>
<li>De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina <strong>Rekeningschema</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>BTW, met de volgende status:
<ul>
<li>De optie Amerikaanse belastingregels wordt uitgeschakeld op de pagina <strong>Grootboekparameters</strong>.</li>
<li>Het veld <strong>Gebruiksbelasting</strong> voor de btw-groep wordt ingeschakeld op de pagina <strong>Btw-groepen</strong>.</li>
</ul></td>
<td><ol>
<li>Als het btw-percentage terug te vorderen is: het veld <strong>Te ontvangen btw</strong> op de pagina <strong>Groepen boekingen in grootboek</strong>.</li>
<li>Als het belastingbedrag niet terug te vorderen is: het veld <strong>Gebruiksbelastinguitgave</strong> op de pagina <strong>Groepen boekingen in grootboek</strong>.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>De financiële dimensies gebruiken voor de totaalprijs of de boekhoudingsverdelingen voor de kost van de leveranciersfactuurregel.</li>
<li>De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina <strong>Rekeningschema</strong>.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kopteksttoeslag</td>
<td><ol>
<li>Als <strong>Grootboekrekening</strong> is geselecteerd in het veld <strong>Debettype</strong> van de pagina <strong>Toeslagcode</strong>: het veld <strong>Debetrekening</strong> op de pagina <strong>Toeslagcode</strong>.</li>
<li>Als <strong>Klant/leverancier</strong> is geselecteerd in het veld <strong>Debettype</strong> op de pagina <strong>Toeslagcode</strong>: het veld <strong>Creditrekening</strong> op de pagina <strong>Toeslagcode</strong>.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>Indien de hoofdrekening een toewijzingsrekening is, gebruikt u de standaardwaarde van de definitie van de toewijzingsrekening.</li>
<li>De standaardsjabloon gebruiken van de financiële dimensie van de leveranciersfactuurtitel.</li>
<li>De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina <strong>Rekeningschema</strong>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Kortingtitel</td>
<td><ol>
<li>Het veld <strong>Hoofdrekening</strong> voor het boekingstype <strong>Korting op leveranciersfactuur</strong> op de pagina <strong>Rekeningen voor automatische transacties</strong>.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>De financiële dimensies gebruiken voor de boekhoudingsverdelingen voor de totaalprijs van de leveranciersfactuurregel.</li>
<li>De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina <strong>Rekeningschema</strong>.</li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="distributing-taxes"></a>Belastingen verdelen

Boekhoudingsverdelingen voor belastingen kunnen pas worden gemaakt nadat belastingen zijn berekend. Voor het berekenen van de btw moet u een van de volgende taken uitvoeren op de pagina **Leveranciersfactuur**:
-   Het factuurtotaal weergeven.
-   De btw weergeven.
-   De subadministratie bekijken.
-   Boekhoudingsverdelingen voor de totale leveranciersfactuur weergeven.
-   Een leveranciersfactuur in wachtstand zetten.
-   De leveranciersfactuur boeken.

## <a name="subledger-journals-for-vendor-invoices"></a>Subgrootboekrekening voor leveranciersfacturen
Voordat u een leveranciersfactuur boekt, kunt u het volledige boekhoudingsjournaal van de factuur bekijken, inclusief debet- en creditbedragen, om te controleren of de factuur naar de juiste rekeningen wordt geboekt. Deze weergave van het volledige boekhoudingsjournaal heet een subadministratie. 

Indien het journaal in de subadministratie onjuist is wanneer u een afdrukvoorbeeld bekijkt voordat u de leveranciersfactuur boekt, kunt u het journaal in de subadministratie niet wijzigen. In plaats daarvan moet u de boekhoudingsverdelingen of het boekingsprofiel wijzigen. De boekhoudingsverdelingen worden gebruikt om één kant van de boekhoudingspost, de debit- of de creditzijde, te definiëren. De compenserende journaalregel in de subadministratie wordt gemaakt van de boekingsprofielen, zoals van de leveranciersrekening of de belasting.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
