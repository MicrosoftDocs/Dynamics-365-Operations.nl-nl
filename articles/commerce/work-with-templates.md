---
title: Werken met sjablonen
description: In dit onderwerp wordt beschreven hoe u werkt met sjablonen in Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f4ed3b6797127113450949aa957437125f37394f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995711"
---
# <a name="work-with-templates"></a>Werken met sjablonen


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u werkt met sjablonen in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Zoals wordt besproken in [Overzicht sjablonen en indelingen](templates-layouts-overview.md), wordt met sjablonen de set opties bepaald die beschikbaar zijn voor auteurs. Sjablonen zijn om verschillende redenen nuttig voor het webontwerpteam van een onderneming. Goed gestructureerde sjablonen helpen bij alle volgende doelstellingen:

- De ontwerpfunctionaliteit voor het dagelijks werk van inhoudseditors vereenvoudigen.

    - Filteren van moduleopties zodat alleen de relevante modules worden weergegeven voor een bepaalde paginasectie. (Een marketingsectie van een sjabloon kan bijvoorbeeld worden geconfigureerd voor het uitfilteren van irrelevante modules die nooit in die context mogen worden gebruikt en die de taken voor het ontwerpen van inhoud complex maken als ze worden weergegeven.)
    - Standaard module-instelling configureren om de ontwerpefficiëntie te helpen verbeteren.
    - Standaard paginafragmenten definiëren om efficiënter te kunnen ontwerpen. (Bijvoorbeeld: kop- en voettekstfragmenten in een sjabloon worden automatisch op elke downstreampagina weergegeven.)

- Zorgen dat bedrijfssites de merkrichtlijnen volgen door een goedgekeurde set indelings- en configuratieopties te definiëren voor modules.

    > [!TIP] 
    > Succesvolle e-commercesites bieden klanten een gebruikservaring (UX) met vertrouwde, herhaalbare en merkconforme ontwerppatronen. Met behulp van sjablonen kunt u de consistentie op de hele site beheren.

- Verbeter de optimalisatiescores van de zoekmachine (SEO) met herhaalde en programmatisch gedefinieerde paginadefinities en metagegevens.

> [!NOTE]
> Hoewel sjablonen zijn ontworpen om de consistentie over een site te beheren, kunnen ze in theorie zo worden geconfigureerd dat ze geen consistentie afdwingen. Merk- en sitebeheerders kunnen elk niveau van variabiliteit definiëren voor de pagina's op de site. Een sjabloon kan bijvoorbeeld geheel open blijven, zodat inhoudontwerpers elk gewenst paginaontwerp kunnen maken. In dit geval zijn geen van de voordelen in de bovenstaande lijst van toepassing.

## <a name="modify-a-template"></a>Een sjabloon wijzigen

Sjablonen worden gewijzigd met de sjablooneditor.

Voer een van de volgende stappen uit om de sjablooneditor te openen:

- Selecteer in het navigatievenster van uw site de optie **Sjablonen** en selecteer vervolgens de sjabloon die u wilt wijzigen.
- Selecteer in de pagina-editor voor een bestaande pagina het bovenste knooppunt in de overzichtsstructuur aan de linkerkant. Selecteer vervolgens in het eigenschappenvenster aan de rechterkant de optie **Sjabloon bewerken**.

In de overzichtsweergave links worden de moduleopties en structuren weergegeven die beschikbaar zijn voor onderliggende indelingen en pagina's. Wanneer u een module selecteert in de overzichtsstructuur, kunt u de sjablooneigenschappen voor de geselecteerde module weergeven in het eigenschappenvenster rechts. Sommige van deze eigenschappen zijn uniek voor het bewerken van sjablonen. Deze eigenschappen worden in de onderstaande tabel beschreven.

