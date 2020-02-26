---
title: Werken met modules
description: In dit onderwerp wordt beschreven hoe en wanneer u modules in Microsoft Dynamics 365 Commerce gebruikt.
author: v-chgri
manager: annbe
ms.date: 01/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 769d6754fa944830b989d657e0dad9cc42212932
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025874"
---
# <a name="work-with-modules"></a>Werken met modules

In dit onderwerp wordt beschreven hoe en wanneer u modules in Microsoft Dynamics 365 Commerce gebruikt.


[!include [banner](includes/banner.md)]

## <a name="overview"></a>Overzicht

Modules zijn logische bouwstenen die de paginastructuur vormen en verschillende doeleinden en bereiken hebben. Sommige modules zijn containers op een hoog niveau en zijn alleen bedoeld voor het vasthouden en organiseren van andere modules (onderliggende modules). Andere modules, zoals een eenvoudige afbeeldingsmodule, hebben een specifiek doel. Modules, zoals carrouselmodules, vallen ergens tussen deze twee categorieën.

Standaard bevat uw site Dynamics 365 Commerce een bibliotheekmodule uit het startpakket waarmee u de meeste elementaire e-commerce-scenario's kunt realiseren. U kunt een complete e-commerce-site samenstellen met behulp van deze modules. U kunt deze modules echter ook aanpassen of nieuwe aangepaste modules maken voor specifieke behoeften. Als u aangepaste modules wilt maken, is er een module-ontwerp-SDK (Software Development Kit) beschikbaar om u te helpen bij het maken van een aangepaste modulebibliotheek.

## <a name="container-modules-and-slots"></a>Containermodules en vakken

Zoals eerder is vermeld, bevatten sommige modules onderliggende modules. Deze modules worden *containers* genoemd en kunnen hiërarchieën van geneste modules bevatten. Containermodules bevatten *vakken*. Vakken worden gebruikt om de indeling en het doel van onderliggende modules in de container te verwerken. Een voorbeeld is een containermodule voor een basispagina (een module op het hoogste niveau voor een willekeurige pagina) waarin verschillende belangrijke vakken worden gedefinieerd:

- Een koptekstvak
- Een tekstvak
- Een voettekstvak

De ontwikkelaar van de module definieert deze vakken en bepaalt welke onderliggende modules en hoeveel onderliggende modules direct in de module kunnen worden geplaatst. Het koptekstvak kan bijvoorbeeld slechts één module van het type **koptekstmodule** ondersteunen, terwijl het vak voor de hoofdtekst een onbeperkt aantal modules van elk type kan ondersteunen (behalve andere containermodules).

In de ontwerphulpmiddelen hoeven de auteurs van de pagina niet van tevoren te weten welke modules in elk vak kunnen worden geplaatst. Wanneer de auteur van een pagina een vak selecteert en een module wil selecteren om hieraan toe te voegen, wordt een gefilterde weergave van de moduletypen getoond die voor die sleuf worden ondersteund.

## <a name="content-modules"></a>Inhoudsmodules

Inhoudsmodules bevatten inhoud en media-elementen, zoals tekst (bijvoorbeeld koppen, alinea's en koppelingen) of activaverwijzingen (bijvoorbeeld afbeeldingen, video en PDF's). Voorbeelden van typische inhoudsmodules zijn **held**, **functie** en **banner**. Modules van deze drie typen kunnen tekst of media bevatten, en vereisen geen onderliggende modules om iets zichtbaar te maken op een pagina.

Bij de meeste standaard dagelijkse activiteiten voor pagina's en inhoud zijn inhoudsmodules betrokken, voornamelijk omdat deze modules de feitelijke inhoud definiëren die wordt weergegeven in de bovenliggende containermodules. Er zijn veel inhoudsmodules beschikbaar die doorgaans de laatste onderdelen zijn die u aan de hiërarchie van geneste modules van de pagina toevoegt.

In de volgende afbeelding wordt aangegeven hoe modules worden genest binnen bovenliggende containermodulevakken.

