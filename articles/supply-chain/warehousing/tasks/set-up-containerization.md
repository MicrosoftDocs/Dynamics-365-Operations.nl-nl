---
title: Containervorming instellen
description: In dit onderwerp wordt beschreven hoe u de containervorming van ladingen in Magazijnbeheer kunt automatiseren.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b5ad1bdd91a2fb9109f29400f082e9a8af009ba
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216937"
---
# <a name="set-up-containerization"></a>Containervorming instellen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u de containervorming van ladingen in Magazijnbeheer kunt automatiseren. Met geautomatiseerde containervorming worden containers en orderverzamelingen voor zendingen gemaakt wanneer een wave wordt verwerkt en werkregels kunnen worden opgesplitst in hoeveelheden die in de containers passen. Dit helpt werknemers de artikelen direct in de gekozen container te verzamelen. Vergeleken met het handmatige verpakkingsproces worden taken zoals het maken van containers, het toewijzen van artikelen en het sluiten van containers geautomatiseerd door het systeem. In deze procedure wordt het demobedrijf USMF gebruikt en deze procedure wordt door een magazijnmanager uitgevoerd.


## <a name="set-up-a-wave-template"></a>Een wavesjabloon instellen
1. Ga in het navigatievenster naar **Modules > Magazijnbeheer > Instellen > Waves >Wave-sjablonen**.
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Wavesjabloon**.
4. Typ een waarde in het veld **Beschrijving van wavesjabloon**.
5. Typ of selecteer een waarde in het veld **Locatie**.
6. Typ of selecteer een waarde In het veld **Magazijn**.
7. Vouw de sectie **Methoden** uit. In het deelvenster **Geselecteerde methoden** worden de methoden voor het geselecteerde type wavesjabloon weergegeven. De wavesjabloon moet de methode Containervormen bevatten.  
8. Typ een waarde in het veld **Wavestapcode**. Voer een wavestapcode voor de toegevoegde methode in. Dit kan elke code zijn. Het is mogelijk om de methode meerdere malen toe te voegen en verschillende wavestapcodes toe te wijzen. Selecteer hiervoor **Herhaalbaar voor deze methode** op de pagina **Methoden voor verwerking van waves**.  
9. Selecteer **Opslaan**.
10. Sluit de pagina.

## <a name="set-up-a-container-type"></a>Een containertype instellen
1. Ga in het navigatievenster naar **Modules > Magazijnbeheer > Instellen > Containers > Containertypen**. U kunt uw containers definiëren op de pagina **Containertypen**. U kunt de fysieke afmetingen van containers configureren, waaronder tarragewicht, maximumgewicht, maximumvolume, lengte, breedte en hoogte. In dit voorbeeld zijn er drie verschillende formaten van dozen.  
2. Selecteer **Nieuw**.
3. Typ een waarde in het veld **Containertype**.
4. Typ een getal in het veld **Tarragewicht**.
5. Typ een getal in het veld **Maximumgewicht**.
6. Typ een getal in het veld **Volume**.
7. Typ een getal in het veld **Lengte**.
8. Typ een getal in het veld **Breedte**.
9. Typ een getal in het veld **Hoogte**.
10. Typ een waarde in het veld **Beschrijving**.
11. Selecteer **Opslaan**.
13. Herhaal stap 2-11 nog twee keer om drie totaal containertypen te maken.
14. Sluit de pagina.

## <a name="set-up-a-container-group"></a>Een containergroep instellen
1. Ga in het navigatievenster naar **Modules > Magazijnbeheer > Instellen > Containers > Containergroepen**.
2. Selecteer **Nieuw** in het actievenster. U kunt logische groepen containertypen instellen. Voor elke groep kunt u de volgorde opgeven waarin de containers moeten worden verpakt, en het percentage te vullen containers. Voor grootte worden de groottedimensies van het artikel gebruikt om te bepalen of het in een container past. De container die het nauwst aansluit bij de groottedimensies van het artikel, wordt gebruikt. Als u meerdere containertypen in een groep hebt, is het raadzaam deze op grootte te rangschikken zodat de grootste container eerste is, nummer 1 is in de volgorde, en de kleinste container laatste is.    
3. Typ in het veld **Containergroep-id** een waarde die u eerder hebt gemaakt.
4. Typ een waarde in het veld **Beschrijving**.
5. Herhaal stap 2-4 voor de drie containertypen die u eerder hebt gemaakt.
6. Selecteer **Opslaan**.
7. Sluit de pagina.

## <a name="set-up-a-container-build-template"></a>Een containervormingsjabloon instellen
1. Ga in het navigatievenster naar **Modules > Magazijnbeheer > Instellen > Containers > Containervormingssjablonen**.
2. Selecteer **Nieuw**. Welke containervormingssjabloon wordt gebruikt, wordt gebaseerd op welke containervormingsprocessen worden uitgevoerd. Met elke containervormingssjabloon wordt één containervormingsproces gedefinieerd dat door een wavesjabloon wordt gebruikt. Met de optie **Query bewerken** kunt u de voorwaarden definiëren waaronder de geselecteerde sjabloon wordt verwerkt. U kunt bijvoorbeeld containervorming alleen voor specifieke klanten, producten of magazijnen uitvoeren of u kunt de bijbehorende querybereiken aan de sjabloon toevoegen. Met het veld **Wavestapcode** wordt bepaald hoe een containervormingssjabloon wordt gekoppeld aan stappen in een wavesjabloon. Wanneer een wave wordt uitgevoerd, wordt bepaald welke containervormingssjabloon wordt gebruikt om containervorming uit te voeren. Met het veld Basisquerytypen wordt bepaald wat moet worden verpakt en waarop de filterquery moet worden gebaseerd. 
3. Typ een waarde in het veld **Id containersjabloon**.
4. Typ of selecteer een waarde in het veld **Containergroep-id**.
5. Typ een waarde in het veld **Wavestapcode**.
6. Schakel het selectievakje **Gesplitst verzamelen toestaan** in.
7. Selecteer **Opslaan**.
8. Selecteer **Beperkingen op mengen containers**. Met Logica-onderbrekingen mengen kunt u regels instellen voor het verpakken van toewijzingsregels in containers. Als u bijvoorbeeld het veld **Artikelnummer** toevoegt, wordt bij het toewijzen van artikelen aan containers een nieuwe container gemaakt wanneer er een nieuw artikelnummer is. Hiermee wordt voorkomen dat werknemers toewijzingsrgels voor twee verschillende klanten in dezelfde container verpakken.  
9. Selecteer **Nieuw**.
10. Selecteer een optie in het veld **Tabel**.
11. Typ of selecteer een waarde in het veld **Veld selecteren**.
12. Selecteer **OK**.

