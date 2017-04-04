---
title: Variabelecompensatieplannen maken
description: Variabele compensatie heeft betrekking op de onregelmatige inkomsten van een werknemer, zoals bonussen of aandelenpakketten. Dit onderwerp beschrijft de onderdelen die moeten worden ingesteld voordat u kunt het gebruik van variabele compensatie en een werknemer inschrijven voor een variabele honoreringsregeling.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9397e84f03ee5b340fa2aa0a64e582fc0078526e
ms.openlocfilehash: be156afa73de731e54985485b617bcbae883db3a
ms.lasthandoff: 03/31/2017


---

# <a name="create-variable-compensation-plans"></a>Variabelecompensatieplannen maken

Variabele compensatie heeft betrekking op de onregelmatige inkomsten van een werknemer, zoals bonussen of aandelenpakketten. In dit artikel worden de onderdelen beschreven die u moet instellen voordat u variabele compensatie kunt gebruiken en werknemers kunt inschrijven voor een plan voor variabele compensatie.

De berekening van variabele compensatiebedragen voor uw werknemers kan worden gebaseerd op verschillende factoren, zoals de prestaties van de werknemer, het compensatieniveau van de werknemer en de prestaties van de afdeling.

## <a name="variable-compensation-components"></a>Onderdelen van variabele compensatie
### <a name="create-compensation-types"></a>Compensatietypen maken

**Typen variabele compensatie** zijn een vereist onderdeel. Met typen variabele compensatie kunt u de soorten variabele compensatie beschrijven die uw organisatie toekent. Met deze typen variabele compensatie kunt u ook opgeven of de compensatie contant of in een niet-monetaire vorm, zoals een aandeel, plaatsvindt.

### <a name="describe-vesting-rules"></a>Toekenningsregels omschrijven

Bedrijven kunnen desgewenst **toekenningsregels** instellen. Vestigingsregels wordt beschreven hoe de variabele toekenning na verloop van tijd moet worden toegewezen. Een vestigingsregel kan bijvoorbeeld aangeven dat de werknemer 25 procent van zijn of haar totale toekenning jaarlijks voor de volgende vier jaar ontvangt. Vestigingsregels zijn alleen ter informatie.

## <a name="variable-compensation-plans"></a>Variabelecompensatieplannen
Het **variabelecompensatieplan** bevat de regels, de berekeningsmethoden en de standaardwaarden voor de berekening van variabele compensatie voor ingeschreven werknemers. Wanneer u een variabele honoreringsregeling maakt, moet u het variabele compensatietype instellen. Het variabele compensatietype bepaalt of het systeem een bedrag of aantal eenheden als de toekenning berekent. U moet de berekeningsmethode ook instellen:

-   **tijdstip** : de berekening van de variabele beloning is gebaseerd op de vaste compensatie waarvoor de werknemer op een bepaalde datum. Met deze datum is opgegeven voor de procesgebeurtenis wanneer nieuwe compensatiebedragen worden verwerkt.
-   **Samengesteld**: een toekenningsbedrag wordt berekend voor elk uniek vast compensatiesalaristarief dat de werknemer tussen de begindatum en de einddatum van de cyclus voor de procesgebeurtenis had. De tarieven worden toegevoegd samen om te bepalen van de definitieve beloning. Bijvoorbeeld tijdens de cyclus overgeboekt van een werknemer naar een andere positie waarvoor een ander tarief. In dit geval wordt de variabele toekenning aangepast aan de tijd gedurende welke de werknemer elk salaristarief had.

Het bedrag van de variabele toekenning kan op een percentage van de normale basisinkomsten van de werknemer of een bepaald aantal eenheden worden gebaseerd.

