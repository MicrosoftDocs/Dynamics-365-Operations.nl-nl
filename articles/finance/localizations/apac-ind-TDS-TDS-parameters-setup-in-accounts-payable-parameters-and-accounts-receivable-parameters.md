---
title: TDS-parameters voor Leveranciers en Klanten instellen
description: In dit onderwerp wordt uitgelegd hoe u parameters kunt instellen in Leveranciers en Klanten om TDS-inhoudingen (belasting ingehouden op bron) te ondersteunen.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023148"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="6c87b-103">TDS-parameters voor Leveranciers en Klanten instellen</span><span class="sxs-lookup"><span data-stu-id="6c87b-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c87b-104">In dit onderwerp wordt uitgelegd hoe u parameters kunt instellen in Leveranciers en Klanten om TDS-inhoudingen (belasting ingehouden op bron) te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="6c87b-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="6c87b-105">Ga naar **Belasting \> Instellen \> Parameters \> Parameters van module Klanten**.</span><span class="sxs-lookup"><span data-stu-id="6c87b-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="6c87b-106">Selecteer **Orderregels bijwerken** op het tabblad **Updates** om het dialoogvenster **Orderregels bijwerken** te openen.</span><span class="sxs-lookup"><span data-stu-id="6c87b-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="6c87b-107">Geef in de sectie van de **TDS-groep** in het veld **TDS-groep bijwerken** de methode op die u wilt gebruiken om de TDS-groep bij te werken op regelniveau.</span><span class="sxs-lookup"><span data-stu-id="6c87b-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="6c87b-108">Deze instelling wordt gebruikt wanneer de TDS-groep wordt bijgewerkt in een orderkoptekst.</span><span class="sxs-lookup"><span data-stu-id="6c87b-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="6c87b-109">De volgende opties zijn beschikbaar:</span><span class="sxs-lookup"><span data-stu-id="6c87b-109">The following options are available:</span></span>

    - <span data-ttu-id="6c87b-110">**Nooit**: de TDS-groep wordt niet bijgewerkt op de orderregels wanneer deze wordt bijgewerkt in de orderkoptekst.</span><span class="sxs-lookup"><span data-stu-id="6c87b-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="6c87b-111">**Altijd**: de TDS-groep wordt automatisch bijgewerkt op de orderregels wanneer deze wordt bijgewerkt in de orderkoptekst.</span><span class="sxs-lookup"><span data-stu-id="6c87b-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="6c87b-112">**Vragen**: gebruikers ontvangen een bericht waarin ze worden gevraagd de TDS-groep op de orderregels bij te werken.</span><span class="sxs-lookup"><span data-stu-id="6c87b-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="6c87b-113">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="6c87b-113">Select **OK**.</span></span>

    <span data-ttu-id="6c87b-114">[![Dialoogvenster Orderregels bijwerken](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="6c87b-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="6c87b-115">Ga naar **Belasting \> Instellen \> Parameters \> Parameters van module Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="6c87b-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="6c87b-116">Stel op het tabblad **Algemeen** op het sneltabblad **Splitsen op basis van aflevergegevens** de optie **Productontvangstbon** in op **Ja** om een productontvangstbon met verschillende afleveradressen en belastingrekeningnummers te boeken en te splitsen.</span><span class="sxs-lookup"><span data-stu-id="6c87b-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="6c87b-117">Als deze optie is ingesteld op **Nee**, kunt u geen inkooppakbon met verschillende afleveradressen en belastingrekeningnummers boeken.</span><span class="sxs-lookup"><span data-stu-id="6c87b-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="6c87b-118">Stel de optie **Factuur** in op **Ja** om een inkoopfactuur met verschillende afleveradressen en belastingrekeningnummers te maken en te splitsen.</span><span class="sxs-lookup"><span data-stu-id="6c87b-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="6c87b-119">[![Sneltabblad Splitsen op basis van aflevergegevens](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="6c87b-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="6c87b-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="6c87b-120">Close the page.</span></span>
