---
title: Documentatie of trainingen maken met Taakregistraties
description: In dit onderwerp wordt uitgelegd welke Taakregistratie en de instructies van de taak zijn, het maken van de taakregistratie, en het aanpassen van Microsoft-taak doorloopt en deze opnemen in uw hulp.
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
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 38bce4a843f0db575c8d1ba08b7dc2ece8366663
ms.lasthandoff: 03/31/2017


---

# <a name="create-documentation-or-training-using-task-recordings"></a>Documentatie of trainingen maken met Taakregistraties
In dit onderwerp wordt uitgelegd welke Taakregistratie en de instructies van de taak zijn, het maken van de taakregistratie, en het aanpassen van Microsoft-taak doorloopt en deze opnemen in uw hulp.

<a name="learn-about-task-recorder"></a>Meer informatie over Taakregistratie
-------------------------

Taakregistratie is een Microsoft Dynamics 365 for Operations tool die u gebruiken kunt voor het vastleggen van acties die u in de product-gebruikersinterface (UI) uitvoeren. Wanneer u Taakregistratie gebruikt, worden alle gebeurtenissen die u in de UI uitvoert die voor de server worden uitgevoerd, inclusief het toevoegen van waarden, wijzigen van instellingen, verwijderen van gegevens, vastgelegd. De stappen die u registreert worden samen een *taakregistratie* genoemd. Taakregistraties kunnen op verschillende manieren worden gebruikt:

-   **Taakregistratie kunnen worden afgespeeld als taakbegeleidingen.** Taak handleidingen zijn een integraal onderdeel van de Dynamics 365 voor bewerkingen Help-ervaring. Een taak gids is een gecontroleerde geleide, interactieve ervaring door de stappen van een bedrijfsproces. De gebruiker wordt door middel van een pop-upprompt (of ballon) om elke stap te voltooien, door de hele UI en het wijst naar het UI-element waarmee de gebruiker interactie aan moet gaan. De 'bel' geeft ook informatie over het werken met het element, zoals 'Klik hier' of "In dit veld een waarde invoeren." Handleiding voor een taak wordt uitgevoerd op de huidige gegevensset van de gebruiker en de gegevens die is ingevoerd in de omgeving van de gebruiker worden opgeslagen.
-   **Taakregistratie kunnen worden weergegeven als procedurele stappen in het Help-venster.** Het Help-venster kunt u zoeken naar en Taakregistratie weer te geven. U kunt het Help-venster openen door te klikken op de **?** Pictogram in de bovenste navigatiebalk of u kunt de sneltoets drukt, **Ctrl + Shift +?**. Vindt u de stappen van een taak registreren in het Help-venster of u kunt ervoor kiezen om te worden vastgelegd als leidraad taak spelen zodat die u bij de gebruikersinterface begeleidt.
-   **Taakregistraties kunnen worden opgeslagen in BPM.** U kunt uw taakregistratie opslaan op een regel van een hiërarchie in een Business Process Modeler (BPM)-bibliotheek in Lifecycle Services (LCS). Een lijst van stappen en een bedrijfsprocesstroomdiagram worden van de registratie gegenereerd. Taakregistratie die zijn opgeslagen in een BPM-bibliotheek kunnen worden weergegeven in Dynamics 365 voor bewerkingen zoals Help.
-   **Taakregistraties kunnen als Word-documenten worden opgeslagen.** Zo kunt u eenvoudig afdrukbare trainingshandleidingen produceren.

U kunt uw eigen Taakregistratie maken, spelen Taakregistratie geleverd door Microsoft of Microsoft geleverde Taakregistratie zodat uw configuratie wijzigen. Zie voor meer informatie over de taakregistratie, [Taakregistratie in Dynamics 365 voor bewerkingen](task-recorder.md).

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
-   Voor elke stap in een taakregistratie kunt u aantekeningen maken. Tijdens het afspelen van een taakbegeleiding verschijnen de aantekeningen in de "ballon" als notities boven of onder de tekst voor de stap. Als het weergegeven als tekst in het Help-venster, worden aantekeningen weergegeven als in line tekst in de stap. Zoals met de omschrijving, is het een goed idee om uw aantekeningen in een apart document te schrijven en op te slaan. Wanneer u de taakregistratie opneemt, knipt en plakt u de aantekeningen vanuit dat document.

