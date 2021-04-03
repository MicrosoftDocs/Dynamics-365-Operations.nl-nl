---
title: Betalingsbonrapport voor Europa
description: Dit onderwerp bevat informatie over betalingsbonrapporten voor Europa.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMLegalEntities, ProjFormletterParameters, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 264604
ms.search.region: Belgium, Denmark, Finland, Norway, Switzerland
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 31cff0eca98aa04f8813eebdae345f05b286894e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258178"
---
# <a name="payment-slip-report-for-europe"></a><span data-ttu-id="a28d6-103">Betalingsbonrapport voor Europa</span><span class="sxs-lookup"><span data-stu-id="a28d6-103">Payment slip report for Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a28d6-104">Dit onderwerp bevat informatie over betalingsbonrapporten voor Europa.</span><span class="sxs-lookup"><span data-stu-id="a28d6-104">This topic provides information about payment slip reports for Europe.</span></span>

<span data-ttu-id="a28d6-105">De functionaliteit voor betalingsbonrapporten is beschikbaar voor rechtspersonen die hun primaire adres in Denemarken, België, Zwitserland, Noorwegen of Finland hebben.</span><span class="sxs-lookup"><span data-stu-id="a28d6-105">The functionality for payment slip reports is available for legal entities that have their primary address in Denmark, Belgium, Norway, Switzerland, or Finland.</span></span> <span data-ttu-id="a28d6-106">Om klanten van dienst te zijn koppelen bedrijven vaak afgedrukte betalingsbonnen aan facturen en leveren een betalingsverwijzing voor het boeken en vereffenen.</span><span class="sxs-lookup"><span data-stu-id="a28d6-106">Businesses often attach printed payment slips to invoices to provide a payment reference for posting and settlement.</span></span> <span data-ttu-id="a28d6-107">De betalingsbon kan naast verkoopfacturen en vrije-tekstfacturen worden gebruikt voor project- of servicefacturen, aanmaningen, rentenota's en rekeningoverzichten.</span><span class="sxs-lookup"><span data-stu-id="a28d6-107">The payment slip can be used for project or service invoices, collection letters, interest notes, and account statements, in addition to sales invoices and free text invoices.</span></span>

## <a name="set-up-a-creditor-id-number-denmark-only"></a><span data-ttu-id="a28d6-108">Een crediteur-ID-nummer instellen (alleen Denemarken)</span><span class="sxs-lookup"><span data-stu-id="a28d6-108">Set up a creditor ID number (Denmark only)</span></span>
<span data-ttu-id="a28d6-109">Voer de volgende stappen uit om het crediteur-ID-nummer van uw bedrijf in te voeren.</span><span class="sxs-lookup"><span data-stu-id="a28d6-109">Follow these steps to enter your company's creditor identification (ID) number.</span></span> <span data-ttu-id="a28d6-110">Uw financiële instelling verstrekt dit nummer.</span><span class="sxs-lookup"><span data-stu-id="a28d6-110">Your financial institution provides this number.</span></span> <span data-ttu-id="a28d6-111">Dit nummer wordt gebruikt als verwijzing wanneer klantbetalingen via financiële instellingen worden ontvangen.</span><span class="sxs-lookup"><span data-stu-id="a28d6-111">It's used as a reference when customer payments are received through financial institutions.</span></span>

1.  <span data-ttu-id="a28d6-112">Klik op **Organisatiebeheer** &gt; **Instellen** &gt; **Organisatie** &gt; **Rechtspersonen**.</span><span class="sxs-lookup"><span data-stu-id="a28d6-112">Click **Organization administration** &gt; **Setup** &gt; **Organization** &gt; **Legal entities**.</span></span>
2.  <span data-ttu-id="a28d6-113">Voer op het sneltabblad **Bankrekeninggegevens** in het veld **FI-crediteur-ID** uw unieke achtcijferige crediteur-ID-nummer in.</span><span class="sxs-lookup"><span data-stu-id="a28d6-113">On the **Bank account information** FastTab, in the **FI-Creditor ID** field, enter your unique eight-digit creditor ID number.</span></span>
3.  <span data-ttu-id="a28d6-114">Sluit het formulier om de wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="a28d6-114">Close the form to save your changes.</span></span>

## <a name="set-up-a-payment-slip-attachment-format-for-invoices-interest-notes-collection-letters-and-account-statements"></a><span data-ttu-id="a28d6-115">Een betalingsbonbijlage-indeling voor facturen, rentenota's, aanmaningen en overzichten instellen</span><span class="sxs-lookup"><span data-stu-id="a28d6-115">Set up a payment slip attachment format for invoices, interest notes, collection letters, and account statements</span></span>
<span data-ttu-id="a28d6-116">Voer de volgende stappen uit om indeling voor betalingsbonbijlagen in te stellen die worden bijgevoegd bij verkoopfacturen, vrije-tekstfacturen, rentenota's, aanmaningen en rekeningoverzichten.</span><span class="sxs-lookup"><span data-stu-id="a28d6-116">Follow these steps to set up a format for payment slip attachments that accompany sales invoices, free text invoices, interest notes, collection letters, and account statements.</span></span>

