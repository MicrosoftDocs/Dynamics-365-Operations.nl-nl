---
title: Serviceniveaus van activa
description: In dit onderwerp worden serviceniveaus voor activa in Activabeheer uitgelegd.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb2730dad0a130dfd3916ae51e9be6d81f97c22b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238081"
---
# <a name="asset-service-levels"></a><span data-ttu-id="409cd-103">Serviceniveaus van activa</span><span class="sxs-lookup"><span data-stu-id="409cd-103">Asset service levels</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="409cd-104">In dit onderwerp worden serviceniveaus voor activa in Activabeheer uitgelegd.</span><span class="sxs-lookup"><span data-stu-id="409cd-104">This topic explains asset service levels in Asset Management.</span></span> <span data-ttu-id="409cd-105">Serviceniveaus van activa zijn gerelateerd aan activa en worden overgebracht naar onderhoudsaanvragen en werkorders.</span><span class="sxs-lookup"><span data-stu-id="409cd-105">Asset service levels are related to assets, and are transferred to maintenance requests and work orders.</span></span> <span data-ttu-id="409cd-106">Ze worden gebruikt om de prioriteit van werkorders te berekenen tijdens de planning van de werkorder.</span><span class="sxs-lookup"><span data-stu-id="409cd-106">They are used to calculate the priority of work orders during work order scheduling.</span></span> <span data-ttu-id="409cd-107">Serviceniveaus van activa kunnen worden gewijzigd als er wijzigingen nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="409cd-107">Asset service levels can be changed, if changes are required.</span></span>

<span data-ttu-id="409cd-108">Zie [Parameters voor activabeheer](../setup-for-objects/enterprise-asset-management-parameters.md) voor meer informatie over de instellingen die zijn gerelateerd aan de berekening van beoordelingsscores voor de planning van werkorders.</span><span class="sxs-lookup"><span data-stu-id="409cd-108">For more information about the setup that is related to the calculation of rating scores for work order scheduling, see [Asset Management parameters](../setup-for-objects/enterprise-asset-management-parameters.md).</span></span> <span data-ttu-id="409cd-109">U moet ten minste één standaardrecord instellen voor het serviceniveau van de activa.</span><span class="sxs-lookup"><span data-stu-id="409cd-109">You must set up at least one default record for the asset service level.</span></span> <span data-ttu-id="409cd-110">Deze standaardrecord wordt gebruikt als er geen andere overeenkomst wordt gevonden tijdens de planning van de werkorder.</span><span class="sxs-lookup"><span data-stu-id="409cd-110">This default record is used if no other match is found during work order scheduling.</span></span>

<span data-ttu-id="409cd-111">**Voorbeeld 1**: het standaard serviceniveau dat wordt gebruikt als er geen andere overeenkomst wordt gevonden.</span><span class="sxs-lookup"><span data-stu-id="409cd-111">**Example 1:** The default service level that is used if no other match is found.</span></span> <span data-ttu-id="409cd-112">In deze record selecteert u alleen een serviceniveau.</span><span class="sxs-lookup"><span data-stu-id="409cd-112">In this record, you select only a service level.</span></span>

<span data-ttu-id="409cd-113">**Voorbeeld 2**: een hoog serviceniveau dat wordt gebruikt om taken voor een Volvo-truckmotor te plannen.</span><span class="sxs-lookup"><span data-stu-id="409cd-113">**Example 2:** A high service level that is used to schedule jobs for a Volvo truck engine.</span></span> <span data-ttu-id="409cd-114">In deze record selecteert u een relevant activumtype (zoals **truckmotor**), een fabrikant (**Volvo**) en een serviceniveau.</span><span class="sxs-lookup"><span data-stu-id="409cd-114">In this record, you select a relevant asset type (such as **Truck Engine**), a manufacturer (**Volvo**), and a service level.</span></span>

## <a name="set-up-asset-service-levels"></a><span data-ttu-id="409cd-115">Serviceniveaus van activa instellen</span><span class="sxs-lookup"><span data-stu-id="409cd-115">Set up asset service levels</span></span>

