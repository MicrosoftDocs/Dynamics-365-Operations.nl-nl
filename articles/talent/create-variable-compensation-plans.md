---
title: Variabelecompensatieplannen maken
description: Variabele compensatie heeft betrekking op de onregelmatige inkomsten van een werknemer, zoals bonussen of aandelenpakketten. In dit onderwerp worden de onderdelen beschreven die u moet instellen voordat u variabele compensatie kunt gebruiken en werknemers kunt inschrijven voor een plan voor variabele compensatie.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HCMCompEligibility, HcmJobFunction, HcmWorker, HRMCompPerfPlan
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 16011
ms.assetid: fc3a394e-9ac6-4f8c-9162-dc16ec22720f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 4e94307ae82200daa3248afdbfde081656747d47
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898776"
---
# <a name="create-variable-compensation-plans"></a>Variabelecompensatieplannen maken

Variabele compensatie heeft betrekking op de onregelmatige inkomsten van een werknemer, zoals bonussen of aandelenpakketten. In dit artikel worden de onderdelen beschreven die u moet instellen voordat u variabele compensatie kunt gebruiken en werknemers kunt inschrijven voor een plan voor variabele compensatie.

De berekening van variabele compensatiebedragen voor uw werknemers kan worden gebaseerd op verschillende factoren, zoals de prestaties van de werknemer, het compensatieniveau van de werknemer en de prestaties van de afdeling.

## <a name="variable-compensation-components"></a>Onderdelen van variabele compensatie
### <a name="create-compensation-types"></a>Compensatietypen maken

**Typen variabele compensatie** zijn een vereist onderdeel. Met typen variabele compensatie kunt u de soorten variabele compensatie beschrijven die uw organisatie toekent. Met deze typen variabele compensatie kunt u ook opgeven of de compensatie contant of in een niet-monetaire vorm, zoals een aandeel, plaatsvindt.

### <a name="describe-vesting-rules"></a>Toekenningsregels omschrijven

Bedrijven kunnen desgewenst **toekenningsregels** instellen. Met vestigingsregels wordt beschreven hoe de variabele beloning na verloop van tijd moet worden toegewezen. Een vestigingsregel kan bijvoorbeeld aangeven dat de werknemer 25 procent van zijn of haar totale beloning elk jaar voor de volgende vier jaar ontvangt. Vestigingsregels zijn alleen ter informatie.

## <a name="variable-compensation-plans"></a>Variabelecompensatieplannen
Het **variabelecompensatieplan** bevat de regels, de berekeningsmethoden en de standaardwaarden voor de berekening van variabele compensatie voor ingeschreven werknemers. Wanneer u een variabel compensatieplan maakt, moet u het variabele compensatietype instellen. Met het variabele compensatietype wordt bepaald of een valutabedrag of een aantal eenheden als beloning wordt berekend. U moet de berekeningsmethode ook instellen:

-   **Punt in tijd**: de berekening van de variabele beloning is gebaseerd op de vaste compensatie die de werknemer op een bepaalde datum had. Met deze datum is in de procesgebeurtenis opgegeven wanneer nieuwe compensatiebedragen worden verwerkt.
-   **Samengesteld**: een toekenningsbedrag wordt berekend voor elk uniek vast compensatiesalaristarief dat de werknemer tussen de begindatum en de einddatum van de cyclus voor de procesgebeurtenis had. De tarieven worden vervolgens samen opgeteld om de definitieve beloning vast te stellen. Voorbeeld: een werknemer die tijdens de cyclus naar een andere positie is overgeplaatst waarvoor een ander loontarief geldt. In dit geval wordt de variabele toekenning aangepast aan de tijd gedurende welke de werknemer elk salaristarief had.

Het bedrag van de variabele toekenning kan op een percentage van de normale basisinkomsten van de werknemer of een bepaald aantal eenheden worden gebaseerd.

