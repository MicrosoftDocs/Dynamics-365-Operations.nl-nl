---
title: Taakbeheer
description: In dit onderwerp wordt de functie voor taakbeheer uitgelegd die beschikbaar is in Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 12/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 614f37236bbd0239925e37ebf29f59ac006d09cd
ms.sourcegitcommit: 4f84540e6121ca3d5ae52ee07e414116d423cefa
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/03/2022
ms.locfileid: "7948790"
---
# <a name="task-management"></a>Taakbeheer

Met taakbeheer kunt u taken maken die moeten worden voltooid om werknemers aan te nemen (onboard), het dienstverband te beëindigen (offboard) en over te plaatsen (transition). Taakbeheer gebruikt het concept van controlelijsten. Een controlelijst is een lijst met taken voor aannemen, dienstverband beëindigen of overplaatsen. Taakbeheer maakt gebruik van controlelijsten om taken te groeperen en om ze toe te wijzen aan personen of groepen. De controlelijstfunctionaliteit voor aannemen, dienstverband beëindigen en overplaatsen is vergelijkbaar.

## <a name="checklist-overview"></a>Controlelijstoverzicht

Een controlelijst is een groep taken. Controlelijsten bieden u een flexibele manier om taken te groeperen. Deze kunnen opnieuw worden gebruikt (bijvoorbeeld wanneer u extra werknemers aanneemt). U kunt zoveel controlelijsten maken als u nodig hebt en u kunt dezelfde taken aan meerdere controlelijsten toewijzen.

### <a name="examples"></a>Voorbeelden

De volgende voorbeelden laten zien hoe controlelijsten kunnen worden gebruikt bij het aannemen. Aangezien de controlelijstfunctionaliteit voor aannemen, dienstverband beëindigen en overplaatsen echter vergelijkbaar is, is de informatie ook van toepassing op de andere processen.

Als onderdeel van het proces voor het aannemen van werknemers kunnen HR-werknemers taken maken die de voortgang van nieuwe en recent aangenomen werknemers bijhouden. Aangezien het proces voor het aannemen van werknemers kan variëren, afhankelijk van de functie of geografische locatie van de werknemer, kunt u meerdere controlelijsten voor het aannemen maken voor verschillende situaties.

**Voorbeeld 1**

Elke werknemer die in de Verenigde Staten wordt aangenomen, moet taken uitvoeren zoals het invullen van belastingformulieren. Taken zoals het toewijzen van een bedrijfsauto kunnen echter alleen van toepassing zijn op leidinggevend personeel. In dit geval kunnen er twee controlelijsten worden gemaakt: **werknemers in de VS** en **alleen leidinggevenden**. Wanneer er dan in de Verenigde Staten een manager op een lager niveau wordt aangesteld, wordt de controlelijst **werknemers in de VS** geselecteerd. Wanneer er echter een leidinggevende in de Verenigde Staten wordt aangenomen, worden beide controlelijsten geselecteerd om ervoor te zorgen dat alle vereiste aanstellingstaken worden voltooid.

**Voorbeeld 2**

In een bedrijf werken zowel seizoensmedewerkers als normale fulltime werknemers. Hoewel sommige taken (zoals het controleren van de ingangsdatum van de nieuwe werknemer) van toepassing zijn op werknemers van beide typen, zijn sommige extra taken alleen van toepassing op normale fulltime werknemers. In dit geval kunt u twee controlelijsten maken. Beide controlelijsten bevatten de taken die van toepassing zijn op zowel seizoens- als normale fulltime werknemers. Maar slechts in één controlelijst staan de taken die specifiek zijn voor normale fulltime werknemers.

## <a name="task-management-workspace"></a>Werkgebied voor taakbeheer

