---
title: Uitvoeringsvolgorde voor de eerste sychronisatie van Finance and Operations en Common Data Service
description: In dit onderwerp wordt de synchronisatievolgorde aangegeven van die u moet volgen om de eerste gegevens te maken.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: b74bc2d3133af7e87663a4e6bafb8780e0a6a66f
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797293"
---
# <a name="execution-order-for-initial-sychronization-of-finance-and-operations-and-common-data-service"></a><span data-ttu-id="32289-103">Uitvoeringsvolgorde voor de eerste sychronisatie van Finance and Operations en Common Data Service</span><span class="sxs-lookup"><span data-stu-id="32289-103">Execution order for initial sychronization of Finance and Operations and Common Data Service</span></span>

<span data-ttu-id="32289-104">Voordat u gegevensintegratie gebruikt, moet u de eerste gegevens maken die vereist zijn voor klanten, leveranciers en contactpersonen.</span><span class="sxs-lookup"><span data-stu-id="32289-104">Before you use data integration, you must create the initial data required for customers, vendors and contacts.</span></span> <span data-ttu-id="32289-105">Als u bijvoorbeeld een nieuw **Leveranciergroep**-item wilt maken en de **betalingsvoorwaarden** wilt instellen op **Net30**, moet u er eerst voor zorgen dat **Net30** bestaat in Finance and Operations en Common Data Service voordat u probeert het **Leveranciergroep**-item te maken.</span><span class="sxs-lookup"><span data-stu-id="32289-105">For example, if you want to create a new **Vendor group** item and set its **Terms of Payment** as **Net30**, then before you attempt to create the **Vendor group** item you need to make sure that **Net30** exists in both Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="32289-106">(In de toekomst zullen we een in het platform Twee keer wegschrijven een functionaliteit met de naam **Initiële synchronisatie**uitbrengen om als onderdeel van de installatie van Twee keer wegschrijven een eenmalige gegevenssynchronisatie uit te voeren tussen Finance and Operations en Common Data Service.)</span><span class="sxs-lookup"><span data-stu-id="32289-106">(In the future, we will release a  dual-write platform functionality called **Initial Sync**. It will do a one-time data synchronization between Finance and Operations and Common Data Service as part of the dual-write setup.)</span></span>

<span data-ttu-id="32289-107">Tips: we geven een toewijzing voor Twee keer wegschrijven uit voor alle referentiegegevens, inclusief **Betalingsvoorwaarden** (betalingsvoorwaarden).</span><span class="sxs-lookup"><span data-stu-id="32289-107">Tips: We are releasing a dual-write map for all reference data including **Terms of Payment** (Payment Terms).</span></span> <span data-ttu-id="32289-108">Als u de initiële gegevens al in één systeem hebt, kan een kleine updatebewerking van een record Twee keer wegschrijven voor die record activeren.</span><span class="sxs-lookup"><span data-stu-id="32289-108">If you already have the initial data in one system, a small update operation on a record can trigger dual-write on that record.</span></span> 

<span data-ttu-id="32289-109">U moet de volgende prioriteitsvolgorde volgen en ervoor zorgen dat de eerste gegevens beschikbaar zijn op zowel Finance and Operations als Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="32289-109">You must follow the following order of precedence and make sure that the initial data is available on both Finance and Operations and Common Data Service.</span></span>   

## <a name="vendor"></a><span data-ttu-id="32289-110">Leverancier</span><span class="sxs-lookup"><span data-stu-id="32289-110">Vendor</span></span>

<span data-ttu-id="32289-111">De volgorde van uitvoering voor Leverancier is:</span><span class="sxs-lookup"><span data-stu-id="32289-111">The order of execution for Vendor is:</span></span>

```
Vendor Group
    Terms of payment
        Payment day & lines
        Payment schedule
Vendor payment method
```

## <a name="customer-organization"></a><span data-ttu-id="32289-112">Klant (organisatie)</span><span class="sxs-lookup"><span data-stu-id="32289-112">Customer (Organization)</span></span>

<span data-ttu-id="32289-113">De volgorde van uitvoering voor Klant is:</span><span class="sxs-lookup"><span data-stu-id="32289-113">The order of execution for Customer is:</span></span>

```
Customer Group
    Terms of payment
        Payment day & lines
        Payment 
Customer payment method
```

## <a name="contact-person"></a><span data-ttu-id="32289-114">Contactpersoon (persoon)</span><span class="sxs-lookup"><span data-stu-id="32289-114">Contact (Person)</span></span>

<span data-ttu-id="32289-115">De volgorde van uitvoering voor Contactpersoon is:</span><span class="sxs-lookup"><span data-stu-id="32289-115">The order of execution for Contact is:</span></span>

```
Customer
Vendor               
```
