---
title: Parameters voor verlof en verzuim configureren
description: Definieer Human resources-parameters voor verlof en verzuim in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2acb8502ebcab122a0a1ff21e9f5e23931026327
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008601"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="c8281-103">Parameters voor verlof en verzuim configureren</span><span class="sxs-lookup"><span data-stu-id="c8281-103">Configure leave and absence parameters</span></span>

<span data-ttu-id="c8281-104">Voordat u verlof- en verzuimplannen instelt in Dynamics 365 Human Resources, kunt u het beste de instellingen controleren voor alle verwante Human resources-parameters, waaronder:</span><span class="sxs-lookup"><span data-stu-id="c8281-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="c8281-105">Nummerreeks voor verlofaanvragen</span><span class="sxs-lookup"><span data-stu-id="c8281-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="c8281-106">FMLA-instellingen (Family and Medical Leave Act)</span><span class="sxs-lookup"><span data-stu-id="c8281-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="c8281-107">Selfservice-instellingen voor werknemers voor verlof- en verzuimaanvragen</span><span class="sxs-lookup"><span data-stu-id="c8281-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="c8281-108">Verlof- en verzuimparameters</span><span class="sxs-lookup"><span data-stu-id="c8281-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="c8281-109">Human resources-parameters weergeven en wijzigen</span><span class="sxs-lookup"><span data-stu-id="c8281-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="c8281-110">Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="c8281-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c8281-111">Selecteer onder **Instellen** de optie **Human resources-parameters**.</span><span class="sxs-lookup"><span data-stu-id="c8281-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="c8281-112">Controleer op het tabblad **Nummerreeksen** de optie **Nummerreekscode** voor **Verlofaanvraag-id** en wijzig deze indien nodig.</span><span class="sxs-lookup"><span data-stu-id="c8281-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="c8281-113">Deze instelling bepaalt de volgorde waarin id's voor verlofaanvragen automatisch worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="c8281-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="c8281-114">Controleer op het tabblad **FMLA** de FMLA instellingen en wijzig deze indien nodig.</span><span class="sxs-lookup"><span data-stu-id="c8281-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="c8281-115">Geef op het tabblad **Selfservice werknemer** aan of managers verlof- en verzuimaanvragen kunnen invoeren namens hun werknemers.</span><span class="sxs-lookup"><span data-stu-id="c8281-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

6. <span data-ttu-id="c8281-116">Controleer op het tabblad **Verlof en verzuim** de instellingen en wijzig deze indien nodig.</span><span class="sxs-lookup"><span data-stu-id="c8281-116">On the **Leave and absence** tab, verify the settings and change as necessary.</span></span>

7. <span data-ttu-id="c8281-117">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c8281-117">Select **Save**.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="c8281-118">Kalenderparameters configureren</span><span class="sxs-lookup"><span data-stu-id="c8281-118">Configure calendar parameters</span></span>

<span data-ttu-id="c8281-119">Als u de preview-functie voor het verlof- en verzuimkalenders hebt ingeschakeld, moet u extra parameters configureren.</span><span class="sxs-lookup"><span data-stu-id="c8281-119">If you have enabled the Leave and absence calendar preview feature, you need to configure additional parameters.</span></span> 

[!include [banner](includes/preview-feature-leave-absence.md)]

> [!NOTE]
> <span data-ttu-id="c8281-120">Voor de preview-versie van 3 februari 2020 zijn alleen **in behandeling zijnde verlofaanvragen** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="c8281-120">For the preview release on February 3, 2020, only **Pending leave requests** are enabled.</span></span>

1. <span data-ttu-id="c8281-121">Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.</span><span class="sxs-lookup"><span data-stu-id="c8281-121">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="c8281-122">Selecteer onder **Instellen** de optie **Human resources-parameters**.</span><span class="sxs-lookup"><span data-stu-id="c8281-122">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="c8281-123">Wijzig op het tabblad **Kalender** de kalenderinstellingen indien nodig.</span><span class="sxs-lookup"><span data-stu-id="c8281-123">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="c8281-124">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="c8281-124">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8281-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c8281-125">See also</span></span>

- [<span data-ttu-id="c8281-126">Overzicht van verlof en verzuim</span><span class="sxs-lookup"><span data-stu-id="c8281-126">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
