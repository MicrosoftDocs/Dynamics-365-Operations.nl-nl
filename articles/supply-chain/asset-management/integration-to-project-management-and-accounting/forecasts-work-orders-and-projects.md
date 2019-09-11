---
title: Prognoses, werkorders en projecten
description: In dit onderwerp worden prognoses en de integratie van werkorders met de module Projectbeheer en boekhouding in Activabeheer beschreven.
author: josaw1
manager: AnnBe
ms.date: 08/16/2019
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
ms.openlocfilehash: 5e986d139ac9d0a7729bb9787f05332bcc09f59b
ms.sourcegitcommit: 109a6ef2d20758dc4a25c51b11e22dd2214a1cc4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/16/2019
ms.locfileid: "1886811"
---
# <a name="forecasts-work-orders-and-projects"></a>Prognoses, werkorders en projecten

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

In Activabeheer wordt de integratie met de module **Projectbeheer en boekhouding** uitgevoerd om het kostenbeheer te optimaliseren, zodat gebruikers kosten voor prognoses van typen onderhoudstaken en werkordertaken kunnen bijhouden.

Voor het bijhouden van prognoses van typen onderhoudstaken moeten er twee instellingen worden geconfigureerd:

1. Selecteer een project in **Activabeheer** > **Instellingen** > **Parameters voor activabeheer** > de koppeling **Activa** > het sneltabblad **Project** > het veld **Onderhoudsprognoseproject**.

2. Wanneer u bij **Standaardinstellingen voor type onderhoudstaak** een standaardregel voor onderhoudstaaktypen maakt, wordt er automatisch een activiteitnummer gemaakt voor de regel (**Activabeheer** > **Instellingen** > **Taken** > **Standaardinstellingen voor type onderhoudstaak**).

Prognoses van typen onderhoudstaken dienen twee doelen: u kunt kosten voor prognoses van typen onderhoudstaken bijhouden in de module **Projectbeheer en boekhouding**. Bovendien worden prognoses automatisch overgebracht naar een werkorderproject wanneer u een onderhoudstaaktype selecteert in een werkordertaak.

Als u de kosten voor werkordertaken wilt bijhouden, moet u eerst werkorderprojecten instellen. Zie de sectie [Projectinstellingen werkorder](../setup-for-work-orders/work-order-project-setup.md) voor een omschrijving van de procedure.

## <a name="work-order-job-projects"></a>Werkordertaakprojecten

Wanneer u een werkordertaak maakt voor een werkorder, wordt het werkorderproject bepaald door de instellingen van het bovenliggende project voor werkorders in **Activabeheer** > **Instellingen** > **Werkorders** > **Projectinstellingen**.

Werkordertaakprojecten worden gemaakt op basis van een combinatie van de volgende werkordergegevens:

- Het geselecteerde werkordertype in de werkorder 
- De functionele locatie gerelateerd aan het activum van de werkordertaak
- Het activumtype dat is gerelateerd aan het activum van de werkordertaak  
- De verwachte begin- en eindtijd die zijn ingesteld voor de werkorder  

Het is mogelijk dat niet alle bovenstaande gegevens in een werkorder zijn opgenomen. Daarom wordt de zoekopdracht naar een bovenliggend project voor een werkorder uitgevoerd met behulp van de beschikbare combinatie van gegevens en de selectie van de project-id die overeenkomt met de werkordergegevens.

Voorbeeld: in de volgende afbeelding betekent de instelling van het activumtype Truckmotor dat elke werkordertaak die met dat activumtype is gemaakt een subproject van project-id 000186 is.

![Figuur 1](media/01-integration-to-pma.png)

De project-id voor de werkordertaak en het gerelateerde activiteitsnummer (**Activabeheer** > **Algemeen** > **Werkorders** > **Alle Werkorders** > werkorder in de lijst selecteren > het sneltabblad **Regeldetails** > het veld **Project-id** en het veld **Activiteitsnummer**) dienen om de kosten bij te houden die zijn gerelateerd aan de werkordertaak en het activum dat is geselecteerd voor de werkordertaak in de module **Projectbeheer en boekhouding**. 

In de volgende afbeelding ziet u een grafisch overzicht van werkorderprojecten en gerelateerde projectactiviteiten.

![Figuur 2](media/02-integration-to-pma.png)

