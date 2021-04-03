---
title: Semansys XBRL-integratie
description: Deze procedure begeleidt u door het gebruik van Nederlandse functionaliteit om financiële gegevens naar de XML-indeling te exporteren.
author: mrolecki
manager: AnnBe
ms.date: 05/28/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Netherlands
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 34bc7a91ad6c70284ec6ad0d8c94f9ecfe3a8e8b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264961"
---
# <a name="deliver-xbrl-to-the-dutch-regulatory-body-via-semansys-xbrlone"></a><span data-ttu-id="2fec6-103">XBRL aan de Nederlandse regelgevende instantie bezorgen via Semansys XBRLOne</span><span class="sxs-lookup"><span data-stu-id="2fec6-103">Deliver XBRL to the Dutch Regulatory body via Semansys XBRLOne</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2fec6-104">Dit onderwerp begeleidt u door de stappen voor het toewijzen, exporteren en leveren van XBRL (eXtensible Business Reporting Language) aan de Nederlandse regelgevende instantie.</span><span class="sxs-lookup"><span data-stu-id="2fec6-104">This topic walks you through the steps to map, export, and deliver eXtensible Business Reporting Language (XBRL) to the Dutch regulatory body.</span></span>  

<span data-ttu-id="2fec6-105">Het proces op hoog niveau is een proces van systeem naar mens naar systeem.</span><span class="sxs-lookup"><span data-stu-id="2fec6-105">The high-level process is a system-to-human-to-system process.</span></span> <span data-ttu-id="2fec6-106">Het eerste systeem waarvoor dit gevolgen heeft, is Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="2fec6-106">The first system involved is Microsoft Dynamics 365 Finance.</span></span> <span data-ttu-id="2fec6-107">Dit systeem is verantwoordelijk voor het maken van alle benodigde vermeldingen, rekeningschema's en toewijzingen.</span><span class="sxs-lookup"><span data-stu-id="2fec6-107">This system is responsible for creating all the necessary entries, chart of accounts, and mappings.</span></span> <span data-ttu-id="2fec6-108">Nadat dit is voltooid, exporteert een gebruiker de gegevens in de Semansys DataBridge-indeling.</span><span class="sxs-lookup"><span data-stu-id="2fec6-108">After this is complete, a user will export the data into the Semansys DataBridge format.</span></span> <span data-ttu-id="2fec6-109">Deze geëxporteerde gegevens kunnen vervolgens naar de XBRLOne-portal worden geüpload om naar XBRL te worden geconverteerd en vervolgens worden gevalideerd en bij de juiste Nederlandse regelgevende instantie worden afgeleverd.</span><span class="sxs-lookup"><span data-stu-id="2fec6-109">This exported data can then be uploaded into the XBRLOne portal to convert to XBRL, and then validated and delivered to the correct Dutch regulatory body.</span></span> 

<span data-ttu-id="2fec6-110">Voor dit proces zijn de volgende vereisten nodig:</span><span class="sxs-lookup"><span data-stu-id="2fec6-110">The following prerequisites are needed for this process:</span></span>

- <span data-ttu-id="2fec6-111">De rapportgegevens zijn beschikbaar voor toewijzing via Grootboek in Finance.</span><span class="sxs-lookup"><span data-stu-id="2fec6-111">The report data is available for mapping by using the General Ledger in Finance.</span></span>
- <span data-ttu-id="2fec6-112">Kennis van de juiste taxonomie waarvoor u rapporteert en de bevestiging dat u aan een Nederlandse regelgevende instantie levert.</span><span class="sxs-lookup"><span data-stu-id="2fec6-112">Knowledge of the correct taxonomy for which you're reporting and the confirmation that you're delivering to a Dutch regulatory body.</span></span>
- <span data-ttu-id="2fec6-113">Importeer de elektronische rapporteringsconfiguraties **Nederlands XBRL-integratiemodel** en **Semansys XBRL (NL)**.</span><span class="sxs-lookup"><span data-stu-id="2fec6-113">Import **Dutch XBRL integration model** and **Semansys XBRL (NL)** electronic reporting configurations.</span></span>

<span data-ttu-id="2fec6-114">Zie voor meer informatie over het downloaden van ER-configuraties vanuit Microsoft Dynamics Lifecycle Services (LCS) [Elektronische rapportageconfiguraties downloaden van Lifecycle Services](../../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="2fec6-114">For more information about how to download ER configurations from Microsoft Dynamics Lifecycle Services (LCS), see [Download Electronic reporting configurations from Lifecycle Services](../../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

<span data-ttu-id="2fec6-115">In het volgende voorbeeld ziet u welke stappen een gebruiker moet uitvoeren om de gegevens voor een jaarrapport voor 2019 te exporteren.</span><span class="sxs-lookup"><span data-stu-id="2fec6-115">The following example shows the steps needed for a user to export the data for reporting a 2019 annual report.</span></span> 

1. <span data-ttu-id="2fec6-116">Ga naar **Grootboek** > **Periodieke taken** > **Financiële gegevens naar XBRL exporteren**.</span><span class="sxs-lookup"><span data-stu-id="2fec6-116">Go to **General ledger** > **Periodic tasks** > **Export financial data to XBRL**.</span></span>
2. <span data-ttu-id="2fec6-117">Voer een datum in het veld **Begindatum** in.</span><span class="sxs-lookup"><span data-stu-id="2fec6-117">In the **From date** field, enter a date.</span></span> <span data-ttu-id="2fec6-118">Bijvoorbeeld *01/01/2019*.</span><span class="sxs-lookup"><span data-stu-id="2fec6-118">For example, *2019-01-01*.</span></span>  
3. <span data-ttu-id="2fec6-119">Voer een datum in het veld **Einddatum** in.</span><span class="sxs-lookup"><span data-stu-id="2fec6-119">In the **To date** field, enter a date.</span></span> <span data-ttu-id="2fec6-120">Bijvoorbeeld *31/12/2019*.</span><span class="sxs-lookup"><span data-stu-id="2fec6-120">For example, *2019-12-31*.</span></span>
4. <span data-ttu-id="2fec6-121">Voer in het veld **Indelingstoewijzing** de juiste indelingen in.</span><span class="sxs-lookup"><span data-stu-id="2fec6-121">In the **Format mapping** field, enter the correct formats.</span></span>
5. <span data-ttu-id="2fec6-122">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="2fec6-122">Select **OK**.</span></span>

<span data-ttu-id="2fec6-123">U kunt het Semansys DataBridge-indelingspakket nu naar de XBRLOne-portal overdragen voor de volgende stappen in het proces.</span><span class="sxs-lookup"><span data-stu-id="2fec6-123">You can now take the Semansys DataBridge format package to the XBRLOne portal for next steps in the process.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]