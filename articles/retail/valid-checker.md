---
title: Consistentiecontrole voor detailhandeltransacties
description: In dit onderwerp wordt de functie voor de consistentiecontrole voor detailhandeltransacties in Microsoft Dynamics 365 for Retail beschreven.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: db01a12b92574b41f1f4fe7281c23992e0d36027
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "302127"
---
# <a name="retail-transaction-consistency-checker"></a><span data-ttu-id="d2ce6-103">Consistentiecontrole voor detailhandeltransacties</span><span class="sxs-lookup"><span data-stu-id="d2ce6-103">Retail transaction consistency checker</span></span>


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

<span data-ttu-id="d2ce6-104">In dit onderwerp wordt de nieuwe functie voor de consistentiecontrole voor detailhandeltransacties in Microsoft Dynamics 365 for Finance and Operations versie 8.1.3 beschreven.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-104">This topic describes the retail transaction consistency checker functionality introduced in Microsoft Dynamics 365 for Finance and Operations version 8.1.3.</span></span> <span data-ttu-id="d2ce6-105">In de consistentiecontrole worden inconsistente transacties geïdentificeerd en geïsoleerd voordat ze worden verzameld door het boekingsproces voor overzichten.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-105">The consistency checker identifies and isolates inconsistent transactions before they are picked up by the statement posting process.</span></span>

<span data-ttu-id="d2ce6-106">Wanneer een overzicht wordt geboekt in Retail, kan de boeking mislukken vanwege inconsistente gegevens in de tabellen met detailhandeltransacties.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-106">When a statement is posted in Retail, posting can fail due to inconsistent data in the retail transaction tables.</span></span> <span data-ttu-id="d2ce6-107">Het gegevensprobleem kan worden veroorzaakt door onvoorziene problemen in de verkooppunttoepassing of door incorrect geïmporteerde transacties uit verkooppuntsystemen van derden.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-107">The data issue may be caused by by unforeseen issues in the point of sale (POS) application, or if transactions were incorrectly imported from third-party POS systems.</span></span> <span data-ttu-id="d2ce6-108">Enkele voorbeelden van hoe deze inconsistenties kunnen worden weergegeven:</span><span class="sxs-lookup"><span data-stu-id="d2ce6-108">Examples of how these inconsistencies may appear include:</span></span> 

  - <span data-ttu-id="d2ce6-109">Het transactietotaal in de kopteksttabel komt niet overeen met het transactietotaal op de regels.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-109">The transaction total on the header table does not match the transaction total on the lines.</span></span>
  - <span data-ttu-id="d2ce6-110">Het aantal regels in de kopteksttabel komt niet overeen met het aantal regels in de transactietabel.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-110">The line count on the header table does not match with the number of lines in the transaction table.</span></span>
  - <span data-ttu-id="d2ce6-111">De btw in de kopteksttabel komen niet overeen met het btw-bedrag op de regels.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-111">Taxes on the header table do not match the tax amount on the lines.</span></span> 
  
<span data-ttu-id="d2ce6-112">Wanneer er inconsistente transacties worden verzameld door het boekingsproces voor overzichten, worden er inconsistente verkoopfacturen en betalingsjournalen gemaakt en mislukt het gehele boekingsproces voor overzichten.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-112">When inconsistent transactions are picked up by the statement posting process, inconsistent sales invoices and payment journals are created, and the entire statement posting process fails as a result.</span></span> <span data-ttu-id="d2ce6-113">Dergelijke overzichten kunnen alleen nog worden hersteld door middel van gecompliceerde gegevenscorrecties via meerdere transactietabellen.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-113">Recovering the statements from such a state involves complex data fixes across multiple transaction tables.</span></span> <span data-ttu-id="d2ce6-114">Met de consistentiecontrole voor detailhandeltransacties kunnen dit soort problemen worden voorkomen.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-114">The retail transaction consistency checker prevents such issues.</span></span>

<span data-ttu-id="d2ce6-115">Het volgende diagram biedt inzicht in het boekingsproces met de consistentiecontrole voor detailhandeltransacties.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-115">The following chart illustrates the posting process with the transaction consistency checker.</span></span>

<span data-ttu-id="d2ce6-116">![Boekingsproces voor overzichten met consistentiecontrole voor detailhandeltransacties](./media/validchecker.png "Boekingsproces voor overzichten met consistentiecontrole voor detailhandeltransacties")</span><span class="sxs-lookup"><span data-stu-id="d2ce6-116">![Statement posting process with retail transaction consistency checker](./media/validchecker.png "Statement posting process with retail transsaction consistency checker")</span></span>

<span data-ttu-id="d2ce6-117">Met het batchproces **Winkeltransacties valideren** wordt de consistentie van de tabellen met detailhandeltransacties gecontroleerd voor de volgende scenario's.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-117">The **Validate store transactions** batch process checks the consistency of the retail transaction tables for the following scenarios.</span></span>

