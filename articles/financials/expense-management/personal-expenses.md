---
title: Persoonlijke onkosten in een onkostennota
description: In dit onderwerp worden de twee methoden toegelicht voor het verwerken van de persoonlijke onkosten van een werknemer in Microsoft Dynamics 365 for Finance and Operations.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e21605dbe9d4f8182b868183e33a12e9b7e62422
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="3945a-103">Persoonlijke onkosten in een onkostennota</span><span class="sxs-lookup"><span data-stu-id="3945a-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3945a-104">Tijdens zakenreizen kan het voorkomen dat werknemers persoonlijke uitgaven afrekenen met een creditcard van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="3945a-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="3945a-105">Als u geen proces voor het verwerken van persoonlijke onkosten definieert, kan het goedkeuringsproces voor onkostennota's worden verstoord wanneer de werknemers de gespecificeerde onkostennota's indienen.</span><span class="sxs-lookup"><span data-stu-id="3945a-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="3945a-106">In Microsoft Dynamics 365 for Finance and Operations zijn er twee methoden voor het verwerken van de persoonlijke onkosten van een werknemer:</span><span class="sxs-lookup"><span data-stu-id="3945a-106">In Microsoft Dynamics 365 for Finance and Operations, there are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="3945a-107">**Door werknemer betaald**: de persoonlijke onkosten op de rekening van de creditcard van het bedrijf worden niet door de organisatie betaald.</span><span class="sxs-lookup"><span data-stu-id="3945a-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="3945a-108">Er wordt een rapport gemaakt met zowel de persoonlijke onkosten als de bedrijfsonkosten die zijn betaald met de creditcard van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="3945a-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="3945a-109">**Door bedrijf betaald**: uw bedrijf betaalt de hele rekening van de creditcard van het bedrijf en schrijft de persoonlijke onkosten vervolgens af van de rekening van de werknemer.</span><span class="sxs-lookup"><span data-stu-id="3945a-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="3945a-110">Selecteer de methode voor uw organisatie op de pagina **Parameters onkostenbeheer**.</span><span class="sxs-lookup"><span data-stu-id="3945a-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>

