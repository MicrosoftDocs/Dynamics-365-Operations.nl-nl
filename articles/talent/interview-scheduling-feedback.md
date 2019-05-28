---
title: Plannen van sollicitatiegesprekken en feedback
description: Dit onderwerp biedt informatie over het plannen van sollicitatiegesprekken en feedbackactiviteiten in Attract.
author: hasrivas
manager: AnnBe
ms.date: 04/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.search.region: Global
ms.author: shielas
ms.openlocfilehash: 39b14f3ca855ca283a7484e480ff2547623938ef
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517699"
---
# <a name="interview-scheduling-and-feedback"></a>Plannen van sollicitatiegesprekken en feedback

[!include[banner](../includes/banner.md)]

## <a name="scheduler-activity"></a>Planneractiviteit

De planneractiviteit is optioneel en bestaat uit twee onderdelen: Beschikbaarheid van kandidaat aanvragen en Planning. Met de component Beschikbaarheid van kandidaat kunt u e-mail gebruiken om te informeren naar de beschikbaarheid van een kandidaat. De component Planning biedt de mogelijkheid sollicitatiegesprekken met de kandidaat en het aanstellend team te plannen.

Als u de planneractiviteit wilt instellen om in te plannen kandidaten op te nemen of uit te sluiten, selecteert u een waarde in het veld **Wie plant u in**. De beschikbare opties zijn **Alle kandidaten**, **Externe kandidaten** en **Interne kandidaten**. Als u bijvoorbeeld interne kandidaten in de eerste planningsronde wilt overslaan, kunt u de planningsactiviteit plannen alleen aan externe kandidaten toewijzen door **Wie plant u in** in te stellen op **Externe kandidaten**.

### <a name="candidate-availability-request"></a>Beschikbaarheid van kandidaat aanvragen

Als u een e-mail naar kandidaten stuurt om te informeren naar hun beschikbaarheid, selecteert u het veld **Beschikbaarheid van kandidaat aanvragen**. Als het veld niet is geselecteerd, wordt deze stap niet weergegeven in het aanstellingsproces voor de functie.

Als u de beschikbaarheidsaanvraag wilt verzenden, klikt u op **Aanvraag verzenden**, kiest u de beschikbare datums en een e-mailsjabloon en verzendt u het e-mailbericht vervolgens naar de kandidaat.

[![Attract Recruiter-weergave voor het verzenden van de aanvraag naar beschikbaarheid van kandidaat](./media/scheduler-candidate-request.png)](./media/scheduler-candidate-request.png)

Wanneer de kandidaat een e-mailbericht ontvangt om te reageren op de aanvraag, kan deze zich aanmelden bij de kandidaatportal, de datums kiezen die overeenkomen met de beschikbaarheid en klikken op **Indienen**.

### <a name="schedule"></a>Planning
Er zijn meerdere configuraties beschikbaar voor de planner van sollicitatiegesprekken om de cyclus van sollicitatiegesprekken te gebruiken, snel te maken en te verzenden naar de interviewers en de kandidaat.

1. Klik op **Planning maken** en geef in het vak **Interviewers toevoegen** alle interviewers weer die deel gaan uitmaken van de cyclus van sollicitatiegesprekken.
[![Attract Recruiter-weergave om de planning van een cyclus sollicitatiegesprekken te starten](./media/schedule-start-over.png)](./media/schedule-start-over.png)   
    Als kandidaten hebben gereageerd op de aanvraag voor een sollicitatiegesprek , wordt de **Datum van sollicitatiegesprek** vooraf ingevuld met hun selectie. U kunt zo nodig een andere datum selecteren.
    
    Als u het veld **Hiervan een vraaggesprekdeelvenster maken** selecteert, wordt de groep van interviewers aan de linkerkant verplaatst naar een cyclus van één deelvenster om het sollicitatiegesprek te maken. Vervolgens moet u een specifieke reeks definiëren voor de sollicitatiegesprekken.
    
    De sollicitatiegesprekplanning moet zo worden geordend dat deze zo goed mogelijk overeenkomt met de beschikbaarheid van de deelnemers. Als het om interne kandidaten gaat, kunt u hun beschikbaarheid opnemen als onderdeel van de planningsaanbeveling.
    
    Voor een on line vergadering selecteert u het veld **Online Skype-vergaderingen toevoegen** en elke gespreksgebeurtenis heeft de koppeling**Skype voor Bedrijven** beschikbaar.

