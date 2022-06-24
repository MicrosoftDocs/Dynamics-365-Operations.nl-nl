---
title: Kanalen aan e-commercesites toewijzen
description: In dit artikel worden enkele veelgebruikte scenario's voor kanaaltoewijzing in Microsoft Dynamics 365 Commerce beschreven die voor de meeste andere zakelijke behoeften kunnen worden toegepast.
author: samjarawan
ms.date: 05/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 94c43df26e8d6e55a5b6d459b65066d5873e1063
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902758"
---
# <a name="map-channels-to-e-commerce-sites"></a>Kanalen aan e-commercesites toewijzen

In dit artikel worden enkele veelgebruikte scenario's voor kanaaltoewijzing in Microsoft Dynamics 365 Commerce beschreven die voor de meeste andere zakelijke behoeften kunnen worden toegepast.

Dynamics 365 Commerce ondersteunt veel zakelijke scenario's voor het toewijzen van [online kanalen](#channels) met een geconfigureerde set producten, prijzen en kortingen aan [e-commercesites](#e-commerce-sites) voor klanten.

In dit artikel worden de volgende scenario's besproken:

- **Een kanaal met één taal met één e-commercesitevoorziening.** In dit scenario kan bijvoorbeeld sprake zijn van één merksite die voor de Engelse markt is geconfigureerd.
- **Een kanaal met meerdere talen met één gelokaliseerde e-commercesitevoorziening.** In dit scenario kan bijvoorbeeld sprake zijn van één merksite die voor Canada is geconfigureerd met taalondersteuning voor Frans en Engels. In dit scenario hebben gebruikers die verschillende talen selecteren dezelfde site-ervaring, maar is deze gelokaliseerd in de geselecteerde taal van elke gebruiker.
- **Een kanaal met meerdere talen met een verschillende sitevoorziening per taal.** In dit scenario kan bijvoorbeeld sprake zijn van één merksite die voor Canada is geconfigureerd met taalondersteuning voor Frans en Engels. In dit scenario is er voor elke taal een unieke sitevoorziening.
- **Meerdere kanalen (in één taal en/of meerdere talen) met één gelokaliseerde sitevoorziening.** In dit scenario kan bijvoorbeeld sprake zijn van één merksite die voor Australië en Nieuw-Zeeland is geconfigureerd. In dit scenario delen beide landen dezelfde sitevoorziening in het Engels, maar is elk land geconfigureerd met verschillende producten, valuta, prijzen, kortingen en verzendmethoden.
- **Meerdere kanalen (in één taal en/of meerdere talen) met een verschillende sitevoorziening per kanaal.** In dit scenario kan bijvoorbeeld sprake zijn van één merksite die voor Australië, Canada en Duitsland is geconfigureerd in meerdere talen. In dit scenario heeft elk land een unieke sitevoorziening, die is geconfigureerd met verschillende producten, valuta, prijzen, kortingen en verzendmethoden.

## <a name="channels"></a>Kanalen

