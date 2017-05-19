---
title: Vastecompensatieplannen maken
description: Vaste compensatie verwijst naar het normale brutosalaris of -loon van een werknemer. In dit artikel worden de onderdelen beschreven die u moet instellen voordat u een plan voor vaste compensatie kunt maken en werknemers kunt inschrijven.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 77e3dc8e8d7b81a366bdf3a164e38c394c90e15f
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="create-fixed-compensation-plans"></a>Vastecompensatieplannen maken

[!include[banner](includes/banner.md)]


Vaste compensatie verwijst naar het normale brutosalaris of -loon van een werknemer. In dit onderwerp worden de onderdelen beschreven die u moet instellen voordat u een plan voor vaste compensatie kunt maken en werknemers kunt inschrijven.

Bedragen van vaste compensaties kunnen voor uw werknemers worden berekend op basis van factoren, zoals prestaties, regio en budgetverhogingen. Microsoft Dynamics 365 for Operations ondersteunt de compensatietypen van stap, schaal en schijf.

## <a name="fixed-compensation-components"></a>Onderdelen van vaste compensatie
### <a name="compensation-levels"></a>Compensatieniveaus

U kunt **compensatieniveaus** gebruiken om de compensatie voor verschillende functies in te stellen. Hiermee wordt ervoor gezorgd dat de werknemers die deze functies bekleden, eerlijk worden betaald. Op de pagina **Compensatieniveaus** kunt u de compensatieniveaus instellen die vereist zijn voor elk stap-, schaal- en schijfplan. Gebruik de knoppen **Omhoog** en **Omlaag** om de niveaus in de juiste volgorde te plaatsen in overeenstemming met het bijbehorende type. Door compensatieniveaus voor een functie in te stellen zorgt u ervoor dat alle werknemers die een positie voor die functie bekleden, op hetzelfde niveau worden betaald.

### <a name="reference-points"></a>Referentiepunten

**Referentiepunten** zijn de kolommen in het raster waarmee de compensatiebereiken voor elk niveau worden gedefinieerd. Het compensatieniveau is de rij in het raster. Normale referentiepunten voor een plan van het type schaal zijn een minimum, een middelpunt en een maximum. U maakt referentiepunten op de pagina **Referentiepunten**.

### <a name="compensation-grids"></a>Compensatierasters

Nadat u de niveaus en de referentiepunten hebt ingesteld, kunnen deze worden gecombineerd om een **compensatieraster** te maken. Op de pagina **Compensatierasters** definieert u gegevens over het raster. Geef bijvoorbeeld op waarvoor het raster is ontworpen, voor welk type plan het wordt gebruikt en welke referentiepunten of kolommen in het raster zijn vereist. Wanneer u klaar bent met het invoeren van die gegevens, klikt u op **Compensatiestructuur** om niveaus en bedragen aan uw raster toe te voegen. 

**Tip:** gebruik de functie **Groepsgewijze wijzigingen** in de compensatiestructuur om oorspronkelijke bedragen in te stellen en deze vervolgens met percentages of bedragen verspreid over uw niveaus of referentiepunten te verhogen.

### <a name="pay-frequencies"></a>Betalingsfrequenties

**Betalingsfrequenties** worden gebruikt om te bepalen hoe het loon of het salaris van een werknemer (bijvoorbeeld € 10 per uur of € 50.000 per jaar) wordt opgegeven en om de omrekening te definiëren tussen de tarieven per uur, per week, per maand (12 maanden) en per jaar. Een bedrijf dat bijvoorbeeld een 38-urige werkweek gebruikt voor werknemers die per uur worden betaald, stelt een betalingsfrequentie in die een wekelijks tarief van 38 heeft, een maandelijks tarief van 164,6666666667 en een jaarlijks tarief van 1.976. Deze conversies worden gebruikt om de verschillende loontarieven te berekenen die in de vaste compensatie van een werknemer worden weergegeven.

