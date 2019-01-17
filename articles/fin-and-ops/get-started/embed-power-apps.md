---
title: PowerApps insluiten
description: In dit onderwerp wordt beschreven hoe PowerApps worden ingesloten in de Finance and Operations-client om de functionaliteit van het product te verbeteren.
author: jasongre
manager: AnnBe
ms.date: 09/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FormRunConfigurationAddPAControl, FormRunConfigurationEditPAControl
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: Platform update 14
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 262d34cbc50251595d22c27387fbd3f1045d1fbb
ms.contentlocale: nl-nl
ms.lasthandoff: 12/18/2018

---

# <a name="embed-powerapps-apps"></a>PowerApps insluiten

[!include [banner](../includes/banner.md)]

In Platformupdate 14 voor Microsoft Dynamics 365 for Finance and Operations wordt de integratie met Microsoft PowerApps ondersteund. Dit is een service voor ontwikkelaars en niet-technische gebruikers om aangepaste bedrijfsapps te bouwen voor mobiele apparaten, tablets en internet zonder code te hoeven schrijven. PowerApps die zijn ontwikkeld door uzelf, uw organisatie of anderen kunnen vervolgens worden ingesloten in de Finance and Operations-client om de functionaliteit van het product te verbeteren. U kunt bijvoorbeeld een PowerApp maken als aanvulling op Finance and Operations met informatie die uit een ander systeem is opgehaald.

