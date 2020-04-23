---
title: Retourartikelen aan een inspectie onderwerpen
description: Onderwerp retourartikelen aan een inspectie.
author: ShylaThompson
manager: tfehr
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: aa85bf4262216c780c3da523f65baf980fdc200f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206560"
---
# <a name="take-returned-items-through-inspection"></a><span data-ttu-id="942ec-103">Retourartikelen aan een inspectie onderwerpen</span><span class="sxs-lookup"><span data-stu-id="942ec-103">Take returned items through inspection</span></span> 

[!include [banner](../includes/banner.md)]


1.  <span data-ttu-id="942ec-104">Klik op **Voorraadbeheer** \> **Periodiek** \> **Kwaliteitsbeheer** \> **Quarantaineorders**.</span><span class="sxs-lookup"><span data-stu-id="942ec-104">Click **Inventory management** \> **Periodic** \> **Quality management** \> **Quarantine orders**.</span></span>

2.  <span data-ttu-id="942ec-105">Zoek de orderregel op van het geretourneerde artikel dat u controleert.</span><span class="sxs-lookup"><span data-stu-id="942ec-105">Locate the order line that corresponds to the returned item that you are inspecting.</span></span>

    > [!NOTE]
    > <P><span data-ttu-id="942ec-106">Een quarantaineorder kan alleen aan een enkel artikelnummer worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="942ec-106">A quarantine order can be associated with just a single item number.</span></span> <span data-ttu-id="942ec-107">Als er in een enkele zending tien artikelen met verschillende artikelnummers worden geretourneerd en in quarantaine worden geplaatst, worden er tien verschillende quarantaineorders gemaakt.</span><span class="sxs-lookup"><span data-stu-id="942ec-107">If 10 items that have different item numbers are returned in a single shipment and sent to quarantine, 10 individual quarantine orders are created.</span></span></P>

3.  <span data-ttu-id="942ec-108">Nadat u het artikel hebt gecontroleerd, geeft u met behulp van het veld **Beschikkingscode** aan wat er met het artikel moet gebeuren en hoe de gerelateerde financiële transacties ervoor worden afgehandeld.</span><span class="sxs-lookup"><span data-stu-id="942ec-108">After examining the item, make a selection in the **Disposition code** field to indicate what should be done with the item and how to handle the related financial transaction.</span></span> <span data-ttu-id="942ec-109">Voorbeelden daarvan zijn onder andere het weer toevoegen van het artikel aan de voorraad en het restitueren van de klant, het vernietigen van het artikel en het sturen van eenzelfde artikel naar de klant of het terugsturen van het artikel naar de klant zonder de klant te crediteren.</span><span class="sxs-lookup"><span data-stu-id="942ec-109">Examples include returning the item to stock and refunding the customer, scrapping the item and sending a replacement to the customer, or returning the item to the customer without credit.</span></span>
    
    > [!NOTE]
    > <P><span data-ttu-id="942ec-110">Als er geen beschikkingscode kan worden toegewezen aan meerdere geretourneerde artikelen in een batch met één artikelnummer, moet u de quarantainecode splitsen (<STRONG>Functies</STRONG> &gt; <STRONG>Splitsen</STRONG>) om aan elke subbatch een andere dispositiecode te kunnen toewijzen.</span><span class="sxs-lookup"><span data-stu-id="942ec-110">If multiple returned items in a single item number batch cannot be assigned the same disposition code, you must split the quarantine order (<STRONG>Functions</STRONG> &gt; <STRONG>Split</STRONG>) to assign a different disposition code to each sub-batch.</span></span></P>


4.  <span data-ttu-id="942ec-111">Wanneer u klaar bent met de inspectie, klikt u op **Gereedmelden** om de geretourneerde artikelen vrij te geven en een journaalpost te maken.</span><span class="sxs-lookup"><span data-stu-id="942ec-111">When you are finished with the inspection, click **Report as finished** to release the returned items and create an item arrival journal entry.</span></span> <span data-ttu-id="942ec-112">De persoon of de afdeling die de artikelen ontvangt, verwerkt het journaal voor de artikelen die weer aan de voorraad moeten worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="942ec-112">The person or department that receives the items then processes the journal for the items to be returned to inventory.</span></span>
    
    <span data-ttu-id="942ec-113">– of –</span><span class="sxs-lookup"><span data-stu-id="942ec-113">–or–</span></span>
    
    <span data-ttu-id="942ec-114">Beëindig de quarantaineorder en plaats de artikelen rechtstreeks terug in de voorraad via een van de functies voor **Voorraad**.</span><span class="sxs-lookup"><span data-stu-id="942ec-114">End the quarantine order, and move the items back into inventory directly by using one of the **Inventory** functions.</span></span>

5.  <span data-ttu-id="942ec-115">Sluit het formulier om de wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="942ec-115">Close the form to save your changes.</span></span>

## <a name="see-also"></a><span data-ttu-id="942ec-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="942ec-116">See also</span></span>

[<span data-ttu-id="942ec-117">Opgeven op welke wijze retourartikelen moeten worden afgestoten</span><span class="sxs-lookup"><span data-stu-id="942ec-117">Specify how to dispose of returned items</span></span>](specify-how-to-dispose-of-returned-items.md)

  


