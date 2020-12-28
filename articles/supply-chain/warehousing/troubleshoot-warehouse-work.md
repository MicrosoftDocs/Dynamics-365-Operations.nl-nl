---
title: Problemen met magazijnwerk oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met inkomend magazijnwerk in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a00ae517ff583e4231099d8e9f5d5b5a696cf7f7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645788"
---
# <a name="troubleshoot-warehouse-work"></a><span data-ttu-id="ba817-103">Problemen met magazijnwerk oplossen</span><span class="sxs-lookup"><span data-stu-id="ba817-103">Troubleshoot warehouse work</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba817-104">In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met inkomend magazijnwerk in Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ba817-104">This topic describes how to fix common issues that you might encounter while you work with warehouse work in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a><span data-ttu-id="ba817-105">Ik kan geen nummerplaten met serienummerartikelen verplaatsen als een lege uitgifte en een lege ontvangst zijn toegestaan in de traceringsdimensiegroep.</span><span class="sxs-lookup"><span data-stu-id="ba817-105">I can't move license plates that have serial number items when blank issue and blank receipt are allowed on the tracking dimension group.</span></span>

### <a name="issue-description"></a><span data-ttu-id="ba817-106">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="ba817-106">Issue description</span></span>

<span data-ttu-id="ba817-107">U kunt een nummerplaat niet verplaatsen via een menuopdracht **Verplaatsing** als het serienummer instellingen heeft van *Lege uitgifte is toegestaan* en *Lege ontvangst toegestaan* in de traceringsdimensiegroep en als er meerdere nummerplaten op dezelfde locatie zijn, waarvan sommige serienummers hebben en andere niet.</span><span class="sxs-lookup"><span data-stu-id="ba817-107">You can't move a license plate by using a **Movement** menu item if the serial number has settings of *Blank issue allowed* and *Blank receipt allowed* on the tracking dimension group, and if there are multiple license plates in the same location, some of which have serial numbers and some of which don't have them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ba817-108">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="ba817-108">Issue resolution</span></span>

<span data-ttu-id="ba817-109">Dit probleem wordt verholpen door wijzigingen die in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) zijn geïmplementeerd.</span><span class="sxs-lookup"><span data-stu-id="ba817-109">This issue will be fixed by changes that are deployed in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687).</span></span> <span data-ttu-id="ba817-110">Deze wijzigingen maken het veld **Serienummer** optioneel als lege ontvangst en lege uitgifte zijn toegestaan.</span><span class="sxs-lookup"><span data-stu-id="ba817-110">Those changes will make the **Serial number** field optional when blank receipt and blank issue are allowed.</span></span>

## <a name="i-receive-the-following-error-message-in-the-warehouse-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a><span data-ttu-id="ba817-111">Het volgende foutbericht wordt weergegeven in de magazijn-app bij het verwerken van verplaatsingen: "De voorraadeigenaar %1 is niet toegestaan in dit proces."</span><span class="sxs-lookup"><span data-stu-id="ba817-111">I receive the following error message in the warehouse app when I process movements: "The inventory owner %1 is not allowed in this process."</span></span>

### <a name="issue-description"></a><span data-ttu-id="ba817-112">Probleembeschrijving</span><span class="sxs-lookup"><span data-stu-id="ba817-112">Issue description</span></span>

<span data-ttu-id="ba817-113">De traceringsdimensie **Eigenaar** ontbreekt wanneer de magazijn-app wordt gebruikt om verplaatsingen te maken.</span><span class="sxs-lookup"><span data-stu-id="ba817-113">The **Owner** tracking dimension is missing when the warehouse app is used to make movements.</span></span> <span data-ttu-id="ba817-114">Een normaal voorraadoverboekingjournaal van de Supply Chain Management-client lijkt te werken zoals bedoeld en kan alleen worden geboekt als de dimensie **Eigenaar** is ingevuld.</span><span class="sxs-lookup"><span data-stu-id="ba817-114">A regular inventory transfer journal from the Supply Chain Management client appears to work as intended and can be posted only if the **Owner** dimension is filled in.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="ba817-115">Probleemoplossing</span><span class="sxs-lookup"><span data-stu-id="ba817-115">Issue resolution</span></span>

<span data-ttu-id="ba817-116">Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is.</span><span class="sxs-lookup"><span data-stu-id="ba817-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="ba817-117">Momenteel ondersteunt magazijnbeheer alleen voorraad die eigendom is van de rechtspersoon.</span><span class="sxs-lookup"><span data-stu-id="ba817-117">Currently, warehouse management processes support only inventory that is owned by the legal entity.</span></span>
