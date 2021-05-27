---
title: TDS-vrijstellingscertificaatnummers registreren
description: In dit onderwerp wordt uitgelegd hoe u de TDS-vrijstellingscertificaatnummers (belasting ingehouden op bron) vastlegt die aan leveranciers worden uitgegeven.
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
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023136"
---
# <a name="record-tds-concession-certificate-numbers"></a><span data-ttu-id="12277-103">TDS-vrijstellingscertificaatnummers registreren</span><span class="sxs-lookup"><span data-stu-id="12277-103">Record TDS concession certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="12277-104">In dit onderwerp wordt uitgelegd hoe u de TDS-vrijstellingscertificaatnummers (belasting ingehouden op bron) vastlegt die aan leveranciers worden uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="12277-104">This topic explains how to record the Tax Deducted at Source (TDS) concession certificate numbers that are issued to vendors.</span></span>

1. <span data-ttu-id="12277-105">Ga naar **Belasting \> Indirecte belastingen \> Bronbelasting \> Vrijstelling van bronbelasting**.</span><span class="sxs-lookup"><span data-stu-id="12277-105">Go to **Tax \> Indirect taxes \> Withholding tax \> Withholding tax concessions**.</span></span>
2. <span data-ttu-id="12277-106">Selecteer in het veld **Belastingtype** de optie **TDS** om vrijstellingscertificaten voor het belastingtype TDS vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="12277-106">In the **Tax type** field, select **TDS** to record concession certificates for the TDS tax type.</span></span>
3. <span data-ttu-id="12277-107">Selecteer **Alt+N** op het tabblad **Overzicht** om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="12277-107">On the **Overview** tab, select **Alt+N** to create a line.</span></span>

    <span data-ttu-id="12277-108">[![Koptekst van de nieuwe regel](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span><span class="sxs-lookup"><span data-stu-id="12277-108">[![Header of the new line](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)</span></span>

4. <span data-ttu-id="12277-109">Selecteer in het veld **Bronbelastingcode** de TDS-belastingcode waarvoor de leveranciersvrijstellingscertificaten worden uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="12277-109">In the **Withholding tax code** field, select the TDS tax code that the vendor concession certificates are issued for.</span></span> <span data-ttu-id="12277-110">In het veld **Bronbelastingcodenaam** wordt de naam van de TDS-belastingcode weergegeven.</span><span class="sxs-lookup"><span data-stu-id="12277-110">The **Withholding tax code name** field shows the name of the TDS tax code.</span></span>
5. <span data-ttu-id="12277-111">Definieer in de velden **Begindatum** en **Einddatum** de geldigheidsduur voor het vrijstellingscertificaat dat de TDS-belastingcode gebruikt om TDS voor de leverancier op vrijstellingsbasis te berekenen.</span><span class="sxs-lookup"><span data-stu-id="12277-111">In the **From date** and **To date** fields, define the period of validity for the concession certificate that uses the TDS tax code to calculate TDS for the vendor on a concessional basis.</span></span>
6. <span data-ttu-id="12277-112">Voer in het veld **Opmerkingen** eventuele opmerkingen in.</span><span class="sxs-lookup"><span data-stu-id="12277-112">In the **Remarks** field, enter any remarks.</span></span>
7. <span data-ttu-id="12277-113">Voer in het veld **Sectie** de wettelijke sectiecode in waaronder het TDS-vrijstellingscertificaat wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="12277-113">In the **Section** field, enter the legal section code that the TDS concession certificate is availed under.</span></span>

    <span data-ttu-id="12277-114">Als de sectiecode 197 is, wordt de waarde "A" weergegeven in zowel de kolom "Reden voor niet-inhouding/lagere inhouding" in Formulier 26Q als de kolom "Reden voor niet-inhouding/lagere inhouding/brutowinst (indien van toepassing)" in Formulier 27Q.</span><span class="sxs-lookup"><span data-stu-id="12277-114">If the section code is 197, the value "A" appears in both the "Reason for non-deduction/lower deduction" column in Form 26Q and the "Reason for non-deduction/lower deduction/grossing up (if any)" column in Form 27Q.</span></span> <span data-ttu-id="12277-115">Als de sectiecode 197A is, wordt op beide plaatsen de waarde "B" weergegeven.</span><span class="sxs-lookup"><span data-stu-id="12277-115">If the section code is 197A, the value "B" appears in both those places.</span></span>

8. <span data-ttu-id="12277-116">Selecteer het sneltabblad **Certificaat** om TDS-vrijstellingscertificaatnummers voor leveranciers vast te leggen.</span><span class="sxs-lookup"><span data-stu-id="12277-116">Select the **Certificate** FastTab to record TDS concession certificate numbers for vendors.</span></span>
9. <span data-ttu-id="12277-117">Selecteer in het veld **Leveranciersrekening** de leveranciersrekening waarvoor het TDS-vrijstellingscertificaat wordt uitgegeven.</span><span class="sxs-lookup"><span data-stu-id="12277-117">In the **Vendor account** field, select the vendor account that the TDS concession certificate is issued for.</span></span>
10. <span data-ttu-id="12277-118">Definieer in de velden **Begindatum** en **Einddatum** de geldigheidsduur voor het TDS-vrijstellingscertificaat.</span><span class="sxs-lookup"><span data-stu-id="12277-118">In the **From date** and **To date** fields, define the period of validity for the TDS concession certificate.</span></span>

    <span data-ttu-id="12277-119">De berekening van TDS op vrijstellingsbasis is gebaseerd op de periode waarin het certificaat voor de leverancier wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="12277-119">The calculation of TDS on a concessional basis is based on the period when the certificate is created for the vendor.</span></span>

11. <span data-ttu-id="12277-120">Voer in het veld **Certificaat** het TDS-vrijstellingscertificaatnummer in.</span><span class="sxs-lookup"><span data-stu-id="12277-120">In the **Certificate** field, enter the TDS concession certificate number.</span></span>

    <span data-ttu-id="12277-121">[![Sneltabblad Certificaat](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span><span class="sxs-lookup"><span data-stu-id="12277-121">[![Certificate FastTab](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)</span></span>

12. <span data-ttu-id="12277-122">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="12277-122">Close the page.</span></span>
