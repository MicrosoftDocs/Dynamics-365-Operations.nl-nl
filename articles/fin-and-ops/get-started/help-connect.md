---
title: Het Help-systeem verbinden
description: In dit onderwerp worden de onderdelen van het Help-systeem voor Microsoft Dynamics 365 for Finance and Operations beschreven en vindt u een overzicht van de wijze waarop u deze verbindt. Daarnaast wordt beknopt aangegeven hoe u aangepaste Help maakt.
author: margoc
manager: AnnBe
ms.date: 09/11/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d67ad79c068651f32ce7dc776bc460698557bc29
ms.openlocfilehash: a27b21ffcde9bfbb7e6276ef35b2e48bd23af70d
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="connect-the-help-system"></a>Het Help-systeem verbinden

[!include[banner](../includes/banner.md)]


In dit onderwerp worden de onderdelen van het Help-systeem voor Microsoft Dynamics 365 for Finance and Operations beschreven. Het bevat een overzicht van hoe deze onderdelen met elkaar zijn verbonden, en een samenvatting hoe u aangepaste Help kunt maken. 

## <a name="help-architecture"></a>Help-architectuur
De volgende afbeelding toont de onderdelen van het Help-systeem van Finance and Operations. Het in-product Help-systeem haalt artikelen op uit de Finance and Operations-site op https://docs.microsoft.com, evenals taakbegeleidingen die zijn opgeslagen in Business Process Modeler in Lifecycle Services (LCS). 
> [!NOTE]
> De functies die in het diagram zijn aangegeven met een sterretje (\*) zijn gepland, maar zijn nog niet beschikbaar. [![Help-architectuur](./media/help-architecture.png)](./media/help-architecture.png)


## <a name="connecting-the-help-system"></a>Verbinding maken met het Help-systeem
> [!NOTE]
> Het tabblad **Taakbegeleidingen** is momenteel niet beschikbaar in Microsoft Dynamics 365 for Talent en Microsoft Dynamics 365 for Retail. Wij werken er momenteel aan om deze functionaliteit in een toekomstige versie beschikbaar te stellen. De taakbegeleidingen in de ervaring Aan de slag in Talent blijven beschikbaar om de basisfunctionaliteit uit te leggen. Procedurele hulp is ook beschikbaar op de website docs.microsoft.com ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) voor zowel Retail als Talent.
 

Met de pagina **Systeemparameters** verbinden systeembeheerders de delen van het Help-systeem voor een implementatie. [![Formulier Systeemparameters met Help-instellingen](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Voer de volgende stappen uit op de pagina **Systeemparameters**:

> [!IMPORTANT]
> De eerste keer dat u het tabblad **Help** opent, moet u verbinding maken met Lifecycle Services. Zorg ervoor dat u op de koppeling in het midden van het formulier klikt, wacht op de verbinding, sluit het dialoogvenster en klik op **OK** om de pagina **Systeemparameters** op te halen[![Verbinden met LCS](./media/connect-to-lcs-crop-1024x365.png "Verbinden met LCS")](./media/connect-to-lcs-crop.png)

1.  Selecteer het project Lifecycle Services om verbinding mee te maken.
2.  Selecteer de BPM-bibliotheken (in het geselecteerde project) om taakregistraties op te halen.
    - Voor Finance and Operations selecteert u voor Microsoft-inhoud de meest recente APQC Unified Library voor Finance and Operations. 
    - Voor Retail brengen we binnenkort een bibliotheek uit. 
    - U hoeft geen bibliotheek te selecteren voor Talent: de verbinding met de juiste bibliotheek wordt voor u ingesteld. 

3.  Stel de weergavevolgorde van de BPM-bibliotheken in. Dit bepaalt de volgorde waarin de taakregistraties uit de bibliotheken verschijnen in het deelvenster **Help**.

Wanneer u deze stappen hebt voltooid, kunt u het deelvenster **Help** openen en op het tabblad **Taakbegeleidingen** klikken. U ziet nu de taakbegeleidingen die van toepassing zijn op de pagina die nu is geopend in Finance and Operations. Als er geen taakbegeleidingen worden gevonden, kunt u trefwoorden invoeren om uw zoekopdracht te verfijnen.

### <a name="showing-translated-task-guides"></a>Vertaalde taakbegeleidingen weergeven

Vertaalde taakbegeleidingen zijn voor het eerst verzonden in de APQC Unified Library van mei 2016 en de Aan de slag-bibliotheek. Als u in Finance and Operations gelokaliseerde help met taakbegeleiding wilt zien, moet u ervoor zorgen verbonden te zijn met de bibliotheek van de mei-versie. De taal waarin een taakbegeleiding wordt weergegeven, wordt voor elke gebruiker bepaald door de instellingen voor taal onder **Opties** &gt; **Voorkeuren**. 

> [!NOTE]
> Hoewel veel taakbegeleidingen zijn vertaald, worden momenteel in de Finance and Operations-client de vertaalde namen van taakbegeleidingen niet weergegeven. Ook zijn op dit moment alleen de taakbegeleidingen die in februari 2016 zijn uitgebracht beschikbaar in vertaling in de bibliotheek voor mei. Wij zullen een bijgewerkte bibliotheek met extra vertalingen uitbrengen.
> -   Als een taakbegeleiding is vertaald, wordt bij het openen van die taakbegeleiding alle tekst van de taakbegeleiding weergegeven in uw geselecteerde taal.
> -   Als een taakbegeleiding nog niet is vertaald, wordt bij het openen van die taakbegeleiding alleen bepaalde tekst (de tekst van de besturingselementen) weergegeven in uw geselecteerde taal.

## <a name="creating-custom-help"></a>Aangepaste Help maken
U kunt voor aangepaste Help voor uw implementatie van Finance and Operations en voor Retail maken door taakregistraties te maken die uw implementatie weerspiegelen en ze op te slaan in een LCS-bibliotheek voor bedrijfsprocessen. U kunt geen aangepaste taakbegeleidingen voor Talent maken. 

Voor partners: als u een bibliotheek propageert als bedrijfsbibliotheek en deze in een oplossing opneemt, wordt deze beschikbaar voor uw klanten. U kunt een kopie van de globale APQC Unified-bibliotheek maken en vervolgens uw kopie openen, hierin taakregistraties openen, deze wijzigen en de registraties met uw wijzigingen opslaan. Zie [Een taakregistratie voor een documentatie of training maken](../../dev-itpro/user-interface/task-recorder.md) voor meer informatie.

<a name="see-also"></a>Zie ook
--------

[Help-overzicht](help-overview.md)

[Overzicht taakrecorder](../../dev-itpro/user-interface/task-recorder.md)

[Een taakregistratie voor een documentatie of training maken](../../dev-itpro/user-interface/task-recorder-training-docs.md)





