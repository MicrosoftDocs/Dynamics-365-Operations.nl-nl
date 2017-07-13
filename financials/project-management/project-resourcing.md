---
title: Resources plannen voor projecten
description: In dit onderwerp vindt u informatie over het plannen van resources voor projecten.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a7275e9ad8d655d0d2ee5ba90a792775dec0cf05
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017


---

# <a name="project-resourcing"></a>Resources plannen voor projecten

[!include[banner](../includes/banner.md)]


In dit onderwerp vindt u informatie over het plannen van resources voor projecten.

Een van de uitdagingen voor projectmanagers en resourcemanagers tijdens de projectplanningsfase is resourcetoewijzing, waarin ze de juiste resources moetn definiëren en reserveren voor werk aan een project. In Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, kunt u met de capaciteiten voor projectresourcing rollen definiëren die worden behandeld als tijdelijke resources. Die kunt u reserveren voor een specifieke taak, ofwel een gedeelte van een taak. Met dit type resourcing kunnen projectmanagers en resourcemanagers de volgende taken uitvoeren:

-   Een rol definiëren met de vereiste competenties om het afstemmen van resources te vergemakkelijken.
-   Met behulp van rollen een initiële taakplanning definiëren op basis van resourcereserveringen.
-   Kosten ramen en een initieel budget opstellen, op basis van rollen en resources die aan een project zijn toegewezen.
-   Met behulp van rollen het aantal resourcereserveringen ramen die voor elke taak zijn vereist.
-   Het aantal resources ramen dat voor de volledige levenscyclus van een project is vereist.
-   Een structuur voor werkanalyse (WBS) opstellen via de initiële resourcetoewijzingen.

