---
title: Overzicht budgetplanning
description: Dit artikel is een introductie tot budgetplanning en bevat informatie waarmee u budgetplanning kunt configureren en budgetplanningprocessen kunt instellen.
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
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: d5073958f8ffe90e47dc10cde67e081420e559a1
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-overview"></a>Overzicht budgetplanning

Dit artikel is een introductie tot budgetplanning en bevat informatie waarmee u budgetplanning kunt configureren en budgetplanningprocessen kunt instellen.

<a name="overview-of-budget-planning"></a>Overzicht van budgetplanning
---------------------------

U voert budgetplanning uit wanneer u de budgetten voorbereidt die door een organisatie worden geïmplementeerd. Een organisatie kan budgetplanning configureren en vervolgens budgetplanningsprocessen instellen om te voldoen aan de bijbehorende beleidsregels, procedures en vereisten voor budgetvoorbereiding. 

Als u begrijpt concepten en terminologie die in Microsoft Dynamics 365 worden gebruikt voor bewerkingen, worden deze gemakkelijker kunt implementeren in uw organisatie plannen van budgetten.

### <a name="key-terms"></a>Belangrijke termen

-   **Budgetplanningsprocessen**: met budgetplanningsprocessen wordt bepaald hoe budgetplannen kunnen worden bijgewerkt, doorgestuurd, beoordeeld en goedgekeurd in de budgetorganisatiehiërarchie. Een budgetplanningsproces wordt gekoppeld aan een budgetcyclus en een organisatie via een rechtspersoon.
-   **Budgetplannen**: de budgetplannen bevatten de budgetgegevens voor een budgetcyclus. U kunt meerdere budgetplannen hebben die voor verschillende doeleinden worden gebruikt. Budgetplannen kunnen bijvoorbeeld worden gebruikt om budgetbedragen te maken voor verschillende organisatie-eenheden of ze kunnen u helpen bij het maken van vergelijkingen en weloverwogen beslissingen.
-   **Budgetplanscenario´s**: met de budgetplanscenario's worden categorieën gegevens gedefinieerd voor de budgetplannen. U definieert budgetplanscenario's ter ondersteuning van klassen van monetaire eenheden en andere maateenheden, zoals hoeveelheid. Voorbeelden van monetaire budgetplanscenario's zijn Afdeling vorig jaar en Afdelingsaanvragen. Voorbeelden van budgetplanscenario´s waarin hoeveelheden worden gebruikt, zijn Ondersteuningsaanvragen vorig jaar en Aantal FTE´s.
-   **Budgetplanningsfasen**: met de budgetplanningsfasen worden de stappen gedefinieerd die een budgetplan volgt vanaf het prille begin tot de definitieve goedkeuring. Budgetplanningsfasen worden gerangschikt in budgetplanningwerkstromen.
-   **Budgetplanningsworkflows**: budgetplanningsworkflows bestaan uit budgetplanningsfasen en de budgetplanningsfasen worden gedefinieerd met de budgetplanningsworkflows. Budgetplanningsworkflows worden gekoppeld aan budgetteringsworkflows. Budgetteringsworkflows zijn de geautomatiseerde en handmatige processen waarmee budgetplannen door de budgetplanningsfasen worden verplaatst.