2. Selecteer de duur van het sollicitatiegesprek voor elke sollicitatiegespreksgebeurtenis en klik vervolgens op **OK** om te beginnen met het maken van de planning.

    Als **Aanbevelingen** is geselecteerd, worden suggesties weergegeven en wordt het raster met sollicitatiegesprekken vooraf ingevuld. U ziet mogelijk de huidige kalenderbeschikbaarheid van alle geselecteerde interviewers. U ziet mogelijk ook de kalender van de kandidaat als het om een interne kandidaat gaat. Voor de interviewers en interne kandidaten kunt u bekijken wanneer ze bezet zijn, wat hun werkuren zijn, wanneer ze niet op kantoor zijn en kunt u ook bepalen of ze in hun agenda hebben aangegeven dat ze elders werken gedurende bepaalde tijdvakken. 

3. Als er geen suggesties beschikbaar zijn in de kolom **Interviewers**, klikt u in een tijdsperiode, geeft u de titel en details van het gesprek op en vult u zo nodig de locatiegegevens in. U kunt ervoor kiezen de koppeling **Skype voor Bedrijven** voor het gesprek op te nemen.

4. Als u extra interviewers wilt opnemen, klikt u op de rasterkolom **Sollicitatiegesprek toevoegen** om een of meer interviewers te selecteren. U kunt de optie met drie puntjes (...) gebruiken om een gesprek te verwijderen uit de cyclus.
    
5. Als de sollicitatiegesprekken worden gepland in een andere tijdzone, kiest u de vereiste plaats/tijdzone in de vervolgkeuzelijst in de rechterbovenhoek. Het raster van de beschikbaarheid van de interviewer wordt bijgewerkt om de nieuwe tijdzone weer te geven. Deze tijdzoneselectie wordt nu ook weergegeven in de weergave **Overzicht sollicitatiegesprek** die wordt gedeeld met de interviewers en de kandidaat. 

6. Klik op **Verzenden naar interviewers** om de uitnodiging voor de bijeenkomst naar de betrokken interviewers te verzenden.

    Nadat de sollicitatiegesprekaanvragen zijn verzonden naar de interviewers, kunnen ze rechtstreeks reageren via de uitnodiging per e-mail die ze ontvangen.

    >[!NOTE]
    > Voor alle 1-op-1-gesprekken worden elke 24 uur herinneringen verzonden naar de interviewers als de interviewer niet geeft gereageerd op het interviewverzoek (geaccepteerd of geweigerd).

    > Voor alle panelgesprekken worden er geen geautomatiseerde herinneringen verzonden voor de sollicitatiegesprekaanvraag. Als u handmatig een herinnering wilt activeren, bewerkt u het gesprek en gebruikt u de optie **Bijwerken en verzenden** om het verzoek terug te sturen naar de interviewers.

    Reacties van interviewers worden vastgelegd en weergegeven in Attract. Als een interviewer de uitnodiging weigert, wordt u geïnformeerd om een wijziging aan te brengen. Als u hun reactie in de rasterweergave **Planner** wilt weergeven, klikt u op het ballonpictogram.

[![Attract Recruiter-weergave van de reactie van een interviewer](./media/schedule-interviewer-response2.png)](./media/schedule-interviewer-response2.png)

7. Nadat de planning van het sollicitatiegesprek klaar is om te worden gedeeld met de kandidaat, klikt u op **Verzenden naar kandidaat**. U kunt ervoor kiezen de namen van de interviewer en de tijdvakken voor de kandidaat te verbergen of weer te geven.

