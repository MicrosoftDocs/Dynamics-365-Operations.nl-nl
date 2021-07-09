---
title: Grootboek voor Algemene voorraadboekhouding (Global Inventory Accounting)
description: Dit onderwerp beschrijft grootboeken voor Algemene voorraadboekhouding, die worden gedefinieerd door een combinatie van een valuta, een kalender, een conventie en een koppeling met een rechtspersoon.
author: AndersGirke
ms.date: 06/18/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2021-06-18
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ea3434675aa3b7f2304be93ef9b489747994fa9d
ms.sourcegitcommit: eceae470f4ae58000ec33fea34db34b7a7a1af43
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/18/2021
ms.locfileid: "6273136"
---
# <a name="global-inventory-accounting-ledger"></a><span data-ttu-id="bb925-103">Grootboek voor Algemene voorraadboekhouding (Global Inventory Accounting)</span><span class="sxs-lookup"><span data-stu-id="bb925-103">Global Inventory Accounting ledger</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="bb925-104">Algemene voorraadboekhouding heeft een eigen set grootboeken.</span><span class="sxs-lookup"><span data-stu-id="bb925-104">Global Inventory Accounting has its own set of ledgers.</span></span> <span data-ttu-id="bb925-105">Telkens wanneer een voorraadgerelateerde transactie wordt verwerkt voor een relevante rechtspersoon, kan het systeem die transactie in elk gewenst aantal grootboeken voor Algemene voorraadboekhouding verantwoorden.</span><span class="sxs-lookup"><span data-stu-id="bb925-105">Each time an inventory-related transaction is processed for a relevant legal entity, the system can account for that transaction in any number of Global Inventory Accounting ledgers, as required.</span></span>

<span data-ttu-id="bb925-106">Een grootboek is een register met debet- en crediteenheden.</span><span class="sxs-lookup"><span data-stu-id="bb925-106">A ledger is a register of debit and credit measures.</span></span> <span data-ttu-id="bb925-107">Deze eenheden worden geclassificeerd met behulp van kostenelementen en grootboekrekeningen.</span><span class="sxs-lookup"><span data-stu-id="bb925-107">These measures are classified by using cost elements and subledger accounts.</span></span> <span data-ttu-id="bb925-108">Een grootboek van Algemene voorraadboekhouding wordt gedefinieerd door de combinatie van een valuta, een kalender, een conventie en een koppeling met een rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="bb925-108">A Global Inventory Accounting ledger is defined by its combination of a currency, a calendar, a convention, and an association with a legal entity.</span></span>

<span data-ttu-id="bb925-109">Als u grootboeken voor Algemene voorraadboekhouding wilt instellen, gaat u naar **Algemene voorraadboekhouding \> Instellingen \> Grootboeken voor Algemene voorraadboekhouding**.</span><span class="sxs-lookup"><span data-stu-id="bb925-109">To set up your Global Inventory Accounting ledgers, go to **Global inventory accounting \> Setup \> Global inventory accounting ledgers**.</span></span> <span data-ttu-id="bb925-110">Stel voor elk grootboek de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="bb925-110">For each ledger, set the following fields:</span></span>

