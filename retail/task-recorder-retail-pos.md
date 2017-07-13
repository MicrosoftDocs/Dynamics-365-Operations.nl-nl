---
title: Taakrecorder en Help voor POS
description: In dit onderwerp wordt beschreven hoe u Taakrecorder gebruikt in Retail Modern POS en Cloud POS.
author: mugunthanm
manager: AnnBe
ms.date: 06/19/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: 41
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 1205393
ms.assetid: 2f13e9cf-55b5-458b-8c32-3f8cd98c9ecf
ms.search.region: Global
ms.industry: Retail
ms.author: mumani
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 59b51840c05fe649cf322bfa64737a321728a5aa
ms.openlocfilehash: 007a7e8a34f3f5a2d0d18eb3955822a8fd8bdd0a
ms.contentlocale: nl-nl
ms.lasthandoff: 06/20/2017


---

# <a name="task-recorder-and-help-for-pos"></a>Taakrecorder en Help voor POS

In dit onderwerp wordt beschreven hoe u Taakrecorder gebruikt in Retail Modern POS en Cloud POS.

<a name="overview"></a>Overzicht
--------

Taakrecorder in Retail Modern POS of Cloud POS is een nieuwe oplossing die is gemaakt met het oog op hoge responsiviteit. Het biedt een flexibele Application Programming Interface (API) voor uitbreidbaarheid en naadloze integratie met gebruikers van zakelijke procesregistraties. Bovendien is integratie van Taakrecorder met het hulpprogramma Business process modeller (BPM) in Microsoft Dynamics Lifecycle Services ([https://bpm.lcs.dynamics.com](https://bpm.lcs.dynamics.com/)) verbeterd. Daarom kunnen gebruikers doorgaan met het produceren van uitgebreide bedrijfsprocesdiagrammen van registraties om hun toepassingen te analyseren en te ontwerpen.

## <a name="architecture"></a>Architectuur
Taakrecorder kan gebruikersacties in de client registreren met exacte betrouwbaarheid. Elk besturingselement wordt ontworpen om Taakrecorder te informeren over de uitvoering van een gebruikersactie. Het besturingselement informeert Taakrecorder dat een gebeurtenis heeft plaatsgevonden en geeft alle relevante informatie over de bijbehorende gebruikersactie in real-time door. Met deze informatie kan Taakrecorder het soort gebruikersactie vastleggen (zoals een klik op een knop, waarde-invoer of navigatie) en alle gegevens die zijn gerelateerd aan de gebruikersactie (zoals de ingevoerde gegevenswaarde en -type, de formuliercontext of de recordcontext). Taakrecorder behoudt de informatie met voldoende details om te garanderen dat als de registratie wordt afgespeeld, de gebruikersacties exact zo worden afgespeeld als de gebruiker ze heeft uitgevoerd. (De functie voor het afspelen is nog niet geïmplementeerd in Retail Modern POS of Cloud POS.)

## <a name="basic-configuration"></a>Basisconfiguratie
Ga als volgt te werk om taakregistratie in POS in te schakelen.

1.  Klik op **Retail** &gt; **Kanaalinstelling** &gt; **POS-instellingen** &gt; **Kassa's**.
2.  Klik op de kassa om taakregistratie in te schakelen.
3.  Stel op het tabblad **Registreren** op het sneltabblad **Algemeen** de optie **Taakregistratie inschakelen** in op **Ja**.
4.  Klik op **Opslaan**.
5.  Klik op **Retail** &gt; **IT detailhandel** &gt; **Distributieplanning**.
6.  Selecteer de taak **1090, kassa's** en klik vervolgens op **Nu uitvoeren**.

## <a name="create-a-recording"></a>Een registratie maken
Volg deze stappen om een nieuwe registratie te maken met Taakrecorder.

1.  Start Retail Modern POS of Cloud POS en meld u aan.
2.  Klik op de pagina **Instellingen** in het gedeelte **Taakrecorder** op **Taakregistratie openen**. Het deelvenster **Taakrecorder** wordt weergegeven. U kunt klikken op de knop **Sluiten** (**X**) in de rechterbovenhoek om het deelvenster **Taakrecorder** te sluiten voordat u een nieuwe registratie start. Als u het deelvenster weer wilt openen, herhaalt u stap 2.
[![Deelvenster Taakrecorder](./media/newrecording-1024x450.jpg)](./media/newrecording.jpg)

3.  Voer een naam en omschrijving voor de registratie in en klik vervolgens op **Start**. De registratiesessie begint zodra u klikt op **Start**.

**Opmerking:** als u op de knop **Sluiten** (**X**) in de rechterbovenhoek klikt terwijl de registratie wordt uitgevoerd, wordt het deelvenster **Taakrecorder** gesloten, maar wordt de registratiesessie niet beëindigd. Klik op de knop **Help** (vraagteken) boven aan het scherm om het deelvenster Taakrecorder weer te openen. 

[![Vraagteken](./media/help.jpg)](./media/help.jpg)

4.  Nadat u op **Starten** hebt geklikt, gaat Taakrecorder in de registratiemodus. Het deelvenster **Taakrecorder** bevat informatie en besturingselementen die zijn gerelateerd aan het registratieproces.
5.  Voer de acties uit die u wilt uitvoeren in de interface (UI) van Retail Modern POS of Cloud POS.
6.  Als u de registratiesessie wilt beëindigen, klikt u op **Stoppen**.

## <a name="download-options"></a>Opties voor downloaden
Nadat u de registratiesessie hebt beëindigd, worden verschillende opties weergegeven, zodat u uw registratie kunt downloaden. 
[![Opties voor downloaden](./media/downlaod-options.jpg)](./media/downlaod-options.jpg)

### <a name="save-to-this-pc"></a>Opslaan op deze pc

U kunt het registratiepakket gebruiken om een taakbegeleider af te spelen, de registratie te onderhouden of de aantekeningen in de registratie te bewerken. (Deze functie is nog niet geïmplementeerd in Retail Modern POS of Cloud POS.)

### <a name="export-as-word-document"></a>Exporteren als Word-document

U kunt de registratie opslaan als Microsoft Word-document. Het document bevat de geregistreerde stappen en de schermopnamen die zijn gemaakt.

### <a name="save-as-developer-recording"></a>Opslaan als ontwikkelaarsregistratie

Het ruwe registratiebestand is nuttig voor ontwikkelaarsscenario's, zoals het genereren van testcode. (Deze functie is niet nog geïmplementeerd.)

## <a name="recording-controls"></a>Besturingselementen voor registratie
### <a name="recording-controlsmediacontrolsjpgmediacontrolsjpg"></a>[![Besturingselementen voor registratie](./media/controls.jpg)](./media/controls.jpg)

### <a name="stop"></a>Stoppen

Als u de registratiesessie wilt beëindigen, klikt u op **Stoppen**. Houd er rekening mee dat u een sessie na het beëindigen ervan niet opnieuw kunt starten. Zorg er daarom voor dat de registratie is voltooid voordat u deze beëindigt.

### <a name="pause"></a>Pauze

Klik op **Onderbreken** om de registratiesessie tijdelijk te stoppen (pauzeren) en ga door met de bewerking. Stappen die u uitvoert nadat u op **Onderbreken** hebt geklikt, worden niet geregistreerd.

### <a name="continue"></a>Doorgaan

Als u de opnamesessie wilt hervatten nadat u deze hebt onderbroken, klikt u op **Doorgaan**.

### <a name="capture-screenshots"></a>Schermopnamen maken

Taakrecorder kan schermopnamen maken van de gebruikersinterface van Retail Modern POS, terwijl u een bedrijfsproces registreert. Taakrecorder gebruikt de schermopnamen als u de registratie downloadt als een Word-document. Als u de functie voor het maken van schermopnamen wilt aanzetten, stelt u de optie **Schermopnamen maken** in op **Ja**. 

#### <a name="note"></a>Opmerking
> Functionaliteit voor het maken van schermopnamen wordt niet ondersteund in Cloud POS.

### <a name="start-task-and-end-task"></a>Taak starten en taak beëindigen

U kunt het begin en einde van een set gegroepeerde stappen opgeven met behulp van de knoppen **Taak starten** en **Taak** **beëindigen**. Klik op **Taak starten** om een 'Taak starten'-taak toe te voegen en voer vervolgens de stappen uit die in de groep moeten worden opgenomen. Als u klaar bent met het uitvoeren van de stappen voor de groep, klikt u op **Taak beëindigen**. Taken helpen u uw procedures te organiseren. Taken kunnen worden genest binnen andere taken. Zo kunt u zeer lange en complexe bedrijfsprocessen beter organiseren.

## <a name="adding-annotations"></a>Aantekeningen toevoegen
Een aantekening is aanvullende tekst die u aan een stap in een registratie kunt toevoegen. U kunt bijvoorbeeld aantekeningen gebruiken om de gebruiker meer context of instructies te geven. U kunt aantekeningen toevoegen vóór of na een stap. U kunt een aantekening aan iedere stap toevoegen door te klikken op de knop **Bewerken** (potloodsymbool), rechts van de stap. 

[![Knop Bewerken voor een stap](./media/annotate.jpg)](./media/annotate.jpg)

### <a name="texts-and-notes"></a>Tekst en notities

U kunt de velden **Teksten** en **Notities** gebruiken om tekst toe te voegen die moet worden gekoppeld aan een stap in een taakbegeleider.
[![Tekst- en notitievelden](./media/annotatesteps.jpg)](./media/annotatesteps.jpg)

#### <a name="text"></a>Tekst

Tekst die u invoert in het veld **Tekst**, verschijnt *boven* de staptekst in de taakbegeleider. Deze locatie is geschikt voor tekst die de gebruiker moet lezen voordat hij of zij de stap voltooit.

#### <a name="notes"></a>Opmerkingen

Tekst die u invoert in het veld **Notities**, verschijnt *onder* de staptekst in de taakbegeleider. Als de gebruiker de tekst wil lezen, moet deze de staptekst in het pop-upvenster uitvouwen. Deze locatie is geschikt voor optionele tekst of andere informatie die van belang kan zijn voor de gebruiker, maar die de gebruiker niet hoeft te lezen om de actie te voltooien.

## <a name="help-in-retail-modern-pos-and-cloud-pos"></a>Help in Retail Modern POS en Cloud POS
Om uw eigen taakregistraties in het Help-deelvenster van Retail Modern Pos en Cloud POS weer te geven zodat ze kunnen worden afgespeeld als taakbegeleidingen of als tekst, moet u uw taakregistraties opslaan in een BPM-bibliotheek, en de parameters van het Help-systeem bijwerken om naar uw BPM-bibliotheek te wijzen. Zie voor meer informatie het onderwerp [Verbinding maken met het Help-systeem.](/dynamics365/unified-operations/dev-itpro/get-started/help-connect) Retail Modern POS en Cloud POS Help doorzoekt LCS in real-time. Alle BPM-bibliotheken worden doorzocht die zijn geselecteerd in de parameters van het Microsoft Dynamics 365 for Retail Help-systeem, en de relevante resultaten worden weergegeven. Voor toegang tot het menu **Help** klikt u op de knop **Help** (vraagteken) bovenaan het scherm, typt u vervolgens in het zoekvak uw procesnaam en klikt u op de zoekknop. 

[![De knop Help](./media/help.jpg)](./media/help.jpg) 

Wanneer u op de taakbegeleider in de zoekresultaten klikt, kunt u de stappen weergeven als een Help-onderwerp of een Word-document. 
#### <a name="note"></a>Opmerking
> Help in Retail Modern POS en Cloud POS opent geen taakbegeleiding op basis van het formulier waar u zich bevindt of de bewerking die u uitvoert. U moet de procesnaam in het zoekvak typen en op **Zoeken** klikken.


