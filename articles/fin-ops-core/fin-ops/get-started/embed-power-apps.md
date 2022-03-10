---
title: Canvas-apps insluiten vanuit Power Apps
description: In dit onderwerp wordt uitgelegd hoe u canvas-apps vanuit Microsoft Power Apps kunt insluiten in de client om de functionaliteit van het product te verbeteren.
author: jasongre
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: c2f7b660d364be6e62d484e67908201027190a8a
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2022
ms.locfileid: "8065096"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Canvas-apps insluiten vanuit Power Apps

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Microsoft Power Apps is een service waarmee ontwikkelaars en niet-technische gebruikers aangepaste zakelijke apps kunnen maken voor mobiele apparaten, tablets en het web zonder code te hoeven schrijven. Apps voor financiële en bedrijfsactiviteiten bieden ondersteuning voor integratie met Power Apps. Canvas-apps die u, uw organisatie of anderen ontwikkelen, kunnen worden ingesloten in apps voor financiële en bedrijfsactiviteiten om de functionaliteit van het product te verbeteren. U kunt bijvoorbeeld een canvas-app maken in Power Apps als aanvulling op een app voor financiële en bedrijfsactiviteiten met informatie die uit een ander systeem wordt opgehaald.

Voor meer informatie over het insluiten van canvas-apps bekijkt u de korte video [Canvas-apps insluiten](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Een ingesloten canvas-app vanuit Power Apps toevoegen aan een pagina

Voordat u een canvas-app vanuit Power Apps in de client insluit, moet u eerst een app zoeken of maken met de gewenste visuele effecten of functionaliteit. Dit onderwerp bevat geen gedetailleerde beschrijving van het proces voor het maken van apps. Als u Power Apps voor het eerst gebruikt, raadpleegt u de [Power Apps-documentatie](/powerapps/).

U kunt op drie manieren een canvas-app in een app voor financiële en bedrijfsactiviteiten insluiten. U kunt de aanpak gebruiken die het beste bij uw scenario past. 

- Plaats de canvas-app in de knop **Power Apps** in het standaardactievenster van een pagina. Apps die u op deze manier toevoegt, worden als items op de menuknop **Power Apps** weergegeven en de apps worden geopend in zijvensters. 
- Sluit de canvas-app rechtstreeks in op een bestaande pagina als een nieuw tabblad (draaitabblad, sneltabblad, blad of werkgebiedsectie).
- Maak een volledige nieuwe pagina voor de canvas-app vanuit het dashboard.

Als u uw ingesloten canvas-app configureert, kunt u één veld selecteren dat u als context naar de app wilt verzenden. Met deze stap kan de app reageren op basis van de gegevens die u momenteel weergeeft.

> [!NOTE]
> U kunt dit mechanisme niet gebruiken om modelgestuurde apps in te sluiten.

### <a name="embedding-a-canvas-app-on-an-existing-page"></a>Een canvas-app op een bestaande pagina insluiten

De volgende procedure laat zien hoe u vanuit Power Apps een canvas-app op een bestaande pagina insluit.

1. Ga naar de pagina waar u de canvas-app wilt insluiten. Deze pagina bevat alle gegevens die als invoer moeten worden doorgegeven aan de app.
2. Open het deelvenster **Een app van Power Apps** toevoegen:

    - Als de app rechtstreeks op de pagina wordt ingesloten, selecteert u **Opties** \> **Deze pagina aanpassen** \> **Meer** en volgt u een van deze stappen:

        - Als de functie **Apps op volledige pagina** is ingeschakeld, selecteert u **Een pagina toevoegen** en selecteert u vervolgens de regio waar u de app wilt toevoegen. Selecteer het actievenster om de app in te sluiten in de menuknop **Power Apps**. Als u de app rechtstreeks op de pagina wilt insluiten, selecteert u het gewenste tabblad, sneltabblad, blad of sectie (als u zich in een werkgebied bevindt). Selecteer vervolgens in het deelvenster **Een app toevoegen** de optie **Power Apps**.
        - Als de functie **Apps op volledige pagina** is ingeschakeld, selecteert u **Een app van Power Apps toevoegen** en selecteert u vervolgens de regio waar u de app wilt toevoegen. Selecteer het actievenster om de app in te sluiten in de menuknop **Power Apps**. Als u de app rechtstreeks op de pagina wilt insluiten, selecteert u het gewenste tabblad, sneltabblad, blad of sectie (als u zich in een werkgebied bevindt).

    - Als de app moet worden geopend via de menuknop **Power Apps**, kunt u de menuknop **Power Apps** in het standaardactievenster selecteren en vervolgens **Een app toevoegen** selecteren.

3. Configureer de ingesloten app. Zie de sectie [Een canvas-app configureren](#configuring-a-canvas-app) verderop in dit onderwerp voor meer informatie.
4. Nadat u hebt bevestigd dat de configuratie juist is, selecteert u **Invoegen**.

    - Als de functie **Opgeslagen weergaven** is uitgeschakeld, wordt u gevraagd om de browser te vernieuwen om de ingesloten app weer te geven.
    - Als de functie **Opgeslagen weergaven** is ingeschakeld, moet u de weergave opslaan om de wijziging door te voeren.

### <a name="embedding-a-canvas-app-as-a-full-page-experience-from-the-dashboard"></a>Een canvas-app als een volledige pagina vanuit het dashboard insluiten

U wilt een canvas-app mogelijk vanuit het dashboard insluiten als de app niet is gekoppeld aan een bestaande pagina of als u de app alleen maar als een volledige pagina wilt weergeven in de app voor financiële en bedrijfsactiviteiten.

> [!NOTE]
> Als u deze mogelijkheid beschikbaar wilt maken, moet u de functie **Apps op volledige pagina** in Functiebeheer inschakelen. 

1. Open het dashboard.
2. Selecteer de pagina en houd deze vast (of klik erop met de rechtermuisknop), selecteer **Personaliseren** en selecteer vervolgens **Een pagina toevoegen**.
3. Selecteer in het deelvenster **Een pagina toevoegen** de optie **Power Apps**.
4. Configureer de ingesloten app. Zie de sectie [Een canvas-app configureren](#configuring-a-canvas-app) verderop in dit onderwerp voor meer informatie.
5. Selecteer **Opslaan** om de app aan het dashboard toe te voegen als een nieuwe tegel.
6. Selecteer de nieuwe tegel op het dashboard en controleer of de canvas-app wordt weergegeven zoals u verwacht.

### <a name="configuring-a-canvas-app"></a>Een canvas-app configureren

Wanneer u een canvas-app insluit, moet u de volgende parameters instellen:

- **Naam**: voer de tekst in die moet worden weergegeven op de knop of het tabblad met de ingesloten app. U wilt de naam van de app in dit veld mogelijk vaak herhalen.
- **App-id**: geef de GUID (Globally Unique Identifier) op voor de canvas-app die u wilt insluiten. Als u deze waarde wilt ophalen, gaat u naar de app op [make.powerapps.com](https://make.powerapps.com) en zoekt u in het veld **App-id** onder **Details**.
- **Context invoeren voor de app**: u kunt eventueel het veld selecteren met de gegevens die u als invoer wilt doorgeven aan de app. Raadpleeg de sectie [Een app bouwen die gebruikmaakt van gegevens die zijn verzonden uit apps voor financiële en bedrijfsactiviteiten](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) verderop in dit onderwerp voor meer informatie over hoe de app toegang krijgt tot de gegevens die zijn verzonden uit apps voor financiële en bedrijfsactiviteiten.

    Vanaf versie 10.0.19 wordt de huidige rechtspersoon ook als context aan de canvas-app doorgegeven via de URL-parameter **cmp**. Dit gedrag is pas van invloed op de doelcanvas-app als de app die informatie gebruikt.

- **Toepassingsgrootte**: selecteer het type app dat dat u insluit. Selecteer **Dun** voor apps die zijn gemaakt voor mobiele apparaten of **Breed** voor apps die zijn gemaakt voor tablets. Met deze parameter zorgt u ervoor dat er voldoende ruimte wordt toegewezen voor de ingesloten app.
- **Rechtspersonen**: u kunt de rechtspersonen selecteren voor wie de app beschikbaar moet zijn. De app is standaard beschikbaar voor alle rechtspersonen. Deze optie is alleen beschikbaar wanneer u de app rechtstreeks op een bestaande pagina insluit en de functie **[Opgeslagen weergave](saved-views.md)** is uitgeschakeld.

## <a name="sharing-an-embedded-app"></a>Een ingesloten app delen

Nadat u een canvas-app op een pagina hebt ingesloten en hebt bevestigd dat deze correct werkt, kunt u de app met andere gebruikers in het systeem delen. Voer de volgende stappen uit om een ingesloten canvas-app te delen.

1. [Deel de canvas-app in Power Apps](/powerapps/maker/canvas-apps/share-app) met de gewenste gebruikers, zodat ze rechtstreeks vanuit Power Apps toegang kunnen krijgen tot de app.
2. Deel de aanpassingen die aan de ingesloten app zijn gekoppeld met de gewenste gebruikers. U kunt een van de twee volgende methoden gebruiken:

    - **De weergave publiceren (aanbevolen):** als de functie **[Opgeslagen weergaven](saved-views.md)** is ingeschakeld, is de aanbevolen benadering dat u een weergave maakt met de ingesloten canvas-app en die weergave vervolgens publiceert naar de gewenste gebruikers. Deze benadering zorgt ervoor dat de canvas-app voor alle gebruikers met beveiligingsrollen voor de gepubliceerde weergave op de pagina wordt weergegeven.

        U kunt ook een canvas-app publiceren die als volledige pagina vanuit het dashboard is ingesloten. Selecteer op het dashboard de tegel die aan de app is gekoppeld en houd deze vast (of klik erop met de rechtermuisknop), selecteer **Personaliseren** en selecteer vervolgens **Pagina publiceren**. Een ervaring die lijkt op de ervaring met *Publicatieweergaven* wordt weergegeven en u kunt de beveiligingsrollen selecteren waarvoor gepubliceerd moet worden. Als u bij update 10.0.21 of hoger de **Verbeterde ondersteuning van de rechtspersoon voor opgeslagen weergaven** hebt ingeschakeld, kunt u de app ook publiceren naar de gewenste rechtspersonen.

    - Als de functie **Opgeslagen weergaven** is uitgeschakeld, kan de systeembeheerder een aanpassing doen waarin de canvas-app wordt toegevoegd aan de juiste gebruikers via de pagina **Persoonlijke instellingen**. U kunt de persoonlijke instellingen van uw pagina ook exporteren en deze vervolgens naar een of meer gebruikers verzenden. Elke gebruiker kan de persoonlijke instellingen vervolgens importeren. De werkbalk met persoonlijke instellingen bevat knoppen waarmee u persoonlijke instellingen kunt importeren en exporteren.

> [!NOTE]
> Als de canvas-app met externe gebruikers is gedeeld, kunnen deze gebruikers de ingesloten app niet in apps voor financiële en bedrijfsactiviteiten gebruiken. Ze kunnen echter rechtstreeks toegang krijgen tot de app in Power Apps. Externe gebruikers zijn gasten en gebruikers die niet behoren tot de Microsoft 365 Azure Directory waar de app voor financiële en bedrijfsactiviteiten wordt geïmplementeerd.

Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over de aanpassingsmogelijkheden van het product en het gebruik ervan.

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Een canvas-app maken waarin gegevens worden gebruikt die vanuit apps voor financiële en bedrijfsactiviteiten worden verzonden

Wanneer u een canvas-app maakt die in een app voor financiële en bedrijfsactiviteiten wordt ingesloten, is een belangrijk onderdeel van het proces dat u de invoergegevens van die app voor financiële en bedrijfsactiviteiten gebruikt. Vanuit de Power Apps-ontwikkelervaring kunt u toegang krijgen tot de invoergegevens die vanuit een app voor financiële en bedrijfsactiviteiten worden doorgegeven met de variabele **Param("EntityId")**. Daarnaast wordt vanaf versie 10.0.19 de huidige rechtspersoon ook doorgegeven naar de canvas-app via de variabele **Param("cmp")**. 

Voor de functie OnStart van de app kunt u de invoergegevens van apps voor financiële en bedrijfsactiviteiten bijvoorbeeld instellen op een variabele als hieronder:

``` Power Apps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));

If(!IsBlank(Param("cmp")), Set(FinOpsLegalEntity, Param("cmp")), Set(FinOpsLegalEntity, ""));
```

## <a name="viewing-a-canvas-app"></a>Een canvas-app weergeven

Als u een ingesloten canvas-app wilt weergeven op een pagina in apps voor financiële en bedrijfsactiviteiten, gaat u naar een pagina die een ingesloten app bevat. U kunt toegang krijgen tot apps via de knop **Power Apps** in het standaardactievenster. Apps kunnen ook rechtstreeks op de pagina worden weergegeven als een nieuw tabblad, sneltabblad, blad of als een nieuwe sectie in een werkgebied. Wanneer gebruikers voor het eerst een app proberen te laden op een pagina, wordt hen gevraagd om zich aan te melden. Met deze stap wordt ervoor gezorgd dat de gebruikers over de juiste machtigingen beschikken om de app te gebruiken.

## <a name="editing-an-embedded-app"></a>Een ingesloten app bewerken

Nadat een app is ingesloten op een pagina, moet u mogelijk enkele wijzigingen aanbrengen in de configuratie van die app. U wilt misschien het label wijzigen dat is gekoppeld aan de ingesloten app of er is een nieuwe versie van een app gemaakt en u moet de App-id bijwerken met de meest recente app.

Ga als volgt te werk om de configuratie van een ingesloten app te bewerken:

1. Ga naar het deelvenster **De app bewerken**.

    - Als de ingesloten app via de menuknop Power Apps wordt geopend, houdt u de menuknop Power Apps ingedrukt (of klikt u met de rechtermuisknop op de menuknop) en selecteert u **Aanpassen**. Selecteer de app die u wilt configureren vanuit de vervolgkeuzelijst **Een app selecteren**.
    - Als de ingesloten app rechtstreeks op de pagina wordt weergegeven, selecteert u **Opties** en vervolgens **Deze pagina aanpassen**. Klik met de functie **Selecteren** op de ingesloten app.
    - Als de ingesloten app is toegevoegd vanuit het dashboard, opent u het dashboard, houdt u de tegel ingedrukt die aan de canvas-app is gekoppeld (of klikt u met de rechtermuisknop op de tegel), selecteert u **Aanpassen** en selecteert u vervolgens **Pagina bewerken**.

2. Breng de benodigde wijzigingen aan in de appconfiguratie en klik op **Opslaan**.

## <a name="removing-an-app"></a>Een app verwijderen

Nadat een app is ingesloten op een pagina, zijn er een paar manieren om deze indien nodig te verwijderen:

- Ga naar het deelvenster **Een app bewerken** aan de hand van de instructies in [Een ingesloten app bewerken](#editing-an-embedded-app) hierboven. Bevestig dat het deelvenster de informatie bevat voor de ingesloten app die u wilt verwijderen en klik op de knop **Verwijderen**.
- Als de ingesloten app is toegevoegd vanuit het dashboard, opent u het dashboard, houdt u de tegel ingedrukt die aan de canvas-app is gekoppeld (of klikt u met de rechtermuisknop op de tegel), selecteert u **Aanpassen** en selecteert u vervolgens **Pagina verwijderen**. 
- Omdat de ingesloten app wordt opgeslagen als persoonlijke gegevens, worden bij het wissen van aanpassingen op uw pagina ook eventuele ingesloten apps op die pagina verwijderd. Houd er rekening mee dat het wissen van de aanpassingen van de pagina definitief is. Als u uw aanpassingen op een pagina wilt verwijderen, selecteert u **Opties** en klikt u op **Deze pagina aanpassen** en tot slot op de knop **Wissen**. Na het vernieuwen van uw browser worden alle vorige aanpassingen voor deze pagina verwijderd. Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over het optimaliseren van pagina's met aanpassingen.

## <a name="appendix"></a>Bijlage

### <a name="developer-modeling-a-canvas-app-on-a-form"></a>[Ontwikkelaar] Een canvas-app modelleren op een formulier

In dit onderwerp wordt besproken hoe canvas-apps door middel van personalisatie kunnen worden ingesloten, maar ontwikkelaars kunnen met behulp van de Visual Studio-ontwikkelervaring ook een canvas-app toevoegen aan een formulier. Hiervoor voegt u gewoon een PowerAppsHostControl toe aan het formulier. De metagegevenseigenschappen die beschikbaar zijn in het besturingselement, bieden dezelfde mogelijkheden als personalisatie.

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>\[Ontwikkelaar\]: opgeven waar een app kan worden ingesloten

Standaard kunt u apps op elke pagina insluiten, hetzij onder de menuknop Power Apps, hetzij rechtstreeks op de pagina als een tabblad, sneltabblad, blad of als een nieuwe sectie in een werkgebied. Indien nodig kunnen ontwikkelaars deze functie echter ook zo configureren dat het insluiten van apps alleen is toegestaan op bepaalde pagina's door het implementeren van de volgende methoden:

- **isPowerAppPersonalizationEnabled**: als deze methode een fout voor een bepaalde pagina retourneert, wordt de menuknop Power Apps niet weergegeven en kunnen gebruikers geen apps insluiten op een willekeurige plaats op deze pagina, met inbegrip van tabbladen.
- **isPowerAppTabPersonalizationEnabled**: als deze methode een fout voor een bepaalde pagina retourneert, kunnen gebruikers apps niet rechtstreeks insluiten op de pagina als een tabblad, sneltabblad of een panoramasectie. Gebruikers kunnen nog wel apps insluiten via de menuknop Power Apps als op de pagina insluiten is toegestaan.

Het volgende voorbeeld toont een nieuwe klasse met de twee methoden die nodig zijn voor het configureren van de plaats waar apps kunnen worden ingesloten.

```powerapps
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return result;
    }
    
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return result;
    }
}
```

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
