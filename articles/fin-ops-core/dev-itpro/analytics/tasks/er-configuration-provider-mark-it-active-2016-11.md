---
title: Aanbieders van configuraties maken en deze als actief markeren
description: In het volgende onderwerp wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een configuratieprovider voor elektronische rapportage (ER) kan maken.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2c092414f058a27cde963b1e8befd41ab3d1e3c
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2249199"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="54e27-103">Aanbieders van configuraties maken en deze als actief markeren</span><span class="sxs-lookup"><span data-stu-id="54e27-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="54e27-104">In het volgende onderwerp wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een configuratieprovider voor elektronische rapportage (ER) kan maken.</span><span class="sxs-lookup"><span data-stu-id="54e27-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="54e27-105">Elke ER-configuratie verwijst naar de provider als auteur van de configuratie.</span><span class="sxs-lookup"><span data-stu-id="54e27-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="54e27-106">In dit voorbeeld maakt u een configuratieprovider voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien providers van ER-configuraties tussen alle bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="54e27-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="54e27-107">Een provider maken</span><span class="sxs-lookup"><span data-stu-id="54e27-107">Create a provider</span></span>
1. <span data-ttu-id="54e27-108">Ga naar het **navigatiepaneel** in de linkerbovenhoek en selecteer **Organisatiebeheer.**</span><span class="sxs-lookup"><span data-stu-id="54e27-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="54e27-109">Ga naar **Werkgebieden > Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="54e27-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="54e27-110">Ga naar **Verwante koppelingen > Configuratieproviders**.</span><span class="sxs-lookup"><span data-stu-id="54e27-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="54e27-111">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="54e27-111">Select **New**.</span></span>
    - <span data-ttu-id="54e27-112">Een providerrecord heeft een unieke naam en URL.</span><span class="sxs-lookup"><span data-stu-id="54e27-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="54e27-113">Bekijk de inhoud van deze pagina en sla deze procedure over als er al een record voor Litware, Inc (https://www.litware.com) bestaat.</span><span class="sxs-lookup"><span data-stu-id="54e27-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="54e27-114">Typ `Litware, Inc.` in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="54e27-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="54e27-115">Typ `https://www.litware.com` in het veld Internetadres.</span><span class="sxs-lookup"><span data-stu-id="54e27-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="54e27-116">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="54e27-116">Select **Save**.</span></span>
8. <span data-ttu-id="54e27-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="54e27-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="54e27-118">Selecteren als actieve provider</span><span class="sxs-lookup"><span data-stu-id="54e27-118">Select as an active provider</span></span>
1. <span data-ttu-id="54e27-119">Selecteer de provider Litware, Inc. .</span><span class="sxs-lookup"><span data-stu-id="54e27-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="54e27-120">Selecteer **Instellingen als actief**.</span><span class="sxs-lookup"><span data-stu-id="54e27-120">Select **Set active**.</span></span>

![Pagina met het werkgebied Elektronische rapportage](../media/GER-Task-ActiveProvider-1.png)