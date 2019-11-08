---
title: Bedrijfsconcept in Common Data Service
description: In dit onderwerp wordt de integratie van bedrijfsgegevens tussen Finance and Operations en Common Data Service beschreven.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa4d54fd7b3ab407751ad6ca1032d742c23eed41
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184526"
---
## <a name="company-concept-in-common-data-service"></a><span data-ttu-id="66ece-103">Bedrijfsconcept in Common Data Service</span><span class="sxs-lookup"><span data-stu-id="66ece-103">Company concept in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="66ece-104">In Finance and Operations is het concept *bedrijf* zowel een juridische constructie als een bedrijfsconstructie.</span><span class="sxs-lookup"><span data-stu-id="66ece-104">In Finance and Operations, the concept of a *company* is both a legal construct and a business construct.</span></span> <span data-ttu-id="66ece-105">Het is ook een beveiligings- en zichtbaarheidsgrens voor gegevens.</span><span class="sxs-lookup"><span data-stu-id="66ece-105">It's also a security and visibility boundary for data.</span></span> <span data-ttu-id="66ece-106">Gebruikers werken altijd in de context van één bedrijf en de meeste gegevens zijn verdeeld per bedrijf.</span><span class="sxs-lookup"><span data-stu-id="66ece-106">Users always work in the context of a single company, and most of the data is striped by company.</span></span>

<span data-ttu-id="66ece-107">Common Data Service heeft geen gelijkwaardig concept.</span><span class="sxs-lookup"><span data-stu-id="66ece-107">Common Data Service doesn't have an equivalent concept.</span></span> <span data-ttu-id="66ece-108">Het concept dat het meest overeenkomt, is *bedrijfseenheid*, wat in de eerste plaats een beveiligings- en zichtbaarheidsgrens is voor gebruikersgegevens.</span><span class="sxs-lookup"><span data-stu-id="66ece-108">The closest concept is *business unit*, which is primarily a security and visibility boundary for user data.</span></span> <span data-ttu-id="66ece-109">Dit concept heeft niet dezelfde juridische of zakelijke implicaties als het bedrijfsconcept.</span><span class="sxs-lookup"><span data-stu-id="66ece-109">This concept doesn't have the same legal or business implications as the company concept.</span></span>

<span data-ttu-id="66ece-110">Omdat bedrijfseenheid en bedrijf geen gelijkwaardige concepten zijn, is het niet mogelijk om een 1:1-toewijzing (één-op-één) tussen beide te forceren met het oog op Common Data Service-integratie.</span><span class="sxs-lookup"><span data-stu-id="66ece-110">Because business unit and company aren't equivalent concepts, it isn't possible to force a one-to-one (1:1) mapping between them for the purpose of Common Data Service integration.</span></span> <span data-ttu-id="66ece-111">Maar omdat gebruikers standaard in de toepassing dezelfde records moeten kunnen zien als in Common Data Service, heeft Microsoft een nieuwe entiteit in Common Data Service geïntroduceerd met de naam cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="66ece-111">However, because users must, by default, be able to see the same records in the application and Common Data Service, Microsoft has introduced a new entity in Common Data Service that is named cdm\_Company.</span></span> <span data-ttu-id="66ece-112">Deze entiteit is gelijk aan de entiteit Bedrijf in de toepassing.</span><span class="sxs-lookup"><span data-stu-id="66ece-112">This entity is equivalent to the Company entity in the application.</span></span> <span data-ttu-id="66ece-113">Om te garanderen dat de zichtbaarheid van records out of the box equivalent is tussen de toepassing en Common Data Service, raden we de volgende instellingen voor Common Data Service-gegevens aan:</span><span class="sxs-lookup"><span data-stu-id="66ece-113">To help guarantee that visibility of records is equivalent between the application and Common Data Service out of the box, we recommend the following setup for data in Common Data Service:</span></span>

