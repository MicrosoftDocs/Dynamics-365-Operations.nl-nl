---
title: IBAN-rekeningvalidatie (International Bank Account Number) account beheren
description: In dit onderwerp wordt uitgelegd hoe u IBAN-rekeningvalidatie (International Bank Account Number) kunt beheren.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: a4f9bc2a22aabc7b83eb15665f37849d505e1b6b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177189"
---
# <a name="manage-international-bank-account-number-iban-validation"></a><span data-ttu-id="54168-103">IBAN-validatie (International Bank Account Number) beheren</span><span class="sxs-lookup"><span data-stu-id="54168-103">Manage International Bank Account Number (IBAN) validation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54168-104">Met IBAN-validatie (International Bank Account Number) wordt meer validatie uitgevoerd wanneer u een IBAN aan een bankrekening toevoegt.</span><span class="sxs-lookup"><span data-stu-id="54168-104">International Bank Account Number (IBAN) validation increases the amount of validation that is done when you add an IBAN to a bank account.</span></span>

<span data-ttu-id="54168-105">Informatie over de structuur van het IBAN wordt opgeslagen in Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="54168-105">Information about the structure of the IBAN is stored in Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="54168-106">Deze informatie wordt automatisch geladen wanneer u voor het eerst het IBAN voor bankrekeningen gebruikt.</span><span class="sxs-lookup"><span data-stu-id="54168-106">That information is automatically loaded when you first use the IBAN on bank accounts.</span></span> <span data-ttu-id="54168-107">Het bevat de lengte van het IBAN, de beginposities van het bankrekeningnummer en het routenummer en de lengte van het bankrekeningnummer en het routenummer.</span><span class="sxs-lookup"><span data-stu-id="54168-107">It contains the length of the IBAN, the starting positions of the bank account number and the routing number, and the length of the bank account number and routing number.</span></span>

## <a name="set-up-iban-structures"></a><span data-ttu-id="54168-108">IBAN-structuren instellen</span><span class="sxs-lookup"><span data-stu-id="54168-108">Set up IBAN structures</span></span>

1. <span data-ttu-id="54168-109">Ga naar **Contanten en bankbeheer \> Instellen \> IBAN-structuren**.</span><span class="sxs-lookup"><span data-stu-id="54168-109">Go to **Cash and bank management \> Setup \> IBAN structures**.</span></span>
2. <span data-ttu-id="54168-110">U ziet dat de IBAN-structuren voor elk land of elke regio automatisch zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="54168-110">Notice that the IBAN structures for each country or region have been set up automatically.</span></span>
3. <span data-ttu-id="54168-111">Als u de structuren voor een bepaald land of bepaalde regio wilt aanpassen, kunt u ze bewerken.</span><span class="sxs-lookup"><span data-stu-id="54168-111">If you want to customize the structures for a specific country or region, you can edit them.</span></span>
4. <span data-ttu-id="54168-112">De structuurdefinities maken deel uit van elke nieuwe release.</span><span class="sxs-lookup"><span data-stu-id="54168-112">The structure definitions will be a part of each new release.</span></span> <span data-ttu-id="54168-113">U kunt het menu **Structuren opnieuw instellen** gebruiken om de nieuwste definities na elke update te laden.</span><span class="sxs-lookup"><span data-stu-id="54168-113">You can use the **Reset structures** menu to load the latest definitions after each update.</span></span>

## <a name="validate-the-iban-structure-in-a-bank-account"></a><span data-ttu-id="54168-114">De IBAN-structuur in een bankrekening valideren</span><span class="sxs-lookup"><span data-stu-id="54168-114">Validate the IBAN structure in a bank account</span></span>

1. <span data-ttu-id="54168-115">Ga naar **Contanten en bankbeheer \> Bankrekeningen \> Bankrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="54168-115">Go to **Cash and bank management \> Bank accounts \> Bank accounts**.</span></span>
2. <span data-ttu-id="54168-116">Maak een bankrekening.</span><span class="sxs-lookup"><span data-stu-id="54168-116">Create a bank account.</span></span>
3. <span data-ttu-id="54168-117">Voer op het sneltabblad **Aanvullende gegevens** een IBAN op.</span><span class="sxs-lookup"><span data-stu-id="54168-117">On the **Additional information** FastTab, enter an IBAN.</span></span>

    <span data-ttu-id="54168-118">Als de lengte van het IBAN niet overeenkomt met de lengte die is gedefinieerd voor elk land of regio, ontvangt u een waarschuwingsbericht.</span><span class="sxs-lookup"><span data-stu-id="54168-118">If the length of the IBAN doesn't match the length that is defined for each country or region, you will receive a warning message.</span></span> <span data-ttu-id="54168-119">U kunt niet verdergaan als de lengte van het IBAN niet overeenkomt met de lengte die is opgegeven in de IBAN-structuur.</span><span class="sxs-lookup"><span data-stu-id="54168-119">You can't continue if the length of the IBAN doesn't match the length specified in the IBAN structure.</span></span>

    <span data-ttu-id="54168-120">Met de validatie wordt ook geverifieerd of het bankrekeningnummer overeenkomt met het deel van het IBAN waarmee het bankrekeningnummer wordt vertegenwoordigd.</span><span class="sxs-lookup"><span data-stu-id="54168-120">The validation also verifies that the bank account number matches the part of the IBAN that represents the bank account number.</span></span> <span data-ttu-id="54168-121">Als het bankrekeningnummer niet overeenkomt, ontvangt u een waarschuwingsbericht.</span><span class="sxs-lookup"><span data-stu-id="54168-121">If the bank account number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="54168-122">Dit bericht is slechts een waarschuwing.</span><span class="sxs-lookup"><span data-stu-id="54168-122">This message is only a warning.</span></span> <span data-ttu-id="54168-123">U kunt toch verdergaan, ook als het bankrekeningnummer niet overeenkomt.</span><span class="sxs-lookup"><span data-stu-id="54168-123">You can continue even if the bank account number doesn't match.</span></span>

    <span data-ttu-id="54168-124">Met de validatie wordt ook geverifieerd of het bankrouteringsnummer overeenkomt met het deel van het IBAN waarmee het bankrouteringsnummer wordt vertegenwoordigd.</span><span class="sxs-lookup"><span data-stu-id="54168-124">The validation also verifies that the bank routing number matches the part of the IBAN that represents the bank routing number.</span></span> <span data-ttu-id="54168-125">Het routenummer bevat een banknummer en vaak een aanvullend filiaalnummer.</span><span class="sxs-lookup"><span data-stu-id="54168-125">The routing number includes a bank number and often an additional bank branch.</span></span> <span data-ttu-id="54168-126">Als het bankrouteringsnummer niet overeenkomt, ontvangt u een waarschuwingsbericht.</span><span class="sxs-lookup"><span data-stu-id="54168-126">If the bank routing number doesn't match, you will receive a warning message.</span></span> <span data-ttu-id="54168-127">Dit bericht is slechts een waarschuwing.</span><span class="sxs-lookup"><span data-stu-id="54168-127">This message is only a warning.</span></span> <span data-ttu-id="54168-128">U kunt toch verdergaan, ook als het bankrouteringsnummer niet overeenkomt.</span><span class="sxs-lookup"><span data-stu-id="54168-128">You can continue even if the bank routing number doesn't match.</span></span>
