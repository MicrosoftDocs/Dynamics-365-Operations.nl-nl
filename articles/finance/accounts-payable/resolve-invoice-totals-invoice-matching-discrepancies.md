---
title: Overzicht van Verschillen m.b.t. factuurtotalen tijdens factuurvereffening oplossen
description: U kunt factuurtotaalvergelijking gebruiken om te zorgen dat totaalfactuurbedragen niet afwijken van verwachte bedragen met meer dan een acceptabel verschil.
author: abruer
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendTotalPriceTolerance
audience: Application User
ms.reviewer: roschlom
ms.custom: 63413
ms.assetid: 9ac42457-95b2-4191-ad06-c7e323704466
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 804800cccdfd0473c9e3514f6c17405eb2ec8335
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827909"
---
# <a name="resolve-discrepancies-during-invoice-totals-matching-overview"></a>Overzicht van Verschillen m.b.t. factuurtotalen tijdens factuurvereffening oplossen

[!include [banner](../includes/banner.md)]

Een type factuurvereffeningsvalidatie is de factuurtotalenvereffening. Om op te geven dat het systeem factuurvereffening voor totalen moet uitvoeren, stelt u op de pagina **Parameters van module Leveranciers** op het tabblad **Factuurvalidatie** u de optie **Factuurtotalen vereffenen** in op **Ja**. 

U kunt factuurtotaalvergelijking gebruiken om te zorgen dat totaalfactuurbedragen niet afwijken van verwachte bedragen met meer dan een acceptabel verschil. Er worden zes totalen vergeleken op de **Totale factuurvereffeningsgegevens** pagina. Indien een van de totalen afwijkt van het verwachte corresponderende inkoopordertotaal, wordt een matchingverschil gemarkeerd. 

Om de factuur met verschillende totalen in te zien, klikt u in de werkruimte op in de **Leveranciersfactuurregistratie** op de regel **Facturen in behandeling**. Klik vervolgens in het actievenster op het tabblad **Controleren** op **Vereffeningsgegevens**. Als vereffeningsverschillen zijn gevonden, worden waarschuwende pictogrammen naast het factuurbedrag weergegeven. U kunt meer details over de totalen weergeven door de vergelijkingsgegevens van de factuurtotalen te bekijken. 

Nadat u het verschil hebt aangegeven, kunt u contact opnemen met de leverancier als u denkt dat de informatie op de factuur niet klopt. Afhankelijk van de uitkomst van dat gesprek kan de leverancier een van de volgende dingen doen:

-   Accepteer het prijsverschil en boek de factuur die matchingverschillen bevat. Uw systeem kan worden ingesteld om goedkeuring te vereisen voordat kan worden geboekt als er vereffeningsverschillen zijn. In dit geval moet u het vereffeningverschil goedkeuren en kunt u desgewenst een goedkeuringopmerking invoeren. U kunt vervolgens de factuur boeken.
-   Het factuurbedrag met het juiste bedrag corrigeren en de factuur boeken.
-   Een volledig credit aan de leverancier vragen en om een nieuwe, gecorrigeerde factuur verzoeken.

Zie voor meer informatie [Uitzonderingen onderzoeken/oplossen](tasks/research-resolve-exceptions.md).




[!INCLUDE[footer-include](../../includes/footer-banner.md)]