---
title: Boekingsrekeningen voor afboeking van vaste activa
description: In dit onderwerp wordt beschreven hoe u grootboekboekingsrekeningen instelt voor het afboeken van activa.
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
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92b653d50744884d56c19601cff74c420eb1b397
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240965"
---
# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="7bbe7-103">Boekingsrekeningen voor afboeking van vaste activa</span><span class="sxs-lookup"><span data-stu-id="7bbe7-103">Fixed asset disposal posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bbe7-104">In dit onderwerp wordt beschreven hoe u grootboekboekingsrekeningen instelt voor het afboeken van activa.</span><span class="sxs-lookup"><span data-stu-id="7bbe7-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="7bbe7-105">Selecteer op de pagina Boekingsprofielen voor vaste activa, op het sneltabblad Grootboekrekeningen, de optie Verkoop/afstoting en Afstoting - uitval voor het instellen van boekingen naar het grootboek.</span><span class="sxs-lookup"><span data-stu-id="7bbe7-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="7bbe7-106">Voor beide transactietypen wordt de grootboekrekening gecrediteerd voor de afboekwaarde van het vaste activum.</span><span class="sxs-lookup"><span data-stu-id="7bbe7-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="7bbe7-107">Het debetbedrag wordt naar een tegenrekening geboekt, die bijvoorbeeld een bankrekening kan zijn.</span><span class="sxs-lookup"><span data-stu-id="7bbe7-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="7bbe7-108">Als een vast activum aan een klant wordt verkocht, wordt de klantrekening in plaats van de tegenrekening gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7bbe7-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="7bbe7-109">Klik op Afstoting en klik vervolgens op Verkoop of Uitval, en stel vervolgens gedetailleerde rekeningen in om de nettoboekwaarde van het vaste activum om te keren.</span><span class="sxs-lookup"><span data-stu-id="7bbe7-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="7bbe7-110">U kunt ook informatie invoeren in de velden Waarde boeken en Verkoopwaarde op de pagina Afstotingsparameters.</span><span class="sxs-lookup"><span data-stu-id="7bbe7-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="7bbe7-111">Door de afboekingstransactie voor een activum in een groep met lage waarden, wordt de nettoboekwaarde van de groep met lage waarden alleen verminderd met het afgeboekte bedrag.</span><span class="sxs-lookup"><span data-stu-id="7bbe7-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="7bbe7-112">Wanneer de verkoop van een activum echter de nettoboekwaarde van de groep met lage waarden overschrijdt, wordt de nettoboekwaarde verlaagd tot nul.</span><span class="sxs-lookup"><span data-stu-id="7bbe7-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]