| Naam van eigenschap. | Beschrijving |
|---|---|
| Min. voorvallen | Met deze eigenschap wordt het minimumaantal exemplaren voor de geselecteerde module gedefinieerd. Als de waarde bijvoorbeeld is ingesteld op **1**, is de module vereist voor auteurs van onderdelen. Als de waarde is ingesteld op **0** (nul), is de module optioneel. |
| Max. voorvallen | Met deze eigenschap wordt het maximumaantal exemplaren voor de geselecteerde module gedefinieerd. Als de waarde bijvoorbeeld is ingesteld op **1**, kan de module slechts één keer worden toegevoegd. |
| Min. modules (Containers) | Voor modules die andere modules bevatten (*container* modules), definieert u met deze eigenschap het minimumaantal modules dat als onderliggende elementen moet worden toegevoegd. Voor een carrouselmodule kan de waarde bijvoorbeeld worden ingesteld op een getal dat groter is dan 1. |
| Max. modules (Containers) | Voor containermodules definieert u met deze eigenschap het maximumaantal modules dat als onderliggende elementen moet worden toegevoegd. Voor een carrouselmodule kan de waarde bijvoorbeeld worden ingesteld op een getal dat kleiner is dan 10. |
| Vergrendeld | Naast alle eigenschappen van de basismodule wordt een **vergrendeld** Boolean-besturingselement weergegeven. Hiermee kan de sjabloonauteur een module-instelling in de sjabloon vergrendelen. Een module-instelling die vergrendeld is, kan niet worden overschreven door onderliggende indelingen of pagina's. Het wordt een centraal bewerkbare eigenschapswaarde voor alle indelingen en pagina's die de sjabloon gebruiken. |

## <a name="create-a-new-template"></a>Een nieuwe sjabloon maken

Volg deze stappen om een nieuwe sjabloon te maken.

1. Selecteer in het navigatievenster van uw site de optie **Sjablonen** om het sjablooncontrolevenster te openen.
1. Selecteer **Nieuwe sjabloon**.
1. Voer in het dialoogvenster voor het maken van sjablonen een naam en een beschrijving in voor de sjabloon. De waarden die u invoert, worden weergegeven voor auteurs die nieuwe pagina's maken. Voer daarom metagegevens in die nuttig zijn voor auteurs van de pagina. Voer bijvoorbeeld **Deze sjabloon gebruiken om algemene marketingpagina's te maken** in als omschrijving. Deze metagegevens kunnen later worden bewerkt.
1. Klik op **OK** om de nieuwe sjabloon te maken en de sjablooneditor te openen. In de sjablooneditor wordt links een overzichtsstructuur weergegeven en aan de rechterkant een eigenschappenvenster.
1. Vouw in de overzichtsstructuur de knooppunten uit en selecteer het vak **HTML-kop**.
1. Als dit vak nog geen modules bevat, selecteert u de knop met het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de optie **Standaard paginaoverzicht** en selecteer vervolgens **OK**.
1. Selecteer in de overzichtsstructuur de nieuwe module en voer vervolgens in het eigenschappenvenster alle standaardinstellingen in die automatisch moeten worden geconfigureerd voor alle onderliggende pagina's van de sjabloon. Als u geen standaardinstellingen wilt instellen, laat u de waarden leeg.
1. Selecteer in de overzichtsstructuur het vak **Hoofdtekst**, selecteer de knop met het weglatingsteken en vervolgens **Module toevoegen**.
1. Selecteer een paginacontainermodule (er kan slechts één optie zijn) en selecteer vervolgens **OK**.

Onder de containermodule voor nieuwe pagina's wordt een nieuwe set met vakken (**kop**, **hoofd**, enzovoort) weergegeven. Hier kunt u de moduleopties toevoegen en configureren die beschikbaar zijn voor auteurs wanneer ze pagina's maken op basis van deze sjabloon. Als u geen modules aan een vak toevoegt, worden standaard alle beschikbare moduletypen voor dat vak ondersteund.

De sjabloon is nu geldig en kan worden opgeslagen, ingecheckt en gebruikt om nieuwe pagina's te maken. In de volgende drie secties worden echter enkele andere standaardinstellingen beschreven die u mogelijk eerst wilt configureren.

## <a name="add-a-header-and-a-footer"></a>Een kop- en voettekst toevoegen

Als uw site al een koptekstfragment heeft, voert u de volgende stappen uit om een koptekst en een voettekst aan een sjabloon toe te voegen.

1. Vouw in de overzichtsstructuur het vak met de **hoofdtekst** en de onderliggende paginamodule uit.
1. Selecteer het vak **Kop**.
1. Selecteer de knop met het weglatingsteken voor het vak **Kop** en selecteer **Fragment toevoegen**.
1. Zoek en selecteer het koptekstfragment van de site en selecteer vervolgens **OK**.

Alle pagina's die de sjabloon gebruiken zullen dit koptekstfragment nu automatisch overnemen.

