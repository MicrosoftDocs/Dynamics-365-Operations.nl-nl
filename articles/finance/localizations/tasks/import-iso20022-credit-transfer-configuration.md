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
ms.openlocfilehash: ee7e69611d31d2577ebafdfc059b0936aef0520b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174821"
---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="b7577-103">Configuratie van ISO20022-kredietoverdracht importeren</span><span class="sxs-lookup"><span data-stu-id="b7577-103">Import ISO20022 credit transfer configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b7577-104">In deze procedure ziet u hoe u een configuratie voor elektronische rapportage van leveranciersbetalingen importeert.</span><span class="sxs-lookup"><span data-stu-id="b7577-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="b7577-105">De Duitse kredietoverdrachtindeling ISO 20022 wordt hier als voorbeeld gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b7577-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="b7577-106">Deze procedure kan worden gebruikt voor andere beschikbare indelingen voor elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="b7577-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="b7577-107">Deze taak is gemaakt met het demobedrijf DEMF, maar u kunt elk bedrijf uit de demogegevens gebruiken om deze taak uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b7577-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="b7577-108">Dit is de eerste van vijf taken die samen het leveranciersbetalingproces toelichten door middel van elektronische rapportageconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="b7577-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="b7577-109">Deze procedure is voor een functie die is toegevoegd in Dynamics 365 for Operations, versie 1611.</span><span class="sxs-lookup"><span data-stu-id="b7577-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="b7577-110">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="b7577-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b7577-111">Selecteer in de lijst met beschikbare configuratieproviders de waarde Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b7577-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="b7577-112">Klik op Instellingen als actief.</span><span class="sxs-lookup"><span data-stu-id="b7577-112">Click Set active.</span></span>
4. <span data-ttu-id="b7577-113">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="b7577-113">Click Repositories.</span></span>
5. <span data-ttu-id="b7577-114">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="b7577-114">Click Open.</span></span>
6. <span data-ttu-id="b7577-115">Klik op Filters weergeven.</span><span class="sxs-lookup"><span data-stu-id="b7577-115">Click Show filters.</span></span>
7. <span data-ttu-id="b7577-116">Pas de volgende filter toe: voer in het veld "Configuratienaam" de waarde "ISO20022 Kredietoverdracht (DE)" in met de filteroperator "begint met".</span><span class="sxs-lookup"><span data-stu-id="b7577-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="b7577-117">Of zoek de configuratie in de lijst, selecteer deze en verplaats de configuratie naar de taak Importeren.</span><span class="sxs-lookup"><span data-stu-id="b7577-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="b7577-118">Klik op Importeren.</span><span class="sxs-lookup"><span data-stu-id="b7577-118">Click Import.</span></span>
    * <span data-ttu-id="b7577-119">Als de knop Importeren niet beschikbaar is, betekent dit dat deze configuratie al is geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="b7577-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="b7577-120">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="b7577-120">Click Yes.</span></span>