+ <span data-ttu-id="66ece-114">Voor elke Finance and Operations-bedrijfsrecord die is ingeschakeld voor Twee keer wegschrijven, wordt een bijbehorende cdm\_Company-record gemaakt.</span><span class="sxs-lookup"><span data-stu-id="66ece-114">For each Finance and Operations Company record that is enabled for dual-write, an associated cdm\_Company record is created.</span></span>
+ <span data-ttu-id="66ece-115">Wanneer een cdm\_Company-record is gemaakt en is ingeschakeld voor Twee keer wegschrijven, wordt er een standaardbedrijfseenheid met dezelfde naam gemaakt.</span><span class="sxs-lookup"><span data-stu-id="66ece-115">When a cdm\_Company record is created and enabled for dual-write, a default business unit is created that has the same name.</span></span> <span data-ttu-id="66ece-116">Hoewel er automatisch een standaardteam voor die bedrijfseenheid wordt gemaakt, wordt de bedrijfseenheid niet gebruikt.</span><span class="sxs-lookup"><span data-stu-id="66ece-116">Although a default team is automatically created for that business unit, the business unit isn't used.</span></span>
+ <span data-ttu-id="66ece-117">Er wordt een afzonderlijk eigenaarsteam gemaakt dat dezelfde naam heeft.</span><span class="sxs-lookup"><span data-stu-id="66ece-117">A separate owner team is created that has the same name.</span></span> <span data-ttu-id="66ece-118">Het wordt ook gekoppeld aan de bedrijfseenheid.</span><span class="sxs-lookup"><span data-stu-id="66ece-118">It's also associated with the business unit.</span></span>
+ <span data-ttu-id="66ece-119">De eigenaar van een record die is gemaakt en twee keer wordt weggeschreven naar Common Data Service, wordt standaard ingesteld op het team 'DW eigenaar' dat is gekoppeld aan de betreffende bedrijfseenheid.</span><span class="sxs-lookup"><span data-stu-id="66ece-119">By default, the owner of any record that is created and dual-written to Common Data Service is set to the "DW Owner" team that is linked to the associated business unit.</span></span>

<span data-ttu-id="66ece-120">In de volgende afbeelding ziet u een voorbeeld van deze gegevensinstelling in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="66ece-120">The following illustration shows an example of this data setup in Common Data Service.</span></span>

![Gegevensinstelling in Common Data Service](media/dual-write-company-1.png)

<span data-ttu-id="66ece-122">Vanwege deze configuratie is elke record die is gerelateerd aan het bedrijf USMF, eigendom van een team dat is gekoppeld aan de bedrijfseenheid USMF in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="66ece-122">Because of this configuration, any record that is related to the USMF company will be owned by a team that is linked to the USMF business unit in Common Data Service.</span></span> <span data-ttu-id="66ece-123">Daarom kunnen gebruikers die toegang hebben tot die bedrijfseenheid via een beveiligingsrol die is ingesteld op zichtbaarheid op bedrijfseenheidsniveau, deze records nu zien.</span><span class="sxs-lookup"><span data-stu-id="66ece-123">Therefore, any user who has access to that business unit through a security role that is set to business unit–level visibility can now see those records.</span></span> <span data-ttu-id="66ece-124">In het volgende voorbeeld ziet u hoe teams kunnen worden gebruikt om de juiste toegang tot deze records te bieden.</span><span class="sxs-lookup"><span data-stu-id="66ece-124">The following example shows how teams can be used to provide the correct access to those records.</span></span>

+ <span data-ttu-id="66ece-125">De rol Verkoopmanager wordt toegewezen aan leden van het team USMF Sales.</span><span class="sxs-lookup"><span data-stu-id="66ece-125">The "Sales Manager" role is assigned to members of the "USMF Sales" team.</span></span>
+ <span data-ttu-id="66ece-126">Gebruikers met de rol Verkoopmanager hebben toegang tot alle accountrecords die lid zijn van dezelfde bedrijfseenheid waarvan ze lid zijn.</span><span class="sxs-lookup"><span data-stu-id="66ece-126">Users who have the "Sales Manager" role can access any account records that are members of the same business unit that they are members of.</span></span>
+ <span data-ttu-id="66ece-127">Het team USMF Sales is gekoppeld aan de bedrijfseenheid USMF die eerder is vermeld.</span><span class="sxs-lookup"><span data-stu-id="66ece-127">The "USMF Sales" team is linked to the USMF business unit that was mentioned earlier.</span></span>
+ <span data-ttu-id="66ece-128">Daarom kunnen leden van het team USMF Sales elk account zien dat eigendom is van de gebruiker USMF DW, die afkomstig zou zijn van de bedrijfsentiteit USMF in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="66ece-128">Therefore, members of the "USMF Sales" team can see any account that is owned by the "USMF DW" user, which would have come from the USMF Company entity in Finance and Operations.</span></span>

![Hoe teams kunnen worden gebruikt](media/dual-write-company-2.png)

