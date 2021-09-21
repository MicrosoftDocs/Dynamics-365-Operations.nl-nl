---
title: Hoeveelheid niet geldig voor order verzamelen met meerdere nummerplaten
description: Wanneer er orderverzamelingswerk is met meerdere nummerplaten op één locatie, is de eenheid niet geldig voor de eenheid stuks. Controleer of de volgende velden juist zijn.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5b245f71e80339fee3e42cfffa0396078a56926e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475971"
---
# <a name="quantity-not-valid-when-theres-picking-work-with-multiple-lps-in-one-location"></a>Hoeveelheid is niet geldig als er orderverzamelingswerk is met meerdere nummerplaten op één locatie

## <a name="symptoms"></a>Symptomen

Wanneer er orderverzamelingswerk is met meerdere nummerplaten op één locatie, is de eenheid niet geldig voor de eenheid *stuks* en wordt het volgende foutbericht weergegeven.

> De hoeveelheid is niet geldig voor eenheid 1%.

## <a name="resolution"></a>Oplossing

Controleer of de velden **Volgordegroep-id eenheid** en **Eenheidsomrekeningen** op het vrijgegeven product of de productvariant juist zijn ingesteld.

Het foutbericht is verbeterd in versie 10.0.15. In het bericht wordt nu de verwachte hoeveelheid aangegeven (zie [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Het nieuwe foutbericht is:

> De hoeveelheid is niet geldig. Verwacht %1 %2.
