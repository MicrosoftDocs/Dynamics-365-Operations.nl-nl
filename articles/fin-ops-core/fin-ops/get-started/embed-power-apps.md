---
title: Power Apps insluiten
description: In dit onderwerp wordt beschreven hoe Power Apps wordt ingesloten in de client om de functionaliteit van het product te verbeteren.
author: jasongre
manager: AnnBe
ms.date: 09/20/2019
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
ms.openlocfilehash: 755a30f89725ca0a7e1c14252984c617d6ba280e
ms.sourcegitcommit: 4162d9ef4239c9d4e5297b8aaa903dd54f9cafc3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/21/2019
ms.locfileid: "2824488"
---
# <a name="embed-microsoft-power-apps"></a>Microsoft Power Apps insluiten

[!include [banner](../includes/banner.md)]

In Platformupdate 14 wordt de integratie met Microsoft Power Apps ondersteund. Dit is een service voor ontwikkelaars en niet-technische gebruikers om aangepaste bedrijfsapps te bouwen voor mobiele apparaten, tablets en internet zonder code te hoeven schrijven. Power Apps die zijn ontwikkeld door uzelf, uw organisatie of anderen kunnen vervolgens worden ingesloten in de Finance and Operations-apps om de functionaliteit van het product te verbeteren. U kunt bijvoorbeeld een Power App maken als aanvulling op Finance and Operations-apps met informatie die uit een ander systeem is opgehaald.

