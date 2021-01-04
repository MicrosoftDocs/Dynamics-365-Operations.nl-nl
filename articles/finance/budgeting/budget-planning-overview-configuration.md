---
title: Overzicht van Budgetplanning
description: In dit onderwerp wordt budgetplanning beschreven. Het bevat informatie waarmee u budgetplanning kunt configureren en budgetplanningprocessen kunt instellen.
author: ryansandness
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17251
ms.assetid: a2e06633-a800-4840-a962-88fed8462104
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3744fd823576b597b4550008338e3cc96cb585d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442088"
---
# <a name="budget-planning-overview"></a>Overzicht van Budgetplanning

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt budgetplanning beschreven. Het bevat informatie waarmee u budgetplanning kunt configureren en budgetplanningprocessen kunt instellen.

## <a name="overview-of-budget-planning"></a>Overzicht van budgetplanning

Een organisatie kan budgetplanning configureren en vervolgens budgetplanningsprocessen instellen om te voldoen aan de bijbehorende beleidsregels, procedures en vereisten voor budgetvoorbereiding. Wanneer u de concepten en terminologie begrijpt die in Microsoft Dynamics 365 Finance worden gebruikt, kunt u gemakkelijker en efficiënt budgetplanning in uw organisatie implementeren.

### <a name="key-terms"></a>Belangrijke termen

- **Budgetplanningsprocessen**: met budgetplanningsprocessen wordt bepaald hoe budgetplannen kunnen worden bijgewerkt, doorgestuurd, beoordeeld en goedgekeurd in de budgetorganisatiehiërarchie. Een budgetplanningsproces wordt gekoppeld aan een budgetcyclus en een organisatie via een rechtspersoon.
- **Budgetplannen**: de budgetplannen bevatten de budgetgegevens voor een budgetcyclus. U kunt meerdere budgetplannen hebben die voor verschillende doeleinden worden gebruikt. U kunt bijvoorbeeld budgetplannen gebruiken om budgetbedragen voor verschillende organisatie-eenheden te maken. U kunt ze ook gebruiken om vergelijkingen uit te voeren en weloverwogen beslissingen te nemen.
- **Budgetplanscenario´s**: met de budgetplanscenario's worden categorieën gegevens gedefinieerd voor de budgetplannen. U definieert budgetplanscenario's ter ondersteuning van klassen van monetaire eenheden en andere maateenheden, zoals hoeveelheden. Voorbeelden van monetaire budgetplanscenario's zijn "Afdeling vorig jaar" en "Afdelingsaanvragen". Voorbeelden van budgetplanscenario´s waarin hoeveelheden worden gebruikt, zijn "Ondersteuningsaanvragen vorig jaar" en "Aantal FTE´s".
- **Budgetplanningsfasen**: met de budgetplanningsfasen worden de stappen gedefinieerd die een budgetplan volgt vanaf het begin tot de definitieve goedkeuring. Budgetplanningsfasen worden gerangschikt in budgetplanningwerkstromen.
- **Budgetplanningsworkflows**: budgetplanningsworkflows bestaan uit budgetplanningsfasen en de budgetplanningsfasen worden gedefinieerd met de budgetplanningsworkflows. Budgetplanningsworkflows worden gekoppeld aan budgetteringsworkflows. Budgetteringsworkflows zijn de geautomatiseerde en handmatige processen waarmee budgetplannen door de budgetplanningsfasen worden verplaatst.

[![Terminologie budgetplanning](./media/budgetplanning-terms-1024x504.png)](./media/budgetplanning-terms.png)

### <a name="typical-tasks"></a>Veelvoorkomende taken

U kunt budgetplanning gebruiken om de volgende taken uit te voeren:

- Budgetplannen maken om de verwachte opbrengsten en uitgaven voor een budgetcyclus te definiëren.
- Analyseren en bijwerken van budgetplannen voor meerdere scenario's.
- De budgetplannen automatisch doorsturen samen met werkbladen, verantwoordingsdocumenten en andere bijlagen voor beoordeling en goedkeuring.
- Meerdere budgetplannen van een lager niveau van de organisatie samenvoegen in één bovenliggend budgetplan op een hoger niveau. U kunt ook een enkel budgetplan ontwikkelen op een hoger niveau in de organisatie en de budgetten toewijzen aan lagere niveaus.

