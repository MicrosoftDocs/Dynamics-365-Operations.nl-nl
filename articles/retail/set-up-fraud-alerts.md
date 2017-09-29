---
title: Fraudewaarschuwingen instellen
description: "Dit onderwerp wordt beschreven hoe u regels instelt om klantenservice medewerkers van potentieel frauduleuze informatie te waarschuwen wanneer bestellingen zijn verwerkt. U kunt speciale codes definiëren die automatisch of handmatig verdachte orders stopzetten."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: nl-nl
ms.lasthandoff: 06/29/2017



---

# <a name="set-up-fraud-alerts"></a><span data-ttu-id="a141a-104">Fraudewaarschuwingen instellen</span><span class="sxs-lookup"><span data-stu-id="a141a-104">Set up fraud alerts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a141a-105">Dit onderwerp wordt beschreven hoe u regels instelt om klantenservice medewerkers van potentieel frauduleuze informatie te waarschuwen wanneer bestellingen zijn verwerkt.</span><span class="sxs-lookup"><span data-stu-id="a141a-105">This topic explains how to set up rules to alert customer service representatives of potentially fraudulent information when orders are processed.</span></span> <span data-ttu-id="a141a-106">U kunt speciale codes definiëren die automatisch of handmatig verdachte orders stopzetten.</span><span class="sxs-lookup"><span data-stu-id="a141a-106">You can define specific codes to use to automatically or manually put suspicious orders on hold.</span></span> 

<span data-ttu-id="a141a-107">Voordat u fraudecontroleregels instelt en gebruikt, moet u fraudecontrole inschakelen en de elementaire fraudecontrolewaarden definiëren in de parameters van het callcenter.</span><span class="sxs-lookup"><span data-stu-id="a141a-107">Before you set up and use fraud checking rules, you must enable fraud checking and define the basic fraud checking values in the call center parameters.</span></span> <span data-ttu-id="a141a-108">Er zijn twee typen frauderegels:</span><span class="sxs-lookup"><span data-stu-id="a141a-108">There are two types of fraud rules:</span></span>

-   <span data-ttu-id="a141a-109">**Statische regels** gebruiken een specifieke waarde, zoals een telefoonnummer dat op de zwarte lijst is geplaatst.</span><span class="sxs-lookup"><span data-stu-id="a141a-109">**Static rules** use a specific value, such as a phone number that has been blacklisted.</span></span>
-   <span data-ttu-id="a141a-110">**Dynamische regels** kunnen worden samengesteld uit variabelen en voorwaarden.</span><span class="sxs-lookup"><span data-stu-id="a141a-110">**Dynamic rules** can be composed from variables and conditions.</span></span>

<span data-ttu-id="a141a-111">Voordat u een dynamische regel maakt, moet u de variabelen en de voorwaarden maken die bepalen op welke producten de regel van toepassing is en wanneer de regel moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="a141a-111">Before you create a dynamic rule, you must create the variables and conditions that define who the rule applies to and when the rule should be applied.</span></span> <span data-ttu-id="a141a-112">U wilt bijvoorbeeld een regel maken om te vereisen dat elke verkooporder die klant 1202 plaatst en die 1.000,00 of meer waard is, in de wachtstand moet worden geplaatst tot de klantbetaling kan worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="a141a-112">For example, you want to create a rule to require that any sales order that customer 1202 places that is worth 1,000.00 or more be put on hold until the customer payment can be verified.</span></span> <span data-ttu-id="a141a-113">In dit geval zijn de variabelen klant 1202 en een ordertotaal van 1,000.00.</span><span class="sxs-lookup"><span data-stu-id="a141a-113">In this case, the variables are customer 1202 and an order total of 1,000.00.</span></span> <span data-ttu-id="a141a-114">De voorwaarde geeft aan dat als klant 1202 een order plaatst en het totale bedrag van de order gelijk is aan of groter is dan 1000,00, de verkooporder in de wachtstand moet worden geplaatst tot
klantbetaling kan worden gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="a141a-114">The condition specifies that if customer 1202 places an order, and the total amount of the order is equal to or more than 1,000.00, the sales order must be put on hold until the customer payment can be verified.</span></span>




