---
title: Power Apps insluiten
description: In dit onderwerp wordt beschreven hoe Power Apps wordt ingesloten in de client om de functionaliteit van het product te verbeteren.
author: jasongre
manager: AnnBe
ms.date: 12/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.openlocfilehash: 90422a34499dab7302ad7722cf84d40e1815991c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042937"
---
# <a name="embed-microsoft-power-apps"></a>Microsoft Power Apps insluiten

[!include [banner](../includes/banner.md)]

Finance and Operations ondersteunt de integratie met Microsoft Power Apps. Dit is een service voor ontwikkelaars en niet-technische gebruikers om aangepaste zakelijke apps te bouwen voor mobiele apparaten, tablets en internet zonder code te hoeven schrijven. Power Apps die zijn ontwikkeld door uzelf, uw organisatie of anderen kunnen vervolgens worden ingesloten in de Finance and Operations-apps om de functionaliteit van het product te verbeteren. U kunt bijvoorbeeld een app van Power Apps bouwen als aanvulling op een Finance and Operations-app met informatie die uit een ander systeem wordt opgehaald.

Voor meer informatie over het insluiten van Power Apps bekijkt u de korte video [PowerApps insluiten in Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-app-from-power-apps-to-a-page"></a>Een ingesloten Power Apps-app toevoegen aan een pagina

### <a name="overview"></a>Overzicht

Voordat u een app van Power Apps in de client kunt insluiten, moet u eerst een app zoeken of maken met de gewenste visuele effecten en/of functionaliteit. Het gedetailleerde proces voor het bouwen van apps wordt hier niet beschreven. Het onderwerp [Inleiding bij Power Apps](https://docs.microsoft.com/powerapps/getting-started) is een goed beginpunt als u niet bekend bent met Power Apps.

Wanneer u klaar bent om een specifieke app in te sluiten, kunt u kiezen tussen twee manieren om toegang te krijgen tot de app op een pagina, afhankelijk van uw scenario. De eerste manier is via de knop Power Apps die is toegevoegd aan het standaard actievenster. Apps die met dit mechanisme zijn toegevoegd, worden als menu-items weergegeven in de menuknop Power Apps. Als u een van deze menu-items selecteert, wordt een zijdeelvenster geopend met de ingesloten app. U kunt een app ook rechtstreeks op een pagina insluiten als een nieuw tabblad, Sneltabblad, blad of als een nieuwe sectie in een werkgebied.

Bij het configureren van uw ingesloten app, kunt u één veld selecteren dat u wilt verzenden als context voor de app. Hierdoor kan de app reageren op basis van de gegevens die u momenteel weergeeft.

### <a name="details"></a>Details

De volgende instructies laten zien hoe u een app van Power Apps insluit in de webclient.

1. Ga naar de pagina waar u de app wilt insluiten. Dit is de pagina die ook alle gegevens bevat die moeten worden doorgegeven aan de app als invoer.
2. Open het deelvenster **Een app van Power Apps** toevoegen:

    - Klik op **Opties** en selecteer **Deze pagina aanpassen**. Kies in het menu **Invoegen** de optie **Power Apps**. Selecteer ten slotte de regio waar u de app wilt toevoegen. Als u de app onder de menuknop Power Apps wilt insluiten, kiest u het actievenster. Als u de app rechtstreeks op de pagina wilt insluiten, kiest u het gewenste tabblad, Sneltabblad, blad of sectie (als u in een werkgebied bent).
    - Als de app wordt benaderd via de menuknop Power Apps, kunt u ook klikken op de menuknop **Power Apps** in het standaard actievenster en vervolgens **Een app invoegen** selecteren.

3. De ingesloten app configureren:

    - Het veld **Naam** geeft de weergegeven tekst aan voor de knop of het tabblad met de ingesloten app. Vaak zult u de naam van de app in dit veld willen herhalen.
    - **App-id** is de GUID voor de app die u wilt insluiten. Als u deze waarde wilt ophalen, gaat u naar de app op [web.powerapps.com](https://web.powerapps.com) en zoekt u het veld **App-id** onder **Details**.
    - Voor **Context invoeren voor de app** kunt u eventueel het veld selecteren dat de gegevens bevat die u als invoer wilt doorgeven aan de app. Raadpleeg de sectie [Een app bouwen die gebruikmaakt van gegevens die vanuit Finance and Operations-apps zijn verzonden](#building-an-app-that-leverages-data-sent-from-finance-and-operations-apps) verderop in dit onderwerp voor meer informatie over hoe de app toegang krijgt tot gegevens uit Finance and Operations-apps.
    - Kies de **Toepassingsgrootte** die overeenkomt met het type app dat u insluit. Selecteer **Dun** voor apps voor mobiele apparaten en **Breed** voor apps voor tablets. Zo zorgt u dat voldoende schijfruimte wordt gereserveerd voor de ingesloten app.
    - Het sneltabblad **Rechtspersonen** biedt de mogelijkheid om te kiezen voor welke rechtspersonen de app beschikbaar is. De standaardwaarde is dat de app voor alle rechtspersonen toegankelijk is. Deze optie is alleen beschikbaar als de functie [Opgeslagen weergaven](saved-views.md) is uitgeschakeld. 

4. Nadat u hebt bevestigd dat de configuratie juist is, klikt u op **Invoegen** om de Power App op de pagina in te sluiten. U wordt gevraagd de browser te vernieuwen om de ingesloten app te kunnen zien.

## <a name="sharing-an-embedded-app"></a>Een ingesloten app delen

Nadat u een app op een pagina hebt ingesloten en hebt bevestigd dat deze correct werkt met de gegevenscontext die wordt doorgegeven vanuit de pagina, wilt u deze mogelijk delen met andere gebruikers in het systeem. Dit kunt doen op twee verschillende manieren met de aanpassingsmogelijkheden van het product:

- Het aanbevolen scenario is via de systeembeheerder, die een aanpassing aan alle gebruikers of een subset van gebruikers kan doorgeven.
- U kunt ook uw aanpassingen op de pagina exporteren en ze naar een of meer gebruikers sturen. Deze gebruikers kunnen uw wijzigingen importeren. Met verschillende acties op de aanpassingswerkbalk kunt u persoonlijke instellingen importeren en exporteren.

Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over de aanpassingsmogelijkheden van het product en het gebruik ervan.

## <a name="building-an-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Een app bouwen die gebruikmaakt van gegevens die vanuit Finance and Operations-apps zijn verzonden

Een belangrijk onderdeel van het bouwen van een app van Power Apps die wordt ingesloten in een Finance and Operations-app, maakt gebruik van de invoergegevens van die toepassing. Vanuit de Power Apps-ontwikkelervaring kunt u toegang krijgen tot de invoergegevens afkomstig uit een Finance and Operations-app met behulp van de variabele Param("EntityId").

Voor de functie OnStart van de app kunt u de invoergegevens van Finance and Operations-apps bijvoorbeeld instellen op een variabele als hieronder:

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-app"></a>Een app weergeven

Als u een ingesloten app wilt weergeven op een pagina in Finance and Operations-apps, gaat u naar een pagina met een ingesloten app. Apps zijn toegankelijk via de knop Power Apps in het standaard actievenster. Ook kunnen ze rechtstreeks op de pagina worden weergegeven als een nieuw tabblad, een sneltabblad of blad of als een nieuwe sectie in een werkgebied. Wanneer een gebruiker een app voor het eerst probeert te laden op een pagina, wordt gevraagd om de aanmeldgegevens, zodat de gebruiker de juiste machtigingen heeft bij het gebruiken van de app.

## <a name="editing-an-embedded-app"></a>Een ingesloten app bewerken

Nadat een app is ingesloten op een pagina, moet u mogelijk enkele wijzigingen aanbrengen in de configuratie van die app. U wilt misschien het label wijzigen dat is gekoppeld aan de ingesloten app of er is een nieuwe versie van een app gemaakt en u moet de App-id bijwerken met de meest recente app.

Ga als volgt te werk om de configuratie van een ingesloten app te bewerken:

1. Ga naar het deelvenster **De app bewerken**.

    - Als de ingesloten app via de menuknop Power Apps wordt geopend, klikt u met de rechtermuisknop op de menuknop Power Apps en selecteert u **Aanpassen**. Selecteer de app die u wilt configureren vanuit de vervolgkeuzelijst **Een app selecteren**.
    - Als de ingesloten app rechtstreeks op de pagina wordt weergegeven, selecteert u **Opties** en vervolgens **Deze pagina aanpassen**. Klik met de functie **Selecteren** op de ingesloten app.

2. Breng de benodigde wijzigingen aan in de appconfiguratie en klik op **Opslaan**.

## <a name="removing-an-app"></a>Een app verwijderen

Nadat een app is ingesloten op een pagina, zijn er twee manieren om deze te verwijderen:

- Ga naar het deelvenster **Een app bewerken** aan de hand van de instructies in [Een ingesloten app bewerken](#editing-an-embedded-app) hierboven. Bevestig dat het deelvenster de informatie bevat voor de ingesloten app die u wilt verwijderen en klik op de knop **Verwijderen**.
- Omdat de ingesloten app wordt opgeslagen als persoonlijke gegevens, worden bij het wissen van aanpassingen op uw pagina ook eventuele ingesloten apps op die pagina verwijderd. Houd er rekening mee dat het wissen van de aanpassingen van de pagina definitief is. Als u uw aanpassingen op een pagina wilt verwijderen, selecteert u **Opties** en klikt u op **Deze pagina aanpassen** en tot slot op de knop **Wissen**. Na het vernieuwen van uw browser worden alle vorige aanpassingen voor deze pagina verwijderd. Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over het optimaliseren van pagina's met aanpassingen.

## <a name="appendix"></a>Bijlage

### <a name="developer-control-over-where-an-app-can-be-embedded"></a>Ontwikkelaars bepalen waar een app kan worden ingesloten

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
