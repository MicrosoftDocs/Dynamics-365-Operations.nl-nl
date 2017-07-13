---
title: Omgekeerde toeslag | Microsoft Docs
description: In dit onderwerp wordt uitgelegd hoe u de omgekeerde toeslag instelt voor Europese landen.
author: epodkolz
manager: AnnBe
ms.date: 05/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 6cb473962f40ed9ef2f5f807f089098764f47009
ms.openlocfilehash: b3c94fa73410d9bdcaaec11dee04a7a239e4d45a
ms.contentlocale: nl-nl
ms.lasthandoff: 06/14/2017

---

# <a name="reverse-charge-vat"></a>Omgekeerde toeslag
In dit onderwerp wordt een generieke aanpak beschreven voor het instellen van de omgekeerde toeslag voor Europese landen.

Omgelegde toeslag is een btw-schema dat de verantwoordelijkheid voor de boekhouding en aangifte van btw verlegt van de verkoper naar de koper van goederen en/of diensten. Daarom geven ontvangers van goederen en/of diensten zowel de te betalen btw (in de rol van verkoper) en de te vorderen btw (in de rol van inkoper) in hun btw-aangifte aan.

De EU-richtlijn van de Europese Unie laat lidstaten bepalen hoe de algemene vereisten worden aangepast aan de lokale vereisten. Daarom wordt het schema Omgekeerde toeslag in sommige landen alleen voor bepaalde goederen en/of diensten geïmplementeerd en zijn er aanvullende voorwaarden of drempels ten aanzien van verkoopbedragen. In andere landen hangt de verantwoordelijkheid voor btw-betaling af van de status van de leverancier en de koper. Als de koper btw moet afdragen, moet dit duidelijk worden aangegeven op de factuur die de leverancier uitgeeft. De factuur moet bijvoorbeeld de woorden 'Omgekeerde toeslag' bevatten en moet aangeven welke posities onder het schema Omgekeerde toeslag vallen. 

Als u de omgekeerde toeslag wilt toepassen, moet u de volgende instellingen uitvoeren.

## <a name="set-up-sales-tax-codes"></a>Btw-codes instellen
Het wordt aangeraden afzonderlijke btw-codes voor inkoopbewerkingen en verkoopbewerkingen te gebruiken.

<table>
<body>
<tr>
<td><strong>Btw-code voor verkoop</strong></td>
<td>Maak een btw-code voor verkoopbewerkingen waarop de omgekeerde toeslag van toepassing is (<strong>Belasting</strong> > <strong>Indirecte belastingen</strong> > <strong>Btw</strong> > <strong>Btw-codes</strong>).
</td>
</tr>
<tr>
<td><strong>Btw-code voor inkoop</strong></td>
<td><p>Maak positieve en negatieve btw-codes voor de omgekeerde toeslag voor inkopen (<strong>Belasting</strong> > <strong>Indirecte belastingen</strong> > <strong>Btw</strong> > <strong>Btw-codes</strong>).</p>
<ol>
<li>Maak een btw-code met een positieve waarde.</li>
<li>Maak een btw-code met een negatieve waarde. Stel de optie <strong>Negatief btw-percentage toestaan</strong> in op <strong>Ja</strong>.
U moet deze negatieve btw-code toewijzen aan een btw-groep voor artikelen en deze btw-groep vervolgens toewijzen aan de artikelen waarop de omgekeerde toeslag van toepassing is.</li>
</ol>
<p>Zie het volgende gedeelte Btw-groepen en artikel-btw-groepen instellen voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a>Btw-groepen en artikel-btw-groepen instellen
Het wordt aangeraden afzonderlijke btw-groepen voor inkoopbewerkingen en verkoopbewerkingen te gebruiken.

<table>
<tr>
<td><strong>Btw-groepen voor verkoop</strong></td>
<td>Maak een btw-groep voor verkoopbewerkingen waarop de omgekeerde toeslag van toepassing is (<strong>Belasting</strong> > <strong>Indirecte belastingen</strong> > <strong>Btw</strong> > <strong>Btw-groepen</strong>). Neem op het tabblad <strong>Instellen</strong> de btw-code op voor de omgekeerde toeslag in deze groep. Schakel de selectievakjes <strong>Vrijstelling</strong> en <strong>Omgekeerde toeslag</strong> voor de btw-code in.</td>
</tr>
<tr>
<td><strong>Btw-groepen voor inkoop</strong></td>
<td>Maak een btw-groep voor inkoopbewerkingen waarop de omgekeerde toeslag van toepassing is (<strong>Belasting</strong> > <strong>Indirecte belastingen</strong> > <strong>Btw</strong> > <strong>Btw-groepen</strong>). Neem op het tabblad <strong>Instellen</strong> zowel positieve als negatieve btw-codes op in deze groep. Schakel het selectievakje <strong>Omgekeerde toeslag</strong> in voor de btw-code met een negatieve waarde.</td>
</tr>
<tr>
<td><strong>Btw-groepen voor artikel</strong></td>
<td>Maak de btw-groep voor artikelen met de btw-code die een negatieve waarde heeft (<strong>Belasting</strong> > <strong>Indirecte belastingen</strong> > <strong>Btw</strong> > <strong>Btw-groepen voor artikel</strong>). U moet de standaard-btw-groep voor artikelen toewijzen aan de producten en categorieën waarop de omgekeerde toeslag van toepassing is.</td>
</tr>
</table>

