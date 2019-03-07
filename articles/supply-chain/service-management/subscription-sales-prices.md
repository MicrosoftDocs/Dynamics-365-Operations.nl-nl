---
title: Verkoopprijzen abonnement
description: Bij het maken van een abonnement wordt de verkoopprijs afgeleid van de verkoopprijs die is ingesteld in het formulier Verkoopprijs (abonnement).
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e18690f7e9b790ecbd0ac0de1955fc95ab1f082
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2019
ms.locfileid: "352155"
---
# <a name="subscription-sales-prices"></a>Verkoopprijzen abonnement   

[!include [banner](../includes/banner.md)]


Bij het maken van een abonnement wordt de verkoopprijs afgeleid van de verkoopprijs die is ingesteld in het formulier **Verkoopprijs (abonnement)**.

In het formulier **Verkoopprijs (abonnement)** kunt u verkoopprijzen maken voor een specifiek abonnement of u kunt verkoopprijzen maken die breder toepasbaar zijn. Als u een verkoopprijs wilt toepassen op een abonnement, moeten de periodecode en de valuta van het abonnement hetzelfde zijn als de periodecode en de valuta van de verkoopprijs.

Als de periodecode en valuta van het abonnement en de verkoopprijs overeenkomen, worden abonnementsverkoopprijzen geselecteerd op basis van de prioriteiten die in de volgende tabel worden vermeld. Met een lege cel in de tabel wordt aangegeven dat het veld leeg is en met X dat de waarde gelijk is aan de waarde in het abonnement op basis waarvan de transactie is gegenereerd.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Prioriteit </p></th>
<th><p><strong>Categorie</strong></p></th>
<th><p><strong>Project-ID</strong></p></th>
<th><p><strong>Abonnement</strong></p></th>
<th><p><strong>Verkoopvaluta</strong></p></th>
<th><p><strong>Periodecode</strong></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>4</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>5</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>6</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>7</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
<tr class="even">
<td><p>8</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
</tr>
</tbody>
</table>


Bij het maken van abonnementskosten wordt de meest gedetailleerde verkoopprijs (zoals aangegeven in bovenstaande tabel) geselecteerd als abonnementsverkoopprijs.

## <a name="update-and-index-subscription-sales-prices"></a>Abonnementsverkoopprijzen bijwerken en indexeren

U kunt de abonnementsverkoopprijs bijwerken door de basisprijs of de index bij te werken. Hiervoor kunt u werken met een percentage of met een nieuwe waarde.

## <a name="subscription-fee-sales-prices"></a>Verkoopprijzen voor abonnementskosten

Bij het maken van abonnementskosten wordt de verkoopprijs gebaseerd op de verkoopprijs in de instellingen van het abonnement. U kunt gebruikmaken van de basisprijs in de instellingen van abonnementsprijzen, maar u kunt ook geïndexeerde verkoopprijzen maken.

## <a name="example"></a>Voorbeeld

U wilt een abonnementsverkoopprijs van EUR 500 instellen voor het nieuwe project 9030. In het formulier **Verkoopprijs (abonnement)** maakt u een regel met de abonnementsverkoopprijs, zoals in de volgende tabel wordt aangegeven.

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Geldig van</p></th>
<th><p>Categorie</p></th>
<th><p>project</p></th>
<th><p>Abonnement</p></th>
<th><p>Periodecode</p></th>
<th><p>Verkoopvaluta</p></th>
<th><p>Verkoopprijs</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2006</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Maand</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


De velden **Categorie** en **Abonnement** zijn leeg.

Vervolgens maakt u de volgende abonnementen.

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Serviceabonnement</p></th>
<th><p>project</p></th>
<th><p>Abonnementsgroep</p></th>
<th><p>Categorie</p></th>
<th><p>Valuta</p></th>
<th><p>Periodecode</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>Abb1</p></td>
<td><p>AbbCat1</p></td>
<td><p>EUR</p></td>
<td><p>Maandelijks</p></td>
</tr>
<tr class="even">
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>Abb1</p></td>
<td><p>AbbCat2</p></td>
<td><p>EUR</p></td>
<td><p>Maandelijks</p></td>
</tr>
</tbody>
</table>


