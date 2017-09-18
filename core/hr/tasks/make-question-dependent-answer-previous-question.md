--- 
title: Een vraag afhankelijk maken van het antwoord op de vorige vraag
description: Voorwaardelijke vragen stellen u in staat op te geven welke opvolgende vraag aan een respondent wordt gepresenteerd op basis van het antwoord op de voorafgaande vraag.
author: twheeloc
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 6e532241d719aa013fcbc0c03f88fbda9cc06b99
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="make-a-question-dependent-on-the-answer-of-the-previous-question"></a>Een vraag afhankelijk maken van het antwoord op de vorige vraag

[!include[task guide banner](../../includes/task-guide-banner.md)]

Voorwaardelijke vragen stellen u in staat op te geven welke opvolgende vraag aan een respondent wordt gepresenteerd op basis van het antwoord op de voorafgaande vraag. Als u bijvoorbeeld vraag"Hebt u liever koffie of thee", kan een logische opvolgende vraag worden bepaald afhankelijk van of de respondent koffie of thee als antwoord selecteert. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="find-the-existing-questionnaire"></a>De bestaande vragenlijst zoeken
1. Ga naar Vragenlijst > Ontwerp > Vragenlijsten.
2. Selecteer in de lijst de vragenlijst WorkFH.

## <a name="add-all-questions-and-sub-questions-to-the-questionnaire"></a>Alle vragen en subvragen toevoegen aan de vragenlijst
1. Klik op Vragen.
2. Klik op Nieuw.
3. Selecteer vraag nummer 00016 in het veld Vraag.
4. Zoek en selecteer de gewenste record in de lijst.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik op Opslaan.
7. Sluit de pagina.

## <a name="set-the-questionnaire-sequence-to-conditional-and-make-the-question-dependent-on-the-appropriate-question"></a>De volgorde van de vragenlijst instellen op Voorwaardelijk en de vraag afhankelijk maken van de bijbehorende vraag
1. Klik op Bewerken.
2. Vouw de sectie Instellingen uit.
3. Selecteer "Voorwaardelijk" in het veld Vraagvolgorde.
4. Klik op Voorwaardelijke vraag.
5. Selecteer "Questions\Explain why you answered the previous question the way you did" in de structuur.
6. Selecteer vraag nummer 00009 in het veld Primaire vraag.
7. Klik in de lijst op de koppeling in de geselecteerde rij.
8. Voer in het veld Antwoord de antwoordvolgorde-id in van de antwoordoptie waarvan u de vraag afhankelijk wilt maken. Voer bijvoorbeeld 1 in voor de eerste antwoordoptie.
9. Klik op Opslaan.
10. Selecteer "Questions\I am paid fairly for the work I do." in de structuur.
    * Merk op dat de vraagstructuur wordt bijgewerkt om de afhankelijkheid aan te geven.  

