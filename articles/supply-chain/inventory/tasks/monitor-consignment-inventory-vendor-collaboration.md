---
title: Consignmentvoorraad bewaken door middel van leverancierssamenwerking
description: Deze procedure laat zien hoe u leverancierssamenwerking gebruikt om gegevens weer te geven over het voorraadniveau van het product dat u in consignatie bij een klant hebt geplaatst.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1c75db4ef5d07e4ae396401a851389b7ecb9242
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244370"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="f6c7f-103">Consignmentvoorraad bewaken door middel van leverancierssamenwerking</span><span class="sxs-lookup"><span data-stu-id="f6c7f-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f6c7f-104">Deze procedure laat zien hoe u leverancierssamenwerking gebruikt om gegevens weer te geven over het voorraadniveau van het product dat u in consignatie bij een klant hebt geplaatst.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="f6c7f-105">U kunt ook het verbruik van de voorraad controleren wanneer de klant eigenaar wordt van de voorraad.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="f6c7f-106">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="f6c7f-107">Deze procedure is voor een functie die in Dynamics 365 for Operations, versie 1611 is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="f6c7f-108">Verbruikte voorraad weergeven</span><span class="sxs-lookup"><span data-stu-id="f6c7f-108">View consumed inventory</span></span>
1. <span data-ttu-id="f6c7f-109">Ga naar Leverancierssamenwerking > Consignatievoorraad > Producten ontvangen uit consignatievoorraad.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="f6c7f-110">De lijst geeft de productontvangstbonregels weer die zijn gegenereerd toen het eigendom van de consignatievoorraad is gewijzigd van de leverancier in de klant.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="f6c7f-111">Mogelijk moet u naar rechts schuiven om hoeveelheden en andere informatie weer te geven.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="f6c7f-112">U kunt de informatie in deze lijst gebruiken om facturen voor de klant te genereren.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="f6c7f-113">U kunt de gegevens ook exporteren naar Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="f6c7f-114">Klik op Inkooporder weergeven.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-114">Click View purchase order.</span></span>
3. <span data-ttu-id="f6c7f-115">Vouw de sectie Regeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="f6c7f-116">De regel wordt gemarkeerd als Consignatie en in de headersectie wordt aangegeven dat de status van de inkooporder Ontvangen is.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="f6c7f-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="f6c7f-118">Voorhanden voorraad weergeven</span><span class="sxs-lookup"><span data-stu-id="f6c7f-118">View on-hand inventory</span></span>
1. <span data-ttu-id="f6c7f-119">Ga naar Leverancierssamenwerking > Consignatievoorraad > Voorhanden consignatievoorraad.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="f6c7f-120">De pagina Voorhanden consignatievoorraad geeft de voorraad weer die u bezit in het magazijn van de klant.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-120">The On-hand consignment inventory page shows the stock that you own at the customer's warehouse.</span></span> <span data-ttu-id="f6c7f-121">U kunt extra dimensies weergeven, zoals de locatie en het magazijn, door op het tabblad Dimensies weergeven te klikken.</span><span class="sxs-lookup"><span data-stu-id="f6c7f-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]