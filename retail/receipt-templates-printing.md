---
title: Ontvangstsjablonen en afdrukken
description: In dit artikel wordt beschreven hoe u formulierindelingen kunt wijzigen om te bepalen hoe ontvangsten, facturen en andere documenten worden afgedrukt. Microsoft Dynamics 365 for Operations - Retail bevat een ontwerper van formulierindeling waarmee u kunt eenvoudig maken en verschillende soorten formulierindelingen te wijzigen.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: fabaacbc7187b38a1745c2139a9eb7760f2be987
ms.lasthandoff: 03/31/2017


---

# <a name="receipt-templates-and-printing"></a>Ontvangstsjablonen en afdrukken

In dit artikel wordt beschreven hoe u formulierindelingen kunt wijzigen om te bepalen hoe ontvangsten, facturen en andere documenten worden afgedrukt. Microsoft Dynamics 365 for Operations - Retail bevat een ontwerper van formulierindeling waarmee u kunt eenvoudig maken en verschillende soorten formulierindelingen te wijzigen.

**Belangrijk:** u moet formulierindelingen instellen en profielen ontvangstbewijzen en andere documenten afdrukken vanuit Retail POS op moderne en Cloud-POS voor ontvangstbewijzen. U kunt meerdere formulierindelingen in een ontvangstbewijsprofiel opnemen. U kunt vervolgens het ontvangstprofiel toewijzen aan een printer door een hardwareprofiel te wijzigen.

## <a name="set-up-a-receipt-format"></a>Een ontvangstbewijsindeling instellen
1.  Klik op **detailhandel en commerce**&gt;**instellingen voor het kanaal**&gt;**POS-instellingen**&gt;**POS**&gt;**indelingen voor ontvangstbewijzen**.
2.  Klik op de pagina **Ontvangstbewijsindeling** op **Nieuw** om een nieuwe formulierindeling te maken, of selecteer een bestaande formulierindeling.
3.  Voer in het veld **Ontvangstbewijsindeling** een id in voor de formulierindeling en selecteer vervolgens het type ontvangstbewijs waarvoor deze indeling wordt gebruikt. U kunt ook een omschrijving en een korte naam voor het ontvangstbewijs invoeren in het veld **Titel**.
4.  Op het sneltabblad **Algemeen** selecteert u een optie om het drukgedrag te definiëren:
    -   **Altijd afdrukken** - De ontvangst wordt automatisch afgedrukt, waar toepasselijk.
    -   **Niet afdrukken** – Het ontvangstbewijs wordt niet afgedrukt.
    -   **Vragen aan gebruiker** - De gebruiker wordt gevraagd het ontvangstbewijs af te drukken.
    -   **Zoals vereist** - Deze optie wordt alleen gebruikt voor giftontvangsten. Wanneer deze optie is geselecteerd, kan de gebruiker een ontvangstbewijs van een geschenk afdrukken vanaf de pagina, **Wijzigen**, als een ontvangstbewijs van geschenk is vereist.

## <a name="design-a-receipt-format"></a>Een ontvangstbewijsindeling ontwerpen
Gebruik de ontwerpfunctie voor formulierindelingen om de grafische indeling van het formulierdocument te maken. De pagina **Ontwerper van ontvangstbewijsindeling** bevat drie gedeelten: **Koptekst**, **Regels** en **Voettekst**. Voor sommige typen formulierindelingen worden elementen uit alle drie de secties gebruikt, terwijl voor andere typen elementen uit slechts één of twee secties worden gebruikt. Als u de beschikbare elementen voor elke sectie wilt bekijken, klikt u op de desbetreffende knop in het navigatievenster aan de linkerkant van de pagina.

