---
title: Handleiding voor lokalisatie van Dynamics 365 Commerce e-commerce
description: In dit onderwerp wordt beschreven hoe u een Microsoft Dynamics 365 Commerce e-commercesite in extra talen kunt lokaliseren en de site kunt configureren om meerdere kanalen te ondersteunen.
author: bicyclingfool
ms.date: 04/29/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1e9d91036ceeb9161dc8ee903532b2cf3ca435e2
ms.sourcegitcommit: 26c726bd0b00935e3d2c31fdc5a3b2ae03a8a2b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661523"
---
# <a name="dynamics-365-commerce-e-commerce-localization-guide"></a>Handleiding voor lokalisatie van Dynamics 365 Commerce e-commerce

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een Microsoft Dynamics 365 Commerce e-commercesite in extra talen kunt vertalen en de site kunt configureren voor ondersteuning van meerdere kanalen. Daarnaast worden de concepten en terminologie met betrekking tot het proces beschreven.

De e-commercemogelijkheden in Dynamics 365 Commerce zijn ontworpen met het oog op online-ervaringen die kunnen worden aangepast aan bepaalde landen/regio's en talen, terwijl sjablonen, pagina's, inhoud en media tegelijkertijd maximaal kunnen worden hergebruikt. U kunt ook een basissite maken en deze vervolgens uitbreiden naar nieuwe markten door in de loop der tijd ondersteuning voor extra landen/regio's en talen toe te voegen.

## <a name="definitions"></a>Definities

**Landinstellingen, landinstellingen-id**: de landinstellingen (ook wel landinstellingen-id genoemd) geven een taal aan die aan een land of regio is gekoppeld. De landinstellingen-id 'fr-ca' is bijvoorbeeld gekoppeld aan Canadees Frans.

**Basistaal**: de taal waarin u de site-inhoud ontwikkelt voordat u deze exporteert voor lokalisatie.

**Kanaal, online winkel**: een kanaal (ook wel een online winkel genoemd) definieert de betalingsmethoden, prijsgroepen, producthiërarchieën, assortimenten en producten voor een online e-commercewinkel.

## <a name="concepts"></a>Concepten

### <a name="url-driven-experience"></a>URL-gestuurde ervaring

Dynamics 365 Commerce e-commercesites bieden unieke marktgerichte en gelokaliseerde ervaringen voor klanten via kanalen en landinstellingen-id's. Met kanalen worden de unieke producten, categorieën, valuta's en betalingsmethoden voor een markt bepaald. De landinstellingen-id bepaalt de taal van de inhoud die klanten zien. Een e-commercesite gebruikt URL's om onderscheid te maken tussen marktgerichte en gelokaliseerde ervaringen. Site-URL's voor deze unieke ervaringen voor kanalen en landinstellingen worden voor een site gedefinieerd op de pagina **Site-instellingen \> Kanalen** in de Dynamics 365 Commerce Site Builder.

In Site Builder is een URL een combinatie van een domein en een pad dat het invoerpunt definieert voor een unieke combinatie van een kanaal en de landinstelling. In het volgende voorbeeld worden door een fictieve online winkel met de naam Fabrikam Inc. vier unieke combinaties van een kanaal en een landinstelling gedefinieerd en wordt elke combinatie toegewezen aan een unieke URL die inhoud aan klanten biedt.

| Domein                     |  Pad      | Afzetkanaal       |   Landinstelling     |
|------------------------|--------|--------------------------------|--------|
| `https://fabrikam.com` | /      | Uitgebreide online winkel Fabrikam | nl  |
| `https://fabrikam.com` | /es    | Uitgebreide online winkel Fabrikam | es     |
| `https://fabrikam.ca`  | /      | Contoso online winkel    | fr-ca  |
| `https://fabrikam.ca`  | /en-ca | Contoso online winkel    | en-ca  |

#### <a name="domain"></a>Domein

Domeinen worden tot stand gebracht bij het instellen van uw e-commercesite in Microsoft Dynamics Lifecycle Services (LCS). Nadat uw e-commerceomgeving is ingericht, kunt u meer domeinen toevoegen door een serviceaanvraag te openen. Meer informatie over het instellen van domeinen voor uw e-commercesite vindt u in [Domeinen in Dynamics 365 Commerce](domains-commerce.md).

