---
title: Parameters onkostenbeheer
description: De volgende parameters bepalen de werking in Onkostenbeheer.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c1bc754b92e647f0fdac6799564273fb6ea6fb20
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841076"
---
# <a name="expense-management-parameters"></a>Parameters onkostenbeheer

[!include [banner](../includes/banner.md)]

-----------------------------

De volgende parameters bepalen de algemene werking in Onkostenbeheer.

### <a name="general"></a>Algemeen

| **Veld**                                                | **Omschrijving**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Standaardtarief van kilometervergoeding**                             | Voer het terugbetalingstarief in voor kilometervergoeding. Het tarief wordt vermenigvuldigd met de reisafstand die is ingevoerd op de onkostennota voor het berekenen van het vergoedingsbedrag voor de reiskosten.                       |
|**Persoonlijke onkosten betaald door**                             | Selecteer de persoon die verantwoordelijk is voor het betalen van creditcardtransactiebedragen die zijn gecategoriseerd als persoonlijk.                                                                                                     |
|**Volledige onkostennota weergeven bij drill-back**               | Selecteer deze optie om alle onkosten voor een onkostennota weer te geven bij het bekijken van de details van het oorspronkelijke document van een specifiek boekstuk dat is gegenereerd bij het boeken van de onkostennota.              |
|**Pre-autorisatie voor reizen is verplicht**                 | Selecteer deze optie om te vereisen dat een reisaanvraag moet worden ingediend en goedgekeurd voordat een werknemer een onkostennota kan indienen.                                                                    |
|**Verdelingen kunnen vóór het boeken worden bewerkt**            | Selecteren of de verdelingen van een onkostennota kunnen worden bewerkt voordat ze worden geboekt.                                                                                                                 |
|**Beleid onkostenbeheer evalueren**                     | Selecteer wanneer onkosten worden beoordeeld om te bepalen of er een onkostenbeleid is geschonden. Uitgaven kunnen worden gecontroleerd op overtredingen wanneer de onkostenboeking wordt ingevoerd en opgeslagen of wanneer de onkostennota ter goedkeuring wordt ingediend. De beleidsregels voor vereiste ontvangstbewijzen worden gecontroleerd wanneer de onkostenregel wordt opgeslagen.                   |
|**Intercompany-onkostenregels toestaan**                         | Selecteer of de invoer van onkosten voor andere rechtspersonen is toegestaan in een onkostennota.                                                                                                          |
|**Wisselkoers bewerken toestaan voor creditcardonkosten** | Selecteer deze optie om toe te staan dat de wisselkoers voor de geïmporteerde creditcardonkosten kan worden bewerkt.                                                                        |
|**Hiërarchievelden met meerdere niveaus om weer te geven**                  | Selecteer welke fiatteurvelden moeten worden weergegeven wanneer het workflowtoewijzingstype voor het onkostenrapport is ingesteld op hiërarchie en de hiërarchieselectie is ingesteld op Goedkeuringshiërarchie met meerdere niveaus voor onkosten. Wanneer de goedkeuringshiërarchie met meerdere niveaus wordt gebruikt voor workflows, worden de geselecteerde velden weergegeven en bewerkt in de onkostennota. |
|**Creditcardnummer van personeel opgeven (update juli 2017)**     | Selecteer of een getal van 15 of 16 tekens kan worden ingevoerd en opgeslagen in het veld **Kaart-id** op de pagina **Creditcards** voor een werknemer.                                                                          |

### <a name="financial"></a>Financieel

