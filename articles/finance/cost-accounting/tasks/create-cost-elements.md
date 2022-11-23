---
title: Kostenelementen maken
description: Er zijn verschillende manieren om kostenelementen in Kostprijsboekhouding te maken.
author: kfend
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
ms.openlocfilehash: 0254f486816e852bcda52f90fe4da65c413c7032
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779684"
---
# <a name="create-cost-elements"></a>Kostenelementen maken 

[!include [banner](../../includes/banner.md)]

Er zijn verschillende manieren om kostenelementen in Kostprijsboekhouding te maken. Deze procedure laat zien hoe u kostenelementen maakt door hoofdrekeningen te importeren via een gegevensconnector. Het demobedrijf USMF wordt gebruikt om deze procedure te maken. Deze procedure is voor een functie van Kostprijsboekhouding die in Dynamics 365 for Operations, versie 1611 is toegevoegd.


## <a name="create-new-cost-elements"></a>Nieuwe kostenelementen maken
1. Ga naar **Kostprijsboekhouding > Dimensies > Dimensies van kostenelement**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Naam**.
4. Typ of selecteer een waarde in het veld **Gegevensconnector voor dimensieleden**.
5. Typ een waarde in het veld **Beschrijving**.
6. Klik op **Opslaan**.

## <a name="configure-the-data-connector"></a>De gegevensconnector configureren
1. Klik op **Dimensielidprovider configureren**.
2. Typ of selecteer een waarde in het veld **Rekeningschema**.
    * Selecteer **Gedeeld** om het gedeelde rekeningschema te gebruiken.  
3. Klik op **Nieuw**.
4. Markeer in de lijst de geselecteerde rij.
    * U kunt filters op rekeningen toepassen om aan de criteria te voldoen.  
5. Typ of selecteer een waarde in het veld **Van hoofdrekening**.
6. Typ of selecteer een waarde in het veld **Naar hoofdrekening**.
7. Klik op **OK**.

## <a name="import-main-accounts"></a>Hoofdrekeningen importeren
1. Klik op **Dimensieleden importeren**.
    * Hoofdrekeningen worden in Kostprijsboekhouding geïmporteerd en gebruikt als kostenelementen.  
2. Klik op **OK**.

## <a name="view-the-imported-accounts-as-cost-elements"></a>De geïmporteerde rekeningen als kostenelementen weergeven
1. Klik op **Dimensieleden weergeven**.
    * Geef in uw bedrijf de geïmporteerde grootboekrekeningen als kostenelementen weer om de kosten daarnaartoe te laten stromen.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
