---
title: Migratie naar Planningsoptimalisatie voor hoofdplanning
description: Dit onderwerp bevat informatie over de nieuwe hoofdplannings-engine, Planningsoptimalisatie, en migratie van de bestaande engine.
author: ChristianRytt
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: ''
ms.author: crytt
ms.search.validFrom: 2020-11-05
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8a55958a4b9573a7c3527d3d97cbcb818457b995
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5007965"
---
# <a name="migration-to-planning-optimization-for-master-planning"></a>Migratie naar Planningsoptimalisatie voor hoofdplanning

[!include [banner](../includes/banner.md)]

De ingebouwde engine voor hoofdplanningen is gepland om verouderd te worden gemaakt (afgeschaft). Deze wordt vervangen door de invoegtoepassing Planningsoptimalisatie voor Microsoft Dynamics 365 Supply Chain Management. In dit onderwerp vindt u informatie over het effect op nieuwe en bestaande implementaties. Het bevat informatie over vereiste acties.

Met Planningsoptimalisatie kunnen de berekeningen van de hoofdplanning buiten Supply Chain Management en de gerelateerde Azure SQL-database plaatsvinden. De voordelen die zijn gekoppeld aan Planningsoptimalisatie omvatten betere prestaties en minimale gevolgen voor de SQL-database tijdens uitvoeringen van de hoofdplanning. Omdat snelle planningsuitvoeringen zelfs tijdens kantooruren kunnen worden uitgevoerd, kunnen planners direct reageren op vraag- of parameterwijzigingen.

Zie [Overzicht van Planningsoptimalisatie](planning-optimization/planning-optimization-overview.md) voor meer informatie over Planningsoptimalisatie.

## <a name="obsolescence-of-the-existing-master-planning-engine"></a>Veroudering van de bestaande hoofdplannings-engine

Microsoft is bezig de ingebouwde planningsengine af te schaffen ten gunste van Planningsoptimalisatie. Deze wijziging is van invloed op alle cloudomgevingen. On-premises installaties worden niet beïnvloed. In versie 10.0.16 en hoger wordt een foutbericht weergegeven als u de ingebouwde hoofdplanning uitvoert zonder geplande productieorders te genereren. De uitvoering van de hoofdplanning wordt echter wel voltooid ondanks het foutbericht.

Zie de aankondigingen in [Verwijderde of afgeschafte functies in Dynamics 365 Supply Chain Management](../get-started/removed-deprecated-features-scm-updates.md) voor meer informatie over de veroudering van de ingebouwde plannings-engine.

## <a name="migration-messages-and-exceptions"></a>Migratie, berichten en uitzonderingen

Eigenaren van bestaande omgevingen die de ingebouwde hoofdplanningsengine uitvoeren zonder geplande productieorders te genereren, ontvangen een e-mailbericht met details over het uitzonderingsproces. We raden u aan met een partner samen te werken om de migratie naar Planningsoptimalisatie te evalueren en te plannen.

Zoals vermeld wordt er in versie 10.0.16 en hoger een foutbericht weergegeven als u de ingebouwde hoofdplanning uitvoert zonder geplande productieorders te genereren. Dit foutbericht bevat informatie over migratie en instructies voor het aanvragen van een uitzondering.

### <a name="new-deployments"></a>Nieuwe implementaties

Planningsoptimalisatie moet worden beschouwd als de standaardhoofdplanningsengine voor alle nieuwe implementaties in de cloud. Planningsoptimalisatie moet in het algemeen worden gebruikt voor alle nieuwe implementaties waarmee geen geplande productieorders worden gegenereerd tijdens de hoofdplanning. Als een nieuwe implementatie afhankelijk is van functionaliteit die niet wordt ondersteund door Planningsoptimalisatie, kunt u een uitzondering aanvragen zodat u de ingebouwde hoofdplanningsengine kunt blijven gebruiken.

### <a name="existing-deployments"></a>Bestaande implementaties

Eigenaren van bestaande, cloudgebaseerde implementaties die afhankelijk zijn van de hoofdplanning, moeten plannen om te migreren naar Planningsoptimalisatie. Als uw implementatie afhankelijk is van functionaliteit die niet wordt ondersteund door Planningsoptimalisatie, kunt u een uitzondering aanvragen zodat u de ingebouwde hoofdplanningsengine kunt blijven gebruiken.

Voor omgevingen waarin momenteel hoofdplanningsprocessen worden gebruikt die worden afgeschaft, stuurt Microsoft een e-mailbericht naar de omgevingsbeheerder. Dit e-mailbericht bevat informatie over de acties die nodig zijn om te migreren of om een uitzondering te aanvragen.

## <a name="the-exception-process"></a>Het uitzonderingsproces

U kunt een uitzondering aanvragen als u de ingebouwde engine voor hoofdplanning moet blijven gebruiken, omdat uw bedrijfsprocessen sterk afhankelijk zijn van ten minste één functie die op dit moment niet is geïmplementeerd bij Planningsoptimalisatie. Zie [Analyse aanpassen aan Planningsoptimalisatie](planning-optimization/planning-optimization-fit-analysis.md) voor een lijst met beschikbare functies.

Uitzonderingen voor de migratie naar Planningsoptimalisatie zijn momenteel alleen relevant als uw hoofdplanningsproces geen productie (d.w.z. door hoofdplanning gegenereerde geplande productieorders) bevat en u een hogere versie van de ingebouwde hoofdplanningsengine nodig hebt dan versie 10.0.15.

