---
title: Belastingcomponenten voor het belastingtype TDS instellen
description: In dit onderwerp wordt uitgelegd hoe u componenten voor bronbelasting, zoals Huur en Contractant, moet instellen voor het belastingtype TDS (belasting ingehouden op bron). Daarnaast wordt uitgelegd hoe u de drempellimiet definieert die wordt gebruikt om TDS te berekenen voor elke TDS-component.
author: kailiang
ms.date: 02/12/2021
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
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 9c86341f7528e2c85b813e4f825ae34f10680a9b
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727112"
---
# <a name="set-up-tax-components-for-the-tds-tax-type"></a>Belastingcomponenten voor het belastingtype TDS instellen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u componenten voor bronbelasting, zoals Huur en Contractant, moet instellen voor het belastingtype TDS (belasting ingehouden op bron). De TDS-compenten zijn TDS, toeslag, PE-Cess en SHE Cess. In dit onderwerp wordt daarnaast uitgelegd hoe u de drempellimiet definieert die wordt gebruikt om TDS te berekenen voor elke TDS-component. Daarnaast kunt u een uitzonderingsdrempel definiëren die wordt gebruikt om TDS te berekenen voor elke TDS-component.

Voer de volgende stappen uit om TDS-componenten in te stellen.

1. Ga naar **Belasting \> Instellen \> Bronbelasting \> Bronbelastingcomponenten**.

    [![Pagina Bronbelastingcomponenten.](./media/apac-ind-TDS-9.png)](./media/apac-ind-TDS-9.png)

2. Selecteer in het veld **Belastingtype** de optie **TDS** om bronbelastingcomponenten in te stellen voor het belastingtype TDS.
3. Selecteer in het actievenster **Nieuw** om een regel te maken.
4. Voer in het veld **Bronbelastingcomponent** een naam in voor de TDS-component.
5. Selecteer in het veld **Componentgroep voor bronbelasting** de TDS-bronbelastingcomponentgroep waar u de TDS-component aan wilt koppelen.
6. Typ op het sneltabblad **Algemeen** in het veld **Omschrijving** een beschrijving van de TDS-component.
7. Selecteer in het actievenster **Drempel** om de pagina **Drempel** te openen zodat u de drempel kunt definiëren die wordt gebruikt om TDS te berekenen voor de TDS-component.
8. Met de velden **Begindatum** en **Einddatum** kunt u de periode definiëren waarop de drempel van toepassing is.
9. Voer op het sneltabblad **Algemeen** in het veld **Drempel** het drempelbedrag in dat wordt gebruikt om TDS te berekenen voor de TDS-component. De btw wordt alleen bij de bron ingehouden als het cumulatieve factuurbedrag de drempel overschrijdt.

    Als het drempelbedrag bijvoorbeeld 10.000 is, wordt TDS berekend nadat het cumulatieve factuurbedrag hoger is dan 10.000 (met andere woorden wanneer het 10.001 of meer is).

10. Voer in het veld **Uitzonderingsdrempel** het uitzonderingsdrempelbedrag in dat wordt gebruikt om TDS te berekenen voor de TDS-component. De belasting op een factuurregel wordt alleen bij de bron ingehouden als het cumulatieve factuurbedrag de uitzonderingsdrempel overschrijdt.

    Als het uitzonderingsdrempelbedrag bijvoorbeeld 5.000 is, wordt TDS berekend op een specifieke factuurregel als het bedrag van de factuurregel hoger is dan 5.000 (met andere woorden, als het 5.001 of meer is).

    [![Pagina Drempel.](./media/apac-ind-TDS-10.png)](./media/apac-ind-TDS-10.png)

    > [!NOTE]
    > Het uitzonderingsdrempelbedrag moet lager zijn dan of gelijk zijn aan het drempelbedrag.
    >
    > De belasting wordt voor een transactie ingehouden als het transactiebedrag de uitzonderingsdrempel overschrijdt, zelfs als het cumulatieve factuurbedrag de drempel die is opgegeven in het veld **Drempel** niet overschrijdt.

11. Sluit de pagina **Drempel** om terug te keren naar de pagina **Bronbelastingcomponenten**.
12. Selecteer in het actievenster **Kopiëren** om het dialoogvenster **Bronbelastingcomponenten kopiëren** te openen, zodat u de TDS-componenten die voor een TDS-componentgroep zijn ingesteld, naar een andere TDS-componentgroep kunt kopiëren.
13. Selecteer in het veld **Van** de TDS-componentgroep waar vandaan u de TDS-componenten wilt kopiëren. Selecteer in het veld **Naar** de componentgroep voor bronbelasting waar u de TDS-componenten naar wilt kopiëren.

    > [!NOTE]
    > Veelgebruikte TDS-componenten die aan beide TDS-componentgroepen zijn gekoppeld, worden niet gekopieerd.

14. Selecteer **OK** om TDS-componenten te kopiëren en te maken voor de andere TDS-componentgroep op de pagina **Bronbelastingcomponenten**.

    [![Dialoogvenster Bronbelastingcomponenten kopiëren.](./media/apac-ind-TDS-11.png)](./media/apac-ind-TDS-11.png)

15. Sluit de pagina.
