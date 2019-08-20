---
title: Opgeslagen weergaven
description: In dit onderwerp wordt beschreven hoe u de functies voor opgeslagen weergaven gebruikt.
author: jasongre
manager: AnnBe
ms.date: 08/01/2019
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
ms.openlocfilehash: 9d19987a44c467381828acb81b6161601268d84f
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863055"
---
# <a name="saved-views"></a>Opgeslagen weergaven

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

## <a name="introduction"></a>Introductie
Persoonlijke instellingen spelen een belangrijke rol bij het toestaan van gebruikers en organisaties om de gebruikerservaring in Microsoft Dynamics 365 for Finance and Operations te optimaliseren op basis van hun behoeften. Zie [De gebruikerservaring aanpassen](personalize-user-experience.md) voor meer informatie over aanpassingen.

Bij traditionele personalisatie beschikten gebruikers slechts over één set persoonlijke instellingen per formulier. Opgeslagen weergaven biedt op verschillende belangrijke manieren meer mogelijkheden:

-    Gebruikers beschikken over meerdere benoemde sets persoonlijke instellingen per formulier waartussen ze snel kunnen schakelen, waar nodig. Zo kan een gebruiker meerdere geoptimaliseerde weergaven van een pagina maken, waarbij elke weergave is aangepast aan de behoeften van het uitvoeren van een bepaalde bedrijfstaak. 

