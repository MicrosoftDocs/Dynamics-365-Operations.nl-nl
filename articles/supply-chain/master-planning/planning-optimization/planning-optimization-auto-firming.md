---
title: Automatisch fiatteren met Planningsoptimalisatie
description: In dit onderwerp wordt uitgelegd hoe u automatische fiattering gebruikt met Planningsoptimalisatie.
author: ChristianRytt
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 90319222e7357d7c54243faa8c64575377348467
ms.sourcegitcommit: 0138b6c108a10f2bcb90c91205da8092917160d8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2783148"
---
# <a name="auto-firming-with-planning-optimization"></a><span data-ttu-id="6d816-103">Automatisch fiatteren met Planningsoptimalisatie</span><span class="sxs-lookup"><span data-stu-id="6d816-103">Auto-firming with Planning Optimization</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6d816-104">Met automatische fiattering kunt u geplande orders fiatteren (vrijgeven) als onderdeel van het hoofdplanningsproces.</span><span class="sxs-lookup"><span data-stu-id="6d816-104">Automatic firming lets you firm (that is, release) planned orders as part of the master planning process.</span></span> <span data-ttu-id="6d816-105">Wanneer geplande orders worden gefiatteerd, worden deze omgezet in werkelijke inkooporders, transferorders of productie orders.</span><span class="sxs-lookup"><span data-stu-id="6d816-105">When planned orders are firmed, they are transformed into actual purchase orders, transfer orders, or production orders.</span></span> <span data-ttu-id="6d816-106">Wanneer Planningsoptimalisatie wordt gebruikt, worden geplande orders gefiatteerd tijdens de uitvoering van een hoofdplanning wanneer de orderdatum (dat wil zeggen de begindatum) binnen de time fence voor fiattering valt.</span><span class="sxs-lookup"><span data-stu-id="6d816-106">When Planning Optimization is used, planned orders are firmed during a master planning run when the order date (that is, the start date) is within the time fence for firming.</span></span>

> [!NOTE]
> <span data-ttu-id="6d816-107">Een geplande inkooporder kan alleen automatisch automatisch worden gefiatteerd als het artikel is gekoppeld aan een leverancier.</span><span class="sxs-lookup"><span data-stu-id="6d816-107">Auto-firming of a planned purchase order can occur only if the item is associated with a vendor.</span></span>

## <a name="turn-on-auto-firming"></a><span data-ttu-id="6d816-108">Automatische fiattering inschakelen</span><span class="sxs-lookup"><span data-stu-id="6d816-108">Turn on auto-firming</span></span>

<span data-ttu-id="6d816-109">Voer de volgende stappen uit om automatische fiattering in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="6d816-109">To turn on auto-firming, follow these steps.</span></span>

1. <span data-ttu-id="6d816-110">Selecteer **Automatisch fiatteren voor Planningsoptimalisatie** in de lijst op het tabblad **Nieuw** van het werkgebied **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="6d816-110">In the **Feature management** workspace, on the **New** tab, select **Auto-firming for Planning Optimization** in the list.</span></span> <span data-ttu-id="6d816-111">Als de functie niet wordt weergegeven op het tabblad **Nieuw**, kijkt u op de tabbladen **Niet ingeschakeld** en **Alle**.</span><span class="sxs-lookup"><span data-stu-id="6d816-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="6d816-112">Selecteer **Nu inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="6d816-112">Select **Enable now**.</span></span> <span data-ttu-id="6d816-113">U kunt ook **Planning** selecteren en vervolgens het tijdstip selecteren waarop u de functie wilt inschakelen.</span><span class="sxs-lookup"><span data-stu-id="6d816-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

## <a name="set-up-the-firming-time-fence"></a><span data-ttu-id="6d816-114">De time fence voor fiatteren instellen</span><span class="sxs-lookup"><span data-stu-id="6d816-114">Set up the firming time fence</span></span>

