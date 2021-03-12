---
title: Diverse toeslagen voor Transportbeheer
description: In dit onderwerp wordt uitgelegd hoe door transport veroorzaakte toeslagen moeten worden gekoppeld aan een toeslagcode.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: cb503072fb76e04aa01ff2d231c756eeb244c65a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004696"
---
# <a name="transportation-management-miscellaneous-charges"></a><span data-ttu-id="43444-103">Diverse toeslagen voor Transportbeheer</span><span class="sxs-lookup"><span data-stu-id="43444-103">Transportation management miscellaneous charges</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43444-104">Zoals met alle diverse toeslagen, moeten door transport veroorzaakte toeslagen worden gekoppeld aan een toeslagcode.</span><span class="sxs-lookup"><span data-stu-id="43444-104">As with all miscellaneous charges, transportation-generated charges must be associated with a charge code.</span></span> <span data-ttu-id="43444-105">Anders worden deze niet weer als divers toeslagbedrag aan de order toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="43444-105">Otherwise, they won't be added back to the order as a miscellaneous charge.</span></span> <span data-ttu-id="43444-106">De **toeslagcode** bepaalt hoe de toeslag wordt verwerkt in relatie tot de order en orderregel waaraan de toeslag wordt toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="43444-106">The **Charges code** determines how the charge is accounted for in relation to the order and order line where it is added.</span></span>

<span data-ttu-id="43444-107">Ga naar **Transportbeheer > Instellingen > Beoordeling > Diverse toeslagen** om de kwalificatiecriteria te definiëren die bepalen wanneer een specifieke **toeslagcode** op een toeslag wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="43444-107">Go to **Transportation management > Setup > Rating > Miscellaneous charges** to define the qualifying criteria that determine when a specific **Charges code** is applied to a charge.</span></span>

<span data-ttu-id="43444-108">U moet minimaal één instellen voor elke relevante **Toeslagmodule**-instelling (*Klant* en *Leverancier*) waarvoor **Type diverse toeslagen** is ingesteld op *Geen*.</span><span class="sxs-lookup"><span data-stu-id="43444-108">You should have at least one setup for each relevant **Charges module** setting (*Customer* and *Vendor*) where the **Miscellaneous charge type** is set to *None*.</span></span> <span data-ttu-id="43444-109">Als deze ontbreekt, worden het diverse toeslagbedag *niet* aan de order toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="43444-109">If this is missing, the miscellaneous charge will *not* be added to the order.</span></span>
