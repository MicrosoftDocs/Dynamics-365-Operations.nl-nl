---
title: Power BI-inoud Beveiliging instellen voor de kostprijsboekhoudingsanalyse
description: In dit onderwerp wordt uitgelegd hoe u de beveiliging op toegangsniveau in Kostprijsboekhouding kunt doorvoeren naar beveiliging op rijniveau in Power BI. Deze functionaliteit borgt dat gebruikers alleen Power BI-gegevens zien waar hen toegang toe is verleend.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270294
ms.assetid: 3a7ba8b0-ac57-4159-9cd8-4308f6021f36
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d1cd378a58d4a4fe4388238f97e84a8e2b07937b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "352868"
---
# <a name="set-up-security-for-the-cost-accounting-analysis-power-bi-content"></a>Power BI-inoud Beveiliging instellen voor de kostprijsboekhoudingsanalyse

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de beveiliging op toegangsniveau in Kostprijsboekhouding kunt doorvoeren naar beveiliging op rijniveau in Power BI. Deze functionaliteit borgt dat gebruikers alleen Power BI-gegevens zien waar hen toegang toe is verleend.

## <a name="overview"></a>Overzicht

De Microsoft Power BI-inhoud **Analyse van kostprijsboekhouding** maakt gebruik van beveiliging op rijniveau in Power BI om toegang door gebruikers te beperken. Beveiliging is gebaseerd op de organisatiehiërarchie op toegangsniveau die is ingesteld in de parameters voor kostprijsboekhouding. Meer informatie over de Power BI-inhoud **Analyse van kostprijsboekhouding** vindt u in het onderwerp [Power BI-inhoud voor analyse van kostprijsboekhouding](cost-accounting-analysis-content-pack.md).

## <a name="setup"></a>Instellen
Om beveiliging op toegangsniveau door te voeren in Power BI, moet de eigenaar van de Power BI-inhoud deze stappen uitvoeren.

> [!NOTE]
> De gebruiker die de Power BI-inhoud **Analyse van kostprijsboekhouding** publiceert, wordt automatisch de eigenaar. Alleen een eigenaar kan de beveiliging in Power BI instellen. Bovendien kan, totdat een eigenaar andere gebruikers toevoegt op PowerBI.com, niemand behalve de eigenaar de gegevens in de Power BI-inhoud **Analyse van kostprijsboekhouding** zien.

1. Publiceer het definitiebestand in Power BI.
2. Meld u aan bij PowerBI.com.
3. Zoek de gegevensset voor de Power BI-inhoud **Analyse van kostprijsboekhouding**.
4. Open de pagina Beveiliging.

    ![De pagina Beveiliging openen](./media/CA-picture-1.png)

5. De rol **Controller voor kostenobjecten** is al gemaakt. Voeg andere leden toe die lid zijn van de organisatiehiërarchie op toegangsniveau van Kostprijsboekhouding.

    ![Leden toevoegen](./media/CA-picture-2.png)

Gebruikers die zijn toegevoegd aan de rol **Controller voor kostenobjecten** zien alleen de gegevens die ze mogen zien, volgens de definitie in de organisatiehiërarchie op toegangsniveau van Kostprijsboekhouding.

> [!NOTE]
> Beveiliging op rijniveau geldt voor tegels en rapporten in Microsoft Dynamics 365 for Finance and Operations die zijn ingesloten vanuit Power BI.

## <a name="updating-security"></a>Beveiliging bijwerken
Als de beveiliging op toegangsniveau in Kostprijsboekhouding wordt bijgewerkt en u deze wijzigingen wilt overnemen in Power BI, moet u de entiteitopslag voor de Power BI-inhoud **Analyse van kostprijsboekhouding** bijwerken. Nadat het bijwerken van de entiteitopslag vanuit Finance and Operations is voltooid, moet u de artefacten op PowerBI.com bijwerken. Meer informatie over het bijwerken van de entiteitopslag vindt u in het onderwerp [De entiteitopslag bijwerken](power-bi-integration-entity-store.md#update-entity-store). De eigenaar van de Power BI-inhoud **Analyse van kostprijsboekhouding** moet ook een update van de entiteitopslag uitvoeren als nieuwe gebruikers toegang krijgen tot de organisatiehiërarchie. Bovendien moet de eigenaar de nieuwe gebruikers toevoegen aan de rol **Controller voor kostenobjecten** in PowerBI.com, zodat voor hen ook beveiliging op rijniveau wordt toegepast.

## <a name="disabling-security"></a>Beveiliging uitschakelen
Er wordt vanuit gegaan dat uw organisatie de toegang tot gegevens wil beperken. Als om de een of andere reden de beveiligingsparameters zijn uitgeschakeld wanneer u Kostprijsboekhouding uitvoert, moet de eigenaar in plaats daarvan gebruikers toevoegen aan de rol **Kostenaccountant** in Power BI. Als u de beveiliging van een ingeschakelde status wijzigt in een uitgeschakelde status, is het een goed idee om gebruikers te verwijderen uit de rol **Controller voor kostenobjecten**. Als u de beveiliging weer inschakelt, moet u dit natuurlijk andersom doen. Gebruikers kunnen lid zijn van beide rollen. Van gekoppelde toegang spreken we wanneer de beide rollen zijn verenigd. In het geval van de Power BI-inhoud **Analyse van kostprijsboekhouding** hebben gebruikers met gekoppelde toegang onbeperkte toegang tot gegevens. Als u beperkte toegang wilt toepassen, moet u aan gebruikers alleen de rol **Controller voor kostenobjecten** toewijzen. Deze updates van de beveiliging op rijniveau zijn onmiddellijk van kracht. De betreffende gebruikers moeten hun browser vernieuwen.

## <a name="additional-resources"></a>Aanvullende bronnen
Meer informatie over beveiliging op rijniveau in Power BI vindt u in [Beveiliging van uw model in Power BI beheren](https://powerbi.microsoft.com/en-us/documentation/powerbi-admin-rls/#manage-security-on-your-model).
