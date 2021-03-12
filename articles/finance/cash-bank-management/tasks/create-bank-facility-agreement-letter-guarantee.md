---
title: Een bankfaciliteitsovereenkomst maken voor de borgstelling
description: Deze taak maakt een bankfaciliteitsovereenkomst om een borgstelling te verwerken.
author: panolte
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: edeadc1b8502171b9ce892efdaeb9347e399b771
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989097"
---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a><span data-ttu-id="f8d8c-103">Een bankfaciliteitsovereenkomst maken voor de borgstelling</span><span class="sxs-lookup"><span data-stu-id="f8d8c-103">Create a bank facility agreement for the letter of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f8d8c-104">Deze taak maakt een bankfaciliteitsovereenkomst om een borgstelling te verwerken.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-104">This task creates a bank facility agreement to process a letter of guarantee.</span></span> <span data-ttu-id="f8d8c-105">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-105">This task uses the USMF demo company.</span></span> 


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="f8d8c-106">Een bankfaciliteitsovereenkomst maken</span><span class="sxs-lookup"><span data-stu-id="f8d8c-106">Create Bank facility agreement</span></span>
1. <span data-ttu-id="f8d8c-107">Ga naar Kas- en bankbeheer > Borgstellingen > Bankfaciliteitsovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-107">Go to Cash and bank management > Letters of guarantee > Bank facility agreements.</span></span>
2. <span data-ttu-id="f8d8c-108">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-108">Click New.</span></span>
3. <span data-ttu-id="f8d8c-109">Voer in het veld Overeenkomstnummer het bankovereenkomstnummer voor de transactie in.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-109">In the Agreement number field, enter the bank agreement number for the transaction.</span></span>
4. <span data-ttu-id="f8d8c-110">Selecteer in het veld Bankrekening het bankrekeningnummer waarvoor de borgstelling is geopend.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-110">In the Bank account field, select the bank account number for which the letter of guarantee is open.</span></span> 
5. <span data-ttu-id="f8d8c-111">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f8d8c-112">Typ in het datumveld voor het begin de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-112">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="f8d8c-113">Typ in het datumveld voor het einde de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-113">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="f8d8c-114">Schakel de uitbreiding van de sectie Algemeen om.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-114">Toggle the expansion of the General section.</span></span>
9. <span data-ttu-id="f8d8c-115">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-115">Click Add line.</span></span>
10. <span data-ttu-id="f8d8c-116">Klik in het veld Type faciliteit op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-116">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="f8d8c-117">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="f8d8c-118">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-118">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="f8d8c-119">Voer in het veld Limiet het bedrag in dat met de bank is overeengekomen.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-119">In the Limit field, enter the amount negotiated with the bank.</span></span>
14. <span data-ttu-id="f8d8c-120">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-120">Click Save.</span></span>
15. <span data-ttu-id="f8d8c-121">Schakel de uitbreiding van de sectie Borgstelling om.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-121">Toggle the expansion of the Letter of guarantee section.</span></span>
16. <span data-ttu-id="f8d8c-122">Selecteer een optie in het veld Berekeningsmethode.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-122">In the Calculation method field, select an option.</span></span>
    * <span data-ttu-id="f8d8c-123">Voer de berekeningsmethode en percentagedetails in voor Contantenmarge, Uitgifteprovisie, Extensieprovisie, Waardeprovisie verhogen of Waardeprovisie verlagen, waar van toepassing.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-123">Enter the calculation method and percentage details for the Cash margin, Issuance commission, Extension commission, Increase value commission, or Decrease value commission, as appropriate.</span></span>   
17. <span data-ttu-id="f8d8c-124">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-124">Click Save.</span></span>

## <a name="extend-bank-facility-agreement"></a><span data-ttu-id="f8d8c-125">Bankfaciliteitsovereenkomst uitbreiden</span><span class="sxs-lookup"><span data-stu-id="f8d8c-125">Extend bank facility agreement</span></span>
1. <span data-ttu-id="f8d8c-126">Klik op Uitbreiden om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-126">Click Extend to open the drop dialog.</span></span>
2. <span data-ttu-id="f8d8c-127">Typ een waarde in het veld Nieuw overeenkomstnummer.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-127">In the New agreement number field, type a value.</span></span>
3. <span data-ttu-id="f8d8c-128">Typ in het datumveld voor het einde de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-128">In the End date field, enter a date and time.</span></span>
4. <span data-ttu-id="f8d8c-129">Klik op Uitbreiden.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-129">Click Extend.</span></span>
5. <span data-ttu-id="f8d8c-130">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-130">Click Save.</span></span>
6. <span data-ttu-id="f8d8c-131">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f8d8c-131">Close the page.</span></span>

