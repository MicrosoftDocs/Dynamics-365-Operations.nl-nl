---
title: Configuratie van ISO20022-kredietoverdracht importeren
description: In deze procedure ziet u hoe u een configuratie voor elektronische rapportage van leveranciersbetalingen importeert.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 01f44c49b6623cbcc2f08cfd6e4978c9a1676b83
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140036"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="de21a-103">Configuratie van ISO20022-kredietoverdracht importeren</span><span class="sxs-lookup"><span data-stu-id="de21a-103">Import ISO20022 credit transfer configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="de21a-104">In deze procedure ziet u hoe u een configuratie voor elektronische rapportage van leveranciersbetalingen importeert.</span><span class="sxs-lookup"><span data-stu-id="de21a-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="de21a-105">De Duitse kredietoverdrachtindeling ISO 20022 wordt hier als voorbeeld gebruikt.</span><span class="sxs-lookup"><span data-stu-id="de21a-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="de21a-106">Deze procedure kan worden gebruikt voor andere beschikbare indelingen voor elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="de21a-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="de21a-107">Deze taak is gemaakt met het demobedrijf DEMF, maar u kunt elk bedrijf uit de demogegevens gebruiken om deze taak uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="de21a-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="de21a-108">Dit is de eerste van vijf taken die samen het leveranciersbetalingproces toelichten door middel van elektronische rapportageconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="de21a-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="de21a-109">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="de21a-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="de21a-110">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="de21a-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="de21a-111">Selecteer in de lijst met beschikbare configuratieproviders de waarde Microsoft.</span><span class="sxs-lookup"><span data-stu-id="de21a-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="de21a-112">Klik op Instellingen als actief.</span><span class="sxs-lookup"><span data-stu-id="de21a-112">Click Set active.</span></span>
4. <span data-ttu-id="de21a-113">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="de21a-113">Click Repositories.</span></span>
5. <span data-ttu-id="de21a-114">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="de21a-114">Click Open.</span></span>
6. <span data-ttu-id="de21a-115">Klik op Filters weergeven.</span><span class="sxs-lookup"><span data-stu-id="de21a-115">Click Show filters.</span></span>
7. <span data-ttu-id="de21a-116">Pas de volgende filter toe: voer in het veld "Configuratienaam" de waarde "ISO20022 Kredietoverdracht (DE)" in met de filteroperator "begint met".</span><span class="sxs-lookup"><span data-stu-id="de21a-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="de21a-117">Of zoek de configuratie in de lijst, selecteer deze en verplaats de configuratie naar de taak Importeren.</span><span class="sxs-lookup"><span data-stu-id="de21a-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="de21a-118">Klik op Importeren.</span><span class="sxs-lookup"><span data-stu-id="de21a-118">Click Import.</span></span>
    * <span data-ttu-id="de21a-119">Als de knop Importeren niet beschikbaar is, betekent dit dat deze configuratie al is geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="de21a-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="de21a-120">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="de21a-120">Click Yes.</span></span>

