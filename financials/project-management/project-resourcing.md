---
title: Resources plannen voor projecten
description: Dit onderwerp biedt informatie over project resourcing.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: cmercado
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: c29c95fc6abd13e668c44d3ccf437bb0e879e46b
ms.lasthandoff: 03/31/2017


---

# <a name="project-resourcing"></a>Resources plannen voor projecten

Dit onderwerp biedt informatie over project resourcing.

Een vraag voor projectmanagers en resourcemanagers tijdens de fase voor de projectplanning is resourcetoewijzing, waar ze moeten bepalen en de juiste resource voor werk aan een project reserveren. In Microsoft Dynamics 365 voor bewerkingen kunt mogelijkheden voor projecten met een resourcing u rollen die worden behandeld als tijdelijke bronnen die kunnen worden gereserveerd voor een specifieke afspraak toe te staan of een deel van een afspraak definiëren. Met dit type resourcing kunnen projectmanagers en resourcemanagers de volgende taken uitvoeren:

-   Een rol definiëren met de vereiste competenties om het afstemmen van resources te vergemakkelijken.
-   Rollen gebruiken voor het definiëren van een eerste toezegging planning op basis van de gereserveerde bronnen.
-   Kosten ramen en een initieel budget opstellen, op basis van rollen en resources die aan een project zijn toegewezen.
-   Rollen gebruiken voor het ramen van het aantal resource-reserveringen die vereist voor elke afspraak toe te staan zijn.
-   Het aantal resources ramen dat voor de volledige levenscyclus van een project is vereist.
-   Een structuur voor werkanalyse (WBS) opstellen via de initiële resourcetoewijzingen.

