---
title: Rapportageopties
description: In dit artikel wordt uitgelegd hoe u het probleem oplost dat ontstaat als een klant Microsoft Dynamics 365 Human Resources-rapporten wil aanpassen of nieuwe rapporten wil maken.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51d84df5c3c29510e2742148b8c260a2cf402639
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527712"
---
# <a name="reporting-options"></a><span data-ttu-id="bbe3d-103">Rapportageopties</span><span class="sxs-lookup"><span data-stu-id="bbe3d-103">Reporting options</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="bbe3d-104">**Omgevingsdetails**</span><span class="sxs-lookup"><span data-stu-id="bbe3d-104">**Environment details**</span></span>

<span data-ttu-id="bbe3d-105">Dit probleem geldt voor alle omgevingen.</span><span class="sxs-lookup"><span data-stu-id="bbe3d-105">This issue applies to all environments.</span></span>

<span data-ttu-id="bbe3d-106">**Symptoom**</span><span class="sxs-lookup"><span data-stu-id="bbe3d-106">**Symptom**</span></span>

<span data-ttu-id="bbe3d-107">De klant wil Dynamics 365 Human Resources-rapporten aanpassen of nieuwe rapporten maken.</span><span class="sxs-lookup"><span data-stu-id="bbe3d-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="bbe3d-108">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="bbe3d-108">**Issue**</span></span>

<span data-ttu-id="bbe3d-109">De gebruiker kan de ingesloten Microsoft Power BI-rapporten niet aanpassen.</span><span class="sxs-lookup"><span data-stu-id="bbe3d-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="bbe3d-110">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="bbe3d-110">**Solution**</span></span>

- <span data-ttu-id="bbe3d-111">De Human Resources-gegevens die naar Common Data Service stromen, kunnen worden gebruikt in rapporten via de Power Apps Common Data Service-connector naar Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="bbe3d-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="bbe3d-112">Houd er rekening mee dat Common Data Service een subset van Human Resources-gegevens bevat.</span><span class="sxs-lookup"><span data-stu-id="bbe3d-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="bbe3d-113">Raadpleeg voor meer informatie over Power BI en dashboards [Power BI-rapporten en dashboards maken met Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="bbe3d-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="bbe3d-114">Elektronische rapportage (ER) is beschikbaar voor sommige rapporten in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bbe3d-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="bbe3d-115">Door de klant gestuurde aanpassingen kunnen worden uitgevoerd via de ER-configuratieopties.</span><span class="sxs-lookup"><span data-stu-id="bbe3d-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="bbe3d-116">Gegevens kunnen worden geëxporteerd naar Microsoft Excel of Microsoft Word met behulp van de verschillende gegevensentiteiten die Human Resources biedt dankzij de integratie met Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="bbe3d-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="bbe3d-117">**Langetermijnoplossing**</span><span class="sxs-lookup"><span data-stu-id="bbe3d-117">**Long-term solution**</span></span>

<span data-ttu-id="bbe3d-118">Er worden meer Power BI-opties beschikbaar en meer gegevens en entiteiten worden opgenomen in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="bbe3d-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
