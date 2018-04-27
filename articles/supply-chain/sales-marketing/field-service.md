---
title: Integratie met Microsoft Dynamics 365 for Field Service
description: In dit onderwerp vindt u een overzicht van de integratie met Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
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
ms.sourcegitcommit: d32a4e376770fc73c79b94924d5ae062d201d84a
ms.openlocfilehash: a224962152e80293f6cf3425dea74d73a283e31a
ms.contentlocale: nl-nl
ms.lasthandoff: 04/12/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a><span data-ttu-id="f178c-103">Integratie met Microsoft Dynamics 365 for Field Service</span><span class="sxs-lookup"><span data-stu-id="f178c-103">Integration with Microsoft Dynamics 365 for Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f178c-104">Microsoft Dynamics 365 for Finance and Operations maakt synchronisatie mogelijk van bedrijfsprocessen tussen Finance and Operations en Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="f178c-104">Microsoft Dynamics 365 for Finance and Operations enables synchronization of business processes between Finance and Operations and Microsoft Dynamics 365 for Field Service.</span></span> <span data-ttu-id="f178c-105">De integratiescenario's worden geconfigureerd met uitbreidbare Gegevensintegrator-sjablonen en de Common Data Service (CDS) voor het inschakelen van de synchronisatie van bedrijfsprocessen.</span><span class="sxs-lookup"><span data-stu-id="f178c-105">The integration scenarios are configured by using extensible Data integrator templates and the Common Data Service (CDS) to enable the synchronization of business processes.</span></span>

