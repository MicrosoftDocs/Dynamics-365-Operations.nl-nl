---
title: Startpagina van Finance Insights (preview)
description: Finance Insights biedt configureerbare en uitbreidbare modellen om u te helpen de cashflow van uw bedrijf nauwkeurig en intelligent te voorspellen, te voorspellen wanneer u een betaling voor openstaande debiteuren ontvangt en een budgetvoorstel te genereren waarmee het budgetproces kan worden versneld. Al deze functies zijn gebaseerd op intelligente machine learning-modellen.
author: ShivamPandey-msft
ms.date: 07/16/2021
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
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 8c9d5b9857e978eb5e591f4d854d687f33b438025e81fe2c827ab7ecdb2be4e4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768814"
---
# <a name="finance-insights-home-page-preview"></a>Startpagina van Financiële inzichten (preview)

[!include [banner](../includes/banner.md)]

Financiële inzichten biedt configureerbare en uitbreidbare modellen om u te helpen de cashflow van uw bedrijf nauwkeurig en intelligent te voorspellen, te voorspellen wanneer u een betaling voor openstaande debiteuren ontvangt en een budgetvoorstel te genereren waarmee het budgetproces kan worden versneld. Al deze functies zijn gebaseerd op intelligente machine learning-modellen. Wanneer deze nieuwe mogelijkheden worden gecombineerd met automatisering in betalingen en incasso's van leveranciers, bieden ze een groot en intelligent financieel systeem dat de besluitvorming aanstuurt en u helpt actie te ondernemen om effectief te reageren op huidige en verwachte zakelijke uitdagingen.

> [!NOTE]
> De openbare preview van Finance Insights is beschikbaar voor implementatie in de Verenigde Staten van Amerika, Canada, het Verenigd Koninkrijk, Europa, Azië/Pacific, Australië en Nieuw-Zeeland. Microsoft voegt incrementeel ondersteuning toe voor meer regio's. Als u Finance Insights wilt inschakelen in productieomgevingen, moeten eerst de capaciteiten voor [Exporteren Data lAKE](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md) worden ingeschakeld in de productieomgeving.

