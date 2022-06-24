---
title: Vaste activa afstoten als uitval
description: In dit artikel wordt het proces beschreven voor het elimineren van transacties voor een vast activum dat als uitval is afgestoten.
author: moaamer
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 6564314c70de1880e437c3c493689f12d96d91ba
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855428"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a>Vaste activa afstoten als uitval

[!include [banner](../includes/banner.md)]

In dit artikel wordt het proces beschreven voor het elimineren van transacties voor een vast activum dat als uitval is afgestoten. De transactietypen die kunnen worden geëlimineerd, zijn onder andere de aanschaf- en geaccumuleerde afschrijvingstransacties van een activum en andere vaste-activatransacties. Het verwijderen van deze transacties heeft invloed op balansrekeningen, zoals aanschafcorrectie, afschrijvingscorrectie, herwaardering, waardevermeerderings- en waardeverminderingsrekeningen.

| Transactie                                         | Debet (Dr.) | Credit (Cr.) |
|-----------------------------------------------------|-------------|--------------|
| Samengevoegde afschrijving Dr.                        | X           |              |
| Winst/verlies vaste activa Cr.                          |             | X            |
| Winst/verlies vaste activa Dr.                          | X           |              |
| Aanschafrekening voor vaste activa Cr.                 |             | X            |
| Winst/verlies vaste activa Dr. (nettoboekwaarde \[NBV\]) | X           |              |
| Winst/verlies vaste activa Cr. (NBW)                    |             | X            |

> [!NOTE]
> We raden u aan nauw samen te werken met de Chief Financial Officer (CFO) of de controller van uw bedrijf om de juiste rekeningen te identificeren die voor elk transactietype moeten worden gebruikt, en ook om te controleren of deze rekeningen op de juiste manier worden bijgewerkt door het buitengebruikstellingsproces en de transacties die erdoor worden gegenereerd.

Voordat u een vast activum afstoot als uitval, moet u grootboekrekeningen maken die zijn gekoppeld aan de aanschafwaarde van het activum, afschrijving voor het huidige jaar, afschrijving voor voorgaande jaren en de NBW van het activum. De transactietypen van de vaste activa worden vermeld op de pagina **Boekingsprofielen van vaste activa**. Ga naar **Vaste activa \> Instellen \> Boekingsprofielen voor vaste activa** en selecteer op het sneltabblad **Afstoting** de optie **Uitval** in het veld boven het raster. In de volgende afbeelding ziet u de lijst met transactietypen voor vaste activa op de pagina **Boekingsprofielen vaste activa**.


[![Een activum afstoten als uitval, figuur 1.](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)

Voor het volgende voorbeeld is een vast activum aangeschaft op 1 januari 2018 en afgestoten op 31 maart 2019.

- **Aanschafprijs:** 24.000,00 euro Amerikaanse dollars (USD)
- **Levensduur:** twee kaar
- **Afschrijvingsmethode:** lineaire levensduur
- **Afschrijvingsbedrag** : 1.000,00 USD per maand

De NBW van een vast activum wordt met de volgende formule berekend:

Nettoboekwaarde = aanschafprijs – afschrijving

In dit voorbeeld is de vaste activa verworven en 15 maanden lang afgeschreven, van januari 2018 tot en met maart 2019. Daarom is de NBW van het activum 9.000,00 USD (24.000,00 USD - 15.000,00 USD).

[![Voorbeeld van afschrijving voor vaste activa.](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)


Als u een buitengebruikstellingsjournaal wilt maken, gaat u naar **Vaste activa \> Journaalboekingen \> Vaste-activajournaal** en selecteert u **Regels** in het actievenster. Selecteer **Afstoting - uitval** en vervolgens een vaste-activa-id. Als u het activum volledig wilt afstoten, voert u geen waarde in het veld **Debet** of het veld **Credit** in.

[![Vaste-activajournaal.](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)

Met de uitvaltransactie voor vaste activa worden de veldwaarden op de volgende manieren gewijzigd in het vaste-activaboek:

- In de sectie **Saldo** wordt het veld **Status** bijgewerkt naar **Buiten gebruik gesteld**.
- In de sectie **Uitgifte** wordt het veld **Afstotingsdatum** ingesteld op de datum waarop het activum buiten gebruik is gesteld.

[![Details vaste-activajournaal.](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)

In de volgende afbeelding wordt het vaste-activasaldo weergegeven.

[![Vaste-activasaldo.](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)

In de volgende afbeelding wordt het boekstuk weergegeven dat is geboekt.

[![Nettoboekwaarde.](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
