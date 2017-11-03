---
title: Ploegen- en kasladebeheer
description: "In dit artikel wordt beschreven hoe u de twee typen ploegen voor detailhandelverkooppunten (POS) kunt instellen en gebruiken: gedeelde en zelfstandige. Gedeelde ploegen kunnen worden gebruikt door meerdere gebruikers op meerdere plaatsen terwijl zelfstandige ploegen kunnen worden gebruikt door slechts één werknemer tegelijk."
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 105011
ms.assetid: 49a0fcc9-d4db-45ad-8c4b-213ccaced82b
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 72f73404f99330c3ff8b23dabed78477a0cd30cd
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="shift-and-cash-drawer-management"></a>Ploegen- en kasladebeheer

[!include[banner](includes/banner.md)]


In dit artikel wordt beschreven hoe u de twee typen ploegen voor detailhandelverkooppunten (POS) kunt instellen en gebruiken: gedeelde en zelfstandige. Gedeelde ploegen kunnen worden gebruikt door meerdere gebruikers op meerdere plaatsen terwijl zelfstandige ploegen kunnen worden gebruikt door slechts één werknemer tegelijk.

Er zijn twee typen ploegen voor detailhandelverkooppunten: zelfstandige en gedeelde. Zelfstandige ploegen kunnen door slechts één werknemer tegelijk worden gebruikt. Gedeelde ploegen kunnen worden gebruikt door meerdere gebruikers op meerdere plaatsen. Hierdoor creëren zij in feite één ploeg voor meerdere werknemers in een winkel.

## <a name="standalone-shifts"></a>Zelfstandige ploegen
Zelfstandige ploegen worden gebruikt in een traditioneel scenario met vaste POS, waarin geld voor elk POS-kassa afzonderlijk wordt afgestemd. In een supermarkt, bijvoorbeeld, zijn er meestal verschillende vaste POS-kassa's en wordt een kassamedewerker toegewezen aan elke kassa. In dit geval maakt elke kassa waarschijnlijk gebruik van een zelfstandige ploeg en is de kassamedewerker verantwoordelijk voor de kassa of de fysieke contanten in die kassa. Een zelfstandige ploeg omvat alle activiteiten op die kassa tijdens de ploegendienst van de kassamedewerker. Activiteiten kunnen het openingsbedrag dat wordt gestort in de kassa omvatten, alle verwijderingen en toevoegingen van contanten via bewerkingen als bankstortingen en wisselgeldinvoer, en de kascontrole aan het einde van de werktijd.

### <a name="set-up-a-stand-alone-shift"></a>Een zelfstandige ploeg instellen

Een zelfstandige ploeg wordt aangewezen op het niveau van de kassalade. In deze procedure wordt uitgelegd hoe u een zelfstandige ploeg kunt instellen op een POS-kassa.

1.  Klik op **Retail** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen** &gt; **Hardwareprofielen**.
2.  Selecteer het hardwareprofiel dat moet worden gebruikt voor de zelfstandige ploeg.
3.  Bevestig op het sneltabblad **Lade** dat de optie **Gedeelde ploeglade** is ingesteld op **Nee**.
4.  Klik op **Opslaan**.
5.  Klik op **Retail** &gt; **Kanaalinstelling** &gt; **POS-instellingen** &gt; **Kassa's**.
6.  Selecteer de kassa waarvoor een zelfstandige ploeg is vereist en klik vervolgens op **Bewerken**.
7.  Selecteer in het veld **Hardwareprofiel** het hardwareprofiel dat u in stap 2 hebt geselecteerd.
8.  Klik op **Opslaan**.
9.  Klik op **Retail** &gt; **IT detailhandel** &gt; **Distributieplanning**.
10. Selecteer de distributieplanning **1090** en klik vervolgens op **Nu uitvoeren** om wijzigingen in het POS te synchroniseren.

### <a name="use-a-stand-alone-shift"></a>Een zelfstandige ploeg gebruiken

1.  Meld u aan bij het POS.
2.  Als er geen ploeg geopend is, selecteert u **Een nieuwe ploeg openen**.
3.  Ga naar de bewerking **Beginbedrag declareren** en geef de hoeveelheid contanten op die aan de kassa wordt toegevoegd aan het begin van de werkdag.
4.  Voer een aantal transacties uit.
5.  Selecteer aan het einde van de dag **Kas controleren** om de hoeveelheid contant geld dat in de kassalade blijft aan te geven.
6.  Voer de hoeveelheid contant geld in en klik vervolgens op **Opslaan** om de kascontrole op te slaan.
7.  Selecteer **Ploeg sluiten** om de ploeg te sluiten.

