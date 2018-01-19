---
title: Elektronische documenten genereren en toepassingsgegevens bijwerken met behulp van het hulpmiddel Elektronische Rapportage
description: U kunt indelingen voor elektronische rapportage (ER) ontwerpen, die in de toepassing Finance and Operations kunnen worden gebruikt voor het genereren van uitgaande elektronische documenten. U kunt ook ER-indelingen ontwerpen die binnenkomende elektronische documenten parseren en de inhoud in die documenten gebruiken om toepassingsgegevens bij te werken.
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 34654c458ce74bf2ee6c2d2bac655d6c399ca393
ms.contentlocale: nl-nl
ms.lasthandoff: 01/19/2018

---

# <a name="generate-electronic-documents-and-update-application-data-using-the-electronic-reporting-tool"></a><span data-ttu-id="a3ca5-104">Elektronische documenten genereren en toepassingsgegevens bijwerken met behulp van het hulpmiddel Elektronische Rapportage</span><span class="sxs-lookup"><span data-stu-id="a3ca5-104">Generate electronic documents and update application data using the Electronic reporting tool</span></span>

<span data-ttu-id="a3ca5-105">U kunt indelingen voor elektronische rapportage (ER) ontwerpen, die in de toepassing Finance and Operations kunnen worden gebruikt voor het genereren van uitgaande elektronische documenten.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-105">You can design Electronic reporting (ER) formats that can be used in the Finance and Operations application to generate outgoing electronic documents.</span></span> <span data-ttu-id="a3ca5-106">U kunt ook ER-indelingen ontwerpen die binnenkomende elektronische documenten parseren en de inhoud in die documenten gebruiken om toepassingsgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-106">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span> 

<span data-ttu-id="a3ca5-107">Met deze functionaliteit kan één ER-indeling worden gebruikt om uitgaande elektronische documenten te genereren en vervolgens de toepassingsgegevens bij te werken.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-107">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="a3ca5-108">U kunt deze functie gebruiken in de volgende scenario's:</span><span class="sxs-lookup"><span data-stu-id="a3ca5-108">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="a3ca5-109">Om te voorkomen dat toepassingsgegevens in opeenvolgende processen herhaaldelijk worden gebruikt, kunt u de gegevens van een toepassing markeren nadat deze zijn gebruik voor het genereren van elektronische documenten.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-109">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="a3ca5-110">U kunt bijvoorbeeld betalingstransacties markeren als verwerkt, direct nadat ze zijn opgenomen in een gegenereerd betalingsbericht.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-110">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="a3ca5-111">Voor het opslaan van de verwerkingsgegevens van elektronische documenten die zijn gegenereerd door middel van ER-logica.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-111">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="a3ca5-112">Bijvoorbeeld, een unieke betalingsbericht-id die wordt gegenereerd op basis van de ER-expressie.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-112">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="a3ca5-113">De expressie is gebaseerd op gegevens die zijn ingevoerd in het ER-dialoogvenster bij het uitvoeren van de ER-indeling voor het genereren van documenten.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-113">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="a3ca5-114">Voor meer informatie over deze functie speelt u de set taakbegeleidingen ER: Documenten genereren met bijwerken van toepassingsgegevens (onderdeel van het bedrijfsproces 7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)) af waarin u de details van Intrastat-rapportage en -archivering krijgt uitgelegd.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-114">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="a3ca5-115">De volgende bestanden zijn vereist voor het uitvoeren van bepaalde stappen in deze taakbegeleidingen.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-115">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="a3ca5-116">Download deze bestanden naar uw lokale computer en sla ze daar op.</span><span class="sxs-lookup"><span data-stu-id="a3ca5-116">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="a3ca5-117">ER-gegevensmodel configureren: Intrastat (model)</span><span class="sxs-lookup"><span data-stu-id="a3ca5-117">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="a3ca5-118">ER-modeltoewijzing configureren: Intrastat (toewijzing)</span><span class="sxs-lookup"><span data-stu-id="a3ca5-118">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="a3ca5-119">ER-indeling configureren: Intrastat (indeling)</span><span class="sxs-lookup"><span data-stu-id="a3ca5-119">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)

