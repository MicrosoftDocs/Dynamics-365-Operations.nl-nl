---
title: Boekhoudingsverdelingen en journaalposten voor leveranciersfacturen
description: Boekhoudingsverdelingen worden gebruikt om te bepalen hoe een bedrag zal worden verwerkt, zoals hoe de onkosten, BTW of heffingen zullen worden verwerkt op een leveranciersfactuur. Elk bedrag dat moet worden verwerkt wanneer de leveranciersfactuur in het boekhoudingsjournaal wordt vastgelegd, heeft een of meerdere boekhoudingsverdelingen.
author: abruer
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da15f27c7fef6367eacc83271419b633c0cbb245
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012283"
---
# <a name="accounting-distributions-and-journal-entries-for-vendor-invoices"></a>Boekhoudingsverdelingen en journaalposten voor leveranciersfacturen

[!include [banner](../includes/banner.md)]

Boekhoudingsverdelingen worden gebruikt om te bepalen hoe een bedrag zal worden verwerkt, zoals hoe de onkosten, BTW of heffingen zullen worden verwerkt op een leveranciersfactuur. Elk bedrag dat moet worden verwerkt wanneer de leveranciersfactuur in het boekhoudingsjournaal wordt vastgelegd, heeft een of meerdere boekhoudingsverdelingen. 

<a name="accounting-distributions"></a>Boekhoudingsverdelingen 
-------------------------

U kunt de volgende knoppen op de pagina Leveranciersfactuur gebruiken voor het weergeven en mogelijk wijzigen van de boekhoudingsverdelingen voor elk bedrag op de leveranciersfactuur.
-   **Bedragen verdelen** – De boekhoudingsverdelingen weergeven en wijzigen voor een afzonderlijke regel en alle onderliggende regels, zoals belastingen of heffingen. U kunt de boekhoudingsverdeling voor de onderliggende regel rechtstreeks weergeven en wijzigen op de pagina Btw-transacties of de pagina Transacties met toeslagen transacties.
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
<li>Het veld Hoofdrekening wanneer Inkoopuitgave voor product is geselecteerd op de pagina Boeking.</li>
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
<li>Het veld Hoofdrekening wanneer Inkoopuitgave voor onkosten is geselecteerd op de pagina Boeking.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>Indien de hoofdrekening een toewijzingsrekening is, gebruikt u de standaardwaarde van de definitie van de toewijzingsrekening.</li>
<li>De standaard financiële dimensiewaarden gebruiken op de leveranciersfactuur.</li>
<li>De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Vaste activa</td>
<td><ol>
<li>De boekhoudingsverdeling voor de inkooporderregel indien de leveranciersfactuurregel verwijst naar een inkooporderregel.</li>
<li>Als Verwerving is geselecteerd in het veld Transactietype in het formulier Leveranciersfactuur, wordt het veld Hoofdrekening geselecteerd op de pagina Boekingsprofielen voor vaste activa.</li>
<li>Als Verwervingscorrectie is geselecteerd in het veld Transactietype, wordt het veld Verwervingscorrectie geselecteerd op de pagina Boekingsprofielen voor vaste activa.</li>
</ol></td>
<td><ol>
<li>Gebruik de boekhoudingsverdeling voor de inkooporderregel als de factuurregel verwijst naar een inkooporderregel.</li>
<li>De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</li>
</ol></td>
</tr>
<tr class="even">
<td>Project gedefinieerd op de leveranciersfactuurregel</td>
<td><ol>
<li>De boekhoudingsverdeling voor de inkooporderregel als de factuurregel verwijst naar een inkooporderregel.</li>
<li>Als Saldo is geselecteerd in het veld Kosten boeken - Artikel op de pagina Projectgroep, wordt het veld Hoofdrekening geselecteerd op de pagina Instellingen boeking in grootboek.</li>
<li>Als Verlies-en-winstrekening is geselecteerd in het veld Kosten boeken - Artikel op de pagina Projectgroep, wordt het veld Kosten - artikel geselecteerd op de pagina Instellingen boeking in grootboek.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Regelkorting</td>
<td><ol>
<li>De boekhoudingsverdeling voor de inkooporderregel als de factuurregel verwijst naar een inkooporderregel.</li>
<li>Het veld Hoofdrekening wanneer Korting is geselecteerd op de pagina Boeking.</li>
<li>Als een hoofdrekening voor een korting niet is gedefinieerd in het boekingsprofiel, de boekhoudingsverdeling van de totaalprijs op de inkooporderregel.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>De financiële dimensies gebruiken voor de boekhoudingsverdelingen voor de totaalprijs van de leveranciersfactuurregel.</li>
<li>De financiële dimensiewaarden voor de leveranciersfactuurregel gebruiken.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</li>
</ol></td>
</tr>
<tr class="even">
<td>Aankooptoeslag, ingevoerd op het tabblad Prijs en korting van de inkooporderregel</td>
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
<li>Als Grootboekrekening is geselecteerd in het veld Debettype in het formulier Toeslagcode, het veld Debetrekening op de pagina Toeslagcode.</li>
<li>Als Artikel is geselecteerd in het veld Debettype in het formulier Toeslagcode, de boekhoudingsverdeling voor de totaalprijs op de inkooporderregel.</li>
<li>Als Klant/leverancier is geselecteerd in het veld Debettype in het formulier Toeslagcode, het veld Creditrekening op de pagina Toeslagcode.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>De financiële dimensies gebruiken voor de boekhoudingsverdelingen voor de totaalprijs van de leveranciersfactuurregel.</li>
<li>De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</li>
</ol></td>
</tr>
<tr class="even">
<td>BTW, met de volgende status:
<ul>
<li>De optie Amerikaanse belastingregels toepassen wordt geselecteerd op de pagina Grootboekparameters.</li>
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
<li>De optie Amerikaanse belastingregels wordt uitgeschakeld op de pagina Grootboekparameters.</li>
<li>Het veld Gebruiksbelasting voor de btw-groep wordt uitgeschakeld op de pagina Btw-groepen.</li>
</ul></td>
<td><ol>
<li>Als het btw-percentage terug te vorderen is, het veld Te ontvangen btw op de pagina Groepen boekingen in grootboek.</li>
<li>Als het btw-bedrag niet recupereerbaar is, de totaalprijs of de boekhoudingsverdeling voor de toeslag.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>De financiële dimensies gebruiken voor de totaalprijs of de boekhoudingsverdelingen voor de kost van de leveranciersfactuurregel.</li>
<li>De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</li>
</ol></td>
</tr>
<tr class="even">
<td>BTW, met de volgende status:
<ul>
<li>De optie Amerikaanse belastingregels wordt uitgeschakeld op de pagina Grootboekparameters.</li>
<li>Het veld Gebruiksbelasting voor de btw-groep wordt ingeschakeld op de pagina Btw-groepen.</li>
</ul></td>
<td><ol>
<li>Als het btw-percentage terug te vorderen is, het veld Te ontvangen btw op de pagina Groepen boekingen in grootboek.</li>
<li>Als het btw-percentage niet terug te vorderen is, het veld Gebruiksbelastinguitgave op de pagina Groepen boekingen in grootboek.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>De financiële dimensies gebruiken voor de totaalprijs of de boekhoudingsverdelingen voor de kost van de leveranciersfactuurregel.</li>
<li>De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kopteksttoeslag</td>
<td><ol>
<li>Als Grootboekrekening is geselecteerd in het veld Debettype in het formulier Toeslagcode, het veld Debetrekening op de pagina Toeslagcode.</li>
<li>Als Klant/leverancier is geselecteerd in het veld Debettype in het formulier Toeslagcode, het veld Creditrekening op de pagina Toeslagcode.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>Indien de hoofdrekening een toewijzingsrekening is, gebruikt u de standaardwaarde van de definitie van de toewijzingsrekening.</li>
<li>De standaardsjabloon gebruiken van de financiële dimensie van de leveranciersfactuurtitel.</li>
<li>De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</li>
</ol></td>
</tr>
<tr class="even">
<td>Kortingtitel</td>
<td><ol>
<li>Het veld Hoofdrekening voor het boekingstype Korting op leveranciersfactuur op de pagina Rekeningen voor automatische transacties.</li>
</ol></td>
<td><ol>
<li>Als de factuurregel verwijst naar een inkooporderregel, gebruikt u de boekhoudingsverdeling voor de inkooporderregel.</li>
<li>De financiële dimensies gebruiken voor de boekhoudingsverdelingen voor de totaalprijs van de leveranciersfactuurregel.</li>
<li>De financiële dimensiewaarden gebruiken van de leveranciersfactuurregel.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de hoofdrekening op de pagina Rekeningschema.</li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a>Belastingen verdelen
------------------

