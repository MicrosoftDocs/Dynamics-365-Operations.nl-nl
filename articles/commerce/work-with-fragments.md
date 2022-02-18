---
title: Werken met fragmenten
description: In dit onderwerp wordt beschreven waarom, wanneer en hoe u fragmenten gebruikt in Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 02/03/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 98cb1fba158ea99427d2068ca49b257cb5290de3
ms.sourcegitcommit: 1eef00796f7c5511f432b01800cdf8920992d7d5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2022
ms.locfileid: "8090739"
---
# <a name="work-with-fragments"></a>Werken met fragmenten 

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven waarom, wanneer en hoe u fragmenten gebruikt in Microsoft Dynamics 365 Commerce.

Fragmenten bieden een gecentraliseerde ontwerpervaring voor moduleconfiguraties die op de gehele site opnieuw moeten worden gebruikt. Kopteksten, voetteksten en banners worden vaak vaak als fragmenten geconfigureerd, omdat ze over meerdere pagina's worden gedeeld. U kunt fragmenten zien als miniatuurwebpagina's die in andere pagina's op uw site kunnen worden ingevoegd. Fragmenten hebben hun eigen levenscyclus. Met andere woorden ze worden in de ontwerphulpmiddelen als onafhankelijke entiteiten gemaakt, als verwijzing genoemd, bijgewerkt en verwijderd.

Nadat u fragmenten hebt geconfigureerd, kunt u deze gebruiken waar modules in uw sitestructuur kunnen worden gebruikt. U kunt naar fragmenten verwijzen via pagina's, in indelingen, in sjablonen en in andere fragmenten.

> [!NOTE]
> Fragmenten kunnen tot zeven niveaus diep in andere fragmenten worden genest.

Als u bijvoorbeeld een seizoensgebonden evenement wilt promoten op meerdere pagina's op onze site, kunt u een fragment gebruiken. De eerste stap bij het maken van een nieuw fragment is het selecteren van het type module waarin u wilt beginnen. Voor dit voorbeeld kunt u het fragment maken vanuit een heldmodule.

> [!NOTE]
> Fragmenten kunnen worden opgebouwd uit elk type module.

Vervolgens kunt u het heldfragment met uw specifieke promotie-inhoud configureren. U kunt het ook lokaliseren indien nodig. Het nieuwe zelfstandige heldfragment kan vervolgens worden gebruikt als een vooraf geconfigureerde module in de hele site. U kunt het eenvoudig toevoegen aan sjablonen, specifieke pagina's of andere fragmenten die heldmodules kunnen bevatten.

Alle plaatsen waar het fragment wordt toegevoegd, zijn verwijzingen naar het centrale heldfragment dat u hebt gemaakt. Als u wijzigingen in het fragment publiceert, worden deze wijzigingen direct doorgevoerd op alle plaatsen binnen de site waar naar het fragment wordt verwezen. Hierdoor beschikken fragmenten over een krachtige en efficiënte manier om moduleconfiguraties op een site te hergebruiken en centraal te beheren. Door ze effectief te gebruiken, kunt u de flexibiliteit aanzienlijk verhogen en de kosten voor het beheren van de inhoud van de site verminderen.

In de volgende afbeelding ziet u hoe fragmenten kunnen worden gebruikt om het ontwerpen van gedeelde moduleconfiguraties op een e-commerce-site te centraliseren.

![In de afbeelding ziet u hoe fragmenten kunnen worden gebruikt om het ontwerpen van gedeelde moduleconfiguraties op een e-commerce-site te centraliseren.](./media/fragment-figure1.png)

## <a name="create-a-fragment"></a>Een fragment maken

U kunt een nieuw fragment maken of een bestaande moduleconfiguratie als fragment opslaan.

### <a name="save-an-existing-module-configuration-as-a-fragment"></a>Een bestaande module configuratie als fragment opslaan

Voer de volgende stappen uit om een eerder geconfigureerde module te converteren naar een herbruikbaar fragment in Commerce Site Builder.

1. Open een pagina of sjabloon die de module bevat die u naar een fragment wilt converteren.
1. Selecteer de eerder geconfigureerde module in het overzichtsvenster links of rechtstreeks in de visuele paginabouwer.
1. Selecteer het beletselteken (**...**) naast de naam van de module in het overzichtsvenster of op de werkbalk van de geselecteerde module in visuele paginabouwer. 
1. Selecteer **Delen als fragment**. 
1. Voer in het dialoogvenster **Fragment opslaan als** een naam voor het fragment in.
1. Selecteer **OK** om de moduleconfiguratie op te slaan als een fragment dat aan andere pagina's kan worden toegevoegd.
<!-- The following image shows how to save a module configuration as a fragment.-->
<!--![A screen capture of how to save a module configuration as a fragment.](./media/save-as-fragment.png)-->

### <a name="create-a-new-fragment"></a>Een nieuw fragment maken

Voer de volgende stappen uit om een nieuw fragment te maken in Commerce Site Builder.

1. Selecteer **Fragmenten** in het navigatievenster aan de linkerkant.
1. Selecteer **Nieuw**. Het dialoogvenster **Nieuw fragment** verschijnt waarin alle beschikbare moduletypen worden weergegeven. Zoals eerder is vermeld, kunnen fragmenten vanuit elk type module worden gemaakt.
1. Selecteer een moduletype voor het fragment.

