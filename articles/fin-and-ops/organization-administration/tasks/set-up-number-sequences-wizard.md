--- 
title: Nummerreeksen instellen met een wizard
description: Nummerreeksen worden gebruikt om leesbare, unieke identificaties te maken voor hoofdgegevensrecords en transactierecords die deze nodig hebben.
author: sericks007
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 96c1bc711350b447611977c3f2070fbc08fbae0f
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-number-sequences-by-using-a-wizard"></a><span data-ttu-id="8082a-103">Nummerreeksen instellen met een wizard</span><span class="sxs-lookup"><span data-stu-id="8082a-103">Set up number sequences by using a wizard</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8082a-104">Nummerreeksen worden gebruikt om leesbare, unieke identificaties te maken voor hoofdgegevensrecords en transactierecords die deze nodig hebben.</span><span class="sxs-lookup"><span data-stu-id="8082a-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="8082a-105">Een hoofdgegevens- of transactieregistratie die een identificatie nodig heeft wordt een verwijzing genoemd.</span><span class="sxs-lookup"><span data-stu-id="8082a-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="8082a-106">Voordat u nieuwe registraties voor een verwijzing kunt maken, moet u een nummerreeks instellen en deze aan de verwijzing koppelen.</span><span class="sxs-lookup"><span data-stu-id="8082a-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="8082a-107">Deze procedure legt uit hoe u alle vereiste nummerreeksen tegelijkertijd instelt met behulp van een wizard.</span><span class="sxs-lookup"><span data-stu-id="8082a-107">This procedure explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="8082a-108">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="8082a-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="8082a-109">Ga naar Organisatiebeheer > Nummerreeksen > Nummerreeksen.</span><span class="sxs-lookup"><span data-stu-id="8082a-109">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="8082a-110">Klik op Genereren.</span><span class="sxs-lookup"><span data-stu-id="8082a-110">Click Generate.</span></span>
3. <span data-ttu-id="8082a-111">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="8082a-111">Click Next.</span></span>
    * <span data-ttu-id="8082a-112">Op deze pagina kunt u de identificatiecode, de laagste waarde en de hoogste waarde wijzigen.</span><span class="sxs-lookup"><span data-stu-id="8082a-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="8082a-113">Bovendien kunt u aangeven of de nummerreeks moet doorlopen.</span><span class="sxs-lookup"><span data-stu-id="8082a-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
    * <span data-ttu-id="8082a-114">Selecteer de optie Continu niet als u vooraf nummers moet toewijzen voor de nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="8082a-114">Do not select the Continuous option if you must preallocate numbers for the number sequence.</span></span>     <span data-ttu-id="8082a-115">Om een bereiksegment toe te voegen aan de notatie van een nummerreeks selecteert u de notatie in de lijst en klikt u op Bereik opnemen in notatie.</span><span class="sxs-lookup"><span data-stu-id="8082a-115">To add a scope segment to the format of a number sequence, select the format in the list, and then click Include scope in format.</span></span>     <span data-ttu-id="8082a-116">Om een bereiksegment te verwijderen uit de notatie van een nummerreeks selecteert u de notatie in de lijst en klikt u op Bereik verwijderen uit notatie.</span><span class="sxs-lookup"><span data-stu-id="8082a-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then click Remove scope from format.</span></span>     <span data-ttu-id="8082a-117">Om een bereiksegment uit te sluiten bij het automatisch genereren selecteert u de nummerreeks in de lijst en klikt u op Verwijderen.</span><span class="sxs-lookup"><span data-stu-id="8082a-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then click Delete.</span></span>  
4. <span data-ttu-id="8082a-118">Klik op Volgende.</span><span class="sxs-lookup"><span data-stu-id="8082a-118">Click Next.</span></span>
5. <span data-ttu-id="8082a-119">Klik op Voltooien.</span><span class="sxs-lookup"><span data-stu-id="8082a-119">Click Finish.</span></span>