Boekhoudingsverdelingen voor belastingen kunnen pas worden gemaakt nadat belastingen zijn berekend. Voor het berekenen van de btw moet u een van de volgende taken uitvoeren op de pagina Leveranciersfactuur:
-   Het factuurtotaal weergeven.
-   De btw weergeven.
-   De subadministratie bekijken.
-   Boekhoudingsverdelingen voor de totale leveranciersfactuur weergeven.
-   Een leveranciersfactuur in wachtstand zetten.
-   De leveranciersfactuur boeken.

## <a name="subledger-journals-for-vendor-invoices"></a>Subgrootboekrekening voor leveranciersfacturen
Voordat u een leveranciersfactuur boekt, kunt u het volledige boekhoudingsjournaal van de factuur bekijken, inclusief debet- en creditbedragen, om te controleren of de factuur naar de juiste rekeningen wordt geboekt. Deze weergave van het volledige boekhoudingsjournaal heet een subadministratie. 

Indien het journaal in de subadministratie onjuist is wanneer u een afdrukvoorbeeld bekijkt voordat u de leveranciersfactuur boekt, kunt u het journaal in de subadministratie niet wijzigen. In plaats daarvan moet u de boekhoudingsverdelingen of het boekingsprofiel wijzigen. De boekhoudingsverdelingen worden gebruikt om één kant van de boekhoudingspost, de debit- of de creditzijde, te definiëren. De compenserende journaalregel in de subadministratie wordt gemaakt van de boekingsprofielen, zoals van de leveranciersrekening of de belasting.





