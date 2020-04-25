---
title: Voorraad in een magazijn tellen
description: In dit onderwerp wordt beschreven hoe u een voorraadtellingsjournaal maakt en boekt om een specifiek artikel op een locatie in het magazijn te tellen.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34013783bab79d80f1dac9a7806042608635e617
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204166"
---
# <a name="count-inventory-in-a-warehouse"></a>Voorraad in een magazijn tellen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een voorraadtellingsjournaal maakt en boekt om een specifiek artikel op een locatie in het magazijn te tellen. De procedure is van toepassing op de functie "basale magazijnen" die beschikbaar is in de module Voorraadbeheer, niet op de magazijnfunctionaliteit die beschikbaar is in de module magazijnbeheer. U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken. Als u uw eigen gegevens gebruikt, moet u ervoor zorgen dat u producten en locaties hebt ingesteld en dat u een voorraadjournaalnaam voor tellingsjournalen hebt gemaakt. Voorraadtelling wordt normaal uitgevoerd door een magazijnwerknemer.


## <a name="create-an-inventory-counting-journal"></a>Een voorraadtellingsjournaal maken
1. Ga naar **Navigatievenster > Modules > Voorraadbeheer > Journaalboekingen > Artikeltelling > Tellen**.
2. Selecteer **Nieuw**.
3. Selecteer in de vervolgkeuzelijst in het veld **Naam** de naam van het voorraadtellingsjournaal dat u wilt gebruiken. Enkele andere velden worden ingevuld op basis van de instellingen van de naam voor het standaardjournaal voor voorraadtelling die u selecteert.  
4. Selecteer in het veld **Medewerker** de vervolgkeuzeknop om de zoekopdracht te openen.
5. **Selecteer** in de lijst de medewerker die u wilt gebruiken.
6. Selecteer **OK**.

## <a name="create-journal-lines"></a>Journaalregels maken
1. Selecteer **Nieuw**.
2. Selecteer in het veld **Artikelnummer** de gewenste record in de vervolgkeuzelijst. Als u het demobedrijf USMF gebruikt, selecteert u **A0001**.  
3. Selecteer in het veld **Vestiging** de gewenste record in de vervolgkeuzelijst. Als u het demobedrijf USMF gebruikt, selecteert u site **2**.
4. Selecteer in het veld **Magazijn** de gewenste record in de vervolgkeuzelijst. Als u het demobedrijf USMF gebruikt, selecteert u magazijn **24**.  
5. Selecteer in het veld **Locatie** de gewenste record in de vervolgkeuzelijst. Als u het demobedrijf USMF gebruikt, selecteert u locatie **BULK-001**.  
6. Voer in het veld Geteld een getal in. Als u een geteld aantal invoert dat verschilt van de waarde die in het veld **Voorhanden** wordt weergegeven, wordt het veld **Hoeveelheid** bijgewerkt om het verschil aan te geven.  
7. Selecteer **Opslaan**.

## <a name="post-the-inventory-counting-journal"></a>Het voorraadtellingsjournaal boeken
1. Selecteer **Boeken**. Als u een voorraadtellingsjournaal boekt en het getelde bedrag afwijkt van het aantal dat in het veld **Voorhanden** wordt vermeld, wordt er een voorraadontvangst of -uitgifte geboekt, worden het niveau en de waarde van de voorraad gewijzigd en worden grootboektransacties gegenereerd.
2. Selecteer **OK**.

## <a name="view-inventory-transactions"></a>Voorraadtransacties weergeven
1. Selecteer **Voorraadmodel**.
2. Selecteer **Transacties**. Hier kunt u de verwante transacties bekijken die worden gemaakt wanneer u uw voorraadtellingsjournaal boekt.   

