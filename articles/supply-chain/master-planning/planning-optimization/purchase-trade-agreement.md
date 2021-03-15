---
title: Hoofdplanning met inkoophandelsovereenkomsten
description: In dit onderwerp wordt beschreven hoe u met Planningsoptimalisatie de leverancier en/of doorlooptijd voor een geplande order kunt vinden op basis van de beste prijs of doorlooptijd die is gevonden in inkoophandelsovereenkomsten.
author: ChristianRytt
manager: tfehr
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: e060f20b65153a7bbe70996e6ff4c3930468348a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992240"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>Hoofdplanning met inkoophandelsovereenkomsten

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u met Planningsoptimalisatie de leverancier en/of doorlooptijd voor een geplande order kunt vinden op basis van de beste prijs of doorlooptijd die is gevonden in alle inkoophandelsovereenkomsten die zijn opgegeven voor een bepaald product.

## <a name="turn-on-the-purchase-trade-agreements-for-planning-optimization-feature"></a>De functie Inkoophandelsovereenkomsten voor Planningsoptimalisatie inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen het werkgebied [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de status van de functie te controleren en desgewenst in te schakelen. De functie wordt daar op de volgende manier weergegeven:

- **Module:** *Hoofdplanning*
- **Functienaam:** *Inkoophandelsovereenkomsten voor Planningsoptimalisatie*

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Uw systeem voorbereiden voor het evalueren van inkoophandelsovereenkomsten tijdens de hoofdplanning

Volg deze stappen om uw systeem te configureren voor het toepassen van Planningsoptimalisatie waarbij inkoophandelsovereenkomsten worden geëvalueerd.

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

    - Op het tabblad **Algemeen** kunt u leveranciersoverschrijvingen instellen. Als u in Planningsoptimilsatie inkoophandelsovereenkomsten wilt gebruiken om een leverancier te selecteren, moet u het selectievakje **Specifieke instelling gebruiken** uitschakelen om leveranciersoverschrijving te voorkomen.
    - Op het tabblad **Levertijd** kunt u overschrijvingen van levertijden instellen. Als u wilt dat inkoophandelsovereenkomsten worden gebruikt in Planningsoptimalisatie om levertijden te selecteren, moet u de overschrijving van levertijden voorkomen. Schakel het selectievakje uit voor elk type levertijd dat u wilt selecteren met behulp van inkoophandelsovereenkomsten (**Inkoop**, **Productie** en/of **Overdracht**).

1. Sluit de pagina **Artikelbehoefteplanning** om terug te keren naar de pagina met details voor het geselecteerde product.
1. Selecteer in het actievenster op het tabblad **Plannen** in de groep **Prognose** de optie **Aanbodprognose** om de pagina **Aanbodprognose** te openen. Zorg ervoor dat geen rij die hier wordt weergegeven een waarde bevat in de kolom **Leveranciersrekening**.
1. Sluit de pagina **Aanbodprognose** om terug te keren naar de pagina met details voor het geselecteerde product.
1. Selecteer in het actievenster op het tabblad **Inkoop** in de groep **Handelsovereenkomsten** de optie **Handelsovereenkomsten weergeven**. Controleer of alle relevante inkoophandelsovereenkomsten worden weergegeven. Controleer ook of de optie **Levertijd negeren** is ingesteld op **Nee** voor elke overeenkomst waarvoor in Plannningsoptimalisatie de levertijd moet worden gebruikt die voor die overeenkomst is opgegeven.
1. Selecteer in het actievenster op het tabblad **Plannen** in de groep **Orderinstellingen** de optie **Standaard orderinstellingen** om de pagina **Standaard orderinstellingen** te openen voor het geselecteerde product. Bekijk op het sneltabblad **Inkooporder** de waarde van het veld **Inkoopdoorlooptijd**. Als er geen overschrijving van de doorlooptijd voor artikelbehoefteplanning is gedefinieerd, wordt deze waarde gebruikt in Planningsoptimalisatie wanneer er handelsovereenkomsten worden geselecteerd waarvoor de optie **Levertijd negeren** is ingesteld op **Ja**. Daarom moet u deze waarde zo wijzigen als nodig is.
1. Herhaal deze procedure voor relevant product.

> [!NOTE]
> De valuta op de regel van de inkoophandelsovereenkomst moet overeenkomen met de valuta van de geselecteerde leverancier. De hoofdplanning bevat alleen informatie uit de regels van de inkoophandelsovereenkomst waarvan de valuta overeenkomt met de valuta van de leverancier.

## <a name="examples-of-how-planning-optimization-finds-vendor-and-lead-times"></a>Voorbeelden van de manier waarop in Planningsoptimalisatie leveranciers en levertijden worden gevonden

De volgende tabel bevat voorbeelden die laten zien hoe verschillende instellingen voor een vrijgegeven product en de bijbehorende inkoophandelsovereenkomsten van invloed zijn op de waarden die voor de resulterende geplande inkooporder zijn gevonden. De **vette** waarden in de twee kolommen uiterst rechts zijn de waarden die zijn geselecteerd door Planningsoptimalisatie. De *_vette en cursieve_* waarden in de andere kolommen zijn de instellingen die de resulterende waarden voor elke rij hebben opgeleverd.

| Vrijgegeven product: Leverancier | Standaard orderinstellingen: Levertijd | Artikelbehoefteplanning: Leverancier overschrijven | Artikelbehoefteplanning: Levertijd overschrijven | Handelsovereenkomst: Leverancier | Handelsovereenkomst: Levertijd | Handelsovereenkomst: Levertijd negeren | Resulterende leverancier | Resulterende levertijd |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| _*_US001_*_ | _*_1_*_ | No | No | US003 | 3 | No | _ *US001** | **1** |
| US001 | 1 | **_Ja: US002_* _ | _*_Ja: 2_*_ | US003 | 3 | No | _ *US002** | **2** |
| *(Leeg)* | 1 | No | No | ***US003** _ | _*_3_*_ | No | _ *US003** | **3** |
| *(Leeg)* | ***1** _ | No | No | _*_US003_*_ | 3 | Ja | _ *US003** | **1** |
| *(Leeg)* | ***1** _ | _*_Ja: US002_*_ | No | US003 | 3 | No | _ *US002** | **1** |
| *(Leeg)* | ***1** _ | _*_Ja: US002_*_ | No | US003 | 3 | No | _ *US002** | **1** |
| *(Leeg)* | 1 | No | Ja: 2 | ***US003** _ | _*_3_*_ | No | _ *US003** | **3** |
| *(Leeg)* | 1 | No | ***Ja: 2** _ | _*_US003_*_ | 3 | Ja | _ *US003** | **2** |

## <a name="additional-resources"></a>Aanvullende bronnen

[Inkoopovereenkomsten](../../procurement/purchase-agreements.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]