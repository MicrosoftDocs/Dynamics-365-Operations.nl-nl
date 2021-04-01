---
title: Aansprakelijkheids-, activa- en onkostentransacties weergeven
description: In dit onderwerp wordt uitgelegd hoe u transacties voor een geleasd activum kunt weergeven. Deze transacties omvatten transacties met leaseverplichtingen en uitgevoerde onkostentransacties die zijn geboekt.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 17753087adb835b4632e929451e2cf3e2d772ed4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249528"
---
# <a name="view-liability-asset-and-expense-transactions"></a>Aansprakelijkheids-, activa- en onkostentransacties weergeven

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u transacties voor een geleasd activum kunt weergeven. Deze transacties omvatten transacties met leaseverplichtingen en uitgevoerde onkostentransacties die zijn geboekt. De boekwaarden van het aansprakelijkheidsactivum en het activum met gebruiksrecht worden in verschillende rapporten gebruikt. Ze worden ook gebruikt om correctiewaarden te berekenen.

## <a name="liability-transactions"></a>Transacties voor leaseverplichtingen

Als u de transacties voor leaseverplichtingen wilt weergeven, selecteert u een lease op de pagina **Leaseoverzicht** en selecteert u **Boeken** om de boeken te openen die aan de leaserecord zijn gekoppeld. Nadat een eerste toerekening, een factuur of een rentejournaal is geboekt, selecteert u **Transacties verplichtingen**.

Op de pagina **Transacties verplichtingen** worden de transacties weergegeven waarmee de leaseverplichting wordt verhoogd of verlaagd. Negatieve bedragen op deze pagina staan voor krediettransacties in de standaardtoepassing. Rentetoerekeningen worden als negatieve waarden weergegeven en verhogen de totale leaseverplichting. Eventuele leasewijzigingen worden weergegeven als positieve of negatieve waarden, afhankelijk van de aard en de impact van het leaseboek. Het huidige netto totaalsaldo van de leaseverplichting voor de geselecteerde lease wordt linksonder op de pagina weergegeven.

## <a name="asset-transactions"></a>Activatransacties

Als u de transacties voor het leaseactivum wilt weergeven, selecteert u een lease op de pagina **Leaseoverzicht** en selecteert u **Boeken** om de leaseboeken te openen die aan de leaserecord zijn gekoppeld. Selecteer vervolgens **Activatransacties**.

Op de pagina **Activatransacties** worden de transacties weergegeven die het leaseactivum en geaccumuleerde afschrijvingsrekeningen verhogen of verlagen. Debetbedragen worden als positieve waarden weergegeven en kredietbedragen worden weergegeven als negatieve waarden, zoals op de pagina **Transacties verplichtingen**. De geboekte eerste toerekening en de volgende samengevoegde afschrijving worden in de linkerbenedenhoek van de pagina weergegeven als het activasaldo. 

## <a name="expenses-transactions"></a>Onkostentransacties

Als u de onkostentransacties voor de lease wilt weergeven, selecteert u een lease op de pagina **Leaseoverzicht** en selecteert u **Boeken** om de leaseboeken te openen die aan de leaserecord zijn gekoppeld. Slecteer vervolgens **Onkostentransacties**.

Op de pagina **Onkostentransacties** worden alle onkosten weergegeven die zijn geboekt tegen de lease, zoals rentelasten, afschrijvingskosten en de administratieve kosten.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]