Budgetplanning is geïntegreerd met andere modules. Zo kunt u informatie van vorige budgetten, werkelijke uitgaven, vaste activa en Human Resources opnemen. Omdat budgetplanning ook geïntegreerd is in Microsoft Excel en Microsoft Word kunt u deze programma's gebruiken om de budgetplanningsgegevens te gebruiken. Een budgetbeheerder kan bijvoorbeeld de budgetaanvraag van een afdeling importeren vanuit een budgetplanscenario in een Excel-werkblad. De gegevens kunnen vervolgens worden geanalyseerd, bijgewerkt en uitgezet in het werkblad en vervolgens terug naar de budgetplanregels worden gepubliceerd.

## <a name="configuring-budget-planning"></a>Budgetplanning configureren

De functionaliteit die is geïntroduceerd in Dynamics 365 Finance in versie 10.0.9 (april 2020), bevat een functie waarmee u de prestaties kunt verbeteren wanneer u de knop **Publiceren** gebruikt om bestaande records in Excel bij te werken en deze vervolgens terug te publiceren naar de client. Deze functie versnelt het updateproces en vermindert ook de kans dat een update wordt geblokkeerd wanneer u meerdere records tegelijk bijwerkt. Om deze functionaliteit beschikbaar te maken, gaat u naar het werkgebied **Functiebeheer** en schakelt u de functie **Optimalisatie van de budgetplanningsquery voor prestaties** in onder **Budgettering**. We raden u aan deze functie in te schakelen.

De pagina **Budgetplanningsconfiguratie** bevat de meeste instellingen die nodig zijn om budgetplanning in te stellen. In de volgende secties wordt een aantal factoren beschreven waarmee u rekening dient te houden wanneer u budgetplanning configureert. Nadat u de configuratie hebt voltooid, stelt u budgetplanningsprocessen in.

### <a name="budget-planning-schema-optional"></a>Budgetplanningsschema (optioneel)

Een optionele maar aanbevolen eerste stap bestaat eruit een schema te maken waarin de procedure van uw organisatie wordt weergegeven voor het formuleren van een budget. U kunt elke gewenste methode gebruiken om dit schema te maken.

In de volgende afbeelding wordt een generiek voorbeeld weergegeven, waarin afzonderlijke budgetplanningsworkflows worden gemaakt voor verschillende niveaus van de organisatie. Fasen worden gedefinieerd in elke workflow en specifieke scenario's worden toegewezen aan elke fase om de budgetgegevens te bewaren. Taken worden voltooid om de gegevens van de ene fase naar de volgende fase te verplaatsen. Bedragen kunnen bijvoorbeeld aan verschillende rekeningen, goedkeuringen of andere beoordelingen worden toegewezen of ermee samengevoegd. In deze illustratie wordt met de cursieve tekst een scenario aangegeven dat niet kan worden bewerkt tijdens de fase, of historische gegevens of gegevens die zijn goedgekeurd in een eerdere fase en daarom niet kunnen worden gewijzigd.

[![Generiek schema budgetplanning](./media/budgetplanninggenericschema-300x145.png)](./media/budgetplanninggenericschema.png) 

De volgende illustratie bevat een voorbeeld waar het hoofdkantoor van het bedrijf de budgetbasisbedragen voor het aanvankelijke budget schat en deze verdeelt over verkoopafdelingen. De verkoopafdelingen maken vervolgens een raming en dienen hun prognose weer in bij het hoofdkantoor, waar de budgetmanager de prognose samenvoegt en corrigeert. Tot slot verzendt de budgetmanager de gecorrigeerde budgetbedragen naar de CFO voor controle, laatste correcties en goedkeuring.

[![Voorbeeld van een budgetplanningsschema](./media/budgetplanningexampleschema-300x145.png)](./media/budgetplanningexampleschema.png)

### <a name="organization-hierarchy-for-budget-planning"></a>Organisatiehiërarchie voor budgetplanning

