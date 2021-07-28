---
title: Btw-specificatie per grootboektransactie (rapport)
description: In dit onderwerp wordt uitgelegd hoe u het rapport btw-specificatie per grootboektransactie kunt gebruiken om informatie weer te geven en af te drukken over grootboektransacties waarvoor btw wordt berekend.
author: ericwang
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 447d319f5a96851f7eb3104b3330026d269e7dd1
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358804"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a>Btw-specificatie per grootboektransactie (rapport)
[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u het rapport **Btw-specificatie per grootboektransactie** kunt gebruiken om informatie weer te geven en af te drukken over grootboektransacties waarvoor btw wordt berekend.

## <a name="tax-accounts-vs-non-tax-accounts"></a>Btw-rekeningen versus niet-btw-rekeningen

In het rapport **Btw-specificatie per grootboektransactie** worden btw-transacties weergegeven voor zowel btw-rekeningen als niet-btw-rekeningen. Deze rekeningen worden op de volgende manier ingedeeld:

- **Belasting rekening** – een rekening wordt gezien als een belastingrekening wanneer een btw-transactie wordt geboekt, en de hoofdrekening op de **Btw**-journaal regel een btw-rekening is, zoals een rekening voor verschuldigde btw of een rekening voor te ontvangen btw.
- **Niet-belasting rekening** – een rekening wordt gezien als een niet-belastingrekening wanneer een btw-transactie wordt geboekt, en de hoofdrekening op de originele transactie niet-belastingrekening is, zoals een rekening voor inkomstenrekening of een uitgavenrekening.

Voor btw-rekeningen worden de kolommen **Oorsprong**, **Te ontvangen btw** en **Verschuldigde btw** in het rapport weergegeven met **0** (nul). Voor niet-belastingrekeningen bevatten deze kolommen bedragen.

## <a name="filtering-the-data-on-the-report"></a>De gegevens in het rapport filteren

Wanneer u dit rapport genereert, zijn de volgende standaardvelden beschikbaar. U kunt deze velden gebruiken om de gegevens te filteren die in het rapport worden weergegeven.

| Veld                      | Beschrijving |
|----------------------------|-------------|
| Datum                       | Gebruik de velden in de secties **Van** en **Naar** om een datumbereik voor de btw-transacties te definiëren. |
| Hoofdrekening               | Gebruik de velden in de secties **Van** en **Naar** om een datumbereik voor de hoofdrekeningen te definiëren. |
| Btw-code             | Gebruik de velden in de secties **Van** en **Naar** om een datumbereik voor btw-codes te definiëren. |
| Groepering                   | Selecteer of het rapport moet worden gegroepeerd op grootboekrekening of btw-code. |
| Subtotaal per btw-code | Stel deze optie in op **Ja** als u subtotalen per btw-code wilt weergeven. |
| Alleen totalen                | Stel deze optie in op **Ja** als u alleen totalen wilt weergeven. |
| Alleen hoofdrekeningen         | Stel deze optie in op **Ja** als u alleen de hoofdrekeningen in het rapport wilt opnemen. |

## <a name="showing-only-non-tax-accounts-on-the-report"></a>Alleen niet-btw-rekeningen weergeven in het rapport

Als u alleen niet-btw-rekeningen wilt weergeven in het rapport, stelt u een filtervoorwaarde in, zoals een asterisk (\*), zoals wordt weergegeven in de volgende afbeelding.

![Rapport met niet-belastingrekeningen.](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]