1.  <span data-ttu-id="a28d6-117">Klik op **Klanten** &gt; **Instellen** &gt; **Formulieren** &gt; **Formulierinstelling**.</span><span class="sxs-lookup"><span data-stu-id="a28d6-117">Click **Accounts receivable** &gt; **Setup** &gt; **Forms** &gt; **Form setup**.</span></span>
2.  <span data-ttu-id="a28d6-118">Selecteer op het tabblad **Factuur** in het veld **Bijlage 'gekoppelde betaling' bij klantfactuur** de indeling voor betalingsbonbijlagen in.</span><span class="sxs-lookup"><span data-stu-id="a28d6-118">On the **Invoice** tab, in the **Associated payment attachment on customer invoice** field, select the payment slip attachment format.</span></span>
3.  <span data-ttu-id="a28d6-119">Selecteer op de tabbladen **Vrije-tekstfactuur**, **Rentenota**, **Aanmaning** en **Rekeningoverzicht** een indeling voor betalingsbonbijlagen voor elk documenttype.</span><span class="sxs-lookup"><span data-stu-id="a28d6-119">On the **Free text invoice**, **Interest note**, **Collection letter**, and **Account statement** tabs, select a payment slip attachment format for each document type.</span></span>
4.  <span data-ttu-id="a28d6-120">Sluit het formulier om de wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="a28d6-120">Close the form to save your changes.</span></span>

<span data-ttu-id="a28d6-121">Voer de volgende stappen uit om een indeling voor betalingsbonbijlagen in te stellen die bij projectfacturen worden bijgevoegd.</span><span class="sxs-lookup"><span data-stu-id="a28d6-121">Follow these steps to set up a format for payment slip attachments that accompany project invoices.</span></span>

1.  <span data-ttu-id="a28d6-122">Klik op **Projectbeheer en boekhouding** &gt; **Instellen** &gt; **Formulieren** &gt; **Formulierinstelling**.</span><span class="sxs-lookup"><span data-stu-id="a28d6-122">Click **Project management and accounting** &gt; **Setup** &gt; **Forms** &gt; **Form setup**.</span></span>
2.  <span data-ttu-id="a28d6-123">Selecteer in het veld **Bijlage gekoppelde betaling** de indeling voor betalingsbonbijlagen.</span><span class="sxs-lookup"><span data-stu-id="a28d6-123">In the **Associated payment attachment** field, select the payment slip attachment format.</span></span>

## <a name="assign-a-payment-slip-attachment-format-to-a-customer-account"></a><span data-ttu-id="a28d6-124">Een indeling voor een betalingsbonbijlage aan een klantrekening toewijzen</span><span class="sxs-lookup"><span data-stu-id="a28d6-124">Assign a payment slip attachment format to a customer account</span></span>
<span data-ttu-id="a28d6-125">Nadat u de indeling voor betalingsbonbijlagen hebt ingesteld voor verkoopfacturen, vrije-tekstfacturen, rentenota's, aanmaningen, projectfacturen en rekeningoverzichten, kunt u specifieke indelingen voor een geselecteerde klant toewijzen.</span><span class="sxs-lookup"><span data-stu-id="a28d6-125">After you set up the payment slip attachment format for sales invoices, free text invoices, interest notes, collection letters, account statements, and project invoices, you can assign specific formats for a selected customer.</span></span>

1.  <span data-ttu-id="a28d6-126">Klik op **Klanten** &gt; **Algemeen** &gt; **Klanten** &gt; **Alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="a28d6-126">Click **Accounts receivable** &gt; **Common** &gt; **Customers** &gt; **All customers**.</span></span>
2.  <span data-ttu-id="a28d6-127">Maak een nieuwe klant of selecteer een bestaande klant.</span><span class="sxs-lookup"><span data-stu-id="a28d6-127">Create a new customer, or select an existing customer.</span></span>
3.  <span data-ttu-id="a28d6-128">Selecteer op het sneltabblad **Factuur en levering** in de velden **Op een klantfactuur**, **Op een vrije-tekstfactuur**, **Op een rentenota**, **Op een aanmaning**, **Op een projectfactuur** en **Op een rekeningoverzicht** de indeling voor betalingsbonbijlagen die worden bijgevoegd bij documenten van elk willekeurig type, die worden verzonden naar de geselecteerde klant.</span><span class="sxs-lookup"><span data-stu-id="a28d6-128">On the **Invoice and delivery** FastTab, in the **On a customer invoice**, **On a free text invoice**, **On an interest note**, **On a collection letter**, **On a project invoice**, and **On an account statement** fields, select the format for payment slip attachments that will accompany documents of each type that are sent to the selected customer.</span></span>
4.  <span data-ttu-id="a28d6-129">Sluit het formulier om de wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="a28d6-129">Close the form to save your changes.</span></span>






[!INCLUDE[footer-include](../../includes/footer-banner.md)]