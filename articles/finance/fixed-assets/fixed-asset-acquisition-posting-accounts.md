---
title: Boekingsrekeningen verwerving vaste activa
description: In dit artikel wordt beschreven hoe u grootboekboekingsrekeningen instelt voor het aanchaffen van activa.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a340df57a6073c6d9b6f2cdaadbf8f21fc11649
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241037"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="70710-103">Boekingsrekeningen verwerving vaste activa</span><span class="sxs-lookup"><span data-stu-id="70710-103">Fixed asset acquisition posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="70710-104">In dit artikel wordt beschreven hoe u grootboekboekingsrekeningen instelt voor het aanchaffen van activa.</span><span class="sxs-lookup"><span data-stu-id="70710-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="70710-105">Rekeningen voor het boeken van verwervingen van vaste activa kunnen verschillen afhankelijk van de methode die wordt gebruikt om het activum te verwerven.</span><span class="sxs-lookup"><span data-stu-id="70710-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="70710-106">Selecteer Verwerving en Verwervingscorrectie op de pagina Boekingsprofielen voor vaste activa op het tabblad Grootboekrekeningen vaste-activarekeningen in te stellen om naar het grootboek te boeken.</span><span class="sxs-lookup"><span data-stu-id="70710-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="70710-107">In journalen en op inkooporders is het grootboek gewoonlijk de balansrekening waar de aanschafwaarde van het nieuwe vaste activum wordt gedebiteerd.</span><span class="sxs-lookup"><span data-stu-id="70710-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="70710-108">Deze rekening wordt niet weergegeven in het journaal en kan niet worden vervangen in transacties.</span><span class="sxs-lookup"><span data-stu-id="70710-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="70710-109">Tegenrekening is ook een balansrekening.</span><span class="sxs-lookup"><span data-stu-id="70710-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="70710-110">In het algemene journaal en in het vaste-activajournaal is deze rekening vaak de bankrekening die wordt gebruikt om te betalen voor de aanschaf van het activum.</span><span class="sxs-lookup"><span data-stu-id="70710-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="70710-111">De tegenrekening is een standaardrekening, die wordt voorgesteld in de journalen.</span><span class="sxs-lookup"><span data-stu-id="70710-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="70710-112">Deze kan in het journaal worden gewijzigd naar een andere rekening uit het rekeningschema of naar een leveranciersrekening, als het vaste activum van een leverancier is gekocht.</span><span class="sxs-lookup"><span data-stu-id="70710-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="70710-113">Als Factuurjournaal of Inkooporders in Leveranciers worden gebruikt voor de verwerving van vaste activa, wordt de tegenrekening voor de vaste-activatransactie vervangen door de leveranciersrekening die voor de transactie is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="70710-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="70710-114">Voor verwervingen die zijn geboekt met het Voorraad naar vaste-activajournaal in het grootboek, is het vaste activum niet gekocht van externe bronnen, maar overgebracht uit de eigen voorraad van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="70710-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="70710-115">Daarom is de tegenrekening een voorraaduitgifterekening voor het voorraadartikel in Voorraadbeheer.</span><span class="sxs-lookup"><span data-stu-id="70710-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="70710-116">Zie voor meer informatie [Verwerving van activa via inkoop](acquire-assets-procurement.md).</span><span class="sxs-lookup"><span data-stu-id="70710-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]