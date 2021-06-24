---
title: Cashflowprognose inschakelen (preview)
description: In dit onderwerp wordt uitgelegd hoe u de functie Cashflowprognoses kunt inschakelen in Financiële inzichten.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: ba8acb2191291e2abed5cabf234c19fe09e6c8ff
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222553"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="016b8-103">Cashflowprognose inschakelen (preview)</span><span class="sxs-lookup"><span data-stu-id="016b8-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="016b8-104">In dit onderwerp wordt uitgelegd hoe u de functie Cashflowprognoses kunt inschakelen in Financiële inzichten.</span><span class="sxs-lookup"><span data-stu-id="016b8-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="016b8-105">Als u betalingsvoorspellingen in de cashflow wilt gebruiken, moet u de functie Voorspellingen klantbetalingen instellen, zoals wordt beschreven in [Voorspellingen klantbetalingen inschakelen](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="016b8-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="016b8-106">Gebruik informatie op de omgevingspagina in Microsoft Dynamics Lifecycle Services (LCS) om verbinding te maken met het primaire exemplaar van Azure SQL voor die omgeving.</span><span class="sxs-lookup"><span data-stu-id="016b8-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="016b8-107">Voer de volgende Transact-SQL-opdracht (T-SQL) uit om flights in te schakelen voor de sandbox-omgeving.</span><span class="sxs-lookup"><span data-stu-id="016b8-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="016b8-108">(Mogelijk moet u de toegang voor uw IP-adres inschakelen in LCS voordat u extern verbinding kunt maken met Application Object Server \[AOS\].)</span><span class="sxs-lookup"><span data-stu-id="016b8-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="016b8-109">Sla deze stap over als u versie 10.0.20 of hoger gebruikt of als u een Service Fabric-implementatie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="016b8-109">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="016b8-110">Het Financiële inzichten-team zou de flight al voor u moeten hebben ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="016b8-110">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="016b8-111">Als de functie niet ziet in het werkgebied **Functiebeheer** of als u problemen ondervindt wanneer u deze wilt inschakelen, neemt u contact op met <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="016b8-111">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="016b8-112">Open het werkgebied **Functiebeheer** en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="016b8-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="016b8-113">Selecteer **Controleren op updates**.</span><span class="sxs-lookup"><span data-stu-id="016b8-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="016b8-114">De volgende functies inschakelen:</span><span class="sxs-lookup"><span data-stu-id="016b8-114">Turn on the following features:</span></span>

        - <span data-ttu-id="016b8-115">Nieuw rasterbesturingselement</span><span class="sxs-lookup"><span data-stu-id="016b8-115">New grid control</span></span>
        - <span data-ttu-id="016b8-116">Groeperen in rasters (preview)</span><span class="sxs-lookup"><span data-stu-id="016b8-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="016b8-117">Betalingsvoorspellingen voor klanten (preview)</span><span class="sxs-lookup"><span data-stu-id="016b8-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="016b8-118">Cashflowprognoses (preview)</span><span class="sxs-lookup"><span data-stu-id="016b8-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="016b8-119">Ga naar **Contanten en bankbeheer \> Instelling van cashflowprognoses** en voeg de liquiditeitsrekeningen toe die in de prognoses moeten worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="016b8-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="016b8-120">Als er geen liquiditeitsrekeningen zijn ingesteld, kan de cashflow niet worden gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="016b8-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="016b8-121">Ga naar **Contanten en bankbeheer \> Instellen \> Financiële inzichten (preview) \> Cashflowprognoses (preview)** en volg deze stappen:</span><span class="sxs-lookup"><span data-stu-id="016b8-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="016b8-122">Selecteer op het tabblad **Cashflowprognose** de optie **Functie inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="016b8-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="016b8-123">Selecteer **Voorspellingsmodel maken**.</span><span class="sxs-lookup"><span data-stu-id="016b8-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="016b8-124">Zie [Cashflowprognose](cash-flow-forecast-intro.md) voor meer informatie over de mogelijkheden voor cashflowprognoses.</span><span class="sxs-lookup"><span data-stu-id="016b8-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
