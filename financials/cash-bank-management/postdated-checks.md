---
title: Gepostdateerde cheques
description: "Dit artikel biedt informatie over ondersteuning voor gepostdateerde cheques in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. Gepostdateerde cheques zijn cheques die worden uitgegeven om betalingen op een datum in de toekomst uit te voeren en te ontvangen. Daarom kan de cheque pas op de opgegeven datum worden geïnd."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: f7cf2b7996d113f0f883b39f3603de8236e8ad2c
ms.contentlocale: nl-nl
ms.lasthandoff: 06/20/2017


---

# <a name="postdated-checks"></a>Gepostdateerde cheques

[!include[banner](../includes/banner.md)]


Dit artikel biedt informatie over ondersteuning voor gepostdateerde cheques in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition. Gepostdateerde cheques zijn cheques die worden uitgegeven om betalingen op een datum in de toekomst uit te voeren en te ontvangen. Daarom kan de cheque pas op de opgegeven datum worden geïnd.

Microsoft Dynamics 365 for Finance and Operations ondersteunt de volledige beheercyclus voor gepostdateerde cheques in Klanten en in Leveranciers, zoals u in de volgende tabel ziet.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scenario</th>
<th>Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Gepostdateerde cheques instellen</td>
<td>U moet een nieuwe betalingsmethode instellen en de betalingsroutine voor speciale rekeningen opgeven voor uitgegeven cheques, ontvangen cheques en bronbelasting.</td>
</tr>
<tr class="even">
<td>Een gepostdateerde cheque voor een leverancier registreren en boeken</td>
<td>Registreer de details van een gepostdateerde cheque die u aan een leverancier uitschrijft. Wanneer de betaling wordt geboekt, wordt de leveranciersaansprakelijkheid erkend, maar wordt de bankrekening nog niet gecrediteerd. In plaats daarvan wordt hiervoor een speciale rekening gebruikt.</td>
</tr>
<tr class="odd">
<td>Een gepostdateerde cheque voor een klant registreren en boeken</td>
<td>Registreer de gegevens van een gepostdateerde cheque die u van een klant ontvangt. Wanneer de betaling wordt geboekt, wordt het klanttegoed wel gecrediteerd, maar wordt de bankrekening nog niet gedebiteerd. In plaats daarvan wordt hiervoor een speciale rekening gebruikt.</td>
</tr>
<tr class="even">
<td>Een vervangende gepostdateerde cheque voor een klant of leverancier registreren en boeken</td>
<td>
Als uw originele cheque voor een leverancier of klant verloren of beschadigd is geraakt, kunt u een vervangende gepostdateerde cheque uitgeven. Wanneer u de gegevens van de cheque registreert, geeft u een referentie naar de originele cheque op en geeft u aan dat de nieuwe cheque de originele cheque vervangt. U kunt de vervangende cheque ook boeken.</td>
</tr>
<tr class="odd">
<td>Een gepostdateerde cheque van een klant overboeken naar een leverancier</td>
<td>Wanneer u een gepostdateerde cheque van een klant ontvangt, kunt u die cheque als betaling naar een leverancier overboeken.</td>
</tr>
<tr class="even">
<td>Een gepostdateerde cheque voor een klant of leverancier vereffenen</td>
<td>Vereffen een gepostdateerde cheque die op een overbruggingsrekening voor een klant of leverancier is geboekt wanneer de cheque eindelijk vervalt. Als de cheque wordt vereffend, wordt de debitering of creditering eindelijk uitgevoerd voor de speciale rekening die eerder is gebruikt.</td>
</tr>
<tr class="odd">
<td>Een gepostdateerde cheque voor een leverancier annuleren</td>
<td>U kunt een geboekte gepostdateerde cheque in dergelijke situaties annuleren: de cheque wordt geretourneerd door de bank.
- De cheque is toegepast op een verkeerde factuur.
- De cheque is contant betaald.
</td>
</tr>
<tr class="even">
<td>Betaling voor een gepostdateerde cheque stoppen</td>
<td>U kunt de betaling stopzetten voor een gepostdateerde cheque die aan een leverancier is uitgeschreven, bijvoorbeeld omdat er sprake is van onvoldoende fondsen, omdat de voorwaarden van de overeenkomst met de leverancier zijn gewijzigd, omdat de leverancier defecte goederen heeft geleverd of omdat er goederen aan de leverancier zijn geretourneerd. Het is alleen mogelijk om de betaling stop te zetten voor cheques die niet zijn verrekend.</td>
</tr>
</tbody>
</table>







