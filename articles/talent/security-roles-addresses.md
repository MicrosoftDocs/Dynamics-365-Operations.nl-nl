---
title: Toegang tot privéadressen per beveiligingsrol
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij een klant geen toegang tot privéadressen krijgt.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 58f3322ad64f7de07e17d193ff665bd6536a4070
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897092"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="22df9-103">Toegang tot privéadressen per beveiligingsrol</span><span class="sxs-lookup"><span data-stu-id="22df9-103">Access to private addresses by security role</span></span>

<span data-ttu-id="22df9-104">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="22df9-104">**Issue**</span></span>

<span data-ttu-id="22df9-105">Als een klant een beveiligingsrol dupliceert en zich aanmeldt als die nieuwe rol, zijn de als privé gemarkeerde adressen niet zichtbaar voor de klant.</span><span class="sxs-lookup"><span data-stu-id="22df9-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="22df9-106">**Resolutie**</span><span class="sxs-lookup"><span data-stu-id="22df9-106">**Resolution**</span></span>

<span data-ttu-id="22df9-107">Om het probleem op te lossen, moet de klant deze stappen uitvoeren voor de gedupliceerde beveiligingsrol.</span><span class="sxs-lookup"><span data-stu-id="22df9-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="22df9-108">Ga naar **Organisatiebeheer \> Globaal adresboek \> Parameters van globaal adresboek**.</span><span class="sxs-lookup"><span data-stu-id="22df9-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="22df9-109">Verplaats de nieuwe beveiligingsrol op het tabblad **Beveiliging privé-locatie** van de lijst **Beschikbare rollen** naar de lijst **Geselecteerde rollen**.</span><span class="sxs-lookup"><span data-stu-id="22df9-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="22df9-110">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="22df9-110">Select **Save**.</span></span>

![De pagina Parameters van globaal adresboek](media/GAD-parameters.png)
