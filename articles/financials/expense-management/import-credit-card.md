---
title: Creditcardtransacties importeren en onderhouden
description: In dit onderwerp wordt uitgelegd hoe u onkostengerelateerde creditcardtransacties importeert en onderhoudt. Deze transacties kunt u zo instellen dat deze automatisch periodiek worden geïmporteerd of u kunt de transacties handmatig invoeren wanneer dit nodig is.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 9674cf495b7fdd40d8672580b9d10e9ebe626bb0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565108"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="0d345-104">Creditcardtransacties importeren en onderhouden</span><span class="sxs-lookup"><span data-stu-id="0d345-104">Import and maintain credit card transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0d345-105">Onkostengerelateerde creditcardtransacties kunnen zo worden ingesteld dat deze automatisch periodiek worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="0d345-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="0d345-106">De transacties kunnen zo nodig ook handmatig worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="0d345-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="0d345-107">De creditcardtransacties worden geïmporteerd via de gegevensentiteit Creditcardtransacties.</span><span class="sxs-lookup"><span data-stu-id="0d345-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="0d345-108">Zie [Gegevensentiteiten](../../dev-itpro/data-entities/data-entities.md) voor meer informatie over gegevensentiteiten.</span><span class="sxs-lookup"><span data-stu-id="0d345-108">For more information about data entities, see [Data entities](../../dev-itpro/data-entities/data-entities.md).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="0d345-109">Creditcardtransacties importeren</span><span class="sxs-lookup"><span data-stu-id="0d345-109">Import credit card transactions</span></span>

1. <span data-ttu-id="0d345-110">Op de pagina **Creditcardtransacties** selecteert u **Transacties importeren**.</span><span class="sxs-lookup"><span data-stu-id="0d345-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="0d345-111">De eerste keer dat u gegevensbeheer opent, moet de lijst met gegevensentiteiten worden bijgewerkt voordat u kunt doorgaan.</span><span class="sxs-lookup"><span data-stu-id="0d345-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="0d345-112">Voer in het veld **Naam** een unieke beschrijving van de importtaak in.</span><span class="sxs-lookup"><span data-stu-id="0d345-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="0d345-113">Selecteer in het veld **Indeling van brongegevens** de indeling in van het bestand met de creditcardtransacties die u wilt importeren.</span><span class="sxs-lookup"><span data-stu-id="0d345-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="0d345-114">Selecteer **Uploaden** en zoek en selecteer het bestand dat u wilt importeren.</span><span class="sxs-lookup"><span data-stu-id="0d345-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="0d345-115">Als het bestand is geüpload, valideert u de toewijzing van het bestand met creditcardtransacties en de kolommen van de gegevensentiteit Creditcardtransacties door de koppeling **Kaart weergeven** op de tegel te selecteren.</span><span class="sxs-lookup"><span data-stu-id="0d345-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="0d345-116">Als er toewijzingsfouten zijn of als u de toewijzing moet wijzigen, brengt u de wijzigingen aan via het tabblad **Visualisering van toewijzing** of **Gegevens toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="0d345-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="0d345-117">Als u de creditcardtransacties wilt automatiseren, selecteert u **Terugkerende gegevenstaak maken**.</span><span class="sxs-lookup"><span data-stu-id="0d345-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="0d345-118">Vervolgens stelt u het terugkeerpatroon in om te bepalen hoe vaak creditcardtransacties moeten worden geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="0d345-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="0d345-119">Wanneer u klaar bent, selecteert u **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d345-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="0d345-120">Als u het geselecteerde bestand nu wilt importeren, selecteert u **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="0d345-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="0d345-121">Als er fouten optreden tijdens het importeren, kunt u het uitvoeringslogboek of de faseringsgegevens controleren om te zien welke fouten u moet corrigeren om een geslaagde import te kunnen garanderen.</span><span class="sxs-lookup"><span data-stu-id="0d345-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="0d345-122">Als u meerdere bestandsindelingen moet importeren, moet u voor elk type indeling aparte importtaken maken.</span><span class="sxs-lookup"><span data-stu-id="0d345-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="0d345-123">De creditcardtransacties van vertrokken werknemers opnieuw toewijzen</span><span class="sxs-lookup"><span data-stu-id="0d345-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="0d345-124">Nadat een werknemerrecord is beëindigd, wordt de AD DS-account (Active Directory Domain Services) van die werknemer uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="0d345-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="0d345-125">Er kunnen echter nog actieve creditcardtransacties zijn die nog moeten worden opgevoerd en vergoed.</span><span class="sxs-lookup"><span data-stu-id="0d345-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="0d345-126">Via de pagina **Creditcardtransacties** kunt u de werknemer voor een creditcardtransactie opnieuw toewijzen, als de oorspronkelijke werknemer niet meer bij het bedrijf werkt.</span><span class="sxs-lookup"><span data-stu-id="0d345-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="0d345-127">Selecteer een of meer creditcardtransacties en selecteer vervolgens **Transacties opnieuw toewijzen**.</span><span class="sxs-lookup"><span data-stu-id="0d345-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="0d345-128">Vervolgens selecteert u een andere werknemer om de creditcardtransacties aan toe te wijzen.</span><span class="sxs-lookup"><span data-stu-id="0d345-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="0d345-129">Nadat de creditcardtransacties opnieuw zijn toegewezen, kunnen deze voor een onkostennota worden geselecteerd en worden betaald via het normale proces voor terugbetaling van onkosten.</span><span class="sxs-lookup"><span data-stu-id="0d345-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
