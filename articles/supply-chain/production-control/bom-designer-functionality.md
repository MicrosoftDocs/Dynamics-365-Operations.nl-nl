---
title: Functionaliteit van stuklijstontwikkelaar
description: In dit onderwerp wordt beschreven hoe u de pagina Stuklijstontwikkelaar kunt gebruiken om stuklijststructuren te ontwerpen en te gebruiken.
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesigner
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 20981
ms.assetid: 2b92eec1-d28c-4965-9086-939c77b3c62b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b7d4530ecccf18d9370d84ff2b61be1514b80192
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="bom-designer-functionality"></a>Functionaliteit van stuklijstontwikkelaar

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u de pagina Stuklijstontwikkelaar kunt gebruiken om stuklijststructuren te ontwerpen en te gebruiken. U kunt op Instellingen klikken om verschillende configuraties te selecteren en te selecteren welke informatie wordt weergegeven op de regels van de structuur.

Wanneer u de pagina **Stuklijstontwikkelaar** vanaf de pagina **Vrijgegeven producten** opent, ziet u de hiërarchie van stuklijsten (BOM's) die actief en goedgekeurd zijn voor het geselecteerde artikel, de standaardordersite van het artikel en de werkelijke datum.  

Klik op **Filter** om de oorspronkelijke selectie in de weergave te wijzigen. Door het weergaveprincipe in te stellen op **Geselecteerd/Actief of Geselecteerd**, kunt u afzondelrijke stuklijst- of routeversies selecteren om in de weergave te gebruiken. U kunt niet-goedgekeurde en inactieve stuklijstversies selecteren om in de stuklijstontwerper weer te geven of te beheren.  

**Opmerking:** Als u de stuklijstontwikkelaar opent vanaf de lijstpagina **Stuklijsten**, worden geen routegegevens weergegeven. Momenteel is de selectie van een stuklijst of routeversie een eigenschap van de stuklijst en routeversie en geldt deze voor alle exemplaren van de stuklijstontwikkelaar.  

In de volgende secties wordt de functionaliteit beschreven die op de verschillende tabbladen van de stuklijstontwikkelaar beschikbaar is.

## <a name="analyzing-a-bom-structure-by-using-the-bom-designer"></a>Een stuklijststructuur analyseren met de stuklijstontwikkelaar
De stuklijstontwerper heeft twee secties:

-   De structuurweergave van de stuklijststructuur.
-   De sectie Details waarin details van de geselecteerde gegevens worden weergegeven. Als u een knooppunt in de structuurweergave selecteert, worden de Sneltabbladen in de sectie Details bijgewerkt op basis van dat knooppunt:
    -   **Regeldetails van stuklijst** - Geeft de details weer van de stuklijstregel die in de structuurweergave is geselecteerd.
    -   **Artikelgegevens** - Geeft de details weer van het belangrijkste artikel of het artikel dat in het geselecteerde knooppunt wordt gebruikt. U kunt op **Vrijgegeven product bewerken** klikken om het geselecteerde artikel te onderhouden.
    -   **Stuklijst** - Geeft de koptekst van de stuklijst weer die aan het geselecteerde knooppunt is gekoppeld.
    -   **Route** - Geeft de koptekst van de route weer die aan het geselecteerde knooppunt is gekoppeld.
    -   **Routebewerkingen** - Geeft een voorbeeld weer van de bewerkingen van de route. Wanneer een stuklijstregel wordt geselecteerd die aan een specifieke bewerking is toegewezen, wordt de bewerking gemarkeerd als **Component nodig bij bewerkingen**.

## <a name="selecting-a-bom-and-route"></a>Een stuklijst en route selecteren
Het filter dat voor de stuklijst en route wordt toegepast, wordt weergegeven in de koptekst van de stuklijstontwikkelaar. U kunt het filter wijzigen met het dialoogvenster **Filter**. In de volgende tabel worden de velden in dit dialoogvenster beschreven.

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
<td>Als het geselecteerde eindproduct een productmodel is, kunt u de actieve productdimensies voor de hoofdselectie definiëren. <strong>Opmerking:</strong> houd er rekening mee dat er geen productdimensies kunnen worden geselecteerd in het dialoogvenster <strong>Filter</strong> als u de stuklijstontwikkelaar opent voor een product dat geen productmodel is.</td>
</tr>
<tr class="even">
<td>Locatie</td>
<td>Wijzig de site waarvoor de stuklijststructuur wordt weergegeven. De standaardlocatie is de site van de standaardvoorraad van het voltooide artikel.</td>
</tr>
<tr class="odd">
<td>Weergaveprincipe</td>
<td>Selecteer het versieweergaveprincipe dat van toepassing is op de huidige stuklijststructuur en de huidige route:
<ul>
<li>Als het weergaveprincipe is ingesteld op <strong>Actief of Geselecteerd/Actief</strong>, wordt de geldige stuklijst of routeversie voor deze datum gevonden.</li>
<li>Als het principe is ingesteld op <strong>Geselecteerd/Actief of Geselecteerd</strong>, kunt u een stuklijstversie of routeversie selecteren door te klikken op <strong>Stuklijst</strong> &gt; <strong>Stuklijstversies</strong> of <strong>Route</strong> &gt; <strong>Routeversies</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Versiedatum</td>
<td>De versiedatum voor de stuklijst en route invoeren. De versie identificeert welke stuklijstversie wordt gebruikt op een specifieke datum, zoals is bepaald door de versiedatums in de stuklijstversie-instellingen.</td>
</tr>
<tr class="odd">
<td>Vanaf hoeveelheid</td>
<td>Filter de versies door een specifieke vanaf-hoeveelheid te selecteren. Als u een waarde instelt, worden mogelijk andere stuklijst- en routeversies geselecteerd.</td>
</tr>
<tr class="even">
<td>Alleen geldige weergeven</td>
<td>Wanneer u het selectievakje inschakelt, toont de boomstructuur alleen stuklijstregels met een geldige datum. Klik met de rechtermuisknop of dubbelklik op een stuklijstregel om de pagina <strong>Stuklijstregel bewerken</strong> te openen waar u de geldigheidsdatums voor die stuklijstregel vindt.</td>
</tr>
</tbody>
</table>

Wanneer u de stuklijstontwikkelaar gebruikt om stuklijsten te controleren of te bewerken die uit een of meerdere niveaus van phantoms bestaan, overspant de route die aan het hoogste artikel is gekoppeld meestal de volledige stuklijsthiërarchie. Als u het overzicht wilt vereenvoudigen, kunt u de route op het hoogste niveau in de weergave vergrendelen door te klikken op **Weergave** &gt; **Route vergrendelen**. Als u de route wilt ontgrendelen, klikt u op **Weergave** &gt; **Route ontgrendelen**.

## <a name="adding-and-editing-boms-and-bom-lines"></a>Stuklijsten en stuklijstregels toevoegen en bewerken
Gebruik de functies **Stuklijstregels** of **Stuklijst** om de stuklijstregels of stuklijst te wijzigen. Als u in de structuur een knooppunt selecteert, bepaalt het type van het knooppunt de functies die beschikbaar zijn.

| Functie                            | Omschrijving                                                                                               | Knooppunttype en voorwaarden                                                                                                                                                                                                                                                                       |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stuklijstregels &gt; Bewerken                 | Open een dialoogvenster waarin u de stuklijstregelkenmerken kunt bewerken.                                             | Deze functie is beschikbaar wanneer een stuklijstregelknooppunt is geselecteerd.                                                                                                                                                                                                                                   |
| Stuklijstregels &gt; Verwijderen               | Verwijder een stuklijstregel uit de geselecteerde stuklijst.                                                                  | Deze functie is alleen beschikbaar wanneer een stuklijstregelknooppunt is ingeschakeld en de stuklijst niet wordt vergrendeld voor bewerkingen.                                                                                                                                                                                             |
| Stuklijstregels &gt; Toevoegen vóór regel      | Open een dialoogvenster waarin u een productvariant kunt selecteren dat u vóór de geselecteerde stuklijstregel wilt invoegen.         | Deze functie is beschikbaar wanneer een stuklijstregelknooppunt is geselecteerd.                                                                                                                                                                                                                                   |
| Stuklijstregels &gt; Toevoegen aan componentstuklijst | Open een dialoogvenster waarin u een productvariant kunt selecteren dat u op het einde van de geselecteerde stuklijst wilt invoegen.       | Deze functie is beschikbaar wanneer het geselecteerde knooppunt een geselecteerde stuklijst heeft. Als deze functie niet beschikbaar is, ontbreekt er mogelijk een stuklijstversie voor de geselecteerde artikelvariant. In dit geval kunt u op **Stuklijst** &gt; **Versie maken** klikken om de ontbrekende versie voor het geselecteerde knooppunt te maken. |
| Stuklijstregels &gt; Toevoegen na regel       | Open een dialoogvenster waarin u een productvariant kunt selecteren dat u na de geselecteerde stuklijstregel wilt invoegen.          | Deze functie is beschikbaar wanneer een stuklijstregelknooppunt is geselecteerd.                                                                                                                                                                                                                                   |
| Stuklijst &gt; Versie maken             | Maak een nieuwe stuklijstversie of stuklijst voor de productvariant van het geselecteerde knooppunt.                             | Deze functie is beschikbaar wanneer het geselecteerde stuklijstregelknooppunt is gekoppeld aan een artikel met producttype **Stuklijst** of **Formule**.                                                                                                                                                  |
| Stuklijst &gt; Berekening                | Open een dialoogvenster waarin u de berekening van kosten of verkoopprijs kunt uitvoeren voor de geselecteerde productvariant. | Deze functie is beschikbaar wanneer het geselecteerde knooppunt gekoppeld is aan een stuklijstversie.                                                                                                                                                                                                         |
| Stuklijst &gt; Controleren                      | Valideer en controleer de geselecteerde stuklijst.                                                                      | Deze functie is beschikbaar wanneer het geselecteerde knooppunt gekoppeld is aan een stuklijstversie.                                                                                                                                                                                                         |

## <a name="configuring-the-tree-view"></a>De structuurweergave configureren
Klik op **Instellingen** om de gegevens aan te passen die in de structuurweergave van de stuklijstontwikkelaar worden weergegeven.

| Veldgroep | Beschrijving                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stuklijst         | Gebruik de selectievakjes om de criteria te selecteren die in de boomstructuur worden weergegeven. In de stuklijstontwikkelaar worden de geselecteerde criteria onder aan beide tabbladen weergegeven. |
| route       | Gebruik de selectievakjes om de criteria te selecteren die voor de routes worden weergegeven.                                                                                    |