-    Weergaven die voor bepaalde pagina typen worden gemaakt, kunnen ook door de gebruiker toegevoegde filters of sorteringen bevatten. Hierdoor kunnen gebruikers snel terugkeren naar vaak gefilterde gegevens sets. Zie het gedeelte [Welke pagina's weergaven ondersteunen](saved-views.md#what-pages-support-views) voor meer informatie. 

-    Weergaven kunnen worden gepubliceerd voor beveiligingsrollen, wat betekent dat elke gebruiker met deze rol toegang heeft tot de weergave en deze kan gebruiken, ongeacht de mogelijkheden voor personalisatie van de gebruiker. Dankzij deze publicatiefunctie kunnen organisaties standaardweergaven voor bedrijven definiëren die voor hun bedrijf zijn geoptimaliseerd. Zie het gedeelte [Persoonlijke instellingen op een organisatieniveau beheren met weergaven](saved-views.md#managing-personalizations-at-an-organizational-level-with-views) voor meer informatie.

-    In tegenstelling tot bij traditionele personalisatie worden weergaven niet automatisch opgeslagen wanneer een gebruiker expliciete aanpassingen uitvoert of een lijst filtert. Expliciete opslag is vereist om flexibiliteit te bieden bij het maken van een weergave voor- of nadat de wijzigingen gekoppeld aan die weergave zijn aangebracht en om ervoor te zorgen dat weergavedefinities niet per ongeluk worden gewijzigd door filters of persoonlijke instellingen die niet zijn bedoeld voor langetermijngebruik.  

## <a name="switching-between-views"></a>Schakelen tussen weergaven
Als weergaven zijn ingeschakeld voor een omgeving, bevat elke pagina die weergaven ondersteunt een selectieoptie voor een samengevouwen weergave boven aan het formulier waarin de naam van de huidige weergave wordt weergegeven.  

Er zijn twee groottes voor deze weergavekiezer: 

-   **Grote weergavekiezers**: pagina's met een aanzienlijke lijst krijgen om enkele redenen een grotere weergavekiezer. In de grotere weergavekiezer worden de pagina's aangegeven waar de weergave door de gebruiker gedefinieerde filters kan bevatten. Aangezien filters in de weergaven zijn opgenomen, is het grotere kiezerformaat ook gerechtvaardigd omdat de weergavenamen vaak de beste beschrijving zijn van de gegevens die op het scherm worden weergegeven en de verwachting is dat gebruikers vaker tussen weergaven schakelen op deze typen pagina's.  
 
-   **Kleine weergavekiezers**: alle andere formulieren van volledige paginagrootte (met uitzondering van werkruimten en het dashboard) hebben een kleinere weergavekiezer die naast het paginabijschrift wordt weergegeven. Weergaven op deze pagina's omvatten alleen persoonlijke instellingen (en geen door de gebruiker gedefinieerde filters). Op deze pagina's is het formulierbijschrift of de recordtitel vaak de belangrijkste informatie boven aan het formulier. De kleinere grootte weerspiegelt ook een lagere verwachte frequentie aan schakelingen tussen weergaven op deze pagina's. 
 
Als u op de naam van de weergave klikt, wordt de weergavekiezer geopend en wordt de lijst met beschikbare weergaven voor deze pagina weergegeven.

-    **Klassieke weergave**: de klassieke weergave is de standaardweergave van de pagina waarop geen expliciete persoonlijke instellingen zijn toegepast.  
-    **Persoonlijke weergaven**: de weergaven zonder hangsloten vertegenwoordigen uw persoonlijke weergaven. Dit zijn weergaven die u hebt gemaakt of die een beheerder aan u heeft gegeven.  
-    **Vergrendelde weergaven**: voor sommige weergaven (zoals de klassieke weergave en alle weergaven die naar uw rol zijn gepubliceerd) wordt een hangslot weergegeven in de weergavekiezer om aan te geven dat u deze weergaven niet kunt bewerken. Impliciete aanpassingen met betrekking tot paginagebruik worden echter automatisch opgeslagen, bijvoorbeeld wanneer de breedte van een rasterkolom wordt gewijzigd of een sneltabblad wordt uit- of samengevouwen. U kunt echter wel een persoonlijke weergave op basis van een vergrendelde weergave maken met de actie **Kopie opslaan**, als u over aanpassingsbevoegdheden beschikt.
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
     1.    Selecteer **Kopie opslaan**. 
     2.    Voer een naam en desgewenst een omschrijving in.
     3.    Selecteer **Opslaan**.

## <a name="changing-the-default-view"></a>De standaardweergave wijzigen
De standaardweergave is de weergave die het systeem probeert te openen wanneer u voor het eerst naar de pagina gaat. U moet deze instellen op de weergave die u het vaakst verwacht te gebruiken.  

Volg deze stappen om de standaardweergave voor een pagina te wijzigen: 
1.  Schakel over naar de weergave die u als standaardweergave gebruikt. 
2.  Selecteer de weergavenaam om de weergavekiezer te openen. 
3.  Selecteer **Meer** en **Vastmaken als standaard**.  

Als u een nieuwe weergave maakt (met de actie **Kopie opslaan**), kunt u hiervan de standaardweergave maken door de optie **Vastmaken als standaard** in te stellen voordat u de weergave opslaat.  

In sommige gevallen wordt de query die is gekoppeld aan de standaardweergave niet uitgevoerd wanneer u voor het eerst naar een pagina gaat. Als u bijvoorbeeld door een tegel naar een pagina navigeert, wordt de query van de tegel uitgevoerd, ongeacht de query die aan de standaardweergave is gekoppeld. Als u naar een pagina gaat waarvoor al een gedefinieerde query bestaat voor de klassieke weergave, wordt de oorspronkelijke query uitgevoerd in plaats van de query van de standaardweergave. In dat geval wordt u gewaarschuwd door een informatief bericht wanneer de weergave wordt geladen. Als u naar een andere weergave schakelt nadat de pagina is geladen, wordt de weergavequery weer zoals verwacht uitgevoerd.

## <a name="managing-personal-views"></a>Persoonlijke weergaven beheren 
In het dialoogvenster **Mijn weergaven beheren** beschikt u over basisfuncties voor het onderhoud van uw persoonlijke weergaven en de volgorde van weergaven in de weergavekiezer. Als u deze pagina wilt openen, klikt u op de naam van de weergave om de vervolgkeuzelijst van de weergavekiezer te openen en selecteert u **Meer** en **Mijn weergaven beheren**.  

De volgende set acties is beschikbaar voor een lijst met beschikbare weergaven voor die pagina.  
-    **Standaardweergave wijzigen**: gebruik de actie **Vastmaken als standaard** om de momenteel gemarkeerde weergave in te stellen als standaardweergave voor deze pagina.  
-    **Volgorde van weergaven wijzigen**: gebruik de acties **Omhoog** en **Omlaag** om de weergaven in een bepaalde volgorde te rangschikken.  
-    **Naam van weergave wijzigen**: gebruik de actie **Naam wijzigen** om de naam van de gemarkeerde persoonlijke weergave te wijzigen. Deze actie is uitgeschakeld voor vergrendelde weergaven. 
-    **Weergave verwijderen**: gebruik de actie **Verwijderen** om de momenteel gemarkeerde weergave permanent van de pagina te verwijderen. Na verwijdering kunt u een weergave niet meer herstellen.  

Eventuele wijzigingen in dit dialoogvenster worden pas van kracht als u de knop **Opslaan** selecteert.

## <a name="managing-personalizations-at-an-organizational-level-with-views"></a>Persoonlijke instellingen op een organisationeel niveau beheren met weergaven
Voor een beter begrip van de verbeteringen bij het beheer van persoonlijke instellingen op een organisationeel niveau moet u eerst kijken hoe dit werkte voordat we met weergaven werkten.  

Zonder weergaven pasten beheerders een set persoonlijke instellingen voor een pagina toe op een gebruiker of een groep gebruikers via de pagina Persoonlijke instellingen. Als deze gebruikers over rechten voor persoonlijke instellingen beschikten, werden de persoonlijke instellingen toegepast op die pagina. Het was echter niet mogelijk om te voorkomen dat gebruikers de pagina verder zouden aanpassen. wat betekende dat de organisatie niet kon garanderen dat de gebruikers over een consistente gebruikersinterface beschikten. Als een van deze gebruikers niet over rechten voor persoonlijke instellingen beschikte, werden de toegewezen persoonlijke instellingen door een beheerder niet geladen. En als nieuwe gebruikers in een organisatie werden aangesteld, moesten beheerders handmatig een verzameling persoonlijke instellingen voor die gebruiker laden. Er was geen automatisch mechanisme om op te geven dat een bepaalde set persoonlijke instellingen beschikbaar moesten zijn voor gebruikers met die rol.

Met de functie voor opgeslagen weergaven is het beheer van persoonlijke instellingen voor de organisatie aanzienlijk eenvoudiger, voornamelijk door de mogelijkheid om weergaven te publiceren naar beveiligingsrollen. Nadat een weergave is gepubliceerd, heeft elke gebruiker met deze rol toegang tot de weergave, ongeacht de mogelijkheden voor personalisatie van de gebruiker. Terwijl elke gebruiker een kopie heeft van de gepubliceerde weergave waarin het paginagebruik (impliciete persoonlijke instellingen) automatisch wordt toegepast, kan geen enkele gebruiker expliciete persoonlijke instellingen of queryupdates opslaan in de gepubliceerde weergave (wat betekent dat gepubliceerde weergaven zijn vergrendeld). Als nieuwe gebruikers een rol krijgen waarnaar de weergave is gepubliceerd, krijgen ze automatisch de weergaven te zien die aan hun rollen zijn gekoppeld. Hiervoor hoeft de beheerder niets te doen. En als een gebruiker een andere rol krijgt in een organisatie, zijn de weergaven gekoppeld aan de oude rol ook niet langer toegankelijk voor deze gebruiker, zonder enige actie van de beheerder. Updates voor een gepubliceerde weergave kunnen eenvoudig naar gebruikers worden gedistribueerd door de weergave opnieuw naar de betreffende beveiligingsrollen te publiceren.

Dankzij de publicatiefunctie kunnen organisaties standaardweergaven voor bedrijven definiëren die voor hun bedrijf zijn geoptimaliseerd, gericht op gebruikers in bepaalde beveiligingsrollen.  

## <a name="publishing-views"></a>Weergaven publiceren
Tijdens het publicatieproces kunnen weergaven worden toegewezen aan een of meer beveiligingsrollen, wat betekent dat elke gebruiker met die rol toegang heeft tot de weergave en deze kan gebruiken, hoewel ze de weergave niet kunnen bewerken. Op dit moment hebben alleen systeembeheerders rechten voor de actie **Publiceren** in het vervolgkeuzemenu Weergavekiezer, maar een nieuwe beveiligingsrol zal in een toekomstige update beschikbaar zijn om publicatierechten te geven aan andere vertrouwde gebruikers.  

Voer deze stappen uit om een weergave te publiceren: 
1.  Maak een persoonlijke kopie van de weergave die u wilt publiceren en sla deze op. 
2.  Selecteer terwijl die weergave is geladen de naam van de weergave om het vervolgkeuzemenu voor de weergavekiezer te openen. 
3.  Selecteer de knop **Meer** en selecteer vervolgens **Publiceren**. Het dialoogvenster Publiceren wordt geopend.  
4.  Voer een naam en desgewenst een omschrijving voor de weergave in. Dit is de naam die de gebruikers die deze weergave ontvangen, te zien krijgen in hun weergavekiezers. Dubbele namen voor gepubliceerde weergaven zijn niet toegestaan voor een pagina, ook niet als ze op verschillende lijsten met rollen worden toegepast.  
5.  Voeg de beveiligingsrollen toe die overeenkomen met de gebruikers die deze weergave ontvangen.  
6.  Selecteer **Publiceren**.

In sommige omgevingen kan het enige tijd duren (maximaal een uur) voordat gebruikers de gepubliceerde weergave kunnen zien.

## <a name="modifying-a-published-view"></a>Een gepubliceerde weergave wijzigen
Na publicatie van een weergave kunt u er achter komen dat u nog wijzigingen in een gepubliceerde weergave wilt aanbrengen. Hoewel u geen live wijzigingen kunt aanbrengen in een gepubliceerde weergave, omdat deze weergaven zijn vergrendeld voor bewerking voor alle gebruikers (inclusief uitgevers), kunt u een weergave wel opnieuw publiceren voor updates.  

Als de wijzigingen die u wilt aanbrengen in een gepubliceerde weergave alleen betrekking hebben op de publicatieparameters (de naam en omschrijving van de weergave of de beveiligingsrollen waarnaar de weergave wordt gepubliceerd), gaat u als volgt te werk: 
1.  Schakel over naar de gepubliceerde weergave voor de parameters die u wilt bijwerken. 
2.  Selecteer **Publiceren** in het vervolgkeuzemenu voor de weergavekiezer. 
3.  Selecteer **Ja** als u de bestaande weergave wilt bijwerken (of **Nee** als u deze wilt publiceren onder een andere naam).
4.  Werk de naam, omschrijving en/of beveiligingsrollen voor de weergave bij. 
5.  Selecteer **Publiceren**. 
6.  Als u de naam van de gepubliceerde weergave hebt bijgewerkt, moet u ook de gepubliceerde weergave met de oude naam verwijderen (zie **Gepubliceerde weergaven beheren** voor meer informatie). 

Als de wijzigingen in de gepubliceerde weergave betrekking hebben op de persoonlijke instellingen of filters gekoppeld aan de weergave, gaat u als volgt te werk: 
1.  Schakel over naar de gepubliceerde weergave die u wilt wijzigen. 
2.  Sla een kopie van de gepubliceerde weergave op om een lokaal concept van de gepubliceerde weergave te maken. 
3.  Wijzig het lokale concept met de benodigde wijzigingen.
4.  Publiceer de weergave onder de oorspronkelijke naam. 

## <a name="managing-published-views"></a>Gepubliceerde weergaven beheren
Net als bij het beheren van persoonlijke weergaven biedt het dialoogvenster **Mijn weergaven beheren** gebruikers met publicatiebevoegdheden de basisbeheerfuncties voor de gepubliceerde weergaven van die pagina (naast hun eigen persoonlijke weergaven). Als u deze pagina wilt openen, selecteert u de naam van de weergave om de vervolgkeuzelijst van de weergavekiezer te openen en selecteert u **Meer** en **Mijn weergaven beheren**.

Hoewel alle gebruikers het tabblad **Mijn weergaven** met hun persoonlijke weergaven te zien krijgen, zien gebruikers met publicatiebevoegdheden ook het tabblad **Gepubliceerd** waarop alle gepubliceerde weergaven voor die pagina worden weergegeven. Omdat er verschillende gebruikers kunnen zijn die weergaven publiceren, is het belangrijk dat u de volledige lijst met gepubliceerde weergaven beheert, ongeacht of u de gebruiker bent die de weergave daadwerkelijk heeft gepubliceerd.

De volgende set acties is beschikbaar voor de lijst met alle gepubliceerde weergaven voor de pagina. 

-    **Publiceren**: gebruik de actie **Publiceren** om een weergave met gewijzigde publicatieparameters (naam, omschrijving, beveiligingsrollen) opnieuw te publiceren.  
-    **Verwijderen**: gebruik de actie **Verwijderen** om een gepubliceerde weergave definitief te verwijderen. Met deze actie verwijdert u de weergave voor alle gebruikers in het systeem.  
 
Eventuele wijzigingen in dit dialoogvenster worden pas van kracht als u de knop **Opslaan** selecteert.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen
### <a name="how-do-i-enable-saved-views-in-my-environment"></a>Hoe schakel ik opgeslagen weergaven in mijn omgeving in? 
Volg de onderstaande stappen om opgeslagen weergaven in te schakelen terwijl de functie in preview is: 

1.  **De vlucht inschakelen**: voer de volgende SQL-instructie uit: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('Dynamics.AX.Application.CLISavedViewsEnableFeature', 1, 0, 5637144576);`

2.  **De functie zoeken**: navigeer naar de werkruimte **Functiebeheer**. Als **Opgeslagen weergaven** niet in de lijst voorkomen, selecteert u de knop **Controleren op updates**.   

3.  **De functie inschakelen**: zoek de functie **Opgeslagen weergaven** in de lijst met functies en klik op de knop **Nu inschakelen** in het detailvenster.

Alle volgende gebruikerssessies worden gestart met opgeslagen weergaven ingeschakeld.  

Als persoonlijke instellingen zijn uitgeschakeld voor de omgeving, worden weergaven wel uitgeschakeld, ook als u de bovenstaande stappen uitvoert. De functie voor weergaven is namelijk gebouwd boven op het subsysteem voor persoonlijke instellingen.

### <a name="what-happens-to-existing-personalizations-when-views-are-enabled"></a>Wat gebeurt er met bestaande persoonlijke instellingen wanneer weergaven worden ingeschakeld? 
Wanneer weergaven worden ingeschakeld, worden bestaande persoonlijke instellingen voor een gebruiker en formulier opgeslagen in een nieuwe weergave met de naam **Mijn weergave** die automatisch wordt ingesteld als de standaardweergave. Dit is bedoeld om ervoor te zorgen dat er een consistente gebruikerservaring bestaat voor- en nadat weergaven worden ingeschakeld, behalve dat de weergavekiezer wordt weergegeven in formulieren.  

### <a name="what-pages-support-views"></a>Welke pagina's ondersteunen weergaven? 
Weergaven zijn beschikbaar op de meeste, maar niet alle pagina's in Finance and Operations. Weergaven zijn momenteel beschikbaar op alle pagina's in het volledige scherm, met uitzondering van dashboards en werkgebieden. Andere pagina's, zoals dialoogvensters, vervolgkeuzemenu's, zoekopdrachten en verbeterde voorbeelden ondersteunen momenteel ook geen weergaven. Mogelijk bieden andere paginatypen, zoals werkgebieden en dialoogvensters, wel ondersteuning voor weergaven in toekomstige updates.   

### <a name="who-is-allowed-to-publish-views"></a>Wie mag weergaven publiceren?
Momenteel zijn systeembeheerders de enige gebruikers die weergaven mogen publiceren.  In een toekomstige update is een nieuwe beveiligingsrol gepland om klanten meer flexibiliteit te bieden met betrekking tot wie mogen publiceren.  

### <a name="why-am-i-not-able-to-save-filters-with-this-view"></a>Waarom kan ik filters niet opslaan met deze weergave? 
Er zijn een aantal redenen waarom een filter mogelijk niet wordt opgeslagen met een weergave: 

- Het opslaan van filters wordt mogelijk niet door de pagina ondersteund als onderdeel van de weergavedefinitie. Alleen voor pagina's met grote weergavekiezers kunnen persoonlijke instellingen en querywijzigingen worden opgeslagen als weergave. Zie Schakelen tussen weergaven voor meer informatie. 

- Als de weergave de standaardweergave is en het navigatiepad naar de pagina een query bevat, wordt de query van de weergave mogelijk eerst niet toegepast. De twee belangrijkste scenario's hiervoor zijn: 
     - Als u van een tegel naar een pagina navigeert, wordt de query uitgevoerd, ongeacht de query die aan de standaardweergave is gekoppeld. 
     - Als u naar een pagina gaat en dat invoerpunt query bevat, wordt de oorspronkelijke query uitgevoerd in plaats van de query van de standaardweergave. 
     
  In dat geval moet u worden gewaarschuwd door een informatief bericht wanneer de weergave wordt geladen. U kunt ook bevestigen door naar deze pagina over te schakelen nadat de pagina is geladen,aangezien de weergavequery in dat geval sowieso moet worden uitgevoerd.  

- De desbetreffende pagina kan weergaven mogelijk niet goed ondersteunen, omdat deze de weergavequery volledig kan negeren of kan werken op een tijdelijke tabel waarvan de gegevens niet persistent zijn. 
