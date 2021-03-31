---
title: Betalingsschema's voor activaleases in batch bevestigen
description: In dit onderwerp wordt uitgelegd hoe u meerdere betalingsschema's in een batch kunt bevestigen.
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
ms.openlocfilehash: 0275fda306a58159a982b342622b9b6a18fa5b71
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225508"
---
# <a name="confirm-asset-leasing-payment-schedules-in-a-batch"></a><span data-ttu-id="8eb9a-103">Betalingsschema's voor activaleases in batch bevestigen</span><span class="sxs-lookup"><span data-stu-id="8eb9a-103">Confirm Asset leasing payment schedules in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8eb9a-104">In dit onderwerp wordt uitgelegd hoe u meerdere betalingsschema's in een batch kunt bevestigen.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-104">This topic explains how to confirm multiple payment schedules in a batch.</span></span> <span data-ttu-id="8eb9a-105">Betalingsschema's worden per lease bevestigd of met het bevestigingsbatchproces.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-105">Payment schedules are confirmed either on a lease-to-lease basis or through the confirmation batch process.</span></span> <span data-ttu-id="8eb9a-106">Een journaalboeking kan alleen worden geboekt naar een lease met een bevestigd betalingsschema.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-106">A journal entry can be posted only against a lease that has a confirmed payment schedule.</span></span> <span data-ttu-id="8eb9a-107">De bevestiging van het betalingsschema dient als laatste goedkeuring van de financiële gegevens voor de lease.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-107">Confirmation of the payment schedule serves as a final approval of the financial information for the lease.</span></span> <span data-ttu-id="8eb9a-108">Alle toekomstige wijzigingen in de financiële informatie voor de lease, zoals betalingen en de leasetermijn, vormen een leasecorrectie en moeten op die manier worden verwerkt.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-108">All future changes to the financial information for the lease, such as payments and the lease term, constitute a lease adjustment and should be processed in that way.</span></span>

<span data-ttu-id="8eb9a-109">Voer de volgende stappen uit om meerdere betalingsschema's te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-109">To confirm multiple payment schedules, follow these steps.</span></span>

1. <span data-ttu-id="8eb9a-110">Ga naar **Activa leasen \> Periodiek \> Bevestigingsbatch**.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-110">Go to **Asset leasing \> Periodic \> Confirmation batch**.</span></span>
2. <span data-ttu-id="8eb9a-111">Selecteer **Bevestigingsbatch** op de pagina **Bevestigingsbatch**.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-111">On the **Confirmation batch** page, select **Confirmation batch**.</span></span>
3. <span data-ttu-id="8eb9a-112">In het dialoogvenster dat wordt weergegeven, filtert u op de boeken die u wilt bevestigen.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-112">In the dialog box that appears, filter for the books that you want to confirm.</span></span>

    - <span data-ttu-id="8eb9a-113">Om alle boeken in een specifieke leasegroep te bevestigen, selecteert u de groep in het veld **Leasegroep**.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-113">To confirm all the books in a specific lease group, select the group in the **Lease group** field.</span></span>
    - <span data-ttu-id="8eb9a-114">Als u specifieke boeken wilt bevestigen, selecteert u de boeken in het veld **Boek-id**.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-114">To confirm specific books, select the books in the **Book ID** field.</span></span>
    - <span data-ttu-id="8eb9a-115">Schakel de parameter **Voor alle boeken** in om alle boeken te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-115">To confirm all books, turn on the **For all books** parameter.</span></span>

<span data-ttu-id="8eb9a-116">De informatie voor de nieuw bevestigde boeken wordt weergegeven op de pagina **Bevestigde boeken**.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-116">Information for the newly confirmed books is shown on the **Confirmed books** page.</span></span> <span data-ttu-id="8eb9a-117">Nadat de betalingsschema's zijn bevestigd, kunnen de journaalposten voor eerste toerekening worden geboekt op basis van de leases.</span><span class="sxs-lookup"><span data-stu-id="8eb9a-117">After the payment schedules are confirmed, the initial recognition journal entries can be posted against the leases.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]