- <span data-ttu-id="d2ce6-118">Klantrekening: hiermee wordt gevalideerd of de klantrekening in de tabellen met detailhandeltransacties bestaat in het HQ-klantmodel.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-118">Customer account - Validates that the customer account in the retail transaction tables exists in the HQ customer master.</span></span>
- <span data-ttu-id="d2ce6-119">Regeltelling: hiermee wordt gevalideerd of het aantal regels, zoals vastgelegd in de transactiekopteksttabel, overeenkomt met het aantal regels in de verkooptransactietabellen.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-119">Line count - Validates that the number of lines, as captured on the transaction header table, matches the number of lines in the sales transaction tables.</span></span>

## <a name="set-up-the-consistency-checker"></a><span data-ttu-id="d2ce6-120">De consistentiecontrole instellen</span><span class="sxs-lookup"><span data-stu-id="d2ce6-120">Set up the consistency checker</span></span>
<span data-ttu-id="d2ce6-121">Configureer het batchproces Winkeltransacties valideren via **Detailhandel \> IT detailhandel \> POS-boekingen** voor periodieke uitvoering.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-121">Configure the "Validate store transactions" batch process, at **Retail \> Retail IT \> POS posting**, for periodic runs.</span></span> <span data-ttu-id="d2ce6-122">De batchverwerking kan worden gepland op basis van de organisatiehiërarchie van de winkel, op dezelfde wijze als de processen Overzichten in batch berekenen en Overzichten in batch boeken zijn ingesteld.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-122">The batch job can be scheduled based on store organization hierarchy, similar to how the "Calculate statement in batch" and "Post statement in batch" processes are set up.</span></span> <span data-ttu-id="d2ce6-123">We raden u aan dit batchproces zo te configureren dat het meerdere keren per dag wordt uitgevoerd en zo te plannen dat het na elke P-taak wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-123">We recommend that you configure this batch process to run multiple times in a day and schedule it so that it runs at the end of every P-job execution.</span></span>

## <a name="results-of-validation-process"></a><span data-ttu-id="d2ce6-124">Resultaten van validatieproces</span><span class="sxs-lookup"><span data-stu-id="d2ce6-124">Results of validation process</span></span>
<span data-ttu-id="d2ce6-125">De resultaten van de validatie door het batchproces worden toegevoegd aan de betreffende detailhandeltransactie.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-125">The results of the validation check by the batch process are tagged on the appropriate retail transaction.</span></span> <span data-ttu-id="d2ce6-126">Het veld **Validatiestatus** in de record van de detailhandeltransactie wordt ingesteld op **Geslaagd** of **Fout** en de datum van de laatste validatie wordt weergegeven in het veld **Laatste validatietijd**.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-126">The **Validation status** field on the retail transaction record is either set to **Successful** or **Error**, and the date of the last validation run appears on the **Last validation time** field.</span></span>

<span data-ttu-id="d2ce6-127">Als u meer beschrijvende fouttekst voor een validatiefout wilt weergeven, selecteert u de betreffende transactierecord voor de detailhandelwinkel en klikt u op de knop **Validatiefouten**.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-127">To view more descriptive error text relating to a validation failure, select the relevant retail store transaction record and click the **Validation errors** button.</span></span>

<span data-ttu-id="d2ce6-128">Transacties die de validatie niet doorstaan en transacties die nog niet zijn gevalideerd, worden niet in overzichten opgenomen.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-128">Transactions that fail the validation check and transactions that have not yet been validated will not be pulled into statements.</span></span> <span data-ttu-id="d2ce6-129">Tijdens het proces Overzicht berekenen wordt voor gebruikers een melding weergegeven als er transacties zijn die door een validatiefout niet in het overzicht zijn opgenomen.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-129">During the "Calculate statement" process, users will be notified if there are transactions that could have been included in the statement but weren't.</span></span>

<span data-ttu-id="d2ce6-130">Als een validatiefout wordt gevonden, kunt u de fout alleen herstelen door contact op te nemen met Microsoft Support.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-130">If a validation error is found, the only way to fix the error is to contact Microsoft Support.</span></span> <span data-ttu-id="d2ce6-131">In een toekomstige versie wordt het voor gebruikers mogelijk om de betreffende records te herstellen via de gebruikersinterface.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-131">In a future release, capability will be added so that users can fix the records that failed through the user interface.</span></span> <span data-ttu-id="d2ce6-132">Daarnaast worden functies voor logboekregistratie en controle toegevoegd, zodat de geschiedenis van de wijzigingen kan worden bijgehouden.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-132">Logging and auditing capabilities will also be made available to trace the history of the modifications.</span></span>

> [!NOTE]
> <span data-ttu-id="d2ce6-133">In een toekomstige versie worden extra validatieregels toegevoegd om meer scenario's te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="d2ce6-133">Additional validation rules to support more scenarios will be added in a future release.</span></span>
