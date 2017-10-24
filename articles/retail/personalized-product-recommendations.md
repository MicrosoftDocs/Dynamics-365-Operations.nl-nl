---
title: Overzicht van gepersonaliseerde productaanbevelingen
description: "In Dynamics 365 for Retail kunnen productaanbevelingen op het POS-apparaat (Point of Sale) worden weergegeven. Aanbevelingen zijn items waarin uw klanten mogelijk geïnteresseerd zijn op basis van hun inkoophistorie, items in hun verlanglijst en items die andere klanten online en in fysieke winkels hebben gekocht. Voor detailhandelaren met grote catalogi helpen aanbevelingen de klant producten te ontdekken. Door producten te belichten die zijn gericht op de interesses van een klant en diens koopgewoontes, kunnen productaanbevelingen detailhandelaren helpen met bij- en meerverkoop en klantenbinding. Productaanbevelingen worden in Dynamics 365 for Retail aangestuurd door cognitieve services en Microsoft Azure Machine Learning."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d727718442f94a2a78a3864741e93439d7c36473
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="ccb16-107">Overzicht van gepersonaliseerde productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="ccb16-107">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="ccb16-108">Deze functie is momenteel alleen beschikbaar in sandbox- en productie-implementatietopologieën (hoge beschikbaarheid).</span><span class="sxs-lookup"><span data-stu-id="ccb16-108">This feature is currently available on sandbox and production (high-availability) deployment topologies only.</span></span> 

<span data-ttu-id="ccb16-109">In Dynamics 365 for Retail kunnen productaanbevelingen op het POS-apparaat (Point of Sale) worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ccb16-109">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="ccb16-110">Aanbevelingen zijn items waarin uw klanten mogelijk geïnteresseerd zijn op basis van hun inkoophistorie, items in hun verlanglijst en items die andere klanten online en in fysieke winkels hebben gekocht.</span><span class="sxs-lookup"><span data-stu-id="ccb16-110">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="ccb16-111">Voor detailhandelaren met grote catalogi helpen aanbevelingen de klant producten te ontdekken.</span><span class="sxs-lookup"><span data-stu-id="ccb16-111">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="ccb16-112">Door producten te belichten die zijn gericht op de interesses van een klant en diens koopgewoontes, kunnen productaanbevelingen detailhandelaren helpen met bij- en meerverkoop en klantenbinding.</span><span class="sxs-lookup"><span data-stu-id="ccb16-112">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="ccb16-113">Productaanbevelingen worden in Dynamics 365 for Retail aangestuurd door cognitieve services en Microsoft Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="ccb16-113">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="ccb16-114">Scenario's</span><span class="sxs-lookup"><span data-stu-id="ccb16-114">Scenarios</span></span>
---------

<span data-ttu-id="ccb16-115">Productaanbevelingen zijn ingeschakeld voor de volgende POS-scenario's.</span><span class="sxs-lookup"><span data-stu-id="ccb16-115">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="ccb16-116">Ze zijn beschikbaar in de cloud-POS of Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="ccb16-116">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="ccb16-117">Op de pagina **Productdetails**:</span><span class="sxs-lookup"><span data-stu-id="ccb16-117">On the **Product details** page:</span></span>

-   <span data-ttu-id="ccb16-118">Als een winkelmedewerker een **productdetails**-pagina bezoekt wanneer hij eerdere transacties uit verschillende kanalen bekijkt, stelt de aanbevelingsengine extra artikelen voor die waarschijnlijk samen worden gekocht.</span><span class="sxs-lookup"><span data-stu-id="ccb16-118">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="ccb16-119">Als de winkelmedewerker een klant aan de transactie toevoegt en vervolgens een **productdetails**-pagina bezoekt, geeft de aanbevelingsengine persoonlijke aanbevelingen op basis van de transactiehistorie van de klant.</span><span class="sxs-lookup"><span data-stu-id="ccb16-119">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="ccb16-120">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="ccb16-120">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="ccb16-121">Op de pagina **Transactie**:</span><span class="sxs-lookup"><span data-stu-id="ccb16-121">On the **Transaction** page:</span></span>

