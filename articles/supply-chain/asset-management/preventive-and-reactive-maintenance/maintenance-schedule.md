---
title: Onderhoudsschema
description: In dit onderwerp wordt het onderhoudsschema in Activabeheer uitgelegd.
author: johanhoffmann
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetObjectCalendarCreateWO, EntAssetObjectCalendarListPagePoolsOpen, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePreviewPart, EntAssetObjectCalendarEdit, EntAssetObjectCalendarAdjust, EntAssetObjectCalendarDiscard, EntAssetObjectCalendarInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 40df8e6cba824f90e13b46cc258c76bef993a3e2dd9c35566d8c6a622ce4eb09
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738314"
---
# <a name="maintenance-schedule"></a>Onderhoudsschema

[!include [banner](../../includes/banner.md)]

 

Het onderhoudsschema bevat een lijst met alle verwachte plannen voor preventief onderhoud, onderhoudsverzoeken en onderhoudsronden die moeten worden uitgevoerd. Sommige schemaregels zijn mogelijk geconverteerd naar werkorders.

De vier onderhoudsschemaweergaven verschillen onderling enigszins afhankelijk van de onderhoudsschemaregels die u wilt bekijken.

| Menuopdracht                  | Beschrijving inhoud                                                                                                                                             |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hele onderhoudsschema       | De regels uit het hele onderhoudsschema worden weergegeven.     |
| Mijn activumplanning        | De regels uit het hele onderhoudsschema die activa bevatten die zijn geïnstalleerd op functionele locaties waaraan u als een medewerker bent verbonden (ingesteld in [Onderhoudsmedewerkers en -medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md)) worden in deze lijst weergegeven. |
| Onderhoudsschemaregels openen | Onderhoudsschemaregels met de status Gemaakt – wat betekent dat ze nog niet zijn omgezet in een werkorder of zijn verwijderd – worden in deze lijst weergegeven.                                            |
| Onderhoudsschemagroepen openen | Onderhoudsschemaregels voor een werkordergroep worden in deze lijst weergegeven.                                                                                                                  |

>[!NOTE]
>Als een onderhoudsschemaregel is opgenomen in verschillende werkordergroepen (zie [Werkordergroepen](../work-orders/work-order-pools.md)), wordt één record voor elke groep weergegeven in **Openstaande onderhoudsschemagroepen**. Dit wordt gedaan om de filteropties voor werkordergroepen te optimaliseren.

Een onderhoudsschema openen:

1. Klik op **Activabeheer** > **Algemeen** > **Onderhoudsschema** > **Hele onderhoudsschema** of **Openstaande onderhoudsschemaregels** of **Openstaande onderhoudsschemagroepen**.

2. Als u het onderhoudsschema wilt bijwerken, klikt u op **Onderhoudsschema** of **Onderhoudsronden**. 

3. U kunt een onderhoudsschemaregel bewerken door deze te selecteren en op **Bewerken** te klikken. U kunt bijvoorbeeld eenvoudig het serviceniveau bijwerken of de medewerker die verantwoordelijk is voor de taak. U kunt alleen onderhoudsschemaregels bewerken die nog niet aan een werkorder zijn gekoppeld.

4. U kunt een onderhoudsschemaregel verwijderen door deze te selecteren op de lijstpagina en op **Verwijderen** te klikken.

5. U kunt een onderhoudsschemaregel negeren door deze te selecteren op de lijstpagina en op **Negeren** te klikken. Deze functie is handig als bijvoorbeeld een activum een onderhoudsplan van 2000 km en een onderhoudsplan van 10.000 km heeft. Vervolgens wilt u misschien de regel die is gemaakt met het onderhoudsplan van 2000 km negeren als deze samenvalt met 10.000 km, 20.000 km, 30.000 km, enzovoort. Als u een onderhoudsschemaregel voor een onderhoudsplan negeert, wordt deze regel niet meer weergegeven wanneer dat onderhoudsplan is gepland.

6. U kunt een aantal onderhoudsschemaregels selecteren in **Hele onderhoudsschema** en op **Werkordergroep** klikken als u wilt dat alle geselecteerde regels in dezelfde werkordergroep worden opgenomen.

7. U kunt een aantal onderhoudsschemaregels selecteren in **Hele onderhoudsschema** of **Openstaande onderhoudsschemaregels** of **Openstaande onderhoudsschemagroepen** en op **Planning aanpassen** klikken als u dezelfde correcties op meerdere regels wilt aanbrengen. U kunt de verwachte begin- en einddatums, het serviceniveau en de verantwoordelijke onderhoudsmedewerkersgroep of verantwoordelijke onderhoudsmedewerker voor de geselecteerde onderhoudsschemaregels wijzigen.

- Wanneer een onderhoudsschemaregel aan een werkorder is gekoppeld, wordt de werkorder-id weergegeven in het veld **Werkorder**.  
- In de detailweergave **Alle activa** > sneltabblad **Onderhoudsplannen voor activa** kunt u onderhoudsplannen voor het activum selecteren. Als u later een onderhoudsplanregel voor een activum in **Alle activa** verwijdert, verwijdert u ook automatisch alle onderhoudsschemaregels met de status 'Gemaakt' die zijn gemaakt op basis van dat onderhoudsplan. Zie ook [Een activum maken](../objects/create-an-object.md).

In de volgende afbeelding ziet u de lijstpagina **Hele onderhoudsschema**.

![Figuur 1.](media/16-preventive-maintenance.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]