Een kanaal (dat ook wel een online winkel of online kanaal wordt genoemd) vormt een online e-commercewinkel waar producten, prijzen, kortingen, talen, betalingsmethoden, leveringsmethoden, afhandelingscentra en andere aspecten van de online voorziening worden toegewezen die beschikbaar zijn voor de e-commerceklanten. Kanalen worden gemaakt en beheerd in Commerce Headquarters en aan één [rechtspersoon](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json#legal-entities) toegewezen. De rechtspersoon is gewoonlijk gevestigd in één land waar belastingaangifte voor het kanaal vereist is en kan worden geconfigureerd met slechts één valuta.

Zie [Overzicht van kanalen](channels-overview.md) voor meer informatie over kanalen. Zie [Een onlinekanaal instellen](channel-setup-online.md) voor meer informatie over het maken van een onlinekanaal.

In de volgende voorbeelden van Commerce Headquarters worden de standaard online kanalen weergegeven die worden geïmplementeerd met Dynamics 365 Commerce als de optie voor demogegevens is geselecteerd.

![Standaardkanalen met demogegevens in Commerce Headquarters.](media/channel-mapping-1.png)

## <a name="e-commerce-sites"></a>e-Commercesites

Een e-commercesite bevat een set sitepagina's waarin klanten kunnen bladeren om te winkelen. E-commercesites worden beheerd in Commerce Site Builder.

Zie [Overzicht van e-commercesites](online-store-overview.md) voor meer informatie over het maken en beheren van sites in Site Builder.

## <a name="common-channel-mapping-scenarios"></a>Veelvoorkomende scenario's voor kanaaltoewijzing

Dynamics 365 Commerce ondersteunt een groot aantal scenario's voor kanaaltoewijzing. De volgende kanaaltoewijzingsscenario's zijn slechts een subset van alle mogelijke scenario's voor kanaaltoewijzing. Deze zijn bedoeld als richtlijn voor de planning van unieke zakelijke scenario's. De fictieve goederenwinkel Adventure Works die is opgenomen in de Dynamics 365 Commerce-demogegevens, wordt voor elk scenario als voorbeeld gebruikt.

### <a name="single-language-channel-that-has-a-single-e-commerce-site-experience"></a>Een kanaal met één taal met één e-commercesitevoorziening

In het meest algemene scenario heeft één kanaal één taal om in één markt te verkopen. Een voorbeeld voor dit scenario is een online winkel van Adventure Works die alleen is ingesteld voor de Engelse markt.

In de volgende afbeelding ziet u een voorbeeld van kanaalconfiguratie in Commerce Headquarters. In deze configuratie ondersteunt het online kanaal slechts één taal (**en-us**), één valuta (**USD**) en één bedrijfsentiteit (**usrt**) die voor belastingaangifte wordt gebruikt.

![Waarden voor rechtspersoon, valuta en taal voor de online winkel van Adventure Works die in Commerce Headquarters is gemarkeerd.](media/channel-mapping-3.png)

Het online kanaal kan aan één e-commercesite in Site Builder worden toegewezen. Zie de sectie [Een kanaal toewijzen aan een site in Site Builder](#map-a-channel-to-a-site-in-site-builder) van dit artikel voor informatie over hoe u een nieuwe site maakt en aan een kanaal toewijst.

### <a name="multi-language-channel-that-has-a-single-localized-site-experience"></a>Een kanaal met meerdere talen met één gelokaliseerde e-commercesitevoorziening

In dit scenario ondersteunt één kanaal meerdere talen. Productnamen, omschrijvingen en kenmerken kunnen daarom worden gelokaliseerd in Commerce Headquarters. U kunt marketinginhoud op de site ook lokaliseren in Commerce Site Builder om een volledige, lokale site-ervaring te bieden.

De beperking van dit scenario is dat één kanaal kan worden geconfigureerd met slechts één valuta, één rechtspersoon en één set producten en prijzen. Deze configuratie is het beste voor landen/regio's met één valuta en meerdere talen (bijvoorbeeld Canada, met Engels en Frans), één rechtspersoon en één reeks producten en prijzen.

Elke taal in een kanaal kan worden geconfigureerd met een eigen domeinnaam. Het domein `www.adventure-works.ca` kan bijvoorbeeld worden geconfigureerd voor de Engelse versie van Canada, en het domein `www.adventure-works-fr.ca` kan worden geconfigureerd voor de Franse versie van Canada. U kunt ook verschillende talen in een kanaal configureren in één domein, waarna voor elke taal een ander pad kan worden gebruikt. Het domein `www.adventure-works.ca` kan bijvoorbeeld worden geconfigureerd voor de Engelse versie van Canada, en het pad `www.adventure-works.ca/fr` kan vervolgens worden gebruikt voor de Franse versie van Canada. [Geodetectie](geo-detection-redirection.md) kan ook worden ingeschakeld om een gebruiker automatisch naar de juiste site te leiden op basis van de locatie van de gebruiker.

Zie de sectie [Een siteselectiemodule toevoegen en configureren](#add-and-configure-the-site-picker-module) van dit artikel voor informatie over handmatig schakelen tussen talen voor klanten. Zie de sectie [Site-inhoud beheren met meerdere kanalen en talen](#manage-site-content-that-has-multiple-channels-and-languages) voor informatie over het aanpassen van gelokaliseerde pagina's en fragmenten.

### <a name="multi-language-channel-that-has-a-different-site-experience-per-language"></a>Een kanaal met meerdere talen met een verschillende sitevoorziening per taal

U kunt ook een scenario kiezen waarbij één kanaal meerdere talen ondersteunt, maar voor elke taal een volledig andere site-ervaring wordt geleverd. De aanbevolen methode voor het implementeren van dit scenario is het gebruik van [paginavarianten](#implement-page-variants-for-each-language) op één site.

Een andere methode is het maken van een nieuwe e-commercesite voor elke taal in Site Builder, en elke site vervolgens toewijzen aan één online kanaal en taal. Het resultaat is één online kanaal dat aan meerdere e-commercesites is gekoppeld, één kanaal voor elke taal. Voor deze methode met meerdere locaties zijn extra beheerresources nodig, omdat er meerdere locaties moeten worden beheerd in Site Builder.

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-single-localized-site-experience"></a>Meerdere kanalen (in één taal en/of meerdere talen) met één gelokaliseerde sitevoorziening

Voor een merksite kunnen meerdere online kanalen per regio zijn vereist ter ondersteuning van verschillende valuta's, productreeksen en prijzen voor elk kanaal op één site. De site Adventure Works kan bijvoorbeeld een online kanaal hebben voor de Canadese markt met meerdere talen, een kanaal voor de Amerikaanse markt met één taal en een kanaal voor de Duitse markt met één taal. In dit scenario wordt elk online kanaal geconfigureerd voor een regiospecifieke rechtspersoon met dezelfde set producten als de andere kanalen, of een subset van die producten of een andere set met producten. Elk kanaal heeft ook eigen prijzen in de regionale valuta, belastingen, kortingen en verzendmethoden.

In dit scenario kan elke markt worden geconfigureerd met eigen domeinnamen. Het domein `www.adventure-works.com` kan bijvoorbeeld worden geconfigureerd voor de Amerikaanse markt en het domein `www.adventure-works.de` voor de Duitse markt. Elke markt kan ook zo worden geconfigureerd dat deze een ander pad gebruikt. Het domein `www.adventure-works.com` kan bijvoorbeeld worden geconfigureerd voor de Amerikaanse markt en het pad `www.adventure-works.com/de` kan vervolgens worden gebruikt voor de Duitse markt. [Geodetectie](geo-detection-redirection.md) kan ook worden ingeschakeld om gebruikers automatisch naar de juiste site te leiden op basis van hun regio.

Mogelijk wilt u ook dat de site een vervolgkeuzelijst bevat waarmee gebruikers handmatig naar een specifieke markt kunnen overschakelen. Zie de sectie [De siteselectiemodule toevoegen en configureren](#add-and-configure-the-site-picker-module) van dit artikel voor meer informatie.

Zie de sectie [Meerdere kanalen configureren op een e-commercesite](#configure-multiple-channels-on-an-e-commerce-site) voor informatie over het configureren van meerdere kanalen op één site.

### <a name="multiple-channels-single-language-andor-multi-language-that-have-a-different-site-experience-per-channel"></a>Meerdere kanalen (in één taal en/of meerdere talen) met een verschillende sitevoorziening per kanaal

Mogelijk wilt u meerdere kanalen voor één merk in verschillende regio's hebben en wilt u dat elke regio een andere site-ervaring heeft. U kunt dit scenario op twee manieren implementeren:

- Gebruik [paginavarianten](#implement-page-variants-for-each-language).
- Configureer een andere site voor elk online kanaal in Site Builder en wijs vervolgens elke site toe aan een ander online kanaal en een andere taal. Voor deze methode met zijn extra beheerresources nodig, omdat er meerdere locaties moeten worden beheerd in Site Builder.

## <a name="cross-channel-sharing"></a>Het delen van inhoud door meerdere kanalen

Het delen van inhoud door meerdere kanalen is handig wanneer meerdere kanalen op één site inhoud kunnen delen. Bijvoorbeeld: een detailhandelaar die meerdere merken en winkelsystemen heeft die zijn gegroepeerd onder één site, kan bepaalde inhoud delen tussen enkele of alle winkelsystemen. Gedeelde inhoud kan pagina's bevatten voor voorwaarden, betalingsvoorwaarden, verzendmethoden en veelgestelde vragen (FAQ). Zie [Delen van meerdere kanalen inschakelen en gebruiken](cross-channel-sharing.md) voor meer informatie.

## <a name="map-a-channel-to-a-site-in-site-builder"></a>Een kanaal aan een site in Site Builder toewijzen

Er zijn meerdere methoden voor het maken en configureren van sites om verschillende online kanalen te gebruiken.

### <a name="create-a-new-site"></a>Een nieuwe site maken

U kunt een nieuwe site maken in Site Builder door naar de lijstpagina **Sites** te gaan en **Nieuwe site** te selecteren. Selecteer in het dialoogvenster **Nieuwe site** dat verschijnt, het standaard online kanaal en de standaardtaal voor de site, zoals in de onderstaande voorbeeldvoorbeeld is weergegeven.

![Maak een nieuw kanaal in Site Builder.](media/channel-mapping-4.png)

De site die u op deze manier maakt, is leeg en bevat geen sitepagina's (bijvoorbeeld een startpagina, categoriepagina's en productpagina's).

Zie voor meer informatie [Een e-commerce-site maken](create-ecommerce-site.md).

### <a name="create-a-new-site-by-using-the-site-copy-operation"></a>Een nieuwe site maken met de kopieerbewerking

In plaats van een nieuwe, lege site te maken zoals in het vorige gedeelte is beschreven, is het handiger te beginnen met een kopie van een van de startersites uit de modulebibliotheek van Commerce, zoals de Fabrikam- of Adventure Works-site.

Als u een bestaande site wilt kopiëren, gaat u naar de lijstpagina **Sites** in Site Builder en selecteert u **Site kopiëren**. Selecteer in het dialoogvenster **Site kopiëren** dat verschijnt, de bronsite en geef de naam van de doelsite op.

Op dit moment kunt u nog niet het standaard online kanaal en de standaardtaal voor de site selecteren. U kunt deze eigenschappen configureren nadat de kopieerbewerking is voltooid. Wanneer u de site de eerste keer selecteert op de lijstpagina **Sites** in Site Builder, verschijnt het dialoogvenster **Uw site instellen** waar u het standaardkanaal en de standaardtaal kunt selecteren.

Zie [Een e-Commerce-site kopiëren](copy-ecommerce-site.md) voor meer informatie over de kopieerbewerking.

### <a name="manage-an-existing-site-channel"></a>Een bestaand sitekanaal beheren

Nadat een site met een kanaal is geconfigureerd, kunt u het kanaal vanaf de geselecteerde site in Site Builder beheren en bijwerken via **Site-instellingen \> Kanalen**, zoals in het onderstaande voorbeeld wordt weergegeven.

![De kanaaltoewijzing in Site Builder beheren.](media/channel-mapping-7.png)

## <a name="support-multiple-sites-in-a-single-tenant"></a>Meerdere sites in één tenant ondersteunen

Meerdere merksites kunnen samen bestaan in één tenant. In het onderstaande voorbeeld ziet u drie verschillende sites (Adventure Works, Adventure Works Business en Fabrikam), die elk aan een ander online kanaal zijn toegewezen.

![Lijst met sites in Site Builder.](media/channel-mapping-8.png)

## <a name="configure-a-single-domain-name-with-paths-for-multiple-sites"></a>Eén domeinnaam met paden voor meerdere sites configureren

U kunt één domeinnaam voor meerdere sites gebruiken en vervolgens paden gebruiken om sites of talen van elkaar te scheiden. Het domein `www.mycompany.com` wordt bijvoorbeeld geconfigureerd voor twee verschillende e-commercesites: voor Fabrikam en Adventure Works. In dit geval kan het standaardpad of het zogenaamde lege pad (`www.mycompany.com`) worden gebruikt voor de site Fabrikam en kan een ander pad (bijvoorbeeld `www.mycompany.com/adventureworks`) voor de locatie Adventure Works worden gebruikt. Een andere optie is om een aangepast pad (bijvoorbeeld `www.mycompany.com/fabrikam`) te gebruiken in plaats van het standaardpad voor de Fabrikam-site.

U kunt ook een andere domeinnaam gebruiken voor elke site (bijvoorbeeld `www.adventure-works.com` en `www.fabrikam.com`). U kunt vervolgens paden gebruiken voor verschillende talen of regio's (bijvoorbeeld `www.adventure-works.com/fr-ca` voor Frans in Canada).

## <a name="configure-multiple-languages-on-a-site"></a>Meerdere talen voor een site configureren

Talen voor e-commercesite kunnen worden geconfigureerd in Site Builder via **Site-instellingen \> Kanalen**. In de onderstaande voorbeeldafbeelding is elke taal geconfigureerd via de landinstelling voor het pad, zodat elke taal een unieke URL heeft.

![Meerdere talen geconfigureerd voor een site.](media/channel-mapping-10.png)

Als u een nieuwe kanaaltaal wilt toevoegen, gaat u naar **Site-instellingen \> Kanalen** en selecteert u de kanaalkoppeling. Selecteer in het deelvenster dat rechts wordt weergegeven **Een landinstelling toevoegen** om het kanaal en de landinstelling te selecteren die u wilt toevoegen. Geef vervolgens het pad op dat u wilt gebruiken voor het geselecteerde kanaal.

### <a name="add-and-configure-the-site-picker-module"></a>De siteselectiemodule toevoegen en configureren

Nadat u een site met meerdere talen en/of kanalen hebt geconfigureerd, wilt u mogelijk een taalselectiefunctie toevoegen aan de koptekst van de sitepagina, zodat gebruikers handmatig hun taal of land/regio kunnen selecteren. De [koptekstmodule](author-header-module.md) van de mobilebibliotheek bevat ingebouwde ondersteuning voor gebruikers om een taal te selecteren met behulp van de [siteselectiemodule](site-selector.md). De siteselectiemodule kan in het koptekstfragment van de koptekstmodule worden toegevoegd.

Zie de sectie [Siteselectiemodule](site-selector.md) voor meer informatie over het toevoegen en configureren van de siteselectiemodule.

### <a name="implement-page-variants-for-each-language"></a>Paginavarianten implementeren voor elke taal

In dit scenario is er slechts één kanaal, maar er zijn meerdere talen. U kunt het uiterlijk van een pagina wijzigen op basis van de geselecteerde taal door er een paginavariant voor te maken. U kunt vervolgens gelokaliseerde inhoud aan de variant toevoegen.

Wanneer u een pagina hebt geopend in Site Builder en de koppeling rechtsboven selecteert waarin het huidige kanaal en de huidige taal worden weergegeven, ziet u een kanaal- en taalselectie, zoals in het onderstaande voorbeeld. Als u de pagina voor de huidige taal wilt overschrijven, selecteert u een andere landinstelling en **Wijzigen**. U kunt het kanaal ook wijzigen als u [een site beheert met meerdere kanalen en talen](#manage-site-content-that has-multiple-channels-and-languages).

![De taal voor een pagina in Site Builder wijzigen.](media/channel-mapping-14.png)

Als de variant voor de geselecteerde pagina of het geselecteerde fragment nog niet is gemaakt, ontvangt u een waarschuwingsbericht, zoals in het onderstaande voorbeeld. Selecteer in dit geval de koppeling **Paginavariant maken** in de berichttekst. In het dialoogvenster dat verschijnt, staan opties voor het starten met een kopie van een bestaande variant of het maken van een nieuwe pagina vanuit een sjabloon.

![Vragen om een paginavariant te maken in Site Builder](media/channel-mapping-16.png)

Als u geen variant maakt, wordt de oorspronkelijke pagina weergegeven en ziet u de juiste taal voor modulereeksen en productgegevens uit Commerce Headquarters. Als tekst, zoals een paginatitel of andere marketinginhoud, rechtstreeks in standaardpaginamodules is opgegeven, blijven de tekenreeksen voor die tekst in de oorspronkelijke taal.

In plaats van elke pagina en elk fragment handmatig te maken, kunt u elke pagina en elk fragment exporteren naar een XLIFF-bestand (XML Localization Interchange File Format) dat vervolgens kan worden verzonden voor lokalisatie. Nadat elke XLIFF-bestand is gelokaliseerd, kan het als een gelokaliseerde paginavariant worden geïmporteerd. Als u een XLIFF-bestand van een pagina of fragment in Site Builder wilt exporteren of als u een XLIFF-bestand in een pagina of fragment wilt importeren, selecteert u **Lokalisatie** op de opdrachtbalk. Selecteer vervolgens **XLIFF exporteren** of **XLIFF importeren**, zoals in het onderstaande voorbeeld.

![Een pagina of fragment importeren of exporteren in XLIFF-indeling.](media/channel-mapping-18.png)

## <a name="manage-site-content-that-has-multiple-channels-and-languages"></a>Site-inhoud beheren met meerdere kanalen en talen

Op een site met meerdere kanalen en/of talen wordt een unieke variant van elke pagina en elk fragment opgeslagen voor elke combinatie van een kanaal en een taal. Hierdoor kunnen de paginavarianten gelokaliseerde gegevens bevatten, maar het geeft u ook de flexibiliteit om het uiterlijk van een pagina voor een specifieke variant te wijzigen.

Zie [Paginavarianten implementeren voor elke taal](#implement-page-variants-for-each-language) van dit artikel voor informatie over het werken met paginavarianten.

## <a name="configure-multiple-channels-on-an-e-commerce-site"></a>Meerdere kanalen op een e-commercesite configureren

U kunt kanalen aan een e-commercesite in Site Builder toevoegen door naar **Site-instellingen \> Kanalen** te gaan en **Een kanaal toevoegen** te selecteren. Vervolgens selecteert u het online kanaal en de standaardlandinstelling in het dialoogvenster **Een kanaal toevoegen**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van kanalen](channels-overview.md)

[Een online afzetkanaal instellen](channel-setup-online.md)

[Overzicht van Organisaties en organisatiehiërarchieën](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md)

[Geodetectie en omleiding instellen](geo-detection-redirection.md)

[Het delen van inhoud door meerdere kanalen inschakelen en gebruiken](cross-channel-sharing.md)

[Een e-commercesite maken](create-ecommerce-site.md)

[Een e-commercesite kopiëren](copy-ecommerce-site.md)

[Siteselectiemodule](site-selector.md)
