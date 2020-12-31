---
title: Scheiding van taken instellen
description: U kunt regels instellen om taken te scheiden die door verschillende gebruikers moeten worden uitgevoerd.
author: peakerbl
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysSecSegregationOfDutiesRule
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 57c7c436c91ab11404cac3ea056b028023a0617a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688168"
---
# <a name="set-up-segregation-of-duties"></a><span data-ttu-id="d3c01-103">Scheiding van taken instellen</span><span class="sxs-lookup"><span data-stu-id="d3c01-103">Set up segregation of duties</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d3c01-104">U kunt regels instellen om taken te scheiden die door verschillende gebruikers moeten worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d3c01-104">You can set up rules to separate tasks that must be performed by different users.</span></span> <span data-ttu-id="d3c01-105">Dit concept wordt scheiding van taken genoemd.</span><span class="sxs-lookup"><span data-stu-id="d3c01-105">This concept is named segregation of duties.</span></span> <span data-ttu-id="d3c01-106">Bijvoorbeeld, u wilt niet dat dezelfde persoon de ontvangst van goederen en het betalingsproces aan de leverancier bevestigt.</span><span class="sxs-lookup"><span data-stu-id="d3c01-106">For example, you might not want the same person both to acknowledge the receipt of goods and to process payment to the vendor.</span></span> <span data-ttu-id="d3c01-107">Scheiding van taken helpt u het risico van fraude beperken en het helpt u ook fouten of onregelmatigheden te detecteren.</span><span class="sxs-lookup"><span data-stu-id="d3c01-107">Segregation of duties helps you reduce the risk of fraud, and it also helps you detect errors or irregularities.</span></span> <span data-ttu-id="d3c01-108">U kunt scheiding van taken ook gebruiken om intern controlebeleid af te dwingen.</span><span class="sxs-lookup"><span data-stu-id="d3c01-108">You can also use segregation of duties to enforce internal control policies.</span></span> <span data-ttu-id="d3c01-109">Voer de volgende procedure uit om een regel te maken.</span><span class="sxs-lookup"><span data-stu-id="d3c01-109">Complete the following procedure to create a rule.</span></span> <span data-ttu-id="d3c01-110">U moet een systeembeheerder zijn om deze procedure te voltooien.</span><span class="sxs-lookup"><span data-stu-id="d3c01-110">You must be a system administrator to complete the procedure.</span></span> <span data-ttu-id="d3c01-111">Het demobedrijf dat wordt gebruikt om deze procedure te maken is DAT.</span><span class="sxs-lookup"><span data-stu-id="d3c01-111">The demo data company used to create this procedure is DAT.</span></span> 

1. <span data-ttu-id="d3c01-112">Ga naar **Navigatievenster > Modules > Systeembeheer > Beveiliging > Scheiding van taken > Regels voor scheiding van taken**.</span><span class="sxs-lookup"><span data-stu-id="d3c01-112">Go to **Navigation pane > Modules > System administration > Security > Segregation of duties > Segregation of duties rules**.</span></span>
2. <span data-ttu-id="d3c01-113">Klik op **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="d3c01-113">Click **New**.</span></span>
3. <span data-ttu-id="d3c01-114">Typ een waarde voor de regel in het veld **Naam**.</span><span class="sxs-lookup"><span data-stu-id="d3c01-114">In the **Name** field, type a value for the rule.</span></span>
4. <span data-ttu-id="d3c01-115">Klik in het veld **Eerste functie** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="d3c01-115">In the **First duty** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="d3c01-116">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d3c01-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="d3c01-117">Selecteer de eerste functie die door de regel wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="d3c01-117">Select the first duty that is controlled by the rule.</span></span>
6. <span data-ttu-id="d3c01-118">Klik in het veld **Tweede functie** op de vervolgkeuzeknop om de zoekopdracht te openen.</span><span class="sxs-lookup"><span data-stu-id="d3c01-118">In the **Second duty** field, click the drop-down button to open the lookup.</span></span> 
7. <span data-ttu-id="d3c01-119">Zoek en selecteer de gewenste record in de lijst.</span><span class="sxs-lookup"><span data-stu-id="d3c01-119">In the list, find and select the desired record.</span></span> <span data-ttu-id="d3c01-120">Selecteer de tweede functie die door de regel wordt gecontroleerd.</span><span class="sxs-lookup"><span data-stu-id="d3c01-120">Select the second duty that is controlled by the rule.</span></span>
10. <span data-ttu-id="d3c01-121">Selecteer een optie in het veld **Ernst**.</span><span class="sxs-lookup"><span data-stu-id="d3c01-121">In the **Severity** field, select an option.</span></span> <span data-ttu-id="d3c01-122">Selecteer de ernst van het risico dat optreedt wanneer dezelfde gebruiker of rol beide taken uitvoert.</span><span class="sxs-lookup"><span data-stu-id="d3c01-122">Select the severity of the risk that occurs when the same user or role performs both duties.</span></span>  
11. <span data-ttu-id="d3c01-123">Typ een waarde in het veld **Beveiligingsrisico**.</span><span class="sxs-lookup"><span data-stu-id="d3c01-123">In the **Security risk** field, type a value.</span></span> <span data-ttu-id="d3c01-124">Voer een omschrijving van het beveiligingsrisico in.</span><span class="sxs-lookup"><span data-stu-id="d3c01-124">Enter a description of the security risk.</span></span>  
12. <span data-ttu-id="d3c01-125">Typ een waarde in het veld **Risicobeperking beveiliging**.</span><span class="sxs-lookup"><span data-stu-id="d3c01-125">In the **Security mitigation** field, type a value.</span></span> <span data-ttu-id="d3c01-126">Voer een omschrijving in van de acties die u uitvoert om het beveiligingsrisico te beperken.</span><span class="sxs-lookup"><span data-stu-id="d3c01-126">Enter a description of the actions that you take to mitigate the security risk.</span></span> <span data-ttu-id="d3c01-127">Bijvoorbeeld, u kunt het risico beperken door meer gedetailleerde controles van het proces uit te voeren, door een maandelijkse managercontrole uit te voeren of door resources met andere afdelingen te delen.</span><span class="sxs-lookup"><span data-stu-id="d3c01-127">For example, you can mitigate the risk by conducting more detailed reviews of the process, by conducting a monthly managerial review, or by sharing resources with other departments.</span></span>     
13. <span data-ttu-id="d3c01-128">Klik op **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="d3c01-128">Click **Save**.</span></span>