In de werkruimte **Taakbeheer** worden alle taken vermeld die zijn toegewezen aan personen in de processen voor aannemen, dienstverband beëindigen en overplaatsen. Als u de taken voor een proces wilt weergeven, selecteert u het toepasselijke tabblad in de rechterbovenhoek: **Aannemen**, **Dienstverband beëindigen** of **Overplaatsen**. Standaard hebben alleen HR-professionals toegang tot de werkruimte **Taakbeheer**.

Het tabblad **Aannemen** bevat een lijst **Start binnenkort** met nieuwe werknemers en een lijst **Recente aanstellingen** met recent aangenomen werknemers. In beide lijsten kunt u slechts één werknemer selecteren. Wanneer u een werknemer selecteert, worden alle taken die zijn gerelateerd aan het in dienst nemen van die werknemer aan de rechterkant van de pagina weergegeven. Het tabblad **Aannemen** bevat ook een lijst **Alle taken** met alle taken voor alle nieuwe of recent aangenomen werknemers. Tot slot bevat het een lijst met achterstallige taken en een lijst met taken die aan de huidige gebruiker zijn toegewezen.

Het tabblad **Dienstverband beëindigen** bevat een lijst met werknemers die het bedrijf verlaten en een lijst met werknemers die het bedrijf al hebben verlaten. In beide lijsten kunt u slechts één werknemer selecteren. Wanneer u een werknemer selecteert, worden alle taken die zijn gerelateerd aan het uit dienst gaan van die werknemer weergegeven. Het tabblad **Dienstverband beëindigen** bevat ook een lijst **Alle taken** met alle taken voor werknemers die het bedrijf verlaten of hebben verlaten. Tot slot bevat het een lijst met achterstallige taken en een lijst met taken die aan de huidige gebruiker zijn toegewezen.

Het tabblad **Overplaatsen** bevat een lijst **Alle taken** met alle taken voor alle werknemers die een andere functie krijgen of onlangs hebben gekregen. Ook is er een lijst met achterstallige taken en een lijst met taken die aan de huidige gebruiker zijn toegewezen.

Op alle drie de tabbladen kunnen HR-medewerkers en managers de volgende activiteiten uitvoeren:

- Een controlelijst toepassen op een werknemer.
- De status van een taak bijwerken.
- Een taak opnieuw toewijzen.
- De vervaldatum van een taak bijwerken.

> [!NOTE]
> Het tabblad **Aannemen** bevat standaard medewerkers die in de afgelopen zeven dagen in dienst zijn genomen. Als u deze instelling wilt wijzigen, voert u op de pagina **Human Resources-parameters** op het tabblad **Algemeen** in het veld **Recent aangenomen werknemers** een tijdsbestek in. De gegevens in de lijst **Recent aangenomen werknemers** kunnen worden weergegeven voor een bepaald aantal dagen, maanden of jaren. Als u bijvoorbeeld de lijst wilt weergeven met medewerkers die in de afgelopen 14 dagen zijn aangenomen, stelt u het veld **Periode** in op **14** en stelt u het veld **Eenheid** in op **Dagen**.
>
> Op de pagina **Human resources-parameters** kunt u ook het datumbereik bijwerken voor de lijsten met vertrekkende en vertrokken werknemers die worden weergegeven op het tabblad **Dienstverband beëindigen**.
>
> Deze instellingen zijn ook van toepassing op de werkruimte **Personeelsbeheer**.

## <a name="setting-up-tasks"></a>Taken instellen

U kunt taken afzonderlijk maken en deze vervolgens opnieuw gebruiken in meerdere controlelijsten. Als u een taak wilt maken, selecteert u op de pagina **Instellingen voor aannemen** op het tabblad **Taken** de optie **Nieuw**.

U kunt ook taken rechtstreeks aan een controlelijst toevoegen. Als u een taak wilt toevoegen aan een controlelijst, maakt u op de pagina **Instellingen voor aannemen** op het tabblad **Controlelijst** een nieuwe controlelijst waaraan u de taak toevoegt, of voegt u de taak aan een bestaande controlelijst toe.