Op de pagina **Organisatiehiërarchie** kunt u een organisatiehiërarchie opgeven als een budgetplanningshiërarchie voor elk budgetplanningsproces. De budgetplanningshiërarchie hoeft niet overeen te komen met de standaardorganisatiehiërarchie die wordt gebruikt voor andere doeleinden. Omdat deze hiërarchie wordt gebruikt om gegevens samen te voegen en te distribueren, kunt u deze wellicht een andere structuur geven. In het voorbeeldschema bevinden de verkoopafdelingen zich onder een hoofdkantoorniveau dat budget- en financiële afdelingen bevat. Deze structuur verschilt waarschijnlijk van de structuur die wordt gebruikt om bewerkingen voor de verkoopafdelingen te beheren. Slechts één organisatiehiërarchie kan worden toegewezen aan elk budgetplanningsproces.

Zie [Organisaties en organisatiehiërarchieën](../../fin-and-ops/organization-administration/organizations-organizational-hierarchies.md) voor meer informatie.

### <a name="user-security"></a>Gebruikersbeveiliging

Budgetplanning kan een van de twee beveiligingsmodellen volgen om gebruikermachtigingen te definiëren. Als u het beveiligingsmodel wilt opgeven, stelt u een budgetplanningsparameter in op de pagina **Budgetplanningsconfiguratie**.

### <a name="budget-planning-workflows-stages"></a>Workflowfasen van budgetplanning

Budgetplanningsworkflows worden gebruikt in combinatie met budgetteringsworkflows om het maken en ontwikkelen van budgetplannen te beheren.

Een budgetplanningwerkstroom bestaat uit een geordende reeks fasen die een budgetplan doorloopt. Elke budgetplanningsworkflow wordt gekoppeld aan een budgetteringsworkflow. Budgetteringsworkflows zijn een type workflow die in heel Dynamics 365 Finance wordt gebruikt. Hiermee worden de budgetplannen samen met de werkbladen, verantwoordingsdocumenten en bijlagen door de hele organisatie doorgestuurd voor beoordeling en goedkeuring.

U maakt een budgetplanningsworkflow in de sectie **Workflowfasen** van de pagina **Budgetplanningsconfiguratie**. Daar kunt u de fasen en de budgetteringsworkflow selecteren die worden gebruikt en kunt u extra instellingen configureren.

Het is een goed idee om een budgetplanningsworkflow voor elk niveau van een budgetteringshiërarchie maken. U wijst vervolgens een budgetteringsworkflow toe die elementen bevat die overeenkomen met de fasen in de budgetplanningsworkflow. In het voorbeeldschema eerder in dit onderwerp wordt een budgetplanningsworkflow gemaakt voor de verkoopafdelingen, wordt een andere budgetplanningsworkflow gemaakt voor het hoofdkantoor. Met een budgetteringsworkflow worden de budgetplannen door de fasen verplaatst.

U maakt de budgetteringsworkflow voor budgetplanning op de pagina **Budgetteringsworkflows**. Het proces lijkt op het proces voor het maken van andere workflows. In de volgende afbeelding ziet u een voorbeeld van een workflow voor het hoofdkantoor.

[![Budgetteringsworkflow voor budgetplanning](./media/budgetingworkflowforbudgetplanning-300x300.png)](./media/budgetingworkflowforbudgetplanning.png) 

De workflow bevat de volgende elementen:

- Toewijzing aan de verkoopafdeling en samenvoeging van hun inzendingen
- Beoordeling van budgetmanager
- Goedkeuring van CFO
- Faseovergangen tussen de fasen van de budgetplanningsworkflow

U wijst de budgetteringsworkflow aan elke budgetplanningsworkflow in de sectie **Workflowfasen** van de pagina **Budgetplanningsconfiguratie** toe.

### <a name="parameters-scenarios-and-stages"></a>Parameters, scenario's en fasen

Met de oorspronkelijke instellingen op de pagina **Budgetplanningsconfiguratie** kunt u een aantal bouwstenen maken voor latere configuratiestappen:

