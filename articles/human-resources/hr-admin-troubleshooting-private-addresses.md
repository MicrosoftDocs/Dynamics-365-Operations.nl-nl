---
title: Toegang tot privéadressen per beveiligingsrol
description: In dit artikel wordt uitgelegd hoe u het probleem oplost waarbij een klant geen toegang tot privéadressen krijgt.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: facfd17f007b2c9e6f068d0ec4c5ce45b85a1b78
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008642"
---
# <a name="access-to-private-addresses-by-security-role"></a><span data-ttu-id="ba1ab-103">Toegang tot privéadressen per beveiligingsrol</span><span class="sxs-lookup"><span data-stu-id="ba1ab-103">Access to private addresses by security role</span></span>

<span data-ttu-id="ba1ab-104">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="ba1ab-104">**Issue**</span></span>

<span data-ttu-id="ba1ab-105">Als een klant een beveiligingsrol dupliceert en zich aanmeldt als die nieuwe rol, zijn de als privé gemarkeerde adressen niet zichtbaar voor de klant.</span><span class="sxs-lookup"><span data-stu-id="ba1ab-105">After a customer duplicates a security role and signs in as that new role, the customer can't see addresses that were marked as private.</span></span>

<span data-ttu-id="ba1ab-106">**Resolutie**</span><span class="sxs-lookup"><span data-stu-id="ba1ab-106">**Resolution**</span></span>

<span data-ttu-id="ba1ab-107">Om het probleem op te lossen, moet de klant deze stappen uitvoeren voor de gedupliceerde beveiligingsrol.</span><span class="sxs-lookup"><span data-stu-id="ba1ab-107">To resolve the issue, the customer must follow these steps for the duplicated security role.</span></span>

1. <span data-ttu-id="ba1ab-108">Ga naar **Organisatiebeheer \> Globaal adresboek \> Parameters van globaal adresboek**.</span><span class="sxs-lookup"><span data-stu-id="ba1ab-108">Go to **Organization administration \> Global address book \> Global address book parameters**.</span></span>
2. <span data-ttu-id="ba1ab-109">Verplaats de nieuwe beveiligingsrol op het tabblad **Beveiliging privé-locatie** van de lijst **Beschikbare rollen** naar de lijst **Geselecteerde rollen**.</span><span class="sxs-lookup"><span data-stu-id="ba1ab-109">On the **Private location security** tab, move the new security role from the **Available roles** list to the **Selected roles** list.</span></span>
3. <span data-ttu-id="ba1ab-110">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ba1ab-110">Select **Save**.</span></span>

![De pagina Parameters van globaal adresboek](media/GAD-parameters.png)
