---
title: Compensatieplannen
description: Managers Compensatie en emolumenten kunnen Compensatiebeheer gebruiken om plannen voor vaste en variabele compensatie voor de werknemers van de organisatie te beheren en te verwerken.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable, HcmCompensationWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: b773b12b7eb3a8a59627d011f2469a98c5dde58a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058915"
---
# <a name="compensation-plans"></a>Compensatieplannen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Managers Compensatie en emolumenten kunnen Compensatiebeheer gebruiken om plannen voor vaste en variabele compensatie voor de werknemers van de organisatie te beheren en te verwerken.

### <a name="introduction"></a>Introductie

Compensatiebeheer wordt gebruikt om de betaling van basisloon en beloningen te beheren. Het vaste basissalaris en verdiensteverhogingen van een werknemer worden via vaste compensatieplannen beheerd. De betaling van prestatiebeloningen, zoals bonusbetalingen, beloningen voor prestaties, aandelenopties, en subsidies en ook eenmalige beloningen, worden gecontroleerd door middel van plannen voor variabele compensatie. 

Werknemers kunnen aangemeld zijn voor een of meer plannen van beide typen. Een werknemer moet voldoen aan de volgende eisen om in aanmerking te komen voor inschrijving bij een compensatieplan:
-   De werknemer moet zijn toegewezen aan een actieve functie.
-   De werknemer moet voldoen aan de criteria die zijn opgesteld om in aanmerking te komen voor een compensatieplan.

## <a name="compensation-setup"></a>Instellen van compensatie
De volgende tabel geeft een overzicht van de onderdelen van het compensatieproces dat geïntegreerd kan worden bij het instellen van de compensatieplannen van uw bedrijf.

