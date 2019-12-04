---
title: Maken en werken met aangepaste velden
description: Dit onderwerp beschrijft hoe aangepaste velden te maken om de toepassing aan te passen aan hun bedrijf.
author: jasongre
manager: AnnBe
ms.date: 07/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 9146921c47e89c5895a1a727de874b0ffbc93c37
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812500"
---
# <a name="create-and-work-with-custom-fields"></a>Maken en werken met aangepaste velden

[!include [banner](../includes/banner.md)]

Hoewel er een uitgebreide reeks kant-en-klare velden voor het beheren van een breed scala van bedrijfsprocessen is, is er soms behoefte in een bedrijf om aanvullende informatie bij te houden in het systeem. Voor deze behoefte kunt u aangepaste velden maken om de toepassing aan te passen aan uw bedrijf, als u machtigingen hebt voor de functie.

De mogelijkheid om aangepaste velden toe te voegen, is beschikbaar in platformupdate 13 en hoger.

In deze video wordt getoond hoe gemakkelijk het is een aangepast veld toe te voegen aan een pagina: [Aangepaste velden toevoegen](https://www.youtube.com/watch?v=gWSGZI9Vtnc).

## <a name="creating-custom-fields"></a>Aangepaste velden maken

Nadat u extra informatie hebt aangegeven die u wilt bijhouden in de toepassing, kunt u het aangepaste veld in de juiste tabel maken en weergeven op een pagina.

De volgende stappen beschrijven het proces voor het maken van een aangepast veld en dat veld plaatsen op een formulier.

1. Ga naar het formulier waar het nieuwe veld is vereist.
2. Aangezien het einddoel is het aangepaste veld op een formulier weer te geven, bestaat het ingangspunt voor het maken van aangepaste velden in de persoonlijke ervaring. Open de aanpassingswerkbalk door **Opties** en vervolgens **Dit formulier aanpassen** te selecteren.
3. Klik op **invoegen** en vervolgens op **Veld**.
4. Selecteer het gebied van het formulier waar u het nieuwe veld wilt weergeven. Na selectie bevat het dialoogvenster **Velden invoegen** een lijst met bestaande velden die kunnen worden ingevoegd in het geselecteerde gebied van het formulier.
5. Controleer dat het veld waarin u geïnteresseerd bent nog niet in de lijst staat. Als dit wel het geval is, selecteert u gewoon dat veld in de lijst en klikt u op **Invoegen**.
6. Klik op de knop **Nieuw veld maken** boven de lijst om het proces te starten om een aangepast veld te maken. Hiermee opent u het dialoogvenster **Nieuw veld maken**.

    Als u de knop **Nieuw veld maken** niet ziet, hebt u niet de benodigde machtigingen om deze functie te gebruiken.

7. Voer in het dialoogvenster **Nieuw veld maken** de volgende informatie in.

    1. Selecteer de databasetabel waar dit veld moet worden toegevoegd. Houd er rekening mee dat alleen de tabellen die ondersteuning bieden voor aangepaste velden, in de vervolgkeuzelijst worden weergegeven. Zie de sectie hieronder voor meer technische informatie over ondersteunde tabellen.
    2. Selecteer het gegevenstype voor het nieuwe veld De beschikbare gegevenstypen zijn selectievakje, datum, datum/tijd, decimaal, nummer, selectielijst en tekst.

        - Als u het tekstgegevenstype kiest, kunt u ook de maximale lengte van de tekst die kan worden ingevoerd in dit veld opgeven.
        - Als u het gegevenstype selectielijst kiest, kunt u ook de set geldige waarden voor het veld selecteren.

    3. Geef een naam, label en help-tekst voor het veld op. De naam komt overeen met de fysieke veldnaam in de database, terwijl het label en de help-tekst de tekst zijn die wordt gebruikt voor het weergeven van dit veld in de gebruikersinterface.

8. Als dit het enige veld dat u wilt maken voor dit formulier, klikt u op **Opslaan**. Als u extra velden moet maken, klikt u op **Opslaan en nieuw** en gaat u terug naar stap 7. Er is momenteel een limiet van **20 aangepaste velden per tabel**.
9. Als u het dialoogvenster **Nieuw veld maken** verlaat, keert u terug naar het dialoogvenster **Velden invoegen**. Eventuele aangepaste velden die zojuist zijn toegevoegd, worden automatisch gemarkeerd in de lijst met velden die in het formulier moeten worden ingevoegd.
10. Klik op **Invoegen** voor het invoegen van de gemarkeerde velden in het geselecteerde gedeelte van het formulier.
11. **Optioneel:** schakel de modus **Verplaatsen** op de aanpassingswerkbalk in om de nieuwe velden naar de gewenste locatie in het geselecteerde gebied te verplaatsen. Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over het gebruik van de verschillende mogelijkheden voor aanpassing van een formulier aan uw persoonlijke gebruik.

## <a name="sharing-custom-fields-with-other-users"></a>Aangepaste velden delen met andere gebruikers

Nadat u een aangepast veld hebt gemaakt en het op een formulier wordt weergegeven, wilt u wellicht deze bijgewerkte paginaweergave met het nieuwe veld aan andere gebruikers in het systeem bieden. Dit kunt doen op twee verschillende manieren met de aanpassingsmogelijkheden van het product:

- De aanbevolen route is via de systeembeheerder, die een aanpassing aan alle gebruikers of een subset van gebruikers kan doorgeven. Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie.
- U kunt ook uw wijzigingen (*aanpassingen* genoemd) exporteren, Stuur ze naar een of meer gebruikers en laat elk van deze gebruikers uw wijzigingen importeren. Met de optie **Beheren** op de aanpassingswerkbalk kunt u persoonlijke instellingen importeren en exporteren.

## <a name="managing-custom-fields"></a>Aangepaste velden beheren

Beheer van de aangepaste velden in het systeem kan worden uitgevoerd via de pagina **Aangepaste velden** in de module Systeembeheer. Op deze pagina kunnen gebruikers toegang tot veel mogelijkheden krijgen, zoals:

- Een lijst weergeven met alle aangepaste velden in het systeem.
- Beperkt bewerken van bestaande aangepaste velden.
- Aangepaste velden verwijderen.
- Aangepaste velden in gegevensentiteiten weergeven.
- Vertalingen van labels van aangepaste velden en help-tekst bieden.

### <a name="viewing-all-custom-fields"></a>Alle aangepaste velden weergeven

De pagina **Aangepaste velden** biedt inzicht in alle aangepaste velden die zijn gedefinieerd in het systeem. Selecteer gewoon de tabel waarin u geïnteresseerd bent en de pagina wordt bijgewerkt met een lijst met aangepaste velden die zijn gekoppeld aan die tabel. Als u een aangepast veld kiest uit de lijst, kunt u alle details weergeven over het veld.

### <a name="editing-custom-fields"></a>Aangepaste velden bewerken

Nadat u een aangepast veld hebt gemaakt, kunnen alleen bepaalde delen van informatie over het aangepaste veld worden gewijzigd op de pagina **Aangepaste velden**.

U *kunt* deze kenmerken wijzigen:

- Label
- Help-tekst
- Lengte voor tekstvelden

U kunt de volgende kenmerken *niet* bewerken:

- Veldnaam
- Gegevenstype

Daarnaast kan voor selectielijstvelden, de lijst geldige waarden voor het aangepaste veld opnieuw worden geordend en kunnen nieuwe waarden worden toegevoegd. Bestaande waarden voor het selectielijstveld kunnen echter niet worden verwijderd. Vergeet niet op **Wijzigingen toepassen** te klikken wanneer u klaar bent met bewerken van velden voor een bepaalde tabel, zodat de wijzigingen worden opgeslagen.

### <a name="exposing-custom-fields-on-data-entities"></a>Aangepaste velden in gegevensentiteiten weergeven

Het is belangrijk toe te staan dat aangepaste velden zichtbaar zijn in gegevensentiteiten. Gegevensentiteiten worden gebruikt in de functie [Overzicht van Office-integratie](../../dev-itpro/office-integration/office-integration.md) en voor scenario's voor het importeren/exporteren van gegevens.

Ga als volgt te werk om een aangepast veld in een gegevensentiteit weer te geven:

1. Selecteer het aangepaste veld op het formulier **Aangepaste velden**.
2. Vouw de sectie **Entiteiten** uit om de set relevante entiteiten weer te geven.
3. Klik op de knop **Bewerken**.
4. Selecteer het veld **Ingeschakeld** voor elke entiteit die dit veld moet weergeven.
5. Klik op **Wijzigingen toepassen** om uw selecties op te slaan.

### <a name="allowing-custom-fields-to-be-displayed-in-other-languages"></a>Toestaan dat aangepaste velden worden weergegeven in andere talen

Omdat gebruikers in allerlei talen toegang moeten kunnen hebben tot aangepaste velden, bevat de pagina **Aangepaste velden** een mechanisme waarmee het label en de help-tekst van een aangepast veld kan worden vertaald in andere talen.

De volgende stappen beschrijven het proces voor het omzetten van aangepaste velden in andere talen:

1. Selecteer het aangepaste veld op de pagina **Aangepaste velden**.
2. Selecteer de knop **Vertalingen** in het actievenster. Hiermee opent u een vervolgkeuzelijst met bestaande vertalingen voor dit veld.
3. De vervolgkeuzelijst **Taal** toont de set talen waarvoor reeds vertalingen zijn verschaft.

    Als u een bestaande vertaling wilt bewerken, selecteert u de gewenste taal in het menu en wijzigt u de waarden voor het label en de help-tekst.

    Klik anders op de knop **Taal toevoegen**, selecteer de gewenste taal in het menu, en geef vertaalde waarden op voor het label en de help-tekst.

4. Wanneer u klaar bent, klikt u op **OK**.

### <a name="deleting-custom-fields"></a>Aangepaste velden verwijderen

In sommige zeldzame gevallen kunt u bepalen dat een aangepast veld niet meer nodig is. Als dit gebeurt kan een systeembeheerder het veld verwijderen van de pagina **Aangepaste velden**. Hiertoe selecteert u het juiste veld, klikt u op **Verwijderen**, klikt u op **Ja** om de verwijdering te bevestigen en klikt u ten slotte op **Wijzigingen toe passen**.

> [!NOTE]
> Deze actie kan niet ongedaan worden gemaakt en leidt ertoe dat de gegevens die zijn gekoppeld aan het veld, permanent worden verwijderd uit de database.

## <a name="appendix"></a>Bijlage

### <a name="who-can-create-custom-fields"></a>Wie kan aangepaste velden maken?

Als beveiliging voor het systeem kunnen alleen systeembeheerders standaard aangepaste velden maken. Hoofdgebruikers van wie de organisatie dat nodig vindt, kunnen echter door systeembeheerders rechten worden gegeven om aangepaste velden te maken met de beveiligingsrol **Runtimeaanpassing hoofdgebruiker**. Gebruikers zonder deze beveiligingsrol kunnen geen aangepaste velden maken, maar kunnen aangepaste velden die door andere gebruikers in het systeem zijn gemaakt, wel zien en gebruiken.

### <a name="what-tables-support-custom-fields"></a>Welke tabellen ondersteunen aangepaste velden?

Omwille van prestaties en technische redenen kunnen momenteel alleen aangepaste velden worden toegevoegd aan tabellen die voldoen aan de volgende voorwaarden.

- De tabel moet zijn gemarkeerd als een van deze groepen:

    - Groep
    - WorksheetHeader
    - Hoofdonderdeel
    - Diversen
    - Parameter
    - Verwijzing
    - TransactionHeader

- De tabel kan niet een andere tabel uitbreiden.
- De tabel kan niet zijn gemarkeerd als een systeemtabel.
- De tabel kan geen tijdelijke tabel zijn.
