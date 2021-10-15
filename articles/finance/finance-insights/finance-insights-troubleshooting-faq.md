---
title: Problemen met het instellen van Finance Insights oplossen
description: In dit onderwerp worden problemen weergegeven die kunnen optreden wanneer u functies van Finance Insights gebruikt. Er wordt ook uitgelegd hoe u deze problemen kunt oplossen.
author: panolte
ms.date: 08/20/2021
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
ms.search.validFrom: 2021-08-20
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 7ff42ffc334147c1a4c6b6349c86580df7f1955b
ms.sourcegitcommit: 47a3ad71210c7ac84d0c25e913c440b5ba205282
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2021
ms.locfileid: "7512885"
---
# <a name="troubleshoot-finance-insights-setup-issues"></a>Problemen met het instellen van Finance Insights oplossen

[!include [banner](../includes/banner.md)]

In dit onderwerp worden problemen weergegeven die kunnen optreden wanneer u functies van Finance Insights gebruikt. Er wordt ook uitgelegd hoe u deze problemen kunt oplossen.

## <a name="symptom-why-cant-i-map-the-customer-payment-insights-data-integration-template-destination-column"></a>Symptoom: waarom kan ik de doelkolom van de sjabloon voor Gegevensintegratie voor inzichten in klantbetalingen niet toewijzen?

### <a name="resolution"></a>Oplossing

Mogelijk gebruikt u een sjabloon voor een eerdere versie. Voor de release van versie 10.0.17 hebben gebruikers van de preview-versie de sjabloon **Resultaten van inzichten in klantbetalingen (CDS naar Fin en Ops)** van Gegevensintegratie geconfigureerd met behulp van de entiteit **Resultaat van betalingsvoorspelling** (preview). Na een upgrade naar 10.0.17 en hoger moet u de sjabloon voor Gegevensintegratie **Resultaten van inzichten in klantbetalingen (CDS naar Fin en Ops 10.0.17 en hoger)** gebruiken om de toewijzing te voltooien. Het is mogelijk dat u de doelkolom van de sjabloon voor Gegevensintegratie pas kunt toewijzen wanneer de lijst met entiteiten voor gegevensbeheer is vernieuwd en de entiteit **Resultaat van betalingsvoorspelling** in de lijst wordt weergegeven. Als u de lijst met entiteiten wilt vernieuwen en het resultaat van de betalingsvoorspelling wilt weergeven, moet u zowel in Microsoft Dynamics 365 Finance als in Dataverse (voorheen het beheerportaal Common Data Service \[CDS\]) een aantal stappen voltooien.

### <a name="in-finance"></a>In Finance

Volg deze stappen in Finance nadat u de upgrade hebt uitgevoerd.

1. Ga naar **Systeembeheer \> Werkruimten \> Gegevensbeheer**.
2. Selecteer in de werkruimte **Gegevensbeheer** de tegel **Raamwerkparameters**.
3. Selecteer op de pagina **Parameters van raamwerk voor gegevensimport/-export** de optie **Entiteitsinstellingen** en selecteer vervolgens **Entiteitslijst vernieuwen**.
4. Sluit de pagina **Parameters van raamwerk voor gegevensimport/-export**.
5. Selecteer in de werkruimte **Gegevensbeheer** de tegel **Gegevensentiteiten**.
6. Zoek naar Resultaat van betalingsvoorspelling. Controleer of de entiteit **Resultaat van betalingsvoorspelling** niet de preview-versie is. De naam van de preview-versie eindigt op '(preview)'. Als u alleen de preview-versie van de entiteit ziet, neemt u contact op met Microsoft Ondersteuning.

### <a name="in-dataverse"></a>In Dataverse

Volg deze stappen in het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com/environments) om uw gegevensintegratieprojecten bij te werken.

1. Als u een preview-versie van Finance Insights gebruikt, verwijdert u het project van Gegevensintegratie dat is gekoppeld aan de sjabloon **Resultaten van inzichten in klantbetalingen (CDS naar Fin en Ops)**.
2. Volg de stappen in [Een gegevensintegratieproject maken](create-data-integrate-project.md). Gebruik de sjabloon **Resultaten van inzichten in klantbetalingen (CDS naar Fin en Ops 10.0.17 en hoger)**.

## <a name="symptom-why-doesnt-the-cash-forecast-tab-in-the-cash-flow-forecast-workspace-show-any-data"></a>Symptoom: waarom worden op het tabblad Cashflowprognose in de werkruimte voor cashflowprognose geen gegevens weergegeven?

### <a name="resolution"></a>Oplossing

De functie voor cashflowprognoses in Contanten en bankbeheer en de functie Cashflowprognoses in Finance Insights moeten zijn ingesteld en ingeschakeld om gegevens juist weer te geven in de werkruimte **Cashflowprognose**.

Stel eerst de cashflowprognose en liquiditeitsrekeningen in en schakel deze in. Zie [Cashflowprognose](../cash-bank-management/cash-flow-forecasting.md) voor meer informatie. Als ze zijn ingesteld, maar u niet de resultaten ziet die u verwacht, raadpleegt u [Problemen met het instellen van cashflowprognoses oplossen](../cash-bank-management/cash-flow-forecasting-tsg.md) voor meer informatie.

Controleer vervolgens of de functie voor cashflowprognoses in Finance Insights (**Contanten en bankbeheer \> Instellen \> Finance Insights \> Cashflowprognoses**) is ingeschakeld en dat de training van het AI-model is voltooid. Als de training niet is voltooid, selecteert u **Nu prognose maken** om het modeltrainingsproces te starten.
