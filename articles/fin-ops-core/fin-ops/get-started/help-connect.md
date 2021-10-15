---
title: De Help-ervaring voor Finance and Operations-apps configureren
description: Dit onderwerp biedt informatie over de onderdelen van het Help-systeem voor sommige Microsoft Dynamics 365-apps.
author: margoc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a6c37822e84ba08fa0720ed2b3912cbec1448e3
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594852"
---
# <a name="configure-the-help-experience-for-finance-and-operations-apps"></a>De Help-ervaring voor Finance and Operations-apps configureren

[!include [banner](../includes/banner.md)]

In dit onderwerp vindt u een overzicht van de onderdelen van het Help-systeem voor Finance and Operations-apps, zoals Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce en Dynamics 365 Human Resources. Ook wordt uitgelegd hoe u deze onderdelen verbindt en u vindt een overzicht van het proces voor het maken van aangepaste Help.

## <a name="help-architecture"></a>Help-architectuur

Finance and Operations-apps bevatten conceptuele overzichten en andere onderwerpen die op de site met [Microsoft Dynamics 365-documentatie](/dynamics365/) worden gepubliceerd. Deze inhoud kan vervolgens worden geopend vanuit het deelvenster **Help** in het product. De volgende afbeelding toont de onderdelen van het Help-systeem.

[![Help-architectuur.](./media/help-architecture.png)](./media/help-architecture.png)

De Help van het product haalt artikelen op van docs.microsoft.com en andere verbonden websites. Daarnaast worden taakbegeleidingen opgehaald die zijn opgeslagen in Modelleertool bedrijfsprocessen in Microsoft Dynamics Lifecycle Services (LCS).

## <a name="adding-task-guides"></a>Taakbegeleidingen toevoegen

> [!NOTE]
> Het tabblad **Taakbegeleidingen** is momenteel niet beschikbaar in Human Resources of Commerce. <!--We are currently working to enable this functionality in a future release.--> De taakbegeleidingen in de ervaring Aan de slag in Human Resources blijven echter beschikbaar om de basisfunctionaliteit uit te leggen. Op de site [Microsoft Dynamics 365-documentatie](/dynamics365/) is procedurele Help beschikbaar voor zowel Human Resources als Commerce.

Op de pagina **Systeemparameters** kunnen systeembeheerders de toegang tot relevante bibliotheken voor taakbegeleidingen configureren voor een implementatie.

> [!NOTE]
> - Voordat u Help kunt configureren, moet u zich aanmelden met een account in de dezelfde tenant als de tenant waarin de app is geïmplementeerd.
> - Een LCS-bibliotheek kan niet worden verbonden vanuit een exemplaar van de app die wordt uitgevoerd op een lokale virtuele harde schijf (VHD).