**Inzicht in verschillende typen aantekeningen** Alle aantekeningen zijn optioneel. Voeg ze alleen toe wanneer ze nuttige informatie voor de gebruiker bevatten.

-   **Titel**: een aantekening titel weergegeven voordat de tekst van de stap die taak recorder automatisch worden gegenereerd. In de handleiding van de taak, wordt het commentaar titel verschijnt boven de automatisch gegenereerde tekst. Gebruik dit type aantekening om uit te leggen waarom de gebruiker de stap doet of om extra context te geven.

Dit is het bewerkingsdeelvenster dat u ziet wanneer u een aantekening toevoegt als u de registratie maakt. Typ een titelaantekening in het vak **Titel**. 

[![scherm1](./media/screen1.png)](./media/screen1.png) 

Zo ziet de titelaantekening eruit in de "ballon" in de taakbegeleider. 

[![--scherm2](./media/screen2.png)](./media/screen2.png)

-   **Opmerkingen:** een notitiesaantekening wordt weergegeven na de staptekst die taakregistratie automatisch genereert. In de taakbegeleiding wordt deze alleen zichtbaar als de gebruiker op de koppeling **Meer weergeven** in de ballon van de taakbegeleiding klikt. Gebruik dit type aantekening om alles te beschrijven wat een gebruiker moet weten om de stap te voltooien.

Dit is het bewerkingsdeelvenster dat u ziet wanneer u een aantekening toevoegt als u de registratie maakt. Typ een aantekening voor notities in het vak **Notities**. 

[![screen3](./media/screen3.png)](./media/screen3.png) 

Dit is het commentaar notities ziet er als in de 'bel' in de handleiding van de taak.

[![screen4](./media/screen4.png)](./media/screen4.png)

-   **Info stap**: deze aantekeningen worden gemaakt met de rechtermuisknop te klikken op een besturingselement of een willekeurige plaats in een formulier &lt;**Taakregistratie**&lt; ** info-stap toevoegen. ** Info stappen worden weergegeven als een genummerde stap op de plaats van u het invoegen, zelfs als er geen actie is vastgelegd in de gebruikersinterface. U kunt een infostap op formulierniveau toevoegen of een infostap toevoegen die aan een besturingselement is gekoppeld. Wanneer een infostap met een formulier is gekoppeld, wordt de taakbegeleidingballon ergens op het formulier weergegeven, zonder aanwijzer, wanneer de taakbegeleiding wordt afgespeeld. Wanneer een stap info gekoppeld aan een besturingselement is, verwijst een handleiding voor de taak 'bel' naar het besturingselement bij het afspelen van de handleiding van de taak. In het Help-venster wordt info stap commentaar weergegeven als een genummerde stap met de tekst die u hebt ingevoerd. Info stappen gebruik te maken van de gebruiker voor de volgende stappen beschrijven de stappen die moet worden gedaan buiten Dynamics 365 for Operations of om te verwijzen naar andere opnamen (Hoewel u geen hyperinks maken in aantekeningen.).

**Bepaal hoe lang het duurt om de registratie te maken**

-   De gebruiker zal over het algemeen de registratie van begin tot eind lezen of afspelen, combineer dus geen stappen of taken die beter afzonderlijk kunnen worden uitgevoerd.
-   Probeer niet om een lang scenario te registreren die meerdere subprocessen omvat. Bijvoorbeeld"Helpdesk voor klanten in de winkel uitvoeren" is te breed. Deel het op in kortere taken zoals "Accepteer retouren" en "Toevoegen aan geschenkbon".
-   Als een taak als onderdeel van verschillende bedrijfsprocessen kan worden uitgevoerd, maakt u er een aparte registratie voor en kunt u ernaar verwijzen in de andere registraties.
-   Als het proces meerdere taken heeft die de persoon waarschijnlijk tegelijk doet, kunt u de taken in één registratie houden, bijvoorbeeld "Functionaliteitprofielen instellen en toewijzen".
-   Als het iets is dat iemand één keer doet (zoals configuratie) en een andere taak die ze onmiddellijk erna maar herhaaldelijk en apart kunnen doen, splitst u ze op in twee taakregistraties.

