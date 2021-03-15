---
title: Onderhoudsbudgetten bijwerken
description: In dit onderwerp wordt uitgelegd hoe u een onderhoudsbudget bijwerkt in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b04549700b51f73a3629fe9cd67a3e1f6c1bafbb
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021015"
---
# <a name="update-maintenance-budgets"></a>Onderhoudsbudgetten bijwerken

[!include [banner](../../includes/banner.md)]

 

Op de pagina **Onderhoudsbudgetregels** worden alle budgetregels weer gegeven die zijn gemaakt voor het budget dat is geselecteerd op de pagina **Onderhoudsbudgetten**. (Zie [Onderhoudsbudgetten maken](create-maintenance-budget.md) voor meer informatie.) U kunt de regels voor het onderhoudsbudget opnieuw berekenen en aanpassen totdat het onderhoudsbudget is goedgekeurd. Nadat de budgetperiode is verstreken en de kosten in het Activabeheer zijn geboekt, kunt u de budgetregels ook bijwerken met de werkelijke kosten.

## <a name="recalculate-a-maintenance-budget"></a>Een onderhoudsbudget opnieuw berekenen

U kunt een onderhoudsbudget opnieuw berekenen op de pagina **Onderhoudsbudgetregels**. Wanneer u een onderhoudsbudget opnieuw berekent, worden de bestaande budgetregels verwijderd en wordt er een nieuwe berekening uitgevoerd.

1. Selecteer op de pagina **Onderhoudsbudgetregels** **Opnieuw berekenen**.
2. Voer in het dialoogvenster **Budget opnieuw berekenen** de vereiste wijzigingen voor de nieuwe berekening in en selecteer vervolgens **OK**.

Nieuwe budgetregels worden gemaakt op basis van de waarden die u instelt.

## <a name="adjust-budget-lines"></a>Budgetregels aanpassen

In plaats van het gehele onderhoudsbudget opnieuw te berekenen, kunt u geselecteerde regels aanpassen die zijn gerelateerd aan budgetkosten.

1. Selecteer op de pagina **Onderhoudsbudgetregels** de regels waarvoor u de budgetkosten wilt bijwerken.
2. Selecteer **aanpassen**.
3. Als u een bedrag wilt toevoegen aan de geselecteerde regels, schakelt u het selectievakje **Kosten toevoegen** in en voert u vervolgens de waarde in het veld **Waarde toevoegen** in.
4. Als u de gebudgetteerde kosten voor de geselecteerde budgetregels met een factor wilt vermenigvuldigen schakelt u het selectievakje **Kosten vermenigvuldigen** in en voert u de factor in het veld **Waarde vermenigvuldigen** in.

    Als u bijvoorbeeld **1,2** invoert in het veld **Waarde vermenigvuldigen**, verhoogt u de budgetkosten voor de geselecteerde regels met 20 procent. Als u **0,7** invoert, verlaagt u de budgetkosten voor de geselecteerde regels met 30 procent.

5. Selecteer **OK**.

De geselecteerde budgetregels worden bijgewerkt volgens de waarden die u in stap 3 of 4 hebt ingesteld.

## <a name="update-actual-costs"></a>Werkelijke kosten bijwerken

Nadat de periode bij de budgetregels is verstreken en de kosten in het Activabeheer zijn geboekt, kunt u de werkelijke kosten bijwerken in het onderhoudsbudget.

1. Selecteer op de pagina **Onderhoudsbudgetregels** **Kosten bijwerken**.
2. Selecteer in het dialoogvenster **Werkelijke kosten berekenen** de optie **OK**.

De velden **Werkelijke kosten** op de budgetregels worden bijgewerkt als de werkelijke kosten zijn geboekt. Er kunnen nieuwe budgetregels worden gegenereerd als er nieuwe activatypen zijn gemaakt nadat u het budget hebt gemaakt, en als deze activatypen zijn gebruikt voor activa waarvoor werkorders zijn gemaakt en gerelateerde kosten zijn geboekt. Op nieuwe budgetregels worden alleen de werkelijke kosten weergegeven, omdat er geen budgetkosten voor zijn berekend.

> [!NOTE]
> Als u een overzicht wilt weergeven van de werkelijke kosten die zijn onderverdeeld in preventieve, corrigerende en investeringskosten, kunt u een berekening uitvoeren voor dezelfde periode op de pagina **Beheer activakosten**. 

## <a name="manually-add-budget-lines"></a>Handmatig budgetregels toevoegen.

Op de pagina **Onderhoudsbudgetregels** kunt u handmatig een nieuwe budgetregel toevoegen door **Nieuw** te selecteren en vervolgens selecties te maken op de regel. Hier volgen enkele voorbeelden van situaties waarin deze aanpak nuttig kan zijn:

- U weet dat de revisie van bepaalde activa momenteel in de planningsfase is, maar gerelateerde taken zijn nog niet in het Activabeheer opgenomen. Budgetkosten voor deze taken moeten echter worden opgenomen in het onderhoudsbudget.
- Nieuwe activa of activatypen zijn gemaakt nadat u het onderhoudsbudget hebt gemaakt, maar er zijn nog geen onderhoudsplannen voor de activa of activatypen ingesteld. Budgetkosten voor deze activatypen moeten echter worden opgenomen in het onderhoudsbudget.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]