-   Selecteer de optie **Percentage van basis** om een standaardpercentage in te voeren en geef op of de basis het vaste salaristarief van de werknemer of het controlepunt voor het compensatieniveau van de werknemer moet zijn. Het compensatieniveau is ingesteld op de baan van de werknemer. Een van de referentiepunten uit de compensatiestructuur kan worden ingesteld als het controlepunt op de vaste honoreringsregeling. Het systeem gebruikt het compensatieniveau van de taak van de werknemer en kruisverwijzing met het controlepunt dat wordt vermeld in de vaste honoreringsregeling van de werknemer het bedrag van de punt control vinden voor het compensatieniveau van de werknemer. Het besturingselement plaats bedrag wordt vervolgens worden gebruikt in plaats van het vaste loontarief van de werknemer als basis voor de toekenning.
-   Selecteer de optie **Aantal eenheden** om een standaardaantal eenheden, de waarde van elke eenheid en de valuta van de eenheidswaarde in te voeren als het compensatieplan voor een niet-contante toekenning is (bijvoorbeeld 200 eenheden van voorraad die wordt gewaardeerd op 40 USD) of alleen het aantal eenheden als het compensatieplan voor een contante toekenning is. Voor een contante beloning ontvangt de werknemer het opgegeven aantal eenheden van de valuta die wordt gebruikt voor zijn of haar plan met vaste compensatie (bijvoorbeeld 500 stuks van 1 USD). Het besturingselement een-relatie kan worden gebruikt om aan te geven of er een directe-op-een toewijzing tussen het aantal eenheden en de waarde per eenheid is. Wanneer u een variabele honoreringsregeling voor een plan met contant geld maakt met behulp van het aantal eenheden, deze optie is automatisch vergrendeld en kan niet **Ja**, en de eenheidwaarde **1,0000**.

De **aanstellingsregel** kunt u opgeven of alle werknemers in aanmerking komt voor de dezelfde toename, ongeacht de datum waarop ze zijn ingehuurd instellen (**aanstellingsregel** = **geen**), of werknemers ontvangt of een percentage van de toekenning die is gebaseerd op de lengte van het dienstverband tijdens de cyclus (**aanstellingsregel** = **procent**). 

**Hefboomwerking** kunt u om aan te passen van een werknemer toekenning die is gebaseerd op de prestaties van de afdeling van de werknemer. Prestatiegegevens voor elke afdeling kan worden ingesteld op de **afdelingen** pagina onder **gerelateerde formulieren**&gt;**vergoeding**&gt;**prestaties**. De beloning die werknemers in die afdeling ontvangt, is afhankelijk van de waarde van de **percentage van het behaalde doel** veld waarmee wordt aangegeven van het departement prestaties:

-   Als de prestaties van de afdeling 100 procent zijn, wordt de toekenning voor de werknemers op die afdeling meegenomen met het percentage dat in het veld **Uitbetaling bij 100%** is ingesteld.
-   Als de prestaties van de afdeling meer dan 100 procent zijn, wordt het percentage dat is ingesteld in het veld **Per 1% boven doelstelling**, toegevoegd aan het percentage dat is ingesteld in het veld **Uitbetaling bij 100%** tot de waarde wordt bereikt die in het veld **Hoogst toegestane uitbetaling** is ingesteld.
-   Als de prestaties van de afdeling minder dan 100 procent zijn, wordt het percentage dat is ingesteld in het veld **Per 1% onder doelstelling**, afgetrokken van het percentage dat is ingesteld in het veld **Uitbetaling bij 100%** tot de waarde wordt bereikt die in het veld **Laagst toegestane uitbetaling** is ingesteld.

U kunt **tolerantieniveaus** voor de drempelpercentages instellen, zodat een waarschuwingsbericht wordt weergegeven als de hefboomwerking ervoor zorgt dat het percentage buiten het drempelpercentage valt. 

Standaard wordt gezocht naar de afdeling die is ingesteld op de positie van de werknemer. De beloning voor sommige werknemers kan echter afhankelijk zijn van de prestaties van meerdere afdelingen. In dit geval kunnen de verschillende afdelingen en het percentage van de beloning die is toegewezen aan de prestaties van elke afdeling worden ingesteld op de inschrijving op variabele compensatie van de werknemer. Zie de volgende sectie 'inschrijving op variabele compensatie' voor meer informatie. 

De hefboomwerking wordt alleen gebruikt als **Prestatieloon** is geselecteerd wanneer het compensatieproces wordt uitgevoerd. 

De **niveaus overschrijvingen** tabblad kunt u de beloning standaardpercentage of aantal eenheden, op basis van het compensatieniveau van de werknemer overschrijven. Als **inschakelen voor niveaus vervangt** is ingesteld op **Ja** voor werknemers die geregistreerd staan in de variabele honoreringsregeling, neemt het systeem het niveau van de taak van een werknemer en vervolgens zoekt deze in de niveaus heeft voorrang boven de tabel om te bepalen het percentage of aantal eenheden voor dat niveau. Als het niveau is niet gevonden in de tabel, het standaardpercentage of aantal eenheden van overschrijft de **algemeen** tabblad wordt gebruikt. Het percentage en het aantal eenheden kunnen ook worden overschreven voor inschrijving van de werknemer in de variabele honoreringsregeling.

