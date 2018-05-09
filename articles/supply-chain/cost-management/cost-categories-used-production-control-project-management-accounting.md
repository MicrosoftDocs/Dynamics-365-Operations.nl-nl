---
title: "Kostencategorieën die worden gebruikt in Productiebeheer en in Projectbeheerboekhouding"
description: "Bepaalde typen productiewerk zijn mogelijk van toepassing op geraamde projecturen en rapportage. Dit artikel bevat informatie over de kostencategorieën die u voor deze soorten productiewerk voor productie- en projectdoeleinden moet definiëren."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjCategory
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 78253
ms.assetid: cfdd58a0-8afa-4a6f-a208-a76e2c162429
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1f4c03d886a7a6e98276422cd954954fe6e8a12e
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="cost-categories-used-in-production-control-and-project-management-accounting"></a><span data-ttu-id="f8b4e-104">Kostencategorieën die worden gebruikt in Productiebeheer en in Projectbeheerboekhouding</span><span class="sxs-lookup"><span data-stu-id="f8b4e-104">Cost categories used in Production control and Project management accounting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8b4e-105">Bepaalde typen productiewerk zijn mogelijk van toepassing op geraamde projecturen en rapportage.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-105">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="f8b4e-106">Dit artikel bevat informatie over de kostencategorieën die u voor deze soorten productiewerk voor productie- en projectdoeleinden moet definiëren.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-106">This article provides information about the cost categories that you must define for these types of production work for production and project purposes.</span></span>

<span data-ttu-id="f8b4e-107">Bepaalde typen productiewerk zijn mogelijk van toepassing op geraamde projecturen en rapportage.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-107">Some types of production work can apply to project time estimates and reporting.</span></span> <span data-ttu-id="f8b4e-108">In een dergelijk geval is een kostencategorie vereist voor productie- en projectdoeleinden.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-108">In this case, a cost category is required for production and project purposes.</span></span> <span data-ttu-id="f8b4e-109">Wanneer er een kostencategorie wordt gebruikt in productie en projecten, moet er extra projectgerelateerde informatie worden gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-109">When a cost category is used in production and projects, additional project-related information must be defined.</span></span> <span data-ttu-id="f8b4e-110">De kosten per uur van projecten kunnen bijvoorbeeld afwijken van de kosten per uur die horen bij de productie.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-110">For example, the hourly costs that are associated with projects can differ from the hourly costs that are associated with production.</span></span> <span data-ttu-id="f8b4e-111">U kunt de pagina **Kostencategorieën** gebruiken om een kostencategorie te definiëren die in Productiebeheer en Projectbeheerboekhouding wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-111">You can use the **Cost categories** page to define a cost category that is used in Production control and Project management accounting.</span></span> 

<span data-ttu-id="f8b4e-112">**Opmerking:** kostprijsboekhouding heeft een pagina **Projectcategorieën**, maar deze pagina heeft geen betrekking op de functionaliteit die in dit onderwerp wordt beschreven.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-112">**Note:** Cost accounting has a **Project categories** page, but this page has no relationship to the functionality that is described in this topic.</span></span> <span data-ttu-id="f8b4e-113">Wanneer u een kostencategorie in projecten gebruikt, heeft de pagina **Kostencategorieën** extra tabbladen die extra projectgerelateerde informatie weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-113">When you use a cost category in projects, the **Cost categories** page has additional tabs that show additional project-related information.</span></span> <span data-ttu-id="f8b4e-114">Deze informatie omvat de categoriegroep, een regeleigenschap en grootboekrekeningen, die aan de kostencategorie worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-114">This information includes the category group, a line property, and ledger accounts that are assigned to the cost category.</span></span>

-   <span data-ttu-id="f8b4e-115">U moet de kostencategorie toewijzen aan een categoriegroep die het transactietype **Uren** ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-115">The cost category must be assigned to a category group that supports a transaction type of **Hours**.</span></span>
-   <span data-ttu-id="f8b4e-116">De regeleigenschap geeft standaardgegevens aan over hoe gerapporteerde tijd in rekening kan worden gebracht bij een project.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-116">The line property indicates default information about how reported time can be charged to a project.</span></span>
-   <span data-ttu-id="f8b4e-117">Grootboekrekeningen die gerelateerd zijn aan kosten en verkopen worden meestal gedefinieerd voor de categoriegroep die is toegewezen aan de kostencategorie.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-117">Typically, the ledger accounts that are related to costs and sales are defined for the category group that is assigned to the cost category.</span></span> <span data-ttu-id="f8b4e-118">Er kunnen echter specifieke rekeningen worden gedefinieerd voor een afzonderlijke kostencategorie.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-118">However, specific accounts can be defined for an individual cost category.</span></span>

<span data-ttu-id="f8b4e-119">Extra knoppen op de pagina **Kostencategorieën** bieden toegang tot projectgerelateerde informatie over een geselecteerde kostencategorie.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-119">Additional buttons on the **Cost categories** page let you access project-related information about a selected cost category.</span></span> <span data-ttu-id="f8b4e-120">U kunt bijvoorbeeld projectgerelateerde transacties weergeven, werknemers of projecten definiëren die gebruik mogen maken van de kostencategorie en rapporten weergeven.</span><span class="sxs-lookup"><span data-stu-id="f8b4e-120">For example, you can view project-related transactions, define employees or projects, define hourly costs and sales prices, and view reports.</span></span>




