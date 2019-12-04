---
title: Aan de slag met Planningsoptimalisatie
description: In dit onderwerp wordt uitgelegd hoe u aan de slag gaat met de functionaliteit Planningsoptimalisatie.
author: ChristianRytt
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 37c2acb2397b2a0ad69272c0645bd200a8d7910d
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773931"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="get-started-with-planning-optimization"></a>Aan de slag met Planningsoptimalisatie

De functie Planningsoptimalisatie ondersteunt momenteel niet alle functies die beschikbaar zijn in de planningsengine die is ingebouwd in Microsoft Dynamics 365 Supply Chain Management. Het is daarom belangrijk dat u evalueert of de functieset die momenteel beschikbaar is in Planningsoptimalisatie voldoet aan uw behoeften. Standaard is de functionaliteit Planningsoptimalisatie niet ingeschakeld in Dynamics Lifecycle Services (LCS). Daarom hebt u de mogelijkheid om uw beoordeling uit te voeren voordat deze is ingeschakeld.

Uiteindelijk vervangt Planningsoptimalisatie de bestaande ingebouwde Supply Chain Management-planningsengine.

Voordat u Planningsoptimalisatie inschakelt, kunt u het beste de resultaten van de analyse voor passende Planningsoptimalisatie evalueren. Zie [Analyse voor passende Planningsoptimalisatie](planning-optimization-fit-analysis.md) voor meer informatie.

### <a name="licensing"></a>Licenties

Als u de hoofdplanning kunt uitvoeren met uw huidige licentie, hoeft u geen extra licentie aan te schaffen om Planningsoptimalisatie te kunnen gebruiken.

### <a name="install-the-add-in"></a>De invoegtoepassing installeren

Als u Planningsoptimalisatie wilt gebruiken, moet u de invoegtoepassing Planningsoptimalisatie voor Dynamics 365 Supply Chain Management gebruiken. U kunt de invoegtoepassing openen vanuit uw LCS-project en de functie Planningsoptimalisatie inschakelen via de gebruikersinterface van Supply Chain Management.

1. Meld u aan bij LCS en open de gewenste omgeving.
1. Ga naar **Volledige details**.
1. Selecteer **Onderhouden** of ga omlaag naar het sneltabblad **Invoegtoepassingen voor omgeving**.
1. Selecteer **Een nieuwe invoegtoepassing installeren**.
1. Selecteer **Planningsoptimalisatie**.
1. Volg de installatiehandleiding en ga akkoord met de voorwaarden en bepalingen.
1. Selecteer **Installeren**.

### <a name="planning-optimization-integration"></a>Integratie van Planningsoptimalisatie

Als u wilt configureren of de invoegtoepassing Planningsoptimalisatie moet worden gebruikt voor de hoofdplanning, gaat u naar **Hoofdplanning** \> **Instellen** \> **Integratie van Planningsoptimalisatie** \> **Integratieparameters**.

#### <a name="connection-status"></a>Verbindingsstatus

De verbindingsstatus geeft de huidige status aan van de verbinding tussen Supply Chain Management en de service Planningsoptimalisatie. De volgende tabel bevat de mogelijke waarden.

| Verbindingsstatus | Beschrijving | Kan Planningsoptimalisatie worden gebruikt? |
|---|---|---|
| Verbonden | Er is een verbinding tot stand gebracht tussen de service Planningsoptimalisatie en Supply Chain Management. | Ja |
| Verbinding wordt ingeschakeld | Een aanvraag om de verbinding met de service Planningsoptimalisatie in te schakelen, wordt momenteel uitgevoerd. | Nee |
| Niet verbonden | Er is geen verbinding met de service Planningsoptimalisatie. De verbinding kan worden ingeschakeld vanuit LCS, zoals eerder in dit onderwerp is beschreven. | Nee |
| Verbinding wordt uitgeschakeld | Een aanvraag om de verbinding met de service Planningsoptimalisatie uit te schakelen, wordt momenteel uitgevoerd. | Nee |
| Status ophalen | Het systeem wacht op statusinformatie van de service Planningsoptimalisatie. | Nee |

#### <a name="the-use-planning-optimization-option"></a>De optie Planningsoptimalisatie gebruiken

De instelling van de optie **Planningsoptimalisatie gebruiken** bepaalt welke planningsengine wordt gebruikt voor de hoofdplanning:

- **Ja**: Planningsoptimalisatie wordt gebruikt voor de hoofdplanning.
- **Nee**: de ingebouwde planningsengine voor Supply Chain Management wordt gebruikt voor de hoofdplanning.

> [!NOTE]
> Als bestaande planningsbatchtaken die zijn gemaakt voor de ingebouwde Supply Chain Management-planningsengine worden geactiveerd terwijl de optie **Planningsoptimalisatie gebruiken** is ingesteld op **Ja**, mislukken deze taken.

### <a name="integration-with-the-setup"></a>Integratie met de setup

Als de Planningsoptimalisatie is ingeschakeld, wordt de hoofdplanning uitgevoerd met behulp van de invoegtoepassing Planningsoptimalisatie. In dit geval worden de resultaten en functies van de hoofdplanning beïnvloed.

## <a name="related-resources"></a>Gerelateerde bronnen

[Algemene voorwaarden voor de preview](https://go.microsoft.com/fwlink/?linkid=2015274)

[Overzicht van Planningsoptimalisatie](planning-optimization-overview.md)

[Analyse voor passende Planningsoptimalisatie](planning-optimization-fit-analysis.md)

[Planhistorie en planningslogboeken weergeven](plan-history-logs.md)

[Filters op een plan toepassen](plan-filters.md)

[Een planningstaak annuleren](cancel-planning-job.md)
