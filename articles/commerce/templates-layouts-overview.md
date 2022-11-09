---
title: Overzicht sjablonen en indelingen
description: In dit artikel worden sjablonen en indelingen in Microsoft Dynamics 365 Commerce besproken.
author: phinneyridge
ms.date: 10/26/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 0664dd1ae06d09557cf8b8ec58baf6d27c1198bd
ms.sourcegitcommit: 023ae5557e1351a8329a59a41a551e8901db99a8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/01/2022
ms.locfileid: "9733379"
---
# <a name="templates-and-layouts-overview"></a>Overzicht sjablonen en indelingen


[!include [banner](includes/banner.md)]

Sjablonen zijn een basiselement van het Microsoft Dynamics 365 Commerce-paginamodel. Als u de werkstromen voor site-ontwerpen doelmatiger en consistenter wilt maken, is het belangrijk dat u de voordelen van sjablonen voor uw website leer kennen. Vroege beslissingen over de sjabloonstructuur zijn belangrijk en kunnen grote invloed hebben op kosten en flexibiliteit voor merkupdates voor elke dag, per seizoen of voor de hele site. Goed gestructureerde sjablonen hebben ook andere voordelen. Ze helpen bijvoorbeeld bij het optimaliseren van de scores van de zoekmachine (SEO) voor de hele site en bij het beperken van het aantal fouten.

Een goede start voor het werken met sjablonen is inzicht krijgen in de functionele voordelen van sjablonen en indelingen, de verschillen tussen de sjablonen en de hiërarchie.

In de volgende afbeelding ziet u de paginamodelhiërarchie achter een weergegeven webpagina.

![Paginamodeldiagram.](../commerce/media/page-model-diagram.png)

| Entiteit        | Basisfunctie |
|---------------|----------------|
| Sjabloon      | Met sjablonen definieert u de moduleopties en de basisopzet voor een aantal indelingen en pagina-exemplaren. |
| Indeling        | Indelingen bepalen de definitieve selectie en de indeling van modules voor een pagina of een set pagina's. |
| Pagina-exemplaar | Paginaexemplaren definiëren de gegevens en inhoud voor specifieke pagina's. |

## <a name="templates"></a>Sjablonen

Sjablonen staan boven in de paginamodelhiërarchie in Dynamics 365 Commerce en vormen een belangrijke eerste stap voor de configuratie van de site. Met sjablonen kunt u de consistentie beheren in een reeks onderliggende indelingen en pagina's door de basisstructuur en ontwerpopties te definiëren voor het vervolgwerkstromen voor het maken van indelingen en pagina's. Met sjablonen kunt u het ontwerpproces voor creëren van inhoud vereenvoudigen met vooraf gedefinieerde, centraal beheerde elementen (zoals kop- en voetteksten) en geleide ontwerpstromen die garanderen dat de opties van de moduleconfiguratie merkconform zijn.

### <a name="controlling-consistency"></a>Consistentiebeheer

Wanneer u een sjabloon ontwerpt, betreft de belangrijkste zakelijke beslissing de controle die de sjabloon moet hebben over het proces van het maken van de pagina. Een sjabloon die alles open laat voor de volgende auteur, is het eenvoudigste type sjabloon, maar kan op de lange termijn gevolgen hebben voor het onderhoud van pagina's die op basis van deze sjabloon worden gemaakt. Een goed geschreven sjabloon biedt een richtlijn en een gestroomlijnde ontwerpervaring, maar biedt auteurs ook voldoende flexibiliteit om hun taak te voltooien. Al deze aspecten zijn afhankelijk van het controleniveau dat de sjabloon afdwingt.

Sjablonen kunnen auteurs van inhoud op de volgende manieren helpen efficiënter te zijn en het merk te volgen:

- Beperk de modules die kunnen worden gebruikt op een pagina.
- Stel standaardmodules en configuratie-instellingen voor.
- Maak een aantal module- en configuratie-opties die worden geregeld op sjabloonniveau. Dit proces wordt ook *vergrendelen* van een instelling genoemd.

In het volgende voorbeeld ziet u hoe een basissjabloon (sjabloon X) kan worden geconfigureerd:

- Alle onderliggende indelingen van sjabloon X moeten een koptekstcontainer, een hoofdcontainer en een voettekstcontainer bevatten.
- In de sjabloon X is de configuratie van de koptekstcontainer vergrendeld en kan deze alleen worden gewijzigd in sjabloon X zelf. Voor alle onderliggende indelingen en pagina's bestaat deze koptekst altijd.
- De hoofdcontainer vereist ten minste één module en maximaal tien modules. Deze modules worden gedefinieerd door vervolgindelingen en -pagina's.
- Voor de hoofdcontainer zijn de modules held, functie, carrousel en banner beschikbaar.
- Een voettekstcontainer wordt geconfigureerd in sjabloon X, maar kan worden overschreven door vervolgindelingen en -pagina's.

