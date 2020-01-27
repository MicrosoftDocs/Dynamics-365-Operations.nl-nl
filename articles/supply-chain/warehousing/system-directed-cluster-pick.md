---
title: Door systeem gestuurde clusterverzameling
description: In dit onderwerp vindt u een overzicht van door het systeem gestuurde clusterverzameling in Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: c3b23a5d3b77bae89e4845bdff4ab20f95c46497
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917851"
---
# <a name="system-directed-cluster-picking"></a>Door systeem gestuurde clusterverzameling

[!include [banner](../includes/banner.md)]

Clusterverzameling is een proces voor stuksverzameling waarmee u artikelen voor meerdere orders tegelijk kunt kiezen door ze te clusteren in verzamelclusters. U hoeft de orderverzamellocatie in dat geval slechts één keer te bezoeken. Deze functionaliteit wordt meestal gebruikt bij het verzamelen van kleine orders of aantallen die kleiner zijn dan aanvraaghoeveelheden.

Wanneer door het systeem gestuurde clusterverzameling is ingesteld, u werkkopteksten in clusters verzamelen, op basis van een door het systeem gegenereerd cluster. Orders worden in clusters verzameld tot het aantal posities dat is opgegeven in het clusterprofiel. Daarom kunt u meerdere orders op hetzelfde moment verzamelen zonder handmatig een cluster te hoeven maken.

Door het systeem gestuurde clusterverzameling biedt een alternatief voor het handmatig maken van clusters, waarbij een clusterprofiel wordt gebruikt om een cluster te maken. Er moeten verschillende instellingsregels in het clusterprofiel worden gedefinieerd voordat dit profiel wordt gebruikt:

- **Aantal posities** komt overeen met het aantal orders dat in een cluster wordt geplaatst. Daarom komt het overeen met het aantal totes.
- **Cluster opsplitsen** bepaalt wanneer het cluster moet worden opgesplitst.
- **Cluster-id maken** bepaalt of de cluster-id wordt gegenereerd door het systeem of ingevoerd door de gebruiker.
- **Verificatietype sorteren** bepaalt of positieverificatie vereist is.

Een nieuw menu-item voor mobiele apparaten wordt gebruikt voor door het systeem gestuurde clusterverzameling. De clusterprofiel-id moet worden opgegeven voor de optie **Bestuurd door**. Bovendien kunnen met de door het systeem gestuurde queryvolgorde orders worden gegroepeerd op basis van bedrijfsspecifieke criteria. Daarom kunt u de toewijzing van werkorders verder optimaliseren door aangepaste sorteercriteria op te geven voor de door het systeem gestuurde queryvolgorde.

Wanneer de door het systeem gestuurde clusterverzameling is uitgevoerd, krijgen magazijnmedewerkers een cluster voorgeschoteld waarin orderverzamelorders vooraf zijn toegewezen aan clusterposities. Daarom kunnen medewerkers beginnen met het verzamelen van een artikel voor meerdere werkorders door slechts één keer naar de orderverzamellocatie te gaan. Het orderverzamelproces voor door het systeem gestuurde clusterverzameling is hetzelfde als het proces voor door de gebruiker gestuurde clusterverzameling.

## <a name="set-up-system-directed-cluster-picking"></a>Door systeem gestuurde clusterverzameling instellen

### <a name="create-cluster-profiles"></a>Clusterprofielen maken