| **Veld**                                                            | **Omschrijving**     |
|----------------------------------------------------------------------|------------------------------------|
|**Naam dagelijks journaal grootboek**                                         | Selecteer de naam van het grootboekjournaal waarnaar goedgekeurde onkostennota's worden geboekt.            |
|**Belastingterugvordering voor onkosten inschakelen**                                  | Selecteer deze optie om belastingteruggave voor onkosten in te schakelen voor in aanmerking komende uitgaven. Deze optie kan niet worden ingeschakeld als de Amerikaanse btw- en gebruiksbelastingregels zijn ingeschakeld.      |
|**Kasvoorschotten onmiddellijk boeken**                                     | Selecteer deze optie voor het boeken van een goedgekeurd kasvoorschot wanneer het proces voor betalen en overboeken is voltooid. Als deze optie niet wordt geselecteerd, genereert het proces voor betalen en overboeken een niet-geboekt algemeen journaal. |
|**Boekingsdatum corrigeren tijdens boeken**                             | Selecteer deze optie om de boekingsdatum bij te werken wanneer onkosten worden geboekt terwijl huidige periode in de wachtstand staat of is gesloten. De boekingsdatum wordt ingesteld op de volgende openstaande periode.   |
|**De groepering van transacties toestaan op basis van de standaardtegenrekening die is opgegeven in de betalingsmethode**      | Selecteer deze optie om de onkostentransacties voor een onkostennota samen te vatten, op basis van de tegenrekening die is opgegeven in de betalingsmethode voor de onkosten.   
|**Inclusief btw**                                                   | Selecteer deze optie om btw standaard op te nemen in het onkostenbedrag.             |
|**Lasten vrijgeven bij sluiten van reisaanvragen**            | Selecteer deze optie om vorderingen vrij te geven wanneer een goedgekeurde reisaanvraag wordt gesloten.                                                                                   |
|**Indienen van reisaanvraag toestaan bij budgetoverschrijding voor budgetregister en projectbudget** | Selecteer deze optie om werknemers toe te staan om reisaanvragen ter goedkeuring in te dienen die het toegestane budget in het budgetregister of het toegestane projectbudget overschrijden.            |
|**Indienen van onkostennota toestaan bij budgetoverschrijding voor budgetregister en projectbudget**    | Selecteer deze optie om werknemers toe te staan om onkostennota's ter goedkeuring in te dienen die het toegestane budget in het budgetregister of het toegestane projectbudget overschrijden.                |
|**Goedkeuren van onkostennota alleen toestaan bij budgetoverschrijding voor budgetregister**                | Selecteer deze optie om fiatteurs toe te staan om onkostennota's goed te keuren die het toegestane budget in het budgetregister overschrijden.                                                                       |

### <a name="per-diem"></a>Per diem

| **Veld**                             | **Omschrijving**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Minimum uren voor per diem**           | Geef het standaard minimumaantal uren op dat een werknemer moet werken op een dag om een dagvergoeding voor reiskosten te ontvangen.  Deze waarde wordt alleen gebruikt als standaardwaarde voor het veld Minimumaantal uren voor dagtariefniveaus.                                                                                      |
|**Percentage maaltijden**                          | Voer het standaardpercentage voor de dagvergoeding voor maaltijden in dat wordt gebruikt op de eerste en laatste dag van reiskosten wanneer het veld **Maaltijdvergoeding berekenen per** is ingesteld op **Maaltijdtype per dag** of **Santal maaltijden per dag**. De werkdag op de eerste en laatste dag is mogelijk korter dan een standaard werkdag. Daarom kan het bedrag van de dagvergoeding op deze dagen verschillen van het standaardbedrag. Als het percentage is ingesteld op 0, wordt de aftrek van de eerste en laatste dag 0,00. |
|**Percentage hotel**                        | Voer het standaardpercentage per dag in voor hotelkosten dat wordt gebruikt voor de eerste en de laatste dag van de reiskosten. De werkdag op de eerste en laatste dag is mogelijk korter dan een standaard werkdag. Daarom kan het bedrag van de dagvergoeding op deze dagen verschillen van het standaardbedrag. Als het percentage is ingesteld op 0, wordt de aftrek van de eerste en laatste dag 0,00.                                              |
|**Percentage overige**                        | Voer het standaardpercentage per dag in voor diverse onkosten dat wordt gebruikt voor de eerste en de laatste dag van de reiskosten. De werkdag op de eerste en laatste dag is mogelijk korter dan een standaard werkdag. Daarom kan het bedrag van de dagvergoeding op deze dagen verschillen van het standaardbedrag. Als het percentage is ingesteld op 0, wordt de aftrek van de eerste en laatste dag 0,00.                                                                                                     |
|**Vergoeding in percentage voor ontbijt** | Voer het bedrag in dat van de dagvergoeding wordt afgetrokken voor het ontbijt. Als de prijs van het ontbijt is inbegrepen voor de werknemer, kunt u er bijvoorbeeld voor kiezen om het bedrag per dag met 10 procent te verminderen.                               |
|**Vergoeding in percentage voor lunch**    | Voer het bedrag in waarmee de dagvergoeding wordt verminderd voor de lunch. Als de prijs van de lunch is inbegrepen voor de werknemer, kunt u er bijvoorbeeld voor kiezen om het bedrag per dag met 15 procent te verminderen.                                       |
|**Vergoeding in percentage voor diner**   | Voer het bedrag in waarmee de dagvergoeding wordt verminderd voor het diner. Als de prijs van het diner is inbegrepen voor de werknemer, kunt u er bijvoorbeeld voor kiezen om het bedrag per dag met 25 procent te verminderen.                                     |
|**Maaltijdvergoeding berekenen per**         | Selecteer hoe het systeem de dagvergoeding voor maaltijden moet berekenen door te selecteren of de vergoeding is gebaseerd op het maaltijdtype per reis of per dag, of op het toegestane aantal maaltijden per dag.|
|**Afronding van per diem**                  | Selecteer het type afronding dat voor de dagvergoedingen wordt gebruikt. Als u normale afronding selecteert, worden alle dagvergoedingen voor een bedrag van 0,50 afgerond naar 1,00 en alle dagvergoedingen voor een bedrag van minder dan 0,50 naar 0,00.                                                                                              |
|**Berekening van per diem baseren op**         | Selecteer of een dagvergoedingsbedrag is gebaseerd op een kalenderdag of een periode van 24 uur.       |