1.  Klik op **detailhandel en commerce**&gt;**instellingen voor het kanaal**&gt;**POS-instellingen**&gt;**POS**&gt;**indelingen voor ontvangstbewijzen**.
2.  Op de **Ontvangstbewijsindeling** pagina selecteert u een indeling, en klikt u op **Ontwerper**.
3.  Klik op **Uitvoeren** om de installatie van de detailhandelsontwerperhost te starten.
4.  Op de Meldingsbalk die onder in het Internet Explorer-venster verschijnt, klikt u op **Openen** om de installatie van de één-klik-ontwerper te starten. (Het systeemvak worden weergegeven mogelijk weergegeven in een andere locatie in andere browsers.) Het voortgangsvenster toont de voortgang van het installatieproces.
5.  Nadat de installatie is voltooid, uw Dynamics 365 voor bewerkingen gebruikersnaam en wachtwoord invoeren en klik vervolgens op **inloggen** om te beginnen de ontwerper.
6.  Nadat uw referenties zijn gevalideerd en de ontwerper is gestart, kunt u beginnen met de ontvangstindeling te ontwerpen of een bestaande indeling te wijzigen.
7.  Voor het maken van de elementen van het formulier selecteert u de sectie **Koptekst**, **Regels** of **Voettekst** en sleept u een element uit die sectie naar de werkruimte. De meeste elementen bevatten variabelen, die automatisch worden gevuld met gegevens uit de database. Met andere elementen, zoals **Tekst**, kunt u aangepaste tekst op het ontvangstbewijs afdrukken. **Opmerking:** U kunt aangeven hoeveel regels elke sectie omvat door het getal te wijzigen in de rechterbenedenhoek van die sectie. Om het gemakkelijker te maken een sectie te veranderen kunt u de hoogte ervan vergroten door de formaatbalk onderaan de sectie te verslepen. De hoogte van de sectie in de werkruimte heeft geen invloed op het aantal regels van het werkelijke ontvangstbewijs.
8.  Nadat u een element naar de werkruimte hebt gesleept, stelt u in het deelvenster **Objectgegevens **onder aan de pagina de eigenschappen voor het onderdeel in. Voer een of meer van de volgende instellingen in:
    -   **Uitlijnen**: stel de uitlijning van het veld in op **Links** of **Rechts**.
    -   **Opvulteken** – Het spatieteken opgeven. Standaard wordt een lege positie gebruikt. U kunt echter elk teken invoeren.
    -   **Voorvoegsel** – Typ de waarde die aan het begin van het veld wordt weergegeven. Deze instelling is slechts van toepassing op het gedeelte **Regels **van de indeling.
    -   **Tekens** – Geef het maximale aantal tekens op dat het veld kan bevatten als het element een variabele bevat. Als de tekst in het veld langer is dan het aantal tekens dat u opgeeft, wordt de tekst ingekort om in het veld te passen.
    -   **Variabele** – Dit selectievakje is automatisch ingeschakeld als dit element een variabele bevat en niet kan worden aangepast.
    -   **Lettertype** – Het lettertype instellen op **Normaal** of **Vet**. Vetgedrukte letters nemen twee maal zoveel plaats in beslag als normale letters. Dit betekent dat sommige tekens mogelijk worden afgekapt.
    -   **Verwijderen**: klik op deze knop om het geselecteerde gedeelte uit de formulierindeling te verwijderen.

## <a name="assign-receipt-profiles"></a>Ontvangstbewijsprofielen toewijzen
De ontvangstprofielen worden direct toegewezen aan printers via het hardwareprofiel.

1.  Het hardwareprofiel openen door te klikken op **detailhandel en commerce**&gt;**instellingen voor het kanaal**&gt;**POS-instellingen**&gt;**POS profielen**&gt;**hardwareprofiel**.
2.  Selecteer de printer en wijs vervolgens in het veld **Ontvangstbewijsprofiel ** het ontvangstprofiel toe voor gebruik in het register.

**Opmerking:** Als twee printers worden gebruikt, kan één printer worden gebruikt om standaard 40 kolom thermische ontvangstbewijzen af te drukken. De tweede printer wordt meestal gebruikt voor het afdrukken van ontvangsttypen van een hele pagina die meer informatie vereisen. Deze ontvangsttypen omvatten de ontvangsten van klantorders en klantfacturen.


