---
title: Toeslagen voor een geproduceerd artikel weergeven
description: De constante kosten van een gefabriceerd artikel staan voor de instellingstijden van de bewerking en voor de componenten die een constante hoeveelheid of een constant uitvalbedrag hebben.
author: AndersGirke
manager: tfehr
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: f8d7fd7488630d9d24d5d7dc31ea39a10385a290
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235503"
---
# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="0b0b9-103">Toeslagen voor een geproduceerd artikel weergeven</span><span class="sxs-lookup"><span data-stu-id="0b0b9-103">Display charges for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b0b9-104">De constante kosten van een gefabriceerd artikel staan voor de instellingstijden van de bewerking en voor de componenten die een constante hoeveelheid of een constant uitvalbedrag hebben.</span><span class="sxs-lookup"><span data-stu-id="0b0b9-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="0b0b9-105">Het berekende bedrag van de toeslagen van een artikel kan met de eenheidskosten van het artikel worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0b0b9-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="0b0b9-106">De toeslagen worden soms echter als afzonderlijke velden weergegeven en zijn niet opgenomen in de eenheidskosten van het artikel.</span><span class="sxs-lookup"><span data-stu-id="0b0b9-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="0b0b9-107">Wanneer de toeslagen als afzonderlijke velden worden weergegeven, staat in één veld het totaalbedrag van de toeslagen en in een ander veld de kostprijsberekening van de partijgrootte waarmee het bedrag wordt afgeschreven.</span><span class="sxs-lookup"><span data-stu-id="0b0b9-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="0b0b9-108">De pagina Artikelprijs geeft bijvoorbeeld de toeslagen weer als twee afzonderlijke velden.</span><span class="sxs-lookup"><span data-stu-id="0b0b9-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="0b0b9-109">Op de pagina Volledig worden echter de totale kosten van het artikel per eenheid weergegeven en de afgeschreven kosten zijn in de eenheidskosten opgenomen.</span><span class="sxs-lookup"><span data-stu-id="0b0b9-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>

<span data-ttu-id="0b0b9-110">De toeslagen voor een gefabriceerd artikel worden voor de standaardkostendoelen altijd opgenomen in de eenheidskosten van het artikel.</span><span class="sxs-lookup"><span data-stu-id="0b0b9-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="0b0b9-111">Deze toeslagen kunnen eventueel worden opgenomen voor geplande kostendoelen.</span><span class="sxs-lookup"><span data-stu-id="0b0b9-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="0b0b9-112">Een beleid in de kostprijsberekeningsversie zorgt ervoor dat de toeslagen in de kosten van een gefabriceerd artikel worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="0b0b9-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="0b0b9-113">Wanneer u de kostenregistratie van een artikel activeert, worden de toeslagen voor de basiskostengegevens van het artikel bijgewerkt, zoals wordt weergegeven op de pagina Artikelprijs.</span><span class="sxs-lookup"><span data-stu-id="0b0b9-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="0b0b9-114">De toeslagen worden als twee afzonderlijke velden weergegeven en zijn niet opgenomen in de eenheidskosten van het artikel.</span><span class="sxs-lookup"><span data-stu-id="0b0b9-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="0b0b9-115">Bij elke activering worden de basiskostengegevens van het artikel bijgewerkt, zelfs als de activering verschillende locaties behelst.</span><span class="sxs-lookup"><span data-stu-id="0b0b9-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="0b0b9-116">Daarom dient u de basiskostengegevens als referentiegegevens beschouwen.</span><span class="sxs-lookup"><span data-stu-id="0b0b9-116">Therefore, you should view the base cost information as reference information.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]