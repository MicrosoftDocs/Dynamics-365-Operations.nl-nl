---
title: Financiële dimensies en hoofdrekeningen in talen die van rechts naar links worden geschreven
description: In dit onderwerp worden de beslissingen beschreven die u moet nemen wanneer u een van rechts naar links geschreven taal gebruikt. Daarnaast wordt aangegeven hoe u financiële dimensies en hoofdrekeningen instelt.
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: rcarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 26fd186415db0adf01b8c53b188171fcf86fbc88
ms.sourcegitcommit: eff3da7ea98758f100d44ff7feec17157afc2e80
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/27/2021
ms.locfileid: "6111657"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a><span data-ttu-id="162d4-103">Financiële dimensies en hoofdrekeningen in talen die van rechts naar links worden geschreven</span><span class="sxs-lookup"><span data-stu-id="162d4-103">Financial dimensions and main accounts in right-to-left languages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="162d4-104">In dit onderwerp worden enkele implementatiebeslissingen beschreven waarmee u rekening moet houden wanneer u een van rechts naar links geschreven taal gebruikt. Daarnaast wordt aangegeven hoe u financiële dimensies en hoofdrekeningen instelt.</span><span class="sxs-lookup"><span data-stu-id="162d4-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="162d4-105">Financiële dimensies en hoofdrekeningen zijn belangrijke onderdelen van de planningsfase voor een implementatie.</span><span class="sxs-lookup"><span data-stu-id="162d4-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="162d4-106">Nadat financiële dimensies en hoofdrekeningen in het systeem zijn gemaakt, worden deze gebruikt op de pagina's **Rekeningstructuren configureren**, **Geavanceerde regelstructuren** en **Configuratie van financiële dimensies voor integrerende toepassingen**.</span><span class="sxs-lookup"><span data-stu-id="162d4-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="162d4-107">De gedefinieerde volgorde op die pagina's wordt gebruikt in het systeem voor gegevensinvoer en -verbruik.</span><span class="sxs-lookup"><span data-stu-id="162d4-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="162d4-108">Op sommige locaties in het systeem worden de financiële dimensies en hoofdrekeningen in afzonderlijke velden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="162d4-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="162d4-109">Op andere locaties, zoals in journalen, worden de financiële dimensies en hoofdrekeningen als één reeks weergegeven.</span><span class="sxs-lookup"><span data-stu-id="162d4-109">In other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="162d4-110">Aanbevolen procedures voor het instellen van financiële dimensies en hoofdrekeningen in een systeem van rechts naar links</span><span class="sxs-lookup"><span data-stu-id="162d4-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

- <span data-ttu-id="162d4-111">Als u het scheidingsteken voor rekeningschema's selecteert, kunt u een van de opties voor dubbele scheidingstekens selecteren: dubbel koppelteken (`--`), dubbele balk (`||`), dubbele punt (`..`) of dubbel onderstrepingsteken (`\\`).</span><span class="sxs-lookup"><span data-stu-id="162d4-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (`--`), double bar (`||`), double period (`..`), or double underscore (`\\`).</span></span>
- <span data-ttu-id="162d4-112">Wanneer u de waarden voor financiële dimensies en hoofdrekeningen maakt, moet u alleen cijfers en tekens voor talen gebruiken die van rechts naar links worden geschreven.</span><span class="sxs-lookup"><span data-stu-id="162d4-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
- <span data-ttu-id="162d4-113">Gebruik niet het geselecteerde scheidingsteken voor rekeningschema's in waarden voor financiële dimensie en hoofdrekeningen.</span><span class="sxs-lookup"><span data-stu-id="162d4-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="162d4-114">Door deze aanbevolen procedures te volgen, zorgt u ervoor dat de door de gebruiker gedefinieerd volgorde consistent wordt weergegeven in het systeem.</span><span class="sxs-lookup"><span data-stu-id="162d4-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]