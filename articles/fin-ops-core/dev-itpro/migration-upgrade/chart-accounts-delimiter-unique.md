---
title: Het scheidingsteken in het rekeningschema uniek maken
description: In dit onderwerp wordt toegelicht waarom het niet mogelijk is om hetzelfde scheidingsteken te gebruiken voor het rekenschema en dimensiewaarden. Na de upgrade moet u het scheidingsteken wijzigen.
author: panolte
manager: AnnBe
ms.date: 03/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 72965e9c6182bdac123feb1bc5cc4b82d91cd588
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020099"
---
# <a name="make-the-chart-of-accounts-delimiter-unique"></a><span data-ttu-id="e8739-104">Het scheidingsteken in het rekeningschema uniek maken</span><span class="sxs-lookup"><span data-stu-id="e8739-104">Make the chart of accounts delimiter unique</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e8739-105">In Microsoft Dynamics AX 2012 kunt u hetzelfde scheidingsteken gebruiken voor het rekeningschema en dimensiewaarden.</span><span class="sxs-lookup"><span data-stu-id="e8739-105">In Microsoft Dynamics AX 2012, you could use the same delimiter for your chart of accounts and dimension values.</span></span> <span data-ttu-id="e8739-106">In de huidige versies van Finance and Operations is niet toegestaan dat hetzelfde scheidingsteken wordt gebruikt voor het rekeningschema en dimensiewaarden.</span><span class="sxs-lookup"><span data-stu-id="e8739-106">In current versions of Finance and Operations, you cannot have the same delimiter for the chart of accounts and dimension values.</span></span> <span data-ttu-id="e8739-107">Als er een dubbele scheidingsteken is, kunt u dit wijzigen na de upgrade.</span><span class="sxs-lookup"><span data-stu-id="e8739-107">If there is a duplicate delimiter, you can change it after upgrade.</span></span> 

<span data-ttu-id="e8739-108">Deze functie is niet beschikbaar in de volgende versies:</span><span class="sxs-lookup"><span data-stu-id="e8739-108">This feature is available in the following versions:</span></span>
- <span data-ttu-id="e8739-109">Finance and Operations versie 8.0</span><span class="sxs-lookup"><span data-stu-id="e8739-109">Finance and Operations version 8.0</span></span>
- <span data-ttu-id="e8739-110">Finance and Operations versie 7.1, KB 4094701 Kan de financiële dimensies niet invoeren als de dimensiewaarden het scheidingsteken voor het rekeningschema bevatten</span><span class="sxs-lookup"><span data-stu-id="e8739-110">Finance and Operations version 7.1, KB 4094701 Cannot enter the financial dimensions when the dimension values contain the chart of accounts delimiter</span></span>
- <span data-ttu-id="e8739-111">Finance and Operations versie 7.2, KB 4092967 Kan subproject niet als dimensie kiezen wanneer de indeling van het subproject het dimensiescheidingsteken bevat</span><span class="sxs-lookup"><span data-stu-id="e8739-111">Finance and Operations version 7.2, KB 4092967 Cannot choose sub-project as dimension when sub-project format contains the dimension delimiter</span></span>

## <a name="update-delimiter"></a><span data-ttu-id="e8739-112">Scheidingsteken bijwerken</span><span class="sxs-lookup"><span data-stu-id="e8739-112">Update delimiter</span></span>
<span data-ttu-id="e8739-113">Als er een conflict is met het rekeningschema, kan het scheidingsteken voor het rekeningschema en de indeling van de project/subproject-ID worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="e8739-113">If there is a conflict with the chart of accounts, the chart of accounts delimiter and the project/subproject ID format can be changed.</span></span> <span data-ttu-id="e8739-114">Geen andere scheidingstekens voor de dimensie kunnen worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="e8739-114">No other dimension delimiters can be changed.</span></span> 
- <span data-ttu-id="e8739-115">U kunt het scheidingsteken voor het rekeningschema wijzigen na de upgrade in **Grootboekparameters** > **Rekeningschema en dimensies** > **Scheidingsteken wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="e8739-115">You can change the chart of accounts delimiter after upgrade in **General ledger parameters** > **Chart of accounts and dimensions** > **Change delimiter**.</span></span> 
- <span data-ttu-id="e8739-116">Als het enige conflict betrekking heeft op de indeling van de project/subproject-ID, kunt u die waarde wijzigen in **Projectbeheer- en boekhoudingsparameters** > **Algemeen** > **Indeling subproject wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="e8739-116">If the only conflict is with the project/subproject ID format, you can change that value in **Project management and accounting parameters** > **General** > **Modify subproject format**.</span></span> 

## <a name="how-to-determine-if-your-environment-requires-updated-delimiters"></a><span data-ttu-id="e8739-117">Bepalen of uw omgeving bijgewerkte scheidingstekens vereist</span><span class="sxs-lookup"><span data-stu-id="e8739-117">How to determine if your environment requires updated delimiters</span></span> 
<span data-ttu-id="e8739-118">Als scheidingstekens in uw bijgewerkte omgeving conflicten veroorzaken, kan het instabiel zijn wanneer u waarden invoert in een besturingselement voor het invoeren van segmenten of dimensies.</span><span class="sxs-lookup"><span data-stu-id="e8739-118">If delimiters in your upgraded environment are conflicting, you may experience instability when entering values in a segmented entry control or dimension entry control.</span></span> <span data-ttu-id="e8739-119">Dit houdt in dat u altijd zoekopdrachten of een flyout-menu moet gebruiken voor het invoeren van combinaties van rekeningen en dimensies.</span><span class="sxs-lookup"><span data-stu-id="e8739-119">This means that you will need to always use lookups or a flyout menu when entering account and dimension combinations.</span></span>
