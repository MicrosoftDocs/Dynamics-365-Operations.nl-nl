---
title: Prognoses, werkorders en projecten
description: In dit onderwerp worden prognoses en de integratie van werkorders met de module Projectbeheer en boekhouding in Activabeheer beschreven.
author: josaw1
manager: tfehr
ms.date: 08/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9e6d20d1538ea68570d6dcc49da001ad76b8042b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/25/2020
ms.locfileid: "3888806"
---
# <a name="forecasts-work-orders-and-projects"></a>Prognoses, werkorders en projecten

[!include [banner](../../includes/banner.md)]

 

In Activabeheer helpt de integratie met de module **Projectbeheer en boekhouding** om het kostenbeheer te optimaliseren, zodat gebruikers kosten voor prognoses van typen onderhoudstaken en werkordertaken kunnen bijhouden.

Voor het bijhouden van prognoses van typen onderhoudstaken zijn twee instellingen vereist:

1. Selecteer een project in **Activabeheer** > **Instellen** > **Parameters voor Activabeheer** en klik vervolgens op het tabblad **Activa** op het sneltabblad **Project** in het veld **Onderhoudsprognoseproject**, en selecteer een project.

2. Wanneer u een standaardregel voor onderhoudstaaktypen maakt, wordt er automatisch een activiteitnummer gemaakt voor de regel op de pagina **Standaardinstellingen voor type onderhoudstaak** (**Activabeheer** > **Instellen** > **Taken** > **Standaardinstellingen voor type onderhoudstaak**).

Prognoses van typen onderhoudstaken dienen twee doeleinden: 

- U kunt kosten voor prognoses voor typen onderhoudstaken bijhouden in de module **Projectbeheer en boekhouding**. 
- Prognoses worden automatisch overgebracht naar een werkorderproject wanneer u een onderhoudstaaktype selecteert in een werkordertaak.

Als u de kosten voor werkordertaken wilt bijhouden, moet u eerst werkorderprojecten instellen. Zie [Werkorderproject instellen](../setup-for-work-orders/work-order-project-setup.md) voor meer informatie.

## <a name="work-order-job-projects"></a>Werkordertaakprojecten

Wanneer u een werkordertaak maakt voor een werkorder, wordt het werkorderproject bepaald door de instellingen van het bovenliggende project op de pagina **Projectinstellingen werkorder** (**Activabeheer** > **Instellen** > **Werkorders** > **Projectinstellingen**).

Werkordertaakprojecten worden gemaakt op basis van een combinatie van de volgende werkordergegevens:

- Het geselecteerde werkordertype in de werkorder 
- De functionele locatie gerelateerd aan het activum van de werkordertaak
- Het activumtype van het activum van de werkordertaak  
- De verwachte begin- en eindtijd die zijn ingesteld voor de werkorder  

Een deel van deze informatie is mogelijk niet gevonden in een werkorder. Daarom wordt de zoekopdracht naar een bovenliggend project voor een werkorder uitgevoerd met behulp van de beschikbare combinatie van gegevens en de selectie van de project-id die overeenkomt met de werkordergegevens.

Vanwege de manier waarop het activumtype **Truckmotor** is ingesteld, is in de volgende afbeelding elke werkordertaak die is gemaakt met het activumtype **Truckmotor**, een subproject van project-id 000186.

![Figuur 1](media/01-integration-to-pma.png)

Het doel van de project-id in de werkordertaak en het bijbehorende activiteitnummer is het bijhouden van kosten die zijn gerelateerd aan de werkordertaak en het activum dat ervoor is geselecteerd in de module **Projectbeheer en boekhouding**. (Als u de project-id en het activiteitnummer wilt bekijken, selecteert u **Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders** en selecteert u de werkorder. Op het sneltabblad **Regeldetails** ziet u in het veld **Project-id** de project-id. In het veld **Activiteitnummer** ziet u het activiteitnummer.) Meer informatie over kostenbeheer in Activabeheer vindt u in [Kosten- en datumbeheer](../controlling-and-reporting/cost-and-date-control.md).

In de volgende afbeelding ziet u een grafisch overzicht van werkorderprojecten en gerelateerde projectactiviteiten.

![Figuur 2](media/02-integration-to-pma.png)

Wanneer een nieuwe werkordertaak wordt gemaakt voor een werkorder, wordt automatisch een werkorderproject gemaakt voor de taak. De financiële dimensies voor het activum dat is gekoppeld aan de werkordertaak, worden automatisch overgebracht naar het werkorderproject.

