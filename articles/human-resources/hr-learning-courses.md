---
title: Trainingen instellen
description: Personeelsmedewerkers en managers kunnen de cursussenfuncties gebruiken om informatie te onderhouden over de cursus die aan werknemers wordt aangeboden.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 45466b8f52ddc261737da7474767c21f5bd331f8
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689882"
---
# <a name="set-up-training-courses"></a>Trainingen instellen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Personeelsmedewerkers en managers kunnen de cursussenfuncties gebruiken om informatie te onderhouden over de cursus die aan werknemers wordt aangeboden.

##  <a name="set-up-prerequisites"></a>Instellingsvereisten

De volgende informatie is vereist en moet worden ingesteld voordat u cursussen maakt.
-   **Cursustypen**

De volgende inforatie is optionele informatie die u u voor cursussen kunt opgeven. Als u weet dat u deze informatie voor cursussen gaat invoeren, moet u deze informatie instellen voordat u cursusregistraties maakt.
-   **Leslokaalgroepen**
-   **Cursusgroepen**
-   **Cursuslocaties**
-   **Leslokalen**
-   **Docenten**

## <a name="course-types"></a>Cursustypen
U kunt cursustypen gebruiken om cursussen te categoriseren cursussen aan de hand van de structuur of de inhoud van de cursus. Cursustypen u kunt maken op de pagina **Cursustypen**. Wanneer u een cursusregistratie maakt, moet u een cursustype selecteren.

## <a name="course-setup-type"></a>Instellingstype cursus
In de volgende tabel worden de drie instellingstypen voor cursussen weergegeven. Instellingstypen bepalen de structuur van de cursus.

<table>
<thead>
<tr class="header">
<th>Instellingstype</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Standaard</strong></td>
<td>Selecteer dit type voor cursussen die geen dagelijkse agenda hebben. Dit is het standaard instellingstype bij het maken van een nieuwe cursus.</td>
</tr>
<tr class="even">
<td><strong>Agenda</strong></td>
<td>Selecteer dit type om de details van elke dag van een cursus te plannen die over meerdere dagen plaatsvindt.</td>
</tr>
<tr class="odd">
<td><strong>Agenda + sessie</strong></td>
<td>Selecteer dit type voor de complexere cursussen. U kunt bijvoorbeeld de agenda voor de cursus onderverdelen in sporen en sessies.
<ul>
<li><strong>Spoor</strong>: Sporen zijn specifieke onderwerpen voor een cursus.</li>
<li><strong>Sessies</strong>: Sporen kunnen vervolgens in sessies worden verdeeld, die specifieke processen of technieken helpen bepalen die relevant zijn voor een spoor.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a>Cursustaken
Voor elke cursus kunt de volgende taken uitvoeren:
- Deelnemers registreren.
- Een registratiedeadline opgeven.
- Het minimale en maximale aantal deelnemers definiëren.
- Een cursuslocatie en een leslokaal toewijzen.
- Hotels aanraden aan deelnemers.
- Een cursusomschrijving aanmaken, die dan kan worden weergegeven in de **Selfservice werknemer**

  >**Opmerking:** u kunt een cursus alleen verwijderen als niemand zich ervoor heeft aangemeld. 

## <a name="course-statuses"></a>Cursusstatussen
In de volgende tabel worden de mogelijke cursusstatussen weergegeven en de acties die u kunt uitvoeren wanneer de cursus een specifieke status heeft.

<table>
<thead>
<tr class="header">
<th>Status</th>
<th>Acties</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Gemaakt</strong></td>
<td><ul>
<li>Cursusinformatie invoeren en wijzigen.</li>
<li>De cursusstatus wijzigen in <strong>Open</strong>, zodat werknemers zich voor de cursus kunnen aanmelden.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Openen</strong></td>
<td><ul>
<li>Deelnemers voor de cursus inschrijven.</li>
<li>Deelnemers verwijderen uit de cursus.</li>
<li>Deelnemers voor de cursus bevestigen.</li>
<li>De status van de cursus wijzigen in <strong>Afgesloten</strong> of <strong>Geannuleerd</strong>.</li>
<li>Vragenlijsten plannen voor deelnemers van wie de status <strong>Bevestigd</strong> is.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Gesloten</strong></td>
<td>U kunt de cursus opnieuw openen.</td>
</tr>
<tr class="even">
<td><strong>Geannuleerd</strong></td>
<td>U kunt de cursus opnieuw openen.</td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a>Deelnemers
Cursusdeelnemers zijn werknemers die deelnemen aan een trainingscursus of -gebeurtenis. U kunt alleen deelnemers registreren voor open cursussen. Het minimum- en maximumaantal deelnemers dat u kunt registreren voor een cursus, wordt gedefinieerd op het sneltabblad **Algemeen** van de pagina **Cursussen**.

## <a name="workflow"></a>Workflow

Werknemers die zich voor een cursus via registreren de pagina **Selfservice werknemer** kunnen hun inschrijving laten routeren via de workflow voor goedkeuring. U kunt een workflow toewijzen aan een cursus op het sneltabblad **Algemeen** van de pagina **Cursussen**.







[!INCLUDE[footer-include](../includes/footer-banner.md)]
