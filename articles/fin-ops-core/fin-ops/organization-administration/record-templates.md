---
title: Overzicht van Recordsjablonen
description: Dit artikel introduceert het concept van recordsjablonen en legt uit hoe deze kunnen worden gebruikt om records te maken waarmee informatie wordt gedeeld.
author: pvillads
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a8f924a5c2dad45d2006240230b85592d56e676
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177249"
---
# <a name="record-templates-overview"></a><span data-ttu-id="9c857-103">Overzicht van Recordsjablonen</span><span class="sxs-lookup"><span data-stu-id="9c857-103">Record templates overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c857-104">Dit artikel introduceert het concept van recordsjablonen en legt uit hoe deze kunnen worden gebruikt om records te maken waarmee informatie wordt gedeeld.</span><span class="sxs-lookup"><span data-stu-id="9c857-104">This article introduces the concept of record templates and explains how they can be used to create records that share information.</span></span>

<span data-ttu-id="9c857-105">Recordsjablonen kunnen u helpen om sneller records te maken, maar u kunt echter alleen voor sommige recordtypen recordsjablonen maken.</span><span class="sxs-lookup"><span data-stu-id="9c857-105">Record templates can help you to create records more quickly, however you can only create record templates for some record types.</span></span>

<span data-ttu-id="9c857-106">Bijvoorbeeld, stel u voor dat u huurinformatie invoert voor een autoverhuurbedrijf die gevestigd is in San Francisco.</span><span class="sxs-lookup"><span data-stu-id="9c857-106">For example, imagine you are entering rental information for a car rental business that is located in San Francisco.</span></span> <span data-ttu-id="9c857-107">Aangezien de meeste klanten waarschijnlijk uit het gebied van San Francisco zijn, kan het prettig zijn als u de waarden voor de velden **Provincie** , **Land**  en **Plaats** automatisch kan vullen op het verhuurformulier.</span><span class="sxs-lookup"><span data-stu-id="9c857-107">Since most of the customers are likely to be from the San Francisco area, it would be nice if you could automatically fill in the values for the **State**, **Country**, and **City** fields on the rental form.</span></span>

> [!NOTE]
> <span data-ttu-id="9c857-108">U kunt alleen sjablonen toepassen op gedeelten waartoe u toegang hebt.</span><span class="sxs-lookup"><span data-stu-id="9c857-108">You can apply templates only in areas that you have access to.</span></span> <span data-ttu-id="9c857-109">Echter, alle sjabloontitels zijn voor u zichtbaar wanneer u een nieuw record aanmaakt en ook voor andere gebruikers, indien u sjablonen maakt die voor alle gebruikers beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="9c857-109">However all template titles are visible to you when you create a new record, and to other users as well, if you are creating templates that will be available for all users.</span></span> <span data-ttu-id="9c857-110">Neem dit in overweging wanneer u sjablonen benoemt.</span><span class="sxs-lookup"><span data-stu-id="9c857-110">Be sure to consider this when naming templates.</span></span> <span data-ttu-id="9c857-111">Vermijd bijvoorbeeld namen met woorden als 'commissie' indien het vertrouwelijk is dat bepaalde werknemers in het bedrijf een salaris hebben dat is gebaseerd op commissie.</span><span class="sxs-lookup"><span data-stu-id="9c857-111">For example, avoid using names that include words, such as "commission," if is confidential that some employees in the company have commission-based salaries.</span></span>

<span data-ttu-id="9c857-112">Wanneer er een of meerdere sjablonen waartoe u toegang hebt bestaan voor een specifiek formulier en u een nieuwe registratie in het formulier probeert te maken, wordt het formulier **Een sjabloon selecteren voor...** weergegeven.</span><span class="sxs-lookup"><span data-stu-id="9c857-112">When one or more templates that you have access to exist for a specific form and you attempt to create a new record in the form, the **Select a template for** page is displayed.</span></span> <span data-ttu-id="9c857-113">Wanneer u een sjabloon uit de lijst selecteert, wordt de nieuwe registratie gemaakt en deze bevat standaardinformatie die gebaseerd is op het door u geselecteerde sjabloon.</span><span class="sxs-lookup"><span data-stu-id="9c857-113">When you select a template from the list, the new record is created and contains default information that is based on the template that you selected.</span></span> <span data-ttu-id="9c857-114">Schakel het selectievakje **De vraag niet meer stellen** in het formulier **Een sjabloon selecteren voor...** in als u bij het maken van nieuwe registraties geen sjabloon wilt gebruiken.</span><span class="sxs-lookup"><span data-stu-id="9c857-114">If you do not want to use templates when you create new records, select the **Do not ask again** check box in the **Select a template for** page.</span></span> <span data-ttu-id="9c857-115">Wilt u dit dialoogvenster opnieuw weergeven, dan klikt u met de rechtermuisknop op een record, klikt u op **Recordinfo** en vervolgens op **Sjabloonselectie weergeven**.</span><span class="sxs-lookup"><span data-stu-id="9c857-115">To display the template selection dialog box again, right-click any record, click **Record info**, and then click **Show template selection**.</span></span>