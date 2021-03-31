---
title: Werken met modules
description: In dit onderwerp wordt beschreven hoe en wanneer u modules in Microsoft Dynamics 365 Commerce gebruikt.
author: phinneyridge
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: eddee09fa81c18bc464b7768921981e6b5159a3e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210894"
---
# <a name="work-with-modules"></a>Werken met modules

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe en wanneer u modules in Microsoft Dynamics 365 Commerce gebruikt.

## <a name="overview"></a>Overzicht

Modules zijn logische bouwstenen die de paginastructuur vormen en verschillende doeleinden en bereiken hebben. Sommige modules zijn containers op een hoog niveau en zijn alleen bedoeld voor het vasthouden en organiseren van andere modules (onderliggende modules). Andere modules, zoals een eenvoudige afbeeldingsmodule, hebben een specifiek doel. Modules, zoals carrouselmodules, vallen ergens tussen deze twee categorieën.

Standaard bevat uw Dynamics 365 Commerce-site een bibliotheekmodule waarmee u de meeste elementaire e-commerce-scenario's kunt realiseren. U kunt een complete e-commerce-site samenstellen met behulp van deze modules. U kunt deze modules echter ook aanpassen of nieuwe aangepaste modules maken voor specifieke behoeften. Als u aangepaste modules wilt maken, is er een module-ontwerp-SDK (Software Development Kit) beschikbaar om u te helpen bij het maken van een aangepaste modulebibliotheek.

## <a name="container-modules-and-slots"></a>Containermodules en vakken

Zoals eerder is vermeld, bevatten sommige modules onderliggende modules. Deze modules worden *containers* genoemd en kunnen hiërarchieën van geneste modules bevatten. Containermodules bevatten *vakken*. Vakken worden gebruikt om de indeling en het doel van onderliggende modules in de container te verwerken. Een voorbeeld is een containermodule voor een basispagina (een module op het hoogste niveau voor een willekeurige pagina) waarin verschillende belangrijke vakken worden gedefinieerd:

- Een koptekstvak
- Een subkoptekstvak
- Een hoofdvak
- Een voettekstvak
- Een subvoettekstvak

De ontwikkelaar van de module definieert deze vakken en bepaalt welke onderliggende modules en hoeveel onderliggende modules direct in de module kunnen worden geplaatst. Het koptekstvak kan bijvoorbeeld slechts één module van het type **koptekstmodule** ondersteunen, terwijl het vak voor de hoofdtekst een onbeperkt aantal modules van elk type kan ondersteunen (behalve andere containermodules).

In de ontwerphulpmiddelen hoeven de auteurs van de pagina niet van tevoren te weten welke modules in elk vak kunnen worden geplaatst. Wanneer de auteur van een pagina een vak selecteert en een module wil selecteren om hieraan toe te voegen, wordt een gefilterde weergave van de moduletypen getoond die voor die sleuf worden ondersteund.

## <a name="content-modules"></a>Inhoudsmodules

Inhoudsmodules bevatten inhoud en media-elementen, zoals tekst (bijvoorbeeld koppen, alinea's en koppelingen) of activaverwijzingen (bijvoorbeeld afbeeldingen, video en PDF's). Standaardinhoudsmoduletypen zijn onder andere modules voor informatieblokken, tekstblokken en speciale acties. Modules van deze drie typen kunnen tekst of media bevatten, en vereisen geen onderliggende modules om iets zichtbaar te maken op een pagina.

Bij de meeste standaard dagelijkse activiteiten voor pagina's en inhoud zijn inhoudsmodules betrokken, voornamelijk omdat deze modules de feitelijke inhoud definiëren die wordt weergegeven in de bovenliggende containermodules. Er zijn veel inhoudsmodules beschikbaar die doorgaans de laatste onderdelen zijn die u aan de hiërarchie van geneste modules van de pagina toevoegt.

In de volgende afbeelding wordt aangegeven hoe modules worden genest binnen bovenliggende containermodulevakken.

