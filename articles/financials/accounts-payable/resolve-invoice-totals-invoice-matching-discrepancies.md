---
title: Verschillen m.b.t. factuurtotalen tijdens factuurvereffening oplossen
description: U kunt factuurtotaalvergelijking gebruiken om te zorgen dat totaalfactuurbedragen niet afwijken van verwachte bedragen met meer dan een acceptabel verschil.
author: abruer
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63f4747c13d70d45404069a200124336d6f54947
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/25/2019
ms.locfileid: "896345"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching"></a>Verschillen m.b.t. factuurtotalen tijdens factuurvereffening oplossen

[!include [banner](../includes/banner.md)]

Een type factuurvereffeningsvalidatie is de factuurtotalenvereffening. Om op te geven dat het systeem factuurvereffening voor totalen moet uitvoeren, stelt u op de pagina **Parameters van module Leveranciers** op het tabblad **Factuurvalidatie** u de optie **Factuurtotalen vereffenen** in op **Ja**. 

U kunt factuurtotaalvergelijking gebruiken om te zorgen dat totaalfactuurbedragen niet afwijken van verwachte bedragen met meer dan een acceptabel verschil. Er worden zes totalen vergeleken op de **Totale factuurvereffeningsgegevens** pagina. Indien een van de totalen afwijkt van het verwachte corresponderende inkoopordertotaal, wordt een matchingverschil gemarkeerd. 

Om de factuur met verschillende totalen in te zien, klikt u in de werkruimte op in de **Leveranciersfactuurregistratie** op de regel **Facturen in behandeling**. Klik vervolgens in het actievenster op het tabblad **Controleren** op **Vereffeningsgegevens**. Als vereffeningsverschillen zijn gevonden, worden waarschuwende pictogrammen naast het factuurbedrag weergegeven. U kunt meer details over de totalen weergeven door de vergelijkingsgegevens van de factuurtotalen te bekijken. 

Nadat u het verschil hebt aangegeven, kunt u contact opnemen met de leverancier als u denkt dat de informatie op de factuur niet klopt. Afhankelijk van de uitkomst van dat gesprek kan de leverancier een van de volgende dingen doen:

-   Accepteer het prijsverschil en boek de factuur die matchingverschillen bevat. Uw systeem kan worden ingesteld om goedkeuring te vereisen voordat kan worden geboekt als er vereffeningsverschillen zijn. In dit geval moet u het vereffeningverschil goedkeuren en kunt u desgewenst een goedkeuringopmerking invoeren. U kunt vervolgens de factuur boeken.
-   Het factuurbedrag met het juiste bedrag corrigeren en de factuur boeken.
-   Een volledig credit aan de leverancier vragen en om een nieuwe, gecorrigeerde factuur verzoeken.

Zie voor meer informatie [Uitzonderingen onderzoeken of oplossen](tasks/research-resolve-exceptions.md).


