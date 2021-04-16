---
title: Power Portal gebruiken met het gegevensmodel van partij
description: In dit onderwerp worden de wijzigingen in de Power Portal-webrollen vanwege het partijgegevensmodel in Twee keer wegschrijven beschreven.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833085"
---
# <a name="using-power-portal-with-the-party-data-model"></a><span data-ttu-id="2aa72-103">Power Portal gebruiken met het gegevensmodel van partij</span><span class="sxs-lookup"><span data-stu-id="2aa72-103">Using Power Portal with the Party data model</span></span>

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2aa72-104">Orkestratieversie 2.0.999.0 en hoger van de oplossing Twee keer wegschrijven omvatten wijzigingen in het gegevensmodel voor partijen en het globale adresboek voor de tabellen Rekening en Contactpersoon.</span><span class="sxs-lookup"><span data-stu-id="2aa72-104">The Dual-write application orchestration solution version 2.0.999.0 and later includes data model changes to party and global address book for the Account and Contact tables.</span></span> <span data-ttu-id="2aa72-105">De wijzigingen maken veel-op-veel-relaties mogelijk die geavanceerde bedrijfsscenario's ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="2aa72-105">The changes allow many-to-many relationships that support advanced business scenarios.</span></span> <span data-ttu-id="2aa72-106">Deze wijzigingen worden niet ondersteund door portalwebrollen, inclusief de klantportal, die out-of-the-box worden verzonden of die in uw omgeving bestonden voordat u Twee keer wegschrijven installeerde.</span><span class="sxs-lookup"><span data-stu-id="2aa72-106">These changes are not supported by portal web roles, including the customer portal, that are shipped out-of-the-box or that existed in your environment before you installed dual-write.</span></span> <span data-ttu-id="2aa72-107">Om de webrollen te laten werken zoals verwacht, moet u nieuwe webrollen maken met behulp van het nieuwe gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="2aa72-107">For the web roles to work as expected, you need to create new web roles using the new data model.</span></span> 

<span data-ttu-id="2aa72-108">Samengevat is de manier waarop de tabellen samenwerken gewijzigd, maar de tabelmachtigingen in de klantportal zijn niet gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="2aa72-108">In summary, the way the tables interact has changed, but the table permissions in the customer portal haven't changed.</span></span> <span data-ttu-id="2aa72-109">In dit onderwerp wordt uitgelegd hoe u nieuwe webrollen maakt die werken met het nieuwe geavanceerde gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="2aa72-109">This topic explains how to create new web roles that work with the new advanced data model.</span></span>

<span data-ttu-id="2aa72-110">Dit diagram toont de tabelrelatie **zonder** het gegevensmodel voor partijen en het globale adresboek:</span><span class="sxs-lookup"><span data-stu-id="2aa72-110">This diagram shows the table relationship **without** the party and global address book data model:</span></span>

   ![zonder partijmodel](media/without-party-model.PNG)

