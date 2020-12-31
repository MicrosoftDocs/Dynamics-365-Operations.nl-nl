---
title: Beveiligingsdiagnose voor taakregistraties
description: Dit onderwerp bevat informatie over het analyseren en beheren van vereisten voor beveiligingsmachtigingen op basis van een taakregistratie.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 88eb90b35f1a9754cc4daa01d8f40cdf712db4f8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679785"
---
# <a name="security-diagnostics-for-task-recordings"></a><span data-ttu-id="e89c8-103">Beveiligingsdiagnose voor taakregistraties</span><span class="sxs-lookup"><span data-stu-id="e89c8-103">Security diagnostics for task recordings</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a><span data-ttu-id="e89c8-104">Voordat u begint</span><span class="sxs-lookup"><span data-stu-id="e89c8-104">Before you begin</span></span>

<span data-ttu-id="e89c8-105">Dit onderwerp bevat informatie over het analyseren en beheren van vereisten voor beveiligingsmachtigingen op basis van een taakregistratie.</span><span class="sxs-lookup"><span data-stu-id="e89c8-105">This topic provides information about how to analyze and manage security permission requirements based on a task recording.</span></span> <span data-ttu-id="e89c8-106">Voordat u de stappen in dit onderwerp uitvoert, moet u beschikken over een taakregistratie van het bedrijfsproces dat u wilt analyseren.</span><span class="sxs-lookup"><span data-stu-id="e89c8-106">Before you complete the steps in this topic, you must have a task recording of the business process that you want to analyze.</span></span> <span data-ttu-id="e89c8-107">Zie [Resources voor Taakrecorder](../../user-interface/task-recorder.md) om een bedrijfsproces vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="e89c8-107">To record a business process, see [Task recorder resources](../../user-interface/task-recorder.md).</span></span> 

## <a name="manage-security-for-a-task-recording"></a><span data-ttu-id="e89c8-108">Beveiliging voor een taakregistratie beheren</span><span class="sxs-lookup"><span data-stu-id="e89c8-108">Manage security for a task recording</span></span>

1. <span data-ttu-id="e89c8-109">Ga naar **Systeembeheer** > **Beveiliging** > **Beveiligingsdiagnose voor taakregistratie**.</span><span class="sxs-lookup"><span data-stu-id="e89c8-109">Go to **System administration** > **Security** > **Security diagnostic for task recording**.</span></span>
2. <span data-ttu-id="e89c8-110">Open de taakregistratie vanaf de locatie.</span><span class="sxs-lookup"><span data-stu-id="e89c8-110">Open the task recording from its location.</span></span> <span data-ttu-id="e89c8-111">Selecteer **Openen vanaf deze pc** of **Openen vanuit Lifecycle Services** en selecteer **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="e89c8-111">Select **Open from this PC** or **Open from Lifecycle Services**, and then select **Close**.</span></span>
3. <span data-ttu-id="e89c8-112">Hiermee opent u de pagina **Details van beveiligingsmenuopdrachten** met de beveiligingsobjecten die nodig zijn voor het proces.</span><span class="sxs-lookup"><span data-stu-id="e89c8-112">This will open the **Security menu item details** page that lists the security objects required for the process.</span></span>

 > [!NOTE]
 > <span data-ttu-id="e89c8-113">De menuopdrachten **Actie** en **Uitvoer** worden niet in de lijst opgenomen.</span><span class="sxs-lookup"><span data-stu-id="e89c8-113">The **Action** and **Output** menu items are not included in the list.</span></span>

4. <span data-ttu-id="e89c8-114">Selecteer een gebruiker in het veld **Gebruikers-id**.</span><span class="sxs-lookup"><span data-stu-id="e89c8-114">In the **User ID** field, select a user.</span></span> <span data-ttu-id="e89c8-115">Als de gebruiker geen machtigingen heeft voor sommige menuopdrachten, wordt het veld **Ontbrekende machtigingen** bijgewerkt naar **Ja**.</span><span class="sxs-lookup"><span data-stu-id="e89c8-115">If the user does not have permissions for some menu items, the **Missing permissions** field will update to **Yes**.</span></span>
  
  ![Pagina Details van beveiligingsmenuopdrachten](../media/Security-Menu-Item-Details.png)

5. <span data-ttu-id="e89c8-117">Selecteer **Verwijzing toevoegen** om een lijst weer te geven met de beveiligingsobjecten, waaronder rollen, functies en bevoegdheden waarmee de ontbrekende machtiging wordt verleend.</span><span class="sxs-lookup"><span data-stu-id="e89c8-117">Select **Add Reference** to see a list of the security objects, including roles, duties, and privileges that grant the missing permission.</span></span>
6. <span data-ttu-id="e89c8-118">Selecteer een beveiligingsobject in de lijst:</span><span class="sxs-lookup"><span data-stu-id="e89c8-118">Select a security object from the list:</span></span>

    - <span data-ttu-id="e89c8-119">Als **Rol** wordt geselecteerd, selecteert u **Rol toevoegen aan gebruiker**.</span><span class="sxs-lookup"><span data-stu-id="e89c8-119">If **Role** is selected, select **Add role to user**.</span></span> <span data-ttu-id="e89c8-120">Hierdoor wordt de pagina **Gebruikers aan rollen toewijzen** geopend.</span><span class="sxs-lookup"><span data-stu-id="e89c8-120">This will open the **Assign users to roles** page.</span></span> <span data-ttu-id="e89c8-121">Zie de pagina [Gebruikers aan beveiligingsrollen toewijzen](assign-users-security-roles.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="e89c8-121">For more information, see [Assign users to security roles](assign-users-security-roles.md) page.</span></span>
    - <span data-ttu-id="e89c8-122">Als **Functie** is geselecteerd, selecteert u **Functie toevoegen aan rol**, selecteert u de rollen waaraan de functie moet worden toegevoegd en selecteert u vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="e89c8-122">If **Duty** is selected, select **Add duty to role**, select the roles that the duty should be added to, and then select **OK**.</span></span>
    - <span data-ttu-id="e89c8-123">Als **Bevoegdheid** is geselecteerd, selecteert u **Bevoegdheid toevoegen aan functies**, selecteert u de rollen waaraan de functie moet worden toegevoegd en selecteert u vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="e89c8-123">If **Privilege** is selected, select **Add privilege to duties**, select the roles that the duty should be added to, and then select **OK**.</span></span>