- **Parameters**: met parameters worden de beveiligingregels gedefinieerd die u wilt toepassen op budgetplannen en de financiële standaarddimensies die moeten worden gebruikt wanneer gebruikers inzoomen op de bedragen van budgetplanscenario's.
- **Scenario's**: de scenario's omvatten de categorieën gegevens die u voor de budgetplannen wilt. U definieert budgetplanscenario's ter ondersteuning van klassen van monetaire eenheden en andere maateenheden, zoals hoeveelheid. In een budgetplan wordt met scenario's één versie van budgetplanningsgegevens voorgesteld. Voorbeelden van monetaire budgetplanscenario's zijn "Verkoop vorig jaar" en "Ondertekende contracten". Voorbeelden van scenario's waarin hoeveelheden worden gebruikt, zijn "Aantal verkoopgesprekken" en "Aantal FTE´s".
- **Fasen**: met fasen worden de stappen bepaald die een budgetplan volgt vanaf het begin tot de definitieve goedkeuring. Voorbeelden van budgetplanningsfasen zijn "HQ-rollup", "CFO-controle" en "Definitief".

### <a name="allocation-schedules"></a>Toewijzingsschema's

In budgetplanning kunt u de bedragen of hoeveelheden op budgetplanregels van een bepaald scenario aan een ander scenario of zelfs aan hetzelfde scenario toewijzen. U kunt bijvoorbeeld bedragen of hoeveelheden toewijzen aan hetzelfde scenario als u wijzigingen op de financiële dimensies of de datums van de bedragen in dat scenario wilt toepassen. Een toewijzing kan plaatsvinden in een budgetplan of vanuit een budgetplan aan een ander budgetplan.

Met toewijzingsschema´s worden budgetplanregels automatisch toegewezen tijdens workflowverwerking. U kunt toewijzingen doen met behulp van een van de volgende methoden in de lijst **Toewijzingsmethode**:

- **Toewijzen aan perioden**: u gebruikt een periodetoewijzingssleutel om de budgetplanregels toe te wijzen vanuit het bronbudgetplanscenario aan perioden in het doelscenario.

    > [!NOTE]
    > Opmerking: voordat u kunt toewijzen aan perioden, moet u periodetoewijzingssleutels instellen op de pagina **Periodetoewijzingscategorieën**.

- **Toewijzen aan dimensies**: de budgetplanregels worden toegewezen vanuit het bronbudgetplanscenario aan de financiële dimensies in het doelscenario.

    > [!NOTE]
    > Opmerking: voordat u kunt toewijzen aan dimensies, moet u budgettoewijzingstermijnen instellen op de pagina **Budgettoewijzingstermijnen**.

- **Samenvoegen**: de budgetplanregels worden samengevoegd vanuit het bronbudgetplanscenario in de gekoppelde budgetplannen met het doelscenario in het bovenliggende budgetplan.
- **Verdelen**: de budgetplanregels worden verdeeld vanuit het budgetplanscenario in het bovenliggende budgetplan naar het doelscenario in de gekoppelde budgetplannen.
- **Grootboektoewijzingsregels gebruiken**: de budgetplanregels worden verdeeld vanuit het bronbudgetplanscenario naar het doelscenario op basis van de grootboektoewijzingsregel die is geselecteerd.
- **Kopie van budgetplan**: u kunt een ander budgetplan selecteren dat u als bron van de toewijzing wilt gebruiken.

### <a name="stage-allocations"></a>Fasetoewijzingen

Fasetoewijzingen worden gebruikt om budgetplanregels automatisch toe te wijzen tijdens workflowverwerking. Wanneer fasetoewijzingen worden gebruikt, kunnen budgetplanregels in het doelscenario worden gemaakt en gewijzigd zonder interventie van de persoon die het budgetplan heeft voorbereid, of van de controleur.

Wanneer u een fasetoewijzing instelt, koppelt u de budgetplanningswerkstroom en de fase met de toewijzingsplanning. De budgetplanningsworkflow moet worden gekoppeld aan een budgetteringsworkflow waarin de geautomatiseerde workflowtaak **Toewijzing budgetplanningsfase** wordt gebruikt. Wanneer de workflow de opgegeven fase bereikt, wordt de toewijzing automatisch uitgevoerd. Deze geautomatiseerde taak kan worden gebruikt om budgetregels te maken in een nieuw scenario.

In het voorbeeldschema eerder in dit onderwerp, wordt een toewijzing gedaan om bedragen van een budgetplan en scenario's in de hoofdkantoorbasisfase over te boeken naar een ander budgetplan en scenario's en in de ramingsfase van de verkoopafdelingen. In de volgende afbeelding ziet u de relevante sectie van het voorbeeldschema.

