---
title: Aanbiedingsbeheer instellen
description: In dit onderwerp wordt beschreven hoe u aanbiedingen instelt in Talent.
author: josaw
manager: AnnBe
ms.date: 02/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa6c8c80870dd7bd06498c7571ba8a110be85c86
ms.sourcegitcommit: 3b12ff5ca81650ae666ff443b0bc998182f3931e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2019
ms.locfileid: "376502"
---
# <a name="set-up-offer-management"></a>Aanbiedingsbeheer instellen 

[!include [banner](includes/banner.md)]

Wanneer een kandidaat wordt verplaatst naar de aanbiedingsfase in Dynamics 365 for Talent: Attract, moet u ervoor zorgen dat de aanbiedingen snel kunnen worden gemaakt voor de kandidaat, goedgekeurd indien nodig en naar de kandidaat verzonden. Aangezien de meeste aanbiedingen standaard zijn, kunnen ze door herbruikbare sjablonen worden gemaakt. In Attract worden alle aanbiedingen in één aanbiedingspakket gecombineerd. Dat is een verzameling van een of meer aanbiedingsdocumenten. 

In dit onderwerp vindt u alle stappen die een Attract-beheerder zou volgen om verschillende aanbiedingspakketsjablonen in te stellen als onderdeel van het aanbiedingsbeheer in Attract. Gebruikers met niet-beheerdersrollen hebben geen toegang tot deze mogelijkheden.

>[!NOTE]
> Mogelijkheden voor aanbiedingsbeheer zijn beschikbaar als onderdeel van de Uitgebreide invoegtoepassing voor aanstellingen.

## <a name="offer-data"></a>Gegevens van aanbieding 

Aanbiedingsgegevens zijn de kleinste eenheid in de aanbiedingspakketsjabloon. Een veel voorkomend aanbod bestaat uit standaardtekst en een set waarden. De sets waarden zijn de enige onderdelen die tussen de aanbiedingen kunnen veranderen. Tijdens het maken van de aanbieding is het belangrijkste aspect waar de maker van de aanbieding op kan focussen, de lijst met tijdelijke aanduidingen voor aanbiedingsgegevens in een aanbiedingspakketsjabloon. Ga als volgt te werk als u aanbiedingsgegevens wilt instellen.

1.  Ga naar **Aanbiedingsbeheer**.

1.  Vouw de sectie **Bibliotheek** in het linkernavigatievenster uit en ga naar **Gegevens van aanbieding**.

    >[!NOTE]
    > De pagina **Gegevens van aanbieding** bevat de secties **Details van kandidaat** en **Functiedetails**. Attract biedt standaard enkele tijdelijke aanduidingen voor aanbiedingsgegevens.
    
    > Er zijn secties op de pagina waarmee u verschillende tijdelijke aanduidingen voor aanbiedingsgegevens in logische groepen kunt ordenen. Deze secties kunnen helpen bij het onderhoud van aanbiedingsgegevens en het invullen van gegevens tijdens het maken van aanbiedingen.

1.  Als u een nieuwe sectie voor aanbiedingsgegevens wilt maken, klikt u op **Een sectie toevoegen** en voert u een unieke naam voor de sectie in.

1.  Als u tijdelijke aanduidingen voor aanbiedingsgegevens aan een sectie wilt toevoegen, klikt u op **Gegevens van aanbieding toevoegen** en voert u een unieke naam voor de tijdelijke aanduiding in.

1.  Als u de naam van een sectie wilt bewerken, plaatst u de aanwijzer boven de sectienaam en werkt u de naam bij.

1.  Als u de naam van een bestaande tijdelijke aanduiding voor aanbiedingsgegevens wilt bewerken, zorgt u eerst dat de tijdelijke aanduiding niet al deel uitmaakt van een sjabloon. Vervolgens plaatst u de muisaanwijzer op de naam van de tijdelijke aanduiding voor aanbiedingsgegevens en werkt u de naam indien nodig bij.

1. Als u een bestaande tijdelijke aanduiding voor aanbiedingsgegevens wilt verwijderen, zorgt u eerst dat de tijdelijke aanduiding geen deel uitmaakt van een andere sjabloon. Plaats vervolgens de muisaanwijzer op de tijdelijke aanduiding en wanneer het prullenbakpictogram wordt weergegeven, klikt u op de prullenbak om de tijdelijke aanduiding voor aanbiedingsgegevens te verwijderen.
    >[!NOTE]
    > U kunt zien van hoeveel sjablonen een tijdelijke aanduiding voor aanbiedingsgegevens deel uitmaakt door de getalindicator naast alle aanbiedingsgegevens. 

