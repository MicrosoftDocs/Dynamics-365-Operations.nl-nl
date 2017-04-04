---
title: De onderdelen van een taak instellen
description: Dit onderwerp beschrijft de conceptuele elementen dat een taak bevatten kan en voorbeelden geeft van hoe u deze elementen in uw organisatie kunt.
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: d96b1f01a5cb4370436888deae8fd4835a0dbb80
ms.openlocfilehash: b8143db5b133337603a7f2f46028d91bb81cd947
ms.lasthandoff: 03/31/2017


---

# <a name="setting-up-the-components-of-a-job"></a>De onderdelen van een taak instellen

Dit onderwerp beschrijft de conceptuele elementen dat een taak bevatten kan en voorbeelden geeft van hoe u deze elementen in uw organisatie kunt. 

Voordat u taken maken kunt, moet u verwijzingsinformatie instellen. U kunt een taak met alleen een naam maken. Echter, door extra informatie, zoals de titel van een taak, waaronder u standaardwaarden opgeven voor de posities die aan de taak zijn toegewezen. Bovendien kan een deel van de gegevens die u invoert worden gebruikt voor het filteren van compensatieplannen voor specifieke taken. Als u instellen in aanmerking komen die u gebruiken wilt kunt voor het filteren van compensatieplannen voor een bepaalde taak, moet u instellen taakfuncties en taaktypen voordat u taken instelt. Doordat deze standaardwaarden beschikbaar, bespaart u tijd wanneer u functies aan de taak toevoegen. 

Sommige taakdetails, zoals de functie, het type en de functie zijn datum effectief. Als u een taak vandaag maakt, maar deze gegevens tot een later tijdstip geen toevoegen en vervolgens de taak vanaf de aanmaakdatum bekijkt, worden deze gegevens niet weergegeven. Daarom moet u enkele van deze naslaginformatie weergeven voordat u deze functie nodig. Op die manier u kunt de informatie toevoegen aan nieuwe taken wanneer u deze maakt.

## <a name="job-titles"></a>Functietitels
Voordat u taken maakt, moet u titels voor deze taken instellen. Posities nemen de taaktitels over van de taken waaraan de posities zijn gekoppeld. 

Met behulp van functies onderhouden de **titels** pagina die u openen kunt via de zoekfunctie. Op de ** titels ** pagina, de titels die u wilt gebruiken voor uw taken invoeren.

## <a name="job-types"></a>Taaktypen
Met taaktypen kunt u vergelijkbare taken groeperen in categorieën. Taaktypen zijn niet vereist. Als u van plan bent om taaktypen te gebruiken wanneer u beschikbaarheidregels instelt voor compensatiebeheer, moet u taaktypen instellen voordat u taken instelt. Enkele voorbeelden van taaktypen zijn fulltime en parttime of salaris en het uurtarief dat te betalen. U taaktypen beheren met behulp van de **taaktypen** pagina. Op de **taaktypen** pagina, voer een naam en een korte omschrijving voor het taaktype. In de **vrijgesteld** veld, selecteert u een van de volgende opties om aan te geven van de Fair Labor Standards Act (FLSA) zijn vrijgesteld van taken met dit taaktype:

-   **Uitgezonderd** : taken zijn vrijgesteld van overtijd volgens de FLSA.
-   **Niet-vrijgestelde** : taken zijn niet vrijgesteld van overtijd volgens de FLSA.
-   **Niet van toepassing op** – FLSA valt niet van toepassing.

## <a name="job-functions"></a>Taakfuncties
Koppelingen van de taak op hoog niveau functionele categorieën beschrijven en betrekking hebben op hoog niveau heffingen. Taakfuncties zijn niet vereist. U kunt taakfuncties samen met taaktypen voor het filteren van compensatieplannen voor specifieke taken. U koppelt taakfuncties en taaktypen aan compensatieplannen door geschiktheidsregels instellen op de **geschiktheidsregels** pagina. Vervolgens koppelt u een set niveaus aan een honoreringsregeling die gelden voor de specifieke combinatie van een taaktype en taakfunctie die u met een geschiktheidsregel hebt gedefinieerd. (Deze functies zijn van toepassing op vaste compensatieplannen en variabele honoreringsregelingen.) Echter, als u van plan bent om taakfuncties te gebruiken wanneer u beschikbaarheidregels instelt voor compensatiebeheer instelt, u moet taakfuncties instellen voordat u taken instelt. De volgende tabel ziet enkele voorbeelden van taakfuncties.

| Functie           | Taakfunctie      |
|---------------|-------------------|
| Verkoopleider | Tussenliggende niveaus Manager |
| Accountant    | Professionals     |

U taakfuncties onderhouden met behulp van de **taakfuncties** pagina. Op de **taakfuncties** pagina, een identificatiecode en een korte omschrijving voor de taakfunctie invoeren.

## <a name="job-tasks"></a>Functies
Functietaken omschrijven de basistaken die een werknemer die in een positie voor een taak moet uitvoeren. Dezelfde taak kan worden toegevoegd aan meerdere taken en functies voor de functies die gebruikmaken van die taken. De volgende tabel ziet enkele voorbeelden van taken.

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
<li><strong>Perf-revisie</strong> : prestaties van de taak van elke verkoper controleren.</li>
<li><strong>ABS-revisie</strong> : goedkeuren of afwijzen van elke verkoper verlofaanvragen of registraties.</li>
</ul></td>
</tr>
<tr class="even">
<td>Accountant</td>
<td><strong>FIN-rapport</strong> – Wekelijks financiële rapporten presenteren aan de chief financial officer.</td>
</tr>
</tbody>
</table>

Beheren van projecttaken met behulp van de **projecttaken** pagina. Op de **projecttaken** pagina, een naam en omschrijving voor de functietaak invoeren. In de **opmerking** ingeschakeld, kunt u eventueel extra informatie opgeven. De notities kunnen worden bijgewerkt voor een bepaalde taak zonder de notities die u hier invoert.

## <a name="areas-of-responsibility"></a>Verantwoordelijkheidsgebieden
U gebruikt verantwoordelijkheidsgebieden om aan te geven de werkrollen, processen en producten die verantwoordelijk is voor een werknemer die in een positie voor een taak. Bijvoorbeeld, voor een taak met de naam 'Boekhouder', een verantwoordelijkheidsgebied mogelijk 'Financiële rapportering voor product a' U Verantwoordelijkheidsgebieden onderhouden met behulp van de **verantwoordelijkheidsgebieden** pagina die u vinden kunt via de zoekfunctie. Op de **verantwoordelijkheidsgebieden** pagina, voer een naam en omschrijving voor de verantwoordelijkheid. In de **opmerking** ingeschakeld, kunt u eventueel extra informatie opgeven. De notities kunnen worden bijgewerkt voor een bepaalde taak zonder de notities die u hier invoert.


