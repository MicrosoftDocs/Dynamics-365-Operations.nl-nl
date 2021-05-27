---
title: TDS-grootboekrekeningen instellen
description: In dit onderwerp wordt uitgelegd hoe u grootboekrekeningen moet instellen voor de functie TDS (belasting ingehouden op bron).
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
ms.openlocfilehash: 93d4cb54488ec0eeee40ca56f3e46f30012f54f5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023147"
---
# <a name="set-up-tds-ledger-accounts"></a><span data-ttu-id="60852-103">TDS-grootboekrekeningen instellen</span><span class="sxs-lookup"><span data-stu-id="60852-103">Set up TDS ledger accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60852-104">In dit onderwerp wordt uitgelegd hoe u grootboekrekeningen moet instellen voor de functie TDS (belasting ingehouden op bron).</span><span class="sxs-lookup"><span data-stu-id="60852-104">This topic explains how to set up ledger accounts for the Tax Deducted at Source (TDS) feature.</span></span> <span data-ttu-id="60852-105">Met de pagina **Rekeningschema** kunt u grootboekrekeningen voor TDS instellen.</span><span class="sxs-lookup"><span data-stu-id="60852-105">You use the **Chart of accounts** page to set up ledger accounts for TDS.</span></span>

1. <span data-ttu-id="60852-106">Ga naar **Grootboek \> Rekeningschema \> Rekeningen \> Hoofdrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="60852-106">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**.</span></span>
2. <span data-ttu-id="60852-107">Selecteer **Alt+N** op het tabblad **Overzicht** om een TDS-grootboekrekening te maken en voer de vereiste gegevens in.</span><span class="sxs-lookup"><span data-stu-id="60852-107">On the **Overview** tab, select **Alt+N** to create a TDS ledger account, and enter the required details.</span></span>
3. <span data-ttu-id="60852-108">Selecteer **Bronbelasting** in het veld **Boekingstype** op het tabblad **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="60852-108">On the **Setup** tab, in the **Posting type** field, select **Withholding tax**.</span></span>     

    > [!NOTE]
    > <span data-ttu-id="60852-109">Grootboekrekeningen met het boekingstype **Bronbelasting** kunnen alleen worden gedefinieerd als klantenrekeningen die worden gebruikt om het te ontvangen TDS-bedrag voor een TDS-belastingcode te boeken.</span><span class="sxs-lookup"><span data-stu-id="60852-109">Ledger accounts that have a posting type of **Withholding tax** can be defined only as receivable accounts that are used to post the TDS receivable amount for a TDS tax code.</span></span>

4. <span data-ttu-id="60852-110">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="60852-110">Close the page.</span></span>
