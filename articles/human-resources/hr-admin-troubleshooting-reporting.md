---
title: Rapportageopties
description: In dit artikel wordt uitgelegd hoe u het probleem oplost dat ontstaat als een klant Microsoft Dynamics 365 Human Resources-rapporten wil aanpassen of nieuwe rapporten wil maken.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 830c8c32128a8dfc1b009557afb272e48ae3a1ff
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112048"
---
# <a name="reporting-options"></a><span data-ttu-id="02c65-103">Rapportageopties</span><span class="sxs-lookup"><span data-stu-id="02c65-103">Reporting options</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="02c65-104">**Omgevingsdetails**</span><span class="sxs-lookup"><span data-stu-id="02c65-104">**Environment details**</span></span>

<span data-ttu-id="02c65-105">Dit probleem geldt voor alle omgevingen.</span><span class="sxs-lookup"><span data-stu-id="02c65-105">This issue applies to all environments.</span></span>

<span data-ttu-id="02c65-106">**Symptoom**</span><span class="sxs-lookup"><span data-stu-id="02c65-106">**Symptom**</span></span>

<span data-ttu-id="02c65-107">De klant wil Dynamics 365 Human Resources-rapporten aanpassen of nieuwe rapporten maken.</span><span class="sxs-lookup"><span data-stu-id="02c65-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="02c65-108">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="02c65-108">**Issue**</span></span>

<span data-ttu-id="02c65-109">De gebruiker kan de ingesloten Microsoft Power BI-rapporten niet aanpassen.</span><span class="sxs-lookup"><span data-stu-id="02c65-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="02c65-110">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="02c65-110">**Solution**</span></span>

- <span data-ttu-id="02c65-111">De Human Resources-gegevens die naar Dataverse stromen, kunnen worden gebruikt in rapporten via de Power Apps Dataverse-connector naar Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="02c65-111">The Human Resources data that flows to Dataverse can be reported on via the Power Apps Dataverse connector to Power BI Desktop.</span></span> <span data-ttu-id="02c65-112">Houd er rekening mee dat Dataverse een subset van Human Resources-gegevens bevat.</span><span class="sxs-lookup"><span data-stu-id="02c65-112">Note that Dataverse contains a subset of Human Resources data.</span></span> <span data-ttu-id="02c65-113">Raadpleeg voor meer informatie over Power BI en dashboards [Power BI-rapporten en dashboards maken met Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="02c65-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="02c65-114">Elektronische rapportage (ER) is beschikbaar voor sommige rapporten in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="02c65-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="02c65-115">Door de klant gestuurde aanpassingen kunnen worden uitgevoerd via de ER-configuratieopties.</span><span class="sxs-lookup"><span data-stu-id="02c65-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="02c65-116">Gegevens kunnen worden geëxporteerd naar Microsoft Excel of Microsoft Word met behulp van de verschillende gegevensentiteiten die Human Resources biedt dankzij de integratie met Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="02c65-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="02c65-117">**Langetermijnoplossing**</span><span class="sxs-lookup"><span data-stu-id="02c65-117">**Long-term solution**</span></span>

<span data-ttu-id="02c65-118">Er worden meer Power BI-opties beschikbaar en meer gegevens en entiteiten worden opgenomen in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="02c65-118">Additional Power BI options will be available, and more data and entities will be part of Dataverse.</span></span>
