---
title: De functionaliteit van Microsoft Dynamics 365 for Talent uitbreiden
description: Als u Microsoft PowerApps hebt gemaakt, kunt u die toepassingen starten via koppelingen in Microsoft Dynamics 365 for Talent.
author: rschloma
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4befe02a59d0d617f80174e6c7fbcf00db95adb2
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="c17cc-103">De functionaliteit van Microsoft Dynamics 365 for Talent uitbreiden</span><span class="sxs-lookup"><span data-stu-id="c17cc-103">Extend the functionality of Microsoft Dynamics 365 for Talent</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c17cc-104">Als u Microsoft PowerApps hebt gemaakt, kunt u die toepassingen starten via koppelingen in Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="c17cc-104">If you’ve created any Microsoft PowerApps, you can start those applications from links within Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="c17cc-105">Als u toegang tot uw toepassingen wilt instellen, moet u bepaalde informatie instellen in Talent op een configuratiepagina die u opent vanuit het werkgebied **Systeembeheer**.</span><span class="sxs-lookup"><span data-stu-id="c17cc-105">To set up access to your applications, you’ll need to set up some information in Talent on a configuration page that you can open from the **System administration** workspace.</span></span>

## <a name="configuring-embedded-powerapps-within-talent"></a><span data-ttu-id="c17cc-106">Ingesloten PowerApps in Talent configureren</span><span class="sxs-lookup"><span data-stu-id="c17cc-106">Configuring embedded PowerApps within Talent</span></span>
<span data-ttu-id="c17cc-107">Gebruik de pagina **Ingesloten Microsoft PowerApps instellen** om Talent-pagina's te configureren om PowerApps-toepassingen te starten.</span><span class="sxs-lookup"><span data-stu-id="c17cc-107">Use the **Set embedded Microsoft PowerApps** page to configure Talent pages to start PowerApps applications.</span></span> <span data-ttu-id="c17cc-108">U opent de pagina **Ingesloten Microsoft PowerApps instellen** door het werkgebied **Systeembeheer** en vervolgens het tabblad **Koppelingen** te openen en **Microsoft PowerApps** te selecteren in de groep **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="c17cc-108">To open the **Set embedded Microsoft PowerApps** page, open the **System administration** workspace and then open the **Links** tab. Select **Microsoft PowerApps** from the **Setup** group.</span></span> 

