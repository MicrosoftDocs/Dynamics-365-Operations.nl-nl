---
title: Leaseparameters configureren (preview)
description: In dit onderwerp worden de configuratie-instellingen voor Activa leasen beschreven, zoals beveiligingsinformatie en boekhoudinstellingen.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f71006570cd8f2bdc0385388eae0800cd29d3ec8
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442164"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="064f7-103">Leaseparameters configureren</span><span class="sxs-lookup"><span data-stu-id="064f7-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="064f7-104">Verschillende configuratie-instellingen zijn van invloed op de werking van de Activa leasen.</span><span class="sxs-lookup"><span data-stu-id="064f7-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="064f7-105">Deze instellingen omvatten de journaalnamen, algemene parameters en instellingen voor boekingsprofielen.</span><span class="sxs-lookup"><span data-stu-id="064f7-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="064f7-106">Ga naar **Activa leasen \> Instellingen \> Parameters voor activa leasen**.</span><span class="sxs-lookup"><span data-stu-id="064f7-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="064f7-107">Selecteer het sneltabblad **Algemeen** op het tabblad **Leases**.</span><span class="sxs-lookup"><span data-stu-id="064f7-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="064f7-108">De parameter **Overschrijven van handmatige classificaties toestaan** bepaalt of de leaseclassificatie kan worden overschreven voordat het betalingsschema wordt bevestigd.</span><span class="sxs-lookup"><span data-stu-id="064f7-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="064f7-109">De parameter **Cross-entiteitbatches** bepaalt of u kunt boeken naar andere rechtspersonen vanuit de huidige rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="064f7-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="064f7-110">Als deze parameter is ingeschakeld, kunt u journaalboekingen maken voor de rechtspersonen waartoe u toegang hebt.</span><span class="sxs-lookup"><span data-stu-id="064f7-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="064f7-111">Stel de optie **Verwijderen van bevestigde leases toestaan** in op **Ja** om toe te staan dat leases met bevestigde betalingsschema's worden verwijderd.</span><span class="sxs-lookup"><span data-stu-id="064f7-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="064f7-112">Leases kunnen niet worden verwijderd als er geboekte of niet-geboekte transacties aan zijn gekoppeld, ongeacht de instelling van deze optie.</span><span class="sxs-lookup"><span data-stu-id="064f7-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="064f7-113">U kunt een leaserecord niet herstellen nadat deze is verwijderd.</span><span class="sxs-lookup"><span data-stu-id="064f7-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="064f7-114">Als u records uploadt voor een verwijderde lease, handmatig of via gegevensentiteiten, wordt de geüploade informatie behandeld als nieuw, niet als een update voor een bestaande lease.</span><span class="sxs-lookup"><span data-stu-id="064f7-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="064f7-115">Als u deze optie instelt op **Ja** en het overgangstype van het boek is ingesteld op **optie A of B voor cumulatief verzamelen**, stelt het systeem het veld **Verhoogd leningtarief** in op de waarde van het veld **Verhoogd leningtarief bij overgang** op de pagina **Instellingen voor boeken**.</span><span class="sxs-lookup"><span data-stu-id="064f7-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="064f7-116">Als deze optie is ingesteld op **Nee**, wordt het tarief op de hoofdlease ingesteld op de waarde van het veld **Verhoogd leningtarief** op de pagina **Boekdetails**, ongeacht het overgangstype van het boek.</span><span class="sxs-lookup"><span data-stu-id="064f7-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="064f7-117">Stel de optie **Afschrijvingsomkeringen voor afgesloten boekversie toestaan** in op **Ja** om het terugboeken van onkostentransacties voor afschrijving toe te staan.</span><span class="sxs-lookup"><span data-stu-id="064f7-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="064f7-118">Onkostentransacties kunnen worden omgekeerd, zelfs als de boekversie is afgesloten.</span><span class="sxs-lookup"><span data-stu-id="064f7-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="064f7-119">U kunt deze optie het beste op **Nee** instellen.</span><span class="sxs-lookup"><span data-stu-id="064f7-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="064f7-120">De instelling van deze optie wordt gebruikt als validatie en controle om te voorkomen dat een gesloten boekversie onbedoeld wordt afgeschreven.</span><span class="sxs-lookup"><span data-stu-id="064f7-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="064f7-121">U kunt de nettoboekwaarde en de toekomstige afschrijvingsberekeningen nauwkeurig bijhouden door de optie op **Nee** in te stellen.</span><span class="sxs-lookup"><span data-stu-id="064f7-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>
