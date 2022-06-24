---
title: Beginselen van kortingsreductie
description: In dit artikel wordt beschreven hoe u reductieprincipes kunt instellen. Reductieprincipes bepalen het gedrag als meerdere kortingen van toepassing zijn op hetzelfde artikel of dezelfde transactie.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5ccf8dc555862d87e8dc6f5b46e3045c72e88945
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8844817"
---
# <a name="rebate-reduction-principles"></a>Kortingsreductieprincipes

[!include [banner](../includes/banner.md)]

U kunt kortingsbeheerdeals groeperen in *reductieprincipes* om andere voorzieningen te reduceren die aan een artikel zijn gekoppeld en/of om de resulterende waarden van kortingsberekeningen te verlagen. Nadat de kortingsreductieprincipes zijn ingesteld, kunt u deze desgewenst toewijzen aan de regels van uw kortingsbeheerdeals.

De regels voor kortingsreductieprincipes zijn alleen van toepassing als kortingsdeals elkaar overlappen. Hierdoor kunnen meerdere kortingen worden toegekend in situaties waarin geen meerdere kortingen verschuldigd zijn.

## <a name="manage-rebate-reduction-principles"></a>Kortingsreductieprincipes beheren

Als u kortingsreductieprincipes wilt gebruiken, gaat u naar **Kortingsbeheer \> Instellen \> Kortingsreductieprincipes**. Vervolgens kunt u de knoppen in het actiedeelvenster gebruiken om naar behoefte reductieprincipes toe te voegen en te verwijderen. Voor elk principe stelt u de velden in zoals beschreven in de volgende tabel.

| Veld | Beschrijving |
|---|---|
| Kortingsreductieprincipe | Voer een unieke naam in voor het kortingsreductieprincipe. |
| Beschrijving | Voer een beschrijving in voor het kortingsreductieprincipe. |
| Reductie toepassen | Schakel dit selectievakje in om een reductiebasis toe te passen op kortingen die bij dit kortingsreductieprincipe horen. |
| Reductiebasis | Als u het selectievakje **Reductie toepassen** hebt ingeschakeld, selecteert u de reductiebasis (*Voorziening*, *Kortingen* of *Beide*). Als u *Beide* selecteert als zowel een voorziening als een korting is geboekt voor een vorige deal, wordt alleen de korting toegepast. |
| Uitsluiten van reductie | Als dit selectievakje is ingeschakeld, worden voorzieningen en kortingen die tot dit kortingsreductieprincipe behoren, niet in daaropvolgende kortingen opgenomen. De instelling van het veld **Reductiebasis** is niet van toepassing op deze instelling. |

## <a name="examples-of-rebate-reduction-principle-setups"></a>Voorbeelden van instellingen voor kortingsreductieprincipes

In de volgende tabel ziet u enkele standaardvoorbeelden van instellingen voor kortingsreductieprincipes. Voor elk van deze kortingsreductieprincipes wordt met de waarde van het veld **Beschrijving** het doel van het kortingsreductieprincipe beschreven.

| Kortingsreductieprincipe | Beschrijving | Reductie toepassen | Reductiebasis | Uitsluiten van reductie |
|---|---|---|---|---|
| Uitgesteld | Korting verminderen | Ja | Beide | Nee |
| Exclreb | Korting uitsluiten | Ja | Korting | Ja |
| Meer | Meerdere kortingen | Ja | Beide | Ja |
| None | Alleen voorziening en korting | Nee | Beide | Ja |
| Inrichten | Alleen voorziening | Ja | Inrichten | Nee |
| Korting | Alleen korting | Ja | Korting | Ja |

## <a name="examples-of-rebate-reduction-principle-calculations"></a>Voorbeelden van berekeningen voor kortingsreductieprincipes

U hebt een verkooporder met een enkele verkooporderregel. Deze regel heeft een waarde van $ 1000. De volgende deals zijn van toepassing op de order:

- **Deal 1:** 10 procent voor $ 1000
- **Deal 2:** 15 procent voor $ 1000
- **Deal 3:** 20 procent voor $ 1000
- **Deal 4:** 25 procent voor $ 1000

De volgorde van verwerking is zeer belangrijk. De verwerkingsorder is gebaseerd op de manier waarop u werkt, zoals wordt beschreven in [Kortingen verwerken, controleren en boeken](process-review-post.md).

