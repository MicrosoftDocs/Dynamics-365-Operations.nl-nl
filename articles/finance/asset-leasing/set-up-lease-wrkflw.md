---
title: Goedkeuringswerkstromen voor lease instellen
description: In het onderwerp wordt uitgelegd hoe u een goedkeuringswerkstroom instelt die wordt uitgevoerd wanneer er een nieuwe lease wordt gemaakt.
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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 58c0fd781710b7ab8efeaa7a6874f412279a5924
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442151"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="b6c07-103">Goedkeuringswerkstromen voor lease instellen</span><span class="sxs-lookup"><span data-stu-id="b6c07-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6c07-104">In het onderwerp wordt uitgelegd hoe u een goedkeuringswerkstroom instelt die wordt uitgevoerd wanneer er een nieuwe lease wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b6c07-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="b6c07-105">Zie [Goedkeuringswerkstromen voor lease gebruiken](use-create-lease-wrkflw.md) voor meer informatie over hoe u de werkstroom kunt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="b6c07-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="b6c07-106">Ga naar **Activa leasen \> Instellingen \> Leasewerkstroom**.</span><span class="sxs-lookup"><span data-stu-id="b6c07-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="b6c07-107">Selecteer **Nieuw** op de pagina **Leasewerkstroom**.</span><span class="sxs-lookup"><span data-stu-id="b6c07-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="b6c07-108">Selecteer in het dialoogvenster dat verschijnt, onder **Werkstroomtype**, de koppeling **Leasewerkstroom**.</span><span class="sxs-lookup"><span data-stu-id="b6c07-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="b6c07-109">De toepassing wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="b6c07-109">The application is opened.</span></span> <span data-ttu-id="b6c07-110">Nadat deze is uitgevoerd, kunt u zich aanmelden bij Azure Active Directory (Azure AD) en wordt u omgeleid naar de werkstroomtoepassing.</span><span class="sxs-lookup"><span data-stu-id="b6c07-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="b6c07-111">Sleep het element **Goedkeuring leasewerkstroom** naar de werkstroom.</span><span class="sxs-lookup"><span data-stu-id="b6c07-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="b6c07-112">Verbind één knooppunt van **Start** naar **Goedkeuring leasewerkstroom**.</span><span class="sxs-lookup"><span data-stu-id="b6c07-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="b6c07-113">Sluit **Goedkeuring leasewerkstroom** vervolgens aan op **Einde**.</span><span class="sxs-lookup"><span data-stu-id="b6c07-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="b6c07-114">Dubbelklik op **Goedkeuring leasewerkstroom**.</span><span class="sxs-lookup"><span data-stu-id="b6c07-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="b6c07-115">Selecteer **Eigenschappen** en voer vervolgens onder **Basisinstellingen** een naam voor de werkstroom in.</span><span class="sxs-lookup"><span data-stu-id="b6c07-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="b6c07-116">Op deze pagina kunt u ook meer parameters voor de werkstroom instellen.</span><span class="sxs-lookup"><span data-stu-id="b6c07-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="b6c07-117">Als u **Automatische acties** hebt ingeschakeld, neemt het systeem automatisch een specifieke actie.</span><span class="sxs-lookup"><span data-stu-id="b6c07-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="b6c07-118">Meldingen kunnen worden verzonden als deze zijn opgegeven op het tabblad **Meldingen**. Op het tabblad **Geavanceerde instellingen** kunt u een definitieve fiatteur opgeven, een tijdslimiet instellen en specifieke acties toewijzen die moeten worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="b6c07-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="b6c07-119">Wanneer u klaar bent met het instellen van de werkstroomparameters, selecteert u **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="b6c07-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="b6c07-120">Selecteer **Stap 1** en selecteer vervolgens **Eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="b6c07-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="b6c07-121">Voer onder **Basisinstellingen** een naam in voor de stap, maak een onderwerpregel voor de goedkeuring en geef instructies op voor de goedkeuring.</span><span class="sxs-lookup"><span data-stu-id="b6c07-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="b6c07-122">Selecteer op de pagina **Toewijzing** het toewijzingstype.</span><span class="sxs-lookup"><span data-stu-id="b6c07-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="b6c07-123">Selecteer **Gebruiker**, selecteer de gebruikers die leases goedkeuren en selecteer **Sluiten** om specifieke gebruikers aan de goedkeuring toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="b6c07-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="b6c07-124">Selecteer **Opslaan en sluiten** om de werkstroom te maken.</span><span class="sxs-lookup"><span data-stu-id="b6c07-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="b6c07-125">Selecteer **OK** wanneer u daarom wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="b6c07-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="b6c07-126">Selecteer op de pagina **Werkstroom maken**, de optie **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="b6c07-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="b6c07-127">Selecteer de nieuwe werkstroom en selecteer vervolgens **Versies**.</span><span class="sxs-lookup"><span data-stu-id="b6c07-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="b6c07-128">Selecteer vervolgens **Actief maken** om ervoor te zorgen dat de werkstroom actief is.</span><span class="sxs-lookup"><span data-stu-id="b6c07-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="b6c07-129">Selecteer **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="b6c07-129">Select **Close**.</span></span> <span data-ttu-id="b6c07-130">De nieuwe actieve versie wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b6c07-130">The new active version appears.</span></span>
