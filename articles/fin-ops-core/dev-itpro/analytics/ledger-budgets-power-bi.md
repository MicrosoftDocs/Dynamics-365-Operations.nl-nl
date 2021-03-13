---
title: Werkelijk vs. budget Power BI-inhoud
description: In dit onderwerp wordt de Power BI-inhoud Werkelijk vs. budget besproken. Er wordt uitgelegd hoe u de rapporten kunt openen en u vindt informatie over het gegevensmodel.
author: panolte
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 908b96af5b3d67f265953648edd6aa7ec31556a4
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093843"
---
# <a name="actual-vs-budget-power-bi-content"></a>Werkelijk vs. budget Power BI-inhoud

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt de Power BI-inhoud **Werkelijk vs. budget** besproken. U vindt hier een uitleg hoe u toegang krijgt tot de Power BI-rapporten en informatie over het gegevensmodel en de entiteiten waarmee de inhoud is samengesteld.

## <a name="overview"></a>Overzicht

De Power BI-inhoud **Werkelijk vs. budget** is gemaakt voor personen die verantwoordelijk zijn voor het controleren van werkelijke versus budget-prestaties in hun organisatie. De Power BI-inhoud **Werkelijk vs. budget** biedt inzicht in uw budgetafwijkingen. U kunt het budget voor het huidige jaar analyseren op rekeningcategorie, budgetcode, hoofdrekening, omschrijvingen van hoofdrekeningen of boekperiode, om beter inzicht te verkrijgen in de oorzaken van eventuele afwijkingen.

## <a name="accessing-the-power-bi-content"></a>Toegang tot de Power BI-inhoud
Rapporten uit de Power BI-inhoud **Werkelijk vs. budget** worden weergegeven in de werkgebieden **Grootboekbudgetten en prognoses** en **CFO**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporten die zijn opgenomen in de Power BI-inhoud
De volgende tabel bevat informatie over de metrische gegevens op elke rapportpagina in de Power BI-inhoud **Werkelijk vs. budget**.

| Rapport                      | Metrische gegevens                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| Onkosten - werkelijk versus gebudgetteerd | <ul><li>Totale kosten dit jaar</li><li>Gebudgetteerde totale kosten dit jaar</li></ul>  |
| Opbrengst - werkelijk versus gebudgetteerd  | <ul><li>Totale omzet dit jaar</li><li>Gebudgetteerde totale omzet dit jaar</li><ul>     |
| Uitgaven                     | <ul><li>Totale kosten dit jaar</li><li>Doel voor onkosten op basis van budget</li><ul> |
| Opbrengst                     | <ul><li>Totale omzet dit jaar</li><li>Doel voor omzet op basis van budget</li><ul>   |
| Netto-inkomsten                  | <ul><li>Netto-inkomsten dit jaar</li><li>Doel voor netto-inkomsten op basis van budget</li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a>Het gegevensmodel en de gegevensentiteiten begrijpen

| Entiteit                    | Inhoud                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| Grootboekactiviteiten | Transactiebedragen voor het grootboek                                       |
| Budgetactiviteiten         | Transactiebedragen voor het budgetregister                                      |
| Hoofdrekeningen             | Hoofdrekeningen om rapporten op te filteren                                               |
| Fiscale kalenders          | Fiscale kalenders om rapporten op te filteren                                            |
| Grootboeken                   | Grootboeken die kunnen worden gebruikt om het rapport te filteren naar het huidige grootboek              |
| Budgetcodes              | Budgetcodes om rapporten op te filteren                                                |
| Rechtspersonen            | Rechtspersonen die kunnen worden gebruikt om het rapport te filteren naar de huidige rechtspersoon |
