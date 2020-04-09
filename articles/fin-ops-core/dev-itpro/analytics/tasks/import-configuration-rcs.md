---
title: (ER) Configuraties importeren uit RCS
description: Dit onderwerp biedt informatie over de manier waarop een gebruiker een nieuwe versie van een ER‑configuratie kan importeren uit RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea2bfd2514be666d05165410ca27041a86464715
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143218"
---
# <a name="er-import-configurations-from-rcs"></a><span data-ttu-id="89530-103">(ER) Configuraties importeren uit RCS</span><span class="sxs-lookup"><span data-stu-id="89530-103">(ER) Import configurations from RCS</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="89530-104">In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe versie van een ER-configuratie uit Microsoft Regulatory Configuration Service (RCS) kan importeren.</span><span class="sxs-lookup"><span data-stu-id="89530-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can import a new version of an Electronic reporting (ER) configuration from Microsoft Regulatory Configuration Services (RCS).</span></span> <span data-ttu-id="89530-105">In dit voorbeeld selecteert u de versie van de ER‑configuratie die is geconfigureerd in een RCS‑exemplaar en importeert u deze in het huidige exemplaar voor voorbeeldbedrijf Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd omdat ER‑configuraties tussen bedrijven worden gedeeld.</span><span class="sxs-lookup"><span data-stu-id="89530-105">In this example, you will select the version of the ER configuration that has been configured in an RCS instance and import it into the current instance for sample company, Litware, Inc. These steps can be performed in any company because ER configurations are shared among companies.</span></span> <span data-ttu-id="89530-106">Als u deze stappen wilt uitvoeren, moet u eerst de stappen voltooien in het onderwerp [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="89530-106">To complete these steps, you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="89530-107">Als u deze stappen wilt voltooien, moet u ook toegang hebben tot een RCS‑exemplaar met minimaal één ER‑configuratie in de status **Voltooid** of **Gedeeld**.</span><span class="sxs-lookup"><span data-stu-id="89530-107">To complete these steps, you must also have access to an RCS instance containing at least one ER configuration in either **Completed** or **Shared** status.</span></span>

1. <span data-ttu-id="89530-108">Ga naar **Organisatiebeheer** > **Werkruimten** > **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="89530-108">Go to **Organization administration** > **Workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="89530-109">Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**.</span><span class="sxs-lookup"><span data-stu-id="89530-109">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="89530-110">Als u deze configuratieprovider niet ziet, voltooit u de stappen in het onderwerp [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="89530-110">If you don't see this configuration provider, complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 
3. <span data-ttu-id="89530-111">Als u geen RCS-omgeving hebt ingericht voor uw bedrijf, klik dan op de link **Regulatory services ‑ Configuratie** en volg de instructies om een RCS-omgeving in te richten.</span><span class="sxs-lookup"><span data-stu-id="89530-111">If you have no RCS environment provisioned to your company, click **Regulatory services – Configuration** external link and follow the instructions to provision an RCS environment.</span></span> 
4. <span data-ttu-id="89530-112">Klik op **Parameters elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="89530-112">Click **Electronic reporting parameters**.</span></span> 
5. <span data-ttu-id="89530-113">Klik op het tabblad **RCS**.</span><span class="sxs-lookup"><span data-stu-id="89530-113">Click the **RCS** tab.</span></span> 
6. <span data-ttu-id="89530-114">Als de RCS-omgeving al is ingericht voor uw bedrijf, gebruikt u de weergave op de pagina met url's om deze te openen.</span><span class="sxs-lookup"><span data-stu-id="89530-114">If RCS environment has been already provisioned to your company, use presented on the page URLs to access it.</span></span> 
7. <span data-ttu-id="89530-115">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="89530-115">Close the page.</span></span> 

## <a name="register-a-new-er-repository"></a><span data-ttu-id="89530-116">Een nieuwe ER‑opslagplaats registreren.</span><span class="sxs-lookup"><span data-stu-id="89530-116">Register a new ER repository.</span></span> 
1. <span data-ttu-id="89530-117">Markeer in de lijst de geselecteerde rij.</span><span class="sxs-lookup"><span data-stu-id="89530-117">In the list, mark the selected row.</span></span> 
2. <span data-ttu-id="89530-118">Selecteer Litware, Inc. provider.</span><span class="sxs-lookup"><span data-stu-id="89530-118">Select Litware, Inc. provider.</span></span> 
3. <span data-ttu-id="89530-119">Klik op Opslagplaatsen.</span><span class="sxs-lookup"><span data-stu-id="89530-119">Click Repositories.</span></span> 
4. <span data-ttu-id="89530-120">Klik op Toevoegen om het dialoogvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="89530-120">Click Add to open the drop dialog.</span></span> 
5. <span data-ttu-id="89530-121">Selecteer 'RCS' in het veld Type opslagplaats van configuratie.</span><span class="sxs-lookup"><span data-stu-id="89530-121">In the Configuration repository type field, enter 'RCS'.</span></span> 
6. <span data-ttu-id="89530-122">Klik op Opslagplaats maken.</span><span class="sxs-lookup"><span data-stu-id="89530-122">Click Create repository.</span></span> 
7. <span data-ttu-id="89530-123">Typ of selecteer een waarde in het veld RCS‑omgeving weergavenaam.</span><span class="sxs-lookup"><span data-stu-id="89530-123">In the RCS environment display name field, enter or select a value.</span></span> 
8. <span data-ttu-id="89530-124">Selecteer het gewenste RCS-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="89530-124">Select the desired RCS instance.</span></span> <span data-ttu-id="89530-125">U kunt er ook meerdere hebben.</span><span class="sxs-lookup"><span data-stu-id="89530-125">Note that you can have several of them.</span></span> 
9. <span data-ttu-id="89530-126">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="89530-126">Click OK.</span></span> 

## <a name="import-er-configurations-from-rcs-based-repository"></a><span data-ttu-id="89530-127">ER-configuraties downloaden uit de RCS-gebaseerde opslagplaats</span><span class="sxs-lookup"><span data-stu-id="89530-127">Import ER configurations from RCS based repository</span></span>
1. <span data-ttu-id="89530-128">Klik op **Filters weergeven**.</span><span class="sxs-lookup"><span data-stu-id="89530-128">Click **Show filters**.</span></span> 
2. <span data-ttu-id="89530-129">Voer een filterwaarde van 'RCS' in het veld **Naam** met gebruik van de de filteroperator **begint met**.</span><span class="sxs-lookup"><span data-stu-id="89530-129">Enter a filter value of "RCS" on the **Name** field using the **begins with** filter operator.</span></span> 
3. <span data-ttu-id="89530-130">Wanneer u de geselecteerde opslagplaats opent, op de pagina **Verbinden met Regulatory Configuration Services** klik dan op de link **Klik hier om verbinding te maken met de Regulatory Configuration Services**.</span><span class="sxs-lookup"><span data-stu-id="89530-130">When you open the selected repository, on the **Connect to Regulatory Configuration Services** page, click **Click here to connect to Regulatory Configuration Services** link.</span></span> 
4. <span data-ttu-id="89530-131">Klik op **Openen**.</span><span class="sxs-lookup"><span data-stu-id="89530-131">Click **Open**.</span></span> 
5. <span data-ttu-id="89530-132">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="89530-132">Click **Close**.</span></span> 
6. <span data-ttu-id="89530-133">Selecteer de gewenste versie van de ER‑configuratie en Klik op **Importeren** om deze in het huidige exemplaar te plaatsen.</span><span class="sxs-lookup"><span data-stu-id="89530-133">Select the desired version of ER configuration and click **Import** to bring it in the current instance.</span></span>