Nu maakt u abonnementskosten voor beide abonnementen in abonnementsgroep Abb1:

1.  Klik op **Servicebeheer** \> **Instellen** \> **Serviceabonnementen** \> **Abonnementsgroepen**.

2.  Klik in het formulier **Abonnementsgroepen** op **Functie** \> **Abonnementskosten maken**.

3.  Voer in het formulier **Abonnementskosten maken** de juiste informatie in. Zie voor meer informatie [Tarieftransacties abonnement maken](create-subscription-fee-transactions.md).

Voor beide abonnementen worden abonnementskosten gemaakt met een verkoopprijs van EUR 500, zoals in de volgende tabel wordt weergegeven.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Projectdatum</p></th>
<th><p>Serviceabonnement</p></th>
<th><p>project</p></th>
<th><p>Categorie</p></th>
<th><p>Begindatum</p></th>
<th><p>Einddatum</p></th>
<th><p>Verkoopvaluta</p></th>
<th><p>Verkoopprijs</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2006</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>AbbCat1</p></td>
<td><p>01-01-2007</p></td>
<td><p>31-03-2007</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28-08-2006</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>AbbCat2</p></td>
<td><p>01-01-2007</p></td>
<td><p>31-03-2007</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


Later besluit u dat u verkoopprijzen wilt opgeven voor de categorie AbbCat1 voor project 9030. Daarom maakt u een nieuwe verkoopprijsregel met een verkoopprijs van EUR 550 voor de combinatie van project 9030 en kostencategorie AbbCat1. Er zijn nu twee regels met abonnementsverkoopprijzen beschikbaar voor project 9030, zoals in de volgende tabel wordt weergegeven.

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Geldig van</p></th>
<th><p>Categorie</p></th>
<th><p>project</p></th>
<th><p>Abonnement</p></th>
<th><p>Periodecode</p></th>
<th><p>Valuta</p></th>
<th><p>Verkoopprijs</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-08-2007</p></td>
<td></td>
<td><p>9030</p></td>
<td></td>
<td><p>Maand</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
<tr class="even">
<td><p>28-08-2007</p></td>
<td><p>AbbCat1</p></td>
<td><p>9030</p></td>
<td></td>
<td><p>Maand</p></td>
<td><p>EUR</p></td>
<td><p>550</p></td>
</tr>
</tbody>
</table>


U herhaalt de bovenstaande procedure om abonnementskosten te maken voor beide abonnementen in abonnementsgroep Abb1. In de volgende tabel worden de transacties weergegeven die voor elk abonnement worden gemaakt dat is gekoppeld aan de abonnementsgroep.

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Projectdatum</p></th>
<th><p>Abonnement</p></th>
<th><p>project</p></th>
<th><p>Categorie</p></th>
<th><p>Begindatum</p></th>
<th><p>Einddatum</p></th>
<th><p>Verkoopvaluta</p></th>
<th><p>Verkoopprijs</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>28-07-2007</p></td>
<td><p>00020_135</p></td>
<td><p>9030</p></td>
<td><p>AbbCat1</p></td>
<td><p>01-01-2008</p></td>
<td><p>31-03-2008</p></td>
<td><p>EUR</p></td>
<td><p>550</p></td>
</tr>
<tr class="even">
<td><p>28-07-2008</p></td>
<td><p>00021_135</p></td>
<td><p>9030</p></td>
<td><p>AbbCat2</p></td>
<td><p>01-01-2008</p></td>
<td><p>31-03-2008</p></td>
<td><p>EUR</p></td>
<td><p>500</p></td>
</tr>
</tbody>
</table>


In de eerste transactie voor abonnement 00020\_135 is de verkoopprijs van EUR 550 afgeleid van de abonnementsverkoopprijs die is ingesteld voor de combinatie van het specifieke project en de categorie. In de tweede transactie voor abonnement 00021\_135 wordt de verkoopprijs van EUR 500 gebruikt als abonnementsverkoopprijs van het project, omdat er geen prijs is ingesteld voor de combinatie van project 9030 en categorie SubCat2.

## <a name="see-also"></a>Zie ook

[Abonnementsverkoopprijzen bijwerken en indexeren](update-and-index-subscription-sales-prices.md)

  


