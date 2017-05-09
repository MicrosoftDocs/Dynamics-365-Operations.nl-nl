---
title: Het Help-systeem verbinden
description: In dit onderwerp worden de onderdelen van het Help-systeem voor Microsoft Dynamics 365 for Operations beschreven en vindt u een overzicht van de wijze waarop u deze verbindt. Daarnaast wordt beknopt aangegeven hoe u aangepaste Help maakt.
author: margoc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 5ac5e30cff2239f601778001368fa7aaba478f5c
ms.lasthandoff: 03/31/2017


---

# <a name="connect-the-help-system"></a>Het Help-systeem verbinden

In dit onderwerp worden de onderdelen van het Help-systeem voor Microsoft Dynamics 365 for Operations beschreven. Het bevat een overzicht van hoe deze onderdelen met elkaar zijn verbonden, en een samenvatting hoe u aangepaste Help kunt maken. 

<a name="help-architecture"></a>Help-architectuur
-----------------

De volgende afbeelding toont de onderdelen van het Help-systeem van Dynamics 365 for Operations. Het in-product Help-systeem haalt artikelen op uit de Dynamics 365 for Operations-site op https://docs.microsoft.com, evenals taakbegeleidingen die zijn opgeslagen in Business Process Modeler in Lifecycle Services (LCS). 
**Opmerking:** de functies in het diagram met een sterretje (\*) zijn gepland, maar zijn nog niet beschikbaar. [![Help-architectuur](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Verbinding maken met het Help-systeem
Met de pagina **Systeemparameters** verbinden systeembeheerders de delen van het Help-systeem voor een implementatie. [![Formulier Systeemparameters met Help-instellingen](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Voer de volgende stappen uit op de pagina **Systeemparameters**:

1.  **Belangrijk:** de eerste keer dat u het **Help**-tabblad opent, moet u verbinding maken met Lifecycle Services. Zorg ervoor dat u op de koppeling in het midden van het formulier klikt, wacht op de verbinding, sluit het dialoogvenster en klik op **OK** om de pagina **Systeemparameters** op te halen[![Verbinden met LCS](./media/connect-to-lcs-crop-1024x365.png "Verbinden met LCS")](./media/connect-to-lcs-crop.png)
2.  Selecteer het project Lifecycle Services om verbinding mee te maken.
3.  Selecteer de BPM-bibliotheken (in het geselecteerde project) om taakregistraties op te halen.
4.  Stel de weergavevolgorde van de BPM-bibliotheken in. Dit bepaalt de volgorde waarin de taakregistraties uit de bibliotheken verschijnen in het deelvenster **Help**.

Nadat u deze stappen hebt voltooid, kunt u het deelvenster **Help** openen en op het tabblad **Taakbegeleidingen** klikken. U ziet nu de taakbegeleidingen die van toepassing zijn op de pagina die nu is geopend in Dynamics 365 for Operations. Als er geen taakbegeleidingen worden gevonden, kunt u trefwoorden invoeren om uw zoekopdracht te verfijnen.

### <a name="showing-translated-task-guides"></a>Vertaalde taakbegeleidingen weergeven

Vertaalde taakbegeleidingen zijn voor het eerst verzonden in de APQC Unified Library van mei 2016 en de Aan de slag-bibliotheek. Als u in Dynamics 365 for Operations gelokaliseerde help met taakbegeleiding wilt zien, moet u ervoor zorgen verbonden te zijn met de bibliotheek van mei. De taal waarin een taakbegeleiding wordt weergegeven, wordt voor elke gebruiker bepaald door de instellingen voor taal onder **Opties** &gt; **Voorkeuren**. **Opmerking:** hoewel veel taakbegeleidingen zijn vertaald, worden momenteel in de Dynamics 365 for Operations-client de vertaalde namen van taakbegeleidingen niet weergegeven. Ook zijn op dit moment alleen de taakbegeleidingen die in februari 2016 zijn uitgebracht beschikbaar in vertaling in de bibliotheek voor mei. Wij zullen een bijgewerkte bibliotheek met extra vertalingen uitbrengen.

-   Als een taakbegeleiding is vertaald, wordt bij het openen van die taakbegeleiding alle tekst van de taakbegeleiding weergegeven in uw geselecteerde taal.
-   Als een taakbegeleiding nog niet is vertaald, wordt bij het openen van die taakbegeleiding alleen bepaalde tekst (de tekst van de besturingselementen) weergegeven in uw geselecteerde taal.

## <a name="creating-custom-help"></a>Aangepaste Help maken
U kunt voor aangepaste Help voor uw implementatie van Dynamics 365 for Operations maken door uw taakregistraties maken die uw implementatie weerspiegelen en ze op te slaan in een LCS-bibliotheek voor bedrijfsprocessen. Voor partners: als u een bibliotheek propageert als bedrijfsbibliotheek en deze in een oplossing opneemt, wordt deze beschikbaar voor uw klanten. U kunt een kopie van de globale APQC Unified-bibliotheek maken en vervolgens uw kopie openen, hierin taakregistraties openen, deze wijzigen en de registraties met uw wijzigingen opslaan. Zie [Een taakregistratie voor een documentatie of training maken](../user-interface/task-recorder.md) voor meer informatie.

<a name="see-also"></a>Zie ook
--------

[Help-overzicht](help-overview.md)

[Overzicht taakrecorder](../user-interface/task-recorder.md)

[Een taakregistratie voor een documentatie of training maken](../user-interface/task-recorder-training-docs.md)

[Creating New Training Libraries for Dynamics 365 for Operations within Lifecycle Services using the Task Recorder (externe koppeling)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)


