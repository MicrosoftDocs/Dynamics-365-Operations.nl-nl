---
title: Een voorkeurstechnicus instellen
description: U kunt een willekeurige werknemer selecteren als voorkeurstechnicus voor een serviceovereenkomst of serviceorder.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 850d91372fb1a918840ebc316a4479f4a70bdc24
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983128"
---
# <a name="set-up-a-preferred-technician"></a><span data-ttu-id="eea76-103">Een voorkeurstechnicus instellen</span><span class="sxs-lookup"><span data-stu-id="eea76-103">Set up a preferred technician</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="eea76-104">U kunt een willekeurige werknemer selecteren als voorkeurstechnicus voor een serviceovereenkomst of serviceorder.</span><span class="sxs-lookup"><span data-stu-id="eea76-104">You can select any worker as a preferred technician for a service agreement or service order.</span></span> <span data-ttu-id="eea76-105">Het is echter een goed idee om de werknemer toe te voegen aan het relevante verzendteam zodat de werknemer is opgenomen op het **Verzendgroep**.</span><span class="sxs-lookup"><span data-stu-id="eea76-105">However, it is a good idea to add the worker to the appropriate dispatch team so that the worker is included on the **Dispatch board**.</span></span>

## <a name="assign-employee-to-a-dispatch-team"></a><span data-ttu-id="eea76-106">Een werknemer toewijzen aan een verzendteam</span><span class="sxs-lookup"><span data-stu-id="eea76-106">Assign employee to a dispatch team</span></span>

1.  <span data-ttu-id="eea76-107">Klik op **Human resources** \> **Algemeen** \> **Medewerkers** \> **Medewerkers**.</span><span class="sxs-lookup"><span data-stu-id="eea76-107">Click **Human resources** \> **Common** \> **Workers** \> **Workers**.</span></span> <span data-ttu-id="eea76-108">Dubbelklik op een werknemer om de detailpagina van de werknemer te openen.</span><span class="sxs-lookup"><span data-stu-id="eea76-108">Double-click a worker to open the worker details page.</span></span> <span data-ttu-id="eea76-109">Klik in het **Actievenster** op **Instellen** \> **Verzendteam** om het formulier **Verzendmedewerkers** te openen.</span><span class="sxs-lookup"><span data-stu-id="eea76-109">On the **Action Pane**, click **Setup** \>**Dispatch team** to open the **Dispatch workers** form.</span></span>

2.  <span data-ttu-id="eea76-110">Selecteer in het veld **Verzendteam** het team om toe te wijzen aan de werknemer.</span><span class="sxs-lookup"><span data-stu-id="eea76-110">In the **Dispatch team** field, select the team to assign the worker to.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a><span data-ttu-id="eea76-111">Een voorkeurstechnicus toewijzen aan een serviceovereenkomst</span><span class="sxs-lookup"><span data-stu-id="eea76-111">Assign a preferred technician to a service agreement</span></span>

1.  <span data-ttu-id="eea76-112">Klik op **Servicebeheer** \> **Algemeen** \> **Serviceovereenkomsten** \> **Serviceovereenkomsten**.</span><span class="sxs-lookup"><span data-stu-id="eea76-112">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span> <span data-ttu-id="eea76-113">Dubbelklik op een serviceovereenkomst om het detailformulier te openen.</span><span class="sxs-lookup"><span data-stu-id="eea76-113">Double-click a service agreement to open the details form.</span></span>

2.  <span data-ttu-id="eea76-114">Selecteer op het tabblad **Algemeen** het veld **Voorkeurstechnicus** en selecteer vervolgens een lid van het relevante verzendteam als de voorkeurstechnicus voor de serviceovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="eea76-114">On the **General** tab, select the **Preferred technician** field, and then select a member of the appropriate dispatch team as the preferred technician for the service agreement.</span></span>

## <a name="assign-a-preferred-technician-to-a-service-order"></a><span data-ttu-id="eea76-115">Een voorkeurstechnicus toewijzen aan een serviceorder</span><span class="sxs-lookup"><span data-stu-id="eea76-115">Assign a preferred technician to a service order</span></span>

1.  <span data-ttu-id="eea76-116">Klik op **Servicebeheer** \> **Periodiek** \> **Verzendbord**.</span><span class="sxs-lookup"><span data-stu-id="eea76-116">Click **Service management** \> **Periodic** \> **Dispatch board**.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="eea76-117">Geef in het formulier <STRONG>Verzendbord</STRONG> een datumbereik op voor de verzendactiviteiten die u wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="eea76-117">In the <STRONG>Dispatch board</STRONG> form, specify a date range for dispatch activities to view.</span></span> <span data-ttu-id="eea76-118">Geef ook op of afgesloten activiteiten moeten worden weergegeven en of de lijst met verzendactiviteiten moet worden beperkt tot teams waartoe u behoort of waarvoor u bevoegd bent om deze te controleren.</span><span class="sxs-lookup"><span data-stu-id="eea76-118">Also, specify whether to display closed activities and whether to limit the dispatch activity list to teams that you belong to or are authorized to monitor.</span></span> <span data-ttu-id="eea76-119">Klik op <STRONG>OK</STRONG> om het formulier <STRONG>Verzendbord</STRONG> te openen.</span><span class="sxs-lookup"><span data-stu-id="eea76-119">Click <STRONG>OK</STRONG> to open the <STRONG>Dispatch board</STRONG>.</span></span></P>



2.  <span data-ttu-id="eea76-120">Selecteer de regel van de te wijzigen serviceactiviteit.</span><span class="sxs-lookup"><span data-stu-id="eea76-120">Select the line of the service activity to modify.</span></span>

3.  <span data-ttu-id="eea76-121">Gebruik op het tabblad **Verwant** de lijst **Werknemer** om een lid van het relevante verzendteam toe te wijzen als voorkeurstechnicus voor de servicebeurt.</span><span class="sxs-lookup"><span data-stu-id="eea76-121">On the **Related** tab, use the **Worker** list to assign a member of the appropriate dispatch team as the preferred technician for the service call.</span></span>

## <a name="see-also"></a><span data-ttu-id="eea76-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="eea76-122">See also</span></span>

[<span data-ttu-id="eea76-123">Overzicht van Servicelevelovereenkomsten opstellen en tot stand brengen</span><span class="sxs-lookup"><span data-stu-id="eea76-123">Develop and establish service agreements overview</span></span>](service-agreements.md)

[<span data-ttu-id="eea76-124">Handmatig serviceorders maken</span><span class="sxs-lookup"><span data-stu-id="eea76-124">Create service orders manually</span></span>](create-service-orders-manually.md)

<span data-ttu-id="eea76-125">[Serviceovereenkomsten (formulier)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span><span class="sxs-lookup"><span data-stu-id="eea76-125">[Service agreements (form)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))</span></span>
  