<table>
<thead>
<tr class="header">
<th>Onderdeel</th>
<th>Meer informatie...</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vastecompensatieacties</td>
<td>Acties voor vaste compensatie hebben twee doelen:
<ul>
<li>Acties kunnen het type informatie opgeven dat moet worden geregistreerd wanneer de compensatie van een werknemer wordt gewijzigd. U kunt bijvoorbeeld vereisen dat de reden van een wijziging, zoals een promotie of demotie, wordt geregistreerd.</li>
<li>Acties kunnen ervoor zorgen dat een berekening wordt toegepast wanneer vaste compensatieplannen worden verwerkt.  Acties van het type Eigen vermogen vergelijken bijvoorbeeld de betaling voor de werknemer met het minimumreferentiepunt voor het niveau van de werknemer en zorgen ervoor dat de werknemer minstens het minimumbedrag krijgt betaald.</li>
</ul></td>
</tr>
<tr class="even">
<td>Niveaus</td>
<td>Niveaus worden gekoppeld aan taken en eventuele functies die zijn gerelateerd aan een taakverwijzing. U kunt afzonderlijke niveaus voor de drie typen compensatieplannen maken: schaal, schijf en stap.</td>
</tr>
<tr class="odd">
<td>Bereikgebruiksmatrix</td>
<td>Een bereikgebruiksmatrix ondersteunt bij de overgang van werknemers naar het besturingspunt voor hun taken. Via bereikgebruik kunt u ook het loontariefvermogen in het bedrijf beheren, ongeacht de prestaties van een afzonderlijke werknemer of de algehele prestaties van het bedrijf. Werknemers die bijvoorbeeld lager worden betaald binnen hun bereik ontvangen een hogere procentuele toename dan werknemers die hoger in het bereik worden betaald. Op deze manier kunt u systematisch vermogensverschillen compenseren. Het bereikgebruik wordt als volgt berekend: (tarief vast salaris - bereik, Minimum) ÷ (bereik Maximum - bereik, Minimum).</td>
</tr>
<tr class="even">
<td>Referentiepuntinstellingen</td>
<td>Referentiepuntinstellingen zijn inclusief een aantal referentiepunten die bereikwaarden in een matrix weergeven. Elk bereik kan worden gekoppeld aan een betalingstarief. Schaalplannen hebben bijvoorbeeld vaak referentiepunten zoals Minimum, Middelpunt en Maximum.</td>
</tr>
<tr class="odd">
<td>Compensatiematrix</td>
<td>Een compensatiematrix is de set van referentiepunten en niveaus die u kunt gebruiken om een compensatiestructuur te maken.</td>
</tr>
<tr class="even">
<td>Compensatiestructuur</td>
<td>Een compensatiestructuur is een compensatiematrix waarin loontarieven zijn gekoppeld de referentiepunten voor elk niveau.</td>
</tr>
<tr class="odd">
<td>Geschiktheidsregels</td>
<td>Er worden geschiktheidsregels toegepast voor het identificeren van werknemers in specifieke taken, taakfuncties, taaktypen, afdelingen, vakbonden of compensatiegebieden waarvoor specifieke compensatieplannen gelden. U moet geschiktheidsregels voor plannen voor zowel variabele als vaste compensatie maken, om werknemers in een plan in te schrijven. Nadat u de geschiktheidsregels voor een compensatieplan hebt opgegeven, kunt u de niveaus definiëren die moeten worden gehanteerd voor de taken waarop het plan betrekking heeft.</td>
</tr>
<tr class="even">
<td>Betalingsfrequenties</td>
<td>Betalingsfrequenties worden gebruikt om de periode te definiëren waarvoor de compensatie is vastgelegd.  De betalingsfrequentie helpt u bijvoorbeeld inzicht te krijgen als het compensatiebedrag is opgegeven als een jaarsalaris versus een uurtarief. Betalingsfrequenties worden ook gebruikt voor het instellen van conversiefactoren om compensatiebedragen van maandelijks, wekelijks, tweewekelijks en per uur te converteren naar jaarlijkse frequentie.</td>
</tr>
<tr class="odd">
<td>Compensatieregio's</td>
<td>Compensatieregio's worden gebruikt voor het aangeven van werknemerscompensatie op basis van de locatie van de werkplek.</td>
</tr>
<tr class="even">
<td>Controlepunt</td>
<td>Met het controlepunt geeft u het optimale loontarief aan voor alle werknemers op een bepaald compensatieniveau. Voor salarisschaalstructuren zijn controlepunten meestal het midden van het bereik. Bandstructuren maken zelden gebruik van besturingspunten. U kunt het controlepunt van een plan voor vaste compensatie opgeven in het formulier Vastecompensatieplannen.</td>
</tr>
<tr class="odd">
<td>Taakfuncties</td>
<td>Taakfuncties worden gebruikt om compensatieplannen te classificeren en te filteren voor specifieke taken.</td>
</tr>
<tr class="even">
<td>Taaktypen</td>
<td>Taakfuncties worden gebruikt om compensatieplannen te classificeren en te filteren voor specifieke taken.</td>
</tr>
<tr class="odd">
<td>Variabelecompensatietypen</td>
<td>Variabele compensatietypen, zoals beloningen in aandelen of bonussen in contant geld, worden ingesteld in variabele compensatieplannen.</td>
</tr>
<tr class="even">
<td>Compensatierasters</td>
<td>Compensatierasters bevatten de compensatiestructuur.  Compensatierasters kunnen worden gebruikt door een of meer compensatieplannen.</td>
</tr>
<tr class="odd">
<td>Prestatieplannen</td>
<td>Prestatieplannen worden gebruikt voor het koppelen van prestatie aan een toewijzingsmatrix, zodat u het plan kunt gebruiken bij de strategie van prestatieloon.</td>
</tr>
<tr class="even">
<td>Prestatieclassificaties</td>
<td>Prestatieclassificaties worden in compensatieplannen gebruikt om het bedrag van een verdienstebeloning of prestatiebeloning vast te stellen.</td>
</tr>
</tbody>
</table>

## <a name="process-events"></a>Procesgebeurtenissen
Een procesgebeurtenis berekent compensatiegegevens voor een bepaalde periode voor alle werknemers die zijn ingeschreven in een of meer vaste of variabele compensatieplannen. U kunt een procesgebeurtenis herhaaldelijk uitvoeren om de berekende compensatieresultaten te testen of bij te werken.

<a name="compensation-events"></a>Compensatiegebeurtenissen
-------------------

Telkens wanneer een procesgebeurtenis wordt uitgevoerd, wordt een compensatiegebeurtenis gemaakt.  Compensatiegebeurtenissen bevatten de resultaten van het compensatieproces voor elke werknemer die is opgenomen in deze procesgebeurtenis.  Wanneer de berekeningen juist zijn, kunt u de compensatiegebeurtenis laden om de compensatierecords bij te werken voor de werknemers op wie de procesgebeurtenis van invloed is.

## <a name="recommendations"></a>Aanbevelingen
Nadat u een procesgebeurtenis uitvoert, kunt u aanbevelingen doen voor aanpassingen aan de toename van de verdiensten van een werknemer of een toekenningsbedrag op basis van de berekende richtlijnen van de procesgebeurtenis. Als u aanbevelingen voor werknemers wilt doen, moet u aanbevelingen inschakelen wanneer u compensatieplannen instelt of wanneer u de procesgebeurtenis instelt.





[!INCLUDE[footer-include](../includes/footer-banner.md)]