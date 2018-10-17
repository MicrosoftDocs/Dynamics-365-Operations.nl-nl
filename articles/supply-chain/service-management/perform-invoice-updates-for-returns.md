---
title: Facturen bijwerken voor retouren
description: Deze functionaliteit ondersteunt de bedrijfsprocessen van organisaties die ervoor kiezen retourorders en verkooporders tegelijkertijd en door dezelfde persoon te laten factureren.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 2f962641f7fdae18a360567d6f37348fabbfc302
ms.contentlocale: nl-nl
ms.lasthandoff: 08/07/2018

---


# <a name="perform-invoice-updates-for-returns"></a><span data-ttu-id="dc841-103">Facturen bijwerken voor retouren</span><span class="sxs-lookup"><span data-stu-id="dc841-103">Perform invoice updates for returns</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="dc841-104">Een retourorder is een type verkooporder dat is gemarkeerd als een retourorder.</span><span class="sxs-lookup"><span data-stu-id="dc841-104">A return order is a type of sales order that is marked as a returned order.</span></span> <span data-ttu-id="dc841-105">De lijstpagina **Alle verkooporders** wordt daarom gebruikt voor het genereren van facturen voor retourorders in plaats van het formulier **Retourorders**.</span><span class="sxs-lookup"><span data-stu-id="dc841-105">Therefore, the **All sales orders** list page is used to generate invoices for return orders instead of the **Return orders** form.</span></span> <span data-ttu-id="dc841-106">Deze functionaliteit ondersteunt de bedrijfsprocessen van organisaties die ervoor kiezen retourorders en verkooporders tegelijkertijd en door dezelfde persoon te laten factureren.</span><span class="sxs-lookup"><span data-stu-id="dc841-106">This functionality supports the business processes of organizations that choose to have return orders and sales orders invoiced at the same time and by the same person.</span></span>

<span data-ttu-id="dc841-107">Omdat de factuur voor een geretourneerd artikel voor een negatief bedrag is, wordt deze een creditnota genoemd.</span><span class="sxs-lookup"><span data-stu-id="dc841-107">Because the invoice for a returned item is for a negative amount, it is called a credit note.</span></span>

<span data-ttu-id="dc841-108">Wanneer u het bijwerken van de factuur instelt op batchverwerking, moet de verkooporder van het type **Geretourneerde order** de retourregelstatus **Ontvangen** hebben. Dit duidt erop dat de pakbon van de order is bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="dc841-108">When you set up the invoice update for batch processing, the sales order of type **Returned order** must have a return line status of **Received**, which indicates that the order's packing slip has been updated.</span></span>

## <a name="post-an-invoice-for-a-return-order"></a><span data-ttu-id="dc841-109">Boek een factuur voor de retourorder.</span><span class="sxs-lookup"><span data-stu-id="dc841-109">Post an invoice for a return order</span></span>

1.  <span data-ttu-id="dc841-110">Klik op **Klanten** \> **Algemeen** \> **Verkooporders** \> **Alle verkooporders**.</span><span class="sxs-lookup"><span data-stu-id="dc841-110">Click **Accounts receivable** \> **Common** \> **Sales orders** \> **All sales orders**.</span></span>

2.  <span data-ttu-id="dc841-111">Selecteer een verkooporder waarvoor **Geretourneerde order** wordt weergegeven in het veld **Ordertype**.</span><span class="sxs-lookup"><span data-stu-id="dc841-111">Select a sales order for which **Returned order** is displayed in the **Order type** field.</span></span>

3.  <span data-ttu-id="dc841-112">Klik in het actievenster op het tabblad **Factuur** in de groep **Genereren** op **Factuur**.</span><span class="sxs-lookup"><span data-stu-id="dc841-112">On the Action Pane, on the **Invoice** tab, in the **Generate** group, click **Invoice**.</span></span>

4.  <span data-ttu-id="dc841-113">Schakel op het tabblad **Parameters** het selectievakje **Boeking** in.</span><span class="sxs-lookup"><span data-stu-id="dc841-113">On the **Parameters** tab, select the **Posting** check box.</span></span>

5.  <span data-ttu-id="dc841-114">Bekijk de informatie in het formulier en breng de wijzigingen aan die nodig zijn.</span><span class="sxs-lookup"><span data-stu-id="dc841-114">Review information in the form and make any changes that are needed.</span></span>

6.  <span data-ttu-id="dc841-115">Klik tot slot op **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc841-115">Click **OK**.</span></span> <span data-ttu-id="dc841-116">De creditnota wordt geboekt.</span><span class="sxs-lookup"><span data-stu-id="dc841-116">The credit note is posted.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc841-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="dc841-117">See also</span></span>

[<span data-ttu-id="dc841-118">Pakbonnen bijwerken voor retouren</span><span class="sxs-lookup"><span data-stu-id="dc841-118">Packing slip updates for returns</span></span>](packing-slip-updates-returns.md)

  


