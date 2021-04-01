---
title: Externe gegevens in cashflowprognoses gebruiken (preview)
description: In dit onderwerp worden de installatiestappen beschreven die u moet voltooien zodat externe gegevens kunnen worden ingevoerd of geïmporteerd in cashflowprognoses.
author: rcarlson
manager: AnnBe
ms.date: 05/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-06-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 03318eaae0b3329dc758c48202f8f47ca2c4ab08
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5245563"
---
# <a name="use-external-data-in-cash-flow-forecasts-preview"></a><span data-ttu-id="a72b0-103">Externe gegevens in cashflowprognoses gebruiken (preview)</span><span class="sxs-lookup"><span data-stu-id="a72b0-103">Use external data in cash flow forecasts (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="a72b0-104">Externe gegevens kunnen worden ingevoerd of geïmporteerd in cashflowprognoses.</span><span class="sxs-lookup"><span data-stu-id="a72b0-104">External data can be entered or imported into cash flow forecasts.</span></span> <span data-ttu-id="a72b0-105">Dit onderwerp beschrijft de instellingsstappen die specifiek zijn voor het gebruik van externe gegevens en waarmee de externe gegevens in een cashflowprognose kunnen worden opgenomen.</span><span class="sxs-lookup"><span data-stu-id="a72b0-105">This topic describes the setup steps that are specific to the use of external data and that enable the external data to be included in a cash flow forecast.</span></span>

## <a name="external-data-setup"></a><span data-ttu-id="a72b0-106">Externe gegevens instellen</span><span class="sxs-lookup"><span data-stu-id="a72b0-106">External data setup</span></span>

<span data-ttu-id="a72b0-107">Gebruik het tabblad **Externe bron** op de pagina **Instelling van cashflowprognose** (**Contanten en bankbeheer \> Cashflowprognose**) om instellingen op te geven die het gebruik van externe gegevens in cashflowprognoses ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="a72b0-107">Use the **External source** tab on the **Cash flow forecast setup** page (**Cash and bank management \> Cash flow forecasting**) to enter settings that support the use of external data in cash flow forecasts.</span></span>

<span data-ttu-id="a72b0-108">Zie voor meer informatie over het instellen [Cashflowprognose](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span><span class="sxs-lookup"><span data-stu-id="a72b0-108">For more information about the setup, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span>

<span data-ttu-id="a72b0-109">Als u externe gegevens wilt invoeren voor cashflowprognoses, kunt u de ervaring Openen in Excel gebruiken voor het invoeren en wijzigen van externe gegevens.</span><span class="sxs-lookup"><span data-stu-id="a72b0-109">To enter external data for cash flow forecasts, you can use the Open in Excel experience for entering and modifying external data.</span></span> <span data-ttu-id="a72b0-110">Selecteer de knop **Externe gegevens** en selecteer vervolgens **Externe gegevens toevoegen** of **Bestaande externe gegevens bewerken**.</span><span class="sxs-lookup"><span data-stu-id="a72b0-110">Select the **External data** button, and then select either **Add External Data** or **Edit existing external data**.</span></span> <span data-ttu-id="a72b0-111">Wanneer het Microsoft Excel-bestand wordt geopend, kunt u informatie invoeren in de volgende velden:</span><span class="sxs-lookup"><span data-stu-id="a72b0-111">When the Microsoft Excel file is opened, you can enter information in the following fields:</span></span>

- <span data-ttu-id="a72b0-112">**Invoer-ID**</span><span class="sxs-lookup"><span data-stu-id="a72b0-112">**Entry ID**</span></span>
- <span data-ttu-id="a72b0-113">**Beschrijving** (optioneel)</span><span class="sxs-lookup"><span data-stu-id="a72b0-113">**Description** (optional)</span></span>
- <span data-ttu-id="a72b0-114">**Naam van externe bron**: selecteer een van de waarden in de lijst die u hebt gedefinieerd bij het instellen van Financiële inzichten.</span><span class="sxs-lookup"><span data-stu-id="a72b0-114">**External Source name** – Select one of the values in the list that you defined when you set up Finance Insights.</span></span>
- <span data-ttu-id="a72b0-115">**Rechtspersoon**</span><span class="sxs-lookup"><span data-stu-id="a72b0-115">**Legal Entity**</span></span>
- <span data-ttu-id="a72b0-116">**Datum**</span><span class="sxs-lookup"><span data-stu-id="a72b0-116">**Date**</span></span>
- <span data-ttu-id="a72b0-117">**Bedrag in transactievaluta**</span><span class="sxs-lookup"><span data-stu-id="a72b0-117">**Amount in transaction currency**</span></span>
- <span data-ttu-id="a72b0-118">**Valutacode**</span><span class="sxs-lookup"><span data-stu-id="a72b0-118">**Currency Code**</span></span>
- <span data-ttu-id="a72b0-119">**Standaarddimensie** (optioneel)</span><span class="sxs-lookup"><span data-stu-id="a72b0-119">**Default Dimension** (optional)</span></span>
- <span data-ttu-id="a72b0-120">**Documentnummer** (optioneel)</span><span class="sxs-lookup"><span data-stu-id="a72b0-120">**Document number** (optional)</span></span>
- <span data-ttu-id="a72b0-121">**Rekeningnummer** (optioneel)</span><span class="sxs-lookup"><span data-stu-id="a72b0-121">**Account number** (optional)</span></span>
- <span data-ttu-id="a72b0-122">**Rekeningnaam** (optioneel)</span><span class="sxs-lookup"><span data-stu-id="a72b0-122">**Account name** (optional)</span></span>

## <a name="importing-external-data-by-using-the-data-management-framework"></a><span data-ttu-id="a72b0-123">Externe gegevens importeren met behulp van het Gegevensbeheer-framework</span><span class="sxs-lookup"><span data-stu-id="a72b0-123">Importing external data by using the Data Management framework</span></span>

<span data-ttu-id="a72b0-124">U kunt externe gegevens importeren voor cashflowprognoses met behulp van het werkgebied **Gegevensbeheer** en de entiteit met de naam **Invoer externe bron cashflowprognose**.</span><span class="sxs-lookup"><span data-stu-id="a72b0-124">You can import external data for cash flow forecasts by using the **Data Management** workspace and the entity that is named **Cash flow forecast external source entry**.</span></span>

<span data-ttu-id="a72b0-125">Bovendien, als u instellingsgegevens van de ene omgeving naar de andere moet verplaatsen, zijn de volgende entiteiten beschikbaar voor de vereiste instellingstabellen:</span><span class="sxs-lookup"><span data-stu-id="a72b0-125">Additionally, if you must move setup data from one environment to another, the following entities area available for the setup tables that are required:</span></span>

- <span data-ttu-id="a72b0-126">Externe bron voor cashflowprognose instellen</span><span class="sxs-lookup"><span data-stu-id="a72b0-126">Cash flow forecast external source setup</span></span>
- <span data-ttu-id="a72b0-127">Rechtspersoon van externe bron voor cashflowprognose instellen</span><span class="sxs-lookup"><span data-stu-id="a72b0-127">Cash flow forecast external source legal entity setup</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="a72b0-128">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="a72b0-128">Privacy notice</span></span>
<span data-ttu-id="a72b0-129">Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="a72b0-129">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]