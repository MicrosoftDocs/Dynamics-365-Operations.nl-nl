---
title: Canvas-apps insluiten vanuit Power Apps
description: In dit onderwerp wordt uitgelegd hoe u canvas-apps vanuit Microsoft Power Apps kunt insluiten in de client om de functionaliteit van het product te verbeteren.
author: jasongre
manager: AnnBe
ms.date: 09/11/2020
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
ms.openlocfilehash: e57e4567a80aa9f9ba5ac434b0d71204460e164f
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893102"
---
# <a name="embed-canvas-apps-from-power-apps"></a>Canvas-apps insluiten vanuit Power Apps

[!include [banner](../includes/banner.md)]

Microsoft Power Apps is een service waarmee ontwikkelaars en niet-technische gebruikers aangepaste zakelijke apps kunnen maken voor mobiele apparaten, tablets en het web zonder code te hoeven schrijven. Finance and Operations-apps ondersteunen integratie met Power Apps. Canvas-apps die u, uw organisatie of anderen ontwikkelen, kunnen worden ingesloten in Finance and Operations-apps om de functionaliteit van het product te verbeteren. U kunt bijvoorbeeld een canvas-app maken in Power Apps als aanvulling op een Finance and Operations-app met informatie die uit een ander systeem wordt opgehaald.

