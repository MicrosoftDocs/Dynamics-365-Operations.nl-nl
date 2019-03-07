---
title: Rapportageopties in Talent
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij een klant Dynamics 365 for Talent-rapporten wil aanpassen of nieuwe rapporten wil maken.
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 2007e6adec7255b0b3abda7490c2103a8583393f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "303950"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="a537a-103">Rapportageopties in Talent</span><span class="sxs-lookup"><span data-stu-id="a537a-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a537a-104">**Omgevingsdetails**</span><span class="sxs-lookup"><span data-stu-id="a537a-104">**Environment details**</span></span>

<span data-ttu-id="a537a-105">Dit probleem geldt voor alle omgevingen.</span><span class="sxs-lookup"><span data-stu-id="a537a-105">This issue applies to all environments.</span></span>

<span data-ttu-id="a537a-106">**Symptoom**</span><span class="sxs-lookup"><span data-stu-id="a537a-106">**Symptom**</span></span>

<span data-ttu-id="a537a-107">De klant wil Dynamics 365 for Talent-rapporten aanpassen of nieuwe rapporten maken.</span><span class="sxs-lookup"><span data-stu-id="a537a-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="a537a-108">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="a537a-108">**Issue**</span></span>

<span data-ttu-id="a537a-109">De gebruiker kan de ingesloten Microsoft Power BI-rapporten niet aanpassen.</span><span class="sxs-lookup"><span data-stu-id="a537a-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="a537a-110">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="a537a-110">**Solution**</span></span>

- <span data-ttu-id="a537a-111">De Core HR-gegevens die naar Common Data Service voor Apps stromen, kunnen via de PowerApps CDS-connector naar Power BI Desktop worden gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="a537a-111">The Core HR data that flows to Common Data Service for Apps can be reported on via the PowerApps CDS connector to Power BI Desktop.</span></span> <span data-ttu-id="a537a-112">Common Data Service voor Apps bevat een subset van Core HR-gegevens.</span><span class="sxs-lookup"><span data-stu-id="a537a-112">Note that Common Data Service for Apps contains a subset of Core HR data.</span></span> <span data-ttu-id="a537a-113">Raadpleeg voor meer informatie over Power BI en dashboards [Power BI-rapporten en -dashboards maken met PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="a537a-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="a537a-114">Elektronische rapportage (ER) is beschikbaar voor sommige rapporten in Talent.</span><span class="sxs-lookup"><span data-stu-id="a537a-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="a537a-115">Door de klant gestuurde aanpassingen kunnen worden uitgevoerd via de ER-configuratieopties.</span><span class="sxs-lookup"><span data-stu-id="a537a-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="a537a-116">Gegevens kunnen worden geëxporteerd naar Microsoft Excel of Microsoft Word met behulp van de verschillende gegevensentiteiten die Talent biedt dankzij de integratie met Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="a537a-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="a537a-117">**Langetermijnoplossing**</span><span class="sxs-lookup"><span data-stu-id="a537a-117">**Long-term solution**</span></span>

<span data-ttu-id="a537a-118">Er worden meer Power BI-opties beschikbaar en meer gegevens en entiteiten worden opgenomen in Common Data Service voor Apps.</span><span class="sxs-lookup"><span data-stu-id="a537a-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service for Apps.</span></span>