[![Projectlevenscyclus](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Wanneer de projectplanning vordert, kunnen geplande resources worden vervangen door bemande resources. De projectmanager kan ook teruggaan naar het begin en de resourcereserveringen bijwerken in elke projectfase.

## <a name="set-up-project-resources"></a>Projectresources instellen
U moet een kalender configureren en deze aan een werknemer of een medewerker (uitvoerende) koppelen. De kalender wordt gebruikt om het project en de werktijd van de resources te plannen, die voor het project zijn gereserveerd. Tijdens het configureren van de kalender kunnen projectmanagers resources herverdelen in het kader van optimalisatie van de resources. Op basis van het kalenderplan kunnen beperkingen aan resources worden opgelegd. U kunt een kalender instellen op de pagina **Kalenders**. 

Wanneer u een medewerker als een projectresource instelt, u kunt kiezen uit de medewerkers die werken in het bedrijf waarvoor u resources instelt of u kunt medewerkers selecteren van andere bedrijven binnen uw organisatie. Dit zijn intercompany-resources. In de volgende procedures wordt beschreven hoe u een medewerker configureert als een projectresource binnen uw bedrijf en hoe u een intercompany-projectresource configureert.

### <a name="set-up-a-worker-as-a-project-resource"></a>Een medewerker instellen als een projectresource

1.  Selecteer op de pagina **Medewerkers** in de lijst **Medewerkers** de medewerker die u als projectresource toevoegt en open de record van de medewerker.
2.  Klik in het Actievenster op **Project** &gt; **Instellen** &gt; **Projectinstellingen**.
3.  Selecteer een kalender en sluit vervolgens de pagina.

U kunt ook standaardprojecten voor een resource opgeven als een type toewijzing vooraf. Voorafgaande toewijzingen kunnen worden gebruikt wanneer de resource- of projectmanager van tevoren al weet aan welke projecten de resource zal gaan werken. Voorafgaande toewijzingen kunnen plaatsvinden op basis van aanvragen van een projectsponsor of klant. Als u voorafgaande toewijzingen wilt uitvoeren voor een project, selecteert u het gewenste project op de pagina **Projecten toewijzen** op het tabblad **Projecten** in de lijst **Resterende projecten**.

### <a name="set-up-an-intercompany-resource"></a>Een intercompany-resource instellen

Wanneer u een medewerker als een intercompany-resource instelt, moet u de instellingen uitvoeren in het bedrijf dat de medewerker uitleent en in het bedrijf dat de medewerker leent. 

**In het uitlenende bedrijf:**

1.  Controleer in Finance and Operations of het uitlenende bedrijf is geselecteerd en voer de voorgaande procedure, 'Een medewerker instellen als een projectresource', uit.
2.  Ga naar ** Grootboek **&gt; ** Boekingsinstellingen **&gt; **Intercompany-boekhouding**. Klik op **Nieuw**.
3.  Selecteer in het veld **Rechtspersoon-ID **het uitlenende bedrijf. Vul de resterende velden in met de vereiste waarden en klik vervolgens op **Opslaan**.
4.  Ga naar **Projectbeheer en boekhouding **&gt; **Instellingen **&gt; **Prijzen ** &gt; **Prijs overboeken****. **
5.  Klik in het formulier **Prijs overboeken ** op **Nieuw** en selecteer in de ** Lenende rechtspersoon **het gewenste bedrijf.
6.  Als aan het lenende bedrijf alleen de resource wilt uitlenen die u hebt gemaakt aan het begin van deze sectie, selecteert u in het veld **Resource** de naam van de resource die u hebt gemaakt. Als u alle resources in het bedrijf beschikbaar wilt stellen voor het lenende bedrijf, laat u het veld **Resource **leeg.
7.  Ga naar **Projectbeheer en boekhouding **&gt; **Instellingen **&gt; **Projectbeheer- en boekhoudingsparameters** en stel op het tabblad **Intercompany ** tabblad het veld **Intercompany-resourceplanning en urenstaten inschakelen ** in op **Ja**.

**In het lenende bedrijf:**

1.  Ga naar **Projectbeheer en boekhouding** &gt; **Projectresources** &gt; **Resourcelijst**.
2.  Voer in het zoekfilter de naam in van de resource die u hebt gemaakt in de vorige procedure voor het uitlenende bedrijf, om te controleren of de naam voorkomt in de lijst met resources voor het lenende bedrijf.

## <a name="manage-resource-competencies"></a>Resourcecompetenties beheren
Resourcecompetenties zijn een cruciaal onderdeel van resourcebeheer. De competenties kunnen als basislijn worden gebruikt om resources aan te wijzen met de juiste mix van vaardigheden, opleiding, certificering en projectervaring. U moet deze informatie configureren voor elke resource en deze gegevens periodiek bijwerken. Op deze manier kunt u mogelijkheden maximaliseren wanneer specifieke resourcecompetenties tijdens projectresourcetoewijzing worden afgestemd. [![Voorbeelden van vaardigheden, certificaten, opleiding en projectervaring](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

De volgende procedures leggen uit hoe u competenties voor een resource kunt instellen. 

Configuratie van competenties voor een medewerker kunt u doen op de lijstpagina **Medewerkers** in Human resources of op de lijstpagina **Resources** in Projectbeheer en boekhouding. In de volgende procedures wordt gebruik gemaakt van de lijstpagina **Medewerkers** in Human Resources.

### <a name="set-up-competencies-certificates"></a>Competenties configureren: getuigschriften

1.  Selecteer op de lijstpagina **Medewerkers** de regel van de medewerker waarvoor u getuigschriftgegevens wilt toevoegen.
2.  Klik in het actievenster op het tabblad **Medewerker** in de groep **Competenties** op **Getuigschriften**.
3.  Klik op **Nieuw**.
4.  Selecteer in het veld **Type getuigschrift** de waarde **PMP**.
5.  Selecteer in het veld **Begindatum** de waarde **1-10-2015**.
6.  Klik op **Opslaan** en sluit de pagina.

### <a name="set-up-competencies-skills"></a>Vaardigheden instellen: vaardigheden

1.  Controleer of op de lijstpagina **Medewerkers** dat de werknemer die u in de vorige procedure hebt gebruikt nog steeds is geselecteerd. Klik in het actievenster op het tabblad **Medewerker** in de groep **Competenties** op **Vaardigheden**.
2.  Klik op **Nieuw**.
3.  Selecteer in het veld **Vaardigheid** de waarde **Projectbeheer**.
4.  Selecteer in het veld **Niveau** de waarde **5 Expert**.
5.  Selecteer in het veld **Niveaudatum** de waarde **14-1-2014**.
6.  Voer in het veld **Jaren ervaring** de waarde **10** in.
7.  Klik op **Opslaan** en sluit de pagina.

## <a name="create-a-new-project"></a>Een nieuw project maken
1.  Klik op **Projectbeheer en boekhouding** &gt; **Werkgebieden** &gt; **Projectbeheer**.
2.  Klik op **Nieuw project** en voer de volgende gegevens in:
    -   **Projecttype:** Tijd en materiaal
    -   **Projectnaam:** Xyz-upgrade fase 2
    -   **Projectgroep:** TM\_WIP
    -   **Projectcontract-id:** 00000002
3.  Klik op **Project maken**.

### <a name="assign-a-resource-to-a-project"></a>Een resource toewijzen aan een project

1.  Klik op **Human resources** &gt; **Medewerkers** &gt; **Medewerkers**.
2.  Selecteer in de lijst **Medewerkers** de record van de medewerker waarvoor u eerder competenties hebt geconfigureerd en openen de medewerkerrecord.
3.  Klik in het actievenster op het tabblad **Project** in de groep **Instellingen** op **Projecten toewijzen**.
4.  Klik op de pagina **Projecttoewijzingen voor resourcevalidatie** op het tabblad **Projecten**.
5.  Ga naar **Het project toevoegen aan geselecteerde projecten** en filter op het project Xyz-upgrade fase 2.
6.  Selecteer een project in het deelvenster **Resterende projecten** en klik op de pijl om dit toe te voegen aan het deelvenster **Geselecteerde projecten**.
7.  Sluit de pagina.

Indien nodig kunt u ook categorieën voor een resource toewijzen. Het categorietype is ofwel Kosten of Opbrengst. Dit wordt bepaald door uw organisatie. Als geen categorieën aan de resource zijn toegewezen, zal Finance and Operations de standaardcategorie opzoeken voor uurtarieven voor kosten en opbrengsten.

### <a name="set-up-project-resource-and-role-characteristics"></a>Kenmerken voor projectresource en rollen configureren

Een projectmanager kan de resourcingfunctionaliteit van het project gebruiken om de rollen te maken die het project vereist. Rollen kunnen worden gebruikt wanneer tijdens het reserveren van resources nog geen bevestigde resources bekend zijn. Met rollen kunt u resources tijdelijk reserveren als gepland, zodat u de projectplanningsfasen kunt voortzetten. 

[![Voorbeeld van een rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso is aangezocht om een project van het type Tijd en materiaal uit te voeren, dat een goedgekeurd projectcharter heeft. De juniorprojectmanager is nog bezig de reikwijdte van het project te bepalen. De resourcemanager identificeert momenteel specifieke resources die worden gereserveerd om aan het nieuwe project te werken. Een van de rollen waarom de projectsponsor vanwege de kritieke aard van het project heeft verzocht, is die van senior projectmanager. De resourcemanager moet de nieuwe resource verkrijgen en de rol in het systeem definiëren, voor het geval de junior projectmanager de resourcegegevens tijdens de projectplanning nodig heeft. 

De volgende stappen geven weer hoe de resourcemanager rol Senior projectmanager kan configureren en er resourcekenmerken aan kan toewijzen. Later kan de worden gebruikt om te zoeken naar beschikbare resources die voldoen aan de vereiste resourcecompetenties.

1.  Klik op **Projectbeheer en boekhouding** &gt; **Instellen** &gt; **Resources** &gt; **Rollen instellen**.
2.  Klik op **Nieuw** en voer de volgende gegevens in:
    -   **Rol-ID:** Senior projectmanager
    -   **Beschrijving:** Senior projectmanager
3.  Klik op **Maken**.
4.  Selecteer de rol **Senior projectmanager** en klik op **Kenmerken configureren**.
5.  Selecteer in het veld **Type kenmerk** de waarde **Vaardigheid**.
6.  Voer in het veld **Beschikbare kenmerken** de vaardigheid in waarnaar u zoekt.
7.  Selecteer in het veld **Type kenmerk** de waarde **Getuigschrift**.
8.  Voer in het veld **Beschikbare kenmerken** het type getuigschrift in waarnaar u zoekt.
9.  Klik op **OK** en sluit de pagina.

### <a name="assign-a-project-resource-to-a-project"></a>Een projectresource toewijzen aan een project

1.  Klik op **Projectbeheer en boekhouding** &gt; **Algemeen** &gt; **Projecten** &gt; **Alle projecten** en open het project **Xyz-upgrade fase 2**.
2.  Klik op het tabblad **Projectteam en planning** op **Toevoegen**.
3.  Selecteer in het veld **Rol** de waarde **Teamlid**.
4.  Klik op **Boeken vanuit kalender**.
5.  Klik op de pagina **Resourcebeschikbaarheid** op **Weergave-instellingen**.
6.  Voer op de pagina **Weergave-instellingen aanpassen** de volgende waarden in:
    -   **Indeling voor weergave datumbereik:** Dag
    -   **Beschikbaarheidsomschrijvingen weergeven:** Ja
    -   **Resterende capaciteit weergeven:** Ja
7.  Selecteer in de lijst van resources een resource.
8.  Klik op **Vast boeken** &gt; **Volledige capaciteit**.
9.  Sluit de pagina.

### <a name="assign-a-resource-to-a-default-role"></a>Een resource aan een standaardrol toewijzen

Om project- of resourcemanagers te helpen, kunt u verder inzoomen op de resources die voor een project kunnen worden gereserveerd. U kunt een standaardrol aan een bestaande resource toewijzen of aan nieuw verworven resource. Toen bijvoorbeeld Daniel werd aangenomen, had hij de ervaring en vaardigheden voor de rol Bedrijfsanalist. De resourcemanager heeft deze rol toegewezen als Daniel's standaardrol. Daartoe heeft de resourcemanager Daniel toegevoegd aan een groep bedrijfsanalisten die beschikbaar zijn voor het werken aan projecten. 

Tijdens resourcereservering kunnen de projectmanagers de rolresources filteren die beschikbaar zijn om aan projecten te werken. Ze kunnen deze informatie als een criterium gebruiken wanneer ze de beslissingsanalyse met meerdere criteria uitvoeren tijdens het vervullen van resources. Ze kunnen ook andere resourcekenmerken aan het filter toevoegen, om te zoeken naar resources die bepaalde vaardigheden, opleiding, en ervaring hebben voor een bepaald project. 

**Scenario:** Een goedgekeurd project is van start gegaan en de rol Senior projectmanager is gereserveerd als geplande resource tijdens de projectplanningsfase. De resourcemanager heeft nu een resource verworven om de rol van Senior projectmanager te vervullen.

1.  Klik op **Projectbeheer en boekhouding** &gt; **Projectresources** &gt; **Resourcelijst**.
2.  Selecteer in de lijst **Resource** de waarde **Daniel Goldschmidt**.
3.  Klik op **Projectresources** &gt; **Onderhouden** &gt; **Resourcerollen**.
4.  Klik op **Nieuw** en voer de volgende gegevens in:
    -   **Ingangsdatum:** (de huidige datum)
    -   **Vervaldatum:** Nooit
    -   **Rol-ID:** Senior projectmanager
5.  Klik op **Opslaan** en sluit de pagina.
6.  Voeg op het tabblad **Competenties** de vaardigheid **Projectbeheer** en het getuigschrift **PMP** toe.

## <a name="set-up-role-based-pricing"></a>Rol-gebaseerde prijzen configreren
Alle prijzen voor kosten, verkoop, en overdracht kunnen voor rollen worden geconfigureerd.

1.  Klik op **Projectbeheer en boekhouding** &gt; **Instellen** &gt; **Prijzen** &gt; **Verkoopprijs (uur)**.
2.  Klik op **Nieuw**.
3.  Voer een ingangsdatum in.
4.  Selecteer een rol in de kolom **Rol**.
5.  Voer in de kolom **Prijscalculatie** een prijs in voor de geselecteerde resourcerol.

## <a name="form-a-project-team"></a>Een projectteam vormen
Om de rollen te gebruiken die eerder in een project zijn geconfigureerd, moet een projectmanager de rollen aan het project koppelen. Meerdere rollen kunnen aan een project worden toegewezen, en Finance and Operations geeft deze rollen automatisch een label tijdens het reserveren om verwarring te voorkomen. Als bijvoorbeeld de projectmanager drie software-engineer nodig heeft, worden automatisch drie software-engineerrollen gegenereerd met de labels Software-engineer 1, Software-engineer 2 en Software-engineer 3. Als voor de rol eerder rolkenmerken zijn ingesteld, worden deze toegepast als filter in zoekopdrachten naar een resource. Aanvullende kenmerken kunnen indien nodig worden toegevoegd om het zoeken te verfijnen. 

Weergave-instellingen kunnen ook worden aangepast voor een betere weergave van de beschikbaarheid van resources. Er zijn opties voor weergave van beschikbaarheid per uur, dag, week, maand, kwartaal en jaar. Er is ook een optie om beschikbaar en resterende capaciteit van resources weer te geven. Deze optie is handig voor tijdbeheer, wanneer u beschikbare tijd voor activiteiten of resourcebeschikbaarheid raamt. 

De projectmanager kan een rol op de pagina selecteren en vervolgens, als er een beschikbare resource is die aan de vereisten voldoet, daarvoor een resource reserveren die de rol vervult. Merk op dat de resources niet op dit moment in de planningsfase hoeven te worden gereserveerd. Wanneer u een WBS maakt, kunt u rollen vervangen door bemande resources voor het project. Als rollen worden vervangen door bemande rollen in de WBS, werkt de resourceconfiguratie automatisch de projectteamlijst en de planning bij. 

[![Projectteamlijst die zowel rollen als werkelijke resources bevat](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

De projectmanager heeft verschillende opties om een resource op een project te boeken, zoals **Resterende capaciteit**, **Volledige capaciteit**, **Percentage van capaciteit** en **Uren opgeven**. Deze boekingsopties kunnen op elk moment worden geannuleerd als de resourcetoewijzingen wijzigen. Twee typen boeking worden ondersteund:

-   **Vast boeken**: De resourcereservering is goedgekeurd en is bevestigd om aan de taak te werken voor de opgegeven periode.
-   **Variabel boeken**: De resourcereservering is voorlopig ingesteld om aan de taak te werken voor de opgegeven periode.

De onderstaande procedure licht toe hoe u een projectteam maakt.

### <a name="create-a-project-team"></a>Een projectteam maken

1.  Selecteer een project op de lijstpagina **Alle projecten** en klik op **Bewerken**.
2.  Voer op het tabblad **Projectteam en planning** in het veld **Planning einddatum** de begindatum van het schema plus één maand in. Als bijvoorbeeld de planningbegindatum 24 juni 2017 is (24-06-2017), voert u **24-07-2017** in.
3.  Klik op **Toevoegen**.
4.  Selecteer in het venster **Rollen toevoegen aan het project** in het veld **Rol** de waarde **Senior projectmanager**.
5.  Klik op **Vereiste competenties**.
6.  Op de pagina **Kenmerken kiezen** zijn de kenmerken die u eerder hebt ingesteld voor de rol Senior projectmanager automatisch geselecteerd. Klik tot slot op **OK**.
7.  Voer op de pagina **Rollen toevoegen aan project** in het veld **Aantal resources** de waarde **1** in.
8.  In het veld **Resource** geeft de zoekopdracht alle resources weer die de vereiste competenties hebben. Selecteer **Daniel Goldschmidt** en klik op **Maken**.
9.  Klik op de pagina **Project** op **Toevoegen**.
10. Selecteer in het venster **Rollen toevoegen aan het project** in het veld **Rol** de waarde **Teamlid**. Voer in het veld **Aantal resources** de waarde **5** in.
11. Klik op **Maken**.
12. Klik op de pagina **Projecten** op **Voorzien in resource**.

## <a name="resource-capacity-synchronization"></a>Capaciteitsynchronisatie voor resource
De processen voor resourcesynchronisatie helpen ervoor te zorgen dat de informatie van kalender en basiskalender doorvloeien naar de planning van projectresources. Als de kalender wordt gewijzigd, voeren de processen de vereiste updates door bij de planning van projectresources. De processen zorgt helpen ook de prestaties te verbeteren, doordat de resourcegegevens van de kalender vooraf zijn gesynchroniseerd, zodat updates voor de planningsinformatie van resources sneller plaatsvinden. Het wordt aangeraden om de processen als batch in te plannen in plaats van een voor een. Anders bestaat het risico dat iemand de inclusieve datums vergeet waarop de informatie voor het laatst is gesynchroniseerd. Als de inclusieve datums niet worden gebruikt, kunnen lacunes optreden tijdens de datumsynchronisatie.

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Kalendersynchronisatie](./media/projectresourcing04-1024x471.jpg)

**Vergaarde resourcecapaciteit synchroniseren**

Het synchronisatieproces is ontworpen om alle resourcekalenderinformatie te synchroniseren. Deze informatie omvat basiskalenderinformatie over de wijzigingen in de tabel met de resourcekalendercapaciteit van het project. Als nieuwe resources aan het project worden toegevoegd, zorgt synchronisatie ervoor dat de bijgewerkte agendagegevens beschikbaar zijn. Deze synchronisatie kan op elk gewenst moment worden uitgevoerd. 

Het wordt aangeraden om een batch te gebruiken. De opties zijn beschikbaar in het synchroniseren van capaciteitsreserveringen.

-   Klik op **Projectbeheer en boekhouding** &gt; **Periodiek** &gt; **Capaciteitsynchronisatie** &gt; **Vergaarde resourcecapaciteit synchroniseren**.

| Optie | Omschrijving                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ja    | Synchroniseer alle resourcegegevens met kalender- en basiskalenderinformatie, en vervang alle informatie in de resourcecapaciteitkalender van het project.                                                  |
| Nee     | Synchroniseer resourcegegevens, op basis van de datumintervalcode, en de opgegeven begin- en einddata. Met deze optie worden geen bestaande gegevens verwijdert en alleen informatie bijgewerkt voor toegevoegde resources. |

[![Synchronisatieproces](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Rollen configureren op WBS-sjablonen
Projectmanagers kunnen WBS-sjablonen configureren, die ze kunnen toepassen wanneer ze een WBS voor nieuwe projecten maken. Projectmanagers kunnen rollen toevoegen wanneer ze een sjabloon maken. Gebruik de volgende procedure om een rol toe te wijzen aan een WBS-sjabloon.** **

1.  Klik op **Projectbeheer en boekhouding** &gt; **Instellen** &gt; **Projecten** &gt; **Structuursjablonen voor werkspecificatie**.
2.  Selecteer een WBS-sjabloon en klik op **Details**.
3.  Selecteer een taak in de lijst en selecteer in het veld **Rol** een rol die u aan de taak wilt toewijzen.

### <a name="work-with-a-wbs"></a>Werken met een WBS

U kunt een nieuwe WBS maken, of u kunt een WBS van een bestaande WBS-sjabloon kopiëren. Een projectmanager kan de resources eenvoudig beheren door rollen aan nieuwe taken op de WBS toe te wijzen. De rollen kunnen worden vervangen wanneer een resource is verworven, of nadat een bevestigde resource is geïdentificeerd die aan de taak gaat werken. Deze flexibiliteit stelt projectmanagers in staat om de volgende taken uit te voeren:

-   Het aantal resources bepalen dat nodig is voor WBS-werkpakketten.
-   Projectkosten ramen.
-   Een voorlopig budget opstellen.
-   De activiteitsduur schatten op basis van rollen en resources.
-   Enkele projectbeheersplannen ontwikkelen, op basis van de beschikbare projectgegevens.

Extra opties zijn toegevoegd aan de WBS, om beter gebruik te kunnen maken van de resourcingfunctionaliteit.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Optie</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Resourcetoewijzingen</td>
<td>Geef de toegewezen resources weer, de datums, het aantal uren, en het boekingstype voor taken op de WBS.</td>
</tr>
<tr class="even">
<td>Team automatisch genereren</td>
<td>Voeg automatisch geplande resources toe door rollen te gebruiken die aan een taak zijn gekoppeld. Finance and Operations suggereert automatisch geplande resources door middel van de op rollen gebaseerde beslissingsanalyse met meerdere criteria. Nadat de rollen en de inzet (uren) voor taken in de WBS zijn ingesteld en de structuur is vrijgegeven, klikt u op <strong>Team automatisch genereren</strong>. Het vereiste aantal geplande resources wordt toegevoegd aan de WBS en het tabblad <strong>Projectteam en planning</strong>.</td>
</tr>
<tr class="odd">
<td>Resource (vervolgkeuzelijst)</td>
<td>Op de pagina <strong>Resourcetoewijzing starten</strong> kunt u resources vast of variabel boeken, op basis van de opgegeven tijdsduur. U kunt de weergaveinstellingen aanpassen om de duur van resourceactiviteiten weer te geven en in te stellen. U kunt resources selecteren en toewijzen op het niveau van het werkpakket met de volgende opties:
<ul>
<li><strong>Accepteren</strong> Wijzigingen bevestigen aan de resource die aan een taak is toegewezen.</li>
<li><strong>Annuleren</strong> Wijzigingen annuleren aan de resource die aan een taak is toegewezen.</li>
<li><strong>Automatisch toewijzen:</strong> Met deze optie selecteert u een beschikbare bemande resource met een overeenkomende rol voor de geselecteerde taak.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Klik op **Projectbeheer en boekhouding** &gt; **Projecten** &gt; **Alle projecten**.
2.  Selecteer in de lijst het project **XYZ-upgrade Fase 2**.
3.  Klik op **Plan** &gt; **Activiteiten** &gt; **Structuur voor werkspecificatie**.
4.  Klik op **Nieuw** en voeg de volgende activiteiten voor niveau 1 aan de WBS toe:
    -   Initiëren
    -   Planning
    -   In uitvoering
    -   Bewaking en controle
    -   Afsluiten

5.  Stel de datums en de inzet (uren) in, zoals getoond in onderstaande schermopname.[![De datums en inzet instellen](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
6.  Selecteer de taakregel **Initiëren** en selecteer in het veld **Rol** de waarde **Senior projectmanager**.
7.  Klik op **Publiceren**.
8.  Selecteer op dezelfde regel in het veld **Resource** de naam **Daniel Goldschmidt**.
9.  Klik op **Accepteren**.
10. Selecteer de taakregel **Planning** en selecteer in het veld **Rol** de rol **Bedrijfsanalyst**.
11. Klik **Publiceren** en klik daarna op **Team automatisch genereren**.
12. Klik in het dialoogvenster dat wordt geopend op **Ja**.
13. Controleer in het veld **Resource** of de waarde **Bedrijfsanalyst 1** is.
14. Open voor de resource **Bedrijfsanalyst 1** de zoekopdracht en klik op **Formulier Resourcetoewijzing starten**.
15. Selecteer een medewerker voor de taak.
16. Klik op **Variabel boeken** &gt; **Volledige capaciteit**.
17. Klik op **Opslaan** en sluit de pagina. 

> [!NOTE] 
> U ontvangt geen waarschuwing dat de opgegeven resource nu 2 is, omdat het aantal resources op 1 blijft staan.
18. Valideer op de pagina **Structuur voor werkspecificatie** de resourcetoewijzing op de WBS en klik op **Opslaan**.

## <a name="resource-fulfillment-for-planned-resources"></a>Resourcevoorziening voor geplande resources
Een projectmanager kan vereiste resourcerollen voor een project plannen. De resourcemanager ziet deze geplande resources als aanvragen op de pagina **Resourcevervulling** en kan werkelijke resources toewijzen.

1.  Klik op **Projectbeheer en boekhouding** &gt; **Projecten** &gt; **Alle projecten**.
2.  Selecteer in de lijst het project **XYZ-upgrade Fase 2**.
3.  Klik op **Project**.
4.  Klik op **Bewerken**.
5.  Klik op het tabblad **Projectteam en planning**** **op **Toevoegen**.
6.  Selecteer in het dialoogvenster **Rollen toevoegen** de rol **Softwareontwikkelaar**.
7.  Klik op **Maken**.
8.  Sluit de projectpagina.
9.  Klik op **Projectbeheer en boekhouding** &gt; **Projectresources** &gt; **Resourcevervulling**.
10. Selecteer **Softwareontwikkelaar 1** voor het project **XYZ-upgrade Fase 2**.
11. Selecteer een medewerker en klik op **Toewijzen**.
12. Controleer of de regel **Softwareontwikkelaar 1** is verwijderd uit het project **XYZ-upgrade Fase 2**.
13. Controleer op het tabblad **Projectteam en planning** voor het project **XYZ-upgrade Fase 2** of de medewerker die u in stap 11 hebt geselecteerd is toegevoegd als **Softwareontwikkelaar**.

## <a name="requests-for-project-resources"></a>Projectresourceaanvragen
De planningsfuncties voor projectresources biedt resourcemanagers alleen de mogelijkheid om bemande resources te distribueren voor taken of projecten. Om deze functionaliteit in te schakelen, voert u de volgende taken uit of controleert u dat ze zijn voltooid.

-   Nummerreeksen instellen.
-   Workflows voor projectbeheer en boekhouding instellen.
-   Workflow voor resourceaanvraag inschakelen.

Nadat u hebt gecontroleerd of de bovenstaande taken zijn uitgevoerd, kunt u de volgende taken zo nodig uitvoeren.

-   Een resourceaanvraag maken op basis van een variabel geboekte bemande resource.
-   Resourceaanvragen bewaken.
-   Resourceaanvragen vervullen.
-   Een bemande resource aanvragen vanuit de projectstructuur.
-   Resources boeken op een project zonder een aanvraag voor een bemande resource.

## <a name="monitor-project-teams"></a>Projectteams bewaken
1.  Klik op **Projectbeheer en boekhouding** &gt; **Projecten** &gt; **Alle projecten**.
2.  Klik in de lijst met projecten op de koppeling **Project-ID** voor het project **XYZ-upgrade Fase 2**.
3.  Controleer op het sneltabblad **Projectteam en planning** of de daar vermelde projectresources correct zijn.





