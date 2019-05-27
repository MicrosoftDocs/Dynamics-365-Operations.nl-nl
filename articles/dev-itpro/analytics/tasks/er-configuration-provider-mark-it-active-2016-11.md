---
title: Aanbieders van configuraties maken en deze als actief markeren
description: In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een configuratieprovider voor elektronische rapportage (ER) kan maken.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13a27c2fec2a2b226e9ae8d5b8f9a61e8b79ceb0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1544904"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="d1f1a-103">Aanbieders van configuraties maken en deze als actief markeren</span><span class="sxs-lookup"><span data-stu-id="d1f1a-103">Create configuration providers and mark them as active</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d1f1a-104">In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een configuratieprovider voor elektronische rapportage (ER) kan maken.</span><span class="sxs-lookup"><span data-stu-id="d1f1a-104">The following steps explain how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="d1f1a-105">Elke ER-configuratie verwijst naar de provider als auteur van de configuratie.</span><span class="sxs-lookup"><span data-stu-id="d1f1a-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="d1f1a-106">In dit voorbeeld maakt u een configuratieprovider voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien providers van ER-configuraties tussen alle bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="d1f1a-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>


## <a name="create-a-provider"></a><span data-ttu-id="d1f1a-107">Een provider maken</span><span class="sxs-lookup"><span data-stu-id="d1f1a-107">Create a provider</span></span>
1. <span data-ttu-id="d1f1a-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="d1f1a-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="d1f1a-109">Klik op Configuratieproviders.</span><span class="sxs-lookup"><span data-stu-id="d1f1a-109">Click Configuration providers.</span></span>
3. <span data-ttu-id="d1f1a-110">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="d1f1a-110">Click New.</span></span>
    * <span data-ttu-id="d1f1a-111">Een providerrecord heeft een unieke naam en URL.</span><span class="sxs-lookup"><span data-stu-id="d1f1a-111">A provider record has a unique name and URL.</span></span> <span data-ttu-id="d1f1a-112">Bekijk de inhoud van deze pagina en sla deze procedure over als er al een record voor Litware, Inc (http://www.litware.com) bestaat.</span><span class="sxs-lookup"><span data-stu-id="d1f1a-112">Review the content of this page and skip this procedure if a record for Litware, Inc. (http://www.litware.com) already exists.</span></span>  
4. <span data-ttu-id="d1f1a-113">Typ 'Litware, Inc.' in het veld Naam.</span><span class="sxs-lookup"><span data-stu-id="d1f1a-113">In the Name field, type 'Litware, Inc.'.</span></span>
    * <span data-ttu-id="d1f1a-114">Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="d1f1a-114">Litware, Inc.</span></span>  
5. <span data-ttu-id="d1f1a-115">Typ 'http://www.litware.com' in het veld Internetadres.</span><span class="sxs-lookup"><span data-stu-id="d1f1a-115">In the Internet address field, type 'http://www.litware.com'.</span></span>
    * http://www.litware.com  
6. <span data-ttu-id="d1f1a-116">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="d1f1a-116">Click Save.</span></span>
7. <span data-ttu-id="d1f1a-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="d1f1a-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="d1f1a-118">Selecteren als actieve provider</span><span class="sxs-lookup"><span data-stu-id="d1f1a-118">Select as an active provider</span></span>
1. <span data-ttu-id="d1f1a-119">Selecteer de provider Litware, Inc. .</span><span class="sxs-lookup"><span data-stu-id="d1f1a-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="d1f1a-120">Klik op Instellingen als actief.</span><span class="sxs-lookup"><span data-stu-id="d1f1a-120">Click Set active.</span></span>

