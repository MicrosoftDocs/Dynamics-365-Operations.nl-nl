---
title: Een dochtermaatschappij voor consolidatie instellen
description: In dit onderwerp wordt uitgelegd hoe u kunt werken met rekeningschema's voor consolidatiebedrijven.
author: jinniew
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: bfa913ca1778391ce0f5a1b2fdf6e5828b30cb66
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8724468"
---
# <a name="set-up-a-subsidiary-legal-entity-for-consolidation"></a>Een dochtermaatschappij voor consolidatie instellen

[!include [banner](../includes/banner.md)]

De methode die u gebruikt voor het voorbereiden van rekeningen van filialen voor consolidatie hangt gedeeltelijk af van de mate waarin de structuur van het rekeningschema in de rechtspersoon van het filiaal het rekeningschema in de geconsolideerde rechtspersoon vertegenwoordigt.

Voordat u een consolidatie start als onderdeel van de afsluiting van het periode-einde, voltooit u de voorbereidende activiteiten voor de afsluiting van het periode-einde, maar sluit de rekeningen van het filiaal niet af totdat de consolidatie is voltooid. Zie [Het grootboek aan het einde van de periode afsluiten](close-general-ledger-at-period-end.md) en [Het boekjaar afsluiten](tasks/close-fiscal-year.md) voor meer informatie over afsluiting van het periode-einde.

> [!NOTE]
>  Het is raadzaam om Management Reporter voor Microsoft Dynamics 365 Finance te gebruiken om de financiële resultaten voor meerdere rechtspersonen te combineren in een geconsolideerde indeling. Met Management Reporter kunt u geconsolideerde financiële rapporten voor rechtspersonen maken, Excel gebruiken om consolidatiegegevens uit andere bronnen te importeren en bedragen om te zetten in het gewenste aantal aangiftevaluta's zonder dat het consolidatieproces in Dynamics 365 Finance te hoeven uitvoeren.

## <a name="map-subsidiary-main-accounts-to-consolidated-main-accounts"></a>Hoofdrekeningen van filialen toewijzen aan geconsolideerde hoofdrekeningen

Als het rekeningschema in de rechtspersoon van het filiaal het rekeningschema in de geconsolideerde rechtspersoon niet volgt, kunt u de hoofdrekeningen in het filiaal toewijzen aan de hoofdrekeningen in de geconsolideerde rechtspersoon.

1. Ga in *dochtermaatschappij* naar **Grootboek \> Instellingen** \> **Rekeningschema \> Rekeningschema**.
2. Selecteer een rekeningschema. Selecteer een hoofdrekening op het sneltabblad **Hoofdrekeningen** en selecteer vervolgens **Bewerken**.
3. Selecteer elke hoofdrekening van het filiaal die dient te worden toegewezen aan een geconsolideerde hoofdrekening. Voer op het sneltabblad **Algemeen** in het veld **Consolidatierekening** de rekening in de geconsolideerde rechtspersoon in waarnaar het saldo of de transacties van de geselecteerde hoofdrekening van het filiaal dient of dienen te worden overgedragen. U kunt dezelfde geconsolideerde hoofdrekening invoeren voor verschillende rekeningen van het filiaal.

    > [!NOTE]
    > Als de hoofdrekeningtypen van de filiaalrekeningen die zijn toegewezen, verschillen van de hoofdrekeningtypen van de rekeningen in de geconsolideerde rechtspersoon, worden de waarden van rekeningen met hoofdrekeningtype **Totaal** overschreven tijdens de consolidatie.

4. Bereid rapporten en financiële overzichten voor de geconsolideerde rechtspersoon voor die zijn gebaseerd op financiële dimensies. Volg deze stappen om de financiële dimensies die worden gebruikt voor de filiaalrekeningen toe te wijzen aan de financiële dimensies in de geconsolideerde rechtspersoon:

    1. Ga in de *dochtermaatschappij* naar **Grootboek \> Instellingen \> Financiële dimensies \> Financiële dimensies**, selecteer een financiële dimensie en selecteer vervolgens **Waarden van financiële dimensies**.
    2. Selecteer de waarde van de financiële dimensie die dient te worden toegewezen aan een andere waarde van de financiële dimensie in de geconsolideerde rechtspersoon.
    3. Voer op het sneltabblad **Algemeen** in het veld **Groepsdimensie** de financiële dimensie in de geconsolideerde rechtspersoon in. Tijdens de consolidatie wordt deze financiële dimensie toegewezen aan transacties en saldi die gebruikmaken van de geselecteerde financiële dimensie in de rechtspersoon van het filiaal. De financiële dimensies die u hier invoert, dienen te worden gebruikt in de geconsolideerde rechtspersoon. U kunt de financiële dimensie die wordt gebruikt aan verschillende financiële dimensies van het filiaal toewijzen als de financiële dimensie van de groep.

