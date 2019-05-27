---
title: Projectverkooporders
description: In dit onderwerp wordt uitgelegd hoe u op projecten gebaseerde verkooporders voor tijd- en materiaalprojecten maakt.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 1d54c98a08dc7cccb5cafbbe401d0ce25a276c25
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1529897"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="d7cee-103">Projectverkooporders voor tijd- en materiaalprojecten</span><span class="sxs-lookup"><span data-stu-id="d7cee-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="d7cee-104">Dit onderwerp beschrijft hoe u een verkooporder voor een project maakt.</span><span class="sxs-lookup"><span data-stu-id="d7cee-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="d7cee-105">Verkooporders kunnen alleen worden gemaakt voor projecten van het type **Tijd en materiaal**.</span><span class="sxs-lookup"><span data-stu-id="d7cee-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="d7cee-106">Als een tijd- en materiaalproject meerdere financieringsbronnen heeft in het projectcontract, moet u de parameter **Verkooporders toestaan voor projecten met meerdere financieringsbronnen** op de pagina **Parameters voor Projectbeheer en boekhouding** inschakelen.</span><span class="sxs-lookup"><span data-stu-id="d7cee-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="d7cee-107">Ondersteuning voor projectverkooporders met meerdere financieringsbronnen is beschikbaar vanaf toepassingsversie 10.0.2 en hoger.</span><span class="sxs-lookup"><span data-stu-id="d7cee-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="d7cee-108">De parameter om de ondersteuning voor projectverkooporders met meerdere financieringsbronnen in te schakelen, wordt verwijderd in de releasewave van april 2020, waarna de functionaliteit altijd wordt ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="d7cee-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="d7cee-109">U kunt verkooporders op basis van een project op twee manieren maken:</span><span class="sxs-lookup"><span data-stu-id="d7cee-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="d7cee-110">Ga naar het project zelf.</span><span class="sxs-lookup"><span data-stu-id="d7cee-110">Go to the project itself.</span></span> <span data-ttu-id="d7cee-111">Selecteer in het actievenster **Beheren > Artikeltaken > Verkooporder**.</span><span class="sxs-lookup"><span data-stu-id="d7cee-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="d7cee-112">De projectgegevens worden standaard ingesteld op de verkooporder van het project.</span><span class="sxs-lookup"><span data-stu-id="d7cee-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="d7cee-113">Als het projectcontract meer dan één financieringsbron heeft, moet u de financieringsbron selecteren om de klant voor de verkooporder te selecteren.</span><span class="sxs-lookup"><span data-stu-id="d7cee-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="d7cee-114">Als er maar één financieringsbron voor het project is, wordt de klant automatisch ingesteld.</span><span class="sxs-lookup"><span data-stu-id="d7cee-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="d7cee-115">Ga naar de lijstpagina **Alle verkooporders** en maak een nieuwe verkooporder.</span><span class="sxs-lookup"><span data-stu-id="d7cee-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="d7cee-116">U moet het project selecteren voor de verkooporder.</span><span class="sxs-lookup"><span data-stu-id="d7cee-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="d7cee-117">Nadat het project is geselecteerd, wordt de klant via de financieringsbron ingesteld of moet u de financieringsbron selecteren als het projectcontract meerdere financieringsbronnen heeft.</span><span class="sxs-lookup"><span data-stu-id="d7cee-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