## <a name="fixed-compensation-plans"></a>Vastecompensatieplannen
U kunt het vastecompensatieplan ontwerpen om alle onderdelen te combineren die u hebt geconfigureerd. Als u een vastecompensatieplan wilt maken, opent u de pagina **Vastecompensatieplannen**. Hier kunt u uw plan een naam en omschrijving geven, aangeven wat voor plan het is (stap, schaal of schijf), de betalingsfrequentie selecteren die u voor het loontarief van de werknemer (bedrag per uur, bedrag per jaar, enzovoort.) wilt gebruiken en bepaalde opties instellen waarmee wordt bepaald hoe compensatie wordt verwerkt. 

Met de instelling **Tolerantie voor buiten bereik** kunt u opgeven hoe strikt u wilt controleren dat compensatiebedragen tussen de minimum- en maximumbedragen zijn. Voor een **harde** tolerantie moet de compensatie binnen het bereik zijn dat is gedefinieerd voor een bepaald niveau. Met een **zachte** tolerantie wordt u gewaarschuwd wanneer het compensatiebedrag buiten het bereik valt, maar u mag doorgaan. Als u de tolerantie instelt op **Geen**, kunt u elk compensatiebedrag invoeren voor een werknemer zonder een waarschuwing of foutberichten te ontvangen. 

Met de instelling **Aanstellingsregel** kunt u opgeven of alle werknemers dezelfde verhoging moeten krijgen, ongeacht de datum waarop ze in dienst zijn gekomen (**Aanstellingsregel** = **Geen**) of dat werknemers een percentage moeten krijgen van de toekenning die wordt gebaseerd op de duur van het dienstverband gedurende de cyclus (**Aanstellingsregel** = **Percentage**). 

Een **matrix voor bereikgebruik** is handig als u de tijd wilt inkorten gedurende welke werknemers het middelpunt van hun bereik moeten bereiken of als u de tijd gedurende welke werknemers het maximale referentiepunt in het bereik moeten bereiken, wilt verlengen. U wilt bijvoorbeeld werknemers die zich in de onderste 25 procent van hun bereik bevinden, 110 procent van hun doeltoekenning geven, maar u wilt werknemers die zich in de bovenste 25 procent van hun bereik bevinden, slechts 80 procent van hun doeltoekenning geven. Dit om te voorkomen dat ze het maximum heel snel bereiken. 

Nadat u de basisprincipes van het vastecompensatieplan hebt gedefinieerd, kunt u de compensatiestructuur voor het plan instellen. Klik op **Compensatie instellen**. Er wordt een schuifregelaar van een dialoogvenster geopend waarin u drie opties hebt:

-   Een nieuw compensatieraster maken door een referentiepuntinstelling te selecteren en het raster een naam te geven.
-   Een nieuw compensatieraster maken door een kopie van een bestaand raster te maken dat u kunt gebruiken als uitgangspunt.
-   Een bestaand compensatieraster gebruiken dat al is gedefinieerd. Alle compensatieplannen die hetzelfde raster gebruiken, ontvangen updates als dat raster wordt gewijzigd.

Nadat u een optie hebt geselecteerd, wordt de pagina **Compensatiestructuur** geopend en kunt u wijzigingen in het nieuwe compensatieraster of het bestaande compensatieraster aanbrengen.

## <a name="fixed-compensation-enrollment"></a>Inschrijving op vaste compensatie
### <a name="determine-who-is-eligible-for-the-plan"></a>Bepalen wie voor het plan aanmerking komt

