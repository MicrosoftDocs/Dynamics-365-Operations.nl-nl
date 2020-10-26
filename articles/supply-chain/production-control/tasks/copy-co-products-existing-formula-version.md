---
title: Coproducten uit een bestaande formuleversie kopiëren
description: Deze procedure toont hoe u coproducten van een bestaande formuleversie kopieert naar een andere formuleversie voor een vrijgegeven product.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79b70ccbdac2061baf3896ecbd9449da3c38842a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979398"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a>Coproducten uit een bestaande formuleversie kopiëren

[!include [banner](../../includes/banner.md)]

Deze procedure toont hoe u coproducten van een bestaande formuleversie kopieert naar een andere formuleversie voor een vrijgegeven product. Het is een vereiste dat er minimaal één formuleversie is gekoppeld aan coproducten. Het demobedrijf USP2 wordt gebruikt om deze procedure te maken.


## <a name="find-a-released-product"></a>Een vrijgegeven product zoeken
1. Ga naar Vrijgegeven producten.
2. Klik op Filters weergeven.
    * U staat op het punt het veld Productietype in het filterdialoogvenster toe te voegen.  
3. Klik op Een Filterveld toevoegen om het veld Productietype toe te voegen.
    * In de volgende stap moet u handmatig Formule in het veld Productietype invoeren voordat u Toepassen selecteert. Hiermee wordt het filter ingesteld in de lijst van vrijgegeven producten.  
4. Voer handmatig Formule in het veld Productietype in.
5. Klik op Toepassen.

## <a name="select-a-released-product"></a>Een vrijgegeven product selecteren
1. Zoek en selecteer de gewenste record in de lijst.
2. Klik op Formuleversies.
    * Klik op het actievenster Engineering op Formuleversies.  

## <a name="copy-co-products"></a>Co-producten kopiëren
1. Klik in het actievenster op Formuleversie.
2. Klik op Coproducten.
3. Klik op Kopiëren.
4. Typ of selecteer een waarde in het veld Artikelnummer.
5. Typ of selecteer een waarde in het veld Formuleversie.
6. Klik op OK.
7. Sluit de pagina.

