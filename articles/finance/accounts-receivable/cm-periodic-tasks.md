---
title: Periodieke taken voor kredietbeheer
description: In dit onderwerp worden de periodieke taken beschreven die een onderdeel zijn van het proces voor het beheren van kredietlimieten voor klanten.
author: JodiChristiansen
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 53b7cd00b3287f18ba65391842ac259ab2434b86
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735431"
---
# <a name="periodic-credit-management-tasks"></a>Periodieke taken voor kredietbeheer

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de periodieke taken beschreven die een onderdeel zijn van het proces voor het beheren van kredietlimieten voor klanten.

## <a name="update-risk-scores"></a>Risicoscores bijwerken

Naarmate bedrijven zich ontwikkelen en omstandigheden veranderen, is het mogelijk dat de kredietrisico's voor een bepaalde klant ook veranderen. Om de benodigde kredietlimieten voor uw klanten te onderhouden, moet u regelmatig de criteria voor elke risicoscore controleren en de scores voor elke klant bijwerken. U kunt de volgende scores bijwerken op de pagina **Risicoscores bijwerken** (**Crediteringen en aanmaningen \> Periodieke taken \> Kredietbeheer \> Risicoscores bijwerken**). Alle door de gebruiker gedefinieerde berekeningen worden ook verwerkt.

- **Gemiddeld aantal betaaldagen**: deze score is het gemiddelde aantal dagen waarop een klant facturen gaat betalen.
- **Klant sinds**: deze score is het aantal jaar dat een klant klant is van uw organisatie.
- **Doet zaken sinds**: deze score is het aantal jaar dat een klant zaken doet. Hiervoor wordt de waarde van het veld **Begin bedrijf** op de pagina **Klanten** gebruikt.
- **Dagen uitstaande verkoop**: deze score is gebaseerd op het saldo van de klant, de omzet en het aantal dagen voor de vorige periode van twaalf maanden.
- **Gemiddeld saldo** : deze score is gebaseerd op het saldo van de klant voor de vorige periode van twaalf maanden.
- **Kredietbeheergroep**, **Rekeningstatus** en **Land** : deze scores gebruiken gegevens van de klant.

## <a name="update-customer-balance-statistics"></a>Saldostatistieken van klant bijwerken

U kunt het proces **Saldostatistieken van klant bijwerken** uitvoeren om de berekening van saldostatistieken bij te werken die worden weergegeven op de pagina **Saldostatistieken opvragen**. Deze informatie wordt gebruikt voor het berekenen van risicoscores en de waarden die worden weergegeven in de feitenblokken met kredietstatistieken op de pagina **Klant**.

Wanneer u het proces uitvoert, worden saldostatistieken voor één klant bijgewerkt. Als u een batchtaak wilt instellen om het proces uit te voeren voor meerdere klanten, kunt de pagina **Saldostatistieken berekenen** gebruiken (**Kredietbeheer \> Periodieke taken \> Saldostatistieken berekenen**).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
