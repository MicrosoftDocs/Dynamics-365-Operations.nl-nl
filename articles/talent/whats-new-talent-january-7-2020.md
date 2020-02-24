---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent (7 januari 2020)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-01-07
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e227c614fdbfe6f3dd410f1a533c593979abf1ec
ms.sourcegitcommit: 615ed3e4260192ba36826e128f1afa1588e94845
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/21/2020
ms.locfileid: "2974425"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-7-2020"></a><span data-ttu-id="81e44-103">Wat is nieuw of gewijzigd in Dynamics 365 Talent (7 januari 2020)</span><span class="sxs-lookup"><span data-stu-id="81e44-103">What's new or changed in Dynamics 365 Talent (January 7, 2020)</span></span>

<span data-ttu-id="81e44-104">In dit artikel worden de functies beschreven die in Dynamics 365 Talent nieuw of gewijzigd zijn.</span><span class="sxs-lookup"><span data-stu-id="81e44-104">This article describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="81e44-105">Wijzigingen in Attract</span><span class="sxs-lookup"><span data-stu-id="81e44-105">Changes in Attract</span></span>

<span data-ttu-id="81e44-106">Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="81e44-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="81e44-107">Wijzigingen in Onboard</span><span class="sxs-lookup"><span data-stu-id="81e44-107">Changes in Onboard</span></span>

<span data-ttu-id="81e44-108">Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="81e44-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="81e44-109">Wijzigingen in Core HR</span><span class="sxs-lookup"><span data-stu-id="81e44-109">Changes in Core HR</span></span>

<span data-ttu-id="81e44-110">Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2697.</span><span class="sxs-lookup"><span data-stu-id="81e44-110">Changes described in this section apply to build number 8.1.2697.</span></span> <span data-ttu-id="81e44-111">De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="81e44-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

 
### <a name="cant-delete-workers-that-dont-have-employment-records---386157"></a><span data-ttu-id="81e44-112">Kan werknemers zonder dienstverbandrecord niet verwijderen - (386157)</span><span class="sxs-lookup"><span data-stu-id="81e44-112">Can't delete workers that don't have employment records - (386157)</span></span>

<span data-ttu-id="81e44-113">Deze wijziging voegt een optie voor verwijderen toe aan het formulier **Medewerkers zonder dienstverband**.</span><span class="sxs-lookup"><span data-stu-id="81e44-113">This change adds a delete option in the **Workers without employment** form.</span></span> <span data-ttu-id="81e44-114">Medewerkers worden weergegeven in dit formulier wanneer er geen dienstverband voor de werknemer bestaat voor het verleden, het heden of de toekomst.</span><span class="sxs-lookup"><span data-stu-id="81e44-114">Workers appear in this form when no future, active, or historical employments exist for the worker.</span></span> <span data-ttu-id="81e44-115">In deze versie kunnen alleen systeembeheerders deze medewerkers verwijderen.</span><span class="sxs-lookup"><span data-stu-id="81e44-115">In this release, delete is only enabled for System Administrators.</span></span> <span data-ttu-id="81e44-116">In de versie van de volgende week wordt de beveiliging echter bijgewerkt, zodat alle gebruikers met de rol van HR-assistent medewerkers zonder dienstverband kunnen verwijderen.</span><span class="sxs-lookup"><span data-stu-id="81e44-116">However, in next week's release, security will be updated to allow all users with the HR assistant role to remove employees without employments.</span></span> <span data-ttu-id="81e44-117">U kunt deze wijzigingen ook handmatig doorvoeren met de volgende stappen.</span><span class="sxs-lookup"><span data-stu-id="81e44-117">You can also make these changes manually by following the following steps.</span></span>

1. <span data-ttu-id="81e44-118">Ga naar **Beveiligingsconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="81e44-118">Go to **Security configuration**.</span></span>
2. <span data-ttu-id="81e44-119">Filter op het tabblad **Bevoegdheden** de lijst **Bevoegdheden** op **Medewerkers onderhouden**.</span><span class="sxs-lookup"><span data-stu-id="81e44-119">In the **Privileges** tab, filter the **Privileges** list to **Maintain workers**.</span></span>
3. <span data-ttu-id="81e44-120">Selecteer in de kolom **Verwijzingen** de optie **Opdrachten in weergavemenu**.</span><span class="sxs-lookup"><span data-stu-id="81e44-120">In the **References** column, select **Display menu items**.</span></span>
4. <span data-ttu-id="81e44-121">Selecteer onder **Opdrachten in weergavemenu** de optie **HcmWOrkersWithoutEmployment**.</span><span class="sxs-lookup"><span data-stu-id="81e44-121">In **Display menu items**, select **HcmWOrkersWithoutEmployment**.</span></span>
5. <span data-ttu-id="81e44-122">Stel de machtiging **Verwijderen** in op Toewijzen.</span><span class="sxs-lookup"><span data-stu-id="81e44-122">Set the **Delete** permission to Grant.</span></span>
6. <span data-ttu-id="81e44-123">Selecteer het tabblad **Niet-gepubliceerde objecten**.</span><span class="sxs-lookup"><span data-stu-id="81e44-123">Select the **Unpublished objects** tab.</span></span>
7. <span data-ttu-id="81e44-124">Selecteer **Alles publiceren**.</span><span class="sxs-lookup"><span data-stu-id="81e44-124">Select **Publish all**.</span></span>
