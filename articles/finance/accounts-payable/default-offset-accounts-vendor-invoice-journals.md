---
title: Standaardtegenrekeningen voor leveranciersfactuur- en factuurgoedkeuringsjournalen
description: Gebruik dit artikel om te bepalen waar u het beste standaardrekeningen voor factuurjournalen kunt toewijzen.
author: abruer
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.form: LedgerJournalTable
ms.openlocfilehash: ed75e0a3b9994d061e94d07ffcc43e3b73bec55e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281667"
---
# <a name="default-offset-accounts-for-vendor-invoice-and-invoice-approval-journals"></a>Standaardtegenrekeningen voor leveranciersfactuur- en factuurgoedkeuringsjournalen

[!include [banner](../includes/banner.md)]

Standaardtegenrekeningen worden gebruikt op de volgende pagina's voor leveranciersfactuurjournalen:

-   Factuurjournaal
-   Factuurgoedkeuringsjournaal

Gebruik de volgende tabel om u te helpen kiezen waar u het beste standaardrekeningen voor factuurjournalen kunt toewijzen.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Geef hier standaardrekeningen op</th>
<th>Waar standaardrekeningen worden opgegeven</th>
<th>Hoe deze optie de verwerking beïnvloedt</th>
<th>Wanneer u deze optie moet gebruiken</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Leveranciersgroep</strong> – Stel standaardtegenrekeningen in voor leveranciersgroepen op de pagina <strong>Instellen van standaardaccount</strong>, die u vanaf de pagina <strong>Leveranciersgroepen</strong> kunt openen.</td>
<td><ul>
<li>Leveranciersrekening</li>
<li>Journaalboekingen voor leveranciersrekeningen in de leveranciersgroep, als standaardrekeningen niet zijn opgegeven voor leveranciersrekeningen</li>
</ul></td>
<td>De standaardtegenrekeningen voor leveranciersgroepen worden weergegeven als standaardtegenrekeningen voor leveranciers op de pagina <strong>Instellen van standaardaccount</strong>. U kunt deze pagina openen vanaf de lijstpagina <strong>Alle leveranciers</strong>.</td>
<td>Gebruik deze optie als u normaal gesproken betaalt voor dezelfde typen artikelen van dezelfde leveranciersgroepen.</td>
</tr>
<tr class="even">
<td><strong>Leverancierrekening</strong> – Stel standaardtegenrekeningen in voor leverancierrekeningen op de pagina <strong>Instellen van standaardaccount</strong>, die u vanaf de pagina <strong>Leveranciers</strong> kunt openen.</td>
<td>Journaalboekingen voor de leveranciersrekening</td>
<td>De standaardtegenrekeningen voor leveranciersrekeningen worden als standaardtegenrekeningen voor journaalboekingen weergegeven voor de leveranciersrekening.</td>
<td>Gebruik deze optie als u normaal gesproken betaalt voor dezelfde typen artikelen van dezelfde leveranciers.</td>
</tr>
<tr class="odd">
<td><strong>Journaalnamen</strong> – Stel standaardtegenrekeningen in voor journalen op de pagina <strong>Journaalnamen</strong>. Selecteer de optie <strong>Vaste tegenrekening</strong>. Merk op dat u &#39;geen standaardtegenrekeningen op journaalnamen kunt opgeven als het journaaltype van de journaalnamen of <strong>Facturenregister</strong> of <strong>Goedkeuring</strong> is.</td>
<td><ul>
<li>Journaalkop die de journaalnaam gebruikt</li>
<li>Journaalboekingen in journalen die de journaalnaam gebruiken</li>
</ul></td>
<td>Als de optie <strong>Vaste tegenrekening</strong> op de pagina <strong>Journaalnamen</strong> is geselecteerd, krijgt de tegenrekening van de journaalnaam voorrang op de standaardtegenrekening voor de leverancier of leveranciersgroep.</td>
<td>Gebruik deze optie om journalen in te stellen voor specifieke kosten en uitgaven die aan specifieke rekeningen worden aangerekend, ongeacht wie de leverancier of leveranciersgroep is waarvan de leverancier deel uitmaakt.</td>
</tr>
<tr class="even">
<td><strong>Journaalnamen</strong> – Stel standaardtegenrekeningen in voor journalen op de pagina <strong>Journaalnamen</strong>. Schakel de optie <strong>Vaste tegenrekening</strong> uit. Merk op dat u geen standaardtegenrekeningen op journaalnamen kunt opgeven als het journaaltype van de journaalnamen of <strong>Facturenregister</strong> of <strong>Goedkeuring</strong> is.</td>
<td><ul>
<li>Journaalkoptekst</li>
<li>Journaalboekingen in journalen die de journaalnaam gebruiken</li>
</ul></td>
<td>Deze standaardboekingen worden gebruikt op pagina's voor journaalkopteksten, en de tegenrekening op de pagina voor de journaalkoptekst wordt als standaardboeking gebruikt op de pagina's voor journaalboekstukken. Standaardrekeningen op de pagina <strong>Journaalnamen </strong>worden alleen gebruikt als er geen standaardrekeningen zijn ingesteld voor de leveranciersrekening.</td>
<td>Gebruik deze optie om standaardrekeningen in te stellen die worden gebruikt wanneer geen standaard tegenrekening voor de leverancier is toegewezen.</td>
</tr>
<tr class="odd">
<td><strong>Journaalkoptekst</strong> – Stel een standaardtegenrekening in die een journaal kan gebruiken als standaardboeking op de pagina's voor journaalboekstukken. Merk op dat u geen standaardtegenrekeningen op de journaalkoptekst kunt opgeven als het journaaltype van de journaalnamen of <strong>Facturenregister</strong> of <strong>Goedkeuring</strong> is.</td>
<td>Journaalboekingen in het journaal</td>
<td>De standaard tegenrekening voor een journaal wordt gebruikt als de standaardboeking op de pagina's voor journaalboekstukken.</td>
<td>Gebruik deze optie om het invoeren van gegevens te versnellen als de meeste boekingen in een journaal dezelfde tegenrekening hebben.</td>
</tr>
</tbody>
</table>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