Voor meer informatie over het insluiten van Power Apps bekijkt u de korte video [PowerApps insluiten in Power Apps](https://www.youtube.com/watch?v=x3qyA1bH-NY).

## <a name="adding-an-embedded-canvas-app-from-power-apps-to-a-page"></a>Een ingesloten canvas-app vanuit Power Apps toevoegen aan een pagina

### <a name="overview"></a>Overzicht

Voordat u een canvas-app vanuit Power Apps in de client insluit, moet u eerst een app zoeken of maken met de gewenste visuele effecten of functionaliteit. Dit onderwerp bevat geen gedetailleerde beschrijving van het proces voor het maken van apps. Als u Power Apps voor het eerst gebruikt, raadpleegt u de [Power Apps-documentatie](https://docs.microsoft.com/powerapps/).

U kunt op twee manieren toegang krijgen tot een specifieke canvas-app op een pagina wanneer u klaar bent om de app in te sluiten. Kies de aanpak die het beste bij uw situatie past. Bij de eerste aanpak wordt de knop **Power Apps** gebruikt die aan het standaardactievenster is toegevoegd. Apps die u met deze methode toevoegt, worden als items op de **Power Apps**-menuknop weergegeven. Als u een van deze items selecteert, wordt een zijdeelvenster geopend met de ingesloten app. U kunt een app ook rechtstreeks op een pagina insluiten als een nieuw tabblad, sneltabblad, blad of als een nieuwe sectie in een werkgebied.

Als u uw ingesloten canvas-app configureert, kunt u één veld selecteren dat u als context naar de app wilt verzenden. Met deze stap kan de app reageren op basis van de gegevens die u momenteel weergeeft.

> [!NOTE]
> U kunt dit mechanisme momenteel niet gebruiken om gemodelleerde apps in te sluiten.  

### <a name="details"></a>Gegevens

De volgende procedure laat zien hoe u een canvas-app vanuit Power Apps in de webclient insluit.

1. Ga naar de pagina waar u de canvas-app wilt insluiten. Deze pagina wordt de pagina die gegevens bevat die als invoer moeten worden doorgegeven aan de app.
2. Open het deelvenster **Een app van Power Apps** toevoegen:

    - Klik op **Opties** en selecteer **Deze pagina aanpassen**. Kies in het menu **Invoegen** de optie **Power Apps**. Selecteer ten slotte de regio waar u de app wilt toevoegen. Als u de app onder de menuknop Power Apps wilt insluiten, kiest u het actievenster. Als u de app rechtstreeks op de pagina wilt insluiten, kiest u het gewenste tabblad, Sneltabblad, blad of sectie (als u in een werkgebied bent).
    - Als de app wordt benaderd via de menuknop Power Apps, kunt u ook klikken op de menuknop **Power Apps** in het standaard actievenster en vervolgens **Een app invoegen** selecteren.

3. De ingesloten app configureren:

    - Het veld **Naam** geeft de weergegeven tekst aan voor de knop of het tabblad met de ingesloten app. Vaak zult u de naam van de app in dit veld willen herhalen.
    - Met het veld **App-ID** wordt de GUID (Globally Unique Identifier) aangegeven voor de canvas-app die u wilt insluiten. Als u deze waarde wilt ophalen, gaat u naar de app op [web.powerapps.com](https://web.powerapps.com) en zoekt u in het veld **App-ID** onder **Details**.
    - Voor **Context invoeren voor de app** kunt u eventueel het veld selecteren dat de gegevens bevat die u als invoer wilt doorgeven aan de app. Raadpleeg de sectie [Een app bouwen die gebruikmaakt van gegevens die vanuit Finance and Operations-apps zijn verzonden](#building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps) verderop in dit onderwerp voor meer informatie over hoe de app toegang krijgt tot gegevens uit Finance and Operations-apps.
    - Kies de **Toepassingsgrootte** die overeenkomt met het type app dat u insluit. Selecteer **Dun** voor apps voor mobiele apparaten en **Breed** voor apps voor tablets. Zo zorgt u dat voldoende schijfruimte wordt gereserveerd voor de ingesloten app.
    - Het sneltabblad **Rechtspersonen** biedt de mogelijkheid om te kiezen voor welke rechtspersonen de app beschikbaar is. De standaardwaarde is dat de app voor alle rechtspersonen toegankelijk is. Deze optie is alleen beschikbaar als de functie [Opgeslagen weergaven](saved-views.md) is uitgeschakeld. 

4. Nadat u hebt bevestigd dat de configuratie juist is, klikt u op **Invoegen** om de Power App op de pagina in te sluiten. U wordt gevraagd de browser te vernieuwen om de ingesloten app te kunnen zien.

## <a name="sharing-an-embedded-app"></a>Een ingesloten app delen

Nadat u een canvas-app op een pagina hebt ingesloten en hebt bevestigd dat deze correct werkt met alle gegevenscontext die wordt doorgegeven vanaf die pagina, kunt u de app met andere gebruikers in het systeem delen. Voer de volgende stappen uit om een ingesloten canvas-app te delen.

1. [Deel de canvas-app](https://docs.microsoft.com/powerapps/maker/canvas-apps/share-app) met de gewenste gebruikers, zodat zij toegang kunnen krijgen tot de app in Power Apps. 

2. Controleer dat de beoogde gebruikers de juiste persoonlijke instellingen hebben, zodat de ingesloten app wordt weergegeven wanneer deze gebruikers de pagina bekijken. U kunt een van de twee volgende methoden gebruiken:

    - Aanbevolen: gebruik de functie [Opgeslagen weergaven](saved-views.md) om een weergave te maken en te publiceren die de ingesloten app bevat. Met deze methode wordt ervoor gezorgd dat alle gebruikers die de beveiligingsrollen voor de gepubliceerde weergave hebben, de app in Finance and Operations-apps zien. 
    - Als u de functie Opgeslagen weergaven niet hebt ingeschakeld, kunt u de systeembeheerder een persoonlijke instelling laten instellen die de ingesloten app bevat voor alle gebruikers of een subset van gebruikers. U kunt ook de persoonlijke instellingen van uw pagina exporteren en deze naar een of meer gebruikers verzenden. Elk van deze gebruikers kan de persoonlijke instellingen vervolgens importeren. De werkbalk met persoonlijke instellingen bevat acties waarmee u persoonlijke instellingen kunt importeren en exporteren. 
    
> [!NOTE]
> Als de canvas-app met externe gebruikers is gedeeld, kunnen deze gebruikers de ingesloten app niet in Finance and Operations-apps gebruiken. Ze kunnen echter rechtstreeks toegang krijgen tot de app in Power Apps. Externe gebruikers zijn gasten en gebruikers die niet behoren tot de Microsoft 365 Azure Directory waar de Finance and Operations-app wordt geïmplementeerd.

Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over de aanpassingsmogelijkheden van het product en het gebruik ervan.

## <a name="building-a-canvas-app-that-uses-data-that-is-sent-from-finance-and-operations-apps"></a>Een canvas-app maken waarin gegevens worden gebruikt die vanuit Finance and Operations-apps worden verzonden

Wanneer u een canvas-app maakt die in een Finance and Operations-app wordt ingesloten, is een belangrijk onderdeel van het proces dat u de invoergegevens van die Finance and Operations-app gebruikt. Vanuit de Power Apps-ontwikkelervaring kunt u toegang krijgen tot de invoergegevens die vanuit een Finance and Operations-app worden doorgegeven met de variabele **Param("EntityId"**).

Voor de functie OnStart van de app kunt u de invoergegevens van Finance and Operations-apps bijvoorbeeld instellen op een variabele als hieronder:

```powerapps
If(!IsBlank(Param("EntityId")), Set(FinOpsInput, Param("EntityId")), Set(FinOpsInput, ""));
```

## <a name="viewing-a-canvas-app"></a>Een canvas-app weergeven

Als u een ingesloten canvas-app wilt weergeven op een pagina in Finance and Operations-apps, gaat u naar een pagina die een ingesloten app bevat. U kunt toegang krijgen tot apps via de knop **Power Apps** in het standaardactievenster. Apps kunnen ook rechtstreeks op de pagina worden weergegeven als een nieuw tabblad, sneltabblad, blad of als een nieuwe sectie in een werkgebied. Wanneer gebruikers voor het eerst een app proberen te laden op een pagina, wordt hen gevraagd om zich aan te melden. Met deze stap wordt ervoor gezorgd dat de gebruikers over de juiste machtigingen beschikken om de app te gebruiken.

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

### <a name="developer-specifying-where-an-app-can-be-embedded"></a>[Ontwikkelaar]: opgeven waar een app kan worden ingesloten

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