## <a name="set-up-reverse-charge-groups"></a>Groepen voor omgekeerde toeslag instellen
Op de pagina **Artikelgroepen omgekeerde toeslag** (**Belasting** > **Instellen** > **Btw** > **Artikelgroepen omgekeerde toeslag**) kunt u groepen producten of diensten of afzonderlijke producten of diensten definiëren, waarop de omgekeerde toeslag kan worden toegepast. Definieer voor elke artikelgroep voor omgekeerde toeslag de lijst met artikelen, artikelgroepen en categorieën voor verkoop en/of inkoop.

## <a name="set-up-reverse-charge-rules"></a>Regels voor omgekeerde toeslag instellen
Op de pagina **Regels omgekeerde toeslag** (**Belasting** > **Instellen** > **Btw** > **Regels omgekeerde toeslag**) kunt u de toepasbaarheidsregels voor inkoop- en verkoopdoeleinden definiëren. U kunt een set toepasbaarheidsregels voor omgekeerde toeslag configureren. Stel voor elke regel de volgende velden in:

- **Documenttype**: selecteer **Inkooporder**, **Leveranciersfactuurjournaal**, **Verkooporder**, **Vrije-tekstfactuur**, **Klantfactuurjournaal** en/of **Leveranciersfactuur**.
- **Type land/regio van partner**: selecteer **Binnenlands**, **EU** of **Buitenlands**. U kunt ook **Alle** selecteren als de regel kan worden toegepast op alle handelspartners, ongeacht het land of regio van hun adres.
- **Binnenlands afleveradres**: schakel dit selectievakje in als u de regel wilt toepassen op leveringen binnen hetzelfde land of dezelfde regio. Dit selectievakje kan niet worden ingeschakeld voor de documenttypen **Leveranciersfactuurjournaal** en **Klantfactuurjournaal**.
- **Artikelgroep omgekeerde toeslag**: selecteer de groep waarop de regel kan worden toegepast.
- **Drempelbedrag** : het schema voor omgekeerde toeslag wordt alleen toegepast op een factuur als de waarde van artikelen en/of diensten die zijn opgenomen in de artikelgroep voor omgekeerde toeslag de limiet overschrijdt die u hier opgeeft.

U kunt de velden **Ingangsdatum** en **Verloopdatum** gebruiken om de periode te definiëren wanneer de regel van kracht is.

U kunt bovendien opgeven of een melding wordt weergegeven en de documentregel wordt bijgewerkt met de btw-groep voor omgekeerde toeslag als aan de voorwaarde voor die documentregel wordt voldaan. De volgende opties zijn beschikbaar:

- **Geen**: de documentregel wordt niet bijgewerkt.
- **Vragen**: er wordt een melding weergegeven om te bevestigen dat de omgekeerde toeslag kan worden toegepast.
- **Instellen**: de documentregel wordt bijgewerkt zonder aanvullende melding.

## <a name="set-up-default-parameters"></a>Standaardparameters instellen
Als u de functionaliteit wilt inschakelen, stelt u op de pagina **Grootboekparameters** op het tabblad **Omgekeerde toeslag** de optie **Omgekeerde toeslag inschakelen** in op **Ja**. Selecteer in de velden **Btw-groep van inkooporder** en **Btw-groep van verkooporder** de standaard-btw-groepen in. Wanneer aan een toepasbaarheidsvoorwaarde voor omgekeerde toeslag wordt voldaan, wordt de verkoop- of inkooporderregel bijgewerkt met deze btw-groepen.

## <a name="reverse-charge-on-a-sales-invoice"></a>Omgekeerde toeslag op een verkoopfactuur
Voor verkoop op basis van het schema Omgekeerde toeslag brengt de verkoper geen btw in rekening. In plaats daarvan worden op de factuur zowel de artikelen waarop de btw voor omgekeerde toeslag van toepassing is, als het totaalbedrag van de btw voor omgekeerde toeslag aangegeven.

Wanneer een verkoopfactuur met omgekeerde toeslag wordt geboekt, hebben de btw-transacties een btw-richting en nul btw van **Te betalen btw** en is het selectievakje **Omgekeerde toeslag** ingeschakeld.

## <a name="reverse-charge-on-a-purchase-invoice"></a>Omgekeerde toeslag op een inkoopfactuur
Voor inkopen op basis van het schema Omgekeerde toeslag fungeert de inkoper die de factuur met de omgekeerde toeslag ontvangt, als koper en verkoper voor btw-boekhouddoeleinden.

Wanneer een inkoopfactuur met omgekeerde toeslag wordt geboekt, worden twee btw-transacties gemaakt. Eén transactie heeft de btw-richting **Te ontvangen btw**. De andere transactie heeft de btw-richting **Te betalen btw** en het selectievakje **Omgekeerde toeslag** is ingeschakeld.

