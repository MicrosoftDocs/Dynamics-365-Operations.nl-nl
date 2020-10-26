---
title: Kredietgroepen van klant
description: Dit onderwerp bevat informatie over kredietgroepen van klant.
author: mikefalkner
manager: AnnBe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1ddf41d88d085b102a7d69eeeff0ec463d8b4137
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977954"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="a320c-103">Kredietgroepen van klant</span><span class="sxs-lookup"><span data-stu-id="a320c-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a320c-104">U kunt groepen klanten definiëren die een gedeelde kredietlimiet hebben.</span><span class="sxs-lookup"><span data-stu-id="a320c-104">You can define groups of customers who have a shared credit limit.</span></span> <span data-ttu-id="a320c-105">Er wordt ook rekening gehouden met de individuele kredietlimiet die is gedefinieerd voor de rekening van de klantfactuur.</span><span class="sxs-lookup"><span data-stu-id="a320c-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="a320c-106">Leden van een kredietgroep van klant kunnen uit verschillende rechtspersonen worden geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="a320c-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="a320c-107">Wanneer u een klant aan de lijst met klanten in de kredietgroep van de klant toevoegt, verandert de vervaldatum van de kredietlimiet voor elke klant in de vervaldatum die is toegewezen aan de groep.</span><span class="sxs-lookup"><span data-stu-id="a320c-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="a320c-108">U kunt kredietgroepen van klant instellen op de pagina **Kredietgroepen van klant** (**Kredietbeheer \> Kredietgroepen van klant \> Kredietgroepen van klant**).</span><span class="sxs-lookup"><span data-stu-id="a320c-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="a320c-109">Voer in de velden **Groepsnummer** en **Beschrijving** een id en beschrijving voor de groep in.</span><span class="sxs-lookup"><span data-stu-id="a320c-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="a320c-110">Voer in de velden **Kredietlimiet** en **Valuta** de kredietlimiet en valuta in die moeten worden gebruikt wanneer het systeem de kredietlimiet voor een lid van de groep controleert.</span><span class="sxs-lookup"><span data-stu-id="a320c-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="a320c-111">Voer in het veld **Kredietlimiet tot datum** de datum in waarop de kredietlimiet vervalt.</span><span class="sxs-lookup"><span data-stu-id="a320c-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="a320c-112">Kredietgroepen van klant moeten een vervaldatum hebben.</span><span class="sxs-lookup"><span data-stu-id="a320c-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="a320c-113">Wanneer u klaar bent met het instellen van een kredietgroep van klant, kunt u er klanten aan toevoegen door hun rechtspersoon en klantrekening-id op te geven.</span><span class="sxs-lookup"><span data-stu-id="a320c-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="a320c-114">Wanneer u een nieuwe klant toevoegt aan een kredietgroep van klant, zoekt het systeem in alle rechtspersonen naar dezelfde klantrekening en wordt u gevraagd of u deze wilt toevoegen aan de kredietgroep van klant.</span><span class="sxs-lookup"><span data-stu-id="a320c-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="a320c-115">Gebruik het menu **Vervallen saldi** als u de details wilt bekijken van het naar ouderdom gerangschikte saldo voor alle factuurklanten in een kredietgroep van klant.</span><span class="sxs-lookup"><span data-stu-id="a320c-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="a320c-116">De pagina **Naar ouderdom gerangschikt saldo** toont een overzicht van de vervallen saldi voor de factuurklantrekeningen.</span><span class="sxs-lookup"><span data-stu-id="a320c-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>
