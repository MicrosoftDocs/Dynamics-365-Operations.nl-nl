---
title: CODA-bankafschrift
description: Dit onderwerp bevat informatie over CODA. Dit is een rapportindeling die in het Belgische elektronische banksysteem wordt gebruikt.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, BankCodaAccountStatement, BankCodaAccountStatementLines, BankCodaParameters, BankCodaTrans, BankCodaTransCategory, BankCodaTransDefTable, BankCodaTransFamily
audience: Application User
ms.reviewer: kfend
ms.custom: 262534
ms.search.region: Belgium
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ae014541bebc253d529665fcd841c571e142d783
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209873"
---
# <a name="coda-bank-statement"></a><span data-ttu-id="cca94-103">CODA-bankafschrift</span><span class="sxs-lookup"><span data-stu-id="cca94-103">CODA bank statement</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cca94-104">Dit onderwerp bevat informatie over CODA. Dit is een rapportindeling die in het Belgische elektronische banksysteem wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="cca94-104">This topic includes information about CODA, which is a report format used in the Belgian electronic banking system.</span></span> 

<span data-ttu-id="cca94-105">Voor importen van Belgische bankoverzichten gebruikt u de CODA-bestandsindeling.</span><span class="sxs-lookup"><span data-stu-id="cca94-105">For Belgian bank statement imports, you'll use the CODA file format.</span></span> <span data-ttu-id="cca94-106">Met deze functie kunt u begin- en eindsaldi van bedrijfsbankrekeningen controleren en kunt u geïmporteerde transacties op basis van afstemmingsregels afstemmen.</span><span class="sxs-lookup"><span data-stu-id="cca94-106">This feature lets you verify company bank account opening and ending balances, and reconcile imported transactions based on reconciliation rules.</span></span>

## <a name="import-transactions-from-a-bank-statement"></a><span data-ttu-id="cca94-107">Transacties van een bankafschrift importeren</span><span class="sxs-lookup"><span data-stu-id="cca94-107">Import transactions from a bank statement</span></span>
<span data-ttu-id="cca94-108">Voer de volgende stappen uit om een bankafschriftbestand voor een bankrekening te importeren.</span><span class="sxs-lookup"><span data-stu-id="cca94-108">To import a bank statement file for a bank account, complete the following steps.</span></span> <span data-ttu-id="cca94-109">**Opmerking**: voordat u een bankafschriftbestand importeert, moet u het volgende al hebben uitgevoerd:</span><span class="sxs-lookup"><span data-stu-id="cca94-109">**Note**: Before you import a bank statement file, you must have already completed the following:</span></span>

