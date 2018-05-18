---
title: De onderdelen van een functie instellen
description: In dit onderwerp worden de conceptuele elementen beschreven die een functie kan bevatten en worden voorbeelden gegeven van de wijze waarop u deze elementen in uw organisatie kunt gebruiken.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: rschloma
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 88e8c1ae98ad5618feff3d2bb88d8f8cfe2ff9ba
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="setting-up-the-components-of-a-job"></a>De onderdelen van een functie instellen

[!include [banner](includes/banner.md)]

[!include [retail name](includes/retail-name.md)]

In dit onderwerp worden de conceptuele elementen beschreven die een functie kan bevatten en worden voorbeelden gegeven van de wijze waarop u deze elementen in uw organisatie kunt gebruiken. 

Voordat u functies kunt maken, moet u enige referentiegegevens instellen. U kunt een functie maken die alleen een naam heeft. Echter door aanvullende informatie op te nemen, zoals de titel van een functie, geeft u standaardwaarden op voor de posities die aan de functie zijn toegewezen. Bovendien kan een deel van de gegevens die u invoert, worden gebruikt voor het filteren van compensatieplannen voor specifieke functies. Als u geschiktheid wilt instellen op basis waarvan u compensatieplannen voor een specifieke functie kunt filteren, moet u functiebeschrijvingen en functietypen instellen voordat u functies instelt. Als u deze standaardwaarden beschikbaar hebt, bespaart u tijd wanneer u posities aan de functie toevoegt. 

Sommige functiedetails, zoals de functietitel en het functietype, zijn datumafhankelijk. Als u een functie vandaag maakt, maar deze gegevens pas later toevoegt en vervolgens de functie vanaf de aanmaakdatum bekijkt, worden deze gegevens niet weergegeven. Daarom moet u een deel van deze referentiegegevens maken voordat u deze nodig hebt. Op die manier kunt u de informatie toevoegen aan nieuwe functies wanneer u deze maakt.

## <a name="job-titles"></a>Functietitels
Voordat u taken maakt, moet u titels voor deze taken instellen. Posities nemen de taaktitels over van de taken waaraan de posities zijn gekoppeld. 

Op de pagina **Titels** kunt u functietitels onderhouden. Deze pagina opent u met de functie Zoeken. Op de pagina **Titels** voert u de titels in die u wilt gebruiken voor uw functies.

## <a name="job-types"></a>Taaktypen
U gebruikt functietypen om vergelijkbare functies in categorieën te groeperen. Functietypen zijn niet verplicht. Als u van plan bent om taaktypen te gebruiken wanneer u beschikbaarheidregels instelt voor compensatiebeheer, moet u taaktypen instellen voordat u taken instelt. Enkele voorbeelden van functietypen zijn fulltime en parttime of salaris en uurtarief. U onderhoudt functietypen met behulp van de pagina **Functietypen**. Voer op de pagina **Functietypen** een naam en een korte omschrijving voor het functietype in. Selecteer in het veld **Vrijstellingsstatus** een van de volgende opties om de FLSA-vrijstellingsstatus (Fair Labor Standards Act) aan te geven voor functies die dit functietype hebben:

-   **Vrijgesteld**: functies zijn vrijgesteld van overuren volgens de FLSA.
-   **Niet-vrijgesteld**: functies zijn niet vrijgesteld van overuren volgens de FLSA.
-   **Niet van toepassing**: FLSA is niet van toepassing.

## <a name="job-functions"></a>Taakfuncties
Functiebeschrijvingen beschrijven functionele categorieën op hoog niveau beschreven en hebben betrekking op taken op hoog niveau. Functiebeschrijvingen zijn niet verplicht. U kunt functiebeschrijvingen in combinatie met functietypen gebruiken om compensatieplannen voor specifieke functies te filteren. U koppelt functiebeschrijvingen en functietypen aan compensatieplannen door geschiktheidsregels in te stellen op de pagina **Geschiktheidsregels**. U kunt vervolgens een aantal niveaus aan een compensatieplan koppelen dat van toepassing is op de specifieke combinatie van een functietype en functiebeschrijving die u via een geschiktheidsregel hebt gedefinieerd. (Deze functies gelden zowel voor vaste compensatieplannen als voor variabele compensatieplannen.) Als u echter van plan bent om functiebeschrijvingen te gebruiken wanneer u geschiktheidsregels instelt voor compensatiebeheer, moet u functiebeschrijvingen instellen voordat u functies instelt. In de volgende tabel vindt u enkele voorbeelden van functiebeschrijvingen.

| Functie           | Taakfunctie         |
|---------------|----------------------|
| Verkoopleider | Manager middelste niveau    |
| Accountant    | Professionals        |

U onderhoudt functiebeschrijvingen met behulp van de pagina **Functiebeschrijvingen**. Voer op de pagina **Functiebeschrijvingen** een identificatiecode en een korte omschrijving voor de functie in.

## <a name="job-tasks"></a>Functies
Functietaken beschrijven de basistaken die een werknemer op een positie voor een functie moet uitvoeren. Dezelfde functietaak kan worden toegevoegd aan meerdere functies, en aan posities voor de functies die deze functietaken gebruiken. In de volgende tabel vindt u enkele voorbeelden van functietaken.

<table>
<thead>
<tr class="header">
<th>Functie</th>
<th>Functietaak</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Verkoopleider</td>
<td><ul>
<li><strong>Perf-revisie</strong> – Bekijk de prestaties van elke verkoper.</li>
<li><strong>Abs-review</strong> – Verlofaanvragen of registraties van elke verkoper goedkeuren of weigeren.</li>
</ul></td>
</tr>
<tr class="even">
<td>Accountant</td>
<td><strong>FIN-rapport</strong> – wekelijks financiële rapporten presenteren aan het hoofd van de financiële afdeling.</td>
</tr>
</tbody>
</table>

U onderhoudt functietaken met behulp van de pagina **Functietaken**. Voer op de pagina **Functietaken** een naam en een omschrijving voor de functietaak in. In het veld **Notitie** kunt u desgewenst aanvullende informatie invoeren. De notities kunnen worden bijgewerkt voor een specifieke functie zonder de notities te wijzigen die u hier hebt ingevoerd.

## <a name="areas-of-responsibility"></a>Verantwoordelijkheidsgebieden
U gebruikt verantwoordelijkheidsgebieden om aan te geven voor welke werkrollen, processen en producten een werknemer op een positie voor een functie verantwoordelijk is. Voor bijvoorbeeld een functie met de titel 'Boekhouder' kan een verantwoordelijkheidsgebied 'Financiële rapportage voor Product A' zijn. U onderhoudt verantwoordelijkheidsgebieden met behulp van de pagina **Verantwoordelijkheidsgebied**. Deze pagina vindt u met de functie Zoeken. Voer op de pagina **Verantwoordelijkheidsgebied** een naam en een omschrijving voor de verantwoordelijkheid in. In het veld **Notitie** kunt u desgewenst aanvullende informatie invoeren. De notities kunnen worden bijgewerkt voor een specifieke functie zonder de notities te wijzigen die u hier hebt ingevoerd.

## <a name="steps-for-creating-a-job"></a>Stappen voor het maken van een taak
Raadpleeg het onderwerp [Nieuwe taken definiëren](../fin-and-ops/hr/tasks/define-new-jobs.md) voor de stapsgewijze procedure voor het maken van een nieuwe taak. 

