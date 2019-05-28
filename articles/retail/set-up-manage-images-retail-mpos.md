---
title: Instellen en beheren van afbeeldingen voor Retail Modern POS (MPOS)
description: In dit artikel worden de stappen uitgelegd voor het instellen en beheren van afbeeldingen voor verschillende entiteiten die in Retail Modern POS (MPOS) worden weergegeven.
author: athinesh99
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelProfile, RetailMediaGallery, RetailImages,
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52851
ms.assetid: 5c21385e-64e0-4091-98fa-6a662eb33010
ms.search.region: global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: d2f4cc99ec239c4c35c44a226235d01e18d4185f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1546358"
---
# <a name="set-up-and-manage-images-for-retail-modern-pos-mpos"></a>Instellen en beheren van afbeeldingen voor Retail Modern POS (MPOS)

[!include [banner](includes/banner.md)]

In dit artikel worden de stappen uitgelegd voor het instellen en beheren van afbeeldingen voor verschillende entiteiten die in Retail Modern POS (MPOS) worden weergegeven.

## <a name="setting-up-the-media-base-url-and-defining-media-templates-to-configure-the-format-for-image-urls"></a>De basis-URL voor media instellen en mediasjablonen definiëren om de indeling voor afbeeldings-URL's te configureren

De afbeeldingen die worden weergegeven in Retail Modern POS (MPOS) moeten extern worden gehost, buiten Microsoft Dynamics 365 for Retail. Doorgaans worden ze gehost in een contentmanagementsysteem , contentleveringsnetwerk (CDN) of mediaserver. MPOS haalt en toont vervolgens de afbeeldingen voor de relevante entiteiten, zoals producten en catalogi, door toegang te krijgen tot de doel-URL. Als u deze extern gehoste afbeeldingen wilt ophalen, moet MPOS over de juiste URL-indeling voor de afbeeldingen beschikken. U kunt de vereiste URL-indeling voor de afbeeldingen configureren door de waarde **Basis-URL voor media** in te stellen in het kanaalprofiel en de functie **Mediasjabloon definiëren** te gebruiken voor elke rechtspersoon. U kunt ook de standaard URL-indeling voor een subset van rechtspersonen overschrijven door de functie **Bewerken in Excel** te gebruiken.

> [!IMPORTANT]
> In de huidige versie van Dynamics 365 for Retail kunt u de URL-indeling niet meer instellen met de XML voor het kenmerk **Afbeelding** voor MPOS in de kenmerkgroep **Standaard** voor entiteiten. Als u bekend bent met Microsoft Dynamics AX 2012 R3 en nu de huidige versie van Dynamics 365 for Retail gebruikt, moet u ervoor zorgen dat u altijd de nieuwe functionaliteit **Media sjabloon definiëren** gebruikt om afbeeldingen in te stellen. Gebruik of wijzig het kenmerk **Afbeelding** in de kenmerkgroep **Standaard** niet voor entiteiten, waaronder producten. Wijzigingen die u direct in de kenmerkgroep **Standaard** voor afbeeldingen maakt, worden niet weergegeven. Deze optie wordt uitgeschakeld in een toekomstige versie.

In de volgende procedures zijn afbeeldingen ingesteld voor de catalogusentiteit als een voorbeeld. Deze procedures helpen waarborgen dat het juiste pad voor de afbeeldingsbestemming impliciet wordt ingesteld voor alle catalogusafbeeldingen die een algemeen pad gebruiken. Als u bijvoorbeeld een mediaserver of CDN extern hebt ingesteld en wilt dat de afbeeldingen voor een bepaalde winkel in MPOS worden weergegeven, helpt de functionaliteit **Mediasjabloon definiëren** u het pad in te stellen waar MPOS de afbeeldingen kan vinden en ophalen.

> [!NOTE]
> Voor dit voorbeeld van demogegevens wordt de mediaserver geïmplementeerd op de detailhandelserver. U kunt het echter overal buiten Dynamics 365 for Retail hebben.

