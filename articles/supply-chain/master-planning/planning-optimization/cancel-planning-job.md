---
title: Een planningstaak annuleren
description: In dit onderwerp wordt uitgelegd hoe u een actieve planningstaak kunt annuleren die gebruikmaakt van de functionaliteit Planningsoptimalisatie.
author: ChristianRytt
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: e9cf4902251c3c2b93af12a8ad9bd571930ef769
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833324"
---
# <a name="cancel-a-planning-job"></a>Een planningstaak annuleren

[!include [banner](../../includes/banner.md)]

In Microsoft Dynamics 365 Supply Chain Management kunt u een actieve planningstaak annuleren die gebruikmaakt van de functionaliteit Planningsoptimalisatie. Wanneer u **Annuleren** selecteert in het dialoogvenster wanneer een taak voor Planningsoptimalisatie rechtstreeks vanuit de gebruikersinterface wordt geactiveerd (niet op de achtergrond), wordt de taak voor Planningsoptimalisatie niet geannuleerd. Zelfs als u een waarschuwing ontvangt zoals 'Bewerking geannuleerd', moet u nog steeds de volgende stappen uitvoeren om een planningstaak met Planningsoptimalisatie te annuleren.


Voer de volgende stappen uit om een actieve planningstaak te annuleren. 

> [!NOTE]
> Alleen actieve taken kunnen worden geannuleerd.

1. Ga naar **Hoofdplanning \> Instellingen \> Plannen**.
2. Selecteer een geschikt plan voor de planningsuitvoering.
3. Selecteer **Historie**.
4. Selecteer de planningstaak die u wilt annuleren
5. Selecteer **Annuleren**.

De taakstatus is **Annuleren** totdat de service Optimalisatie van planning bevestigt dat de taak is geannuleerd. De status wordt vervolgens gewijzigd in **Geannuleerd**.

> [!NOTE]
> Als u statuswijzigingen wilt bekijken, moet u de pagina vernieuwen door op de knop **Vernieuwen** te klikken.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van Planningsoptimalisatie](planning-optimization-overview.md)

[Aan de slag met Planningsoptimalisatie](get-started.md)

[Analyse voor passende Planningsoptimalisatie](planning-optimization-fit-analysis.md)

[Planhistorie en planningslogboeken weergeven](plan-history-logs.md)

[Filters op een plan toepassen](plan-filters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]