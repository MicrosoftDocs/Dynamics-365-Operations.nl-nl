---
title: Onderhoudsbudgetten maken
description: In dit onderwerp wordt uitgelegd hoe u een onderhoudsbudget maakt in Activabeheer.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBudgetLineAdjust, EntAssetBudget, EntAssetBudgetRecalc, EntAssetBudgetCopy, EntAssetBudgetLine, EntAssetBudgetCreate, EntAssetBudgetApprove, EntAssetBudgetCalculateActualCost
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 75deb3dcca2c5a7fd7341b30411e04715bf27c29
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6361181"
---
# <a name="create-maintenance-budgets"></a>Onderhoudsbudgetten maken

[!include [banner](../../includes/banner.md)]

 



Onderhoudsbudgetten worden gebruikt om een overzicht te geven van verwachte kosten voor preventief onderhoud. Budgetregels worden berekend op basis van de regels voor onderhoudsplanning waarvoor de verwachte begindatum gedurende de budgetperiode is verstreken.

Onderhoudsbudgetten zijn gebaseerd op de kostentypen die worden gebruikt in Activabeheer: **Preventief**, **Corrigerend** en **Investering**. Budgetkosten voor investeringsonderhoud worden opgenomen voor actieve activa met een vervangingsdatum gedurende de budgetperiode en een gerelateerde vervangingswaarde. Budgetkosten voor correctief onderhoud worden opgenomen als er een eerdere correctiedatum is opgenomen in de budget berekening. In dat geval worden correctiekosten van een eerdere periode berekend voor dezelfde toekomstige periode waarvoor u het onderhoudsbudget hebt berekend.

## <a name="create-a-maintenance-budget"></a>Een onderhoudsbudget maken

1. Selecteer **Activabeheer** \> **Navragen** \> **Onderhoudsbudget** \> **Budget**.
2. Selecteer **Budget aanmaken**.
3. Voer in het veld **Onderhoudsbudget** een budget-id in.
4. Voer in het veld **Beschrijving** een beschrijving in.
4. Voer in het sneltabblad **Periode** in de velden **Begindatum** en **Einddatum** de begin- en einddatum van de budgetperiode in.
5. Als u gecorrigeerde budgetkosten wilt opnemen die worden berekend op basis van de werkelijke kosten van een vorige periode, voert u in het veld **Corrigerend vanaf datum** de begindatum in van de periode waarvan deze kosten moeten worden opgenomen.
6. Stel, afhankelijk van het vereiste detail niveau in het budget, de relevante opties in op de vijf Sneltabbladen **Groeperen op**.
7. Selecteer **OK**.
8. Selecteer **Budgetregels** om de **Budgetregels voor onderhoud** te openen. Hier kunt u alle budgetregels weergeven die voor de periode zijn gemaakt.
9. Als u het budget wilt goedkeuren, selecteert u het op de pagina **Onderhoudsbudgetten** en selecteert u vervolgens **Goedkeuren**. Selecteer vervolgens in het dialoogvenster **Budget goedkeuren** de optie **OK**. Uw naam wordt ingevoerd in het veld **Goedgekeurd door** op de pagina **Onderhoudsbudgetten**.

    > [!NOTE]
    > Nadat u een onderhoudsbudget hebt goedgekeurd, kunt u de gerelateerde regels niet opnieuw berekenen of aanpassen op de pagina **Budgetregels voor onderhoud**, tenzij u eerst de goedkeuring verwijdert. Als u de goedkeuring van een onderhoudsbudget wilt verwijderen, selecteert u het op de pagina **Onderhoudsbudgetten** en selecteert u vervolgens **Goedkeuren**. Selecteer vervolgens in het dialoogvenster **Budget goedkeuren** de optie **OK**.

![Onderhoudsbudgetten.](media/01-maintenance-budgets.png)

U kunt ook een nieuw onderhoudsbudget maken door een bestaand budget te kopiëren. Selecteer op de pagina **Onderhoudsbudgetten** het te kopiëren budget en selecteer vervolgens **kopiëren**. Deze benadering is handig als u bijvoorbeeld een budget hebt gemaakt voor één maand en dit wilt kopiëren naar andere maanden.

> [!NOTE]
> Het onderhoudsbudget berekent alleen budgetkosten op basis van regels voor onderhoudsplannings. Als u de werkelijke kosten voor dezelfde periode wilt berekenen, kunt u die berekening uitvoeren op de pagina **Kostenbeheer activa**. 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]