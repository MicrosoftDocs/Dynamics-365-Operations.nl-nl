---
title: U kunt een verkooporder voor de klant niet factureren
description: U kunt de oorspronkelijke verkooporder en de inkooporder voor directe levering niet meer factureren nadat u de optie Factuur automatisch boeken hebt ingeschakeld.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ab18a2a1dec4b70c55a55637b087c6b11023aa40
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026401"
---
# <a name="you-cant-invoice-a-customer-facing-sales-order"></a><span data-ttu-id="106db-103">U kunt een verkooporder voor de klant niet factureren</span><span class="sxs-lookup"><span data-stu-id="106db-103">You can't invoice a customer-facing sales order</span></span>

<span data-ttu-id="106db-104">KB-nummer: 4611793</span><span class="sxs-lookup"><span data-stu-id="106db-104">KB number: 4611793</span></span>

## <a name="symptoms"></a><span data-ttu-id="106db-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="106db-105">Symptoms</span></span>

<span data-ttu-id="106db-106">U kunt de oorspronkelijke verkooporder en de inkooporder voor directe levering niet meer factureren nadat u de optie **Factuur automatisch boeken** hebt ingeschakeld op de pagina **Intercompany** voor een leverancier.</span><span class="sxs-lookup"><span data-stu-id="106db-106">You can no longer invoice the original sales order and the original direct delivery purchase order after you enable the **Post invoice automatically** option on the **Intercompany** page for a vendor.</span></span>

## <a name="resolution"></a><span data-ttu-id="106db-107">Oplossing</span><span class="sxs-lookup"><span data-stu-id="106db-107">Resolution</span></span>

<span data-ttu-id="106db-108">Het synchronisatiegedrag voor intercompany-facturen en facturen voor directe leveringsorders wordt gecontroleerd en verplicht gemaakt door de parameters die zijn beschreven in [Parameters instellen voor boeken naar een intercompany-order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span><span class="sxs-lookup"><span data-stu-id="106db-108">The synchronization behavior for intercompany and direct delivery order invoices is controlled and forced by the parameters that are described in [Set up parameters to post an intercompany order](/dynamicsax-2012/appuser-itpro/set-up-parameters-to-post-an-intercompany-order).</span></span>

<span data-ttu-id="106db-109">Nadat u deze parameters hebt ingesteld, moet u eerst de intercompany-verkooporder factureren.</span><span class="sxs-lookup"><span data-stu-id="106db-109">After you set those parameters, you must invoice the intercompany sales order first.</span></span> <span data-ttu-id="106db-110">De oorspronkelijke verkooporders en inkooporders worden vervolgens gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="106db-110">The original sales orders and purchase orders will then be synchronized.</span></span>
