---
title: Rapportageopties in Talent
description: In dit onderwerp wordt uitgelegd hoe u het probleem oplost waarbij een klant Dynamics 365 for Talent-rapporten wil aanpassen of nieuwe rapporten wil maken.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7e00a6e4fc01f72e1ef2347e08754997135215ed
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/12/2019
ms.locfileid: "950054"
---
# <a name="reporting-options-in-talent"></a><span data-ttu-id="67985-103">Rapportageopties in Talent</span><span class="sxs-lookup"><span data-stu-id="67985-103">Reporting options in Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="67985-104">**Omgevingsdetails**</span><span class="sxs-lookup"><span data-stu-id="67985-104">**Environment details**</span></span>

<span data-ttu-id="67985-105">Dit probleem geldt voor alle omgevingen.</span><span class="sxs-lookup"><span data-stu-id="67985-105">This issue applies to all environments.</span></span>

<span data-ttu-id="67985-106">**Symptoom**</span><span class="sxs-lookup"><span data-stu-id="67985-106">**Symptom**</span></span>

<span data-ttu-id="67985-107">De klant wil Dynamics 365 for Talent-rapporten aanpassen of nieuwe rapporten maken.</span><span class="sxs-lookup"><span data-stu-id="67985-107">The customer wants to customize Microsoft Dynamics 365 for Talent reports or create new reports.</span></span>

<span data-ttu-id="67985-108">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="67985-108">**Issue**</span></span>

<span data-ttu-id="67985-109">De gebruiker kan de ingesloten Microsoft Power BI-rapporten niet aanpassen.</span><span class="sxs-lookup"><span data-stu-id="67985-109">The user can't customize the embedded Microsoft Power BI reports.</span></span>

<span data-ttu-id="67985-110">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="67985-110">**Solution**</span></span>

- <span data-ttu-id="67985-111">De Core HR-gegevens die naar Common Data Service stromen, kunnen via de PowerApps Common Data Service-connector aan Power BI Desktop worden gerapporteerd.</span><span class="sxs-lookup"><span data-stu-id="67985-111">The Core HR data that flows to Common Data Service can be reported on via the PowerApps Common Data Service connector to Power BI Desktop.</span></span> <span data-ttu-id="67985-112">Common Data Service bevat een subset van Core HR-gegevens.</span><span class="sxs-lookup"><span data-stu-id="67985-112">Note that Common Data Service contains a subset of Core HR data.</span></span> <span data-ttu-id="67985-113">Raadpleeg voor meer informatie over Power BI en dashboards [Power BI-rapporten en -dashboards maken met PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span><span class="sxs-lookup"><span data-stu-id="67985-113">For more information about Power BI and dashboards, see [Create Power BI reports and dashboards with PowerApps Common Data Service](https://powerapps.microsoft.com/en-us/blog/cdsconnectortopowerbi).</span></span>
- <span data-ttu-id="67985-114">Elektronische rapportage (ER) is beschikbaar voor sommige rapporten in Talent.</span><span class="sxs-lookup"><span data-stu-id="67985-114">Electronic reporting (ER) is available for some reports in Talent.</span></span> <span data-ttu-id="67985-115">Door de klant gestuurde aanpassingen kunnen worden uitgevoerd via de ER-configuratieopties.</span><span class="sxs-lookup"><span data-stu-id="67985-115">Customer-driven customizations can be done via the ER configuration options.</span></span>
- <span data-ttu-id="67985-116">Gegevens kunnen worden geëxporteerd naar Microsoft Excel of Microsoft Word met behulp van de verschillende gegevensentiteiten die Talent biedt dankzij de integratie met Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="67985-116">Data can be exported to Microsoft Excel or Microsoft Word by using the various data entities that Talent provides through the Microsoft Office integration.</span></span>

<span data-ttu-id="67985-117">**Langetermijnoplossing**</span><span class="sxs-lookup"><span data-stu-id="67985-117">**Long-term solution**</span></span>

<span data-ttu-id="67985-118">Er worden meer Power BI-opties beschikbaar en meer gegevens en entiteiten worden opgenomen in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="67985-118">Additional Power BI options will be available, and more data and entities will be part of Common Data Service.</span></span>