8. Selecteer een e-mailsjabloon en verzend het sollicitatiegespreksoverzicht naar de kandidaat. Kandidaten kunnen deze informatie in hun e-mail weergeven, maar ook in hun kandidaatportal.
    
>[!NOTE] 
> De kalenderbeschikbaarheid van een kandidaat wordt alleen weergegeven als de kandidaat intern is. Zo ook kunnen alleen interne kandidaten worden gebruikt om aanbevelingen voor gespreksplanning te verbeteren. Op dit moment ontvangen kandidaten (extern of intern) geen uitnodiging voor een bijeenkomst per e-mail. Ze ontvangen alleen een overzicht van de gesprekken.

Kandidaten ontvangen het e-mailbericht waarin een overzicht wordt gegeven van hun cyclus van sollicitatiegesprekken. De e-mailberichten bevatten een ICS-bestand dat kan worden opgeslagen in hun persoonlijke agenda´s voor eenvoudigere toegang en meldingen over het sollicitatiegesprek.

>[!TIP] 
> Als u de planning van het sollicitatiegesprek opnieuw naar de kandidaat verzendt, ontvangt deze een andere ICS-bestandsbijlage. Het is raadzaam om de e-mailsjablonen voor het overzicht van het sollicitatiegesprek van de kandidaat bij te werken om ervoor te zorgen dat kandidaten de eerder toegevoegde gespreksgebeurtenissen verwijderen zodat ze geen dubbele records in hun agenda zien. 

## <a name="feedback-activity"></a>Feedback activiteit

De feedbackactiviteit is optioneel in een taaksjabloon. Met deze activiteit kunnen deelnemers aan sollicitatiegesprekken aanbevelingen of feedbackopmerkingen invoeren voor een sollicitant. 

Als u wilt bepalen voor welke kandidaten feedback moet worden gegeven of niet, selecteert u een waarde in het veld **Voor wie moeten interviewers feedback geven**.  De beschikbare opties zijn **Alle kandidaten**, **Externe kandidaten** en **Interne kandidaten**. Als u interne kandidaten bijvoorbeeld in de eerste planningsronde wilt overslaan, stelt u **Voor wie moeten interviewers feedback geven** in op **Externe kandidaten**.

Als u het veld **Feedback deelnemers overnemen van aanstellingsteam** selecteert, worden de werver, de aanstellende manager en de interviewers automatisch ingevoerd in de feedbackactiviteit. Organisaties kunnen interviewers toestaan de feedback van anderen weer te geven voordat ze hun eigen feedback indienen. Organisaties kunnen interviewers ook toestaan hun feedback te bewerken nadat zij deze hebben ingediend. Interviewers worden eraan herinnerd om feedback voor de gesprekken die ze onlangs hebben gehad in te dienen op basis van de vooraf ingestelde configuratie als onderdeel van de taaksjabloon. De aanstellingsmanager of een werver voor de functie kan er ook voor kiezen een interviewer er handmatig aan te herinneren om feedback in te dienen.

## <a name="interview-activity"></a>Interviewactiviteit

De sollicitatiegesprekactiviteit is een optionele activiteit met drie componenten: **Beschikbaarheid van kandidaat aanvragen**, **Planning** en **Feedback**. Gebruik de sollicitatiegesprekactiviteit in de functiesjabloon als u de beschikbaarheidsaanvraag van de kandidaat, de planning en feedback wilt opnemen als onderdeel van het proces in plaats van deze afzonderlijk als onderdeel van het aanstellingsproces te gebruiken.

Als u wilt bepalen met welke kandidaten u een sollicitatiegesprek wilt voeren, selecteert u een waarde in het veld **Met wie voert u een sollicitatiegesprek**. De beschikbare opties zijn **Alle kandidaten**, **Externe kandidaten** en **Interne kandidaten**. Als u interne kandidaten bijvoorbeeld in de eerste ronde van sollicitatiegesprekken wilt overslaan, stelt u **Met wie voert u een sollicitatiegesprek** in op **Externe kandidaten**.
