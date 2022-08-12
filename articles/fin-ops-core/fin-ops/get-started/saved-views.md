---
title: Opgeslagen weergaven
description: In dit artikel wordt beschreven hoe u de functies voor opgeslagen weergaven gebruikt.
author: jasongre
ms.date: 04/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: 14369b02f1d7553be5c732f3bdf768825267998b
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2022
ms.locfileid: "9125145"
---
# <a name="saved-views"></a>Opgeslagen weergaven

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

## <a name="introduction"></a>Inleiding

Personalisatie speelt een belangrijke rol bij het toestaan van gebruikers en organisaties om de gebruikerservaring te optimaliseren op basis van hun behoeften. Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over aanpassingen.

Bij traditionele personalisatie beschikten gebruikers slechts over één set persoonlijke instellingen per pagina. De functie **Opgeslagen weergaven** biedt belangrijke nieuwe mogelijkheden voor personalisatie:

- Gebruikers beschikken over meerdere benoemde sets persoonlijke instellingen per formulier waartussen ze snel kunnen schakelen, waar nodig. Zo kan een gebruiker meerdere geoptimaliseerde weergaven van een pagina maken, waarbij elke weergave is aangepast aan de behoeften van het uitvoeren van een bepaalde bedrijfstaak. 
- Weergaven die voor bepaalde pagina typen worden gemaakt, kunnen ook door de gebruiker toegevoegde filters of sorteringen bevatten. Hierdoor kunnen gebruikers snel terugkeren naar vaak gefilterde gegevens sets. Zie het gedeelte [Welke pagina's weergaven ondersteunen](saved-views.md#what-pages-support-views) voor meer informatie. 
- Weergaven kunnen worden gepubliceerd voor gebruikers in specifieke beveiligingsrollen en specifieke rechtspersonen. Daarom kan elke gebruiker die een opgegeven rol heeft en toegang tot een bepaalde rechtspersoon, toegang krijgen tot die weergave, zelfs als die gebruiker niet gemachtigd is om te personaliseren. Dankzij deze publicatiefunctie kunnen organisaties standaardweergaven voor bedrijven definiëren die voor hun bedrijf zijn geoptimaliseerd. Meer informatie vindt u in de sectie [Persoonlijke instellingen op een organisatieniveau beheren met weergaven](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).
- In tegenstelling tot bij traditionele personalisatie worden weergaven niet automatisch opgeslagen wanneer een gebruiker expliciete aanpassingen uitvoert of een lijst filtert. Expliciet opslaan is vereist om gebruikers de flexibiliteit te geven om een weergave te maken voordat of nadat de wijzigingen die aan die weergave zijn gekoppeld, zijn doorgevoerd. Deze vereiste zorgt er ook voor dat weergavedefinities niet onopzettelijk worden gewijzigd door filters of persoonlijke instellingen die niet voor langetermijngebruik zijn bedoeld. Artikelen die door het systeem automatisch worden opgeslagen als onderdeel van het normale paginagebruik (bijvoorbeeld kolombreedten of de uitgevouwen of samengevouwen status van secties) worden per weergave opgeslagen.
- Weergaven kunnen aan werkgebieden worden toegevoegd als tegels, lijsten of koppelingen. Daarom kan een gefilterde gegevensset worden weergegeven in een werkgebied en kunnen gebruikers een set persoonlijke instellingen die relevant is voor die gegevensset, koppelen aan een tegel of koppeling.

## <a name="switching-between-views"></a>Schakelen tussen weergaven

Als weergaven beschikbaar zijn gemaakt voor een omgeving, bevat de bovenzijde van elke pagina die weergaven ondersteunt, een selectieoptie voor een samengevouwen weergave boven aan het formulier waarin de naam van de huidige weergave wordt weergegeven.

Er zijn twee groottes voor deze weergavekiezer: 

- **Grote weergavekiezers**: pagina's met een aanzienlijke lijst krijgen om enkele redenen een grotere weergavekiezer. In de grotere weergavekiezer worden de pagina's aangegeven waar de weergave door de gebruiker gedefinieerde filters en sorteringen kan bevatten. Aangezien filters en sorteringen in de weergaven zijn opgenomen, is het grotere kiezerformaat ook gerechtvaardigd omdat de weergavenamen vaak de beste beschrijving zijn van de gegevens die op het scherm worden weergegeven en de verwachting is dat gebruikers vaker tussen weergaven schakelen op deze typen pagina's. Groeperingen in een raster kunnen ook worden opgeslagen in weergaven op een pagina met grote weergavekiezers. 
- **Kleine weergavekiezers**: alle andere schermen van volledige paginagrootte (met uitzondering van werkruimten en het dashboard) hebben een kleinere weergavekiezer die naast het paginabijschrift wordt weergegeven. Weergaven op deze pagina's omvatten alleen persoonlijke instellingen en geen door de gebruiker gedefinieerde filters. Op deze pagina's is het formulierbijschrift of de recordtitel vaak de belangrijkste informatie boven aan de pagina. Het kleinere formaat van de weergaveselectie weerspiegelt ook de lagere frequentie van weergavewisseling die op deze pagina's wordt verwacht. 
 
Als u de naam van de weergave selecteert, wordt de weergavekiezer geopend en wordt de lijst met beschikbare weergaven voor de pagina weergegeven.

**Versie 10.0.21 of hoger:** als de **Verbeterde ondersteuning van de rechtspersoon voor opgeslagen weergaven** is ingeschakeld, geeft de weergaveselector de beschikbare weergaven weer in twee secties. De eerste sectie toont alle weergaven die specifiek zijn voor de huidige rechtspersoon, en de tweede sectie toont weergaven die beschikbaar zijn voor alle rechtspersonen. De eerste sectie is alleen zichtbaar als er rechtspersoon-specifieke weergaven voor de pagina zijn.

- **Standaardweergave**: de **standaard** weergave is de out-of-the-box weergave van de pagina waarop geen expliciete persoonlijke instellingen zijn toegepast.
- **Persoonlijke weergaven**: de weergaven zonder hangsloten vertegenwoordigen uw persoonlijke weergaven. Dit zijn weergaven die u hebt gemaakt of die een beheerder aan u heeft gegeven.
- **Vergrendelde weergaven**: sommige weergaven (zoals de **standaard** weergave en alle weergaven die naar uw rol zijn gepubliceerd) worden weergegeven met een hangslot-symbool in de weergaveselectie. Dit symbool geeft aan dat u deze weergaven niet kunt bewerken. Wijzigingen die het paginagebruik weerspiegelen, worden echter automatisch opgeslagen. Deze wijzigingen omvatten wijzigingen in de breedte van een rasterkolom en wijzigingen in de uitgevouwen of samengevouwen status van een sneltabblad. Als u echter over aanpassingsbevoegdheden beschikt, kunt u de actie **Kopie opslaan** gebruiken om op basis van een vergrendelde weergave een persoonlijke weergave te maken.
- **Nieuwe weergaven**: gepubliceerde weergaven die nog niet zijn geopend, hebben een vonksymbool links van de weergavenaam.

Als u naar een andere weergave wilt overschakelen, opent u eerst de weergavekiezer en selecteert vervolgens de weergave die u wilt laden. 

## <a name="creating-and-modifying-views"></a>Weergaven maken en wijzigen

In tegenstelling tot traditionele aanpassing worden weergaven niet automatisch opgeslagen wanneer een gebruiker de pagina aanpast of wanneer een gebruiker een filter toepast op een lijst of deze sorteert. Een expliciete actie is vereist om deze wijzigingen in een weergave op te slaan. Deze vereiste biedt gebruikers de flexibiliteit een weergave te maken voordat of nadat de wijzigingen die aan die weergave zijn gekoppeld, zijn doorgevoerd. Het zorgt er ook voor dat de weergavedefinities niet onopzettelijk worden gewijzigd door eenmalige filters of aanpassingen. Gangbare paginagebruiksitems (bijvoorbeeld kolombreedten of de uitgevouwen of samengevouwen status van secties) worden automatisch in de huidige weergave opgeslagen, zelfs bij vergrendelde weergaven.

Om te zorgen dat de huidige status van de weergave bekend is wanneer u een weergave begint te wijzigen door deze te personaliseren of te filteren, staat er een sterretje (\*) naast de naam van de huidige weergave. Dit symbool geeft aan dat u een niet-opgeslagen, gewijzigde versie van die weergave bekijkt.

Voer de volgende stappen uit als u deze wijzigingen wilt opslaan.

1. Selecteer de weergavenaam om de weergavekiezer te openen.
2. Als u de bestaande weergave wilt wijzigen, selecteert u **Opslaan**. Deze actie is niet beschikbaar voor vergrendelde weergaven. 
3. Een nieuwe weergave maken:

    1. Selecteer **Opslaan als**. 
    2. Voer in het deelvenster **Weergave opslaan als** een naam en desgewenst een omschrijving voor de weergave in.
    3. Als u wilt dat deze weergave de standaardweergave is, selecteert u **Als standaardweergave vastpinnen**. Zie het gedeelte [Standaardweergaven wijzigen](#changing-the-default-view) voor meer informatie over standaardweergaven. 
    4. **Versie 10.0.21 of hoger:** als de **Verbeterde ondersteuning van de rechtspersoon voor opgeslagen weergaven** is ingeschakeld, kunt u selecteren of deze weergave beschikbaar moet zijn voor alle rechtspersonen of slechts voor een aantal van deze rechtspersonen.
    5. Selecteer **Opslaan**.

## <a name="changing-the-default-view"></a>De standaardweergave wijzigen

De standaardweergave is de weergave die het systeem probeert te openen wanneer u de pagina voor het eerst opent. U moet de standaardweergave instellen op de weergave die u het vaakst verwacht te gebruiken. 

> [!NOTE]
> - In de basisfunctie **Opgeslagen weergaven** is er één algemene standaardweergave voor alle rechtspersonen. Als u de standaardweergave wijzigt, wordt deze weergave standaard geopend, ongeacht de rechtspersoon die u op dat moment gebruikt.
> - **Versie 10.0.21 of hoger:** wanneer de **Verbeterde ondersteuning van de rechtspersoon voor opgeslagen weergaven** is ingeschakeld, kan elke rechtspersoon een eigen standaardweergave hebben per pagina.

Volg deze stappen om de standaardweergave voor een pagina te wijzigen:

1. Schakel over naar de weergave die u als standaardweergave gebruikt. 
2. Selecteer de weergavenaam om de weergavekiezer te openen. 
3. Selecteer **Meer** en **Vastmaken als standaard**.

Als u een nieuwe weergave maakt (met de actie **Opslaan als**), kunt u hiervan ook de standaardweergave maken door de optie **Vastmaken als standaard** in te stellen voordat u de weergave opslaat.

> [!WARNING]
> In sommige gevallen wordt de query, die aan de standaardweergave gekoppeld is, niet uitgevoerd wanneer u een pagina voor het eerst opent. Als u bijvoorbeeld de pagina via een tegel opent, wordt de query van de tegel uitgevoerd, ongeacht de query die aan de standaardweergave is gekoppeld. Bovendien, als u een pagina opent waarvan de **standaard** weergave al een gedefinieerde query bevat, wordt de oorspronkelijke query uitgevoerd in plaats van de query van de standaardweergave. In dat geval ontvangt u een informatiebericht wanneer de weergave wordt geladen. Als u schakelt tussen weergaven nadat de pagina is geladen, moet de weergavequery kunnen worden uitgevoerd zoals verwacht. In versie 10.0.10 en later bevat het informatieve bericht dat u ontvangt, een ingesloten actie waarmee u de query van de standaardweergave rechtstreeks kunt laden.

## <a name="managing-personal-views"></a>Persoonlijke weergaven beheren

In het dialoogvenster **Mijn weergaven beheren** beschikt u over basisfuncties voor het onderhoud van uw persoonlijke weergaven en de volgorde van weergaven in de weergavekiezer. Als u deze pagina wilt openen, selecteert u de naam van de weergave om de vervolgkeuzelijst van de weergavekiezer te openen en selecteert u **Meer** en **Mijn weergaven beheren**.

**Versie 10.0.21 of hoger:** als de **Verbeterde ondersteuning van de rechtspersoon voor opgeslagen weergaven** is ingeschakeld, worden in het gedeelte **Mijn weergaven** van het dialoogvenster **Mijn weergaven beheren** de beschikbare weergaven voor de pagina in gedeelten weergegeven. Alle weergaven die specifiek zijn voor de huidige rechtspersoon, worden weergegeven in hun eigen sectie. Het gedeelte **Algemene weergaven** wordt altijd weergegeven, zodat u de weergaven voor de pagina kunt beheren die beschikbaar zijn voor alle rechtspersonen. 

De volgende set acties is beschikbaar voor een lijst met beschikbare weergaven voor die pagina.

- **Standaardweergave wijzigen**: gebruik de actie **Vastmaken als standaard** om de momenteel geselecteerde weergave in te stellen als standaardweergave voor deze pagina. Als de functie **Ondersteuning voor juridische entiteiten importeren voor opgeslagen weergaven** is ingeschakeld, kunt u met het gedeelte **Algemene weergaven** een weergave als standaardweergave instellen voor de huidige rechtspersoon of voor alle rechtspersonen.
- **Volgorde van weergaven wijzigen**: gebruik de acties **Omhoog verplaatsen** en **Omlaag verplaatsen** om de weergaven in een bepaalde volgorde te rangschikken.
- **Naam van weergave wijzigen**: gebruik de actie **Naam wijzigen** om de naam van de huidige geselecteerde persoonlijke weergave te wijzigen. Deze actie is uitgeschakeld voor vergrendelde weergaven. 
- **Weergave verwijderen**: gebruik de actie **Verwijderen** om de momenteel geselecteerde weergave permanent van de pagina te verwijderen. Na verwijdering kunt u een weergave niet meer herstellen.

Eventuele wijzigingen in dit dialoogvenster worden pas van kracht als u de knop **Bijwerken** selecteert.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Persoonlijke instellingen op een organisationeel niveau beheren met weergaven

In deze sectie worden enkele verschillen beschreven in het beheer van persoonlijke instellingen met en zonder de functie **Opgeslagen weergaven**, zodat u beter begrijpt hoe opgeslagen weergaven het beheer van persoonlijke instellingen op organisatieniveau kunnen verbeteren.

Zonder weergaven pasten beheerders een set persoonlijke instellingen voor een pagina toe op een gebruiker of een groep gebruikers via de pagina Persoonlijke instellingen. Als deze gebruikers over rechten voor persoonlijke instellingen beschikten, werden de persoonlijke instellingen toegepast op die pagina. Het was echter niet mogelijk om te voorkomen dat gebruikers de pagina verder zouden aanpassen. wat betekende dat de organisatie niet kon garanderen dat de gebruikers over een consistente gebruikersinterface beschikten. Als een van deze gebruikers niet over rechten voor persoonlijke instellingen beschikte, werden de persoonlijke instellingen die door een beheerder waren toegewezen, niet geladen. En als nieuwe gebruikers in een organisatie werden aangesteld, moesten beheerders handmatig een verzameling persoonlijke instellingen voor die gebruiker laden. Er was geen automatisch mechanisme om op te geven dat een bepaalde set persoonlijke instellingen beschikbaar moesten zijn voor gebruikers met die rol.

De functie **Opgeslagen weergaven** maakt het beheer van persoonlijke instellingen voor een organisatie veel eenvoudiger, voornamelijk omdat weergaven kunnen worden gepubliceerd aan groepen gebruikers. Wanneer een weergave is gepubliceerd, kan elke gebruiker die een van de gedefinieerde beveiligingsrollen heeft en toegang heeft tot de opgegeven rechtspersonen, de weergave zien en deze gebruiken, zelfs als die gebruiker geen toegang heeft tot personalisatie. Hoewel elke gebruiker een kopie heeft van de gepubliceerde weergave waarin paginagebruiksitems automatisch worden toegepast, kan geen enkele gebruiker persoonlijke instellingen of queryupdates opslaan in de gepubliceerde weergave. Anders gezegd, gepubliceerde weergaven zijn vergrendeld. En als nieuwe gebruikers worden toegewezen aan rollen in rechtspersonen waarnaar weergaven zijn gepubliceerd, zien deze gebruikers automatisch de weergaven die aan hun rollen en rechtspersonen zijn gekoppeld. De beheerder hoeft geen aanvullende actie uit te voeren. En als gebruikers in een organisatie van rol veranderen of toegang krijgen tot andere rechtspersonen, hebben ze mogelijk geen toegang meer tot de weergaven die eerder aan hen waren gepubliceerd. Ook hier hoeft de beheerder geen verdere actie te ondernemen.

Updates voor een gepubliceerde weergave kunnen eenvoudig naar gebruikers worden gedistribueerd door de weergave opnieuw naar de betreffende beveiligingsrollen en rechtspersonen te publiceren.

Dankzij de publicatiefunctie kunnen organisaties standaardweergaven voor bedrijven definiëren die voor hun bedrijf zijn geoptimaliseerd, gericht op gebruikers in bepaalde beveiligingsrollen.

## <a name="publishing-views"></a>Weergaven publiceren

Tijdens het publicatieproces kunnen weergaven worden toegewezen aan een of meer beveiligingsrollen voor een of meer rechtspersonen. Elke gebruiker die toegang tot een rechtspersoon heeft en is toegewezen aan een van die rollen kan de weergaven daarom zien en gebruiken. De gebruiker kan de weergaven echter niet bewerken. Systeembeheerders hebben standaard toegang tot de actie **Publiceren** in het vervolgkeuzemenu voor de weergavekiezer. Andere vertrouwde gebruikers in uw organisatie kunnen echter ook toegang krijgen tot het bekijken van publicaties via de nieuwe rol **Beheerder van opgeslagen weergaven**.

Voer deze stappen uit om een weergave te publiceren:

1. Maak een persoonlijke kopie van de weergave die u wilt publiceren en sla deze op. 
2. Selecteer terwijl die weergave is geladen de naam van de weergave om het vervolgkeuzemenu voor de weergavekiezer te openen. 
3. Selecteer de knop **Meer** en selecteer vervolgens **Publiceren**. Het dialoogvenster Publiceren wordt geopend.
4. Voer een naam in voor de weergave. De naam die u invoert, is de naam die gebruikers die deze weergave ontvangen, te zien krijgen in hun weergavekiezers. De namen van gepubliceerde weergaven voor een pagina moeten uniek zijn. Dubbele namen zijn niet toegestaan, ook niet als de lijst met rollen of rechtspersonen waarop de weergaven worden toegepast, verschilt.
5. **10.0.17 of hoger bijwerken**: als de functie voor **(Preview) Vertalingsondersteuning voor organisatieweergaven** is ingeschakeld, kunt u vertalingen voor uw weergavenaam in net zoveel talen toevoegen als voor uw organisatie nodig is door de knop **Vertalingen** naast het veld **Naam** te selecteren. De weergavenaam wordt vervolgens weergegeven voor gebruikers in de huidige taal. U kunt ook de standaardtaal instellen om de vertaling op te geven die wordt weergegeven voor gebruikers die talen gebruiken waarvoor geen vertaling is gedefinieerd.
5. Optioneel: voer een omschrijving voor de weergave in, zodat gebruikers die deze weergave ontvangen, het doel ervan beter begrijpen. 
6. Bepaal of de weergave moet worden gepubliceerd als de standaardweergave voor de geselecteerde gebruikers. Wanneer van een weergave de standaardweergave wordt gemaakt, zien gebruikers deze weergave de volgende keer dat ze de doelpagina openen. De enkele algemene standaardweergave van alle beoogde gebruikers wordt gewijzigd. Gebruikers kunnen hun standaardweergave echter nog steeds wijzigen na publicatie.

    > [!NOTE]
    > Wanneer u een weergave als standaardweergave publiceert, moet u rekening houden met het volgende:
    >
    > - Als u een weergave als standaardweergave voor een aantal of voor alle rechtspersonen publiceert, gebeurt het volgende:
    >
    >    - Als alleen de basisfunctie **Opgeslagen weergaven** is ingeschakeld, wordt de algemene standaardweergave voor elke doelgebruiker gewijzigd. 
    >    - **Versie 10.0.21 of hoger:** als de **Verbeterde ondersteuning van de rechtspersoon voor opgeslagen weergaven** is ingeschakeld en u de weergave publiceert naar een aantal rechtspersonen, wordt de standaardweergave voor deze rechtspersonen voor elke beoogde gebruiker gewijzigd.
    >
    > - Als een gebruiker rollen heeft waar meerdere weergaven worden gepubliceerd als de standaardweergave, wordt de laatst gepubliceerde weergave gebruikt als de standaardweergave van de gebruiker. 

8. Voeg de beveiligingsrollen toe die overeenkomen met de gebruikers voor wie deze weergave is bedoeld. 
9. Bepaal of u de weergave wilt publiceren naar de onderliggende rollen van elke geselecteerde beveiligingsrol. Als u dit doet, schakelt u het selectievakje **Onderliggende rollen opnemen** in de rij voor de gewenste beveiligingsrollen in. Dit selectievakje is niet beschikbaar voor rollen die geen onderliggende rollen hebben.
10. Voeg de rechtspersonen toe waarvoor deze weergave beschikbaar moet zijn. 

    > [!NOTE]
    > Houd rekening met het volgende gedrag wanneer u een weergave naar een specifieke rechtspersoon publiceert, maar wanneer u die weergave niet als de standaardweergave publiceert.
    >
    > - Als alleen de basisfunctie **Opgeslagen weergaven** is ingeschakeld, wordt de weergaveselector van de gebruiker voor de pagina in eerste instantie alleen voor de opgegeven rechtspersonen weergegeven. Nadat de weergave echter voor de eerste keer is geladen, zal de weergaveselector voor de pagina deze altijd tonen, ongeacht de rechtspersoon.
    > - **Versie 10.0.21 of hoger:** als de **Verbeterde ondersteuning van de rechtspersoon voor opgeslagen weergaven** is ingeschakeld, geeft de weergaveselector alleen de weergave voor de opgegeven rechtspersonen weer.

11. Selecteer **Publiceren**.

In sommige omgevingen kan het enige tijd duren (maximaal een uur) voordat gebruikers de gepubliceerde weergave kunnen zien.

## <a name="modifying-a-published-view"></a>Een gepubliceerde weergave wijzigen

Nadat u een weergave hebt gepubliceerd, is het mogelijk dat u deze wilt wijzigen. Hoewel u geen live wijzigingen kunt aanbrengen in een gepubliceerde weergave, omdat deze weergaven zijn vergrendeld voor bewerking voor alle gebruikers (inclusief uitgevers), kunt u een weergave wel opnieuw publiceren om deze bij te werken.

Als de wijzigingen die u wilt aanbrengen in een gepubliceerde weergave alleen betrekking hebben op de publicatieparameters (de naam en omschrijving van de weergave of de beveiligingsrollen waarnaar de weergave wordt gepubliceerd), gaat u als volgt te werk:

1. Schakel over naar de gepubliceerde weergave voor de parameters die u wilt bijwerken. 
2. Selecteer **Opnieuw publiceren** in het vervolgkeuzemenu voor de weergavekiezer. Als u versie 10.0.12 of eerder gebruikt, moet u **Publiceren** selecteren en vervolgens **Ja** om de bestaande weergave bij te werken.
3. Werk de naam, omschrijving, beveiligingsrollen en rechtspersonen voor de weergave bij. 
4. Selecteer **Publiceren**. Als u oorspronkelijk deze gepubliceerde weergave als standaardweergave hebt geselecteerd, is dit weer de standaardweergave voor gebruikers nadat u deze opnieuw hebt gepubliceerd. 

Als de wijzigingen in de gepubliceerde weergave betrekking hebben op de persoonlijke instellingen of filters gekoppeld aan de weergave, gaat u als volgt te werk.

1. Laad de gepubliceerde weergave die u wilt wijzigen. 
2. Breng de vereiste wijzigingen in het lokale concept aan.
3. Selecteer **Opnieuw publiceren** in het vervolgkeuzemenu voor de weergavekiezer.
4. Selecteer **Ja** om aan te geven dat u de weergave samen met de niet-opgeslagen wijzigingen wilt publiceren. 
5. Pas de publicatieparameters aan die moeten worden gecorrigeerd en selecteer **Publiceren**. 

## <a name="managing-published-views"></a>Gepubliceerde weergaven beheren

Net als bij het beheren van persoonlijke weergaven biedt het dialoogvenster **Mijn weergaven beheren** gebruikers met publicatiebevoegdheden de basisbeheerfuncties voor de gepubliceerde weergaven van die pagina (naast hun eigen persoonlijke weergaven). Als u deze pagina wilt openen, selecteert u de naam van de weergave om de vervolgkeuzelijst van de weergavekiezer te openen en selecteert u **Meer** en **Mijn weergaven beheren**.

Hoewel alle gebruikers een tabblad **Mijn weergaven** hebben met hun persoonlijke weergaven, hebben gebruikers met publicatiebevoegdheden ook een tabblad **Organisatieweergaven**, waarop alle gepubliceerde en niet-gepubliceerde weergaven voor die pagina worden weergegeven. Omdat er verschillende gebruikers kunnen zijn die weergaven publiceren, is het belangrijk dat u de volledige lijst met gepubliceerde weergaven beheert, zelfs als u niet de gebruiker bent die een bepaalde weergave heeft gepubliceerd.

De volgende set acties is beschikbaar voor de lijst met alle gepubliceerde weergaven voor de pagina. 

- **Opnieuw publiceren**: gebruik de actie **Opnieuw publiceren** om een weergave opnieuw te publiceren nadat publicatieparameters (naam, omschrijving, beveiligingsrollen of rechtspersonen) zijn gewijzigd.
- **Publiceren**: gebruik de actie **Publiceren** om een weergave te publiceren die momenteel niet is gepubliceerd. 
- **Publicatie ongedaan maken**: gebruik de actie **Publicatie ongedaan maken** om een weergave inactief te maken. De weergave is nog steeds beschikbaar in het systeem, maar gebruikers zien deze niet in de weergaveselectie totdat de weergave opnieuw wordt gepubliceerd.
- **Opslaan als persoonlijk**: gebruik de actie **Opslaan als persoonlijk** om een persoonlijk conceptexemplaar van de gepubliceerde weergave te maken. Deze mogelijkheid helpt u de inhoud te begrijpen van een weergave die niet naar u is gepubliceerd of die nog niet is gepubliceerd. U kunt deze ook gebruiken om een weergave te bewerken en opnieuw te publiceren.
- **Verwijderen**: gebruik de actie **Verwijderen** om een gepubliceerde of niet-gepubliceerde weergave definitief te verwijderen. Met deze actie verwijdert u de weergave ook voor alle gebruikers in het systeem. Het verwijderen van gepubliceerde weergaven wordt van kracht nadat op de knop **Opslaan** is geklikt. Nadat een weergave is verwijderd, kan deze niet meer worden hersteld. 

## <a name="managing-views-globally"></a>Weergaven globaal beheren

Hoewel sommige beheermogelijkheden op elke pagina zichtbaar zijn, zoals in dit artikel wordt aangegeven, kunnen weergaven door **systeembeheerders** en **beheerders van opgeslagen weergaven** op een meer holistische wijze voor het systeem worden beheerd via de pagina **Persoonlijke instellingen**. Deze pagina biedt de volgende secties en mogelijkheden: 

- **Gepubliceerde weergaven**: in deze sectie worden alle weergaven vermeld die voor uw organisatie zijn gepubliceerd. Hier kunt u een weergave opnieuw publiceren nadat u de beveiligingsrollen of rechtspersonen in de weergave hebt aangepast. U kunt weergaven ook exporteren, verwijderen of de publicatie ervan ongedaan maken. U kunt de actie **Opslaan als persoonlijk** gebruiken om een persoonlijke kopie van een weergave te maken, zodat u de weergave kunt bijwerken of een beter begrip van de inhoud kunt krijgen. 
- **Niet-gepubliceerde weergaven**: in deze sectie worden alle organisatieweergaven in uw systeem weergegeven die momenteel niet zijn gepubliceerd. Deze weergaven komen het vaakst in het systeem via de importmogelijkheid. U kunt deze weergaven publiceren, exporteren of verwijderen. Met de actie **Snel publiceren** die is toegevoegd in versie 10.0.12, kunnen meerdere weergaven uit deze sectie in één actie worden gepubliceerd met behulp van de bestaande configuratie voor beveiligingsrollen en rechtspersonen. U kunt de actie **Opslaan als persoonlijk** gebruiken om persoonlijke kopieën van deze weergaven te maken, zodat u een beter begrip van de inhoud kunt krijgen.
- **Persoonlijke weergaven**: alle weergaven die zijn gemaakt door gebruikers in het systeem. U kunt hier een persoonlijke weergave voor de organisatie publiceren of een of meer van deze weergaven naar andere gebruikers kopiëren. U kunt deze weergaven ook publiceren, exporteren of verwijderen.
- **Gebruikers instellingen**: selecteer de gebruiker die u wilt bekijken of pas het vermogen van de gebruiker om personalisatie te gebruiken aan voor het gehele systeem of voor specifieke pagina's die de gebruiker heeft bezocht. U kunt de persoonlijke instellingen van de gebruiker in het systeem weergeven en ermee werken. U kunt ook alle persoonlijke instellingen voor die gebruiker verwijderen of de functietoelichtingen voor de gebruiker opnieuw instellen. Als functietoelichtingen opnieuw worden ingesteld, worden pop-upvensters die nieuwe functies hebben geïntroduceerd en die de gebruiker eerder heeft gesloten, opnieuw weergegeven wanneer de gebruiker die functies opnieuw tegenkomt.
- **Systeeminstellingen**: u kunt aanpassingen voor alle gebruikers in het systeem tijdelijk uitschakelen. In dat geval worden geen aanpassingen voor gebruikers toegepast en worden alle pagina's opnieuw ingesteld op de standaardstatus. Als u aanpassingen later weer wilt inschakelen, worden alle aanpassingen opnieuw toegepast. U kunt alle aanpassingen voor alle gebruikers in het systeem ook permanent verwijderen. Er is geen enkele manier om aanpassingen terug te halen die zijn verwijderd. Voordat u deze taak uitvoert, moet u er daarom voor zorgen dat u aanpassingen hebt geëxporteerd die u later mogelijk wilt.

Gebruikers die toegang hebben tot de pagina **Aanpassing** kunnen ook persoonlijke sjablonen of organisatieweergaven importeren met de knop **Weergaven importeren** in het actievenster. Voor organisatieweergaven kunt u **Onmiddellijk publiceren** selecteren om de weergaven beschikbaar te maken voor gebruikers zonder dat deze nog expliciet worden gepubliceerd.

## <a name="known-issues"></a>Bekende problemen

Voor een lijst met bekende problemen met opgeslagen weergaven raadpleegt u [Formulieren maken waarin opgeslagen weergaven volledig worden gebruikt](../../dev-itpro/user-interface/understanding-saved-views.md).

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Hoe schakel ik opgeslagen weergaven in mijn omgeving in?

> [!NOTE]
> Voor de functie **Opgeslagen weergaven** moet het personalisatiesysteem in de apps voor financiën en bedrijfsactiviteiten zijn ingeschakeld. Als persoonlijke instellingen zijn uitgeschakeld voor de gehele omgeving, worden weergaven wel uitgeschakeld, ook als u de onderstaande stappen uitvoert. 

U kunt de functie **Opgeslagen weergaven** in- en uitschakelen via Functiebeheer in elke omgeving. Wanneer de functie is ingeschakeld, worden opgeslagen weergaven ingeschakeld in alle volgende gebruikerssessies.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Wat gebeurt er met bestaande persoonlijke instellingen wanneer weergaven worden ingeschakeld? 

Wanneer weergaven worden ingeschakeld, worden bestaande persoonlijke instellingen voor een gebruiker en formulier opgeslagen in een nieuwe weergave met de naam **Mijn weergave** die automatisch wordt ingesteld als de standaardweergave. Dit is bedoeld om ervoor te zorgen dat er een consistente gebruikerservaring bestaat voor- en nadat weergaven worden ingeschakeld, behalve dat de weergavekiezer wordt weergegeven in formulieren.

### <a name="what-pages-support-views"></a>Welke pagina's ondersteunen weergaven? 

Weergaven zijn beschikbaar op de meeste, maar niet alle pagina's. Weergaven zijn momenteel beschikbaar op alle pagina's in het volledige scherm, met uitzondering van dashboards en werkgebieden. Andere pagina's, zoals dialoogvensters, vervolgkeuzemenu's, zoekopdrachten en verbeterde voorbeelden, ondersteunen momenteel geen weergaven. Mogelijk bieden andere paginatypen, zoals werkgebieden en dialoogvensters, wel ondersteuning voor weergaven in toekomstige updates.

### <a name="who-is-allowed-to-publish-views"></a>Wie mag weergaven publiceren?

Alleen systeembeheerders en gebruikers aan wie de rol **Beheerder van opgeslagen weergaven** is toegewezen, zijn gemachtigd om weergaven te publiceren. 

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Waarom kan ik filters niet opslaan met deze weergave? 

Er zijn een aantal redenen waarom een filter mogelijk niet wordt opgeslagen met een weergave: 

- Het opslaan van filters wordt mogelijk niet door de pagina ondersteund als onderdeel van de weergavedefinitie. Alleen voor pagina's met grote weergavekiezers kunnen persoonlijke instellingen en querywijzigingen worden opgeslagen als weergave. Zie **Schakelen tussen weergaven** voor meer informatie. 
- De desbetreffende pagina kan weergaven mogelijk niet goed ondersteunen, omdat deze de weergavequery volledig kan negeren of kan werken op een tijdelijke tabel waarvan de gegevens niet persistent zijn. 

### <a name="what-data-will-i-see-when-i-visit-a-page"></a>Welke gegevens worden weergegeven wanneer ik een pagina bezoek?

Voor pagina's met kleine weergavekiezers (alleen persoonlijke instellingen kunnen in de weergave worden opgeslagen) worden dezelfde gegevens weergegeven als bij elk voorgaande bezoek aan de pagina. 

Voor pagina's met grote weergavekiezers (zowel persoonlijke instellingen als query's kunnen in de weergave worden opgeslagen) ziet u meestal de gegevens die zijn gekoppeld aan de query die bij uw standaardweergave hoort. Er zijn twee belangrijke uitzonderingen:

- Als u van een tegel naar een pagina navigeert, wordt de query uitgevoerd, ongeacht de query die aan de standaardweergave is gekoppeld. Als u deze tegel hebt gemaakt nadat weergaven zijn ingeschakeld, wordt door het selecteren van een tegel de pagina geopend met de weergave die aan die tegel is gekoppeld.
- Als u naar een pagina gaat en dat invoerpunt query bevat, wordt de oorspronkelijke query uitgevoerd in plaats van de query van de standaardweergave. Wanneer dat gebeurt, moet u een waarschuwing krijgen in een informatief bericht wanneer de weergave wordt geladen. U kunt ook bevestigen door naar deze pagina over te schakelen nadat de pagina is geladen,aangezien de weergavequery in dat geval sowieso moet worden uitgevoerd.

### <a name="why-is-a-view-that-was-published-for-a-specific-legal-entity-visible-in-all-legal-entities"></a>Waarom is een weergave, die voor een specifieke rechtspersoon gepubliceerd is, zichtbaar voor alle rechtspersonen?

Als u een weergave naar een specifieke rechtspersoon publiceert, maar wanneer u die weergave niet als de standaardweergave publiceert, gebeurt het volgende:

- Als alleen de basisfunctie **Opgeslagen weergaven** is ingeschakeld, wordt de weergaveselector van de gebruiker voor de pagina in eerste instantie alleen voor de opgegeven rechtspersonen weergegeven. Nadat de weergave echter voor de eerste keer is geladen, zal de weergaveselector voor de pagina deze altijd tonen, ongeacht de rechtspersoon. Dit vindt plaats, omdat gebruikers een eigen kopie krijgen van de gepubliceerde weergave wanneer deze wordt geladen en omdat persoonlijke weergaven algemeen zijn.
- **Versie 10.0.21 of hoger:** als de **Verbeterde ondersteuning van de rechtspersoon voor opgeslagen weergaven** is ingeschakeld, geeft de weergaveselector alleen de weergave voor de opgegeven rechtspersonen weer. Dit vindt plaats, omdat de functie weergaven (inclusief persoonlijke weergaven) aan specifieke rechtspersonen koppelt.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