Voor meer informatie over het insluiten van PowerApps bekijkt u de korte video [PowerApps insluiten in Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-powerapp-to-a-page"></a>Een ingesloten PowerApp toevoegen aan een pagina

### <a name="overview"></a>Overzicht

Voordat u een PowerApp kunt insluiten in de Finance and Operations-client, moet u eerst een PowerApp zoeken of maken met de gewenste visuele effecten en/of functionaliteit. Het gedetailleerde proces voor het bouwen van een PowerApp wordt hier niet beschreven. Het onderwerp [Inleiding bij PowerApps](https://docs.microsoft.com/powerapps/getting-started) is een goed beginpunt als u niet bekend bent met PowerApps.

Wanneer u klaar bent om een specifieke PowerApp in te sluiten, kunt u kiezen tussen twee manieren om toegang te krijgen tot de PowerApp op een pagina, afhankelijk van uw scenario. De eerste manier is via de knop PowerApps die is toegevoegd aan het standaard actievenster. PowerApps die met dit mechanisme zijn toegevoegd, worden als menu-items weergegeven in de menuknop PowerApps. Als u een van deze menu-items selecteert, wordt een zijdeelvenster geopend met de ingesloten PowerApp. U kunt een PowerApp ook rechtstreeks op een pagina weergeven als een nieuw tabblad, Sneltabblad, blad of als een nieuwe sectie in een werkgebied.

Bij het configureren van uw ingesloten PowerApp in Finance and Operations, kunt u één veld selecteren dat u wilt verzenden als invoer voor de PowerApp. Hierdoor kan de PowerApp reageren op basis van de gegevens die u momenteel weergeeft in Finance and Operations.

### <a name="details"></a>Details

De volgende instructies laten zien hoe u een PowerApp insluit in de webclient Finance and Operations.

1. Ga naar de pagina waar u de PowerApp wilt insluiten. Dit is de pagina die ook alle gegevens bevat die moeten worden doorgegeven aan de PowerApp als invoer.
2. Open het deelvenster **Een PowerApp invoegen**:

    - Klik op **Opties** en selecteer vervolgens **Dit formulier aanpassen**. Kies in het menu **Invoegen** de optie **PowerApp**. Selecteer ten slotte de regio waar u de PowerApp wilt toevoegen. Als u de PowerApp onder de menuknop PowerApps wilt insluiten, kiest u het Actievenster. Als u de PowerApp rechtstreeks op de pagina wilt insluiten, kiest u het gewenste tabblad, Sneltabblad, blad of sectie (als u in een werkgebied bent).
    - Als de PowerApp wordt benaderd via de menuknop PowerApps, kunt u ook klikken op de menuknop **PowerApps** in het standaard Actievenster en vervolgens **Een PowerApp invoegen** selecteren.

3. De ingesloten PowerApp configureren:

    - Het veld **Naam** geeft de weergegeven tekst aan voor de knop of het tabblad met de ingesloten PowerApp. Vaak zult u de naam van de PowerApp in dit veld willen herhalen.
    - **App-id** is de GUID voor de PowerApp die u wilt insluiten. Als u deze waarde wilt ophalen, gaat u naar de PowerApp op [web.powerapps.com](https://web.powerapps.com) en zoekt u het veld **App-id** onder **Details**.
    - Voor **Gegevens invoeren voor de PowerApp** kunt u eventueel het veld selecteren dat de gegevens bevat die u als invoer wilt doorgeven aan de PowerApp. Raadpleeg de sectie [Een PowerApp bouwen die gebruikmaakt van gegevens uit Finance and Operations](#building-a-powerapp-that-leverages-data-sent-from-finance-and-operations) verderop in dit onderwerp voor meer informatie over hoe de PowerApp toegang krijgt tot gegevens uit Finance and Operations.
    - Kies de **toepassingsgrootte** die overeenkomt met het type PowerApp dat u insluit. Selecteer **Dun** voor PowerApps voor mobiele apparaten en **Breed** voor PowerApps voor tabletten. Zo zorgt u dat voldoende schijfruimte wordt gereserveerd voor de ingesloten PowerApp.
    - Het sneltabblad **Rechtspersonen** biedt de mogelijkheid om te kiezen voor welke rechtspersonen de PowerApp beschikbaar is. De standaardwaarde is dat de PowerApp voor alle rechtspersonen wordt weergegeven.

4. Nadat u hebt bevestigd dat de configuratie juist is, klikt u op **Invoegen** om de PowerApp op de pagina in te sluiten. U wordt gevraagd om de browser te vernieuwen om de ingesloten PowerApp te kunnen zien.

## <a name="sharing-an-embedded-powerapp"></a>Een ingesloten PowerApp delen

Nadat u een PowerApp op een pagina hebt ingesloten en hebt bevestigd dat deze correct werkt met de gegevenscontext die wordt doorgegeven vanuit de pagina, wilt u mogelijk deze ingesloten PowerApp delen met andere gebruikers in het systeem. Dit kunt doen op twee verschillende manieren met de aanpassingsmogelijkheden van het product:

- Het aanbevolen scenario is via de systeembeheerder, die een aanpassing aan alle gebruikers of een subset van gebruikers kan doorgeven.
- U kunt ook uw aanpassingen op de pagina exporteren en ze naar een of meer gebruikers sturen. Deze gebruikers kunnen uw wijzigingen importeren. Met de optie Beheren op de aanpassingswerkbalk kunt u persoonlijke instellingen importeren en exporteren.

Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over de aanpassingsmogelijkheden van het product en het gebruik ervan.

## <a name="building-a-powerapp-that-leverages-data-sent-from-finance-and-operations"></a>Een PowerApp bouwen die gebruikmaakt van gegevens uit Finance and Operations

Een belangrijk onderdeel van het bouwen van een PowerApp die wordt ingesloten in Finance and Operations is het gebruiken van invoergegevens uit Finance and Operations. In de PowerApp zijn die invoergegevens beschikbaar via de variabele Param("EntityId").

Voor de functie OnStart van de PowerApp kunt u de invoergegevens van Finance and Operations bijvoorbeeld instellen op een variabele als hieronder:

```
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-an-embedded-powerapp"></a>Een ingesloten PowerApp weergeven

Als u een ingesloten PowerApp wilt weergeven op een pagina in Finance and Operations, gaat u naar een pagina met een ingesloten PowerApp. PowerApps zijn toegankelijk via de knop PowerApps in het standaard Actievenster. Ook kunnen ze rechtstreeks op de pagina worden weergegeven als een nieuw tabblad, een sneltabblad of blad of als een nieuwe sectie in een werkgebied. Wanneer een gebruiker een PowerApp voor het eerst probeert te laden op een pagina, wordt gevraagd om de aanmeldgegevens voor de PowerApps zodat de gebruiker de juiste machtigingen heeft bij het gebruiken van de PowerApp.

## <a name="editing-an-embedded-powerapp"></a>Een ingesloten PowerApp bewerken

Nadat een PowerApp is ingesloten op een pagina, moet u mogelijk enkele wijzigingen aanbrengen in de configuratie van die PowerApp. U wilt misschien het label wijzigen dat is gekoppeld aan de ingesloten PowerApp of er is een nieuwe versie van een PowerApp gemaakt en u moet de App-id bijwerken met de meest recente PowerApp.

Ga als volgt te werk om de configuratie van een ingesloten PowerApp te bewerken:

1. Ga naar het deelvenster **Een PowerApp bewerken**.

    - Als de ingesloten PowerApp via de menuknop PowerApps wordt geopend, klikt u met de rechtermuisknop op de menuknop PowerApps en selecteert u **Aanpassen**. Selecteer de PowerApp die u wilt configureren vanuit de vervolgkeuzelijst **PowerApp selecteren**.
    - Als de ingesloten PowerApp rechtstreeks op de pagina wordt weergegeven, selecteert u **Opties** en vervolgens **Dit formulier aanpassen**. Klik met de functie **Selecteren** op de ingesloten PowerApp.

2. Breng de benodigde wijzigingen aan in de PowerApps-configuratie en klik op **Opslaan**.

## <a name="removing-an-embedded-powerapp"></a>Een ingesloten PowerApp verwijderen

Nadat een PowerApp is ingesloten op een pagina, zijn er twee manieren om deze te verwijderen:

- Ga naar het deelvenster **Een PowerApp bewerken** aan de hand van de instructies in [Een ingesloten PowerApp bewerken](#editing-an-embedded-powerapp) hierboven. Bevestig dat het deelvenster de informatie bevat voor de ingesloten PowerApp die u wilt verwijderen en klik op de knop **Verwijderen**.
- Omdat een ingesloten PowerApp wordt opgeslagen als persoonlijke gegevens, worden bij het wissen van aanpassingen op uw pagina ook eventuele ingesloten PowerApps op die pagina verwijderd. Houd er rekening mee dat het wissen van de aanpassingen van de pagina definitief is. Als u uw aanpassingen op een pagina wilt verwijderen, selecteert u **Opties** en klikt u vervolgens op **Dit formulier aanpassen**. Selecteer onder het menu **Beheren** de knop **Wissen**. Na het vernieuwen van uw browser worden alle vorige aanpassingen voor deze pagina verwijderd. Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over het optimaliseren van pagina's met aanpassingen.

## <a name="appendix"></a>Bijlage

### <a name="developer-control-over-where-a-powerapp-can-be-embedded"></a>Ontwikkelaars bepalen waar een PowerApp kan worden ingesloten

Standaard kunt u PowerApps op elke pagina insluiten, hetzij onder de menuknop PowerApps, hetzij rechtstreeks op de pagina als een tabblad, sneltabblad, blad of als een nieuwe sectie in een werkgebied. Indien nodig kunnen ontwikkelaars deze functie echter ook zo configureren dat het insluiten van PowerApps alleen is toegestaan op bepaalde pagina's door het implementeren van de volgende methoden:

- **isPowerAppPersonalizationEnabled**: als deze methode een fout voor een bepaalde pagina retourneert, wordt de knop PowerApps niet weergegeven en kunnen gebruikers geen PowerApps insluiten op een willekeurige plaats op deze pagina, met inbegrip van tabbladen.
- **isPowerAppTabPersonalizationEnabled**: als deze methode een fout voor een bepaalde pagina retourneert, kunnen gebruikers PowerApps niet rechtstreeks insluiten op de pagina als een tabblad, sneltabblad of een panoramasectie. Gebruikers kunnen nog wel PowerApps insluiten via de menuknop PowerApps als op de pagina insluiten is toegestaan.

Het volgende voorbeeld toont een nieuwe klasse met de twee methoden die nodig zijn voor het configureren van de plaats waar PowerApps kunnen worden ingesloten.

```
[ExtensionOf(classStr(FormRunConfigurationPowerAppsConfiguration))]

public final class ClassTest_Extension
{
    public static boolean isPowerAppPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppPersonalizationEnabled(pageName);
        return true;
    }
    public static boolean isPowerAppTabPersonalizationEnabled(str pageName)
    {
        var result = next isPowerAppTabPersonalizationEnabled(pageName);
        return true;
    }
}
```