**Opmerking:** andere activiteiten zijn beschikbaar tijdens de ploeg, afhankelijk van de bedrijfsprocessen die aanwezig zijn. De bewerkingen **Kluisstorting**, **Bankstorting** en **Kascontrole** kunnen worden gebruikt voor het verwijderen van geld uit de kassa gedurende de dag of voordat de ploeg wordt gesloten. Als nog maar weinig geld in een kassa zit, kan de bewerking **Wisselgeldinvoer** worden gebruikt om geld toe te voegen aan de kassa.

## <a name="shared-shifts"></a>Gedeelde ploegen
Een gedeelde ploeg wordt gebruikt in een omgeving waarin meerdere kassamedewerkers een kassalade of een reeks kassalades delen gedurende de werkdag. Een gedeelde ploeg wordt meestal gebruikt in mobiele POS-omgevingen. In een mobiele omgeving is elke kassamedewerker niet toegewezen aan en verantwoordelijk is voor een enkele kassalade. In plaats daarvan moeten alle kassamedewerkers een verkoop kunnen afhandelen en geld kunnen toevoegen aan de kassalade die zich het dichtst bij hen bevindt. In dit scenario worden de kassalades die worden gedeeld door kassamedewerkers opgenomen in een gedeelde ploeg. Alle kassalades in een gedeelde ploeg zijn opgenomen in de dezelfde ploeg ten behoeve van de activiteiten die betrekking hebben op kasbeheer voor die ploeg. Daarom moet het beginbedrag van de ploeg het totaal van alle geld in alle kassalades omvatten die zijn opgenomen in de gedeelde ploeg. Op vergelijkbare wijze is de kascontrole het totaal van alle geld in alle kassalades die zijn opgenomen in de gedeelde ploeg. **Opmerking:** In elke winkel kan telkens slechts één gedeelde shift tegelijk zijn geopend. Gedeelde ploegen en zelfstandige ploegen kunnen worden gebruikt in dezelfde winkel.

### <a name="set-up-a-shared-shift"></a>Een gedeelde ploeg instellen

1.  Klik op **Retail** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen** &gt; **Hardwareprofielen**.
2.  Selecteer het hardwareprofiel dat moet worden gebruikt voor de gedeelde ploeg.
3.  Stel op het sneltabblad **Lade** de optie **Gedeelde ploeglade** in op **Ja**.
4.  Klik op **Opslaan**.
5.  Klik op **Retail** &gt; **Kanaalinstelling** &gt; **POS-instellingen** &gt; **Kassa's**.
6.  Selecteer de kassa waarvoor een gedeelde ploeg is vereist en klik vervolgens op **Bewerken**.
7.  Selecteer in het veld **Hardwareprofiel** het hardwareprofiel dat u in stap 2 hebt geselecteerd.
8.  Klik op **Opslaan**.
9.  Klik op **Retail** &gt; **IT detailhandel** &gt; **Distributieplanning**.
10. Selecteer de distributieplanning **1090** en klik vervolgens op **Nu uitvoeren** om wijzigingen in het POS te synchroniseren.

### <a name="use-a-shared-shift"></a>Een gedeelde ploeg gebruiken

1.  Meld u aan bij het POS.
2.  Als de POS nog niet met een hardwarestation is verbonden, selecteert u **Niet-ladebewerking** en selecteert u vervolgens de bewerking **Hardwarestation selecteren** om een hardwarestation actief te maken voor de gedeelde ploeg. Deze stap is alleen vereist de eerste keer dat een kassa wordt toegevoegd aan een gedeelde ploegomgeving.
3.  Meld u af bij het POS en vervolgens opnieuw aan.
4.  Selecteer **Een nieuwe ploeg maken**.
5.  Selecteer **Beginbedrag declareren**.
6.  Voer het beginbedrag van alle kassalades in de winkel in die deel uitmaken van de gedeelde ploeg en klik vervolgens op **Opslaan**.
    -   Als u een deel van het beginbedrag wilt toevoegen aan elke opeenvolgende kassalade, gebruikt u de bewerking **Hardwarestation selecteren** om het hardwarestation actief te maken.
    -   U kunt een kassa toevoegen aan een specifieke kassalade door de bewerking **Lade openen** te gebruiken.
    -   Ga door totdat alle kassalades in de gedeelde ploeg hun deel van het beginbedrag bevatten.

7.  Aan het einde van de dag, opent u elke kassalade en verwijdert u het contante geld.
8.  Nadat u het contante geld hebt verwijderd uit de laatste kassalade, telt u alle geld uit alle kassalades.
9.  Gebruik de bewerking **Kas controleren** om het totale bedrag aan contant geld van alle kassalades die zijn opgenomen in de gedeelde ploeg aan te geven.
10. Gebruik de bewerking **Ploeg sluiten** om de gedeelde ploeg te sluiten.





