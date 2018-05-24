---
title: Integratie met Microsoft Dynamics 365 for Field Service
description: In dit onderwerp vindt u een overzicht van de integratie met Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 03a932652cdd93b2a5917d0fca72809d1648b678
ms.openlocfilehash: b1acf0b64914a3199fcf44f8377e32b26f0af99e
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="12ccb-103">Integratie met Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="12ccb-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="12ccb-104">Microsoft Dynamics 365 for Finance and Operations maakt synchronisatie mogelijk van bedrijfsprocessen tussen Finance and Operations en Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="12ccb-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="12ccb-105">De integratiescenario's worden geconfigureerd met uitbreidbare Gegevensintegrator-sjablonen en de Common Data Service (CDS) voor het inschakelen van de synchronisatie van bedrijfsprocessen.</span><span class="sxs-lookup"><span data-stu-id="12ccb-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="12ccb-106">[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="12ccb-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="12ccb-107">De eerste fase van de integratie tussen Field Service en Finance and Operations is gericht op het inschakelen van werkorders en overeenkomsten in het Field Service dien worden gefactureerd in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12ccb-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="12ccb-108">De ondersteunde stroom begint in Field Service, waar informatie uit werkorders wordt gesynchroniseerd met Finance and Operations als verkooporders.</span><span class="sxs-lookup"><span data-stu-id="12ccb-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="12ccb-109">In Finance and Operations worden de verkooporders gefactureerd voor het genereren van factuurdocumenten.</span><span class="sxs-lookup"><span data-stu-id="12ccb-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="12ccb-110">Bovendien wordt de informatie van overeenkomstfacturen in Field Service gesynchroniseerd met Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="12ccb-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="12ccb-111">De Microsoft Dynamics 365 Gegevensintegrator synchroniseert gegevens met behulp van aanpasbare projecten.</span><span class="sxs-lookup"><span data-stu-id="12ccb-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="12ccb-112">Standaardsjablonen kunnen worden gebruikt om aangepaste integratieprojecten te maken waarin extra standaardvelden en aangepaste velden en entiteiten kunnen worden toegewezen voor het corrigeren van de integratie en voor het voldoen aan specifieke behoeften.</span><span class="sxs-lookup"><span data-stu-id="12ccb-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="12ccb-113">In de eerste fase van de integratie tussen Field Service en Finance and Operations wordt de synchronisatie gestart van de volgende items:</span><span class="sxs-lookup"><span data-stu-id="12ccb-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="12ccb-114">Producten in Finance and Operations met producten van Field Service die informatie over het producttype bevatten</span><span class="sxs-lookup"><span data-stu-id="12ccb-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="12ccb-115">Werkorders in Field Service met verkooporders in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="12ccb-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="12ccb-116">Facturen in Field Service vrije-tekstfacturen in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="12ccb-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

<span data-ttu-id="12ccb-117">Als u een voorbeeld wilt bekijken van de manier waarop u een werkorder kunt synchroniseren tussen Field Service en Finance and Operations, bekijkt u de korte YouTube-video:</span><span class="sxs-lookup"><span data-stu-id="12ccb-117">To see an example of how you can synchronize a work order between Field Service and Finance and Operations, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/hAB4TDVMjxU]

[<span data-ttu-id="12ccb-118">Een werkorder synchroniseren tussen Field Service en Finance en Operations (YouTube-video)</span><span class="sxs-lookup"><span data-stu-id="12ccb-118">Synchronize a work order between Field Service and Finance and Operations (YouTube video)</span></span>](https://youtu.be/hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="12ccb-119">Systeemvereisten voor Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="12ccb-119">System requirements for Finance and Operations</span></span>
<span data-ttu-id="12ccb-120">Field Service-integratie ondersteunt de volgende versies:</span><span class="sxs-lookup"><span data-stu-id="12ccb-120">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="12ccb-121">Dynamics 365 for Finance and Operations versie 8.0 (April 2018) of later</span><span class="sxs-lookup"><span data-stu-id="12ccb-121">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="12ccb-122">Dynamics 365 for Finance and Operations versie 8.0 (April 2018) is uitgebracht in april 2018 en heeft een buildnummer 8.0.30.8020 met Platform Update 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="12ccb-122">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="12ccb-123">Systeemvereisten voor Field Service</span><span class="sxs-lookup"><span data-stu-id="12ccb-123">System requirements for Field Service</span></span>
<span data-ttu-id="12ccb-124">Als u de oplossing Field Service-integratie wilt gebruiken, moet u de volgende onderdelen installeren:</span><span class="sxs-lookup"><span data-stu-id="12ccb-124">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="12ccb-125">Microsoft Dynamics 365 for Field Service 9.0 of hoger</span><span class="sxs-lookup"><span data-stu-id="12ccb-125">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="12ccb-126">Dynamics 365 for Field Service-versie 1612 (9.0.1.733) (DB 9.0.1.733) online of een hogere versie.</span><span class="sxs-lookup"><span data-stu-id="12ccb-126">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="12ccb-127">De oplossing Prospect naar contant geld (P2C) voor Dynamics 365, versie 1.15.0.1 of een hogere versie.</span><span class="sxs-lookup"><span data-stu-id="12ccb-127">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="12ccb-128">De oplossing kan worden gedownload van [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="12ccb-128">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="12ccb-129">De oplossing Field Service-integratie voor Dynamics 365, versie 1.0.0.0 of een hogere versie.</span><span class="sxs-lookup"><span data-stu-id="12ccb-129">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="12ccb-130">De oplossing kan worden gedownload van [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span><span class="sxs-lookup"><span data-stu-id="12ccb-130">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).</span></span>

