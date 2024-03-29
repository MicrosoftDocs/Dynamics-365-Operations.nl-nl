---
title: Bronbelasting in inkooptransacties
description: Voor leveranciers die bronbelasting moeten betalen, kunt u de standaard **bronbelastinggroep** toewijzen op de pagina **Alle leveranciers**.
author: kailiang
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: c2220159cef31bf3343bcf39325c7a0ff3e0cf47
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727197"
---
# <a name="withholding-tax-in-purchase-transactions"></a>Bronbelasting in inkooptransacties

Voor leveranciers die bronbelasting moeten betalen, kunt u de standaard **bronbelastinggroep** toewijzen op de pagina **Alle leveranciers**.

1. Ga in het navigatievenster naar **Modules > Leveranciers > Leveranciers > Alle leveranciers**.

2. Klik op de betreffende leveranciersrekening en klik op **Bewerken**.

3. Stel op het tabblad **Factuur en levering** het veld **Bronbelasting berekenen** in op **Ja**.

   > [!NOTE] 
   > Bronbelasting wordt niet berekend als **Bronbelasting berekenen** voor deze leverancier niet wordt ingeschakeld in de gegevens.

4. Selecteer een bronbelastinggroep in **Bronbelastinggroep**.

5. Klik op **Opslaan**.

Voor artikelen/services waarvoor bronbelasting moet worden betaald, kunt u de standaard **artikelbronbelastinggroep** toewijzen in **Vrijgegeven producten**.

1. Ga naar **Navigatievenster > Modules > Productgegevensbeheer > Producten > Vrijgegeven producten**.

2. Klik op het betreffende artikelnummer en klik op **Bewerken**.

3. Klik op het tabblad **Inkopen** op **Bronbelasting berekenen**.

   > [!NOTE] 
   > Bronbelasting wordt niet berekend als **Bronbelasting berekenen** niet op **Ja** is ingesteld voor dit artikel op het tabblad **Inkopen** op de pagina **Vrijgegeven product**.

4. Selecteer een artikelbronbelastinggroep in de lijst **Artikelbronbelastinggroep**.

5. Klik op **Opslaan**.

Bronbelastinggroepen en artikelbronbelastinggroepen kunnen worden toegewezen via de volgende pagina's: 

- **Inkooporder**
- **Leveranciersfactuur**
- **Facturenjournaal**

De standaard bronbelastinggroep en artikelbronbelastinggroep worden naar de regels getransporteerd wanneer u **inkooporders** en/of **leveranciersfacturen in behandeling** maakt. Voor **Leveranciersfactuurjournaal** kunt u **Bronbelasting berekenen** inschakelen en **Artikelbronbelastinggroep** selecteren op het tabblad **Algemeen** van het journaal.

Het tijdelijke bronbelastingbedrag is beschikbaar in het veld **Gecorrigeerde bronbelasting** van het tabblad **Totalen** op de pagina **Inkooporder**.

![Bronbelasting is in de inkooporder opgenomen.](media/withholding-tax-adjusted.png)

Er wordt bronbelasting berekend in **Journaal met betalingen van leverancier**. U kunt de toepasselijke bronbelastingcodes en de werkelijke bronbelastingbedragen handmatig aanpassen op het tabblad **Bronbelasting** op de pagina **Transacties vereffenen**.

![Bronbelasting kan handmatig worden gecorrigeerd op de pagina Transacties vereffenen.](media/withholding-tax-vendor-payment-tab.png)

Het afgeleide bronbelastingbedrag wordt afgetrokken van de leveranciersbetaling en geboekt op de **rekening voor bronbelasting** in een gerelateerd boekstuk.

![Bronbelastingrekening met een gerelateerd boekstuk.](media/withholding-tax-adjusted.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