Voor meer informatie over het insluiten van Power Apps bekijkt u de korte video [PowerApps insluiten in Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-power-app-to-a-page"></a>Een ingesloten Power App toevoegen aan een pagina

### <a name="overview"></a>Overzicht

Voordat u een Power App kunt insluiten in de client, moet u eerst een Power App zoeken of maken met de gewenste visuele effecten en/of functionaliteit. Het gedetailleerde proces voor het bouwen van een Power App wordt hier niet beschreven. Het onderwerp [Inleiding bij Power Apps](https://docs.microsoft.com/powerapps/getting-started) is een goed beginpunt als u niet bekend bent met Power Apps.

Wanneer u klaar bent om een specifieke Power App in te sluiten, kunt u kiezen tussen twee manieren om toegang te krijgen tot de Power App op een pagina, afhankelijk van uw scenario. De eerste manier is via de knop Power Apps die is toegevoegd aan het standaard actievenster. Power Apps die met dit mechanisme zijn toegevoegd, worden als menu-items weergegeven in de menuknop Power Apps. Als u een van deze menu-items selecteert, wordt een zijdeelvenster geopend met de ingesloten Power App. U kunt een Power App ook rechtstreeks op een pagina weergeven als een nieuw tabblad, Sneltabblad, blad of als een nieuwe sectie in een werkgebied.

Bij het configureren van uw ingesloten Power App, kunt u één veld selecteren dat u wilt verzenden als invoer voor de Power App. Hierdoor kan de Power App reageren op basis van de gegevens die u momenteel weergeeft.

### <a name="details"></a>Details

De volgende instructies laten zien hoe u een Power App insluit in de webclient.

1. Ga naar de pagina waar u de Power App wilt insluiten. Dit is de pagina die ook alle gegevens bevat die moeten worden doorgegeven aan de Power App als invoer.
2. Open het deelvenster **Een Power App invoegen**:

    - Klik op **Opties** en selecteer vervolgens **Dit formulier aanpassen**. Kies in het menu **Invoegen** de optie **Power App**. Selecteer ten slotte de regio waar u de Power App wilt toevoegen. Als u de Power App onder de menuknop Power Apps wilt insluiten, kiest u het Actievenster. Als u de Power App rechtstreeks op de pagina wilt insluiten, kiest u het gewenste tabblad, Sneltabblad, blad of sectie (als u in een werkgebied bent).
    - Als de Power App wordt benaderd via de menuknop Power Apps, kunt u ook klikken op de menuknop **Power Apps** in het standaard Actievenster en vervolgens **Een Power App invoegen** selecteren.

3. De ingesloten Power App configureren:

    - Het veld **Naam** geeft de weergegeven tekst aan voor de knop of het tabblad met de ingesloten Power App. Vaak zult u de naam van de Power App in dit veld willen herhalen.
    - **App-id** is de GUID voor de Power App die u wilt insluiten. Als u deze waarde wilt ophalen, gaat u naar de Power App op [web.powerapps.com](https://web.powerapps.com) en zoekt u het veld **App-id** onder **Details**.
    - Voor **Gegevens invoeren voor de Power App** kunt u eventueel het veld selecteren dat de gegevens bevat die u als invoer wilt doorgeven aan de Power App. Raadpleeg de sectie [Een Power App bouwen die gebruikmaakt van gegevens uit Finance and Operations-apps](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations-apps) verderop in dit onderwerp voor meer informatie over hoe de Power App toegang krijgt tot gegevens uit Finance and Operations-apps.
    - Kies de **toepassingsgrootte** die overeenkomt met het type Power App dat u insluit. Selecteer **Dun** voor Power Apps voor mobiele apparaten en **Breed** voor Power Apps voor tabletten. Zo zorgt u dat voldoende schijfruimte wordt gereserveerd voor de ingesloten Power App.
    - Het sneltabblad **Rechtspersonen** biedt de mogelijkheid om te kiezen voor welke rechtspersonen de Power App beschikbaar is. De standaardwaarde is dat de Power App voor alle rechtspersonen wordt weergegeven.

4. Nadat u hebt bevestigd dat de configuratie juist is, klikt u op **Invoegen** om de Power App op de pagina in te sluiten. U wordt gevraagd om de browser te vernieuwen om de ingesloten Power App te kunnen zien.

## <a name="sharing-an-embedded-power-app"></a>Een ingesloten Power App delen

Nadat u een Power App op een pagina hebt ingesloten en hebt bevestigd dat deze correct werkt met de gegevenscontext die wordt doorgegeven vanuit de pagina, wilt u mogelijk deze ingesloten Power App delen met andere gebruikers in het systeem. Dit kunt doen op twee verschillende manieren met de aanpassingsmogelijkheden van het product:

- Het aanbevolen scenario is via de systeembeheerder, die een aanpassing aan alle gebruikers of een subset van gebruikers kan doorgeven.
- U kunt ook uw aanpassingen op de pagina exporteren en ze naar een of meer gebruikers sturen. Deze gebruikers kunnen uw wijzigingen importeren. Met de optie Beheren op de aanpassingswerkbalk kunt u persoonlijke instellingen importeren en exporteren.

Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over de aanpassingsmogelijkheden van het product en het gebruik ervan.

## <a name="building-a-power-app-that-leverages-data-sent-from-finance-and-operations-apps"></a>Een Power App bouwen die gebruikmaakt van gegevens uit Finance and Operations-apps

Een belangrijk onderdeel van het bouwen van een Power App die wordt ingesloten in Finance and Operations-apps is het gebruiken van invoergegevens uit Finance and Operations-apps. In de Power App zijn die invoergegevens beschikbaar via de variabele Param("EntityId").

Voor de functie OnStart van de Power App kunt u de invoergegevens van Finance and Operations-apps bijvoorbeeld instellen op een variabele als hieronder:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-power-app"></a>Een ingesloten Power App weergeven

Als u een ingesloten Power App wilt weergeven op een pagina in Finance and Operations-apps, gaat u naar een pagina met een ingesloten Power App. Power Apps zijn toegankelijk via de knop Power Apps in het standaard Actievenster. Ook kunnen ze rechtstreeks op de pagina worden weergegeven als een nieuw tabblad, een sneltabblad of blad of als een nieuwe sectie in een werkgebied. Wanneer een gebruiker een Power App voor het eerst probeert te laden op een pagina, wordt gevraagd om de aanmeldgegevens voor Power Apps zodat de gebruiker de juiste machtigingen heeft bij het gebruiken van de Power App.

## <a name="editing-an-embedded-power-app"></a>Een ingesloten Power App bewerken

Nadat een Power App is ingesloten op een pagina, moet u mogelijk enkele wijzigingen aanbrengen in de configuratie van die Power App. U wilt misschien het label wijzigen dat is gekoppeld aan de ingesloten Power App of er is een nieuwe versie van een PowerApp gemaakt en u moet de App-id bijwerken met de meest recente Power App.

Ga als volgt te werk om de configuratie van een ingesloten Power App te bewerken:

1. Ga naar het deelvenster **Een Power App bewerken**.

    - Als de ingesloten Power App via de menuknop Power Apps wordt geopend, klikt u met de rechtermuisknop op de menuknop Power Apps en selecteert u **Aanpassen**. Selecteer de Power App die u wilt configureren vanuit de vervolgkeuzelijst **Power App selecteren**.
    - Als de ingesloten Power App rechtstreeks op de pagina wordt weergegeven, selecteert u **Opties** en vervolgens **Dit formulier aanpassen**. Klik met de functie **Selecteren** op de ingesloten Power App.

2. Breng de benodigde wijzigingen aan in de Power Apps-configuratie en klik op **Opslaan**.

## <a name="removing-an-embedded-power-app"></a>Een ingesloten Power App verwijderen

Nadat een Power App is ingesloten op een pagina, zijn er twee manieren om deze te verwijderen:

- Ga naar het deelvenster **Een Power App bewerken** aan de hand van de instructies in [Een ingesloten Power App bewerken](#editing-an-embedded-powerapp) hierboven. Bevestig dat het deelvenster de informatie bevat voor de ingesloten Power App die u wilt verwijderen en klik op de knop **Verwijderen**.
- Omdat een ingesloten Power App wordt opgeslagen als persoonlijke gegevens, worden bij het wissen van aanpassingen op uw pagina ook eventuele ingesloten Power Apps op die pagina verwijderd. Houd er rekening mee dat het wissen van de aanpassingen van de pagina definitief is. Als u uw aanpassingen op een pagina wilt verwijderen, selecteert u **Opties** en klikt u vervolgens op **Dit formulier aanpassen**. Selecteer onder het menu **Beheren** de knop **Wissen**. Na het vernieuwen van uw browser worden alle vorige aanpassingen voor deze pagina verwijderd. Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over het optimaliseren van pagina's met aanpassingen.

## <a name="appendix"></a>Bijlage

### <a name="developer-control-over-where-a-power-app-can-be-embedded"></a>Ontwikkelaars bepalen waar een Power App kan worden ingesloten

Standaard kunt u Power Apps op elke pagina insluiten, hetzij onder de menuknop Power Apps, hetzij rechtstreeks op de pagina als een tabblad, sneltabblad, blad of als een nieuwe sectie in een werkgebied. Indien nodig kunnen ontwikkelaars deze functie echter ook zo configureren dat het insluiten van Power Apps alleen is toegestaan op bepaalde pagina's door het implementeren van de volgende methoden:

- **isPowerAppPersonalizationEnabled**: als deze methode een fout voor een bepaalde pagina retourneert, wordt de menuknop Power Apps niet weergegeven en kunnen gebruikers geen Power Apps insluiten op een willekeurige plaats op deze pagina, met inbegrip van tabbladen.
- **isPowerAppTabPersonalizationEnabled**: als deze methode een fout voor een bepaalde pagina retourneert, kunnen gebruikers Power Apps niet rechtstreeks insluiten op de pagina als een tabblad, sneltabblad of een panoramasectie. Gebruikers kunnen nog wel Power Apps insluiten via de menuknop Power Apps als op de pagina insluiten is toegestaan.

Het volgende voorbeeld toont een nieuwe klasse met de twee methoden die nodig zijn voor het configureren van de plaats waar Power Apps kunnen worden ingesloten.

```
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
