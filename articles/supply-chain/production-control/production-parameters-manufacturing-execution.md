---
title: Productieparameters in Productieregistratie
description: In dit onderwerp vindt u informatie over het instellen van productieparameters in Productieregistratie.
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: b24bb43e740835da25d44cb971e8f528db9cfacb
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="production-parameters-in-manufacturing-execution"></a>Productieparameters in Productieregistratie

[!include[banner](../includes/banner.md)]

In dit onderwerp vindt u informatie over het instellen van productieparameters in Productieregistratie.

De module **Productieregistratie** is voornamelijk bedoeld voor productiebedrijven. Deze module kan worden gebruikt om tijd- en artikelverbruik te registreren voor productietaken of projecten. Voordat u Productieregistratie voor taakregistratie gaat gebruiken, moet u verscheidene productieparameters instellen die bepalen hoe en wanneer de geregistreerde gegevens worden geboekt tijden het productieproces. De instellingen van productieparameters beïnvloeden het voorraad- en productiebeheer en de kostenberekening.

Voordat werknemers registraties voor productietaken beginnen te maken, moet u alle instellingen op de pagina **Standaardwaarden van productieorder** zorgvuldig overwegen. Klik op **Productiebeheer** &gt; **Instellingen** &gt; **Productieregistratie** &gt; **Productieparameters**. Als uw bedrijf gebruik maakt van de functionaliteit voor meerdere locaties, wilt u misschien per locatie andere productieparameters instellen. De parameters voor integratie met de module **Productie** worden ingesteld op de volgende tabbladen op de pagina **Productieparameters**:

- **Algemeen**: Algemene parameterinstellingen voor productietaken in Productieregistratie.
- **Start**: Parameters die worden gebruikt wanneer productiebewerkingen worden gestart.
- **Bewerkingen**: Parameters die worden toegepast op productiebewerkingen en feedback op bewerkingen tijdens het productieproces.
- **Gereedmelden**: Parameters die worden gebruikt wanneer artikelen worden gereedgemeld voor de laatste bewerking van een productieorder.
- **Validatie hoeveelheid**: Parameters voor het valideren van begin- en feedbackhoeveelheden op productieorders.

## <a name="types-of-production-jobs"></a>Typen productietaken
Op het tabblad **Bewerkingen** selecteert u welke typen productietaken registratie vereisen op de pagina **Taakregistratie**.

Gewoonlijk registreren werknemers gegevens voor instellings- en verwerkingstaken. Als er echter gebruik wordt gemaakt van taakplanning, kunt u andere taaktypen selecteren die werknemers moeten registreren wanneer productieorders worden verwerkt. U kunt bijvoorbeeld registraties voor transporttaken vereisen.

> [!IMPORTANT]
> Let erop dat u alle relevante taaktypen selecteert. Anders zijn de taken misschien niet beschikbaar voor registratie op de pagina **Taakregistratie**. Uw selecties moeten overeenkomen met de selecties in de kolom **Taakbeheer** op het tabblad **Instellingen** van de pagina **Routegroepen** (**Productiebeheer** &gt; **Instellingen** &gt; **Routes** &gt; **Routegroepen**).

Als **Taakbeheer** is geselecteerd voor de routegroep, wordt dit taaktype gereedgemeld voor de productieorder wanneer de taak wordt gereedgemeld in Productieregistratie. Als alle taaktypen waarvoor **Taakbeheer** is geselecteerd, zijn gereedgemeld voor een bewerking, wordt ook in Productieregistratie de bewerking gereedgemeld.

> [!NOTE]
> Sommige taaktypen kunnen handmatig worden gereedgemeld via productiejournalen. In dit geval selecteert u **Taakbeheer** voor het taaktype, maar selecteert u niet het taaktype voor registratie op het tabblad **Bewerkingen** op de pagina **Productieparameters** in Productieregistratie.

## <a name="bom-consumption-and-picking-list-journals"></a>Stuklijstverbruik en orderverzamellijstjournalen
Een consistente configuratie voor stuklijstverbruik is belangrijk, omdat dit een efficiënt voorraadbeheer helpt garanderen. Als de parameters voor stuklijstverbruik bijvoorbeeld niet goed zijn ingesteld in Productieregistratie, kan dat ertoe leiden dat materialen tweemaal of juist niet van de voorraad worden afgetrokken.

