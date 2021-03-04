---
title: Scenario's voor het betalen van facturen instellen
description: In dit onderwerp wordt beschreven hoe u Dynamics 365 Commerce configureert om verschillende scenario's met betrekking tot factuurbetalingen te ondersteunen.
author: josaw1
manager: AnnBe
ms.date: 11/14/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8b65fe3968698da1c5b76cf2d0ef706f3f1ec4bb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972652"
---
# <a name="set-up-pay-invoice-scenarios"></a><span data-ttu-id="6358e-103">Scenario's voor het betalen van facturen instellen</span><span class="sxs-lookup"><span data-stu-id="6358e-103">Set up pay invoice scenarios</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6358e-104">De functionaliteit Factuur betalen in Dynamics 365 Commerce is uitgebreid om het volgende te ondersteunen:</span><span class="sxs-lookup"><span data-stu-id="6358e-104">The Pay invoice functionality in Dynamics 365 Commerce has been expanded to support:</span></span>

- <span data-ttu-id="6358e-105">De betaling van meerdere verkooporderfacturen in één POS-transactie.</span><span class="sxs-lookup"><span data-stu-id="6358e-105">Payoff of multiple sales order invoices in a single POS transaction.</span></span>
- <span data-ttu-id="6358e-106">Betaling van verschillende typen klantfacturen, inclusief vrije-tekstfacturen, facturen op basis van projecten en creditnota's.</span><span class="sxs-lookup"><span data-stu-id="6358e-106">Payment of various customer invoice types including free text invoices, project-based invoices, and credit notes.</span></span>

<span data-ttu-id="6358e-107">Om deze scenario's mogelijk te maken moet u het functionaliteitsprofiel voor winkels als volgt configureren.</span><span class="sxs-lookup"><span data-stu-id="6358e-107">To enable these scenarios, the functionality profile for stores must be configured as outlined in below.</span></span>

1. <span data-ttu-id="6358e-108">Ga naar **Detailhandel en commerce \> Afzetkanaalinstellingen \> POS-instellingen \> POS-profielen \> Functionaliteitsprofielen** en selecteer een profiel dat is gekoppeld aan de winkels waarvoor u de wijzigingen wilt doorvoeren.</span><span class="sxs-lookup"><span data-stu-id="6358e-108">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles** and select a profile that's linked to the stores that you want to make the changes for.</span></span>
2. <span data-ttu-id="6358e-109">Op het tabblad **Functies** kunt u de volgende parameters naar wens configureren.</span><span class="sxs-lookup"><span data-stu-id="6358e-109">On the **Functions** tab, configure the following parameters as needed.</span></span>

    - <span data-ttu-id="6358e-110">**Verkooporderfactuur**: selecteer **Ja** om gebruikers in staat te stellen een of meer facturen op basis van verkooporders in één POS-transactie te betalen.</span><span class="sxs-lookup"><span data-stu-id="6358e-110">**Sales order invoice** – Select **Yes** to allow users to pay one or more sales order-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="6358e-111">**Vrije-tekstfactuur**: selecteer **Ja** om gebruikers in staat te stellen een of meer vrije-tekstfacturen in één POS-transactie te betalen.</span><span class="sxs-lookup"><span data-stu-id="6358e-111">**Free text invoice** – Select **Yes** to allow users to pay one or more free text-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="6358e-112">**Projectfactuur**: selecteer **Ja** om gebruikers in staat te stellen een of meer projectfacturen in één POS-transactie te betalen.</span><span class="sxs-lookup"><span data-stu-id="6358e-112">**Project invoice** – Select **Yes** to allow users to pay one or more project-based invoices in a single POS transaction.</span></span>
    - <span data-ttu-id="6358e-113">**Verkooporder - Creditnota**: selecteer **Ja** om gebruikers in staat te stellen meerdere creditnota's op basis van verkooporders te vereffenen op basis van openstaande facturen of om een restitutie aan de klant te verwerken voor een openstaande creditnota.</span><span class="sxs-lookup"><span data-stu-id="6358e-113">**Sales order credit note** – Select **Yes** to allow users to settle multiple sales order-based credit notes against open invoices or process a refund to the customer for an open credit note.</span></span>

> [!NOTE]
> <span data-ttu-id="6358e-114">De betaling of vereffening van gedeeltelijke bedragen wordt nog niet ondersteund.</span><span class="sxs-lookup"><span data-stu-id="6358e-114">Payment or settlement of partial amounts is not yet supported.</span></span>
