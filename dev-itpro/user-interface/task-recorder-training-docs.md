---
title: Documentatie of trainingen maken met Taakregistraties
description: In dit onderwerp wordt uitgelegd wat de Taakrecorder en taakbegeleidingen zijn, hoe u taakregistraties maakt en hoe u Microsoft-taakbegeleidingen aanpast en opneemt in uw Help.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: d2e1ff40f5735f69a3fcdf3a85335f157e1a1a6f
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="create-documentation-or-training-using-task-recordings"></a>Documentatie of trainingen maken met Taakregistraties

[!include[banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd wat de Taakrecorder en taakbegeleidingen zijn, hoe u taakregistraties maakt en hoe u Microsoft-taakbegeleidingen aanpast en opneemt in uw Help.

<a name="learn-about-task-recorder"></a>Meer informatie over Taakregistratie
-------------------------

Taakrecorde is een hulpmiddel in Microsoft Dynamics 365 for Operations, waarmee u acties vast kunt leggen die u uitvoert in de gebruikersinterface (UI). Wanneer u Taakregistratie gebruikt, worden alle gebeurtenissen die u in de UI uitvoert die voor de server worden uitgevoerd, inclusief het toevoegen van waarden, wijzigen van instellingen, verwijderen van gegevens, vastgelegd. De stappen die u registreert worden samen een *taakregistratie* genoemd. Taakregistraties kunnen op verschillende manieren worden gebruikt:

-   **Taakregistratie kunnen worden afgespeeld als taakbegeleidingen.** Taakbegeleidingen zijn een integraal onderdeel van ervaring in de Help van Dynamics 365 for Operations. Een taakbegeleiding is een gecontroleerde, begeleide, interactieve ervaring die u door de stappen van een taak of bedrijfsproces leidt. De gebruiker wordt door middel van een pop-upprompt (of ballon) om elke stap te voltooien, door de hele UI en het wijst naar het UI-element waarmee de gebruiker interactie aan moet gaan. De 'ballon' geeft ook informatie over het werken met het element, zoals 'Klik hier' of 'In dit veld een waarde invoeren'. Een taakbegeleiding wordt uitgevoerd op de huidige gegevensset van de gebruiker en de ingevoerde gegevens worden opgeslagen in de omgeving van de gebruiker.
-   **Taakregistraties kunnen als procedurestappen in het Help-deelvenster worden weergegeven.** U kunt het Help-deelvenster gebruiken om te zoeken naar Taakregistraties en deze weer te geven. U kunt het Help-deelvenster openen door te klikken op het pictogram **?** bovenin de navigatiebalk of u kunt de sneltoetscombinatie **Ctrl+Shift+?** gebruiken. U kunt de stappen van een taakregistratie in het Help-deelvenster lezen, of u kunt ervoor kiezen de registratie als een taakbegeleiding af te spelen zodat deze u door UI begeleidt.
-   **Taakregistraties kunnen worden opgeslagen in BPM.** U kunt uw taakregistratie opslaan op een regel van een hiërarchie in een Business Process Modeler (BPM)-bibliotheek in Lifecycle Services (LCS). Een lijst van stappen en een bedrijfsprocesstroomdiagram worden van de registratie gegenereerd. Taakregistraties die in een taak BPM-bibliotheek zijn opgeslagen, kunnen in Dynamics 365 for Operations als Help worden weergegeven.
-   **Taakregistraties kunnen als Word-documenten worden opgeslagen.** Zo kunt u eenvoudig afdrukbare trainingshandleidingen produceren.

U kunt uw eigen taakregistraties maken, door Microsoft geleverde taakregistraties afspelen of wijzigen, zodat uw configuratie wordt weerspiegelt. Voor meer informatie over Taakregistratie, zie [Taakregistratie in Dynamics 365 for Operations](task-recorder.md).

## <a name="plan-your-task-recording"></a>Uw taakregistratie plannen
Of u nou een nieuwe taakregistratie maakt of uw registratie baseert op een Microsoft-taakregistratie, houd rekening met de volgende informatie.

-   Plan de registratie zoals een video. Maak alle beslissingen op tijd.
-   Loop een of twee keer door het bedrijfsproces zonder op te nemen om de stappen te begrijpen.
-   Wanneer u door het proces loopt voordat u opneemt, let dan op waar u sneltoetsen of de toets **Enter** moet gebruiken, zodat u kunt voorkomen dat u deze daadwerkelijke opname gebruikt.
-   Bepaal het volgende:
    -   Wilt u stappen in deeltaken samen groeperen? Met deeltaken worden secties van een proces visueel onderverdeeld. Als u bijvoorbeeld een registratie voor het "Maken en uitgeven van een product" maakt, kunt u de stappen samen groeperen die zijn vereist om een product te maken, en vervolgens de stappen samen groeperen die zijn vereist om het product uit te geven. Met deeltaken zijn langere processen ook gemakkelijker te lezen.
    -   Wilt u aantekeningen toevoegen en zo ja, waar? Zie "Inzicht in verschillende typen aantekeningen" hieronder voor meer informatie.
    -   Welke waarden wilt u toevoegen in de verschillende velden terwijl u de stappen van het bedrijfsproces voltooit? Het is daarom een goed idee om te bepalen wat u selecteert of invoert terwijl u doorgaat, zodat u geen fouten hoeft op te zoeken of op te lossen terwijl u registreert.

**Schrijf op tijd de omschrijving voor aantekeningen**

-   Aan het begin van elke taakregistratie is er een omschrijvingsveld waarmee u een inleiding tot de registratie kunt invoeren. Het is daarom een goed idee om de omschrijving op tijd in een apart document te schrijven en op te slaan, zodat u de taakregistratie kunt kopiëren en plakken wanneer u registreert. Op die manier kan u de tijd besteden om de tekst te verfijnen wanneer met de registratie bezig bent. Door het knippen en plakken van de tekst gaat het registratieproces sneller en eenvoudiger.
-   Voor elke stap in een taakregistratie kunt u aantekeningen maken. Tijdens het afspelen van een taakbegeleiding verschijnen de aantekeningen in de "ballon" als notities boven of onder de tekst voor de stap. Wanneer aantekeningen worden weergegeven als tekst in het Help-deelvenster verschijnen aantekeningen inline in de stap. Zoals met de omschrijving, is het een goed idee om uw aantekeningen in een apart document te schrijven en op te slaan. Wanneer u de taakregistratie opneemt, knipt en plakt u de aantekeningen vanuit dat document.

**Inzicht in verschillende typen aantekeningen** Alle aantekeningen zijn optioneel. Voeg ze alleen toe wanneer ze nuttige informatie voor de gebruiker bevatten.

-   **Titel:** Een titelaantekening wordt weergegeven vóór de staptekst die taakregistratie automatisch genereert. In de taakbegeleiding wordt de titelaantekening weergegeven boven de automatisch gegenereerde tekst. Gebruik dit type aantekening om uit te leggen waarom de gebruiker de stap doet of om extra context te geven.

Dit is het bewerkingsdeelvenster dat u ziet wanneer u een aantekening toevoegt als u de registratie maakt. Typ een titelaantekening in het vak **Titel**. 

[![screen1](./media/screen1.png)](./media/screen1.png) 

Zo ziet de titelaantekening eruit in de "ballon" in de taakbegeleider. 

[![screen2](./media/screen2.png)](./media/screen2.png)

-   **Opmerkingen:** een notitiesaantekening wordt weergegeven na de staptekst die taakregistratie automatisch genereert. In de taakbegeleiding wordt deze alleen zichtbaar als de gebruiker op de koppeling **Meer weergeven** in de ballon van de taakbegeleiding klikt. Gebruik dit type aantekening om alles te beschrijven wat een gebruiker moet weten om de stap te voltooien.

Dit is het bewerkingsdeelvenster dat u ziet wanneer u een aantekening toevoegt als u de registratie maakt. Typ een aantekening voor notities in het vak **Notities**. 

[![screen3](./media/screen3.png)](./media/screen3.png) 

Zo ziet de notitieaantekening eruit in de 'ballon' in de taakbegeleiding.

[![screen4](./media/screen4.png)](./media/screen4.png)

-   **Info stap**: Deze aantekeningen worden gemaakt door met de rechtermuisknop te klikken op een besturingselement of overal op een formulier &lt; **Taakrecorder** &lt; **Infostap toevoegen. **Infostappen verschijnen als genummerde stap bij het punt waar u ze invoegt, zelfs als geen actie in de UI is geregistreerd. U kunt een infostap op formulierniveau toevoegen of een infostap toevoegen die aan een besturingselement is gekoppeld. Wanneer een infostap met een formulier is gekoppeld, wordt de taakbegeleidingballon ergens op het formulier weergegeven, zonder aanwijzer, wanneer de taakbegeleiding wordt afgespeeld. Wanneer een infostap aan een besturingselement is gekoppeld, wijst de taakbegeleidingballon naar het besturingselement wanneer de taakbegeleiding wordt afgespeeld. In het Help-deelvenster wordt een infostapaantekening als een genummerde stap weergegeven met de tekst u hebt ingevoerd. De stappen van de gebruiksinfo om de gebruiker voor de volgende stappen voor te bereiden, beschrijven stappen die buiten Dynamics 365 for Operations moeten worden uitgevoerd of om naar andere registraties te verwijzen (hoewel u geen hyperlinks in aantekeningen kunt maken).

**Bepaal hoe lang het duurt om de registratie te maken**

-   De gebruiker zal over het algemeen de registratie van begin tot eind lezen of afspelen, combineer dus geen stappen of taken die beter afzonderlijk kunnen worden uitgevoerd.
-   Probeer niet om een lang scenario te registreren die meerdere subprocessen omvat. Bijvoorbeeld"Helpdesk voor klanten in de winkel uitvoeren" is te breed. Deel het op in kortere taken zoals "Accepteer retouren" en "Toevoegen aan geschenkbon".
-   Als een taak als onderdeel van verschillende bedrijfsprocessen kan worden uitgevoerd, maakt u er een aparte registratie voor en kunt u ernaar verwijzen in de andere registraties.
-   Als het proces meerdere taken heeft die de persoon waarschijnlijk tegelijk doet, kunt u de taken in één registratie houden, bijvoorbeeld "Functionaliteitprofielen instellen en toewijzen".
-   Als het iets is dat iemand één keer doet (zoals configuratie) en een andere taak die ze onmiddellijk erna maar herhaaldelijk en apart kunnen doen, splitst u ze op in twee taakregistraties.

**Bepaal waar in de UI een registratie moet worden gestart** De pagina waarop u bent wanneer het opnemen van een taakregistratie start, bepaalt voor welke pagina de taakbegeleiding wordt weergegeven. Als u bijvoorbeeld wilt dat uw taakregistratie wordt vermeld in het Help-deelvenster wanneer een gebruiker klikt op de parameterspagina van Grootboek, dan moet u de registratie op die pagina starten. **Registraties opslaan als .axtr-bestanden** Wanneer u klaar bent met het maken of bewerken van een taakregistratie, krijgt u verschillende opties voor hoe u de registratie wilt downloaden of opslaan. U kunt het bestand downloaden als een taakregistratiepakket (.axtr), als onbewerkt registratiebestand (xml-bestand ) downloaden, als Word-document downloaden, of het bestand in een LCS-bibliotheek opslaan. Het is daarom een goed idee om de taakregistratie op te slaan als een taakregistratiepakketbestand (.axtr). Dit zal helpen om het onderhoud van het bestand eenvoudiger te maken als de procedures of de aantekeningen later moeten wijzigen. Als u het bestand als een Word-document wilt downloaden, slaat u het ook op als een taakregistratiepakketbestand.

## <a name="create-your-task-recording"></a>Uw taakregistratie maken
Voor gedetailleerde stapsgewijze instructies, zie [Een taakregistratie maken](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Taakregistraties van Microsoft kopiëren en aanpassen
U kunt de taakregistraties van Microsoft downloaden en bewerken om ze voor uw eigen Help-documentatie of trainingsmaterialen te gebruiken. Om een Microsoft-taakregistratie te downloaden, volgt u deze stappen:

1.  Open de Taakrecorder in Dynamics 365 for Operations Taakregistratie bevindt zich in het menu **Instellingen**.
2.  Klik in het Taakregistratie-deelvenster op **Een registratie beheren**.
3.  Klik onder **Waar is de opname?** op **Het bevindt zich in een LCS-bibliotheek**.
4.  Klik op **De LCS-bibliotheek selecteren**.
5.  Selecteer de globale bibliotheek van Microsoft.
6.  In de structuur selecteert u het knooppunt van de bedrijfsprocesbibliotheek waaraan de taakregistratie is gekoppeld.
7.  Klik tot slot op **OK**.
8.  Klik op **Start**.
9.  Op dit punt loopt u door de registratie en wijzigt u stappen om opnieuw op te nemen. **Opmerking**: Als u alleen de tekst van een registratie moet wijzigen, kunt u de registratie in de modus **Aantekeningen van een registratie bewerken** openen en vervolgens opslaan.
10. Nadat de registratie helemaal is afgespeeld, klikt u op **Stoppen** in de taakregistratiebalk boven aan het scherm.
11. Geef op hoe u de taakregistratie wilt opslaan.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Uw taakregistraties opnemen in het Help-deelvenster
Om uw eigen taakregistraties in het Help-deelvenster weer te geven zodat ze kunnen worden afgespeeld als taakbegeleidingen of als tekst, moet u uw taakregistraties opslaan in een BPM-bibliotheek, en de parameters van het Help-systeem bijwerken om naar uw BPM-bibliotheek te wijzen. Voor meer informatie, zie [Het Help-systeem verbinden](../get-started/help-connect.md).

<a name="see-also"></a>Zie ook
--------

[Dynamics 365 for Operations Help](..\get-started\help-overview.md)

[Verbinding maken met Help](..\get-started\help-connect.md)

[Taakrecorder in Dynamics 365 for Operations](task-recorder.md)

[Recentelijk toegevoegde functies in Taakrecorder](\core\get-started\recently-added-editing-features-in-task-recorder)

[Creating new training libraries for Dynamics AX within Lifecycle Services using the Task recorder (externe koppeling)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)

[Create Rich Help Topics with Task Recorder (externe koppeling)](https://mbspartner.microsoft.com/AX/Videos/970)