## <a name="variable-compensation-enrollment"></a>Inschrijving op variabele compensatie
### <a name="determine-who-is-eligible-for-the-plan"></a>Bepalen wie voor het plan aanmerking komt

Wanneer u klaar bent om werknemers in een variabelecompensatieplan in te schrijven, bestaat de eerste stap eruit te bepalen wie in aanmerking komt voor de compensatie die in het plan is opgegeven. U kunt het plan alleen aan werknemers toewijzen als u hebt bepaald dat ze in aanmerking komen. Als u geschiktheid wilt instellen, opent u de pagina **Geschiktheidsregels** om een nieuwe geschiktheidsregel voor uw plan te maken, en definieer vervolgens de criteria waaraan een werknemer moet voldoen voor het compensatieplan. U kunt geschiktheid beperken tot afdeling, vakbond, compensatieregio (locatie), taak, functie, functietype en/of compensatieniveau. Werknemers kunnen alleen voor een compensatieplan worden ingeschreven als ze voldoen aan **alle** criteria die voor de geschiktheidsregel zijn ingesteld. 

**Opmerking:** met geschiktheidsregels wordt de geschiktheid bepaald voor zowel vastecompensatieplannen als variabelecompensatieplannen. Voor de geschiktheidsregels worden de volgende velden in de functie-, positie- en werknemersrecords gebruikt om te bepalen of een werknemer voor een compensatieplan in aanmerking komt:

-   Op de pagina **Functie**:
    -   Het veld **Functie**
    -   De velden **Functie** en **Functietype** op het tabblad **Taakclassificatie**
    -   Het veld **Niveau** op het tabblad **Compensatie**
-   Op de pagina **Posities**: de velden **Afdeling** en **Compensatieregio**
-   Op de **werknemers** pagina: de informatie over de vakbonden die is gekoppeld aan de werknemer op **persoonlijke gegevens**&gt;**vakbonden** op de *** werknemer *** tabblad

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Inschrijving voor het variabelecompensatieplan inschakelen

Stel op de pagina **Variabelecompensatieplannen** de optie **Inschrijving inschakelen** in op **Ja** om toe te staan dat werknemers die in aanmerking komen, voor het plan worden ingeschreven.

### <a name="enroll-the-employee"></a>De werknemer inschrijven

U kunt werknemers nu inschrijven voor het variabelecompensatieplan. Als u een werknemer wilt inschrijven, gaat u naar de pagina **Werknemers** en selecteert u de werknemer. Klik in het actievenster op **vergoeding**&gt;**inschrijving op variabel plan**. 

**Opmerking:** **Inschrijving** moet worden ingesteld op **Ja** in het variabelecompensatieplan. De **plannen** veld wordt alleen de plannen waarbij de werknemer in aanmerking komt voor op basis van de geschiktheidsregels die zijn ingesteld voor die programma's wordt weergegeven. Als een geschiktheidsregel is niet ingesteld voor een plan, zijn er geen werknemers niet in aanmerking komt voor dat plan. 

Zorg ervoor dat de **ingangsdatum** veld correct is ingesteld. Als de variabele honoreringsregeling gebruikt de **samengestelde** berekeningsmethode, de ingangsdatum van de inschrijving kan worden beschouwd als tijdens de berekening van de toekenning van de werknemer. 

U kunt de **overschrijft** tabblad om op te heffen van specifieke waarden voor de werknemer. Bijvoorbeeld als **aanstellingsregel** is ingesteld op **procent** op het plan en een ander aanstellingsdatum tijdens de berekening van de werknemer aanstellen moet worden gebruikt, kunt u de aanstellingsdatum de **Datum aanstellingsregel** veld. U kunt ook een overschrijven de **toekenningspercentage** waarde of het **aantal eenheden** waarde voor een bepaalde werknemer, afhankelijk van de instellingen van het plan. Deze waarden wordt nog steeds op de regel, prestatiefactoren en andere instellingen op het plan moet rekening worden gehouden. 

**Organisatie-overschrijvingen** van een werknemer om beloning te baseren op de prestaties van een of meer afdelingen worden gebruikt. Het percentage dat wordt verdeeld over afdelingen moet samen 100 procent. Wordt ook rekening gehouden met de individuele prestaties van de werknemer. Deze instellingen worden alleen gebruikt als **prestatieloon** is ingeschakeld wanneer het compensatieproces wordt uitgevoerd.

<a name="see-also"></a>Zie ook
--------

[Compensatieplannen](compensation-plans.md)


