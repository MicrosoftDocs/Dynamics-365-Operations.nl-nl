---
title: Belasting wordt geboekt naar de verkeerde grootboekrekening in het boekstuk
description: Dit onderwerp bevat informatie voor het oplossen van problemen die kunnen helpen wanneer belasting is geboekt naar de verkeerde grootboekrekening in het boekstuk.
author: qire
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 3d197046bd547757f32712a50949b41897f6fedf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020086"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a>Belasting wordt geboekt naar de verkeerde grootboekrekening in het boekstuk

[!include [banner](../includes/banner.md)]

Tijdens het boeken, kan belasting naar de verkeerde grootboekrekening in het boekstuk worden geboekt. Volg de stappen in de volgende secties zoals vereist om dit probleem op te lossen. In de voorbeelden in dit onderwerp wordt een verkooporder als bedrijfsdocument gebruikt.

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a>Zoek de belastingcode van de onjuist geboekte belastingtransactie

1. Selecteer op de pagina **Boekstuktransacties** de transactie waarmee u aan de slag wilt en selecteer vervolgens **Geboekte btw**.

    [![De knop Geboekte btw op de pagina Boekstuktransacties](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)

2. Bekijk de waarde in het veld **Btw-code**. In dit voorbeeld is dat **Btw 19**.

    [![Veld Btw-code op de pagina Geboekte btw](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a>Controleer de groep boekingen in grootboek van de belastingcode

1. Ga naar **Belasting** \> **Indirecte belastingen** \> **Btw** \> **Btw-codes**.
2. Zoek de belastingcode, selecteer deze en controleer vervolgens de waarde in het veld **Groep boekingen in grootboek**. In dit voorbeeld is dat **Btw**.

    [![Het veld Groep boekingen in grootboek op de pagina Btw-codes](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)

3. De waarde in het veld **Groep boekingen in grootboek** is een koppeling. Selecteer de koppeling om de details van de configuratie van de groep te bekijken. U kunt ook het veld selecteren en vasthouden (of met de rechtermuisknop klikken) en vervolgens **Details weergeven** selecteren.

    [![Opdracht Details weergeven](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)

4. Controleer in het veld **Te betalen btw** of het rekeningnummer juist is aan de hand van het transactietype. Als dit niet zo is, selecteer de juiste rekening waar het naartoe geboekt moet worden. In dit voorbeeld moet de btw van de verkooporder worden geboekt naar de rekening voor te betalen btw 222200.

    [![Het veld Te betalen btw op de pagina Groep boekingen in grootboek](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)

    De volgende tabel bevat informatie over elk veld op de pagina **Groep boekingen in grootboek**.

    | Veld                  | Beschrijving |
    |------------------------|-------------|
    | Te betalen btw      | De hoofdrekening voor uitgaande btw die aan de belastinginstantie moet worden betaald. |
    | Te ontvangen btw   | De hoofdrekening voor ontvangen btw die wordt terugbetaald door de belastinginstantie. |
    | Gebruiksbelastinguitgave        | De hoofdrekening die wordt gebruikt om aftrekbare gebruiksbelastingen die leveranciers niet claimen bij of melden aan de belastinginstantie als onderdeel van omgekeerde toeslag van de Europese Unie (EU) Belasting op goederen en diensten (GST)/Harmonised Sales Tax (HST), te boeken. **Gebruiksbelasting** moet worden geselecteerd voor de btw-code in de btw-groep die in de transactie wordt gebruikt. Dit veld is niet beschikbaar als **Belastingregels btw toepassen** is geselecteerd op de pagina **Grootboekparameters**. |
    | Te betalen gebruiksbelasting        | De hoofdrekening die wordt gebruikt voor het boeken van ontvangen gebruiksbelastingen die moeten worden betaald aan de belastinginstanties. |
    | Vereffeningsrekening     | De hoofdrekening die wordt gebruikt om het nettosaldo van de grootboekrekeningen die zijn gespecificeerd in de velden **Te betalen gebruiksbelasting** en **Te ontvangen btw**, te boeken. |
    | Contantkorting van leverancier   | De hoofdrekening die wordt gebruikt om een betalingskorting voor btw-codes die zijn gekoppeld aan deze groep voor boekingen in grootboek, te boeken. |
    | Korting klantcase | De hoofdrekening die wordt gebruikt om een betalingskorting voor btw-codes die zijn gekoppeld aan deze groep voor boekingen in grootboek, te boeken. |

    Zie [Groepen boekingen in grootboek instellen voor btw](tasks/set-up-ledger-posting-groups-sales-tax.md) voor meer informatie

## <a name="debug-in-code-to-check-ledger-dimensions"></a>Foutopsporing in code om grootboekdimensies te controleren

In de code wordt de boekingsrekening bepaald door de grootboekdimensie. De grootboekdimensie slaat de record-id van een rekening in de database op.

1. Voor een verkooporder voegt u een onderbrekingspunt toe aan de methoden **Tax::saveAndPost()** en **Tax::post()**. Let op de waarde van **\_Grootboekdimensie**.

    [![Voorbeeld van code voor een verkooporder met een onderbrekingspunt](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)

    Voor een inkooporder voegt u een onderbrekingspunt toe aan de methoden **TaxPost::saveAndPost()** en **TaxPost::postToTaxTrans()**. Let op de waarde van **\_Grootboekdimensie**.

    [![Voorbeeld van code voor een inkooporder met een onderbrekingspunt](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)

2. Voer de volgende SQL-query uit om de weergavewaarde van de rekening te zoeken in de database op basis van de record-id die wordt opgeslagen door de grootboekdimensie.

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    [![Weergavewaarde van de record-id](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)

3. Bekijk de aanroepstapel om te zoeken waar de waarde **_ledgerDimension** wordt toegewezen. Meestal is de waarde afkomstig van **TmpTaxWorkTrans**. In dit geval moet u een onderbrekingspunt toevoegen in **TmpTaxWorkTrans::insert()** en **TmpTaxWorkTrans::update()** om te zoeken waar de toegewezen waarde wordt toegewezen.

## <a name="determine-whether-customization-exists"></a>Bekijk of er een aanpassing bestaat

Als u de stappen in de vorige secties hebt voltooid, maar u hebt het probleem niet gevonden, bekijkt u of er een aanpassing bestaat. Als er geen aanpassing bestaat, opent u een ondersteuningsaanvraag bij Microsoft voor verdere ondersteuning.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
