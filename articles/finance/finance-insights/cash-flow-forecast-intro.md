---
title: Cashflowprognose (preview)
description: In dit onderwerp wordt de functie voor cashflowprognoses beschreven.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 3f16c8471123969443af52ff9bed7fc017b8e9c2
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/03/2021
ms.locfileid: "6339210"
---
# <a name="cash-flow-forecast-preview"></a>Cashflowprognose (preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Cashflow is van groot belang voor alle bedrijven. Zelfs winstgevende bedrijven kunnen te maken krijgen met betalingsproblemen als de cashflow niet op peil is om onmiddellijke behoeften te voldoen. De prognosefunctie voor cashflow in Financiële inzichten kan bedrijven helpen hun contante saldi effectief te controleren en te beheren. Deze functie maakt gebruik van machine learning om bedrijven te helpen hun cashflowprognose nauwkeuriger te maken. Ook kunnen managers beslissingen nemen over het optimaliseren van verkoopkansen in de context van hun huidige financiële positie. 

Voor de meeste bedrijven is het beheer van de cashflow en het uitvoeren van cashflowprognoses een omslachtig, herhalend en handmatig proces. De meeste bedrijven vertrouwen op Microsoft Excel-oplossingen met verschillende complexiteitsniveaus. De uitdagingen voor een nauwkeurige cashflowprognose zijn:

- Gegevens zijn niet beschikbaar voor besluitvormers omdat ze over verschillende plaatsen zijn verspreid, waaronder: 
  - Het boekhoud- of planningssysteem voor bedrijfsmiddelen
  - Financiële planningssoftware
  - Excel
  - Andere softwaretoepassingen 
- Prognoses zijn gebaseerd op interne kennis die zich in "silo's" bevindt in verschillende domeinen of afdelingen.
- Het meten van de nauwkeurigheid van cashflowprognoses nadat de financiële gegevens zijn gerealiseerd, is onzeker en moeilijk.
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a>Details van de functie voor cashflowprognoses
De functie voor cashflowprognoses bevat de volgende onderdelen. 

- U kunt de cashflowgegevens van externe systemen eenvoudig integreren in Dynamics 365 Finance. Cashflowprognoses kunnen ook het raamwerk voor importeren/exporteren van gegevens gebruiken. Met dit raamwerk is integratie in Excel OData eenvoudig. U kunt ook gegevens uit meerdere bronnen combineren om een allesomvattende cashflowoplossing te creëren. 

- Introduceert een intelligente kaspositie. De kaspositie wordt opgesteld op basis van het betalingsgedrag van de klant om te voorspellen wanneer een bedrijf kan verwachten dat contant geld op hun rekening beschikbaar is. De historische patronen van de betalingen aan leveranciers worden geanalyseerd, om te voorspellen wanneer toekomstige facturen en orders waarschijnlijk zullen worden betaald. 

- Introduceert intelligente cashflowprognoses voor de lange termijn met behulp van tijdreeksprognoses via automatische integratie met AI Builder.

- Biedt de mogelijkheid om specifieke cashflowposities of -prognoses op te slaan, te bewerken en vervolgens de prognoseprestaties eenvoudig te vergelijken en te meten met de werkelijke financiële waarden.

- Maakt wat-als-analyse mogelijke via vergelijking van momentopnamen. U kunt bijvoorbeeld meerdere momentopnamen maken die een optimistische, pessimistische en de meest realistische weergaven van uw cashflow vertegenwoordigen, en vervolgens de verschillen vergelijken en weergeven.

- Biedt de mogelijkheid om de cashflowprognose voor meerdere valuta's en rechtspersonen weer te geven, en de cashflow te filteren en te bekijken die betrekking heeft op een bankrekening. 

- U kunt filteren op bankrekeningen die zijn gerelateerd aan financiële dimensies.

Met de functionaliteit voor cashflowprognoses in Dynamics 365 Finance kan uw organisatie het saaie, complexe en terugkerende werk voor cashflowprognoses omzetten in een eenvoudig, geautomatiseerd proces. Door de saaie aspecten van cashflowprognoses te automatiseren kunt u zich concentreren op belangrijke besluiten om de gewenste bedrijfsresultaten te behalen.

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Dimensies voor cashflowprognose instellen
Met een nieuw tabblad op de pagina **Cashflowprognose instellen** kunt u bepalen welke financiële dimensies moeten worden gebruikt voor het filteren in het werkgebied **Cashflowprognose**. Dit tabblad wordt alleen weergegeven wanneer de functie Cashflowprognoses is ingeschakeld. 

Kies op het tabblad **Dimensies** in de lijst de dimensies die u wilt gebruiken voor het filteren en verplaats deze naar de rechterkolom met de pijltoetsen. Er kunnen slechts twee dimensies worden geselecteerd voor het filteren van cashflowprognosegegevens. 

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