Wanneer een nieuwe werkordertaak wordt gemaakt voor een werkorder, wordt automatisch een werkorderproject gemaakt voor de taak. De financiële dimensies voor het activum dat aan de werkordertaak is gekoppeld, worden automatisch overgebracht naar het werkorderproject. Aan de projectactiviteit die voor een werkordertaak wordt gemaakt, is gerelateerde informatie gekoppeld over het type onderhoudstaak, de variant van het onderhoudstaaktype en het specialisme. Deze gegevens zijn handig als u bijvoorbeeld een inkooporder maakt op basis van een werkorder (zie [Inkoop](../work-orders/procurement.md)) of als u de module **Projectbeheer en boekhouding** gebruikt voor tijdregistratie.  

Als het activum op een functionele locatie is geïnstalleerd en dit activum later op een andere functionele locatie wordt geïnstalleerd, worden de financiële dimensies die aan de nieuwe functionele locatie zijn gekoppeld automatisch bijgewerkt voor het activum. Wanneer u vervolgens een werkordertaak voor het activum maakt, worden in het werkorderproject voor de werkordertaak automatisch de financiële dimensies weergegeven die nu aan het activum zijn gekoppeld. Wanneer u functionele locaties gebruikt, kunnen kosten dus altijd worden getraceerd voor de functionele locaties waarop een activum op een bepaald moment is geïnstalleerd. De automatische update van financiële dimensies zorgt voor een volledige traceerbaarheid van de kosten voor het beheren en rapporteren van projecten.  


## <a name="work-order-projects-work-order-lifecycle-states-project-stages-and-project-types"></a>Werkorderprojecten, levenscyclusstatussen van werkorders, projectfasen en projecttypen

Houd rekening met de afhankelijkheden in relatie tot de module **Projectbeheer en boekhouding** om ervoor te zorgen dat de levenscyclusstatussen van werkorders en de gerelateerde projectfasen correct worden gebruikt in werkorders:

- In de module **Projectbeheer en boekhouding** worden projectfasen ingesteld voor projecttypen in **Projectbeheer- en boekhoudingsparameters**.  
- Schakel in **Projectbeheer- en boekhoudingsparameters** de selectievakjes voor de relevante projectfasen in voor alle projecttypen die u wilt gebruiken. In de volgende afbeelding zijn de vijf fasen **Gemaakt** - **Geschat** - **Gepland** - **Onderhanden** - **Gereed** geselecteerd voor de projecttypen Tijd en materiaal en Intern. Deze vijf fasen zijn relevant voor interne onderhoudstaken en serviceonderhoudstaken.  
- In **Activabeheer** worden projecttypen gedefinieerd op basis van de projectgroepen die u instelt in het formulier **Projectinstellingen werkorder** > de koppeling **Projectgroep**.  
- De instellingen voor projectgroepen in **Projectinstellingen werkorder** worden gebruikt wanneer u werkorders maakt. Wanneer een werkordertaak wordt gemaakt, wordt automatisch een werkorderproject gemaakt voor de werkorder.  
- Levenscyclusstatussen van werkorders moeten allemaal een bijbehorende projectfase hebben.  
- De projectfase voor een levenscyclusstatus van een werkorder moet worden gedefinieerd als actieve fase voor de projectgroep die in het werkorderproject is gedefinieerd. Het werkorderproject wordt automatisch gemaakt voor een werkorder.  
- Wanneer u een nieuwe werkorder maakt voor een werkorder, wordt de automatische toewijzing van een werkorderproject gebaseerd op de instellingen in **Projectinstellingen werkorder** (**Activabeheer** > **Instellingen** > **Werkorders** > **Projectinstellingen**).  

Koppelingen tussen werkorderprojectgroepen, gerelateerde projecttypen, projectfasen en levenscyclusstatussen van werkorders worden weergegeven in de onderstaande afbeeldingen.  

![Figuur 3](media/03-integration-to-pma.png)

![Figuur 4](media/04-integration-to-pma.png)

![Figuur 5](media/05-integration-to-pma.png)

Zie [Projectinstellingen werkorder](../setup-for-work-orders/work-order-project-setup.md) voor informatie over het instellen van werkorderprojecten en [Levenscyclusstatussen van werkorder](../setup-for-work-orders/work-order-lifecycle-states.md) voor informatie over het maken van levenscyclusstatussen voor werkorders.

In de volgende afbeelding ziet u een grafisch overzicht van de verschillende projecten die in de module **Activabeheer** zijn gemaakt om integratie met de module **Projectbeheer en boekhouding** toe te staan, evenals de werkprocessen waaraan de projecten zijn gerelateerd.

![Figuur 6](media/06-integration-to-pma.png)

