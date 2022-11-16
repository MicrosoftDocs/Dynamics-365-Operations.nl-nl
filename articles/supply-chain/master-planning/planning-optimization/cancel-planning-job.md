---
title: Een planningstaak annuleren
description: In dit artikel wordt uitgelegd hoe u een actieve planningstaak kunt annuleren die gebruikmaakt van de functionaliteit Planningsoptimalisatie.
author: t-benebo
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: f5f1f2c8e3e43e36d837ebf989422b0dca7819d6
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741171"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]