De sjabloon in dit voorbeeld definieert een eenvoudige structuur en een set opties voor auteurs van vervolginhoud. Sommige onderdelen van een pagina (in dit geval de koptekst) zijn volledig gedefinieerd en vergrendeld in de sjabloon en kunnen niet worden gewijzigd door vervolgauteurs. Andere delen (in dit geval de hoofdtekst) kunnen door vervolgauteurs binnen specifieke richtlijnen worden gedefinieerd (in dit geval een minimumaantal en maximumaantal modules van specifieke typen). En andere onderdelen (in dit geval de voettekst) worden gedefinieerd in de sjabloon, maar kunnen worden overschreven door vervolgauteurs.

Een belangrijke stap voor locatie- en merkbeheerders is het bepalen van het juiste evenwicht tussen beperking en flexibiliteit voor onderliggende indelingen en auteurs van pagina's. Wanneer u sjablonen gebruikt, is deze balans volledig configureerbaar. Het bepaalt of pagina-elementen centraal worden bijgewerkt (vergrendeld in de sjabloon) of op afzonderlijke onderliggende niveaus die lager in de paginahiërarchie staan.

### <a name="relationship-between-template-defaults-and-page-content"></a>Relatie tussen standaardwaarden voor sjablonen en pagina-inhoud

De primaire functie van een sjabloon is het stroomlijnen van de ervaring van het maken van een module bij het maken van een pagina. Zelfs wanneer de standaardinstellingen van de module in een sjabloon zijn ingesteld of zelfs vergrendeld, bestaat er geen gegevensverbinding meer vanuit de moduleconfiguraties van een pagina met de sjablooninstellingen, behalve wanneer de pagina wordt bewerkt. Sjablonen bepalen de ontwerpervaring voor de paginastructuur. Nadat een pagina is gemaakt, zijn de standaardsjabloonwaarden niet langer gekoppeld aan de lokaliseerbare inhoud op die pagina. Met andere woorden, de standaardinstellingen van de module die zijn ingesteld in een sjabloon bepalen de ontwerpervaring voor onderliggende pagina's. Ze hebben geen controle over de inhoud op die pagina's nadat de pagina's zijn gemaakt en bewerkt.

De enige uitzondering op het eerder beschreven gedrag treedt op wanneer een [fragment](work-with-fragments.md) aan een sjabloon wordt toegevoegd. U kunt fragmenten gebruiken om op elk moment dynamisch lokaliseerbare inhoud toe te voegen aan of te bewerken op de onderliggende pagina's van een sjabloon of indeling, zelfs nadat een groot aantal pagina's is gemaakt op basis van een bepaalde sjabloon. Het is aan te raden om fragmenten in sjablonen en indelingen te gebruiken wanneer lokaliseerbare inhoud dynamisch moet worden toegevoegd, verwijderd of bewerkt voor alle onderliggende pagina's. U moet bijvoorbeeld fragmenten gebruiken voor kopteksten, voetteksten, algemene metagegevens/scripts of andere inhoud die centraal bewerkbaar moet zijn en hetzelfde moet zijn op alle onderliggende pagina's. Met fragmenten kunt u de inhoud van alle onderliggende pagina's beheren via sjablonen en indelingen.

Zie [Werken met sjablonen](work-with-templates.md) als u sjablonen wilt gaan gebruiken.

## <a name="layouts"></a>Indelingen

Indelingen zijn het volgende niveau in de paginamodelhiërarchie, onder sjablonen. Terwijl een sjabloon alle modules definieert die voor een pagina zijn toegestaan, bevat een indeling een expliciete selectie en indeling van modules. Pagina's zijn het volgende niveau in de paginamodelhiërarchie, onder indelingen. Ze definiëren de gelokaliseerde inhoud voor de modules die in de indeling zijn geselecteerd.

In het volgende voorbeeld wordt het sjabloonvoorbeeld uit de vorige sectie uitgebreid en ziet u hoe een basisindeling kan worden geconfigureerd:

- Voor de bovenliggende sjabloon van de indeling moet de hoofdcontainer tussen één en tien modules bevatten. Deze modules kunnen alleen held-, functie-, carrousel- en bannermodules zijn. In de indeling kunnen daarom de volgende selectie en indeling van modules worden gedefinieerd:

    - De eerste module in de hoofcontainer is een bannermodule die wordt gevolgd door een heldmodule en twee functiemodules.
    - De eerste functiemodule wordt links uitgelijnd en de tweede functiemodule wordt rechts uitgelijnd.

- Hoewel een standaard voettekst wordt overgenomen van de bovenliggende sjabloon, heeft de sjabloonauteur de voettekst ontgrendeld gelaten. Daarom kan de indeling deze overschrijven door een ander voettekstfragment te definiëren.

