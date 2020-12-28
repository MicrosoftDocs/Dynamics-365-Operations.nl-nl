---
title: Attract-gebruikers kunnen niet solliciteren op banen in de vacatureportal
description: In dit onderwerp wordt uitgelegd hoe u een probleem kunt oplossen als Attract-gebruikers niet kunnen solliciteren op vacatures in de carrièreportal.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460771"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="a1445-103">Attract-gebruikers kunnen niet solliciteren op banen in de vacatureportal</span><span class="sxs-lookup"><span data-stu-id="a1445-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="a1445-104">Uitgeven</span><span class="sxs-lookup"><span data-stu-id="a1445-104">Issue</span></span>

<span data-ttu-id="a1445-105">Attract-gebruikers kunnen niet solliciteren op vacatures in de carrièreportal.</span><span class="sxs-lookup"><span data-stu-id="a1445-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="a1445-106">Wanneer ze solliciteren op een vacature die is gemaakt in Dynamics 365 Talent: Attract, wordt de pagina continu door de browser geladen en wordt de actie niet voltooid.</span><span class="sxs-lookup"><span data-stu-id="a1445-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="a1445-107">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="a1445-107">Cause</span></span>

<span data-ttu-id="a1445-108">Dit probleem doet zich voor wanneer het Talent Relationship Team geen Talent-gebruikersrol heeft.</span><span class="sxs-lookup"><span data-stu-id="a1445-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="a1445-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="a1445-109">Resolution</span></span>

<span data-ttu-id="a1445-110">Wijs de Talent-gebruikersrol toe aan het Talent Relationship Team.</span><span class="sxs-lookup"><span data-stu-id="a1445-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="a1445-111">Meld u bij het [Power Platform beheercentrum](https://admin.powerplatform.microsoft.com) aan met een van de volgende beheerdersreferenties:</span><span class="sxs-lookup"><span data-stu-id="a1445-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="a1445-112">Dynamics 365 admin</span><span class="sxs-lookup"><span data-stu-id="a1445-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="a1445-113">Algemeen beheerder</span><span class="sxs-lookup"><span data-stu-id="a1445-113">Global admin</span></span>
   - <span data-ttu-id="a1445-114">Power Platform beheerder</span><span class="sxs-lookup"><span data-stu-id="a1445-114">Power Platform admin</span></span>

2. <span data-ttu-id="a1445-115">Selecteer in het navigatievenster de optie **Omgevingen** en selecteer vervolgens de omgeving waarin u de Talent-gebruikersrol wilt toewijzen aan het Talent Relationship Team.</span><span class="sxs-lookup"><span data-stu-id="a1445-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![Omgeving selecteren](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="a1445-117">Selecteer in het venster **Omgevingen** de **Omgeving-URL** en meld u aan bij de beheerdersportal van de omgeving (bijvoorbeeld https:<orgname>. crm.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="a1445-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="a1445-118">Selecteer **Instellingen**, selecteer **Systeem** en selecteer **Beveiliging**.</span><span class="sxs-lookup"><span data-stu-id="a1445-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![Navigeer naar Beveiliging](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="a1445-120">Selecteer **Teams**.</span><span class="sxs-lookup"><span data-stu-id="a1445-120">Select **Teams**.</span></span>

   ![Selecteer Teams](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="a1445-122">Zoek naar **Talent Relationship Team** in het zoekvak en selecteer vervolgens het team uit de zoekresultaten.</span><span class="sxs-lookup"><span data-stu-id="a1445-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="a1445-123">Selecteer **ROLLEN BEHEREN** op het lint.</span><span class="sxs-lookup"><span data-stu-id="a1445-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="a1445-124">Selecteer in het dialoogvenster **Teamrollen beheren** de optie **Talent-gebruiker** in de lijst met beschikbare rollen en selecteer vervolgens **Ok** om de rol toe te passen.</span><span class="sxs-lookup"><span data-stu-id="a1445-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![Rol Toepassen](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="a1445-126">Test de wijzigingen:</span><span class="sxs-lookup"><span data-stu-id="a1445-126">Test your changes:</span></span>

   1. <span data-ttu-id="a1445-127">Meld u aan bij de carrièreportal in een nieuw browservenster.</span><span class="sxs-lookup"><span data-stu-id="a1445-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="a1445-128">Solliciteer op de vacature in de carrièreportal.</span><span class="sxs-lookup"><span data-stu-id="a1445-128">Apply for the job from the career portal.</span></span> 