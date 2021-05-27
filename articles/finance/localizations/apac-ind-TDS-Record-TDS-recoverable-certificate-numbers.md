---
title: Certificaatnummers voor terugvorderbare TDS registreren
description: In dit onderwerp wordt uitgelegd hoe u de pagina Certificaten voor terugvordering kunt gebruiken om de nummers en datums voor TDS-certificaten te registreren die zijn ontvangen voor een bepaalde leverancier, klant of grootboek.
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023134"
---
# <a name="record-tds-recoverable-certificate-numbers"></a><span data-ttu-id="88f96-103">Certificaatnummers voor terugvorderbare TDS registreren</span><span class="sxs-lookup"><span data-stu-id="88f96-103">Record TDS recoverable certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="88f96-104">In dit onderwerp wordt uitgelegd hoe u de pagina **Certificaten voor terugvordering** kunt gebruiken om de nummers en datums voor TDS-certificaten te registreren die zijn ontvangen voor een bepaalde leverancier, klant of grootboek.</span><span class="sxs-lookup"><span data-stu-id="88f96-104">This topic explains how to use the **Recoverable certificates** page to record the certificate numbers and dates for Tax Deducted at Source (TDS) certificates that are received for a specific vendor, customer, or ledger.</span></span> <span data-ttu-id="88f96-105">Als u de TDS-certificaatnummers en -datums die zijn geregistreerd voor TDS-transacties op deze pagina wilt bijwerken, gebruikt u de pagina **Certificaat bijwerken** (**Grootboek \> Periodiek \> Bronbelasting \> Certificaat bijwerken**).</span><span class="sxs-lookup"><span data-stu-id="88f96-105">To update the TDS certificate numbers and dates that are recorded for TDS transactions on this page, use the **Update certificate** page (**General ledger \> Periodic \> Withholding tax \> Update certificate**).</span></span> <span data-ttu-id="88f96-106">Wanneer u klaar bent met het bijwerken van TDS-certificaatnummers, sluit u deze.</span><span class="sxs-lookup"><span data-stu-id="88f96-106">After you've finished updating TDS certificate numbers, close them.</span></span>

<span data-ttu-id="88f96-107">Volg deze stappen om de certificaatnummers en -datums voor TDS te registreren.</span><span class="sxs-lookup"><span data-stu-id="88f96-107">Follow these steps to record the TDS certificate numbers and dates.</span></span>

