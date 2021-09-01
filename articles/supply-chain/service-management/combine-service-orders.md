---
title: Serviceorders combineren
description: U kunt serviceorders combineren.
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1eff71d49695f54520f983abacff658c771f1084d725f1f8bfef6c050df41dda
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766506"
---
# <a name="combine-service-orders"></a>Serviceorders combineren   

[!include [banner](../includes/banner.md)]


Als u serviceorderregels automatisch maakt in het formulier **Serviceovereenkomsten**, kunt u een van de volgende opties kiezen om op te geven hoe u ze wilt groeperen:

  - **Per serviceovereenkomst**

  - **Per servicetaak**

  - **Per werknemer**

  - **Per serviceobject**

## <a name="example"></a>Voorbeeld

U maakt een serviceovereenkomst waarvan de begindatum 31-03-2007 is. In het veld **Serviceorders combineren** geeft u **Per serviceobject** op. Vervolgens maakt u de volgende serviceovereenkomstregels:

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
<th><p>Overeenkomstregelnummer</p></th>
<th><p>Transactietype</p></th>
<th><p>Omschrijving</p></th>
<th><p>Interval</p></th>
<th><p>Serviceobject</p></th>
<th><p>Begindatum</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>1</p></td>
<td><p><strong>Uur</strong></p></td>
<td><p>SAL1</p></td>
<td><p>Wekelijks</p></td>
<td><p>X-1</p></td>
<td><p>01-04-2007</p></td>
</tr>
<tr class="even">
<td><p>2</p></td>
<td><p><strong>Uur</strong></p></td>
<td><p>SAL2</p></td>
<td><p>Om de twee weken</p></td>
<td><p>X-2</p></td>
<td><p>01-04-2007</p></td>
</tr>
<tr class="odd">
<td><p>3</p></td>
<td><p><strong>Uur</strong></p></td>
<td><p>SAL3</p></td>
<td><p>Wekelijks</p></td>
<td><p>X-2</p></td>
<td><p>01-04-2007</p></td>
</tr>
</tbody>
</table>


U geeft geen tijdvensters voor de serviceovereenkomstregels op. Daarom blijven de serviceorderregels staan op de datum waarop ze zijn ingesteld.

Vervolgens genereert u vanuit het formulier **Serviceorders maken** serviceorderregels van 01-04-2007 tot 30-04-2007.

In totaal worden er tien serviceorders gemaakt. Omdat u de door u geselecteerde gecombineerde instelling **Per serviceobject** is, krijgen alle serviceorders die worden gemaakt alleen serviceorderregels met één specifiek serviceobject. Serviceorderregels die vanuit de serviceovereenkomst worden gegenereerd en dezelfde servicedatum en hetzelfde serviceobject hebben, worden gecombineerd tot één serviceorder.


> [!NOTE]
> <P>In dit voorbeeld heeft de kalender die in het formulier <STRONG>Parameters voor servicebeheer</STRONG> is opgegeven, geen gesloten dagen.</P>



Voor de aanvullende groepering van serviceorderregels tot serviceorders wordt uitgegaan van tijdvensters die u in de serviceovereenkomstregels opgeeft.

## <a name="see-also"></a>Zie ook

[Automatisch serviceorders maken](create-service-orders-automatically.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]