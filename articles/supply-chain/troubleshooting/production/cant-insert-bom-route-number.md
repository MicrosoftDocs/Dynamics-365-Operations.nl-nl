---
title: Kan geen actieve versie van stuklijst- en routenummers invoegen
description: Als de standaardlocatie en het standaardmagazijn al zijn gedefinieerd voor een geselecteerd product, wordt niet gevraagd om de actieve versie van stuklijst- en routenummer in te vullen.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 241618d70f01c85df946a48493f5d84e0964218e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475965"
---
# <a name="cant-insert-bill-of-material-and-route-when-creating-a-new-production-order"></a>Kan geen stuklijst en route invoegen bij het aanmaken van een nieuwe productieorder

## <a name="symptoms"></a>Symptomen

Wanneer u een nieuwe productieorder maakt nadat u het artikelnummer hebt ingevoerd, worden de velden **Locatie** en **Magazijn** automatisch ingesteld op de standaardlocatie en het standaardmagazijn die zijn gedefinieerd op de pagina **Standaardorderinstellingen** voor het gerede artikel. Verder worden het actieve stuklijstnummer en routenummer automatisch ingevoerd, waardoor u niet het volgende bericht ontvangt waarin wordt gevraagd om die waarden:

> Actieve versie voor stuklijst en route invoegen?

## <a name="resolution"></a>Oplossing

U wordt niet gevraagd om stuklijst- en routenummers in te voegen als u een product selecteert waarvoor al een locatie en magazijn zijn gedefinieerd op de pagina **Standaardorderinstellingen**. U wordt er alleen om gevraagd als u deze waarden niet voor het geselecteerde product hebt gedefinieerd.