[![Formulier Systeemparameters met Help-instellingen.](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Als u taakbegeleidingen voor een oplossing wilt configureren, volgt u deze stappen op de pagina **Systeemparameters**.

> [!IMPORTANT]
> De eerste keer dat u het tabblad **Help** opent, moet u verbinding maken met Lifecycle Services. Let erop dat u de koppeling in het midden van het formulier selecteert. Wacht op de verbinding, sluit het dialoogvenster en selecteer **OK** om de pagina **Systeemparameters** te openen.
>
> [![Verbinden met LCS](./media/connect-to-lcs-crop-1024x365.png "Verbinden met LCS.")](./media/connect-to-lcs-crop.png)

1. Selecteer het project Lifecycle Services om verbinding mee te maken.
2. Selecteer de BPM-bibliotheken (in het geselecteerde project) om taakregistraties op te halen.
3. Stel de weergavevolgorde van de BPM-bibliotheken in. Dit weergavevolgorde bepaalt de volgorde waarin de taakregistraties uit de bibliotheken verschijnen in het deelvenster **Help**.

Wanneer u deze stappen hebt voltooid, kunt u het deelvenster **Help** openen en het tabblad **Taakbegeleidingen** selecteren. U ziet nu de taakbegeleidingen die van toepassing zijn op de pagina die nu is geopend in Finance and Operations-apps. Als er geen taakbegeleidingen worden gevonden, kunt u trefwoorden invoeren om uw zoekopdracht te verfijnen.

### <a name="showing-translated-task-guides"></a>Vertaalde taakbegeleidingen weergeven

Vertaalde taakbegeleidingen zijn voor het eerst uitgebracht in de APQC Unified Library van mei 2016 en de Aan de slag-bibliotheek. Als u gelokaliseerde Help met taakbegeleiding wilt zien, moet u ervoor zorgen dat uw Dynamics 365-oplossing is verbonden met de bibliotheek van mei 2016. Gebruikers kunnen de taal wijzigen waarin een taakbegeleiding wordt weergegeven door de taalinstellingen onder **Opties** &gt; **Voorkeuren** te wijzigen.

> [!NOTE]
> Hoewel veel taakbegeleidingen zijn vertaald, worden momenteel in de client de vertaalde namen van taakbegeleidingen niet weergegeven. Daarnaast zijn in de bibliotheek van mei 2016 alleen vertalingen beschikbaar voor de taakbegeleidingen die in februari 2016 zijn uitgebracht. Microsoft brengt een bijgewerkte bibliotheek met extra vertalingen uit.
>
> - Als een taakbegeleiding is vertaald, wordt bij het openen van die taakbegeleiding alle tekst van de taakbegeleiding weergegeven in uw geselecteerde taal.
> - Als een taakbegeleiding nog niet is vertaald, wordt bij het openen van die taakbegeleiding alleen bepaalde tekst (de tekst van de besturingselementen) weergegeven in uw geselecteerde taal.

## <a name="adding-custom-help"></a>Aangepaste Help toevoegen

U kunt taakbegeleidingen maken om aangepaste Help te maken of een aangepaste Help-website koppelen aan het deelvenster **Help**.

### <a name="create-custom-help-by-using-task-guides"></a>Aangepaste Help maken met taakbegeleidingen

U kunt aangepaste Help voor de ondersteunde apps maken door taakregistraties te maken die uw implementatie weerspiegelen en deze op te slaan in een bedrijfsprocesbibliotheek in LCS. U kunt geen aangepaste taakbegeleidingen voor Human Resources maken.

Als u een partner bent en een bibliotheek propageert als bedrijfsbibliotheek en deze in een oplossing opneemt, wordt deze beschikbaar voor uw klanten. U kunt een kopie van de globale APQC Unified-bibliotheek maken en vervolgens de taakregistraties in de kopie openen, deze bewerken en uw wijzigingen opslaan. Zie [Resources voor Taakrecorder](../../dev-itpro/user-interface/task-recorder.md) voor meer informatie.

### <a name="connect-a-custom-help-site"></a>Verbinding maken met een aangepaste Help-site

Finance and Operations-apps worden zelden in hun kant-en-klare vorm gebruikt. In plaats daarvan wordt de oplossing aangepast en uitgebreid om aan de behoeften van de organisatie te voldoen. U kunt de Help-ervaring ook aanpassen en uitbreiden. U kunt bijvoorbeeld aangepaste Help toevoegen aan het deelvenster **Help** in het product.

Microsoft heeft een toolkit geleverd waarmee u aangepaste Help kunt implementeren en kunt koppelen aan het deelvenster **Help**. Zie [Overzicht van aangepaste Help](../../dev-itpro/help/custom-help-overview.md) voor informatie over het instellen van een aangepaste Help-oplossing die is gekoppeld aan het deelvenster **Help**.

Als u wilt samenwerken met Microsoft aan hulpprogramma's en processen voor het aanpassen van de Help, vult u het formulier in op [https://aka.ms/customhelpfeedback](https://aka.ms/customhelpfeedback).

## <a name="see-also"></a>Zie ook

[Help-systeem](help-overview.md)  
[Overzicht van aangepaste Help](../../dev-itpro/help/custom-help-overview.md)  
[Resources voor Taakrecorder](../../dev-itpro/user-interface/task-recorder.md)  
[Documentatie of training maken met Taakrecorder](../../dev-itpro/user-interface/task-recorder-training-docs.md)  
[Custom Help GitHub repository](https://github.com/microsoft/dynamics356f-o-custom-help)  


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