1. Als u een sectie wilt verwijderen, plaatst u de muisaanwijzer op de naam. Als geen van de tijdelijke aanduidingen voor aanbiedingsgegevens in de sectie worden weergegeven in een sjabloon, kunt u klikken op het prullenbakpictogram om de sectie te verwijderen. 
    >[!NOTE]
    > Als u de sectie verwijdert, verwijdert u ook alle tijdelijke aanduidingen voor aanbiedingsgegevens in die sectie.

Nadat de tijdelijke aanduidingen voor aanbiedingsgegevens zijn ingesteld, kunt u ze in elke documentsjabloon gebruiken. Tijdelijke aanduidingen voor aanbiedingsgegevens zijn niet beperkt tot een specifieke sjabloon. Dezelfde set kan worden gebruikt in alle sjablonen.

## <a name="offer-data-rules"></a>Regels aanbiedingsgegevens

De meeste organisaties hebben regels voor hoe aanbiedingen moeten worden gemaakt. Een organisatie wil bijvoorbeeld vereisen dat de maximale aanbieding voor jaarsalaris voor een bepaalde combinatie van vestiging en anciënniteitsniveau ligt in een bepaald bereik, of dat er slechts enkele waarden mogelijk zijn voor het aanbiedingsniveau van de nieuwe aanstelling. Attract ondersteunt momenteel al dergelijke gegevens met behulp van een CSV-bestand.

Ga als volgt te werk om het CSV-bestand met gegevensregels voor te bereiden.

1.  Bepaal de tijdelijke aanduiding voor aanbiedingsgegevens voor de regelset. Bijvoorbeeld **Jaarsalaris**.

1.  Bepaal de afhankelijke waarden voor de tijdelijke aanduiding voor aanbiedingsgegevens. Bijvoorbeeld **Functielocatie** en **Niveau**.

1.  Geef kolommen 1 en 2 op als **Functielocatie** en **Niveau**.

1.  Als u een bereikwaarde wilt uploaden, maakt u van kolom 3 en 4 **Jaarsalaris**. Als u een specifieke waarde wilt uploaden in plaats van een bereik, maakt u alleen van kolom 3 **Jaarsalaris**.

1.  Vul het Microsoft Excel-bestand in op basis van uw vereiste rollen.

1.  Zorg ervoor dat elke rij een unieke combinatie van de gezamenlijke waarden is.

1.  Sla het bestand op in CSV-indeling.

Ga als volgt te werk om het bestand met gegevensregels te uploaden.

1.  Ga naar **Aanbiedingsbeheer**.

1.  Vouw de sectie **Bibliotheek** in het linkernavigatievenster uit en ga naar **Regels aanbiedingsgegevens**.

1.  Klik op **Nieuwe gegevensset** om het dialoogvenster **Uploaden** te openen.

1.  Geef een unieke naam voor de regelset op en upload vervolgens het opgeslagen CSV-bestand.

1.  Klik op **Toevoegen**.
    De regelset wordt verwerkt op de achtergrond en u wordt in de app en per e-mail geïnformeerd zodra het is voltooid.

    U wordt gewaarschuwd als er fouten zijn opgetreden tijdens het uploaden. U kunt vervolgens het foutenlogboek downloaden, het bestand herstellen en opnieuw uploaden.

1.  Gebruik de knop met weglatingstekens (**...**) als u de regelset wilt downloaden en de set waarden wilt bijwerken. Nadat u hebt bijgewerkt, kunt u het bestand opnieuw uploaden.

1.  U kunt een bestaande regelsetupload verwijderen als de tijdelijke aanduiding die wordt gedefinieerd, niet wordt gebruikt in een andere documentsjabloon.

>[!NOTE]
> - Elke tijdelijke aanduiding kan slechts één unieke set kolommen hebben waarvan deze afhankelijk is. Bijvoorbeeld als **Jaarsalaris** afhankelijk is van **Functielocatie** en **Niveau**, kunt u geen andere regelset uploaden waarin **Jaarsalaris** afhankelijk is van een andere set kolommen.