-   Selecteer de optie **Percentage van basis** om een standaardpercentage in te voeren en geef op of de basis het vaste salaristarief van de werknemer of het controlepunt voor het compensatieniveau van de werknemer moet zijn. Het compensatieniveau wordt ingesteld op de functie van de werknemer. Een van de referentiepunten uit de compensatiestructuur kan worden ingesteld als het controlepunt in het vaste compensatieplan. Het systeem gebruikt het compensatieniveau van de functie van de werknemer en voert een kruisverwijzing uit met het controlepunt dat wordt vermeld in het vaste compensatieplan van de werknemer om het controlepuntbedrag te vinden voor het compensatieniveau van de werknemer. Het controlepuntbedrag wordt vervolgens gebruikt in plaats van het vaste loontarief van de werknemer als de basis voor de beloning.
-   Selecteer de optie **Aantal eenheden** om een standaardaantal eenheden, de waarde van elke eenheid en de valuta van de eenheidswaarde in te voeren als het compensatieplan voor een niet-contante toekenning is (bijvoorbeeld 200 eenheden van voorraad die wordt gewaardeerd op 40 USD) of alleen het aantal eenheden als het compensatieplan voor een contante toekenning is. Voor een contante beloning ontvangt de werknemer het opgegeven aantal eenheden van de valuta die wordt gebruikt voor zijn of haar vaste compensatieplan (bijvoorbeeld 500 eenheden van 1 EUR). Het besturingselement van de een-op-een-relatie kan worden gebruikt om aan te geven of er een directe een-op-een-toewijzing tussen het aantal eenheden en de waarde per eenheid is. Wanneer u een variabel compensatieplan maakt voor een op contanten gebaseerd plan met behulp van het aantal eenheden, wordt deze optie automatisch vergrendeld op **Ja** en is de eenheidwaarde **1,0000**.

Met de instelling **Aanstellingsregel** kunt u opgeven of alle werknemers dezelfde verhoging moeten krijgen, ongeacht de datum waarop ze in dienst zijn gekomen (**Aanstellingsregel** = **Geen**) of dat werknemers een percentage krijgen van de beloning die wordt gebaseerd op de duur van het dienstverband gedurende de cyclus (**Aanstellingsregel** = **Percentage**). 

Met **Hefboomwerking** kunt u de beloning van een werknemer aanpassen op basis van de prestaties van de afdeling van de werknemer. Prestatiegegevens kunnen voor elke afdeling worden ingesteld op de pagina **Afdelingen** onder **Gerelateerde formulieren** &gt; **Compensatie** &gt; **Prestaties**. De beloning die werknemers in die afdeling ontvangen, is afhankelijk van de waarde van het veld **Percentage van bereikt doel** waarmee de prestaties van de afdeling worden aangegeven:

-   Als de prestaties van de afdeling 100 procent zijn, wordt de toekenning voor de werknemers op die afdeling meegenomen met het percentage dat in het veld **Uitbetaling bij 100%** is ingesteld.
-   Als de prestaties van de afdeling meer dan 100 procent zijn, wordt het percentage dat is ingesteld in het veld **Per 1% boven doelstelling**, toegevoegd aan het percentage dat is ingesteld in het veld **Uitbetaling bij 100%** tot de waarde wordt bereikt die in het veld **Hoogst toegestane uitbetaling** is ingesteld.
-   Als de prestaties van de afdeling minder dan 100 procent zijn, wordt het percentage dat is ingesteld in het veld **Per 1% onder doelstelling**, afgetrokken van het percentage dat is ingesteld in het veld **Uitbetaling bij 100%** tot de waarde wordt bereikt die in het veld **Laagst toegestane uitbetaling** is ingesteld.

U kunt **tolerantieniveaus** voor de drempelpercentages instellen, zodat een waarschuwingsbericht wordt weergegeven als de hefboomwerking ervoor zorgt dat het percentage buiten het drempelpercentage valt. 

Standaard wordt gezocht naar de afdeling die is ingesteld op de positie van de werknemer. De beloning voor sommige werknemers kan echter afhankelijk zijn van de prestaties van meerdere afdelingen. In dit geval kunnen de verschillende afdelingen en het percentage van de beloning die aan de prestaties van elke afdeling is toegewezen, worden ingesteld op de inschrijving voor de variabele compensatie van de werknemer. Zie de volgende sectie 'Inschrijving op variabele compensatie' voor meer informatie. 

De hefboomwerking wordt alleen gebruikt als **Prestatieloon** is geselecteerd wanneer het compensatieproces wordt uitgevoerd. 

Met het tabblad **Overschrijvingen niveaus** kunt u het standaardpercentage van de beloning of het aantal eenheden op basis van het compensatieniveau van de werknemer overschrijven. Als **Overschrijvingen voor niveaus inschakelen** is ingesteld op **Ja** voor werknemers die zijn ingeschreven voor het variabele compensatieplan, wordt het niveau van de functie van de werknemer gebruikt en wordt vervolgens gezocht naar de tabel met niveau-overschrijvingen om het percentage of het aantal eenheden voor dat niveau te bepalen. Als het niveau niet wordt gevonden in de tabel met niveau-overschrijvingen, wordt het standaardpercentage of het aantal eenheden van het tabblad **Algemeen** gebruikt. Het percentage en het aantal eenheden kunnen ook worden overschreven in de inschrijving van de werknemer in het variabele compensatieplan.