[![Fasetoewijzing](./media/stageallocation-204x300.png)](./media/stageallocation.png) 

Bovendien vindt in het voorbeeldschema een aggregatie plaats vanuit budgetplannen en scenario's in de indieningsfase van de verkoopafdelingen met een bovenliggend plan in de rollup-fase voor het hoofdkantoor. In de volgende afbeelding ziet u de relevante sectie van het voorbeeldschema.

[![Aggregatie](./media/aggregation-109x300.png)](./media/aggregation.png)

### <a name="priorities"></a>Prioriteiten

U kunt budgetplanprioriteiten eventueel gebruiken om categorieën en doelstellingen te definiëren voor de budgetplannen die u hebt ingesteld. U kunt prioriteiten ook gebruiken voor het ordenen, indelen en evalueren van verschillende budgetplannen. U kunt bijvoorbeeld een budgetplanningsprioriteit maken voor gezondheid en veiligheid en vervolgens budgetplannen evalueren die zijn toegewezen aan die prioriteit. U kunt ook een nummer toewijzen aan uw budgetplannen om een rangorde aan te duiden.

### <a name="columns-and-layouts"></a>Kolommen en indelingen

Budgetcijfers worden in een budgetplan weergegeven in rijen en kolommen. U moet eerst de kolommen definiëren en vervolgens kunt u een indeling maken om de weergave van die kolommen te definiëren.

Als u een kolom wilt definiëren, selecteert u een budgetplanscenario. De regelbedragen van dat scenario worden weergegeven in het budgetplan. U kunt een periode selecteren om het bedrag te filteren en u kunt ook filters toepassen die zijn gebaseerd op de grootboekrekening.

Wanneer u een indeling definieert, selecteert u een grootboekdimensie die is ingesteld om de budgetplanrijen te maken die u wilt weergeven en selecteer de kolommen als indelingselementen. U kunt meerdere indelingen maken, zodat een budgetplan de gewenste gegevens bevat die u in verschillende fasen van het budgetplanningsproces wilt.

Naast kolommen voor budgetbedragen kunt u kolommen definiëren voor de velden voor project, voorgesteld project, activum en voorgesteld activum van het budgetplan. U kunt een kolom ook voor gebudgetteerde posities definiëren. Deze optie is handig wanneer u personeelsbudgetten moet analyseren.

Voor het voorbeeldschema wilt u mogelijk kolommen maken voor de scenario's "Verkoop vorig jaar", "Contracten" en "Prognose". (In de volgende afbeelding ziet u de relevante sectie van het voorbeeldschema.) U kunt vervolgens één scenario of al deze scenario's in afzonderlijke kolommen opdelen voor elk kwartaal van het boekjaar, zodat de manager van de verkoopafdeling nauwkeurig prognosebedragen voor elke periode kan invoeren.

[![Kolommen](./media/columns.png)](./media/columns.png)

U kunt ook opgeven of elk indelingselement (kolom) bewerkbaar is en of het beschikbaar is in een werkbladsjabloon die voor die indeling is gemaakt. Voor het voorbeeldschema zijn in de indeling die voor de ramingsfase wordt gebruikt, de prognosekolommen bewerkbaar, terwijl de kolommen "Verkoop vorig jaar" en "Contracten" alleen-lezen zijn.

> [!NOTE]
> Standaard bent u beperkt tot 36 kolommen, tenzij u budgetplanning uitbreidt met de stappen in [De indeling van de budgetplanning uitbreiden](./extending-budget-planning-layout.md).

### <a name="templates"></a>Sjablonen

In de sectie **Indelingen** van de pagina **Budgetplanningsconfiguratie** kunt u een Excel-sjabloon genereren, weergeven of uploaden voor elke indeling. Deze sjablonen zijn de werkmappen die aan elk budgetplan worden gekoppeld om aanvullende analyse, grafieken en gegevensinvoermogelijkheden te verschaffen.

Wanneer een sjabloon wordt gegenereerd, wordt de indeling vergrendeld en kan deze niet worden bewerkt. Door deze vergrendeling wordt gewaarborgd dat de sjabloonindeling overeenkomt met de indeling van het budgetplan en dezelfde gegevens bevat. Nadat een sjabloon is gegenereerd, kan deze worden weergegeven en bewerkt. U kunt bijvoorbeeld grafieken toevoegen aan de sjabloon of de weergave ervan verder aanpassen.

