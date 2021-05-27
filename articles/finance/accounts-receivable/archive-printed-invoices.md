---
title: Afgedrukte klantfacturen met hashnummers archiveren
description: In dit onderwerp wordt uitgelegd hoe u archivering kunt inschakelen om afgedrukte klantfacturen met hekjes op te slaan.
author: ilyako
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 841e6059f5b0d70dbd1fe12a1f8910bbb31ddc86
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018973"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="15a0b-103">Afgedrukte klantfacturen met hashnummers archiveren</span><span class="sxs-lookup"><span data-stu-id="15a0b-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="15a0b-104">In sommige landen is het wettelijk verplicht om berekende hekjes in het systeem op te slaan, samen met afdrukken van bepaalde documenten.</span><span class="sxs-lookup"><span data-stu-id="15a0b-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="15a0b-105">Hekjes kunnen worden gebruikt voor rapportage aan instanties en tijdens audits.</span><span class="sxs-lookup"><span data-stu-id="15a0b-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="15a0b-106">In dit onderwerp wordt uitgelegd hoe u archivering kunt configureren om afgedrukte klantfacturen met hekjes op te slaan.</span><span class="sxs-lookup"><span data-stu-id="15a0b-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="15a0b-107">Vereisten</span><span class="sxs-lookup"><span data-stu-id="15a0b-107">Prerequisites</span></span>

- <span data-ttu-id="15a0b-108">Schakel in de werkruimte **Functiebeheer** de functie **Afgedrukte klantfacturen met hekjes archiveren** in.</span><span class="sxs-lookup"><span data-stu-id="15a0b-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="15a0b-109">Zie [Overzicht van functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="15a0b-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="15a0b-110">Configureer de afdrukbare indelingen van vereiste documenten **Afdrukbeheer**.</span><span class="sxs-lookup"><span data-stu-id="15a0b-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="15a0b-111">Deze functionaliteit is van toepassing op de volgende documenten.</span><span class="sxs-lookup"><span data-stu-id="15a0b-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="15a0b-112">**Klanten**</span><span class="sxs-lookup"><span data-stu-id="15a0b-112">**Accounts receivable**</span></span>
- <span data-ttu-id="15a0b-113">Klantfactuur</span><span class="sxs-lookup"><span data-stu-id="15a0b-113">Customer invoice</span></span>
- <span data-ttu-id="15a0b-114">Creditnota van de klant</span><span class="sxs-lookup"><span data-stu-id="15a0b-114">Customer credit note</span></span>
- <span data-ttu-id="15a0b-115">Vrije-tekstfactuur</span><span class="sxs-lookup"><span data-stu-id="15a0b-115">Free text invoice</span></span>
- <span data-ttu-id="15a0b-116">Vrije-tekstcreditnota</span><span class="sxs-lookup"><span data-stu-id="15a0b-116">Free text credit note</span></span>

<span data-ttu-id="15a0b-117">**Projectbeheer en boekhouding**</span><span class="sxs-lookup"><span data-stu-id="15a0b-117">**Project management and accounting**</span></span>
- <span data-ttu-id="15a0b-118">Projectfactuur</span><span class="sxs-lookup"><span data-stu-id="15a0b-118">Project invoice</span></span>
- <span data-ttu-id="15a0b-119">Creditnota van project</span><span class="sxs-lookup"><span data-stu-id="15a0b-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="15a0b-120">Klanthoofdgegevens configureren</span><span class="sxs-lookup"><span data-stu-id="15a0b-120">Configure customer master data</span></span>
<span data-ttu-id="15a0b-121">Voer de volgende stappen uit om de klantgegevens te configureren en schakel de mogelijkheid in om afgedrukte facturen automatisch als bijlagen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="15a0b-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="15a0b-122">Ga naar **Klanten** > **Alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="15a0b-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="15a0b-123">Selecteer een klant en selecteer op het sneltabblad **Factuur en levering** in de sectie **E-FACTUUR** in het veld **eInvoice-bijlage** de optie **Ja**.</span><span class="sxs-lookup"><span data-stu-id="15a0b-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="15a0b-124">Facturen afdrukken</span><span class="sxs-lookup"><span data-stu-id="15a0b-124">Print invoices</span></span>
<span data-ttu-id="15a0b-125">U kunt elke vrije tekst-, klant- en projectfactuur of creditnota boeken en afdrukken voor de klant die in de vorige procedure is geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="15a0b-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="15a0b-126">Open de pagina **Bijlagen** voor de afgedrukte factuur.</span><span class="sxs-lookup"><span data-stu-id="15a0b-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="15a0b-127">Zoek op het sneltabblad **Bijlage** in de veldgroep **Aanvullende details** in het veld **Hekje voor document** het opgeslagen hekje op dat is berekend voor de afgedrukte factuur.</span><span class="sxs-lookup"><span data-stu-id="15a0b-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![Hekje voor bijlage](media/attach-hash-num.jpg)