## <a name="variable-compensation-enrollment"></a>Inschrijving op variabele compensatie
### <a name="determine-who-is-eligible-for-the-plan"></a>Bepalen wie voor het plan aanmerking komt

Wanneer u klaar bent om werknemers in een variabelecompensatieplan in te schrijven, bestaat de eerste stap eruit te bepalen wie in aanmerking komt voor de compensatie die in het plan is opgegeven. U kunt het plan alleen aan werknemers toewijzen als u hebt bepaald dat ze in aanmerking komen. Als u geschiktheid wilt instellen, opent u de pagina **Geschiktheidsregels** om een nieuwe geschiktheidsregel voor uw plan te maken, en definieer vervolgens de criteria waaraan een werknemer moet voldoen voor het compensatieplan. U kunt geschiktheid beperken tot afdeling, vakbond, compensatieregio (locatie), taak, functie, functietype en/of compensatieniveau. Werknemers kunnen alleen voor een compensatieplan worden ingeschreven als ze voldoen aan **alle** criteria die voor de geschiktheidsregel zijn ingesteld. 

**Opmerking:** met geschiktheidsregels wordt de geschiktheid bepaald voor zowel vastecompensatieplannen als variabelecompensatieplannen. Voor de geschiktheidsregels worden de volgende velden in de functie-, positie- en werknemersrecords gebruikt om te bepalen of een werknemer voor een compensatieplan in aanmerking komt:

- Op de pagina **Functie**:
  -   Het veld **Functie**
  -   De velden **Functie** en **Functietype** op het tabblad **Taakclassificatie**
  -   Het veld **Niveau** op het tabblad **Compensatie**
- Op de pagina **Posities**: de velden **Afdeling** en **Compensatieregio**
- Op de pagina <strong>Werknemers</strong>: de gegevens over vakbonden die zijn gekoppeld aan de werknemer onder <strong>Persoonlijke gegevens</strong> &gt; <strong>Vakbonden</strong> op het tabblad *<strong><em>Werknemer</em></strong>*

### <a name="enable-enrollment-for-the-variable-compensation-plan"></a>Inschrijving voor het variabelecompensatieplan inschakelen

Stel op de pagina **Variabelecompensatieplannen** de optie **Inschrijving inschakelen** in op **Ja** om toe te staan dat werknemers die in aanmerking komen, voor het plan worden ingeschreven.

### <a name="enroll-the-employee"></a>De werknemer inschrijven

U kunt werknemers nu inschrijven voor het variabelecompensatieplan. Als u een werknemer wilt inschrijven, gaat u naar de pagina **Werknemers** en selecteert u de werknemer. Klik in het actievenster op **Compensatie** &gt; **Inschrijving op variabel plan**. 

**Opmerking:** **Inschrijving** moet worden ingesteld op **Ja** in het variabelecompensatieplan. In het veld **Plan** worden alleen de plannen weergegeven waarvoor de werknemer in aanmerking komt op basis van de geschiktheidsregels die voor deze plannen zijn ingesteld. Als er geen geschiktheidsregel voor een plan is ingesteld, komen er geen werknemers in aanmerking voor dat plan. 

Controleer of het veld **Ingangsdatum** juist is ingesteld. Als in het variabele compensatieplan de berekeningsmethode **Samengesteld** wordt gebruikt, kan rekening worden gehouden met de ingangsdatum van de inschrijving tijdens de berekening van de beloning van de werknemer. 

U kunt het tabblad **Overschrijvingen** gebruiken om specifieke waarden voor de werknemer te overschrijven. Bijvoorbeeld als **Aanstellingsregel** is ingesteld op **Percentage** en een ander aanstellingsdatum tijdens de berekening van het aanstellingspercentage van de werknemer moet worden gebruikt, kunt u de aanstellingsdatum instellen in het veld **Datum aanstellingsregel**. U kunt ook de waarde **Toekenningspercentage** of **Aantal eenheden** overschrijven voor een specifieke werknemer, afhankelijk van de instellingen van het plan. Met deze waarden wordt nog steeds rekening gehouden door de aanstellingsregel, prestatiefactoren en andere instellingen in het plan. 

De waarde van **Organisatieoverschrijvingen** wordt gebruikt om de beloning van een werknemer te baseren op de prestaties van een of meer afdelingen. Het percentage dat wordt toegekend aan afdelingen, moet samen 100 procent zijn. Er wordt ook rekening gehouden met de individuele prestaties van de werknemer. Deze instellingen worden alleen gebruikt als **Prestatieloon** is geselecteerd wanneer het compensatieproces wordt uitgevoerd.

<a name="additional-resources"></a>Aanvullende resources
--------

[Compensatieplannen](compensation-plans.md)



