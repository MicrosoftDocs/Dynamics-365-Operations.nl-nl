---
title: Uw werknemers organiseren met afdelingen, taken en posities
description: Afdelingen, taken en functies zijn organisatie-elementen die worden onderhouden in Human resources. Dit onderwerp bevat conceptuele informatie over deze elementen.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmJob, HcmPosition, OMOperatingUnit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent, Retail
ms.custom: 87933
ms.assetid: eb5dcacb-a5fe-451d-b30a-7ef14da65d81
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 8b74542b85810409e062a42e323c0527711d562f
ms.sourcegitcommit: 49a642cd5e0519e381ff558f59c993ee77f55108
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2019
ms.locfileid: "374392"
---
# <a name="organize-your-workforce-by-using-departments-jobs-and-positions"></a>Uw werknemers organiseren met afdelingen, taken en posities

[!include [banner](includes/banner.md)]


Afdelingen, taken en functies zijn organisatie-elementen die worden onderhouden in Human resources. Dit onderwerp bevat conceptuele informatie over deze elementen. 

Het volgende voorbeeld wordt gebruikt om de concepten te illustreren die in dit onderwerp worden beschreven.

|**Afdeling**|**Positie**|**Functie**|
|---|---|---|
|**Verkoop**|Verkoopmanager (Oost)|Verkoopleider|
|**Verkoop**|Verkoopmanager (West)|Verkoopleider|
|**Verkoop**|Verkoopmanager (centraal)|Verkoopleider|
|**Boekhouding**|Supervisor boekhouding|Accountingmanager|
|**Boekhouding**|Accounting-A|Accountant|
|**Human resources**|HR manager (Oost)|HR manager|
|**Human resources**|HR manager (West)|HR manager|
|**Human resources**|HR manager (centraal)|HR manager|


 <a name="departments"></a>Afdelingen
------------

Een afdeling is een operationele eenheid die een categorie of functioneel gebied van een organisatie vertegenwoordigt die verantwoordelijk is voor een bepaald gebied van de organisatie, zoals verkoop of boekhouding. Een afdeling wordt gebruikt voor rapportage over functionele gebieden en kan verantwoordelijk zijn voor winsten en verliezen. Een afdeling kan ook een groep van kostenplaatsen bevatten. Verkoop, boekhouding en human resources zijn enkele voorbeelden van afdelingen in een organisatie.

## <a name="jobs-and-positions"></a>Taken en functies
Een taak is een verzameling taken en verantwoordelijkheden die vereist zijn voor iedere persoon die een taak uitvoert. Een positie is een afzonderlijk exemplaar van een taak. Verantwoordelijkheidsgebieden, taken, functies, vaardigheden, opleidingsinformatie en certificaten die vereist zijn voor een taak, zijn ook vereist voor posities die gekoppeld zijn aan een taak.
### <a name="job-tasks"></a>Functietaken

U kunt taken maken die de basistaken beschrijven die een werknemer in een positie voor die taak moet uitvoeren. Dezelfde taak kan worden toegevoegd aan meerdere taken, en posities voor die taken nemen die taken over. In de volgende tabel staan voorbeelden van taken.

<table>
<thead>
<tr class="header">
<th>Functie</th>
<th>Functietaak</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Verkoopmanager</td>
<td><ul>
<li><span class="input">Perf-revisie</span> – Bekijk de prestaties van elke verkoper.</li>
<li><span class="input">Abs-review</span> – Verlofaanvragen of registraties van elke verkoper goedkeuren of weigeren.</li>
</ul></td>
</tr>
<tr class="even">
<td>Accountant</td>
<td><span class="input">FIN-Rapport</span> – Wekelijks financiële rapporten presenteren aan de chief financial officer.</td>
</tr>
</tbody>
</table>

### <a name="job-functions"></a>Taakfuncties

Functies zijn vergelijkbaar met taken. Een taakfunctie beschrijft een of meer taken, rechten of verantwoordelijkheden die aan een taak zijn toegewezen. Taakfuncties worden toegewezen aan taken en worden gebruikt voor het instellen en implementeren van geschiktheidsregels voor compensatieplannen. In de volgende tabel staan voorbeelden van taakfuncties.

| Functie           | Taakfunctie                                                |
|---------------|-------------------------------------------------------------|
| Verkoopmanager | Mng-mensen – Mensen beheren die aan u rapporteren.               |
| Accountant    | FIN-Revisie – Financiële gegevens beheren voor een set rekeningen. |

### <a name="job-types"></a>Taaktypen

Gebruik taaktypen om vergelijkbare taken in categorieën in te delen. Taaktypes worden net als taakfuncties toegewezen aan taken en worden gebruikt voor het instellen en implementeren van geschiktheidsregels voor compensatieplannen. De volgende lijst bevat enkele voorbeelden van taaktypes:
-   Voltijd
-   Deeltijd
-   Salaris
-   Uurloon

### <a name="areas-of-responsibility"></a>Verantwoordelijkheidsgebieden

Verantwoordelijkheidsgebieden gebruiken om aan te geven voor welke werkrollen, processen en producten een werknemer in een positie voor die taak verantwoordelijk is. Een voorbeeld van een verantwoordelijkheidsgebied voor een taak met de titel 'Boekhouder' is mogelijk 'Financiële rapportering voor Product A'.

<a name="positions"></a>Posities
----------

