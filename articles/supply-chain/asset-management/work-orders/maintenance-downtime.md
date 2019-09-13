---
title: Uitvaltijd voor onderhoud
description: In dit onderwerp wordt uitvaltijd voor onderhoud in Activabeheer beschreven.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cc79dc1b5911679586fa560142ada5add1a881d2
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918239"
---
# <a name="maintenance-downtime"></a>Uitvaltijd voor onderhoud


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

U kunt registraties voor uitvaltijd voor onderhoud maken voor de geselecteerde activa in een werkorder. Dit is handig als u de uitvaltijd voor onderhoud voor een of meer machines in het productiegebied wilt registreren. Eerst maakt u de redencodes voor uitvaltijd voor onderhoud die u wilt gebruiken, bijvoorbeeld storing en geplande beëindiging. Dit wordt gedaan in **Redencodes voor uitvaltijd voor onderhoud**. Vervolgens kunt u registraties voor uitvaltijd voor onderhoud maken in **Uitvaltijd voor onderhoud** en de relevante redencodes toevoegen.

## <a name="create-maintenance-downtime-reason-codes"></a>Redencodes voor uitvaltijd voor onderhoud maken

1. Klik op **Activabeheer** > **Instellingen** > **Werkorders** > **Redencodes voor uitvaltijd voor onderhoud**.

2. Klik op **Nieuw**.

3. Voeg een id in het **Redencode voor uitvaltijd voor onderhoud** in.

4. Typ een naam voor de redencode in het veld **Naam**.

5. Schakel het selectievakje **Opnemen in KPI** in als de redencode moet worden opgenomen in KPI-berekeningen voor activa. Doorgaans moeten geplande productieonderbrekingen niet worden opgenomen in KPI-berekeningen, aangezien deze geen invloed hebben op verwachte prestaties.

6. Klik op **Opslaan**.

![Figuur 1](media/15-work-orders.png)


Wanneer u de redencodes voor uitvaltijd voor onderhoud hebt gemaakt die u wilt gebruiken, kunt u registraties voor uitvaltijd voor onderhoud maken voor werkorders en activa.


## <a name="create-maintenance-downtime-registrations"></a>Registraties voor uitvaltijd voor onderhoud maken

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder en klik op **Uitvaltijd voor onderhoud**.

3. Klik op **Nieuw**.

4. Voeg het datum- en tijdinterval voor de registratie van uitvaltijd voor onderhoud in de velden **Van** en **Tot** in.

5. Wanneer u het veld **Tot** verlaat, wordt de duur in uren automatisch ingevoegd in het veld **Duur**.

6. Selecteer een redencode in het veld **Redencode voor uitvaltijd voor onderhoud**.

7. Herhaal stap 3-6 als u meer registraties wilt toevoegen.

8. Klik op **Opslaan**.


![Figuur 2](media/16-work-orders.png)


De kalender die wordt gebruikt voor het berekenen van de registratie van uitvaltijd voor onderhoud is afhankelijk van uw selectie bij het instellen van activa en parameters. Als een resource wordt geselecteerd voor een activum in **Alle activa** > het sneltabblad **Vaste activa** > het veld **Resource**, wordt de kalender gebruikt die is ingesteld voor de gekoppelde resourcegroep, zoals weergegeven in de volgende afbeelding.

![Figuur 3](media/17-work-orders.png)


Als geen resource is geselecteerd voor het activum, wordt de standaardkalender gebruikt die is geselecteerd in het veld **Parameters voor activabeheer**, zoals weergegeven in de volgende afbeelding.

![Figuur 4](media/18-work-orders.png)


Klik op **Activabeheer voor bedrijven** > **Query's** > **Uitvaltijd voor onderhoud** voor een overzicht van alle registraties van uitvaltijd voor onderhoud.

>[!NOTE]
>Alle kalenders die in de module **Activabeheer** worden gebruikt, worden ingesteld in **Organisatiebeheer** > **Instellingen** > **Kalenders** > **Kalenders**.

