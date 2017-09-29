--- 
title: Een configuratieprovider maken en deze als actief markeren voor elektronische aangifte (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een configuratieprovider voor elektronische rapportage (ER) kan maken.
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: bdb3a3857a7293828a7766b6988c123a43e0673c
ms.contentlocale: nl-nl
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-configuration-providand-mark-it-as-active-for-electronic-reporting-er"></a><span data-ttu-id="82d96-103">Een configuratieprovider maken en deze als actief markeren voor elektronische aangifte (ER)</span><span class="sxs-lookup"><span data-stu-id="82d96-103">Create a configuration providand mark it as active for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82d96-104">In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een configuratieprovider voor elektronische rapportage (ER) kan maken.</span><span class="sxs-lookup"><span data-stu-id="82d96-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="82d96-105">Elke ER-configuratie verwijst naar de provider als auteur van de configuratie.</span><span class="sxs-lookup"><span data-stu-id="82d96-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="82d96-106">In dit voorbeeld maakt u een configuratieprovider voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien providers van ER-configuraties tussen alle bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="82d96-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="82d96-107">Een provider maken</span><span class="sxs-lookup"><span data-stu-id="82d96-107">Create a provider</span></span>
1. <span data-ttu-id="82d96-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="82d96-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="82d96-109">Klik op Configuratieproviders.</span><span class="sxs-lookup"><span data-stu-id="82d96-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="82d96-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="82d96-110">Click New.</span></span>
    * <span data-ttu-id="82d96-111">Een providerrecord heeft een unieke naam en URL.</span><span class="sxs-lookup"><span data-stu-id="82d96-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="82d96-112">Bekijk de inhoud van deze pagina en sla deze procedure over als er al een record voor Litware, Inc. (http://www.litware.com) bestaat.</span><span class="sxs-lookup"><span data-stu-id="82d96-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="82d96-113">Typ 'Litware, Inc.' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="82d96-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="82d96-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="82d96-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="82d96-115">Typ 'http://www.litware.com' in het veld Internetadres.</span><span class="sxs-lookup"><span data-stu-id="82d96-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * <span data-ttu-id="82d96-116">http://www.litware.com</span><span class="sxs-lookup"><span data-stu-id="82d96-116">http://www.litware.com</span></span>  
6. <span data-ttu-id="82d96-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="82d96-117">Click Save.</span></span>
7. <span data-ttu-id="82d96-118">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="82d96-118">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="82d96-119">Selecteren als actieve provider</span><span class="sxs-lookup"><span data-stu-id="82d96-119">Select as an active provider</span></span>
1. <span data-ttu-id="82d96-120">Selecteer de provider Litware, Inc. .</span><span class="sxs-lookup"><span data-stu-id="82d96-120">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="82d96-121">Klik op Instellingen als actief.</span><span class="sxs-lookup"><span data-stu-id="82d96-121">Click Set active.</span></span>


