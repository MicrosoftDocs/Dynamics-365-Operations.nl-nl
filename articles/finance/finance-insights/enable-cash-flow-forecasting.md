---
title: Cashflowprognose inschakelen (preview)
description: In dit onderwerp wordt uitgelegd hoe u de functie Cashflowprognoses kunt inschakelen in Financiële inzichten.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2de75962f5b8a71c8f7138289078b5c669ae1daa
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5250573"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="6dd70-103">Cashflowprognose inschakelen (preview)</span><span class="sxs-lookup"><span data-stu-id="6dd70-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="6dd70-104">In dit onderwerp wordt uitgelegd hoe u de functie Cashflowprognoses kunt inschakelen in Financiële inzichten.</span><span class="sxs-lookup"><span data-stu-id="6dd70-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="6dd70-105">Als u betalingsvoorspellingen in de cashflow wilt gebruiken, moet u de functie Voorspellingen klantbetalingen instellen, zoals wordt beschreven in [Voorspellingen klantbetalingen inschakelen](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="6dd70-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="6dd70-106">Gebruik informatie op de omgevingspagina in Microsoft Dynamics Lifecycle Services (LCS) om verbinding te maken met het primaire exemplaar van Azure SQL voor die omgeving.</span><span class="sxs-lookup"><span data-stu-id="6dd70-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="6dd70-107">Voer de volgende Transact-SQL-opdracht (T-SQL) uit om flights in te schakelen voor de sandbox-omgeving.</span><span class="sxs-lookup"><span data-stu-id="6dd70-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="6dd70-108">(Mogelijk moet u de toegang voor uw IP-adres inschakelen in LCS voordat u extern verbinding kunt maken met Application Object Server \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="6dd70-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="6dd70-109">Als uw implementatie van Microsoft Dynamics 365 Finance een Service Fabric-implementatie is, kunt u deze stap overslaan.</span><span class="sxs-lookup"><span data-stu-id="6dd70-109">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="6dd70-110">Het Financiële inzichten-team zou de flight al voor u moeten hebben ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="6dd70-110">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="6dd70-111">Als de functies niet ziet in het werkgebied **Functiebeheer** of als u problemen ondervindt wanneer u deze wilt inschakelen, neemt u contact op met <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="6dd70-111">If you don't see the features in the **Feature management** workspace, or if experience issues when you try to turn them on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="6dd70-112">Open het werkgebied **Functiebeheer** en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="6dd70-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="6dd70-113">Selecteer **Controleren op updates**.</span><span class="sxs-lookup"><span data-stu-id="6dd70-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="6dd70-114">De volgende functies inschakelen:</span><span class="sxs-lookup"><span data-stu-id="6dd70-114">Turn on the following features:</span></span>

        - <span data-ttu-id="6dd70-115">Nieuw rasterbesturingselement</span><span class="sxs-lookup"><span data-stu-id="6dd70-115">New grid control</span></span>
        - <span data-ttu-id="6dd70-116">Groeperen in rasters (preview)</span><span class="sxs-lookup"><span data-stu-id="6dd70-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="6dd70-117">Betalingsvoorspellingen voor klanten (preview)</span><span class="sxs-lookup"><span data-stu-id="6dd70-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="6dd70-118">Cashflowprognoses (preview)</span><span class="sxs-lookup"><span data-stu-id="6dd70-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="6dd70-119">Ga naar **Contanten en bankbeheer \> Instelling van cashflowprognoses** en voeg de liquiditeitsrekeningen toe die in de prognoses moeten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="6dd70-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6dd70-120">Als er geen liquiditeitsrekeningen zijn ingesteld, kan de cashflow niet worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="6dd70-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="6dd70-121">Ga naar **Contanten en bankbeheer \> Instellen \> Financiële inzichten (preview) \> Cashflowprognoses (preview)** en volg deze stappen:</span><span class="sxs-lookup"><span data-stu-id="6dd70-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="6dd70-122">Selecteer op het tabblad **Cashflowprognose** de optie **Functie inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="6dd70-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="6dd70-123">Selecteer **Voorspellingsmodel maken**.</span><span class="sxs-lookup"><span data-stu-id="6dd70-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="6dd70-124">Zie [Cashflowprognose](cash-flow-forecast-intro.md) voor meer informatie over de mogelijkheden voor cashflowprognoses.</span><span class="sxs-lookup"><span data-stu-id="6dd70-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="6dd70-125">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="6dd70-125">Privacy notice</span></span>

<span data-ttu-id="6dd70-126">Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="6dd70-126">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]