Clusterprofielen bepalen hoe het systeem elk cluster maakt. Als verschillende clusters vereist zijn, moet voor elk menu-item van het mobiele apparaat een ander clusterprofiel worden gemaakt.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Clusterprofielen**.
2. Selecteer **Nieuw**.
3. Voer in het veld **Profiel-id van cluster** de tekst **2 positie** in.
4. Voer in het veld **Naam** de tekst **2 positie** in.
5. Stel op het sneltabblad **Algemeen** de volgende velden in:

    - **Cluster-id maken:** stel deze optie in op **Ja**. Met deze optie bepaalt u of de cluster-id automatisch wordt gemaakt door het systeem of dat de gebruiker deze maakt bij het begin van het orderverzamelen.
    - **Posities activeren**: stel deze optie in op **Ja**. Met deze optie bepaalt u of de positienamen automatisch worden gegenereerd op basis van de instellingen voor positienamen. Als deze optie is ingesteld op **Nee**, wordt de nummerplaat-id gebruikt voor de positie.
    - **Aantal posities:** voer **2** in. Dit veld bepaalt het maximum aantal posities dat het cluster kan hebben (het maximum aantal vakken, totes, enzovoort).
    - **Positienaam**: selecteer **Numeriek** zodat posities worden benoemd op basis van doorlopende nummers. Als u **Alfabetisch** selecteert, worden de posities in alfabetische volgorde benoemd.
    - **Cluster opsplitsen bij**: selecteer **Wegzetten**. Dit veld bepaalt wanneer het cluster wordt opgesplitst.
    - **Verificatietype sorteren**: selecteer **Positie scannen**. Met dit veld bepaalt u of de stap voor wegzetten naar positie wordt geverifieerd.

6. Op het sneltabblad **Clustersortering** kunt u sorteercriteria definiëren door een nieuwe regel te maken en de volgende velden in te stellen:

    - **Volgnummer**: dit veld bepaalt de volgorde waarin wordt gesorteerd. Er wordt automatisch een waarde ingevoerd, maar u kunt deze naar wens wijzigen.
    - **Veldnaam:** selecteer **WMSLocationId**. Met dit veld bepaalt u welk veld door de regel wordt gebruikt voor sorteercriteria.
    - **Sorteren:** selecteer **Oplopend**. Met dit veld bepaalt u of de sortering in oplopende of aflopende volgorde wordt uitgevoerd.

### <a name="create-a-mobile-device-menu-item"></a>Een menuopdracht van mobiel apparaat maken

Ga als volgt te werk als u een nieuw menu-item voor mobiele apparaten wilt maken voor door het systeem gestuurde clusterverzameling en de clusterprofiel-id aan het menu-item van het mobiele apparaat wilt koppelen.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
2. Selecteer **Nieuw**.
3. Voer **SD-cluster** in het veld **Naam van menuopdracht** in.
4. Voer **SD-cluster** in het veld **Titel** in.
5. Selecteer **Werk** in het veld **Modus**.
6. Stel de optie **Bestaand werk gebruiken** in op **Ja**.
7. Stel op het sneltabblad **Algemeen** de volgende velden in:

    - **Bestuurd door**: selecteer **Door systeem bestuurd**.
    - **Nummerplaat maken**: stel deze optie in op **Ja**.
    - **Clusterprofiel-id**: selecteer **2 positie**.

8. Stel op het sneltabblad **Werkklassen** de geldige werkklasse voor deze menuopdracht voor mobiel apparaten in door de volgende velden in te stellen:

    - **Werkklasse-id**: zorg dat **Verkoop** is ingevoerd.
    - **Werkordertype**: zorg dat **Verkooporders** is ingevoerd.

9. Volg deze stappen om een nieuwe door het systeem gestuurde werkreeksquery op te geven:

    1. Selecteer **Nieuw**.
    2. Voer in het veld **Volgnummer** de waarde **1** in.
    3. Selecteer **Werkprioriteit – Werk-id** in het veld **Beschrijving**.

10. Selecteer **Query bewerken** in het menu.
11. Stel de volgende velden in op het tabblad **Sorteren**:

    - **Tabel:** selecteer **Werk**.
    - **Afgeleide tabel**: selecteer **Werk**.
    - **Veld**: selecteer **Werkprioriteit**.
    - **Zoekrichting:** selecteer **Oplopend**.
    - **Tabel:** selecteer **Werk**.
    - **Afgeleide tabel**: selecteer **Werk**.
    - **Veld**: selecteer **Werk-id**.
    - **Zoekrichting:** selecteer **Oplopend**.

Het systeem sorteert werk-id's nu in het cluster, eerst op werkprioriteit en vervolgens op werk-id.