<span data-ttu-id="6d816-115">De time fence voor fiattering wordt vooruit vanaf de datum van hoofdplanningsuitvoering berekend.</span><span class="sxs-lookup"><span data-stu-id="6d816-115">The firming time fence is calculated forward from the master planning run date.</span></span> <span data-ttu-id="6d816-116">Deze wordt gedefinieerd op basis van het aantal dagen dat u invoert.</span><span class="sxs-lookup"><span data-stu-id="6d816-116">It's defined by the number of days that you enter.</span></span> <span data-ttu-id="6d816-117">U kunt de time fence voor fiatteren op de volgende manieren beheren:</span><span class="sxs-lookup"><span data-stu-id="6d816-117">You can control the firming time fence in the following ways:</span></span>

- <span data-ttu-id="6d816-118">Als u de standaard time fence voor fiattering voor een behoefteplanningsgroep wilt definiëren, gaat u naar **Hoofdplanning** \> **Instellingen** \> **Behoefteplanning** \> **Behoefteplanningsgroepen** en selecteert u een behoefteplanningsgroep.</span><span class="sxs-lookup"><span data-stu-id="6d816-118">To define the default firming time fence for a coverage group, go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**, and select a coverage group.</span></span> <span data-ttu-id="6d816-119">Voer vervolgens op het sneltabblad **Overige** in het veld **Time fence automatische fiattering (dagen)** het aantal dagen in.</span><span class="sxs-lookup"><span data-stu-id="6d816-119">Then, on the **Other** FastTab, in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="6d816-120">Als u de gedefinieerde time fence voor de behoefteplanningsgroep voor een specifiek artikel wilt overschrijven, gaat u naar **Productgegevensbeheer** \> **Vrijgegeven producten** en selecteert u vervolgens in het actievenster **Planning** en **Artikelbehoefteplanning**.</span><span class="sxs-lookup"><span data-stu-id="6d816-120">To overwrite the firming time fence that is defined for the coverage group for a specific item, go to **Product information management** \> **Released products**, then from the action pane select **Plan** and then select **Item coverage**.</span></span> <span data-ttu-id="6d816-121">Selecteer vervolgens op het tabblad **Algemeen** de optie **Time fence overschrijven** en voer in het **Time fence automatische fiattering (dagen)** het aantal dagen in.</span><span class="sxs-lookup"><span data-stu-id="6d816-121">Then, on the **General** tab, select **Override time fence** and in the **Automatic firming time fence (days)** field, enter the number of days.</span></span>
- <span data-ttu-id="6d816-122">Als u de gedefinieerde time fence voor fiattering voor de behoefteplanningsgroep en artikelbehoefteplanning voor een specifiek hoofdplan wilt overschrijven, gaat u naar **Hoofdplanning** \> **Instellingen** \> **Hoofdplannen** en selecteert u een hoofdplan.</span><span class="sxs-lookup"><span data-stu-id="6d816-122">To overwrite the firming time fence that is defined for the coverage group and item coverage for a specific master plan, go to **Master planning** \> **Setup** \> **Master plans**, and select a Master plan.</span></span> <span data-ttu-id="6d816-123">Stel vervolgens op het sneltabblad **Time fence in dagen** de optie **Vergrendeling** in op **Ja** om het aantal dagen in te voeren.</span><span class="sxs-lookup"><span data-stu-id="6d816-123">Then, on the **Time fence in days** FastTab, set **Freeze** to **Yes**, and enter the number of days.</span></span>

<span data-ttu-id="6d816-124">Als automatische fiattering is ingeschakeld voor een uitvoering van de hoofdplanning waarbij wordt gebruikgemaakt van Planningsoptimalisatie, wordt het proces voor automatische fiattering uitgevoerd volgens de instellingen voor automatische fiattering.</span><span class="sxs-lookup"><span data-stu-id="6d816-124">If auto-firming is turned on for a master planning run that uses Planning Optimization, the auto-firming process is done according to the auto-firming setup.</span></span> <span data-ttu-id="6d816-125">Als automatische fiattering niet is ingeschakeld of als planning wordt gestart vanaf de pagina **Nettobehoeften**, wordt het proces voor automatisch fiatteren overgeslagen.</span><span class="sxs-lookup"><span data-stu-id="6d816-125">If auto-firming isn't turned on, or if planning is started from the **Net requirements** page, the auto-firming process is skipped.</span></span>

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a><span data-ttu-id="6d816-126">Planningsoptimalisatie vs. de ingebouwde planningsengine voor Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6d816-126">Planning Optimization vs. the built-in Supply Chain Management planning engine</span></span>

