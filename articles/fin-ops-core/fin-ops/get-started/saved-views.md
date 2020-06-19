---
title: Opgeslagen weergaven
description: In dit onderwerp wordt beschreven hoe u de functies voor opgeslagen weergaven gebruikt.
author: jasongre
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2019-07-31
ms.dyn365.ops.version: Platform update 28
ms.openlocfilehash: f6b7f1c64c273f52dc1d414185ba54efdfb8e5c0
ms.sourcegitcommit: dc67232c9aa3223d42f22cc1f7aafbd121e7e616
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/30/2020
ms.locfileid: "3412326"
---
# <a name="saved-views"></a>Opgeslagen weergaven

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Introductie
Personalisatie speelt een belangrijke rol bij het toestaan van gebruikers en organisaties om de gebruikerservaring te optimaliseren op basis van hun behoeften. Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over aanpassingen.

Bij traditionele personalisatie beschikten gebruikers slechts over één set persoonlijke instellingen per formulier. Opgeslagen weergaven biedt op verschillende belangrijke manieren meer mogelijkheden:

-    Gebruikers beschikken over meerdere benoemde sets persoonlijke instellingen per formulier waartussen ze snel kunnen schakelen, waar nodig. Zo kan een gebruiker meerdere geoptimaliseerde weergaven van een pagina maken, waarbij elke weergave is aangepast aan de behoeften van het uitvoeren van een bepaalde bedrijfstaak. 

