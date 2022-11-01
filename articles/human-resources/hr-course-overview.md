---
title: Overzicht van cursussen
description: In dit artikel wordt beschreven hoe HR-beheerders en -managers de cursussenfuncties kunnen gebruiken om informatie te onderhouden over de cursussen die beschikbaar zijn voor werknemers.
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
ms.openlocfilehash: a1fd00fb9feea9ab426f67095770389696452215
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716333"
---
# <a name="courses-overview"></a>Overzicht van cursussen

Microsoft Dynamics 365 Human Resources biedt een oplossing voor de leerbehoeften van uw organisatie. Deze oplossing biedt twee leertrajecten voor cursussen: *virtueel* en *geleid door docent*.

*Virtueel leren* is een leerervaring die wordt verbeterd door middel van online resources. Bij *geleid door docent* geeft een docent een trainingssessie voor een groep werknemers of cursisten.

In onze leermodule kunnen HR-professionals, -beheerders, -trainingsmanagers en -managers beide cursuspaden voor werknemers maken en toewijzen.

> [!NOTE]
> Als u deze virtuele cursussen wilt gebruiken, moet u de functie **Cursusverbeteringen** inschakelen in Functiebeheer.

## <a name="set-up-virtual-courses"></a>Virtuele cursussen instellen

Als u virtuele cursussen wilt configureren, moet u de functie **Cursusverbeteringen** inschakelen in Functiebeheer. Ga naar **Cursussen \> Nieuw** en stel de optie **Virtueel** in op **Ja**. Nadat de functie is ingeschakeld, is een koppeling naar een cursus vereist. Het veld **Cursusstatus** wordt ingesteld op **Open**. De optie **Werknemer kan zichzelf registreren** wordt ingesteld op **Ja** maar kan op **Nee** worden ingesteld.

Nadat de functie **Cursusverbeteringen** is ingeschakeld in Functiebeheer, treden de volgende wijzigingen op:

- Er moet een vervaldatum worden gedefinieerd voor cursustoewijzing.
- Er is een cursuskoppeling vereist.
- **Selfservice werknemer** geeft een werknemersoverzicht in **Cursussen** weer. De gebruiker kan cursussen bekijken die achterstallig zijn, die binnenkort moeten worden gevolgd en cursussen die toegewezen zijn.
- Werknemers kunnen virtuele cursussen afronden en een zelfbeoordeling doen.

## <a name="set-up-instructor-led-courses"></a>Door docent geleide cursussen instellen

Cursussen die door docenten worden geleid, hoeven niet te worden geconfigureerd voordat ze worden gebruikt.

De volgende informatie is optioneel en kan voor cursussen worden opgeven. Als deze informatie voor cursussen wordt ingevoerd, moet u deze instellen voordat de cursusrecords worden gemaakt:

- Cursustype
- Leslokaalgroepen
- Cursusgroepen
- Cursuslocaties
- Leslokalen
- Docenten
- Cursustypen

U kunt *cursustypen* gebruiken om cursussen te categoriseren aan de hand van hun structuur of inhoud. Cursustypen kunt u maken op de pagina  **Cursustypen** .

Het minimum- en maximumaantal deelnemers dat u kunt registreren voor een cursus, wordt gedefinieerd op het sneltabblad  **Algemeen**  van de pagina  **Cursussen** .

### <a name="course-setup-type"></a>Instellingstype cursus 

*Instellingstypen* bepalen de structuur van de cursus. Er zijn drie instellingstypen voor cursussen.

| Type instellingen | Description |
|------|--------|
| Standaard | Cursussen van dit insteltype hebben geen dagelijkse agenda. Het is het standaard instellingstype bij het maken van een nieuwe cursus. |
| Agenda | Selecteer dit instellingstype om de details van elke dag van een cursus te plannen die over meerdere dagen plaatsvindt. |
| Agenda + sessie | <p>Selecteer dit instellingstype voor de complexere cursussen. U kunt bijvoorbeeld de agenda voor de cursus onderverdelen in *sporen* en *sessies*:</p><ul><li>*Sporen* zijn specifieke onderwerpen voor een cursus.</li><li>*Sessies* dienen om sporen op te delen en specifieke processen of technieken vast te stellen die relevant zijn voor een spoor.</li></ul> |

### <a name="course-tasks"></a>Cursustaken

Voor elke cursus worden de volgende taken uitgevoerd:

- Deelnemers registreren.
- Een registratiedeadline opgeven.
- Het minimale en maximale aantal deelnemers definiëren.
- Een cursuslocatie en een leslokaal toewijzen.
- Hotels aanraden aan deelnemers.
- Een cursusomschrijving maken, die dan kan worden geplaatst op  **Selfservice werknemer**.

> [!NOTE]
> U kunt een cursus alleen verwijderen als niemand zich ervoor heeft aangemeld.

### <a name="course-statuses"></a>Cursusstatussen

In de volgende tabel staan de cursusstatussen en de acties die voor elke cursus zijn voltooid.

| Status | Acties |
|------|--------|
| Gemaakt | <ul><li>Cursusinformatie invoeren en wijzigen.</li><li>De cursusstatus wijzigen in  **Open**, zodat werknemers zich voor de cursus kunnen aanmelden.</li></ul> | 
| Openen | <ul><li>Deelnemers voor de cursus inschrijven.</li><li>Deelnemers verwijderen uit de cursus.</li><li>Deelnemers voor de cursus bevestigen.</li><li>De status van de cursus wijzigen in  **Afgesloten**  of  **Geannuleerd** voor deelnemers van wie de status  **Bevestigd** is.</li></ul>|
| Dicht | U kunt de cursus opnieuw openen. |
| Geannuleerd | U kunt de cursus opnieuw openen. |

### <a name="course-participants"></a>Deelnemers

*Cursusdeelnemers* zijn werknemers die deelnemen aan een trainingscursus of -gebeurtenis. U kunt deelnemers alleen registreren voor open cursussen.

### <a name="workflow"></a>Werkstroom

Werknemers die zich voor een cursus via registreren de pagina  **Selfservice werknemer**  kunnen hun registratie laten routeren via een werkstroom voor goedkeuring. U kunt een werkstroom toewijzen aan een cursus op het sneltabblad  **Algemeen**  van de pagina  **Cursussen** .
