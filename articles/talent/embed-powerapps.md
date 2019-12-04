---
title: Power Apps-apps insluiten in Dynamics 365 - Core HR
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij het menu-item Microsoft Power Apps uit de module Systeembeheer is verdwenen.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 6d1b7f1dd71e6bcbf10c4d91fe33e9494b041a2c
ms.sourcegitcommit: ae0efac749ab34d423fac44d00a597801c143fbb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/22/2019
ms.locfileid: "2830204"
---
# <a name="embed-power-apps-apps-in-dynamics-365---core-hr"></a>Power Apps-apps insluiten in Dynamics 365 - Core HR

[!include [banner](includes/banner.md)]

**Uitgifte**

Het menu-item **Power Apps** is verdwenen uit de module **Systeembeheer**.

**Oorzaak**

Het ontwerp van de gebruikersinterface is gewijzigd en Microsoft Power Apps is nu opgenomen in het standaardaanpassingsmodel.

**Oplossing**

De manier waarop Power Apps zijn ingesloten, is gewijzigd. Power Apps worden nu toegevoegd via het aanpassingsmodel. U kunt Power Apps toevoegen aan vrijwel alle pagina's in Microsoft Dynamics 365 Talent.

Zie [Microsoft Power Apps insluiten](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/embed-power-apps) voor informatie over het insluiten van Power Apps in Talent.

Voor Power Apps-klanten die apps hadden ingesloten voordat de wijziging van kracht werd, had een upgrade naar het nieuwe model moeten worden uitgevoerd.

De knop **Power Apps** bevindt zich in de rechterbovenhoek van bijna elke pagina in Talent. Met deze knop kunt u een Power Apps invoegen.

Hier volgt een voorbeeld.

1. Ga naar **Personeelsbeheer \> Koppelingen \> Medewerkers \> Werknemers**.
2. Selecteer de knop **Power Apps** en selecteer vervolgens **Een PowerApp invoegen**.

    ![Power Apps-knop](media/png.png)

3. Vul de velden in het dialoogvenster **Een PowerApp invoegen** in.

    ![Het dialoogvenster Een PowerApp invoegen](media/insert-powerapp.png)

U kunt ook deze stappen uitvoeren.

1. Selecteer **Dit formulier aanpassen** in de groep **Aanpassen** op het tabblad **Opties** van het actievenster van de pagina.

    ![De groep Aanpassen op het tabblad Opties](media/options.png)

    De aanpassingswerkbalk wordt weergegeven.

2. Selecteer **Invoegen \> PowerApp** op de werkbalk.

    ![Een Power Apps-app invoegen via de aanpassingswerkbalk](media/powerapp-bar.png)