#### <a name="path"></a>Pad

- Een pad is een willekeurige tekenreeks die, in combinatie met het domein, wordt toegewezen aan een unieke combinatie van een kanaal en een landinstelling. In het voorgaande voorbeeld komt de tekenreeks die wordt gebruikt als het pad, overeen met de landinstellingen-id waaraan het pad is toegewezen. U kunt echter een andere benadering gebruiken.
- Een combinatie van een kanaal en een landinstelling kan worden toegewezen aan een domein en een leeg pad ("/"). In het voorgaande voorbeeld zien klanten die `https://fabrikam.ca/` bezoeken de producten en het assortiment voor de Canadese markt in Canadees Frans.
- Commerce Site Builder voorkomt dat u dubbele combinaties van een domein en een pad maakt. U kunt echter dubbele combinaties van een kanaal en een landinstelling toewijzen aan een andere combinatie van een domein en een pad.

#### <a name="channel"></a>Afzetkanaal

- Kanalen (ook wel online winkels genoemd) definiëren de betalingsmethoden, prijsgroepen, producthiërarchieën, assortimenten en producten voor een online e-commercewinkel.
- Kanalen worden in het Dynamics 365 Commerce-hoofdkantoor gedefinieerd, geconfigureerd en gepubliceerd.
- Site Builder kan de online winkels detecteren die zijn geconfigureerd in Commerce Headquarters en die kunnen worden toegewezen aan een site.

Zie [Overzicht van kanalen](channels-overview.md) voor meer informatie over kanalen. Zie [Een onlinekanaal instellen](channel-setup-online.md) voor meer informatie over het instellen van een onlinekanaal.

#### <a name="locale"></a>Landinstelling

- De landinstelling is de werkelijke id die wordt gebruikt wanneer u XLIFF-bestanden (XML Localization Interchange File Format) aanlevert voor lokalisatie. Landinstellingen worden voor elk kanaal in Commerce Headquarters gedefinieerd en gepubliceerd. Zie het volgende onderdeel voor informatie over het configureren van talen en kanalen in Site Builder.
- Dezelfde landinstellingen kunnen aan meerdere kanalen worden toegewezen. Op deze manier kan een gemeenschappelijke taal worden aangeboden op meerdere markten.

## <a name="configure-languages-and-channels-for-your-e-commerce-site"></a>Talen en kanalen configureren voor uw e-commercesite

Standaard worden alle e-commercesites in Dynamics 365 Commerce geconfigureerd om één online kanaal en één taal te gebruiken, ongeacht of u met de demosite Fabrikam begint of zelf een nieuwe site maakt.

In deze configuratie ontwikkelen klanten en partners meestal alle onderdelen die worden gebruikt voor de verschillende landen/regio's en talen. Deze onderdelen zijn sjablonen, pagina's, fragmenten, inhoud en media. Alle site-inhoud wordt ontwikkeld in de eerste taal die u voor uw site hebt geselecteerd. Of als u de Fabrikam-demosite gebruikt, wordt de inhoud in het Engels ontwikkeld.

![Standaard e-commercesite van Dynamics 365 Commerce](media/loc-guide-1.png)