<span data-ttu-id="f178c-106">[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span><span class="sxs-lookup"><span data-stu-id="f178c-106">[![Synchronization of business processes between Finance and Operations and Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)</span></span>

<span data-ttu-id="f178c-107">De eerste fase van de integratie tussen Field Service en Finance and Operations is gericht op het inschakelen van werkorders en overeenkomsten in het Field Service dien worden gefactureerd in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f178c-107">The first phase  of the integration between Field Service and Finance and Operations is focused on enabling work orders and agreements in Field Service to be invoiced in Finance and Operations.</span></span> <span data-ttu-id="f178c-108">De ondersteunde stroom begint in Field Service, waar informatie uit werkorders wordt gesynchroniseerd met Finance and Operations als verkooporders.</span><span class="sxs-lookup"><span data-stu-id="f178c-108">The supported flow starts in Field Service, where information from work orders is synchronized to Finance and Operations as sales orders.</span></span> <span data-ttu-id="f178c-109">In Finance and Operations worden de verkooporders gefactureerd voor het genereren van factuurdocumenten.</span><span class="sxs-lookup"><span data-stu-id="f178c-109">In Finance and Operations, the sales orders are invoiced to generate invoice documents.</span></span> <span data-ttu-id="f178c-110">Bovendien wordt de informatie van overeenkomstfacturen in Field Service gesynchroniseerd met Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f178c-110">In addition, the information from Field Service agreement invoices is synchronized to Finance and Operations.</span></span> <span data-ttu-id="f178c-111">De Microsoft Dynamics 365 Gegevensintegrator synchroniseert gegevens met behulp van aanpasbare projecten.</span><span class="sxs-lookup"><span data-stu-id="f178c-111">The Microsoft Dynamics 365 Data integrator synchronizes data by using customizable projects.</span></span> <span data-ttu-id="f178c-112">Standaardsjablonen kunnen worden gebruikt om aangepaste integratieprojecten te maken waarin extra standaardvelden en aangepaste velden en entiteiten kunnen worden toegewezen voor het corrigeren van de integratie en voor het voldoen aan specifieke behoeften.</span><span class="sxs-lookup"><span data-stu-id="f178c-112">Standard templates can be used to create custom integration projects where additional standard and custom fields, and also entities, can be mapped to adjust the integration and meet specific requirements.</span></span>

<span data-ttu-id="f178c-113">In de eerste fase van de integratie tussen Field Service en Finance and Operations wordt de synchronisatie gestart van de volgende items:</span><span class="sxs-lookup"><span data-stu-id="f178c-113">The first phase of the integration between Field Service and Finance and Operations enables synchronization of the following items:</span></span>

- [<span data-ttu-id="f178c-114">Producten in Finance and Operations met producten van Field Service die informatie over het producttype bevatten</span><span class="sxs-lookup"><span data-stu-id="f178c-114">Products in Finance and Operations to products in Field Service that include Product Type information</span></span>](field-service-product.md)
- [<span data-ttu-id="f178c-115">Werkorders in Field Service met verkooporders in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f178c-115">Work orders in Field Service to sales orders in Finance and Operations</span></span>](field-service-work-order.md)
- [<span data-ttu-id="f178c-116">Facturen in Field Service vrije-tekstfacturen in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f178c-116">Invoices in Field Service to free text invoices in Finance and Operations</span></span>](field-service-invoice.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="f178c-117">Systeemvereisten voor Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f178c-117">System requirements for Finance and Operations</span></span>
<span data-ttu-id="f178c-118">Field Service-integratie ondersteunt de volgende versies:</span><span class="sxs-lookup"><span data-stu-id="f178c-118">Field Service integration supports the following versions:</span></span>

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a><span data-ttu-id="f178c-119">Dynamics 365 for Finance and Operations versie 8.0 (April 2018) of later</span><span class="sxs-lookup"><span data-stu-id="f178c-119">Dynamics 365 for Finance and Operations version 8.0 (April 2018) or later</span></span>

- <span data-ttu-id="f178c-120">Dynamics 365 for Finance and Operations versie 8.0 (April 2018) is uitgebracht in april 2018 en heeft een buildnummer 8.0.30.8020 met Platform Update 15 (7.0.4841.35234).</span><span class="sxs-lookup"><span data-stu-id="f178c-120">Dynamics 365 for Finance and Operations version 8.0 (April 2018) was released in April 2018 and has an application build number 8.0.30.8020 with Platform Update 15 (7.0.4841.35234).</span></span> 

## <a name="system-requirements-for-field-service"></a><span data-ttu-id="f178c-121">Systeemvereisten voor Field Service</span><span class="sxs-lookup"><span data-stu-id="f178c-121">System requirements for Field Service</span></span>
<span data-ttu-id="f178c-122">Als u de oplossing Field Service-integratie wilt gebruiken, moet u de volgende onderdelen installeren:</span><span class="sxs-lookup"><span data-stu-id="f178c-122">To use the Field Service integration solution, you must install the following components:</span></span>

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a><span data-ttu-id="f178c-123">Microsoft Dynamics 365 for Field Service 9.0 of hoger</span><span class="sxs-lookup"><span data-stu-id="f178c-123">Microsoft Dynamics 365 for Field Service 9.0 or later</span></span>

- <span data-ttu-id="f178c-124">Dynamics 365 for Field Service-versie 1612 (9.0.1.733) (DB 9.0.1.733) online of een hogere versie.</span><span class="sxs-lookup"><span data-stu-id="f178c-124">Dynamics 365 for Field Service version 1612 (9.0.1.733) (DB 9.0.1.733) online or a later version.</span></span>
- <span data-ttu-id="f178c-125">De oplossing Prospect naar contant geld (P2C) voor Dynamics 365, versie 1.15.0.1 of een hogere versie.</span><span class="sxs-lookup"><span data-stu-id="f178c-125">Prospect to Cash (P2C) solution for Dynamics 365, version 1.15.0.1 or a later version.</span></span> <span data-ttu-id="f178c-126">De oplossing kan worden gedownload van [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="f178c-126">The solution is available for download from [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
- <span data-ttu-id="f178c-127">De oplossing Field Service-integratie voor Dynamics 365, versie 1.0.0.0 of een hogere versie.</span><span class="sxs-lookup"><span data-stu-id="f178c-127">Field Service integration solution for Dynamics 365, version 1.0.0.0 or a later version.</span></span> <span data-ttu-id="f178c-128">De oplossing kan worden gedownload van AppSource.</span><span class="sxs-lookup"><span data-stu-id="f178c-128">The solution is available for download from AppSource.</span></span> <span data-ttu-id="f178c-129">**(IN AFWACHTING VAN VRIJGAVE)**</span><span class="sxs-lookup"><span data-stu-id="f178c-129">**(PENDING RELEASE)**</span></span>

