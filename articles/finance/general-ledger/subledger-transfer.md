---
title: Subadministratie overboeken naar het grootboek
description: In dit onderwerp worden mogelijkheden beschreven in Microsoft Dynamics 365 Finance met betrekking tot het overboekingsproces voor subadministratie naar het grootboek.
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1ae10f406148e213fd0272d1387f15606233be27
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000442"
---
# <a name="subledger-transfer-to-the-general-ledger"></a><span data-ttu-id="626ef-103">Subadministratie overboeken naar het grootboek</span><span class="sxs-lookup"><span data-stu-id="626ef-103">Subledger transfer to the General ledger</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="626ef-104">In dit onderwerp worden mogelijkheden van Microsoft Dynamics 365 Finance beschreven die zijn gerelateerd aan de regels voor het overdragen van batches van journaalposten in de subadministratie.</span><span class="sxs-lookup"><span data-stu-id="626ef-104">This topic describes capabilities in Microsoft Dynamics 365 Finance that are related to the rules for transferring batches of subledger journal entries.</span></span>

<span data-ttu-id="626ef-105">In versie 8.1 werd de overdracht van regels toegestaan, waardoor de optie Synchroon werd afgeschaft.</span><span class="sxs-lookup"><span data-stu-id="626ef-105">In version 8.1, changes were made to allow the transfer of rules, which deprecated the Synchronous option.</span></span> <span data-ttu-id="626ef-106">Zie voor meer informatie [Verwijderde of verouderde functies voor Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span><span class="sxs-lookup"><span data-stu-id="626ef-106">For more information, see [Removed or deprecated features for Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).</span></span>

<span data-ttu-id="626ef-107">De volgende opties zijn beschikbaar voor het overboeken van batches uit de subadministratie.</span><span class="sxs-lookup"><span data-stu-id="626ef-107">The following options are available for transferring subledger batches.</span></span> 

 - <span data-ttu-id="626ef-108">Asynchroon: Met deze optie wordt onmiddellijk de overdracht van posten in de subadministratie naar het grootboek gepland.</span><span class="sxs-lookup"><span data-stu-id="626ef-108">Asynchronous – This option will immediately schedule the transfer of the subledger accounting entries to the general ledger.</span></span> <span data-ttu-id="626ef-109">Het boekstuk in het grootboek wordt geregistreerd zodra resources vrij zijn om deze aanvraag te verwerken op de server.</span><span class="sxs-lookup"><span data-stu-id="626ef-109">The general ledger voucher will be recorded as soon as resources are free to process this request on the server.</span></span> 

- <span data-ttu-id="626ef-110">Geplande batch: Met deze optie worden de posten uit de subadministratie toegevoegd die worden overgeboekt naar de verwerkingswachtrij in het grootboek, waar de posten worden verwerkt in de volgorde waarin ze worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="626ef-110">Scheduled batch – This option will add the subledger accounting entries that are being transferred to the processing queue in the general ledger, where the entries will be processed in order received.</span></span> <span data-ttu-id="626ef-111">Het boekstuk in het grootboek wordt geregistreerd op de geplande tijd, als resources vrij zijn om deze batchtaak te verwerken op de server.</span><span class="sxs-lookup"><span data-stu-id="626ef-111">The general ledger voucher will be recorded at the scheduled time if resources are free to process this batch job on the server.</span></span> 
 
<span data-ttu-id="626ef-112">In versie 10.0.8 werden verbeteringen uitgevoerd om de prestaties van de optie Asynchroon te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="626ef-112">In version 10.0.8, improvements were made to enhance the performance of the Asynchrounous option.</span></span> <span data-ttu-id="626ef-113">Deze functie is ingeschakeld onder de functienaam **Prestatieoptimalisatie voor overboeken van subadministratie naar grootboek**.</span><span class="sxs-lookup"><span data-stu-id="626ef-113">This feature is enabled under the feature name **Subledger transfer to General Ledger performance optimization**.</span></span> 
 
<span data-ttu-id="626ef-114">Deze functionaliteit verbetert de overdracht van gegevens vanuit de subadministratie naar het grootboek.</span><span class="sxs-lookup"><span data-stu-id="626ef-114">This functionality improves the transfer of data from the subledger to the general ledger.</span></span> <span data-ttu-id="626ef-115">Dit maakt het proces efficiënter, en groepeert sets van kleinere transacties bijeen voor overboeking.</span><span class="sxs-lookup"><span data-stu-id="626ef-115">It allows the process to be more efficient, and it groups together sets of smaller transactions to transfer.</span></span> <span data-ttu-id="626ef-116">Hierdoor kan de batchserver efficiënter worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="626ef-116">This allows for a more efficient use of the batch server.</span></span> <span data-ttu-id="626ef-117">Voor deze functionaliteit moet de batchserver zijn ingesteld en online en functioneel zijn, zodat de optie voor asynchrone overdrachts werkt.</span><span class="sxs-lookup"><span data-stu-id="626ef-117">This functionality requires that the batch server be set up, online, and functioning in order for the Asynchrounous transfer option to work.</span></span> 