---
title: Een standaardstatus voor de productlevenscyclus maken
description: Deze procedure laat zien hoe u een standaardstatus voor een productlevenscyclus maakt en hoe u de standaardstatus koppelt aan vrijgegeven producten.
author: t-benebo
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a628ed2b609f48c22076f409889c212e4d9463ac
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578195"
---
# <a name="create-a-default-product-lifecycle-state"></a>Een standaardstatus voor de productlevenscyclus maken

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een standaardstatus voor een productlevenscyclus maakt en hoe u de standaardstatus koppelt aan vrijgegeven producten.


## <a name="create-a-default-lifecycle-state"></a>Een standaardstatus voor de levenscyclus maken
1. Ga naar Productgegevensbeheer > Instellen > Levenscyclusstatus van product.
2. Klik op Nieuw.
3. Typ een waarde in het veld Status.
4. Selecteer Ja in het veld Standaard bij vrijgave aan rechtspersoon.
5. Typ een waarde in het veld Omschrijving.
6. Selecteer Nee in het veld Is actief voor planning.

> [!NOTE]
> Selecteer Nee, als u een nieuw vrijgegeven product niet wilt opnemen in de Hoofdplanning. Als het wel moet worden opgenomen in de Hoofdplanning, laat u de standaardwaarde Ja staan.  

## <a name="create-a-new-released-product"></a>Een nieuw vrijgegeven product maken
1. Sluit de pagina.
2. Ga naar Productgegevensbeheer > Producten > Vrijgegeven producten.
3. Klik op Nieuw.
4. Typ een waarde in het veld Productnummer.
5. Typ een waarde in het veld Productnaam.
6. Typ een waarde in het veld Zoeknaam.
7. Typ of selecteer een waarde in het veld Artikelmodelgroep.
8. Typ of selecteer een waarde in het veld Artikelgroep.
9. Typ of selecteer een waarde in het veld Opslagdimensiegroep.
10. Typ of selecteer een waarde in het veld Traceringsdimensiegroep.
11. Klik op OK.

> [!NOTE]
> De standaardstatus voor de productlevenscyclus is een algemene definitie.  

## <a name="change-the-product-to-an-active-state"></a>Het product wijzigen in een actieve status
1. Typ of selecteer een waarde in het veld Levenscyclusstatus van product.

> [!NOTE]
> Stel dat u een actieve status hebt ingesteld, dan kunt u nu de actieve status selecteren om toe te staan dat het product wordt gebruikt in de Hoofdplanning en in de berekening op stuklijstniveau. Uiteraard is dit alleen zinvol als de productgegevens zijn opgegeven die vereist zijn voor een consistente planning.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]