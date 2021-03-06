---
title: Kostenelementen maken
description: Er zijn verschillende manieren om kostenelementen in Kostprijsboekhouding te maken.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0c4c1e2aee7ba98c1cca378286afb643eaca1600
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810073"
---
# <a name="create-cost-elements"></a>Kostenelementen maken 

[!include [banner](../../includes/banner.md)]

Er zijn verschillende manieren om kostenelementen in Kostprijsboekhouding te maken. Deze procedure laat zien hoe u kostenelementen maakt door hoofdrekeningen te importeren via een gegevensconnector. Het demobedrijf USMF wordt gebruikt om deze procedure te maken. Deze procedure is voor een functie van Kostprijsboekhouding die in Dynamics 365 for Operations, versie 1611 is toegevoegd.


## <a name="create-new-cost-elements"></a>Nieuwe kostenelementen maken
1. Ga naar Kostprijsboekhouding > Dimensies > Dimensies van kostenelement.
2. Klik op Nieuw.
3. Typ een waarde in het veld Naam.
4. Typ of selecteer een waarde in het veld Gegevensconnector voor dimensieleden.
5. Typ een waarde in het veld Omschrijving.
6. Klik op Opslaan.

## <a name="configure-the-data-connector"></a>De gegevensconnector configureren
1. Klik op Dimensielidprovider configureren.
2. Typ of selecteer een waarde in het veld Rekeningschema.
    * Selecteer Gedeeld om het gedeelde rekeningschema te gebruiken.  
3. Klik op Nieuw.
4. Markeer in de lijst de geselecteerde rij.
    * U kunt filters op rekeningen toepassen om aan de criteria te voldoen.  
5. Typ of selecteer een waarde in het veld Van hoofdrekening.
6. Typ of selecteer een waarde in het veld Naar hoofdrekening.
7. Klik op OK.

## <a name="import-main-accounts"></a>Hoofdrekeningen importeren
1. Klik op Dimensieleden importeren.
    * Hoofdrekeningen worden in Kostprijsboekhouding geïmporteerd en gebruikt als kostenelementen.  
2. Klik op OK.

## <a name="view-the-imported-accounts-as-cost-elements"></a>De geïmporteerde rekeningen als kostenelementen weergeven
1. Klik op Dimensieleden weergeven.
    * Geef in uw bedrijf de geïmporteerde grootboekrekeningen als kostenelementen weer om de kosten daarnaartoe te laten stromen.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]