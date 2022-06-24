---
title: Financiële dimensies toevoegen aan het CFO-werkgebied
description: In dit artikel wordt uitgelegd hoe u financiële dimensies toevoegt aan het werkgebied CFO zodat ze kunnen worden gebruikt voor grootboek- en budgetrapporten.
author: aprilolson
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: ea453eed826dec2e97371ec559e91b94933bdce6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853375"
---
# <a name="add-financial-dimensions-to-the-cfo-workspace"></a>Financiële dimensies toevoegen aan het CFO-werkgebied

[!include [banner](../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u financiële dimensies toevoegt aan het werkgebied CFO (Chief Financial Officer) zodat ze kunnen worden gebruikt voor grootboek- en budgetrapporten. Het CFO-werkgebied omvat een tabblad **Overzicht** en een tabblad **Financieel**. De rapporten op deze twee tabbladen worden ondersteund door twee maateenheden: LedgerActivityMeasure en BudgetActivityMeasure. Er bestaat een relatie tussen deze twee afmetingen en de DimensionCombinationEntity-entiteit. Daarom kunt u alle dimensies selecteren.

1. Werk in Finance op de pagina **Entiteitopslag** de maateenheden **LedgerActivityMeasure** en **BudgetActivityMeasure** bij.
2. Open Toepassingsverkenner in Microsoft Visual Studio en zoek naar **LedgerCFO**.
3. Open onder **Resources** **LedgerCFOWorkspacePBIX**.
4. Wanneer de resource wordt geopend in Microsoft Power BI Desktop, selecteert u **Gegevens ophalen**, **SQL Server-database** en vervolgens **Verbinden**.
5. Voer de servernaam in en **AxDW** als de gedatabase. Selecteer **DirectQuery** en vervolgens **OK**.
6. Zoek en selecteer **LedgerActivityMeasure\_DimensionCombination**, en selecteer vervolgens **laden**.

    > [!TIP]
    > In de lijst **Velden** wijzigt u de naam van de tabel **Financiële dimensies**, zodat deze gemakkelijk kan worden herkend.

7. Selecteer **Relaties beheren** en selecteer vervolgens **Nieuw**.
8. Selecteer in het eerste veld **Grootboekactiviteiten** en selecteer vervolgens **LedgerDimension**.
9. Selecteer in het tweede veld **LedgerActivityMeasure\_DimensionCombination** (of **Financiële dimensies** als u de naam van de tabel hebt gewijzigd). Selecteer de koptekst **DimensionCombinationRECID**.
10. Selecteer in het veld **Kardinaliteit** **Veel-op-één**.
11. Wijzig de waarde **Cross-filter richting** in **Eén**.
12. Selecteer **Deze relatie actief maken** en **Uitgaan van referentiële integriteit**, selecteer **OK** en vervolgens **Sluiten**.

    [![Een relatie maken.](./media/Create-relationship.png)](./media/Create-relationship.png)

13. In de lijst **Velden** ziet u de tabel en de beschikbare financiële dimensies. Sleep de gewenste financiële dimensies naar de filters voor het rapportniveau.
14. Sla de wijzigingen op.
15. Klik in de Application Object Tree (AOT) met de rechtermuisknop op het project en selecteer **Synchroniseren**.
16. Stel het project samen en open vervolgens de toepassing om de resultaten weer te geven.

    [![Voltooid werkgebied.](./media/workspace.png)](./media/workspace.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
