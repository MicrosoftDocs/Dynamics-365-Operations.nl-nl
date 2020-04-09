---
title: Een bankfaciliteitsovereenkomst maken voor een kredietbrief
description: Deze taak helpt u bij het maken van een bankfaciliteitsovereenkomst om een kredietbrief te verwerken.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankDocumentFacilityAgreement, BankAccountTableLookUp, BankDocumentFacilityAgreementExtension, DefaultDashboard
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb624700e0b052de977fabecf9670b3515d32ab7
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141710"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="150a2-103">Een bankfaciliteitsovereenkomst maken voor een kredietbrief</span><span class="sxs-lookup"><span data-stu-id="150a2-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="150a2-104">Deze taak helpt u bij het maken van een bankfaciliteitsovereenkomst om een kredietbrief te verwerken.</span><span class="sxs-lookup"><span data-stu-id="150a2-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="150a2-105">U kunt bankfaciliteiten en boekingsprofielen instellen vóór deze taak.</span><span class="sxs-lookup"><span data-stu-id="150a2-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="150a2-106">Bij deze taak wordt het demobedrijf USMF gebruikt.</span><span class="sxs-lookup"><span data-stu-id="150a2-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="150a2-107">Een bankfaciliteitsovereenkomst maken</span><span class="sxs-lookup"><span data-stu-id="150a2-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="150a2-108">Ga naar Kas- en bankbeheer > Kredietbrieven > Bankfaciliteitsovereenkomsten.</span><span class="sxs-lookup"><span data-stu-id="150a2-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="150a2-109">Klik op Nieuw.</span><span class="sxs-lookup"><span data-stu-id="150a2-109">Click New.</span></span>
3. <span data-ttu-id="150a2-110">Voer in het veld Overeenkomstnummer het overeenkomstnummer in dat hoort bij de overeenkomst met de bank.</span><span class="sxs-lookup"><span data-stu-id="150a2-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="150a2-111">Geef in het veld Bankrekening het bankrekeningnummer op van de uitgevende bank.</span><span class="sxs-lookup"><span data-stu-id="150a2-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="150a2-112">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="150a2-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="150a2-113">Typ in het datumveld voor het begin de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="150a2-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="150a2-114">Typ in het datumveld voor het einde de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="150a2-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="150a2-115">Vouw de sectie Algemeen uit of samen.</span><span class="sxs-lookup"><span data-stu-id="150a2-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="150a2-116">Klik op Regel toevoegen.</span><span class="sxs-lookup"><span data-stu-id="150a2-116">Click Add line.</span></span>
10. <span data-ttu-id="150a2-117">Klik in het veld Type faciliteit op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="150a2-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="150a2-118">Zoek en selecteer het gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="150a2-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="150a2-119">Klik in de lijst op de koppeling in de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="150a2-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="150a2-120">Voer in het veld Grenswaarde het faciliteitsbedrag in dat met de bank is overeengekomen.</span><span class="sxs-lookup"><span data-stu-id="150a2-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="150a2-121">Klik op Opslaan.</span><span class="sxs-lookup"><span data-stu-id="150a2-121">Click Save.</span></span>
15. <span data-ttu-id="150a2-122">Klik op Uitbreiden om het verwijderdialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="150a2-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="150a2-123">Typ een waarde in het veld Nieuw overeenkomstnummer.</span><span class="sxs-lookup"><span data-stu-id="150a2-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="150a2-124">Typ in het datumveld voor het einde de datum en een tijd.</span><span class="sxs-lookup"><span data-stu-id="150a2-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="150a2-125">Klik op Uitbreiden.</span><span class="sxs-lookup"><span data-stu-id="150a2-125">Click Extend.</span></span>
19. <span data-ttu-id="150a2-126">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="150a2-126">Close the page.</span></span>