Op de pagina **Productieparameters** stelt u automatisch stuklijstverbruik in drie fasen in:

- Bij het begin van een productieproces. Deze fase stelt u in op het tabblad **Start**.
- Tijdens het productieproces wanneer een bewerking is voltooid. Deze fase stelt u in op het tabblad **Bewerkingen**.
- Wanneer een productieorder gereed wordt gemeld. Deze fase stelt u in op het tabblad **Gereedmelden**.

Voor elke fase kunt u in het veld **Automatisch stuklijstverbruik** kiezen uit drie methoden voor het verzamelen van artikelen voor een productieorder:

- **Backflushing**: Deze optie wordt gebruikt in combinatie met een optie die is gedefinieerd in de stuklijst in de module **Productie**. Klik op **Productiecontrole** &gt; **Algemeen** &gt; **Productieorders** &gt; **Alle productieorders**. Selecteer op de pagina **Alle productieorders** een productieorder in de lijst en klik vervolgens in het actievenster op **Stuklijst**. Selecteer op de pagina **Stuklijst**, op het tabblad **Instellingen** in het veld **Backflushing** een van de volgende opties:

    - **Beginnen**
    - **Voltooien**
    - **Handmatig**
    - Leeg (geen optie geselecteerd)
    - **Beschikbaar op locatie**

    Als in Productieregistratie **Backflushing** is geselecteerd in het veld **Automatisch stuklijstverbruik** op het tabblad **Starten**, worden alle materialen die in de stuklijst zijn ingesteld op **Starten**, afgetrokken van de voorraad wanneer de bewerking wordt gestart. De optie **Beschikbaar op locatie** wordt gebruikt voor producten die beschikbaar zijn voor geavanceerde magazijnprocessen. Als u deze vorm van backflushing instelt, wordt materiaal gewist wanneer magazijnwerk voor grondstofverzameling wordt voltooid. Materiaal wordt ook gewist wanneer een stuklijstregel, die dit wisprincipe gebruikt, wordt vrijgegeven voor het magazijn en het materiaal beschikbaar is op de productie-invoerlocatie.
    
    > [!NOTE]
    > Als het veld **Backflushing** is ingesteld op het tabblad **Beginnen** in Productieregistratie, moet u dezelfde methode selecteren op het tabblad **Bewerkingen** of op het tabblad **Gereedmelden**. Deze vereiste helpt garanderen dat materialen worden afgetrokken van de voorraad op de stuklijsten die **Voltooien** gebruiken voor backflushing op de productieorder. Als hetzelfde wisprincipe niet wordt geselecteerd op het tabblad **Bewerkingen** of het tabblad **Gereedmelden**, kunnen materialen twee keer worden afgetrokken van de voorraad.
 
- **Altijd**: Als u deze optie selecteert voor een fase, worden materialen altijd van de voorraad afgetrokken in die fase. Materialen voor de productie worden bijvoorbeeld van de voorraad afgetrokken, wanneer de productieorder wordt gestart. Deze instelling vereist dat **Nooit** is geselecteerd op de tabbladen **Bewerkingen** en **Gereedmelden**. Dit vereiste helpt voorkomen dat artikelen tweemaal van de voorraad worden afgetrokken.
- **Nooit**: Als u deze optie selecteert voor een fase, vindt geen stuklijstverbruik plaats in die fase. Als de optie **Nooit** bijvoorbeeld is geselecteerd op alle drie de tabbladen **Beginnen**, **Bewerkingen** en **Gereedmelden**, moeten materialen handmatig van de voorraad worden afgetrokken.

> [!IMPORTANT]
> Overweeg zorgvuldig hoe u de productieparameters instelt en let erop dat de parameters die u selecteert op de verschillende tabbladen van de pagina **Productieparameters** niet strijdig zijn met elkaar.

In de volgende voorbeelden worden de parameterinstellingen voor de verschillende stuklijstverbruikprincipes verduidelijkt. De parameters worden ingesteld op de pagina **Productieparameters** in Productieregistratie.

### <a name="example-1-backflushing-on-operations"></a>Voorbeeld 1: Backflushing bij bewerkingen

Gebruik de volgende instellingen voor het genereren van orderverzamellijstjournalen en stuklijstartikelverbruik wanneer artikelen gereed worden gemeld voor een bewerking.

