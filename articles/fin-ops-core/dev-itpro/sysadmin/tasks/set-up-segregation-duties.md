---
title: Scheiding van taken instellen
description: U kunt regels instellen om taken te scheiden die door verschillende gebruikers moeten worden uitgevoerd.
author: maertenm
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 47747cba7f83d0b43a284750cff232824e00053a
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982401"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="e22cf-103">Scheiding van taken instellen</span><span class="sxs-lookup"><span data-stu-id="e22cf-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e22cf-104">U kunt regels instellen om taken te scheiden die door verschillende gebruikers moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="e22cf-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="e22cf-105">Dit concept wordt scheiding van taken genoemd.</span><span class="sxs-lookup"><span data-stu-id="e22cf-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="e22cf-106">Bijvoorbeeld, u wilt niet dat dezelfde persoon de ontvangst van goederen en het betalingsproces aan de leverancier bevestigt.</span><span class="sxs-lookup"><span data-stu-id="e22cf-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="e22cf-107">Scheiding van taken helpt u het risico van fraude beperken en het helpt u ook fouten of onregelmatigheden te detecteren.</span><span class="sxs-lookup"><span data-stu-id="e22cf-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="e22cf-108">U kunt scheiding van taken ook gebruiken om intern controlebeleid af te dwingen.</span><span class="sxs-lookup"><span data-stu-id="e22cf-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="e22cf-109">Voer de volgende procedure uit om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="e22cf-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="e22cf-110">U moet een systeembeheerder zijn om deze procedure te voltooien.</span><span class="sxs-lookup"><span data-stu-id="e22cf-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="e22cf-111">Het demobedrijf dat wordt gebruikt om deze procedure te maken is DAT.</span><span class="sxs-lookup"><span data-stu-id="e22cf-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="e22cf-112">Ga naar **Navigatievenster > Modules > Systeembeheer > Beveiliging > Scheiding van taken > Regels voor scheiding van taken**.</span><span class="sxs-lookup"><span data-stu-id="e22cf-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="e22cf-113">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="e22cf-113">Click **New**.</span></span>
3. <span data-ttu-id="e22cf-114">Typ een waarde voor de regel in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="e22cf-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="e22cf-115">Klik in het veld **Eerste functie** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e22cf-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e22cf-116">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e22cf-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="e22cf-117">Selecteer de eerste functie die door de regel wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="e22cf-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="e22cf-118">Klik in het veld **Tweede functie** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="e22cf-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="e22cf-119">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="e22cf-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="e22cf-120">Selecteer de tweede functie die door de regel wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="e22cf-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="e22cf-121">Selecteer een optie in het veld **Ernst**.</span><span class="sxs-lookup"><span data-stu-id="e22cf-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="e22cf-122">Selecteer de ernst van het risico dat optreedt wanneer dezelfde gebruiker of rol beide taken uitvoert.</span><span class="sxs-lookup"><span data-stu-id="e22cf-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="e22cf-123">Typ een waarde in het veld **Beveiligingsrisico**.</span><span class="sxs-lookup"><span data-stu-id="e22cf-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="e22cf-124">Voer een omschrijving van het beveiligingsrisico in.</span><span class="sxs-lookup"><span data-stu-id="e22cf-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="e22cf-125">Typ een waarde in het veld **Risicobeperking beveiliging**.</span><span class="sxs-lookup"><span data-stu-id="e22cf-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="e22cf-126">Voer een omschrijving in van de acties die u uitvoert om het beveiligingsrisico te beperken.</span><span class="sxs-lookup"><span data-stu-id="e22cf-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="e22cf-127">Bijvoorbeeld, u kunt het risico beperken door meer gedetailleerde controles van het proces uit te voeren, door een maandelijkse managercontrole uit te voeren of door resources met andere afdelingen te delen.</span><span class="sxs-lookup"><span data-stu-id="e22cf-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="e22cf-128">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="e22cf-128">Click **Save**.</span></span>

