---
title: Overzicht van gepersonaliseerde productaanbevelingen
description: Dit onderwerp bevat informatie over de Dynamics 365 for Retail-productaanbevelingen die kunnen worden weergegeven op het POS-apparaat (Point Of Sale).
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 259664
ms.assetid: 5dd8db08-cd96-4f7e-9e65-b05ca815d580
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 16bdf2176869e5822ddf8732c829b65f1e60632c
ms.openlocfilehash: ce91f675082a34bd5a1e88be7a7af6884dc47add
ms.contentlocale: nl-nl
ms.lasthandoff: 02/07/2018

---

# <a name="personalized-product-recommendations-overview"></a><span data-ttu-id="d19a2-103">Overzicht van gepersonaliseerde productaanbevelingen</span><span class="sxs-lookup"><span data-stu-id="d19a2-103">Personalized product recommendations overview</span></span>

[!include[banner](includes/banner.md)]


> [!NOTE]
> <span data-ttu-id="d19a2-104">We verwijderen de huidige versie van de productaanbevelingsservice aangezien we deze opnieuw willen ontwerpen met een beter algoritme en nieuwe mogelijkheden voor detailhandelaren.</span><span class="sxs-lookup"><span data-stu-id="d19a2-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="d19a2-105">Zie voor meer informatie [Verwijderde of verouderde functies](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="d19a2-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span> 

<span data-ttu-id="d19a2-106">In Dynamics 365 for Retail kunnen productaanbevelingen op het POS-apparaat (Point of Sale) worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="d19a2-106">In Dynamics 365 for Retail, product recommendations can be displayed on the point of sale (POS) device.</span></span> <span data-ttu-id="d19a2-107">Aanbevelingen zijn items waarin uw klanten mogelijk geïnteresseerd zijn op basis van hun inkoophistorie, items in hun verlanglijst en items die andere klanten online en in fysieke winkels hebben gekocht.</span><span class="sxs-lookup"><span data-stu-id="d19a2-107">The recommendations are items that the customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="d19a2-108">Voor detailhandelaren met grote catalogi helpen aanbevelingen de klant producten te ontdekken.</span><span class="sxs-lookup"><span data-stu-id="d19a2-108">For retailers with large catalogs, recommendations help the customer with product discovery.</span></span> <span data-ttu-id="d19a2-109">Door producten te belichten die zijn gericht op de interesses van een klant en diens koopgewoontes, kunnen productaanbevelingen detailhandelaren helpen met bij- en meerverkoop en klantenbinding.</span><span class="sxs-lookup"><span data-stu-id="d19a2-109">By showcasing products targeted to a customer’s interests and buying habits, product recommendations can help retailers with up-sell and cross-sell, and can enhance customer retention.</span></span> <span data-ttu-id="d19a2-110">Productaanbevelingen worden in Dynamics 365 for Retail aangestuurd door cognitieve services en Microsoft Azure Machine Learning.</span><span class="sxs-lookup"><span data-stu-id="d19a2-110">In Dynamics 365 for Retail, product recommendations are powered by cognitive services and Microsoft Azure machine learning.</span></span>


<a name="scenarios"></a><span data-ttu-id="d19a2-111">Scenario's</span><span class="sxs-lookup"><span data-stu-id="d19a2-111">Scenarios</span></span>
---------

<span data-ttu-id="d19a2-112">Productaanbevelingen zijn ingeschakeld voor de volgende POS-scenario's.</span><span class="sxs-lookup"><span data-stu-id="d19a2-112">Product recommendations are enabled for the following POS scenarios.</span></span> <span data-ttu-id="d19a2-113">Ze zijn beschikbaar in de cloud-POS of Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="d19a2-113">They are available in Cloud POS or Modern POS (MPOS).</span></span>

1.  <span data-ttu-id="d19a2-114">Op de pagina **Productdetails**:</span><span class="sxs-lookup"><span data-stu-id="d19a2-114">On the **Product details** page:</span></span>

-   <span data-ttu-id="d19a2-115">Als een winkelmedewerker een **productdetails**-pagina bezoekt wanneer hij eerdere transacties uit verschillende kanalen bekijkt, stelt de aanbevelingsengine extra artikelen voor die waarschijnlijk samen worden gekocht.</span><span class="sxs-lookup"><span data-stu-id="d19a2-115">If a store associate visits a **Product details** page when looking at previous transactions across different channels, the recommendation engine suggests additional items that are likely to be purchased together.</span></span>
-   <span data-ttu-id="d19a2-116">Als de winkelmedewerker een klant aan de transactie toevoegt en vervolgens een **productdetails**-pagina bezoekt, geeft de aanbevelingsengine persoonlijke aanbevelingen op basis van de transactiehistorie van de klant.</span><span class="sxs-lookup"><span data-stu-id="d19a2-116">If the store associate adds a customer to the transaction and then visits a **Product details** page, the recommendation engine provides personalized recommendations using the customer's transaction history.</span></span>