1. <span data-ttu-id="409cd-116">Selecteer **Activabeheer** \> **Instellingen** \> **Serviceniveaus van activa**.</span><span class="sxs-lookup"><span data-stu-id="409cd-116">Select **Asset management** \> **Setup** \> **Asset service levels**.</span></span>
2. <span data-ttu-id="409cd-117">Selecteer **Nieuw** om een record te maken.</span><span class="sxs-lookup"><span data-stu-id="409cd-117">Select **New** to create a record.</span></span>
3. <span data-ttu-id="409cd-118">Afhankelijk van het detailniveau dat is vereist voor het activumserviceniveau, moet u relevante selecties maken in de velden **Functionele locatie**, **Type activum**, **Fabrikant**, **Model**, **Activum**, **Type werkorder** en **Serviceniveau**.</span><span class="sxs-lookup"><span data-stu-id="409cd-118">Depending on the detail level that is required for the asset service level, make relevant selections in the **Functional location**, **Asset type**, **Manufacturer**, **Model**, **Asset**, **Work order type**, and **Service level** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="409cd-119">Wanneer het serviceniveau voor activa wordt gebruikt voor onderhoudsaanvragen en werkorders, worden in Activabeheer alle activumserviceniveaurecords gecontroleerd op een mogelijke overeenkomst.</span><span class="sxs-lookup"><span data-stu-id="409cd-119">When the asset service level is used for maintenance requests and work orders, Asset Management goes through all asset service level records to check for a possible match.</span></span> <span data-ttu-id="409cd-120">De meest specifieke combinatie wordt altijd als eerste gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="409cd-120">It always checks the most specific combination first.</span></span> <span data-ttu-id="409cd-121">Dat wil zeggen dat Activabeheer eerst controleert op een overeenkomst voor het veld **Type werkorder**.</span><span class="sxs-lookup"><span data-stu-id="409cd-121">In other words, Asset Management first checks for a match for the **Work order type** field.</span></span> <span data-ttu-id="409cd-122">Als er geen overeenkomst wordt gevonden, wordt er gecontroleerd op een overeenkomst voor het veld **Activum** enzovoort.</span><span class="sxs-lookup"><span data-stu-id="409cd-122">If no match is found, it checks for a match for the **Asset** field, and so on.</span></span> <span data-ttu-id="409cd-123">Zoals u kunt zien in de indeling van de pagina **Serviceniveaus voor activa**, betekent dit gedrag dat Activabeheer elke record van rechts naar links controleert op overeenkomst om de meest specifieke combinatie te vinden.</span><span class="sxs-lookup"><span data-stu-id="409cd-123">As you can see in the layout of the **Asset service levels** page, this behavior means that, to find the most specific combination, Asset Management checks each record from right to left for a match.</span></span> <span data-ttu-id="409cd-124">Als er geen overeenkomst wordt gevonden, wordt in deze velden de standaardrecord zonder selecties gebruikt.</span><span class="sxs-lookup"><span data-stu-id="409cd-124">If no match is found, the default record that has no selections in those fields is used.</span></span>

4. <span data-ttu-id="409cd-125">Selecteer in het veld **Serviceniveau** een getal dat het serviceniveau (prioriteit) aangeeft.</span><span class="sxs-lookup"><span data-stu-id="409cd-125">In the **Service level** field, select a number that indicates the service level (priority).</span></span>


> [!NOTE]
> <span data-ttu-id="409cd-126">Als u een activumserviceniveaurecord op de pagina **Serviceniveaus van activa** wijzigt nadat u deze al op een werkorder hebt gebruikt, wordt het serviceniveau voor onderhoudsaanvragen en werkorders niet dienovereenkomstig bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="409cd-126">If you change an asset service level record on the **Asset service levels** page after you've already used it on a work order, the service level on maintenance requests and work orders isn't updated accordingly.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]