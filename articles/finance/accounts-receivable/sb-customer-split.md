---
title: Klantsplitsing in factureringsplanningen
description: In dit artikel wordt beschreven hoe u een klant kunt splitsen bij het factureren van abonnementen.
author: JodiChristiansen
ms.date: 11/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2022-11-05
ms.dyn365.ops.version: 10.0.31
ms.openlocfilehash: cfbe61ca4b7e809a8183f4622bf6db4fc83a4d83
ms.sourcegitcommit: 9e2e54ff7d15aa51e58309da3eb52366328e199d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/04/2022
ms.locfileid: "9746311"
---
# <a name="customer-split-on-billing-schedules"></a>Klantsplitsing in factureringsplanningen

In een factureringsplanning is de *te factureren rekening* de klant die de verkooporderfactuur ontvangt zodat deze de rekening kan betalen. In sommige scenario's kunnen meerdere klanten een factuur betalen. Met de functionaliteit **Klantsplitsing** kunt u meer klanten toevoegen die voor dezelfde factureringsplanning kunnen worden gefactureerd. Als u deze functionaliteit wilt inschakelen, gaat u naar **Facturering van abonnementen \> Terugkerende contractfacturering \> Instelling \> Terugkerende contractfactureringsparameters** en stelt u de optie **Klantsplitsing** in op **Ja**.

## <a name="customer-split-on-the-billing-schedule-header"></a>Klantsplitsing in de koptekst voor factureringsplanning

Nadat een factureringsplanning is gemaakt, kunnen er extra klanten aan de koptekst voor de factureringsplanning worden toegevoegd.

Volg deze stappen om een tegel klant toe te voegen.

1. Selecteer **Klantsplitsing** op het tabblad **Factureringsplanning**. In de velden **Klantrekening** en **Klantrekeningnaam** boven aan geeft u de klant op die is aangewezen als **Klant factureringsplanning**.

    > [!NOTE]
    > De klantrekening die u toevoegt, kan niet overeenkomen met de factuurrekening.

2. Selecteer **Regel toevoegen** op het tabblad **Regels voor klantsplitsing**.
3. Selecteer een klant en voer vervolgens het percentage van elke factuur voor die klant in.
4. Standaard worden de begin- en einddatums van de factureringsplanning gebruikt als begin- en einddatum. Voer verschillende begin- en einddatums in als de nieuwe klant het opgegeven percentage slechts voor een deel van de factureringsplanning betaalt. Als de factureringsplanning bijvoorbeeld als begindatum 1 januari en als einddatum 31 december heeft en de nieuwe klant voor de eerste negen maanden 40 procent krijgt gefactureerd, geeft u 1 januari op als begindatum en 30 september als einddatum en voert u **40,00** in als percentage.

U kunt meerdere klanten toevoegen aan de klantsplitsingsregels. In dit geval mag het totale percentage dat wordt ingevoerd niet hoger zijn dan 100 procent. Voer een klantverwijzing en een bestelopdracht van de klant in als informatievelden die worden weergegeven op de verkooporderregel tijdens het proces **Factuur genereren**.

In de regeldetails worden de contactgegevens, het afleveradres, het factuuradres en de betalingsgegevens van de toegevoegde klanten weergegeven. Deze informatie wordt ook weergegeven op de verkooporder voor de klanten.

Wanneer u gesplitste klantgegevens toevoegt aan de koptekst van de factureringsplanning, ontvangt u, als er niet-gefactureerde factureringsplanningsregels in de factureringsplanning staan, het volgende bericht: Wilt u de wijziging doorvoeren vanuit de koptekst naar de regels? Wijzigingen zullen alleen de factureringsplanningsregels bijwerken die niet zijn gefactureerd. Selecteer **Ja om** de gesplitste klantgegevens op de factureringsplanningsregel bij te werken. Wijzigingen worden niet bijgewerkt als de factureringsplanningsregel al is gefactureerd.

Als er een factureringsplanning wordt gemaakt met de optie **Planning kopiëren**, wordt standaardinformatie ingevoerd op koptekstregels voor klantsplitsing. Deze kan niet gelijk zijn aan de klantrekening.

Wanneer het proces **Factuur genereren** is voltooid, worden er meerdere verkooporders gemaakt. (Er worden ook meerdere verkoopfacturen gemaakt als automatische boeking wordt gebruikt.) Deze verkooporders en verkoopfacturen kunnen worden weergegeven op het tabblad **Factuur** op het sneltabblad **Regeldetails** van de pagina **Factureringsdetails**. **Meerdere** wordt op de factureringsdetailregel weergegeven om aan te geven dat meerdere verkooporders en verkoopfacturen zijn gemaakt.

## <a name="customer-split-on-billing-schedule-lines"></a>Klantsplitsing op factureringsplanningsregels

De klantsplitsing kan worden toegevoegd aan afzonderlijke factureringsplanningsregels als u alleen specifieke factureringsplanningsregels wilt splitsen. Schakel het selectievakje **Klantsplitsing** op de regel in en selecteer vervolgens **Klantsplitsing** in het menu voor de factureringsplanningsregel om de gegevens over de klantsplitsing bij te werken of in te voeren.

De controlegegevens worden bijgewerkt als de factureringsplanning al is gefactureerd, maar het percentage vervolgens is gewijzigd op de factureringsplanningsregel. Alle regels die na deze wijziging worden gefactureerd, gebruiken het nieuwe percentage.

> [!NOTE]
> - De optie voor klantsplitsing kan niet worden gebruikt voor voorraadproducten.
> - Als het selectievakje **Niet-gefactureerde opbrengst** is ingeschakeld, kan het selectievakje **Klantsplitsing** niet worden ingeschakeld.
> - Als u alleen de optie **Alleen gesplitste opbrengst** gebruikt, bevat de bovenliggende regel de optie **Klantsplitsing**, maar de onderliggende regelartikelen niet.
