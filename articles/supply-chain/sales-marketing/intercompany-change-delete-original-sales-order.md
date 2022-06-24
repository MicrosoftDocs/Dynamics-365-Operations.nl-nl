---
title: Een originele intercompany-verkooporder wijzigen of verwijderen
description: In dit artikel wordt uitgelegd hoe u een oorspronkelijke verkooporderfunctionaliteit kunt wijzigen en verwijderen
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 6ff7eeb00fec7c1b9fa1dc08fa231669f728ed3c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859072"
---
# <a name="change-or-delete-an-original-intercompany-sales-order"></a>Een originele intercompany-verkooporder wijzigen of verwijderen

[!include [banner](../../includes/banner.md)]

Wanneer u een verkooporder wijzigt, worden uw wijzigingen automatisch gesynchroniseerd, zowel met de relevante intercompany-inkooporder als met de intercompany-verkooporder.

> [!NOTE]
> De wijzigingen die u aanbrengt, worden niet doorgevoerd in inkooporders voor externe leveranciers en ook niet in de oorspronkelijke verkooporderregels die zijn gekoppeld aan de inkooporderregels voor externe leveranciers.

In de volgende tabel wordt een overzicht gegeven van de wijzigingen die u kunt aanbrengen en de verwachte resultaten.

| Bewerking | Resultaat |
|---|---|
| Een&nbsp;oorspronkelijke&nbsp;verkooporder&nbsp;verwijderen&nbsp;. | De gerelateerde intercompany-inkooporder en de intercompany-verkooporder worden ook verwijderd. Als de order de status **Orderverzamellijst** of een latere status in het proces heeft, kunt u de verkooporderregel niet verwijderen. |
| Een oorspronkelijke verkooporderregel verwijderen. | De gerelateerde intercompany-inkooporderregel en de intercompany-verkooporderregel worden verwijderd. Als de order de status **Orderverzamellijst** of een latere status in het proces heeft, kunt u de verkooporderregel niet verwijderen. |
| Een nieuwe verkoopregel aan een oorspronkelijke verkooporder toevoegen. | De nieuwe verkoopregel wordt zowel in de intercompany-inkooporder als in de intercompany-verkooporder gemaakt. |
| De hoeveelheid van een oorspronkelijke verkooporderregel wijzigen. | De hoeveelheid wordt zowel met de intercompany-inkooporderregel als met de intercompany-verkooporderregel gesynchroniseerd. Het nettobedrag wordt voor alle orders opnieuw berekend. |
| De rechtstreekse levering voor een originele verkooporder uitschakelen. | U kunt het veld **Rechtstreekse levering** op de oorspronkelijke verkooporder niet wijzigen als de intercompany-verkooporderregel de minimumstatus **Orderverzamellijst**, **Uitvoerorder** of **Orderverzamellijstjournaal** heeft bereikt. Het afleveradres op de intercompany-inkooporder wordt gewijzigd in het standaardafleveradres (standaardafleveradres op de inkooporder). Ook de intercompany-inkooporderregels worden gewijzigd in het standaardafleveradres voor de regels. Beide worden gesynchroniseerd met de intercompany-verkooporder en de verkooporderregels. Het leveringstype in alle regels van de oorspronkelijke verkooporder wordt gewijzigd in **Geen** en het veld wordt gesynchroniseerd met de intercompany-inkooporderregels. De wijzigingen worden niet doorgevoerd in inkooporders voor externe leveranciers en ook niet in de oorspronkelijke verkooporderregels die zijn gekoppeld aan de inkooporderregels voor externe leveranciers. De leveringsdatum op de intercompany-inkooporder en intercompany-inkooporderregels en de aangevraagde ontvangst-/verzenddatums op de intercompany-verkooporder en intercompany-verkooporderregels worden bijgewerkt. |
| De rechtstreekse aflevering voor een oorspronkelijke verkooporder inschakelen. | U kunt het veld **Rechtstreekse levering** op de oorspronkelijke verkooporder niet wijzigen als de intercompany-verkooporderregel de minimumstatus **Orderverzamellijst**, **Uitvoerorder** of **Orderverzamellijstjournaal** heeft bereikt. Het afleveradres in de intercompany-inkooporder wordt gewijzigd in het afleveradres van de oorspronkelijke verkooporder en gesynchroniseerd met de intercompany-verkooporder. Het leveringstype in alle regels van de oorspronkelijke verkooporder wordt gewijzigd in **Rechtstreekse levering** en het veld wordt gesynchroniseerd met de intercompany-inkooporderregels. Het afleveradres op elke oorspronkelijke verkooporderregel wordt gesynchroniseerd met zowel de intercompany-inkooporderregels als met de intercompany-verkooporderregels. De leveringsdatum op de intercompany-inkooporder en intercompany-inkooporderregels en de aangevraagde ontvangst-/verzenddatums op de intercompany-verkooporder en intercompany-verkooporderregels worden bijgewerkt. |
| Een notitie toevoegen aan de kop en de regels van de oorspronkelijk verkooporder. | De notitie wordt naar de intercompany-inkooporder en de intercompany-verkooporder gekopieerd. |
| Een notitie wijzigen of verwijderen. | Als u een notitie wijzigt of verwijdert, wordt ook de bijbehorende notitie in de intercompany-inkooporder en de intercompany-verkooporder gewijzigd of verwijderd. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
