---
title: Rapporten van Francoprijzen
description: In dit onderwerp wordt beschreven hoe u de verschillende typen rapporten kunt opzoeken en gebruiken die beschikbaar zijn voor de module Francoprijzen.
author: sherry-zheng
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 565303a4f51d1726c62a85faaf8c4d8692c110fc
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500641"
---
# <a name="landed-cost-reports"></a>Rapporten voor francoprijzen

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="outstanding-invoices"></a>Openstaande facturen

Het rapport Openstaande facturen bevat een lijst met alle openstaande facturen van de verschillende kostenniveaus die aan elke reis zijn gekoppeld. Het rapport wordt gebruikt om regelmatig de kosten en reiskosten af te stemmen op de lijst met grootboektransacties. Nadat er overheadkosten zijn gefactureerd, worden deze uit het rapport verwijderd.

Ga als volgt te werk om een rapport met openstaande facturen te genereren.

1. Ga naar **Francoprijzen \> Rapporten \> Traceren \> Openstaande facturen**.
1. Geef in het dialoogvenster **Openstaande facturen** in het veld **Van datum** een datum op. Alle facturen die op of voor die datum openstaand waren, worden in de uitvoer opgenomen.
1. Selecteer onder **Weergeven** een van de volgende opties:

    - **Niet-gefactureerde kosten**: bevat kosten voor gefactureerde zendingen met een geraamde kostprijs maar geen werkelijke kosten.
    - **Niet-gefactureerde voorraad**: bevat kosten die zijn gefactureerd, maar waarvoor nog geen inkooporder is ontvangen.
    - **Alle niet gefactureerd**: bevat de resultaten van de optie **Niet-gefactureerde kosten** en de optie **Niet-gefactureerde voorraad**.

1. Stel de optie **Nieuwe kosten opnemen** in op *Ja* als u kosten wilt opnemen die nog geen werkelijke kosten bevatten en waarvoor nog geen voorraad is ontvangen. Als u deze optie instelt op *Nee*, bevat het rapport alleen kosten die zijn gefactureerd.
1. Schakel in de sectie **Weergeven** elk type detail in dat u in het rapport wilt opnemen.
1. Gebruik net als bij andere typen rapporten in Microsoft Dynamics 365 Supply Chain Management het sneltabblad **Bestemming** om de uitvoerindeling van het rapport te selecteren.
1. Gebruik net als bij andere typen rapporten in Supply Chain Management het sneltabblad **Op te nemen records** om de records die in het rapport worden opgenomen, verder te beperken.
1. Selecteer **OK** om het rapport te genereren.

## <a name="activityprovider-analysis-reports"></a>Analyserapporten van activiteiten en providers

Met de analyserapporten van activiteiten en providers kunt u de nauwkeurigheid van uw geraamde tijden voor elke provider controleren.

Ga als volgt te werk om een analyserapport van activiteiten en providers te genereren.

1. Volg een van de volgende stappen, afhankelijk van het type rapport dat u wilt maken:

    - Ga naar **Francoprijzen \> Rapporten \> Analyse van activiteiten/providers op activiteit**. In dit geval worden de geraamde tijden gegroepeerd op activiteit.
    - Ga naar **Francoprijzen \> Rapporten \> Analyse van activiteiten/providers op provider**. In dit geval worden de geraamde tijden gegroepeerd op provider.

    Het dialoogvenster **Analyse van activiteiten/providers per activiteit** of het dialoogvenster **Analyse van activiteiten/providers per provider** wordt weergegeven. Beide dialoogvensters bieden dezelfde opties.

1. Gebruik net als bij andere typen rapporten in Supply Chain Management het sneltabblad **Bestemming** om de uitvoerindeling van het rapport te selecteren.
1. Gebruik net als bij andere typen rapporten in Supply Chain Management het sneltabblad **Op te nemen records** om de records die in het rapport worden opgenomen, verder te beperken.
1. Selecteer **OK** om het rapport te genereren.

## <a name="voyage-costing-reports"></a>Rapporten van kostprijsberekening van reizen

In de rapporten van kostprijsberekeningen van reizen worden de kosten van de artikelen en de importkosten per folio, container of reis weergegeven, afhankelijk van de opties die u selecteert wanneer u het rapport genereert. Met elk rapport van de kostprijsberekening van een reis kunt u de geschatte kosten van een reis ten opzichte van de werkelijke kosten bekijken. Dit rapport kan worden opgesplitst in de verschillende identificatiefactoren.

Ga als volgt te werk om een rapport van de kostprijsberekening van een reis te genereren.

