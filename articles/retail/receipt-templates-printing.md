---
title: Ontvangstbewijsindelingen instellen en ontwerpen
description: In dit artikel wordt beschreven hoe u formulierindelingen kunt wijzigen om te bepalen hoe ontvangsten, facturen en andere documenten worden afgedrukt. Microsoft Dynamics 365 for Retail heeft een ontwerper voor formulierindelingen waarmee u gemakkelijk en grafisch verschillende soorten formulierindelingen kunt maken en veranderen.
author: rubencdelgado
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFormLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 57841
ms.assetid: e530dd8e-95e2-4021-90bd-ce1235f9e250
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 13249e1b109586b2c520a1be30c47ac4393abe49
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553063"
---
# <a name="set-up-and-design-receipt-formats"></a>Ontvangstbewijsindelingen instellen en ontwerpen

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u formulierindelingen kunt wijzigen om te bepalen hoe ontvangsten, facturen en andere documenten worden afgedrukt. Microsoft Dynamics 365 for Retail heeft een ontwerper voor formulierindelingen waarmee u gemakkelijk en grafisch verschillende soorten formulierindelingen kunt maken en veranderen.

> [!IMPORTANT]
> U moet formulierindelingen en ontvangstprofielen instellen om ontvangstbewijzen en andere documenten af te drukken vanuit Retail Modern POS en Cloud POS. U kunt meerdere formulierindelingen in een ontvangstbewijsprofiel opnemen. U kunt vervolgens het ontvangstprofiel toewijzen aan een printer door een hardwareprofiel te wijzigen.

## <a name="set-up-a-receipt-format"></a>Een ontvangstbewijsindeling instellen

1. Klik op **Retail** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS** &gt; **Ontvangstbewijsindelingen**.
2. Klik op de pagina **Ontvangstbewijsindeling** op **Nieuw** om een nieuwe formulierindeling te maken, of selecteer een bestaande formulierindeling.
3. Voer in het veld **Ontvangstbewijsindeling** een id in voor de formulierindeling en selecteer vervolgens het type ontvangstbewijs waarvoor deze indeling wordt gebruikt. U kunt ook een omschrijving en een korte naam voor het ontvangstbewijs invoeren in het veld **Titel**.
4. Op het sneltabblad **Algemeen** selecteert u een optie om het drukgedrag te definiëren:

    - **Altijd afdrukken** - De ontvangst wordt automatisch afgedrukt, waar toepasselijk.
    - **Niet afdrukken** – Het ontvangstbewijs wordt niet afgedrukt.
    - **Vragen aan gebruiker** - De gebruiker wordt gevraagd het ontvangstbewijs af te drukken.
    - **Zoals vereist** - Deze optie wordt alleen gebruikt voor giftontvangsten. Wanneer deze optie is geselecteerd, kan de gebruiker een ontvangstbewijs van een geschenk afdrukken vanaf de pagina, **Wijzigen**, als een ontvangstbewijs van geschenk is vereist.

## <a name="design-a-receipt-format"></a>Een ontvangstbewijsindeling ontwerpen

Gebruik de ontwerpfunctie voor formulierindelingen om de grafische indeling van het formulierdocument te maken. De pagina **Ontwerper van ontvangstbewijsindeling** bevat drie gedeelten: **Koptekst**, **Regels** en **Voettekst**. Voor sommige typen formulierindelingen worden elementen uit alle drie de secties gebruikt, terwijl voor andere typen elementen uit slechts één of twee secties worden gebruikt. Als u de beschikbare elementen voor elke sectie wilt bekijken, klikt u op de desbetreffende knop in het navigatievenster aan de linkerkant van de pagina.

