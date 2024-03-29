---
title: Aangepaste velden maken en gebruiken
description: In dit artikel wordt aangegeven hoe u in de gebruikersinterface aangepaste velden kunt maken om de toepassing aan te passen aan uw bedrijf.
author: jasongre
ms.date: 12/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysCustomFieldManageFields
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2018-1-31
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: 18e7e8525352e8fdc397621c381ed4297837e30c
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887282"
---
# <a name="create-and-work-with-custom-fields"></a>Aangepaste velden maken en gebruiken

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Hoewel er een uitgebreide reeks kant-en-klare velden voor het beheren van een breed scala van bedrijfsprocessen is, is er soms behoefte in een bedrijf om aanvullende informatie bij te houden in het systeem. Hoewel programmeurs deze velden kunnen toevoegen als extensies in de hulpprogramma's voor ontwikkelaars, kunnen velden met aangepaste velden direct vanuit de gebruikersinterface worden toegevoegd, zodat u de toepassing via uw webbrowser kunt aanpassen aan uw bedrijf.

*Alleen gebruikers met speciale machtigingen hebben toegang tot deze functie.*

In deze video wordt getoond hoe gemakkelijk het is een aangepast veld toe te voegen aan een pagina: [Aangepaste velden toevoegen](https://www.youtube.com/watch?v=gWSGZI9Vtnc).

## <a name="creating-custom-fields"></a>Aangepaste velden maken

Nadat u extra informatie hebt aangegeven om bij te houden in de toepassing, kunt u het aangepaste veld in de juiste tabel maken en weergeven op een pagina.

De volgende stappen beschrijven het proces voor het maken van een aangepast veld en dat veld plaatsen op een pagina.

1. Ga naar de pagina waar het nieuwe veld is vereist.
2. Aangezien het einddoel is het aangepaste veld op een formulier weer te geven, bestaat het ingangspunt voor het maken van aangepaste velden in de persoonlijke ervaring. Open de aanpassingswerkbalk door **Opties** en vervolgens **Dit formulier aanpassen** te selecteren.
3. Klik op **invoegen** en vervolgens op **Veld**.
4. Selecteer het gebied van het formulier waar u het nieuwe veld wilt weergeven. Na selectie bevat het dialoogvenster **Velden invoegen** een lijst met bestaande velden die kunnen worden ingevoegd in het geselecteerde gebied van de pagina.
5. Bevestig dat het veld waarin u geïnteresseerd bent nog niet in de lijst staat. Als dit wel het geval is, selecteert u gewoon dat veld in de lijst en klikt u op **Invoegen**.
6. Klik op de knop **Nieuw veld maken** boven de lijst om het proces te starten om een aangepast veld te maken. Hiermee opent u het dialoogvenster **Nieuw veld maken**.

    Als u de knop **Nieuw veld maken** niet ziet, hebt u niet de benodigde machtigingen om deze functie te gebruiken.

7. Voer in het dialoogvenster **Nieuw veld maken** de volgende informatie in.
   
    1. Selecteer de databasetabel waar dit veld moet worden toegevoegd. Houd er rekening mee dat alleen de tabellen die ondersteuning bieden voor aangepaste velden, in de vervolgkeuzelijst worden weergegeven. Zie de sectie hieronder voor meer technische informatie over ondersteunde tabellen.

    2. Selecteer het gegevenstype voor het nieuwe veld De beschikbare gegevenstypen zijn selectievakje, datum, datum/tijd, decimaal, nummer, selectielijst en tekst.

        - Als u het tekstgegevenstype kiest, kunt u ook de maximale lengte van de tekst die kan worden ingevoerd in dit veld opgeven.
        - Als u het gegevenstype selectielijst kiest, kunt u ook de set geldige waarden voor het veld selecteren.

    3. Geef een naam, label en help-tekst voor het veld op. De naam komt overeen met de fysieke veldnaam in de database, terwijl het label en de help-tekst de tekst zijn die wordt gebruikt voor het weergeven van dit veld in de gebruikersinterface.

8. Als dit het enige veld dat u wilt maken voor deze pagina, klikt u op **Opslaan**. Als u extra velden moet maken, klikt u op **Opslaan en nieuw** en gaat u terug naar stap 7. 

>[!Note] 
> Er is momenteel een limiet van **20 aangepaste velden per tabel**.

9. Als u het dialoogvenster **Nieuw veld maken** verlaat, keert u terug naar het dialoogvenster **Velden invoegen**. Eventuele aangepaste velden die zojuist zijn toegevoegd, worden automatisch gemarkeerd in de lijst met velden die in de pagina moeten worden ingevoegd.
10. Klik op **Invoegen** voor het invoegen van de gemarkeerde velden in het geselecteerde gedeelte van de pagina.
11. **Optioneel:** schakel de modus **Verplaatsen** op de aanpassingswerkbalk in om de nieuwe velden naar de gewenste locatie in het geselecteerde gebied te verplaatsen. Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over het gebruik van de verschillende mogelijkheden voor aanpassing van een formulier aan uw persoonlijke gebruik.

> [!WARNING]
> De mogelijkheid om waarden in te voeren in een aangepast veld dat aan een pagina is toegevoegd, is afhankelijk van de vraag of de tabel die aan het aangepaste veld is gekoppeld, bewerkbaar of alleen-lezen is. Wanneer de gekoppelde tabel alleen-lezen is, worden alle aan deze tabel gekoppelde velden, inclusief aangepaste velden, ook alleen-lezen.


## <a name="sharing-custom-fields-with-other-users"></a>Aangepaste velden delen met andere gebruikers

Nadat u een aangepast veld hebt gemaakt en het op een pagina wordt weergegeven, wilt u wellicht deze bijgewerkte paginaweergave met het nieuwe veld aan andere gebruikers in het systeem bieden. Dit kunt doen op twee verschillende manieren met de aanpassingsmogelijkheden van het product:

- De aanbevolen route is het **publiceren van een [opgeslagen weergave](saved-views.md)** met het aangepaste veld dat aan de pagina is toegevoegd aan de juiste set gebruikers. Als de functie voor opgeslagen weergaven niet is ingeschakeld, kan de systeembeheerder de personalisatie vanuit de pagina **Personalisatie** toepassen op de gewenste gebruikers. Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie.
- U kunt ook uw wijzigingen (*aanpassingen* genoemd) exporteren, Stuur ze naar een of meer gebruikers en laat elk van deze gebruikers uw wijzigingen importeren. Met de optie **Beheren** op de aanpassingswerkbalk kunt u persoonlijke instellingen importeren en exporteren.

## <a name="managing-custom-fields"></a>Aangepaste velden beheren

Beheer van de aangepaste velden kan worden uitgevoerd via de pagina **Aangepaste velden** in de module Systeembeheer. Op deze pagina kunnen gebruikers toegang tot veel mogelijkheden krijgen, zoals:

- Een lijst weergeven met alle aangepaste velden in het systeem.
- Beperkt bewerken van bestaande aangepaste velden.
- Aangepaste velden verwijderen.
- Aangepaste velden in gegevensentiteiten weergeven.
- Vertalingen van labels van aangepaste velden en help-tekst bieden.

### <a name="viewing-all-custom-fields"></a>Alle aangepaste velden weergeven

De pagina **Aangepaste velden** biedt inzicht in alle aangepaste velden die zijn gedefinieerd in het systeem. Selecteer de tabel waarin u geïnteresseerd bent en de pagina wordt bijgewerkt met een lijst met aangepaste velden die zijn gekoppeld aan die tabel. Als u een aangepast veld kiest uit de lijst, kunt u alle details weergeven over het veld.

### <a name="editing-custom-fields"></a>Aangepaste velden bewerken

Nadat u een aangepast veld hebt gemaakt, kunnen alleen bepaalde delen van informatie over het aangepaste veld worden gewijzigd op de pagina **Aangepaste velden**.

U *kunt* deze kenmerken wijzigen:

- Etiket
- Help-tekst
- Lengte voor tekstvelden

U kunt de volgende kenmerken *niet* bewerken:

- Veldnaam
- Gegevenstype

Daarnaast kan voor selectielijstvelden, de lijst geldige waarden voor het aangepaste veld opnieuw worden geordend en kunnen nieuwe waarden worden toegevoegd. Bestaande waarden voor het selectielijstveld kunnen echter niet worden verwijderd. Klik op **Wijzigingen toepassen** wanneer u klaar bent met bewerken van velden voor een bepaalde tabel, zodat de wijzigingen worden opgeslagen.

### <a name="exposing-custom-fields-on-data-entities"></a>Aangepaste velden in gegevensentiteiten weergeven

Het is belangrijk toe te staan dat aangepaste velden zichtbaar zijn in gegevensentiteiten. Gegevensentiteiten worden gebruikt in de functie [Overzicht van Office-integratie](../../dev-itpro/office-integration/office-integration.md) en voor scenario's voor het importeren/exporteren van gegevens.

Ga als volgt te werk om een aangepast veld in een gegevensentiteit weer te geven:

1. Selecteer het aangepaste veld op de pagina **Aangepaste velden**.
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

    Als u een bestaande vertaling wilt bewerken, selecteert u de taal in het menu en wijzigt u de waarden voor het label en de help-tekst.

    Klik anders op de knop **Taal toevoegen**, selecteer de gewenste taal in het menu, en geef vertaalde waarden op voor het label en de help-tekst.

4. Wanneer u klaar bent, klikt u op **OK**.

### <a name="deleting-custom-fields"></a>Aangepaste velden verwijderen

Als u besluit dat een aangepast veld niet meer nodig is, kan een systeembeheerder het veld verwijderen van de pagina **Aangepaste velden**. Om een aangepast veld te verwijderen, selecteert u het te verwijderen veld, klikt u op **Verwijderen**, klikt u op **Ja** om de verwijdering te bevestigen en klikt u ten slotte op **Wijzigingen toepassen**.

> [!NOTE]
> Deze actie kan niet ongedaan worden gemaakt en leidt ertoe dat de gegevens die zijn gekoppeld aan het veld, permanent worden verwijderd uit de database.

## <a name="appendix"></a>Bijlage

### <a name="why-cant-i-enter-a-value-in-my-custom-field"></a>Waarom kan ik geen waarde invoeren in mijn aangepaste veld? 

Als u geen waarde in het aangepaste veld kunt typen wanneer de pagina in de modus **Bewerken** wordt weergegeven, is dit mogelijk omdat de tabel waar het veld aan is toegevoegd momenteel alleen-lezen is. Alle velden in een tabel worden alleen-lezen als de archieftabel momenteel is geconfigureerd als alleen-lezen op de pagina.   

### <a name="who-can-create-custom-fields"></a>Wie kan aangepaste velden maken?

Standaard kunnen alleen systeembeheerders aangepaste velden maken. Hoofdgebruikers van wie de organisatie dat nodig vindt, kunnen echter door systeembeheerders rechten worden gegeven om aangepaste velden te maken met de beveiligingsrol **Runtimeaanpassing hoofdgebruiker**. Gebruikers zonder deze beveiligingsrol kunnen geen aangepaste velden maken, maar kunnen aangepaste velden die door andere gebruikers in het systeem zijn gemaakt, wel zien en gebruiken.

### <a name="what-tables-support-custom-fields"></a>Welke tabellen ondersteunen aangepaste velden?

Omwille van prestaties en technische redenen kunnen momenteel alleen aangepaste velden worden toegevoegd aan tabellen die voldoen aan de volgende voorwaarden.

- De tabel moet zijn gemarkeerd als een van deze groepen:

    - Groep
    - WorksheetHeader
    - Hoofdonderdeel
    - Overige
    - Parameter
    - Verwijzing
    - TransactionHeader

- De tabel kan niet een andere tabel uitbreiden.
- De tabel kan niet zijn gemarkeerd als een systeemtabel.
- De tabel kan geen tijdelijke tabel zijn.

### <a name="can-i-reference-custom-fields-from-the-developer-tools"></a>Kan ik naar aangepaste velden verwijzen vanuit de hulpprogramma's voor ontwikkelaars?  

Aangepaste velden kunnen alleen via de gebruikersinterface worden beheerd en er kan niet naar worden verwezen op basis van code. 

### <a name="how-can-i-move-custom-fields-between-environments"></a>Hoe kan ik aangepaste velden verplaatsen tussen omgevingen? 

De huidige aanbeveling voor het verplaatsen van aangepaste velden tussen omgevingen is het handmatig opnieuw maken van de aangepaste velden in de doelomgeving. U kunt als volgt de volledige lijst met aangepaste velden in een bepaalde tabel bekijken:
1. Ga naar de pagina **Aangepaste velden** en selecteer die tabel in de vervolgkeuzelijst. 
2. Volg in de doelomgeving het proces dat eerder in dit artikel is beschreven om elk veld opnieuw te maken. 
3. Wanneer alle velden zijn gemaakt, klikt u op **Wijzigingen toepassen**.  
4. Verplaats alle persoonlijke instellingen met aangepaste velden door die persoonlijke instellingen te exporteren vanuit de oorspronkelijke omgeving en ze in de doelomgeving te importeren.  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
