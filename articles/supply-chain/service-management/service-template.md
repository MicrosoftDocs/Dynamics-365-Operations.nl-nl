---
title: Servicesjablonen
description: "U kunt een serviceovereenkomst als sjabloon definiëren en de regels van de sjabloon later naar een andere serviceovereenkomst of serviceorder kopiëren."
author: YuyuScheller
manager: AnnBe
ms.date: 02/19/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 24b7ffd18e6f69f497597eb12657d09f8d600dcf
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="service-templates"></a><span data-ttu-id="6a2c4-103">Servicesjablonen</span><span class="sxs-lookup"><span data-stu-id="6a2c4-103">Service templates</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="6a2c4-104">U kunt een serviceovereenkomst als sjabloon definiëren en de regels van de sjabloon later naar een andere serviceovereenkomst of serviceorder kopiëren.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-104">You can define a service agreement as a template and copy the lines of the template later into another service agreement or into a service order.</span></span>

## <a name="example"></a><span data-ttu-id="6a2c4-105">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="6a2c4-105">Example</span></span>

<span data-ttu-id="6a2c4-106">Een klant voor wie u een service levert, heeft identieke dienstliften op vijf verschillende locaties.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-106">A customer for whom you provide service has identical service elevators at five different locations.</span></span>

<span data-ttu-id="6a2c4-107">U wilt vijf serviceovereenkomsten instellen voor de klant, één overeenkomst voor elke locatie.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-107">You want to set up five service agreements for the customer, one for each site.</span></span>
<span data-ttu-id="6a2c4-108">Als u de instellingen niet steeds wilt herhalen en ervoor wilt zorgen dat de instellingsgegevens in de serviceovereenkomsten gelijk zijn, kunt u een serviceovereenkomst maken en deze opgeven als sjabloon voor de servicewerkzaamheden aan de liften.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-108">To limit repetitive setup work, and to make sure that the setup information in the service agreements is identical, you create a service agreement and specify it as a template for the service work on the elevators.</span></span>

<span data-ttu-id="6a2c4-109">U kunt de sjabloonregels nu kopiëren naar de vijf nieuwe serviceovereenkomsten, zodat elke serviceovereenkomst wordt gevuld met de regels uit de sjabloon.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-109">You can now copy the template lines into the five new service agreements, so that each service agreement is populated with the lines from the template.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="6a2c4-110">Een sjabloon maken</span><span class="sxs-lookup"><span data-stu-id="6a2c4-110">Create a template</span></span>

<span data-ttu-id="6a2c4-111">Wanneer u een servicesjabloon maakt, maakt u een serviceovereenkomst en de vereiste regels hierin en koppelt u de serviceovereenkomst naar een servicesjabloongroep.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-111">When you create a service template, you create a service agreement, create the required lines on it, and attach the service agreement to a service-template group.</span></span>

> [!NOTE]
> <span data-ttu-id="6a2c4-112">U kunt een serviceovereenkomst alleen definiëren als sjabloon als hieraan geen serviceorders zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-112">A service agreement can be defined as a template only if it has no service orders attached to it.</span></span> <span data-ttu-id="6a2c4-113">Daarnaast kunnen er geen serviceorders worden gegenereerd van een serviceovereenkomst die is gedefinieerd als sjabloon.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-113">Also, no service orders can be generated from a service agreement that is defined as a template.</span></span>

## <a name="copy-template-lines"></a><span data-ttu-id="6a2c4-114">Sjabloonregels kopiëren</span><span class="sxs-lookup"><span data-stu-id="6a2c4-114">Copy template lines</span></span>

<span data-ttu-id="6a2c4-115">U kunt sjabloonregels uit een servicesjabloon kopiëren naar een andere serviceovereenkomst of naar een serviceorder.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-115">You can copy template lines from a service template into another service agreement or into a service order.</span></span>

<span data-ttu-id="6a2c4-116">Wanneer u sjabloonregels naar serviceorders of serviceovereenkomsten kopieert, worden de sjabloongroepen weergegeven in een structuurweergave waarin elke groep kan worden uitgevouwen.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-116">When you copy template lines into your service orders or service agreements, your template groups are displayed in a tree view in which each group can be expanded.</span></span> <span data-ttu-id="6a2c4-117">In deze weergave kunt u elke sjabloon en sjabloonregel bekijken.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-117">This display lets you view each template and template line.</span></span>

<span data-ttu-id="6a2c4-118">U kunt eenvoudiger bepalen welke servicesjabloonregels u wilt kopiëren als u de sjablonen hebt gegroepeerd onder namen die het gebruik van de sjablonen aanduiden.</span><span class="sxs-lookup"><span data-stu-id="6a2c4-118">It is easier to determine the service-template lines that you want to copy if you have grouped the templates under names that reflect the use of the templates.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a2c4-119">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="6a2c4-119">Related topics</span></span>

[<span data-ttu-id="6a2c4-120">Servicesjabloonregels kopiëren</span><span class="sxs-lookup"><span data-stu-id="6a2c4-120">Copy service templates lines</span></span>](copy-service-template-lines.md)