<span data-ttu-id="d19a2-117">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span><span class="sxs-lookup"><span data-stu-id="d19a2-117">[![proddetails](./media/proddetails.png)](./media/proddetails.png)</span></span>

2.  <span data-ttu-id="d19a2-118">Op de pagina **Transactie**:</span><span class="sxs-lookup"><span data-stu-id="d19a2-118">On the **Transaction** page:</span></span>

-   <span data-ttu-id="d19a2-119">De aanbevelingsengine stelt artikelen voor op basis van de volledige lijst met artikelen in het winkelmandje.</span><span class="sxs-lookup"><span data-stu-id="d19a2-119">The recommendation engine suggests items based on the entire list of items in the basket.</span></span>
-   <span data-ttu-id="d19a2-120">Als de winkelmedewerker een klant aan de transactie toevoegt, geeft de aanbevelingsengine persoonlijke aanbevelingen op basis van de transactiehistorie van de klant en de lijst met artikelen in het winkelmandje.</span><span class="sxs-lookup"><span data-stu-id="d19a2-120">If the store associate adds a customer to the transaction, the recommendation engine provides personal recommendations using the customer’s transaction history and the list of items in the basket.</span></span>

> [!NOTE]
> <span data-ttu-id="d19a2-121">Om aanbevelingen weer te geven op de pagina **Transactie**, moet de detailhandelaar de schermindeling in Dynamics 365 for Retail bijwerken.</span><span class="sxs-lookup"><span data-stu-id="d19a2-121">To display recommendations on the **Transaction** page, the retailer needs to update the screen layout in Dynamics 365 for Retail.</span></span> <span data-ttu-id="d19a2-122">Het besturingselement **Aanbevelingen** moet aan de pagina **Transactie** worden toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="d19a2-122">The **Recommendations** control must be dropped on to the **Transaction** page.</span></span> <span data-ttu-id="d19a2-123">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span><span class="sxs-lookup"><span data-stu-id="d19a2-123">[![transactionscreenmultipleproductslargemessengersbag-5](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)](./media/transactionscreenmultipleproductslargemessengersbag-5.jpg)</span></span>

3.  <span data-ttu-id="d19a2-124">Op de pagina **Details klant**:</span><span class="sxs-lookup"><span data-stu-id="d19a2-124">On the **Customer details** page:</span></span>
    -   <span data-ttu-id="d19a2-125">De aanbevelingsengine stelt artikelen voor op basis van de gebruikers-id en de artikelen op het wensenlijstje van de klant.</span><span class="sxs-lookup"><span data-stu-id="d19a2-125">The recommendation engine suggests items based on the user ID and items in the customer’s wish list.</span></span>

<span data-ttu-id="d19a2-126">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span><span class="sxs-lookup"><span data-stu-id="d19a2-126">[![customerdetailsrecommendations](./media/customerdetailsrecommendations.png)](./media/customerdetailsrecommendations.png)</span></span>

## <a name="configure-dynamics-365-for-retail-to-enable-pos-recommendations"></a><span data-ttu-id="d19a2-127">Dynamics 365 for Retail configureren voor POS-aanbevelingen</span><span class="sxs-lookup"><span data-stu-id="d19a2-127">Configure Dynamics 365 for Retail to enable POS recommendations</span></span>
<span data-ttu-id="d19a2-128">Ga als volgt te werk om productaanbevelingen te configureren:</span><span class="sxs-lookup"><span data-stu-id="d19a2-128">To set up product recommendations, you need to do the following.</span></span>

1.  <span data-ttu-id="d19a2-129">Controleer of u de juiste **rechtspersoon** hebt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="d19a2-129">Make sure that you have selected the correct **Legal entity**.</span></span>
2.  <span data-ttu-id="d19a2-130">Ga naar **Entiteitopslag**, selecteer **Detailhandelverkoop** en klik vervolgens op **Vernieuwen**.</span><span class="sxs-lookup"><span data-stu-id="d19a2-130">Navigate to **Entity store**, select **Retail sales**, and then click **Refresh**.</span></span> <span data-ttu-id="d19a2-131">Hierdoor worden de demonstratiegegevens (of uw gegevens) uit uw operationele database gebruikt en verplaatst naar de entiteitopslag.</span><span class="sxs-lookup"><span data-stu-id="d19a2-131">This will use the demo data (or your data) from your operational database and move it to Entity store.</span></span>
3.  <span data-ttu-id="d19a2-132">Optioneel: als u aanbevelingen in het transactiescherm wilt weergeven, gaat u naar **Schermindeling**, kiest u de schermindeling, start u **Ontwerper van schermindeling** en plaats u het besturingselement **aanbevelingen** op de gewenste locatie.</span><span class="sxs-lookup"><span data-stu-id="d19a2-132">Optional: To display recommendations on the transaction screen, go to **Screen Layout**, choose your screen layout, launch the **Screen layout designer**, and then drop the **recommendations** control where needed.</span></span>