[![budget plannen terminologie](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="common-tasks"></a>Algemene taken

U kunt budgetplanning gebruiken om de volgende taken uit te voeren:

-   Budgetplannen maken om de verwachte opbrengsten en uitgaven voor een budgetcyclus te definiëren.
-   Analyseren en bijwerken van budgetplannen voor meerdere scenario's.
-   De budgetplannen automatisch doorsturen samen met werkbladen, verantwoordingsdocumenten en andere bijlagen voor beoordeling en goedkeuring.
-   Meerdere budgetplannen van een lager niveau van de organisatie samenvoegen in één bovenliggend budgetplan op een hoger niveau van de organisatie. U kunt ook een enkel budgetplan ontwikkelen op een hoger niveau in de organisatie en de budgetten toewijzen aan lagere niveaus van de organisatie.

Budgetplanning is geïntegreerd met andere Microsoft Dynamics 365 voor bewerkingen modules. Zo kunt u informatie van vorige budgetten, werkelijke uitgaven, vaste activa en Human Resources gebruiken. Omdat budgetplanning ook is geïntegreerd met Microsoft Excel en Microsoft Word, kunt u deze programma's gebruiken om met budgetplanningsgegevens te werken. Een budgetbeheerder kan bijvoorbeeld de budgetaanvraag van een afdeling importeren vanuit een budgetplanscenario in een Excel-werkblad. De gegevens kunnen worden geanalyseerd, bijgewerkt en uitgezet in het werkblad en vervolgens terug naar de budgetplanregels worden gepubliceerd.

## <a name="configuring-budget-planning"></a>Budgetplanning configureren
De pagina **Budgetplanningsconfiguratie** bevat de meeste instellingen die u nodig hebt om budgetplanning in te stellen. In de volgende secties wordt een aantal belangrijke factoren beschreven waarmee u rekening dient te houden wanneer u budgetplanning configureert. Nadat u de configuratie hebt voltooid, stelt u budgetplanningsprocessen in.

### <a name="create-a-budget-planning-schema"></a>Een budgetplanningsschema maken

Een optionele maar aanbevolen eerste stap bestaat eruit een schema te maken waarin de procedure van uw organisatie wordt weergegeven voor het formuleren van een budget. U kunt elke gewenste methode gebruiken om dit schema te maken. In de volgende afbeelding wordt een generiek voorbeeld weergegeven, waarin afzonderlijke budgetplanningsworkflows worden gemaakt voor verschillende niveaus van de organisatie. Fasen worden gedefinieerd in elke workflow en specifieke scenario's worden toegewezen aan elke fase om de budgetgegevens te bewaren. Taken worden uitgevoerd om de gegevens van de ene fase naar de volgende fase te verplaatsen. Bedragen kunnen bijvoorbeeld aan verschillende rekeningen, goedkeuringen of andere beoordelingen worden toegewezen of ermee samengevoegd. In dit voorbeeld wordt met de cursieve tekst een scenario aangegeven dat niet kan worden bewerkt tijdens de fase, of historische gegevens of gegevens die zijn goedgekeurd in een eerdere fase en daarom niet kunnen worden gewijzigd. 

[![budget plannen algemene schema](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

In het volgende voorbeeld wordt het hoofdkantoor maakt een schatting van de oorspronkelijke budgetbedragen voor de basislijn en verdeeld naar de verkoopafdelingen zijn opgenomen. De verkoopafdelingen maken vervolgens een raming en dienen hun prognose weer in bij het hoofdkantoor, waar de budgetmanager de prognose samenvoegt en corrigeert. Tot slot verzendt de budgetmanager gecorrigeerde budgetbedragen naar de CFO voor controle, laatste correcties en goedkeuring. 

[![budget plannen schema-voorbeeld](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

###  <a name="organization-hierarchy-for-budget-planning"></a>Organisatiehiërarchie voor budgetplanning

Op de pagina **Organisatiehiërarchie** kunt u een organisatiehiërarchie toewijzen als een budgetplanningshiërarchie voor elk budgetplanningsproces. De budgetplanningshiërarchie hoeft niet overeen te komen met de standaardorganisatiehiërarchie die wordt gebruikt voor andere doeleinden. Omdat deze hiërarchie wordt gebruikt om gegevens samen te voegen en te distribueren, kunt u deze wellicht een andere structuur geven. In het voorbeeldschema bevinden de verkoopafdelingen zich onder een hoofdkantoorniveau dat budget- en financiële afdelingen bevat. Deze structuur verschilt waarschijnlijk van de structuur die wordt gebruikt om bewerkingen voor de verkoopafdelingen te beheren. Slechts één organisatiehiërarchie kan worden toegewezen aan elk budgetplanningsproces. 

Zie [Organisaties en organisatiehiërarchieën](/dynamics365/operations/organization-administration/organizations-organizational-hierarchies) voor meer informatie.

### <a name="user-security"></a>Gebruikersbeveiliging

Budgetplanning kan een van de twee beveiligingsmodellen volgen om gebruikermachtigingen te definiëren. Als u het beveiligingsmodel wilt opgeven, stelt u een budgetplanningsparameter in op de pagina **Budgetplanningsconfiguratie**.

### <a name="budget-planning-workflows-stages"></a>Workflowfasen van budgetplanning

Budgetplanningsworkflows worden gebruikt in combinatie met budgetteringsworkflows om het maken en ontwikkelen van budgetplannen te beheren.

Een budgetplanningwerkstroom bestaat uit een geordende reeks fasen die een budgetplan doorloopt. Elke budgetplanningsworkflow wordt gekoppeld aan een budgetteringsworkflow. Budgetteringsworkflows zijn een van de types workflow die overal in Microsoft Dynamics 365 worden gebruikt voor bewerkingen. Met de budgetteringsworkflow worden de budgetplannen samen met de werkbladen, verantwoordingsdocumenten en bijlagen door de hele organisatie doorgestuurd voor beoordeling en goedkeuring. 

U maakt de budgetplanningsworkflow in de sectie **Workflowfasen** van de pagina **Budgetplanningsconfiguratie**. Daar kunt u de fasen en de budgetteringsworkflow selecteren die worden gebruikt en ook kunt u extra instellingen configureren. 

Het is een goed idee om een budgetplanningsworkflow voor elk niveau van een budgetteringshiërarchie maken. U wijst vervolgens een budgetteringsworkflow toe die elementen bevat die overeenkomen met de fasen in de budgetplanningsworkflow. In het voorbeeldschema eerder in dit artikel wordt een budgetplanningsworkflow gemaakt voor de verkoopafdelingen, wordt een andere budgetplanningsworkflow gemaakt voor het hoofdkantoor. Met een budgetteringsworkflow worden de budgetplannen door de fasen verplaatst. 

U maakt de budgetteringsworkflow voor budgetplanning op de pagina **Budgetteringsworkflows**. Het proces lijkt op het proces voor het maken van andere werkstromen in Microsoft Dynamics 365 voor bewerkingen. In de volgende afbeelding ziet u een voorbeeld van een hoofdkantoorworkflow. 

[![budgetteringsworkflow opzetten voor budgetplanning](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

De workflow bevat elementen voor toewijzing aan verkoopafdelingen en samenvoeging van hun bijdragen, de controle door de budgetmanager, de goedkeuring door de financieel Directeur en fase-overgangen tussen elke fase. 

U wijst de budgetteringsworkflow aan elke budgetplanningsworkflow in de sectie **Workflowfasen** van de pagina **Budgetplanningsconfiguratie** toe.

### <a name="parameters-scenarios-and-stages"></a>Parameters, scenario's en fasen

Met de oorspronkelijke instellingen op de pagina **Budgetplanningsconfiguratie** kunt u een aantal bouwstenen maken voor latere configuratiestappen:

-   **Parameters**: met parameters worden de beveiligingregels gedefinieerd die u wilt toepassen op budgetplannen en de financiële standaarddimensies die moeten worden gebruikt wanneer gebruikers inzoomen op de bedragen van budgetplanscenario´s.
-   **Scenario's**: de scenario's omvatten de categorieën gegevens die u voor de budgetplannen wilt. U definieert budgetplanscenario's ter ondersteuning van klassen van monetaire eenheden en andere maateenheden, zoals hoeveelheid. In een budgetplan wordt met scenario's één versie van budgetplanningsgegevens voorgesteld. Voorbeelden van monetaire budgetplanscenario's zijn Verkoop vorig jaar en Ondertekende contracten. Voorbeelden van scenario's waarin hoeveelheden worden gebruikt, zijn Aantal verkoopgesprekken en Aantal FTE´s.
-   **Fasen**: met fasen worden de stappen bepaald die een budgetplan volgt vanaf het prille begin tot de definitieve goedkeuring. Voorbeelden van budgetplanningsfasen zijn HQ-rollup, CFO-controle en Definitief.

### <a name="allocation-schedules"></a>Toewijzingsschema's

In budgetplanning kunt u de bedragen of hoeveelheden op budgetplanregels van een bepaald scenario aan een ander scenario of zelfs aan hetzelfde scenario toewijzen. U kunt bijvoorbeeld toewijzen aan hetzelfde scenario als u wijzigingen op de financiële dimensies of de datums van de bedragen in dat scenario wilt toepassen. Een toewijzing kan plaatsvinden in een budgetplan of vanuit een budgetplan aan een ander budgetplan. 

Met toewijzingsschema´s worden budgetplanregels automatisch toegewezen tijdens workflowverwerking. U kunt toewijzingen uitvoeren met behulp van een van de volgende methoden in de lijst **Toewijzingsmethode**:

-   **Toewijzen aan perioden**: u gebruikt een periodetoewijzingssleutel om de budgetplanregels toe te wijzen vanuit het bronbudgetplanscenario aan perioden in het doelscenario. **opmerking:** voordat u over perioden toewijzen kunt, moet u instellen periodetoewijzingssleutels op de *** periodetoewijzing categorieën *** pagina.
-   **Toewijzen aan dimensies**: de budgetplanregels worden toegewezen vanuit het bronbudgetplanscenario aan de financiële dimensies in het doelscenario. **opmerking:** voordat u dimensies toewijzen kunt, moet u instellen budgettoewijzingstermijnen op de *** budget toewijzing voorwaarden *** pagina.
-   **Samenvoegen**: de budgetplanregels worden samengevoegd vanuit het bronbudgetplanscenario in de gekoppelde budgetplannen met het doelscenario in het bovenliggende budgetplan.
-   **Verdelen**: de budgetplanregels worden verdeeld vanuit het budgetplanscenario in het bovenliggende budgetplan naar het doelscenario in de gekoppelde budgetplannen.
-   **Grootboektoewijzingsregels gebruiken**: de budgetplanregels worden verdeeld vanuit het bronbudgetplanscenario naar het doelscenario op basis van de grootboektoewijzingsregel die is geselecteerd.
-   **Kopie van budgetplan**: u kunt een ander budgetplan selecteren dat u als bron van de toewijzing wilt gebruiken.

### <a name="stage-allocations"></a>Fasetoewijzingen

Fasetoewijzingen worden gebruikt om budgetplanregels automatisch toe te wijzen tijdens workflowverwerking. Wanneer fasetoewijzingen worden geb ruikt, kunnen budgetplanregels in het doelscenario worden gemaakt en gewijzigd zonder interventie van de voorbereider of de controleur van het budgetplan.

Wanneer u een fasetoewijzing instelt, koppelt u de budgetplanningswerkstroom en de fase met de toewijzingsplanning. De budgetplanningswerkstroom moet worden gekoppeld aan een budgetteringsworkflow waarbij de *** budgetplanningsproces fase toewijzing *** geautomatiseerde workflowtaak. Wanneer de workflow de opgegeven fase bereikt, wordt de toewijzing automatisch uitgevoerd. Deze geautomatiseerde taak kan worden gebruikt om budgetregels te maken in een nieuw scenario. 

In het voorbeeldschema eerder in dit artikel, wordt een toewijzing uitgevoerd om bedragen van een budgetplan en scenario's in de hoofdkantoorbasisfase over te boeken naar een ander budgetplan en scenario's en in de ramingsfase van een verkoopafdeling. In de volgende afbeelding ziet u de relevante sectie van het voorbeeldschema.

[![Fasetoewijzing](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

In het voorbeeldschema wordt een samenvoeging bovendien naar een bovenliggend plan in het werkgebied HQ Rollup verleend van budgetplannen en scenario's op de verkoopafdeling ingediend fase. In de volgende afbeelding ziet u de relevante sectie van het voorbeeldschema.

[![Aggregation](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Prioriteiten

U kunt budgetplanprioriteiten eventueel gebruiken om categorieën en doelstellingen te definiëren voor de budgetplannen die u hebt ingesteld. U kunt prioriteiten ook gebruiken voor het ordenen, indelen en evalueren van verschillende budgetplannen. U kunt bijvoorbeeld een budgetplanningsprioriteit maken voor gezondheid en veiligheid en vervolgens budgetplannen evalueren die zijn toegewezen aan die prioriteit. U kunt ook een nummer toewijzen om budgetplannen te rangschikken over alle budgetplannen.

### <a name="columns-and-layouts"></a>Kolommen en indelingen

Budgetcijfers worden in een budgetplan weergegeven in rijen en kolommen. U moet eerst de kolommen definiëren en vervolgens kunt u een indeling maken om de weergave van de kolommen te definiëren. 

Als u een kolom wilt definiëren, selecteert u een budgetplanscenario. De regelbedragen van dat scenario worden weergegeven in het budgetplan. U kunt een periode selecteren om het bedrag te filteren en u kunt ook filters toepassen die zijn gebaseerd op de grootboekrekening. 

Wanneer u een indeling definieert, selecteert u een grootboekdimensie die is ingesteld om de budgetplanrijen te maken die u wilt weergeven en selecteer de kolommen als indelingselementen. U kunt meerdere indelingen maken, zodat een budgetplan de gegevens bevat die u in verschillende fasen van het budgetplanningsproces wilt. 

Naast kolommen voor budgetbedragen kunt u kolommen definiëren voor de velden voor project, voorgesteld project, activum en voorgesteld activum van het budgetplan. U kunt een kolom ook voor gebudgetteerde posities definiëren. Deze optie is heel handig wanneer u personeelsbudgetten moet analyseren. 

Voor het voorbeeldschema kunt u kolommen maken voor Verkoop vorig jaar, Contracten en Prognosescenario's (in de volgende afbeelding ziet u de relevante sectie van het schema). U kunt vervolgens één scenario of al deze scenario's in afzonderlijke kolommen opdelen voor elk kwartaal van het boekjaar, zodat de manager van de verkoopafdeling nauwkeurig prognosebedragen voor elke periode kan invoeren.

[![Columns](./media/columns.png)](./media/columns.png) 

U ook opgeven of elk element indeling (kolom) kan worden bewerkt, en of deze is beschikbaar in een werkbladsjabloon die u voor deze indeling is gemaakt. Voor het voorbeeldschema zijn in de indeling die voor de ramingsfase wordt gebruikt, de prognosekolommen bewerkbaar, terwijl de kolommen Verkoop vorig jaar en Contracten alleen-lezen zijn.

### <a name="templates"></a>Sjablonen

In de sectie **Indelingen** van de pagina **Budgetplanningsconfiguratie** kunt u ook Excel-sjablonen genereren, weergeven of uploaden. Deze sjablonen zijn de werkmappen die aan elk budgetplan worden gekoppeld om aanvullende analyse, grafieken en gegevensinvoermogelijkheden te verschaffen. 

U kunt een sjabloon voor elke indeling genereren, weergeven of uploaden. Wanneer een sjabloon wordt gegenereerd, wordt de indeling vergrendeld en kan deze niet worden bewerkt. Door deze vergrendeling wordt gewaarborgd dat de sjabloonindeling overeenkomt met de indeling van het budgetplan en dezelfde gegevens bevat. Nadat een sjabloon is gegenereerd, kan deze worden weergegeven en bewerkt. U kunt bijvoorbeeld grafieken toevoegen aan de sjabloon of de weergave ervan verder aanpassen.

> [!NOTE] 
> De sjabloon moet worden opgeslagen naar een locatie die de gebruiker toegang heeft, zodat deze kan worden geüpload naar de indeling nadat de bewerking is voltooid. Op die manier wordt de sjabloon gebruikt met budgetplannen waarin de indeling wordt gebruikt.

### <a name="descriptions"></a>Beschrijvingen

De omschrijvingen die u in de sectie **Indelingen** kunt toewijzen, worden gebruikt om de naam van een financiële dimensie weer te geven die in een indeling is opgenomen. Een organisatie kan bijvoorbeeld de naam van de hoofdrekening weergeven naast het hoofdrekeningnummer in een budgetplan, maar wil de namen van andere financiële dimensies weglaten om te voorkomen dat de weergave te vol is.

## <a name="setting-up-budget-planning-processes"></a>Budgetplanningsprocessen instellen

Wanneer u klaar bent met het configureren van de budgetplanning, kunt u budgetplanningsprocessen instellen op de pagina **Budgetplanningsproces**. Budgetplanningsprocessen zij regelsets waarmee wordt bepaald hoe budgetplannen kunnen worden bijgewerkt, doorgestuurd, beoordeeld en goedgekeurd in de budgetorganisatiehiërarchie. 

Voor elk budgetplanningsproces selecteert u eerst een budgetcyclus en een grootboek. Elk budgetplanningsproces is gerelateerd aan slechts één budgetcyclus en één grootboek. Selecteer vervolgens de budgetorganisatiehiërarchie op het sneltabblad **Administratie budgetplanningsproces** en wijs een budgetplanningsworkflow toe aan alle divisies binnen de organisatie die worden weergegeven in het raster. 

Als u de budgetplanningsworkflow voor soortgelijke divisies wilt toewijzen of wijzigen, klikt u op **Workflow toewijzen** en selecteert u vervolgens het gewenste organisatietype en de budgetplanningsworkflow die u wilt gebruiken. De budgetteringsworkflow-ID die is gekoppeld aan elke budgetplanningsworkflow wordt automatisch toegevoegd aan het raster. 

Wanneer u de faseregels en sjablonen definieert op het sneltabblad **Faseregels en indelingen van budgetplanning** kunt u een andere set regels en standaardsjablonen definiëren voor elke budgetplanningsfase. In de ramingsfase van de verkoopafdeling kan gebruikers bijvoorbeeld worden toegestaan de regels in een budgetplan te wijzigen, maar niet om regels toe te voegen. In de indieningsfase kan gebruikers worden toegestaan regels weer te geven, maar niet om regels te wijzigen of toe te voegen, omdat het werk in die fase is voltooid en wijzigingen in de budgetplannen moeten worden voorkomen. Als u de indelingen wilt selecteren die voor budgetplannen beschikbaar zijn, klikt u op **Alternatieve indelingen**. 

U kunt desgewenst budgetplanningsprioriteiten selecteren op het sneltabblad **Prioriteitsbeperkingen budgetplan**. Prioriteiten kunnen vervolgens worden geselecteerd in budgetplannen. 

De laatste stap is het budgetplanningsproces te activeren via het menu **Acties**. Een budgetplanningsproces kan pas worden gebruikt als het is geactiveerd. 

In het menu **Acties** kunt u ook een nieuw proces maken door een bestaand proces te kopiëren. Deze functie is handig voor organisaties die dezelfde processtroom voor elke budgetcyclus volgen en weinig tot geen wijzigingen aanbrengen. 

Een andere nuttige opdracht in het menu **Acties** is **Budgetprocesstatus weergeven**. Met deze opdracht worden de budgetplannen in een proces grafisch weergegeven, samen met relevante gegevens, zoals de workflowstatus van de plannen, overzichten per bedrag en per eenheid en navigatie naar de budgetplannen zelf via één keer klikken.

[![Budget planning process status](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)


