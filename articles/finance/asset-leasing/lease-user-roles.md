---
title: Gebruikersrollen voor lease toewijzen
description: In dit onderwerp worden de beveiligingsrollen beschreven die worden gebruikt voor activa-leasing. Ook wordt uitgelegd hoe u gebruikers aan deze rollen toewijst.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: df23e219f5bd859b0072785dfd5f7a0ec63f540e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995388"
---
# <a name="assign-lease-user-roles"></a><span data-ttu-id="ae6b3-104">Gebruikersrollen voor lease toewijzen</span><span class="sxs-lookup"><span data-stu-id="ae6b3-104">Assign lease user roles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae6b3-105">In dit onderwerp worden de beveiligingsrollen beschreven die worden gebruikt voor activa-leasing.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-105">This topic describes the security roles that are used in Asset leasing.</span></span> <span data-ttu-id="ae6b3-106">Ook wordt uitgelegd hoe u gebruikers aan deze rollen toewijst.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-106">It also explains how to assign users to those roles.</span></span>

<span data-ttu-id="ae6b3-107">Drie gebruikersrollen geven verschillende toegang tot activa-leasing.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-107">Three user roles differentiate access in Asset leasing.</span></span> <span data-ttu-id="ae6b3-108">Eén rol is geschikt voor het onderhouden van leases, een is geschikt voor het weergeven van leases en een is geschikt voor het uitvoeren van de taken van een leasemedewerker.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-108">One role is appropriate for maintaining leases, one is appropriate for viewing leases, and one is appropriate for performing a lease clerk's duties.</span></span> <span data-ttu-id="ae6b3-109">Elke rol heeft specifieke machtigingen voor alle leasepagina's, en gebruikers kunnen met elk van deze rollen leases weergeven, maken, bewerken of verwijderen op basis van hun functie.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-109">Each role has specific permissions for all lease pages, and each lets users view, create, edit, or delete leases, according to their job duties.</span></span>

| <span data-ttu-id="ae6b3-110">Rol</span><span class="sxs-lookup"><span data-stu-id="ae6b3-110">Role</span></span>           | <span data-ttu-id="ae6b3-111">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ae6b3-111">Description</span></span> |
|----------------|-------------|
| <span data-ttu-id="ae6b3-112">Lease onderhouden</span><span class="sxs-lookup"><span data-stu-id="ae6b3-112">Maintain Lease</span></span> | <span data-ttu-id="ae6b3-113">Gebruikers met deze rol kunnen leases toevoegen, bewerken, verwijderen en weergeven.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-113">Users in this role can add, edit, delete, and view leases.</span></span> <span data-ttu-id="ae6b3-114">Deze rol is bedoeld voor dagelijkse gebruikers van wie de taken het maken en boeken van maandelijkse journaalposten en het toevoegen van nieuwe leases omvatten.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-114">This role is designed for daily users whose tasks include creating and posting monthly journal entries and adding new leases.</span></span> <span data-ttu-id="ae6b3-115">Deze rol geeft toegang tot alle functies voor activa-leasing.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-115">This role gives access to all Asset leasing functionality.</span></span> |
| <span data-ttu-id="ae6b3-116">Lease weergeven</span><span class="sxs-lookup"><span data-stu-id="ae6b3-116">View Lease</span></span>     | <span data-ttu-id="ae6b3-117">Gebruikers met deze rol kunnen alleen leaserecords, planningen en uitvoeringsrapporten weergeven.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-117">Users in this role can only view lease records, schedules, and run reports.</span></span> <span data-ttu-id="ae6b3-118">Ze kunnen geen nieuwe leases maken, bestaande leases bewerken of journaalposten voor leases maken.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-118">They can't create new leases, edit existing leases, or create journal entries against leases.</span></span> <span data-ttu-id="ae6b3-119">De rol is bedoeld voor gebruikers die alleen leases, lease-schema's en transacties voor deze leases hoeven te bekijken.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-119">The role is designed for users who just have to view leases, lease schedules, and the transactions that occur against those leases.</span></span> |
| <span data-ttu-id="ae6b3-120">Leasemedewerker</span><span class="sxs-lookup"><span data-stu-id="ae6b3-120">Lease Clerk</span></span>    | <span data-ttu-id="ae6b3-121">Gebruikers met deze rol kunnen alleen nieuwe leases maken.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-121">Users in this role can only create new leases.</span></span> <span data-ttu-id="ae6b3-122">Ze kunnen geen bestaande leases bewerken of verwijderen, lease-schema's weergeven of leasing-journaalposten boeken.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-122">They can't edit or delete existing leases, view lease schedules, or post leasing journal entries.</span></span> <span data-ttu-id="ae6b3-123">Deze rol is bedoeld voor gebruikers die gegevens invoeren.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-123">This role is designed for users who work in a data entry capacity.</span></span> |

<span data-ttu-id="ae6b3-124">Volg deze stappen om gebruikers toe te wijzen aan de rollen die worden gebruikt bij de leasing van activa.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-124">Follow these steps to assign users to the roles that are used in Asset leasing.</span></span>

1. <span data-ttu-id="ae6b3-125">Ga naar **Systeembeheer \> Beveiliging \> Gebruikers toewijzen aan rollen**.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-125">Go to **System administration \> Security \> Assign users to roles**.</span></span>
2. <span data-ttu-id="ae6b3-126">Selecteer de rol **Lease onderhouden**, **Leasemedewerker** of **Lease weergeven** en selecteer vervolgens **Gebruikers handmatig toewijzen / uitsluiten**.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-126">Select the **Maintain lease**, **Lease clerk**, or **View lease** role, and then select **Manually assign/exclude users**.</span></span>
3. <span data-ttu-id="ae6b3-127">Selecteer de gebruiker die u aan de rol wilt toewijzen en selecteer vervolgens **Toewijzen aan rol**.</span><span class="sxs-lookup"><span data-stu-id="ae6b3-127">Select the user to assign to the role, and then select **Assign to role**.</span></span>
