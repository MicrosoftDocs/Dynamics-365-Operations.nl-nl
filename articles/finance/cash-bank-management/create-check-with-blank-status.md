---
title: Cheques met een status Blanco maken
description: In dit onderwerp wordt uitgelegd hoe u op de pagina Cheques een blanco cheque maakt voor een bankrekening.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 47d54524f87cf718b9b41462b5133df267d5dd9e
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570282"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="f3418-103">Cheques met een status Blanco maken</span><span class="sxs-lookup"><span data-stu-id="f3418-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3418-104">In dit onderwerp wordt uitgelegd hoe u blanco cheques maakt.</span><span class="sxs-lookup"><span data-stu-id="f3418-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="f3418-105">U kunt bijvoorbeeld een blanco cheque maken om een cheque te registreren die beschadigd is en die niet kan worden gebruikt om een betaling mee te verrichten.</span><span class="sxs-lookup"><span data-stu-id="f3418-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="f3418-106">Op de pagina **Cheques** voert u onderhoudstaken uit voor cheques.</span><span class="sxs-lookup"><span data-stu-id="f3418-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="f3418-107">U kunt bijvoorbeeld nieuwe chequenummers maken en cheques verwijderen.</span><span class="sxs-lookup"><span data-stu-id="f3418-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="f3418-108">U kunt ook cheques maken met de status **Blanco**.</span><span class="sxs-lookup"><span data-stu-id="f3418-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="f3418-109">Blanco cheques die zijn gemaakt, kunnen niet meer worden verwijderd of opnieuw worden gebruikt in het systeem.</span><span class="sxs-lookup"><span data-stu-id="f3418-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="f3418-110">Deze functie is alleen beschikbaar op de pagina **Cheques** als u de functie **Cheques met een blanco status maken op de pagina Cheques** inschakelt op de pagina **Functiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="f3418-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="f3418-111">Als die functie niet is ingeschakeld, kunnen cheques met een status **Blanco** alleen worden gemaakt via het dialoogvenster **Betaling per cheque** tijdens het genereren van de betaling in Leveranciers.</span><span class="sxs-lookup"><span data-stu-id="f3418-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="f3418-112">Als u de pagina **Cheques** wilt openen, gaat u naar **Contanten en bankbeheer \> Bankrekeningen \> Bankrekeningen** en selecteert u in het actievenster op het tabblad **Betalingen beheren** in de groep **Verwante informatie** de optie **Cheques**.</span><span class="sxs-lookup"><span data-stu-id="f3418-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="f3418-113">U kunt ook naar **Contanten en bankbeheer \> Query's en rapporten \> Cheques** gaan.</span><span class="sxs-lookup"><span data-stu-id="f3418-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="f3418-114">Als u cheques met de status **Blanco** wilt maken, selecteert u in het actievenster de optie **Blanco cheques maken**.</span><span class="sxs-lookup"><span data-stu-id="f3418-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="f3418-115">Terwijl er door het systeem blanco cheques worden gemaakt, wordt de bijbehorende bankrekening tijdelijk uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="f3418-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="f3418-116">Hierdoor wordt het risico kleiner dat betalingen worden gegenereerd op het moment dat blanco cheques worden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f3418-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="f3418-117">Als de verwerking is voltooid, wordt de bijbehorende bankrekening opnieuw geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="f3418-117">When the processing is completed, the associated bank account is reactivated.</span></span>