![Modules nesten](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Modules toevoegen of verwijderen

In de volgende procedures wordt beschreven hoe u modules toevoegt en verwijdert.

### <a name="add-a-module"></a>Een module toevoegen

Voer deze stappen uit om een vak of een container aan een pagina toe te voegen.

1. Selecteer in het overzichtsvenster links of rechtstreeks op het hoofdtekenpapier een container of vak waaraan een onderliggende module kan worden toegevoegd.

    > [!NOTE]
    > De moduleontwerper definieert de lijst met moduletypen die aan een bepaald modulevak kunnen worden toegevoegd. Sjabloonschrijvers kunnen de toegestane moduleopties vervolgens verfijnen om een consistente SEO-werking (Search Engine Optimization) te garanderen en een efficiënt ontwerp voor alle pagina's die op basis van een bepaalde sjabloon worden gemaakt. Wanneer een module aan een vak wordt toegevoegd, wordt het dialoogvenster **Module toevoegen** automatisch gefilterd, zodat alleen modules worden weergegeven die in de geselecteerde container of het geselecteerde vak worden ondersteund. De lijst met toegestane modules wordt bepaald door de sjabloon van de pagina of door de moduledefinitie van de container.

1. Als u het overzichtsvenster gebruikt, selecteert u het weglatingsteken (**...**) naast de modulenaam en selecteert u **Module toevoegen**. Als u de besturingselementen direct binnen het tekenpapier gebruikt, selecteert u het plussymbool (**+**) in een leeg vak of naast de huidige geselecteerde module en selecteert u vervolgens **Module toevoegen**.

    > [!NOTE]
    > Als nieuwe onderliggende modules niet door een container of vak worden ondersteund, is de optie **Module toevoegen** niet beschikbaar.

1. Selecteer in het dialoogvenster **Module toevoegen** een module die u aan de pagina wilt toevoegen.

    > [!TIP]
    > **Inhoudsblok** is een goed type module waarmee beginners kunnen werken.

1. Klik op **OK** om de geselecteerde module toe te voegen aan de geselecteerde container of het vak op de pagina.

### <a name="remove-a-module"></a>Een module verwijderen

Voer deze stappen uit om een module uit een vak of een container op een pagina te verwijderen.

1. Selecteer in het overzichtsvenster aan de linkerkant het weglatingsteken (**...**) naast de naam van de module die u wilt verwijderen en selecteer vervolgens de knop Prullenbak. U kunt ook op het hoofdtekenpapier de prullenbak selecteren op de werkbalk van een geselecteerde module.
1. Wanneer u wordt gevraagd te bevestigen dat u de module wilt verwijderen, selecteert u **OK**.

## <a name="move-a-module-to-a-new-position"></a>Een module naar een nieuwe positie verplaatsen

Gebruik een van de volgende methoden om een module naar een nieuwe positie binnen uw pagina te verplaatsen.

### <a name="move-a-module-using-the-outline-pane"></a>Een module verplaatsen met behulp van het overzichtsvenster

Voer de volgende stappen uit om een module te verplaatsen met behulp van het overzichtsvenster.

1. Selecteer en houd de module die u wilt verplaatsen vast in het overzichtsvenster en sleep de module naar een nieuwe positie in het overzicht. De blauwe regel in het overzicht en op het tekenpapier geeft aan waar de module kan worden geplaatst.
1. Laat de module los om deze op de nieuwe positie neer te zetten.

### <a name="move-a-module-directly-within-the-canvas"></a>Een module rechtstreeks binnen het tekenpapier verplaatsen

Voer de volgende stappen uit om een module rechtstreeks binnen het tekenpapier te verplaatsen.

1. Selecteer de module die u wilt verplaatsen in het tekenpapier. 
1. Selecteer een pijl symbool omhoog of omlaag op de werkbalk van de module en sleep vervolgens de pijl naar een nieuwe positie op de pagina. De blauwe regel in het tekenpapier en overzicht geeft aan waar de module kan worden geplaatst. Als een module niet omhoog of omlaag kan worden verplaatst, wordt het pijl symbool grijs weergegeven. 
1. Laat de module los om deze op de nieuwe positie neer te zetten.

### <a name="move-a-module-using-the-ellipsis-menu"></a>Een module verplaatsen met behulp van het menu met het weglatingsteken

Voer de volgende stappen uit om een module te verplaatsen met behulp van het menu met het weglatingsteken.

1. Selecteer een module in het overzicht of op het tekenpapier.
1. Selecteer het weglatingsteken (**...**) naast de naam van de module in het overzichtsvenster of op de werkbalk van de module op het tekenpapier.
1. Als de module in de container of het vak omhoog of omlaag kan worden verplaatst, ziet u opties voor **Omhoog verplaatsen** of **Omlaag verplaatsen**. Selecteer de gewenste optie voor verplaatsen om de module omhoog of omlaag te verplaatsen ten opzichte van de items op hetzelfde niveau.

## <a name="configure-modules"></a>Modules configureren

In de volgende procedures wordt beschreven hoe u inhouds- en containermodules configureert.

### <a name="configure-a-content-module"></a>Een inhoudsmodule configureren

Voer de volgende stappen uit om een inhoudsmodule op een pagina te configureren.

1. Vouw in het overzichtsvenster aan de linkerkant de boomstructuur uit en selecteer een inhoudsmodule (bijvoorbeeld **Inhoudsblok**). Of selecteer de module die u wilt verplaatsen op het hoofdtekenpapier.
1. Voer in het deelvenster met module-eigenschappen rechts eigenschappen in voor de gewenste modulebesturingselementen.
1. Selecteer **Opslaan** op de opdrachtbalk. Hierdoor wordt ook het canvas met de voorbeeldweergave vernieuwd.

### <a name="edit-module-text-properties"></a>Eigenschappen van moduletekst bewerken

Moduleteksteigenschappen die niet alleen-lezen zijn, kunnen rechtstreeks op het tekenpapier worden bewerkt.

Voer de volgende stappen uit om de moduleteksteigenschappen te bewerken.

1. Selecteer het tekstbesturingselement op het tekenpapier en plaats vervolgens de cursor op de plaats waar u tekst wilt bewerken.
1. Voer uw tekstinhoud in.
1. Selecteer ergens buiten de tekst inhoud om verder te gaan met het bewerken van andere inhoud.

### <a name="inline-image-selection"></a>Inline afbeeldingen selecteren

Moduleafbeeldingen die niet alleen-lezen zijn, kunnen rechtstreeks vanaf het tekenpapier worden bewerkt.

Voer de volgende stappen uit om een nieuwe afbeelding te selecteren voor een inhoudsmodule.

1. Dubbelklik op het tekenpapier op de afbeelding. Hiermee wordt het venster mediakiezer weergeven.
1. Zoek en selecteer een nieuwe afbeelding die u wilt gebruiken en klik vervolgens op **OK**. De nieuwe afbeelding wordt nu op het tekenpapier weergegeven.

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



[!INCLUDE[footer-include](../includes/footer-banner.md)]