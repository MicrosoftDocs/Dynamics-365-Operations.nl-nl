---
title: Nummerreeks voor Transportbeheer
description: In dit onderwerp wordt beschreven hoe u nummerreeksen voor transportbeheer kunt instellen.
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
ms.openlocfilehash: cc19110f481c11ab28532d69a4689c1db048f6c3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233362"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="7e4c8-103">Nummerreeks voor Transportbeheer</span><span class="sxs-lookup"><span data-stu-id="7e4c8-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e4c8-104">Gebruik de pagina **Nummerreeksen** in de module Transportbeheer om verschillende Pro-nummers in te stellen.</span><span class="sxs-lookup"><span data-stu-id="7e4c8-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="7e4c8-105">Pro-nummers worden door vervoerders gebruikt om de voortgang van elke zending te organiseren en te volgen.</span><span class="sxs-lookup"><span data-stu-id="7e4c8-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="7e4c8-106">Een nummerreeks maken voor een Pro-nummer</span><span class="sxs-lookup"><span data-stu-id="7e4c8-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="7e4c8-107">Ga als volgt te werk om een nummerreeks voor een Pro-nummer te maken:</span><span class="sxs-lookup"><span data-stu-id="7e4c8-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="7e4c8-108">Ga naar **Transportbeheer \> Instellingen \> Vervoerders \> Nummerreeksen**.</span><span class="sxs-lookup"><span data-stu-id="7e4c8-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="7e4c8-109">Selecteer **Nieuw** om een nieuwe nummerreeks te maken.</span><span class="sxs-lookup"><span data-stu-id="7e4c8-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="7e4c8-110">Voer een unieke id en een omschrijvende naam in voor de nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="7e4c8-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="7e4c8-111">In het veld **Type nummerreeks** is *Pro-nummer* de enige optie.</span><span class="sxs-lookup"><span data-stu-id="7e4c8-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="7e4c8-112">In het veld **Controlecijfer** is *Controlecijfer* de enige optie en deze wordt ingesteld als een algemene engine.</span><span class="sxs-lookup"><span data-stu-id="7e4c8-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="7e4c8-113">Geef op het sneltabblad **Reeks** informatie over de reeks op.</span><span class="sxs-lookup"><span data-stu-id="7e4c8-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="7e4c8-114">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7e4c8-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="7e4c8-115">Een nummerreeks aan een vervoerder koppelen</span><span class="sxs-lookup"><span data-stu-id="7e4c8-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="7e4c8-116">Ga als volgt te werk om een nummerreeks aan een vervoerder te koppelen:</span><span class="sxs-lookup"><span data-stu-id="7e4c8-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="7e4c8-117">Ga naar **Transportbeheer \> Instellingen \> Vervoerders \> Vervoerders**.</span><span class="sxs-lookup"><span data-stu-id="7e4c8-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="7e4c8-118">Selecteer een vervoerder.</span><span class="sxs-lookup"><span data-stu-id="7e4c8-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="7e4c8-119">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="7e4c8-119">Select **Edit**.</span></span>
1. <span data-ttu-id="7e4c8-120">Selecteer op het sneltabblad **Overzicht** een optie in het veld **Pro-nummerreeks**.</span><span class="sxs-lookup"><span data-stu-id="7e4c8-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="7e4c8-121">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="7e4c8-121">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]