### <a name="set-up-a-mobile-device-menu"></a>Een menu van een mobiel apparaat instellen

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menu voor mobiel apparaat**.
2. Voeg de zojuist gemaakte menuoptie toe aan het gewenste menu.

## <a name="example"></a>Voorbeeld

### <a name="create-picking-work"></a>Orderverzamelingswerk maken

Voordat u door het systeem gestuurde clusterverzameling kunt instellen, moet u in aanmerking komend uitgaand werk maken. Met het clusterprofiel dat u eerder hebt gemaakt, worden twee clusterposities opgegeven. Daarom moet u ten minste twee werk-id's maken.

1. Ga naar **Verkoop en marketing \> Verkooporders \> Alle verkooporders**.
2. Selecteer **Nieuw** om een verkooporder te maken.
3. Selecteer een klant in het veld **Klantrekening**.
4. Selecteer op het sneltabblad **Algemeen** magazijn **62** in het veld **Magazijn**.
5. Selecteer **OK**.
6. Selecteer **Regel toevoegen** op het sneltabblad **Verkooporderregels**.
7. Selecteer in het veld **Artikelnummer** de optie **A0001**.
8. Typ **1** in het veld **Hoeveelheid**.
9. Selecteer **Regel toevoegen** om een tweede regel toe te voegen.
10. Selecteer in het veld **Artikelnummer** de optie **A0002**.
11. Typ **3** in het veld **Hoeveelheid**.
12. Herhaal stap 2 t/m 6.
13. Selecteer in het veld **Artikelnummer** de optie **A0001**.
14. Typ **4** in het veld **Hoeveelheid**.
15. Selecteer **Regel toevoegen** om een tweede regel toe te voegen.
16. Selecteer in het veld **Artikelnummer** de optie **A0002**.
17. Typ **2** in het veld **Hoeveelheid**.

Reserveer de voorraad en geef deze vrij aan het magazijn. Er worden twee verschillende werk-id's gemaakt. Elke werk-id heeft twee orderverzamelregels.

### <a name="run-the-mobile-device-flow"></a>De stroom voor mobiele apparaten uitvoeren

1. Selecteer op het mobiele apparaat het menu dat de nieuwe menuoptie voor mobiele apparaten bevat.
2. Selecteer de menuopdracht **SD-cluster** en start de orderverzameling. Er wordt een cluster gemaakt en de twee werk-id's die u eerder hebt gemaakt, worden hieraan gekoppeld. Als u meer dan twee werk-id's hebt gemaakt, worden alleen de eerste twee toegevoegd aan het cluster. U ziet dat de werk-id's in oplopende volgorde worden toegevoegd aan het cluster, zoals u hebt opgegeven in de query-instellingen.

    > [!NOTE]
    > Het nieuwe cluster wordt alleen automatisch gemaakt als er eerder voldoende extra werk-id's zijn gemaakt. Anders wordt het volgende bericht weergegeven: Er is niet genoeg werk gevonden voor het cluster.

    Nadat u het menu selecteert, wordt het eerste orderverzamelscherm weergegeven. Het systeem verzamelt alle overeenkomende orderverzamelregels van de twee werk-id's en instrueert u om één keer naar de orderverzamellocatie te gaan, zodat u aan beide orders voldoen met behulp van één orderverzameling. Dit proces wordt op dezelfde manier uitgevoerd als het proces voor door de gebruiker gestuurde clusterverzameling.

3. Bevestig de eerste orderverzameling. U moet vervolgens de positienaam invoeren om te bevestigen dat de artikelen op de juiste positie zijn geplaatst.
4. Herhaal dit proces totdat alle artikelen zijn verzameld en op de juiste positie zijn geplaatst.
5. De laatste stap die u op het mobiele apparaat uitvoert, is het cluster op de uiteindelijke locatie plaatsen. Wanneer deze wegzetbewerking wordt bevestigd, wordt het cluster gesloten en opgesplitst, op basis van de waarde die u hebt ingesteld voor het veld **Cluster opsplitsen bij** in het clusterprofiel. Werk-id's worden ook gesloten.
6. Op het mobiele apparaat wordt aangegeven dat het cluster is voltooid.