### <a name="set-up-the-media-base-url-for-a-channel"></a>De basis-URL voor media voor een kanaal instellen

1. Open de Dynamics 365 for Retail HQ-portal.
2. Klik op **Retail** &gt; **Kanaalinstellingen** &gt; **Kanaalprofielen**.

    [![channel-profile1](./media/channel-profile1.png)](./media/channel-profile1.png)

3. Werk in het kanaalprofiel dat uw winkel voor MPOS gebruikt, het veld **Basis-URL voor media** bij met de basis-URL van uw mediaserver of CDN. De basis-URL is het eerste deel van URL, dat door alle afbeeldingmappen van verschillende entiteiten wordt gedeeld.

    [![channel-profile2](./media/channel-profile2.png)](./media/channel-profile2.png)

### <a name="define-the-media-template-for-an-entity"></a>De mediajabloon definiëren voor een entiteit

1. Klik op **Retail** &gt; **Catalogusbeheer** &gt; **Catalogusafbeeldingen**.
2. Op de **Catalogusafbeeldingen** pagina, klikt u op het actievenster op **Mediasjabloon definiëren**. In het dialoogvenster **Mediasjabloon definiëren** in het veld **Entiteit**, moet standaard **Catalogus** zijn geselecteerd.
3. op het sneltabblad **Mediapad** voert u het resterende pad van de afbeeldinglocatie in. De media padondersteuningen **LanguageID** als variabele. Voor de demogegevens kunt u bijvoorbeeld een map **Catalogi** maken voor alle catalogusafbeeldingen onder de mediabasis-URL voor uw mediaserver (`https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer`). U kunt vervolgens een map voor elke taal maken, zoals en-US of fr-FR, en de gewenste afbeeldingen naar elke map kopiëren. Als u geen andere afbeeldingen voor de diverse talen hebt, kunt u de variabele **LanguageID** uit uw mapstructuur gebruiken en direct verwijzen naar de catalogimap die de catalogusafbeeldingen bevat.

    > [!NOTE]
    > De huidige versie van Dynamics 365 for Retail ondersteunt het token **{LanguageId}** voor catalogus-, product- en categorie-entiteiten. (Het token **{LanguageID}** wordt niet ondersteund voor klant- en werknemersentiteiten, volgens de bestaande standaard die sinds Microsoft Dynamics AX 6.x geldt.)

4. Voor afbeeldingen is de naamindeling hard gecodeerd op de catalogusnaam en kan deze niet worden gewijzigd. Daarom wijzigt u de naam van uw afbeeldingen zodat ze geschikte catalogusnamen hebben. Dit helpt waarborgen dat MPOS deze correct verwerkt.
5. Selecteer in het veld **Bestandsextensie** de verwachte bestandsnaamextensie, afhankelijk van het type afbeeldingen dat u hebt. Voor de demogegevens krijgen de catalogusafbeeldingen bijvoorbeeld de extensie .jpg. (De afbeeldingsbestanden worden ook hernoemd zodat deze catalogusnamen hebben.)
6. Klik op **OK**.
7. Om te valideren dat de mediasjabloon voor afbeeldingen correct is opgeslagen, klikt u op de pagina **Catalogusafbeeldingen** op **Mediasjabloon definiëren**. Om de sjabloon te valideren zonder het dialoogvenster **Mediasjabloon definiëren** te sluiten, kunt u het sneltabblad **Afbeeldings-URL's voor Excel genereren** gebruiken. Controleer de weergave van de afbeeldings-URL en controleer of de URL voldoet aan de eerder genoemde sjabloonstandaard. Het dialoogvenster **Mediasjabloon definiëren** heeft nu impliciet het afbeeldingspad ingesteld voor alle catalogusafbeeldingen die dit algemene URL-pad gebruiken. Dit URL-pad geldt voor alle catalogusafbeeldingen tenzij deze worden overschreven. Het eerste deel van het afbeeldingpad wordt overgenomen van de basis-URL voor media die u in het kanaalprofiel hebt gedefinieerd. Het resterende gedeelte van het pad is afkomstig uit het pad dat u in de sjabloon heeft opgegeven. De twee delen worden aaneengeschakeld om de volledige URL van de afbeeldingslocatie te bieden. Een catalogus in de demogegevens heeft bijvoorbeeld de naam Fabrikam-basiscatalogus. Daarom moet de afbeeldingsnaam Fabrikam Base Catalog.jpg zijn zodat deze de catalogusnaam en de bestandsnaamextensie .jpg gebruikt die in de sjabloon is geconfigureerd. In dit geval wordt de URL na samenvoeging `https://testax3ret.cloud.test.dynamics.com/RetailServer/MediaServer/Catalogs/en-US/Fabrikam Base Catalog.jpg`.
8. Voer de synchronisatietaken uit om de nieuwe sjabloon naar de te kanaaldatabase te zenden, zodat MPOS de sjabloon kan gebruiken om afbeeldingen te openen.
9. Om de mediasjabloon voor catalogusafbeeldingen aan de kanaalkant bij te werken, zorgt ervoor dat u **Catalogustaak 1150** uitvoert vanuit **Kleinhandel-IT** &gt; **Distributieplanning**.

    [![catalog1](./media/catalog1.png)](./media/catalog1.png)

