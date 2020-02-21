---
title: Groepsgewijs orders voor detailhandeltransacties maken
description: Dit onderwerp beschrijft het groepsgewijs maken van orders voor detailhandeltransacties in Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3f691017ad06d3416e4ba0e86d7a0bc207aba5bd
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004269"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a><span data-ttu-id="b9e26-103">Groepsgewijs orders voor detailhandeltransacties maken (Openbare preview)</span><span class="sxs-lookup"><span data-stu-id="b9e26-103">Trickle feed-based order creation for retail store transactions (Public preview)</span></span>

[!include [banner](includes/banner.md)]



<span data-ttu-id="b9e26-104">In Dynamics 365 Retail versie 10.0.4 en eerder is het boeken van een overzicht een bewerking die aan het einde van de dag plaatsvindt. Alle transacties worden aan het einde van de dag geboekt.</span><span class="sxs-lookup"><span data-stu-id="b9e26-104">In Dynamics 365 Retail versions 10.0.4 and earlier, statement posting is an end-of-day operation and all transactions are posted in the books at the end of the day.</span></span> <span data-ttu-id="b9e26-105">Grote transacties moeten vervolgens in een beperkt tijdvenster worden verwerkt, met soms als gevolg dat er fouten optreden bij het laden, vergrendelen en boeken van overzichten.</span><span class="sxs-lookup"><span data-stu-id="b9e26-105">Large transactions must then be processed in a limited time window, sometimes resulting in load and locks and statement posting failures.</span></span> <span data-ttu-id="b9e26-106">Bovendien kunnen winkeliers gedurende de dag geen opbrengsten en betalingen in hun boeken toerekenen.</span><span class="sxs-lookup"><span data-stu-id="b9e26-106">Retailers also can't recognize revenue and payments in their books throughout the day.</span></span>

<span data-ttu-id="b9e26-107">Met de openbare preview voor het groepsgewijs maken van orders in Retail versie 10.0.5 kunnen transacties gedurende de hele dag worden verwerkt, en worden alleen de financiële afstemming van de kas en andere contante transacties aan het einde van de dag verwerkt.</span><span class="sxs-lookup"><span data-stu-id="b9e26-107">With the public preview of trickle feed-based order creation introduced in Retail version 10.0.5, transactions are processed throughout the day, and only the financial reconciliation of tenders and other cash management transactions are processed at the end of the day.</span></span> <span data-ttu-id="b9e26-108">Met deze functionaliteit wordt de werklast voor het maken van verkooporders, facturen en betalingen verspreid over de hele dag. Dit leidt tot betere prestaties en de mogelijkheid om opbrengsten en betalingen in de boeken bijna in realtime toe te rekenen.</span><span class="sxs-lookup"><span data-stu-id="b9e26-108">This functionality splits the load of creating sales orders, invoices, and payments throughout the day, providing better perceived performance and the ability to recognize revenue and payments in the books in near real-time.</span></span> 


## <a name="how-to-use-trickle-feed-based-posting"></a><span data-ttu-id="b9e26-109">Groepsgewijs boeken gebruiken</span><span class="sxs-lookup"><span data-stu-id="b9e26-109">How to use trickle feed-based posting</span></span>
  
1. <span data-ttu-id="b9e26-110">Als u groepsgewijs boeken van transacties wilt inschakelen, gaat u naar **Systeembeheer > Instellen > Licentieconfiguratie** en schakelt u de sleutel **Overzichten** uit.</span><span class="sxs-lookup"><span data-stu-id="b9e26-110">To enable trickle feed-based posting of transactions, go to **System administration > Set up > License configuration** and disable the the **Statements** key.</span></span>

2. <span data-ttu-id="b9e26-111">Schakel op dezelfde pagina licentiesleutel **Overzichten (groepsgewijze invoer) - Preview** in.</span><span class="sxs-lookup"><span data-stu-id="b9e26-111">On the same page, enable the **Statements (trickle feed) – Preview** license key.</span></span> <span data-ttu-id="b9e26-112">Wanneer u deze sleutel inschakelt, moet u ervoor zorgen dat er geen overzichten wachten om te worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="b9e26-112">When you enable this key, make sure there are no pending statements waiting to be posted.</span></span> 

    > [!Important]
    > <span data-ttu-id="b9e26-113">Voordat u de licentiesleutel **Overzichten (groepsgewijze invoer) - Preview** inschakelt, moet u controleren of er geen overzichten wachten om te worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="b9e26-113">Before you enable the **Statements (trickle feed) – Preview** license key, make sure that no pending statements are waiting to be posted.</span></span>