### <a name="fax-cover-pages"></a>Faxvoorbladen

| **Veld**                      | **Omschrijving**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Instructies**                   | Voer de instructies in die werknemers moeten volgen wanneer ze een voorblad maken voor een fax die wordt gebruikt om ontvangstbewijzen te verzenden die betrekking hebben op een onkostennota. Klik op de knop **Vertalingen** om de taalspecifieke tekst in te voeren die verschijnt op basis van de taal van de gebruiker. |
|**Gebruikers-id (Streepjescodegegevens)** | Selecteer deze optie om de unieke id van een werknemer op te slaan in de streepjescode op het voorblad van de fax.                 |
|**Streepjescode**                      | Selecteer de streepjescode die wordt gebruikt op het voorblad van de fax. Streepjescodes 39 en 128 worden ondersteund door Onkostenbeheer.               |

### <a name="anti-corruption"></a>Anti-corruptie

|                 <strong>Veld</strong>                 |                                                                                                                                                                                            <strong>Beschrijving</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Anti-corruptieattest weergeven</strong>  | Selecteer deze optie om de anti-corruptietekst weer te geven wanneer een nieuwe onkostennota wordt gemaakt. Voor bepaalde onkostencategorieën kan vervolgens worden ingeschakeld dat het anti-corruptieattest moet worden geselecteerd in de onkostennota. Bij een geschenkencategorie voor onkosten voor een overheidsfunctionaris kan bijvoorbeeld worden geëist dat de werknemer bevestigt dat de onkosten voldoen aan het bedrijfsbeleid voor overheidsfunctionarissen. |
| <strong>Anti-corruptiebericht voor inzender</strong> |                                                                                             Voer de tekst in die aan de werknemer wordt weergegeven wanneer een nieuwe onkostennota wordt gemaakt. Klik op de knop <strong>Vertalingen</strong> om de taalspecifieke tekst in te voeren die verschijnt op basis van de taal van de gebruiker.                                                                                             |
| <strong>Anti-corruptiebericht voor fiatteur</strong>  |                                                                                             Voer de tekst in die aan de fiatteur wordt weergegeven wanneer een nieuwe onkostennota wordt gemaakt. Klik op de knop <strong>Vertalingen</strong> om de taalspecifieke tekst in te voeren die verschijnt op basis van de taal van de gebruiker.                                                                                             |