> [!NOTE]
> Deze functionaliteit wordt aangeboden als een set preview-functies. Omdat het een preview-functie is, moet u de resulterende machine-leermodellen niet gebruiken als uitgangspunt voor uw zakelijke beslissingen of budgetvoorstellen. Uw gebruik van deze functie valt onder de [Aanvullende gebruiksrechtovereenkomst](https://go.microsoft.com/fwlink/?linkid=2105274).

## <a name="prerequisites"></a>Vereisten

In deze sectie worden de vereisten voor het gebruik van Financiële inzichten weergegeven. Waar mogelijk worden koppelingen naar bronnen met aanvullende informatie verstrekt.

### <a name="legal-requirements"></a>Wettelijke vereisten

Als u wilt deelnemen aan het preview-programma, vult u de [Preview Financiële inzichten voor Dynamics 365 Finance-overeenkomst](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUM1c0Uzc1RFpaU1RVTEwxVTNWUERPRThUSy4u) in.

### <a name="system-requirements"></a>Systeemvereisten

Een Tier-2-omgeving (multi-box) is vereist voor de preview van Finance insights. Zie [Omgevingsplanning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) voor achtergrondinformatie over omgevingen.

### <a name="version-requirements"></a>Versievereisten

Dit document is van toepassing op versie 10.0.11 van Finance and Operations-apps (platformupdate 35) en latere versies.

### <a name="historical-data-requirements"></a>Historische gegevens-vereisten

Er is ten minste één jaar klantfacturen nodig om het machine learning-model te trainen dat wordt gebruikt voor de functie Voorspellingen van klantbetalingen.

### <a name="role-and-permission-requirements"></a>Vereisten voor rollen en machtigingen

Wijzigingen worden aangebracht in Microsoft Dynamics 365 Finance, Microsoft Dynamics Lifecycle Services (LCS), Power Apps en Azure. In deze omgevingen zijn juiste machtigingen vereist. Hier volgen enkele voorbeelden van de wijzigingen die worden aangebracht:

- Er wordt een nieuwe omgeving gemaakt in Microsoft Power Platform.
- Er wordt een opslagaccount, een sleutelkluis en een toepassing gemaakt in Azure.
- De tenantbeheerder van Active Directory moet de toepassing AI Builder machtigen om toegang te krijgen tot de data lake.
- De functie wordt ingeschakeld in Dynamics 365.

Bij het voltooien van dit proces helpt het als u vertrouwd bent met het maken en beheren van resources in Azure, Microsoft Dataverse en LCS.

## <a name="configure-finance-insights"></a>Finance Insights configureren

U moet enkele configuratiestappen uitvoeren voordat u Finance Insights kunt gebruiken. Zie voor meer informatie over het configureren van Finance Insights:
  - Voor versies tot en met 10.0.19: [Configuratie voor Finance Insights (preview) - versies tot en met 10.0.19](configure-for-fin-insites.md).
  - Voor versies 10.0.20 en hoger: [Configuratie voor Finance Insights (preview) - versie 10.0.20 en hoger](configure-for-fin-insites-PubPrvw.md).

## <a name="create-a-data-integrator-project"></a>Een gegevensintegratorproject maken

U moet een gegevensintegratorproject maken, zodat de gegevens die het machine learning-model genereert, in Dynamics 365 Finance kunnen stromen. Zie [Een gegevensintegratorproject maken](create-data-integrate-project.md) voor de stappen om dat project te maken.

## <a name="enable-finance-insights-capabilities"></a>Mogelijkheden van Finance Insights inschakelen

Wanneer u de configuratiestappen hebt voltooid en demogegevens hebt ingesteld, moet u elke mogelijkheid die u wilt gebruiken, inschakelen en instellen: klantbetalingsvoorspellingen, cashflowprognoses en budgetvoorstellen.

### <a name="enable-customer-payment-predictions"></a>Voorspellingen voor klantbetalingen inschakelen
Als u demogegevens gebruikt om klantbetalingsvoorspellingen te testen, moet u mogelijk extra demogegevens importeren om het AI-model te kunnen maken. 

Als u Voorspellingen van klantbetalingen wilt inschakelen, moet u een reeks stappen uitvoeren om een machine learning model te maken waarin de gegevens van uw organisatie worden gebruikt om voorspellingen te genereren over wanneer klanten waarschijnlijk openstaande facturen betalen, en wanneer bepaalde facturen waarschijnlijk zullen worden betaald. Zie [Voorspellingen van klantbetalingen inschakelen](enable-cust-paymnt-prediction.md) voor meer informatie en de stappen die u moet uitvoeren. 

### <a name="enable-cash-flow-forecasting"></a>Cashflowprognose inschakelen
Als u cashflowprognoses wilt inschakelen, moet u een reeks stappen uitvoeren om een Machine Learning-model te maken waarin de gegevens van uw organisatie worden gebruikt om cashflowprognoses te genereren. Zie [Cashflowprognose inschakelen](enable-cash-flow-forecasting.md) voor meer informatie en de specifieke stappen die u moet uitvoeren.

### <a name="enable-budget-proposals"></a>Budgetvoorstellen inschakelen

De functie Budgetvoorstellen gebruikt een machine learning-model met de historische gegevens van uw organisatie om een budgetvoorstel te genereren. Het gegenereerde voorstel kan u helpen bij het starten van een budgetteringsproces dat effectiever en efficiënter is dan een handmatig proces. Zie voor de specifieke stappen voor het inschakelen van deze functie [Budgetvoorstellen inschakelen](enable-budget-proposal.md). 

## <a name="using-finance-insights-features"></a>Werken met functies van Finance Insights

### <a name="using-customer-payment-predictions"></a>Voorspellingen voor klantbetalingen gebruiken

De intelligente cashflowprognoses worden gebouwd op basis van de bestaande functionaliteit voor cashflowprognoses in Dynamics 365 Finance. Raadpleeg voor het bekijken van de bestaande mogelijkheid [Cashflowprognose](../cash-bank-management/cash-flow-forecasting.md).

- Zie [Voorspellingen van klantbetalingen gebruiken](use-customer-payment-predictions.md) voor meer informatie over hoe Voorspellingen van klantbetalingen de gegevens kan leveren die nodig zijn om proactief incasso-activiteiten uit te voeren.
- Zie [Het aanvankelijke voorspellingsmodel voor klantbetalingen evalueren](evaluate-payment-prediction.md) voor informatie die u kan helpen de effectiviteit van het voorspellingsmodel te evalueren nadat u de functie bent gaan gebruiken.
- Zie [Het voorspellingsmodel verbeteren](improve-model.md) voor informatie die u kan helpen bij het aanpassen van de gegevens die worden gebruikt om de voorspelling te maken en om de effectiviteit te verbeteren.

Voor meer informatie over de resultaten van AI-voorspellingsmodellen zie [Resultaten van machine learning-modellen](confusion-matrix.md).

### <a name="using-cash-flow-forecasts"></a>Cashflowprognoses gebruiken

De mogelijkheid Cashflowprognose kan u helpen om de positie van contant geld nauwkeuriger in te schatten. 

- Zie [Cashflowprognose](cash-flow-forecast-intro.md) voor meer informatie over de nieuwe mogelijkheden in Cashflowprognose.
- Zie [Externe gegevens gebruiken in cashflowprognoses](external-data-in-cash-flow.md) voor informatie over het importeren van externe gegevens die u in de cashflowprognose wilt opnemen. 
- Zie [Kaspositie](cash-position.md) voor informatie over het gebruik van een AI-model voor cashflowprognoses voor de korte termijn.
- Zie [Overzicht van momentopnamen](payment-snapshots.md) voor informatie over het opslaan van cashflowposities en cashflowprognoses als momentopnamen en voor het vergelijken van een momentopname met werkelijke waarden.

### <a name="using-budget-proposal"></a>Budgetvoorstel gebruiken

Zie [Budgetvoorstellen](budget-proposals.md) voor informatie over het versnellen van het maken van een budget. 

## <a name="feedback-and-support"></a>Feedback en ondersteuning

Stuur een e-mail naar [Inzichten voor betalingen van klanten (preview)](mailto:fiap@microsoft.com) als u feedback wilt geven of ondersteuning nodig hebt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
