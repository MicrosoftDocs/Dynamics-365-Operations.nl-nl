---
title: Btw-berekening voor algemene journaalregels
description: In dit artikel wordt uitgelegd hoe btw wordt berekend voor verschillende typen rekeningen (leverancier, klant, grootboek en project) voor algemene journaalregels.
author: EricWangChen
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: a73e145dd26e930c860e9ea31d7dab4f1593c2a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845282"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a>Btw-berekening voor algemene journaalregels
[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe btw wordt berekend voor verschillende typen rekeningen (leverancier, klant, grootboek en project) voor algemene journaalregels.

Het proces kan in drie stappen worden onderverdeeld:

- De btw-richting bepalen.

- Het btw-bedrag bepalen dat wordt opgeslagen in de tijdelijke btw-tabel.

- Het btw-bedrag en de rekening op het boekstuk bepalen.

## <a name="determine-the-sales-tax-direction"></a>De btw-richting bepalen

De manier waarop de richting van de btw wordt bepaald, is afhankelijk van het type rekening in het boekstuk. De btw-richting wordt bepaald door de combinatie van rekeningtype en btw-code. In de volgende gedeelten vindt u meer informatie over de mogelijkheden. 

### <a name="account-type-is-project"></a>Het rekeningtype is Project.

Als een boekstuk een journaalregel heeft waarvoor het rekeningtype **Project** is, gebruiken alle journaalregels in het boekstuk dezelfde belastingrichting. In de volgende afbeelding ziet u de regel. De volgende punten tonen de mogelijke belastingrichtingen voor projectrekeningen.

• Als de btw-code gebruiksbelasting is, is de btw-richting Gebruiksbelasting.

• Als de btw-code vrijgesteld van belasting is, is de btw-richting Belastingvrije Aankoop.

• Als de btw-code intracommunautaire btw is, is de btw-richting Verschuldigde Btw.

• Als de btw-code verlegd is, is de btw-richting Verschuldigde Btw.

Anders is de btw-richting Te Ontvangen Btw.

In het volgende diagram wordt de regel grafisch weergeven.

![Mogelijke belastingrichtingen voor projectrekeningen.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a>Het rekeningtype is Leverancier

Als een boekstuk een journaalregel heeft waarvoor het rekeningtype **Leverancier** is, gebruiken alle journaalregels in het boekstuk dezelfde belastingrichting. De volgende punten tonen de mogelijke belastingrichtingen voor leveranciersrekeningen. 

• Als de btw-code gebruiksbelasting is, is de btw-richting Gebruiksbelasting.

• Als de btw-code vrijgesteld van belasting is, is de btw-richting Belastingvrije Aankoop.

• Als de btw-code intracommunautaire btw is, is de btw-richting Verschuldigde Btw.

• Als de btw-code verlegd is, is de btw-richting Verschuldigde Btw.

Anders is de btw-richting Te Ontvangen Btw.

In het volgende diagram wordt de regel grafisch weergeven.

![Mogelijke belastingrichtingen voor leveranciersrekeningen.](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a>Het rekeningtype is Klant

Als een boekstuk een journaalregel heeft waarvoor het rekeningtype **Klant** is, gebruiken alle journaalregels in het boekstuk dezelfde belastingrichting. 

Als de btw-code vrijgesteld van belasting is, is de btw-richting Verkoop zonder btw. Anders is de btw-richting Verschuldigde Btw.

### <a name="account-type-is-ledger"></a>Het rekeningtype is Grootboek

In de volgende afbeelding ziet u de regel die van toepassing is, wanneer een boekstuk alleen journaalregels heeft waarvoor het rekeningtype **Grootboek** is. De volgende punten tonen de mogelijke belastingrichtingen voor grootboekrekeningen.

• Als de btw-code gebruiksbelasting is, is de btw-richting Gebruiksbelasting.

• Als de btw-code vrijgesteld van belasting is, is de btw-richting Belastingvrije Aankoop.

Als het bedrag van het journaal debet (positief) is, is de btw-richting Te Ontvangen Btw. Als het bedrag van het journaal credit is (negatief), is de btw-richting Verschuldigde Btw.

In het volgende diagram wordt de regel grafisch weergeven.

![Mogelijke belastingrichtingen voor grootboekrekeningen.](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a>De btw-richting negeren

U kunt de btw-richting negeren wanneer het boekstuk alleen regels bevat waarvoor het rekeningtype **Grootboek is**.

Ga naar **Grootboek \> Rekeningschema \> Rekeningen \> Hoofdrekeningen** en selecteer het sneltabblad **Rechtspersoon overschrijvingen**.

## <a name="determine-the-sales-tax-amount"></a>Het btw-bedrag bepalen

In deze sectie wordt beschreven hoe het teken voor het btw-bedrag wordt berekend.

![Pagina Btw-transacties.](media/sales-tax-amount-sign.jpg)

In de volgende tabel wordt de algemene regel weergegeven voor het bepalen van de btw-richting en het teken van btw-bedragen in de tijdelijke btw-tabel.

| Bedrag journaalregel: | Btw-richting  | Teken btw-bedrag |
|---------------------|----------------------|-----------------------|
| Positief            | Te Ontvangen Btw | Positief              |
| Positief            | Verschuldigde Btw    | Negatief              |
| Negatief            | Te Ontvangen Btw | Negatief              |
| Negatief            | Verschuldigde Btw    | Positief              |

Er is een speciale regel voor boekstukken die alleen **Project-** of **Grootboek** regels hebben, wanneer een btw-groep of artikel-btw-groep wordt geselecteerd op de **Grootboek** regel. Deze regel wordt beheerd door de functie, **Onafhankelijke btw-berekeningsfunctie inschakelen voor algemene journalen**. Wanneer deze functie is uitgeschakeld, gebruikt het btw-bedrag van de **Grootboek** regel de debet/credit-richting van de **Project** regel. Wanneer de functie is ingeschakeld, gebruikt het btw-bedrag van de **Grootboek** regel zijn eigen debet/credit-richting. In de volgende tabellen wordt de regel voor elk scenario weer gegeven. 

**Regel wanneer de functie is ingeschakeld.**

| Journaalregel bedrag van project | Btw-richting  | Teken btw-bedrag |
|--------------------------------|----------------------|-----------------------|
| Positief                       | Te Ontvangen Btw | Positief              |
| Negatief                       | Te Ontvangen Btw | Negatief              |

**Regel wanneer de functie is uitgeschakeld**

| Journaalregel bedrag van grootboek  | Btw-richting  | Teken btw-bedrag |
|--------------------------------|----------------------|-----------------------|
| Positief                       | Te Ontvangen Btw | Positief              |
| Negatief                       | Te Ontvangen Btw | Negatief              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a>Het btw-bedrag en de rekening op het boekstuk bepalen

Wanneer u btw boekt, wordt de hoofdrekening opgehaald uit het groepsprofiel voor de grootboek-boekingen. Wanneer de btw terug te ontvangen is, gebruikt het systeem de rekening voor Te Ontvangen Btw die in het profiel is opgegeven. Wanneer de btw verschuldigd is, gebruikt het systeem de rekening voor Verschuldigde Btw die in het profiel is opgegeven.

De volgende tabel laat de generieke regel zien.

| Btw-richting  | Teken btw-bedrag | Btw-rekening      | Bedrag op boekstuk |
|----------------------|-----------------------|------------------------|-------------------|
| Te Ontvangen Btw | Positief              | Rekening voor Te Ontvangen Btw | Positief (Debet)  |
| Te Ontvangen Btw | Negatief              | Rekening voor Te Ontvangen Btw | Negatief (Credit)  |
| Verschuldigde Btw    | Positief              | Rekening voor Verschuldigde Btw    | Negatief (Credit)  |
| Verschuldigde Btw    | Negatief              | Rekening voor Verschuldigde Btw    | Positief (Debet)  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
