---
title: Consignmentvoorraad bewaken door middel van leverancierssamenwerking
description: Deze procedure laat zien hoe u leverancierssamenwerking gebruikt om gegevens weer te geven over het voorraadniveau van het product dat u in consignatie bij een klant hebt geplaatst.
author: sherry-zheng
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ConsignmentProductReceiptLines, PurchVendorPortalConfirmedOrders, DefaultDashboard, ConsignmentVendorPortalOnhand
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: chuzheng
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92e397c12b9f605d1c864ce053477090ed8c1700
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839266"
---
# <a name="monitor-consignment-inventory-using-vendor-collaboration"></a><span data-ttu-id="db40c-103">Consignmentvoorraad bewaken door middel van leverancierssamenwerking</span><span class="sxs-lookup"><span data-stu-id="db40c-103">Monitor consignment inventory using vendor collaboration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="db40c-104">Deze procedure laat zien hoe u leverancierssamenwerking gebruikt om gegevens weer te geven over het voorraadniveau van het product dat u in consignatie bij een klant hebt geplaatst.</span><span class="sxs-lookup"><span data-stu-id="db40c-104">This procedure shows how to use vendor collaboration to see information about the stock level of product that you have placed in consignment with a customer.</span></span> <span data-ttu-id="db40c-105">U kunt ook het verbruik van de voorraad controleren wanneer de klant eigenaar wordt van de voorraad.</span><span class="sxs-lookup"><span data-stu-id="db40c-105">You can also monitor the consumption of the stock when the customer takes ownership of the inventory.</span></span> <span data-ttu-id="db40c-106">U kunt deze procedure gebruiken in het demobedrijf USMF.</span><span class="sxs-lookup"><span data-stu-id="db40c-106">You can use this procedure in the USMF demo data company.</span></span> <span data-ttu-id="db40c-107">Deze procedure is voor een functie die in Dynamics 365 for Operations, versie 1611 is toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="db40c-107">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="view-consumed-inventory"></a><span data-ttu-id="db40c-108">Verbruikte voorraad weergeven</span><span class="sxs-lookup"><span data-stu-id="db40c-108">View consumed inventory</span></span>
1. <span data-ttu-id="db40c-109">Ga naar Leverancierssamenwerking > Consignatievoorraad > Producten ontvangen uit consignatievoorraad.</span><span class="sxs-lookup"><span data-stu-id="db40c-109">Go to Vendor collaboration > Consignment inventory > Products received from consignment inventory.</span></span>
    * <span data-ttu-id="db40c-110">De lijst geeft de productontvangstbonregels weer die zijn gegenereerd toen het eigendom van de consignatievoorraad is gewijzigd van de leverancier in de klant.</span><span class="sxs-lookup"><span data-stu-id="db40c-110">The list shows the product receipt lines that were generated when ownership of the consignment inventory was changed from the vendor to the customer.</span></span> <span data-ttu-id="db40c-111">Mogelijk moet u naar rechts schuiven om hoeveelheden en andere informatie weer te geven.</span><span class="sxs-lookup"><span data-stu-id="db40c-111">You might have to scroll to the right to see quantities and other information.</span></span> <span data-ttu-id="db40c-112">U kunt de informatie in deze lijst gebruiken om facturen voor de klant te genereren.</span><span class="sxs-lookup"><span data-stu-id="db40c-112">You can use the information in this list to generate invoices for your customer.</span></span> <span data-ttu-id="db40c-113">U kunt de gegevens ook exporteren naar Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="db40c-113">You can also export the data to Microsoft Excel.</span></span>   
2. <span data-ttu-id="db40c-114">Klik op Inkooporder weergeven.</span><span class="sxs-lookup"><span data-stu-id="db40c-114">Click View purchase order.</span></span>
3. <span data-ttu-id="db40c-115">Vouw de sectie Regeldetails uit.</span><span class="sxs-lookup"><span data-stu-id="db40c-115">Expand the Line details section.</span></span>
    * <span data-ttu-id="db40c-116">De regel wordt gemarkeerd als Consignatie en in de headersectie wordt aangegeven dat de status van de inkooporder Ontvangen is.</span><span class="sxs-lookup"><span data-stu-id="db40c-116">The line is marked as Consignment, and the header section shows that the purchase order has a status of Received.</span></span>  
4. <span data-ttu-id="db40c-117">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="db40c-117">Close the page.</span></span>

## <a name="view-on-hand-inventory"></a><span data-ttu-id="db40c-118">Voorhanden voorraad weergeven</span><span class="sxs-lookup"><span data-stu-id="db40c-118">View on-hand inventory</span></span>
1. <span data-ttu-id="db40c-119">Ga naar Leverancierssamenwerking > Consignatievoorraad > Voorhanden consignatievoorraad.</span><span class="sxs-lookup"><span data-stu-id="db40c-119">Go to Vendor collaboration > Consignment inventory > On-hand consignment inventory.</span></span>
    * <span data-ttu-id="db40c-120">De pagina Voorhanden consignatievoorraad geeft de voorraad weer die u bezit in het magazijn van de klant.</span><span class="sxs-lookup"><span data-stu-id="db40c-120">The On-hand consignment inventory page shows the stock that you own at the customer's warehouse.</span></span> <span data-ttu-id="db40c-121">U kunt extra dimensies weergeven, zoals de locatie en het magazijn, door op het tabblad Dimensies weergeven te klikken.</span><span class="sxs-lookup"><span data-stu-id="db40c-121">You can show additional dimensions, such as the site and warehouse, by clicking the Display dimensions tab.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]