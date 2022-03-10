---
title: Startpagina van Finance Insights
description: Finance Insights biedt configureerbare en uitbreidbare modellen om u te helpen de cashflow van uw bedrijf nauwkeurig en intelligent te voorspellen, te voorspellen wanneer u een betaling voor openstaande debiteuren ontvangt en een budgetvoorstel te genereren waarmee het budgetproces kan worden versneld. Al deze functies zijn gebaseerd op intelligente machine learning-modellen.
author: ShivamPandey-msft
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "14151"
- intro-internal
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 05b0de8b0104238a33f006234d4a0e8ba9fcdb2a
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087288"
---
# <a name="finance-insights-home-page"></a>Startpagina van Finance Insights

[!include [banner](../includes/banner.md)]

Finance Insights biedt configureerbare en uitbreidbare oplossingen om u te helpen de cashflow van uw bedrijf intelligent te voorspellen, te voorspellen wanneer u mogelijk een betaling voor openstaande debiteuren ontvangt en een budgetvoorstel te genereren waarmee het budgetproces kan worden versneld. Deze functies maken gebruik van intelligente machine learning-sjablonen om modellen samen te bouwen met gegevens die u verstrekt (inclusief gegevens van derden, zoals informatie over consumentenrapports van een bureau). Met deze intelligente mogelijkheden wordt de besluitvorming bevorderd en kunt u actie ondernemen om effectief op huidige en verwachte zakelijke activiteiten te reageren. U bent verantwoordelijk voor alle gegevens die worden gebruikt met of uitgevoerd vanuit Finance insights.

> [!NOTE]
> Finance Insights is beschikbaar voor implementatie in de Verenigde Staten, Canada, het Verenigd Koninkrijk, Europa, Azië/Pacific, Japan, Australië en Nieuw-Zeeland. Microsoft voegt incrementeel ondersteuning toe voor meer regio's.

## <a name="prerequisites"></a>Vereisten

In deze sectie worden de vereisten voor het gebruik van Financiële inzichten weergegeven. Waar mogelijk worden koppelingen naar bronnen met aanvullende informatie verstrekt.

### <a name="system-requirements"></a>Systeemvereisten

Een Tier-2-omgeving (multi-box) is vereist voor de preview van Finance insights. Zie [Omgevingsplanning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) voor achtergrondinformatie over omgevingen.

### <a name="version-requirements"></a>Versievereisten

Dit onderwerp is van toepassing op Microsoft Dynamics 365 Finance versie 10.0.21 en hoger.

### <a name="license-requirements"></a>Licentievereisten

In Finance Insights wordt gebruikgemaakt van AI Builder-credits om financiële voorspellingen te maken. Alle benodigde licenties hiervoor worden opgenomen in de tenantlicentie. Elke Dynamics 365 Finance-tenant krijgt 20.000 AI Builder-credits per maand. Als er aanvullende credits vereist zijn, kunnen deze rechtstreeks worden aangeschaft bij AI Builder.

### <a name="historical-data-requirements"></a>Historische gegevens-vereisten

Er is ten minste één jaar klantfacturen nodig om het machine learning-model te trainen dat wordt gebruikt voor de functie Voorspellingen van klantbetalingen. Drie jaar historische gegevens worden aanbevolen voor cashflowprognoses. Drie jaar historische budgetten en/of actualiteiten worden aanbevolen voor budgetvoorstellen.

## <a name="configure-finance-insights"></a>Finance Insights configureren

U moet configuratiestappen uitvoeren voordat u Finance Insights kunt gebruiken. Zie [Configuratie voor Financiële inzichten](configure-for-fin-insites.md) voor meer informatie over het configureren van Financiële inzichten.

## <a name="create-a-data-integrator-project"></a>Een gegevensintegratorproject maken

U moet een gegevensintegratorproject maken, zodat de gegevens die het machine learning-model genereert, in Dynamics 365 Finance kunnen stromen. Zie [Een gegevensintegratorproject maken](create-data-integrate-project.md) voor de stappen om dat project te maken.

## <a name="enable-finance-insights-capabilities"></a>Mogelijkheden van Finance Insights inschakelen

Wanneer u de configuratiestappen hebt voltooid en demogegevens hebt ingesteld, moet u elke mogelijkheid die u wilt gebruiken, inschakelen en instellen: klantbetalingsvoorspellingen, cashflowprognoses en budgetvoorstellen.