-   <span data-ttu-id="cca94-110">De CODA-configuraties vanuit Lifecycle Services (LCS) importeren</span><span class="sxs-lookup"><span data-stu-id="cca94-110">Import the CODA configurations from Lifecycle Services (LCS).</span></span> <span data-ttu-id="cca94-111">Zie voor meer informatie [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="cca94-111">For more information, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>
-   <span data-ttu-id="cca94-112">Selecteer de geïmporteerde CODA-configuratie op de pagina **CODA-parameters**.</span><span class="sxs-lookup"><span data-stu-id="cca94-112">Select the imported CODA configuration on the **CODA parameters** page.</span></span>

1.  <span data-ttu-id="cca94-113">Ga naar de pagina **Bankrekeningen**.</span><span class="sxs-lookup"><span data-stu-id="cca94-113">Go to the **Bank accounts** page.</span></span>
2.  <span data-ttu-id="cca94-114">Klik op **Afstemmen** &gt; **CODA**.</span><span class="sxs-lookup"><span data-stu-id="cca94-114">Click **Reconcile** &gt; **CODA**.</span></span>
3.  <span data-ttu-id="cca94-115">Klik op **CODA** &gt; **Importeren uit bestand** en selecteer vervolgens het pad naar het bankafschriftbestand.</span><span class="sxs-lookup"><span data-stu-id="cca94-115">Click **CODA** &gt; **Import from file**, and then select the path to the bank statement file.</span></span>

<span data-ttu-id="cca94-116">Nadat u transacties hebt geïmporteerd, kunt u het volgende doen op de pagina **Bankafschrift**.</span><span class="sxs-lookup"><span data-stu-id="cca94-116">After you import transactions, you can do the following on the **Bank statement** page.</span></span>

-   <span data-ttu-id="cca94-117">De begin- en eindsaldi controleren.</span><span class="sxs-lookup"><span data-stu-id="cca94-117">Verify the opening and ending balances.</span></span>
-   <span data-ttu-id="cca94-118">De geïmporteerde transacties weergeven als een bankafschriftrapport dat u kunt afdrukken.</span><span class="sxs-lookup"><span data-stu-id="cca94-118">View the imported transactions as a bank statement report that you can print.</span></span>
-   <span data-ttu-id="cca94-119">Geïmporteerde transacties weergeven met extra regels, zoals regels met het rekeningtype 'Geen'.</span><span class="sxs-lookup"><span data-stu-id="cca94-119">View imported transactions with additional lines, such as lines with an Account type of "None".</span></span> <span data-ttu-id="cca94-120">Klik op **CODA &gt; Details**.</span><span class="sxs-lookup"><span data-stu-id="cca94-120">Click **CODA &gt; Details**.</span></span>

## <a name="process-imported-bank-statement-transactions"></a><span data-ttu-id="cca94-121">Geïmporteerde bankafschrifttransacties verwerken</span><span class="sxs-lookup"><span data-stu-id="cca94-121">Process imported bank statement transactions</span></span>
<span data-ttu-id="cca94-122">Voer de volgende stappen uit om de bankafschrifttransacties te verwerken.</span><span class="sxs-lookup"><span data-stu-id="cca94-122">Complete the following steps to process the bank statement transactions.</span></span>

1. <span data-ttu-id="cca94-123">Verwerk detailregels (**CODA** &gt; **Detailregels verwerken**).</span><span class="sxs-lookup"><span data-stu-id="cca94-123">Process details lines (**CODA** &gt; **Process detail lines**).</span></span> <span data-ttu-id="cca94-124">Start automatisch afstemmen op basis van **CODA-definities**.</span><span class="sxs-lookup"><span data-stu-id="cca94-124">Start automatic matching based on **CODA definitions**.</span></span> <span data-ttu-id="cca94-125">Deze regels bepalen welk grootboek of welke klant of leverancier moet worden gebruikt voor deze transactie.</span><span class="sxs-lookup"><span data-stu-id="cca94-125">These rules determine which ledger, customer, or vendor account should be used for this transaction.</span></span> <span data-ttu-id="cca94-126">De vergelijking wordt gebaseerd op welke transactiegroepscode, transactiecode en transactiecategoriecode zijn opgegeven in het CODA-bestand voor elke transactie.</span><span class="sxs-lookup"><span data-stu-id="cca94-126">Comparison is based on which Transaction group code, Transaction code, and Transaction category code are specified in CODA file for each transaction.</span></span>
2. <span data-ttu-id="cca94-127">Transacties met een klant- en leveranciersrekeningtype kunnen worden vergeleken met de facturen.</span><span class="sxs-lookup"><span data-stu-id="cca94-127">Transactions with a customer and vendor account type can be matched with the invoices.</span></span> <span data-ttu-id="cca94-128">Indien nodig kunnen geïmporteerde transacties handmatig op elk gewenst moment na verwerking worden gewijzigd, alvorens ze worden overgeboekt naar het grootboek.</span><span class="sxs-lookup"><span data-stu-id="cca94-128">If necessary, imported transactions can be manually changed at any time after processing, before transferring to the ledger.</span></span>
3. <span data-ttu-id="cca94-129">Als er transacties met fouten zijn (in het algemeen als er geen regels zijn ingesteld), kunnen deze worden verwezen naar de speciale grootboekrekening die is opgegeven op de pagina <strong>CODA-parameters **(</strong>CODA** &gt; <strong>Fouten wissen</strong>).</span><span class="sxs-lookup"><span data-stu-id="cca94-129">If there are any transactions with errors (generally, if there are no rules set up), these can be referred to the special ledger account, specified on the <strong>CODA parameters **page (</strong>CODA** &gt; <strong>Clear errors</strong>).</span></span>
4. <span data-ttu-id="cca94-130">Nadat alle transacties in het bankafschrift zijn vereffend, kunnen ze worden overgeboekt naar het grootboekjournaal (<strong>CODA</strong> &gt;<strong>Overboeken naar grootboek</strong>).</span><span class="sxs-lookup"><span data-stu-id="cca94-130">After all transactions in the bank statement are settled, they are ready to be transferred to the general ledger journal (<strong>CODA</strong> &gt;<strong>Transfer to ledger</strong>).</span></span> <span data-ttu-id="cca94-131">Voor de bankrekening moeten journaalinstellingen worden opgegeven.</span><span class="sxs-lookup"><span data-stu-id="cca94-131">Journal settings should be specified for the bank account.</span></span> <span data-ttu-id="cca94-132">Journalen kunnen worden geopend op de pagina <strong>Bankrekeningen\*\* voor de geselecteerde record door te klikken op \*\*Instellen</strong> &gt; <strong>CODA-journaal</strong>.</span><span class="sxs-lookup"><span data-stu-id="cca94-132">Journals can be opened on the <strong>Bank accounts \*\*page for the selected record by clicking \*\*Set up</strong> &gt; <strong>CODA journal</strong>.</span></span>

<span data-ttu-id="cca94-133">Nadat bankafschrifttransacties zijn verwerkt, wordt een nieuw grootboekjournaal gemaakt en is deze gereed voor boeking.</span><span class="sxs-lookup"><span data-stu-id="cca94-133">After processing bank statement transactions is complete, a new general ledger journal is created and ready for posting.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]