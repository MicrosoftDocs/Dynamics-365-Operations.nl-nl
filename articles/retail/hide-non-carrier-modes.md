---
title: Leveringsmethoden voor niet-vervoerders verbergen in de verzendopties in POS
description: In dit onderwerp wordt een configuratieoptie beschreven waarmee u kunt voorkomen dat leveringsmethoden voor niet-vervoerders worden weergegeven voor selectie wanneer verzendorders worden gemaakt in de POS-toepassing.
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 09ea83b3336b208f8af0a91025c2e6c50d64c385
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/24/2019
ms.locfileid: "2659016"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a>Leveringsmethoden voor niet-vervoerders verbergen in de verzendopties in POS

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp wordt een configuratieoptie beschreven die beschikbaar is voor de POS-toepassing. Met deze configuratieoptie wijzigt u het gedrag voor de selectie van leveringsmethoden wanneer verzendorders worden gemaakt in POS.

Wanneer gebruikers verzendorders voor een klant maken in POS, kunnen ze een leveringsmethode selecteren voor de zending. Deze functionaliteit is beschikbaar ongeacht of de gehele order wordt verzonden of alleen geselecteerde regels.

Standaard worden in het dialoogvenster waarin een leveringsmethode wordt geselecteerd, alle geldige leveringsmethoden weergegeven voor de combinatie van kanaal, artikel en afleveradres. Deze leveringsmethoden worden gedefinieerd op de pagina **Leveringsmethoden** in Retail Headquarters (**Verkoop en marketing \> Instellingen \> Distributie \> Leveringsmethoden**). De leveringsmethoden "niet-vervoerders", zoals **Uitvoeren** of **Ophalen**, kunnen ook worden weergegeven voor selectie in het dialoogvenster.

Er is echter een functie toegevoegd waarmee u de leveringsmethoden voor niet-vervoerders kunt verbergen in het dialoogvenster. Als u deze functie wilt inschakelen, stelt u op de pagina **Detailhandelparameters** op het tabblad **Klantorders** de optie **Alleen opties voor vervoerdersmethoden weergeven voor verzendorders** in op **Ja**. Nadat u deze functie hebt ingeschakeld en de desbetreffende distributietaken hebt uitgevoerd om de informatie te synchroniseren met de kanaaldatabase, worden de leveringsmethoden voor niet-vervoerders niet weergegeven voor selectie tijdens het maken van verzendorders in POS.
