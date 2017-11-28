---
title: Resources plannen voor projecten
description: In dit onderwerp vindt u informatie over het plannen van resources voor projecten.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4dbcfd31030db8e40f89f86a76cdc666ac433749
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="project-resourcing"></a>Resources plannen voor projecten

[!include[banner](../includes/banner.md)]

In dit onderwerp vindt u informatie over het plannen van resources voor projecten.

Een van de uitdagingen voor projectmanagers en resourcemanagers tijdens de projectplanningsfase is resourcetoewijzing, waarin ze de juiste resources moetn definiëren en reserveren voor werk aan een project. In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition kunt u met de capaciteiten voor projectresourcing rollen definiëren die worden behandeld als tijdelijke resources. Die kunt u reserveren voor een specifieke taak of een deel van een taak. Met dit type resourcing kunnen projectmanagers en resourcemanagers de volgende taken uitvoeren:

- Een rol definiëren met de vereiste competenties om het afstemmen van resources te vergemakkelijken.
- Met behulp van rollen een initiële taakplanning definiëren op basis van resourcereserveringen.
- Kosten ramen en een initieel budget opstellen, op basis van rollen en resources die aan een project zijn toegewezen.
- Met behulp van rollen het aantal resourcereserveringen ramen die voor elke taak zijn vereist.
- Het aantal resources ramen dat voor de volledige levenscyclus van een project vereist is.
- Een structuur voor werkanalyse (WBS) opstellen via de initiële resourcetoewijzingen.

[![Projectlevenscyclus](./media/projectresourcing02-1024x812.jpg)](./media/projectresourcing02.jpg)

Wanneer de projectplanning vordert, kunnen geplande resources worden vervangen door bemande resources. De projectmanager kan ook teruggaan naar het begin en de resourcereserveringen bijwerken in elke projectfase.

## <a name="set-up-project-resources"></a>Projectresources instellen
U moet een kalender configureren en deze aan een werknemer of een medewerker (uitvoerende) koppelen. De kalender wordt gebruikt om het project en de werktijd van de resources te plannen, die voor het project zijn gereserveerd. Tijdens het configureren van de kalender kunnen projectmanagers resources herverdelen in het kader van optimalisatie van de resources. Op basis van het kalenderplan kunnen beperkingen aan resources worden opgelegd. U kunt een kalender instellen op de pagina **Kalenders**.

Wanneer u een werknemer als een projectresource instelt, u kunt kiezen uit de werknemers die werken in het bedrijf waarvoor u resources instelt. U kunt ook werknemers selecteren van andere bedrijven binnen uw organisatie. Dit zijn intercompany-resources.

In de volgende procedures wordt beschreven hoe u een werknemer configureert als een projectresource binnen uw bedrijf en hoe u een intercompany-projectresource configureert.

### <a name="set-up-a-worker-as-a-project-resource"></a>Een medewerker instellen als een projectresource

1. Selecteer op de pagina **Medewerkers** in de lijst **Medewerkers** de medewerker die u als projectresource toevoegt en open de record van de medewerker.
2. In het actievenster selecteert u **Project** &gt; **Instellen** &gt; **Projectinstellingen**.
3. Selecteer een kalender en sluit vervolgens de pagina.

U kunt ook standaardprojecten voor een resource opgeven als een type toewijzing vooraf. Voorafgaande toewijzingen kunnen worden gebruikt wanneer de resource- of projectmanager van tevoren al weet aan welke projecten de resource zal gaan werken. Voorafgaande toewijzingen kunnen plaatsvinden op basis van aanvragen van een projectsponsor of klant. Als u voorafgaande toewijzingen wilt uitvoeren voor een project, selecteert u het gewenste project op de pagina **Projecten toewijzen** op het tabblad **Projecten** in de lijst **Resterende projecten**.

### <a name="set-up-an-intercompany-resource"></a>Een intercompany-resource instellen

Wanneer u een werknemer als een intercompany-resource instelt, moet u de instellingen uitvoeren in het bedrijf dat de werknemer uitleent en in het bedrijf dat de werknemer leent.

**In het uitlenende bedrijf**