## <a name="previewing-an-image-from-the-entity-level"></a>Een voorbeeld van een afbeelding weergeven vanaf het entiteitniveau

1. Vanaf de pagina voor het entiteitartikel in het hoofdkantoor kunt u de voorbeeldafbeelding bekijken die de afbeeldings-URL gebruikt die is afgeleid van de mediasjabloon. Voor dit voorbeeld gaat u naar de juiste catalogus en klikt u in het actievenster op **Media** &gt; **Afbeeldingen**. Gebruik de vervolgkeuzelijst om verschillende opslag te selecteren die verschillende kanaalprofielen kan hebben.
2. Om de impliciete mediasjabloon te bewerken of te verwijderen, moet u teruggaan naar het dialoogvenster **Mediasjabloon definiëren** voor de pagina **Catalogusafbeeldingen**.
3. U kunt de knoppen **Toevoegen** en **Verwijderen** gebruiken om handmatig het pad te wijzigen dat is gebaseerd op de impliciete sjabloon en wordt gebruikt voor een specifieke afbeelding. Zie het gedeelte [De mediasjabloon overschrijven voor entiteitartikelen](#overwriting-the-media-template-for-entity-items) later in dit artikel voor meer informatie.
4. Als u klaar bent met het bekijken van een voorbeeld van een afbeelding en het aanbrengen van de gewenste wijzigingen, start u het MPOS-exemplaar voor de betreffende winkel en kijkt u of de catalogusafbeeldingen worden weergegeven.

    [![catalog4](./media/catalog4.png)](./media/catalog4.png)

> [!NOTE]
> U kunt dezelfde procedure gebruiken voor alle vijf de rechtspersonen die worden ondersteund: Werknemer, Klant, Catalogus, Categorie en Producten. 'Catalogusproducten' (producten die zijn ingesteld op catalogusniveau) en 'kanaalproducten' (producten die zijn ingesteld op kanaalniveau) gebruiken de mediasjabloon die is ingesteld voor de productentiteit. Voor de productmediasjabloon kunt u het aantal productafbeeldingen selecteren dat per product moet worden weergegeven. U kunt ook de standaardafbeelding voor een bepaald product instellen. Op deze manier kunt u lege afbeeldingen in MPOS voorkomen en helpen te regelen welke afbeelding als standaardafbeelding voor een productartikel wordt gebruikt. In het volgende voorbeeld heeft elk product vijf afbeeldingen en de eerste afbeelding is ingesteld als de standaardafbeelding. Productvarianten worden op dezelfde manier verwerkt als hoofdproducten. De bestandsnaam van het afbeeldingsbestand moet op het productnummer moeten worden gebaseerd. Sommige tekens zijn ook voor wisseltekens terwijl de bestandsnaam wordt gegenereerd. Daarom is het goed om de bestandsnaam te verifiëren door de sectie **Afbeeldings-URL's voor Excel genereren** te gebruiken.
>
> [![prods](./media/prods.png)](./media/prods.png)

## <a name="synchronization-jobs-to-send-a-media-template-to-the-channel-side"></a>Synchronisatietaken om een mediasjabloon naar de kanaalkant te verzenden

Voor alle vijf de ondersteunde entiteiten (Werknemer, Klant, Catalogus, Categorie en Producten) geldt dat als u het dialoogvenster **Mediasjabloon definiëren** bijwerkt om een afbeelding in te stellen, u moet zorgen dat u de Catalogustaak (1150) uitvoert vanuit **Detailhandel IT** &gt; **Distributieplanning**. Deze taak maakt het mogelijk om de bijgewerkte mediasjabloon te synchroniseren met het kanaal en te laten gebruiken door MPOS. Voer de catalogustaak (1150) uit nadat u een van de volgende wijzigingen maakt:

- U werkt de mediasjabloon voor catalogusafbeeldingen bij via **Catalogusafbeeldingen** &gt; **Mediasjabloon definiëren**.
- U werkt de mediasjabloon voor werknemersafbeeldingen bij via **Werknemersafbeeldingen** &gt; **Mediasjabloon definiëren**.
- U werkt de mediasjabloon voor klantafbeeldingen bij via **Klantafbeelding** &gt; **Mediasjabloon definiëren**.
- U werkt de mediasjabloon voor productafbeeldingen bij via **Productafbeeldingen** &gt; **Mediasjabloon definiëren**.
- U werkt de mediasjabloon voor categorieafbeeldingen bij via **Categorieafbeeldingen** &gt; **Mediasjabloon definiëren**. U moet het kanaal ook publiceren.

## <a name="overwriting-the-media-template-for-entity-items"></a>Mediasjabloon voor entiteitsartikelen overschrijven

Zoals u in de vorige sectie hebt geleerd, ondersteunt de mediasjabloon voor een bepaalde entiteit slechts één algemeen pad. Dit pad is gebaseerd op de basis-URL voro media die is geconfigureerd en het mediapad dat is gedefinieerd. In veel gevallen wil een detailhandelaar echter afbeeldingen uit verschillende bronnen kunnen gebruiken voor een subset artikelen in een entiteit. Een winkel gebruikt bijvoorbeeld de zelfgehoste mediaserver voor de ene set catalogusafbeeldingen, maar gebruikt CDN URL's voor een andere set. Om afbeeldings-URL's te overschrijven die op een mediasjabloon voor entiteitafbeeldingen op het entiteitsniveau zijn gebaseerd, u kunt Bewerken in Excel en de functie Handmatig bewerken van de pagina **Voorbeeld** gebruiken.

### <a name="overwrite-by-using-edit-in-excel"></a>Overschrijven door Bewerken in Excel te gebruiken

1. Klik op **Retail** &gt; **Catalogusbeheer** &gt; **Catalogusafbeeldingen**.
2. Op de **Catalogusafbeeldingen** pagina, klik op **Mediasjabloon definiëren**. In het dialoogvenster **Mediasjabloon definiëren** in het veld **Entiteit**, moet **Catalogus** zijn geselecteerd.
3. Op het sneltabblad **Mediapad** merkt u de afbeeldinglocatie op.
4. Op het sneltabblad **Afbeeldings-URL's voor Excel genereren** klikt u op **Genereren**.

    > [!IMPORTANT]
    > Wanneer de mediasjabloon is gewijzigd, moet u klikken op **Genereren** voordat u de functionaliteit Bewerken in Excel kunt gebruiken.

    [![excel1](./media/excel1.jpg)](./media/excel1.jpg)

    U ziet nu een voorbeeld van de afbeeldings-URL's die zijn gegenereerd op basis van de laatst opgeslagen mediasjabloon.

    [![excel2](./media/excel2.png)](./media/excel2.png)

    > [!NOTE]
    > De URL's die worden gegenereerd voor Excel gebruiken het pad en de conventies van de gedefinieerde mediasjabloon. Deze conventies omvatten de conventies voor bestandsnamen. De verwachting is dat u de fysieke afbeeldingen buiten Dynamics 365 for Retail hebt ingesteld en dat de afbeeldingen kunnen worden opgehaald van URL's die zijn afgeleid van de mediasjabloon die u eerder hebt gedefinieerd. U kunt deze afgeleide URL's overschrijven via Bewerken in de Excel-functie.

5. Klik op **Bewerken in Excel**.
6. Nadat het Microsoft Excel-werkblad is geopend, klikt u op **Bewerken inschakelen** wanneer u daarom wordt gevraagd.
7. Wanneer u hierom wordt gevraagd, klikt u in het rechter deelvenster op **Deze invoegtoepassing vertrouwen** en wacht u tot de invoegtoepassing de installatie heeft voltooid.

    [![Deze invoegtoepassing vertrouwen](./media/excel4.jpg)](./media/excel4.jpg)

8. Als u wordt gevraagd u aan te melden, voert u de referenties in die u hebt gebruikt om u aan te melden bij het hoofdkantoor.

    [![Aanmeldingsprompt](./media/excel5.png)](./media/excel5.png)

9. Wanneer u zich aanmeldt, zou u de lijst met afbeeldings-URL's moeten kunnen zien voor de verschillende catalogusvermeldingen.
10. U kunt de afbeeldings-URL's voor diverse entiteitsartikelen bewerken, toevoegen en verwijderen.
11. Voor alle entiteiten behalve Producten kunt u de afbeelding-URL's overschrijven. Wijzig de bestaande afbeeldings-URL's, zodat de nieuwe bestemmings-URL van de afbeelding wordt gebruikt, en werk de bestandsnaam met de nieuwe bestandsnaam voor het afbeeldingsbestand. De bestandsnaam moet uniek zijn om te helpen waarborgen dat de record is uniek.

    [![Afbeeldings-URL's in Excel overschrijven](./media/excel6.jpg)](./media/excel6.jpg)

    > [!NOTE]
    > Wanneer u afbeeldings-URL's voor productentiteiten overschrijft met de functionaliteit Bewerken in Excel of de entiteitartikelpagina, geeft MPOS altijd alle mediasjabloonafbeeldings-URL's weer met de overschreven afbeeldings-URL's.

12. Wanneer u klaar bent met aanbrengen van wijzigingen, klikt u op **Publiceren in Excel** om een nieuwe, expliciete koppelingsinvoer te maken.
13. Ga terug naar HQ en klik op **OK**.
14. Voer de juiste synchronisatietaken uit voor de entiteit en controleer het voorbeeld op de entiteitpagina of in MPOS.

#### <a name="creating-new-records"></a>Nieuwe records maken

U kunt nieuwe records maken in Excel. Zorg echter dat u de juiste informatie opgeeft. Als u bijvoorbeeld een nieuw artikel wilt maken voor een catalogus, moet u ervoor zorgen dat de catalogus-id en de catalogusnaam kloppen. U moet ook een unieke bestandsnaam opgeven. De unieke bestandsnaam is zeer belangrijk omdat de uniciteit van records in Excel wordt gevalideerd tijdens de publicatie. Kopieer eerst de details van de catalogus waarvoor u een nieuwe record wilt maken, en kopieer de record. U moet alleen de bestandsnaam en de URL bijwerken, de rest van de gegevens is hetzelfde. U kunt nieuwe records maken voor productentiteitsartikelen door dezelfde basisprocedure te gebruiken. Kopieer vanuit het Excel-werkblad een bestaande record voor het product waarvoor u een nieuwe record maakt en vervang vervolgens de afbeeldings-URL en de bestandsnaam. Zorg ervoor dat de bestandsnaam uniek is.

#### <a name="deleting-an-existing-record"></a>Een bestaande record verwijderen

Alleen de overgeschreven afbeeldings-URL-records kunnen worden verwijderd. Nadat een afbeelding is verwijderd en synchronisatie is voltooid, wordt de afbeelding niet meer op de pagina **Voorbeeld** of in MPOS weergegeven. Afbeeldings-URL-records die zijn afgeleid van de mediasjabloon, kunnen niet worden verwijderd, omdat deze records altijd steeds worden afgeleid van de mediasjabloon.

### <a name="overwrite-from-the-entity-level-preview-page"></a>Overschrijven vanuit Voorbeeldpagina op entiteitsniveau

Voor alle entiteiten behalve Producten kunt u de afbeeldings-URL voor een bepaald entiteitartikel op het niveau van het entiteitartikel overschrijven vanaf de pagina **Voorbeeld**. Voor producten kunt u de entiteitpagina 'Catalogusproducten' gebruiken. Dit voorbeeld toont hoe u een catalogusafbeelding kunt overschrijven.

1. Klik op **Catalogi** &gt; **Media** &gt; **Afbeeldingen** en selecteer de catalogusafbeelding die moet worden bijgewerkt.
2. Klik op **Toevoegen** en voer de afbeeldings-URL in om de URL van de mediasjabloon te overschrijven.
3. Als u wilt dat deze afbeelding wordt weergegeven in MPOS voor de catalogus, kunt u deze als standaardafbeelding instellen.
4. Klik tot slot op **OK**. De afbeeldings-URL wordt bijgewerkt voor deze catalogusafbeelding, en een voorbeeld wordt weergegeven.

    [![preview3](./media/preview3.png)](./media/preview3.png)

5. U kunt ook het afbeeldingvoorbeeld voor alle overschreven afbeeldings-URL's weergeven op de galeriepagina **Catalogusafbeeldingen**.

    [![preview-4](./media/preview-4.png)](./media/preview-4.png)

> [!NOTE]
> Momenteel geeft de galerie geen afbeeldingsvoorbeelden weer voor URL's van mediasjabloonafbeeldingen. Voor de entiteiten Catalogus, Werknemer, Klant en Categorie, als de gebruiker expliciet een URL opgeeft via deze pagina, bevelen we aan dat u aangeeft welke afbeelding de standaardafbeelding is, omdat detailhandelserverclients slechts één afbeelding weergeven per catalogus, werknemer en categorie. Als de gebruiker geen standaardafbeelding opgeeft, bepaalt het systeem de standaardafbeelding en stuurt deze naar de aanroeper van de detailhandelsservice (MPOS of Ecommerce).

### <a name="overwrite-the-image-url-for-catalog-product-images-from-the-preview-page"></a>Overschrijf de afbeeldings-URL voor afbeeldingen van catalogusproducten vanuit de pagina Voorbeeld

Als u afbeeldings-URL's voor de catalogusproductafbeeldingen wilt overschrijven, moet u de pagina **Voorbeeld** gebruiken. U kunt Bewerken in de Excel-functie niet gebruiken.

1. Om productafbeeldingen op een catalogusniveau te overschrijven, selecteert u een catalogus, en selecteert u vervolgens het product waarvoor u de afbeelding wilt overschrijven.
2. Klik op **Kenmerken**.
3. Selecteer op de volgende pagina **Afbeelding** en klik vervolgens op **Bewerken**. De pagina **Voorbeeld** wordt geopend als een dialoogvenster.
4. Klik op **Toevoegen** en overschrijf de afbeeldings-URL met een nieuwe URL.
5. Klik tot slot op **OK**. U ziet nu het voorbeeld van de nieuwe afbeelding en kunt deze instellen als standaardafbeelding.

    [![cat3](./media/cat3.png)](./media/cat3.png)

> [!NOTE]
> Na de koppeling van de categorieafbeelding moet u het kanaal publiceren en de kanaaltaak uitvoeren om ervoor te zorgen dat de wijzigingen in de kanaaldatabase worden gepubliceerd.

## <a name="setting-up-images-to-appear-in-offline-mode-for-mpos"></a>Afbeeldingen instellen om te worden weergegeven in de offline MPOS-modus

MPOS kan in de online modus werken (wanneer MPOS is verbonden met de detailhandelsserver) of de offlinemodus (wanneer er geen detailhandelsserver of netwerkconnectiviteit is, en transacties worden opgeslagen in een lokale offlinedatabase). Wanneer MPOS in offlinemodus wordt uitgevoerd, kan het geen afbeeldingen van de externe afbeeldingserver halen om van de detailhandelserver weer te geven, omdat de verbinding is verbroken. U kunt echter nog afbeeldingen instellen, zodat ze worden weergegeven wanneer MPOS in de offlinemodus wordt uitgevoerd.

### <a name="set-up-product-images-to-appear-in-offline-mode-for-mpos"></a>De productafbeeldingen instellen om te worden weergegeven in de offline MPOS-modus

De productafbeeldingen die in offlinemodus moeten worden gebruikt, kunnen worden ingesteld door de vereiste fysieke afbeelding te uploaden naar de afbeelding van het basisproduct.

1. Klik op **Productgegevensbeheer** &gt; **Producten** &gt; **Producten**.
2. Selecteer het product om de offlineafbeelding in te stellen.
3. Klik op **Bewerken** en klik vervolgens op de pijl in de rechterbovenhoek om het rechterdeelvenster weer te geven.
4. Op het sneltabblad **Productafbeelding** klikt u op **Afbeelding wijzigen**, en uploadt u de fysieke afbeelding voor het geselecteerde product die u in offlinemodus wilt gebruiken.
5. De pagina opslaan en sluiten
6. Terwijl MPOS in modus Online is, moet de Catalogustaak in HQ uitvoeren om ervoor te zorgen dat de gegevens ten minste eenmaal aan de offlinedatabase worden verzonden.
7. Zet MPOS in offlinemodus. U moet de afbeelding zien die u hebt geüpload voor het specifieke product in HQ.

    [![offline1](./media/offline1.png)](./media/offline1.png)

### <a name="set-up-catalog-category-employee-and-customer-images-to-appear-in-offline-mode-for-mpos"></a>Catalogus, categorie, werknemer, en klantafbeeldingen instellen die in de offlinemodus van MPOS worden weergegeven

De catalogus, de categorie, werknemer en de afbeeldingen van klanten die in offlinemodus moeten worden gebruikt, kunnen worden ingesteld door de bestemmingskoppeling van de vereiste afbeelding toe te voegen aan de galerie en de afbeelding in te stellen als de standaardafbeelding voor de geselecteerde entiteit.

1. Ga naar de catalogus en klik vervolgens in het actievenster op **Media** &gt; **Afbeeldingen**.
2. Volg de stappen in de sectie [Overschrijven vanaf de voorbeeldpagina op entiteitniveau](#overwrite-from-the-entity-level-preview-page) om de externe afbeeldings-URL toe te voegen.
3. Markeer deze afbeelding als standaardafbeelding voor de catalogus door het selectievakje voor de afbeelding te selecteren in het raster.
4. Voer de catalogustaak uit. Deze afbeelding wordt nu gebruikt als Offline afbeelding voor die catalogus in MPOS.
5. Volg een vergelijkbaar proces voor andere entiteiten, zoals Categorie, Werknemer en Klant.

    [![offline2](./media/offline2.png)](./media/offline2.png)
