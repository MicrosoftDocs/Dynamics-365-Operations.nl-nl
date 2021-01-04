---
title: Betalingsfacturen maken
description: In dit onderwerp wordt uitgelegd hoe u maandelijkse leasefacturen maakt. U kunt facturen maken voor afzonderlijke leases of u kunt een batchproces gebruiken om deze voor meerdere leases te maken.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 32618814d00cb1e1f1082169a64b187cce1e76b4
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442150"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="c86ee-104">Betalingsfacturen maken</span><span class="sxs-lookup"><span data-stu-id="c86ee-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c86ee-105">U kunt maandelijkse facturen maken voor afzonderlijke leases of u kunt een batchproces gebruiken om deze voor meerdere leases te maken.</span><span class="sxs-lookup"><span data-stu-id="c86ee-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="c86ee-106">Met de volgende procedure wordt aangegeven hoe u een individuele leasebetalingspost kunt maken wanneer de parameter **Betalen aan leverancier** op de pagina **Leaseboek instellen** is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="c86ee-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="c86ee-107">Selecteer op de pagina **Lease-overzicht** een lease en selecteer vervolgens **Boeken \> Betalingsschema**.</span><span class="sxs-lookup"><span data-stu-id="c86ee-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="c86ee-108">Selecteer de betaling die moet worden uitgevoerd en selecteer **Journaal maken**.</span><span class="sxs-lookup"><span data-stu-id="c86ee-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="c86ee-109">U ontvangt een bericht met de mededeling dat er een journaal is gemaakt voor de geselecteerde betaling.</span><span class="sxs-lookup"><span data-stu-id="c86ee-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="c86ee-110">Selecteer **Factuurjournalen** en selecteer vervolgens de factuur die moet worden betaald.</span><span class="sxs-lookup"><span data-stu-id="c86ee-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="c86ee-111">Bekijk op het tabblad **Regels** de journaalpost voordat u deze naar het grootboek boekt.</span><span class="sxs-lookup"><span data-stu-id="c86ee-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c86ee-112">De leveranciersfactuurregels die worden gemaakt, gebruiken standaard het boekingsprofiel van de leverancier van de pagina **Parameters van module Leveranciers**.</span><span class="sxs-lookup"><span data-stu-id="c86ee-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="c86ee-113">Selecteer het juiste journaal en selecteer vervolgens de factuur die moet worden betaald.</span><span class="sxs-lookup"><span data-stu-id="c86ee-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="c86ee-114">Voor dit voorbeeld is de parameter **Betalen aan leverancier** op het leaseboek ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="c86ee-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="c86ee-115">De factuur wordt daarom in het factuurjournaal opgenomen.</span><span class="sxs-lookup"><span data-stu-id="c86ee-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="c86ee-116">In de sectie **Overzicht** wordt een overzicht van de journaalpost weergegeven en de sectie **Regels** bevat details van de werkelijke journaalregels.</span><span class="sxs-lookup"><span data-stu-id="c86ee-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c86ee-117">Als de parameter **Betalen aan leverancier** is uitgeschakeld, worden de betalingsjournaalposten weergegeven op de pagina **Activa leasen** voor het leaseboek en wordt er een post voor activa leasen gemaakt in plaats van een factuur.</span><span class="sxs-lookup"><span data-stu-id="c86ee-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="c86ee-118">De leasebetalingspost wordt geboekt naar de journaalnaam die is opgegeven in het veld **Maandelijks leasejournaal**.</span><span class="sxs-lookup"><span data-stu-id="c86ee-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="c86ee-119">Nadat de transactie is geboekt, kunt u de transactiegegevens en de boekwaarde van de leaseverplichtingen weergeven door **Transacties verplichtingen** in het leaseboek te selecteren.</span><span class="sxs-lookup"><span data-stu-id="c86ee-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="c86ee-120">In het betalingsschema is het selectievakje **Journaal geboekt** ingeschakeld en geeft de regel het factuurjournaalnummer weer.</span><span class="sxs-lookup"><span data-stu-id="c86ee-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="c86ee-121">Nadat een betalingsjournaal en een post voor dat journaal zijn gemaakt, moet u de post terugboeken voordat u deze opnieuw kunt maken.</span><span class="sxs-lookup"><span data-stu-id="c86ee-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>
