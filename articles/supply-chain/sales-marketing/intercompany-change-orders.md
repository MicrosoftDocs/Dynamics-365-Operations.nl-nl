---
title: Intercompany-orders wijzigen
description: In dit onderwerp wordt uitgelegd hoe u de functionaliteit voor intercompany-orders wijzigt.
author: GalynaFedorova
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 1129794bf0ac6513770f8b2a0eeb7fb6154d7942
ms.sourcegitcommit: fcfd85a508c0de52cfe11d1986892219e39ef406
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7548204"
---
# <a name="change-intercompany-orders"></a>Intercompany-orders wijzigen

[!include [banner](../../includes/banner.md)]

Als u een intercompany-verkooporder of -inkooporder wijzigt, wordt die wijziging ook doorgevoerd in de bijbehorende verkoop- of inkooporder in het overeenkomstige bedrijf.

## <a name="adding-new-lines"></a>Nieuwe regels toevoegen

Wanneer een oorspronkelijke verkooporder deel uitmaakt van de intercompany-orderketen, kunt u nieuwe regels toevoegen aan een intercompany-verkooporder en -inkooporder. U kunt ook nieuwe regels toevoegen als de oorspronkelijke verkooporder geen rechtstreekse levering is. Als de oorspronkelijke verkooporder wel een rechtstreekse levering is, kunt u alleen nieuwe orderregels toevoegen aan de intercompany-verkooporder en -inkooporder als het veld **Indirect maken toestaan** is geselecteerd op het sneltabblad **Intercompany-instellingen** op de oorspronkelijke verkooporder.

## <a name="changing-prices-and-discounts"></a>Prijzen en kortingen wijzigen

U kunt de prijzen en kortingen wijzigen als de selectievakjes **Bewerking van prijs toestaan** en **Bewerking van korting toestaan** zijn ingeschakeld op de **Intercompany**-pagina.

Als u de eenheidsprijs wijzigt van een van de bestaande regels op de intercompany-verkooporderregel, wordt de eenheidsprijs op de intercompany-inkooporder ook gewijzigd.

Als u kortingsvelden wijzigt op de intercompany-verkooporderregel, worden in de bijbehorende kortingsvelden op de intercompany-inkooporder ook bijgewerkt.

## <a name="changing-and-adding-new-charges"></a>Nieuwe toeslagen wijzigen en toevoegen

U kunt toeslagen wijzigen als de selectievakjes **Bewerking van prijs toestaan** en **Bewerking van korting toestaan** zijn ingeschakeld op de **Intercompany**-pagina.

Als u een nieuwe toeslag aan de koptekst van de intercompany-verkooporder en een nieuwe toeslag aan de intercompany-verkoopregel toevoegt, worden beide toeslagen naar de intercompany-inkooporder gekopieerd. Daarom hebben de intercompany-verkooporder en de intercompany-inkooporder hetzelfde totaalbedrag. De toeslagen worden nooit naar de oorspronkelijke verkooporder gekopieerd.

## <a name="copying-a-fee"></a>Kosten kopiëren

Als u kosten wilt kopiëren naar de oorspronkelijke verkooporder, maakt u deze aan als een nieuwe verkoopregel met een artikel van het type **Service**.

## <a name="changing-quantities-and-deleting-intercompany-purchases-and-sales-order-lines"></a>Hoeveelheden wijzigen en intercompany-inkooporderregels en -verkooporderregels verwijderen

U kunt de hoeveelheid of een intercompany-inkooporderregel of verkooporderregel alleen verwijderen als de regel rechtstreeks is gemaakt vanuit het formulier **Verkooporder** of **Inkooporder**. Met deze wijziging maakt u van de intercompany-inkooporder of van de intercompany-verkooporder of orderregels de bron.

## <a name="origins-of-orders-and-order-lines"></a>Oorsprong van orders en orderregels

Intercompany-orders en -orderregels kunnen een of twee oorsprongen hebben:

- **Afgeleid** – De order is automatisch gemaakt als gevolg van een intercompany-orderketen.
- **Bron** – De order is handmatig gemaakt door een gebruiker.

De oorsprong wordt weergegeven in de orderkoptekst van intercompany-inkooporders en -verkooporders in het veld **Oorsprong**. Het veld bevindt zich op het sneltabblad **Intercompany-instellingen** op de verkooporder en op het sneltabblad **Instellen** op de inkooporder.

De oorsprongen **Afgeleid** en **Bron** zijn alleen van toepassing op intercompany-orders. Het veld **oorsprong** is leeg voor alle andere verkooporders, inkooporders en orderregels. Dit veld is ook leeg op de oorspronkelijke verkooporder.

## <a name="example-derived-origin"></a>Voorbeeld: Afgeleide oorsprong

U maakt een oorspronkelijke verkooporder voor een externe klant. Deze verkooporder bevat één orderregel. Met deze oorspronkelijke verkooporder wordt een intercompany-inkooporder gemaakt die één orderregel bevat waarmee een intercompany-verkooporder wordt gemaakt die één orderregel bevat. De koptekst van de intercompany-inkoopregel en de orderregel worden automatisch gemaakt op basis van de oorspronkelijke verkooporder.

De waarde van het veld **Oorsprong** op het sneltabblad **Instellen** van de intercompany-inkooporder en het sneltabblad **Intercompany-instellingen** is **Afgeleid**. De waarde van het veld **Oorsprong** op het tabblad **Regeldetails** van de inkooporder- en verkooporderregels is ook **Afgeleid**.

Als een orderregel de oorsprong **Afgeleid** heeft, kunt u de orderregel niet rechtstreeks verwijderen. U kunt de orderregel alleen verwijderen vanuit de bron waarmee de orderregel is gemaakt. U kunt de bestelde hoeveelheid ook alleen wijzigen vanuit de bron waarmee de orderregel is gemaakt.

Als een oorspronkelijke verkooporder en verkooporderregel deel uitmaken van de intercompany-orderketen, kunt u de bestelde hoeveelheden van de oorspronkelijke verkooporder wijzigen en kunt u orderregels uit de oorspronkelijke verkooporder verwijderen.

## <a name="example-source-origin"></a>Voorbeeld: Bronoorsprong

U maakt een inkooporder voor een intercompany-leverancier. De intercompany-inkooporder en -orderregel hebben beide de oorsprong **Bron**. Dit betekent dat deze intercompany-inkooporder de controller is en de automatisch gemaakte intercompany-verkooporder in het bedrijf van de leverancier de oorsprong **Afgeleid** heeft.

Daarnaast kunnen de bestelde hoeveelheden van een orderregel die op de intercompany-inkooporder zijn gemaakt, niet worden gewijzigd op de intercompany-verkooporder. De orderregel kan alleen worden verwijderd vanuit de intercompany-inkooporderregel. Als er een nieuwe regel aan de intercompany-verkooporder wordt toegevoegd, heeft de intercompany-verkooporderregel de oorsprong **Bron**.

Wanneer een oorspronkelijke verkooporder deel uitmaakt van de intercompany-orderketen, kunt u de intercompany-orders en intercompany-orderregels van de oorspronkelijke verkooporder altijd beheren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