Aan de projectactiviteit die is gemaakt voor een werkordertaak zijn gerelateerde gegevens gekoppeld. Deze informatie gaat over het type onderhoudstaak, de variant van het type onderhoudstaak en handel. Deze gegevens zijn bijvoorbeeld handig als u een inkooporder maakt op basis van een werkorder (zie [Inkoop](../work-orders/procurement.md)) of als u de module **Projectbeheer en boekhouding** gebruikt voor tijdregistratie.

Als het activum op een functionele locatie is geïnstalleerd, maar later wordt geïnstalleerd op een andere functionele locatie, worden de financiële dimensies die aan de nieuwe functionele locatie zijn gekoppeld automatisch bijgewerkt voor het activum. Wanneer u dan een werkordertaak voor het activum maakt, worden in het werkorderproject voor de werkordertaak automatisch de financiële dimensies weergegeven die nu aan het activum zijn gekoppeld. Wanneer u functionele locaties gebruikt, kunnen kosten dus altijd worden getraceerd voor de functionele locaties waarop een activum op een bepaald moment is geïnstalleerd. De automatische update van financiële dimensies bevordert een volledige traceerbaarheid van de kosten voor projectbeheer en -rapportage.

## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Werkorderprojecten, levenscyclusstatussen van werkorders, projectfasen en projecttypen

Houd rekening met de afhankelijkheden in relatie tot de module **Projectbeheer en boekhouding** om ervoor te zorgen dat de levenscyclusstatussen van werkorders en de gerelateerde projectfasen correct worden gebruikt in werkorders:

- In de module **Projectbeheer en boekhouding** worden projectfasen ingesteld voor projecttypen op de pagina **Projectbeheer- en boekhoudingsparameters**.  
- Gebruik op de pagina **Projectbeheer- en boekhoudingsparameters** de selectievakjes om relevante projectfasen te selecteren voor alle projecttypen die u wilt gebruiken. In de volgende afbeelding zijn vijf fasen (**Gemaakt**, **Geschat**, **Gepland**, **Onderhanden** en **Gereed**) geselecteerd voor de projecttypen **Tijd en materiaal** en **Intern**. Deze vijf fasen zijn relevant voor zowel interne onderhoudstaken als serviceonderhoudstaken.
- In de module **Activabeheer** worden projecttypen gedefinieerd door de projectgroepen die u instelt op de pagina **Werkorderproject instellen** > tabblad **Projectgroep** (**Activabeheer** > **Instellen** > **Werkorders** > **Projectinstellingen**).  
- De projectgroepen die op de pagina **Projectinstellingen werkorder** zijn ingesteld, worden gebruikt wanneer u werkorders maakt. Wanneer een werkordertaak wordt gemaakt, wordt automatisch een werkorderproject gemaakt voor de werkorder.  
- Elke levenscyclusstatus van een werkorder moet een bijbehorende projectfase hebben.  
- De projectfase die is gerelateerd aan een levenscyclusstatus van een werkorder moet worden gedefinieerd als actieve fase voor de projectgroep die in het werkorderproject is gedefinieerd. Het werkorderproject wordt automatisch gemaakt voor een werkorder.
- Wanneer u een nieuwe werkorder maakt, wordt de automatische toewijzing van een werkorderproject gebaseerd op de pagina **Projectinstellingen werkorder**.  

De volgende afbeeldingen tonen de koppelingen tussen werkorderprojectgroepen, gerelateerde projecttypen, projectfasen en levenscyclusstatussen van werkorders.

![Figuur 3](media/03-integration-to-pma.png)

![Figuur 4](media/04-integration-to-pma.png)

![Figuur 5](media/05-integration-to-pma.png)

Informatie over het instellen van werkorderprojecten vindt u in [Projectinstellingen werkorder](../setup-for-work-orders/work-order-project-setup.md). Zie [Levenscyclusstatussen van werkorder](../setup-for-work-orders/work-order-lifecycle-states.md) voor meer informatie over het maken van levenscyclusstatussen van werkorders.

In de volgende afbeelding ziet u een grafisch overzicht van de verschillende projecten die in de module **Activabeheer** zijn gemaakt om de integratie met de module **Projectbeheer en boekhouding** mogelijk te maken. Ook worden de werkprocessen weergegeven waaraan de projecten zijn gekoppeld.

![Figuur 6](media/06-integration-to-pma.png)

