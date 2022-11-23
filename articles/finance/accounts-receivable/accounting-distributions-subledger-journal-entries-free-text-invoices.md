---
title: Boekhoudingsverdelingen en journaalposten voor vrije-tekstfacturen
description: Boekhoudingsverdelingen worden gebruikt om te bepalen hoe een bedrag zal worden verwerkt, zoals hoe de omzet, btw of heffingen zal worden verwerkt op een factuur met vrije tekst. Elk bedrag dat moet worden verwerkt wanneer de factuur met vrije tekst in het boekhoudingsjournaal wordt vastgelegd, heeft een of meerdere boekhoudingsverdelingen.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f5120c4e75e821776201d5add2d498feb94d0297
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778406"
---
# <a name="accounting-distributions-and-subledger-entries-for-free-text-invoices"></a>Boekhoudingsverdelingen en posten in de subadministratie voor vrije-tekstfacturen

[!include [banner](../includes/banner.md)]

Boekhoudingsverdelingen worden gebruikt om te bepalen hoe een bedrag zal worden verwerkt, zoals hoe de omzet, btw of heffingen zal worden verwerkt op een factuur met vrije tekst. Elk bedrag dat moet worden verwerkt wanneer de factuur met vrije tekst in het boekhoudingsjournaal wordt vastgelegd, heeft een of meerdere boekhoudingsverdelingen.

## <a name="accounting-distributions"></a>Boekhoudingsverdelingen

U kunt de volgende knoppen op de pagina **Vrije-tekstfactuur** gebruiken voor het weergeven en mogelijk wijzigen van de boekhoudingsverdelingen voor elk bedrag op de factuur met vrije tekst.

-   **Bedragen verdelen**: De boekhoudingsverdelingen weergeven en wijzigen voor een afzonderlijke regel en alle onderliggende regels, zoals belastingen of heffingen. U kunt de boekhoudingsverdeling voor de onderliggende regel rechtstreeks weergeven en wijzigen op de pagina **Btw-transacties** of de pagina **Transacties met toeslagen**.
    -   Bedragen in de koptekst van facturen met vrije tekst wijzigen, zoals heffingen of valuta-afrondingsbedragen.
    -   Bedragen op regels van facturen met vrije tekst wijzigen.
-   **Verdelingen weergeven**: Voor alle regels op het document de boekhoudingsverdelingen weergeven. Vanuit deze weergave kunt u de boekhoudingsverdelingen niet wijzigen.
    -   Bedragen in de koptekst en op de regel weergeven.