1. Controleer in Finance and Operations of het uitlenende bedrijf is geselecteerd en voer de bovenstaande procedure Een werknemer instellen als een projectresource uit.
2. Selecteer op de pagina **Intercompany-boekhouding** de optie **Nieuw**.
3. Selecteer in het veld **Rechtspersoon-ID** het uitlenende bedrijf. Vul de resterende velden in met de vereiste waarden en selecteer **Opslaan**.
4. Selecteer op de pagina **Prijs overboeken** de optie **Nieuw**.
5. Selecteer in het veld **Lenende rechtspersoon** het betreffende bedrijf.
6. Als u aan het lenende bedrijf alleen de resource wilt uitlenen die u hebt gemaakt aan het begin van deze sectie, selecteert u in het veld **Resource** de naam van de resource die u hebt gemaakt. Als u alle resources in het uitlenende bedrijf beschikbaar wilt stellen voor het lenende bedrijf, laat u het veld **Resource** leeg.
7. Stel op de pagina **Projectbeheer- en boekhoudingsparameters** op het tabblad **Intercompany** de optie **Intercompany-resourceplanning en urenstaten inschakelen** in op **Ja**.

**In het lenende bedrijf**

- Voer op de pagina **Resourcelijst** in het zoekfilter de naam in van de resource die u hebt gemaakt in de vorige procedure voor het uitlenende bedrijf, om te controleren of de naam voorkomt in de lijst met resources voor het lenende bedrijf.

## <a name="manage-resource-competencies"></a>Resourcecompetenties beheren
Resourcecompetenties zijn een cruciaal onderdeel van resourcebeheer. De competenties kunnen als basislijn worden gebruikt om resources aan te wijzen met de juiste mix van vaardigheden, opleiding, certificering en projectervaring. U moet deze informatie configureren voor elke resource en deze gegevens periodiek bijwerken. Op deze manier kunt u mogelijkheden maximaliseren wanneer specifieke resourcecompetenties tijdens projectresourcetoewijzing worden afgestemd.

[![Voorbeelden van vaardigheden, certificaten, opleiding en projectervaring](./media/projectresourcing06-1024x383.jpg)](./media/projectresourcing06.jpg)

De volgende procedures leggen uit hoe u competenties voor een resource kunt instellen.

Configuratie van competenties voor een medewerker kunt u doen op de lijstpagina **Medewerkers** in Human resources of op de lijstpagina **Resources** in Projectbeheer en boekhouding. In de volgende procedures wordt gebruik gemaakt van de lijstpagina **Medewerkers** in Human Resources.

### <a name="set-up-competencies-certificates"></a>Competenties configureren: getuigschriften

1. Selecteer op de lijstpagina **Werknemers** de regel van de werknemer waarvoor u getuigschriftgegevens wilt toevoegen.
2. Selecteer in het actievenster op het tabblad **Werknemer** in de groep **Competenties** de optie **Getuigschriften**.
3. Selecteer **Nieuw** en selecteer in het veld **Type getuigschrift** de waarde **PMP**.
4. In het veld **Begindatum** selecteert u **1-10-2015** en vervolgens selecteert u **Opslaan**.

### <a name="set-up-competencies-skills"></a>Vaardigheden instellen: vaardigheden

1. Controleer of op de lijstpagina **Medewerkers** dat de werknemer die u in de vorige procedure hebt gebruikt nog steeds is geselecteerd. Selecteer in het actievenster op het tabblad **Werknemer** in de groep **Competenties** de optie **Vaardigheden**.
2. Selecteer **Nieuw**.
3. Selecteer in het veld **Vaardigheid** de waarde **Projectbeheer**.
4. Selecteer in het veld **Niveau** de waarde **5 Expert**.
5. Selecteer in het veld **Niveaudatum** de waarde **14-1-2014**.
6. Voer in het veld **Jaren ervaring** de waarde **10** in.
7. Selecteer **Opslaan** en sluit de pagina.

## <a name="create-a-new-project"></a>Een nieuw project maken
1. Selecteer op de pagina **Projectbeheer** de optie **Nieuw project** en voer de volgende waarden in:

    - **Projecttype:** Tijd en materiaal
    - **Projectnaam:** Xyz-upgrade fase 2
    - **Projectgroep:** TM\_WIP
    - **Projectcontract-id:** 00000002

