--- 
title: Aanbieders van configuraties maken en deze als actief markeren
description: In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een configuratieprovider voor elektronische rapportage (ER) kan maken.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 37957f224cb57fd9f6c5014740bcea124a99a03a
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="658e1-103">Aanbieders van configuraties maken en deze als actief markeren</span><span class="sxs-lookup"><span data-stu-id="658e1-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="658e1-104">In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een configuratieprovider voor elektronische rapportage (ER) kan maken.</span><span class="sxs-lookup"><span data-stu-id="658e1-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="658e1-105">Elke ER-configuratie verwijst naar de provider als auteur van de configuratie.</span><span class="sxs-lookup"><span data-stu-id="658e1-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="658e1-106">In dit voorbeeld maakt u een configuratieprovider voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien providers van ER-configuraties tussen alle bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="658e1-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="658e1-107">Een provider maken</span><span class="sxs-lookup"><span data-stu-id="658e1-107">Create a provider</span></span>
1. <span data-ttu-id="658e1-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="658e1-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="658e1-109">Klik op Configuratieproviders.</span><span class="sxs-lookup"><span data-stu-id="658e1-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="658e1-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="658e1-110">Click New.</span></span>
    * <span data-ttu-id="658e1-111">Een providerrecord heeft een unieke naam en URL.</span><span class="sxs-lookup"><span data-stu-id="658e1-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="658e1-112">Bekijk de inhoud van deze pagina en sla deze procedure over als er al een record voor Litware, Inc (`http://www.litware.com`) bestaat.</span><span class="sxs-lookup"><span data-stu-id="658e1-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (`http://www.litware.com`) already exists.</span></span>  
4. <span data-ttu-id="658e1-113">Typ 'Litware, Inc.' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="658e1-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="658e1-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="658e1-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="658e1-115">Typ `http://www.litware.com` in het veld Internetadres.</span><span class="sxs-lookup"><span data-stu-id="658e1-115">In the Internet address field, type `http://www.litware.com`.</span></span>
6. <span data-ttu-id="658e1-116">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="658e1-116">Click Save.</span></span>
7. <span data-ttu-id="658e1-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="658e1-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="658e1-118">Selecteren als actieve provider</span><span class="sxs-lookup"><span data-stu-id="658e1-118">Select as an active provider</span></span>
1. <span data-ttu-id="658e1-119">Selecteer de provider Litware, Inc. .</span><span class="sxs-lookup"><span data-stu-id="658e1-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="658e1-120">Klik op Instellingen als actief.</span><span class="sxs-lookup"><span data-stu-id="658e1-120">Click Set active.</span></span>


