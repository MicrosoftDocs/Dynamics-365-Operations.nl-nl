--- 
title: Vragenlijsten distribueren met een planning
description: Met vragenlijstplanning kunt u vragenlijsten plannen voor en distribueren naar meerdere respondenten.
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6795c5ed48ef1d716ddec5cca1a2f6414bb318ce
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="distribute-questionnaires-using-scheduling"></a>Vragenlijsten distribueren met een planning

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Met vragenlijstplanning kunt u vragenlijsten plannen voor en distribueren naar meerdere respondenten. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="create-a-questionnaire-schedule"></a>Een planning voor vragenlijsten maken
1. Ga naar Vragenlijst > Distribueren > Vragenlijstplanningen.
2. Klik op Nieuw.
3. Typ een waarde in het veld Planning.
4. Typ een waarde in het veld Omschrijving.
    * Stel de planning in op Anoniem als de antwoorden zonder aan het antwoord gekoppelde namen moeten worden vastgelegd.  
    * Het toestaan van anonieme resultaten moet eerst zijn ingesteld in de HR-parameters.  
5. Selecteer in het veld Type het type planning.  In dit voorbeeld wordt het type Tevredenheid gebruikt.
6. Zoek en selecteer de gewenste record in de lijst.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Voer een datum in het veld Datum in.
9. Vouw de sectie E-mail voor werknemersselfservice uit.
10. Typ een waarde in het veld Onderwerp.
    * Voorbeeld: Vragenlijst beschikbaar  
11. Typ in het veld Tekst de tekst van uw e-mail. De variabele kan worden gebruikt om waarden in het systeem te vertegenwoordigen.
    * Voorbeeld: Beste %P%, Meld u aan bij de Werknemerselfservice en vul de vragenlijst Personeelsgezondheid in.  Contoso  
12. Klik op Opslaan.

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a>De instellingsdetails gebruiken om de vragenlijst(en) te selecteren die moet(en) worden beantwoord en eventuele query's die moeten worden gebruikt om respondenten te selecteren.
1. Klik op Instellingsdetails.
2. Selecteer in de lijst een query waarmee u in het systeem wilt laten zoeken naar respondenten voor de vragenlijst.
    * Voorbeeld: Medewerkers  
3. Klik op Query weergeven of wijzigen om specifieke personen te selecteren of de query aan te passen om personen te zoeken die aan specifieke criteria voldoen.
    * Houd er rekening mee dat alle respondenten ook gebruikers in het systeem moeten zijn.  
4. Markeer in de lijst de rij voor Persoon.
5. Typ of selecteer een waarde in het veld Criteria.
    * Selecteer Julia Funderburk  
6. Selecteer in de lijst Julia Funderburk.
7. Klik op OK.
8. Klik op het tabblad Vragenlijsten.
9. Vouw in de structuur het knooppunt voor het vragenlijsttype 'Tevredenheidsonderzoek' uit.
10. Selecteer in de structuur 'Workforce Health Assessment'.
11. Klik op OK.
12. Klik op Geplande antwoordsessie.
    * Houd er rekening mee dat geplande antwoordsessies voor elke geselecteerde/opgezochte gebruiker zijn gemaakt.  
13. Sluit de pagina.

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a>De vragenlijstplanning starten om de vragenlijst beschikbaar te maken voor respondenten zodat ze deze kunnen invullen.
1. Klik op Functies.
2. Klik op Start.
3. Klik op OK.

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a>De e-mail verzenden om respondenten te informeren dat de vragenlijst beschikbaar is.
1. Klik op Functies.
2. Klik op E-mail verzenden.
3. Klik op Annuleren.

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a>Geplande antwoordsessies gebruiken om te controleren wie de vragenlijst moet invullen.
1. Klik op Geplande antwoordsessie.
    * Verwijder alle resterende geplande antwoordsessies wanneer u klaar bent om de geplande sessie te beëindigen.  
2. Klik op Verwijderen.
3. Klik op Ja.
4. Sluit de pagina.

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a>Beëindig de planning wanneer alle respondenten de vragenlijst hebben ingevuld en/of alle resterende geplande antwoordsessies zijn verwijderd.
1. Klik op Functies.
2. Klik op Beëindigen.
3. Klik op OK.