2. Selecteer **Project maken**.

### <a name="assign-a-resource-to-a-project"></a>Een resource toewijzen aan een project

1. Selecteer op de pagina **Werknemers** in de lijst **Werknemers** de record van de werknemer waarvoor u eerder competenties hebt geconfigureerd. Open vervolgens de werknemerrecord.
2. Selecteer in het actievenster op het tabblad **Project** in de groep **Instellingen** de optie **Projecten toewijzen**.
3. Filter op de pagina **Projecttoewijzingen voor resourcevalidatie** op het tabblad **Projecten** het veld **Het project toevoegen aan geselecteerde projecten** op het project **XYZ-upgrade Fase 2**.
4. Selecteer een project in het deelvenster **Resterende projecten** en selecteer de pijlknop om het toe te voegen aan het deelvenster **Geselecteerde projecten**.

Indien nodig kunt u ook categorieën aan een resource toewijzen. Het categorietype is **Kosten** of **Opbrengst**. Uw organisatie bepaalt het categorietype. Als er geen categorieën zijn toegewezen voor een resource, wordt de standaardcategorie voor uurtarieven voor kosten en opbrengsten opgezocht.

### <a name="set-up-project-resource-and-role-characteristics"></a>Kenmerken voor projectresource en rollen configureren

Een projectmanager kan de resourcingfunctionaliteit van het project gebruiken om de rollen te maken die het project vereist. Rollen kunnen worden gebruikt als tijdens het reserveren van resources nog geen bevestigde resources bekend zijn. Met rollen kunt u resources tijdelijk reserveren als gepland, zodat u de projectplanningsfasen kunt voortzetten.

