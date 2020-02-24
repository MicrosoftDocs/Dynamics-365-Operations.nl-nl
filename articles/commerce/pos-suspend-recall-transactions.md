---
title: Een transactie uitstellen en hervatten in het verkooppunt (POS)
description: In dit onderwerp wordt beschreven hoe gebruikers transacties in uitvoering kunnen uitstellen en later of op een andere kassa kunnen hervatten met Dynamics 365 Commerce.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: f513e2d857908f2b95d27bf48ff1e826724d7cbf
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022182"
---
# <a name="suspend-and-resume-a-transaction-in-the-point-of-sale-pos"></a><span data-ttu-id="84133-103">Een transactie uitstellen en hervatten in het verkooppunt (POS)</span><span class="sxs-lookup"><span data-stu-id="84133-103">Suspend and resume a transaction in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="84133-104">POS-gebruikers kunnen transacties in uitvoering uitstellen en deze later of op een andere kassa hervatten.</span><span class="sxs-lookup"><span data-stu-id="84133-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="84133-105">Transacties worden vaak uitgesteld om snel een kassa vrij te maken voor een andere taak zonder de voortgang van de huidige transactie te verliezen.</span><span class="sxs-lookup"><span data-stu-id="84133-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="84133-106">Stel, een winkelmedewerker begint de transactie van een klant te verwerken op een mobiel apparaat, maar moet de transactie voltooien op een kassa met een kassalade.</span><span class="sxs-lookup"><span data-stu-id="84133-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="84133-107">In dat geval kan de winkelmedewerker de transactie uitstellen op het mobiele apparaat en vervolgens ophalen en hervatten op een kassa.</span><span class="sxs-lookup"><span data-stu-id="84133-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="84133-108">Functie voor onderbreken en hervatten configureren</span><span class="sxs-lookup"><span data-stu-id="84133-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="84133-109">POS-bewerkingen</span><span class="sxs-lookup"><span data-stu-id="84133-109">POS operations</span></span>

<span data-ttu-id="84133-110">Met twee [POS-bewerkingen](pos-operations.md) kan het POS ondersteuning bieden voor uitstel- en hervatscenario's.</span><span class="sxs-lookup"><span data-stu-id="84133-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="84133-111">U kunt deze bewerkingen toewijzen aan [knoppenrasters](pos-screen-layouts.md) op de transactie- of welkomstpagina.</span><span class="sxs-lookup"><span data-stu-id="84133-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="84133-112">503: Transactie uitstellen</span><span class="sxs-lookup"><span data-stu-id="84133-112">503: Suspend transaction</span></span>
- <span data-ttu-id="84133-113">504: Transactie intrekken (ophalen)</span><span class="sxs-lookup"><span data-stu-id="84133-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="84133-114">Ontvangstsjabloon</span><span class="sxs-lookup"><span data-stu-id="84133-114">Receipt template</span></span>

<span data-ttu-id="84133-115">Het POS kan zo worden geconfigureerd dat er een afgedrukte pakbon wordt gegenereerd wanneer een transactie wordt uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="84133-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="84133-116">Die pakbon kan vervolgens worden gebruikt om de transactie later snel te identificeren en op te halen.</span><span class="sxs-lookup"><span data-stu-id="84133-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="84133-117">Als u het POS in staat wilt stellen een pakbon af te drukken, moet u de ontvangstbewijsindeling **Uitgestelde transactie** toevoegen aan het ontvangstbewijsprofiel van de de winkel.</span><span class="sxs-lookup"><span data-stu-id="84133-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="84133-118">U kunt de ontvangstbewijsindeling zo ontwerpen dat deze specifieke details over de transactie bevat of uitsluit.</span><span class="sxs-lookup"><span data-stu-id="84133-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="84133-119">De indeling kan bijvoorbeeld een streepjescode omvatten om scannen te ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="84133-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="84133-120">Ontvangstbewijsnummering</span><span class="sxs-lookup"><span data-stu-id="84133-120">Receipt numbering</span></span>

<span data-ttu-id="84133-121">Zoals voor andere POS-transactietypen die een afgedrukt ontvangstbewijs genereren, kunt u een nummerreeks voor uitgestelde transacties opgeven in de sectie **Ontvangstbewijsnummering** van het functionaliteitsprofiel van de winkel.</span><span class="sxs-lookup"><span data-stu-id="84133-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="84133-122">Ongeldig maken bij sluiten van dienst</span><span class="sxs-lookup"><span data-stu-id="84133-122">Void when closing shift</span></span>