3. <span data-ttu-id="b9e26-114">Het huidige overzichtsdocument wordt opgesplitst in twee verschillende typen: transactieoverzicht en financieel overzicht.</span><span class="sxs-lookup"><span data-stu-id="b9e26-114">The current statement document will be split into two different types; transactional statement and financial statement.</span></span>

      - <span data-ttu-id="b9e26-115">In het transactieoverzicht worden alle niet-geboekte en gevalideerde transacties opgenomen. Vervolgens worden verkooporders, verkoopfacturen, betalings- en kortingsjournalen en inkomsten-/uitgaventransacties gemaakt op basis van de door u geconfigureerde frequentie.</span><span class="sxs-lookup"><span data-stu-id="b9e26-115">The transactional statement will pick up all unposted and validated transactions and create sales orders, sales invoices, payment and discount journals, and income-expense transactions at the cadence that you configure.</span></span> <span data-ttu-id="b9e26-116">U moet dit proces configureren met een hoge frequentie, zodat documenten worden gemaakt wanneer de transacties in Headquarters worden geüpload via de P-taak.</span><span class="sxs-lookup"><span data-stu-id="b9e26-116">You should configure this process to run at a high frequency so that documents are created when the transactions are uploaded into Headquarters through the P-job.</span></span> <span data-ttu-id="b9e26-117">Aangezien met het transactieoverzicht al verkooporders en verkoopfacturen worden gemaakt, is het niet echt nodig om de batchtaak **Voorraad boeken** te configureren.</span><span class="sxs-lookup"><span data-stu-id="b9e26-117">With the transactional statement that already creates sales orders and sales invoices, there is no real need to configure the **Post inventory** batch job.</span></span> <span data-ttu-id="b9e26-118">U kunt deze echter nog wel gebruiken om te voldoen aan de specifieke vereisten van uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="b9e26-118">However, you can still use it to meet specific business requirements that you may have.</span></span>  
      
     - <span data-ttu-id="b9e26-119">Het financiële overzicht is ontworpen om aan het einde van de dag te worden gemaakt en ondersteunt alleen de afsluitingsmethode **Ploeg**.</span><span class="sxs-lookup"><span data-stu-id="b9e26-119">The financial statement is designed to be created at the end of the day and only supports the closing method of **Shift**.</span></span> <span data-ttu-id="b9e26-120">Dit overzicht wordt alleen gebruikt voor financiële afstemming en maakt alleen de journalen voor de verschillen tussen het getelde bedrag en het transactiebedrag voor de verschillende betalingsmethoden, samen met journalen voor andere contante transacties.</span><span class="sxs-lookup"><span data-stu-id="b9e26-120">This statement will be limited to financial reconciliation and will only create the journals for the difference amounts between counted amount and transaction amount for the different tenders, along with journals for other cash management transactions.</span></span>   

4. <span data-ttu-id="b9e26-121">Als u het transactieoverzicht wilt berekenen, klikt u op **Detailhandel en commerce > IT detailhandel en commerce > POS-boekingen > Transactieoverzichten in batch berekenen**.</span><span class="sxs-lookup"><span data-stu-id="b9e26-121">To calculate the transactional statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate transactional statements in batch**.</span></span> <span data-ttu-id="b9e26-122">Als u het transactieoverzicht in batch wilt boeken, klikt u op **Detailhandel en commerce > IT detailhandel en commerce > POS-boekingen > Transactieoverzichten in batch boeken**.</span><span class="sxs-lookup"><span data-stu-id="b9e26-122">To post the transactional statement statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post transactional statements in batch**.</span></span>

5. <span data-ttu-id="b9e26-123">Als u het financiële overzicht wilt berekenen, klikt u op **Detailhandel en commerce > IT detailhandel en commerce > POS-boekingen > Financiële overzichten in batch berekenen**.</span><span class="sxs-lookup"><span data-stu-id="b9e26-123">To calculate the financial statement, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate financial statements in batch**.</span></span> <span data-ttu-id="b9e26-124">Als u de financiële overzicht in batch wilt boeken, klikt u op **Detailhandel en commerce > IT detailhandel en commerce > POS-boekingen > Financiële overzichten in batch boeken**.</span><span class="sxs-lookup"><span data-stu-id="b9e26-124">To post the financial statements in batch, click **Retail and Commerce > Retail and Commerce IT > POS Posting > Post financial statements in batch**.</span></span>

> [!NOTE]
> <span data-ttu-id="b9e26-125">De menuopdrachten **Detailhandel en commerce > IT detailhandel en commerce > POS-boekingen > Overzichten in batch berekenen** en **Detailhandel en commerce > IT detailhandel en commerce > POS-boekingen > Overzichten in batch boeken** worden vervangen door deze nieuwe functie.</span><span class="sxs-lookup"><span data-stu-id="b9e26-125">The menu items **Retail and Commerce > Retail and Commerce IT > POS Posting > Calculate statements in batch** and **Retail and Commerce > Retail and Commerce IT > POS Posting > Post statements in batch** are removed with this new feature.</span></span>

<span data-ttu-id="b9e26-126">U kunt de typen van transactie- en financiële overzichten ook handmatig maken.</span><span class="sxs-lookup"><span data-stu-id="b9e26-126">Alternately, transactional and financial statement types can be created manually.</span></span> <span data-ttu-id="b9e26-127">Ga naar **Detailhandel en commerce > Afzetkanalen > Winkels** en klik op **Overzichten**.</span><span class="sxs-lookup"><span data-stu-id="b9e26-127">Go to **Retail and Commerce > Channels > Stores** and click **Statements**.</span></span> <span data-ttu-id="b9e26-128">Klik op **Nieuw** en selecteer het type overzicht dat u wilt maken.</span><span class="sxs-lookup"><span data-stu-id="b9e26-128">Click **New** and then choose the type of statement that you want to create.</span></span> <span data-ttu-id="b9e26-129">De velden op de pagina **Overzichten** en de acties onder **Overzichtsgroep** op de pagina laten de relevante gegevens en acties zien op basis van het geselecteerde overzichtstype.</span><span class="sxs-lookup"><span data-stu-id="b9e26-129">Fields on the **Statements** page and actions under the **Statement group** of the page will show relevant data and actions based on the selected statement type.</span></span>
