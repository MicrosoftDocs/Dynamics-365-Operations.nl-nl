---
title: Serviceorderfasen instellen
description: Stel serviceorderfasen in.
author: ShylaThompson
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30f6a6afa6ab91bed41bb19b8312dc7e25bd2478
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551714"
---
# <a name="set-up-service-order-stages"></a><span data-ttu-id="4221c-103">Serviceorderfasen instellen</span><span class="sxs-lookup"><span data-stu-id="4221c-103">Set up service order stages</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="4221c-104">Klik op **Servicebeheer** \> **Instellen** \> **Serviceorders** \> **Servicefasen**.</span><span class="sxs-lookup"><span data-stu-id="4221c-104">Click **Service management** \> **Setup** \> **Service orders** \> **Service stages**.</span></span>

2.  <span data-ttu-id="4221c-105">Druk op Ctrl+N om een nieuwe record te maken.</span><span class="sxs-lookup"><span data-stu-id="4221c-105">Press CTRL+N to create a new record.</span></span>

3.  <span data-ttu-id="4221c-106">Geef in de velden **Servicefase** en **Beschrijving** een servicefase-ID en omschrijving op.</span><span class="sxs-lookup"><span data-stu-id="4221c-106">In the **Service stage** and **Description** fields, specify a service stage ID and description.</span></span>

4.  <span data-ttu-id="4221c-107">Selecteer de juiste parameters voor de fase.</span><span class="sxs-lookup"><span data-stu-id="4221c-107">Select the appropriate parameters for the stage.</span></span>

5.  <span data-ttu-id="4221c-108">Selecteer de bovenliggende fase voor de huidige fase of laat het veld **Bovenliggend** leeg als het gaat om de initiële fase in de fase-instellingen.</span><span class="sxs-lookup"><span data-stu-id="4221c-108">Select the parent stage for the current stage or leave the **Parent** field blank if the stage is the initial stage in the stage setup.</span></span>


> [!NOTE]
> <P><span data-ttu-id="4221c-109">U kunt het veld <STRONG>Bovenliggend</STRONG> niet meer wijzigen nadat u de fase hebt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="4221c-109">You cannot modify the <STRONG>Parent</STRONG> field after you save the stage.</span></span> <span data-ttu-id="4221c-110">In plaats daarvan kunt u de record verwijderen en de record opnieuw maken waarbij u een andere waarde selecteert in het veld <STRONG>Bovenliggend</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="4221c-110">Instead, you can delete the record and create the record again with a different selection in the <STRONG>Parent</STRONG> field.</span></span></P>
> <P><span data-ttu-id="4221c-111">Bovendien kunt u slechts één fase maken met een leeg veld <STRONG>Bovenliggend</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="4221c-111">Also, you can only create one stage with a blank <STRONG>Parent</STRONG> field.</span></span> <span data-ttu-id="4221c-112">Er is met andere woorden slechts één initiële fase toegestaan.</span><span class="sxs-lookup"><span data-stu-id="4221c-112">That is, only one initial stage is permitted.</span></span></P>


  


