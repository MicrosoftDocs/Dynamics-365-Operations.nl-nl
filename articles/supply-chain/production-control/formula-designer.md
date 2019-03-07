---
title: Formuleontwerper
description: In dit onderwerp wordt uitgelegd hoe u met de formuleontwerper formules kunt analyseren en beheren in een boomstructuur.
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31a46230251be3a654092a4acc05a404533001b2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "348498"
---
# <a name="formula-designer"></a>Formuleontwerper

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u met de formuleontwerper formules kunt analyseren en beheren in een boomstructuur.

Bij het openen van de pagina **Formuleontwerper** via de pagina **Vrijgegeven producten** bevat de structuur in het linkerdeelvenster de lijst met coproducten en de hiërarchie van ingrediënten voor het vrijgegeven product. De structuur wordt afgeleid van de hiërarchie van formules die actief zijn en zijn goedgekeurd voor het geselecteerde artikel en de bijbehorende ingrediënten, de standaardorderlocatie van het artikel en de werkelijke datum.

Klik op **Instellingen** om verschillende configuraties te selecteren en op te geven welke informatie wordt weergegeven op de regels van de structuur.

Klik op **Filter** om de oorspronkelijke selectie in de weergave te wijzigen. Als u het weergaveprincipe instelt op **Geselecteerd/Actief** of **Geselecteerd**, kunt u afzonderlijke formule- of routeversies selecteren om in de weergave te gebruiken. U kunt niet-goedgekeurde en niet-actieve formuleversies selecteren om in de formuleontwerper weer te geven of te beheren.  

> [!NOTE]
> Als u de pagina **Formuleontwerper** opent vanaf de lijstpagina **Stuklijsten**, worden geen routegegevens weergegeven. Op dit moment is de selectie van een formule- of routeversie van toepassing op alle exemplaren van de formuleontwerper.  

In de volgende gedeelten wordt de functionaliteit beschreven die in de stuklijstontwikkelaar beschikbaar is.

## <a name="analyze-a-formula-structure-by-using-the-formula-designer"></a>Een formulestructuur analyseren met behulp van de formuleontwerper
De formuleontwerper heeft twee secties:

-   De structuurweergave van de formulestructuur.
-   De sectie Details waarin details van de geselecteerde gegevens worden weergegeven. Als u een knooppunt in de structuurweergave selecteert, worden de Sneltabbladen in de sectie Details bijgewerkt op basis van dat knooppunt:
    -   **Details formuleregel**: geef de details weer van de formuleregel die in de structuurweergave is geselecteerd.
    -   **Artikelgegevens**: geef de details weer van het hoofdartikel of het artikel dat in het geselecteerde knooppunt wordt gebruikt. U kunt op **Vrijgegeven product bewerken** klikken om het geselecteerde artikel te onderhouden.
    -   **Formule**: geef de koptekst van de formule weer die aan het geselecteerde knooppunt is gekoppeld.
    -   **Route**: geef de koptekst van de route weer die aan het geselecteerde knooppunt is gekoppeld.
    -   **Routebewerkingen**: geef een voorbeeld weer van de bewerkingen van de route. Wanneer een stuklijstregel wordt geselecteerd die aan een specifieke bewerking is toegewezen, wordt de bewerking gemarkeerd als **Component nodig bij bewerkingen**.

## <a name="select-a-formula-and-route"></a>Een formule en route selecteren
Het filter dat voor de formule en route wordt toegepast, wordt weergegeven in de koptekst van de formuleontwerper. U kunt het filter wijzigen met het dialoogvenster **Filter**. In de volgende tabel worden de velden in dit dialoogvenster beschreven.

<table>
<thead>
<tr class="header">
<th>Veld</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Productdimensies</td>
<td>Als het geselecteerde eindproduct een productmodel is, kunt u de actieve productdimensies voor de hoofdselectie definiëren. Houd er rekening mee dat als u de formuleontwerper opent voor een product dat geen productmodel is, er geen productdimensies kunnen worden geselecteerd in het dialoogvenster <strong>Filter</strong>.</p></td>
</tr>
<tr class="even">
<td>Vestiging</td>
<td>Wijzig de locatie waarvoor de ingrediëntstructuur wordt weergegeven. De standaardlocatie is de site van de standaardvoorraad van het voltooide artikel.</td>
</tr>
<tr class="odd">
<td>Weergaveprincipe</td>
<td><p>Selecteer het versieweergaveprincipe dat van toepassing is op de huidige formulestructuur en de huidige route:</p>
<ul>
<li>Als het weergaveprincipe is ingesteld op <strong>Actief</strong> of <strong>Geselecteerd/Actief</strong>, wordt de geldige formule of routeversie voor deze datum gevonden.</li>
<li>Als het principe is ingesteld op <strong>Geselecteerd/Actief</strong> of <strong>Geselecteerd</strong>, kunt u een formuleversie of routeversie selecteren door te klikken op <strong>Formule</strong> &gt; <strong>Formuleversies</strong> of <strong>Route</strong> &gt; <strong>Routeversies</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Versiedatum</td>
<td>Geef de versiedatum op voor de formule en route. Met de versie wordt aangegeven welke formuleversie wordt gebruikt op een specifieke datum, op basis van de versiedatums in de formuleversie-instellingen.</td>
</tr>
<tr class="odd">
<td>Vanaf hoeveelheid</td>
<td>Filter de versies door een specifieke &quot;vanaf&quot;-hoeveelheid te selecteren. Als u een waarde instelt, worden mogelijk andere formule- en routeversies geselecteerd.</td>
</tr>
<tr class="even">
<td>Alleen geldige weergeven</td>
<td>Wanneer u het selectievakje inschakelt, toont de boomstructuur alleen formuleregels met een geldige datum. Klik met de rechtermuisknop of dubbelklik op een formuleregel om de pagina <strong>Formuleregel bewerken</strong> te openen waar u de geldigheidsdatums voor die formuleregel vindt.</td>
</tr>
</tbody>
</table>