De eerste stap bij het inschrijven van werknemers voor een vastecompensatieplan bestaat eruit te bepalen wie in aanmerking komt voor de compensatie die in het plan is gedefinieerd. U kunt het plan pas aan werknemers toewijzen als u hebt bepaald wie in aanmerking komen. Open de pagina **Geschiktheidsregels** om geschiktheid in te stellen. Hier maakt u een nieuwe geschiktheidsregel voor uw compensatieplan en definieert u de criteria waaraan een werknemer moet voldoen om in aanmerking voor een plan. U kunt geschiktheid beperken tot afdeling, vakbond, compensatieregio (locatie), taak, functie, functietype of compensatieniveau. Werknemers kunnen alleen voor een compensatieplan worden ingeschreven als ze voldoen aan alle voorwaarden die voor de geschiktheidsregel zijn ingesteld. 

**Opmerking:** met geschiktheidsregels wordt de geschiktheid bepaald voor zowel vastecompensatieplannen als variabelecompensatieplannen. 

Voor de geschiktheidsregel wordt rekening gehouden met de waarde van specifieke velden in de records Functie, Positie en Werknemer om te bepalen of een werknemer voor een compensatieplan aanmerking komt.

-   Op de pagina **Functie** wordt voor de geschiktheidsregel rekening gehouden met de volgende velden:
    -   Het veld **Functie**
    -   Op het tabblad **Taakclassificatie** de velden **Functie** en **Functietype**
    -   Op het tabblad **Compensatie** het veld **Niveau**
-   Op de pagina **Posities** wordt voor de geschiktheidsregel rekening gehouden met de velden **Afdeling** en **Compensatieregio**.

Voor de geschiktheidsregel wordt ook rekening gehouden met vakbonden die zijn gekoppeld aan de werknemer (klik op de pagina **Werknemers** op het tabblad **Werknemer** op **Persoonlijke gegevens** &gt; **Vakbonden**).

### <a name="define-fixed-compensation-actions"></a>Acties voor vaste compensatie definiëren

**Acties voor vaste compensatie** worden gebruikt wanneer u wijzigingen instelt of toepast op de vaste compensatie van een werknemer. Met acties voor vaste compensatie kunt u de beschrijvende namen voor de typen acties bevatten die een manager voor compensatie en vergoedingen kan uitvoeren. Achter verschillende actietypen zit een speciale logica, zodat deze op specifieke tijden kunnen worden gebruikt. 

Als de vaste compensatie bijvoorbeeld is ingesteld voor een werknemer, kunnen alleen acties met het type **Aanstellen/Opnieuw aanstellen** worden gebruikt. In dit geval kunt u drie verschillende acties van het type **Aanstellen/Opnieuw aanstellen** maken en deze **Aanstellen**, **Opnieuw aanstellen** en **Overplaatsen** noemen. U hebt dan een meer beschrijvende uitleg van de reden waarom de vaste compensatie is gegeven aan een werknemer of waarom deze is gewijzigd.

### <a name="enroll-the-employee"></a>De werknemer inschrijven

U kunt een werknemer nu toewijzen aan een vastecompensatieplan. Open de pagina **Werknemers** en selecteer de werknemer voor inschrijving in het compensatieplan. Klik in het actievenster op **Compensatie** &gt; **Vast plan**. U kunt nu een nieuwe vastecompensatieactie maken voor deze werknemer. 

**Opmerking:** in het veld voor het compensatieplan worden alleen de plannen weergegeven waarvoor een werknemer in aanmerking komt op basis van de geschiktheidsregels die voor elk plan zijn in gesteld. Als geen geschiktheidsregel voor een plan is ingesteld, komen er geen werknemers in aanmerking voor dat plan. 

Het systeem controleert of het compensatiebedrag dat voor een compensatieplan is opgegeven van het type schaal of schijf, binnen de minimale en maximale referentiepunten van het opgegeven compensatieniveau voor de functie van de werknemer valt. Als het compensatiebedrag buiten het toegestane bereik valt, wordt een waarschuwing of foutbericht weergegeven, afhankelijk van het tolerantieniveau dat voor het vastecompensatieplan is ingesteld.

<a name="see-also"></a>Zie ook
--------

[Compensatieplannen](compensation-plans.md)




