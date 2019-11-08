---
title: Restbedrag vereffenen
description: U kunt het resterende bedrag van de vereffeningsactiviteit vereffenen door het toe te passen op een grootboekrekening.
author: mikefalkner
manager: aolson
ms.date: 10/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 6b1b1ddbc8eb8b1d926e68715336edc8e275ff29
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177183"
---
# <a name="settle-remainder"></a><span data-ttu-id="8ffc3-103">Restbedrag vereffenen</span><span class="sxs-lookup"><span data-stu-id="8ffc3-103">Settle remainder</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ffc3-104">U kunt het resterende bedrag van de vereffeningsactiviteit vereffenen door het toe te passen op een grootboekrekening of een andere klant.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-104">You can settle the amount remaining from settlement activity by applying that amount to a ledger account or another customer.</span></span> <span data-ttu-id="8ffc3-105">U kunt de rest vereffenen wanneer u bedragen vereffent die zijn ingevoerd in een journaal of wanneer u alleen openstaande transacties vereffent.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-105">You can settle the remainder when you are settling amounts entered into a journal or when you are only settling open transactions.</span></span>

## <a name="setting-up-defaults"></a><span data-ttu-id="8ffc3-106">Standaardinstellingen opgeven</span><span class="sxs-lookup"><span data-stu-id="8ffc3-106">Setting up defaults</span></span> 
<span data-ttu-id="8ffc3-107">U moet de functie Restbedrag vereffenen inschakelen en de standaardinstellingen instellen voordat u Restbedrag vereffenen gebruikt</span><span class="sxs-lookup"><span data-stu-id="8ffc3-107">You must enable the Settle remainder feature and set up the default settings before you use Settle remainder</span></span>

1)  <span data-ttu-id="8ffc3-108">Klik op **Klanten   > Parameters > Vereffeningen** of **Leveranciers > Parameters > Vereffeningen**</span><span class="sxs-lookup"><span data-stu-id="8ffc3-108">Click **Accounts receivable > Parameters > Settlements** or **Accounts payable > Parameters > Settlements**</span></span>
2)  <span data-ttu-id="8ffc3-109">Selecteer het tabblad **Vereffening** en klik op **Restbedrag vereffenen inschakelen**</span><span class="sxs-lookup"><span data-stu-id="8ffc3-109">Select the **Settlement** tab and click **Enable settle remainder**</span></span>
3)  <span data-ttu-id="8ffc3-110">Selecteer bij **Standaardredencode** een standaardredencode.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-110">In **Default reason code**, select a default reason code.</span></span> <span data-ttu-id="8ffc3-111">De redencodes moeten al zijn ingesteld in **Klanten > Instellingen > Redencodes voor afschrijvingen van klant** of **Leveranciers > Instellingen > Redencodes voor afschrijvingen van klant**.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-111">The reason codes must have already been set up in **Accounts receivable > Setup > Customer write-off reason codes** or **Accounts payable > Setup > Customer write-off reason codes**.</span></span> <span data-ttu-id="8ffc3-112">Bij **Standaardrekening voor restbedrag vereffenen** wordt standaard de rekening ingesteld die is toegewezen aan de redencode voor afschrijving.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-112">The **Default settle remainder account** will default to the account assigned to the write-off reason code.</span></span>
3)  <span data-ttu-id="8ffc3-113">Werk de waarde voor **Standaardrekening voor restbedrag vereffenen** zo nodig bij.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-113">Update the **Default settle remainder account** as needed.</span></span>
4)  <span data-ttu-id="8ffc3-114">Selecteer bij **Standaardjournaalnaam** een betalingsjournaal dat wordt gebruikt als u een betalingsjournaal wilt maken wanneer u alleen openstaande transacties vereffent.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-114">In the **Default journal name**, select a payment journal that will be used if you want to create a payment journal when you only settling open transactions.</span></span> <span data-ttu-id="8ffc3-115">Als u de functie Restbedrag vereffenen inschakelt, moet u een standaardjournaalnaam toevoegen.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-115">If you enable the settle remainder feature, you must add a default journal name.</span></span>

## <a name="settle-remainder-from-a-journal"></a><span data-ttu-id="8ffc3-116">Restbedrag uit een journaal vereffenen</span><span class="sxs-lookup"><span data-stu-id="8ffc3-116">Settle remainder from a journal</span></span>
<span data-ttu-id="8ffc3-117">Als u de functie **Restbedrag vereffenen** niet inschakelt, kunt u nog steeds een transactie invoeren in een journaal en vervolgens transacties hiervoor vereffenen, net als in het verleden.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-117">If you do not enable the **Settle remainder** feature, you can still enter a transaction in a journal and then settle transactions against it as you have done in the past.</span></span> <span data-ttu-id="8ffc3-118">Wanneer u op de knop **OK** klikt, wordt het openstaande saldo op de factuur verminderd met het contante bedrag.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-118">When you click the **OK** button, the open balance on the invoice is reduced by the cash amount.</span></span> <span data-ttu-id="8ffc3-119">Als de factuur niet volledig wordt vereffend met het contante bedrag, blijft de factuur openstaan met een resterend bedrag dat op een later tijdstip moet worden vereffend.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-119">If the cash does not fully settle the invoice, the invoice is left open with a remaining amount to be settled at a later time.</span></span>

