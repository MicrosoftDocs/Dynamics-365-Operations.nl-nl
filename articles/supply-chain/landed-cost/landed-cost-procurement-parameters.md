---
title: Parameters voor inkoopbeheer voor Francoprijzen
description: In dit onderwerp wordt beschreven hoe u de relevante parameters voor inkoopbeheer kunt instellen wanneer u de module Francoprijzen gebruikt.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: df91fcb97794be32924707fcecf2b5fb34844596
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833924"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="7294a-103">Parameters voor inkoopbeheer voor Francoprijzen</span><span class="sxs-lookup"><span data-stu-id="7294a-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7294a-104">Op de pagina **Parameters voor inkoopbeheer** zijn een paar instellingen beschikbaar die met name relevant zijn wanneer u de module **Francoprijzen** gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7294a-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="7294a-105">Gebruik het dialoogvenster **Orderregels bijwerken**, dat u kunt openen vanaf de pagina **Parameters voor inkoopbeheer**, om op te geven of inkooporderregels automatisch moeten worden bijgewerkt wanneer er wijzigingen worden aangebracht in de header van de inkooporder.</span><span class="sxs-lookup"><span data-stu-id="7294a-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="7294a-106">Volg deze stappen om de instellingen te voltooien.</span><span class="sxs-lookup"><span data-stu-id="7294a-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="7294a-107">Ga naar **Inkoop en sourcing \> Instellen \> Parameters voor Inkoopbeheer**.</span><span class="sxs-lookup"><span data-stu-id="7294a-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="7294a-108">Selecteer op het tabblad **Algemeen** de koppeling **Orderregels bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="7294a-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="7294a-109">In het dialoogvenster **Orderregels bijwerken** worden de velden in de orderkop weergegeven waarmee ook automatische updates kunnen worden toegepast op gerelateerde velden in de orderregels.</span><span class="sxs-lookup"><span data-stu-id="7294a-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="7294a-110">Stel elk veld in de lijst in op een van de volgende waarden:</span><span class="sxs-lookup"><span data-stu-id="7294a-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="7294a-111">**Altijd**: de orderregels worden automatisch bijgewerkt wanneer de orderheader wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="7294a-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="7294a-112">**Nooit**: de orderregels worden nooit bijgewerkt wanneer de orderheader wordt bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="7294a-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="7294a-113">**Vragen**: de gebruiker wordt gevraagd of de orderregels moeten worden bijgewerkt of niet.</span><span class="sxs-lookup"><span data-stu-id="7294a-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