> [!NOTE]
> Een sjabloon moet worden opgeslagen op een locatie waartoe de gebruiker toegang heeft, zodat deze naar de indeling kan worden geüpload nadat de bewerking is voltooid. Op die manier wordt de sjabloon gebruikt met budgetplannen waarin de indeling wordt gebruikt.

### <a name="descriptions"></a>Omschrijvingen

In de sectie **Indelingen** kunt u beschrijvingen toewijzen om de naam van een financiële dimensie weer te geven die in een indeling is opgenomen. Een organisatie wil bijvoorbeeld mogelijk de naam van de hoofdrekening weergeven naast het nummer van de hoofdrekening in een budgetplan. Het is echter mogelijk dat u de namen van andere financiële dimensies wilt weglaten, om te voorkomen dat de weergave onoverzichtelijk wordt.

## <a name="setting-up-budget-planning-processes"></a>Budgetplanningsprocessen instellen

Wanneer u klaar bent met het configureren van de budgetplanning, kunt u budgetplanningsprocessen instellen op de pagina **Budgetplanningsproces**. Budgetplanningsprocessen zij regelsets waarmee wordt bepaald hoe budgetplannen kunnen worden bijgewerkt, doorgestuurd, beoordeeld en goedgekeurd in de budgetorganisatiehiërarchie.

Voor elk budgetplanningsproces selecteert u eerst een budgetcyclus en een grootboek. Elk budgetplanningsproces is gerelateerd aan slechts één budgetcyclus en één grootboek. Selecteer vervolgens de budgetorganisatiehiërarchie op het sneltabblad **Administratie budgetplanningsproces** en wijs een budgetplanningsworkflow toe aan alle divisies binnen de organisatie die worden weergegeven in het raster.

Als u de budgetplanningsworkflow voor soortgelijke divisies wilt toewijzen of wijzigen, selecteert u **Workflow toewijzen** en selecteert u vervolgens het gewenste organisatietype en de budgetplanningsworkflow die u wilt gebruiken. De budgetteringsworkflow-id die is gekoppeld aan elke budgetplanningwerkstroom wordt automatisch toegevoegd aan het raster.

Wanneer u de faseregels en sjablonen definieert op het sneltabblad **Faseregels en indelingen van budgetplanning** kunt u een andere set regels en standaardsjablonen definiëren voor elke budgetplanningsfase. In de ramingsfase van de verkoopafdelingen kan gebruikers bijvoorbeeld worden toegestaan de regels in een budgetplan te wijzigen, maar niet om regels toe te voegen. In de indieningsfase kan gebruikers worden toegestaan regels weer te geven, maar niet om regels te wijzigen of toe te voegen, omdat het werk in die fase is voltooid en wijzigingen in de budgetplannen moeten worden voorkomen. Als u de indelingen wilt selecteren die voor budgetplannen beschikbaar zijn, selecteer u **Alternatieve indelingen**.

U kunt desgewenst budgetplanningsprioriteiten selecteren op het sneltabblad **Prioriteitsbeperkingen budgetplan**. Prioriteiten kunnen vervolgens worden geselecteerd in budgetplannen.

De laatste stap is het activeren van het budgetplanningsproces via het menu **Acties**. Een budgetplanningsproces kan pas worden gebruikt nadat het is geactiveerd.

Via het menu **Acties** kunt u ook een nieuw proces maken door een bestaand proces te kopiëren. Deze functie is handig voor organisaties die dezelfde processtroom voor elke budgetcyclus volgen en weinig tot geen wijzigingen aanbrengen.

Een andere nuttige opdracht in het menu **Acties** is **Budgetprocesstatus weergeven**. Met deze opdracht worden de budgetplannen in een proces grafisch weergegeven, samen met relevante gegevens, zoals de workflowstatus van de plannen, overzichten per bedrag en per eenheid en navigatie naar de budgetplannen zelf via één keer klikken.

[![Status van budgetplanningproces](./media/budgetplanningprocessstatus-300x171.png)](./media/budgetplanningprocessstatus.png)
