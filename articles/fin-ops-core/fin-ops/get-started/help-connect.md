---
title: Verbinding maken met het Help-systeem
description: In dit onderwerp worden de onderdelen van het Help-systeem voor Finance and Operations-apps beschreven en vindt u een overzicht van de wijze waarop u deze verbindt. Daarnaast wordt beknopt aangegeven hoe u aangepaste Help maakt.
author: margoc
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 491024c9c3d6c7d20ef212e167ceab6abac8dac7
ms.sourcegitcommit: d554faca895609b8124bf2ea5aca5a55c407534a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/02/2019
ms.locfileid: "2537850"
---
# <a name="connect-the-help-system"></a>Verbinding maken met het Help-systeem

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de onderdelen van het Help-systeem voor Finance and Operations-apps beschreven, zoals Dynamics 365 Finance, Supply Chain Management, Retail en Talent. Het bevat een overzicht van hoe deze onderdelen met elkaar zijn verbonden, en een samenvatting hoe u aangepaste Help kunt maken.

## <a name="help-architecture"></a>Help-architectuur

De volgende afbeelding toont de onderdelen van het Help-systeem. Het in-product Help-systeem haalt artikelen op uit https://docs.microsoft.com, evenals taakbegeleidingen die zijn opgeslagen in Business Process Modeler in Lifecycle Services (LCS).

> [!NOTE]
> De functies die in het diagram zijn aangegeven met een sterretje (\*) zijn gepland, maar zijn nog niet beschikbaar.

[![Help-architectuur](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Verbinding maken met het Help-systeem

> [!NOTE]
> Het tabblad **Taakbegeleidingen** is momenteel niet beschikbaar in Dynamics 365 Talent of Retail. Wij werken er momenteel aan om deze functionaliteit in een toekomstige versie beschikbaar te stellen. De taakbegeleidingen in de ervaring Aan de slag in Talent blijven beschikbaar om de basisfunctionaliteit uit te leggen. Procedurele Help is ook beschikbaar op de site docs.microsoft.com voor zowel Retail als Talent.

Met de pagina **Systeemparameters** verbinden systeembeheerders de delen van het Help-systeem voor een implementatie.

[![Formulier Systeemparameters met Help-instellingen](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png)

Voer op de pagina **Systeemparameters** de volgende stappen uit:

> [!IMPORTANT]
> De eerste keer dat u het tabblad **Help** opent, moet u verbinding maken met Lifecycle Services. Let erop dat u op de koppeling in het midden van het formulier klikt. Wacht op de verbinding, sluit het dialoogvenster en klik op **OK** om de pagina **Systeemparameters** op te halen.
>
> [![Verbinden met LCS](./media/connect-to-lcs-crop-1024x365.png "Verbinden met LCS")](./media/connect-to-lcs-crop.png)

1. Selecteer het project Lifecycle Services om verbinding mee te maken.
2. Selecteer de BPM-bibliotheken (in het geselecteerde project) om taakregistraties op te halen.
3. Stel de weergavevolgorde van de BPM-bibliotheken in. Dit bepaalt de volgorde waarin de taakregistraties uit de bibliotheken verschijnen in het deelvenster **Help**.

Wanneer u deze stappen hebt voltooid, kunt u het deelvenster **Help** openen en op het tabblad **Taakbegeleidingen** klikken. U ziet nu de taakbegeleidingen die van toepassing zijn op de pagina die nu is geopend in Finance and Operations-apps. Als er geen taakbegeleidingen worden gevonden, kunt u trefwoorden invoeren om uw zoekopdracht te verfijnen.

### <a name="showing-translated-task-guides"></a>Vertaalde taakbegeleidingen weergeven

Vertaalde taakbegeleidingen zijn voor het eerst verzonden in de APQC Unified Library van mei 2016 en de Aan de slag-bibliotheek. Als u in Finance and Operations-apps gelokaliseerde Help met taakbegeleiding wilt zien, moet u ervoor zorgen verbonden te zijn met de bibliotheek van de mei-versie. De taal waarin een taakbegeleiding wordt weergegeven, wordt voor elke gebruiker bepaald door de instellingen voor taal onder **Opties** &gt; **Voorkeuren**.

> [!NOTE]
> Hoewel veel taakbegeleidingen zijn vertaald, worden momenteel in de client de vertaalde namen van taakbegeleidingen niet weergegeven. Ook zijn op dit moment alleen de taakbegeleidingen die in februari 2016 zijn uitgebracht beschikbaar in vertaling in de bibliotheek voor mei. Wij zullen een bijgewerkte bibliotheek met extra vertalingen uitbrengen.
>
> - Als een taakbegeleiding is vertaald, wordt bij het openen van die taakbegeleiding alle tekst van de taakbegeleiding weergegeven in uw geselecteerde taal.
> - Als een taakbegeleiding nog niet is vertaald, wordt bij het openen van die taakbegeleiding alleen bepaalde tekst (de tekst van de besturingselementen) weergegeven in uw geselecteerde taal.

## <a name="creating-custom-help"></a>Aangepaste Help maken

U kunt taakbegeleiders maken om aangepaste Help te maken of een website te koppelen aan het Help-venster.

### <a name="create-custom-help-with-task-guides"></a>Aangepaste Help maken met taakbegeleiders

U kunt voor aangepaste Help voor uw implementatie van Finance, Supply Chain Management en Retail maken door taakregistraties te maken die uw implementatie weerspiegelen en ze op te slaan in een LCS-bibliotheek voor bedrijfsprocessen. U kunt geen aangepaste taakbegeleidingen voor Talent maken.

Voor partners: als u een bibliotheek propageert als bedrijfsbibliotheek en deze in een oplossing opneemt, wordt deze beschikbaar voor uw klanten. U kunt een kopie van de globale APQC Unified-bibliotheek maken en vervolgens uw kopie openen, hierin taakregistraties openen, deze wijzigen en de registraties met uw wijzigingen opslaan. Zie [Een taakregistratie voor een documentatie of training maken](../../dev-itpro/user-interface/task-recorder.md) voor meer informatie.

### <a name="connect-a-custom-site"></a>Verbinding maken met een aangepaste site

Microsoft heeft een whitepaper en voorbeeldcode beschikbaar gesteld waarin wordt beschreven hoe u een aangepaste Help-site maakt en koppelt aan het Help-venster. Ga voor meer informatie naar:

- [Aangepaste Help maken voor Finance and Operations-apps (whitepaper)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Custom help GitHub repository](https://github.com/microsoft/dynamics356f-o-custom-help)

## <a name="additional-resources"></a>Aanvullende resources

[Help-overzicht](help-overview.md)

[Overzicht taakrecorder](../../dev-itpro/user-interface/task-recorder.md)

[Een taakregistratie voor een documentatie of training maken](../../dev-itpro/user-interface/task-recorder-training-docs.md)