### <a name="enable-customer-payment-predictions"></a>Voorspellingen voor klantbetalingen inschakelen
Als u demogegevens gebruikt om klantbetalingsvoorspellingen te testen, moet u mogelijk extra demogegevens importeren om het AI-model te kunnen maken. 

Als u Voorspellingen voor klantbetalingen wilt inschakelen, moet u een reeks stappen uitvoeren om een machine learning-model te maken waarin de gegevens van uw organisatie worden gebruikt om voorspellingen te genereren over wanneer klanten waarschijnlijk openstaande facturen betalen, en wanneer bepaalde facturen waarschijnlijk zullen worden betaald. Zie [Voorspellingen van klantbetalingen inschakelen](enable-cust-paymnt-prediction.md) voor meer informatie en de stappen die u moet uitvoeren. 

### <a name="enable-cash-flow-forecasting"></a>Cashflowprognose inschakelen
Als u cashflowprognoses wilt inschakelen, moet u een reeks stappen uitvoeren om een Machine Learning-model te maken waarin de gegevens van uw organisatie worden gebruikt om cashflowprognoses te genereren. Zie [Cashflowprognose inschakelen](enable-cash-flow-forecasting.md) voor meer informatie en de specifieke stappen die u moet uitvoeren.

### <a name="enable-budget-proposals"></a>Budgetvoorstellen inschakelen

De functie Budgetvoorstellen gebruikt een machine learning-model met de historische gegevens van uw organisatie om een budgetvoorstel te genereren. Het gegenereerde voorstel kan u helpen bij het starten van een budgetteringsproces dat effectiever en efficiënter is dan een handmatig proces. Zie voor de specifieke stappen voor het inschakelen van deze functie [Budgetvoorstellen inschakelen](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Werken met functies van Finance Insights

### <a name="using-customer-payment-predictions"></a>Voorspellingen voor klantbetalingen gebruiken

- Zie [Voorspellingen voor klantbetalingen gebruiken](use-customer-payment-predictions.md) voor meer informatie over hoe Voorspellingen voor klantbetalingen de gegevens kan leveren die nodig zijn om proactief incasso-activiteiten uit te voeren.
- Zie [Het aanvankelijke voorspellingsmodel voor klantbetalingen evalueren](evaluate-payment-prediction.md) voor informatie die u kan helpen de effectiviteit van het voorspellingsmodel te evalueren nadat u de functie bent gaan gebruiken.
- Zie [Het voorspellingsmodel verbeteren](improve-model.md) voor informatie die u kan helpen bij het aanpassen van de gegevens die worden gebruikt om de voorspelling te maken en om de effectiviteit te verbeteren.
- Voor meer informatie over de resultaten van AI-voorspellingsmodellen zie [Resultaten van machine learning-modellen](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Cashflowprognoses gebruiken

De mogelijkheid Cashflowprognose kan u helpen om de positie van contant geld nauwkeuriger in te schatten. De intelligente cashflowprognoses worden gebouwd op basis van de bestaande functionaliteit voor cashflowprognoses in Dynamics 365 Finance. Raadpleeg voor het bekijken van de bestaande mogelijkheid [Cashflowprognose](../cash-bank-management/cash-flow-forecasting.md).

- Zie [Cashflowprognose](cash-flow-forecast-intro.md) voor meer informatie over de nieuwe mogelijkheden in Cashflowprognose.
- Zie [Externe gegevens gebruiken in cashflowprognoses](external-data-in-cash-flow.md) voor informatie over het importeren van externe gegevens die u in de cashflowprognose wilt opnemen. 
- Zie [Kaspositie](cash-position.md) voor informatie over het gebruik van een AI-model voor cashflowprognoses voor de korte termijn.
- Zie [Overzicht van momentopnamen](payment-snapshots.md) voor informatie over het opslaan van cashflowposities en cashflowprognoses als momentopnamen en voor het vergelijken van een momentopname met werkelijke waarden.

### <a name="using-budget-proposal"></a>Budgetvoorstel gebruiken

Zie [Budgetvoorstellen](budget-proposals.md) voor informatie over het versnellen van het maken van een budget. 

## <a name="feedback-and-support"></a>Feedback en ondersteuning

Stuur een e-mail naar [Finance Insights](mailto:fiap@microsoft.com) als u feedback wilt geven of ondersteuning nodig hebt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