> [!NOTE]
> Als u een taak rechtstreeks aan een controlelijst toevoegt, kunt u deze niet opnieuw gebruiken in andere controlelijsten.

In de volgende tabel worden de velden beschreven die beschikbaar zijn wanneer u een taak maakt volgens een van beide methoden.

| Veld           | Description |
|-----------------|-------------|
| Opdracht            | De naam van de taak invoeren. |
| Description     | Een omschrijving van de taak invoeren. |
| Optioneel        | Opgeven of de taak optioneel is en alleen ter informatie is. |
| Taakkoppeling       | De URL van een externe webpagina of een specifieke pagina in de app invoeren waar de gebruiker de taak moet voltooien. Zie [Taakkoppelingen](#task-links) voor meer informatie. |
| Toewijzingstype | Taken kunnen worden toegewezen aan een specifieke werknemer, functie of groep functies, de manager van de betrokken werknemer (dat wil zeggen de werknemer die deel uitmaakt van het proces voor aannemen, dienstverband beëindigen of overplaatsen) of de betrokken werknemer. Het type toewijzing selecteren. Zie [Toewijzingstypen](#assignment-types) voor meer informatie. |
| Toegewezen aan     | Selecteer de specifieke werknemer, functie of groep functies waaraan u de taak wilt toewijzen. |
| Contactpersoon  | De persoon opgeven met wie contact moet worden opgenomen als er vragen zijn over de taak. |
| Offset vervaldatum | Het aantal dagen vóór of na de aanstellings-, beëindigings- of overplaatsingsdatum opgeven dat de taak moet zijn voltooid. Zie de sectie [Vervaldatums van taken en het veld Verschuiving van vervaldatum](#task-due-dates-and-the-due-date-offset-field) voor meer informatie. |
| Instructies    | Instructies voor het voltooien van de taak invoeren. Zie het gedeelte [Instructies](#instructions) voor meer informatie. |

### <a name="task-links"></a>Taakkoppelingen

Een taakkoppeling levert een koppeling naar een externe webpagina of een pagina in de app Dynamics 365. U kunt een taakkoppeling opgeven als de persoon die aan een taak is toegewezen, naar een specifieke webpagina of een specifieke pagina in de app Dynamics 365 moet gaan om die taak te voltooien. Wanneer u een taakkoppeling maakt, kunt u een van de volgende opties selecteren:

- **Menu-item:** als u deze optie selecteert, wordt een lijst met alle pagina's in de app Dynamics 365 weergegeven. Selecteer een pagina in de lijst.
- **URL** – Als u deze optie selecteert, voert u de URL van de webpagina in waarnaar de persoon moet gaan die aan de taak is toegewezen. De opgegeven pagina kan een pagina zijn die geen deel uitmaakt van de app Dynamics 365.
- **Werknemerdetails** – Als u deze optie selecteert, selecteert u een van de volgende opties:

    - **Self-serviceacties voor werknemers** – Deze optie toont een lijst met pagina's die beschikbaar zijn in **Self-service voor werknemers**. Gebruik deze als de taak die is toegewezen aan de in dienst genomen werknemer moet worden voltooid in **Self-service voor werknemers**. Als u bijvoorbeeld wilt dat de werknemer zijn of haar persoonlijke contactgegevens invoert, selecteert u **Self-service acties voor werknemers** en selecteert u vervolgens **Persoonlijke details&gt;Persoonlijke informatie**.
    - **Acties voor werknemersbeheer** – Deze optie toont een lijst met pagina's die betrekking hebben op de record van de werknemer, maar die niet toegankelijk zijn voor de werknemer. Als u bijvoorbeeld wilt dat de eigenaar van de taak specifieke informatie voor een in dienst genomen werknemer invoert, zoals compensatiegegevens, selecteert u **Werknemersbeheeracties** en selecteert u vervolgens **Compensatie&gt;Vaste compensatie**.

### <a name="assignment-types"></a>Toewijzingstypen

Wanneer een werknemer wordt aangenomen, uit dienst gaat of wordt overgeplaatst, kunnen er een of meer controlelijsten worden geselecteerd. Nadat een controlelijst is geselecteerd en het aanstellings-, beëindigings- of overplaatsingsproces is voltooid, worden taken gemaakt en toegewezen aan gebruikers om de voortgang bij te houden.

Wanneer een taak is gemaakt, wordt deze toegewezen aan een specifieke gebruiker. Aan welke gebruiker een taak wordt toegewezen, is afhankelijk van het toewijzingstype dat voor die taak is geselecteerd. De volgende waarden zijn beschikbaar in het veld **Toewijzingstype**:

- **Medewerker** – De taak toewijzen aan een specifieke medewerker. Nadat u deze waarde hebt geselecteerd, selecteert u de medewerker in het veld **Toegewezen aan**.
- **Functie** – De taak toewijzen aan een specifieke functie. Nadat u deze waarde hebt geselecteerd, selecteert u de functie in het veld **Toegewezen aan**.

    Een IT-engineer is bijvoorbeeld altijd verantwoordelijk voor de voorbereiding van een laptop voor een nieuwe werknemer. In dat geval selecteert u bij het maken van de taak voor de configuratie van een laptop **Functie** als toewijzingstype en selecteert u **IT-engineer** als functie. Wanneer vervolgens een werknemer wordt aangenomen en de controlelijst wordt toegewezen, wordt de laptopconfiguratietaak toegewezen aan de werknemer met de functie IT-engineer op het moment dat de aanstellingsactie wordt ingevoerd.

- **Groep** – Wijs de taak toe aan een groep functies (toewijzingsgroep). Nadat u deze waarde hebt geselecteerd, selecteert u de groep in het veld **Toegewezen aan**. Zie [Toewijzingsgroepen instellen (optioneel)](#setting-up-assignment-groups-optional) voor meer informatie.
- **Manager** – Wijs de taak toe aan de manager van de werknemer die wordt aangesteld, uit dienst gaat of wordt overgeplaatst.

    > [!IMPORTANT]
    > Wanneer een controlelijst wordt toegepast en er op dit moment geen functie is toegewezen aan de werknemer die wordt aangesteld, uit dienst gaat of wordt overgeplaatst, kan de manager niet worden bepaald. In dit geval wordt de taak toegewezen aan de eigenaar van de controlelijst. Zie [Controlelijsten instellen](#setting-up-checklists) voor meer informatie.

- **Werknemer** - wijs de werknemer toe die wordt aangenomen, uit dienst gaat of wordt overgeplaatst.

### <a name="task-due-dates-and-the-due-date-offset-field"></a>Vervaldatums van taken en het veld Verschuiving van vervaldatum

Vervaldatums van taken zijn gebaseerd op de begindatum van het dienstverband, de beëindigingsdatum of de overplaatsingsdatum. Sommige taken moeten vóór de begindatum van een werknemer worden voltooid, terwijl andere taken later kunnen worden voltooid. Wanneer u een taak definieert, stelt u het veld **Verschuiving van vervaldatum** in om een vervaldatum op te geven ten opzichte van de begindatum, beëindigingsdatum of datum van overplaatsing. Een IT-engineer moet bijvoorbeeld twee dagen voor de begindatum van de werknemer een laptop voor de nieuwe werknemer voorbereiden. Wanneer u in dat geval de configuratietaak 'laptop' maakt, stelt u het veld **Verschuiving voor vervaldatum** in op **-2**. Als de begindatum van een werknemer dan 5 mei is, moet de taak op 3 mei zijn uitgevoerd.

> [!NOTE]
> Vervaldatums kunnen worden aangepast nadat de taak is gemaakt.

Vervaldatums worden berekend op basis van de kalender die aan de controlelijst is gekoppeld. Zie [Controlelijsten instellen](#setting-up-checklists) voor meer informatie.

### <a name="instructions"></a>Instructies

Complexe taken vereisen mogelijk meerdere stappen of de persoon die de taak uitvoert moet mogelijk extra informatie opgeven. U kunt in het veld **Instructies** instructies of extra informatie invoeren om de persoon te helpen die de taak moet voltooien.

## <a name="setting-up-checklists"></a>Controlelijsten instellen

Een controlelijst is een groep taken. U kunt zoveel controlelijsten maken als u nodig hebt en u kunt dezelfde taken aan meerdere controlelijsten toewijzen. Wanneer u een controlelijst maakt, geeft u een eigenaar en een kalender op.

Als het veld **Toewijzingstype** voor een taak is ingesteld op **Functie**, **Manager** of **Groep** maar er geen specifieke persoon kan worden afgeleid van het toewijzingstype, wordt de taak toegewezen aan de eigenaar van de controlelijst. Hieronder vindt u enkele voorbeelden van situaties waarin taken worden toegewezen aan de eigenaar van de controlelijst:

- Er is geen functie toegewezen aan de werknemer die wordt aangenomen of uit dienst gaat. Omdat de werknemer geen functietoewijzing heeft, kan de manager niet worden bepaald.
- Het veld **Toewijzingstype** wordt ingesteld op **Functie**, maar er is geen werknemer aan de functie toegewezen op het moment dat de taak wordt gemaakt. De taak **Laptop instellen** wordt bijvoorbeeld toegewezen aan functienummer 000876 (**Technical Support Specialist**). Op het moment dat een werknemer in dienst wordt genomen, is geen werknemer toegewezen aan de functie 000876. Daarom wordt een taak gemaakt voor de eigenaar van de controlelijst.
- Het veld **Toewijzingstype** wordt ingesteld op **Groep**, maar er is geen werknemer aan de functies in de groep toegewezen op het moment dat de taak wordt gemaakt.

De kalender die voor een controlelijst is opgegeven, wordt gebruikt om de vervaldatum van taken te berekenen die deel uitmaken van die controlelijst. In de kalender-instellingen worden werk- en niet-werkdagen gedefinieerd. Werkdagen worden opgenomen wanneer de vervaldatum van taken wordt berekend en niet-werkdagen worden uitgesloten. Niet-werkdagen zijn weekends en vakanties. 

Nadat een kalender is ingesteld, is deze gekoppeld aan een controlelijstsjabloon. Op die manier wordt de vervaldatum van elke taak in de controlelijst op dezelfde manier berekend. U kunt meerdere kalenders instellen, maar aan elke controlelijst kan slechts één kalender worden gekoppeld.

## <a name="setting-up-assignment-groups-optional"></a>Toewijzingsgroepen instellen (optioneel)

Soms is een groep personen verantwoordelijk voor een taak. Een groep IT-medewerkers kan bijvoorbeeld verantwoordelijk zijn voor de voorbereiding van laptops voor nieuw personeel.

Ga als volgt te werk om een toewijzingsgroep in te stellen.

1. Selecteer op de pagina **Groepstoewijzing** de optie **Nieuw**.
1. Voer een naam (bijv. **Laptop IT**) en een beschrijving voor de groep in.
1. Selecteer **Opslaan**.
1. Selecteer op het sneltabblad **Leden** de optie **Toevoegen**.
1. Selecteer in het veld **Functies** alle functies die verantwoordelijk zijn voor de taak.

Nadat u een toewijzingsgroep hebt gemaakt, kunt u deze selecteren wanneer er een taak wordt gemaakt. Als u een specifieke groep voor een taak wilt selecteren, moet u **Groep** selecteren in het **toewijzingstype**. De groep die u hebt gemaakt, kan vervolgens worden geselecteerd in het veld **Toegewezen aan**.

> [!IMPORTANT]
> Als een taak wordt toegewezen aan een groep, wordt de taak gemarkeerd als **Voltooid** wanneer een persoon in de groep deze voltooit. Taken worden gemaakt bij het aannemen, beëindigen of overplaatsen. Ze worden gemaakt voor de gebruikers die zijn toegewezen aan de functies die in de groep zijn opgenomen.

## <a name="setting-up-task-groups-optional"></a>Taakgroepen instellen (optioneel)

Een proces voor aannemen, dienstverband beëindigen of overplaatsen kan veel taken omvatten. Om het eenvoudiger te maken om alle vereiste taken aan een controlelijst toe te wijzen, kunt u optionele taakgroepen maken om verwante taken te categoriseren. Zo moeten de afdelingen HR, IT en Salarisadministratie elk specifieke taken uitvoeren om een nieuwe werknemer aan te stellen. Daarom maakt u de volgende taakgroepen: **HR**, **IT** en **Salaris**. Wanneer u vervolgens een taak maakt, kunt u een van deze taakgroepen koppelen.

Als u een taak wilt toevoegen aan een controlelijst, kunt u de lijst met taken filteren op de taakgroep waaraan de gewenste taak is toegewezen. Wanneer u bijvoorbeeld een controlelijstsjabloon maakt, kunt u de lijst filteren zodat alleen de IT-taken worden weergegeven die aan de **IT**-taakgroep zijn toegewezen. U kunt er daarom voor zorgen dat alleen de relevante IT-taken worden geselecteerd.

## <a name="using-checklists"></a>Controlelijsten gebruiken

Wanneer een medewerker wordt aangenomen, uit dienst gaat of wordt overgeplaatst, kunnen er een of meer controlelijsten worden geselecteerd. Vervaldatums voor taken en werknemertoewijzingen worden gemaakt nadat het wervings-, beëindigings- of overplaatsingsproces is voltooid. Als u bijvoorbeeld de knop **Aanstelling** of **Aanstelling en details toevoegen** selecteert, worden taken voor personen gemaakt op basis van het toewijzingstype.

Aan elke taak wordt een vervaldatum toegewezen door de verschuiving voor de vervaldatum op te tellen of af te trekken van de begindatum van de werknemer. Zie de sectie [Vervaldatums van taken en het veld Verschuiving van vervaldatum](#task-due-dates-and-the-due-date-offset-field) voor meer informatie.

Als u personeelsacties gebruikt, worden de taken gemaakt wanneer de knop **Voltooien** wordt geselecteerd of de actie wordt goedgekeurd.

In het werkgebied **Taakbeheer** kunt u een controlelijst toepassen op een werknemer door de werknemer op de eenvoudige lijstpagina of op de detailpagina te selecteren en vervolgens **Controlelijst toepassen** te selecteren. De waarde van het veld **Doeldatum** wordt gebruikt om de vervaldatum van de taken te berekenen. Normaal gesproken moet de doeldatum overeenkomen met de datum waarop de werknemer wordt aangenomen, het dienstverband wordt beëindigd of de overplaatsing.

U kunt een controlelijst ook toepassen op een werknemer door de pagina **Werknemer** te openen en **Controlelijsten** in het menu te selecteren.

## <a name="completing-tasks"></a>Taken voltooien

Op de pagina **Self-service medewerkers** kan een werknemer alle taken bekijken die aan hen zijn toegewezen. Voor elke toegewezen taak worden de waarden **Taak**, **Omschrijving**, **Instructies** en **Contactpersoon** weergegeven. Daarnaast kan de werknemer voor elke taak de bijbehorende externe webpagina of de bijbehorende pagina in de app Dynamics 365 openen.

Taken kunnen worden gemarkeerd als **In uitvoering**, **Geannuleerd** of **Voltooid**. Als een taak is toegewezen aan een groep, wordt de taak gemarkeerd als **Voltooid** wanneer een persoon in de groep deze voltooit.

Taken kunnen ook opnieuw worden toegewezen.
