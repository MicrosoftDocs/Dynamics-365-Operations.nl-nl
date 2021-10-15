---
title: Voorbeeld van reductiedagen
description: Voorbeeld van reductiedagen.
author: kamaybac
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97fb032d02df1dbedaeccec14496cb1d63e8cf70
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7567938"
---
# <a name="reduction-days-example"></a>Voorbeeld van reductiedagen

[!include [banner](../includes/banner.md)]

U hebt een abonnementstransactie gemaakt voor het onderhoudsabonnement van een klant dat wordt beschreven in de volgende tabel.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Begindatum</p></th>
<th><p>Einddatum</p></th>
<th><p>Abonnement</p></th>
<th><p>Type abonnement</p></th>
<th><p>Project</p></th>
<th><p>Categorie</p></th>
<th><p>Verkoopvaluta</p></th>
<th><p>Verkoopprijs</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>01 maart 2011</p></td>
<td><p>31 maart 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Normaal</strong></p></td>
<td><p>9013</p></td>
<td><p>AbbCat2</p></td>
<td><p>EUR</p></td>
<td><p>200,00</p></td>
</tr>
</tbody>
</table>

De klant geeft aan dat de service niet nodig is gedurende twee dagen (10 maart en 11 maart). U zegt toe het abonnement te verkorten met deze twee dagen.

U maakt een nieuwe transactie met het type **Reductiedagen** zoals in de volgende tabel wordt beschreven.

<table>
<colgroup>
<col />
<col />
<col />
<col />
<col />
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Begindatum</p></th>
<th><p>Einddatum</p></th>
<th><p>Abonnement</p></th>
<th><p>Type abonnement</p></th>
<th><p>Project</p></th>
<th><p>Categorie</p></th>
<th><p>Verkoopvaluta</p></th>
<th><p>Verkoopprijs</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>10 maart 2011</p></td>
<td><p>11 maart 2011</p></td>
<td><p>NR-2</p></td>
<td><p><strong>Reductiedagen</strong></p></td>
<td><p>9013</p></td>
<td><p>AbbCat2</p></td>
<td><p>EUR</p></td>
<td><p>-12,90</p></td>
</tr>
</tbody>
</table>

Wanneer de transacties voor maart 2011 worden gefactureerd, wordt de verkoopprijs van EUR 200 verminderd met EUR 12,90. Het toerekenbare bedrag voor de abonnementstransactie is daarom EUR 187,10 en er worden twee transacties gefactureerd met een totaal van EUR 187,10.

## <a name="see-also"></a>Zie ook

[De dagen van abonnementskosten verminderen](reduce-the-days-on-subscription-fees.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]