<span data-ttu-id="8ffc3-120">Wanneer de functie **Restbedrag vereffenen** is ingeschakeld, kunt u het restbedrag vereffenen naar een grootboekrekening.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-120">When the **Settle remainder** feature is enabled, you can settle the remaining amount to a ledger account.</span></span> <span data-ttu-id="8ffc3-121">U kunt ook de rest overboeken naar een andere klantrekening (voor klanttransacties) of een andere leverancier (voor leverancierstransacties) in plaats van de facturen open te laten.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-121">You can also transfer the remainder to another customer account (for customer transactions) or another vendor (for vendor transactions) instead of leaving the invoices open.</span></span> 

<span data-ttu-id="8ffc3-122">Ga als volgt te werk om de rest te vereffenen via de pagina **Vereffening**:</span><span class="sxs-lookup"><span data-stu-id="8ffc3-122">To settle the remainder from the **Settlement** page, perform the following steps:</span></span>

1)  <span data-ttu-id="8ffc3-123">Markeer op de pagina **Vereffening** de facturen of transacties die u wilt vereffenen.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-123">On the **Settlement** page, mark the invoices or transactions that you want to settle.</span></span>
2)  <span data-ttu-id="8ffc3-124">Klik op de knop **Restbedrag vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-124">Click the **Settle remainder** button.</span></span>
3)  <span data-ttu-id="8ffc3-125">Er wordt een dialoogvenster weergegeven met het bedrag dat wordt vereffend met een grootboekrekening, de datum die wordt gebruikt voor het vereffenen van het restbedrag, de standaardredencode uit de parameters en de standaardrekening uit de parameters.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-125">A dialog box will display, showing the amount that will be settled against a ledger account, the date that will be used to settle the remainder, the default reason code from the parameters, and the default account from the parameters.</span></span> 
4)  <span data-ttu-id="8ffc3-126">Selecteer een nieuwe vereffeningsreden als u de standaardreden wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-126">Select a new settlement reason if you want to change the default reason.</span></span> <span data-ttu-id="8ffc3-127">De vereffeningsrekening wordt gewijzigd in de rekening die is gekoppeld aan de redencode.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-127">The settlement account will be changed to the account associated with the reason code.</span></span>
5)  <span data-ttu-id="8ffc3-128">Bewerk de vereffeningsrekening als u deze wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-128">Edit the settlement account if you want to change it.</span></span>
6)  <span data-ttu-id="8ffc3-129">Als u bij het vereffenen van klanttransacties het restbedrag wilt verplaatsen naar een andere klant, selecteert u een klant bij **Restbedrag vereffenen met klantrekening**.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-129">If you are settling customer transactions and you want the remainder to be moved to another customer, then select a customer in the **Settle remainder against customer account**.</span></span> <span data-ttu-id="8ffc3-130">Als u bij het vereffenen van leverancierstransacties het restbedrag wilt verplaatsen naar een andere leverancier, selecteert u een leverancier bij **Restbedrag vereffenen met leveranciersrekening**.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-130">If you are settling vendor transactions and you want the remainder to be moved to another vendor, then select a vendor in the **Settle remainder against vendor account**.</span></span>
6)  <span data-ttu-id="8ffc3-131">Klik op **Restbedrag vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-131">Click **Settle remainder**.</span></span>
7)  <span data-ttu-id="8ffc3-132">De pagina **Journaal** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-132">The **Journal** page will display.</span></span> <span data-ttu-id="8ffc3-133">Er wordt een extra regel aan het journaal toegevoegd met het resterende vereffeningsbedrag als het bedrag en met de rekening voor het restbedrag als tegenrekening.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-133">An additional journal line will be added to the journal with the settle remainder amount as the amount and with the settlement remainder account as the offset account.</span></span> <span data-ttu-id="8ffc3-134">Als u een klant of leverancier hebt toegevoegd zodat u het vereffeningsbedrag naar een andere klant of leverancier kunt verplaatsen, wordt een extra regel toegevoegd aan het journaal om het vereffeningsbedrag naar die klant of leverancier te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-134">If you added a customer or vendor so that you can move the settlement amount to another customer or vendor, then an additional line will be added to the journal to move the settlement amount to that customer or vendor.</span></span>

<span data-ttu-id="8ffc3-135">Wanneer u het journaal boekt, wordt de openstaande transactie volledig vereffend.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-135">When you post the journal, the open transaction will be fully settled.</span></span> 

## <a name="settle-remainder-when-you-are-only-settling-open-transactions"></a><span data-ttu-id="8ffc3-136">Restant vereffenen wanneer u alleen openstaande transacties vereffent</span><span class="sxs-lookup"><span data-stu-id="8ffc3-136">Settle remainder when you are only settling open transactions</span></span>
<span data-ttu-id="8ffc3-137">U kunt het restant ook vereffenen wanneer u openstaande transacties zonder een journaal vereffent.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-137">You can also settle the remainder when you are settling open transactions without a journal.</span></span>