**Bepaalt waar in de gebruikersinterface, opname moet starten** de pagina waarop u zich bevindt wanneer u start het vastleggen van de registratie van een taak is van invloed op welke pagina voor de handleiding van de taak weergegeven. Als u wilt dat het registreren van uw taak om te worden vermeld in het Help-venster wanneer een gebruiker op Help op de pagina van de parameters voor het grootboek, moet u de opname starten op de pagina van de parameters voor het grootboek. **Registraties opslaan als .axtr-bestanden** Wanneer u klaar bent met het maken of bewerken van een taakregistratie, krijgt u verschillende opties voor hoe u de registratie wilt downloaden of opslaan. U kunt het bestand downloaden als een taakregistratiepakket (.axtr), als onbewerkt registratiebestand (xml-bestand ) downloaden, als Word-document downloaden, of het bestand in een LCS-bibliotheek opslaan. Het is daarom een goed idee om de taakregistratie op te slaan als een taakregistratiepakketbestand (.axtr). Dit zal helpen om het onderhoud van het bestand eenvoudiger te maken als de procedures of de aantekeningen later moeten wijzigen. Als u het bestand als een Word-document wilt downloaden, slaat u het ook op als een taakregistratiepakketbestand.

## <a name="create-your-task-recording"></a>Uw taakregistratie maken
Zie voor gedetailleerde overzicht stappen, [het maken van een taak vastleggen](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Taakregistraties van Microsoft kopiëren en aanpassen
U kunt downloaden en bewerken van de taakregistratie van Microsoft om ze te gebruiken voor uw eigen Help-documentatie of de trainingsmaterialen. Om een Microsoft-taakregistratie te downloaden, volgt u deze stappen:

1.  Open in Dynamics 365 for Operations, Taakregistratie. Taakregistratie bevindt zich in het menu **Instellingen**.
2.  Klik in het Taakregistratie-deelvenster op **Een registratie beheren**.
3.  Klik onder **Waar is de opname?** op **Het bevindt zich in een LCS-bibliotheek**.
4.  Klik op **De LCS-bibliotheek selecteren**.
5.  Selecteer de algemene bibliotheek van Microsoft.
6.  In de structuur selecteert u het knooppunt van de bedrijfsprocesbibliotheek waaraan de taakregistratie is gekoppeld.
7.  Klik tot slot op **OK**.
8.  Klik op **Start**.
9.  Op dit moment stap tot en met de registratie, stappen wijzigen terwijl u deze nog een keer opnemen. **opmerking**: als u alleen de tekst van een opname wijzigen wilt, opent u de opname in **aantekeningen van een registratie bewerken** modus, en vervolgens op te slaan.
10. Nadat de registratie helemaal is afgespeeld, klikt u op **Stoppen** in de taakregistratiebalk boven aan het scherm.
11. Geef op hoe u de taakregistratie wilt opslaan.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Uw Taakregistratie opnemen in het Help-venster
Als uw eigen aangepaste Taakregistratie in het Help-venster weergeven, zodat ze kunnen worden afgespeeld als leidraad taak of als tekst weergegeven, moet u uw Taakregistratie opslaan in uw eigen BPM-bibliotheek en werk vervolgens uw Help-systeemparameters om te verwijzen naar de BPM-bibliotheek. Zie voor meer informatie [verbinding maken met het Help-systeem.](../get-started/help-connect.md)

<a name="see-also"></a>Zie ook
--------

[Help bij Dynamics 365 voor bewerkingen](..\get-started\help-overview.md)

[Verbinding maken met Help](..\get-started\help-connect.md)

[Taakregistratie in Dynamics 365 voor bewerkingen](task-recorder.md)

[Taakfuncties recorder als laatste is toegevoegd](\core\get-started\recently-added-editing-features-in-task-recorder)

[Nieuwe opleiding bibliotheken maken voor Dynamics AX binnen Lifecycle Services met behulp van Taakregistratie (externe koppeling)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)

[Uitgebreide Help-onderwerpen met Taakregistratie (externe koppeling) maken](https://mbspartner.microsoft.com/AX/Videos/970)


