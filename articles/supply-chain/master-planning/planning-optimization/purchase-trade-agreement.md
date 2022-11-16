---
title: Hoofdplanning met inkoophandelsovereenkomsten
description: In dit artikel wordt beschreven hoe u met een hoofdplanning de leverancier en/of doorlooptijd voor een geplande order kunt vinden op basis van de beste prijs of doorlooptijd die is gevonden in inkoophandelsovereenkomsten.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c36827738b13d5ca71da910d32e8877c1a408f62
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740980"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>Hoofdplanning met inkoophandelsovereenkomsten

[!include [banner](../../includes/banner.md)]

In dit artikel wordt beschreven hoe u met een hoofdplanning de leverancier en/of doorlooptijd voor een geplande order kunt vinden op basis van de beste prijs of doorlooptijd die is gevonden in alle inkoophandelsovereenkomsten die zijn opgegeven voor een bepaald product.

## <a name="turn-the-purchase-trade-agreements-for-planning-optimization-feature-on-or-off"></a>De functie Inkoophandelsovereenkomsten voor Planningsoptimalisatie in- of uitschakelen

Voordat u de functie kunt gebruiken, moet deze zijn ingeschakeld voor uw systeem. Vanaf Supply Chain Management versie 10.0.29 is de functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.29 gebruikt, kunnen beheerders deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Inkoophandelsovereenkomsten voor planningsoptimalisatie* in de werkruimte [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Uw systeem voorbereiden voor het evalueren van inkoophandelsovereenkomsten tijdens de hoofdplanning

Volg deze stappen om uw systeem te configureren voor het toepassen van een hoofdplanning waarbij inkoophandelsovereenkomsten worden geëvalueerd.

1. Ga naar **Hoofdplanning \> Instellen \> Parameters hoofdplanning**. Stel op het tabblad **Geplande orders** in de sectie **Leverancier** de volgende waarden in:

    - **Handelsovereenkomst zoeken**: stel deze optie in op **Ja** als u inkoophandelsovereenkomsten wilt opnemen in de hoofdplanning.
    - **Zoekcriterium**: selecteer de factor die u voor elke inkoophandelsovereenkomst wilt prioriteren: **Minimale levertijd** of **Laagste eenheidsprijs**.

1. Ga naar **Inkoopbeheer \> Instellen \> Prijzen en kortingen \> Prijs/korting activeren** en zorg dat de optie **Leverancier** is ingesteld op **Ja**.
1. Ga naar **Productgegevensbeheer \> Instellen \> Dimensie- en variantgroepen \> Opslagdimensiegroepen** en selecteer een opslagdimensiegroep die van toepassing is op producten waarvoor de hoofdplanning inkoophandelsovereenkomsten moet evalueren. Controleer of voor elke relevante opslagdimensie in deze groep het selectievakje in de kolom **Voor inkoopsprijzen** is ingeschakeld. Herhaal deze stap voor elke andere relevante opslagdimensiegroep.

## <a name="prepare-a-released-product-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Een vrijgegeven product voorbereiden voor het evalueren van inkoophandelsovereenkomsten tijdens de hoofdplanning

Nadat het systeem is voorbereid zoals is beschreven in het vorige gedeelte, moet u deze stappen uitvoeren om ervoor te zorgen dat elk product dat u met deze functie wilt gebruiken correct is ingesteld.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten** en open een doelproduct.
1. Controleer of op het sneltabblad **Inkoop** of er geen leverancier is toegewezen in het veld **Leverancier**.
1. Selecteer in het actievenster op het tabblad **Plannen** in de groep **Behoefteplanning** de optie **Artikelbehoefteplanning** om de pagina **Artikelbehoefteplanning** te openen voor het geselecteerde product. Controleer de volgende instellingen:

    - Op het tabblad **Algemeen** kunt u leveranciersoverschrijvingen instellen. Als u in de hoofdplanning inkoophandelsovereenkomsten wilt gebruiken om een leverancier te selecteren, moet u het selectievakje **Specifieke instelling gebruiken** uitschakelen om leveranciersoverschrijving te voorkomen.
    - Op het tabblad **Levertijd** kunt u overschrijvingen van levertijden instellen. Als u wilt dat inkoophandelsovereenkomsten worden gebruikt in de hoofdplanning om levertijden te selecteren, moet u de overschrijving van levertijden voorkomen. Schakel het selectievakje uit voor elk type levertijd dat u wilt selecteren met behulp van inkoophandelsovereenkomsten (**Inkoop**, **Productie** en/of **Overdracht**).

1. Sluit de pagina **Artikelbehoefteplanning** om terug te keren naar de pagina met details voor het geselecteerde product.
1. Selecteer in het actievenster op het tabblad **Plannen** in de groep **Prognose** de optie **Aanbodprognose** om de pagina **Aanbodprognose** te openen. Zorg ervoor dat geen rij die hier wordt weergegeven een waarde bevat in de kolom **Leveranciersrekening**.
1. Sluit de pagina **Aanbodprognose** om terug te keren naar de pagina met details voor het geselecteerde product.
1. Selecteer in het actievenster op het tabblad **Inkoop** in de groep **Handelsovereenkomsten** de optie **Handelsovereenkomsten weergeven**. Controleer of alle relevante inkoophandelsovereenkomsten worden weergegeven. Controleer ook of de optie **Levertijd negeren** is ingesteld op **Nee** voor elke overeenkomst waarvoor in de hoofdplanning de levertijd moet worden gebruikt die voor die overeenkomst is opgegeven.
1. Selecteer in het actievenster op het tabblad **Plannen** in de groep **Orderinstellingen** de optie **Standaard orderinstellingen** om de pagina **Standaard orderinstellingen** te openen voor het geselecteerde product. Bekijk op het sneltabblad **Inkooporder** de waarde van het veld **Inkoopdoorlooptijd**. Als er geen overschrijving van de doorlooptijd voor artikelbehoefteplanning is gedefinieerd, wordt deze waarde gebruikt in de hoofdplanning wanneer er handelsovereenkomsten worden geselecteerd waarvoor de optie **Levertijd negeren** is ingesteld op **Ja**. Daarom moet u deze waarde zo wijzigen als nodig is.
1. Herhaal deze procedure voor relevant product.

> [!NOTE]
> De hoofdplanning biedt ondersteuning voor inkoophandelsovereenkomsten in meerdere valuta. Bij het zoeken naar een handelsovereenkomst met de optie **Laagste eenheidsprijs** wordt rekening gehouden met regels van de handelsovereenkomst met verschillende valuta's als er een wisselkoers is gedefinieerd tussen de valuta van de regel van de handelsovereenkomst en de valuta van deboekhouding van de rechtspersoon. Als dit niet het geval is, wordt de regel van de handelsovereenkomst genegeerd en wordt er een fout weergegeven tijdens de hoofdplanning. Daarom bevat de hoofdplanning informatie uit alle relevante regels van de inkoophandelsovereenkomst waar prijzen kunnen worden geconverteerd naar de valuta van de boekhouding. Houd er rekening mee dat er tijdens de prijsconversie van de handelsovereenkomst geen rekening wordt gehouden met afrondingsregels.

## <a name="examples-of-how-master-planning-finds-vendor-and-lead-times"></a>Voorbeelden van de manier waarop in een hoofdplanning leveranciers en levertijden worden gevonden

De volgende tabel bevat voorbeelden die laten zien hoe verschillende instellingen voor een vrijgegeven product en de bijbehorende inkoophandelsovereenkomsten van invloed zijn op de waarden die voor de resulterende geplande inkooporder zijn gevonden. De **vette** waarden in de twee kolommen uiterst rechts zijn de waarden die zijn geselecteerd door de hoofdplanning. De **_vette en cursieve_** waarden in de andere kolommen zijn de instellingen die de resulterende waarden voor elke rij hebben opgeleverd.

| Vrijgegeven product: Leverancier | Standaard orderinstellingen: Levertijd | Artikelbehoefteplanning: Leverancier overschrijven | Artikelbehoefteplanning: Levertijd overschrijven | Handelsovereenkomst: Leverancier | Handelsovereenkomst: Levertijd | Handelsovereenkomst: Levertijd negeren | Resulterende leverancier | Resulterende levertijd |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ***US001** _ | _*_1_*_ | Nee | Nee | US003 | 3 | Nee | _ *US001** | **1** |
| US001 | 1 | ***Ja: US002** _ | _*_Ja: 2_*_ | US003 | 3 | Nee | _ *US002** | **2** |
| *(Leeg)* | 1 | Nee | Nee | ***US003** _ | _*_3_*_ | Nee | _ *US003** | **3** |
| *(Leeg)* | ***1** _ | Nee | Nee | _*_US003_*_ | 3 | Ja | _ *US003** | **1** |
| *(Leeg)* | ***1** _ | _*_Ja: US002_*_ | Nee | US003 | 3 | Nee | _ *US002** | **1** |
| *(Leeg)* | ***1** _ | _*_Ja: US002_*_ | Nee | US003 | 3 | Nee | _ *US002** | **1** |
| *(Leeg)* | 1 | Nee | Ja: 2 | ***US003** _ | _*_3_*_ | Nee | _ *US003** | **3** |
| *(Leeg)* | 1 | Nee | ***Ja: 2** _ | _*_US003_*_ | 3 | Ja | _ *US003** | **2** |

## <a name="additional-resources"></a>Aanvullende bronnen

- [Inkoopovereenkomsten](../../procurement/purchase-agreements.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