<span data-ttu-id="8ffc3-138">Ga als volgt te werk om het restant te vereffenen:</span><span class="sxs-lookup"><span data-stu-id="8ffc3-138">To settle the remainder, perform the following steps:</span></span>

1)  <span data-ttu-id="8ffc3-139">Markeer op de pagina **Vereffening** de facturen of transacties die u wilt vereffenen</span><span class="sxs-lookup"><span data-stu-id="8ffc3-139">On the **Settlement** page, mark the invoices or transactions that you want to settle</span></span>
2)  <span data-ttu-id="8ffc3-140">Klik op **Restbedrag vereffenen**</span><span class="sxs-lookup"><span data-stu-id="8ffc3-140">Click on **Settle remainder**</span></span>
3)  <span data-ttu-id="8ffc3-141">Er wordt een dialoogvenster weergegeven met het bedrag dat wordt vereffend met een grootboekrekening, de datum die wordt gebruikt voor het vereffenen van het restbedrag, de standaardredencode uit de parameters en de standaardrekening uit de parameters.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-141">A dialog box will display, showinh the amount that will be settled against a ledger account, the date that will be used to settle the remainder, the default reason code from the parameters, and the default account from the parameters.</span></span> 
4)  <span data-ttu-id="8ffc3-142">Selecteer een nieuwe vereffeningsreden als u de standaardreden wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-142">Select a new settlement reason if you want to change the default reason.</span></span> <span data-ttu-id="8ffc3-143">De vereffeningsrekening wordt gewijzigd in de rekening die is gekoppeld aan de redencode.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-143">The settlement account will be changed to the account associated with the reason code.</span></span>
5)  <span data-ttu-id="8ffc3-144">Bewerk de **vereffeningsrekening** als u deze wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-144">Edit the **settlement account** if you want to change it.</span></span>
6)  <span data-ttu-id="8ffc3-145">Als u bij het vereffenen van klanttransacties het restbedrag wilt verplaatsen naar een andere klant, selecteert u een klant bij **Restbedrag vereffenen met klantrekening**.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-145">If you are settling customer transactions and you want the remainder to be moved to another customer, then select a customer in the **Settle remainder against customer account**.</span></span> <span data-ttu-id="8ffc3-146">Als u bij het vereffenen van leverancierstransacties het restbedrag wilt verplaatsen naar een andere leverancier, selecteert u een leverancier bij **Restbedrag vereffenen met leveranciersrekening**</span><span class="sxs-lookup"><span data-stu-id="8ffc3-146">If you are settling vendor transactions and you want the remainder to be moved to another vendor, then select a vendor in the **Settle remainder against vendor account**</span></span>
7)  <span data-ttu-id="8ffc3-147">U kunt er ook voor kiezen een betalingsjournaal met het restbedrag van de vereffening te maken of dit alleen zonder een journaal boeken.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-147">You can also choose to create a payment journal with the settlement remainder or just post it without a journal.</span></span> <span data-ttu-id="8ffc3-148">Selecteer **Ja** voor **Bewerken in journaal** om een betalingsjournaal te maken.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-148">Select **Yes** for **Edit in journal** to create a payment journal.</span></span> <span data-ttu-id="8ffc3-149">U kunt het door u gemaakte betalingsjournaal bewerken.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-149">You will be able to edit the payment journal that you create.</span></span>
8)  <span data-ttu-id="8ffc3-150">Klik op **Restbedrag vereffenen**.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-150">Click **Settle remainder**.</span></span> <span data-ttu-id="8ffc3-151">Als u ervoor hebt gekozen een journaal te maken, wordt de knop gewijzigd in **Journaal maken**.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-151">If you chose to create a journal, the button will change to **Create journal**.</span></span> <span data-ttu-id="8ffc3-152">Klik in dat geval op **Journaal maken**.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-152">Click **Create journal** instead.</span></span>
9)  <span data-ttu-id="8ffc3-153">Als u een betalingsjournaal hebt gemaakt, wordt de journaalpagina geopend als u op **Restbedrag vereffenen** klikt.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-153">If you created a payment journal, the journal page will open after you click **Settle remainder**.</span></span> <span data-ttu-id="8ffc3-154">Er wordt een regel aan het journaal toegevoegd met het resterende vereffeningsbedrag als het bedrag en met de rekening voor het restbedrag als tegenrekening.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-154">A journal line will be added to the journal with the settle remainder amount as the amount and with the settlement remainder account as the offset account.</span></span> <span data-ttu-id="8ffc3-155">Als u een klant of leverancier hebt toegevoegd zodat u het vereffeningsbedrag naar een andere klant of leverancier kunt verplaatsen, wordt een extra regel toegevoegd aan het journaal om het vereffeningsbedrag naar die klant of leverancier te verplaatsen.</span><span class="sxs-lookup"><span data-stu-id="8ffc3-155">If you added a customer or vendor so that you can move the settlement amount to another customer or vendor, then an additional line will be added to the journal to move the settlement amount to that customer or vendor.</span></span>