---
title: Leasejournaalnamen instellen
description: In dit onderwerp wordt uitgelegd hoe u leasejournaalnamen definieert. Leasejournaalnamen specificeren in welke journalen invoer vanuit Activa leasen wordt geboekt.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c139df124b249ec9dc5d16096e6f45f22d435456
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880881"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="93d02-104">Leasejournaalnamen instellen</span><span class="sxs-lookup"><span data-stu-id="93d02-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93d02-105">Leasejournaalnamen specificeren in welke journalen transacties van Activa leasen worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="93d02-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="93d02-106">Alleen journaalnamen die zijn toegewezen aan het journaaltype **Activa leasen** worden weergegeven in de velden **Initiële toerekening** en **Maandelijkse journaalnaam** op de pagina **Parameters voor activa leasen**.</span><span class="sxs-lookup"><span data-stu-id="93d02-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="93d02-107">Alleen het journaaltype **Leveranciersfactuurregistratie** kan worden toegewezen aan het veld **Factuurjournaalnaam**.</span><span class="sxs-lookup"><span data-stu-id="93d02-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="93d02-108">Voer de volgende stappen uit om leasejournaalnamen te configureren.</span><span class="sxs-lookup"><span data-stu-id="93d02-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="93d02-109">Ga naar **Activa leasen \> Instellingen \> Parameters voor activa leasen**.</span><span class="sxs-lookup"><span data-stu-id="93d02-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="93d02-110">Ga op het tabblad **Algemeen** naar het veld **Journaalnaam initiële toerekening**, en selecteer een journaal.</span><span class="sxs-lookup"><span data-stu-id="93d02-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="93d02-111">Alle journaalboekingen voor initiële toerekening worden naar deze journaalnaam geboekt.</span><span class="sxs-lookup"><span data-stu-id="93d02-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="93d02-112">Selecteer een journaal in het veld **Factuurjournaalnaam**.</span><span class="sxs-lookup"><span data-stu-id="93d02-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="93d02-113">Als de optie **Betalen aan leverancier** is ingesteld op **Ja** voor het leaseboek, worden leasefacturen onkostenfacturen naar deze journaalnaam geboekt.</span><span class="sxs-lookup"><span data-stu-id="93d02-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="93d02-114">Selecteer een journaal in het veld **Leasejournaalnaam**.</span><span class="sxs-lookup"><span data-stu-id="93d02-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="93d02-115">Alle afschrijvingsposten, renteposten en herindelingsposten op korte termijn worden naar deze journaalnaam geboekt.</span><span class="sxs-lookup"><span data-stu-id="93d02-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="93d02-116">Als de optie **Betalen aan leverancier** is ingesteld op **Nee** voor het leaseboek, worden boekingen voor leasebetalingen en onkostenbetalingen ook naar deze journaalnaam geboekt.</span><span class="sxs-lookup"><span data-stu-id="93d02-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
