---
title: Financiële-dimensiesets
description: In dit onderwerp worden financiële dimensiesets beschreven en vindt u enkele tips voor optimalisatie van het gebruik.
author: yukonpeegs
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ba11be028ebeea140df93e2a07dbb463402e3ef0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021823"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="f299d-103">Financiële-dimensiesets</span><span class="sxs-lookup"><span data-stu-id="f299d-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f299d-104">In dit onderwerp worden financiële dimensiesets beschreven en vindt u enkele tips voor optimalisatie van het gebruik.</span><span class="sxs-lookup"><span data-stu-id="f299d-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="f299d-105">Een dimensieset is een geordende lijst met financiële dimensies die kan worden gebruikt om grootboekgegevens op een door de gebruiker gedefinieerde manier samen te vatten.</span><span class="sxs-lookup"><span data-stu-id="f299d-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="f299d-106">De primaire toepassing van dimensiesets is het definiëren van een proefbalans.</span><span class="sxs-lookup"><span data-stu-id="f299d-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="f299d-107">De enige standaarddimensieset is de dimensieset die alleen de hoofdrekening bevat.</span><span class="sxs-lookup"><span data-stu-id="f299d-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="f299d-108">U gebruikt de pagina **Financiële dimensiesets** om financiële dimensiesets te maken en te beheren.</span><span class="sxs-lookup"><span data-stu-id="f299d-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="f299d-109">Saldi van dimensiesets</span><span class="sxs-lookup"><span data-stu-id="f299d-109">Dimension set balances</span></span>

<span data-ttu-id="f299d-110">Een dimensieset kan saldi hebben die zijn gebaseerd op de financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="f299d-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="f299d-111">De saldi bestaan in het grootboek en zijn gebaseerd op de dimensiesetdefinitie.</span><span class="sxs-lookup"><span data-stu-id="f299d-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="f299d-112">De saldi worden samengevat uit de grootboekgegevens om de prestaties te verbeteren wanneer deze worden opgehaald (bijvoorbeeld wanneer er een proefbalans wordt gegenereerd).</span><span class="sxs-lookup"><span data-stu-id="f299d-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="f299d-113">Saldi maken</span><span class="sxs-lookup"><span data-stu-id="f299d-113">Create balances</span></span>

<span data-ttu-id="f299d-114">Gebruik de knop **Saldi maken** om de saldi te initialiseren voor een dimensieset die momenteel geen saldi heeft.</span><span class="sxs-lookup"><span data-stu-id="f299d-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="f299d-115">Het is raadzaam om het aantal dimensiesets met saldi te beperken, omdat saldo-updates van invloed zijn op alle boekingsactiviteiten in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="f299d-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="f299d-116">Saldi bijwerken</span><span class="sxs-lookup"><span data-stu-id="f299d-116">Update balances</span></span>

<span data-ttu-id="f299d-117">Gebruik de knop **Saldi bijwerken** om de laatste boekingsactiviteit voor grootboek op te nemen in de saldi.</span><span class="sxs-lookup"><span data-stu-id="f299d-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="f299d-118">Saldo-updates zijn lichte bewerkingen.</span><span class="sxs-lookup"><span data-stu-id="f299d-118">Balance updates are light operations.</span></span> <span data-ttu-id="f299d-119">Ze worden verwerkt alleen voor de boekingsactiviteit in het grootboek van na de laatste update.</span><span class="sxs-lookup"><span data-stu-id="f299d-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="f299d-120">De weergave van de proefbalans dwingt een update af om ervoor te zorgen dat de weergegeven saldi actueel zijn.</span><span class="sxs-lookup"><span data-stu-id="f299d-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="f299d-121">U kunt een terugkerende batchtaak gebruiken, zodat de meest gebruikte dimensiesets snel kunnen worden bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="f299d-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="f299d-122">Op deze manier beperkt u de tijd dat gebruikers van de proefbalans moeten wachten.</span><span class="sxs-lookup"><span data-stu-id="f299d-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="f299d-123">Saldi opnieuw maken</span><span class="sxs-lookup"><span data-stu-id="f299d-123">Rebuild balances</span></span>

<span data-ttu-id="f299d-124">Gebruik de knop **Saldi opnieuw maken** om de saldi weer helemaal opnieuw te maken.</span><span class="sxs-lookup"><span data-stu-id="f299d-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="f299d-125">Op deze manier zorgt u ervoor dat ze overeenkomen met de gegevens in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="f299d-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="f299d-126">Voor het opnieuw samenstellen van de saldi is veel verwerkingskracht vereist en dat is meestal niet nodig.</span><span class="sxs-lookup"><span data-stu-id="f299d-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="f299d-127">Als u een scenario hebt waarin het saldo regelmatig opnieuw moet worden opgebouwd, kunt u het beste contact opnemen met de klantenondersteuning.</span><span class="sxs-lookup"><span data-stu-id="f299d-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="f299d-128">Klantenondersteuning kan u helpen om te bepalen waarom saldi niet overeenkomen met de gegevens in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="f299d-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="f299d-129">Saldi wissen</span><span class="sxs-lookup"><span data-stu-id="f299d-129">Clear balances</span></span>

<span data-ttu-id="f299d-130">Gebruik de knop **Saldi wissen** maken om de saldi te verwijderen en verdere updates te stoppen.</span><span class="sxs-lookup"><span data-stu-id="f299d-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="f299d-131">De dimensieset heeft dan geen invloed meer op boekingsactiviteiten in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="f299d-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="f299d-132">Zie voor meer informatie het onderwerp [Financiële dimensies](financial-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="f299d-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
