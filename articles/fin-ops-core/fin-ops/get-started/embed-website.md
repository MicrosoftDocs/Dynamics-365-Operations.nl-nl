---
title: Apps van derden insluiten
description: In dit onderwerp wordt uitgelegd hoe u apps van derden kunt insluiten om de functionaliteit van het product te verbeteren.
author: jasongre
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, UserWorkspaceAdd, UserWorkspaceConfigureWebsite
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2021-04-30
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f47fb6a2fdb586fbc9f25938c3b9c1cfc16ddc1af432b91621421bd829b23925
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6737794"
---
# <a name="embed-third-party-apps"></a>Apps van derden insluiten

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Veel klanten gebruiken een meerdere toepassingen om hun activiteiten uit te voeren. Sommige van deze toepassingen zijn webtoepassingen van derden, die werken in combinatie met Finance and Operations-apps. Voor een soepele gebruikerservaring kunt u met de functie **Apps op volledige pagina (preview)** deze toepassingen van derden rechtstreeks in uw Finance and Operations-apps insluiten (als deze toepassingen van derden het toelaten te worden ingesloten). Op deze manier hebben gebruikers toegang tot de websites en apps die ze nodig hebben, zonder dat ze tussen tabbladen of vensters moeten wisselen.

Voordat u apps van derden in het product kunt insluiten, moet u de functie **Apps op volledige pagina (preview)** inschakelen in Functiebeheer. U kunt vervolgens met een van de volgende methoden een app of website van een derde partij insluiten. Deze methoden zijn vergelijkbaar met de methoden waarmee canvas-toepassingen uit Microsoft Power Apps worden ingesloten in Finance and Operations-apps.

- Sluit de app of website in op een bestaande pagina als een nieuw tabblad (draaitabblad, sneltabblad, blade of werkgebiedsectie).
- Maak een volledige nieuwe pagina voor de app of website vanuit het dashboard.

## <a name="embed-a-website-on-an-existing-page"></a>Een website op een bestaande pagina insluiten

Gebruik deze procedure als u een bestaande pagina in het systeem wilt aanvullen met een ingesloten app.

1. Open de pagina waarop u de canvas-app wilt insluiten.
2. Open het deelvenster **Een app toevoegen**:

    1. Selecteer **Instellingen** en vervolgens **Aanpassen** om de werkbalk **Persoonlijke instellingen** te openen.
    2. Selecteer **Meer \> Een app toevoegen**.

3. Selecteer de regio van de pagina waarop u de app wilt toevoegen. Deze regio moet een *tabbladcontainer* zijn voor een draaitabblad, sneltabblad, blade of werkgebiedsectie.
4. Selecteer **Website**.
5. De ingesloten app configureren:

    - **Naam**: Voer de tekst in die moet worden weergegeven op het tabblad dat de ingesloten app bevat. Vaak is het wenselijk dat deze tekst de naam van de app is.
    - **URL**: Geef de locatie van de app op.

    > [!IMPORTANT]
    > - Uit oogpunt van beveiliging moet de URL gebruik maken van Hypertext Transfer Protocol Secure (HTTPS).
    > - De app of website moet zo worden geconfigureerd dat hij toelaat te worden ingesloten.

