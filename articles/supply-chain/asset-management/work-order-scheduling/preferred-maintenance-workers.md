---
title: Onderhoudsmedewerkers van voorkeur instellen
description: In dit onderwerp wordt uitgelegd hoe u onderhoudsmedewerkers van voorkeur instelt in Activabeheer.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkerPreferred
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 38b7371ab668eb76801fbe7f15894609a846bbd8
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687664"
---
# <a name="set-up-preferred-maintenance-workers"></a>Onderhoudsmedewerkers van voorkeur instellen

[!include [banner](../../includes/banner.md)]

Tijdens de planning van werkorders kunt u een voorkeur instellen met betrekking tot welke onderhoudsmedewerker of mederwerkersgroep u wilt toewijzen om de werkorder te voltooien. Het gebruik van deze functionaliteit is optioneel, maar het kan u helpen om een keuze te maken voor de meest gekwalificeerde onderhoudsmedewerker om een taak te voltooien, op basis van vaardigheden en competenties van medewerkers. Er worden alleen onderhoudsmedewerkers gepland die beschikbaar zijn op de planningstijd. Als een voorkeursinstelling voor een onderhoudsmedewerker tijdens de planning overeenkomt met een werkorder, maar de onderhoudsmedewerker al is toegewezen aan andere taken, wordt de werkorder gepland voor een andere, beschikbare onderhoudsmedewerker.

Voordat u voorkeursonderhoudsmedewerkers kunt instellen, moet u eerst de onderhoudsmedewerkers en medewerkersgroepen instellen. Zie [Onderhoudsmedewerkers en -medewerkersgroepen](../setup-for-objects/workers-and-worker-groups.md) voor een beschrijving van hoe u onderhoudsmedewerkers en medewerkersgroepen instelt.

## <a name="set-up-preferred-workers"></a>Medewerkers van voorkeur instellen

Een voorkeursonderhoudsmedewerker of medewerkersgroep kan worden gerelateerd aan een of meer van de volgende elementen:

- Handel  
- variant van een onderhoudstaaktype  
- type onderhoudstaak  
- categorie onderhoudstaaktype  
- activum  
- activumtype  

Hoe meer selecties u voor dezelfde record maakt, hoe specifieker uw instellingen zijn.

1. Klik op **Activabeheer** > **Instellingen** > **Medewerkers** > **Onderhoudsmedewerkers van voorkeur**.

2. Klik op **Nieuw** om een nieuwe registratie te maken.

3. Maak eerst een 'standaard'onderhoudsmedewerker of -medewerkersgroep. Dit betekent dat u alleen een selectie maakt in het veld **Onderhoudsmedewerkergroep van voorkeur** of **Onderhoudsmedewerkers van voorkeur**. In onderstaande schermafbeelding ziet u een voorbeeld in de eerste record waarin Aanvragen is geselecteerd als de **Voorkeursonderhoudsmedewerkersgroep**.

    > [!NOTE]
    > De standaardinstellingen worden gebruikt tijdens de planning van de werkorder als er geen andere, specifiekere combinatie overeenkomt met de inhoud van de werkorder.

4. Herhaal stap 2 om een nieuwe record te maken. Maak de vereiste selecties, afhankelijk van het detailniveau voor de medewerker of medewerkersgroep van voorkeur. 

    *Voorbeeld*: in onderstaande schermafbeelding is in de zesde record de onderhoudsmedewerker Shawn Richardson geselecteerd als voorkeursmedewerker. Hij wordt tijdens de planning van een werkorder met het activum CH-BP1-03-02 en het onderhoudstaaktype Beoordeling van faciliteit automatisch geselecteerd als hij op de geplande tijd beschikbaar is.

    > [!NOTE]
    > Wanneer er een onderhoudsmedewerker van voorkeur wordt geselecteerd tijdens de planning van de werkorder, doorloopt Activabeheer alle records met **onderhoudsmedewerkers van voorkeur** om deze op een mogelijke overeenkomst te controleren, waarbij altijd de meest specifieke combinatie eerst wordt gecontroleerd. Als er geen overeenkomst wordt gevonden, wordt de standaardrecord met een selectie in het veld **Onderhoudsmedewerkergroep van voorkeur** of **Onderhoudsmedewerkers van voorkeur** gebruikt.

![Figuur 1.](media/02-work-order-scheduling.png)

U kunt ook *verantwoordelijke* onderhoudswerkers instellen; deze kunnen worden geselecteerd wanneer een onderhoudsverzoek of werkorder wordt gemaakt. U kunt de selectie in **Alle werkorders** en **Alle onderhoudsverzoeken** zo nodig bewerken. Zie [Verantwoordelijke onderhoudsmedewerkers](../setup-for-maintenance-requests/responsible-workers.md) voor meer informatie.

Tijdens de planning van werkorders worden verschillende scores berekend om te bepalen welke medewerkers de taken met betrekking tot een werkorder moeten voltooien (deze scores worden ingesteld via **Parameters voor activabeheer** > **Planning werkorder**). Als twee of meer onderhoudsmedewerkers of verantwoordelijke onderhoudsmedewerkers dezelfde score krijgen tijdens de werkorderplanning, wordt een willekeurige medewerker geselecteerd. Anders is het altijd de medewerker met de hoogste score die wordt toegewezen om een werkorder te voltooien.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]