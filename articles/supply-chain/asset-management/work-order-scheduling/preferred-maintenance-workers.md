---
title: Onderhoudsmedewerkers van voorkeur instellen
description: In dit onderwerp wordt uitgelegd hoe u onderhoudsmedewerkers van voorkeur instelt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/19/2019
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
ms.openlocfilehash: 8f26be81e7057d0cea1473d81452216251633ad9
ms.sourcegitcommit: f93ead945afe5ae18706c66bce6e64a6b57aac50
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/19/2019
ms.locfileid: "1887406"
---
# <a name="preferred-maintenance-workers"></a>Onderhoudsmedewerkers van voorkeur

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

U kunt een voorkeur instellen maken met betrekking tot welke onderhoudsmedewerkers moeten worden toegewezen om werkorders te voltooien tijdens de planning van werkorders. Het gebruik van deze functionaliteit is optioneel, maar het kan u helpen om een keuze te maken voor de meest gekwalificeerde onderhoudsmedewerker om een taak te voltooien, op basis van vaardigheden en competenties van medewerkers. Daarom worden bij de planning van werkorders de instellingen in **Onderhoudsmedewerkers van voorkeur** gebruikt om te bepalen of een specifieke onderhoudsmedewerker of medewerkersgroep moet worden gepland voor een werkorder. Er worden alleen onderhoudsmedewerkers gepland die beschikbaar zijn op de planningstijd. Als een voorkeursinstelling voor onderhoudsmedewerkers overeenkomt met een werkorder tijdens de planning, maar de onderhoudsmedewerker is toegewezen aan andere taken, wordt de werkorder gepland voor een andere, beschikbare onderhoudsmedewerker.

Voordat u onderhoudsmedewerkers van voorkeur kunt instellen, moet u de onderhoudsmedewerkers en medewerkersgroepen instellen die beschikbaar moeten zijn voor selectie. Zie [Onderhoudsmedewerkers en -medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md) voor informatie over het instellen van onderhoudsmedewerkers en medewerkersgroepen.

## <a name="set-up-preferred-workers"></a>Medewerkers van voorkeur instellen

Een onderhoudsmedewerker of medewerkersgroep kan worden gerelateerd aan een bepaald(e)

- Handel  
- variant van een onderhoudstaaktype  
- type onderhoudstaak  
- categorie onderhoudstaaktype  
- activum  
- activumtype  

of een combinatie van deze selecties. Hoe meer selecties u voor dezelfde record maakt, hoe specifieker uw instellingen zijn.

1. Klik op **Activabeheer** > **Instellingen** > **Medewerkers** > **Onderhoudsmedewerkers van voorkeur**.

2. Klik op **Nieuw** om een nieuwe registratie te maken.

3. Maak eerst een standaardinstelling voor onderhoudsmedewerkers of medewerkersgroepen zonder selecties in de lijst met opsommingstekens hierboven. Dit betekent dat u alleen een selectie maakt in het veld **Onderhoudsmedewerkergroep van voorkeur** of **Onderhoudsmedewerkers van voorkeur**. In de volgende afbeelding ziet u een voorbeeld in de eerste record waarin Aanvragen is geselecteerd als de onderhoudsmedewerkergroep van voorkeur.

>[!NOTE]
>De standaardinstellingen worden gebruikt tijdens de planning van de werkorder als er geen andere, specifiekere combinatie overeenkomt met de inhoud van de werkorder.

4. Herhaal stap 2 om een nieuwe record te maken. Maak de vereiste selecties, afhankelijk van het detailniveau voor de medewerker of medewerkersgroep van voorkeur. *Voorbeeld*: in de volgende afbeelding is in de zesde record de onderhoudsmedewerker Shawn Richardson geselecteerd als medewerker van voorkeur. Hij wordt automatisch geselecteerd tijdens de planning van een werkorder met het activum CH-BP1-03-02 en het onderhoudstaaktype Beoordeling van faciliteit als hij op de geplande tijd beschikbaar is.

>[!NOTE]
>Wanneer er een onderhoudsmedewerker van voorkeur wordt geselecteerd tijdens de planning van de werkorder, doorloopt Activabeheer alle records met **onderhoudsmedewerkers van voorkeur** om deze op een mogelijke overeenkomst te controleren, waarbij altijd de meest specifieke combinatie eerst wordt gecontroleerd. Als er geen overeenkomst wordt gevonden, wordt de standaardrecord met een selectie in het veld **Onderhoudsmedewerkergroep van voorkeur** of **Onderhoudsmedewerkers van voorkeur** gebruikt.


![Figuur 1](media/02-work-order-scheduling.png)

U kunt ook verantwoordelijke onderhoudswerkers instellen die kunnen worden geselecteerd wanneer een onderhoudsverzoek of werkorder wordt gemaakt. In **Alle werkorders** en **Alle onderhoudsverzoeken** kunt u zo nodig de selectie bewerken. Zie [Verantwoordelijke onderhoudsmedewerkers](../setup-for-maintenance-requests/responsible-workers.md) voor meer informatie.

Tijdens de planning van werkorders worden verschillende scores berekend om te bepalen welke medewerkers de taken met betrekking tot een werkorder moeten voltooien (deze scores worden ingesteld via **Parameters voor activabeheer** > **Planning werkorder**). Als twee of meer onderhoudsmedewerkers of verantwoordelijke onderhoudsmedewerkers dezelfde score krijgen tijdens de werkorderplanning, wordt een willekeurige medewerker geselecteerd. Anders is het altijd de medewerker met de hoogste score die wordt toegewezen om een werkorder te voltooien.

