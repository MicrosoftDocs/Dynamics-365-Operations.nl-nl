---
title: IBAN-rekeningvalidatie (International Bank Account Number) account beheren
description: In dit onderwerp wordt uitgelegd hoe u IBAN-rekeningvalidatie (International Bank Account Number) kunt beheren.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e091aab70a98e0f4b96c41c1ee48926947539105
ms.contentlocale: nl-nl
ms.lasthandoff: 08/31/2018

---

# <a name="manage-international-bank-account-number-iban-account-validation"></a><span data-ttu-id="d76c5-103">IBAN-rekeningvalidatie (International Bank Account Number) account beheren</span><span class="sxs-lookup"><span data-stu-id="d76c5-103">Manage International Bank Account Number (IBAN) account validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d76c5-104">Met IBAN-rekeningvalidatie (International Bank Account Number) wordt meer validatie uitgevoerd wanneer u een IBAN aan een bankrekening toevoegt.</span><span class="sxs-lookup"><span data-stu-id="d76c5-104">International Bank Account Number (IBAN) account validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="d76c5-105">De structuur van het IBAN is opgeslagen in Microsoft Dynamics 365 for Finance and Operation en wordt automatisch geladen wanneer u het IBAN voor het eerst voor bankrekeningen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d76c5-105">The structure of the IBAN is stored in Microsoft Dynamics 365 for Finance and Operation, and is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="d76c5-106">Het bankrekeningnummer is onderdeel van de structuur die is gedefinieerd voor een IBAN-nummer.</span><span class="sxs-lookup"><span data-stu-id="d76c5-106">The bank account number is part of the structure defined for an IBAN number.</span></span> <span data-ttu-id="d76c5-107">Op basis van die structuur ontvangt u waarschuwingsberichten als de positie en de lengte van het rekeningnummer in het IBAN niet overeenkomen met de positie die is gedefinieerd in de structuur voor elk land of regio.</span><span class="sxs-lookup"><span data-stu-id="d76c5-107">Based on that structure, if the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you will receive warning messages.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="d76c5-108">IBAN-structuren instellen</span><span class="sxs-lookup"><span data-stu-id="d76c5-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="d76c5-109">Ga naar **Contanten en bankbeheer \> Instellen \> IBAN-structuren**.</span><span class="sxs-lookup"><span data-stu-id="d76c5-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="d76c5-110">U ziet dat de IBAN-structuren voor elk land of elke regio automatisch zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="d76c5-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="d76c5-111">Als u de structuren voor een bepaald land of bepaalde regio moet aanpassen moet, kunt u ze bewerken.</span><span class="sxs-lookup"><span data-stu-id="d76c5-111">If you must customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="d76c5-112">De structuurdefinities maken deel uit van elke nieuwe release.</span><span class="sxs-lookup"><span data-stu-id="d76c5-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="d76c5-113">U kunt het menu **Structuren opnieuw instellen** gebruiken om de nieuwste definities na elke update te laden.</span><span class="sxs-lookup"><span data-stu-id="d76c5-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="d76c5-114">De IBAN-structuur in een bankrekening valideren</span><span class="sxs-lookup"><span data-stu-id="d76c5-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="d76c5-115">Ga naar **Contanten en bankbeheer \> Bankrekeningen \> Bankrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="d76c5-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="d76c5-116">Maak een bankrekening.</span><span class="sxs-lookup"><span data-stu-id="d76c5-116">Create a bank account.</span></span>
3. <span data-ttu-id="d76c5-117">Voer op het sneltabblad **Aanvullende gegevens** een IBAN op.</span><span class="sxs-lookup"><span data-stu-id="d76c5-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="d76c5-118">Als de positie en de lengte van het rekeningnummer in het IBAN niet overeenkomen met de positie die is gedefinieerd in de structuur voor elk land of elke regio, ontvangt u een bericht.</span><span class="sxs-lookup"><span data-stu-id="d76c5-118">If the position and length of the account number in the IBAN don't match the position that is defined in the structure for each country or region, you receive a message.</span></span> <span data-ttu-id="d76c5-119">U kunt niet verdergaan als de lengte van het IBAN niet overeenkomt met de lengte in de IBAN-structuur.</span><span class="sxs-lookup"><span data-stu-id="d76c5-119">You can't continue if the length of the IBAN doesn't match the length in the IBAN structure.</span></span>

    <span data-ttu-id="d76c5-120">Met de validatie wordt ook geverifieerd of het bankrekeningnummer overeenkomt met het deel van het IBAN waarmee het bankrekeningnummer wordt vertegenwoordigd.</span><span class="sxs-lookup"><span data-stu-id="d76c5-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="d76c5-121">Als het bankrekeningnummer niet overeenkomt, ontvangt u een waarschuwingsbericht.</span><span class="sxs-lookup"><span data-stu-id="d76c5-121">If the bank account number doesn't match, you receive a warning message.</span></span> <span data-ttu-id="d76c5-122">Dit bericht is slechts een waarschuwing.</span><span class="sxs-lookup"><span data-stu-id="d76c5-122">This message is only a warning.</span></span> <span data-ttu-id="d76c5-123">U kunt toch verdergaan, ook als het bankrekeningnummer niet overeenkomt.</span><span class="sxs-lookup"><span data-stu-id="d76c5-123">You can continue even if the bank account number doesn't match.</span></span>