<span data-ttu-id="84133-123">U kunt de optie **Ongeldig maken bij sluiten van dienst** gebruiken om te vereisen dat gebruikers uitgestelde transacties voltooien of ongeldig maken voordat ze hun dienst sluiten.</span><span class="sxs-lookup"><span data-stu-id="84133-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="84133-124">Tijdens de bewerking **Ploeg sluiten** moeten gebruikers aangeven of ze eventueel openstaande uitgestelde transacties willen annuleren of weergeven.</span><span class="sxs-lookup"><span data-stu-id="84133-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="84133-125">Een transacties uitstellen en hervatten</span><span class="sxs-lookup"><span data-stu-id="84133-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="84133-126">Een transactie uitstellen</span><span class="sxs-lookup"><span data-stu-id="84133-126">Suspend a transaction</span></span>

<span data-ttu-id="84133-127">Gebruikers die over voldoende bevoegdheden beschikken en een schermindeling met de bewerking **Transactie uitstellen** gebruiken, kunnen een transactie uitstellen zodat deze later of op een andere kassa kan worden opgehaald.</span><span class="sxs-lookup"><span data-stu-id="84133-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="84133-128">Transacties kunnen alleen worden uitgesteld als deze **niet** de volgende soorten regels bevatten:</span><span class="sxs-lookup"><span data-stu-id="84133-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="84133-129">Actieve betalingsregels</span><span class="sxs-lookup"><span data-stu-id="84133-129">Active payment lines</span></span>
- <span data-ttu-id="84133-130">Geschenkbonregels (om een geschenkbon uit te geven of toe te voegen aan het geschenkbonsaldo)</span><span class="sxs-lookup"><span data-stu-id="84133-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="84133-131">Een uitgestelde transactie heeft geen invloed op verkoopgegevens of voorraadbeschikbaarheidsgegevens voor de winkel.</span><span class="sxs-lookup"><span data-stu-id="84133-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="84133-132">Een uitgestelde transactie hervatten</span><span class="sxs-lookup"><span data-stu-id="84133-132">Resume a suspended transaction</span></span>

<span data-ttu-id="84133-133">Uitgestelde transacties kunnen worden opgehaald en hervat op dezelfde locatie door elke gebruiker die over voldoende bevoegdheden beschikt en een indeling met de bewerking **Transactie intrekken** gebruikt.</span><span class="sxs-lookup"><span data-stu-id="84133-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="84133-134">Scan de streepjescode op de afgedrukte pakbon terwijl u de lijst met transacties vanuit de bewerking **Transactie intrekken** bekijkt om snel en eenvoudig een uitgestelde transactie op te halen.</span><span class="sxs-lookup"><span data-stu-id="84133-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="84133-135">Overwegingen voor offlinemodus</span><span class="sxs-lookup"><span data-stu-id="84133-135">Considerations for offline mode</span></span>

- <span data-ttu-id="84133-136">Een transactie die wordt uitgesteld terwijl het POS online is, kan niet worden hervat in de offlinemodus omdat de gegevens niet zijn gesynchroniseerd met de offlinedatabase.</span><span class="sxs-lookup"><span data-stu-id="84133-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="84133-137">Als u een transactie uitstelt terwijl het POS offline is, kunt u deze ophalen in de offlinemodus, mits het POS niet online is gezet sinds u de transactie hebt uitgesteld.</span><span class="sxs-lookup"><span data-stu-id="84133-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="84133-138">Zodra het POS weer online is, worden gegevens over uitgestelde transacties verplaatst naar de onlinedatabase en uit de offlinedatabase verwijderd.</span><span class="sxs-lookup"><span data-stu-id="84133-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="84133-139">De transacties kunnen daarom alleen in de onlinemodus worden hervat.</span><span class="sxs-lookup"><span data-stu-id="84133-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="84133-140">Als u de offlinemodus weer inschakelt voor het POS, kunt u deze uitgestelde transactie niet hervatten omdat ze al zijn verwijderd uit de offlinedatabase.</span><span class="sxs-lookup"><span data-stu-id="84133-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="84133-141">Een uitgestelde transactie ongeldig maken</span><span class="sxs-lookup"><span data-stu-id="84133-141">Void a suspended transaction</span></span>

<span data-ttu-id="84133-142">U kunt een uitgestelde transactie ongeldig maken door de transactie op te halen en vervolgens de bewerking **Ongeldig gemaakte transactie** uit te voeren of door de transactie te selecteren in de lijst **Transactie intrekken** en **Annuleren** te selecteren op de appbalk.</span><span class="sxs-lookup"><span data-stu-id="84133-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="84133-143">De winkel kan ook zo worden geconfigureerd dat gebruikers wordt gevraagd om uitgestelde transacties ongeldig te maken wanneer ze hun dienst sluiten.</span><span class="sxs-lookup"><span data-stu-id="84133-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>