<span data-ttu-id="c17cc-109">De volgende gegevens worden ingevoerd of ingesteld op deze pagina:</span><span class="sxs-lookup"><span data-stu-id="c17cc-109">The following information is entered or set on this page:</span></span> 

 -  <span data-ttu-id="c17cc-110">Een beschrijvende naam of id voor elke PowerApps-toepassing.</span><span class="sxs-lookup"><span data-stu-id="c17cc-110">A descriptive name or identifier for each PowerApps application.</span></span>
 -  <span data-ttu-id="c17cc-111">Een unieke id (GUID) voor elke toepassing die u aan een Talent-pagina toevoegt.</span><span class="sxs-lookup"><span data-stu-id="c17cc-111">A unique identifier (GUID) for each application that you add to a Talent page.</span></span> <span data-ttu-id="c17cc-112">De app-id is beschikbaar op de PowerApps-site [powerapps.com](http://powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="c17cc-112">The app ID is available on the PowerApps site, [powerapps.com](http://powerapps.com/).</span></span> 
 -  <span data-ttu-id="c17cc-113">De pagina waarop gebruikers een toepassing of rapport kunnen openen.</span><span class="sxs-lookup"><span data-stu-id="c17cc-113">The page from which users can open an application or report.</span></span> <span data-ttu-id="c17cc-114">Niet alle Talent-pagina's ondersteunen ingesloten PowerApps en Power BI-rapporten.</span><span class="sxs-lookup"><span data-stu-id="c17cc-114">Not all Talent pages support embedded PowerApps and Power BI reports.</span></span> 

 > [!NOTE]
 >  <span data-ttu-id="c17cc-115">Voer in plaats van de weergavenaam die boven aan de pagina wordt weergegeven de interne naam van de pagina in.</span><span class="sxs-lookup"><span data-stu-id="c17cc-115">Enter the internal name of the page, rather than the display name that appears at the top of the page.</span></span> <span data-ttu-id="c17cc-116">U vindt de interne naam door de betreffende pagina te openen en met de rechtermuisknop op de pagina te klikken.</span><span class="sxs-lookup"><span data-stu-id="c17cc-116">To find the internal name, open the page that you need the internal name of, and right-click anywhere on the page.</span></span> <span data-ttu-id="c17cc-117">Wanneer het menu wordt geopend, beweegt u de muisaanwijzer over het item **Formuliergegevens**.</span><span class="sxs-lookup"><span data-stu-id="c17cc-117">When the menu opens, hover over the **Form information** item.</span></span> <span data-ttu-id="c17cc-118">De interne formuliernaam wordt weergegeven naast het item **Formuliergegevens** in het menu.</span><span class="sxs-lookup"><span data-stu-id="c17cc-118">The internal form name is displayed next to the **Form information** item in the menu.</span></span>
 
-   <span data-ttu-id="c17cc-119">Geef op vanuit welk formulierbesturingselement de toepassing contextgegevens kan ophalen.</span><span class="sxs-lookup"><span data-stu-id="c17cc-119">Specify the form control from which the application can retrieve context data.</span></span> <span data-ttu-id="c17cc-120">Een toepassing kan bijvoorbeeld gegevens over een werknemer gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c17cc-120">For example, an application might use data about a worker.</span></span> <span data-ttu-id="c17cc-121">Als u de pagina **Werknemer** invoert in het veld **Context**, wordt de pagina **Werknemer** geopend wanneer u de toepassing start.</span><span class="sxs-lookup"><span data-stu-id="c17cc-121">If you enter the **Worker** page in the **Context** field, the **Worker** page will open when you start the application.</span></span> <span data-ttu-id="c17cc-122">U bent niet verplicht om iets in te voeren in het veld **Context**.</span><span class="sxs-lookup"><span data-stu-id="c17cc-122">An entry in the **Context field** is optional.</span></span> 
-   <span data-ttu-id="c17cc-123">Stel de grootte in van het dialoogvenster waarin de PowerApps-toepassing wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c17cc-123">Set the size of the dialog box on which the PowerApps application will run.</span></span> <span data-ttu-id="c17cc-124">De dialoogvensters worden aangewezen als klein of groot om de gebruikersinterface te optimaliseren wanneer uw toepassing respectievelijk op een telefoon of een groter apparaat wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c17cc-124">The dialog boxes are designated as “small” or “large” to optimize the user interface when your application for running on a phone or a larger device, respectively.</span></span> 


<span data-ttu-id="c17cc-125">U kunt ook opgeven voor welke rechtspersonen een toepassing beschikbaar wordt of u kunt deze beschikbaar maken voor alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="c17cc-125">You can also specify which legal entities an application will be available for, or you can make it available to all your legal entities.</span></span> <span data-ttu-id="c17cc-126">Standaard zijn uw PowerApps-toepassingen beschikbaar voor alle rechtspersonen.</span><span class="sxs-lookup"><span data-stu-id="c17cc-126">By default, your PowerApps applications are available to all legal entities.</span></span>

## <a name="opening-an-application"></a><span data-ttu-id="c17cc-127">Een toepassing openen</span><span class="sxs-lookup"><span data-stu-id="c17cc-127">Opening an application</span></span>
<span data-ttu-id="c17cc-128">Wanneer u ingesloten PowerApps-toepassingen hebt geconfigureerd, worden er koppelingen naar de opgegeven toepassingen toegevoegd aan de pagina's in Talent.</span><span class="sxs-lookup"><span data-stu-id="c17cc-128">When you’ve configured embedded PowerApps applications, links to the applications that you specified will be added to the pages within Talent.</span></span> <span data-ttu-id="c17cc-129">Klik op een koppeling om een toepassing te openen.</span><span class="sxs-lookup"><span data-stu-id="c17cc-129">Click a link to open an application.</span></span> 



