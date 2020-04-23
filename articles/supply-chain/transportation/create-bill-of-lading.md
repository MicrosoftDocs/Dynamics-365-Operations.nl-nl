---
title: Een vrachtbrief maken
description: In dit onderwerp wordt uitgelegd hoe u een vrachtbrief maakt wanneer u gebruik maakt van de processen voor magazijnbeheer.
author: MarkusFogelberg
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSBillOfLading, WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 193583
ms.assetid: 1ad0c1cb-4346-4042-a59b-923115fac03e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 05ad5d4b49f1fa50bde7df9c835ee99a981420c4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206306"
---
# <a name="create-a-bill-of-lading"></a><span data-ttu-id="44621-103">Een vrachtbrief maken</span><span class="sxs-lookup"><span data-stu-id="44621-103">Create a bill of lading</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44621-104">In dit onderwerp wordt uitgelegd hoe u een vrachtbrief maakt wanneer u gebruik maakt van de processen voor magazijnbeheer.</span><span class="sxs-lookup"><span data-stu-id="44621-104">This topic describes how to create a bill of lading when using warehouse management processes.</span></span>  

<span data-ttu-id="44621-105">Een vrachtbrief is een juridisch document tussen het bedrijf dat de artikelen verzendt en de vervoerder.</span><span class="sxs-lookup"><span data-stu-id="44621-105">A bill of lading is a legal document between the company that ships the items and the carrier.</span></span> <span data-ttu-id="44621-106">Het document begeleidt de verzonden artikelen en dient als ontvangstbewijs wanneer artikelen op de plaats van bestemming worden afgeleverd.</span><span class="sxs-lookup"><span data-stu-id="44621-106">The document accompanies the shipped items, and it serves as a receipt of shipment when the items are delivered at the destination.</span></span> <span data-ttu-id="44621-107">Als u magazijnbeheer gebruikt, zijn er twee manieren om een vrachtbrief te genereren:</span><span class="sxs-lookup"><span data-stu-id="44621-107">If you're using warehouse management, there are two ways to generate a bill of lading:</span></span>

  -   <span data-ttu-id="44621-108">Het rapport handmatig aanmaken, op de pagina **Vrachtbrief**.</span><span class="sxs-lookup"><span data-stu-id="44621-108">Create the report manually, using the **Bill of lading** page.</span></span>
  -   <span data-ttu-id="44621-109">Het rapport genereren in de **Workbench ladingplanning**.</span><span class="sxs-lookup"><span data-stu-id="44621-109">Generate the report from the **Load planning workbench**.</span></span>

<span data-ttu-id="44621-110">Als u de vrachtbrief genereert in de **Workbench ladingplanning** moet de ladingsstatus **Verzonden** zijn.</span><span class="sxs-lookup"><span data-stu-id="44621-110">If you generate the bill of lading from the **Load planning workbench**, the load status must be **Shipped.**</span></span> <span data-ttu-id="44621-111">Als de lading meer dan één zending bevat, kunt u een vrachtbrief maken voor elke zending.</span><span class="sxs-lookup"><span data-stu-id="44621-111">If there's more than one shipment in the load, a bill of lading is created for each shipment.</span></span> <span data-ttu-id="44621-112">Nadat een vrachtbrief is gemaakt, kunt u er wijzigingen in aanbrengen op de pagina **Vrachtbrief**.</span><span class="sxs-lookup"><span data-stu-id="44621-112">After a bill of lading has been created you can make changes to it on the **Bill of lading** page.</span></span>

## <a name="master-bill-of-lading"></a><span data-ttu-id="44621-113">Hoofdvrachtbrief</span><span class="sxs-lookup"><span data-stu-id="44621-113">Master bill of lading</span></span>
<span data-ttu-id="44621-114">Als de lading meer dan een zending bevat, kunt u een hoofdvrachtbrief maken.</span><span class="sxs-lookup"><span data-stu-id="44621-114">If there's more than one shipment in the load, you can generate a master bill of lading.</span></span> <span data-ttu-id="44621-115">Deze heeft dezelfde indeling en informatie als een vrachtbrief, maar bevat de samengevatte inhoud voor alle zendingen.</span><span class="sxs-lookup"><span data-stu-id="44621-115">This has the same layout and information as a bill of lading, but contains the summarized content for all the shipments.</span></span> <span data-ttu-id="44621-116">Als op de pagina **Transportbeheerparameters** de optie **Een hoofdvrachtbrief maken wanneer een lading uit meer dan een zending bestaat** is ingesteld op **Ja**, wordt een hoofdvrachtbrief automatisch gegenereerd wanneer u een vrachtbrief maakt in de **Workbench ladingplanning** en er meerdere zendingen zijn.</span><span class="sxs-lookup"><span data-stu-id="44621-116">If the **Create a master bill of lading when there's more than one shipment on a load** option is set to **Yes** on the **Transportation management parameters** page, a master bill of lading is automatically generated if you create a bill of lading from the **Load planning workbench**, and there's more than one shipment.</span></span> <span data-ttu-id="44621-117">U kunt ook een lijst met de vrachtbrieven verkrijgen door te klikken op **Gerelateerde informatie** &gt; **Vrachtbrief**.</span><span class="sxs-lookup"><span data-stu-id="44621-117">You can also get a list of the bills of lading by clicking **Related information** &gt; **Bill of lading**.</span></span> <span data-ttu-id="44621-118">Als u vrachtbrieven handmatig aanmaakt, kunt u een hoofdvrachtbrief maken op de pagina **Vrachtbrief**.</span><span class="sxs-lookup"><span data-stu-id="44621-118">If you're creating bills of lading manually, you can create a master bill of lading on the **Bill of lading** page.</span></span>