[![Levenscyclus van projecten](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg) 

Als de projectplanning opbrengst kunnen geplande resources worden vervangen door de resources waar iemand aanwezig is. De projectmanager kan ook teruggaan en de resourcing reserveringen tijdens een van de projectfasen bijwerken.

## <a name="set-up-project-resources"></a>Projectresources instellen
U moet een kalender configureren en deze aan een werknemer of een medewerker (uitvoerende) koppelen. De kalender wordt gebruikt om het project en de werktijd van de resources die zijn gereserveerd voor het project te plannen. Tijdens het configureren van de kalender kunnen projectmanagers resources herverdelen in het kader van optimalisatie van de resources. Op basis van het kalenderplan kunnen beperkingen aan resources worden opgelegd. U kunt een kalender instellen op de **kalenders** pagina. 

Wanneer u een werknemer als een project-resource instelt, u kunt kiezen uit de werknemers die werken in het bedrijf waarvoor u resources instellen of kunt u werknemers van andere bedrijven binnen uw organisatie. Dit zijn intercompany-resources. De volgende procedures wordt beschreven hoe een werknemer instellen als een projectresource binnen uw bedrijf en het instellen van een projectbron voor intercompany.

### <a name="set-up-a-worker-as-a-project-resource"></a>Een medewerker instellen als een projectresource

1.  Op de **werknemers** pagina in de **werknemers** lijst, de werknemer selecteren die u als de projectresource voor een toevoegen wilt en open de werknemersrecord.
2.  Klik in het actievenster op **project**&gt;**Setup**&gt;**projectinstellingen**.
3.  Selecteer een kalender en sluit vervolgens de pagina.

U kunt ook standaardprojecten voor een resource opgeven als een type toewijzing vooraf. Voorafgaande toewijzingen kunnen worden gebruikt wanneer de resource- of projectmanager van tevoren al weet aan welke projecten de resource zal gaan werken. Voorafgaande toewijzingen kunnen plaatsvinden op basis van aanvragen van een projectsponsor of klant. Als u voorafgaande toewijzingen wilt uitvoeren voor een project, selecteert u het gewenste project op de pagina **Projecten toewijzen** op het tabblad **Projecten** in de lijst **Resterende projecten**.

### <a name="set-up-an-intercompany-resource"></a>Een intercompany-resource instellen

Wanneer u een werknemer als een intercompany-resource instelt, kunt u de instellingen in het bedrijf van de lening en het bedrijf leningen moet uitvoeren. 

**In het bedrijf leningen:**

1.  Controleer in Dynamics 365 voor bewerkingen, of dat het bedrijf van de lening is ingeschakeld en voer de voorgaande procedure, 'Instellen van een werknemer als een projectresource '.
2.  Ga naar ** grootboek **&gt; ** boekingsinstellingen **&gt;**intercompany-boekhouding**. Click **New**.
3.  In de ** rechtspersoon-ID ** Selecteer het bedrijf van de lening. Vul de resterende velden indien nodig, en klik vervolgens op **opslaan**.
4.  Ga naar de ** projectbeheer en boekhouding **&gt; ** instellingen **&gt;**prijzen ** &gt;**overdrachtsprijs**.** **
5.  Op de ** overdrachtsprijs ** formulier, klikt u op **nieuw**, en in de ** lenende rechtspersoon ** Selecteer het juiste bedrijf.
6.  Als u lenen alleen het bedrijf leningen de resource die u hebt gemaakt aan het begin van dit punt wilt in de **Resource** veld, selecteert u de naam van de resource die u hebt gemaakt. Als u alle resources in het bedrijf beschikbaar maken voor het bedrijf leningen wilt, laat de ** Resource ** veld leeg.
7.  Ga naar ** projectbeheer en boekhouding **&gt; ** instellingen **&gt;**voor projectbeheer en boekhoudparameters**, en klik in de ** Intercompany ** tabblad, stelt u de ** intercompany resourceplanning en urenstaten inschakelen ** veld **Ja**.

**In het bedrijf leningen:**

1.  Ga naar **projectbeheer en boekhouding**&gt;**project resources**&gt;**lijst met Resources**.
2.  Voer de naam van de resource die u hebt gemaakt in de vorige procedure voor het bedrijf lening om te controleren of de naam wordt opgenomen in de lijst met resources voor het bedrijf leningen in het zoekfilter.

## <a name="manage-resource-competencies"></a>Resourcecompetenties beheren
Resourcecompetenties zijn een essentieel onderdeel van bronbeheer. De competenties kunnen als basislijn worden gebruikt om resources aan te wijzen met de juiste mix van vaardigheden, opleiding, certificering en projectervaring. U moet deze informatie configureren voor elke resource en deze gegevens periodiek bijwerken. Op deze manier kunt u mogelijkheden maximaliseren wanneer specifieke resourcecompetenties tijdens projectresourcetoewijzing worden afgestemd. [![Voorbeelden van vaardigheden, certificeringen, opleiding en projectervaring](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg) 

De volgende procedures leggen uit hoe u competenties voor een resource kunt instellen. 

Configuratie van competenties voor een medewerker kunt u doen op de lijstpagina **Medewerkers** in Human resources of op de lijstpagina **Resources** in Projectbeheer en boekhouding. Voor de volgende procedures, de **werknemers** lijstpagina in HRM wordt gebruikt.

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
1.  Klik op **projectbeheer en boekhouding**&gt;**werkruimten**&gt;**projectbeheer**.
2.  Klik op **Nieuw project** en voer de volgende gegevens in:
    -   **projecttype** - tijd- en materiaalprojecten
    -   **projectnaam** -XYZ Upgrade fase 2
    -   **projectgroep** -TM\_OHW
    -   **project, projectcontract-ID** -00000002
3.  Klik op **Project maken**.

### <a name="assign-a-resource-to-a-project"></a>Een resource toewijzen aan een project

1.  Klik op **Human resources**&gt;**werknemers**&gt;**werknemers**.
2.  Selecteer in de lijst **Medewerkers** de record van de medewerker waarvoor u eerder competenties hebt geconfigureerd en openen de medewerkerrecord.
3.  Klik in het actievenster op het tabblad **Project** in de groep **Instellingen** op **Projecten toewijzen**.
4.  Klik op de pagina **Projecttoewijzingen voor resourcevalidatie** op het tabblad **Projecten**.
5.  In de **het project toevoegen aan geselecteerde projecten**, filter op het project, XYZ Upgrade fase 2
6.  Selecteer een project in het deelvenster **Resterende projecten** en klik op de pijl om dit toe te voegen aan het deelvenster **Geselecteerde projecten**.
7.  Sluit de pagina.

Indien nodig kunt u ook categorieën voor een resource toewijzen. Het categorietype is ofwel Kosten of Opbrengst. Dit wordt bepaald door uw organisatie. Als er geen toegewezen categorieën voor de resource, opzoeken Dynamics 365 for Operations standaardcategorie op uur-prijzen voor kosten en opbrengsten.

### <a name="set-up-project-resource-and-role-characteristics"></a>Kenmerken voor projectresource en rollen configureren

Een projectmanager kan de resourcingfunctionaliteit van het project gebruiken om de rollen te maken die het project vereist. Rollen kunnen worden gebruikt wanneer de bevestigde resources nog niet bekend zijn bij het reserveren van resources. Rollen kunnen tijdelijk als geplande resources worden gereserveerd, zodat u de fasen van de projectplanning kunt doorgaan. 

[![Voorbeeld van een rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso is aangezocht om een project van het type Tijd en materiaal uit te voeren, dat een goedgekeurd projectcharter heeft. De juniorprojectmanager is nog bezig de reikwijdte van het project te bepalen. De resourcemanager is momenteel identificeren van specifieke bronnen die wordt gereserveerd als u wilt werken in het nieuwe project. Een van de rollen die de opdrachtgever project heeft aangevraagd, vanwege het kritieke karakter van het project, is de Senior projectmanager. De resourcemanager moet verkrijgen van de nieuwe resource en de rol definiëren in het systeem in het geval de junior projectmanager de resourcegegevens tijdens de projectplanning moet. 

De volgende stappen weergeven hoe de resourcemanager kunt instellen van de rol Senior manager resource kenmerken aan gekoppeld. Later kan de worden gebruikt om te zoeken naar beschikbare resources die voldoen aan de vereiste resourcecompetenties.

1.  Klik op **projectbeheer en boekhouding**&gt;**Setup**&gt;**Resources**&gt;**rollen instellen**.
2.  Klik op **Nieuw** en voer de volgende gegevens in:
    -   **Rol-ID** -Senior projectmanager
    -   **Beschrijving** -Senior projectmanager
3.  Klik op **Maken**.
4.  Selecteer de rol **Senior projectmanager** en klik op **Kenmerken configureren**.
5.  Selecteer in het veld **Type kenmerk** de waarde **Vaardigheid**.
6.  Voer in het veld **Beschikbare kenmerken** de vaardigheid in waarnaar u zoekt.
7.  Selecteer in het veld **Type kenmerk** de waarde **Getuigschrift**.
8.  Voer in het veld **Beschikbare kenmerken** het type getuigschrift in waarnaar u zoekt.
9.  Klik op **OK** en sluit de pagina.

### <a name="assign-a-project-resource-to-a-project"></a>Een projectresource toewijzen aan een project

1.  Klik op **projectbeheer en boekhouding**&gt;**veelgebruikte**&gt;**projecten**&gt;**alle projecten**, en open de **XYZ Upgrade fase 2** project.
2.  Klik op het tabblad **Projectteam en planning** op **Toevoegen**.
3.  Selecteer in het veld **Rol** de waarde **Teamlid**.
4.  Klik op **Boeken vanuit kalender**.
5.  Klik op de pagina **Resourcebeschikbaarheid** op **Weergave-instellingen**.
6.  Voer op de pagina **Weergave-instellingen aanpassen** de volgende waarden in:
    -   **De opmaak voor weergave van datum-bereik** - dag
    -   **Beschikbaarheid beschrijvingen weergeven** : Ja
    -   **Weergave resterende capaciteit** : Ja
7.  Selecteer in de lijst van resources een resource.
8.  Klik op **definitieve boeking**&gt;**capaciteit volledig**.
9.  Sluit de pagina.

### <a name="assign-a-resource-to-a-default-role"></a>Een resource aan een standaardrol toewijzen

Als u wilt project of de resource managers, kunt u inzoomen verder op de resources die kunnen worden gereserveerd voor een project. U kunt een standaardrol aan een bestaande resource toewijzen of aan nieuw verworven resource. Bijvoorbeeld wanneer Daniel is aangesteld, had hij de ervaring en vaardigheden voor het vullen van de zakelijke analisten rol. De resourcemanager deze functie als de standaardfunctie van Daniel toegewezen. Daarom wordt de resourcemanager Daniel toegevoegd aan een groep zakelijke analisten die beschikbaar zijn voor het werken aan projecten. 

Bij het reserveren van de resource, kunnen projectmanagers filteren, de rol resources die beschikbaar zijn aan projecten kunnen werken. Ze kunnen deze informatie als een criterium gebruiken wanneer ze de beslissingsanalyse met meerdere criteria uitvoeren tijdens het vervullen van resources. Ze kunnen ook andere resourcekenmerken aan het filter toevoegen, om te zoeken naar resources die bepaalde vaardigheden, opleiding, en ervaring hebben voor een bepaald project. 

**Scenario:** een goedgekeurde project is gestart en de rol Senior manager tijdens de planningsfase project als een geplande resource is gereserveerd. De resourcemanager heeft nu een resource verworven om de rol van Senior projectmanager te vervullen.

1.  Klik op **projectbeheer en boekhouding**&gt;**project resources**&gt;**lijst met Resources**.
2.  Selecteer in de lijst **Resource** de waarde **Daniel Goldschmidt**.
3.  Klik op **project resource**&gt;**onderhouden**&gt;**resourcerol**.
4.  Klik op **Nieuw** en voer de volgende gegevens in:
    -   **Effectieve** - (de huidige datum)
    -   **Vervaldatum** - nooit
    -   **Rol** -Senior projectmanager
5.  Klik op **Opslaan** en sluit de pagina.
6.  Voeg op het tabblad **Competenties** de vaardigheid **Projectbeheer** en het getuigschrift **PMP** toe.

## <a name="set-up-role-based-pricing"></a>Rol-gebaseerde prijzen configreren
Alle prijzen voor kosten, verkoop, en overdracht kunnen voor rollen worden geconfigureerd.

1.  Klik op **projectbeheer en boekhouding**&gt;**Setup**&gt;**prijzen**&gt;**verkoopprijs (uur)**.
2.  Click **New**.
3.  Voer een ingangsdatum in.
4.  Selecteer een rol in de kolom **Rol**.
5.  Voer in de kolom **Prijscalculatie** een prijs in voor de geselecteerde resourcerol.

## <a name="form-a-project-team"></a>Een project-team
Voor het gebruik van de rollen die eerder zijn ingesteld in een project, moet een projectmanager de rollen koppelen aan het project. Meerdere rollen kunnen worden toegewezen voor een project en deze rollen Dynamics 365 for Operations automatisch labels tijdens reservering om verwarring te voorkomen dat. Bijvoorbeeld: als de projectmanager moet drie softwareontwikkelaars, drie rollen van de Software engineer met software voor technicus 1, software, technicus 2 en software engineer 3 als de bijbehorende labels worden automatisch gegenereerd. Als voor de rol eerder rolkenmerken zijn ingesteld, worden deze toegepast als filter in zoekopdrachten naar een resource. Aanvullende kenmerken kunnen indien nodig worden toegevoegd om het zoeken te verfijnen. 

Weergave-instellingen kunnen ook worden aangepast voor een betere weergave van de beschikbaarheid van resources. Er zijn opties voor weergave van beschikbaarheid per uur, dag, week, maand, kwartaal en jaar. Er is ook een optie om beschikbaar en resterende capaciteit van resources weer te geven. Deze optie is handig voor tijdbeheer, wanneer u beschikbare tijd voor activiteiten of resourcebeschikbaarheid raamt. 

De projectmanager kan een rol op de pagina selecteren en als er een beschikbare bron die voldoet aan de behoefte, selecteer een resource voor de rol gereserveerd. Houd er rekening mee dat de resources niet worden gereserveerd op dit moment tijdens de planning. Wanneer u een projectstructuur maakt, kunt u rollen vervangen waar iemand aanwezig is resources voor het project. Als rollen worden vervangen door de bronnen voor waar iemand aanwezig is in de projectstructuur, de resource-instellingen automatisch bijgewerkt met het projectteam kunt opnemen en plannen. 

[![projectlijst team met zowel de rollen en de werkelijke resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

De projectmanager heeft verschillende opties om een resource op een project te boeken, zoals **Resterende capaciteit**, **Volledige capaciteit**, **Percentage van capaciteit** en **Uren opgeven**. Deze boekingsopties kunnen op elk moment worden geannuleerd als de resourcetoewijzingen wijzigen. Twee typen boeking worden ondersteund:

-   **Definitieve boeking** : de reservering van de resource is goedgekeurd en bevestigd voor werkzaamheden aan de overeenkomst voor de opgegeven duur.
-   **Variabele boeking** : de reserveringen voor de resource voorlopig werken op de afspraak toe te staan voor de opgegeven duur is ingesteld.

De onderstaande procedure licht toe hoe u een projectteam maakt.

### <a name="create-a-project-team"></a>Een projectteam maken

1.  Selecteer een project op de lijstpagina **Alle projecten** en klik op **Bewerken**.
2.  Op de **team en planning van projecten** tabblad in het **planning einddatum** en voer de begindatum van publicatieschema plus één maand. Als de begindatum van het schema is bijvoorbeeld 24 juni 2017 (24/06/2017), voer **24/07/2017**.
3.  Click **Add**.
4.  Selecteer in het venster **Rollen toevoegen aan het project** in het veld **Rol ** de waarde **Senior projectmanager**.
5.  Klik op **Vereiste competenties**.
6.  Op de pagina **Kenmerken kiezen** zijn de kenmerken die u eerder hebt ingesteld voor de rol Senior projectmanager automatisch geselecteerd. Klik tot slot op **OK**.
7.  Voer op de pagina **Rollen toevoegen aan project** in het veld **Aantal resources** de waarde **1** in.
8.  In het veld **Resource** geeft de zoekopdracht alle resources weer die de vereiste competenties hebben. Selecteer **Daniel Goldschmidt** en klik op **Maken**.
9.  Klik op de pagina **Project** op **Toevoegen**.
10. Selecteer in het venster **Rollen toevoegen aan het project** in het veld **Rol ** de waarde **Teamlid**. Voer in het veld **Aantal resources** de waarde **5** in.
11. Klik op **Maken**.
12. Klik op de pagina **Projecten** op **Voorzien in resource**.

## <a name="resource-capacity-synchronization"></a>Capaciteitsynchronisatie voor resource
De processen voor resourcesynchronisatie helpen ervoor te zorgen dat de informatie van kalender en basiskalender doorvloeien naar de planning van projectresources. Als de kalender wordt gewijzigd, voeren de processen de vereiste updates door bij de planning van projectresources. De processen zorgt helpen ook de prestaties te verbeteren, doordat de resourcegegevens van de kalender vooraf zijn gesynchroniseerd, zodat updates voor de planningsinformatie van resources sneller plaatsvinden. Het wordt aangeraden om de processen als batch in te plannen in plaats van een voor een. Anders bestaat het risico dat iemand de inclusieve datums vergeet waarop de informatie voor het laatst is gesynchroniseerd. Als de inclusieve datums niet worden gebruikt, kunnen lacunes optreden tijdens de datumsynchronisatie.

### <a name="calendar-synchronizationmediaprojectresourcing04-1024x471jpg"></a>![Synchronisatie van de agenda](./media/projectresourcing04-1024x471.jpg)

**Synchronize resource capacity roll-ups**

Het synchronisatieproces is ontworpen om alle resourcekalenderinformatie te synchroniseren. Deze informatie omvat basiskalenderinformatie over de wijzigingen in de tabel met de resourcekalendercapaciteit van het project. Als er nieuwe resources worden toegevoegd in het project, wordt er synchronisatie zorgt ervoor dat de bijgewerkte kalendergegevens beschikbaar is. Deze synchronisatie kan op elk gewenst moment worden uitgevoerd. 

Het wordt aangeraden om een batch te gebruiken. De opties zijn beschikbaar in het synchroniseren van capaciteitsreserveringen.

-   Klik op **projectbeheer en boekhouding**&gt;**periodiek**&gt;**capaciteit synchronisatie**&gt;**resources capaciteit samengevouwen gegevens synchroniseren**.

| Optie | Omschrijving                                                                                                                                                                                          |
|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ja    | Synchroniseer alle resourcegegevens met kalender- en basiskalenderinformatie, en vervang alle informatie in de resourcecapaciteitkalender van het project.                                                  |
| Nee     | Synchroniseer resourcegegevens, op basis van de datumintervalcode, en de opgegeven begin- en einddata. Met deze optie worden geen bestaande gegevens verwijdert en alleen informatie bijgewerkt voor toegevoegde resources. |

[![Synchronisatieproces](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Rollen configureren op WBS-sjablonen
Projectmanagers kunnen WBS-sjablonen configureren, die ze kunnen toepassen wanneer ze een WBS voor nieuwe projecten maken. Projectmanagers kunnen rollen toevoegen wanneer ze een sjabloon maken. Gebruik de volgende procedure een rol toewijzen aan een projectstructuur template.* * **

1.  Klik op **projectbeheer en boekhouding**&gt;**Setup**&gt;**projecten**&gt;**Structuursjablonen voor werkspecificatie**.
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
<td>Voeg automatisch geplande resources toe door rollen te gebruiken die aan een taak zijn gekoppeld. Dynamics 365 voor bewerkingen stelt automatisch geplande resources met behulp van meerdere criteria beslissing analyse op basis van rollen. Nadat de rollen en de inzet (uren) voor taken in de WBS zijn ingesteld en de structuur is vrijgegeven, klikt u op <strong>Team automatisch genereren</strong>. Het vereiste aantal geplande resources wordt toegevoegd aan de WBS en het tabblad <strong>Projectteam en planning</strong>.</td>
</tr>
<tr class="odd">
<td>Resource (vervolgkeuzelijst)</td>
<td>Op de pagina <strong>Resourcetoewijzing starten</strong> kunt u resources vast of variabel boeken, op basis van de opgegeven tijdsduur. U kunt de weergaveinstellingen aanpassen om de duur van resourceactiviteiten weer te geven en in te stellen. U kunt resources selecteren en toewijzen op het niveau van het werkpakket met de volgende opties:
<ul>
<li><strong>Accepteren</strong> Wijzigingen bevestigen aan de resource die aan een taak is toegewezen.</li>
<li><strong>Annuleren</strong> Wijzigingen annuleren aan de resource die aan een taak is toegewezen.</li>
<li><strong>Automatische toewijzing van</strong> : deze optie worden geselecteerd voor een beschikbare waar iemand aanwezig is, bron met een overeenkomende rol aan de geselecteerde taak.</li>
</ul></td>
</tr>
</tbody>
</table>

1.  Klik op **projectbeheer en boekhouding**&gt;**projecten**&gt;**alle projecten**.
2.  Selecteer in de lijst het project **XYZ-upgrade Fase 2**.
3.  Klik op **plannen**&gt;**activiteiten**&gt;**structuur voor werkspecificatie**.
4.  Klik op **Nieuw** en voeg de volgende activiteiten voor niveau 1 aan de WBS toe:
    -   Initiëren
    -   Planning
    -   In uitvoering
    -   Bewaking en controle
    -   Afsluiten

5.  Stel de datums en inzet (uren), zoals in de volgende schermopname. [![De datums en inzet instellen](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)
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
16. Klik op **zacht toewijzen**&gt;**capaciteit volledig**.
17. Klik op **Opslaan** en sluit de pagina. 

> [!NOTE] 
> U niet gewaarschuwd dat de opgegeven resource nu 2 is, omdat het aantal resources bij 1 blijft.
18. Valideer op de pagina **Structuur voor werkspecificatie ** de resourcetoewijzing op de WBS en klik op **Opslaan**.

## <a name="resource-fulfillment-for-planned-resources"></a>Resourcevoorziening voor geplande resources
Een projectmanager kan vereiste resourcerollen voor een project plannen. De resourcemanager ziet deze geplande resources als aanvragen op de pagina **Resourcevervulling** en kan werkelijke resources toewijzen.

1.  Klik op **projectbeheer en boekhouding**&gt;**projecten**&gt;**alle projecten**.
2.  Selecteer in de lijst het project **XYZ-upgrade Fase 2**.
3.  Klik op **Project**.
4.  Klik op **Bewerken**.
5.  Op de **team en planning van projecten** tabblad ** ** Klik op **Add**.
6.  Selecteer in het dialoogvenster **Rollen toevoegen** de rol **Softwareontwikkelaar**.
7.  Klik op **Maken**.
8.  Sluit de projectpagina.
9.  Klik op **projectbeheer en boekhouding**&gt;**project resources**&gt;**Resource afhandeling**.
10. Selecteer **Softwareontwikkelaar 1** voor het project **XYZ-upgrade Fase 2**.
11. Selecteer een medewerker en klik op **Toewijzen**.
12. Controleer of de regel **Softwareontwikkelaar 1** is verwijderd uit het project **XYZ-upgrade Fase 2**.
13. Controleer op het tabblad **Projectteam en planning** voor het project **XYZ-upgrade Fase 2** of de medewerker die u in stap 11 hebt geselecteerd is toegevoegd als **Softwareontwikkelaar**.

## <a name="requests-for-project-resources"></a>Aanvragen voor projectbronnen
De planningsfuncties voor project-resource ondersteunt alleen resourcemanagers waar iemand bronnen op algemeen of projecten verdelen. Deze functionaliteit, zodat de volgende taken uitvoeren of controleren dat ze zijn voltooid.

-   Nummerreeksen instellen.
-   Projectbeheer en boekhoudingwerkstromen instellen.
-   Workflow voor gebruikersaanvragen resource inschakelen.

Nadat u hebt gecontroleerd of de bovenstaande taken uitgevoerd, kunt u de volgende taken uitvoeren, indien nodig.

-   Een aanvraag voor een resource van een zachte waar iemand resource maken
-   Bron aanvragen controleren.
-   Voldoen aan verzoeken van resource om.
-   Een bron waar iemand aanwezig is bij projectstructuur aanvragen.
-   Boek de resources aan een project zonder een aanvraag voor een resource waar iemand aanwezig is.

## <a name="monitor-project-teams"></a>Projectteams bewaken
1.  Klik op **projectbeheer en boekhouding**&gt;**projecten**&gt;**alle projecten**.
2.  Klik in de lijst met projecten op de koppeling **Project-ID** voor het project **XYZ-upgrade Fase 2**.
3.  Controleer op het sneltabblad **Projectteam en planning** of de daar vermelde projectresources correct zijn.



