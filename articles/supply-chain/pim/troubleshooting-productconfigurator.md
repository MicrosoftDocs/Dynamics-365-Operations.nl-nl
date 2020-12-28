---
title: Problemen met de productconfigurator oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met de productconfigurator.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dacc7205eaf2084f6fbd3be9d8ac0572f9e1bcde
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516759"
---
# <a name="troubleshoot-the-product-configurator"></a>Problemen met de productconfigurator oplossen

In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met de productconfigurator.

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a>De tekst van een artikel wordt overschreven wanneer ik een product configureer op een verkooporderregel.

### <a name="issue-description"></a>Probleembeschrijving

Dit probleem doet zich voor wanneer u een verkooporderregel voor een configureerbaar artikel maakt en vervolgens de tekst van het artikel wijzigt. Wanneer u het artikel configureert en vervolgens **OK** selecteert, wordt de tekst overschreven met de standaardtekst.

### <a name="issue-resolution"></a>Probleemoplossing

Dit gedrag is verwacht. Het tekstveld bevat de variantnaam, die alleen wordt ingevuld nadat u de regel hebt geconfigureerd. Daarom moet u de tekst wijzigen nadat u de regel hebt geconfigureerd.

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>De kenmerken van gehele getallen worden onjuist afgerond wanneer de productconfiguratiemodellen worden berekend.

### <a name="issue-description"></a>Probleembeschrijving

Dit probleem kan optreden wanneer u de volgende reeks acties uitvoert:

1. Stel de volgende kenmerken in op een productieconfiguratiemodel:

    - Invoer (geheel getal)
    - Percentage (decimaal)
    - Resultaat (geheel getal)

2. Maak een berekening die de volgende expressie bevat:

    *Resultaat* = *invoer* × *procent* ÷ 100

In dit geval wordt het resultaat van het gehele getal niet altijd juist afgerond. De invoer is bijvoorbeeld 1000 en het percentage is 2,40. Daarom verwacht u dat het resultaat van een geheel getal 24 is, omdat 2,40 procent van 1000 24 is (of 24,00 in decimale notatie). In plaats daarvan wordt het resultaat weergegeven als 23. Wanneer het percentage echter 2,39 is, wordt de berekening afgerond naar 24 in plaats van 23. Wanneer het percentage 2,50 is, wordt de berekening afgerond naar 25, zoals verwacht.

### <a name="issue-resolution"></a>Probleemoplossing

Dit probleem doet zich voor vanwege de manier waarop getallen door Microsoft Solver Foundation intern worden aangeduid met breuken. Voor het bovenstaande voorbeeld wordt het resultaat van de berekening waarbij het percentage 2,40 is, weergegeven als 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375. Wanneer .NET deze waarde als een geheel getal converteert, wordt 23 geretourneerd.

Dit gedrag wordt niet gewijzigd, omdat andere scenario's hiervan afhankelijk zijn. Voor het voorgaande voorbeeld kunt u het probleem oplossen door een extra, decimaal kenmerk en een berekening te introduceren.

Stel bijvoorbeeld de volgende kenmerken in op een productieconfiguratiemodel:

- Invoer (geheel getal)
- Percentage (decimaal)
- ResultDecimal (decimaal)
- ResultInteger (geheel getal)

Vervolgens kunt u de volgende berekeningen toevoegen:

- *ResultDecimal* = *invoer* × *procent* ÷ 100
- *ResultInteger* = *ResultDecimal*
