---
title: Instellen van gegevens voor TDS-groep, PAN en TAN voor klanten en leveranciers
description: In dit onderwerp wordt uitgelegd hoe u gegevens kunt instellen over de TDS-groep (belasting ingehouden op bron), het permanente rekeningnummer (PAN) en het belastingrekeningnummer (TAN) voor leveranciers en klanten.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: fd33b1775afefed798f1e9bb7601f4112222c430
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023149"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a><span data-ttu-id="ed5f6-103">Gegevens instellen voor TDS-groep, PAN en TAN voor klanten en leveranciers</span><span class="sxs-lookup"><span data-stu-id="ed5f6-103">TDS group, PAN, and TAN information setup for vendors and customers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed5f6-104">In dit onderwerp wordt uitgelegd hoe u gegevens kunt instellen over de TDS-groep (belasting ingehouden op bron), het permanente rekeningnummer (PAN) en het belastingrekeningnummer (TAN) voor leveranciers en klanten.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-104">This topic explains how to set up information about the Tax Deducted at Source (TDS) group, permanent account number (PAN), and tax account number (TAN) for vendors and customers.</span></span>

1. <span data-ttu-id="ed5f6-105">Ga naar **Leveranciers \> Leveranciers \> Alle leveranciers** of **Klanten \> Klanten \> Alle klanten**.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-105">Go to **Accounts payable \> Vendors \> All vendors** or **Accounts receivable \> Customers \> All customers**.</span></span>

    <span data-ttu-id="ed5f6-106">[![Pagina Alle leveranciers](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span><span class="sxs-lookup"><span data-stu-id="ed5f6-106">[![All vendors page](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)</span></span>

2. <span data-ttu-id="ed5f6-107">Selecteer in het actievenster **Nieuw** om een leverancier of klant te maken en voer de vereiste gegevens in.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-107">On the Action Pane, select **New** to create a vendor or customer, and enter the required details.</span></span> <span data-ttu-id="ed5f6-108">U kunt ook een bestaande leverancier of klant selecteren.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-108">Alternatively, select an existing vendor or customer.</span></span>
3. <span data-ttu-id="ed5f6-109">Stel op het sneltabblad **Factuur en levering** in de sectie **Bronbelasting** de optie **Bronbelasting berekenen** in op **Ja** om bronbelasting, TDS (belasting ingehouden op bron) of TCS (belasting geïnd aan bron) voor de leverancier of klant te berekenen.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-109">On the **Invoice and delivery** FastTab, in the **Withholding tax** section, set the **Calculate withholding tax** option to **Yes** to calculate withholding tax, TDS, or Tax Collected at Source (TCS) for the vendor or customer.</span></span>
4. <span data-ttu-id="ed5f6-110">TDS voor een inkoopfactuur wordt berekend op basis van de standaard-TDS-groep die voor de leverancier of klant is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-110">TDS for a purchase invoice is calculated based on the default TDS group that is defined for the vendor or customer.</span></span> <span data-ttu-id="ed5f6-111">Selecteer de standaardgroep voor TDS in het veld **TDS-groep**.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-111">In the **TDS group** field, select the default TDS group.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ed5f6-112">Wanneer u een TDS-groep selecteert in het veld **TDS-groep**, worden de velden van de **Bronbelastinggroep** en de **TCS-groep** niet meer beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-112">When you select a TDS group in the **TDS group** field, the **Withholding tax group** and **TCS group** fields become unavailable.</span></span>

5. <span data-ttu-id="ed5f6-113">Selecteer in de sectie **PAN-gegevens** van het sneltabblad **Belastinginformatie** in het veld **Status** de status van het permanente rekeningnummer voor de leverancier of klant:</span><span class="sxs-lookup"><span data-stu-id="ed5f6-113">On the **Tax information** FastTab, in the **PAN information** section, in the **Status** field, select the status of the permanent account number for the vendor or customer:</span></span>

    - <span data-ttu-id="ed5f6-114">**Niet beschikbaar**: de leverancier of klant heeft geen PAN.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-114">**Not available** – The vendor or customer doesn't have a PAN.</span></span>
    - <span data-ttu-id="ed5f6-115">**Ontvangen**: de leverancier of klant heeft een PAN.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-115">**Received** – The vendor or customer has a PAN.</span></span>
    - <span data-ttu-id="ed5f6-116">**Aangevraagd**: de leverancier of klant heeft een PAN aangevraagd.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-116">**Applied** – The vendor or customer has applied for a PAN.</span></span>
    - <span data-ttu-id="ed5f6-117">**Ongeldig**: de leverancier of klant heeft een PAN, maar deze is niet geldig.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-117">**Invalid** – The vendor or customer has a PAN, but it isn't valid.</span></span>

6. <span data-ttu-id="ed5f6-118">Als u **Ontvangen** hebt geselecteerd in het veld **Status** om aan te geven dat de leverancier of klant een PAN heeft, voert u de PAN in het veld **Nummer** in.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-118">If you selected **Received** in the **Status** field to indicate that the vendor or customer has a PAN, enter the PAN in the **Number** field.</span></span> <span data-ttu-id="ed5f6-119">De PAN moet bestaan uit vijf alfabetische tekens, vervolgens vier numerieke tekens en daarna één alfabetisch teken.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-119">The PAN must consist of five alphabetic characters, then four numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="ed5f6-120">Dit is een voorbeeld: **ABCDE1260A**.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-120">Here is an example: **ABCDE1260A**.</span></span>
7. <span data-ttu-id="ed5f6-121">Als u **Aangevraagd** hebt geselecteerd in het veld **Status** om aan te geven dat de leverancier of klant een PAN heeft aangevraagd, voert u het verwijzingsnummer in het veld **Verwijzingsnummer** in.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-121">If you selected **Applied** in the **Status** field to indicate that the vendor or customer has applied for PAN, enter the reference number in the **Reference number** field.</span></span>
8. <span data-ttu-id="ed5f6-122">Selecteer in het veld **Soort belastingplichtige** de soort belastingplichtige waar de leverancier of klant toe hoort:</span><span class="sxs-lookup"><span data-stu-id="ed5f6-122">In the **Nature of assessee** field, select the nature of assessee category that the vendor or customer belongs to:</span></span>

    - <span data-ttu-id="ed5f6-123">Bedrijf</span><span class="sxs-lookup"><span data-stu-id="ed5f6-123">Company</span></span>
    - <span data-ttu-id="ed5f6-124">HUF</span><span class="sxs-lookup"><span data-stu-id="ed5f6-124">HUF</span></span>
    - <span data-ttu-id="ed5f6-125">Firma</span><span class="sxs-lookup"><span data-stu-id="ed5f6-125">Firm</span></span>
    - <span data-ttu-id="ed5f6-126">Afzonderlijk</span><span class="sxs-lookup"><span data-stu-id="ed5f6-126">Individual</span></span>
    - <span data-ttu-id="ed5f6-127">AOP</span><span class="sxs-lookup"><span data-stu-id="ed5f6-127">AOP</span></span>
    - <span data-ttu-id="ed5f6-128">BOI</span><span class="sxs-lookup"><span data-stu-id="ed5f6-128">BOI</span></span>
    - <span data-ttu-id="ed5f6-129">Lokale dienst</span><span class="sxs-lookup"><span data-stu-id="ed5f6-129">Local authority</span></span>
    - <span data-ttu-id="ed5f6-130">Andere</span><span class="sxs-lookup"><span data-stu-id="ed5f6-130">Others</span></span>

    <span data-ttu-id="ed5f6-131">[![Sneltabblad Belastinginformatie](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span><span class="sxs-lookup"><span data-stu-id="ed5f6-131">[![Tax information FastTab](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)</span></span>

9. <span data-ttu-id="ed5f6-132">Selecteer vervolgens in het actievenster op het tabblad **Leverancier** in de groep **Registratie** de optie **Registratie-id's** om de pagina **Adressen beheren** te openen.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-132">On the Action Pane, on the **Vendor** tab, in the **Registration** group, select **Registration IDs** to open the **Manage addresses** page.</span></span>
10. <span data-ttu-id="ed5f6-133">Selecteer op de pagina **Adressen beheren** op het sneltabblad **Belastinginformatie** de optie **Toevoegen** of **Bewerken** om de pagina **Belastinginformatie beheren** te openen, waar u de belastingregistratie-invoer kunt onderhouden.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-133">On the **Manage addresses** page, on the **Tax information** FastTab, select **Add** or **Edit** to open the **Manage tax information** page, where you can maintain the tax registration entry.</span></span>
11. <span data-ttu-id="ed5f6-134">Voer op de pagina **Belastinginformatie beheren** op het sneltabblad **Bronbelasting** in het veld **Belastingrekeningnummer (TAN)** het TAN in.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-134">On the **Manage tax information** page, on the **Withholding tax** FastTab, in the **Tax Account Number (TAN)** field, enter the TAN.</span></span> <span data-ttu-id="ed5f6-135">De TAN moet bestaan uit vier alfabetische tekens, vervolgens vijf numerieke tekens en daarna één alfabetisch teken.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-135">The TAN must consist of four alphabetic characters, then five numeric characters, and then one alphabetic character.</span></span> <span data-ttu-id="ed5f6-136">Dit is een voorbeeld: **AFGH54821T**.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-136">Here is an example: **AFGH54821T**.</span></span>
12. <span data-ttu-id="ed5f6-137">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="ed5f6-137">Close the page.</span></span>