<span data-ttu-id="66ece-130">Zoals u in de voorgaande afbeelding kunt zien, is deze 1:1-toewijzing tussen bedrijfseenheid, bedrijf en team slechts een beginpunt.</span><span class="sxs-lookup"><span data-stu-id="66ece-130">As the preceding illustration shows, this 1:1 mapping between business unit, company, and team is just a starting point.</span></span> <span data-ttu-id="66ece-131">In dit voorbeeld wordt in Common Data Service handmatig een nieuwe bedrijfseenheid Europa gemaakt als bovenliggend element voor zowel DEMF als ESMF.</span><span class="sxs-lookup"><span data-stu-id="66ece-131">In this example, a new "Europe" business unit is manually created in Common Data Service as the parent for both DEMF and ESMF.</span></span> <span data-ttu-id="66ece-132">Deze nieuwe bedrijfseenheid in de basismap is niet gerelateerd aan Twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="66ece-132">This new root business unit is unrelated to dual-write.</span></span> <span data-ttu-id="66ece-133">Deze kan echter worden gebruikt om leden van het team EUR Sales toegang te geven tot accountgegevens in zowel DEMF als ESMF, door de zichtbaarheid van gegevens in te stellen op **Bovenliggende/onderliggende bedrijfseenheid** in de bijbehorende beveiligingsrol.</span><span class="sxs-lookup"><span data-stu-id="66ece-133">However, it can be used to give members of the "EUR Sales" team access to account data in both DEMF and ESMF by setting the data visibility to **Parent/Child BU** in the associated security role.</span></span>

<span data-ttu-id="66ece-134">In een laatste onderwerp wordt beschreven hoe Twee keer wegschrijven bepaalt aan welk eigenaarsteam records moeten worden toegewezen.</span><span class="sxs-lookup"><span data-stu-id="66ece-134">A final topic to discuss is how dual-write determines which owner team it should assign records to.</span></span> <span data-ttu-id="66ece-135">Dit gedrag wordt bepaald met het veld **Standaardeigenaarsteam** van de record cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="66ece-135">This behavior is controlled by the **Default owning team** field on the cdm\_Company record.</span></span> <span data-ttu-id="66ece-136">Wanneer een cdm\_Company-record is ingeschakeld voor Twee keer wegschrijven, maakt een invoegtoepassing automatisch de gekoppelde bedrijfseenheid en het eigenaarsteam (als dit nog niet bestaat) en wordt het veld **Standaardeigenaarsteam** ingesteld.</span><span class="sxs-lookup"><span data-stu-id="66ece-136">When a cdm\_Company record is enabled for dual-write, a plug-in automatically creates the associated business unit and owner team (if it doesn't already exist), and sets the **Default owning team** field.</span></span> <span data-ttu-id="66ece-137">De beheerder kan dit veld wijzigen in een andere waarde.</span><span class="sxs-lookup"><span data-stu-id="66ece-137">The admin can change this field to a different value.</span></span> <span data-ttu-id="66ece-138">De beheerder kan het veld echter niet wissen zolang de entiteit is ingeschakeld voor Twee keer wegschrijven.</span><span class="sxs-lookup"><span data-stu-id="66ece-138">However, the admin can't clear the field as long as the entity is enabled for dual-write.</span></span>

![Veld Standaardeigenaarsteam](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a><span data-ttu-id="66ece-140">Bedrijfsstriping en -bootstrapping</span><span class="sxs-lookup"><span data-stu-id="66ece-140">Company striping and bootstrapping</span></span>

<span data-ttu-id="66ece-141">Common Data Service-integratie bewerkstelligt bedrijfspariteit door een bedrijfs-id te gebruiken om gegevens te stripen.</span><span class="sxs-lookup"><span data-stu-id="66ece-141">Common Data Service integration brings company parity by using a company identifier to stripe data.</span></span> <span data-ttu-id="66ece-142">Zoals u in de volgende afbeelding kunt zien, worden alle bedrijfsspecifieke entiteiten uitgebreid zodat ze een N:1-relatie (veel-op-één) hebben met de entiteit cdm\_Company.</span><span class="sxs-lookup"><span data-stu-id="66ece-142">As the following illustration shows, all company-specific entities are extended so that they have a many-to-one (N:1) relationship with the cdm\_Company entity.</span></span>

![N:1-relatie tussen een bedrijfsspecifieke entiteit en de entiteit cdm_Company](media/dual-write-bootstrapping.png)

+ <span data-ttu-id="66ece-144">De waarde voor records wordt alleen-lezen nadat een bedrijf is toegevoegd en opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="66ece-144">For records, after a company is added and saved, the value becomes read-only.</span></span> <span data-ttu-id="66ece-145">Dat betekent dat gebruikers ervoor moeten zorgen dat ze het juiste bedrijf selecteren.</span><span class="sxs-lookup"><span data-stu-id="66ece-145">Therefore, users should make sure that they select the correct company.</span></span>
+ <span data-ttu-id="66ece-146">Alleen records met bedrijfsgegevens komen in aanmerking voor Twee keer wegschrijven tussen de toepassing en Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="66ece-146">Only records that have company data are eligible for dual-write between the application and Common Data Service.</span></span>
+ <span data-ttu-id="66ece-147">Voor bestaande Common Data Service-gegevens zal binnenkort een door de beheerder geleide bootstrap-ervaring beschikbaar zijn.</span><span class="sxs-lookup"><span data-stu-id="66ece-147">For existing Common Data Service data, an admin-led bootstrapping experience will soon be available.</span></span>