In de volgende tabel wordt het resultaat samengevat als u order *1, 2, 3, 4* gebruikt en alleen de voorzieningen verwerkt.

| Transactie | Beschrijving en instellingen | Voorzieningsresultaat |
|---|---|---|
| 1 | <p>In de classificatie worden geen andere deals voor inhoudingen gecontroleerd. De controle wordt uitgevoerd voor zowel voorzieningen als kortingen.</p><ul><li>**Reductie toepassen:** *Nee*</li><li>**Reductiebasis:** *Beide*</li><li>**Uitsluiten van reductie:** *Nee*</li></ul> | $ 1000 × 10% = $ 100 |
| 2 | <p>Bij de classificatie worden andere deals voor inhoudingen gecontroleerd, maar deze worden gemarkeerd, zodat deze zelf wordt genegeerd. De controle wordt alleen uitgevoerd voor kortingen.</p><ul><li>**Reductie toepassen:** *Ja*</li><li>**Reductiebasis:** *Korting*</li><li>**Uitsluiten van reductie:** *Ja*</li></ul> | $ 1000 × 15% = $ 150 |
| 3 | <p>In de classificatie worden geen andere deals voor reducties gecontroleerd. De controle wordt uitgevoerd voor zowel voorzieningen als kortingen.</p><ul><li>**Reductie toepassen:** *Ja*</li><li>**Reductiebasis:** *Beide*</li><li>**Uitsluiten van reductie:** *Nee*</li></ul> | ($ 1000 – Deal 1) × 20% = $ 180 |
| 4 | <p>In de classificatie worden geen andere deals voor reducties gecontroleerd. De controle wordt uitgevoerd voor zowel voorzieningen als kortingen.</p><ul><li>**Reductie toepassen:** *Ja*</li><li>**Reductiebasis:** *Beide*</li><li>**Uitsluiten van reductie:** *Nee*</li></ul> | ($ 1000 – Deal 1 – Deal 3) × 25% = $ 180 |

In de volgende tabel ziet u enkele voorbeelden waarbij de voorziening wordt verwerkt in verschillende orders en waarbij verschillende totalen worden bereikt. De afwijking in de voorzieningen is afhankelijk van de volgorde waarin de transacties worden verwerkt. Het is belangrijk dat u weet wat de invloed is van de verwerkingsorder op het uiteindelijke kortingsbedrag.

| Volgorde | Berekening |
|---|---|
| 1<br>(1, 2, 3, 4) | <ul><li>**Deal 1:** $ 1000 × 10% = $ 100</li><li>**Deal 2:** $ 1000 × 15% = $ 150</li><li>**Deal 3:** ($ 1000 – Deal 1) × 20% = $ 180</li><li>**Deal 4:** ($ 1000 – Deal 1 – Deal 2) × 25% = $ 180</li><li>**Totale voorziening:** $ 610</li></ul> |
| 2<br>(4, 3, 2, 1) | <ul><li>**Deal 4:** $ 1000 x 25% = $ 250</li><li>**Deal 3:** ($ 1000 – Deal 4) × 20% = $ 150</li><li>**Deal 2:** $ 1000 x 15% = $ 150</li><li>**Deal 1:** $ 1000 x 10% = $ 100</li><li>**Totale voorziening:** $ 650</li></ul> |
| 3<br>(3, 2, 1, 4) | <ul><li>**Deal 3:** $ 1000 x 20% = $ 200</li><li>**Deal 2:** $ 1000 x 15% = $ 150</li><li>**Deal 1:** $ 1000 x 10% = $ 100</li><li>**Deal 4:** ($ 1000 – Deal 3 – Deal 1) × 25% = $ 175</li><li>**Totale voorziening:** $ 625</li></ul> |
| 4<br>(2, 4, 1, 3) | <ul><li>**Deal 2:** $ 1000 × 15% = $ 150</li><li>**Deal 4:** $ 1000 × 25% = $ 250</li><li>**Deal 1:** $ 1000 × 10% = $ 100</li><li>**Deal 3:** ($ 1000 – Deal 4 – Deal 1) × 20% = $ 130</li><li>**Totale voorziening:** $ 630</li></ul> |
