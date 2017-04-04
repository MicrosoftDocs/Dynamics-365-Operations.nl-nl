---
title: Details productie in productie-uitvoering
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70073
ms.assetid: 620944ae-3e20-444a-807e-65495f160904
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: b310e799c1ef0756291c5f7ab886531e4caf1945
ms.lasthandoff: 03/31/2017


---

# <a name="production-order-defaults-in-manufacturing-execution"></a>Details productie in productie-uitvoering



Overweeg de instellingen op de **productie details** pagina voordat werknemers beginnen om te registreren voor productietaken. Als uw bedrijf gebruikmaakt van de functionaliteit voor meerdere locaties, wilt u mogelijk verschillende standaardinstellingen opgeven voor productieorders voor elke locatie. De orderstandaarden voor integratie met Productiebeheer worden ingesteld op de volgende tabbladen op de pagina **Standaardwaarden van productieorder**:

-   **Algemeen** - Algemene orderstandaarden voor productietaken in Productieregistratie.
-   **Begin** - Orderstandaarden die worden gebruikt wanneer de productietaken of bewerkingen worden gestart.
-   **Bewerkingen** - Orderstandaarden die worden toegepast op productietaken of -bewerkingen en feedback op bewerkingen tijdens het productieproces.
-   **Gereedmelden** - Orderstandaarden die worden toegepast wanneer artikelen worden gereedgemeld voor de laatste bewerking van een productieorder.
-   **Validatie hoeveelheid** - Orderstandaarden voor het valideren van begin- en feedbackhoeveelheden op productieorders.

## <a name="types-of-production-jobs"></a>Typen productietaken
Op het tabblad **Bewerkingen** selecteert u de typen productietaken die registratie vereisen op de pagina **Taakregistratie**. Gewoonlijk registreren werknemers gegevens voor instellings- en verwerkingstaken. Als er echter gebruik wordt gemaakt van taakplanning, kunt u andere taaktypen selecteren, zoals transporttaken, die werknemers moeten registreren wanneer ze een productieorder hebben verwerkt. **Belangrijk:** Controleer of alle relevante taaktypen zijn geselecteerd. Anders zijn de taken misschien niet beschikbaar voor registratie op de pagina **Taakregistratie**. Stem uw selecties af met de selecties die u in de kolom **Taakbeheer** op de pagina **Routegroepen** hebt gemaakt. Als **Taakbeheer** is geselecteerd voor de routegroep, wordt het taaktype gereedgemeld voor de productieorder. Deze rapportage gebeurt als de taak gereed wordt gemeld in Productieregistratie. Als alle taaktypen waarvoor **Taakbeheer** is geselecteerd, zijn gereedgemeld voor een bewerking, wordt ook in Productieregistratie gerapporteerd dat de bewerking voltooid is. **Opmerking:** Sommige taaktypen kunnen handmatig worden gereedgemeld via productiejournalen. In dit geval selecteert u **Taakbeheer** voor het taaktype, maar selecteert u niet het taaktype voor registratie op het tabblad **Bewerkingen** op de pagina **Standaardwaarden van productieorder**.

## <a name="bom-consumption-and-picking-list-journals"></a>Stuklijstverbruik en orderverzamellijstjournalen
Materialen worden ingesteld zodat deze tijdens de productie automatisch of handmatig worden verbruikt. Automatisch verbruik wordt gecontroleerd door het wisprincipe dat is ingesteld op de stuklijstregels en door de instelling van het veld **Automatisch stuklijstverbruik** in de Standaardwaarden van productieorder. Automatisch verbruik kan zo worden ingesteld dat dit optreedt wanneer een productieorder is gestart of gereedgemeld. Dit kan ook op het taakniveau plaatsvinden wanneer een taak is gestart of voltooid.

### <a name="controlling-material-consumption-when-a-production-order-is-started"></a>Beheer van materiaalverbruik wanneer een productieorder is gestart

Materiaalverbruik aan het begin van een productieorder wordt bepaald door het veld **Automatisch stuklijstverbruik** op het tabblad **Begin**. De volgende waarden zijn beschikbaar:

-   **Wisprincipe** - Wanneer een productieorder is gestart, worden de hoeveelheden materialen verbruikt volgens het wisprincipe dat op de productiestuklijstregels is ingesteld. Alleen materiaalregels waarop het wisprincipe is ingesteld op **Begin** worden aan het begin van de productie verbruikt.
-   **Altijd** - Hoeveelheden materiaal die in verhouding zijn met de beginhoeveelheid worden altijd verbruikt.
-   **Nooit** - Hoeveelheden materiaal worden nooit verbruikt.

### <a name="controlling-material-consumption-when-a-production-job-is-started-or-completed"></a>Beheer van materiaalverbruik wanneer een productietaak is gestart of voltooid

Materiaalverbruik aan het begin of bij de voltooiing van een productietaak wordt bepaald door het veld **Automatisch stuklijstverbruik** op het tabblad **Bewerkingen**. De volgende waarden zijn beschikbaar:

-   **Wisprincipe** - Wanneer een hoeveelheid op een productietaak is gestart of voltooid, worden de hoeveelheden materialen verbruikt volgens het wisprincipe dat op de productiestuklijstregels is ingesteld. Alleen materiaalregels waarop het wisprincipe is ingesteld op **Beginnen** of **Voltooien** worden verbruikt.
-   **Altijd** - Hoeveelheden materiaal die in verhouding zijn met de beginhoeveelheid van de taak worden altijd verbruikt.
-   **Nooit** - Hoeveelheden materiaal worden nooit verbruikt.

### <a name="controlling-material-consumption-when-a-production-order-is-reported-as-finished"></a>Beheer van materiaalverbruik wanneer een productieorder wordt gereedgemeld

Materiaalverbruik tijdens het gereedmeldproces van een productieorder wordt bepaald door het veld **Automatisch stuklijstverbruik** op het tabblad **Gereedmelden**. De volgende waarden zijn beschikbaar:

-   **Wisprincipe** - Wanneer een productieorder is gereedgemeld, worden de hoeveelheden materialen verbruikt volgens het wisprincipe dat op de productiestuklijstregels is ingesteld. Alleen materiaalregels waarop het wisprincipe is ingesteld op **Voltooien** worden verbruikt.
-   **Altijd** - Hoeveelheden materiaal die in verhouding zijn met de hoeveelheid die is gereedgemeld worden altijd verbruikt.
-   **Nooit** - Hoeveelheden materiaal worden nooit verbruikt.



