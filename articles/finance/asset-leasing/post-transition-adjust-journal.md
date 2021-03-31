---
title: Journaalboeking voor transitiecorrectie boeken in Activa leasen
description: In dit onderwerp wordt de functionaliteit beschreven waarmee u een leaseportefeuille kunt overzetten naar de nieuwe boekhoudstandaarden voor leases, Accounting Standards Codification Topic 842 (ASC 842) en International Financial Reporting Standard 16 (IFRS 16).
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7ed62f52753a6697a7547ada0317041669cf3506
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207200"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="1d080-103">Journaalboeking voor transitiecorrectie boeken in Activa leasen</span><span class="sxs-lookup"><span data-stu-id="1d080-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1d080-104">In dit onderwerp wordt de functionaliteit beschreven waarmee u een lease portfolio kunt overzetten naar de nieuwe boekhoudstandaarden voor leases: Accounting Standards Codification Topic 842 (ASC 842), de standaard voor algemeen geaccepteerde boekhoudprincipes in de Verenigde Staten (US GAAP) en International Financial Reporting Standard 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="1d080-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="1d080-105">Zie [Leaseboeken instellen](set-up-lease-books.md) voor informatie over het overzetten van een boek naar de nieuwe standaarden.</span><span class="sxs-lookup"><span data-stu-id="1d080-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="1d080-106">Wanneer u een journaalboeking voor transitiecorrectie maakt, wordt er een journaalboeking gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="1d080-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="1d080-107">Deze boeking weerspiegelt het effect op de balans van het vastleggen van de lease volgens de nieuwe standaarden op die datum.</span><span class="sxs-lookup"><span data-stu-id="1d080-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="1d080-108">De betreffende activumrekening wordt gedebiteerd voor de boekwaarde op die datum en de passivarekening wordt gecrediteerd.</span><span class="sxs-lookup"><span data-stu-id="1d080-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="1d080-109">Het verschil wordt gedebiteerd of gecrediteerd op ingehouden inkomsten.</span><span class="sxs-lookup"><span data-stu-id="1d080-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="1d080-110">Voer de volgende stappen uit om een transitiecorrectie te boeken conform de nieuwe boekhoudstandaarden.</span><span class="sxs-lookup"><span data-stu-id="1d080-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="1d080-111">Selecteer de lease op de pagina **Lease-overzicht** en selecteer vervolgens **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="1d080-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="1d080-112">Selecteer **Betalingsschema** in het boek.</span><span class="sxs-lookup"><span data-stu-id="1d080-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="1d080-113">Selecteer **Bevestigen** in het dialoogvenster **Betalingsschema**.</span><span class="sxs-lookup"><span data-stu-id="1d080-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="1d080-114">Sluit vervolgens het dialoogvenster.</span><span class="sxs-lookup"><span data-stu-id="1d080-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="1d080-115">Selecteer **Transitiecorrectie**.</span><span class="sxs-lookup"><span data-stu-id="1d080-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="1d080-116">Een transitiecorrectie kan alleen worden gemaakt voor leaseboeken die zijn toegewezen aan een boek waarin het veld **Transitieboek** beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="1d080-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="1d080-117">Als de waarde in het veld **Begin van lease** later valt dan de transitiedatum, wordt de waarde in het veld **Transitiecorrectie** niet bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="1d080-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="1d080-118">Selecteer **Activaleasejournalen** om de boeking het journaal weer te geven.</span><span class="sxs-lookup"><span data-stu-id="1d080-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="1d080-119">Selecteer het nieuwe journaal en selecteer vervolgens **Boeken**.</span><span class="sxs-lookup"><span data-stu-id="1d080-119">Select the new journal, and then select **Post**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]