Posities zijn een belangrijk element van het lagere niveau van een organisatiehiërarchie. Een positie is een afzonderlijk exemplaar van een taak. De positie 'Verkoopmanager (Oost)' is bijvoorbeeld maar een van de posities die is gekoppeld aan de taak 'Verkoopmanager'. Posities komen voor in een afdeling en worden aan werknemers toegewezen.
### <a name="position-creation-and-maintenance"></a>Maken en onderhouden van posities

-   U kunt een historie bekijken van wijzigingen in het systeem met betrekking tot de positie in een gemakkelijk toegankelijke lijstpagina.
-   U kunt redencodes maken die uw gebruikers kunnen selecteren wanneer ze posities maken of wijzigen.
-   U kunt actietypen voor personeel maken en een nummerreeks aan personeelacties toewijzen.
-   U kunt een werkstroom instellen zodat het toevoegen en wijzigen van posities goedkeuring kan vereisen.

### <a name="position-duration"></a>Positieduur

Elke positie heeft een periode waarbinnen die positie van kracht is. Deze periode wordt duur genoemd. Zomerposities kunnen bijvoorbeeld duren van 1 mei 2015 tot en met 31 augustus 2015.

### <a name="worker-assignments"></a>Medewerkerstoewijzingen

Als u een werknemer aan een positie toewijst, vult u die positie in. U kunt medewerkers toewijzen aan meerdere posities, maar slechts één werknemer kan tegelijkertijd aan een positie worden toegewezen.

### <a name="reporting-relationships"></a>Rapportagerelaties

Posities zijn belangrijke elementen van het lagere niveau van een organisatiehiërarchie. In het formulier Positie kunt u de positie opgeven waaraan een positie rapporteert. Wanneer u een werknemer toewijst aan een positie die aan een andere positie rapporteert, maakt u een rapporteringsrelatie tussen de werknemers die zijn toegewezen aan de twee posities. 'Boekhouder A' rapporteert bijvoorbeeld aan de positie "Supervisor boekhouding". Kim Akers is toegewezen aan de positie "Supervisor boekhouding" en Sanjay Patel is toegewezen aan de positie "Boekhouder A". Dit betekent dat Sanjay Patel rapporteert aan Kim Akers. 

Als uw organisatie gebruikmaakt van een matrixhiërarchie of een andere aangepaste hiërarchie, kunt u positiehiërarchietypen instellen en vervolgens rapporteringsrelaties toevoegen aan posities voor elke hiërarchie die u hebt ingesteld. Lori Penor is bijvoorbeeld een algemeen manager bij Adventure Works en is toegewezen aan de positie 'Algemeen manager '. Lori beheert de ontwikkeling van een product dat wordt gebruikt voor het reinigen van widgets. Lori wil dat een boekhouder haar helpt met de financiën voor de ontwikkeling van het product. Daarom heeft ze Sanjay Patel als haar boekhouder aangeworven. Sanjay rapporteert rechtstreeks aan Kim Akers, maar werkt ook met Lori Penor met betrekking tot de financiën voor de ontwikkeling van de widgetreiniger. 

In het vorige voorbeeld zou u de volgende taken voltooien voor het instellen van de werkrelatie tussen Sanjay Patel en Lori Penor:
1.  Maak een aangepast positiehiërarchietype genaamd "Widget" om een hiërarchie te maken die posities bevat die verantwoordelijk zijn voor het werken aan de widgetreiniger.
2.  Wijs de positie van Algemeen manager toe aan de positie waaraan de positie van Boekhouder A rapporteert in de hiërarchie Widget.

Gebruik de positiehiërarchie de rapporteringsstructuur van posities weer te geven. Als u meerdere positiehiërarchieën hebt, kunt u de hiërarchie voor elk hiërarchietype weergeven in de positiehiërarchie. U kunt ook een positie zoeken via positie-id of de naam van de werknemer die aan de positie is toegewezen. De positiehiërarchie is een organisatiehiërarchie.

## <a name="date-effective-records"></a>Ingangsdatumrecords
Voor sommige records, kunt u toekomstige wijzigingen aan de record opgeven. De volgende informatie heeft een ingangsdatum.

<table>
<thead>
<tr class="header">
<th>Records</th>
<th>Informatie met ingangsdatum</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Taken</td>
<td><ul>
<li>Gedetailleerde taakinformatie</li>
<li>Classificatie van taakgegevens</li>
<li>Compensatiegegevens</li>
</ul></td>
</tr>
<tr class="even">
<td>Posities</td>
<td><ul>
<li>Gedetailleerde positie-informatie</li>
<li>Werknemertoewijzingen</li>
<li>Positieduren</li>
<li>Functiehiërarchieën</li>
</ul></td>
</tr>
</tbody>
</table>

U kunt de gegevens vermeld in de vorige tabel wijzigen voor een functie of een taak en een datum opgeven waarop de wijzigingen in de positie of de taak moeten ingaan. Een positie kan bijvoorbeeld alleen worden toegewezen aan één werknemer, maar Sanjay Patel, die is toegewezen aan de positie Boekhouder A, vertrekt binnen twee weken. Joe Healy vervangt Sanjay Patel wanneer hij vertrekt. Hoewel Sanjay nog steeds aan zijn positie is toegewezen, kunt u Joe Healy zo toewijzen aan dezelfde positie dat de toewijzing slechts ingaat na de laatste dag van Sanjay.





