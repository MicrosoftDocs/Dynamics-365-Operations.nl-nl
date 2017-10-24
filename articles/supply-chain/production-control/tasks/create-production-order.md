--- 
title: Een productieorder maken
description: Deze procedure laat zien hoe u een productieorder maakt.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 730adcea0ac59f683ecae8cbb62025bd7db75c55
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-production-order"></a>Een productieorder maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat zien hoe u een productieorder maakt. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Dit is de eerste procedure van zeven die de productieorderlevenscyclus beschrijven.


## <a name="create-a-production-order"></a>Een productieorder maken
1. Ga naar Productiebeheer > Productieorders > Alle productieorders.
2. Klik op Nieuwe productieorder.
3. Typ in het veld Artikelnummer de waarde 'D0001'.
4. Geef een datum op in het veld Levering.
    * De leveringsdatum geeft aan wanneer de productieorder moet eindigen om op tijd te leveren. Deze datum kan in het planningsproces worden gebruikt. Bijvoorbeeld: u kunt de order terug in de tijd plannen vanaf de leveringsdatum.  
5. Stel Hoeveelheid in op '20'.
    * Opmerking: Het veld voor het stuklijstnummer bevat automatisch het nummer van een actieve stuklijst voor het huidige artikel, maar u kunt de stuklijst voor de productieorder wijzigen door een actieve stuklijst in de lijst met goedgekeurde stuklijstversies te selecteren.    Het veld voor het routenummer bevat automatisch het nummer van een actieve route voor het huidige artikel, maar u kunt de route voor de productieorder wijzigen door een actieve route in de lijst met goedgekeurde routeversies te selecteren.  
6. Klik op Maken.

## <a name="validate-the-production-order"></a>De productieorder valideren
1. Klik in de lijst op de koppeling in de geselecteerde rij.
    * Klik op de koppeling voor het productieordernummer dat u zojuist hebt gemaakt. Hiermee wordt de detailspagina voor de order geopend.  
2. Klik op Bewerken.
3. Geef een datum op in het veld Levering.
    * Bijvoorbeeld: u kunt de leveringsdatum voor de productieorder wijzigen.  
4. Klik op Opslaan.
5. Sluit de pagina.

## <a name="update-the-bom"></a>De stuklijst bijwerken
1. Klik in het actievenster op Productieorder.
2. Klik op Stuklijst.
    * Open de stuklijstpagina om de stuklijstgegevens te valideren die van de standaardgegevens zijn gekopieerd toen de productieorder werd gemaakt. In deze procedure moet u de hoeveelheid voor een stuklijst bijwerken.  
3. Klik op Bewerken.
4. Voer in het veld Hoeveelheid een getal in.
    * Het wijzigen van de hoeveelheid op de stuklijstregel is van invloed op de kostenraming van materiaalverbruik voor de productieorder.  
5. Klik op Opslaan.
6. Sluit de pagina.

## <a name="update-the-production-route"></a>De productieroute bijwerken
1. Klik in het actievenster op Productieorder.
2. Klik op Route.
    * Open de routepagina om de gegevens van de productieroute te valideren die van de standaardgegevens zijn gekopieerd toen de order werd gemaakt. In deze procedure moet u de hoeveelheid voor een van de bewerkingen in de productieroute bijwerken.  
3. Zoek en selecteer de gewenste record in de lijst.
4. Klik op Bewerken.
5. Voer in het veld Verwerkingshoeveelheid een getal in.
    * Het wijzigen van de verwerkingstijd is van invloed op het geraamde routeverbruik en de kosten van de productieorder.  
6. Klik op Opslaan.
7. Sluit de pagina.


