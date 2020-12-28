---
title: Uitvaltijd voor onderhoud voor werkorders
description: In dit onderwerp wordt beschreven hoe u registraties voor uitvaltijd voor onderhoud maakt voor het geselecteerde activum in een werkorder.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 263a044a0a378e95ea271ac1c6f468f9e3287f26
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425262"
---
# <a name="maintenance-downtime-for-work-orders"></a>Uitvaltijd voor onderhoud voor werkorders

[!include [banner](../../includes/banner.md)]


U kunt registraties voor uitvaltijd voor onderhoud maken voor de geselecteerde activa in een werkorder. Deze functie is handig als u de uitvaltijd voor onderhoud voor een of meer machines in het productiegebied wilt registreren. Eerst maakt u de redencodes voor uitvaltijd voor onderhoud die u wilt gebruiken, bijvoorbeeld **Storing** en **Geplande beëindiging**. Deze stap wordt uitgevoerd op de pagina **Redencodes voor uitvaltijd voor onderhoud**. Vervolgens kunt u registraties voor uitvaltijd voor onderhoud maken op de pagina **Uitvaltijd voor onderhoud** en de relevante redencodes voor uitvaltijd toevoegen.

## <a name="create-maintenance-downtime-reason-codes"></a>Redencodes voor uitvaltijd voor onderhoud maken

1. Selecteer **Activabeheer** > **Instellingen** > **Werkorders** > **Redencodes voor uitvaltijd voor onderhoud**.

2. Selecteer **Nieuw**.

3. Voer in het veld **Redencode voor uitvaltijd voor onderhoud** een id in voor de redencode voor uitvaltijd voor onderhoud.

4. Voer in het veld **Naam** een naam in.

5. Schakel het selectievakje **KPI opnemen** in als de redencode moet worden opgenomen in berekeningen van KPI's voor de activa. Doorgaans moeten geplande productieonderbrekingen niet worden opgenomen in KPI-berekeningen, omdat deze geen invloed hebben op verwachte prestaties.

6. Selecteer **Opslaan**.

In de onderstaande afbeelding ziet u een voorbeeld van de pagina **Redencodes voor uitvaltijd voor onderhoud**.

![Figuur 1](media/15-work-orders.png)

Nadat u de redencodes voor uitvaltijd voor onderhoud hebt gemaakt die u wilt gebruiken, kunt u registraties voor uitvaltijd voor onderhoud maken voor werkorders en activa.


## <a name="create-maintenance-downtime-registrations"></a>Registraties voor uitvaltijd voor onderhoud maken

1. Klik op **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** of **Actieve werkorders**.

2. Selecteer de werkorder en selecteer vervolgens op het tabblad **Werkorder** in de groep **Activum** de optie **Uitvaltijd voor onderhoud**.

3. Selecteer **Nieuw**.

4. Bepaal het datum- en tijdinterval voor de registratie van uitvaltijd voor onderhoud in de velden **Van** en **Tot**.

>[!NOTE]
>Wanneer u het veld **Tot** verlaat, wordt de duur in uren automatisch ingevoegd in het veld **Duur**.

5. Selecteer een redencode in het veld **Redencode voor uitvaltijd voor onderhoud**.

6. Herhaal stap 3 en 5 als u nog meer registraties wilt toevoegen.

7. Selecteer **Opslaan**.

In de onderstaande afbeelding ziet u een voorbeeld van een registratie voor uitvaltijd voor onderhoud.

![Figuur 2](media/16-work-orders.png)

De kalender die wordt gebruikt voor het berekenen van de registratie van uitvaltijd voor onderhoud is afhankelijk van uw selectie bij het instellen van activa en parameters. Als een resource wordt geselecteerd voor een activum in het veld **Resource** op het het sneltabblad **Vaste activa** van de pagina **Alle activa**, wordt de kalender gebruikt die is ingesteld voor de gekoppelde resourcegroep, zoals weergegeven in de volgende afbeelding.

![Figuur 3](media/17-work-orders.png)

Als geen resource is geselecteerd voor het activum, wordt de standaardkalender gebruikt die is geselecteerd op de pagina **Parameters voor activabeheer**, zoals weergegeven in de volgende afbeelding.

![Figuur 4](media/18-work-orders.png)

Klik op **Activabeheer voor bedrijven** > **Query's** > **Uitvaltijd voor onderhoud** voor een overzicht van alle registraties van uitvaltijd voor onderhoud.

>[!NOTE]
>Alle kalenders die in de module **Activabeheer** worden gebruikt, worden ingesteld in **Organisatiebeheer** > **Instellingen** > **Kalenders** > **Kalenders**.

