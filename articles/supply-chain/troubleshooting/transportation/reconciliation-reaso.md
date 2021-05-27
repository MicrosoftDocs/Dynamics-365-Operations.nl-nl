---
title: U kunt om afstemmingsredenen alleen de hoofdrekening als de creditrekening toevoegen
description: Wanneer u in Transportbeheer een afstemmingsreden in stelt, kunt u alleen de hoofdrekening als de creditrekening toevoegen.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026391"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="796d0-103">U kunt om afstemmingsredenen alleen de hoofdrekening als de creditrekening toevoegen</span><span class="sxs-lookup"><span data-stu-id="796d0-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="796d0-104">KB-nummer: 4603538</span><span class="sxs-lookup"><span data-stu-id="796d0-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="796d0-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="796d0-105">Symptoms</span></span>

<span data-ttu-id="796d0-106">Wanneer u in Transportbeheer een afstemmingsreden in stelt, kunt u alleen de hoofdrekening als de creditrekening toevoegen.</span><span class="sxs-lookup"><span data-stu-id="796d0-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="796d0-107">U kunt geen kostenplaats of een andere dimensie toevoegen als de creditrekening.</span><span class="sxs-lookup"><span data-stu-id="796d0-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="796d0-108">Met de debetrekening kunt u echter andere dimensies selecteren.</span><span class="sxs-lookup"><span data-stu-id="796d0-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="796d0-109">Oplossing</span><span class="sxs-lookup"><span data-stu-id="796d0-109">Resolution</span></span>

<span data-ttu-id="796d0-110">Als het afstemmingsproces niet is uitgevoerd om de leverancier te betalen maar een bepaalde hoofdrekening te crediteren, staat het systeem u niet toe om een financiële dimensie voor de creditrekening te selecteren wanneer u de afstemmingsreden instelt.</span><span class="sxs-lookup"><span data-stu-id="796d0-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="796d0-111">Als voor de rekeningstructuur een specifieke waarde voor de financiële dimensie nodig is voor de credithoofdrekening, kan het resulterende leveranciersjournaal niet automatisch worden geboekt, omdat de waarde voor de financiële dimensie ontbreekt.</span><span class="sxs-lookup"><span data-stu-id="796d0-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="796d0-112">Daarom moet u de creditrekening eerst handmatig opgeven via de pagina **Factuurjournaal**.</span><span class="sxs-lookup"><span data-stu-id="796d0-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="796d0-113">Omdat er een dimensiewaarde vereist is voor de creditrekening, kan het leveranciersfactuurjournaal niet automatisch worden geboekt.</span><span class="sxs-lookup"><span data-stu-id="796d0-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="796d0-114">U moet dit handmatig doen nadat u de dimensiewaarde handmatig aan de hoofdrekening voor de creditregel hebt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="796d0-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>
