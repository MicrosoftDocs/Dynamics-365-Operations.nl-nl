---
title: Leverancierscode niet geautoriseerd voor een specifiek product en specifieke datum
description: Wanneer u een geplande order probeert te fiatteren of een regel aan een inkooporder wilt toevoegen, wordt een foutbericht weergegeven waarin staat dat de leverancierscode niet is geautoriseerd voor een product en datum.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 67cb054a648eac2b9a0e89b5e6a645af3c6142ad25237adb7afbd28f96c7e2eb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777714"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a>Leverancierscode niet geautoriseerd voor een specifiek product en specifieke datum

Foutcode: SYP4881415

## <a name="symptoms"></a>Symptomen

Wanneer u probeert een geplande order te fiatteren of een regel toe te voegen aan een inkooporder, wordt het volgende foutbericht weergegeven:

> Leverancierscode %1 is niet geautoriseerd voor %2 op %3.

## <a name="cause"></a>Oorzaak

De fout treedt op omdat het veld **Controlemethode voor goedgekeurde leveranciers** is ingesteld op *Alleen waarschuwing* of *Niet toegestaan* voor het opgegeven product en de leverancier op dit moment niet is geautoriseerd om dat product te leveren.

## <a name="resolution"></a>Oplossing

Om dit probleem op te lossen, schakelt u de leverancierscontrole voor het relevante product uit of keurt u de leverancier goed.

Volg deze stappen om de leverancierscontrole voor een product uit te schakelen.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Open het relevante product.
1. Stel op het sneltabblad **Inkoop** het veld **Controlemethode voor goedgekeurde leveranciers** in op een andere waarde dan *Alleen waarschuwing* of *Niet toegestaan*.

Volg deze stappen om een leverancier voor een product goed te keuren.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Open het betreffende artikel.
1. Klik in het actievenster in het tabblad **Inkoop** in de groep **Goedgekeurde leverancier** op **Instellingen**.
1. Voeg op de lijstpagina **Goedgekeurde leverancier** een rij toe aan het raster en stel er de volgende waarden voor in:

    - **Leverancier**: selecteer de leverancier die moet worden goedgekeurd voor het huidige product.
    - **Ingangsdatum**: selecteer de eerste datum waarvoor de leverancier is goedgekeurd.
    - **Vervaldatum**: selecteer de laatste datum waarvoor de leverancier is goedgekeurd.

Meer informatie over dit onderwerp vindt u in [Leveranciers goedkeuren voor specifieke producten](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).
