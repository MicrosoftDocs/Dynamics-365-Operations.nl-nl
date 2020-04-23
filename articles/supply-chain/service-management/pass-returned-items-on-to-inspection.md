---
title: Geretourneerde artikelen doorgeven voor inspectie
description: Bepaal bij het registreren van een geretourneerd artikel dat een artikel ter controle moet worden verzonden voordat het naar de voorraad wordt geretourneerd of op een andere manier wordt afgestoten.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSJournalTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cbb43bc4f696935bba9fca6435eb73fc9a2e5149
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3202095"
---
# <a name="pass-returned-items-on-to-inspection"></a><span data-ttu-id="164f1-103">Geretourneerde artikelen doorgeven voor inspectie</span><span class="sxs-lookup"><span data-stu-id="164f1-103">Pass returned items on to inspection</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="164f1-104">Bij het registreren van een geretourneerd artikel kunt u ervoor kiezen een artikel ter controle te verzenden voordat het wordt geretourneerd naar de voorraad of op een andere manier wordt afgestoten.</span><span class="sxs-lookup"><span data-stu-id="164f1-104">When registering a returned item, you may determine that an item should be sent for inspection before it is returned to inventory or disposed of in some other way.</span></span>

1.  <span data-ttu-id="164f1-105">Ga naar **Voorraadbeheer** \> **Journaalposten** \> **Artikelontvangst** \> **Artikelontvangst**.</span><span class="sxs-lookup"><span data-stu-id="164f1-105">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Item arrival**.</span></span>
    
    <span data-ttu-id="164f1-106">\-of-</span><span class="sxs-lookup"><span data-stu-id="164f1-106">\-or-</span></span>
    
    <span data-ttu-id="164f1-107">Klik op **Voorraadbeheer** \> **Journaalen** \> **Artikelontvangst** \> **Productie-invoer**.</span><span class="sxs-lookup"><span data-stu-id="164f1-107">Click **Inventory management** \> **Journals** \> **Item arrival** \> **Production input**.</span></span>

2.  <span data-ttu-id="164f1-108">Registreer de ontvangst van een artikel zoals gebruikelijk in het formulier **Locatiejournaal**.</span><span class="sxs-lookup"><span data-stu-id="164f1-108">On the **Location journal** form, register the receipt of an item as usual.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="164f1-109">Zie voor informatie over het registreren van de ontvangst van geretourneerde artikelen <A href="register-the-receipt-of-returned-items.md">De ontvangst van geretourneerde artikelen registreren</A></span><span class="sxs-lookup"><span data-stu-id="164f1-109">For information about registering the receipt of returned items, see <A href="register-the-receipt-of-returned-items.md">Register the receipt of returned items</A></span></span></P>



3.  <span data-ttu-id="164f1-110">Op het tabblad **Standaardwaarden** in het gebied **Verwerkingsmethode** schakelt u het vakje **Quarantainebeheer** in.</span><span class="sxs-lookup"><span data-stu-id="164f1-110">On the **Default values** tab, in the **Mode of handling** area, select the **Quarantine management** box.</span></span>

<span data-ttu-id="164f1-111">Er wordt automatisch een quarantaineorder gemaakt en de persoon of afdeling die controles uitvoert, reageert op deze order met het formulier **Quarantaineorder**.</span><span class="sxs-lookup"><span data-stu-id="164f1-111">This will prompt the system to create a quarantine order, and the person or department that performs inspections will respond to this order using the **Quarantine order** form.</span></span>

## <a name="see-also"></a><span data-ttu-id="164f1-112">Zie ook</span><span class="sxs-lookup"><span data-stu-id="164f1-112">See also</span></span>

[<span data-ttu-id="164f1-113">Retourartikelen aan een inspectie onderwerpen</span><span class="sxs-lookup"><span data-stu-id="164f1-113">Take returned items through inspection</span></span>](take-returned-items-through-inspection.md)

[<span data-ttu-id="164f1-114">Opgeven op welke wijze retourartikelen moeten worden afgestoten</span><span class="sxs-lookup"><span data-stu-id="164f1-114">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

