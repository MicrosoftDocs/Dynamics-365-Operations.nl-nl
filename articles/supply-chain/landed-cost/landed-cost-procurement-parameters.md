---
title: Parameters voor inkoopbeheer voor Francoprijzen
description: In dit artikel wordt beschreven hoe u de relevante parameters voor inkoopbeheer kunt instellen wanneer u de module Francoprijzen gebruikt.
author: Weijiesa
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 92ce3e3d09bed15970375735f680b1b8348bbca8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905974"
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
