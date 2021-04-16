---
title: Mechanisme voor omgekeerde toeslagen van btw/GST-schema
description: In dit onderwerp wordt uitgelegd hoe u de omgekeerde toeslag instelt voor Europese landen, Saudi-Arabië en Singapore.
author: epodkolz
ms.date: 10/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Saudi Arabia, Spain, Sweden, United Kingdom, Singapore, Bahrain, Kuwait, Oman, Qatar
ms.author: epodkolz
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: b59be8b395826914e8196009c339c2ced5a4debf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818301"
---
# <a name="reverse-charge-mechanism-for-vatgst-scheme"></a>Mechanisme voor omgekeerde toeslagen van btw/GST-schema

[!include [banner](../includes/banner.md)]

Dit onderwerp beschrijft een algemene aanpak voor het instellen van de functionaliteit voor omgekeerde toeslagen voor landen/regio's die de btw- of GST-schema's aannemen.
                                                                                 
De beschikbaarheid van de land/regiofunctionaliteit wordt beheerd door de volgende functies in de werkruimte **Functiebeheer**.

| Functie                                              | Land/regio                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Geen specifieke functie                                | Oostenrijk </br>België </br>Bulgarije </br>Kroatië </br>Cyprus </br>Tsjechische Republiek </br>Denemarken  </br>Estland  </br>Finland  </br>Frankrijk  </br>Duitsland  </br>Hongarije  </br>IJsland  </br>Ierland  </br>Italië  </br>Letland  </br>Liechtenstein  </br>Litouwen  </br>Luxemburg  </br>Nederland  </br>Noorwegen Polen </br>Portugal </br>Roemenië  </br>Saoedi-Arabië </br>Singapore  </br>Slowakije  </br>Slovenië  </br>Spanje  </br>Zweden  </br>Zwitserland  </br>Verenigd Koninkrijk  </br>Verenigde Arabische Emiraten |
| Omgekeerde toeslag voor extra landen            | Bahrein  </br>Koeweit  </br>Oman  </br>Qatar                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Mechanisme voor omgekeerde toeslag voor btw/GST-schema inschakelen | Alle andere landen/regio's, met uitzondering van:  </br>Brazilië  </br>India  </br>Rusland                                                                                                                                                                                                                                                                                                                                                                                         |
 
 Zie de [functie Mechanisme voor omgekeerde toeslag voor btw/GST-schema inschakelen](#enable-reverse-charge) verderop in dit onderwerp voor meer informatie.

Omgelegde toeslag is een btw-schema dat de verantwoordelijkheid voor de boekhouding en aangifte van btw verlegt van de verkoper naar de koper van goederen en/of diensten. Daarom geven ontvangers van goederen en/of diensten zowel de te betalen btw (in de rol van verkoper) en de te vorderen btw (in de rol van inkoper) in hun btw-aangifte aan.

Daarom wordt het schema Omgekeerde toeslag in sommige landen of regio's alleen voor bepaalde goederen en/of diensten geïmplementeerd en zijn er aanvullende voorwaarden of drempels ten aanzien van verkoopbedragen. In andere landen of regio's hangt de verantwoordelijkheid voor btw-betaling af van de status van de leverancier en de koper. Als de koper btw moet afdragen, moet dit duidelijk worden aangegeven op de factuur die de leverancier uitgeeft. De factuur moet bijvoorbeeld de woorden 'Omgekeerde toeslag' bevatten en moet aangeven welke posities onder het schema Omgekeerde toeslag vallen. 

Als u de omgekeerde toeslag wilt toepassen, moet u de volgende instellingen uitvoeren.

## <a name="set-up-sales-tax-codes"></a>Btw-codes instellen
Het wordt aangeraden afzonderlijke btw-codes voor verkoopbewerkingen en inkoopbewerkingen te gebruiken.

<table>
<body>
<tr>
<td><strong>Btw-code voor verkoop</strong></td>
<td>Maak een btw-code voor verkoopbewerkingen waarop de omgekeerde toeslag van toepassing is (<strong>Belasting</strong> &gt; <strong>Indirecte belastingen</strong> &gt; <strong>Btw</strong> &gt; <strong>Btw-codes</strong>).
</td>
</tr>
<tr>
<td><strong>Btw-code voor inkoop</strong></td>
<td><p>Maak positieve en negatieve btw-codes voor de omgekeerde toeslag voor inkopen (<strong>Belasting</strong> &gt; <strong>Indirecte belastingen</strong> &gt; <strong>Btw</strong> &gt; <strong>Btw-codes</strong>).</p>
<ol>
<li>Maak een btw-code met een positieve waarde.</li>
<li>Maak een btw-code met een negatieve waarde. Stel de optie <strong>Negatief btw-percentage toestaan</strong> in op <strong>Ja</strong>.
U moet deze negatieve btw-code toewijzen aan een btw-groep voor artikelen en deze btw-groep vervolgens toewijzen aan de artikelen waarop de omgekeerde toeslag van toepassing is.</li>
</ol>
<p>Zie het volgende gedeelte &quot;Btw-groepen en artikel-btw-groepen instellen&quot; voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

## <a name="set-up-sales-tax-groups-and-item-sales-tax-groups"></a><a name="sales-tax-item-sales-tax-groups"></a>Btw-groepen en artikel-btw-groepen instellen
Het wordt aangeraden afzonderlijke btw-groepen voor verkoopbewerkingen en inkoopbewerkingen te gebruiken.

<table>
<tr>
<td><strong>Btw-groepen voor verkoop</strong></td>
<td>Maak een btw-groep voor verkoopbewerkingen waarop de omgekeerde toeslag van toepassing is (<strong>Belasting</strong> &gt; <strong>Indirecte belastingen</strong> &gt; <strong>Btw</strong> &gt; <strong>Btw-groepen</strong>). Neem op het tabblad <strong>Instellen</strong> de btw-code op voor de omgekeerde toeslag in deze groep. Schakel de selectievakjes <strong>Vrijstelling</strong> en <strong>Omgekeerde toeslag</strong> voor de btw-code in.</td>
</tr>
<tr>
<td><strong>Btw-groepen voor inkoop</strong></td>
<td>Maak een btw-groep voor inkoopbewerkingen waarop de omgekeerde toeslag van toepassing is (<strong>Belasting</strong> &gt; <strong>Indirecte belastingen</strong> &gt; <strong>Btw</strong> &gt; <strong>Btw-groepen</strong>). Neem op het tabblad <strong>Instellen</strong> zowel positieve als negatieve btw-codes op in deze groep. Schakel het selectievakje <strong>Omgekeerde toeslag</strong> in voor de btw-code met een negatieve waarde.</td>
</tr>
<tr>
<td><strong>Btw-groepen voor artikel</strong></td>
<td>Maak de btw-groep voor artikelen met de btw-code die een negatieve waarde heeft (<strong>Belasting</strong> &gt; <strong>Indirecte belastingen</strong> &gt; <strong>Btw</strong> &gt; <strong>Btw-groepen voor artikel</strong>). U moet de standaard-btw-groep voor artikelen toewijzen aan de producten en categorieën waarop de omgekeerde toeslag van toepassing is.</td>
</tr>
</table>

## <a name="set-up-reverse-charge-item-groups"></a><a name="reverse-charge-item-group"></a>Artikelgroepen voor omgekeerde toeslagen instellen
Op de pagina **Artikelgroepen omgekeerde toeslag** (**Belasting** &gt; **Instellen** &gt; **Btw** &gt; **Artikelgroepen omgekeerde toeslag**) kunt u groepen producten of diensten of afzonderlijke producten of diensten definiëren, waarop de omgekeerde toeslag kan worden toegepast. Definieer voor elke artikelgroep voor omgekeerde toeslag de lijst met artikelen, artikelgroepen en categorieën voor verkoop en/of inkoop.

## <a name="set-up-reverse-charge-rules"></a><a name="reverse-charge-rules"></a>Regels voor omgekeerde toeslag instellen
Op de pagina **Regels omgekeerde toeslag** (**Belasting** &gt; **Instellen** &gt; **Btw** &gt; **Regels omgekeerde toeslag**) kunt u de toepasbaarheidsregels voor inkoop- en verkoopdoeleinden definiëren. U kunt een set toepasbaarheidsregels voor omgekeerde toeslag configureren. Stel voor elke regel de volgende velden in:

- **Documenttype**: selecteer **Inkooporder**, **Leveranciersfactuurjournaal**, **Verkooporder**, **Vrije-tekstfactuur**, **Klantfactuurjournaal** en/of **Leveranciersfactuur**.
- **Type land/regio van partner**: selecteer **Binnenlands**, **EU**, **GCC** of **Buitenlands**. U kunt ook **Alle** selecteren als de regel kan worden toegepast op alle handelspartners, ongeacht het land of regio van hun adres.
- **Binnenlands afleveradres**: schakel dit selectievakje in als u de regel wilt toepassen op leveringen binnen hetzelfde land of dezelfde regio. Dit selectievakje kan niet worden ingeschakeld voor de documenttypen **Leveranciersfactuurjournaal** en **Klantfactuurjournaal**.
- **Artikelgroep omgekeerde toeslag**: selecteer de groep waarop de regel kan worden toegepast.
- **Drempelbedrag** : het schema voor omgekeerde toeslag wordt alleen toegepast op een factuur als de waarde van artikelen en/of diensten die zijn opgenomen in de artikelgroep voor omgekeerde toeslag de limiet overschrijdt die u hier opgeeft.

U kunt ook de velden **Ingangsdatum** en **Verloopdatum** gebruiken om de periode te definiëren wanneer de regel van kracht is.

U kunt bovendien opgeven of een melding wordt weergegeven en de documentregel wordt bijgewerkt met de btw-groep voor omgekeerde toeslag als aan de voorwaarde voor die documentregel wordt voldaan. De volgende opties zijn beschikbaar:

- **Geen**: de documentregel wordt niet bijgewerkt.
- **Vragen**: er wordt een melding weergegeven om te bevestigen dat de omgekeerde toeslag kan worden toegepast.
- **Instellen**: de documentregel wordt bijgewerkt zonder aanvullende melding.

## <a name="set-up-countryregion-properties"></a><a name="Set-up-Country/region-properties"></a>Land-/regio-eigenschappen instellen
Stel op de pagina **Parameters buitenlandse handel** (**Belasting** &gt; **Instellen** &gt; **Btw** &gt; **Buitenlandse handel** &gt; **Parameters buitenlandse handel**) op het tabblad **Land-/regio-eigenschappen** het land/de regio van de huidige rechtspersoon in op *Binnenlands*. Stel het **land-/regiotype** van de landen/regio's in de EU die deelnemen aan de EU-handel met de huidige rechtspersoon in op *EU*. Stel het **land-/regiotype** van de landen/regio's in de GCC die deelnemen aan de GCC-handel met de huidige rechtspersoon in op *GCC*.

## <a name="set-up-default-parameters"></a>Standaardparameters instellen
Als u de functionaliteit voor omgekeerde toeslag wilt inschakelen, stelt u op de pagina **Grootboekparameters** op het tabblad **Omgekeerde toeslag** de optie **Omgekeerde toeslag inschakelen** in op **Ja**. Selecteer in de velden **Btw-groep van inkooporder** en **Btw-groep van verkooporder** de standaard-btw-groepen in. Wanneer aan een toepasbaarheidsvoorwaarde voor omgekeerde toeslag wordt voldaan, wordt de verkoop- of inkooporderregel bijgewerkt met deze btw-groepen.

## <a name="reverse-charge-on-a-sales-invoice"></a><a name="reverse-charge-sale"></a>Omgekeerde toeslag op een verkoopfactuur
Voor verkoop op basis van het schema Omgekeerde toeslag brengt de verkoper geen btw in rekening. In plaats daarvan worden op de factuur zowel de artikelen waarop de btw voor omgekeerde toeslag van toepassing is, als het totaalbedrag van de btw voor omgekeerde toeslag aangegeven.

Wanneer een verkoopfactuur met omgekeerde toeslag wordt geboekt, hebben de btw-transacties een btw-richting en nul btw van **Te betalen btw** en zijn de selectievakjes **Omgekeerde toeslag** en **Vrijgesteld** ingeschakeld.

## <a name="reverse-charge-on-a-purchase-invoice"></a><a name="reverse-charge-purchase"></a>Omgekeerde toeslag op een inkoopfactuur
Voor inkopen op basis van het schema Omgekeerde toeslag fungeert de inkoper die de factuur met de omgekeerde toeslag ontvangt, als koper en verkoper voor btw-boekhouddoeleinden.

Wanneer een inkoopfactuur met omgekeerde toeslag wordt geboekt, worden twee btw-transacties gemaakt. Eén transactie heeft de btw-richting **Te ontvangen btw**. De andere transactie heeft de btw-richting **Te betalen btw** en het selectievakje **Omgekeerde toeslag** is ingeschakeld.

In de volgende schermopname heeft één transactie de richting **Te ontvangen btw** en de andere transactie de richting **Te betalen btw**. 

![Geboekte btw](media/apac-sau-posted-sales-tax.png)

## <a name="enable-reverse-charge-mechanism-for-vatgst-scheme-feature"></a><a name="enable-reverse-charge"></a>De functie Mechanisme voor omgekeerde toeslagen voor btw/GST-schema inschakelen
Zoek de functie in de werkruimte **Functiebeheer** en selecteer **Inschakelen**.

Nadat u de functie hebt ingeschakeld, is het tabblad **Omgekeerde toeslag** beschikbaar bij alle rechtspersonen. Schakel de functionaliteit voor terugboeken voor een rechtspersoon in door de optie **Omgekeerde toeslagen inschakelen** in te stellen op **Ja**.

De volgende pagina's en menuopdrachten die betrekking hebben op de instellingen van de functie zijn beschikbaar:
 - **Artikelgroepen voor omgekeerde toeslagen** (**Belasting** > **Instellingen** > **Btw** > **Artikelgroepen voor omgekeerde toeslag**). Zie [Artikelgroepen voor omgekeerde toeslagen instellen](#reverse-charge-item-group) voor meer informatie.
 - **Regels voor omgekeerde toeslagen** (**Belasting** > **Instellen** > **Btw** > **Regels voor omgekeerde toeslagen**). Zie [Regels voor omgekeerde toeslag instellen](#reverse-charge-rules).
 - **Parameters voor buitenlandse handel** (**Belasting** > **Instellingen** > **Btw** > **Buitenlandse handel** > **Parameters voor buitenlandse handel**). Zie [Land-/regio-eigenschappen instellen](#Set-up-Country/region-properties).

Het selectievakje **Omgekeerde toeslag** is beschikbaar op de pagina's **Btw-groep** en **Geboekte btw**. Zie [Btw-groepen en artikelgroepen voor btw instellen](#sales-tax-item-sales-tax-groups), [Omgekeerde toeslag op een verkoopfactuur](#reverse-charge-sale) en [Omgekeerde toeslag op een verkoopfactuur](#reverse-charge-purchase).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]