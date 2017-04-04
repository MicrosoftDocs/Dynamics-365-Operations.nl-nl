---
title: Beveiliging voor de analyse van kostprijsboekhouding Power BI-inhoud instellen
description: Dit onderwerp wordt uitgelegd hoe u de beveiliging van het toegangsniveau tot beveiligbare objecten in de kostprijsboekhouding voor beveiliging in Microsoft Power BI kunt doorgeven. Deze functionaliteit zorgt ervoor dat gebruikers alleen Power BI-gegevens die ze toegang tot krijgen zien.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 1e42622e7621c645d7eda3299f78c34c7e41a251
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Beveiliging voor de analyse van kostprijsboekhouding Power BI-inhoud instellen

Dit onderwerp wordt uitgelegd hoe u de beveiliging van het toegangsniveau tot beveiligbare objecten in de kostprijsboekhouding voor beveiliging in Microsoft Power BI kunt doorgeven. Deze functionaliteit zorgt ervoor dat gebruikers alleen Power BI-gegevens die ze toegang tot krijgen zien.

<a name="overview"></a>Overzicht
--------

De **Analyse kostprijsboekhouding** Microsoft Power BI inhoud Power BI rijniveau beveiliging gebruikt van een gebruiker toegang te beperken. Beveiliging is gebaseerd op het toegangsniveau tot beveiligbare objecten organisatiehiërarchie die is ingesteld in de parameters voor kostprijsboekhouding. Voor meer informatie over de **Analyse kostprijsboekhouding** Power BI-inhoud, Zie [Analyse kostprijsboekhouding Power BI inhoud](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Instellen
Als u wilt toegang beveiligingsniveau Power BI worden doorgegeven, moet de eigenaar van de inhoud van de Power BI Volg deze stappen. **opmerking:** de gebruiker die u publiceert de **Analyse kostprijsboekhouding** Power BI-inhoud wordt automatisch de eigenaar. Alleen een eigenaar kunt van de beveiliging in Power BI instellen. Bovendien totdat een eigenaar wordt toegevoegd van andere gebruikers in PowerBI.com, niemand behalve de eigenaar zien alle gegevens in de **Analyse kostprijsboekhouding** Power BI-inhoud.

1.  Het definitiebestand publiceren naar Power BI.
2.  Log in op PowerBI.com.
3.  Zoeken naar de dataset voor de **Analyse kostprijsboekhouding** Power BI-inhoud.
4.  Open het tabblad Beveiliging. 

    [![De van de beveiligingspagina wordt geopend](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-1.png)

5.  De **kosten object controller** rol al is gemaakt. Andere leden die deel van de organisatiehiërarchie van kostprijsboekhouding toegangsniveau tot beveiligbare objecten uitmaken toevoegen. 

    [![Leden toevoegen](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)](https://msdynamics.blob.core.windows.net/media/2017/02/CA-picture-2.png)

Gebruikers die zijn toegevoegd aan de **kosten object controller** rol ziet alleen de gegevens die ze zien kunnen, volgens de definitie in de organisatiehiërarchie van kostprijsboekhouding toegangsniveau openen. **opmerking:** beveiliging van toepassing is op naast elkaar en rapporten in Microsoft Dynamics 365 voor bewerkingen die zijn ingesloten in Power BI.

## <a name="updating-security"></a>Beveiliging bijwerken
Als beveiliging in kostprijsboekhouding toegangsniveau tot beveiligbare objecten wordt bijgewerkt en u Power BI om weer te geven die updates wilt, moet u de winkel entiteit voor bijwerken de **Analyse kostprijsboekhouding** Power BI-inhoud. Nadat u het bijwerken van de winkel entiteit van Dynamics 365 voor bewerkingen hebt voltooid, moet u de onderdelen op PowerBI.com bijwerken. Zie voor meer informatie hierover een update van de winkel entiteit [Update entiteit winkel](power-bi-integration-entity-store.md#update-entity-store). De eigenaar van de **Analyse kostprijsboekhouding** Power BI-inhoud ook een update van de winkel entiteit moet doen als u nieuwe gebruikers toegang krijgen tot de organisatiehiërarchie. Bovendien de eigenaar moet de nieuwe gebruikers toevoegen aan de **kosten object controller** rol in PowerBI.com, zodat deze zekerheid rijniveau voor hen wordt toegepast.

## <a name="disabling-security"></a>Beveiliging uitschakelen
Nemen we aan dat uw organisatie wil beperken van toegang tot gegevens. Als de beveiligingsparameters zijn voor een of andere reden uitgeschakeld wanneer u kostprijsboekhouding uitvoert, de eigenaar moet gebruikers toevoegen aan de **accountant kosten** rol in Power BI in plaats daarvan. Als u beveiliging van een ingeschakelde status wijzigen in een uitgeschakeld, is het een goed idee om gebruikers verwijderen uit de **kosten object controller** rol. En vice versa als u beveiliging opnieuw in te schakelen. Gebruikers kunnen behoren tot beide rollen. Gemeenschappelijke toegang is de vereniging van beide rollen. In geval van de **Analyse kostprijsboekhouding** Power BI inhoud, de gebruikers die beschikken over gezamenlijke hebben onbeperkte toegang tot gegevens. Als u wilt toepassen met beperkte toegang, gebruikers beschikken uitsluitend naar de **kosten object controller** rol. Deze beveiligingsupdates rijniveau zijn onmiddellijk van kracht. Betreffende gebruikers moeten hun browser vernieuwen.

## <a name="additional-resources"></a>Aanvullende bronnen
Zie voor meer informatie over beveiliging Power BI, [beheer van de beveiliging van uw Power BI-model](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).