Zie [Een fragment maken](work-with-fragments.md#create-a-fragment) voor informatie over het maken van de site en het uitvoeren van de vorige procedure als de site nog geen koptekstfragment heeft.

## <a name="change-the-template-theme"></a>Het sjabloonthema wijzigen

Voer de volgende stappen uit om het standaardthema in te stellen voor alle pagina's met een sjabloon.

1. Vouw in de overzichtsstructuur aan de linkerkant het vak met de **hoofdtekst** uit.
1. Selecteer in het vak met de **hoofdtekst** de paginacontainermodule (bijvoorbeeld **standaardpagina**).
1. Selecteer in het eigenschappenvenster aan de rechterkant een thema in het veld **Thema**.

Standaard wordt op alle nieuwe pagina's het geselecteerde thema gebruikt. Als u wilt voorkomen dat deze instelling door pagina's wordt overschreven op indelings- of paginaniveau, steltu het **vergrendelde** Boolean-besturingselement in op **True**.

## <a name="add-a-script-to-a-template"></a>Een script aan een sjabloon toevoegen

U kunt HTML-**&lt;script&gt;**-elementen die JavaScript bevatten, aan uw sjabloon toevoegen. Op deze manier kunt u het standaardscriptgedrag bepalen voor de secties HTML-kop, begin en einde hoofdtekst van de pagina's.

Om een script aan een sjabloon toe te voegen, volgt u deze stappen.

1. Selecteer in de overzichtsstructuur aan de linkerkant het vak waaraan u het **&lt;script&gt;**-element wilt toevoegen (bijvoorbeeld HTML-kop, begin of einde van hoofdtekst).
1. Selecteer de knop met het weglatingsteken voor het vak en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** een scriptmodule (bijvoorbeeld **extern script** of **inline script**).
1. Voer in het eigenschappenvenster aan de rechterkant in het desbetreffende besturingselement voor de scripteigenschap (bijvoorbeeld **inline script** of **scriptcodes**) het script in.
1. Voer in het eigenschappenvenster de overige optionele instellingen in die u wilt configureren.

> [!TIP]
> Als u scriptmodules opnieuw wilt gebruiken voor andere sjablonen, kunt u deze converteren naar fragmenten. Op deze manier zorgt u ervoor dat het ontwerpproces efficiënter verloopt en kunt u het updateproces centraliseren. Zie [Een bestaande moduleconfiguratie als fragment opslaan](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment) voor informatie over het converteren van een scriptmodule naar een fragment.

## <a name="save-check-in-preview-and-publish-a-template"></a>Een sjabloon opslaan, inchecken, vooraf bekijken en publiceren

Om een sjabloon op te slaan en in te checken, volgt u deze stappen.

1. Selecteer de optie **Opslaan** boven aan de sjablooneditor. Opgeslagen wijzigingen zijn niet van invloed op vervolgpagina's totdat ze zijn ingecheckt.
1. Selecteer **Bewerken voltooien**. Uw wijzigingen zijn nu detecteerbaar voor vervolgworkflows.

Als u de wijzigingen wilt bekijken, opent u een bestaande pagina die de sjabloon gebruikt of maakt u een nieuwe pagina op basis van de sjabloon.

Nadat u een voorbeeld van de wijzigingen in de sjabloon hebt bekeken, volgt u een van deze stappen om de sjabloon naar uw live site te publiceren:

* Ga naar **Sjablonen**, selecteer de sjabloon en selecteer **Publiceren.**
* Selecteer de indelingsnaam om de indelingseditor te openen en selecteer vervolgens **Publiceren**.
* Publiceer een pagina die verwijst naar de niet-gepubliceerde sjabloon. De sjabloon wordt automatisch gepubliceerd.

> [!WARNING]
> Wanneer een sjabloon of een ander CMS-item (Content Management System) wordt gepubliceerd, kan dit op internet worden gedetecteerd. Publiceer geen documenten of elementen totdat u klaar bent om deze openbaar te maken. Documentversies die zijn opgeslagen en ingecheckt maar nog niet zijn gepubliceerd, kunnen alleen worden gedetecteerd door geverifieerde systeemgebruikers.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht sjablonen en indelingen](templates-layouts-overview.md)

[Werken met vooraf ingestelde indelingen](work-with-layouts.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]