> [!NOTE]
> U kunt de Fabrikam-demosite voor een extra taal configureren zodat de inhoud in die taal kan worden ontwikkeld. Zie het onderdeel [Een extra taal configureren voor uw site](#configure-an-additional-language-for-your-site) verderop in dit onderwerp voor informatie over het toevoegen van een nieuwe taal aan een site en kanaal.

Het contentmanagementsysteem (CMS) en het paginamodel voor de Dynamics 365 Commerce e-commercesites zijn echter ontworpen om uitbreiding naar nieuwe markten en landinstellingen mogelijk te maken. Daarom kunt u via één e-commercesite de onderdelen beheren voor een online winkel die meerdere markten en talen omvat.

![Dynamics 365 Commerce e-commercesite die meerdere markten en talen omvat](media/loc-guide-2.png)

### <a name="configure-an-additional-language-for-your-site"></a>Een extra taal voor uw site configureren

Het proces van het configureren van een nieuwe taal voor een e-commercesite omvat drie stappen.

#### <a name="step-1-add-the-language-to-your-channel-online-store-in-commerce-headquarters"></a>Stap 1: De taal toevoegen aan uw kanaal (online winkel) in Commerce Headquarters

1. Ga in Commerce Headquarters naar het kanaal waaraan u de nieuwe taal wilt toevoegen. Ga naar **Retail en Commerce \> Afzetkanalen \> Online winkels** om de lijst met kanalen te vinden die in Commerce Headquarters zijn geconfigureerd.
1. Open de online winkel openen die aan uw site is toegewezen door de waarde voor **Id van detailhandelafzetkanaal** te selecteren. U kunt de online winkel verifiëren die aan uw site is toegewezen door de pagina **Afzetkanalen** met site-instellingen te openen in Commerce Site Builder en naar de naam van de online winkel te kijken in de kolom **Afzetkanalen**. 
1. Selecteer op het sneltabblad **Talen** de optie **Toevoegen**. Selecteer in het veld **Taal** de landinstellingscode voor de nieuwe taal. Selecteer **Save**.
1. Ga naar **Retail en commerce \> Retail en commerce IT \> Distributieplanning** en voer taak **1070 Afzetkanaalconfiguratie** uit. Wanneer de taak is voltooid, kunt u verder gaan met stap 2 en de taal toevoegen aan een kanaal voor uw site in Site Builder.

![Sneltabblad Talen van een online winkel in Commerce Headquarters](media/loc-guide-3.png)

#### <a name="step-2-add-the-language-to-a-channel-in-site-builder"></a>Stap 2: De taal toevoegen aan een afzetkanaal in Site Builder

Voer de volgende stappen uit om een taal toe te voegen aan een kanaal in Site builder.

1. Open uw site in Commerce Site Builder en open vervolgens de pagina **Afzetkanalen** in de site-instellingen.
1. Selecteer de naam van het kanaal waaraan u de taal wilt toevoegen.
1. Selecteer **Een landinstelling toevoegen** in het rechterdeelvenster.
1. Selecteer in het dialoogvenster **Een landinstelling toevoegen** onder **Een landinstelling toevoegen** de landinstelling voor de taal die u eerder aan het afzetkanaal in Commerce Headquarters hebt toegevoegd.
1. Selecteer het domein en het pad dat klanten aanvragen om uw site weer te geven in dit kanaal en in deze taal.
1. Als u wilt dat de taal de standaardtaal is voor het weergeven, maken en bijwerken van pagina's en fragmenten van Site Builder, schakelt u het selectievakje **Gebruiken als standaardtaal voor kanaal voor schrijven**. 
    > [!NOTE]
    > Deze instelling is alleen van invloed op Site Builder. Dit heeft geen invloed op de ervaring met de gepubliceerde site voor uw klanten.
1. Selecteer **OK**.
1. Selecteer **Opslaan en publiceren**.

#### <a name="step-3-localize-your-site-content"></a>Stap 3: De inhoud van uw locatie lokaliseren

Wanneer u teruggaat naar de weergave **Pagina's** in Commerce Site Builder, is de nieuwe taal beschikbaar in het kanaal en de kiezer voor landinstellingen rechtsboven. U kunt nu lokale versies van pagina's maken in uw basistaal.

Het proces voor het lokaliseren van de inhoud van uw pagina's en fragmenten wordt besproken in de sectie [Inhoud van e-commercesite lokaliseren](#localize-e-commerce-site-content) later in dit onderwerp.

### <a name="configure-a-new-channel-for-your-site"></a>Een nieuw kanaal configureren voor uw site

E-commercesites in Dynamics 365 Commerce kunnen functies gebruiken die worden gedefinieerd via meerdere online kanalen die in Commerce Headquarters zijn geconfigureerd. Een site gebruikt meerdere kanalen om klanten een unieke configuratie van betalingsmethoden, prijsgroepen, producthiërarchieën, assortimenten en een reeks producten te laten zien. Een kanaal wordt doorgaans gebruikt om deze dimensies zo te configureren dat ze voldoen aan de vereisten en voorkeuren voor de ervaring die aan afzonderlijke landen/regio's is gekoppeld. Deze benadering is echter een zakelijke beslissing die de klant neemt. Het is geen vereiste.

De vereisten en taken die zijn gekoppeld aan het instellen van een afzetkanaal (online winkel) gaan verder dan het reikwijdte van dit document. Zie [Basisinformatie over het instellen van kanalen](channels-overview.md#channel-setup-basics) voor meer informatie over het instellen van een onlinekanaal in Commerce Headquarters. Zie [Een onlinekanaal instellen](channel-setup-online.md) voor informatie over de stappen en vereisten die specifiek zijn voor onlinekanalen.

Voer de volgende stappen uit om een kanaal toe te voegen aan uw site in Site builder.

1. Ga in Commerce Site Builder naar **Site-instellingen \> Afzetkanalen**. 
1. Selecteer **Een kanaal toevoegen**.
1. Selecteer in het dialoogvenster **Een kanaal toevoegen** onder **Kanaal** het kanaal dat u wilt toevoegen. 
    > [!NOTE]
    > U kunt alleen kanalen toevoegen die nog niet aan uw site zijn toegevoegd.
1. Selecteer de standaard landinstelling voor het kanaal. Als u nieuwe talen aan het kanaal toevoegt, kunt u de standaardtaal in een van deze talen wijzigen.
1. Geef het domein en het pad op voor de URL met de inhoud en de voorzieningen voor deze combinatie van kanaal en taal.
1. Selecteer **OK**.
1. Selecteer **Opslaan en publiceren**.

## <a name="localize-e-commerce-site-content"></a>Inhoud van e-commercesite lokaliseren

### <a name="xliff-basics"></a>XLIFF-basisprincipes

XLIFF is een industriestandaard bestandsindeling voor het doorgeven van lokalisatieinhoud tussen inhoudsbeheerprogramma's. Commerce Site Builder gebruikt de XLIFF-bestandsindeling om de inhoud van de pagina, het fragment en de metagegevens voor afbeeldingen te exporteren zodat deze kan worden gelokaliseerd en opnieuw kan worden weergegeven.

Microsoft Dynamics-klanten werken doorgaans met externe leveranciers, [zoals Translated.com](https://translated.com/welcome) om hun XLIFF-bestanden te vertalen in de talen die ze nodig hebben.

### <a name="localize-assets-in-site-builder"></a>Onderdelen in Site Builder lokaliseren

De volgende onderdelen voor de e-commercesites kunnen worden gelokaliseerd in Site Builder:

- Pagina's
- Fragmenten
- Mediaonderdelen
- Modules

Alle nieuwe pagina's, fragmenten en mediaonderdelen worden gemaakt in de context van het kanaal en de taal die momenteel zijn geselecteerd in de kiezer voor kanaal en landinstellingen. Deze taal is meestal uw basistaal, mits u nog geen extra talen of kanalen hebt geconfigureerd. Op sites waar meerdere kanalen en talen zijn geconfigureerd, wordt de 'basistaal' gedefinieerd door het kanaal en de landinstelling die u als standaardinstelling hebt ingesteld op de pagina **Kanalen** in site-instellingen.

De stappen voor het lokaliseren van inhoud voor pagina's, fragmenten en mediaonderdelen zijn vergelijkbaar. Uitzonderingen en verschillen worden aangegeven in de secties die daarop volgen. De stappen voor het lokaliseren van de inhoud van de module verschillen echter. Zie de sectie [Modules lokaliseren](#localize-modules), verderop in dit onderwerp voor meer informatie.

#### <a name="step-1-export-an-xliff-file"></a>Stap 1: Een XLIFF-bestand exporteren

Voer de volgende stappen uit om een een XLIFF-bestand te exporteren voor een pagina, fragment of afbeelding in Site builder.

1. Open het onderdeel dat u wilt exporteren, zodat het kan worden gelokaliseerd.
1. Selecteer **Lokalisatie \> XLIFF exporteren** op de opdrachtbalk.
    > [!NOTE]
    > De optie **Lokalisatie** is alleen zichtbaar als het onderdeel de status **Bewerken** heeft.

Een XLIFF -bestand met de naam **\<assetname\>.xlf** wordt gedownload naar de downloadmap van uw browser. Dit XLIFF-bestand is specifiek voor het onderdeel dat u gaat lokaliseren. U exporteert een XLIFF-bestand voor elk onderdeel dat u wilt lokaliseren.

#### <a name="step-2-localize-the-xliff-file"></a>Stap 2: Het XLIFF-bestand lokaliseren

In de meeste gevallen werkt u samen met een lokalisatievendor om uw XLIFF-bestanden te vertalen. Als u onderdelen echter intern gaat lokaliseren of als u alleen het lokalisatieproces wilt testen, moet u de volgende wijzigingen aanbrengen in een XLIFF-bestand:

- Voeg een doeltaalkenmerk toe aan het element /xliff/file en stel de waarde in op de landinstelling-id van de taal waarin u lokaliseert. 
    > [!NOTE]
    > Deze landinstelling-id moet overeenkomen met de landinstelling-id van de pagina **Kanalen** in site-instellingen.
- Voeg voor elk //source-element een doelelement toe waar de tekstwaarde de gelokaliseerde versie is van de inhoud van dat bronelement.

Zie de [XLIFF 1.2-specificatie](http://docs.oasis-open.org/xliff/xliff-core/xliff-core.html) voor informatie over het schema voor XLIFF-bestanden.

> [!NOTE]
> Als u onderdeel in meerdere talen wilt lokaliseren, moet u voor elk van deze talen een gelokaliseerd XLIFF-bestand maken.

#### <a name="step-3-import-the-localized-xliff-file"></a>Stap 3: Het gelokaliseerde XLIFF-bestand importeren

Als u een XLIFF-bestand voor een onderdeel wilt importeren, gaat u als volgt te werk.

1. Open in Commerce Site Builder het onderdelen waarvoor u een XLIFF-bestand wilt importeren.
1. Selecteer in de kiezer voor kanaal en landinstellingen rechtsboven het kanaal en de taal waarvoor u de gelokaliseerde inhoud importeert.
1. Selecteer **Lokalisatie \> XLIFF importeren** op de opdrachtbalk. Blader vervolgens naar het gelokaliseerde XLIFF-bestand voor het geselecteerde onderdeel en taal, en selecteer dit.

Nadat het XLIFF-bestand is geïmporteerd, wordt een variant van de pagina, het fragment of het onderdeel gemaakt. Vanaf dat punt hebben alle wijzigingen die in de gelokaliseerde variant worden aangebracht alleen invloed op die variant. Ze hebben geen invloed op het basisactivum waarvan de variant is afgeleid. Zo hebben wijzigingen in de basisactiva ook geen invloed op de variant van dat activum. 

Bij pagina's kunt u echter wijzigingen aanbrengen in varianten door de sjabloon of indeling te wijzigen waaraan deze pagina's zijn verbonden. Zo zijn wijzigingen in een fragment ook van invloed op alle pagina's die afhankelijk zijn van die variant.

### <a name="images"></a>Afbeeldingen

Afbeeldingen kunnen alleen in een pagina- of modulevariant worden weergegeven als de metagegevens van de inhoud die met deze afbeeldingen samenhangen, zijn gelokaliseerd. Op dit moment kunnen de volgende metagegevens in een mediaonderdeel worden gelokaliseerd:

- Alternatieve tekst
- Description
- Titel

Op dit moment kunt u het binaire bestand voor een digitaal onderdeel, zoals een afbeelding of een video, niet lokaliseren. Het Dynamics 365 Commerce-productteam werkt momenteel aan deze mogelijkheid.

### <a name="localize-modules"></a>Modules lokaliseren

Tekenreeksen die worden weergegeven als onderdeel van de module zelf (bijvoorbeeld 'Vorige' en 'Volgende' in een carrouselmodule) worden apart van de module-inhoud gelokaliseerd. Zie [Een module lokaliseren](e-commerce-extensibility/localize-module.md) voor instructies.

## <a name="additional-resources"></a>Aanvullende bronnen

[Woordenlijst voor paginamodellen](page-elements-overview.md)

[Het delen van inhoud door meerdere kanalen](cross-channel-sharing.md)

[Een module lokaliseren](e-commerce-extensibility/localize-module.md)

[Bestand voor definitie van module](e-commerce-extensibility/module-definition-file.md)

[Resources voor Commerce-extensies en labelbestanden lokaliseren](dev-itpro/extension-resource-localization.md)

[Modules globaliseren met de klasse CultureInfoFormatter](e-commerce-extensibility/globalize-modules.md)

[App-instellingen: thema's](e-commerce-extensibility/app-settings.md#themes-section)