6. Selecteer **Opslaan** om de app in te sluiten in de pagina. De app wordt toegevoegd als het laatste tabblad of de laatste sectie in de groep.
7. Controleer of de app wordt weergegeven zoals u verwacht. Als de app niet wordt weergegeven, raadpleeg dan de sectie [Probleemoplossing](#troubleshooting) verderop in dit artikel.
8. Open de weergaveselector en selecteer **Opslaan** (als de app moet worden gekoppeld aan de huidige weergave) of **Opslaan als** (als u de app in een andere weergave wilt opslaan).

    Als de pagina geen weergaveselector heeft (bijvoorbeeld als de pagina een dialoogvenster of werkgebied is), kunt u deze stap overslaan.

## <a name="embed-a-website-as-a-full-page-experience-from-the-dashboard"></a>Een website insluiten als volledige pagina vanuit het dashboard

Gebruik deze procedure als de app die u wilt insluiten die geen verband houdt met een bestaande pagina, of als u alleen een volledige pagina wilt gebruiken voor de app in de Finance and Operations-app.

1. Open het dashboard.
2. Selecteer de pagina en houd deze vast (of klik erop met de rechtermuisknop), selecteer **Personaliseren** en selecteer vervolgens **Een pagina toevoegen**.
3. Selecteer in het deelvenster **Een pagina toevoegen** de optie **Website**.
4. De ingesloten app configureren:

    - **Naam**: Voer de tekst in die u wilt laten weergeven op de tegel die wordt toegevoegd voor de ingesloten app in het dashboard. Vaak is het wenselijk dat deze tekst de naam van de app is.
    - **URL**: Geef de locatie van de app op.

    > [!IMPORTANT]
    > - Uit oogpunt van beveiliging moet de URL gebruik maken van HTTPS.
    > - De app of website moet zo worden geconfigureerd dat hij toelaat te worden ingesloten.

5. Selecteer **Opslaan** om de app aan het dashboard toe te voegen als een nieuwe tegel.
6. Selecteer de nieuwe tegel op het dashboard en controleer of de app wordt weergegeven zoals u verwacht. Als de app niet wordt weergegeven, raadpleeg dan de sectie [Probleemoplossing](#troubleshooting) verderop in dit artikel.

## <a name="sharing-embedded-apps"></a>Ingesloten apps delen

Nadat u een app hebt ingesloten via een van de methoden die in de vorige secties zijn beschreven, wilt u de weergave mogelijk delen met andere gebruikers in het systeem. Gebruik een van de volgende methoden om een ingesloten app te delen:

- **De weergave publiceren (aanbevolen)**: Als de ingesloten app is opgeslagen in een weergave, wordt het aanbevolen (en verdient het de voorkeur) om deze te delen door de weergave te publiceren naar gebruikers met de juiste beveiligingsrollen. Zo zorgt u ervoor dat alle gebruikers die de beveiligingsrollen voor de gepubliceerde weergave hebben, de app in Finance and Operations-apps zien. Meer informatie over het publiceren van een weergave vindt u in [Weergaven publiceren](saved-views.md#publishing-views).

    U kunt ook een app publiceren die is ingesloten als volledige pagina vanuit het dashboard. Selecteer op het dashboard de tegel die aan de app is gekoppeld en houd deze vast (of klik erop met de rechtermuisknop), selecteer **Personaliseren** en selecteer vervolgens **Pagina publiceren**. U kunt op dit moment alleen publiceren naar beveiligingsrollen. De mogelijkheid om naar rechtspersonen te publiceren wordt echter nog wel toegevoegd voordat de functie algemeen beschikbaar wordt.

- **De personalisatie kopiëren**: Voor pagina's die geen weergaven ondersteunen (bijvoorbeeld dialoogvensters of werkgebieden) of voor de app met een volledige pagina kunt u de personalisatie naar de juiste gebruikers kopiëren. Meer informatie over dit onderwerp vindt u in [Persoonlijke instellingen delen](personalize-user-experience.md#sharing-personalizations).

## <a name="viewing-embedded-apps"></a>Ingesloten apps weergeven

Als u een ingesloten app wilt weergeven in Finance and Operations-apps, opent u de pagina die de ingesloten app bevat. Onthoud dat u op sommige pagina's toegang kunt krijgen tot apps via de knop **Power Apps** in het standaardactievenster. Apps kunnen ook rechtstreeks op de pagina worden weergegeven als een nieuw tabblad, sneltabblad, blade of als een nieuwe sectie in een werkgebied.

## <a name="editing-or-removing-embedded-apps"></a>Ingesloten apps bewerken of verwijderen

Nadat een app is ingesloten op een pagina, kan het zijn dat u de configuratie moet bewerken (bijvoorbeeld door het sectielabel of de URL te wijzigen). Mogeljik moet u het ook van de pagina verwijderen. Gebruik een van de volgende procedures om de configuratie van een ingesloten app te bewerken of de app volledig te verwijderen.

### <a name="apps-that-are-embedded-on-existing-pages"></a>Apps die in bestaande pagina's zijn ingesloten

1. Open de pagina waarop de app is ingesloten.
2. Selecteer **Instellingen** en vervolgens **Aanpassen** om de werkbalk **Persoonlijke instellingen** te openen.
3. Selecteer het hulpmiddel **Selecteren** en selecteer dan de ingesloten app.
4. Als u de app wilt bewerken, wijzigt u de configuratie ervan waar nodig en selecteert u **Opslaan**.

    Als u de app wilt verwijderen, selecteert u **Verwijderen**.

5. De weergave opnieuw opslaan of opnieuw publiceren. Als u de pagina verlaat zonder de weergave expliciet op te slaan, blijft geen van de acties bewaard die u in het deelvenster **Website bewerken** hebt uitgevoerd.

### <a name="apps-that-are-embedded-from-the-dashboard"></a>Apps die vanuit het dashboard zijn ingesloten

1. Open het dashboard.
2. Selecteer de tegel die aan de ingesloten app is gekoppeld en houd deze vast (of klik erop met de rechtermuisknop) en selecteer **Personaliseren**.
3. Om de app te bewerken, selecteert u **Pagina bewerken**. Voer in het deelvenster **Website bewerken** de gewenste wijzigingen door in de app-configuratie en selecteer **Opslaan**.

    Als u de app wilt verwijderen, selecteert u **Pagina verwijderen**.

## <a name="appendix"></a>Bijlage

### <a name="troubleshooting"></a>Problemen oplossen

Als een website niet correct wordt weergegeven nadat deze is ingesloten in een Finance and Operation-app of als u een foutbericht ontvangt waarin wordt vermeld dat de verbinding met de URL is geweigerd, is de website waarschijnlijk geconfigureerd om te voorkomen dat ze in een iFrame wordt ingesloten. Volg deze stappen om te bepalen of de website kan worden ingesloten.

1. Open de ontwikkelhulpprogramma's voor de browser die u gebruikt.
2. Ga naar het tabblad **Netwerk** en selecteer de response van de ingesloten site.
3. Zoek op het tabblad **Headers** onder **Responseheaders** naar **x-frame-options**. Als de **x-frame-options** bestaat in de responseheaders en de waarde **DENY** of **SAMEORIGIN** heeft, kan de website momenteel niet worden ingesloten. U moet samenwerken met de eigenaar van de app om de app veilig in te kunnen sluiten.

### <a name="developer-modeling-a-website-on-a-form"></a>[Ontwikkelaar] Een website modelleren op een formulier

Hoewel dit onderwerp zich richt op het insluiten van apps of websites van derden via personalisatie, kunnen ontwikkelaars deze ook in een formulier insluiten door middel van de Visual Studio-ontwikkelomgeving. U voegt hiervoor gewoon een besturingselement **WebsiteHostControl** toe aan het formulier. De metagegevenseigenschappen die beschikbaar zijn voor het besturingselement, bieden dezelfde mogelijkheden als personalisatie.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
