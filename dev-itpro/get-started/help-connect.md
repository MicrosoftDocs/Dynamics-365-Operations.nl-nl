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

Dit onderwerp beschrijft de onderdelen van het Help-systeem voor Microsoft Dynamics 365 voor bewerkingen. Deze biedt een overzicht van hoe deze onderdelen verbindt en een overzicht van het maken van aangepaste help. 

<a name="help-architecture"></a>Help-architectuur
-----------------

De volgende afbeelding ziet de onderdelen van de Dynamics 365 for Operations Help-systeem. De productspecifieke Help-systeem haalt artikelen uit de Dynamics 365 voor bewerkingen site op https://docs.microsoft.com, alsmede taak handleidingen in proces bedrijfsmodelleur in Lifecycle Services (LCS) opgeslagen. 
**opmerking:** de functies die worden vermeld in het diagram met een sterretje (\*) zijn gepland, maar nog niet beschikbaar. [![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Het Help-systeem verbinden
Met behulp van de **systeemparameters** pagina systeembeheerders de delen van het Help-systeem voor een implementatie. [![Formulier Systeemparameters met Help-instellingen](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) op de **systeemparameters** pagina, als volgt te werk:

1.  **Belangrijk:** de eerste keer dat u opent de **Help** tabblad, u moet verbinding maken met Lifecycle Services. Zorg ervoor dat op de koppeling klikken in het midden van het formulier, wachten op de verbinding sluit het dialoogvenster en klik vervolgens op **OK** naar de **systeemparameters** pagina. [![Verbinding maken met Kredietbrieven](./media/connect-to-lcs-crop-1024x365.png "verbinding maken met Kredietbrieven")](./media/connect-to-lcs-crop.png)
2.  Selecteer het project Lifecycle Services om verbinding mee te maken.
3.  Selecteer de BPM-bibliotheken (in het geselecteerde project) om taakregistraties op te halen.
4.  Stel de weergavevolgorde van de BPM-bibliotheken in. Dit bepaalt de volgorde waarin de taakregistraties uit de bibliotheken verschijnen in het deelvenster **Help**.

Nadat u deze stappen hebt voltooid, kunt u het deelvenster **Help** openen en op het tabblad **Taakbegeleidingen** klikken. U ziet nu de taakbegeleidingen die van toepassing zijn op de pagina die nu is geopend in Dynamics 365 for Operations. Als er geen taakbegeleidingen worden gevonden, kunt u trefwoorden invoeren om uw zoekopdracht te verfijnen.

### <a name="showing-translated-task-guides"></a>Vertaalde taakbegeleidingen weergeven

Vertaalde taak handleidingen eerst zijn verzonden in de mei 2016 APQC centrale bibliotheek en de bibliotheek aan de slag. Als u in Dynamics 365 for Operations gelokaliseerde help met taakbegeleiding wilt zien, moet u ervoor zorgen verbonden te zijn met de bibliotheek van mei. De taal die in de handleiding van een taak wordt weergegeven voor elke gebruiker wordt gecontroleerd door de taalinstellingen onder **opties**&gt;**voorkeuren**. **Opmerking:** hoewel veel taakbegeleidingen zijn vertaald, worden momenteel in de Dynamics 365 for Operations-client de vertaalde namen van taakbegeleidingen niet weergegeven. De taak-instructies die zijn uitgebracht in februari 2016 zijn ook beschikbaar in de vertaling in de bibliotheek mei. Wij zullen een bijgewerkte bibliotheek met extra vertalingen uitbrengen.

-   Als een taakbegeleiding is vertaald, wordt bij het openen van die taakbegeleiding alle tekst van de taakbegeleiding weergegeven in uw geselecteerde taal.
-   Als een taakbegeleiding nog niet is vertaald, wordt bij het openen van die taakbegeleiding alleen bepaalde tekst (de tekst van de besturingselementen) weergegeven in uw geselecteerde taal.

## <a name="creating-custom-help"></a>Aangepaste Help maken
U kunt voor aangepaste Help voor uw implementatie van Dynamics 365 for Operations maken door uw taakregistraties maken die uw implementatie weerspiegelen en ze op te slaan in een LCS-bibliotheek voor bedrijfsprocessen. Voor partners: als u een bibliotheek propageert als bedrijfsbibliotheek en deze in een oplossing opneemt, wordt deze beschikbaar voor uw klanten. U kunt een kopie van de globale APQC Unified-bibliotheek maken en vervolgens uw kopie openen, hierin taakregistraties openen, deze wijzigen en de registraties met uw wijzigingen opslaan. Zie voor meer informatie [het maken van de opname van een taak wilt gebruiken als documentatie of training](../user-interface/task-recorder.md).

<a name="see-also"></a>Zie ook
--------

[Help overview](help-overview.md)

[Recorder taakoverzicht](../user-interface/task-recorder.md)

[Een taakregistratie voor een documentatie of training maken](../user-interface/task-recorder-training-docs.md)

[Nieuwe opleiding bibliotheken maken voor Dynamics 365 for Operations binnen Lifecycle Services met behulp van Taakregistratie (externe koppeling)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)


