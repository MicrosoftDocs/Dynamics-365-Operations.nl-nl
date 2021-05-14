---
title: U kunt werk dat aan een gebruiker is toegewezen, niet annuleren
description: U kunt werk dat aan een gebruiker is toegewezen, niet annuleren
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTable_WHSWorkCancel, WHSWorkTableListPage_WHSWorkCancel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e5f6912cfb1d5be8e46b7989856af99f8a611c11
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924396"
---
# <a name="you-cant-cancel-work-that-is-on-a-user"></a><span data-ttu-id="4f6f0-103">U kunt werk dat aan een gebruiker is toegewezen, niet annuleren</span><span class="sxs-lookup"><span data-stu-id="4f6f0-103">You can't cancel work that is on a user</span></span>

<span data-ttu-id="4f6f0-104">Foutcode: WAX708</span><span class="sxs-lookup"><span data-stu-id="4f6f0-104">Error code: WAX708</span></span>

## <a name="symptoms"></a><span data-ttu-id="4f6f0-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="4f6f0-105">Symptoms</span></span>

<span data-ttu-id="4f6f0-106">Het systeem toont het volgende foutbericht:</span><span class="sxs-lookup"><span data-stu-id="4f6f0-106">The system shows the following error message:</span></span>

> <span data-ttu-id="4f6f0-107">U kunt geen werk annuleren dat op een naam van een gebruiker staat.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-107">You cannot cancel work that is on a user.</span></span>

## <a name="cause"></a><span data-ttu-id="4f6f0-108">Oorzaak</span><span class="sxs-lookup"><span data-stu-id="4f6f0-108">Cause</span></span>

<span data-ttu-id="4f6f0-109">Het werk is vergrendeld door een gebruiker en kan niet worden geannuleerd.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-109">The work is locked by a user and can't be canceled.</span></span> <span data-ttu-id="4f6f0-110">Om dit te bevestigen, opent u de werk-id en vervolgens opent u het tabblad **Algemeen**. Als het werk is vergrendeld, is het veld **Werkstatus** ingesteld op *Wordt uitgevoerd* en het veld **Vergrendeld door** is ingesteld op een gebruikers-id.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-110">To confirm this, open the work ID and then open the **General** tab. If the work is locked, the **Work status** field will be set to *In progress*, and the **Locked by** field will be set to a user ID.</span></span>

## <a name="resolution"></a><span data-ttu-id="4f6f0-111">Oplossing</span><span class="sxs-lookup"><span data-stu-id="4f6f0-111">Resolution</span></span>

<span data-ttu-id="4f6f0-112">Volg deze stappen om werk te annuleren.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-112">To cancel the work, follow these steps.</span></span>

1. <span data-ttu-id="4f6f0-113">Ga naar **Magazijnbeheer \> Periodieke taken \> Opschonen \> Werk annuleren**.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-113">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="4f6f0-114">In het veld **Werk-id** geeft de id op van het werk dat u wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-114">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span>
1. <span data-ttu-id="4f6f0-115">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-115">Select **OK**.</span></span>
1. <span data-ttu-id="4f6f0-116">Selecteer **Ja** om te bevestigen dat u het werk wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-116">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="4f6f0-117">Zie [Magazijnwerk voor afhandeling van uitzonderingen annuleren](../../warehousing/cancel-warehouse-work.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-117">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
