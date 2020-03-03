---
title: Leveringsmethoden voor niet-vervoerders verbergen in de verzendopties in POS
description: In dit onderwerp wordt een configuratieoptie beschreven waarmee u kunt voorkomen dat leveringsmethoden voor niet-vervoerders worden weergegeven voor selectie wanneer verzendorders worden gemaakt in de POS-toepassing.
author: hhainesms
manager: annbe
ms.date: 10/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: hhainesms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 75e7e8f183982f7829db78eb75b8c29c9ab95e89
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022199"
---
# <a name="hide-non-carrier-delivery-modes-from-the-shipping-options-in-pos"></a><span data-ttu-id="ce4a1-103">Leveringsmethoden voor niet-vervoerders verbergen in de verzendopties in POS</span><span class="sxs-lookup"><span data-stu-id="ce4a1-103">Hide non-carrier delivery modes from the shipping options in POS</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ce4a1-104">In dit onderwerp wordt een configuratieoptie beschreven die beschikbaar is voor de POS-toepassing.</span><span class="sxs-lookup"><span data-stu-id="ce4a1-104">This topic describes a configuration option that is available for the point of sale (POS) application.</span></span> <span data-ttu-id="ce4a1-105">Met deze configuratieoptie wijzigt u het gedrag voor de selectie van leveringsmethoden wanneer verzendorders worden gemaakt in POS.</span><span class="sxs-lookup"><span data-stu-id="ce4a1-105">This configuration option changes the behavior for the selection of a mode of delivery when shipment orders are created in POS.</span></span>

<span data-ttu-id="ce4a1-106">Wanneer gebruikers verzendorders voor een klant maken in POS, kunnen ze een leveringsmethode selecteren voor de zending.</span><span class="sxs-lookup"><span data-stu-id="ce4a1-106">When users create customer shipment orders in POS, they can select a mode of delivery for the shipment.</span></span> <span data-ttu-id="ce4a1-107">Deze functionaliteit is beschikbaar ongeacht of de gehele order wordt verzonden of alleen geselecteerde regels.</span><span class="sxs-lookup"><span data-stu-id="ce4a1-107">This functionality is available regardless of whether the whole order is being shipped or only selected lines.</span></span>

<span data-ttu-id="ce4a1-108">Standaard worden in het dialoogvenster waarin een leveringsmethode wordt geselecteerd, alle geldige leveringsmethoden weergegeven voor de combinatie van kanaal, artikel en afleveradres.</span><span class="sxs-lookup"><span data-stu-id="ce4a1-108">By default, the dialog box where a mode of delivery is selected shows all the valid modes of delivery for the combination of a channel, an item, and a delivery address.</span></span> <span data-ttu-id="ce4a1-109">Deze leveringsmethoden worden gedefinieerd op de pagina **Leveringsmethoden** in Headquarters (**Verkoop en marketing \> Instellingen \> Distributie \> Leveringsmethoden**).</span><span class="sxs-lookup"><span data-stu-id="ce4a1-109">These modes of delivery are defined on the **Modes of delivery** page in Headquarters (**Sales and marketing \> Setup \> Distribution \> Modes of delivery**).</span></span> <span data-ttu-id="ce4a1-110">De leveringsmethoden "niet-vervoerders", zoals **Uitvoeren** of **Ophalen**, kunnen ook worden weergegeven voor selectie in het dialoogvenster.</span><span class="sxs-lookup"><span data-stu-id="ce4a1-110">"Non-carrier" modes of delivery, such as **Carryout** or **Pickup**, might also appear for selection in the dialog box.</span></span>

<span data-ttu-id="ce4a1-111">Er is echter een functie toegevoegd waarmee u de leveringsmethoden voor niet-vervoerders kunt verbergen in het dialoogvenster.</span><span class="sxs-lookup"><span data-stu-id="ce4a1-111">However, a feature has been added that lets you hide non-carrier modes of delivery in the dialog box.</span></span> <span data-ttu-id="ce4a1-112">Als u deze functie wilt inschakelen, stelt u op de pagina **Commerce-parameters** op het tabblad **Klantorders** de optie **Alleen opties voor vervoerdersmethoden weergeven voor verzendorders** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="ce4a1-112">To turn on this feature, on the **Commerce parameters** page, on the **Customer orders** tab, set the **Show only carrier mode options for ship orders** option to **Yes**.</span></span> <span data-ttu-id="ce4a1-113">Nadat u deze functie hebt ingeschakeld en de desbetreffende distributietaken hebt uitgevoerd om de informatie te synchroniseren met de kanaaldatabase, worden de leveringsmethoden voor niet-vervoerders niet weergegeven voor selectie tijdens het maken van verzendorders in POS.</span><span class="sxs-lookup"><span data-stu-id="ce4a1-113">After you turn on this feature and run the appropriate distribution jobs to sync the information to the channel database, non-carrier modes of delivery won't appear for selection during the process of creating shipment orders in POS.</span></span>