1. <span data-ttu-id="88f96-108">Ga naar **Belasting \> Indirecte belasting \> Bronbelasting \> Certificaten voor terugvordering**.</span><span class="sxs-lookup"><span data-stu-id="88f96-108">Go to **Tax \> Indirect tax \> Withholding tax \> Recoverable certificates**.</span></span>

    <span data-ttu-id="88f96-109">[![Pagina Certificaten voor terugvordering](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span><span class="sxs-lookup"><span data-stu-id="88f96-109">[![Recoverable certificates page](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span></span> 

2. <span data-ttu-id="88f96-110">Selecteer **TDS** in het veld **Belastingtype** op de pagina **Certificaten voor terugvordering**.</span><span class="sxs-lookup"><span data-stu-id="88f96-110">On the **Recoverable certificates** page, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="88f96-111">Selecteer **Nieuw** om een record te maken.</span><span class="sxs-lookup"><span data-stu-id="88f96-111">Select **New** to create a record.</span></span>
4. <span data-ttu-id="88f96-112">Voer in het veld **Certificaatnummer** het TDS-certificaatnummer in.</span><span class="sxs-lookup"><span data-stu-id="88f96-112">In the **Certificate number** field, enter the TDS certificate number.</span></span>
5. <span data-ttu-id="88f96-113">Selecteer in het veld **Rekeningtype** het type rekening waar het TDS-certificaat voor wordt ontvangen: **Leverancier**, **Klant** of **Grootboek**.</span><span class="sxs-lookup"><span data-stu-id="88f96-113">In the **Account type** field, select the type of account that the TDS certificate is received for: **Vendor**, **Customer**, or **Ledger**.</span></span>
6. <span data-ttu-id="88f96-114">Selecteer in het veld **Rekening** het rekeningnummer van de leverancier, de klant of het grootboek, afhankelijk van het rekeningtype dat u hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="88f96-114">In the **Account** field, select the vendor, customer, or ledger account number, depending on the account type that you selected.</span></span> <span data-ttu-id="88f96-115">Het veld **Naam** geeft de naam van de leveranciers-, klant- of grootboekrekening weer.</span><span class="sxs-lookup"><span data-stu-id="88f96-115">The **Name** field shows the name of the vendor, customer, or ledger account.</span></span>
7. <span data-ttu-id="88f96-116">Voer in het veld **Certificaatbedrag** het bedrag in voor het TDS-certificaat.</span><span class="sxs-lookup"><span data-stu-id="88f96-116">In the **Certificate amount** field, enter the amount of the TDS certificate.</span></span>
8. <span data-ttu-id="88f96-117">Voer in het veld **Datum** de certificaatdatum in voor het certificaatnummer.</span><span class="sxs-lookup"><span data-stu-id="88f96-117">In the **Date** field, enter the certificate date for the certificate number.</span></span>
9. <span data-ttu-id="88f96-118">Selecteer **Aanvragen** om de pagina **Certificaattransacties te openen**, waar u de TDS-transacties kunt bekijken waarvoor het TDS-certificaatnummer en de TDS-datum zijn bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="88f96-118">Select **Inquiries** to open the **Certificate transactions** page, where you can view the TDS transactions that the TDS certificate number and date are updated for.</span></span> <span data-ttu-id="88f96-119">Deze informatie kan worden bijgewerkt op de pagina **Certificaat bijwerken** (**Belasting \> Aangiften \> Bronbelasting \> Certificaat bijwerken**).</span><span class="sxs-lookup"><span data-stu-id="88f96-119">This information can be updated on the **Update certificate** page (**Tax \> Declarations \> Withholding tax \> Update certificate**).</span></span>

    <span data-ttu-id="88f96-120">Op de pagina **Certificaat bijwerken** wordt de volgende informatie voor elke TDS-transactie weergegeven:</span><span class="sxs-lookup"><span data-stu-id="88f96-120">The **Update certificate** page shows the following information for each TDS transaction:</span></span>

    - <span data-ttu-id="88f96-121">**Datum**: de boekingsdatum van de TDS-transactie.</span><span class="sxs-lookup"><span data-stu-id="88f96-121">**Date** – The posting date of the TDS transaction.</span></span>
    - <span data-ttu-id="88f96-122">**Boekstuk**: het boekstuknummer van de TDS-transactie.</span><span class="sxs-lookup"><span data-stu-id="88f96-122">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="88f96-123">**Bron**: de module waarin de TDS-transactie is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="88f96-123">**Source** – The module that the TDS transaction was created in.</span></span>
    - <span data-ttu-id="88f96-124">**Rekening**: het leveranciers-, klant- of grootboekrekeningnummer waarvoor de TDS-transactie is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="88f96-124">**Account** – The vendor, customer, or ledger account number that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="88f96-125">**Naam**: de naam van de leveranciers-, klant- of grootboekrekening waarvoor de TDS-transactie is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="88f96-125">**Name** – The name of the vendor, customer, or ledger account that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="88f96-126">**Bedrag**: het factuurbedrag waarover de TDS is berekend.</span><span class="sxs-lookup"><span data-stu-id="88f96-126">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="88f96-127">**Belastingbedrag**: het TDS-belastingbedrag dat voor de transactie is berekend.</span><span class="sxs-lookup"><span data-stu-id="88f96-127">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>
    - <span data-ttu-id="88f96-128">**Certificaatdatum**: de datum van het TDS-certificaat die is bijgewerkt voor de TDS-transactie.</span><span class="sxs-lookup"><span data-stu-id="88f96-128">**Certificate date** – The TDS certificate date that was updated for the TDS transaction.</span></span>
    - <span data-ttu-id="88f96-129">**Certificaatnummer**: het TDS-certificaatnummer dat is bijgewerkt voor de TDS-transactie.</span><span class="sxs-lookup"><span data-stu-id="88f96-129">**Certificate number** – TDS certificate number that was updated for the TDS transaction.</span></span>

10. <span data-ttu-id="88f96-130">Schakel op de pagina **Certificaten voor terugvordering** het selectievakje **Afgesloten** in om het TDS-certificaatnummer te sluiten nadat u het hebt bijgewerkt voor TDS-transacties op de pagina **Certificaat bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="88f96-130">On the **Recoverable certificates** page, select the **Closed** check box to close the TDS certificate number after you've finished updating it for TDS transactions on the **Update certificate** page.</span></span>

    <span data-ttu-id="88f96-131">Als u het selectievakje **Afgesloten** voor alle records op de pagina wilt inschakelen, selecteert u **Alles markeren**.</span><span class="sxs-lookup"><span data-stu-id="88f96-131">To select the **Closed** check box for all records on the page, select **Mark all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="88f96-132">TDS-certificaatnummers waar het selectievakje **Afgesloten** voor is ingeschakeld, zijn niet beschikbaar op de pagina **Certificaat bijwerken**.</span><span class="sxs-lookup"><span data-stu-id="88f96-132">TDS certificate numbers that the **Closed** check box is selected for aren't available on the **Update certificate** page.</span></span>
