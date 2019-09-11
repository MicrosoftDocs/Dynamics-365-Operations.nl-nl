---
title: Nummerreeksen instellen met een wizard
description: In dit onderwerp wordt uitgelegd hoe u alle vereiste nummerreeksen tegelijkertijd instelt met behulp van een wizard.
author: sericks007
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceWizard
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f97c4cd6cdb117ebdd67a155478bb6f8d1703541
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867384"
---
# <a name="set-up-number-sequences-using-a-wizard"></a><span data-ttu-id="b56b4-103">Nummerreeksen instellen met een wizard</span><span class="sxs-lookup"><span data-stu-id="b56b4-103">Set up number sequences using a wizard</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b56b4-104">Nummerreeksen worden gebruikt om leesbare, unieke identificaties te maken voor hoofdgegevensrecords en transactierecords die deze nodig hebben.</span><span class="sxs-lookup"><span data-stu-id="b56b4-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require them.</span></span> <span data-ttu-id="b56b4-105">Een hoofdgegevens- of transactieregistratie die een identificatie nodig heeft wordt een verwijzing genoemd.</span><span class="sxs-lookup"><span data-stu-id="b56b4-105">A master data or transaction record that requires an identifier is referred to as a reference.</span></span> <span data-ttu-id="b56b4-106">Voordat u nieuwe registraties voor een verwijzing kunt maken, moet u een nummerreeks instellen en deze aan de verwijzing koppelen.</span><span class="sxs-lookup"><span data-stu-id="b56b4-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="b56b4-107">In dit onderwerp wordt uitgelegd hoe u alle vereiste nummerreeksen tegelijkertijd instelt met behulp van een wizard.</span><span class="sxs-lookup"><span data-stu-id="b56b4-107">This topic explains how to set up all required number sequences at the same time by using a wizard.</span></span> <span data-ttu-id="b56b4-108">Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.</span><span class="sxs-lookup"><span data-stu-id="b56b4-108">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="b56b4-109">Ga naar **Navigatiedeelvenster > Modules > Organisatiebeheer > Nummerreeksen > Nummerreeksen**.</span><span class="sxs-lookup"><span data-stu-id="b56b4-109">Go to **Navigation > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="b56b4-110">Selecteer **Genereren**.</span><span class="sxs-lookup"><span data-stu-id="b56b4-110">Select **Generate**.</span></span>
3. <span data-ttu-id="b56b4-111">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="b56b4-111">Select **Next**.</span></span>

   - <span data-ttu-id="b56b4-112">Op deze pagina kunt u de identificatiecode, de laagste waarde en de hoogste waarde wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b56b4-112">On this page, you can modify the identification code, the lowest value, and the highest value.</span></span> <span data-ttu-id="b56b4-113">Bovendien kunt u aangeven of de nummerreeks moet doorlopen.</span><span class="sxs-lookup"><span data-stu-id="b56b4-113">In addition, you can indicate whether the number sequence must be continuous.</span></span>   
   - <span data-ttu-id="b56b4-114">Selecteer de optie **Continu** niet als u vooraf nummers moet toewijzen voor de nummerreeks.</span><span class="sxs-lookup"><span data-stu-id="b56b4-114">Do not select the **Continuous** option if you must preallocate numbers for the number sequence.</span></span> <span data-ttu-id="b56b4-115">Om een bereiksegment toe te voegen aan de notatie van een nummerreeks selecteert u de notatie in de lijst en vervolgens **Bereik opnemen in notatie**.</span><span class="sxs-lookup"><span data-stu-id="b56b4-115">To add a scope segment to the format of a number sequence, select the format in the list, and then select **Include scope in format**.</span></span> <span data-ttu-id="b56b4-116">Om een bereiksegment te verwijderen uit de notatie van een nummerreeks selecteert u de notatie in de lijst en vervolgens **Bereik verwijderen uit notatie**.</span><span class="sxs-lookup"><span data-stu-id="b56b4-116">To remove a scope segment from the format of a number sequence, select the format in the list, and then select **Remove scope from format**.</span></span> <span data-ttu-id="b56b4-117">Om een bereiksegment uit te sluiten bij het automatisch genereren selecteert u de nummerreeks in de lijst en vervolgens **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="b56b4-117">To exclude a number sequence from automatic generation, select the number sequence in the list, and then select **Delete**.</span></span>  

4. <span data-ttu-id="b56b4-118">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="b56b4-118">Select **Next**.</span></span>
5. <span data-ttu-id="b56b4-119">Selecteer **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="b56b4-119">Select **Finish**.</span></span>