<!-- The following image shows where to create a new fragment.-->
<!-- ![A screen capture of where to create a new fragment.](./media/fragment-nav-menu.png)-->
> [!TIP]
> Selecteer een algemeen containermoduletype voor de meeste flexibiliteit wanneer u het fragment later moet bijwerken en configureren.

## <a name="add-remove-or-edit-fragments-on-a-page"></a>Fragmenten op een pagina toevoegen, verwijderen of bewerken

In de volgende procedures wordt beschreven hoe u fragmenten toevoegt en verwijdert.

### <a name="add-a-fragment"></a>Een fragment toevoegen

Voer de volgende stappen uit om een fragment aan een pagina toe te voegen in Commerce Site Builder.

1. Selecteer in het overzichtsvenster links of rechtstreeks in visuele paginabouwer een container of vak waaraan onderliggende modules kunnen worden toegevoegd.
1. Selecteer het weglatingsteken (**...**) naast de naam van de container of het vak.  Als alternatief kunt u, als u visuele paginabouwer gebruikt, het plusteken (**+**) selecteren.  
1. Selecteer **Fragment toevoegen**.
    <!-- ![A screen capture of how to add an existing fragment to a slot or container.](./media/add-fragment.png)-->
 
    > [!NOTE]
    > Als nieuwe onderliggende modules niet door de container of het vak worden ondersteund, is de optie **Fragment toevoegen** niet beschikbaar.
    
1. Zoek in het dialoogvenster **Fragment selecteren** een fragment dat u wilt toevoegen en selecteer het. Als er geen beschikbare fragmenten worden weergegeven, moet u mogelijk eerst een fragment maken van een moduletype dat door de geselecteerde container of of het geselecteerde vak wordt ondersteund.
1. Selecteer het gewenste fragment en voeg het toe aan de container of het vak op uw pagina.
<!--    ![A screen capture of the fragment picker modal window.](./media/fragment-picker.png)-->

> [!NOTE]
> De modules die in een container of vak zijn toegestaan, worden gedefinieerd door de paginasjabloon of de eigen definities van de modules.

### <a name="remove-a-fragment"></a>Een fragment verwijderen

Voer de volgende stappen uit om een fragment te verwijderen uit een vak of container op een pagina in Commerce Site Builder.

1. Selecteer in het overzichtsvenster aan de linkerkant het weglatingsteken (**...**) naast het fragment dat u wilt verwijderen en selecteer vervolgens de knop Prullenbak.  U kunt ook het fragment in visuele paginabouwer selecteren en het symbool Prullenbak op de werkbalk van de fragment selecteren.
1. Wanneer u wordt gevraagd te bevestigen dat u het fragment wilt verwijderen, selecteert u **OK**.

> [!NOTE]
> Wanneer u een fragment van een pagina verwijdert, verwijdert u alleen de verwijzing naar het fragment van die pagina. U verwijdert **niet** het fragment van uw site. Als u fragmenten van uw site wilt verwijderen, moet u de gebruikersinterface voor fragmentcontrole gebruiken. U kunt fragmenten alleen van een site verwijderen als er op dat moment niet door pagina's, sjablonen of andere fragmenten naar wordt verwezen.

### <a name="edit-a-fragment"></a>Een fragment bewerken

Als u fragmenten wilt bewerken, moet u de gebruikersinterface voor de fragmenteditor gebruiken. Dit is zo ontworpen. Hierdoor kunnen ontwerpers het proces van het bewerken van modules voor een bepaalde pagina niet verwarren met het proces voor het bewerken van fragmenten die op veel pagina's kunnen worden gedeeld.

Voer de volgende stappen uit om een fragment te bewerken in Commerce Site Builder.

1. Selecteer **Fragmenten** in het navigatievenster aan de linkerkant.
1. Selecteer onder **Fragmenten** het fragment dat u wilt bewerken.
1. Bewerk waar nodig de module-eigenschappen en de structuur van het fragment. Het proces lijkt op het proces voor het bewerken van modules in de pagina-editorweergave.

U kunt een fragment ook bewerken door het te selecteren op een pagina, in een sjabloon of in een bovenliggend fragment en vervolgens **Fragment bewerken** te selecteren in het deelvenster Eigenschappen aan de rechterkant.

### <a name="rename-a-fragment"></a>De naam van een fragment wijzigen

Voer de volgende stappen uit om de naam van een bestaand fragment te wijzigen in Site Builder.

1. Selecteer **Fragmenten** in het deelvenster voor navigatie aan de linkerkant.
1. Selecteer de naam van het fragment waarvan u de naam wilt wijzigen.
1. Selecteer **Bewerken** om het fragment te gaan bewerken. U kunt een fragment niet bewerken als iemand anders het fragment al aan het bewerken is.
1. Selecteer in het deelvenster met eigenschappen voor fragmenten het pensymbool naast de naam van het fragment.
1. Bewerk de naam van het fragment indien nodig.
1. Selecteer het vinkje om de naamswijziging te bevestigen.
1. Selecteer **Bewerken voltooien**.

U kunt de naam van een fragment wijzigen nadat het is gemaakt door het te bewerken en vervolgens het pensymbool naast de naam van het fragment in het eigenschappenvenster te selecteren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht sjablonen en indelingen](templates-layouts-overview.md)

[Werken met sjablonen](work-with-templates.md)

[Werken met vooraf ingestelde indelingen](work-with-layouts.md)

[Werken met publicatiegroepen](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