De indeling in dit voorbeeld bepaalt de definitieve indeling van modules voor onderliggende pagina's. Net als een sjabloon kan een indeling standaard of vergrendelde module-eigenschappen definiëren die altijd worden overgenomen door onderliggende pagina's (bijvoorbeeld de uitlijning van de functiemodules). De werkelijke inhoud of gegevens voor elke module in de indeling wordt vervolgens verder omlaag in de hiërarchie gedefinieerd in elk onderliggend pagina-exemplaar. Een belangrijk verschil is dat de indelingen niet direct lokaliseerbare inhoud bevatten, maar de onderliggende pagina's wel. De primaire functie van de indeling is het definiëren van de definitieve rangschikking en de standaardconfiguratie van modules voor de onderliggende pagina's.

Deze hiërarchie is om twee redenen krachtig. In de eerste plaats worden indelingen met dezelfde bovenliggende sjabloon behandeld als compatibel voor scenario's met wisselende indelingen. Daardoor kan de indeling voor een pagina worden gewijzigd in een andere indeling van dezelfde sjabloonhiërarchie, zonder dat de inhoud van het paginaniveau opnieuw moet worden geschreven. U kunt gebruikmaken van deze mogelijkheid om seizoensgebonden ontwerpupdates uit te voeren, te experimenteren of een permanente site te ontwerpen. Ten tweede bieden indelingen een andere manier om gedeelde elementen centraal te wijzigen voor een groep pagina's zonder dat er updates zijn vereist voor afzonderlijke pagina's. Als een productcategorie bijvoorbeeld over 1.000 pagina's met dezelfde indeling beschikt, kunnen de modules opnieuw worden geordend in de indeling. Deze wijziging wordt direct doorgevoerd in alle 1.000 onderliggende pagina's.

Door inzicht te krijgen in deze hiërarchie kunt u een flexibele en efficiënte sitestructuur bieden die kosten bespaart, schaalbaar is en betere resultaten geeft wanneer de site in de loop van de tijd wordt uitgebreid.

### <a name="preset-and-custom-layouts"></a>Vooraf ingestelde en aangepaste indelingen

Indelingen op uw site kunnen *vooraf worden ingesteld* of worden *aangepast*:

- **Vooraf ingestelde** indelingen maken een werkstroom voor het maken van pagina's mogelijk waarbij alle modules al zijn geselecteerd en gerangschikt, en er is alleen gegevensinvoer vereist. Deze benadering bespaart tijd wanneer veel pagina's moeten worden geschreven met dezelfde indelingsvereisten. Vooraf ingestelde indelingen hebben een een-op-veel-relatie met de bijbehorende onderliggende pagina's. Daarom kan met één vooraf ingestelde indeling de modulerangschikking voor honderden of duizenden onderliggende pagina's centraal worden bepaald.
- **Aangepaste indelingen** zijn hoofdzakelijk indelingen voor eenmalig gebruik die op één pagina zijn ingesloten. Ze zijn niet beschikbaar als optie wanneer andere nieuwe pagina's worden gemaakt of in scenario's met wisselende indelingen. Het voordeel van deze benadering is dat een auteur kan experimenteren door een pagina met een aangepaste indeling te ontwerpen. Als de auteur vervolgens de indeling voor andere pagina's wil gebruiken, kan deze eenvoudig worden geconverteerd naar een vooraf ingestelde indeling. De nieuwe vooraf ingestelde indeling wordt vervolgens weergegeven als optie bij het maken van pagina's en in scenario's met wisselende indelingen voor pagina's uit dezelfde sjabloonhiërarchie. De vooraf gedefinieerde indelingen kunnen ook worden opgenomen in aangepaste indelingen. Op deze manier kan een auteur een pagina loskoppelen van de vooraf ingestelde indeling en een nieuwe aangepaste indeling voor eenmalig gebruik maken. (Deze nieuwe aangepaste indeling is nog steeds afhankelijk van eventuele beperkingen in de bovenliggende sjabloon.)

Vooraf gedefinieerde indelingen en aangepaste indelingen worden in verschillende delen van de ontwerpfunctieset bewerkt. Aangezien aangepaste indelingen geen afhankelijkheden hebben voor andere pagina's, worden ze rechtstreeks in de pagina-editor bewerkt. In dit geval is het bestaan van een indeling grotendeels transparant voor de gebruiker en wordt deze alleen weergegeven in de eigenschappen op paginaniveau en via de acties voor indelingsopties. Aangezien wijzigingen in vooraf ingestelde indelingen echter van invloed kunnen zijn op veel onderliggende pagina's, moeten ze worden bewerkt in de indelingseditor, waarbij de publicatieacties van invloed zijn op alle onderliggende pagina's.

In de volgende illustratie ziet u scenario's voor vooraf ingestelde en aangepaste indelingen.

![Vooraf ingestelde en aangepaste indelingsscenario's.](../commerce/media/template-figure1.png)

Zie [Werken met vooraf ingestelde indelingen](work-with-layouts.md) om vooraf gedefinieerde indelingen te gebruiken.

## <a name="additional-resources"></a>Aanvullende resources

[Werken met sjablonen](work-with-templates.md)

[Werken met vooraf ingestelde indelingen](work-with-layouts.md)

[Werken met publicatiegroepen](publish-groups.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
