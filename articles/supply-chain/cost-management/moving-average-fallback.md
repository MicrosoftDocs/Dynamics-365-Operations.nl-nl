---
title: Terugvalkostenreeks met zwevend gemiddelde
description: Dit onderwerp bevat informatie over terugvalkostenreeksen voor berekeningen met zwevend gemiddelde in Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
manager: tfehr
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 0538701588b9c71dff4c538711606913a359de6a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425630"
---
# <a name="moving-average-fallback-cost-sequence"></a><span data-ttu-id="bd61b-103">Terugvalkostenreeks met zwevend gemiddelde</span><span class="sxs-lookup"><span data-stu-id="bd61b-103">Moving average fallback cost sequence</span></span>

<span data-ttu-id="bd61b-104">Eén manier waarop u de voorraadkosten kunt berekenen, is door een _zwevend gemiddelde_ te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="bd61b-104">One way that you can calculate the cost of your inventory is by using a _moving average_.</span></span> <span data-ttu-id="bd61b-105">U kunt maximaal drie kostenwaarden koppelen aan elk voorraadartikel:</span><span class="sxs-lookup"><span data-stu-id="bd61b-105">Up to three cost values can be associated with each inventory item:</span></span>

- <span data-ttu-id="bd61b-106">**Laatste uitgifte**: de laatste uitgiftekosten die zijn toegewezen voordat de voorraad negatief werd</span><span class="sxs-lookup"><span data-stu-id="bd61b-106">**Last issue** – The last issue cost that was assigned before inventory went negative</span></span>
- <span data-ttu-id="bd61b-107">**Actieve kosten**: de laatste kosten die in een kostprijsberekeningsversie zijn geactiveerd</span><span class="sxs-lookup"><span data-stu-id="bd61b-107">**Active cost** – The latest cost that was activated in a costing version</span></span>
- <span data-ttu-id="bd61b-108">**Artikelprijs**: de kosten die zijn opgegeven voor het vrijgegeven product</span><span class="sxs-lookup"><span data-stu-id="bd61b-108">**Item price** – The cost that is specified for the released product</span></span>

<span data-ttu-id="bd61b-109">Om te bepalen welke van deze kostenwaarden moet worden gebruikt bij berekeningen van het zwevend gemiddelde, gebruikt het systeem een _terugvalkostenreeks_ om de voorkeursvolgorde voor de waarden in te stellen.</span><span class="sxs-lookup"><span data-stu-id="bd61b-109">To determine which of these cost values should be used in moving average calculations, the system uses a _fallback cost sequence_ to establish the order of preference for the values.</span></span> <span data-ttu-id="bd61b-110">Als de gewenste kostenwaarde niet beschikbaar is, wordt de volgende voorkeurswaarde van het systeem gebruikt, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="bd61b-110">If the preferred cost value isn't available, the system uses the next-preferred value, and so on.</span></span>

<span data-ttu-id="bd61b-111">In eerdere versies van Microsoft Dynamics 365 Supply Chain Management heeft het systeem een vaste terugvalkostenreeks gebruikt (_Laatste uitgifte – Actieve kosten – Artikelprijs_).</span><span class="sxs-lookup"><span data-stu-id="bd61b-111">In previous versions of Microsoft Dynamics 365 Supply Chain Management, the system used a fixed fallback cost sequence (_Last issue – Active cost – Item price_).</span></span> <span data-ttu-id="bd61b-112">In versie 10.0.11 is dit nog steeds de standaardvolgorde.</span><span class="sxs-lookup"><span data-stu-id="bd61b-112">In version 10.0.11, this sequence is still the default sequence.</span></span> <span data-ttu-id="bd61b-113">U kunt echter ook een functie inschakelen waarmee u kunt kiezen uit drie beschikbare terugvalkostencombinaties.</span><span class="sxs-lookup"><span data-stu-id="bd61b-113">However, you can also turn on a feature that lets you select among three available fallback cost sequences.</span></span> <span data-ttu-id="bd61b-114">Deze functie kan vooral nuttig zijn voor organisaties die regelmatig negatieve voorraadwaarden gebruiken.</span><span class="sxs-lookup"><span data-stu-id="bd61b-114">This feature can be especially useful for organizations that regularly use negative inventory values.</span></span>

<span data-ttu-id="bd61b-115">Als u de selector voor de terugvalkostenreeks beschikbaar wilt maken, moet u (of een beheerder) [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) gebruiken om de functie _Terugvalkostenreeks met zwevend gemiddelde_ te activeren.</span><span class="sxs-lookup"><span data-stu-id="bd61b-115">To make the selector for the fallback cost sequence available, you (or an admin) must use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named _Moving average fallback cost sequence_.</span></span>

<span data-ttu-id="bd61b-116">Ga als volgt te werk om de terugvalkostenreeks voor de berekening van het zwevende gemiddelde te selecteren.</span><span class="sxs-lookup"><span data-stu-id="bd61b-116">To select the fallback cost sequence for moving average calculations, follow these steps.</span></span>

1. <span data-ttu-id="bd61b-117">De pagina **Parameters** openen.</span><span class="sxs-lookup"><span data-stu-id="bd61b-117">Open the **Parameters** page.</span></span>
2. <span data-ttu-id="bd61b-118">Stel op het tabblad **Voorraadboekhouding** in het gedeelte **Zwevend gemiddelde** het veld **Terugvalkostenreeks** in op een van de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="bd61b-118">On the **Inventory accounting** tab, in the **Moving average** section, set the **Fallback cost sequence** field to one of the following values:</span></span>

    - <span data-ttu-id="bd61b-119">**Laatste uitgifte – Actieve kosten – Artikelprijs**: deze volgorde is de standaardvolgorde.</span><span class="sxs-lookup"><span data-stu-id="bd61b-119">**Last issue – Active cost – Item price** – This sequence is the default sequence.</span></span> <span data-ttu-id="bd61b-120">Dit is de dezelfde reeks die wordt gebruikt als de functie _Terugvalkostenreeks met zwevend gemiddelde_ niet is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="bd61b-120">It's the same sequence that is used if the _Moving average fallback cost sequence_ feature isn't turned on.</span></span>
    - <span data-ttu-id="bd61b-121">**Actieve kosten - laatste uitgifte**</span><span class="sxs-lookup"><span data-stu-id="bd61b-121">**Active cost – Last issue**</span></span>
    - <span data-ttu-id="bd61b-122">**Actieve kosten – Artikelprijs**: organisaties kunnen prestatieproblemen ondervinden als ze bedrijfsprocessen gebruiken waarbij de voorraadregel negatief wordt en tegelijkertijd het transactievolume hoog is.</span><span class="sxs-lookup"><span data-stu-id="bd61b-122">**Active cost – Item price** – Organizations might experience performance issues if they use business processes where inventory regularly goes negative and, at the same time, the transaction volume is high.</span></span> <span data-ttu-id="bd61b-123">Met deze instelling beperken ze de prestatieproblemen.</span><span class="sxs-lookup"><span data-stu-id="bd61b-123">This setting can help mitigate those performance issues.</span></span>

<span data-ttu-id="bd61b-124">![Parameters voorraadboekhouding](media/inventory-accounting-parameters.png "Parameters voorraadboekhouding")</span><span class="sxs-lookup"><span data-stu-id="bd61b-124">![Inventory accounting parameters](media/inventory-accounting-parameters.png "Inventory accounting parameters")</span></span>
