---
title: Parameters voor inkoopbeheer voor Francoprijzen
description: In dit onderwerp wordt beschreven hoe u de relevante parameters voor inkoopbeheer kunt instellen wanneer u de module Francoprijzen gebruikt.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ccda3bd769a646e2390711883b8e40bec50e4d6a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020978"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a>Parameters voor inkoopbeheer voor Francoprijzen

[!include [banner](../../includes/banner.md)]

Op de pagina **Parameters voor inkoopbeheer** zijn een paar instellingen beschikbaar die met name relevant zijn wanneer u de module **Francoprijzen** gebruikt. Gebruik het dialoogvenster **Orderregels bijwerken**, dat u kunt openen vanaf de pagina **Parameters voor inkoopbeheer**, om op te geven of inkooporderregels automatisch moeten worden bijgewerkt wanneer er wijzigingen worden aangebracht in de header van de inkooporder.

Volg deze stappen om de instellingen te voltooien.

1. Ga naar **Inkoop en sourcing \> Instellen \> Parameters voor Inkoopbeheer**.
1. Selecteer op het tabblad **Algemeen** de koppeling **Orderregels bijwerken**.
1. In het dialoogvenster **Orderregels bijwerken** worden de velden in de orderkop weergegeven waarmee ook automatische updates kunnen worden toegepast op gerelateerde velden in de orderregels. Stel elk veld in de lijst in op een van de volgende waarden:

    - **Altijd**: de orderregels worden automatisch bijgewerkt wanneer de orderheader wordt bijgewerkt.
    - **Nooit**: de orderregels worden nooit bijgewerkt wanneer de orderheader wordt bijgewerkt.
    - **Vragen**: de gebruiker wordt gevraagd of de orderregels moeten worden bijgewerkt of niet.