| Tabblad                | Veld                          | Instelling                             |
|--------------------|--------------------------------|-------------------------------------|
| Beginnen              | Begin online bijwerken           | **Status** of **Status + hoeveelheid** |
| Beginnen              | Automatisch stuklijstverbruik      | **Nooit**                           |
| Operations         | Automatisch stuklijstverbruik      | **Altijd**                          |
| Rapporteren als gereed | Automatisch stuklijstverbruik      | **Nooit**                           |
| Rapporteren als gereed | Gereedmelding online bijwerken | **Status + hoeveelheid**               |

### <a name="example-2-backflushing-on-production"></a>Voorbeeld 2: Backflushing bij productie

Gebruik de volgende instellingen voor het genereren van orderverzamellijstjournalen en stuklijstartikelverbruik wanneer artikelen gereed worden gemeld voor de productieorder.

| Tabblad                | Veld                          | Instelling                             |
|--------------------|--------------------------------|-------------------------------------|
| Beginnen              | Begin online bijwerken           | **Status** of **Status + hoeveelheid** |
| Beginnen              | Automatisch stuklijstverbruik      | **Nooit**                           |
| Operations         | Automatisch stuklijstverbruik      | **Nooit**                           |
| Rapporteren als gereed | Automatisch stuklijstverbruik      | **Altijd**                          |
| Rapporteren als gereed | Gereedmelding online bijwerken | **Status + hoeveelheid**               |

### <a name="example-3-flushing-principle"></a>Voorbeeld 3: Wisprincipe

Gebruik de volgende instellingen als orderverzamellijstjournalen en stuklijstartikelverbruik moeten worden gegenereerd volgens het wisprincipe dat is ingesteld voor de stuklijstartikelen.

| Tabblad                | Veld                          | Instelling                |
|--------------------|--------------------------------|------------------------|
| Beginnen              | Begin online bijwerken           | **Status + hoeveelheid**  |
| Beginnen              | Automatisch stuklijstverbruik      | **Wisprincipe** |
| Operations         | Automatisch stuklijstverbruik      | **Wisprincipe** |
| Rapporteren als gereed | Automatisch stuklijstverbruik      | **Nooit**              |
| Rapporteren als gereed | Gereedmelding online bijwerken | **Status + hoeveelheid**  |

### <a name="example-4-deduction-of-materials-during-startup-of-a-production-order"></a>Voorbeeld 4: Materialen aftrekken tijdens het opstarten van een productieorder

Gebruik de volgende instellingen voor het genereren van orderverzamellijstjournalen en stuklijstartikelverbruik wanneer de productie wordt gestart.

| Tabblad                | Veld                          | Instelling                             |
|--------------------|--------------------------------|-------------------------------------|
| Beginnen              | Begin online bijwerken           | **Status + hoeveelheid**               |
| Beginnen              | Automatisch stuklijstverbruik      | **Altijd**                          |
| Operations         | Automatisch stuklijstverbruik      | **Nooit**                           |
| Rapporteren als gereed | Automatisch stuklijstverbruik      | **Nooit**                           |
| Rapporteren als gereed | Gereedmelding online bijwerken | **Status** of **Status + hoeveelheid** |

Orderverzamellijstjournalen worden op basis van de geselecteerde opties, die eerder in deze sectie zijn beschreven, geboekt in verschillende fasen van de productieorderverwerking:

- Wanneer een bewerking wordt gestart.
- Wanneer hoeveelheidsfeedback wordt gerapporteerd voor een bewerking.
- Wanneer artikelen worden gereedgemeld voor de productieorder.

### <a name="example-5-manual-bom-consumption"></a>Voorbeeld 5: Handmatig stuklijstverbruik

U kunt de volgende instellingen gebruiken, als materialen altijd handmatig moeten worden afgetrokken van de voorraad. In dit geval worden geen orderverzamellijstjournalen geboekt.

| Tabblad                | Veld                          | Instelling    |
|--------------------|--------------------------------|------------|
| Beginnen              | Begin online bijwerken           | **Status** |
| Beginnen              | Automatisch stuklijstverbruik      | **Nooit**  |
| Operations         | Automatisch stuklijstverbruik      | **Nooit**  |
| Rapporteren als gereed | Automatisch stuklijstverbruik      | **Nooit**  |
| Rapporteren als gereed | Gereedmelding online bijwerken | **Status** |