<span data-ttu-id="6d816-127">Zowel Planningsoptimalisatie als de planningsengine die is ingebouwd in Microsoft Dynamics 365 Supply Chain Management kan worden gebruikt voor het automatisch fiatteren van geplande orders.</span><span class="sxs-lookup"><span data-stu-id="6d816-127">Both Planning Optimization and the planning engine that is built into Microsoft Dynamics 365 Supply Chain Management can be used to auto-firm planned orders.</span></span> <span data-ttu-id="6d816-128">Er zijn echter enkele belangrijke verschillen.</span><span class="sxs-lookup"><span data-stu-id="6d816-128">However, there are some important differences.</span></span> <span data-ttu-id="6d816-129">Terwijl Planningsoptimalisatie bijvoorbeeld de orderdatum (de begindatum) gebruikt om te bepalen welke geplande orders moeten worden gefiatteerd, gebruikt de ingebouwde planningsengine voor Supply Chain Management de behoeftedatum (dat wil zeggen de einddatum).</span><span class="sxs-lookup"><span data-stu-id="6d816-129">For example, whereas Planning Optimization uses the order date (that is, the start date) to determine which planned orders to firm, the built-in Supply Chain Management planning engine uses the requirement date (that is, the end date).</span></span> <span data-ttu-id="6d816-130">Hier volgt een overzicht van de verschillen.</span><span class="sxs-lookup"><span data-stu-id="6d816-130">Here is a summary of the differences.</span></span>

<span data-ttu-id="6d816-131">**Planningsoptimalisatie**</span><span class="sxs-lookup"><span data-stu-id="6d816-131">**Planning Optimization**</span></span>

- <span data-ttu-id="6d816-132">Automatische fiattering is gebaseerd op de orderdatum (begindatum).</span><span class="sxs-lookup"><span data-stu-id="6d816-132">Auto-firming is based on the order date (start date).</span></span>
- <span data-ttu-id="6d816-133">Omdat de orderdatum (begindatum) de fiattering activeert, hoeft u geen rekening te houden met de doorlooptijd als onderdeel van de time fence voor fiattering.</span><span class="sxs-lookup"><span data-stu-id="6d816-133">Because the order date (start date) triggers the firming, you don't have to consider the lead time as part of the firming time fence.</span></span>
- <span data-ttu-id="6d816-134">Als u alle orders wilt fiatteren die in de huidige week moeten beginnen, moet de time fence voor fiattering één week zijn.</span><span class="sxs-lookup"><span data-stu-id="6d816-134">If you want to firm all orders that must start during the current week, the firming time fence must be one week.</span></span>

<span data-ttu-id="6d816-135">**Ingebouwde planningsengine voor Supply Chain Management**</span><span class="sxs-lookup"><span data-stu-id="6d816-135">**Built-in Supply Chain Management planning engine**</span></span>

- <span data-ttu-id="6d816-136">Automatische fiattering is gebaseerd op de behoeftedatum (einddatum).</span><span class="sxs-lookup"><span data-stu-id="6d816-136">Auto-firming is based on the requirement date (end date).</span></span>
- <span data-ttu-id="6d816-137">Om te garanderen dat orders tijdig worden gefiatteerd, moet de time fence voor fiattering langer zijn dan de levertijd.</span><span class="sxs-lookup"><span data-stu-id="6d816-137">To help guarantee that orders are firmed in due time, the firming time fence must be longer than the lead time.</span></span>
- <span data-ttu-id="6d816-138">Als u alle orders wilt fiatteren die in de huidige week moeten beginnen, moet de time fence voor fiattering de levertijd plus één week zijn.</span><span class="sxs-lookup"><span data-stu-id="6d816-138">If you want to firm all orders that must start during the current week, the firming time fence must be the lead time plus one week.</span></span>