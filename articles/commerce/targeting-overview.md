---
title: Targeting op apparaten, markt en geolocatie
description: In dit onderwerp wordt beschreven hoe u doelgroepen en doelen kunt aanmaken, bewerken en beheren in Microsoft Dynamics 365 Commerce Site Builder met behulp van apparaat-, markt- en geolocatiegegevens.
author: sushma-rao
ms.date: 07/30/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2021-07-31
ms.dyn365.ops.version: AX 10.0.21
ms.openlocfilehash: b17c394105d4bb878c8375989924d3c3da079c78
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985132"
---
# <a name="device-market-and-geolocation-targeting"></a>Targeting op apparaten, markt en geolocatie

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u doelgroepen en doelen kunt aanmaken, bewerken en beheren in Microsoft Dynamics 365 Commerce Site Builder met behulp van apparaat-, markt- en geolocatiegegevens.

Met Dynamics 365 Commerce kunt u variaties van uw pagina-inhoud (ook wel *doelen* genoemd) voor specifieke groepen klanten (ook wel *doelgroepen* genoemd) personaliseren om de interactie met gebruikers en de tevredenheid te vergroten. U kunt eerst een doelgroep of een doel aanmaken. Voor een geslaagde targeting-ervaring zijn echter beide onderdelen vereist.

U maakt doelgroepen aan en beheert deze in Commerce Site Builder op basis van klantgegevens als locatie, apparaatgegevens, aanmeldingsstatus en andere dynamisch afgeleide gegevens van webaanvragen van klanten. U kunt ook doelen aanmaken en beheren in e-commercemodules en -fragmenten in Commerce Site Builder.

**Disclaimer**: u bent verantwoordelijk voor het gebruik van deze functie in overeenstemming met alle toepasselijke wet- en regelgeving, waaronder wet- en regelgeving die betrekking heeft op targeting en het maken van profielen. 

## <a name="audiences"></a>Doelgroepen

Een doelgroep is een groep gebruikers, en het lidmaatschap van de groep wordt bepaald door een reeks dynamische regels. Deze regels zijn eenvoudige logicatests die worden uitgevoerd op gegevens die beschikbaar zijn in klantaanvragen of andere beschikbare segmenten. U kunt meerdere regels combineren met behulp van AND/OR-operators.

Commerce ondersteunt van nature basissegmenten zoals apparaatinformatie, aanmeldingsstatus, verwijzer en querytekenreeksparameters. Commerce ondersteunt ook uitbreidbare segmenten via verbindingen met externe providers.

### <a name="basic-segments"></a>Basissegmenten

De volgende segmenten zijn standaard beschikbaar en kunnen worden opgenomen in doelgroepdefinities:

- **Aanmeldingsstatus** - testen of een gebruiker is geverifieerd.
- **Apparaatplatform** - testen op de volgende apparaattypen:

    - Mobiel
    - Desktop
    - Tablet
    - Anders

- **OS apparaat** - testen op de volgende besturingssystemen:

    - Windows
    - Linux
    - iOS
    - Android, overige

- **Parameters querytekenreeks** - testen of er een sleutelwaardepaar in een querytekenreeksparameter van een aanvraag-URL bestaat. Er kan bijvoorbeeld voor de URL `www.fabrikam.com/en-us/request?promo=true` een regel worden geschreven om te testen of de **promotie** parameter de waarde **waar** heeft.
- **Cookie** - testen op een cookie-waarde die voor het domein in de aanvraag-URL is ingesteld. Een aanvraag voor Fabrikam.com kan bijvoorbeeld een cookie bevatten met de naam **AangepasteLayout** en de waarde **1**. De cookietest controleert of er een cookie bestaat, maar maakt geen cookie aan. In het vorige voorbeeld moet JavaScript de cookie **AangepasteLayout** al vanuit een andere module of een ander bedrijfsproces hebben ingesteld.

    > [!NOTE]
    > Zorg ervoor dat uw gebruik van cookies in overeenstemming is met toepasselijke wetgeving.

- **Verwijzer** - als een gebruiker een koppeling volgt om de pagina aan te vragen, is de verwijzer de URL van de pagina die de koppeling host.

### <a name="extensible-segments"></a>Uitbreidbare segmenten

Met Commerce kunt u de lijst met beschikbare segmenten uitbreiden door verbinding te maken met externe segmentatieproviders. Een segmentatieprovider zal de beschikbare segmenttypen beschrijven. Raadpleeg [Connectors configureren en inschakelen](e-commerce-extensibility/connectors.md) voor meer informatie over het maken van verbinding met een geroep geolocatie of segmentatieprovider.

