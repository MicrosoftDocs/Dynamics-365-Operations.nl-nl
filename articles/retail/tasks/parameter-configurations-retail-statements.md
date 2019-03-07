---
title: " Parameterconfiguraties voor detailhandeloverzichten"
description: Deze procedure demonstreert configuraties voor detailhandelparameters die van invloed zijn op hoe detailhandelsoverzichten worden gemaakt en geboekt.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6dacd2b80ca0d51d81d2bdf5bc2636b47da621ee
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "352615"
---
# <a name="parameter-configurations-for-retail-statements"></a><span data-ttu-id="8d634-103"> Parameterconfiguraties voor detailhandeloverzichten</span><span class="sxs-lookup"><span data-stu-id="8d634-103">Parameter configurations for Retail statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="8d634-104">Deze procedure demonstreert configuraties voor detailhandelparameters die van invloed zijn op hoe detailhandelsoverzichten worden gemaakt en geboekt.</span><span class="sxs-lookup"><span data-stu-id="8d634-104">This procedure demonstrates configurations for Retail parameters that affect how Retail statements get created and posted.</span></span> <span data-ttu-id="8d634-105">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="8d634-105">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="8d634-106">Ga naar Detailhandel en commerce > Instelling van hoofdkantoor > Parameters > Detailhandelparameters.</span><span class="sxs-lookup"><span data-stu-id="8d634-106">Go to Retail and commerce > Headquarters setup  > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="8d634-107">Klik op het tabblad Boeking.</span><span class="sxs-lookup"><span data-stu-id="8d634-107">Click the Posting tab.</span></span>
    * <span data-ttu-id="8d634-108">Selecteer 'Ja' als u de periodieke kortingsbedragen specifiek wilt boeken.</span><span class="sxs-lookup"><span data-stu-id="8d634-108">Select "Yes" if you want to post the periodic discount amounts specifically.</span></span>  
    * <span data-ttu-id="8d634-109">Selecteer 'Standaard' om standaardrekeningen te gebruiken of selecteer 'Periodiek' als u wilt definiëren welke rekening moet worden gebruikt voor elke periodieke rekening.</span><span class="sxs-lookup"><span data-stu-id="8d634-109">Select "Standard" to use default accounts, or select "Periodic" if you want to define which account to use for each periodic discount.</span></span>  
    * <span data-ttu-id="8d634-110">Selecteer 'Overzicht' als voorraadregels moeten worden samengevoegd indien mogelijk.</span><span class="sxs-lookup"><span data-stu-id="8d634-110">Select "Summary" if inventory lines should get aggregated whenever possible.</span></span>  
    * <span data-ttu-id="8d634-111">Selecteer 'Ja' als facturen en betalingen automatisch moeten worden vereffend als onderdeel van het overzichtsboekingsproces.</span><span class="sxs-lookup"><span data-stu-id="8d634-111">Select "Yes" if Invoices and Payments should get automatically settled as part of the Statement posting process.</span></span>  
    * <span data-ttu-id="8d634-112">Selecteer 'Ja' als kluisstortingstransacties moeten worden samengevoegd.</span><span class="sxs-lookup"><span data-stu-id="8d634-112">Select "Yes" if Safe drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="8d634-113">Selecteer 'Ja' als bankstortingstransacties moeten worden samengevoegd.</span><span class="sxs-lookup"><span data-stu-id="8d634-113">Select "Yes" if Bank drop transactions should get aggregated.</span></span>  
    * <span data-ttu-id="8d634-114">Selecteer 'Ja' om samenvoeging in te schakelen voor overzichtsboeking.</span><span class="sxs-lookup"><span data-stu-id="8d634-114">Select "Yes" to turn aggregation on for Statement posting.</span></span>  
    * <span data-ttu-id="8d634-115">Selecteer 'Ja' om orders parallel te maken en te verwerken wanneer overzichten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="8d634-115">Select "Yes" to create and process orders in parallel when statements are posted.</span></span>  
    * <span data-ttu-id="8d634-116">Voer de maximale orders in die moeten worden verwerkt in elke batchtaak.</span><span class="sxs-lookup"><span data-stu-id="8d634-116">Enter the maximum orders to be processed in each batch job task.</span></span>  
3. <span data-ttu-id="8d634-117">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="8d634-117">Click Save.</span></span>