5. Als u een online consolidatie uitvoert, volgt u deze stappen om ervoor te zorgen dat de overboekingen plaatsvinden zoals u wilt:

    1. Ga in de *geconsolideerde rechtspersoon* naar **Grootboek \> Periodiek \> Consolideren \> Consolideren \[Exporteren naar\]** om de pagina **Consolideren \[online\]** te openen.
    2. Schakel het selectievakje **Consolidatierekening gebruiken** op het tabblad **Criteria** in.
    3. Selecteer op het tabblad **Financiële dimensies** de juiste financiële dimensies.
    4. Voor elke financiële dimensie die u selecteert, voert u een getal in het veld **Segmentvolgorde** in om de volgorde aan te geven waarin de dimensies moeten worden weergegeven.

## <a name="maintain-the-same-chart-of-accounts-in-the-subsidiary-and-consolidated-legal-entities"></a>Hetzelfde rekeningschema bijhouden in de rechtspersoon van het filiaal en de geconsolideerde rechtspersoon

De hoofdrekeningen in de rechtspersoon van het filiaal hebben mogelijk dezelfde rekeningnummers en dezelfde structuur voor het rekeningschema als de hoofdrekeningen in de geconsolideerde rechtspersoon. In dit geval dient u de hoofdrekeningen in het filiaal niet handmatig toe te wijzen aan de hoofdrekeningen in de geconsolideerde rechtspersoon.

Volg deze stappen voordat u de consolidatie start.

1. Ga in de *geconsolideerde rechtspersoon* naar **Grootboek \> Periodiek \> Consolideren \> Consolideren \[Exporteren naar\]** om de pagina **Consolideren \[online\]** te openen.
2. Schakel het selectievakje **Consolidatierekening gebruiken** in. Tijdens de consolidatie worden de transacties en saldi automatisch aan de correcte rekening overgedragen.

> [!NOTE]
> Als de rekeningen niet overeenkomen, stopt de consolidatie en ontvangt u een bericht.

## <a name="create-a-chart-of-accounts-for-the-consolidated-legal-entity-based-on-an-existing-chart-of-accounts"></a>Een rekeningschema voor de geconsolideerde rechtspersoon maken op basis van een bestaand rekeningschema

Zelfs als een rekeningschema nog niet is gemaakt in de geconsolideerde rechtspersoon, kunt u de consolidatie uitvoeren.

- Als u de rekeningstructuur die u wilt gebruiken in de geconsolideerde rechtspersoon hebt gepland, kunt u de rekeningen van het filiaal toewijzen aan deze structuur.
- Als u geen rekeningen van het filiaal toewijst, worden de rekeningen in de geconsolideerde rechtspersoon automatisch gemaakt wanneer gegevens van het filiaal worden overgedragen aan de geconsolideerde rechtspersoon. Deze rekeningen zijn gebaseerd op de hoofdrekening. Verdere gegevens worden gecumuleerd in rekeningen in de geconsolideerde rechtspersoon die hetzelfde rekeningnummer heeft als de rekeningen van het filiaal.

Ongeacht of u rekeningen hebt toegewezen, schakelt u het selectievakje **Consolidatierekening gebruiken** uit op de pagina **Consolideren** in de geconsolideerde rechtspersoon voordat u dit type consolidatie uitvoert.

> [!NOTE]
> U kunt deze methode gebruiken voor het maken van een rekeningschema in de geconsolideerde rechtspersoon op basis van het rekeningschema in een van de rechtspersonen van het filiaal. Zie [Consolidatiegroepen en extra consolidatierekeningen maken](../budgeting/consolidation-account-groups-consolidation-accounts.md) voor meer informatie. Wijs dan een geschikt consolidatieomrekeningsprincipe toe aan elke geconsolideerde hoofdrekening en voer de consolidatie uit voor alle rechtspersonen van het filiaal.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