-    Weergaven die voor bepaalde pagina typen worden gemaakt, kunnen ook door de gebruiker toegevoegde filters of sorteringen bevatten. Hierdoor kunnen gebruikers snel terugkeren naar vaak gefilterde gegevens sets. Zie het gedeelte [Welke pagina's weergaven ondersteunen](saved-views.md#what-pages-support-views) voor meer informatie. 

-    Weergaven kunnen worden gepubliceerd voor gebruikers in specifieke beveiligingsrollen en specifieke rechtspersonen. Daarom kan elke gebruiker die een opgegeven rol heeft in en toegang tot een bepaalde rechtspersoon, toegang krijgen tot die weergave en deze gebruiken, zelfs als die gebruiker deze mogelijk niet kan aanpassen. Dankzij deze publicatiefunctie kunnen organisaties standaardweergaven voor bedrijven definiëren die voor hun bedrijf zijn geoptimaliseerd. Meer informatie vindt u in de sectie [Persoonlijke instellingen op een organisatieniveau beheren met weergaven](saved-views.md#managing-personalizations-at-an-organizational-level-with-views).

-    In tegenstelling tot bij traditionele personalisatie worden weergaven niet automatisch opgeslagen wanneer een gebruiker expliciete aanpassingen uitvoert of een lijst filtert. Expliciete opslag is vereist om flexibiliteit te bieden bij het maken van een weergave voor- of nadat de wijzigingen gekoppeld aan die weergave zijn aangebracht en om ervoor te zorgen dat weergavedefinities niet per ongeluk worden gewijzigd door filters of persoonlijke instellingen die niet zijn bedoeld voor langetermijngebruik.  

-    Weergaven kunnen aan werkgebieden worden toegevoegd als tegels, lijsten of koppelingen. Daarom kan een gefilterde gegevensset worden weergegeven in een werkgebied en kunnen gebruikers een set persoonlijke instellingen die relevant is voor die gegevensset, koppelen aan de tegel of koppeling.

## <a name="switching-between-views"></a>Schakelen tussen weergaven
Als weergaven zijn ingeschakeld voor een omgeving, bevat elke pagina die weergaven ondersteunt een selectieoptie voor een samengevouwen weergave boven aan het formulier waarin de naam van de huidige weergave wordt weergegeven.  

Er zijn twee groottes voor deze weergavekiezer: 

-   **Grote weergavekiezers**: pagina's met een aanzienlijke lijst krijgen om enkele redenen een grotere weergavekiezer. In de grotere weergavekiezer worden de pagina's aangegeven waar de weergave door de gebruiker gedefinieerde filters kan bevatten. Aangezien filters in de weergaven zijn opgenomen, is het grotere kiezerformaat ook gerechtvaardigd omdat de weergavenamen vaak de beste beschrijving zijn van de gegevens die op het scherm worden weergegeven en de verwachting is dat gebruikers vaker tussen weergaven schakelen op deze typen pagina's.  
 
-   **Kleine weergavekiezers**: alle andere formulieren van volledige paginagrootte (met uitzondering van werkruimten en het dashboard) hebben een kleinere weergavekiezer die naast het paginabijschrift wordt weergegeven. Weergaven op deze pagina's omvatten alleen persoonlijke instellingen (en geen door de gebruiker gedefinieerde filters). Op deze pagina's is het formulierbijschrift of de recordtitel vaak de belangrijkste informatie boven aan het formulier. De kleinere grootte weerspiegelt ook een lagere verwachte frequentie aan schakelingen tussen weergaven op deze pagina's. 
 
Als u op de naam van de weergave klikt, wordt de weergavekiezer geopend en wordt de lijst met beschikbare weergaven voor deze pagina weergegeven.

-    **Standaardweergave**: de **Standaard**weergave (voorheen de **Klassieke** weergave genoemd) is de out-of-box-weergave van de pagina, waarop geen expliciete persoonlijke instellingen zijn toegepast.
-    **Persoonlijke weergaven**: de weergaven zonder hangsloten vertegenwoordigen uw persoonlijke weergaven. Dit zijn weergaven die u hebt gemaakt of die een beheerder aan u heeft gegeven.  
-    **Vergrendelde weergaven**: sommige weergaven (zoals de **Standaard**weergave en alle weergaven die naar uw rol zijn gepubliceerd) worden weergegeven met een hangslot-symbool. Dit symbool geeft aan dat u deze weergaven niet kunt bewerken. Impliciete persoonlijke instellingen die het paginagebruik weerspiegelen, worden echter automatisch opgeslagen. Deze impliciete persoonlijke instellingen omvatten het wijzigen van de breedte van een rasterkolom of het uitbreiden of samenvouwen van een sneltabblad. Als u echter over aanpassingsbevoegdheden beschikt, kunt u de actie **Kopie opslaan** gebruiken om op basis van een vergrendelde weergave een persoonlijke weergave te maken.
-    **Nieuwe weergaven**: gepubliceerde weergaven die nog niet zijn geopend, worden afgebakend door een vonk links van de weergavenaam.  

Als u naar een andere weergave wilt overschakelen, opent u eerst de weergavekiezer en selecteert vervolgens de weergave die u wilt laden. 

## <a name="creating-and-modifying-views"></a>Weergaven maken en wijzigen
In tegenstelling tot bij traditionele personalisatie worden weergaven niet automatisch opgeslagen wanneer een gebruiker expliciete aanpassingen uitvoert (of een lijst filtert). Een expliciete actie is vereist om deze wijzigingen in een weergave op te slaan. Dit biedt de gebruiker flexibiliteit bij het maken van een weergave voor- of nadat de wijzigingen gekoppeld aan die weergave zijn aangebracht en om ervoor te zorgen dat weergavedefinities niet per ongeluk worden gewijzigd door eenmalige filters of persoonlijke instellingen. Impliciete aanpassingen (zoals het uit- of samenvouwen van een sneltabblad of het wijzigen van de breedte van een rasterkolom) worden automatisch opgeslagen in de huidige weergave, zelfs voor vergrendelde weergaven. 

Om er zeker van te zijn dat de huidige status van de weergave bekend wordt er, wanneer u wijzigingen begint aan te brengen in een weergave door een expliciete aanpassing uit te voeren of filters toe te passen, een sterretje naast de huidige weergavenaam weergegeven om aan te geven dat u een niet-opgeslagen, gewijzigde versie van die weergave bekijkt.

Voer de volgende stappen uit als u deze wijzigingen wilt opslaan.
1.  Selecteer de weergavenaam om de weergavekiezer te openen.
2.  De bestaande weergave wijzigen:
     1. Selecteer **Opslaan**. Deze actie wordt niet ingeschakeld voor vergrendelde weergaven. 
3.  Een nieuwe weergave maken:
     1.    Selecteer **Opslaan als**. 
     2.    Voer een naam en desgewenst een omschrijving in.
     3.    Selecteer **Opslaan**.

## <a name="changing-the-default-view"></a>De standaardweergave wijzigen
De standaardweergave is de weergave die het systeem probeert te openen wanneer u voor het eerst naar de pagina gaat. U moet deze instellen op de weergave die u het vaakst verwacht te gebruiken.  

Volg deze stappen om de standaardweergave voor een pagina te wijzigen: 
1.  Schakel over naar de weergave die u als standaardweergave gebruikt. 
2.  Selecteer de weergavenaam om de weergavekiezer te openen. 
3.  Selecteer **Meer** en **Vastmaken als standaard**.  

Als u een nieuwe weergave maakt (met de actie **Opslaan als**), kunt u hiervan ook de standaardweergave maken door de optie **Vastmaken als standaard** in te stellen voordat u de weergave opslaat.

In sommige gevallen wordt de query die is gekoppeld aan de standaardweergave niet uitgevoerd wanneer u voor het eerst naar een pagina gaat. Als u bijvoorbeeld via een tegel naar een pagina navigeert, wordt de query van de tegel uitgevoerd, ongeacht de query die aan de standaardweergave is gekoppeld. Als u naar een pagina navigeert waarvan de standaardweergave al een gedefinieerde query bevat, wordt de oorspronkelijke query uitgevoerd in plaats van de query van de standaardweergave. In dat geval wordt u gewaarschuwd door een informatief bericht wanneer de weergave wordt geladen. Als u naar een andere weergave schakelt nadat de pagina is geladen, wordt de weergavequery weer zoals verwacht uitgevoerd. Vanaf versie 10.0.10 platformupdate 34 bevat het informatieve bericht een ingesloten actie waarmee u de query van de standaardweergave rechtstreeks kunt laden.

## <a name="managing-personal-views"></a>Persoonlijke weergaven beheren 
In het dialoogvenster **Mijn weergaven beheren** beschikt u over basisfuncties voor het onderhoud van uw persoonlijke weergaven en de volgorde van weergaven in de weergavekiezer. Als u deze pagina wilt openen, klikt u op de naam van de weergave om de vervolgkeuzelijst van de weergavekiezer te openen en selecteert u **Meer** en **Mijn weergaven beheren**.  

De volgende set acties is beschikbaar voor een lijst met beschikbare weergaven voor die pagina.  
-    **Standaardweergave wijzigen**: gebruik de actie **Vastmaken als standaard** om de momenteel gemarkeerde weergave in te stellen als standaardweergave voor deze pagina.  
-    **Volgorde van weergaven wijzigen**: gebruik de acties **Omhoog** en **Omlaag** om de weergaven in een bepaalde volgorde te rangschikken.  
-    **Naam van weergave wijzigen**: gebruik de actie **Naam wijzigen** om de naam van de gemarkeerde persoonlijke weergave te wijzigen. Deze actie is uitgeschakeld voor vergrendelde weergaven. 
-    **Weergave verwijderen**: gebruik de actie **Verwijderen** om de momenteel gemarkeerde weergave permanent van de pagina te verwijderen. Na verwijdering kunt u een weergave niet meer herstellen.  

Eventuele wijzigingen in dit dialoogvenster worden pas van kracht als u de knop **Opslaan** selecteert.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Persoonlijke instellingen op een organisationeel niveau beheren met weergaven
In deze sectie worden enkele verschillen beschreven in het beheer van persoonlijke instellingen met en zonder de functie opgeslagen weergaven, zodat u beter begrijpt hoe opgeslagen weergaven het beheer van persoonlijke instellingen op organisatieniveau kunnen verbeteren.

Zonder weergaven pasten beheerders een set persoonlijke instellingen voor een pagina toe op een gebruiker of een groep gebruikers via de pagina Persoonlijke instellingen. Als deze gebruikers over rechten voor persoonlijke instellingen beschikten, werden de persoonlijke instellingen toegepast op die pagina. Het was echter niet mogelijk om te voorkomen dat gebruikers de pagina verder zouden aanpassen. wat betekende dat de organisatie niet kon garanderen dat de gebruikers over een consistente gebruikersinterface beschikten. Als een van deze gebruikers niet over rechten voor persoonlijke instellingen beschikte, werden de persoonlijke instellingen die door een beheerder waren toegewezen, niet geladen. En als nieuwe gebruikers in een organisatie werden aangesteld, moesten beheerders handmatig een verzameling persoonlijke instellingen voor die gebruiker laden. Er was geen automatisch mechanisme om op te geven dat een bepaalde set persoonlijke instellingen beschikbaar moesten zijn voor gebruikers met die rol.

De functie voor opgeslagen weergaven maakt het beheer van persoonlijke instellingen voor een organisatie aanzienlijk eenvoudiger, voornamelijk omdat weergaven kunnen worden gepubliceerd aan groepen gebruikers. Wanneer een weergave is gepubliceerd, kan elke gebruiker die een van de gedefinieerde beveiligingsrollen heeft en toegang heeft tot de opgegeven rechtspersonen, de weergave zien en deze gebruiken, zelfs als die gebruiker deze mogelijk niet kan aanpassen. Hoewel elke gebruiker een kopie heeft van de gepubliceerde weergave waarin het paginagebruik (impliciete persoonlijke instellingen) automatisch wordt toegepast, kan geen enkele gebruiker expliciete persoonlijke instellingen of queryupdates opslaan in de gepubliceerde weergave. Anders gezegd, gepubliceerde weergaven zijn vergrendeld. En als nieuwe gebruikers rollen krijgen in rechtspersonen waarnaar weergaven zijn gepubliceerd, zien deze gebruikers automatisch de weergaven die aan hun rollen en rechtspersonen zijn gekoppeld. Hier hoeft de beheerder geen verdere actie te ondernemen. En als gebruikers in een organisatie van rol veranderen of toegang krijgen tot andere rechtspersonen, hebben ze mogelijk geen toegang meer tot de weergaven die eerder aan hen waren gepubliceerd. Ook hier hoeft de beheerder geen verdere actie te ondernemen.

Updates voor een gepubliceerde weergave kunnen eenvoudig naar gebruikers worden gedistribueerd door de weergave opnieuw naar de betreffende beveiligingsrollen en rechtspersonen te publiceren.

Dankzij de publicatiefunctie kunnen organisaties standaardweergaven voor bedrijven definiëren die voor hun bedrijf zijn geoptimaliseerd, gericht op gebruikers in bepaalde beveiligingsrollen.  

## <a name="publishing-views"></a>Weergaven publiceren
Tijdens het publicatieproces kunnen weergaven worden toegewezen aan een of meer beveiligingsrollen voor een of meer rechtspersonen. Dat betekent dat een gebruiker die toegang heeft tot een rechtspersoon en die aan een van deze rollen is toegewezen, toegang heeft tot de weergaven en deze kan gebruiken, hoewel hij ze niet kan bewerken. Systeembeheerders hebben toegang tot de actie **Publiceren** in het vervolgkeuzemenu voor de weergavekiezer. Andere vertrouwde gebruikers in uw organisatie kunnen echter ook toegang krijgen tot het bekijken van publicaties via de nieuwe rol **Beheerder van opgeslagen weergaven**.

Voer deze stappen uit om een weergave te publiceren: 
1.  Maak een persoonlijke kopie van de weergave die u wilt publiceren en sla deze op. 
2.  Selecteer terwijl die weergave is geladen de naam van de weergave om het vervolgkeuzemenu voor de weergavekiezer te openen. 
3.  Selecteer de knop **Meer** en selecteer vervolgens **Publiceren**. Het dialoogvenster Publiceren wordt geopend.  
4.  Voer een naam en desgewenst een omschrijving voor de weergave in. De naam die u invoert, is de naam die gebruikers die deze weergave ontvangen, te zien krijgen in hun weergavekiezers. De namen van gepubliceerde weergaven voor een pagina moeten uniek zijn. Dubbele namen zijn niet toegestaan, ook niet als de lijst met rollen of rechtspersonen waarop de weergaven worden toegepast, verschilt.
5.  Voeg de beveiligingsrollen toe die overeenkomen met de gebruikers voor wie deze weergave is bedoeld.
6. Voeg de rechtspersonen toe waarvoor deze weergave beschikbaar moet zijn. 
7. [10.0.9/platformupdate 33 of hoger] Bepaal of de weergave moet worden gepubliceerd als de standaardweergave voor de geselecteerde gebruikers. Een weergave instellen als standaardweergave betekent dat gebruikers deze weergave zien de volgende keer dat ze de doelpagina openen. Hierdoor wordt de standaardweergave voor deze gebruikers gewijzigd. Gebruikers kunnen hun eigen standaardweergave echter nog steeds wijzigen nadat de publicatie heeft plaatsgevonden.    
8.  Selecteer **Publiceren**.

In sommige omgevingen kan het enige tijd duren (maximaal een uur) voordat gebruikers de gepubliceerde weergave kunnen zien.

## <a name="modifying-a-published-view"></a>Een gepubliceerde weergave wijzigen
Na publicatie van een weergave kunt u er achter komen dat u nog wijzigingen in een gepubliceerde weergave wilt aanbrengen. Hoewel u geen live wijzigingen kunt aanbrengen in een gepubliceerde weergave, omdat deze weergaven zijn vergrendeld voor bewerking voor alle gebruikers (inclusief uitgevers), kunt u een weergave wel opnieuw publiceren voor updates.  

Als de wijzigingen die u wilt aanbrengen in een gepubliceerde weergave alleen betrekking hebben op de publicatieparameters (de naam en omschrijving van de weergave of de beveiligingsrollen waarnaar de weergave wordt gepubliceerd), gaat u als volgt te werk: 
1.  Schakel over naar de gepubliceerde weergave voor de parameters die u wilt bijwerken. 
2.  Selecteer **Publiceren** in het vervolgkeuzemenu voor de weergavekiezer. 
3.  Selecteer **Ja** als u de bestaande weergave wilt bijwerken (of **Nee** als u deze wilt publiceren onder een andere naam).
4.  Werk de naam, omschrijving en/of beveiligingsrollen voor de weergave bij. 
5.  Selecteer **Publiceren**. 
6.  [10.0.8/platformupdate 32 of eerder] Als u de naam van de gepubliceerde weergave hebt bijgewerkt, moet u ook de gepubliceerde weergave met de oude naam verwijderen (zie **Gepubliceerde weergaven beheren** voor meer informatie). 
7. [10.0.9/platform update 33 of hoger] Als u deze gepubliceerde weergave eerder had ingesteld als standaardweergave, wordt dit opnieuw de standaardweergave voor deze gebruikers nadat hij opnieuw is gepubliceerd.  

Als de wijzigingen in de gepubliceerde weergave betrekking hebben op de persoonlijke instellingen of filters gekoppeld aan de weergave, gaat u als volgt te werk: 
1.  Laad de gepubliceerde weergave die u wilt wijzigen. 
2.  Sla een kopie van de gepubliceerde weergave op om een lokaal concept van de gepubliceerde weergave te maken. 
3.  Wijzig het lokale concept met de benodigde wijzigingen.
4.  Publiceer de weergave onder de oorspronkelijke naam. 

## <a name="managing-published-views"></a>Gepubliceerde weergaven beheren
Net als bij het beheren van persoonlijke weergaven biedt het dialoogvenster **Mijn weergaven beheren** gebruikers met publicatiebevoegdheden de basisbeheerfuncties voor de gepubliceerde weergaven van die pagina (naast hun eigen persoonlijke weergaven). Als u deze pagina wilt openen, selecteert u de naam van de weergave om de vervolgkeuzelijst van de weergavekiezer te openen en selecteert u **Meer** en **Mijn weergaven beheren**.

Hoewel alle gebruikers het tabblad **Mijn weergaven** met hun persoonlijke weergaven te zien krijgen, zien gebruikers met publicatiebevoegdheden ook het tabblad **Gepubliceerd** waarop alle gepubliceerde weergaven voor die pagina worden weergegeven. Omdat er verschillende gebruikers kunnen zijn die weergaven publiceren, is het belangrijk dat u de volledige lijst met gepubliceerde weergaven beheert, ongeacht of u de gebruiker bent die de weergave daadwerkelijk heeft gepubliceerd.

De volgende set acties is beschikbaar voor de lijst met alle gepubliceerde weergaven voor de pagina. 

-    **Publiceren**: gebruik de actie **Publiceren** om een weergave opnieuw te publiceren nadat publicatieparameters (naam, omschrijving, beveiligingsrollen of rechtspersonen) zijn gewijzigd.
-    **Opslaan als persoonlijk**: gebruik de actie **Opslaan als persoonlijk** om een persoonlijk conceptexemplaar van de gepubliceerde weergave te maken. Deze mogelijkheid helpt u de inhoud te begrijpen van een weergave die niet naar u is gepubliceerd of die nog niet is gepubliceerd. U kunt deze ook gebruiken om een weergave te bewerken en opnieuw te publiceren. Deze mogelijkheid is geïntroduceerd in versie 10.0.12.  
-    **Verwijderen**: gebruik de actie **Verwijderen** om een gepubliceerde weergave definitief te verwijderen. Met deze actie verwijdert u de weergave voor alle gebruikers in het systeem. Het verwijderen van gepubliceerde weergaven wordt pas van kracht nadat u op de knop **Opslaan** hebt geklikt.

## <a name="managing-views-globally"></a>Weergaven globaal beheren
Hoewel sommige beheermogelijkheden op elke pagina zichtbaar zijn, zoals in dit onderwerp wordt aangegeven, kunnen weergaven door **systeembeheerders** en **beheerders van opgeslagen weergaven** op een meer holistische wijze voor het systeem worden beheerd via de pagina **Persoonlijke instellingen**. Deze pagina biedt de volgende secties en mogelijkheden: 

- **Gepubliceerde weergaven**: in deze sectie worden alle weergaven vermeld die voor uw organisatie zijn gepubliceerd. Hier kunt u een weergave opnieuw publiceren nadat u de beveiligingsrollen of rechtspersonen in de weergave hebt aangepast. U kunt ook een of meer gepubliceerde weergaven exporteren of verwijderen. In versie 10.0.12 en hoger kunt u de actie **Opslaan als persoonlijk** gebruiken om een persoonlijke kopie van de weergave te maken, zodat u de weergave kunt bijwerken of een beter begrip van de inhoud kunt krijgen. 
- **Niet-gepubliceerde weergaven**: alle weergaven die in uw systeem zijn geïmporteerd, maar nog niet zijn gepubliceerd. U kunt deze weergaven publiceren, exporteren of verwijderen. Met de actie **Snel publiceren** die is toegevoegd in versie 10.0.12, kunnen meerdere weergaven uit deze sectie in één actie worden gepubliceerd met behulp van de bestaande configuratie voor beveiligingsrollen en rechtspersonen. In versie 10.0.12 en hoger kunt u de actie **Opslaan als persoonlijk** gebruiken om een persoonlijke kopie van deze weergaven te maken, zodat u een beter begrip van de inhoud kunt krijgen.   
- **Persoonlijke weergaven**: alle weergaven die zijn gemaakt door gebruikers in het systeem. U kunt hier een persoonlijke weergave voor de organisatie publiceren of een of meer van deze weergaven naar andere gebruikers kopiëren. U kunt deze weergaven ook publiceren, exporteren of verwijderen.
- **Gebruikers**: selecteer een gebruiker om een lijst met de pagina's weer te geven die de gebruiker heeft bezocht. Vervolgens kunt u in- of uitschakelen of de gebruiker voor bepaalde pagina's of voor het hele systeem aanpassingen kan doorvoeren. U kunt ook een aanpassing importeren, exporteren of wissen voor de gebruiker. Daarnaast kunt u de functietoelichtingen voor de gebruiker opnieuw instellen. Als de gebruiker pop-upvensters voor nieuwe functies eerder heeft gesloten, worden deze opnieuw weergegeven wanneer de gebruiker de betreffende functie opnieuw tegenkomt.
- **Systeem**: u kunt tijdelijk aanpassingen voor alle gebruikers in het systeem uitschakelen. In dat geval worden alle aanpassingen voor alle gebruikers verwijderd en worden alle pagina's opnieuw ingesteld op de standaardstatus. Als u aanpassingen later weer wilt inschakelen, worden alle aanpassingen opnieuw toegepast. U kunt alle aanpassingen voor alle gebruikers in het systeem ook permanent verwijderen. Er is geen enkele manier om aanpassingen terug te halen die zijn verwijderd. Voordat u deze taak uitvoert, moet u er daarom voor zorgen dat u aanpassingen hebt geëxporteerd die u later mogelijk wilt.

Gebruikers die toegang hebben tot de pagina **Aanpassing** kunnen ook persoonlijke sjablonen of sjabloonweergaven importeren met de knop **Weergaven importeren** in het actievenster. In versie 10.0.12 en hoger is een mechanisme toegevoegd voor het onmiddellijk publiceren van weergaven wanneer deze worden geïmporteerd.  

## <a name="frequently-asked-questions"></a>Veelgestelde vragen
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Hoe schakel ik opgeslagen weergaven in mijn omgeving in? 
> [!NOTE]
> Voor de functie **Opgeslagen weergaven** moet het personalisatiesysteem in Finance and Operations zijn ingeschakeld. Als persoonlijke instellingen zijn uitgeschakeld voor de gehele omgeving, worden weergaven wel uitgeschakeld, ook als u de onderstaande stappen uitvoert. 

**10.0.9/platform update 33 en hoger** De functie **Opgeslagen weergaven** is in alle omgevingen meteen beschikbaar in Functiebeheer. Net als bij andere previewfuncties is het inschakelen van deze functie in productie afhankelijk van de [aanvullende gebruiksrechtovereenkomst](https://go.microsoft.com/fwlink/?linkid=2105274).  

**10.0.8/platform update 32 en eerder** De functie **Opgeslagen weergaven** kan worden ingeschakeld in omgevingen in laag 1 (Dev/Test) en in laag 2 (Sandbox) om extra tests en ontwerpwijzigingen te kunnen doorvoeren, door de volgende stappen uit te voeren.

1.  **De vlucht inschakelen**: voer de volgende SQL-instructie uit: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2. **IIS opnieuw instellen** om de statische flightingcache leeg te maken. 

3.  **De functie zoeken**: ga naar het werkgebied **Functiebeheer**. Als **Opgeslagen weergaven** niet in de lijst voorkomen, selecteert u **Controleren op updates**.   

4.  **De functie inschakelen**: zoek de functie **Opgeslagen weergaven** in de lijst met functies en selecteer **Nu inschakelen** in het detailvenster.

Alle volgende gebruikerssessies worden gestart met opgeslagen weergaven ingeschakeld.


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

Voor pagina's met grote weergavekiezers (persoonlijke instellingen en query's kunnen in de weergave worden opgeslagen) ziet u primair de gegevens die zijn gekoppeld aan de query die bij uw standaardweergave hoort. Hierop zijn twee belangrijke uitzonderingen: als u van een tegel naar een pagina navigeert, wordt de query uitgevoerd, ongeacht de query die aan de standaardweergave is gekoppeld. Als u deze tegel hebt gemaakt nadat weergaven zijn ingeschakeld, wordt door het selecteren van een tegel de pagina geopend met de weergave die aan die tegel is gekoppeld.   
     - Als u naar een pagina gaat en dat ingangspunt een query bevat, wordt de oorspronkelijke query uitgevoerd in plaats van de query van de standaardweergave. Wanneer dat gebeurt, moet u een waarschuwing krijgen in een informatief bericht wanneer de weergave wordt geladen. U kunt ook bevestigen door naar deze pagina over te schakelen nadat de pagina is geladen,aangezien de weergavequery in dat geval sowieso moet worden uitgevoerd.  


