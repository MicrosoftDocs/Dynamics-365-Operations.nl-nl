---
title: Er treedt een fout op wanneer de locatie wordt geselecteerd tijdens de registratie van de orderverzamellijst
description: Er treedt een fout op wanneer de locatie wordt geselecteerd tijdens de registratie van de orderverzamellijst.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: b7fc579821f9a80d94aea949fcc0301b9d8f6935
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026389"
---
# <a name="an-error-occurs-when-the-location-is-selected-during-picking-list-registration"></a><span data-ttu-id="b92c4-103">Er treedt een fout op wanneer de locatie wordt geselecteerd tijdens de registratie van de orderverzamellijst</span><span class="sxs-lookup"><span data-stu-id="b92c4-103">An error occurs when the location is selected during picking list registration</span></span>

<span data-ttu-id="b92c4-104">KB-nummer: 4613106</span><span class="sxs-lookup"><span data-stu-id="b92c4-104">KB number: 4613106</span></span>

## <a name="symptoms"></a><span data-ttu-id="b92c4-105">Symptomen</span><span class="sxs-lookup"><span data-stu-id="b92c4-105">Symptoms</span></span>

<span data-ttu-id="b92c4-106">Dit probleem treedt op wanneer uw systeem is geconfigureerd voor het automatisch reserveren van verkooporders.</span><span class="sxs-lookup"><span data-stu-id="b92c4-106">This issue occurs when your system is configured to automatically reserve sales orders.</span></span> <span data-ttu-id="b92c4-107">Als u de locatie voor een registratieregel van de orderverzamellijst probeert te selecteren, wordt het volgende foutbericht weergegeven wanneer u reserveringsprocessen van magazijnbeheer (WMS) gebruikt:</span><span class="sxs-lookup"><span data-stu-id="b92c4-107">If you try to select the location for a picking list registration line, you receive the following error message when you use warehouse management (WMS) reservation processes:</span></span>

> <span data-ttu-id="b92c4-108">Kan hoeveelheid niet bijwerken met nieuwe dimensies</span><span class="sxs-lookup"><span data-stu-id="b92c4-108">Can't update quantity with new dimensions</span></span>

<span data-ttu-id="b92c4-109">Dit probleem kan optreden omdat u niet voldoende voorhanden voorvoorraad op een opgegeven locatie hebt.</span><span class="sxs-lookup"><span data-stu-id="b92c4-109">This issue can occur because you don't have enough on-hand inventory at a specified location.</span></span>

## <a name="resolution"></a><span data-ttu-id="b92c4-110">Oplossing</span><span class="sxs-lookup"><span data-stu-id="b92c4-110">Resolution</span></span>

<span data-ttu-id="b92c4-111">Dit gedrag van het systeem is inherent aan het ontwerp.</span><span class="sxs-lookup"><span data-stu-id="b92c4-111">The system is behaving as designed.</span></span>

<span data-ttu-id="b92c4-112">In scenario's waarin u het reserveringsproces op magazijnniveau gebruikt, is het aan te raden om het handmatige reserveringsproces te gebruiken voor de orderverzamelregel, als de voorhanden voorraad niet op alle voorraaddimensieniveaus wordt gereserveerd en u niet over voldoende voorhanden voorraad op een bepaalde locatie beschikt.</span><span class="sxs-lookup"><span data-stu-id="b92c4-112">In scenarios where you use the warehouse-level reservation process, if the on-hand inventory won't be reserved on all inventory dimension levels, and you don't have enough on-hand inventory at a specified location, we recommend that you use the manual reservation process from the picking line.</span></span> <span data-ttu-id="b92c4-113">U kunt vervolgens de functie *Partij reserveren* gebruiken om de lagere reserveringen, zoals locatie, voor alle beschikbare voorhanden hoeveelheden te verdelen.</span><span class="sxs-lookup"><span data-stu-id="b92c4-113">You can then use the *Reserve lot* function to distribute the lower reservations, such as location, for all the available on-hand quantities.</span></span>
