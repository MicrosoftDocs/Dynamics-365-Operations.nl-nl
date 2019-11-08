---
title: Overzicht van positieve betalingen
description: Dit artikel bevat info over positieve betalingen die worden gebruikt om een elektronische lijst met cheques te genereren die aan de bank wordt gegeven.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankPositivePaySummary
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 88463
ms.assetid: 1e3a39d3-f9b3-4073-9730-c96a607243e2
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 49fe8369fce599d16134541b1c968727f38ebff9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189632"
---
# <a name="positive-pay-overview"></a><span data-ttu-id="16635-103">Overzicht van positieve betalingen</span><span class="sxs-lookup"><span data-stu-id="16635-103">Positive pay overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16635-104">Dit artikel bevat info over positieve betalingen die worden gebruikt om een elektronische lijst met cheques te genereren die aan de bank wordt gegeven.</span><span class="sxs-lookup"><span data-stu-id="16635-104">This article provides information about positive pay, which is used to generate an electronic list of checks that can be presented to a bank.</span></span> 

<span data-ttu-id="16635-105">U kunt positieve betalingen gebruiken om een elektronische lijst met cheques te genereren die aan de bank wordt gegeven.</span><span class="sxs-lookup"><span data-stu-id="16635-105">Positive pay is used to generate an electronic list of checks that can be presented to a bank.</span></span> <span data-ttu-id="16635-106">Positieve betalingsbestanden kunnen banken helpen fraude te voorkomen.</span><span class="sxs-lookup"><span data-stu-id="16635-106">Positive pay files can help banks prevent check fraud.</span></span> <span data-ttu-id="16635-107">U kunt positief betalen gebruiken om een elektronische lijst met cheques te genereren telkens als cheques worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="16635-107">You set up positive pay to generate an electronic list of checks every time that checks are printed.</span></span> <span data-ttu-id="16635-108">Wanneer een cheque aan de bank wordt voorgelegd, vergelijkt de bank de cheques met een lijst van cheques die eerder werden ingediend.</span><span class="sxs-lookup"><span data-stu-id="16635-108">Then, when a check is presented to the bank, the bank compares the check with the list of checks that you previously submitted.</span></span> <span data-ttu-id="16635-109">Als de cheque overeenkomt met wat de bank op de lijst heeft, keert de bank de cheque uit.</span><span class="sxs-lookup"><span data-stu-id="16635-109">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="16635-110">Als de cheque niet overeenkomt met een cheque in de lijst, gaat de bank de cheque controleren.</span><span class="sxs-lookup"><span data-stu-id="16635-110">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

<span data-ttu-id="16635-111">Positief betalen staat ook bekend als SafePay.</span><span class="sxs-lookup"><span data-stu-id="16635-111">Positive pay is also known as SafePay.</span></span> 

<span data-ttu-id="16635-112">Positieve betalingsbestanden kunnen vertrouwelijke informatie over begunstigden bevatten en chequebedragen.</span><span class="sxs-lookup"><span data-stu-id="16635-112">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="16635-113">Verzeker daarom dat u de juiste beveiligingsmaatregelen treft vanaf de tijd dat bestanden worden gegenereerd, totdat deze door de bank worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="16635-113">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="16635-114">Positief betalen bestanden zijn gedownload volgens de downloadinstructies voor de webbrowser.</span><span class="sxs-lookup"><span data-stu-id="16635-114">Positive pay files are downloaded according to the download instructions for the web browser.</span></span> 

<span data-ttu-id="16635-115">Positieve betalingsbestanden worden gemaakt door gegevensentiteiten te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="16635-115">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="16635-116">Voordat u een positief betalingsbestand genereert, moet u de transformatie-indelingen instellen voor de XML die de gegevens vertaalt in een indeling die de bank kan gebruiken.</span><span class="sxs-lookup"><span data-stu-id="16635-116">Before you generate a positive pay file, you must set up the transformation formats for the XML that translates the data into a format that the bank can consume.</span></span> 

<span data-ttu-id="16635-117">Wijs voor elke bankrekening waarvoor u positieve betalingsinformatie wilt genereren, de positieve betalingsindeling toe.</span><span class="sxs-lookup"><span data-stu-id="16635-117">For each bank account that you want to generate positive pay information for, you must assign the positive pay format.</span></span> <span data-ttu-id="16635-118">Nadat u betalingen genereert, kunt u een positief betalingsbestand genereren voor slechts één rechtspersoon en één bankrekening.</span><span class="sxs-lookup"><span data-stu-id="16635-118">After you generate payments, you can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="16635-119">U kunt ook positieve betalingsbestanden genereren voor meerdere rechtspersonen en bankrekeningen tegelijk.</span><span class="sxs-lookup"><span data-stu-id="16635-119">Alternatively, you can generate positive pay files for multiple legal entities and bank accounts at the same time.</span></span> 

<span data-ttu-id="16635-120">Nadat de cheques betaald zijn die in een positive pay-bestand staan geregistreerd, ontvangt u een bevestigingsnummer van uw bank.</span><span class="sxs-lookup"><span data-stu-id="16635-120">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="16635-121">U kunt het positive pay-bestand dan bevestigen in het systeem.</span><span class="sxs-lookup"><span data-stu-id="16635-121">You can then confirm the positive pay file in the system.</span></span> 

<span data-ttu-id="16635-122">Als u een positief betalingsbestand moet wijzigen, kunt u het intrekken.</span><span class="sxs-lookup"><span data-stu-id="16635-122">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="16635-123">Vervolgens wordt voor elke cheque in het positieve betalingsbestand het veld dat aangeeft of die cheque is opgenomen in een positief betalingsbestand opnieuw ingesteld.</span><span class="sxs-lookup"><span data-stu-id="16635-123">Then, for each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span>

<span data-ttu-id="16635-124">Zie voor meer informatie [Positieve betalingsbestanden instellen en genereren](set-up-generate-positive-pay-files.md).</span><span class="sxs-lookup"><span data-stu-id="16635-124">For more information, see [Set up and generate positive pay files](set-up-generate-positive-pay-files.md).</span></span>