Nadat de vereiste functies beschikbaar zijn, geeft Microsoft een respijtperiode totdat de uitzondering is verlopen. De omgevingsbeheerder wordt geïnformeerd wanneer de vereiste functies beschikbaar zijn geworden en de respijtperiode is gestart.

> [!NOTE]
> U kunt alleen een uitzondering voor productieomgevingen aanvragen, niet voor sandbox-omgevingen. Als u de uitzonderingsfout voor Planningsoptimalisatie in een IaaS-sandboxomgeving (infrastructure as a service) wilt uitschakelen, voert u de SQL-query uit die in [Sandbox-omgevingen](#faq-sandbox) wordt geleverd.

## <a name="frequently-asked-questions"></a>Veelgestelde vragen

### <a name="sandbox-environments"></a><a name="faq-sandbox"></a>Sandbox-omgevingen

Kan ik ingebouwde hoofdplanning gebruiken in mijn sandbox-omgeving? Heb ik een uitzondering nodig?

**Antwoord:** uitzonderingen zijn normaal gezien niet relevant voor sandbox-omgevingen omdat de uitzonderingsfout voor Planningsoptimalisatie niet verhindert dat de ingebouwde hoofdplanning-engine met goed gevolg kan worden uitgevoerd. Als het foutbericht u echter stoort, kunt u dit uitschakelen in een IaaS-sandbox-omgeving (niet Service Fabric) door de volgende query uit te voeren op uw database:

```sql
-- Insert or update an enabled flight:
DECLARE @flightName NVARCHAR(100) = 'ReqPlanningOptimizationExceptionToggle';
IF NOT EXISTS (SELECT TOP 1 1 FROM SysFlighting WHERE flightName = @flightName)
    INSERT INTO SYSFLIGHTING(FLIGHTNAME,ENABLED, FLIGHTSERVICEID,PARTITION)
    SELECT @flightName, 1, 12719367,RECID FROM DBO.[PARTITIONS];
ELSE
    UPDATE SysFlighting SET enabled = 1, flightServiceId = 12719367 WHERE flightName = @flightName;
```

### <a name="on-premises-environments"></a>On-premises omgevingen

Mijn omgeving is on-premises. Heb ik een uitzondering nodig?

**Antwoord:** Nee. Er is geen uitzondering vereist voor on-premises omgevingen. U kunt de ingebouwde hoofdplanning blijven gebruiken. Uw omgevingsbeheerder wordt op de hoogte gebracht als er actie moet worden ondernomen.

### <a name="production-scenarios"></a>Productiescenario's

We gebruiken geplande productieorders, maar ik maak me zorgen over wat er gebeurt als we naar versie 10.0.16 upgraden. Moet ik actie ondernemen?

**Antwoord:** Maak u geen zorgen. U kunt de ingebouwde hoofdplanning blijven gebruiken in versie 10.0.16. We raden u echter aan te beoordelen of migratie naar Planningsoptimalisatie kan worden gestart met de huidige functionaliteit. We raden u ook aan om op de hoogte te blijven van nieuwe functies.

### <a name="email-from-microsoft"></a>E-mail van Microsoft

Onze omgevingsbeheerder heeft een e-mailbericht ontvangen van Microsoft. Deze e-mail geeft aan dat wij moeten migreren naar Planningsoptimalisatie of een uitzondering moeten aanvragen. Moet ik actie ondernemen?

**Antwoord:** Ja. Uw omgeving wordt beïnvloed, tenzij u de instructies in het e-mailbericht opvolgt. U kunt migreren naar Planningsoptimalisatie op de opgegeven datum of een uitzondering aanvragen met behulp van de koppeling in het e-mailbericht. Met deze koppeling wordt een vragenlijst geopend. Nadat u deze vragenlijst hebt ingevuld en verzonden, ontvangt u een antwoord via e-mail. Hoewel dit een handmatig proces is, probeert Microsoft binnen een week te antwoorden nadat de vragenlijst is ingediend.

### <a name="error-messages"></a>Foutmeldingen

Ik gebruik versie 10.0.16 of hoger en het volgende foutbericht wordt weergegeven wanneer ik hoofdplanning uitvoer. Is hoofdplanning geblokkeerd?

> Dit foutbericht wordt weergegeven omdat de ingebouwde engine voor hoofdplanning werd gebruikt voor scenario's die worden ondersteund door Planningsoptimalisatie. U moet nu migreren naar Planningsoptimalisatie, omdat de huidige ingebouwde hoofdplanning wordt afgeschaft. De uitvoering van deze hoofdplanning is succesvol voltooid.
>
> Als uw migratie sterke afhankelijkheden heeft van functies die in behandeling zijn, kan een uitzondering voor het gebruik van de ingebouwde hoofdplanningsengine worden aangevraagd.
>
> Vul de volgende vragenlijst in om aan de slag te gaan en indien relevant uitzondering van de migratie naar Planningsoptimalisatie aan te vragen.

**Antwoord:** Nee, de hoofdplanning wordt niet geblokkeerd. De uitvoering van de hoofdplanning is voltooid en u kunt het resultaat op de gebruikelijke manier gebruiken. Om dit foutbericht echter te vermijden tijdens toekomstige uitvoeringen van hoofdplanningen, moet u direct migreren naar Planningsoptimalisatie of een uitzondering aanvragen via de koppeling in het foutbericht.