[![Voorbeeld van een rol](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Scenario:** Contoso is aangezocht om een project van het type Tijd en materiaal uit te voeren, dat een goedgekeurd projectcharter heeft. De juniorprojectmanager is nog bezig de reikwijdte van het project te bepalen. De resourcemanager identificeert momenteel specifieke resources die worden gereserveerd om aan het nieuwe project te werken. Vanwege de kritieke aard van het project heeft de projectsponsor om de senior projectmanager gevraagd als een van de rollen. De resourcemanager moet de nieuwe resource verkrijgen en de rol in het systeem definiëren, voor het geval de junior projectmanager de resourcegegevens tijdens de projectplanning nodig heeft.

De volgende stappen geven weer hoe de resourcemanager rol Senior projectmanager kan configureren en er resourcekenmerken aan kan toewijzen. Later kan de worden gebruikt om te zoeken naar beschikbare resources die voldoen aan de vereiste resourcecompetenties.

1. Selecteer op de pagina **Rollen instellen** de optie **Nieuw** en voer de volgende waarden in:

    - **Rol-ID:** Senior projectmanager
    - **Beschrijving:** Senior projectmanager

2. Selecteer **Maken**.
3. Selecteer de rol **Senior projectmanager** en selecteer **Kenmerken configureren**.
4. Selecteer in het veld **Type kenmerk** de waarde **Vaardigheid**.
5. Voer in het veld **Beschikbare kenmerken** de vaardigheid in waarnaar u zoekt.
6. Selecteer in het veld **Type kenmerk** de waarde **Getuigschrift**.
7. Voer in het veld **Beschikbare kenmerken** het type getuigschrift in waarnaar u zoekt.

### <a name="assign-a-project-resource-to-a-project"></a>Een projectresource toewijzen aan een project

1. Op de pagina **Alle projecten** selecteert u het project **XYZ-upgrade Fase 2**.
2. Selecteer op het tabblad **Projectteam en planning** de optie **Toevoegen**.
3. Selecteer in het veld **Rol** de waarde **Teamlid**.
4. Selecteer **Boeken vanuit kalender**.
5. Selecteer op de pagina **Resourcebeschikbaarheid** de optie **Weergave-instellingen**.
6. Voer op de pagina **Weergave-instellingen aanpassen** de volgende waarden in:

    - **Indeling voor weergave datumbereik:** Dag
    - **Beschikbaarheidsomschrijvingen weergeven:** Ja
    - **Resterende capaciteit weergeven:** Ja

7. Selecteer in de lijst van resources een resource.
8. Selecteer **Vast boek** en **Volledige capaciteit**.


### <a name="assign-a-resource-to-a-default-role"></a>Een resource aan een standaardrol toewijzen

Om project- of resourcemanagers te helpen, kan verder worden ingezoomd op de resources die voor een project kunnen worden gereserveerd. U kunt een standaardrol aan een bestaande resource toewijzen of aan nieuw verworven resource. Toen bijvoorbeeld Daniel werd aangenomen, had hij de ervaring en vaardigheden voor de rol Bedrijfsanalist. De resourcemanager heeft deze rol toegewezen als Daniel's standaardrol. Daartoe heeft de resourcemanager Daniel toegevoegd aan een groep bedrijfsanalisten die beschikbaar zijn voor het werken aan projecten.

Tijdens resourcereservering kunnen de projectmanagers de rolresources filteren die beschikbaar zijn om aan projecten te werken. Ze kunnen deze informatie als een criterium gebruiken wanneer ze de beslissingsanalyse met meerdere criteria uitvoeren tijdens het vervullen van resources. Ze kunnen ook andere resourcekenmerken aan het filter toevoegen, om te zoeken naar resources die bepaalde vaardigheden, opleiding, en ervaring hebben voor een bepaald project.

**Scenario:** Een goedgekeurd project is van start gegaan en de rol Senior projectmanager is gereserveerd als geplande resource tijdens de projectplanningsfase. De resourcemanager heeft nu een resource verworven om de rol van Senior projectmanager te vervullen.

1. Selecteer op de pagina **Resourcelijst** de waarde **Daniel Goldschmidt**.
2. Selecteer op de pagina **Resourcerol** de optie **Nieuw** en voer de volgende waarden in:

    - **Ingangsdatum:** voer de huidige datum in.
    - **Vervaldatum:** voer **Nooit** in.
    - **Rol:** voer **Senior projectmanager** in.

3. Selecteer **Opslaan** en sluit de pagina.
4. Voeg op het tabblad **Competenties** de vaardigheid **Projectbeheer** en het getuigschrift **PMP** toe.

## <a name="set-up-role-based-pricing"></a>Rol-gebaseerde prijzen configreren
Alle prijzen voor kosten, verkoop, en overdracht kunnen voor rollen worden geconfigureerd.

1. Op de pagina **Verkoopprijs (uur)** selecteert u **Nieuw** en voert u een ingangsdatum in.
2. Selecteer een rol in de kolom **Rol**.
3. Voer in de kolom **Prijscalculatie** een prijs in voor de geselecteerde resourcerol.

## <a name="form-a-project-team"></a>Een projectteam vormen
Om de rollen te gebruiken die eerder in een project zijn geconfigureerd, moet een projectmanager de rollen aan het project koppelen. Voor een project kunnen meerdere rollen worden toegewezen. Om verwarring te voorkomen, worden deze rollen automatisch gelabeld tijdens de reservering. Als de projectmanager drie software-engineers nodig heeft, worden bijvoorbeeld automatisch drie software-engineerrollen gegenereerd met de labels **Software-engineer 1**, **Software-engineer 2** en **Software-engineer 3**. Als voor de rol eerder rolkenmerken zijn ingesteld, worden deze toegepast als filter in zoekopdrachten naar een resource. Aanvullende kenmerken kunnen indien nodig worden toegevoegd om het zoeken te verfijnen.

Weergave-instellingen kunnen ook worden aangepast voor een betere weergave van de beschikbaarheid van resources. Er zijn opties voor weergave van beschikbaarheid per uur, dag, week, maand, kwartaal en jaar. Er is ook een optie om beschikbaar en resterende capaciteit van resources weer te geven. Deze optie is handig voor tijdbeheer, wanneer u beschikbare tijd voor activiteiten of resourcebeschikbaarheid raamt.

De projectmanager kan een rol op de pagina selecteren en vervolgens, als er een beschikbare resource is die aan de vereisten voldoet, daarvoor een resource reserveren die de rol vervult. De resources hoeven niet op dit moment in de planningsfase te worden gereserveerd. Wanneer u een WBS maakt, kunt u rollen vervangen door bemande resources voor het project. Als rollen worden vervangen door bemande rollen in de WBS, werkt de resourceconfiguratie automatisch de projectteamlijst en de planning bij.

[![Projectteamlijst die zowel rollen als werkelijke resources bevat](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

De projectmanager heeft verschillende opties om een resource op een project te boeken, zoals **Resterende capaciteit**, **Volledige capaciteit**, **Percentage van capaciteit** en **Uren opgeven**. Deze boekingsopties kunnen op elk moment worden geannuleerd als de resourcetoewijzingen wijzigen. Twee typen boeking worden ondersteund:

- **Vast boeken**: De resourcereservering is goedgekeurd en is bevestigd om aan de taak te werken voor de opgegeven periode.
- **Variabel boeken**: De resourcereservering is voorlopig ingesteld om aan de taak te werken voor de opgegeven periode.

De onderstaande procedure licht toe hoe u een projectteam maakt.

### <a name="create-a-project-team"></a>Een projectteam maken

1. Selecteer een project op de lijstpagina **Alle projecten** en selecteer **Bewerken**.
2. Voer op het tabblad **Projectteam en planning** in het veld **Planning einddatum** de begindatum van het schema plus één maand in. Als bijvoorbeeld de planningbegindatum 24 juni 2017 is (24-06-2017), voert u **24-07-2017** in.
3. Selecteer **Toevoegen**.
4. Selecteer in het venster **Rollen toevoegen aan het project** in het veld **Rol** de waarde **Senior projectmanager**.
5. Selecteer **Vereiste competenties**.
6. Op de pagina **Kenmerken kiezen** zijn de kenmerken die u eerder hebt ingesteld voor de rol Senior projectmanager automatisch geselecteerd. Selecteer **OK**.
7. Voer op de pagina **Rollen toevoegen aan project** in het veld **Aantal resources** de waarde **1** in.
8. In het veld **Resource** geeft de zoekopdracht alle resources weer die de vereiste competenties hebben. Selecteer **Daniel Goldschmidt** en **Maken**.
9. Selecteer op de pagina **Project** de optie **Toevoegen**.
10. Selecteer in het venster **Rollen toevoegen aan het project** in het veld **Rol** de waarde **Teamlid**. Voer in het veld **Aantal resources** de waarde **5** in.
11. Selecteer **Maken**.
12. Selecteer op de pagina **Projecten** de optie **Voorzien in resource**.

## <a name="resource-capacity-synchronization"></a>Capaciteitsynchronisatie voor resource
De processen voor resourcesynchronisatie helpen ervoor te zorgen dat informatie voor de kalender en basiskalender doorvloeien naar de planning van projectresources. Als de kalender wordt gewijzigd, voeren de processen de vereiste updates door bij de planning van projectresources. De processen helpen ook de prestaties te verbeteren, omdat de resourcegegevens van de kalender van tevoren worden gesynchroniseerd. Daarom wordt resourceplanningsinformatie sneller bijgewerkt. Het wordt aangeraden om de processen als batch in te plannen in plaats van een voor een. Anders bestaat het risico dat iemand de inclusieve datums vergeet waarop de informatie voor het laatst is gesynchroniseerd. Als de inclusieve datums niet worden gebruikt, kunnen lacunes optreden tijdens de datumsynchronisatie.

![Kalendersynchronisatie](./media/projectresourcing04-1024x471.jpg)

### <a name="synchronize-resource-capacity-roll-ups"></a>Vergaarde resourcecapaciteit synchroniseren

Het synchronisatieproces is ontworpen om alle resourcekalenderinformatie te synchroniseren. Deze informatie omvat basiskalenderinformatie over de wijzigingen in de tabel met de resourcekalendercapaciteit van het project. Als nieuwe resources aan het project worden toegevoegd, zorgt synchronisatie ervoor dat de bijgewerkte agendagegevens beschikbaar zijn. Deze synchronisatie kan op elk gewenst moment worden uitgevoerd.

Het wordt aangeraden om een batch te gebruiken. De opties zijn beschikbaar tijdens het synchroniseren van capaciteitsreserveringen.

1. Selecteer **Projectbeheer en boekhouding** &gt; **Periodiek** &gt; **Capaciteitsynchronisatie** &gt; **Vergaarde resourcecapaciteit synchroniseren**.
2. Stel de opties in de volgende tabel in.

    | Optie      | Omschrijving |
    |-------------|-------------|
    | Periodecode | Selecteer eventueel de datumintervalcode voor het grootboek om de begin- en einddatums in te stellen voor het synchronisatieproces voor vergaarde resourcecapaciteit. |
    | Begindatum  | Voer de begindatum in voor het synchronisatieproces voor vergaarde resourcecapaciteit. |
    | Einddatum    | Voer de einddatum in voor het synchronisatieproces voor vergaarde resourcecapaciteit. |

[![Synchronisatieproces](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

## <a name="set-up-roles-on-wbs-templates"></a>Rollen configureren op WBS-sjablonen
Projectmanagers kunnen WBS-sjablonen configureren, die ze kunnen toepassen wanneer ze een WBS voor nieuwe projecten maken. Projectmanagers kunnen rollen toevoegen wanneer ze een sjabloon maken. Gebruik de volgende procedure om een rol toe te wijzen aan een WBS-sjabloon. 

1. Selecteer **Projectbeheer en boekhouding** &gt; **Instellen** &gt; **Projecten** &gt; **Structuursjablonen voor werkspecificatie**.
2. Selecteer een WBS-sjabloon en selecteer **Details**.
3. Selecteer een taak in de lijst en selecteer in het veld **Rol** een rol die u aan de taak wilt toewijzen.

### <a name="work-with-a-wbs"></a>Werken met een WBS

U kunt een nieuwe WBS maken, of u kunt een WBS van een bestaande WBS-sjabloon kopiëren. Een projectmanager kan de resources eenvoudig beheren door rollen aan nieuwe taken op de WBS toe te wijzen. Rollen kunnen worden vervangen wanneer een resource is verworven of nadat een bevestigde resource is geïdentificeerd die aan de taak gaat werken. Deze flexibiliteit stelt projectmanagers in staat om de volgende taken uit te voeren:

- Het aantal resources bepalen dat nodig is voor WBS-werkpakketten.
- Projectkosten ramen.
- Een voorlopig budget opstellen.
- De activiteitsduur schatten op basis van rollen en resources.
- Enkele projectbeheersplannen ontwikkelen, op basis van de beschikbare projectgegevens.

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
<td>Voeg automatisch geplande resources toe door rollen te gebruiken die aan een taak zijn gekoppeld. Finance and Operations suggereert automatisch geplande resources door middel van de op rollen gebaseerde beslissingsanalyse met meerdere criteria. Nadat de rollen en de inzet (uren) voor taken in de WBS zijn ingesteld en de structuur is vrijgegeven, selecteert u <strong>Team automatisch genereren</strong>. Het vereiste aantal geplande resources wordt toegevoegd aan de WBS en het tabblad <strong>Projectteam en planning</strong>.</td>
</tr>
<tr class="odd">
<td>Resource (vervolgkeuzelijst)</td>
<td>Op de pagina <strong>Resourcetoewijzing starten</strong> kunt u resources vast of variabel boeken, op basis van de opgegeven tijdsduur. U kunt de weergaveinstellingen aanpassen om de duur van resourceactiviteiten weer te geven en in te stellen. U kunt resources selecteren en toewijzen op het niveau van het werkpakket met de volgende opties:
<ul>
<li><strong>Accepteren</strong> Wijzigingen bevestigen aan de resource die aan een taak is toegewezen.</li>
<li><strong>Annuleren</strong> Wijzigingen annuleren aan de resource die aan een taak is toegewezen.</li>
<li><strong>Automatisch toewijzen:</strong> er wordt automatisch een beschikbare bemande resource met een overeenkomende rol geselecteerd en toegewezen aan de geselecteerde taak.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Op de pagina **Alle projecten** selecteert u het project **XYZ-upgrade Fase 2**.
2. Selecteer **Plan** &gt; **Activiteiten** &gt; **Structuur voor werkspecificatie**.
3. Selecteer **Nieuw** en voeg de volgende activiteiten voor niveau 1 aan de WBS toe:

    - Initiëren
    - Planning
    - In uitvoering
    - Bewaking en controle
    - Sluiten

4. Stel de datums en inzet (uren) in, zoals in de volgende afbeelding.

    [![De datums en inzet instellen](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Selecteer de taakregel **Initiëren** en selecteer in het veld **Rol** de waarde **Senior projectmanager**.
6. Selecteer **Publiceren**.
7. Selecteer op dezelfde regel in het veld **Resource** de naam **Daniel Goldschmidt** en selecteer **Accepteren**.
8. Selecteer de taakregel **Planning** en selecteer in het veld **Rol** de rol **Bedrijfsanalyst**.
9. Selecteer **Publiceren** en **Team automatisch genereren**.
10. Selecteer **Ja** in het dialoogvenster dat wordt geopend.
11. Controleer in het veld **Resource** of de waarde **Bedrijfsanalyst 1** is.
12. Open voor de resource **Bedrijfsanalist 1** de zoekopdracht en selecteer **Formulier voor resourcetoewijzing openen**. Selecteer een werknemer voor de taak.
13. Selecteer **Variabel boeken** &gt; **Volledige capaciteit**.

    > [!NOTE] 
    > U ontvangt geen waarschuwing dat de opgegeven resource nu 2 is, omdat het aantal resources 1 blijft.

14. Valideer op de pagina **Structuur voor werkspecificatie** de resourcetoewijzing voor de WBS en selecteer **Opslaan**.

## <a name="resource-fulfillment-for-planned-resources"></a>Resourcevoorziening voor geplande resources
Een projectmanager kan vereiste resourcerollen voor een project plannen. De resourcemanager ziet deze geplande resources als aanvragen op de pagina **Resourcevervulling** en kan werkelijke resources toewijzen.

1. Op de pagina **Alle projecten** selecteert u het project **XYZ-upgrade Fase 2**.
2. Selecteer **Project** en **Bewerken**.
3. Selecteer op het tabblad **Projectteam en planning** de optie **Toevoegen**.
4. Selecteer in het dialoogvenster **Rollen toevoegen** de rol **Softwareontwikkelaar**.
5. Selecteer **Maken** en sluit de projectpagina.
6. Selecteer op de pagina **Bronafhandeling** de optie **Softwareontwikkelaar 1** voor het project **XYZ-upgrade Fase 2**.
7. Selecteer een werknemer en selecteer **Toewijzen**.
8. Controleer of de regel **Softwareontwikkelaar 1** is verwijderd uit het project **XYZ-upgrade Fase 2**.
9. Controleer op het tabblad **Projectteam en planning** voor het project **XYZ-upgrade Fase 2** of de werknemer die u in de vorige stap hebt geselecteerd, is toegevoegd als **Softwareontwikkelaar**.

## <a name="requests-for-project-resources"></a>Projectresourceaanvragen
De planningsfunctionaliteit voor projectresources biedt resourcemanagers alleen de mogelijkheid om bemande resources te distribueren voor taken of projecten. Als u deze functionaliteit wilt inschakelen, voert u de volgende taken uit of controleert u of ze zijn voltooid:

- Nummerreeksen instellen.
- Workflows voor projectbeheer en boekhouding instellen.
- Workflows voor resourceaanvraag inschakelen.

Nadat u deze taken hebt voltooid, kunt u zo nodig de volgende taken uitvoeren:

- Een resourceaanvraag maken op basis van een variabel geboekte bemande resource.
- Resourceaanvragen bewaken.
- Resourceaanvragen vervullen.
- Een bemande resource aanvragen vanuit een projectstructuur.
- Resources boeken voor een project zonder een aanvraag voor een bemande resource.

## <a name="monitor-project-teams"></a>Projectteams bewaken
1. Selecteer op de pagina **Alle projecten** de koppeling **Project-ID** voor het project **XYZ-upgrade Fase 2**.
2. Controleer op het sneltabblad **Projectteam en planning** of de daar vermelde projectresources correct zijn.

