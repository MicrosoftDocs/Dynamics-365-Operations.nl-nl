---
title: Regulatory Configuration Service (RCS) - een RCS-omgeving verwijderen
description: In dit onderwerp wordt uitgelegd hoe een beheerder van de RCS (Regulatory Configuration Service) een RCS-omgeving en bijbehorende gegevens kan verwijderen.
author: JaneA07
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Global
audience: Application User, System Admin
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.15
ms.openlocfilehash: 637962cf63bfd8c2330726f33545f939ec91d58d
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295813"
---
# <a name="regulatory-configuration-service-rcs---delete-an-rcs-environment"></a><span data-ttu-id="d3276-103">Regulatory Configuration Service (RCS) - een RCS-omgeving verwijderen</span><span class="sxs-lookup"><span data-stu-id="d3276-103">Regulatory Configuration Service (RCS) - Delete an RCS environment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3276-104">In dit onderwerp wordt uitgelegd hoe een beheerder van de RCS (Regulatory Configuration Service) een RCS-omgeving en bijbehorende gegevens kan verwijderen.</span><span class="sxs-lookup"><span data-stu-id="d3276-104">This topic explains how a Regulatory Configuration Service (RCS) system administrator can delete an RCS environment and related data.</span></span>

<span data-ttu-id="d3276-105">Voordat u de procedure in dit onderwerp kunt voltooien, moet aan de volgende vereisten zijn voldaan:</span><span class="sxs-lookup"><span data-stu-id="d3276-105">Before you can complete the procedure in this topic, the following prerequisites must be met:</span></span>

- <span data-ttu-id="d3276-106">De rol **Systeembeheerder** moet aan u zijn toegewezen voor de RCS-omgeving.</span><span class="sxs-lookup"><span data-stu-id="d3276-106">You must have the **System Admin** role assigned to you for the RCS environment.</span></span>
- <span data-ttu-id="d3276-107">Aan de rol **Systeembeheerder** moet de rol **RCSDeleteEnvironmentDuty** zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="d3276-107">The **System Admin** role must have the **RCSDeleteEnvironmentDuty** role assigned to it.</span></span>

## <a name="delete-an-rcs-environment"></a><span data-ttu-id="d3276-108">Een omgeving verwijderen</span><span class="sxs-lookup"><span data-stu-id="d3276-108">Delete an RCS environment</span></span>

1. <span data-ttu-id="d3276-109">Open RCS en selecteer de tegel **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="d3276-109">Open RCS, and select the **Electronic reporting** workspace tile.</span></span>
2. <span data-ttu-id="d3276-110">Selecteer **RCS-omgeving verwijderen** in de sectie **Verwante koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="d3276-110">In the **Related links** section, select **Delete RCS environment**.</span></span>

    ![De RCS-omgevingskoppeling in de sectie Verwante koppelingen verwijderen](media/01_RCS-Delete-Environ-Related-Link.PNG)

3. <span data-ttu-id="d3276-112">Controleer in het dialoogvenster dat verschijnt de berichten over het bereik van de verwijdering van de omgeving.</span><span class="sxs-lookup"><span data-stu-id="d3276-112">In the dialog box that appears, review the messages about the scope of environment deletion.</span></span>

    ![Berichten in het dialoogvenster RCS-omgeving verwijderen](media/01_RCS-Delete-Environ-Msg_noGUID.PNG)

    > [!IMPORTANT]
    > <span data-ttu-id="d3276-114">Verwijdering van een RCS-omgeving kan niet worden omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="d3276-114">Deletion of an RCS environment can't be reversed.</span></span>
    >
    > <span data-ttu-id="d3276-115">De bewerking verwijdert de geselecteerde RCS-omgeving en bijbehorende gegevens, waaronder functies en configuraties die zijn opgeslagen in de algemene opslagplaats.</span><span class="sxs-lookup"><span data-stu-id="d3276-115">The operation deletes the selected RCS environment and any related data, including features and configurations that are stored in the Global repository.</span></span> <span data-ttu-id="d3276-116">Functies en configuraties die worden gedeeld met andere organisaties worden niet meer gedeeld en worden verwijderd als deze geen afhankelijkheden hebben.</span><span class="sxs-lookup"><span data-stu-id="d3276-116">Features and configurations that are shared with other organizations will be unshared and deleted if they have no dependencies.</span></span> <span data-ttu-id="d3276-117">Functies en configuraties met afhankelijkheden worden gemarkeerd als gestopt.</span><span class="sxs-lookup"><span data-stu-id="d3276-117">Features and configurations that have dependencies will be marked as discontinued.</span></span>

4. <span data-ttu-id="d3276-118">Voer in het betreffende veld de Globally Unique Identifier (GUID) van de RCS-omgeving in om te bevestigen dat u deze wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="d3276-118">In the field that is provided, enter the globally unique identifier (GUID) of the RCS environment to confirm that you want to delete it.</span></span> <span data-ttu-id="d3276-119">De GUID van de omgeving is opgenomen in het verwijderingsbericht.</span><span class="sxs-lookup"><span data-stu-id="d3276-119">The environment's GUID is included in the deletion message.</span></span>
5. <span data-ttu-id="d3276-120">Selecteer **Omgeving verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="d3276-120">Select **Delete environment**.</span></span>
    
<span data-ttu-id="d3276-121">Uw RCS-omgeving en alle bijbehorende gegevens worden nu verwijderd.</span><span class="sxs-lookup"><span data-stu-id="d3276-121">Your RCS environment and any related data are now deleted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3276-122">Nadat u een RCS-omgeving hebt verwijderd, kunnen de gegevens niet meer worden hersteld.</span><span class="sxs-lookup"><span data-stu-id="d3276-122">After you delete an RCS environment, there is no way to recover the data.</span></span> <span data-ttu-id="d3276-123">Er kan een nieuwe RCS-omgeving worden gemaakt in elke beschikbare RCS-regio.</span><span class="sxs-lookup"><span data-stu-id="d3276-123">A new RCS environment can be created in any available RCS region.</span></span>