-   <span data-ttu-id="ccb16-122">De aanbevelingsengine stelt artikelen voor op basis van de volledige lijst met artikelen in het winkelmandje.</span><span class="sxs-lookup"><span data-stu-id="ccb16-122">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="ccb16-123">Als de winkelmedewerker een klant aan de transactie toevoegt, geeft de aanbevelingsengine persoonlijke aanbevelingen op basis van de transactiehistorie van de klant en de lijst met artikelen in het winkelmandje.</span><span class="sxs-lookup"><span data-stu-id="ccb16-123">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="ccb16-124">Om aanbevelingen weer te geven op de pagina **Transactie**, moet de detailhandelaar de schermindeling in Dynamics 365 for Retail bijwerken.</span><span class="sxs-lookup"><span data-stu-id="ccb16-124">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="ccb16-125">Het besturingselement **Aanbevelingen** moet aan de pagina **Transactie** worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="ccb16-125">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="ccb16-126">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="ccb16-126">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="ccb16-127">Op de pagina **Details klant**:</span><span class="sxs-lookup"><span data-stu-id="ccb16-127">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="ccb16-128">De aanbevelingsengine stelt artikelen voor op basis van de gebruikers-id en de artikelen op het wensenlijstje van de klant.</span><span class="sxs-lookup"><span data-stu-id="ccb16-128">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="ccb16-129">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="ccb16-129">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="ccb16-130">Dynamics 365 for Retail configureren voor POS-aanbevelingen</span><span class="sxs-lookup"><span data-stu-id="ccb16-130">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="ccb16-131">Ga als volgt te werk om productaanbevelingen te configureren:</span><span class="sxs-lookup"><span data-stu-id="ccb16-131">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="ccb16-132">Controleer of u de juiste **rechtspersoon** hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="ccb16-132">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="ccb16-133">Ga naar **Entiteitopslag**, selecteer **Detailhandelverkoop** en klik op **Vernieuwen**. Hierdoor worden de demonstratiegegevens (of uw gegevens) uit uw operationele database gebruikt en verplaatst naar de entiteitopslag.</span><span class="sxs-lookup"><span data-stu-id="ccb16-133">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="ccb16-134">Optioneel: als u aanbevelingen in het transactiescherm wilt weergeven, gaat u naar **Schermindeling**, kiest u de schermindeling, start u **Ontwerper van schermindeling** en plaats u het besturingselement **aanbevelingen** op de gewenste locatie.</span><span class="sxs-lookup"><span data-stu-id="ccb16-134">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**,and then drop the **recommendations** control where needed.</span></span>
4.  <span data-ttu-id="ccb16-135">Ga naar **Detailhandelparameters**, selecteer **Machine Learning** en selecteer **Ja** onder **POS-aanbevelingen inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="ccb16-135">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="ccb16-136">Als u aanbevelingen op POS wilt zien, voert u algemene-configuratietaak **1110** uit.</span><span class="sxs-lookup"><span data-stu-id="ccb16-136">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="ccb16-137">Om wijzigingen in de ontwerper van de POS-schermindeling door te voeren, voert u afzetkanaalconfiguratietaak **1070** uit.</span><span class="sxs-lookup"><span data-stu-id="ccb16-137">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="ccb16-138">[]()Hoe functioneert dit?</span><span class="sxs-lookup"><span data-stu-id="ccb16-138">[]()How does it work?</span></span>
<span data-ttu-id="ccb16-139">Wanneer u de **entiteitsopslag** vernieuwt, worden de volgende acties uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ccb16-139">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="ccb16-140">Gegevens in de door Cognitieve services vereiste indeling worden opgehaald uit de operationele database Dynamics 365 for Retail en naar de entiteitsopslag gezonden.</span><span class="sxs-lookup"><span data-stu-id="ccb16-140">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="ccb16-141">De gegevens worden gebruikt door Azure Data Factory (ADF) om de gegevens om de gegevens op te schonen, door middel van Hive-scripts in het kader van de ADF-activiteiten.</span><span class="sxs-lookup"><span data-stu-id="ccb16-141">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="ccb16-142">Opgeschoonde gegevens worden opgeslagen in de blob-opslag.</span><span class="sxs-lookup"><span data-stu-id="ccb16-142">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="ccb16-143">Gegevens uit de blob-opslag worden gebruikt door de API voor cognitieve services om een aanbevelingsmodel te trainen.</span><span class="sxs-lookup"><span data-stu-id="ccb16-143">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="ccb16-144">Wanneer u **Aanbevelingen inschakelen** activeert en de configuratietaken uitvoert, worde de volgende acties uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="ccb16-144">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="ccb16-145">Modelreferenties en een model-id worden opgehaald in de API en opgeslagen in de operationele database van Dynamics 365 for Retail, in het bestand web.config voor AOS en ook in de detailhandelserver.</span><span class="sxs-lookup"><span data-stu-id="ccb16-145">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="ccb16-146">Modelreferenties en de model-id worden beschikbaar gesteld aan CRT, zodat aanroepen voor productaanbevelingen vanuit de cloud-POS en MPOS in de online modus kunnen worden gehonoreerd.</span><span class="sxs-lookup"><span data-stu-id="ccb16-146">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="ccb16-147">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ccb16-147">See also</span></span>
--------

[<span data-ttu-id="ccb16-148">Een besturingselement voor aanbevelingen toevoegen aan de transactiepagina op een POS-apparaat</span><span class="sxs-lookup"><span data-stu-id="ccb16-148">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




