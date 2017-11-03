---
title: Boekhoudingsbronverkenner
description: Dit artikel bevat informatie over Boekhoudingsbronverkenner, dat u kunt gebruiken voor een gedetailleerde analyse van de brongegevens achter de grootboekboekingen.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15391
ms.assetid: 57b95899-7298-43c0-8034-45b5d993cbf2
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 421b371c70abc82907810244e8224d859da9fab2
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---

# <a name="accounting-source-explorer"></a><span data-ttu-id="c1294-103">Boekhoudingsbronverkenner</span><span class="sxs-lookup"><span data-stu-id="c1294-103">Accounting source explorer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c1294-104">Dit artikel bevat informatie over Boekhoudingsbronverkenner, dat u kunt gebruiken voor een gedetailleerde analyse van de brongegevens achter de grootboekboekingen.</span><span class="sxs-lookup"><span data-stu-id="c1294-104">This article provides information about Accounting source explorer, which you can use for detailed analysis of the source information behind general ledger accounting entries.</span></span>

<span data-ttu-id="c1294-105">Boekhoudingsbronverkenner is een nieuwe pagina waarop brongegevens worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c1294-105">Accounting source explorer is a new page that shows source information.</span></span> <span data-ttu-id="c1294-106">U kunt Boekhoudingsbronverkenner gebruiken als zelfstandig hulpprogramma of voor het analyseren van de gegevens achter de grootboekposten voor boekhouding.</span><span class="sxs-lookup"><span data-stu-id="c1294-106">You can use Accounting source explorer either as a stand-alone tool or to analyze the details behind general ledger accounting entries.</span></span> <span data-ttu-id="c1294-107">U kunt Boekhoudingsbronverkenner bijvoorbeeld gebruiken om de meest gedetailleerde brongegevens voor een saldo in Proefbalans voor een boekstuktransactie op te halen.</span><span class="sxs-lookup"><span data-stu-id="c1294-107">For example, you can use Accounting source explorer to get the most detailed source information for a balance in Trail balance or for a voucher transaction.</span></span> <span data-ttu-id="c1294-108">Vervolgens kunt u de functie Exporteren naar MS Excel gebruiken om de gegevens verder in te delen en te verdelen in Microsoft Excel (bijvoorbeeld in draaitabel of een draaitabelrapport).</span><span class="sxs-lookup"><span data-stu-id="c1294-108">You can then use the Export to MS Excel feature to further slice and dice the information in Microsoft Excel (for example, in a PivotTable or on a PivotTable report).</span></span>

<span data-ttu-id="c1294-109">Met Boekhoudingsbronverkenner wordt altijd hetzelfde totaalbedrag per grootboekrekening weergegeven wanneer het grootboek wordt getoond (bijvoorbeeld in Proefbalans).</span><span class="sxs-lookup"><span data-stu-id="c1294-109">Accounting source explorer always shows the same total amount per ledger account as General ledger shows (for example, in Trial balance).</span></span> <span data-ttu-id="c1294-110">Net als in Proefbalans kunt u segmenten in afzonderlijke kolommen weergeven.</span><span class="sxs-lookup"><span data-stu-id="c1294-110">As in Trial balance, you can display segments in separate columns.</span></span> <span data-ttu-id="c1294-111">Selecteer alleen de juiste set met financiële dimensies.</span><span class="sxs-lookup"><span data-stu-id="c1294-111">Just select the appropriate financial dimension set.</span></span> 

<span data-ttu-id="c1294-112">U kunt parameters gebruiken om een datuminterval voor de analyse te definiëren.</span><span class="sxs-lookup"><span data-stu-id="c1294-112">You can use parameters to define a date interval for the analysis.</span></span> <span data-ttu-id="c1294-113">Deze functionaliteit lijkt ook op de functionaliteit in Proefbalans.</span><span class="sxs-lookup"><span data-stu-id="c1294-113">This functionality also resembles the functionality in Trial balance.</span></span>

<span data-ttu-id="c1294-114">Voor alle documenten die gebruikmaken van het raamwerk voor brondocumenten geeft Boekhoudingsbronverkenner aanvullende informatie weer op basis van de boekhoudingsverdelingen en, indien van toepassing, de projectboekhoudingsverdelingen.</span><span class="sxs-lookup"><span data-stu-id="c1294-114">For all documents that use the source document framework, Accounting source explorer shows additional information, based on accounting distributions and, if applicable, project accounting distributions.</span></span> <span data-ttu-id="c1294-115">Deze informatie omvat geldbedragtype, project, activiteit, categorie en regeleigenschap.</span><span class="sxs-lookup"><span data-stu-id="c1294-115">This information includes the monetary amount type, project, activity, category, and line property.</span></span> <span data-ttu-id="c1294-116">Hieronder staan enkele voorbeelden van de analyse die u kunt uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="c1294-116">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="c1294-117">Afwijkingen tussen inkooporders en leveranciersfacturen, omdat elke afwijking wordt vertegenwoordigd met een type monetair bedrag, zoals toeslagafwijking</span><span class="sxs-lookup"><span data-stu-id="c1294-117">Variances between purchase orders and vendor invoices, because each variance is represented by a monetary amount type, such as charge variance</span></span>
-   <span data-ttu-id="c1294-118">Factureerbare en niet-factureerbare uren en onkosten per project, bedrijfseenheid en hoofdrekening</span><span class="sxs-lookup"><span data-stu-id="c1294-118">Billable versus non-billable hours and expenses per project, business unit, and main account</span></span>

<span data-ttu-id="c1294-119">Voor brondocumenten waarin het concept van identiteiten voor brondocumentverwijzing wordt gebruikt, worden met Boekhoudingbronverkenner zelfs meer details weergegeven, zoals de klant, de leverancier, de werknemer, het product, de hoeveelheid, de eenheidstekst en omschrijvingen.</span><span class="sxs-lookup"><span data-stu-id="c1294-119">For source documents that use the source document reference identities concept, Accounting source explorer shows even more details, such as the customer, vendor, worker, product, quantity, unit text, and descriptions.</span></span> <span data-ttu-id="c1294-120">Hieronder staan enkele voorbeelden van de analyse die u kunt uitvoeren:</span><span class="sxs-lookup"><span data-stu-id="c1294-120">Here are some examples of the analysis that you can do:</span></span>

-   <span data-ttu-id="c1294-121">Hotelonkosten per bedrijfseenheid en hotelmerk voor een belastingperiode op basis van onkostennota's</span><span class="sxs-lookup"><span data-stu-id="c1294-121">Hotel expenses per business unit and hotel brand for a fiscal period, based on expense reports</span></span>
-   <span data-ttu-id="c1294-122">Kortingen per leverancier, product, afdeling</span><span class="sxs-lookup"><span data-stu-id="c1294-122">Discounts per vendor, product, department</span></span>

<span data-ttu-id="c1294-123">Voor deze documenten kunt u ook naar het werkelijke brondocument van Boekhoudingsbronverkenner navigeren.</span><span class="sxs-lookup"><span data-stu-id="c1294-123">For these documents, you can also navigate to the actual source document from Accounting source explorer.</span></span>




