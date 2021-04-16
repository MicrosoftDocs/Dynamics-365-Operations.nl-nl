---
title: Controlebeleidsregels
description: U kunt een auditbeleid gebruiken om onkostenrapporten, leveranciersfacturen en inkooporders te beoordelen om zeker te zijn dat ze de beleidsregels die u maakt naleven. Alle regels die aan een auditbeleid zijn gekoppeld, worden in batchmodus uitgevoerd volgens een planning die u opgeeft.  Elke beleidsregel is een instantie van een beleidsregeltype. Voor elk beleidsregeltype, kan slechts één beleidsregel tegelijkertijd actief zijn.
author: panolte
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1297f405e57c2de4f42f05f78ef52b2d763f0f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821980"
---
# <a name="audit-policy-rules"></a>Controlebeleidsregels

[!include [banner](../includes/banner.md)]

U kunt een auditbeleid gebruiken om onkostenrapporten, leveranciersfacturen en inkooporders te beoordelen om zeker te zijn dat ze de beleidsregels die u maakt naleven. Alle regels die aan een auditbeleid zijn gekoppeld, worden in batchmodus uitgevoerd volgens een planning die u opgeeft.  Elke beleidsregel is een instantie van een beleidsregeltype. Voor elk beleidsregeltype, kan slechts één beleidsregel tegelijkertijd actief zijn. 

<a name="queries-and-query-types"></a>Query's en querytypen
-----------------------

Wanneer u een auditbeleidsregel maakt, selecteert u eerst een beleidsregeltype. Het beleidsregeltype specificeert de AOT-query (Application Object Tree) die u wilt gebruiken als uitgangspunt voor het maken van de beleidsregel. Het specificeert ook het querytype dat u voor de beleidsregel moet gebruiken. De query bepaalt het brondocument waarvoor de beleidsregel een beoordeling uitvoert. Het specificeert ook de velden in het brondocument dat zowel de rechtspersoon identificeert als de te gebruiken datum wanneer documenten voor een audit worden geselecteerd. Met het querytype worden de standaardvelden op de querypagina en op de pagina Controlebeleidsregel bepaald. De volgende tabel geeft de beschikbare querytypen voor auditbeleidsregels weer.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Querytype</th>
<th>Doel</th>
<th>Meer informatie</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Voorwaardelijk</td>
<td>Brondocumentkenmerken beoordelen op basis van opgegeven waarden.</td>
<td></td>
</tr>
<tr class="even">
<td>Samenvoegen</td>
<td>Beoordeel meerdere brondocumenten of brondocumentregels op basis van een beleidsregel door numerieke waarden samen te voegen.</td>
<td></td>
</tr>
<tr class="odd">
<td>Bemonstering</td>
<td>Selecteer willekeurig een opgegeven percentage van de brondocumenten om dit op beleidsovertredingen te beoordelen.</td>
<td>Wanneer u deze optie selecteert, geeft u op de pagina Controlebeleidsregel het percentage documenten op dat willekeurig moet worden geselecteerd voor controle.</td>
</tr>
<tr class="even">
<td>Dupliceren</td>
<td>Brondocumenten beoordelen om te bepalen of ze dubbele vermeldingen bevatten in opgegeven velden.</td>
<td>Wanneer u deze optie selecteert, geeft u op de pagina Controlebeleidsregel het aantal dagen op dat u wilt toevoegen aan het begin van het datumbereik van de documentselectie wanneer documenten op dubbele vermeldingen worden gecontroleerd.</td>
</tr>
<tr class="odd">
<td>Zoeken in lijst</td>
<td>Brondocumenten beoordelen op specifieke vermeldingen.</td>
<td>Het basisdocument van de query bepaalt welk document wordt gecontroleerd. De query moet een lijstquery zijn die een verwijzing bevat naar de tabel dirpartytable. Deze optie kan alleen worden gebruikt met de volgende AOT-query´s:
<ul>
<li><span class="ui">AuditPolicyExpenseList</span> (Werknemers met bewaakte onkostennota)</li>
<li><span class="ui">AuditPolicyPurchList</span> (Leveranciers met bewaakte inkooporder)</li>
<li><span class="ui">AuditPolicyVendInvoiceList</span> (Leveranciers met bewaakte leveranciersfactuur)</li>
</ul>
Als u deze optie selecteert, geeft u de gecontroleerde entiteiten op de pagina Controlebeleidsregel op.</td>
</tr>
<tr class="even">
<td>Zoeken op trefwoord</td>
<td>Brondocumenten beoordelen om te bepalen of ze bepaalde woorden bevatten.</td>
<td>Als u deze optie selecteert, voert u de woorden in waarnaar u wilt zoeken op de pagina Controlebeleidsregel. De pagina Controlebeleidsregel bevat ook opties waarmee u de tabellen en velden kunt opgeven die u wilt controleren op de woorden die u hebt ingevoerd.</td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a>Gezamenlijke parameters
Alle beleidsregels voor een specifiek auditbeleid delen dezelfde batchparameters en hetzelfde datumbereik voor documentselectie. Deze parameters worden voor het beleid opgegeven op de pagina Extra opties.



<a name="additional-resources"></a>Aanvullende resources
--------

[Overtredingen van controlebeleid en voorbeelden](audit-policy-violations-cases.md)
[Auditbeleid voor brondocumenten definiëren](tasks/define-audit-policies-source-documents.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]