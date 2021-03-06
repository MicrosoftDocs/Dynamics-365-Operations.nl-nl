---
title: Voorbeeld van reductiedagen
description: Voorbeeld van reductiedagen.
author: ShylaThompson
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
ms.openlocfilehash: 90a2efff0add508ddb3d750bb3ca27ea35bf113a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836057"
---
# <a name="reduction-days-example"></a>Voorbeeld van reductiedagen 

[!include [banner](../includes/banner.md)]


U hebt een abonnementstransactie gemaakt voor het onderhoudsabonnement van een klant dat wordt beschreven in de volgende tabel.

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