---
title: Jaarafsluiting optimaliseren
description: In dit artikel wordt de service-invoegtoepassing Jaarafsluiting optimaliseren beschreven die beschikbaar is voor het jaarafsluitingsproces van het grootboek.
author: moaamer
ms.date: 11/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2022-11-28
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 41d0c2975341cf3d612cc36be348326e24e94f1b
ms.sourcegitcommit: 707957bb7bcd98faf2600eff1c98067901a0fb73
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/08/2022
ms.locfileid: "9750006"
---
# <a name="optimize-year-end-close"></a>Jaarafsluiting optimaliseren

Met de service-invoegtoepassing Jaarafsluiting optimaliseren voor Microsoft Dynamics 365 Finance kan de jaarafsluiting worden uitgevoerd buiten het AOS-exemplaar (Application Object Server) voor Dynamics 365 Finance-resources. Hierbij wordt gebruikgemaakt van microservicetechnologie. De voordelen die zijn gekoppeld aan de functionaliteit Jaarafsluiting optimaliseren omvatten betere prestaties en minimale gevolgen voor de SQL-database tijdens de jaarafsluiting.

U moet de volgende taken uitvoeren om de functionaliteit Jaarafsluiting optimaliseren te gebruiken:

1. Installeer de service-invoegtoepassing Jaarafsluiting optimaliseren vanuit uw project in Microsoft Dynamics Lifecycle Service.
2. Schakel de functie **Jaarafsluiting optimaliseren** in Functiebeheer in.

> [!NOTE]
> U kunt de huidige functionaliteit voor het sluiten van het jaar voor nog gebruiken voor Finance-resources door de functie **Jaarafsluiting optimaliseren** uit te schakelen in Functiebeheer.

## <a name="improved-performance"></a>Betere prestaties

De functie **Jaarafsluiting optimaliseren** is ontworpen om de jaarafsluiting te versnellen, met name voor klanten met grote hoeveelheden gegevens. Wanneer de jaarafsluiting wordt uitgevoerd voor een service, wordt de zware verwerking van Finance-resources overgeheveld om de verwerkingstijd te verminderen en de resources vrij te maken die van invloed kunnen zijn op de dagelijkse bewerkingen van andere gebruikers.

De functie **Jaarafsluiting optimaliseren** kan u helpen de volgende doelen te behalen:

- Vereenvoudig de prestaties van de jaarafsluiting door de runtime te verkorten.
- Verminder het effect op andere processen tijdens de uitvoering van de jaarafsluiting.
- Verbeter de rapportage en correcties voor de eindejaarsresultaten omdat de uitvoering van de jaarafsluiting minder tijd kost.

## <a name="new-options-and-visibility"></a>Nieuwe opties en zichtbaarheid

Wanneer de functie **Jaarafsluiting optimaliseren** is ingeschakeld, worden op de volgende plaatsen de twee nieuwe kolommen **Resultaten** en **Status** toegevoegd:

- Op de pagina **Jaarafsluiting**
- In het dialoogvenster **Jaarafsluitingsresultaten**
- In de opties voor het **overboeken van financiële dimensies van balans** op de pagina **Jaarafsluitingssjabloon**

In de volgende afbeelding ziet u een voorbeeld van de kolommen **Resultaten** en **Status** op de pagina **Jaarafsluiting**. U kunt de koppeling **Resultaten weergeven** in de kolom **Resultaten** selecteren om de resultaten van de jaarafsluiting te openen. In de kolom **Status** wordt de huidige status van de jaarafsluiting weergegeven. Daarom bieden de nieuwe kolommen zichtbaarheid in de voortgang van het jaarafsluitingsproces.

[![De kolommen Resultaten en Status op de pagina Jaarafsluiting.](./media/Yearendclose.jpg)](./media/Yearendclose.jpg)

Wanneer de functie **Jaarafsluiting optimaliseren** is ingeschakeld, wordt bovendien het sneltabblad **Financiële dimensies van balans** beschikbaar op de pagina **Jaarafsluitingssjabloon**. U kunt dit sneltabblad gebruiken om financiële dimensies van de balans gedetailleerd op te geven wanneer u een jaar afsluit. Deze mogelijkheid is gelijk aan de mogelijkheid die al beschikbaar is voor verlies-en-winstrekeningen.

## <a name="architecture-and-data-flow"></a>Architectuur en gegevensstroom

Als u de functie **Jaarafsluiting optimaliseren** wilt gebruiken en de jaarafsluiting wilt uitvoeren op een microservice, moet u de service-invoegtoepassing Jaarafsluiting optimaliseren installeren vanuit Lifecycle Services en vervolgens de functie **Jaarafsluiting optimaliseren** in Functiebeheer inschakelen.

In de volgende afbeelding ziet u dat bij de verwerking van de jaarafsluiting wordt gecontroleerd of de invoegfunctie is geïnstalleerd en of de functie is ingeschakeld. Als aan beide voorwaarden is voldaan, wordt de jaarafsluiting uitgevoerd op de microservice.

[![Gegevensstroomdiagram.](./media/Lifecycle-services.jpg)](./media/Lifecycle-services.jpg)

## <a name="high-level-flow-for-year-end-close-processing"></a>Stroom op hoog niveau voor verwerking van jaarafsluiting

1. Het jaarafsluitingsproces begint in Finance bij **Grootboek \> Afgesloten periode \> Jaarafsluiting**. Het proces maakt afsluitingsbatchtaken en taken voor de rechtspersonen die worden afgesloten.
2. De jaarafsluiting bepaalt of de jaarafsluiting moet worden uitgevoerd op basis van de microservice of de huidige afsluitingslogica.

    - Als de service-invoegtoepassing Jaarafsluiting optimaliseren installeren is geïnstalleerd in Lifecycle Services en de functie **Jaarafsluiting optimaliseren** in Functiebeheer is ingeschakeld, wordt de jaarafsluiting uitgevoerd op basis van de microservice.

        1. Met de functionaliteit Jaarafsluiting optimaliseren wordt een servicetaak voor jaarafsluiting gemaakt voor elke rechtspersoon die wordt afgesloten. Vervolgens wordt de logica voor jaarafsluiting uitgevoerd. De microservice voert de jaarafsluiting uit.
        2. Finance controleert de jaarafsluiting op de microservice om te bepalen wanneer de microservice is voltooid. De jaarafsluitingsresultaten worden vervolgens bijgewerkt op de pagina **Jaarafsluiting** in Finance.

    - Anders wordt de jaarafsluiting uitgevoerd op basis van de huidige afsluitingslogica.