> - U kunt gegevenssets met voorbeeldaanbiedingsgegevens downloaden op het tabblad **Voorbeelden** op de pagina **Regels aanbiedingsgegevens**.

> - Wanneer de maker van een aanbieding de waarden overschrijft die worden aanbevolen door de aanbiedingsgegevensregels, wordt de aanbieding gemarkeerd als niet-standaard en is een werkstroom voor aanbiedingsgoedkeuring verplicht.

## <a name="document-templates"></a>Documentsjablonen

Een aanbiedingsdocumentsjabloon kan beheerders helpen aanbiedingsbrieven te maken. De aanbiedingsdocumentsjabloon is een combinatie van de tekst die deel van de aanbieding uitmaakt, en de gedefinieerde tijdelijke aanduidingen voor aanbiedingsgegevens. 

Ga als volgt te werk voor het maken van een aanbiedingsdocumentsjabloon.

1.  Ga naar **Aanbiedingsbeheer**.

1.  Vouw de sectie **Bibliotheek** in het linkernavigatievenster uit en ga naar **Sjablonen**.

    De pagina **Sjablonen** bevat een lijst met documentsjablonen die al zijn gedefinieerd.

1.  Als u een nieuwe documentsjabloon wilt maken, klikt u op **Nieuwe sjabloon**.

1.  Voer een unieke naam voor de sjabloon in en klik op **Maken**.

1.  Gebruik de RTF-editor om de inhoud van het aanbiedingsdocument in te voegen of te bewerken. U kunt tabellen, afbeeldingen en hyperlinks invoegen met de beschikbare opties boven in de teksteditor.

1.  U kunt tijdelijke aanduidingen voor aanbiedingsgegevens in het aanbiedingssjabloondocument invoegen door:

    - Slepen en neerzetten vanuit het rechterdeelvenster.

    - De tijdelijke aanduiding voor aanbiedingsgegevens op de positie hashtaggen. Typ **\#** en begin de naam van de tijdelijke aanduiding voor aanbiedingsgegevens te typen. Opties worden weergegeven in de vervolgkeuzelijst. Klik of druk op **Enter** om de tijdelijke aanduiding voor aanbiedingsgegevens in te voegen.

    >[!NOTE]
    > - Als u een tijdelijke aanduiding voor aanbiedingsgegevens aan de documentsjabloon wilt koppelen zonder de waarde ervan aan de kandidaat te tonen, plaatst u de muisaanwijzer op de tijdelijke aanduiding voor aanbiedingsgegevens en klikt u op het pictogram **Vastmaken**. Hiermee wordt de tijdelijke aanduiding vastgemaakt aan de sectie **Vastgemaakte aanbiedingsgegevens** van de aanbiedingsdocumentsjabloon. Als u de tijdelijke aanduiding wilt losmaken, volgt u dezelfde stappen maar klikt u op **Losmaken** in de lijst met tijdelijke aanduidingen voor aanbiedingsgegevens.

    > - Als u de lijst met actieve tijdelijke aanduidingen voor aanbiedingsgegevens wilt weergeven, schakelt u over op het tabblad **Actief** in het rechterdeelvenster.

    > - Als u een tijdelijke aanduiding invoegt die wordt aangestuurd door een regelset voor aanbiedingsgegevens, ziet u de afhankelijkheid van die tijdelijke aanduiding voor aanbiedingsgegevens van andere waarden.

    > - U kunt ook de inhoud uit een .docx-bestand op uw lokale computer **importeren** en indien nodig bewerken. Op die manier hoeft u niet alle content te typen in de editor.

1. Als u een voorbeeld van het document wilt bekijken, gebruikt u de optie **Voorbeeld** boven aan de pagina.

1. Als u wilt bepalen of de maker van een aanbieding de inhoud van het aanbiedingsdocument kan bewerken, gebruikt u de optie **Machtiging beheren** boven aan de pagina. Als u wilt dat de maker van de aanbieding alleen waarden van tijdelijke aanduidingen kan invoegen en geen tekst kan bewerken, stelt u de machtigingswaarde in op **Nee**.

1. Klik op **Opslaan** om uw voortgang op te slaan. De sjabloon wordt opgeslagen in een conceptstaat.

1. Als u het document wilt voltooien en wilt markeren als gepubliceerd, klikt u op **Voltooien**.

