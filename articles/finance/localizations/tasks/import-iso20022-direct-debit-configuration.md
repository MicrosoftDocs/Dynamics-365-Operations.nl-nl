---
title: Configuratie van ISO20022 automatische afschrijving importeren
description: In deze procedure ziet u hoe u een configuratie voor elektronische rapportage van klantenbetalingen importeert.
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
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 964f396625340d593a2fe3dd5be5a1b7da795e9a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218753"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="4de93-103">Configuratie van ISO20022 automatische afschrijving importeren</span><span class="sxs-lookup"><span data-stu-id="4de93-103">Import ISO20022 direct debit configuration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4de93-104">In deze procedure ziet u hoe u een configuratie voor elektronische rapportage van klantenbetalingen importeert.</span><span class="sxs-lookup"><span data-stu-id="4de93-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="4de93-105">Deze procedure gebruikt als voorbeeld de indeling voor automatische incasso van ISO20022.</span><span class="sxs-lookup"><span data-stu-id="4de93-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="4de93-106">Deze procedure is gemaakt met het demobedrijf DEMF, maar u kunt elk bedrijf uit de demogegevens voor dit doel gebruiken.</span><span class="sxs-lookup"><span data-stu-id="4de93-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="4de93-107">Dit is de eerste van vijf taken die het proces voor klantenbetalingen toelichten door middel van elektronische rapportageconfiguraties.</span><span class="sxs-lookup"><span data-stu-id="4de93-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="4de93-108">Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.</span><span class="sxs-lookup"><span data-stu-id="4de93-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4de93-109">Selecteer in de lijst met beschikbare configuratieproviders de waarde Microsoft.</span><span class="sxs-lookup"><span data-stu-id="4de93-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="4de93-110">Klik op Instellingen als actief.</span><span class="sxs-lookup"><span data-stu-id="4de93-110">Click Set active.</span></span>
4. <span data-ttu-id="4de93-111">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="4de93-111">Click Repositories.</span></span>
5. <span data-ttu-id="4de93-112">Klik op Openen.</span><span class="sxs-lookup"><span data-stu-id="4de93-112">Click Open.</span></span>
6. <span data-ttu-id="4de93-113">Klik op Filters weergeven.</span><span class="sxs-lookup"><span data-stu-id="4de93-113">Click Show filters.</span></span>
7. <span data-ttu-id="4de93-114">Pas de volgende filter toe: voer in het veld "Configuratienaam" de waarde "ISO20022 Automatische incasso (DE)" in met de filteroperator "begint met".</span><span class="sxs-lookup"><span data-stu-id="4de93-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="4de93-115">Desgewenst kunt u de configuratie in de lijst zoeken, selecteren en deze stap overslaan.</span><span class="sxs-lookup"><span data-stu-id="4de93-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="4de93-116">Klik op Importeren.</span><span class="sxs-lookup"><span data-stu-id="4de93-116">Click Import.</span></span>
    * <span data-ttu-id="4de93-117">Als de knop Importeren niet beschikbaar is, betekent dit dat deze configuratie al is geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="4de93-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="4de93-118">Klik op Ja.</span><span class="sxs-lookup"><span data-stu-id="4de93-118">Click Yes.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]