- <span data-ttu-id="bb925-111">**Naam**: voer de naam van het grootboek in.</span><span class="sxs-lookup"><span data-stu-id="bb925-111">**Name** – Enter the name of the ledger.</span></span>
- <span data-ttu-id="bb925-112">**Beschrijving**: voer een beschrijving van het grootboek in.</span><span class="sxs-lookup"><span data-stu-id="bb925-112">**Description** – Enter a description of the ledger.</span></span>
- <span data-ttu-id="bb925-113">**Fiscale kalender**: geef de fiscale kalender voor het grootboek op.</span><span class="sxs-lookup"><span data-stu-id="bb925-113">**Fiscal calendar** – Specify the fiscal calendar for the ledger.</span></span>
- <span data-ttu-id="bb925-114">**Valuta en wisselkoerstype**: gebruik de velden op dit sneltabblad om de boekhoudingvaluta te selecteren die in het grootboek wordt gebruikt en het wisselkoerstype.</span><span class="sxs-lookup"><span data-stu-id="bb925-114">**Currency and exchange rate type** – Use the fields on this FastTab to select the accounting currency that the ledger uses, and the exchange rate type.</span></span> <span data-ttu-id="bb925-115">De valuta die u selecteert, kan verschillen van de valuta die de rechtspersoon gebruikt.</span><span class="sxs-lookup"><span data-stu-id="bb925-115">The currency that you select can differ from the currency that the legal entity uses.</span></span> <span data-ttu-id="bb925-116">In Global Inventory Accounting kunnen gebruikers zoveel kostprijsboekhoudingsgrootboeken definiëren als nodig is.</span><span class="sxs-lookup"><span data-stu-id="bb925-116">In Global Inventory Accounting, users can define as many costing ledgers as they require.</span></span> <span data-ttu-id="bb925-117">Global Inventory Accounting ondersteunt voorraadboekhouding in meerdere valuta's en in meerdere waarderingen.</span><span class="sxs-lookup"><span data-stu-id="bb925-117">Global Inventory Accounting supports inventory accounting in multiple currencies and in multiple valuations.</span></span> <span data-ttu-id="bb925-118">Stel de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="bb925-118">Set the following fields:</span></span>

    - <span data-ttu-id="bb925-119">**Valuta**: selecteer de kostprijsprijsvaluta waarin voorraadgerelateerde waarden worden onderhouden.</span><span class="sxs-lookup"><span data-stu-id="bb925-119">**Currency** – Select the costing currency that inventory-related values are maintained in.</span></span> <span data-ttu-id="bb925-120">Deze waarden omvatten de voorraadwaarde, de kosten van de verkochte goederen, de transitvoorraad en alle soorten afwijkingen.</span><span class="sxs-lookup"><span data-stu-id="bb925-120">These values include the inventory value, cost of goods sold, inventory in transit, and all kinds of variance.</span></span>
    - <span data-ttu-id="bb925-121">**Type wisselkoers**: selecteer de wisselkoers die het systeem moet gebruiken om het transactiebedrag in de transactievaluta en de standaardkosten van de artikelen naar de kostprijsprijsvaluta te converteren.</span><span class="sxs-lookup"><span data-stu-id="bb925-121">**Exchange rate type** – Select the exchange rate that the system should use to convert the transaction amount in the transaction currency and the standard cost of the items into the costing currency.</span></span>

- <span data-ttu-id="bb925-122">**Conventienaam**: geef een conventie op.</span><span class="sxs-lookup"><span data-stu-id="bb925-122">**Convention name** – Specify a convention.</span></span> <span data-ttu-id="bb925-123">Een conventie is een verzameling beleidsregels die bepalen hoe kosten in dit grootboek worden vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="bb925-123">A convention is a collection of policies that establish how costs will be accounted in this ledger.</span></span>
- <span data-ttu-id="bb925-124">**Rechtspersoon**: de documenten die naar de geselecteerde rechtspersoon zijn geboekt, worden in het grootboek vastgelegd.</span><span class="sxs-lookup"><span data-stu-id="bb925-124">**Legal entity** – The ledger will account the documents that are posted to the selected legal entity.</span></span>
- <span data-ttu-id="bb925-125">**Priming**: bepaal of voorraadtransacties die zijn gemaakt voordat het grootboek werd gemaakt, moeten worden verwerkt volgens de valuta en conventie in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="bb925-125">**Priming** – Select whether inventory transactions that were created before the ledger was created should be processed according to the currency and convention in the ledger.</span></span> <span data-ttu-id="bb925-126">Selecteer een van de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="bb925-126">Select one of the following values:</span></span>

    - <span data-ttu-id="bb925-127">**Geactiveerd**: het grootboek moet transacties verwerken die zijn gemaakt voordat het grootboek werd gemaakt.</span><span class="sxs-lookup"><span data-stu-id="bb925-127">**Activated** – The ledger should process transactions that were created before the ledger was created.</span></span>
    - <span data-ttu-id="bb925-128">**Gedeactiveerd**: het grootboek moet alleen transacties verwerken die zijn gemaakt na dat het grootboek werd gemaakt.</span><span class="sxs-lookup"><span data-stu-id="bb925-128">**Deactivated** – The ledger should process only transactions that are created after the ledger was created.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="bb925-129">U kunt **niet meer** terug naar dit veld om het in te stellen nadat u nieuwe documenten hebt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="bb925-129">You will **not** be able to come back and set this field after you enter new documents.</span></span>

- <span data-ttu-id="bb925-130">**Status**: de status van de nieuwe grootboeken wordt automatisch op *Voorbereiden* ingesteld door het systeem.</span><span class="sxs-lookup"><span data-stu-id="bb925-130">**Status** – The system automatically sets the status of newly created ledgers to *Prepare*.</span></span>
