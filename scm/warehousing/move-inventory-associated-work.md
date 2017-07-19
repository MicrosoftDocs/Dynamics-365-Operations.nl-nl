---
title: Mutatie van voorraad met gekoppeld werk in Magazijnbeheer
description: In dit onderwerp wordt beschreven hoe u bevestiging voor stuksverzameling instelt en toepast vanaf een mobiel apparaat.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: d2db0431a3f749cbdaf35cc5108851f1e116bc96
ms.contentlocale: nl-nl
ms.lasthandoff: 06/20/2017

---

# <a name="movement-of-inventory-with-associated-work-in-warehouse-management"></a>Mutatie van voorraad met gekoppeld werk in Magazijnbeheer

[!include[banner](../includes/banner.md)]

Als u mutatie van voorraad gebruikt, kunt u bepalen welke magazijnmedewerkers gereserveerde voorraad mogen verplaatsen. Dit biedt de flexibiliteit om in gereguleerde magazijnen niet toe te staan dat een werknemer een nieuwe orderverzamellocatie kiest voor verzamelwerk dat al is gemaakt. Zo kan een magazijnbeheerder bepalen welke mogelijkheden beschikbaar zijn voor sommige minder ervaren werknemers.

De flexibiliteit in het beheer van de dagelijkse handelingen van magazijnmedewerkers kan van pas komen in scenario's zoals deze:

## <a name="scenario-1"></a>Scenario 1
Een bedrijf heeft een relatief klein ontvangstgebied en dit staat vol met pallets en dozen die nog moet worden weggezet. Vandaag wordt een grote verzending verwacht en de de ontvangstadministrateur besluit het ontvangstgebied leeg te maken door enkele pallets te verplaatsen naar een secundair inkomend faseringsgebied.

## <a name="scenario-2"></a>Scenario 2
Een ervaren magazijnmedewerker ziet een mogelijkheid om in een magazijn artikelen samen te brengen op één locatie, in plaats van ze verdeeld te laten over drie locaties dicht bij elkaar die elk slechts een kleine hoeveelheid bevatten. De werknemer wil de hoeveelheid consolideren door artikelen vanaf elk van deze locaties te verplaatsen naar één en dezelfde locatie en naar dezelfde nummerplaat.

## <a name="scenario-3"></a>Scenario 3
Een pallet wacht op verzending op een faseringslocatie zoals STAGE01, die zich vlakbij BAYDOOR01 bevindt. Vanwege een wijziging in de plannen is de vrachtwagen echter gepland voor aankomst op BAYDOOR04. De expeditiemedewerker is op de hoogte en moet ervoor zorgen dat de vrachtwagen niet hoeft te wachten op het laden vanuit STAGE01. De expeditiemedewerker besluit de artikelen in deze levering te verplaatsen van STAGE01 naar STAGE04, dat zich dichter bij de nieuwe bestemming bevindt.

### <a name="current-limitations"></a>Huidige beperkingen

De werkreserveringen die u kunt verplaatsen, zijn beperkt tot Verkooporders, Uitgifte van een transferorder Ontvangst van transferorder, Inkooporder en Aanvullingswerk.

Artikelen verplaatsen is beperkt om te voorkomen dat werkregels worden opgesplitst. Dit betekent dat als u een werkregel hebt voor 100 stuks van artikel A van locatie Loc1, u niet slechts 30 stuks van artikel A van daaruit naar een andere locatie kunt verplaatsen. Dit zou leiden tot een splitsing van de bestaande werkregel in 30 en 70, omdat er nu twee verschillende locaties zijn.

Bij faseringscenario's waarin de nummerplaat van waaruit u de goederen verplaatst of waarnaar u de goederen verplaatst is ingesteld als doelnummerplaat voor een werkorder, is alleen de verplaatsing van de gehele nummerplaat toegestaan. Anders zou de doelnummerplaat in verschillende stukken worden opgebroken.
Alleen de ad-hocverplaatsing wordt momenteel ondersteund. Dit betekent dat u gereserveerde voorraad niet kunt verplaatsen via de beweging door sjabloonmenu-items voor mobiele apparaten.

### <a name="set-up-the-permission-to-move-reserved-inventory-for-individual-workers"></a>Machtigingen voor het verplaatsen van gereserveerde voorraad instellen voor afzonderlijke werknemers

Voor de werknemers die gereserveerde voorraad mogen verplaatsen, schakelt u het selectievakje **Mutatie van voorraad met gekoppeld werk toestaan** in onder **Magazijnbeheer** > **Instellingen** > **Medewerker**.  

### <a name="backported"></a>Backport

Deze functie is ook beschikbaar gemaakt voor de oudere versies Microsoft Dynamics AX 2012 R3. U vindt hem in CU12.
U kunt hem ook afzonderlijk downloaden via KB-nummer 3192548. 