1. Volg een van de volgende stappen, afhankelijk van het type rapport dat u wilt maken:

    - Ga naar **Francoprijzen \> Rapporten \> Kostprijsberekening \> Kostprijsberekening van reis per afzonderlijke kosten**. In dit geval worden via de optie voor afzonderlijke kosten de importkosten per kostengebied, per kostentypecode weergegeven.
    - Ga naar **Francoprijzen \> Rapporten \> Kostprijsberekening \> Kostprijsberekening van reis per rapportagecategorie**. In dit geval worden de importkosten opgesplitst in de verschillende rapportagecategorieën. Kostentypen worden gegroepeerd op rapportagecategorieën.

    Het dialoogvenster **Kostprijsberekening van reis per afzonderlijke kosten** of het dialoogvenster **Kostprijsberekening van reis per rapportagecategorie** wordt weergegeven. Deze dialoogvensters zijn vergelijkbaar. Eventuele verschillen worden in het resterende deel van deze procedure aangegeven.

1. Als u het dialoogvenster **Kostprijsberekening van reis per rapportcategorie** hebt geopend, selecteert u een van de volgende waarden in het veld **Kosten**:

    - **Kostenwaarde**: de waarde wordt berekend met behulp van automatische kosten of wordt handmatig gemaakt in het kostengebied.
    - **Geraamd**: nadat de goederen zijn ontvangen, worden de geschatte kosten ingesteld.
    - **Werkelijk**: nadat de order is gefactureerd, worden de werkelijke kosten ingesteld bij de kosten op de factuur.
    - **Beste**: het systeem gebruikt de opties die het meest nauwkeurig zijn uit de vorige drie opties. (U wordt aangeraden deze optie te selecteren.)

1. Stel de optie **Per artikel** in op *Ja* om de kosten van elk artikel weer te geven. Stel de optie in op *Nee* om de kosten per transport weer te geven.
1. Selecteer in de sectie **Weergeven** de categorieën op basis waarvan de kosten moeten worden onderverdeeld.
1. Selecteer in de sectie **Dimensies** de dimensies die u in het rapport wilt opnemen.
1. Gebruik net als bij andere typen rapporten in Supply Chain Management het sneltabblad **Bestemming** om de uitvoerindeling van het rapport te selecteren.
1. Gebruik net als bij andere typen rapporten in Supply Chain Management het sneltabblad **Op te nemen records** om de records die in het rapport worden opgenomen, verder te beperken.
1. Selecteer **OK** om het rapport te genereren.

## <a name="shipping-container-receipts-list"></a>Lijst met containerontvangsten

De ontvangstlijst van de container bevat alle niet-ontvangen hoeveelheden die op of vóór een verwachte datum moeten worden ontvangen. Magazijnmedewerkers kunnen dit rapport gebruiken om de verwachte goederen van een container te identificeren. De lijst kan ook worden gebruikt om goederen handmatig te valideren als deze in een container worden ontvangen.

Volg deze stappen om een ontvangstlijst voor containers te genereren.

1. Ga naar **Francoprijzen \> Rapporten \> Traceren \> Ontvangstlijst container**.
1. Geef in het dialoogvenster **containerontvangstlijst** in het veld **Verwachte datum** een datum op. Alle hoeveelheden die niet op of voor die datum zijn ontvangen, worden in de uitvoer opgenomen.
1. Selecteer in de sectie **Dimensies** de dimensies die u in het rapport wilt opnemen.
1. Gebruik net als bij andere typen rapporten in Supply Chain Management het sneltabblad **Bestemming** om de uitvoerindeling van het rapport te selecteren.
1. Gebruik net als bij andere typen rapporten in Supply Chain Management het sneltabblad **Op te nemen records** om de records die in het rapport worden opgenomen, verder te beperken.
1. Selecteer **OK** om het rapport te genereren.

## <a name="expected-delivery-report"></a>Rapport met verwachte levering

Het rapport met verwachte levering bevat basisinformatie over de reis, container, het folio, de artikelen en de verwachte leveringsdatum.

Ga als volgt te werk om een rapport met verwachte leveringen te genereren.

1. Ga naar **Francoprijzen \> Rapporten \> Traceren \> Verwachte levering**.
1. Selecteer in het dialoogvenster **Verwachte levering** in het veld **Verwachte datum** de datum waarop de levering van de goederen naar het definitieve doelmagazijn wordt verwacht. Alle reisregels met een verwachte datum op of vóór die datum en die nog niet zijn ontvangen, worden in de uitvoer opgenomen.
1. Optioneel: selecteer in het veld **Leverancierrekening** een leverancierrekening om alleen leveringen van een bepaalde leverancier op te nemen.
1. Selecteer in de sectie **Dimensies** de dimensies die u in het rapport wilt opnemen.
1. Gebruik net als bij andere typen rapporten in Supply Chain Management het sneltabblad **Bestemming** om de uitvoerindeling van het rapport te selecteren.
1. Gebruik net als bij andere typen rapporten in Supply Chain Management het sneltabblad **Op te nemen records** om de records die in het rapport worden opgenomen, verder te beperken.
1. Selecteer **OK** om het rapport te genereren.