![Modules nesten](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Modules toevoegen of verwijderen

In de volgende procedures wordt beschreven hoe u modules toevoegt en verwijdert.

### <a name="add-a-module"></a>Een module toevoegen

Voer deze stappen uit om een vak of een container aan een pagina toe te voegen.

1. Selecteer in het overzichtsvenster aan de linkerkant een container of een vak waaraan een onderliggende module kan worden toegevoegd.

    > [!NOTE]
    > De moduleontwerper definieert de lijst met moduletypen die aan een bepaald modulevak kunnen worden toegevoegd. Sjabloonontwerpers kunnen de toegestane moduleopties vervolgens verfijnen om een uniforme SEO-werking (Search Engine Optimization) te garanderen en een efficiënt ontwerp voor alle pagina's die op basis van een bepaalde sjabloon worden gebouwd.

1. Selecteer de knop met het weglatingsteken (**...**) voor de module en selecteer **Module toevoegen**. Het dialoogvenster **Module toevoegen** wordt weergegeven. Dit dialoogvenster wordt automatisch gefilterd, zodat alleen modules worden weergegeven die in de geselecteerde container of het geselecteerde vak worden ondersteund. De lijst met modules wordt bepaald door de sjabloon van de pagina of door de containermoduledefinitie.

    > [!NOTE]
    > Als nieuwe onderliggende modules niet door een container of vak worden ondersteund, is de optie **Module toevoegen** niet beschikbaar.

1. Zoek in het dialoogvenster en selecteer een module die u aan de pagina wilt toevoegen.

    > [!TIP]
    > **Functie** en **Held** zijn goede typen modules voor beginners.

1. Klik op **OK** om de geselecteerde module toe te voegen aan de geselecteerde container of het vak op de pagina.

### <a name="remove-a-module"></a>Een module verwijderen

Voer deze stappen uit om een module uit een vak of een container op een pagina te verwijderen.

1. Selecteer in het overzichtsvenster aan de linkerkant de knop met het weglatingsteken naast de naam van de module die u wilt verwijderen en selecteer vervolgens de knop Prullenbak.
1. Wanneer u wordt gevraagd te bevestigen dat u de module wilt verwijderen, selecteert u **OK**.

## <a name="configure-modules"></a>Modules configureren

In de volgende procedures wordt beschreven hoe u inhouds- en containermodules configureert.

### <a name="configure-a-content-module"></a>Een inhoudsmodule configureren

Voer de volgende stappen uit om een inhoudsmodule op een pagina te configureren.

1. Vouw in het overzichtsvenster aan de linkerkant de boomstructuur uit en selecteer een van de inhoudsmodules (bijvoorbeeld **Functie**, **Held** of **Banner**).
1. Zoek in het eigenschappenvenster aan de rechterkant de inhoud en instellingen van de module.
1. Geef waar nodig eigenschappen op voor besturingselementen van de module.
1. Selecteer **Opslaan** op de opdrachtbalk. Hierdoor wordt ook het canvas met de voorbeeldweergave vernieuwd.

### <a name="configure-a-container-module"></a>Een containermodule configureren

Voer de volgende stappen uit om een containermodule op een pagina te configureren.

1. Selecteer een containermodule op de pagina (bijvoorbeeld een carrousel of een vloeibare containermodule).
1. Vouw in het deelvenster Eigenschappen rechts de geneste besturingselementen uit door de kopteksten te selecteren en stel de vereiste waarden voor besturingselementen in.
1. Selecteer in het overzichtsvenster aan de linkerkant de knop met het weglatingsteken naast de naam van de containermodule of van vakken in de container, en selecteer **Module toevoegen**. Voeg vervolgens onderliggende modules toe aan de geselecteerde container. Zie de sectie [Werken met modules](#add-a-module) eerder in dit onderwerp voor meer informatie.
1. Als er meerdere onderliggende modules op hetzelfde niveau zijn in een bovenliggende container, kunt u de weergavevolgorde in de bovenliggende container wijzigen. Selecteer de knop met het weglatingsteken voor een module en gebruik vervolgens de knoppen pijl-omhoog en pijl-omlaag.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht sjablonen en indelingen](templates-layouts-overview.md)

[Werken met sjablonen](work-with-templates.md)

[Werken met vooraf ingestelde indelingen](work-with-layouts.md)

[Werken met fragmenten](work-with-fragments.md)

[Een containermodule toevoegen aan een pagina](add-container-module.md)

[Werken met groepen publiceren](publish-groups.md)

