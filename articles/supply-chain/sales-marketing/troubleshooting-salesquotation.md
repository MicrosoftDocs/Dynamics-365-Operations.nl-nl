---
title: Problemen met verkoopoffertes oplossen
description: In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met verkoopoffertes.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTable, SalesQuotationTableListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9a9cc821d2fe9accad1dae210271682cdd2ce4ba
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232201"
---
# <a name="troubleshoot-sales-quotations"></a><span data-ttu-id="623ae-103">Problemen met verkoopoffertes oplossen</span><span class="sxs-lookup"><span data-stu-id="623ae-103">Troubleshoot sales quotations</span></span>

<span data-ttu-id="623ae-104">In dit onderwerp wordt beschreven hoe u problemen kunt oplossen die kunnen optreden tijdens het werken met verkoopoffertes.</span><span class="sxs-lookup"><span data-stu-id="623ae-104">This topic describes how to fix issues that you might encounter while you work with sales quotations.</span></span>

## <a name="i-cant-change-the-sales-quantity-of-a-sales-quotation-for-a-service-item"></a><span data-ttu-id="623ae-105">Ik kan de verkoophoeveelheid van een verkoopofferte voor een serviceartikel niet wijzigen.</span><span class="sxs-lookup"><span data-stu-id="623ae-105">I can't change the sales quantity of a sales quotation for a service item.</span></span>

### <a name="issue-description"></a><span data-ttu-id="623ae-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="623ae-106">Issue description</span></span>

<span data-ttu-id="623ae-107">Als u probeert een verkoophoeveelheid (veld **SalesQty**) voor een artikel van het type *Service* op een verkoopofferteregel in te stellen, wordt het volgende bericht weergegeven: 'Bijwerken niet toegestaan voor veld Hoeveelheid'.</span><span class="sxs-lookup"><span data-stu-id="623ae-107">If you try to set a sales quantity (**SalesQty** field) for an item of the *Service* type on a sales quotation line, you will receive the following message: "Update not allowed for field Quantity."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="623ae-108">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="623ae-108">Issue resolution</span></span>

<span data-ttu-id="623ae-109">U kunt geen verkoophoeveelheid instellen voor producten die serviceartikelen zijn.</span><span class="sxs-lookup"><span data-stu-id="623ae-109">You can't set a sales quantity for products that are service items.</span></span> <span data-ttu-id="623ae-110">Als u bijvoorbeeld een service voor het installeren van een artikel aanbiedt, is het niet zinvol om een hoeveelheid vast te leggen, omdat er geen fysiek artikel is.</span><span class="sxs-lookup"><span data-stu-id="623ae-110">For example, if you offer a service to install an item, it doesn't make sense to record a quantity, because there is no physical item.</span></span> <span data-ttu-id="623ae-111">Er is alleen een service.</span><span class="sxs-lookup"><span data-stu-id="623ae-111">There is only a service.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]