---
title: Journalen met enkel boekstuk en herwaarderingen van valuta upgraden
description: Sommige organisaties voeren journalen in met een enkel boekstuk dat meer dan één klant of leverancier bevat, waarbij ze ook het herwaarderingsproces voor vreemde valuta voor klanten of leveranciers uitvoeren. In dit onderwerp worden de stappen beschreven die deze organisaties moeten volgen wanneer ze een upgrade uitvoeren naar Microsoft Dynamics 365 for Operations, versie 1611.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7c06e54c5be8d0a410b9f15f2a89def3076b4638
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681019"
---
# <a name="upgrade-single-voucher-journals-and-currency-revaluations"></a><span data-ttu-id="f7558-104">Journalen met enkel boekstuk en herwaarderingen van valuta upgraden</span><span class="sxs-lookup"><span data-stu-id="f7558-104">Upgrade single-voucher journals and currency revaluations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7558-105">Sommige organisaties voeren journalen in met een enkel boekstuk dat meer dan één klant of leverancier bevat, waarbij ze ook het herwaarderingsproces voor vreemde valuta voor klanten of leveranciers uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="f7558-105">Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process.</span></span> <span data-ttu-id="f7558-106">In dit onderwerp worden de stappen beschreven die deze organisaties moeten volgen wanneer ze een upgrade uitvoeren naar Microsoft Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="f7558-106">This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

<span data-ttu-id="f7558-107">Voer deze stappen uit voor een upgrade naar Microsoft Dynamics 365 for Operations versie 1611.</span><span class="sxs-lookup"><span data-stu-id="f7558-107">Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.</span></span>

1.  <span data-ttu-id="f7558-108">Voordat u een upgrade naar Finance and Operations uitvoert, moet u de processen voor herwaardering van vreemde valuta uitvoeren voor klanten en leveranciers.</span><span class="sxs-lookup"><span data-stu-id="f7558-108">Before you upgrade to Finance and Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="f7558-109">Stel het veld **Methode** in op **Factuurdatum**.</span><span class="sxs-lookup"><span data-stu-id="f7558-109">Set the **Method** field to **Invoice date**.</span></span> <span data-ttu-id="f7558-110">Een herwaarderingstransactie wordt gemaakt waarin de laatste herwaardering van vreemde valuta wordt omgekeerd.</span><span class="sxs-lookup"><span data-stu-id="f7558-110">A revaluation transaction is created that reverses the last foreign currency revaluation.</span></span> <span data-ttu-id="f7558-111">Daarom worden de openstaande transacties gewaardeerd tegen hun oorspronkelijke boekhoudingsvaluta.</span><span class="sxs-lookup"><span data-stu-id="f7558-111">Therefore, the open transactions are valued at their original accounting currency.</span></span>
2.  <span data-ttu-id="f7558-112">Upgraden naar versie 1611.</span><span class="sxs-lookup"><span data-stu-id="f7558-112">Upgrade to version 1611.</span></span>
3.  <span data-ttu-id="f7558-113">Voer de herwaardering van vreemde valuta voor zowel Leveranciers als Klanten opnieuw uit.</span><span class="sxs-lookup"><span data-stu-id="f7558-113">Run the Accounts receivable and Accounts payable foreign currency revaluation processes again.</span></span> <span data-ttu-id="f7558-114">Stel deze keer het veld **Methode** in op **Standaard**.</span><span class="sxs-lookup"><span data-stu-id="f7558-114">This time, set the **Method** field to **Standard**.</span></span> <span data-ttu-id="f7558-115">Een nieuwe herwaarderingstransactie wordt gemaakt op basis van de huidige wisselkoersen.</span><span class="sxs-lookup"><span data-stu-id="f7558-115">A new revaluation transaction is created that is based on the current exchange rates.</span></span> <span data-ttu-id="f7558-116">Deze transactie legt de niet-gerealiseerde winst/verlies vast en het juiste bedrag in het totaalgrootboek.</span><span class="sxs-lookup"><span data-stu-id="f7558-116">This transaction records the unrealized gain/loss and the correct summary ledger account.</span></span>
