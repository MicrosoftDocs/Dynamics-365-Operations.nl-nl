---
title: Onkostentypen instellen
description: In dit onderwerp wordt uitgelegd hoe u onkostentypen instelt in Activa leasen.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2019-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: b50f406c7411ff8ed990a312fde9c2fc0ba3c3db
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819693"
---
# <a name="set-up-expense-types"></a><span data-ttu-id="cb532-103">Onkostentypen instellen</span><span class="sxs-lookup"><span data-stu-id="cb532-103">Set up expense types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb532-104">In dit onderwerp wordt uitgelegd hoe u onkostentypen instelt in Activa leasen.</span><span class="sxs-lookup"><span data-stu-id="cb532-104">This topic explains how to set up expense types in Asset leasing.</span></span> <span data-ttu-id="cb532-105">Kosten die niet in het betalingsschema worden vertegenwoordigd, worden *onkosten* genoemd.</span><span class="sxs-lookup"><span data-stu-id="cb532-105">Costs that aren't represented by the payment schedule are known as *expense costs*.</span></span> <span data-ttu-id="cb532-106">Voorbeelden van deze kosten zijn: onroerendgoedbelastingen, onderhoudskosten van algemene ruimten en verzekeringskosten.</span><span class="sxs-lookup"><span data-stu-id="cb532-106">Examples of these costs include property taxes, common area maintenance costs, and insurance expenses.</span></span>

## <a name="add-an-administrative-expense-type"></a><span data-ttu-id="cb532-107">Een administratief onkostentype toevoegen</span><span class="sxs-lookup"><span data-stu-id="cb532-107">Add an administrative expense type</span></span>

1. <span data-ttu-id="cb532-108">Ga naar **Activa leasen \> Instellingen \> Onkostentypen**.</span><span class="sxs-lookup"><span data-stu-id="cb532-108">Go to **Asset leasing \> Setup \> Expense types**.</span></span>
2. <span data-ttu-id="cb532-109">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="cb532-109">Select **New**.</span></span>
3. <span data-ttu-id="cb532-110">Voer in de betreffende velden het nieuwe onkostentype en een omschrijving in.</span><span class="sxs-lookup"><span data-stu-id="cb532-110">In the appropriate fields, enter the new expense type and a description.</span></span>

## <a name="assign-accounts-to-administrative-costs"></a><span data-ttu-id="cb532-111">Rekeningen toewijzen aan administratieve kosten</span><span class="sxs-lookup"><span data-stu-id="cb532-111">Assign accounts to administrative costs</span></span>

<span data-ttu-id="cb532-112">Vervolgens koppelt u rekeningen aan de onkostentypen.</span><span class="sxs-lookup"><span data-stu-id="cb532-112">Next, you should associate accounts with the expense types.</span></span> <span data-ttu-id="cb532-113">Deze rekeningen worden gedebiteerd wanneer er onkostenschemaposten worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="cb532-113">These accounts will be debited when expense schedule entries are posted.</span></span> <span data-ttu-id="cb532-114">De tegenrekening wordt opgegeven op de regels **Betalingschema voor administratieve kosten** van elke lease.</span><span class="sxs-lookup"><span data-stu-id="cb532-114">The offset account is specified on the **Executory costs payment schedule** lines on each lease.</span></span>

1. <span data-ttu-id="cb532-115">Ga naar **Activa leasen \> Instellingen \> Parameters voor activa leasen**.</span><span class="sxs-lookup"><span data-stu-id="cb532-115">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="cb532-116">Selecteer het onkostentype op het tabblad **Rekeningen**, op het sneltabblad **Administratieve kosten**, in het veld **Onkosten type**.</span><span class="sxs-lookup"><span data-stu-id="cb532-116">On the **Accounts** tab, on the **Executory costs** FastTab, in the **Expense type** field, select the expense type.</span></span>
3. <span data-ttu-id="cb532-117">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="cb532-117">Select **Add**.</span></span>
4. <span data-ttu-id="cb532-118">Selecteer in het veld **Boektype** het boektype dat u wilt koppelen aan de administratieve kosten.</span><span class="sxs-lookup"><span data-stu-id="cb532-118">In the **Book type** field, select the book type to link to the administrative costs.</span></span>

    > [!NOTE]
    > <span data-ttu-id="cb532-119">U kunt meerdere boektypen aan dezelfde onkostenrekening koppelen.</span><span class="sxs-lookup"><span data-stu-id="cb532-119">Multiple book types can be linked to the same expense account.</span></span>

5. <span data-ttu-id="cb532-120">Geef in het veld **Rekeningcode** op voor welke leases u het boek wilt toepassen:</span><span class="sxs-lookup"><span data-stu-id="cb532-120">In the **Account code** field, specify which leases the book should be applied to:</span></span>

    - <span data-ttu-id="cb532-121">**Alle**: pas het boek toe op alle leases.</span><span class="sxs-lookup"><span data-stu-id="cb532-121">**All** – Apply the book to all leases.</span></span>
    - <span data-ttu-id="cb532-122">**Groep**: pas het boek toe op een specifieke groep leases.</span><span class="sxs-lookup"><span data-stu-id="cb532-122">**Group** – Apply the book to a specific group of leases.</span></span>
    - <span data-ttu-id="cb532-123">**Tabel**: pas het boek toe op specifieke leases.</span><span class="sxs-lookup"><span data-stu-id="cb532-123">**Table** – Apply the book to specific leases.</span></span>

6. <span data-ttu-id="cb532-124">Als u **Groep** of **Tabel** hebt geselecteerd in het veld **Rekeningcode**, selecteert u een rekeningnummer of groepnummer in het veld **Rekening-/groepnummer**.</span><span class="sxs-lookup"><span data-stu-id="cb532-124">If you selected **Group** or **Table** in the **Account code** field, select an account number or group number in the **Account/Group number** field.</span></span>
7. <span data-ttu-id="cb532-125">Selecteer in de desbetreffende velden de hoofdrekening voor financiële leases en de hoofdrekening voor operationele leases.</span><span class="sxs-lookup"><span data-stu-id="cb532-125">In the appropriate fields, select the finance lease main account and the operating lease main account.</span></span>

<span data-ttu-id="cb532-126">Wanneer u deze stappen hebt voltooid, kunt u onkosten toevoegen via de regels **Betalingsschema voor administratieve kosten** op de pagina **Leasedetails** van een geselecteerde lease.</span><span class="sxs-lookup"><span data-stu-id="cb532-126">When you've completed these steps, you can add expenses through the **Executory costs payment schedule** lines on the **Lease details** page of a selected lease.</span></span> <span data-ttu-id="cb532-127">U kunt ook onkosten toevoegen wanneer u een nieuwe lease maakt.</span><span class="sxs-lookup"><span data-stu-id="cb532-127">Alternatively, you can add expenses when you create a new lease.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]