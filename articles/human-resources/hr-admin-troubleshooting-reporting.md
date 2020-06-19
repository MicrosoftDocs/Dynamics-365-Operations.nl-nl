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
ms.openlocfilehash: 5d47524033bf39a1db6b22b28ee3fcc65348829c
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431010"
---
# <a name="reporting-options"></a><span data-ttu-id="d096b-103">Rapportageopties</span><span class="sxs-lookup"><span data-stu-id="d096b-103">Reporting options</span></span>

<span data-ttu-id="d096b-104">**Omgevingsdetails**</span><span class="sxs-lookup"><span data-stu-id="d096b-104">**Environment details**</span></span>

<span data-ttu-id="d096b-105">Dit probleem geldt voor alle omgevingen.</span><span class="sxs-lookup"><span data-stu-id="d096b-105">This issue applies to all environments.</span></span>

<span data-ttu-id="d096b-106">**Symptoom**</span><span class="sxs-lookup"><span data-stu-id="d096b-106">**Symptom**</span></span>

<span data-ttu-id="d096b-107">De klant wil Dynamics 365 Human Resources-rapporten aanpassen of nieuwe rapporten maken.</span><span class="sxs-lookup"><span data-stu-id="d096b-107">The customer wants to customize Microsoft Dynamics 365 Human Resources reports or create new reports.</span></span>

<span data-ttu-id="d096b-108">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="d096b-108">**Issue**</span></span>

<span data-ttu-id="d096b-109">De gebruiker kan de ingesloten Microsoft Power BI-rapporten niet aanpassen.</span><span class="sxs-lookup"><span data-stu-id="d096b-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="d096b-110">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="d096b-110">**Solution**</span></span>

- <span data-ttu-id="d096b-111">De Human Resources-gegevens die naar Common Data Service stromen, kunnen worden gebruikt in rapporten via de Power Apps Common Data Service-connector naar Power BI Desktop.</span><span class="sxs-lookup"><span data-stu-id="d096b-111">The Human Resources data that flows to Common Data Service can be reported on via the Power Apps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="d096b-112">Houd er rekening mee dat Common Data Service een subset van Human Resources-gegevens bevat.</span><span class="sxs-lookup"><span data-stu-id="d096b-112">Note that Common Data Service contains a subset of Human Resources data.</span></span> <span data-ttu-id="d096b-113">Raadpleeg voor meer informatie over Power BI en dashboards [Power BI-rapporten en dashboards maken met Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="d096b-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with Power Apps Common Data Service](https://powerapps.microsoft.com/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="d096b-114">Elektronische rapportage (ER) is beschikbaar voor sommige rapporten in Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d096b-114">Electronic reporting (ER) is available for some reports in Human Resources.</span></span> <span data-ttu-id="d096b-115">Door de klant gestuurde aanpassingen kunnen worden uitgevoerd via de ER-configuratieopties.</span><span class="sxs-lookup"><span data-stu-id="d096b-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="d096b-116">Gegevens kunnen worden geëxporteerd naar Microsoft Excel of Microsoft Word met behulp van de verschillende gegevensentiteiten die Human Resources biedt dankzij de integratie met Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d096b-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Human Resources provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="d096b-117">**Langetermijnoplossing**</span><span class="sxs-lookup"><span data-stu-id="d096b-117">**Long-term solution**</span></span>

<span data-ttu-id="d096b-118">Er worden meer Power BI-opties beschikbaar en meer gegevens en entiteiten worden opgenomen in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d096b-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