> [!NOTE]
> - Als een externe provider is ingeschakeld, kan deze verbinding maken met een service met onvoorspelbare prestaties. Om te zorgen voor een betere gebruikerservaring wordt de standaardversie van de pagina getoond als een gebruiker een pagina aanvraagt die is voorzien van targeting en die pagina verwijst naar een doelgroep die een externe segmentprovider controleert.
> - De gebruiker moet toestemming geven voor het gebruik van cookies. De browser van de gebruiker vraagt vervolgens alle segmenten aan bij de betreffende providers en de resultaten worden in een cookie geplaatst die naar de gebruiker wordt teruggestuurd. Volgende aanvragen voor de pagina zullen deze informatie gebruiken om targeted inhoud aan de gebruiker te laten zien. Raadpleeg [Cookie-conformiteit](cookie-compliance.md) voor meer informatie over cookie-conformiteit.

**Disclaimer:** als u deze functie inschakelt, worden uw gegevens gedeeld met externe systemen die u selecteert. U kunt zelf bepalen welke gegevens u aan de derde verstrekt. U begrijpt dat de nalevingsnormen voor gegevensverwerking van de derde kunnen afwijken van die van Microsoft Dynamics 365 Commerce. Uw privacy is belangrijk voor Microsoft. Lees onze [Privacy- en cookieverklaring](https://privacy.microsoft.com/privacystatement) voor meer informatie.

### <a name="create-an-audience-in-site-builder"></a>Een doelgroep maken in Site Builder

Voer de volgende stappen uit om een doelgroep aan te maken in Commerce Site Builder.

1. Selecteer **Doelgroepen** in het deelvenster voor navigatie aan de linkerkant.
1. Selecteer **Nieuw**.
1. Voer een naam voor de doelgroep in. U kunt optioneel ook labels en een omschrijving toevoegen.
1. Selecteer **Aanmaken** en vervolgens **Nieuw regelblok toevoegen**. Een regelblok is een verzameling regels die voldoen aan AND-voorwaarden. U kunt ook meerdere regelblokken aanmaken met OR-voorwaarden ertussen.
1. Selecteer een gegevensbron voor uw segmenten en geef vervolgens de segmentnaam, operator en waarden op. U kunt meer regels in een regelblok aanmaken en verwijderen, of u kunt complete regelblokken aanmaken en verwijderen. U kunt regelblokken ook naar behoefte omhoog of omlaag verplaatsen.

    > [!NOTE]
    > Er kunnen maximaal 100 waarden in een lijst staan, en elk lijstitem kan uit maximaal 50 tekens bestaan.

1. Als u tevreden bent over de configuratie van de doelgroep, selecteert u **Bewerken voltooien**. U kunt vervolgens **Publiceren** selecteren om de doelgroep beschikbaar te maken voor gebruik in een live doel. Als alternatief kunt u de doelgroep samen met het doel publiceren. 

Als u een doelgroep wilt bewerken, selecteert u de hyperlink voor de doelgroep op het tabblad **Doelgroepen** en selecteert u **Bewerken** in de doelgroepeditor die verschijnt. Als u de lijst met doelen en pagina's wilt weergeven die naar een doelgroep verwijzen, selecteert u de doelgroep in de doelgroeplijstweergave en selecteert u vervolgens **Toewijzingen weergeven**. Als u een doelgroep uit de lijstweergave voor doelgroepen of de doelgroepeditor wilt verwijderen, maakt u de publicatie ongedaan als deze al is gepubliceerd en selecteert u vervolgens **Verwijderen** op de opdrachtbalk.

> [!NOTE]
> Een doelgroep is een concept op site-niveau in Commerce Site Builder. U kunt dezelfde doelgroep delen voor meerdere doelen.

## <a name="targets"></a>Doelen

Een doel is de gebruikerservaring die wordt getoond aan leden van een of meer geselecteerde doelgroepen. Een doel kan variaties van een of meer modules op een pagina of in een fragment bevatten. 

U kunt een planning definiëren voor uw doelen om op te geven hoe lang ze actief moeten blijven. Houd er rekening mee dat deze actie los staat van de actie voor het plannen van een publicatiegroep die bepaalt wanneer een verzameling inhoud wordt gepubliceerd. U kunt ook een voorbeeld van uw doelen bekijken om te zien hoe ze er voor de leden van de geselecteerde doelgroepen uit zullen zien. Verder kunt u de prioriteit van uw doelen instellen om op te geven welk doel in geval van een conflict moet worden getoond.

### <a name="create-a-target"></a>Een doel aanmaken

Volg deze stappen om een doel-shell voor paginamodules in Commerce Site Builder aan te maken.

1. Selecteer **Pagina's** in het navigatievenster aan de linkerkant. Selecteer vervolgens de hyperlink voor de pagina met de modules waar u zich op wilt richten.
1. Selecteer **Bewerken** om de pagina uit te checken voor bewerken.
1. Selecteer in het menu **Doel** **Nieuw doel** om een nieuwe doel-shell aan te maken. U kunt op een pagina naar behoefte meerdere doelen aanmaken.
1. Voer een naam en een omschrijving in voor het doel en selecteer **Volgende**.
1. Selecteer **Toevoegen** als u de doelgroepen wilt opnemen die de beoogde inhoud zullen zien of als u doelgroepen wilt uitsluiten. Selecteer **Volgende**.

    > [!NOTE]
    > Een doelgroeptoewijzing is een optionele stap bij het aanmaken van een doel. Voordat u het doel publiceert, moet u echter ten minste één doelgroep opnemen om ervoor te zorgen dat de beoogde groepen gebruikers de beoogde inhoud zien.

1. Definieer het tijdvenster voor de weergave van uw doel door de tijdzone en de begin- en einddatums en -tijden te selecteren. U kunt het doel zo instellen dat het op alle tijden tijdens het venster wordt getoond, of u kunt specifieke dagen en tijden selecteren. Wanneer u klaar bent, selecteert u **Volgende**.

    > [!NOTE]
    > De tijden en tijdzone die u opgeeft, zijn globaal. Als u zich wilt richten op verschillende locaties of in verschillende tijdzones, moet u verschillende doelen aanmaken en de gewenste planning voor elke locatie definiëren.

1. Controleer de gegevens. Wanneer alles er goed uitziet, selecteert u **Doelervaring aanmaken** en vervolgens **Naar doel gaan**. De doel-shell wordt aangemaakt. U kunt er nu modules aan toevoegen.
1. Selecteer de doelmodule, selecteer de ellips (**...**) en selecteer vervolgens **Toevoegen aan het huidige doel**. Wanneer het doel een bovenliggende module is, worden alle modules daaronder deel van dat doel. De doelmodules worden groen gemarkeerd.
1. Maak de gewenste inhoudsupdates voor de beoogde module aan en voeg indien nodig meer modules aan het doel. Selecteer vervolgens **Opslaan** om alle wijzigingen op te slaan.
1. Zorg ervoor dat, voordat het doel wordt gepubliceerd, **Voorbeeld** op de opdrachtbalk is geselecteerd om het doel te bekijken. U kunt vervolgens een van de volgende opties selecteren:

    - **Basisvoorbeeld** - selecteer deze optie als u alleen een voorbeeld van de geselecteerde variatie (standaardpagina of doel) wilt bekijken zonder gekoppelde doelgroepen.
    - **Geavanceerd voorbeeld** - selecteer deze optie als u meerdere doelen op een pagina hebt en daarvan voorbeelden wilt weergeven als een gebruiker die bij een geselecteerde reeks doelgroepen hoort of op een bepaalde datum/tijd. Selecteer **Volgende** om te selecteren in een lijst met relevante doelgroepen. U kunt ook het filter verwijderen om uit alle doelgroepen te kiezen.

1. Als u tevreden bent over de doelconfiguratie, moet u de pagina publiceren om het doel live te laten gaan. Selecteer **Publiceren** om het doel onmiddellijk live te laten gaan. U kunt ook een publicatiegroep gebruiken om te plannen wanneer de pagina live gaat. Zie [Werken met publicatiegroepen](publish-groups.md) voor informatie over publicatiegroepen.

U kunt zich ook op fragmenten richten. De procedure is vergelijkbaar. In stap 1 selecteert u echter **Fragmenten** in plaats van **Pagina's** in het deelvenster voor navigatie aan de linkerkant.

> [!NOTE]
> Om negatieve gevolgen voor uw metrische gegevens te voorkomen, kunt u een experiment of doelen hebben op een pagina of in een fragment. U kunt niet zowel een experiment als een doel hebben.

### <a name="manage-targets"></a>Doelen beheren

Als u doelen wilt bewerken, dupliceren of verwijderen, gaat u naar de standaardpagina of het standaardfragment en volgt u deze stappen.

1. Selecteer in het vervolgkeuzemenu **Doel** en selecteer vervolgens **Doelen beheren**.
1. Selecteer een doel dat u wilt bewerken, dupliceren of verwijderen.
1. Als u meerdere doelen in dezelfde module hebt of als er meerdere doelen zijn met een conflicterende planning, selecteert u **Doelen prioriteren** om de volgorde op te geven waarin ze moeten worden getoond. Als u meerdere doelen op een pagina of in een fragment toevoegt, wordt de knop **Doelen prioriteren** ook weergegeven op de meldingsbalk om u eraan te herinneren de doelen te prioriteren. Als er geen prioriteit is opgegeven, wordt standaard het meest recente doel geselecteerd.

### <a name="localize-targets"></a>Doelen lokaliseren

Doelen op pagina's en in fragmenten worden automatisch opgenomen wanneer XLIFF-bestanden worden geëxporteerd en geïmporteerd voor lokalisatiedoeleinden. Als er echter geen landinstellingen nodig zijn, kunt u de doelen daarvoor verwijderen nadat de gelokaliseerde XLIFF-bestanden zijn geïmporteerd.

> [!NOTE]
> Doelen worden per kanaal en per landinstelling beheerd. Wijzigingen die u doorvoert aan doelen in het ene kanaal of de ene landinstelling worden niet automatisch doorgevoerd naar andere kanalen of landinstellingen.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
