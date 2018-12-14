---
title: PowerApps-apps insluiten in Core HR
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij het menu-item PowerApps uit de module Systeembeheer is verdwenen.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 197b553f0b202ee29ad42274e2c0e03446ec782c
ms.contentlocale: nl-nl
ms.lasthandoff: 12/04/2018

---

# <a name="embed-powerapps-apps-in-core-hr"></a>PowerApps-apps insluiten in Core HR

[!include [banner](includes/banner.md)]

**Probleem**

Het menu-item **PowerApps** is verdwenen uit de module **Systeembeheer**.

**Oorzaak**

Het ontwerp van de gebruikersinterface is gewijzigd en Microsoft PowerApps is nu opgenomen in het standaardaanpassingsmodel.

**Resolutie**

De manier waarop PowerApps-apps zijn ingesloten, is gewijzigd. PowerApps-apps worden nu toegevoegd via het aanpassingsmodel. U kunt PowerApps-apps toevoegen aan vrijwel alle pagina's in Microsoft Dynamics 365 for Talent.

Zie [Ingesloten PowerApps](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps) voor informatie over het insluiten van een PowerApps-app in Talent.

Voor PowerApps-klanten die apps hadden ingesloten voordat de wijziging van kracht werd, had een upgrade naar het nieuwe model moeten worden uitgevoerd.

De knop **PowerApps** knop bevindt zich in de rechterbovenhoek van bijna elke pagina in Talent. Met deze knop kunt u een PowerApps-app invoegen.

Hier volgt een voorbeeld.

1. Ga naar **Personeelsbeheer \> Koppelingen \> Medewerkers \> Werknemers**.
2. Selecteer de knop **PowerApps** en selecteer vervolgens **Een PowerApp invoegen**.

    ![De knop PowerApps](media/png.png)

3. Vul de velden in het dialoogvenster **Een PowerApp invoegen** in.

    ![Het dialoogvenster Een PowerApp invoegen](media/insert-powerapp.png)

U kunt ook deze stappen uitvoeren.

1. Selecteer **Dit formulier aanpassen** in de groep **Aanpassen** op het tabblad **Opties** van het actievenster van de pagina.

    ![De groep Aanpassen op het tabblad Opties](media/options.png)

    De aanpassingswerkbalk wordt weergegeven.

2. Selecteer **Invoegen \> PowerApp** op de werkbalk.

    ![Een PowerApps-app invoegen via de aanpassingswerkbalk](media/powerapp-bar.png)
