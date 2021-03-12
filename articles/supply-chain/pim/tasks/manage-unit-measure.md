---
title: Maateenheid beheren
description: Deze procedure laat zien hoe u een maateenheid kunt definiëren, vertalingen voor de eenheid en de beschrijving ervan kunt verstrekken en conversieregels voor gerelateerde eenheden kunt definiëren.
author: sorenva
manager: tfehr
ms.date: 07/08/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, UnitOfMeasure, UnitOfMeasureReportingTranslation, UnitOfMeasureTranslation, UnitOfMeasureConversion, UnitOfMeasureConversionEditOrCreate, UnitOfMeasureLookup, UnitOfMeasureCalculator, UnitOfMeasureWizard, UnitOfMeasureLookupTest
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71b478ca294719c20af9de16c27139aeca36bf07
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992290"
---
# <a name="manage-unit-of-measure"></a>Maateenheid beheren

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u een maateenheid kunt definiëren, vertalingen voor de eenheid en de beschrijving ervan kunt verstrekken en conversieregels voor gerelateerde eenheden kunt definiëren. U kunt deze procedure doorlopen met demogegevens of uw eigen gegevens.

1. Ga naar **Navigatievenster > Modules > Productgegevensbeheer > Producten > Vrijgegeven productonderhoud**.
2. Klik op **Eenheden**.

## <a name="create-a-unit-of-measure"></a>Een maateenheid maken
1. Klik op **Nieuw**.
2. Typ een waarde in het veld **Eenheid**. Voer de id of het symbool in dat moet worden gebruikt om te verwijzen naar de maateenheid.  
3. Typ een waarde in het veld **Beschrijving**. Voer een beschrijvende naam in voor de maateenheid in de systeemtaal.  
4. Selecteer een optie in het veld **Eenheidsklasse**. De eenheidsklasse definieert van welke logische groepering, zoals oppervlakte, massa of hoeveelheid, de maateenheid deel uitmaakt.  
5. Voer een getal in het veld **Decimale precisie** in. Geef het aantal decimalen op waarop de omgerekende maateenheid wordt afgerond bij voltooiing van een berekening met de maateenheid.  
6. Klik op **Opslaan**.

## <a name="define-unit-translations"></a>Eenheidsvertalingen definiëren
1. Ga naar het **actievenster** en klik op **Eenheidsteksten**.
2. Klik op **Nieuw**. Gebruik eenheidstekst om een vertaling van de id of een symbool te maken waarmee de maateenheid wordt aangeduid voor gebruik op externe documenten in klant- of leverancierspecifieke talen.  
3. Typ of selecteer een waarde in het veld **Taal**.
4. Typ een waarde in het veld **Tekst**.
5. Klik op **Opslaan**.
6. Sluit de pagina.
7. Ga naar het **actievenster** en klik op **Vertaalde eenheidsbeschrijvingen**.
8. Klik op **Nieuw**. Definieer taalspecifieke beschrijvingen voor de maateenheid.  
9. Typ of selecteer een waarde in het veld **Taal**.
10. Typ een waarde in het veld **Beschrijving**.
11. Klik op **Opslaan**.
12. Sluit de pagina.

## <a name="define-unit-conversion-rules"></a>Regels voor eenheidsconversie definiëren
1. Ga naar het **actievenster** en klik op **Eenheidsconversies**. Definieer regels om de maateenheid te converteren van en naar andere maateenheden in de geselecteerde eenheidsklasse.  
2. Klik op **Nieuw** om het uitklapdialoogvenster te openen.
3. Voer een getal in het veld **Factor** in. Conversiefactor tussen Van eenheid en Naar eenheid. De omrekeningsfactor van centimeter naar meter is 100, aangezien er 100 centimeters in 1 meter gaan.  
4. Typ of selecteer een waarde in het veld **Naar eenheid**.
5. Selecteer een optie in het veld **Afronding**. Definieer hoe de geconverteerde waarde moet worden afgerond.  
6. Klik op **OK**.
7. Sluit de pagina.

