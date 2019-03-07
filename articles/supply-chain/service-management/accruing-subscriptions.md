---
title: Toerekenen van abonnementen
description: Met serviceabonnementen boekt u de transitorische opbrengst handmatig in de perioden die volgen op de datum waarop u een tarieftransactie hebt gefactureerd.
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a183e17749c04b407eb17155ecb1363e96ade18a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "317172"
---
# <a name="accruing-subscriptions"></a>Toerekenen van abonnementen 

[!include [banner](../includes/banner.md)]


Met serviceabonnementen boekt u de transitorische opbrengst handmatig in de perioden die volgen op de datum waarop u een tarieftransactie hebt gefactureerd.

Perioden voor transitorische opbrengsten worden gemaakt voor de factuurperiode die u voor de abonnementskosten hebt gedefinieerd en worden gebaseerd op de periodecode van het abonnement.

U kunt de transitorische opbrengst boeken en terugboeken.

## <a name="reverse-accruals-of-credit-amounts"></a>Transitorische creditbedragen terugboeken

Bij het crediteren van gefactureerde abonnementsbedragen kunt u twee verschillende methoden gebruiken om de transitorische bedragen terug te boeken:

  - u kunt elke transitorische opbrengsttransactie afzonderlijk terugboeken voordat u een creditnotavoorstel maakt voor de transactie. Dit is de handmatige methode. (handmatig)

  - u kunt de transitorische bedragen laten terugboeken op de boekingsdatum van de creditnota of op de oorspronkelijke boekingsdatum van de toerekening.

Zie [Parameters voor abonnement (formulier)](https://technet.microsoft.com/en-us/library/aa619615.aspx) voor meer informatie.

## <a name="setup-requirements"></a>Vereisten instellen

Controleer of wordt voldaan aan de volgende gegevensvereisten als u transitorische opbrengst wilt boeken:

## <a name="account-setup"></a>Rekeninginstelling

De rekeningen **OHW - abonnement** en **Transitorische opbrengsten - abonnement** moeten worden ingesteld in de module **Project**.

Wanneer u transitorische opbrengsten boekt, wordt de rekening **OHW - abonnement** gedebiteerd met het transitorische bedrag. Dit bedrag wordt gecrediteerd aan de rekening **Transitorische opbrengsten - abonnement**.

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a>Rekeningen instellen voor het boeken van transitorische opbrengsten van abonnementen

1.  Klik op **Projectbeheer en boekhouding** \> **Instellen** \> **Boeking** \> **Instellingen boeking in grootboek**.

2.  Klik op het tabblad **Opbrengstrekeningen** en selecteer **OHW - abonnement** of **Transitorische opbrengsten - abonnement** om de rekeningen in te stellen.

## <a name="subscription-group-setup"></a>Abonnementsgroep instellen

U moet het selectievakje **Opbrengst samenvoegen** inschakelen om transitorische opbrengst voor abonnementen te kunnen boeken. U vindt dit selectievakje in het formulier **Abonnementsgroepen** voor de groep die aan het abonnement is gekoppeld. Klik op **Servicebeheer** \> **Instellen** \> **Serviceabonnementen** \> **Abonnementsgroepen**.

## <a name="enable-revenue-accrual-on-a-subscription-group"></a>Transitorische opbrengst voor een abonnementsgroep inschakelen

1.  Klik op **Servicebeheer** \> **Instellen** \> **Serviceabonnementen** \> **Abonnementsgroepen**.

## <a name="periods"></a>Perioden

U moet een factureringsperiodecode definiëren. Als u niet wilt dat transitorische opbrengst wordt geboekt in dezelfde tijdsintervallen die u voor facturering gebruikt, moet u ook een transitorische periode definiëren.

In de volgende tabel vindt u een overzicht van de transitorische perioden die u voor elke factureringsperiode kunt definiëren:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Factureringsperiode</p></th>
<th><p>Transitorische periode</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Jaren</strong></p></td>
<td><ul>
<li><p><strong>Jaren</strong></p></li>
<li><p><strong>Kwartaal</strong></p></li>
<li><p><strong>Maand</strong></p></li>
<li><p><strong>Dag</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Kwartaal</strong></p></td>
<td><ul>
<li><p><strong>Kwartaal</strong></p></li>
<li><p><strong>Maand</strong></p></li>
<li><p><strong>Dag</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Maand</strong></p></td>
<td><ul>
<li><p><strong>Maand</strong></p></li>
<li><p><strong>Dag</strong></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><strong>Week</strong></p></td>
<td><ul>
<li><p><strong>Dag</strong></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><strong>Dag</strong></p></td>
<td><ul>
<li><p><strong>Dag</strong></p></li>
</ul></td>
</tr>
</tbody>
</table>

Het instellen van een factureringsperiode is een verplicht onderdeel voor het instellen van een abonnementsgroep. U kunt zelf bepalen of u ook een transitorische periode voor de abonnementsgroep wilt instellen. Als u een transitorische periode voor de abonnementsgroep instelt, wordt deze periode voorgesteld in het veld **Periodecode**. U vindt dit veld in het formulier **Abonnementsopbrengsten samenvoegen** wanneer u de transitorische opbrengst van abonnementen boekt. De transitorische periode is echter optionele informatie over de abonnementsgroep.


> [!NOTE]
> <P>Gebruik het volgende pad om het formulier <STRONG>Abonnementopbrengsten samenvoegen</STRONG> te openen. Klik op <STRONG>Servicebeheer</STRONG> &gt; <STRONG>Periodiek</STRONG> &gt; <STRONG>Serviceabonnementen</STRONG> &gt; <STRONG>Abonnementsopbrengsten samenvoegen</STRONG>.</P>


## <a name="transactions"></a>Transacties

U kunt het aantal grootboektransacties beperken dat wordt gemaakt wanneer u transitorische opbrengsten boekt. Geef voor abonnementen op of de grootboektransacties als een totaal of per regel moeten worden gemaakt.

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a>Opgeven welk niveau van boekingsdetails moet worden weergegeven voor transitorische transacties

1.  Klik op **Projectbeheer en boekhouding** \> **Instellen** \> **Projectbeheer- en boekhoudingsparameters**.

2.  Selecteer op het tabblad **Financieel** in het veld **Factuur** **Totaal** of **Regel**.


## <a name="see-also"></a>Zie ook

[Abonnementsopbrengsten samenvoegen](accrue-subscription-revenue.md)

  