1. Op de landingspagina van de documentsjabloonbibliotheek kunt u zien welke documentsjablonen momenteel actief zijn, zich in de conceptmodus bevinden en zijn gearchiveerd en niet langer in gebruik zijn.

>[!NOTE]
> U kunt elke aanbiedingsdocumentsjabloon verwijderen die geen deel uitmaakt van een bestaande aanbiedingspakketsjabloon.


## <a name="offer-package-templates"></a>Pakketsjablonen aanbieden

Aanbiedingspakketten zijn de aanbiedingsartefacten die worden gedeeld met de kandidaat en bestaan uit een combinatie van een of meer aanbiedingsdocumentsjablonen. Ga als volgt te werk voor het maken van een aanbiedingspakket.

1.  Ga naar **Aanbiedingsbeheer**.

1.  Ga naar **Pakketten** in het linkernavigatievenster.

    Een lijst met actieve pakketsjablonen die beschikbaar zijn voor makers van aanbiedingen, wordt weergegeven.

1.  Als u een nieuw aanbiedingspakket wilt maken, klikt u op **Nieuw pakket**.

1.  Voer een unieke naam in en klik op **Maken**.

1.  Klik op **Sjabloon toevoegen**.

    >[!NOTE]
    > - U kunt een nieuwe sjabloon te maken of een bestaande kiezen.

    > - Als u een bestaande sjabloon toevoegt, moet u zorgen dat de aanbiedingsdocumentsjabloon is opgeslagen, is voltooid, en als actief is gemarkeerd.
    
    > - U kunt zoveel documentsjablonen kiezen als u wilt. 
    
1.  Klik op **Gereed** om terug te keren naar **Pakketbeheer**.

    U kunt de volgorde van de documenten configureren en ook markeren of het specifieke aanbiedingsdocument tijdens het maken van de aanbieding vereist is. De maker van de aanbieding heeft de optie de documenten te verwijderen die zijn gemarkeerd als **Niet verplicht**.

1. Als u de aanbiedingspakketsjabloon wilt opslaan, zodat deze bruikbaar is voor alle makers van aanbiedingen, klikt u op **Opslaan en publiceren**.

   Als u concepten van aanbiedingspakketsjablonen wilt zien, gaat u naar het tabblad **Concepten**. Als een wijziging wordt aangebracht in de aanbiedingspakketsjabloon, moet deze worden opgeslagen er opnieuw worden gepubliceerd.

## <a name="configure-an-offer-process"></a>Een aanbiedingsproces configureren

Er zijn verschillende onderdelen van het proces voor het maken van een aanbieding die kunnen worden geconfigureerd door de beheerder van Attract.

- **Aanbiedingsgoedkeuringen**: kies of aanbiedingsgoedkeuringen vereist zijn voordat de aanbieding kan worden verzonden naar de kandidaat. Als beheerder kunt u ook besluiten of alle aanbiedingsgoedkeuringen sequentieel plaatsvinden of in een parallelle goedkeuringswerkstroom. U kunt ook vereisen dat goedkeurders van aanbiedingen een opmerking toevoegen met hun goedkeuring van de aanbieding. Goedkeuringen van aanbiedingen zijn verplicht voor alle niet-standaard aanbiedingen.

- **Aanbieding van kandidaat**: als beheerder kunt u kiezen of alle aanbiedingen een verloopdatum hebben en zo ja, wat de standaard voor de vervaldatum moet zijn. U kunt ook configureren of kandidaten een aanbieding kunnen afwijzen.

- **Elektronische handtekeningen**: als beheerder kunt u de methode kiezen waarmee kandidaten aanbiedingen kunnen ondertekenen.
    - Adobe Sign: alle aanbiedingspakketten worden verzonden en ondertekend via Adobe Sign. Alle makers van aanbiedingen die de aanbieding willen publiceren, moet beschikken over hun eigen Adobe Sign-licentie die is verbonden met Attract. 

    - ESign: dit is de standaardoptie, die kant en klaar wordt geleverd, waarmee de gebruiker een aanbod kan ondertekenen door zijn/haar naam en initialen te typen.

>[!NOTE]
> Ga voor Adobe Sign-licenties en een gratis proefversie deze [koppeling](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).

Als u meer wilt weten over het maken van aanbiedingen, raadpleegt u [Aanbiedingen maken, goedkeuren en ondertekenen](./creating-offers.md).