<span data-ttu-id="2aa72-112">Dit diagram toont de tabelrelatie **met** het gegevensmodel voor partijen en het globale adresboek:</span><span class="sxs-lookup"><span data-stu-id="2aa72-112">This diagram shows the table relationship **with** the party and global address book data model:</span></span>

   ![met partijmodel](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a><span data-ttu-id="2aa72-114">Een nieuwe tabelmachtiging maken</span><span class="sxs-lookup"><span data-stu-id="2aa72-114">Create a new table permission</span></span>

<span data-ttu-id="2aa72-115">Voer de volgende stappen uit om deze nieuwe tabelmachtigingen te maken:</span><span class="sxs-lookup"><span data-stu-id="2aa72-115">To create these new table permissions, follow these steps:</span></span>

1. <span data-ttu-id="2aa72-116">Meld u aan bij [Power Apps](https://make.powerapps.com) en ga naar uw apps.</span><span class="sxs-lookup"><span data-stu-id="2aa72-116">Sign in to [Power Apps](https://make.powerapps.com), and go to your apps.</span></span>
2. <span data-ttu-id="2aa72-117">Selecteer uw Portalbeheer-app.</span><span class="sxs-lookup"><span data-stu-id="2aa72-117">Select your Portal Management app.</span></span>
3. <span data-ttu-id="2aa72-118">Selecteer **Beveiliging > Tabelmachtigingen** in de zijbalk.</span><span class="sxs-lookup"><span data-stu-id="2aa72-118">In the side bar, select **Security > Table permissions**.</span></span>

    <span data-ttu-id="2aa72-119">U moet drie nieuwe machtigingen maken:</span><span class="sxs-lookup"><span data-stu-id="2aa72-119">You must create three new permissions:</span></span>

    + <span data-ttu-id="2aa72-120">Verbinding van contactpersoon met partij</span><span class="sxs-lookup"><span data-stu-id="2aa72-120">Contact to Party connection</span></span>
    + <span data-ttu-id="2aa72-121">Verbinding van partij met contactpersoon</span><span class="sxs-lookup"><span data-stu-id="2aa72-121">Party to Account connection</span></span>
    + <span data-ttu-id="2aa72-122">Verbinding van rekening met order</span><span class="sxs-lookup"><span data-stu-id="2aa72-122">Account to Order connection</span></span>

4. <span data-ttu-id="2aa72-123">Maak met de volgende parameters een nieuwe machtiging voor de verbinding van contactpersoon met partij en sla deze op:</span><span class="sxs-lookup"><span data-stu-id="2aa72-123">Create and save a new permission for the Contact to Party connection, setting these parameters:</span></span>

    + <span data-ttu-id="2aa72-124">**Naam**: verbinding van partij met rekening (of uw keuze)</span><span class="sxs-lookup"><span data-stu-id="2aa72-124">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="2aa72-125">**Tabelnaam**: msdyn_contactforparty</span><span class="sxs-lookup"><span data-stu-id="2aa72-125">**Table Name**: msdyn_contactforparty</span></span>
    + <span data-ttu-id="2aa72-126">**Website**: klantportal</span><span class="sxs-lookup"><span data-stu-id="2aa72-126">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="2aa72-127">**Bereik**: contactpersoon</span><span class="sxs-lookup"><span data-stu-id="2aa72-127">**Scope**: Contact</span></span>
    + <span data-ttu-id="2aa72-128">**Bevoegdheden**: alles selecteren</span><span class="sxs-lookup"><span data-stu-id="2aa72-128">**Privileges**: Select all</span></span>
    + <span data-ttu-id="2aa72-129">**Webrollen**: geverifieerde gebruikers, klantvertegenwoordiger (of uw keuze)</span><span class="sxs-lookup"><span data-stu-id="2aa72-129">**Web roles**: Authenticated Users, Customer Representative (or your choice)</span></span>

5. <span data-ttu-id="2aa72-130">Maak met de volgende parameters een nieuwe machtiging voor de verbinding van partij met rekening en sla deze op:</span><span class="sxs-lookup"><span data-stu-id="2aa72-130">Create and save a new permission for the Party to Account connection, setting these parameters:</span></span>

    + <span data-ttu-id="2aa72-131">**Naam**: verbinding van partij met rekening (of uw keuze)</span><span class="sxs-lookup"><span data-stu-id="2aa72-131">**Name**: Party to Account Connection (or your choice)</span></span>
    + <span data-ttu-id="2aa72-132">**Tabelnaam**: rekening</span><span class="sxs-lookup"><span data-stu-id="2aa72-132">**Table Name**: account</span></span>
    + <span data-ttu-id="2aa72-133">**Website**: klantportal</span><span class="sxs-lookup"><span data-stu-id="2aa72-133">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="2aa72-134">**Bereik**: bovenliggend</span><span class="sxs-lookup"><span data-stu-id="2aa72-134">**Scope**: Parent</span></span>
    + <span data-ttu-id="2aa72-135">**Bevoegdheden**: alles selecteren</span><span class="sxs-lookup"><span data-stu-id="2aa72-135">**Privileges**: Select all</span></span>
    + <span data-ttu-id="2aa72-136">**Machtiging bovenliggende tabel**: verbinding van contactpersoon met partij</span><span class="sxs-lookup"><span data-stu-id="2aa72-136">**Parent Table Permission**: Contact to Party Connection</span></span>

6. <span data-ttu-id="2aa72-137">Maak met de volgende parameters een nieuwe machtiging voor de verbinding van rekening met order en sla deze op:</span><span class="sxs-lookup"><span data-stu-id="2aa72-137">Create and save a new permission for the Account to Order connection, setting these parameters:</span></span>

    + <span data-ttu-id="2aa72-138">**Naam**: verbinding van rekening met order (of uw keuze)</span><span class="sxs-lookup"><span data-stu-id="2aa72-138">**Name**: Account to Order Connection (or your choice)</span></span>
    + <span data-ttu-id="2aa72-139">**Tabelnaam**: verkooporder</span><span class="sxs-lookup"><span data-stu-id="2aa72-139">**Table Name**: salesorder</span></span>
    + <span data-ttu-id="2aa72-140">**Website**: klantportal</span><span class="sxs-lookup"><span data-stu-id="2aa72-140">**Website**: Customer Portal</span></span>
    + <span data-ttu-id="2aa72-141">**Bereik**: bovenliggend</span><span class="sxs-lookup"><span data-stu-id="2aa72-141">**Scope**: Parent</span></span>
    + <span data-ttu-id="2aa72-142">**Bevoegdheden**: alles selecteren</span><span class="sxs-lookup"><span data-stu-id="2aa72-142">**Privileges**: Select all</span></span>
    + <span data-ttu-id="2aa72-143">**Machtiging bovenliggende tabel**: verbinding van partij met rekening</span><span class="sxs-lookup"><span data-stu-id="2aa72-143">**Parent Table Permission**: Party to Account Connection</span></span>

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