1. Klik op **Retail** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS** &gt; **Ontvangstbewijsindelingen**.
2. Op de **Ontvangstbewijsindeling** pagina selecteert u een indeling, en klikt u op **Ontwerper**.
3. Klik op **Uitvoeren** om de installatie van de detailhandelsontwerperhost te starten.
4. Op de meldingsbalk die onder in het Internet Explorer-venster verschijnt, klikt u op **Openen** om de installatie van de één-klik-ontwerper te starten. (De meldingsbalk kan op een andere locatie worden weergegeven in andere browsers.) De voortgangsindicator geeft de voortgang van het installatieproces weer.
5. Nadat de installatie is voltooid, voert u uw Dynamics 365 for Retail-gebruikersnaam en -wachtwoord in en klikt u op **Aanmelden** om de ontwerper te starten.
6. Nadat uw referenties zijn gevalideerd en de ontwerper is gestart, kunt u beginnen met de ontvangstindeling te ontwerpen of een bestaande indeling te wijzigen.
7. Voor het maken van de elementen van het formulier selecteert u de sectie **Koptekst**, **Regels** of **Voettekst** en sleept u een element uit die sectie naar de werkruimte. De meeste elementen bevatten variabelen, die automatisch worden gevuld met gegevens uit de database. Met andere elementen, zoals **Tekst**, kunt u aangepaste tekst op het ontvangstbewijs afdrukken.

    > [!NOTE]
    > U kunt aangeven hoeveel regels elke sectie omvat door het getal te wijzigen in de rechterbenedenhoek van die sectie. Om het gemakkelijker te maken een sectie te veranderen kunt u de hoogte ervan vergroten door de formaatbalk onderaan de sectie te verslepen. De hoogte van de sectie in de werkruimte heeft geen invloed op het aantal regels van het werkelijke ontvangstbewijs.

8. Nadat u een element naar de werkruimte hebt gesleept, stelt u in het deelvenster **Objectgegevens** onder aan de pagina de eigenschappen voor het onderdeel in. Voer een of meer van de volgende instellingen in:

    - **Uitlijnen**: stel de uitlijning van het veld in op **Links** of **Rechts**.
    - **Opvulteken** – Het spatieteken opgeven. Standaard wordt een lege positie gebruikt. U kunt echter elk teken invoeren.
    - **Voorvoegsel** – Typ de waarde die aan het begin van het veld wordt weergegeven. Deze instelling is slechts van toepassing op het gedeelte **Regels** van de indeling.
    - **Tekens** – Geef het maximale aantal tekens op dat het veld kan bevatten als het element een variabele bevat. Als de tekst in het veld langer is dan het aantal tekens dat u opgeeft, wordt de tekst ingekort om in het veld te passen.
    - **Variabele** – Dit selectievakje is automatisch ingeschakeld als dit element een variabele bevat en niet kan worden aangepast.
    - **Lettertype** – Het lettertype instellen op **Normaal** of **Vet**. Vetgedrukte letters nemen twee maal zoveel plaats in beslag als normale letters. Dit betekent dat sommige tekens mogelijk worden afgekapt.
    - **Tekengrootte** – De tekengrootte instellen op **Normaal** of **Groot**. Grote letters zijn twee keer zo hoog als gewone letters. Daarom kan gebruik van grote letters leiden tot overlappende tekst op de kassabon.
    - **Verwijderen**: klik op deze knop om het geselecteerde gedeelte uit de formulierindeling te verwijderen.

## <a name="assign-receipt-profiles"></a>Ontvangstbewijsprofielen toewijzen

De ontvangstprofielen worden direct toegewezen aan printers via het hardwareprofiel.

1. Open het hardwareprofiel door te klikken op **Retail** &gt; **Kanaalinstellingen** &gt; **POS-instellingen** &gt; **POS-profielen** &gt; **Hardwareprofiel**.
2. Selecteer de printer en wijs vervolgens in het veld **Ontvangstbewijsprofiel** het ontvangstprofiel toe voor gebruik in het register.

> [!NOTE]
> Als twee printers worden gebruikt, kan één printer worden gebruikt om standaard 40 kolom thermische ontvangstbewijzen af te drukken. De tweede printer wordt meestal gebruikt voor het afdrukken van ontvangsttypen van een hele pagina die meer informatie vereisen. Deze ontvangsttypen omvatten de ontvangsten van klantorders en klantfacturen.
