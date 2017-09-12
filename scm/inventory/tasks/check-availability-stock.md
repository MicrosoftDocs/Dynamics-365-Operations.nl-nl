---
title: De beschikbaarheid van voorraad controleren
description: Deze procedure laat zien hoe u voorhanden en fysieke voorraad voor een specifiek artikelnummer kunt controleren.
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: d103eb52a498e6273b1fdb43fc10dae4133e76b2
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# De beschikbaarheid van voorraad controleren

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u voorhanden en fysieke voorraad voor een specifiek artikelnummer kunt controleren. Het geeft ook weer hoe u aanbodinformatie voor een artikel krijgt. De fysieke voorhanden voorraad is de voorhanden voorraad die beschikbaar is, dat wil zeggen dat de voorraad is ingekocht, ontvangen en geregistreerd. De voorhanden voorraad bevat de beschikbare voorraad, maar ook de voorraad die is besteld en wordt verwacht, maar nog niet is ontvangen of geregistreerd. U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken. Als u USMF gebruikt, kunt u de voorbeeldwaarden gebruiken die worden weergegeven. Deze taken worden meestal uitgevoerd door een magazijnmedewerker.


## Voorhanden voorraad voor een artikel controleren
1. Ga naar Voorraadbeheer > Query's en rapporten > Voorhanden voorraad.
2. Selecteer de rij Artikelnummer.
    * Om de voorhanden voorraad op artikelnummer op te vragen, selecteert u de rij waar de tabel op Voorhanden voorraad is ingesteld en het veld op Artikelnummer is ingesteld.  
3. Selecteer in het veld Criteria het artikel waarvoor u een query wilt uitvoeren.
    * Als u het USMF-demobedrijf gebruikt, kunt u 'M9201' selecteren.  
4. Klik op OK.
5. Klik op Dimensies.
    * Met het dimensiestabblad selecteert u hoeveel details u wilt zien over de voorhanden voorraad. Als u gegevens met betrekking tot reserveringen nodig hebt, moet u alle voorraaddimensies voor de artikelen weergeven die geavanceerde magazijnbeheerprocessen gebruiken.  
6. Klik op OK.
7. Klik in het actievenster op Gerelateerde informatie.
    * Als dit niet wordt weergegeven, kunt u op de knop met weglatingstekens (...) klikken om extra actievensteropties te bekijken.  
8. Klik op Aanbodoverzicht.
    * Het tabblad Aanbodoverzicht biedt aanbodinformatie voor een bepaald artikel, zoals de voorhanden hoeveelheid, doorlooptijd, en leveranciersgegevens.  
9. Vouw de sectie Voorhanden uit.
10. Vouw de sectie Leveranciers uit.
11. Sluit de pagina.
12. Sluit de pagina.

## Fysieke voorhanden voorraad controleren
1. Ga naar Magazijnbeheer > Query's en rapporten > Fysieke voorhanden voorraad.
2. Typ een waarde in het veld Artikelnummer.
    * U kunt Locatie en Magazijn gebruiken om de lijst met artikelen te filteren.  
3. Vernieuw de pagina.
4. Klik op Dimensies weergeven.
    * Met het tabblad Dimensies weergeven selecteert u hoeveel details u wilt zien over de voorhanden voorraad.  
5. Klik op OK.
6. Sluit de pagina.

## De voorhanden voorraad per locatie controleren
1. Ga naar Magazijnbeheer > Query's en rapporten > Voorhanden voorraad per locatie.
2. Typ een waarde in het veld Magazijn.
    * Als u het USMF-bedrijf van de demogegevens gebruikt, kunt u 51 gebruiken.  
3. Vernieuw de pagina.
4. Klik op Dimensies weergeven.
5. Klik op OK.
6. Sluit de pagina.