## <a name="distributing-amounts"></a>Bedragen verdelen
Wanneer u een factuur met vrije tekst invoert, wordt elk bedrag als volgt verdeeld.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Type monetair bedrag</th>
<th>Van waaruit de hoofdrekening wordt weergegeven</th>
<th>Volgorde van prioriteit die bepaalt welke standaard financiële dimensie wordt weergegeven</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Factuurregel van vrije tekst-factuur</td>
<td>De grootboekrekening op de factuurregel van de vrije tekst-factuur.</td>
<td><ol>
<li>Indien de hoofdrekening een toewijzingsrekening is, gebruikt u de standaardwaarde van de definitie van de toewijzingsrekening.</li>
<li>Indien de hoofdrekening geen toewijzingsrekening is, gebruikt u de standaardsjabloon voor financiële dimensie op de factuurregel voor de vrije tekst-factuur.</li>
<li>De standaard financiële dimensiewaarden gebruiken op de factuurregel voor de vrije tekst-factuur.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de grootboekrekening op de pagina Rekeningschema.</li>
</ol></td>
</tr>
<tr class="even">
<td>Factuurregel voor vrije tekst-factuur voor een vaste activa-nummer en waardemodelcombinatie
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>Opmerking </strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>De hoofdrekening op de factuurregel voor de vrije tekst-factuur is de verwerkingsrekening voor vaste activa.</td>
</tr>
</tbody>
</table>
</div></td>
<td>De grootboekrekening op de factuurregel van de vrije tekst-factuur.</td>
<td><ol>
<li>De standaard financiële dimensiewaarden gebruiken op de factuurregel voor de vrije tekst-factuur.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de grootboekrekening op de pagina Rekeningschema.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Kortingsbedrag voor de vrije tekst-factuur</td>
<td>Het veld Hoofdrekening voor klantkortingen op de pagina Contantkortingen.</td>
<td><ol>
<li>Indien de hoofdrekening een toewijzingsrekening is, gebruikt u de standaardwaarde van de definitie van de toewijzingsrekening.</li>
<li>Indien de hoofdrekening geen toewijzingsrekening is, gebruikt u de standaardsjabloon voor financiële dimensie op de factuurregel voor de vrije tekst-factuur.</li>
<li>De standaard financiële dimensiewaarden gebruiken op de factuurregel voor de vrije tekst-factuur.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de grootboekrekening op de pagina Rekeningschema.</li>
</ol></td>
</tr>
<tr class="even">
<td>Btw-bedrag voor de vrije tekst-factuur</td>
<td>Het veld Te betalen btw op de pagina Grootboekboekingsgroepen.</td>
<td><ol>
<li>De financiële dimensies gebruiken die zijn gedefinieerd op het regelbedrag van de vrije tekst-factuur of de verdelingen voor het heffingsregelbedrag.</li>
<li>De standaard financiële dimensiewaarden gebruiken op de factuurregel voor de vrije tekst-factuur.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de grootboekrekening op de pagina Rekeningschema.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Heffingsregelbedrag op vrije tekst-factuur</td>
<td>Het veld Creditrekening op de pagina Toeslagcode.</td>
<td><ol>
<li>Indien de hoofdrekening een toewijzingsrekening is, gebruikt u de standaardwaarde van de definitie van de toewijzingsrekening.</li>
<li>Indien de hoofdrekening geen toewijzingsrekening is, gebruikt u de standaardsjabloon voor financiële dimensie op de factuurregel voor de vrije tekst-factuur.</li>
<li>De standaard financiële dimensiewaarden gebruiken op de factuurregel voor de vrije tekst-factuur.</li>
<li>De standaard financiële dimensiewaarden gebruiken van de grootboekrekening op de pagina Rekeningschema.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a>Belastingen verdelen
Boekhoudingsverdelingen voor belastingen kunnen pas worden gemaakt nadat belastingen zijn berekend. Voor het berekenen van de btw moet u een van de volgende taken uitvoeren op de pagina **Vrije-tekstfactuur**:
-   De btw weergeven.
-   Het factuurtotaal weergeven.
-   De cashflow weergeven.
-   Boekhoudingsverdelingen voor de totale vrije tekst-factuur weergeven.
-   De subadministratie bekijken.

## <a name="subledger-journals-for-free-text-invoices"></a>Subadministratie voor vrije tekst-facturen
Voordat u een vrije tekst-factuur boekt, kunt u het volledige boekhoudingsjournaal van de factuur bekijken, inclusief debet- en creditbedragen, om te controleren of de factuur naar de juiste rekeningen wordt geboekt. Deze weergave van het volledige boekhoudingsjournaal heet een subadministratie. Indien het journaal in de subadministratie onjuist is wanneer u een afdrukvoorbeeld bekijkt voordat u de vrije tekst-factuur boekt, kunt u het journaal in de subadministratie niet wijzigen. In plaats daarvan moet u de boekhoudingsverdelingen of het boekingsprofiel wijzigen. De boekhoudingsverdelingen worden gebruikt om één kant van de boekhoudingspost, de debit- of de creditzijde, te definiëren. De compenserende journaalregel in de subadministratie wordt gemaakt van de boekingsprofielen, zoals van de klantrekening of de belasting.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
