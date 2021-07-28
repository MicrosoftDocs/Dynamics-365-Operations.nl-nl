---
title: Bronbelastingcodes voor het TDS-belastingtype instellen
description: In dit onderwerp wordt uitgelegd hoe u belastingcodes moet instellen voor TDS (belasting ingehouden op bron).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 57de382c6d363a6c1d87cf734e9aedb32d6009a9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349923"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a>Bronbelastingcodes voor het TDS-belastingtype instellen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u belastingcodes moet instellen voor TDS (belasting ingehouden op bron).

1. Ga naar **Belasting \> Indirecte belastingen \> Bronbelasting \> Bronbelastingcodes**.

    [![Pagina Bronbelastingcodes.](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)

2. Selecteer in het actievenster **Nieuw** om een bronbelastingcode voor TDS te maken en voer de vereiste gegevens in.
3. Selecteer op het sneltabblad **Algemeen** in het veld **Belastingtype** de optie **TDS** om de belastingcode als een TDS-belastingcode te categoriseren.
4. Selecteer in het veld **Vereffeningsperiode** de TDS-vereffeningsperiode voor de TDS-belastingcode.
5. Selecteer in het veld **Hoofdrekening** de grootboekrekening waar het TDS-bedrag naar moet worden geboekt.
6. Selecteer in het veld **Debiteurenrekening** de debiteurenrekening waar het TDS-bedrag, dat wordt afgetrokken in verkooptransacties, naar moet worden geboekt.

    Het veld **Oorsprong** wordt automatisch ingesteld op **Percentage van brutobedrag** en de waarde kan niet worden gewijzigd.

    > [!NOTE]
    > U kunt de oorsprong niet instellen op **Percentage van nettobedrag** voor belastingcodes van het TDS-belastingtype.

7. Selecteer in het veld **Bronbelastingcomponent** de TDS-belastingcomponent voor de TDS-belastingcode.
8. Selecteer **Waarden** in het actievenster om de pagina **Bronbelastingwaarden** te openen.
9. Voer in het veld **Begindatum** de begindatum in voor de TDS-waarde. Voer in het veld **Einddatum** de einddatum in.

    > [!NOTE]
    > De velden **Ondergrens**, **Bovengrens** en **% uitsluiten** zijn niet beschikbaar voor belastingcodes van het TDS-belastingtype.

10. Voer in het veld **Waarde** het TDS-percentage in voor de TDS-belastingcode.
11. Sluit de pagina **Bronbelastingwaarden** om terug te keren naar de pagina **Bronbelastingcodes**.

    > [!NOTE]
    > De knop **Limieten** op de pagina **Bronbelastingcodes** is niet beschikbaar voor belastingcodes van het TDS-belastingtype.

12. Sluit de pagina.