Wanneer u de formuleontwerper gebruikt om formules te controleren of te bewerken die uit een of meerdere niveaus van phantoms bestaan, overspant de route die aan het hoogste artikel is gekoppeld meestal de volledige formulehiërarchie. Als u het overzicht wilt vereenvoudigen, kunt u de route op het hoogste niveau in de weergave vergrendelen door te klikken op **Weergave** &gt; **Route vergrendelen**. Als u de route wilt ontgrendelen, klikt u op **Weergave** &gt; **Route ontgrendelen**.

## <a name="add-and-edit-formulas-and-formula-lines"></a>Formules en formuleregels toevoegen en bewerken
Gebruik de functies **Stuklijstregels** of **Formule** om de formuleregels of formule te wijzigen. Als u in de structuur een knooppunt selecteert, bepaalt het type van het knooppunt de functies die beschikbaar zijn.

| Functie                            | Omschrijving                                                                                               | Knooppunttype en voorwaarden |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|--------------------------|
| Stuklijstregels &gt; Bewerken                 | Open een dialoogvenster waarin u de formuleregelkenmerken kunt bewerken.                                         | Deze functie is beschikbaar wanneer een formuleregelknooppunt is geselecteerd. |
| Stuklijstregels &gt; Verwijderen               | Een formuleregel uit de geselecteerde formule verwijderen.                                                          | Deze functie is beschikbaar wanneer een formuleregelknooppunt is ingeschakeld en de formule niet wordt vergrendeld voor bewerkingen. |
| Stuklijstregels &gt; Toevoegen vóór regel      | Open een dialoogvenster waarin u een productvariant kunt selecteren dat u vóór de geselecteerde formuleregel wilt invoegen.     | Deze functie is beschikbaar wanneer een formuleregelknooppunt is geselecteerd. |
| Stuklijstregels &gt; Toevoegen aan componentstuklijst | Open een dialoogvenster waarin u een productvariant kunt selecteren dat u aan het einde van de geselecteerde formule wilt invoegen.   | Deze functie is beschikbaar wanneer het geselecteerde knooppunt een geselecteerde formule heeft. Als deze functie niet beschikbaar is, ontbreekt er mogelijk een formuleversie voor de geselecteerde artikelvariant. In dit geval kunt u op **Formule** &gt; **Versie maken** klikken om de ontbrekende versie voor het geselecteerde knooppunt te maken. |
| Stuklijstregels &gt; Toevoegen na regel       | Open een dialoogvenster waarin u een productvariant kunt selecteren dat u na de geselecteerde formuleregel wilt invoegen.      | Deze functie is beschikbaar wanneer een formuleregelknooppunt is geselecteerd. |
| Formule &gt; Versie maken         | Maak een nieuwe formuleversie of formule voor de productvariant van het geselecteerde knooppunt.                     | Deze functie is beschikbaar wanneer het geselecteerde formuleregelknooppunt is gekoppeld aan een artikel met producttype **Stuklijst** of **Formule**. |
| Formule &gt; Berekening            | Open een dialoogvenster waarin u de berekening van kosten of verkoopprijs kunt uitvoeren voor de geselecteerde productvariant. | Deze functie is beschikbaar wanneer het geselecteerde knooppunt gekoppeld is aan een formuleversie. |
| Formule &gt; Controleren                  | De geselecteerde formule valideren en controleren.                                                                  | Deze functie is beschikbaar wanneer het geselecteerde knooppunt gekoppeld is aan een formuleversie. |

## <a name="configuring-the-tree-view"></a>De structuurweergave configureren
Klik op **Instellingen** om de gegevens aan te passen die in de structuurweergave van de formuleontwerper worden weergegeven.


| Veldgroep |                                                                          Omschrijving                                                                          |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Stuklijst     | Gebruik de selectievakjes om de criteria te selecteren die in de boomstructuur worden weergegeven. In de formuleontwerper worden de geselecteerde criteria onder aan de tabbladen weergegeven. |
|    route    |                                           Gebruik de selectievakjes om de criteria te selecteren die voor de routes worden weergegeven.                                           |