4.  <span data-ttu-id="d19a2-133">Ga naar **Detailhandelparameters**, selecteer **Machine Learning** en selecteer **Ja** onder **POS-aanbevelingen inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="d19a2-133">Go to **Retail parameters**, select **Machine-learning**, select **Yes** under **Enable POS recommendations**.</span></span>
5.  <span data-ttu-id="d19a2-134">Als u aanbevelingen op POS wilt zien, voert u algemene-configuratietaak **1110** uit.</span><span class="sxs-lookup"><span data-stu-id="d19a2-134">To see recommendations on POS, run global configuration job **1110**.</span></span> <span data-ttu-id="d19a2-135">Om wijzigingen in de ontwerper van de POS-schermindeling door te voeren, voert u afzetkanaalconfiguratietaak **1070** uit.</span><span class="sxs-lookup"><span data-stu-id="d19a2-135">To reflect changes made to POS screen layout designer, run channel configuration job **1070**.</span></span>

## <a name="how-does-it-work"></a><span data-ttu-id="d19a2-136">[]()Hoe functioneert dit?</span><span class="sxs-lookup"><span data-stu-id="d19a2-136">[]()How does it work?</span></span>
<span data-ttu-id="d19a2-137">Wanneer u de **entiteitsopslag** vernieuwt, worden de volgende acties uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d19a2-137">When you refresh the **Entity store** entity, the following actions take place.</span></span>

-   <span data-ttu-id="d19a2-138">Gegevens in de door Cognitieve services vereiste indeling worden opgehaald uit de operationele database Dynamics 365 for Retail en naar de entiteitsopslag gezonden.</span><span class="sxs-lookup"><span data-stu-id="d19a2-138">Data in the format required by the Cognitive services is extracted from the Dynamics 365 for Retail operational database and sent to the Entity store.</span></span>
-   <span data-ttu-id="d19a2-139">De gegevens worden gebruikt door Azure Data Factory (ADF) om de gegevens om de gegevens op te schonen, door middel van Hive-scripts in het kader van de ADF-activiteiten.</span><span class="sxs-lookup"><span data-stu-id="d19a2-139">The data is used by Azure Data Factory (ADF) to cleanse the data using Hive scripts as part of ADF activities.</span></span> <span data-ttu-id="d19a2-140">Opgeschoonde gegevens worden opgeslagen in de blob-opslag.</span><span class="sxs-lookup"><span data-stu-id="d19a2-140">Cleansed data is stored in blob storage.</span></span>
-   <span data-ttu-id="d19a2-141">Gegevens uit de blob-opslag worden gebruikt door de API voor cognitieve services om een aanbevelingsmodel te trainen.</span><span class="sxs-lookup"><span data-stu-id="d19a2-141">Data from blob storage is used by the Cognitive services API to train a recommendation model.</span></span>

<span data-ttu-id="d19a2-142">Wanneer u **Aanbevelingen inschakelen** activeert en de configuratietaken uitvoert, worde de volgende acties uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d19a2-142">When you turn on **Enable recommendations** and run the configuration jobs, the following actions take place.</span></span>

-   <span data-ttu-id="d19a2-143">Modelreferenties en een model-id worden opgehaald in de API en opgeslagen in de operationele database van Dynamics 365 for Retail, in het bestand web.config voor AOS en ook in de detailhandelserver.</span><span class="sxs-lookup"><span data-stu-id="d19a2-143">Model credentials and ID are picked up from the API and stored in the Dynamics 365 for Retail operational database, in the web.config for AOS, and also in the retail server.</span></span>
-   <span data-ttu-id="d19a2-144">Modelreferenties en de model-id worden beschikbaar gesteld aan CRT, zodat aanroepen voor productaanbevelingen vanuit de cloud-POS en MPOS in de online modus kunnen worden gehonoreerd.</span><span class="sxs-lookup"><span data-stu-id="d19a2-144">Model credentials and ID are made available to CRT so that calls for product recommendations from Cloud POS and MPOS in online mode can be honored.</span></span>


<a name="see-also"></a><span data-ttu-id="d19a2-145">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d19a2-145">See also</span></span>
--------

[<span data-ttu-id="d19a2-146">Een besturingselement voor aanbevelingen toevoegen aan de transactiepagina op een POS-apparaat</span><span class="sxs-lookup"><span data-stu-id="d19a2-146">Add a recommendations control to the transaction page on a POS device</span></span>](add-recommendations-control-pos-screen.md)




