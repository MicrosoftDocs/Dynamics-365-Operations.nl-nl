---
title: Voorwaardelijke beslissingen configureren in een workflow
description: Met behulp van de volgende procedure kunt u de eigenschappen van een voorwaardelijke beslissing configureren.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a593d4e188f47b73967f0c5468f7d7c3e9f64dc8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567455"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a><span data-ttu-id="11870-103">Voorwaardelijke beslissingen configureren in een workflow</span><span class="sxs-lookup"><span data-stu-id="11870-103">Configure conditional decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11870-104">Met behulp van de volgende procedure kunt u de eigenschappen van een voorwaardelijke beslissing configureren.</span><span class="sxs-lookup"><span data-stu-id="11870-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="11870-105">Een voorwaardelijke beslissing is een punt waarop een workflow in twee takken wordt verdeeld.</span><span class="sxs-lookup"><span data-stu-id="11870-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="11870-106">Om een voorwaardelijke beslissing te configureren, klikt u in de workfloweditor met de rechtermuisknop op de voorwaardelijke beslissing en klikt u vervolgens op **Eigenschappen** om het formulier **Eigenschappen** te openen.</span><span class="sxs-lookup"><span data-stu-id="11870-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="11870-107">Een naam geven aan een beslissing</span><span class="sxs-lookup"><span data-stu-id="11870-107">Name a decision</span></span>

<span data-ttu-id="11870-108">Voer deze stappen uit om een naam op te geven voor een voorwaardelijke beslissing.</span><span class="sxs-lookup"><span data-stu-id="11870-108">Follow these steps to enter a name for a conditional decision.</span></span>

1. <span data-ttu-id="11870-109">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="11870-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="11870-110">Voer in het veld **Naam** een unieke naam voor de voorwaardelijke beslissing in.</span><span class="sxs-lookup"><span data-stu-id="11870-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="11870-111"> Voorwaarden instellen</span><span class="sxs-lookup"><span data-stu-id="11870-111">Set conditions</span></span>

<span data-ttu-id="11870-112">Het systeem bepaalt welke tak wordt gebruikt om het aangeboden document te verwerken door te beoordelen of het document aan de specifieke voorwaarden voldoet.</span><span class="sxs-lookup"><span data-stu-id="11870-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>

1. <span data-ttu-id="11870-113">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="11870-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="11870-114">Klik op **Voorwaarde toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="11870-114">Click **Add condition**.</span></span>
3. <span data-ttu-id="11870-115">Een voorwaarde invoeren.</span><span class="sxs-lookup"><span data-stu-id="11870-115">Enter a condition.</span></span>
4. <span data-ttu-id="11870-116">Geef desgewenst extra voorwaarden op.</span><span class="sxs-lookup"><span data-stu-id="11870-116">Enter additional conditions, if they are required.</span></span>
5. <span data-ttu-id="11870-117">Voer de volgende stappen uit om te controleren of de door u ingevoerde voorwaarden correct zijn geconfigureerd.</span><span class="sxs-lookup"><span data-stu-id="11870-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="11870-118">Klik op **Testen** om het formulier **Workflowvoorwaarde testen** te openen.</span><span class="sxs-lookup"><span data-stu-id="11870-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="11870-119">Selecteer een record in het gebied **Voorwaarde valideren** van het formulier.</span><span class="sxs-lookup"><span data-stu-id="11870-119">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="11870-120">Klik op **Testen**.</span><span class="sxs-lookup"><span data-stu-id="11870-120">Click **Test**.</span></span> <span data-ttu-id="11870-121">Het systeem evalueert de registratie en bepaalt of het voldoet aan de voorwaarden die u hebt gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="11870-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="11870-122">Klik op **OK** of **Annuleren** om terug te gaan naar het formulier **Eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="11870-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]